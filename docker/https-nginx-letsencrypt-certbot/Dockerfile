FROM node as build-node
WORKDIR /app
COPY ./test-angular-https/ .
RUN npm install
RUN node node_modules/@angular/cli/bin/ng build --prod

FROM staticfloat/nginx-certbot
COPY --from=build-node ./app/dist/test-angular-https/ /usr/share/nginx/html
COPY ./conf.d /etc/nginx/conf.d/
COPY ./nginx.conf /etc/nginx/nginx.conf
EXPOSE 80 443

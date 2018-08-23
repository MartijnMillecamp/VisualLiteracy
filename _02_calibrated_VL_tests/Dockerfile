
# in this folder run:
# docker build -t "augment:VisualLiteracy" .
# docker run --name VisualLiteracy -p 3002:80  -t  "augment:VisualLiteracy"
# with 3002 the fysical port
# http://0.0.0.0:3002/_03_BC/ should work (locally)
# access data
# docker exec -it VisualLiteracy bash
# cd _03_BC/data
# docker cp  VisualLiteracy:/var/www/app/_03_BC/data/  data/


FROM php
ENV APP_DIR /var/www/app
ENV APPLICATION_ENV .
RUN mkdir -p $APP_DIR

COPY _00_static $APP_DIR/_00_static
COPY _03_BC $APP_DIR/_03_BC

WORKDIR $APP_DIR
EXPOSE 80
VOLUME $APP_DIR
CMD ["php", "-S", "0.0.0.0:80"]


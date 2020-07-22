FROM postgres:12 AS extension_builder
RUN apt-get update -y
RUN apt-get install wget -y
RUN wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -
RUN apt-get install postgresql-12-unit -y

FROM postgres:12
COPY --from=extension_builder /usr/lib/postgresql/12/lib /usr/lib/postgresql/12/lib
COPY --from=extension_builder /usr/share/postgresql/12/extension /usr/share/postgresql/12/extension

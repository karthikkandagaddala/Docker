FROM mysql:8.0
# not a human, only for system
RUN adduser -r expense
ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1 \
    MYSQL_USER=expense \
    MYSQL_PASSWORD=ExpenseApp@1 \
    MYSQL_DATABASE=transactions
RUN chown -R expense:expense /var/lib/mysql /var/run/mysqld
COPY Scripts/*.sql /docker-entrypoint-initdb.d/
# Scripts/*.sql:- It will go to Scripts folder and copy the .sql related files into /docker-entrypoint-initdb.d/ --->when ever servr intilization time automatically it will run schema data
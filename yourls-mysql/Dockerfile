FROM mysql:5.7

COPY ./schema.sql.gz /docker-entrypoint-initdb.d/
COPY ./dump.sh /dump.sh

CMD [ "--server-id=1", "--innodb-api-enable-binlog=TRUE", "--gtid-mode=ON", "--enforce-gtid-consistency=ON", "--binlog-checksum=NONE", "--log-slave-updates=ON", "--log-bin=binlog", "--binlog-format=ROW"]

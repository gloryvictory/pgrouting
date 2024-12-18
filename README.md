# pgrouting
Test with installation of PGRouting

tar -xzf pgrouting-3.5.0.tar.gz

cd pgrouting-3.5.0

mkdir build && cd build

export POSTGRESQL_ROOT=/usr/pgsql-version/

export CMAKE_PREFIX_PATH=$POSTGRESQL_ROOT:$CMAKE_PREFIX_PATH

cmake -DPOSTGRESQL_EXECUTABLE=/usr/pgsql-15/bin/pg_config ..

make

sudo make install

sudo systemctl restart postgresql-version

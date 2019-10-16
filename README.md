Debezium on OpenShift


# In postgres need to have replication role for debezium user
# In postgres need to create a publication for the table
# In postgres need to set the wal_level

# https://www.postgresql.org/docs/9.4/runtime-config-wal.html
# This setting it turns out cannot be reloaded. The cluster has to restart
ALTER SYSTEM SET wal_level = logical;
pg_reload_conf()

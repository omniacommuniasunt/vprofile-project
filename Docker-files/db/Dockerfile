# Use the official MySQL image as base
FROM mysql

# Metadata
LABEL "Project"="Vprofile"
LABEL "Author"="Nixx"

# Environment variables
ENV MYSQL_ROOT_PASSWORD="topsecret"
ENV MYSQL_DATABASE="accounts"

# Add SQL script for initialization
ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql

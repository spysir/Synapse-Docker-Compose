# Synapse-Docker-Compose
Matrix Synapse Docker-Compose

1. Update docker-compose.yml
2. docker-compose run --rm -e SYNAPSE_SERVER_NAME=yourdomain.tld -e SYNAPSE_REPORT_STATS=no synapse generate
3. Update ./files/homeserver.yaml
   - Update web_client_location to app.yourdomain.tld (Remember to remove the comment #)
   - Update public_baseurl to matrix.yourdomain.tld (Remember to remove the comment #)
   - Uncomment serve_server_wellknown to enable it and configure https://yourdoman.tld/.well-known/matrix/server for federation
   - Change `pepper` in your password config. Uncomment the setting to enable it.
   - Change the default database from SQLite to PostgreSQL
   - Configure the mail credentials if you have a mail server 
   - Enable `encryption_enabled_by_default_for_room_type` by default
   - Enable redis. Put `redis` as the host instead of `localhost`.
   - Edit whatever else you might want to

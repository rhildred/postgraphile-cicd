# postgraphile-cicd
gitlab, pgadmin, postgraphile ci/cd with docker compose

With many thanks for [this article](https://medium.com/@BuildWithLal/dockerized-gitlab-ci-setting-up-and-connecting-your-gitlab-runner-b810a02e42f2) and [this article](https://www.graphile.org/postgraphile/running-postgraphile-in-docker/)

**NB** Make sure that you block the Administrator user as the password is in the docker-compose.yml and only necessary for creation of a real administrator account.

To make the database run `gitlab-psql`

```sql
-- Create a new user with a password
CREATE USER appuser WITH PASSWORD 'securepassword';

-- Create a new database
CREATE DATABASE appdb;

-- Grant all privileges on the new database to the new user
GRANT ALL PRIVILEGES ON DATABASE appdb TO appuser;
```

Still a work in progress!
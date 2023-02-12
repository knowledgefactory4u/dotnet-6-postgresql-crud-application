# Build REST CRUD APIs with .Net 6 and PostgreSQL

# Local Setup and Run the application

<h2>Create database and table</h2>

```CREATE DATABASE testdb;```
```
CREATE TABLE IF NOT EXISTS public.users
(
    id bigint NOT NULL DEFAULT nextval('users_id_seq'::regclass),
    email character varying(100) COLLATE pg_catalog."default",
    first_name character varying(100) COLLATE pg_catalog."default",
    last_name character varying COLLATE pg_catalog."default",
    CONSTRAINT primary_key_id PRIMARY KEY (id)
)
WITH (
    OIDS = FALSE
)
TABLESPACE pg_default;

ALTER TABLE IF EXISTS public.users
    OWNER to postgres;
```

Download or clone the source code from GitHub to the local machine


You can start the api by running ```dotnet run``` from the command line in the project root folder (where the WebApi.csproj file is located)

OR

You can also start the application in debug mode in Visula Studio by opening the project root folder in Visual Studio and pressing F5 or by selecting Debug -> Start Debugging from the top menu, running in debug mode.




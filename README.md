# School Facility and Equipment Reservation System

## Requirements
- dotnet

## Installation 
1. Request `.env` file for developers or define `SA_PASSWORD` in the `.env` file.
2. Build the program
```
dotnet build
```
3. Run the project
```
dotnet run --project ./SFERS/SFERS.csproj
```

### Database with docker
1. Start and build container 
```
docker compose up --build
```
2. To shutdown
```
docker compose down
```

### Start migrations
1. Request the connection string from the developers
2. Add the user secrets
```
dotnet user-secrets set "ConnectionStrings:SFERS_Db" <connection string>
```
3. Ensure that the container is running
```
docker compose up
```
4. The database is now port forwarded in `localhost:1433`. You can update the db with just
```
dotnet ef database update --project ./SFERS/SFERS.csproj
```
and their respective migration commands
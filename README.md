# Net Core 5 Basic Restull application based on Onion Architecture with Redis Cache

Basic RESTful project based on Onion architecture using Redis Cache.

## Installation

Pretty straightforward, just modify the appsettings.json file located on WebAPI project under Presentation folder by replacing your database connection.

```bash
"ConnectionStrings": {
    "DefaultConnection": "Data Source=YOUR_CONNECTION;Initial Catalog=OnionExampleDb;Integrated Security=True;MultipleActiveResultSets=True",
    "IdentityConnection": "Data Source=YOUR_CONNECTION;Initial Catalog=OnionExampleIdentityDb;Integrated Security=True;MultipleActiveResultSets=True"
  }
```

## Usage

1. Set the WebAPI project as the main project on the presentation folder
2. After changing the connectionString you need to execute a migration, do this by applying the following commands:
```bash
add-migration Initial
update-database
```
3. To run Redis Cache you need to download the latests build by going to this repo: 

```bash
https://github.com/microsoftarchive/redis/releases/tag/win-3.0.504
```

To run redis, just extract the package, then execute redis-server.exe and minimize the window.
You can also  test if redis is running without issues by executing "redis-cli.exe" and sending the command "ping", you should recive "pong" as a response, then close the client window.

```bash
$ redis-cli ping
PONG
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)

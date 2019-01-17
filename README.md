# Speller

Speller is a .NET Core application that implements symmetric spelling algorithm.

## Installation

Use the [.NET Core 2.2+](https://dotnet.microsoft.com/download) to execute this application.

First you should restore all packages which are used by application. Go to the application root and execute.

```bash
dotnet restore
```

Now, you should build your application.

```bash
dotnet build
```

If you would like to execute the Web API application, go to the `Speller.Presentation.Web.Api` project and execute. It will create a self-hosted application.

```bash
dotnet run
```

## Usage

The console application is static. To use it, just run the application.

If you would like to use the Web API application, execute it (check the installation section). Using [Postman](https://www.getpostman.com/) you can send data to the API.

By default, the API is on `/api/speller`.

Using REST, the request will be something like below.

```
POST /api/speller HTTP/1.1
Host: localhost:32768
Content-Type: application/json
{
    "dictionary": [
        "love",
        "kid",
        "card"
    ],
    "words": [
        "ove",
        "car"
    ]
}
```

In `dictionary` array, you are supposed to send the destination words, that is, the words the algorithm will "search".

In `words` array, you are supposed to send the origin words, that is, the words the algorithm will check and validate.

#### Docker support

This project is ready for be executed in (Linux) Docker containers. The provided `Dockerfile` will create the machine and exposes it by port `80`.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://darnley.mit-license.org/)

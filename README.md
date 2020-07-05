# ASPNETSessionStateManagement

> ASP.NET Core Web App Example of Session State usage with Redis Cache

This project is for [ASP.NET Core Web Application Session Stame Management & Redis Implementation](https://medium.com/@kayamuhammet/asp-net-core-web-application-session-state-management-redis-implementation-dec75e0598c2) stories source code.

## Prerequisites

- Redis
- Net Core 3.1
- Docker

## Installation

1. Clone the repo

```sh
git clone https://github.com/muhammetkaya/ASPNETSessionStateManagement.git
```

2. Create Redis instance using Docker

```sh
docker run --name dist-session-container -p 6379:6379 -d redis
```

3. Run project

```sh
dotnet run -p ./dist-session-management/dist-session-management.csproj
```

## Usage example

There are some test key and values on Index Page OnGet Action. When you execute the project index page will add session state to Redis cache. Session states are stored by "Session\_" prefix.

To check keys on Redis execute code below

```sh
KEYS *Session_*
```

If you want to disable Redis cache just remove the AddDistributedRedisCache line in Startup.cs

## About Me

Muhammet Kaya

[LinkedIn](https://www.linkedin.com/in/kayamuhammet/)

[Medium](https://medium.com/@kayamuhammet)

[Github](https://github.com/muhammetkaya)

muhammetkaya3509@hotmail.com

## Contributing

1. Fork it (<https://github.com/yourname/yourproject/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

Copyright [2020][muhammet]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

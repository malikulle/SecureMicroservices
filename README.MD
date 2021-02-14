# Getting started
    -This project is developed by `Mehmet Ali Külle` to understand Microservices architecture with `IdentityServer` and `API Gateway`

## Code Overview
    - `ApiGateway` is Gateway layer. In this layer is communicating other server.
        -`ocelot.json` is the configuration json file.
    - `IdentityServer` is Authentication layer. This layer protect project.
        - `Config.cs`  is the configuration file.
    - `Movies.API` is API project.
    - `Movies.Client` is Client project.

## Project Structure

    - `Movies.Client` is sending request to `ApiGateway` project.
    - `ApiGateway` is sending to request to `Movies.API`. Then result return to again `Movies.Client`.
    - `IdentityServer` project protect routes and generate token to login system.
    - Movies API return Movies like this to table
    ![MoviesAPI](https://github.com/malikulle/ProShop/blob/master/images/1.png?raw=true)
    - Routes are secure with `Identity Server`. `Only Admin Page` is seen and reachable for user who has `admin` role.
    ![MoviesAPI](https://github.com/malikulle/ProShop/blob/master/images/2.png?raw=true)
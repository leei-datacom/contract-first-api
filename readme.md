# Swagger Code Gen

## Installing

To install as a global nodejs package:

npm install @openapitools/openapi-generator-cli -g
openapi-generator-cli version

see https://github.com/OpenAPITools/openapi-generator?tab=readme-ov-file#17---npm for details and other installation approaches.

## Generating Server Side Code

Server side ASP.NET Core generator is called aspnetcore

To get help for the generator options: `openapi-generator-cli config-help -g aspnetcore`

To generate ASP.NET server code: `openapi-generator-cli generate -i leeapi.yaml -g aspnetcore -o .\server --additional-properties aspnetCoreVersion=6.0`

Note the server side generated code will not build if the API definition does not have any schemas defined.  The following line will need to be commented out of the controllers: `//using Org.OpenAPITools.Models;`

To debug in VS Code open the program.cs file and press F5

## Generating Client Side Code

To generate C# client code: `openapi-generator-cli generate -i leeapi.yaml -g csharp -o .\client\csharp --additional-properties targetFramework=net8.0`

See https://openapi-generator.tech/docs/generators/csharp/

To generate Typescript client code: `openapi-generator-cli generate -i leeapi.yaml -g typescript -o .\client\typescript --additional-properties platform=browser`

See https://openapi-generator.tech/docs/generators/typescript/




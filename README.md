Commands Run to Setup Testing Environment:

dotnet new sln -o UnitTestingBasics
cd UnitTestingBasics
dotnet new classlib -o PrimeService
dotnet sln add ./PrimeService/PrimeService.csproj

dotnet new xunit -o PrimeService.Tests
dotnet add ./PrimeService.Tests/PrimeService.Tests.csproj reference ./PrimeService/PrimeService.csproj
dotnet sln add ./PrimeService.Tests/PrimeService.Tests.csproj

Run the tests in ./PrimeService.Tests with:

dotnet test
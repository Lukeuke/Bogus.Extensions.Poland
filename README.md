# Bogus.Extensions.Poland

### API Extension Methods

- using Bogus.Extensions.Poland;
  - Bogus.Person.Pesel() - Polish Personal Identity Number (gender and date of birth are taken from Person)
  - Bogus.Company.Nip() - Polish Tax Identity Number
  - Bogus.Company.Regon(RegonType) - Polish National Business Registry Number


## Description
I'm a big fun of Bogus Faker library
https://github.com/bchavez/Bogus

 That's why I decided to write an extension for Bogus.
  
  
## Get Started
Extensions can be installed using the Nuget package manager or the dotnet CLI.

~~~ 
Install-Package Sulmar.Bogus.Extensions.Poland
~~~

~~~ 
dotnet add package Sulmar.Bogus.Extensions.Poland
~~~

## Usage

~~~ csharp
 var faker = new Faker<Customer>()
                .RuleFor(p => p.FirstName, f => f.Person.FirstName)
                .RuleFor(p => p.BirthDate, f=> f.Person.DateOfBirth)
                .RuleFor(p => p.Pesel, f=> f.Person.Pesel())
                .RuleFor(p => p.Nip, f=> f.Company.Nip())
                .RuleFor(p => p.Regon, f=> f.Company.Regon(RegonType.Regon9));

  var customer = faker.Generate();
~~~ 



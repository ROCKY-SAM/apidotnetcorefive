
C:\Users\sameera> dotnet --info
C:\Users\sameera\Desktop>dotnet new -h
C:\Users\sameera\Desktop\netcore>dotnet new sln
The template "Solution File" was created successfully.

C:\Users\sameera\Desktop\netcore>dotnet new webapi -o API
The template "ASP.NET Core Web API" was created successfully.

Processing post-creation actions...
Running 'dotnet restore' on API\API.csproj...
  Determining projects to restore...
  Restored C:\Users\sameera\Desktop\netcore\API\API.csproj (in 9.22 sec).
Restore succeeded.

C:\Users\sameera\Desktop\netcore>dotnet sln add API
Project `API\API.csproj` added to the solution.

-----------------------------
C#  ms-dotnettools.csharp
c# extention

dotnet run 
dotnet dev-certs https --trust
------------------------------

dotnet watch run

NuGet Gallery
patcx.vscode-nuget-gallery

dotnet tool install --global dotnet-ef --version 5.0.1

dotnet ef migrations add InitialCreate -o Data/Migrations

https://www.nuget.org/packages/dotnet-ef/5.0.3

dotnet ef database update  

SQLite alexcvzz.vscode-sqlite

![Screenshot_2021-02-28 Swagger UI](https://user-images.githubusercontent.com/12700182/109419470-a22ffd80-79f3-11eb-9fbd-7a8a77f40bdd.png)

dotnet ef migrations add UserPasswordAdded
dotnet ef database update

dotnet ef database drop


System.IdentityModel.Tokens.Jwt by Microsoft

Microsoft.AspNetCore.Authentication.JwtBearer

-------------------------------------------
So we've reached the end of Section four, and that's just wrap this up with a summary and take a look

at our learning goals for this particular section.

Now, we've gone ahead and we've implemented basic authentication in our app.

And hopefully we've got an understanding now of how to store passwords in a database.

Now, I often get questions from students about this, certainly around the sorting and the hashing

of the password.

Now, hashing the password is good because it's a one way operation and it means that our password cannot

be read in clear text.

But it's not good enough because there's a thousand different dictionaries out there of all common passwords

and every possible password combination that's already been hashed using multiple different algorithms.

So it's very easy to take a hash and find out what the original password is from these dictionaries.

Salting protects us against that, but it doesn't solve everything.

It does protect against general dictionary attacks on a password.

But it doesn't stop a concerted attack on a single password, it just protects people who have the same

password on multiple machines, but it certainly doesn't make poorly chosen passwords any better.

But we do have passwords stored in our database that are not in clear text.

And we do solve that one problem of protecting against general dictionary attacks.

Having our database compromised is still a very bad thing, and we would still need to tell all of our

users that we've been compromised and they need to change their password everywhere they've used it.

What we've also taken a look at is using inheritance for our base API controller, and this prevents

us typing out repetitive code.

So it's that do not repeat yourself.

Think.

We've also taken a look at using the C sharp debugger, and this can help us see what's going on with

our methods.

Step by step, we can see what values are variables have any given time during a method.

We've also taken a look at data transfer objects and how we can shape the data that we both receive

and also what we return to, the client will enter a look at validation and made sure that we had required

attributes on our toes so that we don't take up bad data.

And we've also taken a look at Jason, Web tokens, these little tokens that we're going to send out

with every authenticated request that we need to make from the client.

And as I mentioned, we don't need to call our database to check that the token is valid because the

API server is going to verify that it's a valid token based on the signature that it's signed it with.

And we also took a look at using services in C Sharp to help us generate the token.

And this keeps our code clean because the service are token service.

It's just got one job.

All it needs to do is generate a token.

It doesn't need to authenticate the user.

It doesn't need to do anything like that.

It's just got a single responsibility of receiving a user and then returning a token.

That's all it does.

And we also took a look at adding the authentication middleware.

And please remember, the ordering of that is always important.

And then we took a look at the extension methods as well, just to tidy up our Start-Up class and keep

our code clean.

So now we've implemented this in the API.

What's coming up next is what we're going to do in the client regarding login and registration.
-------------------------------------------------------


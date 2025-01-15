### The problem

If you install the dotnet SDK in an OSX environment and you want to start writing dotnet based WebAPI projects, for instance, you want to make use of dotnet's EF framework CLI tools.
Generally, after you added your models to your code, you want to create the migration code by executing the following command on your shell:
```
dotnet ef migrations add Init
```
For that, the EF CLI tools need to be installed and they were up to a certain point, but they are not anymore. 
At least at the time of writing this blog post, they are not - maybe Microsoft will add them back at some point.

### The solution

So you need to install them manually[^1], which you will be doing by executing this command:
```
dotnet tool install --global dotnet-ef
```
After that, you can go executing your ef commands.

----
[^1]: Bug report on github: https://github.com/dotnet/AspNetCore.Docs/issues/23414.

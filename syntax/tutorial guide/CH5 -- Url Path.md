# CH5 -- Url Path
## objectives
You will learn

+ why the url path is specified

## CH5.1 -- why the url path is specified
url path is specified according to file structure. 

the file structure will directly reflect to url path.

> [!CAUTION]
> file that will be processed by ASP.NET engine when user browses in webbrowser.
>
> MUST be placed under `~/web` folder 
>
> where
>
> `~` refers the root directory of project (**NOT** the root of solution).

The file structure will directly reflect to url path.

### examples
#### example 1
Assume there are `~\web\Login.aspx`,

The corresponding url

```
<protocal>://<ip-address>:<port>/web/Login.aspx
```

#### example 2
Assume there are `~\web\Cooking\Prepare.aspx`,

The corresponding url

```
<protocal>://<ip-address>:<port>/web/Cooking/Prepare.aspx
```

## reference
### Google Gemini
+ [Google Gemini's response -- How the naming convention is defined?](https://g.co/gemini/share/6df4a3112b83)


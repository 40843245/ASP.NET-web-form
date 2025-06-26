# CH1 -- Page Directives
## objectives
You will learn

+ basic structure of page directives
  
+ meaning page directives

## CH1.1 -- basic structure of page directives

It must be on top of `.aspx` file.

It is enclosed with `<%@` and `%>` 

```
<%@ ... %>
```

## CH1.2 -- meaning page directives

Take page directives of `Login.aspx` for example,

```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Login.aspx.cs" Inherits="Web.Login" %>
```

In this example, we can know that

+ In `Language="C#"`, it indicates that it uses `C#` as programming language

+ In `AutoEventWireup="true"`, `ASP.NET` will automatically attempt to link page events for code-behind file by its naming convention.

> [!IMPORTANT]
> If `AutoEventWireup="false"`, then you need to wire these event up.
>
> that is, you need to define your own method then add the event (with your defined method) to the listener.

+ In `CodeBehind="index.aspx.cs"`

NOT ONLY tells the ASP.NET runtime the name and location of the code-behind file associated with this `.aspx` page

BUT ALSO you will need to write code (in `C#` programming language) in `index.aspx.cs` file 

for handling events, interacting with data, and manipulating the UI elements that is defined in `index.aspx`. 

+ In `Inherits="Web.index"`

It connects the `Login.aspx` page to its code-behind class defined in `Web.index` file.

so that `Login.aspx` page inherits class defined in `Web.index` file.

In `index.aspx.cs` file, you will see like following,

```
namespace Web
{
    public partial class index : System.Web.UI.Page
    {
        // ... your logic about page ...
    }
}
```

When ASP.NET processes the `index.aspx` page, it compiles `index.aspx` into a class that inherits from `Web.index`.

### examples
#### example 1 -- `AutoEventWireup="true"`
If you set `AutoEventWireup="true"`,

There is a `Button` named `Button1`, its callback function of click event is defined in `Button1_Click`.

There is a `Page` named `Page`, its callback function of load event is defined in `Page_Load`.

#### example 2 -- `AutoEventWireup="false"`
If you set `AutoEventWireup="false"`, 

then to add a load event of `Page` instance,

you need to define a `Page_Load` method, 

then add `Page_Load` event to the listener.

`LoadEvent.aspx`

```
public void Page_Init(){
  // ... will be executed iff the initialize the page at startup.
  this.Load += new EventListener(Page_Load);
}

public void Page_Load(){
  // ... executed these code when the event is triggered
}
```

## reference
### Google Gemini
+ [`Google Gemini's response -- What is Page directive in ASP.NET Web Forms`](https://g.co/gemini/share/ab989e640eea)

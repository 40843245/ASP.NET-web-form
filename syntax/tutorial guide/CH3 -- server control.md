# CH3 -- server control
## objectives
You will learn

+ what is server control

+ how to tell ASP.NET engine that these HTML element should be treated as `HTML server control`

## CH3.1 -- what is server control
control is categorized as follows.

+ HTML server controls

HTML elements exposed to the server so you can program them. 

HTML server controls expose an object model that 

maps very closely to the HTML elements that they render.

+ Web server controls

controls with more built-in features than HTML server controls. 

Web server controls include not only form controls such as buttons and text boxes, but also special-purpose controls something

(such as a calendar, menus, and a tree view control). 

Web server controls are more abstract than HTML server controls in that their object model that does not necessarily reflect HTML syntax.

+ Validation controls

enable validation for user inputs when pressing enter key.

+ User controls

controls that you create as ASP.NET Web pages. 

You can embed ASP.NET user controls in other ASP.NET Web pages,

which is an easy way to create toolbars and other reusable elements.

## CH3.2 -- how to tell ASP.NET engine that these HTML element should be treated as `HTML server control`
specifying the attr of `runat` as "server" (runat="server") in `<head>` tag.

For example,

```
<head id="Head1" runat="server">
```

## reference
### MSDS
+ About controls, see [ASP.NET Web Server Controls Overview](https://learn.microsoft.com/en-us/previous-versions/aspnet/zsyt68f1(v=vs.100))
  
### Google Gemini
+ [Google Gemini's response -- What is `runat="server"`](https://g.co/gemini/share/c6d5118e25d7)

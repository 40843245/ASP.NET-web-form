# CH2 -- Document Type Declaration
## objectives
You will learn

+ basic structure of Document Type Declaration

+ meaning of Document Type Declaration

## CH2.1 -- basic structure of Document Type Declaration
+ It MUST be next below to Page Directives

```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Login.aspx.cs" Inherits="Web.Login" %>

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

+ It MUST be enclosed with `<!DOCTYPE` and `>`

followed by either `html` (indicates it will be parsed with rule native html) or `html5` (indicates it will be parsed with rule native html5)

This principle is same as `.html` (html) file.

## CH2.2 -- meaning of Document Type Declaration
### examples
#### example 1
Take it as example,

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

+ In `<!DOCTYPE`, it indicates the startup of a web page.

+ In `html`, the browser will parse this file as parsing html

+ In `PUBLIC`, it indicates the identifier `"-//W3C//DTD XHTML 1.0 Transitional//EN"` is a public indentifier.

+ In `"-//W3C//DTD XHTML 1.0 Transitional//EN"` is a public indentifier.

Here `-` in `-//W3C//DTD`, indicates that this is an unregistered owner identifier.

Here `W3C` identifies W3C (stands for World Wide Web Consortium) is the owner or organization that created and maintains the DTD.

> [!IMPORTANT]
> W3C (stands for World Wide Web Consortium) is the main international standards organization for WWW (stands for World Wide Web).
>
> For more details, see [World Wide Web Consortium](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium)

Here `DTD` states that the identified resource is a DTD (stands for Document Type Definition).

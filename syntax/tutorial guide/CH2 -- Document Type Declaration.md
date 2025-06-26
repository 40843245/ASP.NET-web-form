# CH2 -- Document Type Declaration
## objectives
You will learn

+ basic structure of Document Type Declaration

+ meaning of Document Type Declaration

+ importance of Document Type Declaration for most web development

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

+ In `XHTML 1.0`

It specifies that the document conforms to the `XHTML 1.0` Transitional standard.

+ In `Transitional`

The word is self-explanatory, it is more lenient in the document.

+ In `EN`

It indicates that the `DTD` use English.

+ In `"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"`

A system identifier, which points `"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"` to the document

on the W3C (stands for World Wide Web Consortium) website.

## CH2.3 -- importance of Document Type Declaration for most web development
1. Browser Rendering Mode: The Document Type Declaration (in `<!DOCTYPE`)  tells the browser which rendering mode to use
2. Validation: It allows tools (and theoretically browsers) to validate that your HTML/XHTML.
3. Backward Compatibility: The `Transitional` in "-//W3C//DTD XHTML 1.0 Transitional//EN" indicates that it is more lenient in the document (as we discussed befor),

it is often used for backward compatibity.

## reference
### Google Gemini
+ About `<!DOCTYPE !>`,

    see [Google Gemini's response -- What is `<!DOCTYPE !>`](https://g.co/gemini/share/b90af93ad1c5)

+ About importance of Document Type Declaration for most web development

    see [Google Gemini's response -- importance of Document Type Declaration for most web development](https://g.co/gemini/share/b90af93ad1c5)

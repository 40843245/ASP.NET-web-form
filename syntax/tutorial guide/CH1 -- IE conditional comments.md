# CH1 -- IE conditional comments
## objectives
You will learn

+ what is IE conditional comments

+ syntax of IE conditional comments

+ operators of IE conditional comments

+ examples

+ how to write IE conditional comments

## CH1.1 -- what is IE conditional comments
IE conditional statement in ASP.NET web form is used to check the current version of IE (which is obsolete now)

that is used by user satisfies the IE conditional statement, or check IE is used as current webbrowser. 

> [!CAUTION]
> It is obsolete and only can check current webbrowser is IE or current webbrowser is between IE 5 to IE 9 (BOTH inclusive).
>
> That is, it's impossible to check current webbrowser
>
> which version is less than IE 5 (such as IE 4) and greater than IE 9 (such as IE 10) conditional statement,
>
> apply IE conditional statement to those IE whose version is less than IE 5 (such as IE 4) and greater than IE 9 (such as IE 10) conditional statement and  
>
> For other version, you can get the current of webbrowser in JS.

## CH1.2 -- syntax of IE conditional comments

> [!TIP]
> In html 5, comments are enclosed with `<!--` and `-->`

IE conditional statement is enclosed with these tag:

+ `<!--[if <followed by IE conditional statement>]>`

+ `<![endif]-->`

replace `<followed by IE conditional statement>` to your real IE conditional statement.

Basic format

```
`<!--[if <followed by IE conditional statement>]>`
  <!-- IE conditional comments block -->
<![endif]-->
```

> [!NOTE]
> In standard way, we put **IE** at the begin of IE conditional statement.
>
> such as `<!--[if IE lt 7]>`
> 
> While there are non-standard way -- to put **IE** at the middle of IE conditional statement.
>
> such as `<!--[if lt IE 7]>`
>
> BUT I highly **discourage** it since the behavior of the parser of webbrowser.
>
> The non-standard way might be able to be parsered correct in IE 5 to IE 10 (BOTH inclusive)

> [!CAUTION]
> Forthurmore, they are disallowed to
>
> + put `eq` at the beginning of IE conditional statement followed by **IE** (such as `<!--[if eq IE 7]>`)
>
> + NOT put a conditional statement after negation operator `!` (such as `<!--[if IE(! | gt 6)]>`)

These are equivalent.

```
<!--[if IE gt 8]>
```

and 

```
<!--[if gt IE 8]>
```

Similarly these are equivalent.

```
<!--[if IE (gte 6 & lte 8)]>
```

and 

```
<!--[if (gte IE 6 & lte IE 8)]>
```

## CH1.3 -- operators of IE conditional comments

| symbol or keyword | meaning | example |
| :-- | :-- | :-- |
| `!` | NOT | `<!--[if !IE]>`|
| `eq` | *e*qual *t*o | `<!--[if IE eq 6]>`|
| `gt` | *g*reater *t*han | `<!--[if IE gt 7]>`<br>`<!--[if gt IE 7]>`|
| `lt` | *l*ess *t*han | `<--[if IE lt 8]>` |
| `gte` | *g*reater *t*han or *e*qual to | `<!--[if IE gte 8]>` |
| `lte` | *l*ess *t*han or *e*qual to | `<!--[if IE lte 8]>` |
| enclosed with `(` and `)` | group conditional statement | `<!--[if IE (gte 6 & lte 8)]>`<br>`<!--[if (gte IE 6 & lte IE 8)]>` |
| `&` | logical AND  | `<!--[if IE (gte 6 & lte 8)]>`<br>`<!--[if (gte IE 6 & lte IE 8)]>` |
| `|` | logical OR  | `<!--[if IE (lte 6 |  gt 7)]>`<br>`<!--[if (lte IE 6 & gt IE 7)]>` |

## CH1.4 -- examples
### example 1
```
<!--[if IE gt 7]>
  <p>Hello</p>
<![endif]-->
```

Only when current webbrowser is in IE with version 7 (exclusive) (or above), that is IE x>7, will render `<p>Hello</p>`.

where x is current of IE version.

### example 2
```
<!--[if IE lt 8]>
  <p>Hello</p>
<![endif]-->
```

Only when current webbrowser is in IE with version 8 (exclusive) (or below), that is IE x<8, will render `<p>Hello</p>`.

where x is current of IE version.

### example 3
```
<!--[if IE gte 7]>
  <p>Hello</p>
<![endif]-->
```

Only when current webbrowser is in IE with version 7 (inclusive) (or below), that is IE x>=7, will render `<p>Hello</p>`.

where x is current of IE version.

### example 4
```
<!--[if IE lte 7]>
  <p>Hello</p>
<![endif]-->
```

Only when current webbrowser is in IE with version 7 (inclusive) (or below), that is IE x<=7, will render `<p>Hello</p>`.

where x is current of IE version.

### example 5
```
<!--[if IE (gte 6 & lte 7]>
  <p>Hello</p>
<![endif]-->
```

Only when current webbrowser is in IE with version between 6 (inclusive) and 7 (inclusive), that is IE 6<= x <=7, will render `<p>Hello</p>`.

where x is current of IE version.

### example 6
```
<!--[if IE (lte 6 | gt 7]>
  <p>Hello</p>
<![endif]-->
```

Only when current webbrowser is in IE with version less than 6 (inclusive) or 7 (exclusive), that is IE x<=6 & x>7, will render `<p>Hello</p>`.

where x is current of IE version.

### example 7
```
<!--[if IE]>
  <p>Hello</p>
<![endif]-->
```

Only when current webbrowser is IE, will render `<p>Hello</p>`.

### example 8
```
<!--[if !IE]>
  <p>Hello</p>
<![endif]-->
```

Only when current webbrowser is NOT IE, will render `<p>Hello</p>`.

### example 9
```
<!--[if (!IE |IE gt 6)]>
  <p>Hello</p>
<![endif]-->
```

Only when current webbrowser is NOT IE or IE with version 6 (exclusive), will render `<p>Hello</p>`.

> [!CAUITON]
> About syntax,
> 
> although we say that
>> 
>> we can put **IE** at the begin of IE conditional statement
>>
> However, in this cases, it is disallowed.
>
> The following wrong example
>  
>> ```
>> <!--[if IE(! | gt 6)]>
>>  <p>Hello</p>
>> <![endif]-->
>> ```
>>
>> it is wrong because the negation operator (`!`) does NOT follow any conditions.

## CH1.5 -- how to write IE conditional comments
Step 1: 

write the basic architecture

```
<!--[if ]>
  <!-- IE conditional comments block -->
<![endif]-->
```

Step 2:

Think which content will be used in IE conditional comments block. 

Then express it with html tags.

Step 3:

Think which version will use the html tags IE conditional comments block.

Then express it with a valid IE conditional comments.

For more details about valid operators and valid IE conditional comments, see CH1.2 and CH1.3

Step 4:

Place them together

```
<!--[if <IE conditional statement>]>
  <!-- IE conditional comments block -->
<![endif]-->
```
 
replace `<IE conditional statement>` to  IE conditional statement that you get in Step 3.

replace `<!-- IE conditional comments block -->` to  IE conditional comments block that you get in Step 2.




## reference
### Google Gemini

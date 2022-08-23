
>  use_external_html-in_html

# This repository explains how to include and use external or other html files in your desired html.

How to add html elements form other page to your page.

  

**requirement:** Ash-js directory.

  

**Step 1:**
Go in the html file you want to include external html files to,
lets call it *index.html*



**Step 2:**
Add these scripts in index.html head to include these files from Ash-js directory.
```
<script  src="Ash-js/jquery-Ash.min.js"></script>
<script  src="Ash-js/Ash-import.min.js"></script>
```
  

**Step 3:**
Whereever you want to show external html file into current file, include this div.
```
<div  Ash-import="any.html"  id="any-id"></div>
```
  

**DONE:**

***whereever you placed this div will show the external html file you included with div.***

  
  

> Example-

  

Let, the external file you want to include=
```
a.html=
{
<h1>I am included Page</h1>
}

Output=
I am included Page

  ```
  The file to include external file in=
  ```
index.html=
{
<!DOCTYPE  html>
<html  lang="en">
<head>
<meta  charset="UTF-8">
<meta  http-equiv="X-UA-Compatible"  content="IE=edge">
<meta  name="viewport"  content="width=device-width, initial-scale=1.0">
<title>Document</title>
<script  src="Ash-js/jquery-Ash.min.js"></script>
<script  src="Ash-js/Ash-import.min.js"></script>
</head>
<body>
<h1>I am home Page</h1>
<div  Ash-import="a.html"  id="any-id"></div>
</body>
</html>
}

Output Old=
I am home Page

```
  
```
Output New=
I am included Page
I am home
```

  

***In this way you can include and use external html pages in html file.***

  

## How it Works?

It uses jquery to create a custom attribute,
the included and required jquery is located in /Ash-js/jquery-Ash.min.js
the configuration of this attribute is in /Ash-js/Ash-import.min.js

It searches for the included div in the page where above files are included,
Then it parsed the external html file.

Its That Simple,😉🤗

# QuoteAPI by Andyproject.de
A collection of German and English quotes. Over 6000 quotes. Free and fast forever.

# Documentation
The API can be reached via `https://api.andyproject.de/quotes/`.<br>
Backup API: `http://data.andyproject.de/quotes/`. <br>
Notice: The Backup API have no SSL certificat also not working vor Images.
<br>This will output random quotes in any language. 
<br>
<br>
<b>German</b>
<br>
To get German quotes the URL `https://api.andyproject.de/quotes/de` can be used.
<br>
<br>
<b>English</b><br>
To get English quotes the URL `https://api.andyproject.de/quotes/de` can be used.
<br>
<br>
<b>Parameters and options</b><br>
- List all authors with `?sortby=authors`
- Search quote by author `?sortby=[name of author]`
- Search quote by ID `?id=[ID]`
- Show all quotes (token required) `?all&token=[token]`
<br>
Note: These parameters and options are only available for the url `/de` and `/en`.<br><br>

<b> Example:</b>
```
import requests

response = requests.get('https://api.andyproject.de/quotes/de/?id=54')

if response.status_code == 200:
    data = response.json()
    print(f'"{data["quote"]}" - {data["author"]}')
else:
    print(f'Error {response.status_code}: {response.text}')
```

# Image API
You can also use ready-made images with German quotes. 
<br>These are also uploaded on instagram at <a href="https://instagram.com/dailywords4u">@dailywords4u</a>.
<br>Pictures with English quotes will follow. 
<br>Please note that the rights and licenses of the images in this API are held by <a href="https://pexels.com">Pexels</a>. So you are obligated to cite Prexels as source.<br><br>
URL: `https://api.andyproject.de/quotes/img/dailywords4u`
<br>
Note: There are no parameters or options for this URL.
<br><br>

<b>Reponse:</b>
``` 
{"bild":
{
"link":"https:\/\/img.andyproject.de\/dailywords4u?link=dailywords4u_581.png",
"date":"2023-05-04 15:19:34",
"size":3598217,
"extension":"png"
}} 
```

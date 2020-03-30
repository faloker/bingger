# Bingger
Dead-simple, small and extra-limited tool to search Bing from the command-line.

# How To
Get a key from the Azure (free pricing tier):
https://ms.portal.azure.com/#create/Microsoft.CognitiveServicesBingSearch-v7

and export it:
```
export BING_API_KEY=your-api-key-here
```

Install it
```
npm install -g bingger
```

And when use it
```
bingger "site:mysite.com filetype:pdf"
```

If Bing has something to show it will be a JSON object
```
[
  {
    "_type": "WebPage",
    "id": "https://api.cognitive.microsoft.com/api/v7/#WebPages.0",
    "name": "npm-link | npm Documentation",
    "url": "https://docs.npmjs.com/cli/link",
    "displayUrl": "https://docs.npmjs.com/cli/link",
    "snippet": "Next, in some other location, ...",
    "dateLastCrawled": "2020-03-25T21:25:00.0000000Z"
  },
  ...
]
```

Otherwise you get a JSON object `[]`.
# Search
## Search from several search engines

### Usage

The function returns back a UIViewController
``` swift
String.search(searchEngine: .duckduckgo)

// E.g.
"Hello World".search(searchEngine: .google)
```
You can present the ViewController using
``` swift
present("Hello World".search(searchEngine: .google), animated: true, completion: nil)
```

---
### Search Engines 
- Google `.google`
- DuckDuckGo `.duckduckgo`
- Bing `.bing`
- Yahoo `.yahoo`

---
### Additional Info
- This uses SafariServices 
- In order to return a URL, 
``` swift
func search(searchEngine: searchEngines) -> UIViewController {
// CHANGE IT TO
func search(searchEngine: searchEngines) -> URL {

// AND

return safariViewController
// CHANGE IT TO
return url
```

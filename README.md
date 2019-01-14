# Search
## Search from several search engines

### Usage

#### If you want the function to return a UIViewController
This uses `SafariServices` to return a UIViewController therefore, you can just use `present()`
``` swift
String.searchVC(searchEngine: .duckduckgo)

// E.g.
"Hello World".searchVC(searchEngine: .google) // Type UIViewController
```
You can present the ViewController using
``` swift
present("Hello World".searchVC(searchEngine: .google), animated: true, completion: nil)
```

#### If you want the function to return a **URL**
This allows you to open a URL, for example if you want to open a URL inside the Safari app instead of using `SafariServices` for some reason
``` swift
String.searchURL(searchEngine: .duckduckgo)

// E.g.
"Hello World".searchURL(searchEngine: .google) // Type URL
```
You can open the URL in the Safari app by
``` swift
UIApplication.shared.open("Hello".searchURL(searchEngine: .duckduckgo))
```

---
### Search Engines 
- Google `.google`
- DuckDuckGo `.duckduckgo`
- Bing `.bing`
- Yahoo `.yahoo`

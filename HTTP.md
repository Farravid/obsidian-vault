
# What is a User-Agent

A **User-Agent** is a string sent by the client (such as a web browser or an application) in the HTTP request header to identify itself to the web server. The **User-Agent** provides details about the client's environment, such as:

- Type of device (e.g., mobile, desktop)
- Operating system (e.g., Windows, Linux, macOS)
- Browser (e.g., Chrome, Firefox, Safari)
- Rendering engine (e.g., WebKit, Gecko)

### Why is a User-Agent Used?
1. **Server Optimization**: The server can adapt the response based on the type of device or browser, for example, sending a mobile-optimized page to smartphones.
2. **Tracking**: Some websites use User-Agents to track and differentiate between visitors.
3. **Access Control**: Some servers allow or block access depending on the User-Agent, which may help prevent bots or unwanted clients.
4. **Analytics**: Web analytics tools use User-Agent strings to determine the user's platform, browser, and device type for statistics.

### Example of a User-Agent
Here's a typical **User-Agent** string:

```
Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/93.0.4577.63 Safari/537.36
```

Breaking it down:
- **Mozilla/5.0**: Legacy from older browsers like Netscape and Firefox. Most browsers use this for compatibility.
- **Windows NT 10.0**: Specifies the operating system (Windows 10 in this case).
- **Win64; x64**: Indicates a 64-bit system.
- **AppleWebKit/537.36**: The browser's rendering engine (in this case, Apple's WebKit used by Chrome).
- **Chrome/93.0.4577.63**: Specifies the browser version (Chrome version 93 in this case).
- **Safari/537.36**: Indicates compatibility with Safari's rendering engine.

### Custom User-Agent in Code
Sometimes, when making requests from a program (like with the **CPR** library in C++ or Rust's `reqwest`), you may want to change the **User-Agent** string. For example, you may want to mimic a popular browser or identify the request as coming from your application.

### Example Scenario
Suppose you're scraping data from a website or fetching financial data from an API. Some websites may block or restrict bots or scripts with generic User-Agents like "curl" or "python-requests." To bypass these restrictions, you can set the **User-Agent** to something more typical of a regular browser.

```cpp
cpr::Response r = cpr::Get(cpr::Url{"https://example.com"},
                           cpr::Header{{"User-Agent", "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36"}});
```

In this example, the **User-Agent** is set to make the server believe the request is coming from a Chrome browser on Linux.

### Why Modify the User-Agent?
1. **Bypassing Restrictions**: Some websites serve different content based on the User-Agent (e.g., mobile vs desktop).
2. **Avoiding Blocking**: Some servers block requests from non-browser clients (such as `curl`, `wget`, or automated tools) but allow requests that seem to come from browsers.
3. **Identification**: You might want to identify your application with a custom User-Agent (e.g., "MyCustomApp/1.0").

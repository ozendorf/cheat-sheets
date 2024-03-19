# Curl Cheat Sheet

## 1. Basic GET Request

```bash
# Send a GET request to a URL
curl <url>
```

## 2. GET Request with Headers
```
# Send a GET request with custom headers
curl -H "HeaderName: HeaderValue" <url>
```

## 3. POST Request with Data
```
# Send a POST request with data
curl -X POST -d "key1=value1&key2=value2" <url>
```

## 4. POST Request with JSON Data
# Send a POST request with JSON data
```
curl -X POST -H "Content-Type: application/json" -d '{"key1": "value1", "key2": "value2"}' <url>
```

## 5. Follow Redirects
```
# Follow redirects when making a request
curl -L <url>
```

## 6. Basic Authentication
```
# Send a request with basic authentication
curl -u username:password <url>
```

## 7. Set Custom User-Agent
```
# Set a custom user-agent header
curl -A "CustomUserAgent" <url>
```

## 8. Save Response to File
```
# Save the response to a file
curl -o output.txt <url>
```

## 9. Verbose Output
```
# Print verbose output including request and response headers
curl -v <url>
```

## 10. Ignore SSL Certificate Verification
```
# Send a request without verifying the SSL certificate
curl -k <url>
```


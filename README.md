# HTTP smuggling file converter

Useful for getting files past web filtering and web proxies. It converts the file into a binary base64 encoded blob that is included in a Javascript variable. The tool generates an example HTML file with the encoded file included in it. Upon rendering the page a createObjectURL() is made with the content triggering a file download.

# How to use:
1. Get the script
2. Make the script executable and run the script where you specify the file you want to make downloadable using HTTP smuggling.
3. If you are using any kind of automation for downloading the content then be careful on what file extension you give the file as some web browsers or web clients will not allow dangerous types e.g. executable files.
4. Consider downloading the file with a temporary extension and then renaming the file after download.

Usage:
```
$ ./smugweb.sh calc.exe
-Javascript file smuggling page generator -- @0xtosh
OK Created download.html
```
4. Host the ```download.html``` file somewhere on a web server or use it in whatever content you have that is relevant.
5. Make sure only the relevant IP addresses have access to your content and use HTTPS.
6. Go to the page directly with a browser or include the content of the ```download.html``` in your own client side web rendering content that supports Javascript. This should trigger the file download.

Different web browsers and web clients (with or without a web proxy) will have different download behaviors. Microsoft Edge usually allows for silent downloads.

For testing purposes. Use responsively.

1. Describe the path an HTTP Request takes from a browser to your GitHub Pages site.
  When I type my GitHub Pages URL into a browser, the browser first looks up the domain name in DNS to find the IP address associated with GitHub’s servers.
After it gets the IP address, the browser opens a TCP connection to that server, usually over HTTPS. Then a TLS handshake happens so the connection is encrypted and secure.
Once the secure connection is established, the browser sends an HTTP GET request asking for the webpage. The request is typically handled by a content delivery network run by Fastly, which routes it to a nearby server.
That server sends back the static files like HTML, CSS, and JavaScript, and the browser renders the page. If the page needs additional resources, the browser makes more HTTP requests for those files.

2. We discussed Docker Containers in class. Explain how a Docker Container differs from the
environment provided by GitHub Pages.
  A Docker container is different from the environment provided by GitHub Pages because a Docker container includes its own runtime and dependencies and can run full applications, including servers and databases.
It gives you control over the software and environment inside the container. In contrast, GitHub Pages only hosts static files and does not allow you to run code on the server or control the underlying system.
Docker is more flexible and customizable, while GitHub Pages is a platform just for static websites.

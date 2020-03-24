# vue-production-server-proxy
Boilerplate for Vue project ready for production, with neat implementation of "devServer proxy" in production environment, using **Nginx**.
***

## Getting Started
I'm using [Docker](https://www.docker.com/products/docker-desktop) as a production environment, but feel free to use any other production environment which you prefer. My solution **does not** rely on [Docker](https://www.docker.com/products/docker-desktop), the trick is all about [Nginx](https://www.nginx.com/).

### Prerequisites
To install docker: https://www.docker.com/products/docker-desktop

### Installing
```
git clone https://github.com/zhzhang-4390/vue-production-server-proxy.git

cd vue-production-server-proxy

npm i
```
***

## Running
### Development Environment
```
npm run serve
```

Go to http://localhost:8080 using your browser.

Other than the Vue starter page, you should be able to see the rendered HTML of my Github page :)

This is the ```vue.config.js``` proxying.

```Ctrl+C``` to stop the development server.

### Production Environment
```
docker build . -t demo

docker run -d -p 8080:80 demo
```

Go to http://localhost:8080 using your browser.

Now if you still can see the rendered HTML of my Github page, then that's ```nginx.conf``` proxying :)
***

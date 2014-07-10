# jitta/nodejs

[`jitta/nodejs`](https://index.docker.io/u/jitta/nodejs) is a [docker](https://docker.io) base image that bundles the latest version of v0.8 [nodejs](https://nodejs.org) and [npm](https://npmjs.org) installed from [nodejs.org](http://nodejs.org/download/).

## Usage

- Create a Dockerfile in your nodejs application directory with the following content:

        FROM jitta/nodejs:v0.8
        
        WORKDIR /app
        ADD package.json /app/
        RUN npm install
        ADD . /app
        
        CMD []
        ENTRYPOINT ["/nodejs/bin/npm", "start"]

- Run the following command in your application directory:

        docker build -t my/app .

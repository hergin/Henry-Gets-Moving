# Development
## Replication of development environment:
- Clone project repository
- `cd` into the root directory
- Run `npm i`
- Run `npm start`
- Good-to-go!

## Run via Docker:
- Clone project repository
- Build: `docker build -t hgm .`
- Run: `docker run -d -p 3000:3000 --name hgm hgm`
- Navigate to http://localhost:3000 in your browser!

# Email indexer from the Enron database
## First steps
- Download the latest version of ZincSearch from its [repository](https://github.com/zincsearch/zincsearch/releases)
- Download the Enron emails database [here](http://www.cs.cmu.edu/~enron/enron_mail_20110402.tgz)
This repository contains two aplications: `enron-indexer` and `search-api`.

## enron-indexer
This app parses the raw files from the Enron Database and upload emails to a ZincZearch index.

### Build
- Get dependencies
```bash
go mod download
```
- Build app
```bash
go build -o zincindexer
```
### Environment variables
Don't forget to include the following environment variables before running the `./zincindexer` command:

```bash
export ZINC_FIRST_ADMIN_USER="admin"
export ZINC_FIRST_ADMIN_PASSWORD="Complexpass#123"
export ZINC_SERVER_URL = "http://localhost:4080/api/"
./zincindexer
```
_Remember that your environment credentials variables must match with your ZincSearch server credentials._

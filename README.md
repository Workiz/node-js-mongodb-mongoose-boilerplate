# Workiz ACADEMY : MONGO DB Via Mongoose

## Getting Started 🚀

```bash
git clone <THIS_REPO>
npm install
```

## Development 🤓

```bash
npm run dev-server
```

```

### Build Artifacts 🛠

```bash
npm build
```

### Deploy to staging
```
npm run deploy-staging
``
It will perform a `npm run build-image` action , that takes COMMIT SHA and builds a new image with a tag of COMMIT SHA.
Later it will use `infra/deploy-staging.sh` to apply new `deployment.yaml` configuration with new COMMIT SHA.

Note: If you will update code without commiting it change, commit sha wont get changed , so it won't deploy the change.


### Sample REST Calls:

POST http://localhost:9090/academy

# add new academy item
```bash
{
    "name":"Eran Peled",
    "ID" : 30203023,
    "projects": [
        {
            "name":"mongodb",
            "type":"lecture"
        },
        {
            "name":"nodejs",
            "type":"lecture"
        }
    ]
}
```

# delete academy item
DELETE http://localhost:9090/academy/delete/60fbd4a5c0e6850ef3951874
where 60fbd4a5c0e6850ef3951874 is the ID of the document.

# Un-delete academy item
DELETE http://localhost:9090/academy/restore/60fbd4a5c0e6850ef3951874
where 60fbd4a5c0e6850ef3951874 is the ID of the document.

# GET academy item
GET http://localhost:9090/academy/60fbd4a5c0e6850ef3951874
where 60fbd4a5c0e6850ef3951874 is the ID of the document.

# UPDATE academy item
PUT http://localhost:9090/academy/60fbd4a5c0e6850ef3951874
where 60fbd4a5c0e6850ef3951874 is the ID of the document.

BODY: 

```bash
{
    "name":"Eran Peled - 2",
    "ID" : 6782872,
    "projects": [
        {
            "name":"mongodb",
            "type":"lecture"
        },
        {
            "name":"nodejs",
            "type":"lecture"
        }
    ]
}
```

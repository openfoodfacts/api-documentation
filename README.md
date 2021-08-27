# Documentation of the Open Food Facts API

The new version of the documentation is available here: 
- https://documenter.getpostman.com/view/8470508/SVtN3Wzy
- Stable version of the doc: https://openfoodfacts.github.io/api-documentation/
- Staging version of the doc: https://openfoodfacts.github.io/api-documentation-staging/

We have an older version available on the Wiki.

- https://wiki.openfoodfacts.org/Documentation

# Roadmap

We need documentation maintainers
- [ ] to document new features (Eco-Score, Attributes…)
- [ ] to improve existing documents based on feedback and questions in the #api channel

- What can I help with ? https://github.com/openfoodfacts/api-documentation/issues/23


# Edit the documentation


## Install the Postman application

https://www.postman.com/downloads/

## Clone the repository

```
git clone https://github.com/openfoodfacts/api-documentation
git checkout -b <DOC_FIX_BRANCH_NAME>
```

## Edit the collection and push to git

* Open Postman
* Click "Import" then "Folder" and browse to the repo's folder.
* Postman collection and environment located in the repo will be imported in your Postman application.
* Edit the collection using the application, and once you're done click "Export"
* Rename the file as `off-pm-collection.json`
* Push to git


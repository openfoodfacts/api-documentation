# Documentation of the Open Food Facts API

The new version of the documentation is available here: 
- Stable version of the doc: https://openfoodfacts.github.io/api-documentation/
- Staging version of the doc: https://openfoodfacts.github.io/api-documentation-staging/

We have an older version available on the Wiki.

- https://wiki.openfoodfacts.org/Documentation

# Tests
- Note: This documentation is actually able to run API tests, that will fail if not properly specified or if the API has changed, and the documentation has not. Currently, around 20 tests are failing.

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

## Edit the collection with Postman

* Open Postman
* Click "Import" then "Folder" and browse to this repository's folder.
* Postman collection and environment located in the repo will be imported in your Postman application.
* Edit the collection using the application, and once you're done click "Export"
* Rename the file as `off-pm-collection.json`
* Save it (overwrite the original one)

## Push to git

Now it's time to propose your changes as a pull request on the repository.
We're going to make a branch and commit our updated `off-pm-collection.json`.

Run:
  ```
  git checkout -b <NEW_BRANCH_NAME>
  git add off-pm-collection.json
  git commit -m "<COMMIT_MESSAGE>"`
  git push --set-upstream origin <NEW_BRANCH_NAME>
  ```

Once you are done:

* Open a browser
* Navigate to https://github.com/openfoodfacts/api-documentation
* Open a new PR from your branch ("Create Pull Request" button).
* View your updated documentation that was automatically deployed to the staging environment https://openfoodfacts.github.io/api-documentation-staging.

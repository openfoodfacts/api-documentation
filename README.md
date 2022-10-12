# README

## Documentation of the Open Food Facts API

The new version of the documentation is available here :

* Stable version of the doc: https://openfoodfacts.github.io/api-documentation/
* Staging version of the doc: https://openfoodfacts.github.io/api-documentation-staging/

We have an older version available on the Wiki.

* https://wiki.openfoodfacts.org/Documentation

## Roadmap

We need documentation maintainers

* [ ] to document new features (Eco-Score, Attributes…)
* [ ] to improve existing documents based on feedback and questions in the #api channel
* [ ] What can I help with ? https://github.com/openfoodfacts/api-documentation/issues/23

## Edit the documentation

### Install the Postman application

https://www.postman.com/downloads/

### Clone the repository

```
git clone https://github.com/openfoodfacts/api-documentation
git checkout -b <DOC_FIX_BRANCH_NAME>
```

### Edit the collection with Postman

* Open Postman
* Click "Import" then "Folder" and browse to this repository's folder.
* Postman collection and environment located in the repo will be imported in your Postman application.
* Edit the collection using the application, and once you're done click "Export"
* Rename the file as `off-pm-collection.json`
* Save it (overwrite the original one)

### Push to git

Now it's time to propose your changes as a pull request on the repository. We're going to make a branch and commit our updated `off-pm-collection.json`.

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


## Applications using this API

### Official application

The official Open Food Facts app uses the API.

### Third party applications

Feel free to open a PR to add your application in this list.

- **Gluten Scan**. [Android](https://play.google.com/store/apps/details?id=com.healthyfood.gluten_free_app) / [iOS](https://apps.apple.com/ch/app/gluten-scanner/id1540660083)
- **Halal & Healthy**. [Android](https://play.google.com/store/apps/details?id=com.TagIn.Tech.handh) / [iOS](https://apps.apple.com/ch/app/halal-healthy/id1603051382)
- **Fitness Tracker**. [Android](https://play.google.com/store/apps/details?id=dk.cepk.fitness_tracker)

# API Documentation Friction Log

This log lists all the glitches that makes the [Open Food Facts API documentation](https://openfoodfacts.github.io/api-documentation/) hard to use, but frames it around a narrative  use case. Each log item can be created as issues so thier progress can be tracked.

## User Friction

These are frictions of [Open Food Facts API documentation](https://openfoodfacts.github.io/api-documentation/) framed around a customer(user) use case.

Title    |          Description
 ------------------------| ---------
 | Filter products based on countries| Do you use countries or countries_tag ? (Properly indicate in the next doc)
 | JSON response| The fields returned in a response are not properly described. For example it turns out that _nutriments.unit_ and _nutriments.value_ does not mean anything. Can the [READ Request](https://openfoodfacts.github.io/api-documentation/#collapse-2READrequests-Getnutritionfactsforaspecificbarcode) response length be reviewed? This is because the response is too lengthy and so many information can be lost in the crowd.
 |Contribution guidelines | A more detailed and easily understandable guideline for open source enthusiasts to easily contribute to the current documentation.
 |FAQ | [The link is broken](https://openfoodfacts.github.io/api-documentation/#9FAQ) and it should be more visible. A survey can be done for the development team to get more FAQ with detailed answers. The texts in the FAQ’s do not match up with the rest of the documentation. FAQ’s should also be updated with more questions as the  API keeps improving its version. 
 |Taxonomy Unit| Remove _unit_ and _value_ from value in  returned fields because they cprrespond to each other and they are for internal purposes.
 |Add image to existing product | Improved the guidelines on how to add photo to an existing product irrespective of file type etc.
 |Tutorials | Create real-life sample tutorials on how to build with the Open Food Facts database (either articles or video tutorials)
 |Glossary | Build a glossary for all technical terms in this project
 |Visibility | The documentation isnt easy to see , at least it should be visible in the project landing page and github .
 |Navigation | Current documentation is overcrowded and difficult to navigate. The side navbar section does not stay in the same place when the user scrolls down, this makes the docs harder to use since the user has to scroll upwards again to find new information within the docs.
 |Authentication | Do we need to authenticate at any point when using this API? If yes, indicate properly.
 |Version |3 different versions of the documentation, but no authoritative version (wiki (obsolete, should be deleted), api-documentation (more up to date but not complete), Postman cloud (obsolete).
 |Broswer compatibility | It does not display in firefox
 |News & Updates | A News & Updates section where users are informed of the updates that have been made to the documentation.

## Future Proposals

After the new documention shipped its first phase, these plans can be looked at to improve community contributions.

### Proper contributor follow-up and community check-in

Create good first issues, do follow ups on contributors for these issues and keep improving contributors guideline. Schedule weekly/biweekly contributors meet/newcomers call so new contributors can habe a great headstart with contributing to the project.

## Developer Friction

These are frictions of [Open Food Facts API documentation](https://openfoodfacts.github.io/api-documentation/) framed around a developer/documentation contributor use case.

Title    |          Description
 ------------------------| ----------
 |Proximity | The documentation isn't close to the code
 |Review    | Changes should be reviewable via Github Pull Requests
 |Test      | Run tests on the proposed changes in the documentation before any merge is made to the main documentation.

## API Friction Log

During the survey , some frictions were discovered that resulted from the API itself. They are key things for the developers to look out while building the next API version.

Title    |          Description
 ------------------------| ---------
 |Search| Current API: not being able to do a precise search on product name. E.g _The database result are working fine for normal products like “Milk” but when I try to query for a fruit or vegetable like “Apple” the results always show me products like “Apple juice”, “Apple rings”  instead of the actual product I'm searching for which is an Apple._
 |Add image to existing product | In a future version of the API, having a field name for the image that does not change depending on the image type or language.

 

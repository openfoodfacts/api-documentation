# API documentation friction log

This log lists all the glitches that makes the Open Food Facts [API documentation](https://openfoodfacts.github.io/api-documentation/) hard to use, but frames it around a narrative or customer(user) use case. Each log item can be created as issues so thier progress can be tracked.

Title    |          Description
 ------------------------| ---------
 | Filter products based on countries| Do you use countries or countries_tag ? (Properly indicate in the next doc)
 | JSON response| The fields returned in a response are not properly described. For example it turns out that _nutriments.unit_ and _nutriments.value_ does not mean anything. Can the [READ Request](https://openfoodfacts.github.io/api-documentation/#collapse-2READrequests-Getnutritionfactsforaspecificbarcode) response length be reviewed? This is because the response is too lengthy and so many information can be lost in the crowd.
 |Contribution guidelines | A more detailed and easily understandable guideline for open source enthusiasts to easily contribute to the current documentation.
 |FAQ | Make it more visible and do a survey from team on more FAQ with detailed answers. The texts in the FAQ’s do not match up with the rest of the documentation. Addition of new FAQ’s is also needed since the OFF API goes through major changes every once in a while. [The link is also broken](https://openfoodfacts.github.io/api-documentation/#9FAQ)
 |Remove _unit_ and _value_ from value in  returned fields | [Taxonomy Unit](https://openfoodfacts.slack.com/archives/C043X1X90/p1653923029786469?thread_ts=1653919835.888889&cid=C043X1X90)
 |Add image to existing product | [Improved guidelines on how to add photo to an existing product irrespective of file type etc.](https://openfoodfacts.slack.com/archives/C043X1X90/p1653409395542189?thread_ts=1653213518.473549&cid=C043X1X90)
 |Tutorials | Create real-life sample tutorials on how to build with the Open Food Facts database (either articles or video tutorials)
 |Glossary | Build a glossary for all technical terms in this project
 |Visibility | The documentation isnt easy to see , at least it should be visible in the project landing page and github .
 |Navigation | Current documentation is overcrowded and difficult to navigate. The side navbar section does not stay in the same place when the user scrolls down, this makes the docs harder to use since the user has to scroll upwards again to find new information within the docs.
 |Authentication | Do we need to authenticate at any point when using this API? If yes, indicate properly.

## Future Proposals

After the new documention has its first phase shipped, these plans can be looked at to improve community contributions.

### Proper contributor follow-up and community check-in

Create good first issues, do follow ups on contributors for these issues and keep improving contributors guideline. Schedule weekly/biweekly contributors meet/newcomers call so new contributors can habe a great headstart with contributing to the project.

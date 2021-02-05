# Documentation of the Open Food Facts API

The new version of the documentation is available here: 🚀 https://documenter.getpostman.com/view/8470508/SVtN3Wzy 🚀
Version 2 of the documentation of the V1 API. 

- https://wiki.openfoodfacts.org/Documentation
- https://world.openfoodfacts.org/files/api-documentation.html

We have an older version available on the Wiki.
We need volunteers
- [ ] to document new features (Eco-Score, Attributes…)
- [ ] to publish and update the docs on fast services
- [ ] to improve existing documents based on feedback and questions in the #api channel

Roadmap



How to convert to HTML
https://medium.com/@thedevsaddam/create-api-documentation-from-postman-collection-d40540582155

docgen build -i "Open Food Facts API Documentation.postman_collection.json" -o api-documentation.html

How to convert to MarkDown
docgen build -i "Open Food Facts API Documentation.postman_collection.json" -o ~/Downloads/index.md -m

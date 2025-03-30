# Understanding Image Identifiers in Open Food Facts

When working with product images in the Open Food Facts API, you'll encounter two different types of identifiers: `imgid` and `id`. This document explains their differences, relationships, and how they're used in image URLs.

## imgid

The `imgid` is a unique numerical identifier automatically assigned to each uploaded image:

- Every uploaded image receives an `imgid` upon upload
- This identifier is permanent and never changes
- It identifies the raw image file as uploaded by users
- The `imgid` exists regardless of whether the image is selected as an "official" product image

**Example:**
In the URL `https://world.openfoodfacts.org/images/products/376/028/487/0115/1.jpg`, the `1` is the `imgid`.

## id

The `id` is a functional identifier that represents the image's purpose or selection status:

- Examples include `front_fr`, `ingredients_en`, `nutrition_de`
- The first part indicates the view type (front, ingredients, nutrition, etc.)
- The suffix indicates the language code (fr, en, de, etc.)
- An `id` is assigned when an image is selected to represent a specific aspect of a product

**Example:**
In the URL `https://world.openfoodfacts.org/images/products/376/028/487/0115/front_fr.8.full.jpg`, `front_fr` is the `id`.

## Relationship Between imgid and id

When a user uploads an image, the process works as follows:

1. The image receives an `imgid` (e.g., `1`)
2. If the image is selected to represent a specific view of the product (e.g., the front packaging in French), it gets assigned an `id` (e.g., `front_fr`)
3. The original image remains accessible via its `imgid`
4. The selected and possibly processed version is accessible via the `id`

An image with a specific `imgid` can be selected and assigned any `id` based on its content and purpose. The same raw image could potentially be used for different purposes.

## Image URL Structure

### URL Structure for imgid
```
https://world.openfoodfacts.org/images/products/{barcode_segments}/{imgid}.jpg
```

### URL Structure for id
```
https://world.openfoodfacts.org/images/products/{barcode_segments}/{id}.{rev}.{size}.jpg
```

Where:
- `{barcode_segments}`: The product barcode divided into segments (e.g., `376/028/487/0115`)
- `{imgid}`: The numerical image identifier (e.g., `1`)
- `{id}`: The functional identifier (e.g., `front_fr`)
- `{rev}`: A revision number that gets assigned automatically when rotations or other modifications are applied (e.g., `8`)
- `{size}`: The image size/type such as `full`, `400`, etc.

## Example Use Case

1. A user uploads an image of a product's front packaging
2. The system assigns it `imgid=1`
3. The image is available at `https://world.openfoodfacts.org/images/products/376/028/487/0115/1.jpg`
4. The user or moderator selects this image as the front packaging image for the French version
5. The system assigns it `id=front_fr`
6. After rotation is applied (revision 8), the image is now also available at `https://world.openfoodfacts.org/images/products/376/028/487/0115/front_fr.8.full.jpg`

Both URLs now point to the same image, but the `id` version may include additional processing (rotation, cropping, etc.) and indicates the image's purpose in the product presentation.

## API Response Example

When requesting product information with image fields, you'll receive both identifiers in the response:

```json
{
  "images": {
    "1": {
      "sizes": {
        "full": {
          "w": 2000,
          "h": 3000
        },
        "400": {
          "w": 400,
          "h": 600
        }
      },
      "uploaded_t": 1615283540,
      "uploader": "user123"
    },
    "front_fr": {
      "imgid": "1",
      "angle": "90",
      "rev": "8",
      "sizes": {
        "full": {
          "w": 3000,
          "h": 2000
        },
        "400": {
          "w": 600,
          "h": 400
        }
      }
    }
  }
}
```

In this example, the image with `imgid=1` has been selected as `front_fr` and rotated 90 degrees.
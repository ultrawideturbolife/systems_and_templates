# Firestore Datamodel Repository

# ❤️‍🔥 **Firestore Datamodel Repository Instructions**

---

<aside>
💡 The project has an example folder where the philosophy behind this repository is demonstrated with example collections and subcollections.

</aside>

Through this type of repository we are trying to organise a place where changes to our firestore database can be managed and communicated from a central location.

![https://media.giphy.com/media/5b5CuS5enNTxhwAkSD/giphy.gif](https://media.giphy.com/media/5b5CuS5enNTxhwAkSD/giphy.gif)

⚠️ Everyone that works with data from our firestore database should always be added as a reviewer of every pull request. This is to make sure that any changes we make to our data models are communicated to those that might need to act on it. If any of us needs to change/respond to any of the changes, we do so before accepting the pull request. Accepting the pull request means we have seen the data model, reviewed it and acted on it (if needed).

To structure and communicate the state of our database we use easily readable (and perhaps parsable in the future) .yaml files where we specify the following per model:

- **name:** This is the preferred name of the model, preferrably ending with DTO so we always know we're talking about the purest form of data throughout the company when we're discussing something that ends with DTO.
- **description:** Short description of the model. What is it used for?
- **locations:** Possible locations in our database where the model is used, keep the following rules in mind:
    - `ExampleCollection/{**$id**}`
        - The `id` here has a `$` prefix. This means it represents every `document` in the collection.
        - So in this example we’re saying that the model that we’re describing is is every `document` located in the `ExampleCollection` collection.
    - `ExampleCollection/{**$id**}.ExampleField`
        - The `id` here also has a `$` prefix, again meaning it represents any document in the collection.
        - The `.ExampleField` stands for a specific field name in that document. In this case that field name is `ExampleField`.
        - So in this example we’re saying that the model that we’re describing is a `map`  (since it’s a field) located in every document in the `ExampleCollection` collection where the field name is `ExampleField`.
    - `ExampleCollection/{ExampleId}`
        - The `{ExampleId}` id here does not have a `$` . This means the id of the document equals `ExampleId`.
        - So in this example we’re saying that the model that we’re describing is a single `document` located in the `ExampleCollection` where the id of the document is `ExampleId`.
- **fields:** Possible fields of the model:
    - Starts with name of the field followed by a colon:
        - **deprecated**: Which version we stopped using this field. This field may be omitted if false.
        - **type**: Type of the fields as represented in our firestore database.
            - `string`
            - `number`
            - `boolean`
            - `map`
            - `array`
            - `null`
            - `timestamp`
            - `geopoint`
            - `reference`
        - **required**: Whether the field is always present. This may also be a condition so `Type == Incidental` would mean it's only required when the `Type` field inside that DTO is `Incidental`.
        - **enums**: Possible enum values of a field. This field may be omitted if not applicable.
        - **description**: Short description of the field. What is it used for?
        - **ref**: The type used for arrays, maps or the name of the model that is used to serialise this field. This field may be omitted if not applicable. Examples could be (but not limited to) `string`, `string/dynamic` or a different model specified in this repository.
        - **example**: Possible example values of this field.
- Fields should be in alphabetical order to resemble true structure and presentation of a firestore database.

# ✂️ Snippets

Save these snippets for quick and easy model creation.

### Start of each document

```yaml
name: $name$
description: $description$
locations:
- $location$
  fields:
  $END$
```

### Each field

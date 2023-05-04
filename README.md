# Image Finder

## Brief
The Aim of the task is to create a system that displays images fetched from an external service.
The Backend gets the data, transforms it, and exposes to the Frontend. The Frontend shows the images using React.

Tasks - Backend:
- Create an HTTP server that fetches data from an external API
- Expose a list of image URLs to the frontend

Tasks - Frontend:
- Fetch data from the backend
- Display data using React

For the purpose of this exercise, the external API will be NASA's media searching API

    https://images-api.nasa.gov/search?q=moon

Here is an example of the payload:

```
{
  "collection": {
    "href": "https://images-api.nasa.gov/search?q=moon",
    "version": "1.0",
    "items": [
      {
        "href": "https://images-assets.nasa.gov/image/PIA12235/collection.json",
        "data": [ ... ],
        "links": [
          {
            "href": "https://images-assets.nasa.gov/image/PIA12235/PIA12235~thumb.jpg",
            "render": "image",
            "rel": "preview"
          }
        ]
      }
    ]
  }
}
```

Here is what we expect our App to show:

```
<div>
    <img src="https://images-assets.nasa.gov/image/PIA12235/PIA12235~thumb.jpg" />
    <img src="https://images-assets.nasa.gov/image/PIA12235/PIA12236~thumb.jpg" />
    <img src="https://images-assets.nasa.gov/image/PIA12235/PIA12237~thumb.jpg" />
    (...)
</div>
```

## Usage
To start the application you need to build it first:

```
npm install
npm run start
```

You are free to code and run the application using any IDE/text editor of your choice.
You can search the web for information as you'd do in normal work day or ask your interviewers for help and collaboration.

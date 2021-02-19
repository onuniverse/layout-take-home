# layout-take-home

Create a React application that takes a grid description json file (an oversimplified version of our universe site data) and uses it to display colored boxes at the right positions.

## Simple Grids

```json
{
  "type": "grid",
  "gridSize": {
    "width": 3,
    "height": 5
  },
  "backgroundColor": "#000000",
  "children": [
    {
      "type": "block",
      "color": "#0000FF",
      "position": {
        "x": 0,
        "y": 0
      },
      "size": {
        "width": 2,
        "height": 1
      }
    },
    {
      "type": "block",
      "color": "#FF0000",
      "position": {
        "x": 2,
        "y": 4
      },
      "size": {
        "width": 1,
        "height": 1
      }
    }
  ]
}
```

Should display a black screen with a blue block in the top left corner that is 2/3 the screen width and 1/5 the screen height and a red block in the bottom right corner that is 1/3 the screen width and 1/5 the screen height.

## Nested Grids

Grids can also have other grids nested inside of them. The grids height and width are their size within their parent grids coordinate system, but they have their own coordinate system that can be different than their size.

```json
{
  "type": "grid",
  "gridSize": {
    "width": 4,
    "height": 4
  },
  "backgroundColor": "#444444",
  "children": [
    {
      "type": "grid",
      "backgroundColor": "#000000",
      "size": {
        "width": 2,
        "height": 2
      },
      "position": {
        "x": 0,
        "y": 0
      },
      "gridSize": {
        "width": 5,
        "height": 5
      },
      "children": [
        {
          "type": "block",
          "color": "#FF8800",
          "position": {
            "x": 0,
            "y": 0
          },
          "size": {
            "width": 1,
            "height": 5
          }
        },
        {
          "type": "block",
          "color": "#FF8800",
          "position": {
            "x": 1,
            "y": 2
          },
          "size": {
            "width": 3,
            "height": 1
          }
        },
        {
          "type": "block",
          "color": "#FF8800",
          "position": {
            "x": 4,
            "y": 0
          },
          "size": {
            "width": 1,
            "height": 5
          }
        }
      ]
    },
    {
      "type": "block",
      "color": "#00FF00",
      "position": {
        "x": 3,
        "y": 0
      },
      "size": {
        "width": 1,
        "height": 4
      }
    }
  ]
}
```

This activity is not intended to take more than 4 hours, build out support for simple grids first and then nested grids if time allows.

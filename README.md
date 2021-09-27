# GraphQL Restaurant Data Exercise 🍽

API (GraphQL) queries and CRUD implementaion solution.

## Tasks:

- Set up GraphQL for a restaurant data.
- Add mutations to get and update these data.

## List of GraphQL queries used:

- restaurant: This gets a single restaurant based on a provided ID. 
- restaurants: This gets a list of all restaurants. 
- setrestaurant: This creates a new restaurant. 
- deleterestaurant: This deletes a restaurant based on the provided id.
- editrestaurant: This updates a restaurant based on the provided id.

```javaScript
mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}

mutation deleterestaurants($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}
```

## Installation

- Run `npm install` to install node modules.
- Run the index.js file on `http://localhost:5500/graphql` in order to make queries with GraphQL.

## Usage

<img src = 'https://raw.githubusercontent.com/anyapages/graphql-restaurant-data-exercise/main/image.png?token=ATDMTEB7ZUUGO34UBGIMEGTBLLXHK' width="550" height="440"> 

## Learn More

To learn GraphQL, queries and mutations, check out the [GraphQL documentation](https://graphql.org/), [Queries and Mutations](https://graphql.org/learn/queries/).

## License

[MIT](https://github.com/anyapages/graphql-restaurant-data-exercise/blob/main/LICENSE) 

# GraphQL Restaurants Exercise

## Description:
Exercise to learn how to use GraphQL to Create, Read, Update and Delete (CRUD) records.


## How to Run:
1. Clone Repo
2. Run 'npm install'
3. Run 'node index.js'
4. Open http://localhost:5500/graphql in a browser

Use the following Queryies and Mutations in GraphiQL:

query singlerestaurant($idd: Int = 1) {
  restaurant(id: $idd) {
    id
    name
  }
}

query allrestaurants {
  restaurants {
    id
    name
    description
    dishes {
      name
      price
    }
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

mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}


## License Information:
MIT License
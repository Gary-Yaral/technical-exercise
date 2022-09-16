# technical-exercise

Given the following array (users) of objects complete the tasks described below – Code efficiency will be considered. 
(Use the programming language of your preference):
1.- Sort the array by attribute “name” (Descending).
2.- Delete duplicated objects.
3.- Create a new array with those objects which "Age" attribute is bigger than 21.
4.- Find the oldest user.
Please print each step result on the screen.
users = [
    {
        name: Josh,
        age: 31    },
    {
        name: Carl,
        age: 11    },
    {
        name: Maria,
        age: 16    },
    {
        name: Peter,
        age: 65    },
    {
        name: Josh,
        age: 31    },
    {
        name: Moe,
        age: 27    },
    {
        name: Stephan,
        age: 19    },
    {
        name: Moe,
        age: 41    },
    {
        name: Albert,
        age: 2    },
    {
        name: Henry,
        age: 64    },
    {
        name: Paul,
        age: 57    }
]

``` javascript
let users = [
    {
        name: 'Josh',
        age: 31    
    },
    {
        name: 'Carl',
        age: 11    
    },
    {
        name: 'Maria',
        age: 16    
    },
    {
        name: 'Peter',
        age: 65    
    },
    {
        name: 'Josh',
        age: 31    
    },
    {
        name: 'Moe',
        age: 27    
    },
    {
        name: 'Stephan',
        age: 19    
    },
    {
        name: 'Moe',
        age: 41    
    },
    {
        name: 'Albert',
        age: 2    
    },
    {
        name: 'Henry',
        age: 64    
    },
    {
        name: 'Paul',
        age: 57    
    }
]

// 1.- Sort the array by attribute “name” (Descending).
  let result = users.sort((a, b) => {
      if(a.name < b.name) return 1
      if(a.name > b.name) return -1
      return 0
  })
  console.log(result)

  // 2.- Delete duplicated objects.
  let check = {};
  result = result.map(data => {
      if(!check[data.name]) {
          check[data.name] = true
          return data
      } 
  }).filter(user => user !== undefined)
  console.log(result)

  // 3.- Create a new array with those objects which "Age" attribute is bigger than 21.
  let arrayCopy = []
  result.forEach(user => {
      if (user.age > 21) {
          arrayCopy.push(user)
      }
  })
  console.log(arrayCopy)

  // 4.- Find the oldest user.
  let biggest = result.sort((a, b) => b.age - a.age)[0]
  console.log(biggest)

```

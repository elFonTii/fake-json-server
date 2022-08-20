# Fake JSON Server

This will create some endpoints define in the `db.json` where you can fetch data.

`https://my-fake-json-server.herokuapp.com/superheroes`
`https://my-fake-json-server.herokuapp.com/superheroes/:id`
`https://my-fake-json-server.herokuapp.com/friends`
`https://my-fake-json-server.herokuapp.com/friends/:id`

You can also make `post/put/delete` requests. Example:

```javascript
const createUser = () => {
  axios
    .post('https://my-fake-json-server.herokuapp.com/superheroes', {
      id: 4,
      name: 'The Flash',
      alterEgo: 'Barry Allen',
    })
    .then((resp) => {
      console.log(resp.data);
    })
    .catch((error) => {
      console.log(error);
    });
};

const updateUser = () => {
  axios
    .put('https://my-fake-json-server.herokuapp.com/superheroes/4', {
      name: 'Flash',
      alterEgo: 'Barry Allen',
    })
    .then((resp) => {
      console.log(resp.data);
    })
    .catch((error) => {
      console.log(error);
    });
};

const deleteUser = () => {
  axios
    .delete('https://my-fake-json-server.herokuapp.com/superheroes/4')
    .then((resp) => {
      console.log(resp.data);
    })
    .catch((error) => {
      console.log(error);
    });
};
```

# Expressjs - tips
### Routing
#### Route parameters

call [/book/1234](http://localhost:8080/book/1234)
```JavaScript
app.get('/book/:id', (req, res) => {
  console.log(req.params) // { id: '1234' }
})
```
call [/book?id=1234](http://localhost:8080/book?id=1234)
```JavaScript
app.get('/book', (req, res) => {
  console.log(req.query); // { id: '1234' }
});
```
call [/book](http://localhost:8080/book)
with POST method & data { id: 1234 } 
```JavaScript
app.post('/book', (req, res) => {
  console.log(req.body); // { id: 1234 }
});
```

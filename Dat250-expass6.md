# Expass 6

Githublink til kode: https://github.com/587851/DAT250Expass6.git

![image](https://github.com/587851/DAT250md/assets/69521897/d05ffcae-dbf8-47fc-af28-000e6d968af6)


### Load todos using the Todo-API (HTTP GET)
```
  ngOnInit() {
    this.loadTodos();
  }
```

### Display all todos in a table, including a delete button in every row (HTTP DELETE)
```
 deleteTodo(id: number) {
    this.todoService.deleteTodo(id).subscribe(() => {
      this.loadTodos();
    });
  }
```
### Refresh displayed todos by clicking a button (HTTP GET)
```
loadTodos() {
    this.todoService.getTodos().subscribe(data => {
      this.todos = data;
    });
  }
```
### Add a todo by giving its description and summary (HTTP POST)
```
addTodo() {
    this.todoService.addTodo(this.newTodo).subscribe(() => {
      this.newTodo = { id: 0, description: '', summary: '' };
      this.loadTodos(); 
    });
  }
```

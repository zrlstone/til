# Conditional Style Class Names

The class_names provides a way to conditionally add classes to html tags (introduced in rails 6.1).

```
  <%= link_to(
    "Home",
    root_path,
    class: class_names({"active": current_page?(root_path)})
  )>

  <a href="/" class="active">Home</a>
```

See [the
docs](https://www.rubydoc.info/docs/rails/ActionView%2FHelpers%2FTagHelper:class_names)
for more details.
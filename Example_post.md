+++
using Dates
date = Date("2023-07-29")
title = "Hello from JuliaCon 2023!"
author = "kevin"
+++

# Hello from JuliaCon 2023!

This is an example post for the new website.


```>
println("This is REPL code!")
```

```!
foo = "This is a regular code block"
bar = "Variables get saved"
@show foo bar
```

```!
println(foo)
```

We can even include Literate.jl notebooks
with their own environment / deps!

\literate{_assets/literate/literate_example/post.jl; project=.} 

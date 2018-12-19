## Vuex
When using vuex stores, this may be something really simple but can consume hours of your time trying to solve. Vuex stores are isolated. Each instance of vue contains a respective vuex instance. You cannot communicate between instances without using some "glue" code such as localStorage.
Why does this matter? Multiple tabs.

Let's consider an example scenario:

1. You login on tab A at `/login`

2. On tab B, you refresh the URL: `/products/create` and wonder why your access Token is `null`. You break your head. You think it's a problem with Vuex.

And then, it strikes you - The vuex instances on tab A and tab B are different. Sounds familiar?

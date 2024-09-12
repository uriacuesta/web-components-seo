# Web components SEO
### Testing indexability of web components.

This website tests how standard and custom HTML tags are indexed by Google under different circumstances.


## Standard HTML

| Content          | Javascript | Link                                                                                    | Seen by Google |
|------------------|------------|-----------------------------------------------------------------------------------------|----------------|
| static html      | –          | [/html-static](/html-static)               | yes            |
| sync javascript  | ES5        | [/html-dynamic-sync](/html-dynamic-sync)   | yes            |
| async javascript | ES5        | [/html-dynamic-async](/html-dynamic-async) | no             |


## Custom HTML

| Content          | Tag definition | Shadow DOM | Javascript | Link                                                                                                    | Seen by Google |
|------------------|----------------|------------|------------|---------------------------------------------------------------------------------------------------------|----------------|
| static html      | undefined      | —          | —          | [/undefined-static](/undefined-static)                     | yes            |
| static html      | immediate      | yes        | ES5        | [/shadow-static-sync-es5](/shadow-static-sync-es5)         | yes            |
| static html      | immediate      | yes        | ES6        | [/shadow-static-sync](/shadow-static-sync)                 | yes            |
| static html      | lazy           | yes        | ES6        | [/shadow-static-async](/shadow-static-async)               | yes            |
| sync javascript  | immediate      | no         | ES5        | [/noshadow-dynamic-sync-es5](/noshadow-dynamic-sync-es5)   | no             |
| sync javascript  | immediate      | no         | ES6        | [/noshadow-dynamic-sync](/noshadow-dynamic-sync)           | no             |
| sync javascript  | immediate      | yes        | ES5        | [/shadow-dynamic-sync-es5](/shadow-dynamic-sync-es5)       | no             |
| sync javascript  | immediate      | yes        | ES6        | [/shadow-dynamic-sync](/shadow-dynamic-sync)               | no             |
| async javascript | lazy           | no         | ES6        | [/noshadow-dynamic-async](/noshadow-dynamic-async)         | no             |
| async javascript | lazy           | yes        | ES6        | [/shadow-dynamic-async](/shadow-dynamic-async)             | no             |

### Conclusion

Google can always see static HTML content on the page, in standard or custom HTML tags.

When it comes to Javascript-rendered content, Google completely ignores custom HTML tags but not standard ones.

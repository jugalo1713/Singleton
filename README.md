# Singleton

Singleton is a creational design pattern, which ensures that only one object of its kind exists and provides a single point of access to it for any other code.

## Benefits of Singleton Pattern

1. Ensure that a class has just a single instance
2. Provide a global access point to that instance

## How to use it

1. Create a sealed class
2. Use a private constructor
3. Create a private static instance of the class
4. Create a public static property that returns the instanced class or if null then creates one

## When to use it

Use singleton when the service is:

- shared globally
- thread-safe
- stateless OR intentionally shared-state
- expensive to recreate
- independent from individual users/requests

Avoid singleton when the service:

- stores per-user data
- depends on request context
- is not thread-safe
- changes state frequently

Good use cases

- Configuration or settings providers
- Logging services
- Cache services
- Expensive-to-create services
- Stateless utility services

## Important notes

In .Net there is no need to manually create Singleton classes, it can be done using the framework and registering the classes as singleton service

```
builder.Services.AddSingleton<IMyService, MyService>();
```

Then just use dependency injection to use it

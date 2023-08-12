# Angular-Universal-SSR
 Server side rendering  in Angular


 # Create angular project 
 ```
ng new  angular-universal
 ```

To add server-side rendering (SSR) to an Angular project, follow these steps:

1. Install Angular Universal: First, install Angular Universal, which is the library used for SSR in Angular projects. Use the following command to add it to your project:
   ```
   ng add @nguniversal/express-engine@14.2.0
   ```



6. Build and Run: To build your Angular app with SSR, use the following command:
   ```
   npm run build:ssr
   ```
   To run the server, use:
   ```
   npm run serve:ssr
   ```

That's it! Now your Angular app should be set up with server-side rendering. This will improve SEO, initial load times, and overall performance for your application.

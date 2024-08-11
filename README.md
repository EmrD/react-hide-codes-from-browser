****Hide React Codes From Browser****
If you want to hide your codes in production deployment; you can do this with React.

**To hide codes, follow these steps**
1. Add this code to your build script in ```package.json```:

   ```
   GENERATE_SOURCEMAP=false
   ```
   
3. Run your build script, for example

   ```
   npm run build
   ```
   
4. Just add your ```dist``` folder to production server.
5. Test your app.

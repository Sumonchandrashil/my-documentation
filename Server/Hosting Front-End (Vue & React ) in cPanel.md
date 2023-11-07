### Deploy Front End

1. Set the backend URL in `env.js`:

   Open your `env.js` file and set the backend URL to your Laravel project's API endpoint. For example:
   ```javascript
   static PRODUCTION = 'https://bulk-erp-backend.magrepo.com/';
   ```

2. Enable production mode in `vite.config.js`:

   Open your `vite.config.js` file and set the mode to 'production':
   ```javascript
   mode: 'production',
   ```

3. Build your Vue.js project:

   Run the following command to build your Vue.js project:
   ```
   npm run build
   ```

4. Upload the build files to the server:

   Using an FTP client or the cPanel File Manager, upload the contents of the `dist` or `build` directory generated in the previous step to your cPanel hosting account.

5. Edit or create an `.htaccess` file in your project's root directory:

   If the `.htaccess` file doesn't exist, create one and add the following rules to handle routing in a Vue.js application:
   ```
	<IfModule mod_rewrite.c>
		RewriteEngine On
		RewriteBase /
		RewriteRule ^index\.html$ - [L]
		RewriteCond %{REQUEST_FILENAME} !-f
		RewriteCond %{REQUEST_FILENAME} !-d
		RewriteRule . /index.html [L]
	</IfModule>   
   ```

   These rules ensure that your Vue.js routes work correctly without needing to include `#` in the URLs.
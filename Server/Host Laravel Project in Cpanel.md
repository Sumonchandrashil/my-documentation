### Deploy Laravel Project

1. Clone the project repository:
   ```
   git clone [repository_url]
   ```

2. Switch to the correct branch:
   ```
   git checkout [branch_name]
   ```

3. Pull the latest changes from the branch:
   ```
   git pull
   ```

4. Update Composer dependencies:
   ```
   composer update
   ```

5. Copy the example environment file:
   ```
   cp .env.example .env
   ```

6. Generate an application key:
   ```
   php artisan key:generate
   ```

7. Database:
   - Create a database
   - Create a database user.
   - Assign the database user to the database with the required privileges.
   - Import your database dump, if available.

8. *Install Passport for API authentication*:
   ```
   php artisan passport:install
   ```

9. Set the database credentials in your `.env` file.

10. Optimize the application for better performance:
    ```
    php artisan optimize
    ```

11. Edit or create an `.htaccess` file in your project's root directory. If it doesn't exist, create one and add the following rules:

   ```
   	RewriteEngine on
	RewriteRule ^$ public/ [L]
	RewriteRule ((?s).*) public/$1 [L]
   ```

12. Create an `index.php` file in the root directory of your domain or subdomain. This file should point to the `public` directory of your Laravel project.

### Ignoring */public* from the Site URL

To ignore `/public` from the site URL, you need to set up the `index.php` file in your root (usually domain or subdomain) to point to the `public` directory.

### Upgrading PHP

To upgrade PHP using cPanel:

1. Search for "Select PHP Version" in the cPanel's search bar.

2. In the PHP version manager, choose the desired PHP version you want to upgrade to and save the changes.
# Baochip Static Website

This project is a custom-built static website for Baochip, created using a customized version of the Bootstrap framework.

## Project Structure

The project is organized into two main parts:

-   **Source Files (`scss/`)**: This directory contains the source Sass files used to generate the site's custom stylesheet. Any changes to the site's styling should be made in `scss/custom.scss`.
-   **Distribution Files (`dist/`)**: This directory contains the final, self-contained website ready for deployment. All the necessary HTML, CSS, JavaScript, and image files are located here. **You should not edit files in this directory directly**, as they will be overwritten during the build process. However, these should be fairly evergreen and can be edited directly if need be without using the build tools.

## How to Compile the Custom CSS

To make changes to the website's styling, you must edit the source Sass files and then recompile them into a final CSS file.

### Step 1: Install Dependencies

This project requires Bootstrap as a development dependency. Navigate to the project's root directory in your terminal and run the following command to install it:

```bash
npm install bootstrap
```
This will create a `node_modules` directory in your project.

### Step 2: Compile the CSS

After making your desired changes in the `scss/custom.scss` file, run the following command from the project's root directory to compile the Sass into the final CSS file located in the `dist/` folder:

```bash
sass --load-path=node_modules scss/custom.scss dist/custom.css
```

This command does the following:
-   `--load-path=node_modules`: Tells Sass to look inside the `node_modules` directory to find the Bootstrap source files.
-   `scss/custom.scss`: Specifies the input source file.
-   `dist/custom.css`: Specifies the output destination and filename.

Your changes will now be live in the `dist/index.html` file.

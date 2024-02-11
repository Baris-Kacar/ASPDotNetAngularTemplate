# Installation
Before running the project locally, ensure that you have Node.js and npm installed on your system.

1. Clone this repository to your local machine.
2. Navigate to the ClientApp directory:  `cd ClientApp`
4. Run the command `npm install` to install the required npm packages.

**Note**: To run ASP.NET applications on Windows, the "Internet Information Services (IIS)" Windows feature must be enabled. Please follow the instructions below to enable it:

1. Open the Windows Control Panel.
2. Navigate to "Programs" and select "Programs and Features."
3. Click on "Turn Windows features on or off."
4. Look for "Internet Information Services (IIS)" in the list of features.
5. Check the box next to "Internet Information Services (IIS)."
6. Click "OK" to apply the changes. Windows will install and configure Internet Information Services (IIS).

# Version
This project utilizes the following versions of .NET and Angular:

- **.NET**: Version 8
- **Angular**: Version 17

# Running the Project
After completing the installation, you can run the project as follows:

Either enter `dotnet build` via the terminal or:

1. Start your preferred Integrated Development Environment (IDE).
2. Select IIS Express as your execution environment. ![Untitled](https://github.com/Baris-Kacar/ASPDotNetAngularTemplate/assets/73958902/6d3df261-dde8-4ecc-820a-8f245583ae4e)
3. Wait until the server is fully started. ![NPM](https://github.com/Baris-Kacar/ASPDotNetAngularTemplate/assets/73958902/14ffb1b8-1718-4637-853e-599bb2442984)  ![SPAProxy](https://github.com/Baris-Kacar/ASPDotNetAngularTemplate/assets/73958902/522d8ef5-ae79-4e68-9c89-f3e455266567)
4. You will automatically be redirected to the Angular page. ![Capture](https://github.com/Baris-Kacar/ASPDotNetAngularTemplate/assets/73958902/ff6e2520-4270-4d2e-b507-8baf1a337588)

## Creating a Dotnet Project Template
To make this template readily available for repeated use, you can install it as a Dotnet project template. This allows you to quickly scaffold projects based on this template without having to recreate it manually each time.

Below is an example of a template.json file: <br>
```json
{
  "$schema": "http://json.schemastore.org/template",
  "author": "Baris Kacar",
  "classifications": [ "Web", "MVC", "Angular" ],
  "identity": "PBIntelligence",
  "name": "ASP.NET Core Angular (SPA)",
  "shortName": "angularSPA",
  "sourceName":"DotNetSPA",
  "description": "This is a template for an ASP.Net Core project with .NET 8 and Angular v17 (SPA).",
  "tags": {
    "language": "C#",
    "type": "project"
  }
}
````
Explanation of template.json metadata:
- $schema: A reference to the schema used to validate the structure of the template.json file.
- author: The author of the template.
- classifications: A list of classifications describing the template, such as various frameworks, libraries, or patterns used in the template.
- identity: The unique identity of the template.
- name: The full name of the template.
- shortName: A shorter name or alias for the template.
- sourceName: The name under which the template is identified in source code.
- description: A brief description explaining the template and its usage.
- tags: Additional tags or keywords describing the template. These can be used for categorization and searching for templates.

Once the template.json is defined, you can create and package the template to make it available either locally or globally. Use the following command:<br>
`dotnet new --install` <br> <br>
Now, you can navigate to the directory where you want to use the project template and enter the following command: <br>
`dotnet new angularSPA` <br><br>
After creating the project, you need to build it to ensure all dependencies are resolved and the project is ready for execution.
1. **Build the Project**: Navigate to the root directory of your project and execute the following command to build it: <br>
   `dotnet build` <br>
  This command will compile the project and generate the necessary output files.

## What is an SPA Proxy?
An SPA Proxy is an intermediary between your backend server and your frontend framework. It acts as a mediator that receives requests from your backend server and forwards them to your frontend development server. The proxy patiently waits until the frontend development server is fully started before forwarding requests.

An SPA Proxy (Single Page Application Proxy) is a mechanism used to forward requests from a web server to a Single Page Application (SPA) hosted separately from a backend server. This is especially useful when the SPA and the backend are hosted on different servers or ports.

In the context of ASP.NET Core and Angular, the SPA Proxy could function as follows:

- The backend server using ASP.NET Core runs on a specific port (44345).
- The Angular SPA runs separately on another port (44422) using the Angular CLI server (with ng serve).
- Since both servers run separately, the SPA Proxy can be configured on the backend server to forward requests to the Angular SPA when it runs on a different port.

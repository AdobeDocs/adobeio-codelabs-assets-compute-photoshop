## Lesson 1: Create a Firefly app from the Asset Compute template

To begin this codelab, you should have [a project already created from Project Firefly Template in Adobe Developer Console](https://github.com/AdobeDocs/project-firefly/blob/master/getting_started/first_app.md#2-creating-a-new-project-on-developer-console). Please add the `Asset Compute` and `Adobe Photoshop APIs (Trial)` services to the workspace that you are using for the codelab.

![Console Workspace](assets/console-workspace.png)

Make sure to have the Adobe I/O CLI installed locally. In your terminal, execute the command `aio app init <app-name>`.

If you have not logged in already, this command prompts a browser asking you to sign into the Adobe Developer Console with your Adobe ID. See [here](https://github.com/AdobeDocs/project-firefly/blob/master/getting_started/first_app.md#3-signing-in-from-cli) for more information on signing in from the cli.

After logging in, follow the prompts in the CLI and select the Organization, Project, and Workspace to use for the application. Choose the project and workspace you created when you set up your environment.

```bash
$ aio app init <app-name>
Retrieving information from [!DNL Adobe I/O] Console.
? Select Org My Adobe Org
? Select Project MyFireflyProject
? Select Workspace myworkspace
create console.json
```

When prompted with `Which Adobe I/O App features do you want to enable for this project?`, select `Actions`. Make sure to **deselect** `Web Assets` option as web assets use different authentication and authorization checks.

```bash
? Which Adobe I/O App features do you want to enable for this project?
select components to include (Press <space> to select, <a> to toggle all, <i> to invert selection)
❯◉ Actions: Deploy Runtime actions
 ◯ Events: Publish to Adobe I/O Events
 ◯ Web Assets: Deploy hosted static assets
 ◯ CI/CD: Include GitHub Actions based workflows for Build, Test and Deploy
```

When prompted `Which type of sample actions do you want to create?`, make sure to select `Adobe Asset Compute Worker`:

```bash
? Which type of sample actions do you want to create?
Select type of actions to generate
 ◯ Generic
❯◉ Adobe Asset Compute Worker
```

Follow the rest of the prompts and open the new application in Visual Studio Code (or your favorite code editor). It contains the scaffolding and sample code for a custom application.

The template application leverages the [Asset Compute SDK](https://github.com/adobe/asset-compute-sdk) for the uploading, downloading, and orchestration of application renditions so developers only need to implement the custom application logic. Inside the `actions/<worker-name>` folder, the `index.js` file is where to add the custom application code.

Next lesson: [Configure the app](lesson2.md)
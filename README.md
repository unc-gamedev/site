# UNC Club Wiki

Website for the UNC-CH Game Development Club. Contains club information, schedules, ongoing projects, internal/external resources, archives of example projects, and links to other pages.

## Developer Setup

Download the required dependencies.

### Angular Frontend

```bash
cd frontend
npm install
```

### FastAPI + PostgreSQL Backend

```bash
cd backend
python -m pip install -r requirements.txt
```

### MkDocs

`cd /docs`\
Download latest versions of Python and pip (package manager for Python)\
Install all python module requirements with `python -m pip install -r requirements.txt` (may not need `python -m` part depending on your python installation).\
The exact dependencies can be found in `requirements.txt`. For now, this will install MkDocs and MkDocs Material on your machine.

## Contributing

### Edit site contents (frontend)

Open a new terminal.\
Run the frontend on http://localhost:4200 with

```bash
cd frontend
ng serve
```

The site will auto-reload. Make changes in the `frontend/src` folder, where all the site pages are located.
Read the frontend README file for some resources on how to use Angular.
Each page of the site is in its own folder and has its own html, ts and css file. Edit the contents of the HTML to edit the site appearance.

### Edit models and databases (backend)

Open a new terminal.\
Run the backend on http://localhost:8000:

```bash
cd backend
fastapi dev main.py
```

The server will auto-reload. Make changes in the `backend` folder.

### Edit documentation and resources (documentation)

Edit overarching site navigation in `mkdocs.yml`.\
Use Markdown format to directly edit relevant .md files under `/docs`. MkDocs might not support certain syntax, such as \ for line breaks.\
Run `mkdocs serve` to preview your changes on a local server (default <http://127.0.0.1:8000/>) This also enables live reload, so you can see your changes as you write them.
Run `mkdocs build` to regenerate the `site/` directory containing the actual site pages. To stop the local server, press Ctrl+C in the command line where it's running.\
Please remain close to best practices when creating and naming branches, naming commits and writing descriptions. If you do not know what they are, refer to <https://gist.github.com/luismts/495d982e8c5b1a0ced4a57cf3d93cf60> for more details.

## DevOps

### CI/CD with GitHub Pages

This step is a work in progress and is yet to follow best practices.\
When any change is pushed to main, GitHub Actions will automatically run the workflow to deploy the changes to a gh-pages branch hosted on GH Pages. Therefore, you do not need to `build` or `serve` as long as the .md files are correct, though it may be helpful for your own reference.\
With that said, preview your changes locally before pushing, please.\
Alternatively, create a new branch with your changes and open a pull request for review.\
If you visit the deployed site more than once, there's a chance you'll have to do a hard refresh to clear your browser cache to see updates it due to it being static - this is `shift + F5` on most browsers.

## Further resources

For full documentation visit [mkdocs.org](https://www.mkdocs.org).\
You can use `mkdocs -h` to view help options.

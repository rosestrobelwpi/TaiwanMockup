## arcwww03 auto-deployed website template
This is a template for websites which will be deployed through Gitlab's CI system to the webhost on arcwww03.

## Setup steps:

1. Fork repository
2. Add `arcwww03` user to new repository
3. Add site info to ansible
4. deploy ansible's `arc.yml` (`-l arcwww03`)

## Site setup & Usage:

- Put all files which will be directly served in html/
- Put stuff that should not be accessible from the Internet anywhere else
- Use local clone, or gitlab webIDE to edit files
- Upon push (or webui commit), gitlab will automatically trigger the updated content to go to the web server

### git-lfs

For storing binary content such as images or video, please use git-lfs rather than storing directly in git.
The repository comes pre-configured for most common file types, but if you're cloning locally, you'll likely need the `git-lfs` package installed (e.g. via `sudo apt install git-lfs; git lfs install`).

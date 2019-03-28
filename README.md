# links
jekyll site for useful links populated by staticmanapp.

**This repo is only compatible with my [staticman fork](https://github.com/ujjwal96/staticman/tree/production) (as of now)**  
To self host staticman API see [this](https://gist.github.com/ujjwal96/70eabafefa8c2e3f5fa900f352f16c5e)

## Setting up
1. Add the user whose github token is used while hosting the API as a collaborator to this repo.
2. Go to `https://<api url>/v2/connect/{your GitHub username}/{your repository name}` to accept collaborator invite.
3. Generate a unique token (uuid) and open `https://<api url>/v2/encrypt/<unique token>`
4. Save the output from above in `staticman.yml` with `staticmanToken` key.
5. Use the decrypted token in all the entry requests sent as `options[staticman-token]`

## Adding categories
* Make changes to `_config.yml` under `collections:` and `defaults:`
* Add `<category>.md` to `_pages`
* Edit `_data/navigation.yml` to add categories to nav bar

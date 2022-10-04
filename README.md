# ui-plugin-examples
Example plugins for the Rancher Dashboard UI.

This repository contains 2 example plugins in the `pkg` folder.

|Name|Description|
|----|-----------|
|homepage|Plugin that changes the landing home page|
|new-feature|Plugin that adds a new feature to the top-level slide-in menu|

> Note: Currently, only the 'homepage' plugin is published to the Helm Chart repository.

You can find the built packages for these plugins in the [releases](https://github.com/rancher/ui-plugin-examples/releases) section of this GitHub repository. These are assets named in the form `[plugin-name]-[version].tgz`.

Additionally, fake Helm charts for the plugins are published to the releases as well - these currently only contain enough metadata to test the UI Plugin catalog. These are assets named in the form `[plugin-name]-chart-[version].tgz`.

You can also add this repository as a Helm Repository in Rancher - to do this:

- Go to the local cluster, to 'Apps' and 'Repositories'
- Click 'Create' and enter a name, e.g. 'ui-plugin-examples'
- Choose Target 'Git repository containing Helm chart or cluster template definitions'
- Enter `https://github.com/rancher/ui-plugin-examples.git` for the 'Git Repo URL'
- Enter `main` for the Git Branch
- Click `Create`

## Building and running locally

You can build and run the plugins locally, to do so:

- Run `yarn install`
- Set the API environment variable to point to a Rancher backend
- Run Rancher in development mode with `yarn dev`
- Open a web browser to `https://127.0.0.1:8005`

Once you login, you should see Rancher load with the two plugins automatically loaded. You can edit the code for the plugins
and then should hot-reload within the browser.

### Bugs & Issues
Please submit bugs and issues to [rancher/dashboard](//github.com/rancher/dashboard/issues).

Or just [click here](//github.com/rancher/dashboard/issues/new) to create a new issue.

License
=======
Copyright (c) 2014-2022 [Rancher Labs, Inc.](http://rancher.com)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

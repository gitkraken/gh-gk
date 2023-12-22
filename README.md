
# 🚀 GitKraken CLI Extension

`gk` is the GitKraken command line extension to GitHub CLI (`gh`).  It makes working across multiple repos easier with Workspaces, provides access to pull requests and issues from multiple services (GitHub, GitLab, Bitbucket, etc.), and seamlessly connects with [GitKraken Client](https://www.gitkraken.com/git-client) and [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) in VS Code to visualize `git` information when you need it.

<p align="center">
<img src="https://user-images.githubusercontent.com/86774052/225326381-aaea81a3-9f19-4170-9e0b-2f42fac8edda.png" style="margin: 0 auto" />
</p>

GitKraken CLI is available on macOS, Windows and Unix systems.

## 📚 Documentation

Check out the [installation instructions](#installation) and [examples](#examples) below. For command usage [see the docs][documentation].

## Installation

```sh
 gh extension install gitkraken/gh-gk
```


## Updating extension

```sh
gh extension upgrade gitkraken/gh-gk
```

## Uninstalling extension

```sh
gh extension remove gitkraken/gh-gk
```

## ⚙️ Configuration
### Nerd Fonts
The GitKraken CLI supports Nerd Fonts to display icons for some commands. To ensure correct icon rendering, please obtain and install a Nerd Font available at https://www.nerdfonts.com/. After installation, set the selected Nerd Font as the default font for your terminal.

## Examples
### 🤝 Create Workspaces to group repos
```
gh gk ws create
```
GitKraken workspaces associate groups of repos and set the context for helpful commands that can operate on, or get information for, multiple repos at once. There are two types of workspaces:
##### Local
Local Workspaces exist only on your machine.
##### Cloud
Cloud Workspaces are accessible on any machine, and can be connected to hosting and issue providers like GitHub and GitLab to get additional information about pull requests and issues. Share Cloud Workspaces with your team to improve onboarding with the ability to clone all repos at once. To enable this extra functionality, Cloud Workspaces require a free GitKraken account. We are continuing to evolve and improve GitKraken Workspaces and welcome any feedback.

![Screenshot 2023-12-22 at 10 34 29 AM](https://github.com/gitkraken/gh-gk/assets/115040794/8786324d-cabe-425f-94aa-cdfab12b928a)

#### Adding and locating repos
```
gh gk ws add-repo
```
This will add a new repo to a workspace either by path or remote URL.
```
gh gk ws locate
```
If you're accessing a Cloud Workspace for the first time, you might need to `locate` the local repos on your machine. Run this command in the directory where youre repos are located so `gk` knows where they are.
```
gh gk ws clone
```
You can also `clone` all repos in a Workspace at once into a single directory. This is helpful for onboarding when your team works on multiple repos.

### 🎬 Perform `git` actions on multiple repos at once
```
gh gk ws [action]
```
In any workspace, you can perform `git` operations like `fetch`, `pull`, `push`, and `checkout` across all repos in the workspace.

### 📋 Get pull requests and issues
```
gh gk provider add
```
Before fetching pull requests and issues, ensure that you have the appropriate provider (GitHub, GitLab, etc.) connected. This will open a browser to authenticate.

```
gh gk pr list
```
When a Cloud Workspace has a provider connected, you can list all pull requests and issues for repos in the workspace, and view details for a specific one.

![gh-gk-pr-list-screenshot](https://github.com/gitkraken/gh-gk/assets/115040794/4579ed18-8457-4834-a640-27797d4ec093)

```
gh gk pr view
```
Returns a list of all pull requests for all repos in a workspace. Type to search for a specific pull request and press `enter` to view details.

![Screenshot 2023-12-22 at 10 22 30 AM](https://github.com/gitkraken/gh-gk/assets/115040794/bd1a79ee-fd79-444a-b910-c17ef14a973b)

### 📈 Pull Request Insights
```
gh gk ws insights
```
See the following metrics for all repositories in a Cloud Workspace. The default time period is 7 days, but can be increased to 14 days with any paid GitKraken license.
- Average Cycle Time
- Average Throughput
- Merge Rate
- Opened Pull Requests
- Merged Pull Requests
- Closed Pull Requests

![gh-gk-insights-screenshot](https://github.com/gitkraken/gh-gk/assets/115040794/3d1eb72b-5e8d-4c2f-b1a7-de13714ceba4)


### ✨ Visual Commit Graph
```
gh gk graph
```
Open a visual graph of the repo in your current directory in either [GitKraken Client](https://www.gitkraken.com/git-client) or [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) in VS Code.

https://github.com/gitkraken/gh-gk/assets/115040794/9ac6bc82-3596-4544-b3c7-c6966cfd09fd

[documentation]: https://gitkraken.github.io/gk-cli/
[releases page]: https://github.com/gitkraken/gh-gk/releases/latest

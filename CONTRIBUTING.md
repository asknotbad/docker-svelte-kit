# Contributing

## Contents

  - [Instructions](#instructions)

## Instructions

1. Fork the repository.

1. Create a new branch:

   ```bash
   git branch new-branch
   ```

1. Checkout new branch:

   ```bash
   git checkout new-branch
   ```

1. Add, commit and push your changes to the new branch

   ```bash
   git add .
   git commit -m "changes"
   git push origin new-branch
   ```

1. To make sure your forked repository is up to date with this repository. Add this repository as the upstream repository by doing the following:

   ```bash
   git remote add upstream https://github.com/asknotbad/docker-svelte-kit.git
   ```

   Then, to fetch from this repository:
   
   ```bash
   git fetch upstream
   git merge upstream/main main
   ```

1. Go to your forked repository and press the “New pull request” button.
   
1. Once the pull request is reviewed and approved, it will be merged.

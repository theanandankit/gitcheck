# gitcheck

This is demo app

## Submitting a PR

If you have a specific idea of a fix or update, follow these steps below to submit a PR:

- [Step 1: Make the change](#step-1-make-the-change)
- [Step 2: Commit and push your changes](#step-2-commit-and-push-your-changes)
- [Step 3: Create a pull request](#step-3-create-a-pull-request)

### Step 1: Make the change

1. Fork the Chaos Mesh repo, and then clone it:

   ```bash
   $ export user={your github. profile name}
   $ git clone git@github.com:${user}/gitcheck.git
   ```
2. Set your cloned local to track the upstream repository:

   ```bash
   $ cd gitcheck
   $ git remote add upstream https://github.com/manishdangi98/gitcheck
   ```

3. Disable pushing to upstream master:

   ```bash
   $ git remote set-url --push upstream no_push
   $ git remote -v
   ```

   The output should look like:

   ```bash
   origin    git@github.com:$(user)/gitcheck.git (fetch)
   origin    git@github.com:$(user)/gitcheck.git (push)
   upstream  https://github.com/manishdangi98/gitcheck (fetch)
   upstream  no_push (push)
   ```
4. Get your local master up-to-date and create your working branch:

   ```bash
   $ git fetch upstream
   $ git checkout master
   $ git rebase upstream/master
   $ git checkout -b myfeature
   
### Step 2: Commit and push your changes

Congratulations! Now you have finished all tests and are ready to commit your code.

1. Run the following commands to keep your branch in sync:

   ```bash
   $ git fetch upstream
   $ git rebase upstream/master
   ```

2. Commit your changes:

   ```bash
   $ git add -A
   $ git commit --signoff
   ```

3. Push your changes to the remote branch:

   ```bash
   $ git push -f origin myfeature
   ```

### Step 3: Create a pull request

1. Visit your fork at <https://github.com/manishdangi98/gitcheck> (replace the first chaos-mesh with your username).
2. Click the Compare & pull request button next to your `myfeature` branch.
3. Edit the description of the pull request to match your changes.

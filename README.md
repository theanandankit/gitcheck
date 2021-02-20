# gitcheck

this is demo app

## Submitting a PR

If you have a specific idea of a fix or update, follow these steps below to submit a PR:

- [Step 1: Make the change](#step-1-make-the-change)


### Step 1: Make the change

1. Fork the Chaos Mesh repo, and then clone it:

   ```bash
   $ export user={your github. profile name}
   $ git clone git@github.com:${user}/gitcheck.git
   ```
2. Set your cloned local to track the upstream repository:

   ```bash
   $ cd chaos-mesh
   $ git remote add upstream https://github.com/chaos-mesh/chaos-mesh
   ```

3. Disable pushing to upstream master:

   ```bash
   $ git remote set-url --push upstream no_push
   $ git remote -v
   ```

   The output should look like:

   ```bash
   origin    git@github.com:$(user)/chaos-mesh.git (fetch)
   origin    git@github.com:$(user)/chaos-mesh.git (push)
   upstream  https://github.com/chaos-mesh/chaos-mesh (fetch)
   upstream  no_push (push)
   ```

# aqua-dv-git-sync-template

Template for the **Git** part of a Code Ocean deployment verification run (commit and push with
Git Sync). The run needs a repository that the tester **can push to**, so don't use this public
repository directly. Make your own copy:

1. Click **Use this template > Create a new repository** on GitHub.
2. Put the copy in your own account or organization. **Private** is fine and recommended.
3. Make sure the GitHub credential saved in the tester's Code Ocean account (Account > Credentials)
   can read and write the new repository.

Then give its URL to the **deployment-verification** Aqua skill
([aqua-dv-skill](https://github.com/codeocean-nate/aqua-dv-skill)) as `git_repo`. The skill:

1. creates a capsule **linked** to your repository (Clone from Git);
2. appends a line to `code/dv-git-check.md` and commits it (checklist §3.1);
3. asks you to press **Sync with GitHub**; Aqua can't push by itself (checklist §3.2);
4. asks you to confirm the commit is on GitHub.

`code/run` only prints the Code Ocean identity banner, so a Reproducible Run of the linked capsule
needs nothing beyond a basic starter environment.

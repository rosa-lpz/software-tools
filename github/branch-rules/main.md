## **Other contributors must use Pull Requests, but the owner of the project can push directly to main** 

GitHub supports this with a **branch ruleset** and a bypass for your account. 

### Recommended setup

Go to your repository:

**Settings → Rules → Rulesets → New ruleset → New branch ruleset**

Configure:

1. **Ruleset name:** `Protect main`
2. **Enforcement status:** `Active`
3. **Target branches:** `main`
4. Enable **Require a pull request before merging**
5. Under **Bypass list**, add **your GitHub account**
6. For your account, choose **Always allow**.

Then contributors who aren't on the bypass list must make a PR to modify `main`, while you can push directly. GitHub explicitly supports bypass actors for rulesets. 

### Even better for an open-source project

 ```github
 YOU
  └── can push directly to main
       └── optional PR for your own changes
 
 CONTRIBUTORS
  └── fork
       └── branch
            └── Pull Request → main
                 └── you review
                      └── merge
 
 ```

```text

```

You can additionally require **1 approval** for contributors' PRs. Note that GitHub's required-review rules can be configured to require approval before merging. 

**One caveat:** if you're using a personal repository,  your repository role as owner/admin may interact with bypass behavior  differently depending on whether you're using a classic branch  protection rule or the newer rulesets. If you tell me whether your repo  is **personal or an organization repo**, I can give you the exact settings to click.





## Rule public github, only owner do commits

Yes. For your **public GitHub repository**, if your desired workflow is:

- **You:** can commit/push directly to `main`.
- **Everyone else:** must use a Pull Request.
- **You:** review and merge contributors' PRs.

The cleanest setup is a **Ruleset**. GitHub supports rulesets in public repositories, including on GitHub Free. 

### Create this rule

Go to:

**Repository → Settings → Rules → Rulesets → New ruleset → New branch ruleset**

Set:

```text
Name:
Protect main

Enforcement status:
Active

Target branches:
main

Branch protections:
☑ Require a pull request before merging
☑ Block force pushes
☑ Restrict deletions
```

The important part is **Require a pull request before merging**. This makes changes to `main` go through a PR. 

### But here's the important part

Under **Bypass list**, add **your GitHub account** and select:

**Always allow**

That means the ruleset applies to contributors, while you can bypass  it and push your own commits directly. GitHub specifically supports  bypass actors for rulesets. 

So your workflow becomes:

```text
YOU
  │
  └── git push → main ✅

CONTRIBUTOR
  │
  ├── fork
  ├── create branch
  ├── make changes
  └── Pull Request → main
                     │
                     └── You review → Merge
```

### One thing I'd recommend

Don't enable **"Require approvals"** unless you actually want another person to approve PRs. The PR requirement itself doesn't necessarily require an approval. 

For your Python notes project, I'd use exactly this simple setup:

**`main` → PR required for contributors + your account bypasses the rule + no force pushes.**

# How to Add a New Offer

Always work on a **new branch** and submit a **pull request (PR) to `main`**. Do **not** commit directly to `main`, because direct commits don't notify people watching the repo. PRs do.

## Steps

### 1. Update your local `main`

```bash
git checkout main
git pull origin main
```

### 2. Create a new branch

Use a short, descriptive name.

```bash
git checkout -b add-offer-<short-offer-name>
# example: git checkout -b add-offer-data-days-2026
```

### 3. Add the offer

1. Create a new folder at the repo root named after the offer, in lowercase with hyphens (example: `data-days-exam-voucher-2026`).
2. Inside it, add a `README.md` with:
   - Offer title and a one-line summary
   - Register / claim button or link
   - Active period (dates and time zone)
   - Quick summary (what you do, reward, deadlines, limits)
   - Eligibility and steps to participate
   - Official source link
3. Put any images in an `images/` folder inside the offer folder.
4. Open the main [README.md](./README.md) and:
   - Add a new row at the **top** of the **Opportunities** table (renumber the `#` column).
   - Add a matching entry at the **top** of the **Opportunity List**.
   - Set the status: 🟢 Upcoming / Active, 🟡 Ending soon, or 🔴 Closed / Expired.
5. Verify the details against the official Microsoft source, and check that all links work.

### 4. Commit to your branch

```bash
git add .
git commit -m "Add <offer name> offer"
```

### 5. Push the branch

```bash
git push -u origin add-offer-<short-offer-name>
```

### 6. Open a pull request to `main`

1. Go to the repository on GitHub and click **Compare & pull request**.
2. Set the base branch to `main` and the compare branch to your new branch.
3. Give the PR a clear title (example: `Add Data Days exam voucher offer`) and a short description with the official source link.
4. Click **Create pull request**, then merge it after review.

Watchers are notified when the PR is opened and merged.

## Updating or expiring an existing offer

Follow the same flow: new branch → edit → commit → PR to `main`. For an expired offer, change its status to 🔴 Closed / Expired in the main README table.

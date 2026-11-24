# Current AWS operation and GitHub source guidance

Updated: **24 November 2026**.

## Operating environment

CRAYS development, builds, testing, previews and server operation now use **AWS**. This is the current human-confirmed operating decision. Vercel hosting, Neon databases, XXL build instructions and local-machine paths in older source captures are historical context, not current deployment instructions.

AWS operation does not mean that every application feature, provider connection, booking, payment, permission check or data workflow has passed acceptance. Preserve each product's actual validation and release boundaries.

## Find the current source

- [Repository guide](repositories.md): 26 repositories, 19 public and 7 private at this check.
- [crays-web](https://github.com/CraysWorld/crays-web) (private): shared web release assembly. Its `preview` branch contains release inputs and packaging; `main` provides navigation.
- [crays-platform](https://github.com/CraysWorld/crays-platform): preserved shared application, service and operations source. Named snapshots retain their original scope.
- [crays-openclaw](https://github.com/CraysWorld/crays-openclaw) (private): independent source-owner branches. Use its current branch index; early pinned capsules remain historical snapshots.
- Each website and native app retains its original repository, history and notices. Archived upstream forks remain read-only historical references.

## Source updates and release versions

A GitHub commit, a framework build ID, a container/image digest and an AWS deployment job identify different things. The latest branch commit can belong to a cancelled or failed deployment. Use the selected release inputs and the actual successful job together before calling a version published.

GitHub synchronisation must not start a deployment. For the shared Amplify preview, automatic branch builds, automatic branch creation and PR previews were confirmed disabled during this check. Publishing and production routing require their existing separate authorisation; no deployment was started for this documentation update.

## One-time check limits

This pass checked the organisation inventory, default-branch entry points, current component/source branches and the shared preview's publication metadata. It corrected current hosting/navigation statements. It did not republish arbitrary local working trees, merge independent product branches, run native programs, inspect credentials or test all application features.

The retained development trees include modified source and local history that cannot be treated as approved public source solely because a file exists. Exact source coverage and outstanding checkpoint questions are recorded separately from the AWS hosting decision. Secrets, customer data and private runtime bindings remain outside public repositories.

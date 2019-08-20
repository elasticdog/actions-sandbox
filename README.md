# actions-sandbox

## Notes

- Even though the `$GITHUB_TOKEN` secret changes for each run, they appear to be
  using regular GitHub Application credentials tied to @github-actions and they
  don't expire until an hour after creation. I was able to use a token to post a
  status on the [initial commit][]. Just something to keep in mind.

- There are some documented [Workflow Limitations][].

[initial commit]:
  https://github.com/elasticdog/actions-sandbox/commit/057541729acfb981b38a2034edf8ecea0b0ef7ea
[workflow limitations]:
  https://developer.github.com/actions/managing-workflows/workflow-configuration-options/#workflow-limitations

## Unanswered Questions

### Can you delete the build logs for an individual run?

I haven't seen a way to do this in the UI or from any of the checks/status APIs.

### Are scheduled jobs only available to run from the master branch?

It didn't seem like the stale issue check was running from
https://github.com/elasticdog/actions-sandbox/pull/8 until I merged it into the
`master` branch. We'll have to see if that's a known limitation, a config I may
have missed, or something else.

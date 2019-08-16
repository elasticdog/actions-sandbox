# actions-sandbox

## Notes

- Even though the `$GITHUB_TOKEN` secret changes for each run, it looks like
  they don't expire...at least not right away. 10 minutes after a run, I was
  able to use a token to post a status on the [initial commit][].

[initial commit]:
  https://github.com/elasticdog/actions-sandbox/commit/057541729acfb981b38a2034edf8ecea0b0ef7ea

## Unanswered Questions

### Can you delete the build logs for an individual run?

I haven't seen a way to do this in the UI or from any of the checks/status APIs.

### How do you prevent unauthorized users from adding jobs to exfiltrate secrets?

If the user can create a pull request, what stops them from adding a workflow
that dumps out secrets?

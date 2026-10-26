# lizard-build/checkout

A drop-in replacement for [`actions/checkout`](https://github.com/actions/checkout) for
[Lizard](https://lizard.build) GitHub Actions runners (`runs-on: lizard-<n>vcpu-ubuntu-2404`).

```yaml
- uses: lizard-build/checkout@v1
```

On a Lizard runner with a lasting cache disk (private repositories), the repository is mirrored on
that disk: each job brings the mirror up to date (only new commits travel) and the checkout borrows
its objects. Everywhere else it is `actions/checkout`, with the same inputs and outputs.

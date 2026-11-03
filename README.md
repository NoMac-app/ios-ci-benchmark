# iOS CI benchmark

The Wikipedia iOS app's own unit tests, run on two macOS CI runners side by side:

- **GitHub-hosted:** `runs-on: xcode-27`, GitHub's standard macOS runner with the Xcode 27 image (3 cores and 7 GB of an M1).
- **NoMac CI:** `runs-on: nomac` ([nomac.app/ci](https://nomac.app/ci)), 6 cores and 8 GB of an Apple M4 to M6.

Both run the same job: [wikimedia/wikipedia-ios](https://github.com/wikimedia/wikipedia-ios) at commit `ca8aaeb9`, the `Wikipedia` scheme's tests from its "Run Unit Tests" workflow, on an iPhone 17 simulator with iOS 27.0, built with Xcode 27.0, from a cold start (no cache). It is the same app and commit used in other published runner benchmarks, so the numbers can be compared.

The workflow is [`.github/workflows/wikipedia-unit-tests.yml`](.github/workflows/wikipedia-unit-tests.yml). Every run is public under [Actions](../../actions), with its timings and logs.

**Result (median of 16 paired runs, November 2 and 3, 2026):** the whole job took 14m 32s on GitHub's runner and 5m 24s on NoMac CI; a run cost 93¢ on GitHub in a private repository (free in a public one) and 9¢ on NoMac CI. GitHub's runner started the job sooner: 4s from queued to running, against 39s.

Details and every run are in [RESULTS.md](RESULTS.md), measured from the GitHub API (each job's start and end, and its build-and-test step), with every run linked. Data: CC BY 4.0.

NoMac makes NoMac CI. Run the workflow in your own fork to check the numbers.

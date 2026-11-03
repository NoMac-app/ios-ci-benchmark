# Results

The Wikipedia iOS app's unit tests (commit `ca8aaeb9`, Wikipedia scheme, 430 tests), Xcode 27.0, iPhone 17 on iOS 27.0, cold. 16 paired runs, November 2 and 3, 2026.

| Median | GitHub-hosted (`xcode-27`) | NoMac CI (`nomac`) |
| --- | --- | --- |
| Whole job | 14m 32s | 5m 24s |
| Build and test | 13m 54s | 4m 48s |
| Waiting for a Mac (queued to running) | 4s | 39s |
| Cost of a run | 93¢ in a private repository (whole minutes at $0.062), free in a public one | 9¢ (the minutes the Mac ran, at NoMac's price that day) |
| Machine | M1, 3 cores, 7 GB | M5 Pro, M6, 6 cores, 8 GB |

Range of the whole job: GitHub 10m 08s to 23m 39s, NoMac CI 4m 50s to 14m 49s. Failed jobs: 1 on GitHub and 1 on NoMac CI, each the app's flaky Swift Testing test `fixtureClientSupportsDownloadTask` (a temporary download file gone before the test reads it), which also made those two runs each side's slowest. They are included above.

Every run:

| Run | Runner | Machine | Result | Waiting | Whole job | Build and test | Tests | Cost |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [41541046556](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41541046556/job/125604998325) | nomac | M5 Pro | passed | 56s | 5m 40s | 5m 13s | 430 | 10.5¢ |
| [41541046556](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41541046556/job/125604998609) | xcode-27 | M1 | passed | 4s | 16m 57s | 16m 33s | 430 | $1.05 |
| [41543800886](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41543800886/job/125614236148) | nomac | M5 Pro | passed | 35s | 5m 40s | 5m 02s | 430 | 9¢ |
| [41543800886](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41543800886/job/125614236600) | xcode-27 | M1 | passed | 3s | 13m 59s | 13m 27s | 430 | 86.8¢ |
| [41543852085](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41543852085/job/125614413675) | nomac | M5 Pro | passed | 44s | 5m 03s | 4m 38s | 430 | 9¢ |
| [41543852085](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41543852085/job/125614413293) | xcode-27 | M1 | passed | 11s | 12m 18s | 11m 52s | 430 | 80.6¢ |
| [41545538284](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41545538284/job/125620100710) | nomac | M5 Pro | passed | 43s | 5m 09s | 4m 43s | 430 | 9¢ |
| [41545538284](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41545538284/job/125620101179) | xcode-27 | M1 | passed | 3s | 16m 10s | 15m 40s | 430 | $1.05 |
| [41545714946](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41545714946/job/125620699805) | nomac | M5 Pro | passed | 40s | 6m 18s | 5m 51s | 430 | 10.5¢ |
| [41545714946](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41545714946/job/125620700162) | xcode-27 | M1 | passed | 2s | 10m 08s | 9m 51s | 430 | 68.2¢ |
| [41547087698](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41547087698/job/125625206451) | nomac | M6 | passed | 34s | 5m 07s | 4m 31s | 430 | 9¢ |
| [41547087698](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41547087698/job/125625206808) | xcode-27 | M1 | failed | 7s | 23m 39s | 23m 09s | 430 | $1.49 |
| [41548983779](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41548983779/job/125631492788) | nomac | M6 | passed | 51s | 5m 33s | 5m 12s | 430 | 10.5¢ |
| [41548983779](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41548983779/job/125631493154) | xcode-27 | M1 | passed | 3s | 11m 40s | 11m 21s | 430 | 74.4¢ |
| [41555202548](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41555202548/job/125652291959) | nomac | M5 Pro | passed | 35s | 5m 21s | 4m 48s | 430 | 9¢ |
| [41555202548](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41555202548/job/125652291287) | xcode-27 | M1 | passed | 3s | 18m 04s | 17m 38s | 430 | $1.18 |
| [41556153583](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41556153583/job/125655421672) | nomac | M6 | passed | 42s | 6m 27s | 5m 56s | 430 | 10.5¢ |
| [41556153583](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41556153583/job/125655421288) | xcode-27 | M1 | passed | 14s | 14m 13s | 12m 46s | 430 | 93¢ |
| [41559896337](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41559896337/job/125667744748) | nomac | M6 | failed | 39s | 14m 49s | 14m 25s | 430 | 24¢ |
| [41559896337](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41559896337/job/125667745112) | xcode-27 | M1 | passed | 4s | 14m 50s | 14m 21s | 430 | 93¢ |
| [41559936743](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41559936743/job/125667873285) | nomac | M5 Pro | passed | 41s | 4m 50s | 4m 33s | 430 | 9¢ |
| [41559936743](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41559936743/job/125667873602) | xcode-27 | M1 | passed | 3s | 14m 56s | 14m 27s | 430 | 93¢ |
| [41561672065](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41561672065/job/125673488376) | nomac | M5 Pro | passed | 31s | 5m 14s | 4m 47s | 430 | 9¢ |
| [41561672065](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41561672065/job/125673488133) | xcode-27 | M1 | passed | 4s | 12m 37s | 12m 15s | 430 | 80.6¢ |
| [41561711711](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41561711711/job/125673620046) | nomac | M5 Pro | passed | 35s | 5m 26s | 4m 46s | 430 | 9¢ |
| [41561711711](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41561711711/job/125673619756) | xcode-27 | M1 | passed | 4s | 16m 45s | 16m 20s | 430 | $1.05 |
| [41563414877](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41563414877/job/125679098713) | nomac | M5 Pro | passed | 34s | 5m 49s | 5m 23s | 430 | 10.5¢ |
| [41563414877](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41563414877/job/125679098920) | xcode-27 | M1 | passed | 4s | 17m 24s | 16m 57s | 430 | $1.12 |
| [41567186564](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41567186564/job/125691402266) | nomac | M5 Pro | passed | 36s | 5m 13s | 4m 41s | 430 | 9¢ |
| [41567186564](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41567186564/job/125691402564) | xcode-27 | M1 | passed | 3s | 13m 17s | 12m 59s | 430 | 86.8¢ |
| [41567227866](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41567227866/job/125691536808) | nomac | M5 Pro | passed | 38s | 4m 56s | 4m 34s | 430 | 9¢ |
| [41567227866](https://github.com/NoMac-app/ios-ci-benchmark/actions/runs/41567227866/job/125691536516) | xcode-27 | M1 | passed | 2s | 10m 53s | 10m 35s | 430 | 68.2¢ |

Times come from the GitHub API (each job's start and end, and its build-and-test step). Data: CC BY 4.0.

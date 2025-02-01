# Firebase Realtime Database QuotaExceededError despite being under quota

This repository demonstrates a scenario where a `QuotaExceededError` is thrown by the Firebase Realtime Database even when the application is well within its defined quota limits. The issue is caused by exceeding rate limits (write operations/connections) rather than data size limits.  This is a common issue that isn't explicitly documented in the Firebase documentation, leading to unexpected application behavior.

The `quotaError.js` file demonstrates the problem, where multiple rapid writes trigger the error. `quotaErrorSolution.js` presents a potential solution implementing exponential backoff to handle temporary rate limit exceedances.
# Upload this project to GitHub

1. Extract the ZIP.
2. Upload the contents of the extracted folder to the root of a GitHub repository.
3. Keep `.github/workflows/build.yml` at that exact path and `Makefile` at the repository root.
4. Open Actions, choose **Build AflatoonMubdi**, then select **Run workflow**.
5. Download the artifact only after the run succeeds.

This is a Theos dylib source project, not a prebuilt IPA. Runtime hook backends require the appropriate supported environment.

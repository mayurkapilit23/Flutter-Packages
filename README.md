# Flutter-Packages

modal_progress_hud_nsn This Flutter package is used to show a loading spinner (progress indicator) over the entire screen while an async task is running (like login or data fetch). It helps block user interaction until the task is complete.

✅ Useful for showing loading during API calls or form submissions.

Example:

    ModalProgressHUD(
      inAsyncCall: isLoading,
      child: YourWidget(),
    )

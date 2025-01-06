# Expo CLI Error: Managed Workflow/Bare Workflow Mismatch

This repository demonstrates a common Expo CLI error related to mismatching managed and bare workflows.  The `bug.js` file shows an example of the problematic code, while `bugSolution.js` provides the solution.

**Problem:** Attempting to use managed workflow features (like `expo build:ios`) in a bare workflow project or bare workflow modules in a managed project leads to errors because the underlying build systems are incompatible.

**Solution:** Ensure consistency between the project's workflow and the features/modules used.  If you are using Expo's managed workflow, don't try to directly interact with native modules without using the appropriate Expo APIs (like `expo install react-native-camera` and using the Expo Camera API).  If using bare workflow, manage builds directly with the native tools.
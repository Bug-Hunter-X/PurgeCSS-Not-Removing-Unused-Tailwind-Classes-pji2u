# PurgeCSS Issue with Unused Tailwind Class

This repository demonstrates a problem where PurgeCSS, used with Tailwind CSS, fails to remove an unused CSS class.  The `text-red-500` class is defined in the Tailwind config but is never actually applied in the code. Yet, it still appears in the final CSS output, leading to unnecessary file size.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run build`. This will build the project using PurgeCSS.
4. Examine the generated CSS file (usually `dist/output.css`).  You'll see the `text-red-500` class is still present even though it's unused.

## Expected Behavior

PurgeCSS should remove unused classes to minimize CSS file size.  The `text-red-500` class should be removed because it is not used anywhere in the JavaScript code.
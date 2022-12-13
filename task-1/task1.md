&#9733; &#9733; &#9733;

1. [Chrome accessability audit devTools](Chrome_audit.png) - **65**:

   - [aria-*] attributes do not match their roles
   - Buttons do not have an accessible name
   - Form elements do not have associated labels
   - Links do not have a discernible name
   - [user-scalable="no"] is used in the <meta name="viewport"> element or the [maximum-scale] attribute is less than 5.
   - Background and foreground colors do not have a sufficient contrast ratio.
   - Lists do not contain only <li> elements and script supporting elements `<script>` and `<template>`.

2. [Siteimprove plugin](Siteimprove_checker.png) - **11 issues**:

- A and AA:
  - Link without a text alternative
  - Button without a text alternative
  - Page zoom is restricted
  - Text not included in an ARIA landmark
  - Container element is empty
  - Color contrast is not sufficient
  - Form field is not labeled
- And also AAA:
  - Line height is below minimum value
  - Font size is fixed
  - Line height is fixed

3. [Wave plugin](WAVE.png) - **53 errors, 95 alerts, 535 contrast errors**:

- Errors:
  - Missing form label
  - Empty form label
  - Empty heading
  - Empty button
  - Empty link
  - Broken ARIA menu
  - Very HUGE number of contrast errors
- Alerts:
  - Redundant alternative text
  - Suspicious alternative text
  - Broken same-page link
  - Redundant link
  - Very small text

4. In my own opinion `Very small text`, `Container element is empty` and `Empty form label` are misidentified by the audit tools. `Very small text` is a very tricky rule - it might be useful for some web applications using small text once at the page and small text mean that it is not important information, so I'd rather leave it as it is. `Container element is empty` - should be useful trick in some pages so I could not see any problems with it. It's better to miss it by screenreaders that fix that issue. `Empty form label` - I guess form might be without label because heading of the form very often is duplicated in label.

&#9733; &#9733; &#9733; &#9733;

1. NVDA tool:

- [image1](<NVDA(1).png>) - Links have empty accessible name and don't have identical accessible names and same context serve equivalent purpose. All links in header are without identical accessible names and same context serve equivalent purpose.
- [image2](<NVDA(2).png>) - Link in context isn't descriptive, alternating and link name are the same in all cards. Visible label is not a part of accessible name - it is duplicated. Links text has not minimum and enhanced contrast, so links names on cards are not accessible.
- [image3](<NVDA(3).png>) - Heading is not descriptive, Heading has empty accessible name, and there is only one heading in all page.
- [image4](<NVDA(4).png>) - Buttons has empty accessible name, alternations are the same in all buttons.
- [image5](<NVDA(5).png>) - Form field label isn't descriptive, Form field has empty accessible name.

&#9733; &#9733; &#9733; &#9733; &#9733;

1. Color contrast analyzer

- [image1](contrast-wcag-aa-large.png) - issues: text in header does not passed check at all, as well as headers on cards (Free, Online). Sorting value, which was chosen also didn't pass analysis.
- [image2](<contrast-wcag-aa-large%20(1).png>) - issues: in addition to issues in the first point, button `register` and `view more trainings` didn't pass analysis.
- [image3](<contrast-wcag-aa-large%20(2).png>) - issues: button `subscribe` as well as `career test` didn't pass analysis. Sorting point by country which was chosen also didn't pass analysis.
- [image4](<contrast-wcag-aa-large%20(3).png>) - issues: button `all articles` and blue text in description to cards, sorting point which was chosen.
- [image5](<contrast-wcag-aa-large%20(4).png>) - issues: despite header, there are no issues on the screen.

General comment: a color scheme #76cdd8 and #f6ffff and #ffffff for text/bg is not good case for reading information. It wasn't passed analysis at all.

2. [Siteimprove plugin](Siteimprove5.png)  
   Elements, that should be improved:
   - `EN` in header - has 1.83:1 - Increase the color contrast to 4.5 : 1 or higher.
   - `Sign in` in header - has 1.83:1 - Increase the color contrast to 4.5 : 1 or higher.
   - `View more training(25)` in the middle of the page - has 1.68:1 - Increase the color contrast to 4.5 : 1 or higher.
   - `Hungary` in country sorting - has 1.83:1 - Increase the color contrast to 4.5 : 1 or higher.
   - `13 October 2022` and all dates beside in Blog section - almost good! - has 4.48:1 - Increase the color contrast to 4.5 : 1 or higher.

General comment: very similar issues as in Color contrast analyzer.

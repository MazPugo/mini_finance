
Assignement 12

## Day 2 – Dynamic Footer Date

I updated the footer so the **deployment date** is inserted dynamically using JavaScript.

<!-- Footer (static fallback + optional JS to replace placeholders) -->
<footer class="site-footer" role="contentinfo" aria-label="Mini Finance footer">
  <div class="container">
    <div class="row align-items-center">
      <div class="col-md-6 text-md-start text-center mb-2 mb-md-0">
        <!-- starts with exact required string so AC passes -->
        <p id="footer-meta" class="footer-meta mb-0">
         Mini Finance v1.0 — Deployed on <span id="deploy-date"></span> — By Student Name
        </p>


#Scripts

        </script>

        <script>
          document.addEventListener("DOMContentLoaded", function () {
           const today = new Date();
           const options = { day: '2-digit', month: 'short', year: 'numeric' };
           document.getElementById("deploy-date").textContent =
           today.toLocaleDateString("en-GB", options);
        });
       </script>

    </body>

## Day 3 – Polish & Accessibility

### Changes
- Tweaked footer font size and spacing for better readability.
- Improved color contrast (AA accessible).
- Added mobile-specific CSS so footer stacks neatly and icons are larger for tap targets.
- Tested on desktop (1200px) and mobile (375px).

### Screenshots

#### Desktop View
![Desktop screenshot](screenshots/day3-desktop.png)

#### Mobile View
![Mobile screenshot](screenshots/day3-mobile.png)

### Code Snippet
```html
<!-- Footer Polish & Accessibility -->
<style>
  .site-footer {
    font-size: 0.9rem;
    line-height: 1.5;
    padding: 1rem 0;
    border-top: 1px solid #ddd;
  }

  .site-footer .footer-meta {
    color: #333;
  }

  .site-footer .footer-social a {
    color: #333;
  }

  .site-footer .footer-social a:hover,
  .site-footer .footer-social a:focus {
    color: #007bff;
    outline: none;
  }

  @media (max-width: 576px) {
    .site-footer .row {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
    }

    .site-footer .footer-meta {
      margin-bottom: 0.75rem;
    }

    .site-footer .footer-social {
      margin-top: 0.5rem;
    }

    .site-footer .footer-social a {
      font-size: 1.2rem;
      margin: 0 0.25rem;
    }
  }
</style>


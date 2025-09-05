<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Image Generator Tool</title>
  <meta name="description" content="Generate and optimize responsive images with dynamic levels. Easy AdSense integration for monetization.">
  <!-- Google AdSense: Paste your Ad Unit ID below -->
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-INSERT-YOUR-UNIT-ID" crossorigin="anonymous"></script>
  <style>
    body { margin: 0; font-family: Arial, sans-serif; }
    .main-container { max-width: 820px; margin: 0 auto; padding: 20px; }
    header, footer { text-align: center; }
    .generator-section { padding: 20px; background: #fafafa; border-radius: 8px; }
    .image-result img { max-width: 100%; height: auto; border: 1px solid #ddd; border-radius: 4px; }
    .ad-top, .ad-bottom { margin: 18px 0; text-align: center; }
    @media (max-width: 600px) {
      .main-container { padding: 8px; }
      .generator-section { padding: 10px; }
    }
  </style>
</head>
<body>
  <!-- AdSpace Top -->
  <div class="ad-top">
    <!-- AdSense code for top ad unit -->
    <ins class="adsbygoogle"
         style="display:block"
         data-ad-client="ca-pub-INSERT-YOUR-UNIT-ID"
         data-ad-slot="1234567890"></ins>
    <script>
      (adsbygoogle = window.adsbygoogle || []).push({});
    </script>
  </div>
  <main class="main-container">
    <header>
      <h1>Responsive Image Generator Tool</h1>
      <h2>Optimize your images, select generator level, and monetize easily!</h2>
    </header>
    <section class="generator-section">
      <form id="image-generator-form">
        <label for="generator-level">Generator Level:</label>
        <select id="generator-level">
          <option value="basic">Basic</option>
          <option value="optimized">Optimized</option>
          <option value="high-res">High Resolution</option>
        </select>
        <label for="image-url">Image URL:</label>
        <input type="url" id="image-url" placeholder="Enter image URL" required />
        <button type="submit">Generate Image</button>
      </form>
      <div id="result" class="image-result">
        <!-- Dynamically generated image will appear here -->
      </div>
    </section>
    <!-- AdSpace Bottom -->
    <div class="ad-bottom">
      <!-- AdSense code for bottom ad unit -->
      <ins class="adsbygoogle"
           style="display:block"
           data-ad-client="ca-pub-INSERT-YOUR-UNIT-ID"
           data-ad-slot="0987654321"></ins>
      <script>
        (adsbygoogle = window.adsbygoogle || []).push({});
      </script>
    </div>
  </main>
  <footer>
    <p>Copyright &copy; 2025. All rights reserved.</p>
  </footer>
  <script>
    document.getElementById('image-generator-form').addEventListener('submit', function(e) {
      e.preventDefault();
      var level = document.getElementById('generator-level').value;
      var url = document.getElementById('image-url').value;
      let optimizedUrl = url;
      // Example optimization based on generator level
      if (level === 'optimized') {
        optimizedUrl += '?w=600&auto=compress';
      } else if (level === 'high-res') {
        optimizedUrl += '?w=1200&auto=compress';
      }
      document.getElementById('result').innerHTML =
        `<img src="${optimizedUrl}" alt="Generated Image" class="responsive-img">`;
    });
  </script>
</body>
</html>

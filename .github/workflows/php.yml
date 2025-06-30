<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $raw_domain = $_POST["domain"];
    $clean = preg_replace("/[^a-zA-Z0-9.-]/", "", $raw_domain);
    $safe_arg = escapeshellarg($clean);
    $reportPath = "recon-$clean/report.html";

    shell_exec("./recon.sh $safe_arg");

    if (file_exists($reportPath)) {
        header("Content-Type: text/html");
        echo file_get_contents($reportPath);
    } else {
        echo <<<HTML
        <!DOCTYPE html>
        <html>
        <head>
          <title>Recon Report Fallback</title>
          <style>
            body { font-family: Arial; background: #111; color: #eee; padding: 40px; text-align: center; }
            .box { background: #222; padding: 20px; border-radius: 8px; display: inline-block; }
          </style>
        </head>
        <body>
          <div class="box">
            <h1>⚠️ Recon report could not be generated</h1>
            <p>Domain entered: <strong>$clean</strong></p>
            <p>Please check if necessary commands are available (e.g. <code>whois</code>, <code>dig</code>, <code>curl</code>)</p>
          </div>
        </body>
        </html>
        HTML;
    }
}
?>

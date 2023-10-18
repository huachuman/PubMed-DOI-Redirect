// ==UserScript==
// @name         PubMed-DOI-Redirect
// @namespace    http://tampermonkey.net/
// @version      1.0
// @description  Redirect from PubMed to DOI link
// @author       Huachuman
// @match        https://pubmed.ncbi.nlm.nih.gov/*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    // Get all links on the page.
    var links = document.querySelectorAll('a');

    // Loop through the links.
    for (var i = 0; i < links.length; i++) {
        var link = links[i];

        // Check if the link href starts with 'https://doi.org/'
        if (link.href.startsWith('https://doi.org/')) {
            // If it does, display a message on the page and then redirect to this link.

            var message = document.createElement('div');
            message.textContent = 'Redirecting with DOI...';
            message.style.position = 'fixed';
            message.style.left = '50%';
            message.style.top = '50%';
            message.style.transform = 'translate(-50%, -50%)';
            message.style.borderRadius = '10px';
            message.style.color = 'white'
            message.style.fontSize = '26px';
            message.style.backgroundColor = 'rgba(242, 74, 68, 0.8)';  // Semi-transparent background
            message.style.padding = '150px';
            message.style.zIndex = '10000';
            message.style.whiteSpace = 'nowrap';  // This will prevent the text from wrapping.
            message.style.display = 'flex';
            message.style.flexDirection = 'column';
            message.style.justifyContent = 'center';
            message.style.alignItems = 'center';

            // Create a title element:
            var title = document.createElement('div');
            title.textContent = '(PubMed Redirect Tampermonkey Script)';
            title.style.fontSize = '16px';
            title.style.marginBottom = '20px';  // This will add a 20px space below the title.
            title.style.marginTop = '20px';  // This will add a 20px space below the title.

            // Add the title to the message:
            message.appendChild(title);

            // Create a spinning wheel element:
            var spinner = document.createElement('div');
            spinner.style.border = '16px solid #f3f3f3';
            spinner.style.borderTop = '16px solid #3498db';
            spinner.style.borderRadius = '50%';
            spinner.style.width = '60px';
            spinner.style.height = '60px';
            spinner.style.animation = 'spin 2s linear infinite';
            spinner.style.marginTop = '20px';

            // Add the spinning wheel to the message:
            message.appendChild(spinner);

            document.body.appendChild(message);

            window.location.href = link.href;
            break;  // This line stops the loop after finding the first DOI link.
        }
    }
})();

// Add this to your CSS styles to create the spinning animation:
var style = document.createElement('style');
style.innerHTML = `
@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}`;
document.head.appendChild(style);

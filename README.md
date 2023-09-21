<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gardenia</title>
    <style>
        /* Your existing CSS code */

        /* Modify the background color to blue */
        .bpw-header-container {
            /* sets the border radius of the element */
            border-radius: var(--spacing-large);
            /* sets the background color to blue */
            background: #0074D9; /* You can change this color code to the shade of blue you prefer */
            /* sets the border of the element */
            border: 1px solid var(--zinc-200);
            /* sets the border radius of the element (repeated declaration) */
            border-radius: var(--spacing-medium);
            /* sets the padding of the element */
            padding: var(--spacing-large) var(--spacing-x-large);
        }
    </style>
</head>
<body>
    <!-- JavaScript to load the chatbot asynchronously -->
    <script>
        function loadChatbotScript() {
            var script = document.createElement('script');
            script.src = 'https://cdn.botpress.cloud/webchat/v1/inject.js';
            script.async = true;
            document.body.appendChild(script);

            script.onload = function () {
                window.botpressWebChat.init({
                    "botId": "73a61896-2be5-4968-a382-ad188572ef87",
                    "clientId": "73a61896-2be5-4968-a382-ad188572ef87",
                    "hostUrl": "https://cdn.botpress.cloud/webchat/v0",
                    "messagingUrl": "https://messaging.botpress.cloud",
                    "botName": "Gardenia",
                    "avatarUrl": "https://i.postimg.cc/YC8DyGW1/Screenshot-2023-09-13-213012.jpg",
                    "containerWidth": "100%25",
                    "layoutWidth": "100%25",
                    "composerPlaceholder": "Start typing here",
                    "botConversationDescription": "Your Property Partner",
                    "hideWidget": true,
                    "useSessionStorage": true,
                    "disableAnimations": true,
                    "enableConversationDeletion": true
                });
                window.botpressWebChat.onEvent(function () {
                    window.botpressWebChat.sendEvent({ type: 'show' });
                }, ['LIFECYCLE.LOADED']);
            };
        }

        // Call the function to load the chatbot script
        loadChatbotScript();
    </script>
</body>
</html>


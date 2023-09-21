<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gardenia</title>

    <style>
        /* Make the chatbot container fullscreen */
        #botpress-webchat {
            width: 100%;
            height: 100%;
            position: fixed;
            top: 0;
            left: 0;
            z-index: 9999; /* Ensure it's on top of other elements */
        }
    </style>
</head>
<body>
    <!-- JavaScript to load the chatbot asynchronously -->
    <script>
        function loadChatbotScript() {
            var script = document.createElement('script');
            script.src = 'https://cdn.botpress.cloud/webchat/v1/inject.js'; // Using v1
            script.async = true;
            document.body.appendChild(script);

            script.onload = function () {
                window.botpressWebChat.init({
                    "botId": "73a61896-2be5-4968-a382-ad188572ef87", // Bot ID from the first script
                    "clientId": "73a61896-2be5-4968-a382-ad188572ef87", // Client ID from the first script
                    "hostUrl": "https://cdn.botpress.cloud/webchat/v1",
                    "messagingUrl": "https://messaging.botpress.cloud",
                    "composerPlaceholder": "Start typing here",
                    "botConversationDescription": "Your Property Partner",
                    "hideWidget": true,
                    "disableAnimations": true,
                    "enableConversationDeletion": true,
                    "botName": "Gardenia", // Add botName
                    "avatarUrl": "https://i.postimg.cc/YC8DyGW1/Screenshot-2023-09-13-213012.jpg", // Add avatarUrl
                    "containerWidth": "100%", // Set containerWidth to 100%
                    "layoutWidth": "100%", // Set layoutWidth to 100%
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


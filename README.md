<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gardenia</title>
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

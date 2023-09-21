<html lang="en">
<head>
    <meta charset="UTF-8">
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
                    "botId": "0e30855c-6873-4f87-9de6-b3352a0622b3",
                    "clientId": "0e30855c-6873-4f87-9de6-b3352a0622b3",
                    "hostUrl": "https://cdn.botpress.cloud/webchat/v1",
                    "messagingUrl": "https://messaging.botpress.cloud",
                    "botName": "Gardenia",
                    "avatarUrl": "https://i.postimg.cc/YC8DyGW1/Screenshot-2023-09-13-213012.jpg",
                    "containerWidth": "100%100",
                    "layoutWidth": "100%100",
                    "composerPlaceholder": "Start typing here",
                    "botConversationDescription": "Your Property Partner",
                    "hideWidget": true,
                    "useSessionStorage": true,
                    "disableAnimations": true,
                    "frontendVersion": "v1",
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

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Website Title</title>
    <!-- Include your CSS code here -->
    <style>
        /* Global styles */
        .bpw-header-icon,
        .bpw-header-icon svg,
        .bpw-header-icon svg path {
          fill: #ffffff !important;
        }

        #input-message::placeholder {
          color: rgba(0, 0, 0, .30);
        }

        .bpw-composer textarea,
        .bpw-composer textarea:focus {
          outline: none !important;
          border: 1px solid rgba(0, 0, 0, .15);
        }

        /* Keyboard single choice option */
        .bpw-keyboard-single-choice {
          background-color: #ffffff;
          border: none;
        }

        /* Buttons */
        .bpw-button,
        .bpw-button-alt,
        .bpw-button:hover,
        .bpw-button-alt:hover {
          background-color: #dcdcdc;
          color: #000000;
          border-radius: 10px;
          border: none;
        }

        /* Hyperlinks */
        a {
          color: #ffffff;
          text-decoration: underline;
        }

        /* Chat container and scrollbars */
        .bpw-chat-container,
        .bpw-chat-container::-webkit-scrollbar,
        .bpw-chat-container::-moz-scrollbar {
          background-color: #ffffff;
          scrollbar-width: thin;
          scrollbar-color: #f5f5f5 #ffffff;
          border: none;
        }

        /* Chat bubble content */
        .bpw-from-bot .bpw-chat-bubble .bpw-chat-bubble-content {
          background-color: #f5f5f5;
          color: #000000;
        }

        .bpw-from-user .bpw-chat-bubble .bpw-chat-bubble-content {
          background-color: #6675fa;
          color: #ffffff;
        }

        /* Composer section */
        .bpw-composer {
          background-color: #ffffff;
          border-top: none;
        }

        /* Bot avatar */
        .bpw-bot-avatar img,
        .bpw-bot-avatar svg {
          background: #000000;
          border: 3px solid #ffffff;
        }

        /* Scrollbars */
        ::-webkit-scrollbar,
        ::-webkit-scrollbar-track,
        .bpw-chat-container::-webkit-scrollbar-track,
        .bpw-chat-container::-moz-scrollbar-track {
          width: 0.5rem;
          background-color: transparent;
        }

        ::-webkit-scrollbar-thumb,
        .bpw-chat-container::-webkit-scrollbar-thumb,
        .bpw-chat-container::-moz-scrollbar-thumb {
          background-color: #ffffff;
          border-radius: 1rem;
          border: 0.5rem solid transparent;
        }

        /* Floating button icon */
        .bpw-floating-button i svg path {
          fill: #6675fa;
        }
    </style>
</head>
<body>
    <!-- JavaScript to load the chatbot asynchronously -->
    <script>
        function loadChatbotScript() {
            var script = document.createElement('script');
            script.src = 'https://cdn.botpress.cloud/webchat/v0/inject.js';
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

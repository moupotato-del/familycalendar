<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ファミリーカレンダー - 家族の予定管理掲示板</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Kaisei+Decol:wght@700&family=M+PLUS+Rounded+1c:wght@900&family=Zen+Maru+Gothic:wght@900&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --pink-light: #ffd1dc;
            --green-light: #d1f7c4;
            --main-pink: #ff8da1;
            --main-green: #88d498;
            --main-yellow: #ffec99;
            --dark: #333333;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        html, body {
            width: 100%;
            height: 100%;
            position: fixed;
            overflow: hidden;
            background-color: #222;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .app-container {
            width: 100%;
            height: 100%;
            max-width: 480px;
            max-height: 100vh;
            background: #ffffff;
            position: relative;
            display: flex;
            flex-direction: column;
            overflow: hidden;
        }

        @media (min-width: 481px) {
            .app-container {
                height: 844px;
                border-radius: 32px;
                box-shadow: 0 10px 30px rgba(0,0,0,0.3);
                border: 8px solid #333;
            }
        }

        .screen {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            transition: opacity 0.5s ease;
            background: #fff;
        }

        .screen.hidden {
            opacity: 0;
            pointer-events: none;
            z-index: -1;
        }

        /* 1. タイ
        

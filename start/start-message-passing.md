# 訊息傳送

我們可以透過 Chrome API 去傳送訊息

## Content Script `app.js` 傳送訊息

在 `app.js` 加入傳送該網頁的標題的 function

```javascript
chrome.runtime.sendMessage('Hello Taiwan');
```

## Background Script 接收訊息

```javascript
chrome.runtime.onMessage.addListener(function(response, sender, sendResponse){
    alert(response);
});
```

重新載入套件之後，你可以看到這個 alert 訊息

![Script Message Passing Hello Taiwan](./images/start-message-passing-hello-taiwan.png)


## Content Script 傳送網頁標題

在 `app.js` 中我們改傳送該網頁的標題，這樣我們就可以在 Background Script 也接收到這個網頁的標題了

```javascript
chrome.runtime.sendMessage(document.getElementsByTagName('title')[0].innerText);
```

![Script Message Passing HTML Title](./images/start-message-passing-html-title.png)
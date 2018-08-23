# Manifest 參數說明


## Page Action / Browser Action

* 在功能只針對部份網頁時，使用 page action。
* 如果功能需要常駐在每個網頁，使用 browser action。


*Browser Action*

```json
{
    "browser_action": {
        "default_popup": "popup.html",
        "default_icon": {
          "16": "images/get_started16.png",
          "32": "images/get_started32.png",
          "48": "images/get_started48.png",
          "128": "images/get_started128.png"
        }
    }
}
```

*Page Action*

```json
{
    "page_action": {
        "default_popup": "popup.html",
        "default_icon": {
          "16": "images/get_started16.png",
          "32": "images/get_started32.png",
          "48": "images/get_started48.png",
          "128": "images/get_started128.png"
        }
    }
}
```

## 參考資料
* [大兜的 Chrome Extension 學習筆記 - 不歸錄](https://tonytonyjan.net/2012/05/25/get-start-with-chrome-extension/)

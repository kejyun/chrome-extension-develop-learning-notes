# manifest.json

`manifest.json` 是 Google 套件的相關設定檔案，可以設定 `icon`、`權限` ... 等等的相關資訊，檔案的內容會長得像這樣

```json
{
    "manifest_version": 2,

    "name": "KeJyun 的 Chrome 套件",
    "description": "KeJyun 的 Chrome 套件描述",
    "version": "1.0",

    "browser_action": {
        "default_icon": "icon.png",
        "default_popup": "popup.html"
    },
    "permissions": [
        "activeTab",
        "https://ajax.googleapis.com/"
    ]
}
```

設定完成後，在擴充套件重新載入設定後，就會看到設定的結果

![設定結果](./images/start-manifest-json-plugin-demo.png)

## 設定值

### [manifest_version](https://developer.chrome.com/extensions/manifest/manifest_version)

在 Chrome 18 的版本中，`manifest_version` 應該被設定為 2，若需要使用較舊版本的 Chrome 才需將 `manifest_version` 設為 1


### [name](https://developer.chrome.com/extensions/manifest/name#name)

套件名稱

### [description](https://developer.chrome.com/extensions/manifest/description)

套件描述

### [version](https://developer.chrome.com/extensions/manifest/version)

套件版本號，下列為允許設定的版本號類型

```json
{
    "version": "1",
    "version": "1.0",
    "version": "2.10.2",
    "version": "3.1.2.4567",
}
```

### [browser_action](https://developer.chrome.com/extensions/browserAction)

瀏覽器動作

|  選項 | 描述  |
|---|---|
| default_icon  | icon  |
| default_title  | 按鈕描述  |
| default_popup  | 按鈕按下彈出頁面 HTML  |

### [permissions](https://developer.chrome.com/extensions/declare_permissions)

權限


|  選項 | 描述  |
|---|---|
| [activeTab](https://developer.chrome.com/extensions/activeTab)  | 存取目前的 tab 頁面  |


### [icons](https://developer.chrome.com/extensions/manifest/icons)

套件圖示

```json
{
    "icons": {
        "16": "icon16.png",
        "48": "icon48.png",
        "128": "icon128.png"
    }
}
```

## 參考資料
* [Manifest File Format - Google Chrome](https://developer.chrome.com/extensions/manifest)
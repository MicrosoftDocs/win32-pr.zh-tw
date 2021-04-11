---
title: 使用 HTMLView 的優點
description: 使用 HTMLView 的優點
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Windows Media 中繼檔播放清單，HTMLView 優點
- 播放清單，HTMLView 優點
- 中繼檔播放清單，HTMLView 優點
- Windows Media 中繼檔播放清單，HTMLView 的優點
- 播放清單，HTMLView 的優點
- 中繼檔播放清單，HTMLView 的優點
- HTMLView 的優點
- Windows Media Player，HTMLView 的優點
- Windows Media Player，HTMLView 的優點
- HTMLView，優點
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5e5409db969f5e9a8e0df18738f4995490b1d83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372408"
---
# <a name="advantages-of-using-htmlview"></a>使用 HTMLView 的優點

HTMLView 功能可讓您輕鬆地建立以網路為基礎的整合式使用者體驗，並使用熟悉的 Web 外觀來播放數位媒體內容。 當您將 Web 內容與 Windows Media Player 使用者介面中的數位媒體內容結合時， (UI) 的結果可能會對使用者造成更大的影響，而不是個別查看元素時。 數位媒體內容是由相關的相關資訊來增強，而網頁可以提供類似內容的連結，進而創造新的商機。

## <a name="htmlview-provides-a-better-user-experience"></a>HTMLView 可提供更佳的使用者體驗

使用者想要存取可透過數位媒體內容提供的資訊，但不想要處理看似無限的快顯公告系列。 使用快顯瀏覽器視窗來顯示網路上的廣告已經很常見，因為現在有軟體可以防止這些視窗開啟。 這種軟體可能會造成不必要的副作用，以防止顯示合法的網頁，有時會隱藏整個數位媒體簡報。

當您使用 HTMLView 功能時，使用者不再需要處理快顯視窗。 您不需要開啟另一個瀏覽器視窗來提供其他資訊給使用者，您可以在播放程式播放使用者想要的音訊或影片內容時，在 Windows Media Player UI 的「 **立即播放** 」功能中顯示自訂的 Web 內容。 使用者可以使用 Windows Media Player 控制項來控制播放。 由於您的內容是在全模式播放程式中播放，因此設計來防止彈出廣告的軟體不會阻止使用者享受內容。

## <a name="htmlview-content-is-easy-to-create"></a>HTMLView 內容很容易建立

如同功能名稱所示，您可以使用超文字標記語言 (HTML)  (HTML) 來建立以 HTMLView 功能顯示的 Web 內容。 如果您已經建立 Web 的內容，這表示您不需要學習新的程式設計語言，即可輕鬆地使用 HTMLView 功能建立豐富的內容。 如果您已經有內嵌 Windows Media Player ActiveX 控制項的網頁，您可以將這些頁面出現在播放程式 UI 中，只要從 Windows Media 中繼檔中指向這些網頁，就可以使用特殊參數) 的 ( .asx 檔。

Windows Media Player 使用內嵌的 Microsoft Internet Explorer 實例來顯示 HTMLView 內容。 這表示在建立網頁時，您不需要考慮不同的網際網路瀏覽器、多個腳本模型或不同的指令碼語言。 即使使用者未使用 Internet Explorer 作為預設瀏覽器，您的網頁仍會在播放程式中正確顯示。

Windows Media Player 以外的程式可能會將自己註冊為開啟 .asx 檔案的預設程式。 Windows Media Player 9 系列或更新版本的物件模型包含新的方法 **openPlayer**，可讓您針對想要播放的內容，指定統一資源定位器 (URL) 。 當您使用 **openPlayer** 方法時，Windows Media Player 一律會以完整模式開啟，以播放指定的內容。 使用這個方法時，您可以確保 HTMLView 內容會顯示在 Windows Media Player 中，而不是其他已接管該 .asx 檔案類型關聯的應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**OpenPlayer**](player-openplayer.md)
</dt> </dl>

 

 





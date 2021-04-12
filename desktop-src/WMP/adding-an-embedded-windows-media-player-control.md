---
title: 加入內嵌 Windows Media Player 控制項
description: 加入內嵌 Windows Media Player 控制項
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Windows Media 中繼檔播放清單，新增內嵌的 Windows Media Player 控制項
- 播放清單，加入內嵌的 Windows Media Player 控制項
- 中繼檔播放清單，新增內嵌的 Windows Media Player 控制項
- Windows Media 中繼檔播放清單，embedded Windows Media Player 控制項
- 播放清單、內嵌 Windows Media Player 控制項
- 中繼檔播放清單、內嵌 Windows Media Player 控制項
- 新增內嵌的 Windows Media Player 控制項
- 內嵌的 Windows Media Player 控制項
- Windows Media Player，加入內嵌的控制項
- Windows Media Player、內嵌控制項
- HTMLView，加入內嵌 Windows Media Player 控制項
- HTMLView、embedded Windows Media Player 控制項
- HTMLView，Windows Media Player 物件模型
- HTMLView，Player 物件模型
- Windows Media Player 物件模型，關於
- 物件模型，關於
- Player 物件
- Windows Media、Player 物件模型
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372392"
---
# <a name="adding-an-embedded-windows-media-player-control"></a>加入內嵌 Windows Media Player 控制項

有兩個原因，您可能會考慮將 Windows Media Player 的內嵌實例新增至 HTMLView 簡報。 首先，如果您想要顯示影片內容，您需要使用 Windows Media Player ActiveX 控制項。 其次，如果您想要從 HTMLView 網頁內利用 Windows Media Player 物件模型的功能，您必須使用 Player 控制項的實例來執行此動作。

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a>使用 Player 控制項在 HTMLView 內容中顯示影片

通常，Windows Media Player 會使用 **目前播放** 功能的 [影片和視覺效果] 窗格來顯示影片。 由於 HTMLView 會使用此區域來顯示您的網頁，因此如果您希望播放程式播放影片，則必須提供額外的影片顯示區域。 您可以使用 Windows Media Player ActiveX 控制項來輕鬆完成這項作業。

若要使用 Player 控制項來顯示影片，請使用 **物件** 標記將控制項內嵌在您的 HTMLView 網頁中。 這是您用來將播放機控制項內嵌到您想要顯示影片之任何網頁的相同技術。 下列範例程式碼顯示在 Internet Explorer 中內嵌 Player 控制項的基本語法：


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



*AutoStart* 參數可確保每當指定新的 URL 時，內容就會自動播放。 您為 *uiMode* 指定的值是由您所指定，但是在建立 HTMLView 簡報的內容時，通常會想要指定「無」。 當您以這種方式內嵌 Windows Media Player 控制項來顯示影片時，使用者可以使用全模式播放程式的控制項來控制播放，所以不需要在網頁中提供其他傳輸控制項。 您可以使用通常配置給傳輸控制項的空間，以顯示更多文字、圖形或其他內容的連結。

在設計要顯示于 HTMLView 簡報中的網頁上內嵌 Windows Media Player 控制項時，請勿指定 *URL* 參數。 相反地，請在用來開啟內容的 .asx 檔案中指定數位媒體檔案。

由於您在 HTMLView 網頁中提供影片顯示區域，因此您可以決定影片的放置位置，以及您想要的顯示區域大小。 例如，您可以在 HTML **DIV** 專案內包含 **Player** 物件，然後指定 **DIV** 的位置，讓影片顯示在網頁上。 您可以藉由指定 **物件** 專案的 [高度] 和 [寬度] 屬性值，來變更影片顯示的尺寸。 您也可以使用腳本來指定這些值。

## <a name="using-the-player-object-model"></a>使用 Player 物件模型

Windows Media Player 物件模型會公開您可以在 HTMLView 網頁中使用的屬性、方法和事件。 當您在 HTMLView 網頁中內嵌 Windows Media Player ActiveX 控制項時，您會自動擁有 Player 物件模型的存取權。

如果您在 HTMLView 網頁中內嵌 Windows Media Player 控制項，請勿使用 Player 物件模型來指定要播放的數位媒體檔案。 例如，如果您使用腳本來指定內嵌控制項的 **URL** 屬性值，當數位媒體檔案播放時，您的 HTMLView 網頁將會從「 **立即播放** 」功能中卸載。 若要避免發生這種情況，當您需要使用腳本從 HTMLView 網頁開啟數位媒體內容時，請一律開啟包含 HTMLView 參數的 .asx 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**UiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**設定。 autoStart**](settings-autostart.md)
</dt> </dl>

 

 





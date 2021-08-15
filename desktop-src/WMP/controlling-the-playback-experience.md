---
title: 控制播放體驗
description: 控制播放體驗
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Windows媒體中繼檔播放清單，控制播放
- 播放清單，控制播放
- 中繼檔播放清單，控制播放
- Windows媒體中繼檔播放清單，播放問題
- 播放清單，播放問題
- 中繼檔播放清單，播放問題
- 控制播放
- Windows Media Player，控制播放
- Windows Media Player，播放問題
- HTMLView，播放問題
- HTMLView，控制播放
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: efca4d299edc40cfb94820fbb1aae7115329c0f3fcbd2859db0bbbc56d7a0d4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341885"
---
# <a name="controlling-the-playback-experience"></a>控制播放體驗

本節將討論使用 HTMLView 功能時可能遇到的一些播放問題。

## <a name="requiring-the-user-to-view-web-based-content"></a>要求使用者查看 Web 內容

您可能會想要讓使用者能夠在 HTMLView 的 Web 內容顯示時，享受您的數位媒體內容。 如果使用者切換離開 **立即播放** 的功能，您可以在 HTMLView 網頁中包含腳本，以停止播放數位媒體內容。 若要這樣做，您可以將 **unload** 事件的事件處理常式指定為 **BODY** 元素的一部分，如下列 HTML 程式碼所示：


```XML
<BODY onunload = "UnloadMe();">

```



然後，您可以在事件處理常式函式中包含腳本，以關閉播放程式中的檔案。 下列範例程式碼會執行這項操作：


```XML
function UnloadMe()
{
   Player.close();
}

```



當使用者按一下按鈕以開啟另一個 Windows Media Player 功能（例如媒體櫃）來切換離開時，**播放程式會** 關閉內嵌的瀏覽器。 這會造成 **onunload** 事件發生，並在名為 **UnloadMe** 的函式中執行腳本。 [Player. close](player-close.md)方法會停止播放和卸載目前的數位媒體檔案。 若要再次查看內容，使用者必須重新開啟原始檔案。 當使用者離開 HTMLView 網頁時，這項技術也會停止播放。 請注意，當使用者切換至面板模式時，這項技術無法防止使用者觀看數位媒體內容。

您會記得 HTMLView 參數可以套用至 .asx 檔案中的每個 **ENTRY 專案** 。 您可以利用這項功能，確保每次新的數位媒體檔案啟動時，就會顯示您的 HTMLView 內容。 若要這樣做，請將 HTMLView 的 **PARAM** 元素與您 .asx 播放清單中的每個專案產生關聯。 當每個專案播放時，播放清單都會回到全模式，並顯示您在播放清單中指定的 HTMLView 內容。

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>預設會停用 URL 和檔案指令碼命令類型

Windows Media Player 9 系列或更新版本提供的設定，可讓使用者指定 URL 和檔案類型的指令碼命令是否能夠執行。 根據預設，這兩個指令碼命令類型都不會執行。 如果您使用自訂指令碼命令類型，不論使用者的設定為何，它們都會繼續執行。 如果您必須使用 URL 和檔案類型的指令碼命令，則必須提示使用者變更設定。 若要變更設定，請依序按一下 [ **工具**]、[ **選項**] 和 [ **安全性**]。

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>重新開啟 HTMLView 並不會重載網頁

當使用者開啟包含 HTMLView 參數的 .asx 檔案，並接著重新開啟相同的檔案時，Windows Media Player 不會重新整理 HTMLView 網頁。 這也表示，如果您允許使用者離開您的 HTMLView 網頁，播放程式就不會將內嵌瀏覽器傳回初始的 HTMLView 網頁。

## <a name="hiding-the-content-location"></a>隱藏內容位置

您可能會決定不希望 Windows Media Player 在播放 .asx 檔案時顯示數位媒體內容的位置。 通常，Windows Media Player 只會在從網際網路串流內容時顯示播放清單本身的相關資訊。 不過，您可以採取進一步的步驟，以防止使用者判斷內容的位置。 例如，有一種方式可確保播放程式不會顯示內容的路徑，而是使用 Windows Media Services 伺服器端播放清單來串流您的內容。 如此一來，當使用者流覽內容的內容時，就會看到伺服器的 URL，而不是您的內容 URL。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**PARAM 元素**](param-element.md)
</dt> </dl>

 

 





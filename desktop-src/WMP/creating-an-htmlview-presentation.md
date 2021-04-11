---
title: 建立 HTMLView 簡報
description: 建立 HTMLView 簡報
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Windows Media 中繼檔播放清單，HTMLView 簡報
- 播放清單、HTMLView 簡報
- 中繼檔播放清單，HTMLView 簡報
- Windows Media 中繼檔播放清單，建立 HTMLView 簡報
- 播放清單，建立 HTMLView 簡報
- 中繼檔播放清單，建立 HTMLView 簡報
- 建立 HTMLView 簡報
- Windows Media Player，建立 HTMLView 簡報
- Windows Media Player，HTMLView 簡報
- HTMLView，建立簡報
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372345"
---
# <a name="creating-an-htmlview-presentation"></a>建立 HTMLView 簡報

若要建立基本的 HTMLView 簡報，您需要至少三個元素：

-   **數位媒體內容。** 這是一或多個 Windows Media Player 播放的音訊或影片檔案。
-   **網頁。** 這是以網路為基礎的內容，會顯示在播放程式 UI 的「 **立即播放** 」功能中。
-   **Windows Media 中繼檔。** 這是用來指示 Windows Media Player 將數位媒體內容與網頁結合的中繼檔播放清單。

.Asx 檔案是一種文字檔，可提供檔案資料流程及其簡報的相關資訊。 根據可延伸標記語言 (XML)  (XML) 語法，.asx 檔案可以包含各種不同的元素，而每個專案都是由具有相關聯屬性的標記所識別。 **PARAM** 元素提供一種方式，可讓自訂參數與中繼檔播放清單中的特定專案或整個中繼檔產生關聯。 其中一個可供您使用的預先定義參數名稱為 "HTMLView"。 這是讓 URL 值指定的網頁顯示在 Windows Media Player 中的參數。

下列範例程式碼顯示將單一數位媒體檔案與單一網頁結合的 .asx 檔案：


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



當 Windows Media Player 在上述範例中開啟 .asx 檔案時，它會從名為 content1 的檔案播放音訊，並在全模式播放程式的「 **立即播放** 」功能中開啟名為 htmlview.htm 的網頁。 使用者可以使用 Windows Media Player 控制項來暫停、搜尋及停止音訊內容。

您可以藉由將 **PARAM** 元素與每個專案產生關聯，輕鬆地變更每個內容所顯示的網頁，如下列程式碼範例所示：


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



在上述範例中，Windows Media Player 先顯示在播放數位音訊檔案 content1 時的網頁 htmlview1.htm。 當播放清單開啟播放清單（content2）中的下一個專案時，顯示在中的網頁 **現在現正播放** htmlview2.htm 的變更。 如此一來，您就可以指定使用者針對每個數位媒體內容所看到的網頁。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**PARAM 元素**](param-element.md)
</dt> </dl>

 

 





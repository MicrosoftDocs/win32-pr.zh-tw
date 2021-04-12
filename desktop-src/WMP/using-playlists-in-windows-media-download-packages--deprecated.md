---
title: '在 Windows Media 下載套件中使用播放清單 (已淘汰) '
description: '在 Windows Media 下載套件中使用播放清單 (已淘汰) '
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Windows Media 中繼檔，Windows Media 下載套件
- Windows Media Player，Windows Media 下載套件
- 中繼檔，Windows Media 下載套件
- Windows Media、Windows Media 下載套件
- 播放清單，Windows Media 下載套件
- 中繼檔播放清單，Windows Media 下載套件
- Windows Media 中繼檔播放清單，Windows Media 下載套件
- Windows Media 下載套件，播放清單
- Windows Media 下載套件，中繼檔播放清單
- Windows Media 下載套件，Windows Media 中繼檔播放清單
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372448"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a>在 Windows Media 下載套件中使用播放清單 (已淘汰) 

本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。

播放清單是具有 .asx 副檔名的 Windows Media 中繼檔，其提供的資訊會告訴 Windows Media Player 如何播放封裝的內容。 藉由將多個內容檔案結合成單一 Windows Media 下載套件，您可以使用播放清單來控制和自訂 Windows Media 下載套件。

> [!Note]  
> 一般情況下，Windows Media 下載套件會使用中繼檔播放清單來參考封裝中的多媒體內容，而不是從內部網路或網際網路上的伺服器來參考資料流。 不過，支援該 .asx 檔案內的 URL 參考。

 

使用 XML 時，中繼檔會提供 Windows Media Player 用來播放和顯示內容的資訊。 播放清單是由各種 XML 程式碼元素及其相關聯的標記和屬性所組成。 Windows Media 中繼檔播放清單中的每個元素都會定義 Windows Media Player 中的特定設定或動作。

使用者的電腦會將副檔名為 .asx 的 Windows Media 中繼檔與 Windows Media Player 產生關聯。 Windows Media Player 會開啟並剖析中繼檔中的 XML 程式碼，其中包含尋找已封裝音訊或影片檔案的路徑。 然後，中繼檔腳本會控制音訊、影片和圖形化體驗。 中繼檔也包含 Windows Media Player 處理，並顯示在 [播放清單] 下拉式清單方塊中的資訊。 在清單顯示之後，會立即播放清單中的第一個專案。

中繼檔播放清單是包含已封裝內容之檔案的快捷方式。 下列程式碼是中繼檔的範例，其中指定要使用 **面板元素顯示** 的框線、要播放的兩個歌曲，以及每一首歌曲的播放清單資訊。


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player (已淘汰) 的框線**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**(淘汰的 Windows Media 下載套件)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Windows Media 中繼檔**](windows-media-metafiles.md)
</dt> </dl>

 

 





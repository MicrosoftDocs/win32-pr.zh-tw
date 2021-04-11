---
title: 範例無線電站播放清單
description: 範例無線電站播放清單
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Windows Media 中繼檔播放清單、播放清單範例
- 播放清單、播放清單範例
- 中繼檔播放清單，播放清單範例
- Windows Media 中繼檔播放清單，範例播放清單
- 播放清單、範例播放清單
- 中繼檔播放清單，範例播放清單
- Windows Media 中繼檔播放清單、範例播放清單
- 播放清單、範例播放清單
- 中繼檔播放清單，範例播放清單
- Windows Media 中繼檔播放清單，程式碼範例
- 播放清單，程式碼範例
- 中繼檔播放清單，程式碼範例
- Windows Media 中繼檔播放清單，無線電站播放清單範例
- 播放清單、無線電站播放清單範例
- 中繼檔播放清單，無線電站播放清單範例
- Windows Media Player，播放清單範例
- Windows Media Player，範例播放清單
- Windows Media Player，範例播放清單
- Windows Media Player，無線電站播放清單範例
- 播放清單範例
- 範例播放清單
- 範例播放清單
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372068"
---
# <a name="an-example-radio-station-playlist"></a>範例無線電站播放清單

下列範例程式碼說明如何建立播放清單來掃描三個岩石電臺電臺。 虛構的公司艾德作品無線電品牌位於播放清單上，以及播放清單中所有個別的串流。 當您撰寫程式碼時，請將所有 Url 和檔案名變更為可存取 Windows Media Player 的有效檔案名。

每個工作站都會建立播放清單。 第四個播放清單會掃描前三個播放清單。 系統會建立播放清單，以參考動態產生的廣告，並具有「艾德作品」無線電商標。

其中一個代表電臺的播放清單可能如下所示。


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



接著可以將播放清單視為個別播放清單的參考。

範例程式碼


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



此範例會在每個所參考的三個電臺中，每一個都有30秒的時間來播放廣告。 這個週期將會無限期重複，因為未定義 **重複** 專案的 **COUNT** 屬性。

-   本文所述之公司、組織、產品、人物及事件均屬虛構， 並非影射任何真實的公司、組織、產品、人物或事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**範例播放清單**](example-playlists.md)
</dt> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





---
title: 個人化媒體傳遞
description: 個人化媒體傳遞
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Windows媒體中繼檔播放清單，個人化媒體傳遞
- 播放清單、個人化媒體傳遞
- 中繼檔播放清單，個人化媒體傳遞
- Windows媒體中繼檔播放清單、媒體傳遞個人化
- 播放清單、媒體傳遞個人化
- 中繼檔播放清單，媒體傳遞個人化
- 媒體傳遞個人化
- 個人化媒體傳遞
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9483f4fc7a068c6f6456a5d170b4be73a9ba31ef85294f9a6939181dff00c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996008"
---
# <a name="personalizing-media-delivery"></a>個人化媒體傳遞

不同于將相同內容廣播給大量物件的單向通訊，Windows 媒體技術可提供您使用人口統計來賦予廣播的工具。 在網際網路上，大規模的雙向通訊可供使用。 這項動態的資訊交換可讓內容提供者知道其物件，並以自訂的簡報回應。

下列範例（使用虛構公司）說明如何將串流內容的傳遞傳遞給個人化。 本文假設您已熟悉 Active Server Pages (ASP 或 .asp 檔案) 和定義變數。

新聞網路是虛構的廣播新聞群組織，已擴充其作業以包含網站。 網站的主要功能是一個區段，使用者可以在其中建立自己的個人化 newscasts。 使用者不會看到以大量物件為目標的傳統 newscast，而是會查看只包含個人興趣主題的完整新聞方案。 下列順序說明一般使用者體驗。

1.  新的使用者前往網站，然後按一下 [ **建立您的個人 Newscast**]。
2.  喜好設定表單隨即開啟。 在此表單上，使用者會回答有關個人喜好的問題，例如我的最愛新聞故事、最愛的新聞報導、業餘新聞，以及日常接收日常新聞的方法。
3.  使用者傳送此資訊，而幾秒鐘之後，就會查看完整、15分鐘的個人 newscast，內含程式內容、轉換和電視廣告。 每個媒體元件的選取專案（包括電視廣告）是以使用者設定檔為基礎，並且會自動使用 Windows 媒體技術元件和現成的網際網路工具來完成。

下列清單說明各種工具如何互動以建立個人化 newscast。

1.  使用者填寫的喜好設定表單是使用中的伺服器頁 (ASP)  (選項。 asp) 。 從喜好設定形式取得的資料會由兩個伺服器元件進行分析。 其中一個元件會使用此資訊來查詢 Microsoft SQL Server 的新聞故事資料庫。 另一個元件是一種 ad 伺服器，會根據合約需求和人口統計來使用一組複雜的規則，以便在該時間排程適合使用者的廣告。
2.  這兩個資料庫會傳回不同的播放清單部分。 新聞故事資料庫會傳回一組適當的故事專案，而且 ad 伺服器會傳回一組適當的商業專案。
3.  第二個 ASP 網頁 (PlayShow asp) 從新聞故事資料庫和 ad 伺服器接收專案，並將這些專案與標準顯示開啟、關閉和轉換專案結合。 然後，所有專案都會根據 PlayShow 所提供的範本來配置，而 ASP 頁面會將播放清單傳回給使用者。
4.  使用者電腦上的內嵌 Windows Media Player 控制項播放播放清單的播放清單，而使用者則會查看個人化 newscast。

下列範例是使用者可能會收到的播放清單檔案部分。 Ad 橫幅、MOREINFO 連結和摘要已新增至其中。


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   本文所述之公司、組織、產品、人物及事件均屬虛構， 並非影射任何真實的公司、組織、產品、人物或事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**使用中繼檔播放清單**](using-metafile-playlists.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





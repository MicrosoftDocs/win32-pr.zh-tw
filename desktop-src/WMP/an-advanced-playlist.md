---
title: Advanced 播放清單
description: Advanced 播放清單
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Windows媒體中繼檔播放清單、播放清單範例
- 播放清單、播放清單範例
- 中繼檔播放清單，播放清單範例
- Windows媒體中繼檔播放清單，範例播放清單
- 播放清單、範例播放清單
- 中繼檔播放清單，範例播放清單
- Windows媒體中繼檔播放清單、範例播放清單
- 播放清單、範例播放清單
- 中繼檔播放清單，範例播放清單
- Windows媒體中繼檔播放清單，程式碼範例
- 播放清單，程式碼範例
- 中繼檔播放清單，程式碼範例
- Windows媒體中繼檔播放清單，advanced 播放清單範例
- 播放清單、advanced 播放清單範例
- 中繼檔播放清單，advanced 播放清單範例
- Windows Media Player，播放清單範例
- Windows Media Player，範例播放清單
- Windows Media Player，範例播放清單
- Windows Media Player，advanced 播放清單範例
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
ms.openlocfilehash: 6573d5bef05c8af943368a12d03677526a9783915d6915b6cc5f1516bc9942f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583255"
---
# <a name="an-advanced-playlist"></a>Advanced 播放清單

下列播放清單範例顯示如何使用一組更完整的播放清單元素。 撰寫您自己的程式碼時，您必須將所有 Url 和檔案名變更為有效的檔案名，而您的 Windows Media Player 可以存取這些名稱。

範例程式碼


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



下表描述上述的 advanced 播放清單。



| 折線圖                                                                                            | 描述                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | [ASX](asx-element.md)元素會識別用戶端 (Windows Media Player) 這是 Windows 媒體中繼檔播放清單。 **Version** 屬性會指定中繼檔元素的版本號碼。                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | [Title](title-element--metafile.md)元素會識別播放清單的整體標題。 Windows Media Player 會將此中繼資料顯示為 [顯示標題]。                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | [ABSTRACT](abstract-element.md)元素提供顯示標題的工具提示。                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | [MOREINFO](moreinfo-element.md)元素會將顯示標題連結到 URL。 如果已定義工具提示，則將滑鼠指標暫停在顯示標題上方即可存取工具提示。 選取 [顯示標題] 之後，就會開啟指定的 URL。                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | [橫幅](banner-element.md)元素會在 Windows Media Player 中建立廣告橫幅。 **HREF** 屬性指定橫幅圖形 (必須是194圖元寬、32圖元高) 。                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | [ABSTRACT](abstract-element.md)元素提供 **橫幅** 的工具提示。                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | [MOREINFO](moreinfo-element.md)元素會將 **橫幅** 圖形連結到 URL。 如果有定義工具提示，請將滑鼠指標放在 **橫幅** 上來存取工具提示。 選取 **橫幅** 會開啟指定的 URL。                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | [PARAM](param-element.md)元素定義自訂參數。 **Name** 屬性會將自訂參數的名稱定義為「track」。 **Value** 屬性會將 "track" 的值定義為 "1"。                                                                                                                          |
| `</BANNER>`                                                                                 | 關閉 **橫幅** 元素                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | 開始 [輸入](entry-element.md) 元素區塊。 這個元素會藉由指定 **REF** 元素中的連結，來定義播放清單中的剪輯。 將 **ClientSkip** 設定為 [否] 表示使用者無法向前快轉或跳到下一個剪輯                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | 建立廣告橫幅。 **HREF** 是橫幅圖形 (194x32 圖元) 。                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | 提供橫幅的工具提示。                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | 提供橫幅 URL 的連結。 選取橫幅會連接到 URL。                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | 關閉 **橫幅** 元素                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | 提供剪輯 **標題** 文字 URL 的連結。                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | 註解。 只有在程式碼被查看時，才會顯示[批註](comments.md)。                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | 提供剪輯 **標題** 文字的工具提示。                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | 識別剪輯的標題。 這是剪輯 **標題** ，因為它是在 **專案專案** 內進行嵌套。 Windows Media Player 會將此中繼資料顯示為剪輯標題。                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | 識別媒體剪輯的作者。 Windows Media Player，此中繼資料會顯示為剪輯 **作者**。                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | [著作權](copyright-element.md)元素會指定與媒體剪輯相關聯的著作權。 Windows Media Player 會將此中繼資料顯示為剪輯著作權。                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | 與 **XML** 批註相同格式的批註。                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | 媒體內容的 URL。 [REF](ref-element.md)元素會將該行識別為媒體內容的指標。 **HREF** 屬性是檔案的 URL。請注意，使用類似 XML 的元素 "/>" 而非 " &lt; /REF &gt; "。 因為這個元素沒有子專案，所以它會自行關閉。<br/> |
| `</ENTRY>`                                                                                  | 指定第一個 **專案** 元素的結尾。                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | 開始第二個 **ENTRY** 元素。                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | 識別第二個剪輯的標題。                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | 識別第二個媒體剪輯的作者。                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | 註解。 只有在程式碼被查看時，才會顯示。                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | 這是剪輯 **標題** 文字的工具提示文字。                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | 註解。 只有在程式碼被查看時，才會顯示。                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | 將該行識別為媒體內容的指標。 **HREF** 屬性是檔案的 URL。                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | 指定第二個 **ENTRY** 元素的結尾。                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | 指定播放清單的結尾。                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**範例播放清單**](example-playlists.md)
</dt> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 






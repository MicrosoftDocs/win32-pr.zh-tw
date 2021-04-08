---
title: 修改顯示
description: 修改顯示
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Windows Media 中繼檔播放清單，修改顯示
- 播放清單，修改顯示
- 中繼檔播放清單，修改顯示
- Windows Media 中繼檔播放清單，顯示修改
- 播放清單，顯示修改
- 中繼檔播放清單，顯示修改
- Windows Media Player，顯示修改
- Windows Media Player，修改顯示
- Windows Media Player，文字屬性
- Windows Media Player，影像屬性
- Windows Media Player，MOREINFO 屬性
- Windows Media Player，摘要文字
- MOREINFO 屬性
- 摘要文字
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021234"
---
# <a name="modifying-the-display"></a>修改顯示

播放清單可以四種主要方式改變 Windows Media Player 使用者介面：

-   Text 屬性
-   映像屬性
-   MOREINFO 屬性
-   摘要文字

## <a name="text-properties"></a>Text 屬性

Windows Media Player 啟用標題、作者、著作權和描述中繼資料文字的顯示。 剪輯中繼資料可以來自資料流程或媒體檔案，也可以來自播放清單。 顯示中繼資料來自播放清單。 一般情況下，播放清單是將文字屬性傳遞至 Windows Media Player 的較佳方法，尤其是可能變更文字元素時。 編輯播放清單中的文字比重新撰寫媒體檔案更容易。 而且因為從播放清單中讀取的屬性會覆寫媒體檔案中包含的屬性，所以您可以將新文字加入播放清單中的對應屬性，輕鬆地更新顯示文字。 在下列範例中，播放清單中標題和作者中繼資料的文字會覆寫媒體檔案中所含的標題和作者文字（例如 .wma）。

除非中繼檔播放清單中有一個 **抽象** 元素，否則會從 **專案專案** 中參考的 Windows Media 檔案取出 **描述** 文字。 如果有 **摘要** 文字，則會顯示並覆寫 **描述** 文字。


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a>映像屬性

橫幅影像可以新增至 Windows Media Player 的使用者介面。 此圖形可用於廣告、提供資訊，以及提供網站的存取權，以提供一些可能的名稱。

使用 **橫幅** 元素可指定 Windows Media Player 顯示的圖形影像， (32 圖元高、194圖元寬) 。 圖形會顯示在任何影片內容下方。 您可以使用 **MOREINFO** 子項目，將超連結新增至橫幅。

工具提示可以由 **橫幅** 元素範圍內的 **抽象** 元素定義。 您可以藉由將滑鼠指標暫停在橫幅圖形上方，來顯示任何定義的工具提示文字。 選取具有滑鼠指標的橫幅圖形將會啟動任何以 **MOREINFO** 元素定義的超連結。

慣用的 **橫幅** 圖形格式為 GIF 格式。 如果圖形的大小正確，則可以使用 JPG 格式。

上述範例說明如何使用 **橫幅** 元素。

> [!Note]  
> 使用 DRM 檔案時，或在網頁中內嵌 Windows Media Player 時，不支援 **橫幅** 影像。

 

如需橫幅的詳細資訊，請參閱 [Windows Media Player 中的自訂圖形](custom-graphics-in-windows-media-player.md)。

## <a name="moreinfo-properties"></a>MOREINFO 屬性

使用者介面的文字和影像區域可以與 Url 相關聯。 在播放期間，使用者可以選取其中一個區段，以連接到其網頁瀏覽器中與其相關聯的 URL。 例如，您可以將廣告網站的網站與廣告橫幅影像產生關聯，如下列程式碼片段所示。


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a>摘要文字

**ABSTRACT** text 可用來顯示與所關聯之使用者介面的文字或影像區域的簡短快顯描述。 在播放期間，如果滑鼠指標停留在這些區域的其中一個，則滑鼠指標旁邊會出現工具提示，顯示與區域相關聯的 **摘要** 文字。 **抽象** 文字是從中繼檔抓取，並以 **抽象** 元素定義。 **ABSTRACT** 元素可以是專案或 **橫幅****專案** 的子項目。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**使用中繼檔播放清單**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





---
title: 偵測播放玩家
description: 偵測播放玩家
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player 線上商店，偵測玩家
- 線上商店，偵測玩家
- 輸入1個線上商店，偵測玩家
- 輸入2個線上商店，偵測玩家
- Windows Media Player 線上商店、播放機偵測
- 線上商店、播放機偵測
- 輸入1個線上商店、播放機偵測
- 輸入2個線上商店、播放機偵測
- 播放機偵測
- 偵測播放玩家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932291"
---
# <a name="detecting-the-player"></a>偵測播放玩家

當您為線上商店建立網頁時，您可能會想要讓使用者能夠在網頁瀏覽器或 Windows Media Player 中查看頁面。 您可以使用 ASP 腳本來判斷是否已在播放程式中主控您的網頁。

下列範例程式碼會從 URL 查詢字串中抓取 version 參數，以判斷頁面是否裝載于 Windows Media Player 中：


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



請注意，上述程式碼會假設在 Windows Media Player 中裝載時，查詢字串中有 version 參數。 這適用于使用者開啟的頁面，但對於使用 **外部 NavigateTaskPaneURL** 開啟的頁面，可能不是正確的。 若要在以程式設計方式流覽時存在版本查詢字串，您必須將 version 參數加入至方法呼叫，或以動態方式將版本附加至 ServiceInfo 檔的 **導覽** 元素基底 URL。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**動態建立 ServiceInfo 檔**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





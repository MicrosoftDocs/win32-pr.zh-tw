---
title: 使用公告
description: 使用公告
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Windows媒體中繼檔播放清單，公告
- 播放清單、公告
- 中繼檔播放清單，公告
- Windows Media Player，公告
- 宣告
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 24408211f6ce708d380406026de45be0cce86521fdc188aaaf785ccf03790c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134381"
---
# <a name="using-announcements"></a>使用公告

公告是一個檔案，其中包含媒體串流 URL 的相關資訊，包括多播 IP 位址、埠、串流格式，以及其他工作站設定。 建立單播或多播發布串流時，Windows 媒體管理員可以建立公告。 用戶端可以快速載入公告檔案，然後繼續存取串流處理媒體檔案。

若為單播發行端點，則會開啟發行端點媒體資料流程。 若是多播發行端點，則會從 .nsc 副檔名的廣播站檔案解壓縮 URL，並存取串流媒體。 不同于單播串流，多播資料流程中不包含任何標頭資訊。 這是來自廣播站檔案，副檔名為 .nsc 的資訊。 Windows Media Player 通常會先開啟公告檔案，這是一個用於中繼檔播放清單，指向廣播站檔案的位置。

範例程式碼


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**使用中繼檔播放清單**](using-metafile-playlists.md)
</dt> </dl>

 

 





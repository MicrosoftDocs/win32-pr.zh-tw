---
description: 查詢搜尋功能
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: 查詢搜尋功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846571"
---
# <a name="querying-for-seeking-capabilities"></a>查詢搜尋功能

Microsoft® DirectShow®支援 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面的搜尋。 篩選圖形管理員會公開此介面，但搜尋功能一律會由圖形中的篩選器來執行。

某些資料無法 seeked。 例如，您不能從相機搜尋即時影片串流。 但是，如果資料流程是可搜尋的，則有各種類型的搜尋可能會受到支援。 這些包括：

-   搜尋至資料流程中的任意位置。
-   正在抓取資料流程的持續時間。
-   正在抓取資料流程中的目前位置。
-   反向播放。

**IMediaSeeking** 介面會定義一組旗標，以尋找可描述可能搜尋功能的搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)。 若要取出資料流程的功能，請呼叫 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 方法。 方法會傳回旗標的位元組合。 應用程式可以使用 & (位 **and**) 運算子來測試它們。 例如，下列程式碼會檢查圖形是否可以搜尋至任意位置：


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 




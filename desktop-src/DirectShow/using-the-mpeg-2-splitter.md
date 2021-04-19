---
description: 使用 MPEG-2 分隔器
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: 使用 MPEG-2 分隔器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987666"
---
# <a name="using-the-mpeg-2-splitter"></a>使用 MPEG-2 分隔器

> [!Note]  
> 從 Microsoft® Windows® XP 開始，MPEG 2 分隔器篩選器已被取代。 請改用 [Mpeg-2 信號](mpeg-2-demultiplexer.md) 。

 

MPEG-2 分隔器篩選器支援包含至少下列其中一種資料流程類型的 MPEG-2 程式資料流程的提取模式播放。

-   MPEG-2 影片
-   MPEG-2 音訊
-   針對 DVD-Video 所定義的杜比 AC-3 音訊編碼
-   LPCM (線性脈衝程式碼的調製) 音訊編碼，如 DVD-Video 所定義

如需 MPEG-2 分隔器所支援之媒體類型的清單，請參閱 [Mpeg-2 分隔器媒體類型](mpeg-2-splitter-media-types.md)。

MPEG-2 分隔器不會剖析傳輸資料流程。 只有) 使用 (推送模式的傳輸資料流程的 MPEG-2 信號篩選篩選。

**時間戳記**

播放 MPEG-2 程式串流時，MPEG-2 分隔器篩選器會將它所遇到的第一個系統時鐘參考視為任何資料流程的時間來源。 這與使用呈現時間戳記的 [Mpeg-2 資料流程分隔器](mpeg-1-stream-splitter-filter.md)不同。 [**IAMParse：： GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime)方法會傳回已處理之資料的 (可能估計) 資料流程系統時鐘時間。

如果 MPEG-2 分隔器篩選器遇到具有非持續性屬性集的輸入範例 (可使用 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 或 [**IMediaSample2：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)) 來設定 [中斷] 屬性，直到它找到資料中的第一個元件並調整其時間戳記，如此一來，該套件 (scr) 的系統時鐘參考才會被視為與中斷之前的 scr 時間相同。 如果 SCR 時鐘顯示為向前跳或向前跳到一秒以上，則 (與 MPEG-2 程式串流規格) ，這也會被視為時鐘不連續，並從傳遞給下游篩選器的時間戳記減去明顯的時鐘差異。

**資料流程選取範圍**

播放 MPEG-2 程式串流時，會選擇第一個影片串流和第一個播放程式串流的音訊串流。 最多支援一個音訊和一個影片輸出 pin。 透過 [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) 介面，相同類型的不同資料流程可以選取為系統標頭中的音訊限制所指定的數位。 針對 MPEG-2 音訊，目前假設資料流程形成連續的範圍，從資料流程0xC0 開始。

**支援的介面**

MPEG-2 分隔器篩選器支援下列介面。

-   [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)。 僅限 MPEG-2 程式串流。
-   [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)。 僅限 MPEG-2 程式串流，僅限音訊串流。
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)。 包括位元組模式搜尋。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的 MPEG 2 支援](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 




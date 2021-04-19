---
description: 處理資料
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: 處理資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbece449df36c2de88414f313d477b8a16ba896
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106986235"
---
# <a name="processing-data"></a>處理資料

**剖析媒體資料**

如果您的篩選器會剖析媒體資料，請勿信任標題或內容中的其他自我描述資料。 例如，不信任出現在 AVI RIFF 區塊或 MPEG 封包中的大小值。 這類錯誤的常見範例包括：

-   讀取 *n* 位元組的資料，其中 *n* 的值來自內容，而不會針對緩衝區的實際大小檢查 *n* 。
-   跳到緩衝區內的位元組位移，而不驗證位移是否落在緩衝區內。

另一個常見的錯誤類別，則不會驗證內容中所找到的格式描述。 例如：

-   [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構後面可以加上色彩表。 **BITMAPINFO** 結構定義為 **BITMAPINFOHEADER** 結構，後面接著組成色彩表的 **RGBQUAD** 值陣列。 陣列的大小取決於 **biClrUsed** 的值。 絕對不要將色彩表複製到 **BITMAPINFO** ，而不需要先檢查已配置給 **BITMAPINFO** 結構的緩衝區大小。
-   [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構可能會在結構上附加額外的格式資訊。 **CbSize** 成員會指定額外資訊的大小。

在連接 pin 期間，篩選應確認所有格式結構的格式是否正確，而且包含合理的值。 如果沒有，則會拒絕連接。 在驗證格式結構的程式碼中，請特別小心算術溢位。 例如，在 **BITMAPINFOHEADER** 中，寬度和高度是32位的 **long** 值，但影像大小 (這是兩個) 產品的函式，只是 **DWORD** 值。

如果來源的格式資料大於您配置的緩衝區，請勿截斷來源資料，以便將它複製到您的緩衝區。 這麼做可以建立一個結構，其隱含大小大於實際大小。 例如，點陣圖標頭可能會指定不再存在的調色板資料表。 請改為重新配置緩衝區，或直接使連接失敗。

**串流期間的錯誤**

當圖形正在執行時，如果您的篩選器收到格式不正確的內容，則應終止串流。 執行下列動作：

-   從 **Receive** 傳回錯誤碼。
-   在下游篩選器上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 。
-   呼叫 [**CBaseFilter：： NotifyEvent**](cbasefilter-notifyevent.md) 以張貼 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件。

**格式變更**

有幾個機制可供篩選器變更中間資料流程的格式。 其中每個步驟都牽涉到一個以上的步驟，這會產生錯誤接受的可能性。 如果您的篩選器取得動態格式變更的要求，則必須拒絕要求，或在到達時接受新的格式。 同樣地，除非其他篩選準則同意，否則絕不會切換格式。 如需詳細資訊，請參閱 [動態格式變更](dynamic-format-changes.md)。

 

 

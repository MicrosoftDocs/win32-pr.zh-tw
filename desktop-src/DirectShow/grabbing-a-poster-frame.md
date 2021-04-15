---
description: 抓取海報框架
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: 抓取海報框架
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467935"
---
# <a name="grabbing-a-poster-frame"></a>抓取海報框架

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本文說明如何使用由[DirectShow 編輯服務](directshow-editing-services.md)提供的媒體偵測器[ (MediaDet) ](media-detector--mediadet.md)物件，顯示數位媒體檔案中的海報框架。

媒體偵測器是協助程式物件，可從媒體來源檔案取得格式資訊。 它也可以從來源檔案中的影片資料流程抓取點陣圖影像。 假設檔案是可搜尋的，您可以從檔案中的任何時間點取得映射。 傳回的影像一律採用24位 RGB 格式。

媒體偵測器不是篩選準則，而且應用程式不需要使用篩選圖形管理員或建立篩選圖形。 就內部而言，媒體偵測器會建立包含 [**範例捕獲篩選器**](sample-grabber-filter.md)的篩選圖形。 為了取得點陣圖，媒體偵測器會搜尋並暫停篩選圖形，然後從範例捕獲篩選器抓取點陣圖。 應用程式會透過 [**IMediaDet**](imediadet.md) 介面與媒體偵測器進行通訊。 媒體偵測器是在協助程式物件內封裝篩選圖形的絕佳範例，以便保護應用程式不受圖形相關的詳細資料。

媒體偵測器會以兩種模式運作。 當您第一次建立時，媒體偵測器會處於「資訊收集」模式。 您可以指定媒體檔案的名稱，並取得檔案中每個資料流程的相關資訊，例如格式類型、畫面播放速率或持續時間。 如果檔案包含影片串流，您可以將媒體偵測器切換為「點陣圖抓取」模式，並從來源取出點陣圖。 不過，一旦您這麼做，就無法將媒體偵測器切換回其原始模式;它會永久連接到該影片串流。 若要使用另一個資料流程或另一個檔案，您必須建立媒體偵測器的新實例。

> [!Note]  
> 本教學課程中的程式碼範例會使用 ATL **CComPtr** 類別，此類別會自動管理參考計數。 如果您想要使用原始介面指標，請記得在完成時釋放每個介面。 此外，為了簡潔起見，程式碼範例會省略應用程式應該執行的大部分錯誤檢查。 在工作程式碼中，一律檢查 **HRESULT** 值。

 

本教學課程包含下列步驟：

-   [步驟1：建立 Windows Framework](step-1--create-the-windows-framework.md)
-   [步驟2：新增功能表命令以抓取海報畫面](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [步驟3：執行 Frame-Grabbing 函式](step-3--implement-the-frame-grabbing-function.md)
-   [步驟4：在工作區上繪製點陣圖](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務](using-directshow-editing-services.md)
</dt> </dl>

 

 




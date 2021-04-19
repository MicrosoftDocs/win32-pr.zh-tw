---
description: 管理影片編輯專案
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: 管理影片編輯專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970879"
---
# <a name="managing-video-editing-projects"></a>管理影片編輯專案

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

下列秘訣可協助您管理 [DirectShow 編輯服務](directshow-editing-services.md)中的專案。

變更至時間軸

-   如果您在建立篩選圖形之後變更時間軸，請再次呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 來重建前端。 這通常不會影響圖形的其餘部分。 不過，有時候轉譯引擎必須先刪除整個圖形，才能重建前端。  (例如，如果您新增或移除群組，就會發生這種情況。 ) **ConnectFrontEnd** 方法會傳回 S \_ 警告 \_ OUTPUTRESET，表示它刪除了圖形。 如果發生這種情況，您的應用程式必須重建圖形的呈現區段。
-   若要從時間軸完全移除所有物件，請呼叫 [**IAMTimeline：： ClearAllGroups**](iamtimeline-clearallgroups.md) 方法。

**清除**

-   當您完成使用轉譯引擎時，請呼叫 [**IRenderEngine：： ScrapIt**](irenderengine-scrapit.md) 方法。 就像任何 COM 物件一樣，當您使用完介面指標時，請務必釋放每個介面指標。
-   轉譯引擎不會在時間軸上保留參考計數。 請勿在使用完成之前釋出時程表，而且一律先在轉譯引擎上呼叫 **ScrapIt** 。
-   如果您釋出時間軸的所有參考，請勿使用該時間軸中的任何物件，即使您持有它們的參考計數也一樣。

**多個時間軸實例**

-   請勿在時間軸之間移動時間軸物件。 時間軸中的每個物件都必須由該時間軸建立。 時間軸會保存內部快取，其中包含它所建立之物件的相關資訊;移動時間軸物件可能會中斷快取。
-   絕對不要使用具有一個以上時間軸的相同轉譯引擎實例。 轉譯引擎會保留快取，內含時間軸的相關資訊。 多個時間軸會中斷快取，並導致無法預期的結果。 如果您需要兩個作用中的時間軸，請為每個時間軸建立個別的轉譯引擎實例。
-   時間軸可以使用一個以上的轉譯引擎，但不能同時使用。 使用其他轉譯引擎之前，請先刪除舊的轉譯引擎。  (當您從使用基本轉譯引擎進行預覽時，通常會發生這種情況，以供寫入檔案的智慧型轉譯引擎。 ) 

**持續性**

-   當您將專案儲存至 XML 檔案時，篩選圖形不會持續。 因此，您會遺失與 smart recompression、壓縮格式或壓縮參數相關的任何資訊。 在載入專案之後，應用程式會由應用程式還原這些參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務](using-directshow-editing-services.md)
</dt> </dl>

 

 




---
description: 提供自訂的影片調整
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: 提供自訂的影片調整
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108905"
---
# <a name="providing-a-custom-video-resizer"></a>提供自訂的影片調整

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

> [!Note]  
> 這項功能需要 DirectX 9.0 或更新版本。

 

當 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 調整大小的影片來源剪輯時，預設行為是 *StretchBlt*，這是快速但不是消除鋸齒的。 您可以藉由將自訂的調整器實作為 DirectShow 轉換篩選，來變更調整大小行為。 篩選器必須公開 [**IResize**](iresize.md) 介面，這可讓 DES 指定輸入和輸出影片大小。 如需撰寫轉換篩選的相關資訊，請參閱 [寫入轉換](writing-transform-filters.md)篩選。 建議使用 **CTransformFilter** 基類做為起始點。 當您執行篩選準則時，請注意下列事項：

-   支援篩選 (的 **IResize** 介面，而不是) 的釘選。
-   篩選器只應接受 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式 (格式 \_ VideoInfo) 。 拒絕其他格式類型。
-   DES 的影片格式可能是任何未壓縮的 RGB 類型，包括32位 RGB 與 Alpha (MEDIASUBTYPE \_ ARGB32) 。 您的篩選可以安全地拒絕 **biHeight** < 0 的格式。
-   在轉譯引擎連接篩選器的輸出圖釘之前，它會呼叫 [**IResize：:p \_**](iresize-put-mediatype.md) 的 ui 媒體設定輸出類型。 它也可能會呼叫 [**IResize：:p 的工作 \_ 空間大小**](iresize-put-size.md) 來調整輸出大小。 它可以在連接輸出釘選之前，以任何順序呼叫這兩個方法，不限次數。
-   轉譯引擎連接輸出釘選之後，可能會再次呼叫 **put \_ 大小** 。 調整器篩選器應該以新的大小重新連接其輸出圖釘。
-   在篩選的 [**CTransformFilter：： Transform**](ctransformfilter-transform.md) 方法內，將輸入影片延展至輸出大小。
-   您的篩選準則絕對不應該在輸出範例上設定不連續旗標，或將媒體類型附加至輸出範例。
-   若要將篩選的狀態儲存在 GraphEdit (. grf) 檔中，請執行 **IPersistStream** 介面。  (這是選擇性的，但對測試而言很有用。 ) 

若要使用 [調整] 篩選準則，您必須在使用者的系統上將篩選註冊為 COM 物件。 在應用程式呈現影片專案之前，請查詢 [**IRenderEngine2**](irenderengine2.md) 介面的轉譯引擎，並以調整器篩選的 CLSID 呼叫 [**IRenderEngine2：： SetResizerGUID**](irenderengine2-setresizerguid.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯專案](rendering-a-project.md)
</dt> </dl>

 

 




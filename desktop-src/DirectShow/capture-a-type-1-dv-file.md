---
description: 捕捉類型 1 DV 檔案
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: 捕捉類型 1 DV 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567413"
---
# <a name="capture-a-type-1-dv-file"></a>捕捉類型 1 DV 檔案

類型 1 DV AVI 檔案包含單一交錯式資料流程。 若要在預覽時捕捉類型1檔案，請使用下圖所示的篩選圖形。

![具有預覽的類型 1 capture](images/dv1-cap.png)

此圖表中的篩選包括：

-   [Smart t](smart-tee-filter.md)濾波器會將交錯的 DV 分割成捕獲資料流程和預覽資料流程。 這兩個數據流都包含相同的交錯資料。
-   [AVI Mux](avi-mux-filter.md)和檔案[寫入器](file-writer-filter.md)會將交錯串流寫入磁片。
-   [Dv 分隔器](dv-splitter-filter.md)會將交錯的資料流程分割成 DV 影片串流和音訊串流。 這兩個串流都是 rendererd 進行預覽。
-   [Dv 影片解碼會解碼](dv-video-decoder-filter.md)dv 影片串流以進行預覽。

建立此圖形，如下所示：


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  呼叫 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) ，將 AVI Mux 篩選器連線到檔案寫入器篩選器。
2.  使用釘選分類釘選類別捕獲來呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) \_ \_ ，以轉譯捕獲資料流程。 「捕獲圖形產生器」會自動插入智慧的 t a 濾波器。
3.  再次呼叫 RenderStream，但使用釘選類別 PIN \_ 類別目錄 \_ 預覽，以轉譯預覽資料流程。 如果您不想要預覽影片，請略過此呼叫。

對於 RenderStream 的這兩個呼叫，媒體類型是媒體類型 \_ ，表示交錯 DV 影片。 在此程式碼中，「捕獲圖形產生器」會自動新增所需的每個篩選準則，但 MSDV Capture 篩選器除外。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 




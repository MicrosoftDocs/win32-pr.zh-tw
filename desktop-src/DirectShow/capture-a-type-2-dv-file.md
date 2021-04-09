---
description: 捕捉類型 2 DV 檔案
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: 捕捉類型 2 DV 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845851"
---
# <a name="capture-a-type-2-dv-file"></a>捕捉類型 2 DV 檔案

類型 2 DV AVI 檔案有兩個數據流，其中一個包含 DV 影片，另一個包含音訊。 若要在預覽時捕捉類型2檔案，請使用下圖所示的篩選圖形。

![具有預覽的類型2捕獲](images/dv2-cap.png)

This graph is almost the same as the graph for type-1 capture (see [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)). 不過，capture 資料流程會先經過 [DV 分隔](dv-splitter-filter.md) 器篩選器，再到達 [AVI Mux](avi-mux-filter.md) 篩選器。 因此，AVI Mux 會接收兩個數據流，也就是音訊串流和 DV 編碼的影片串流。

建立此圖形，如下所示：


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  建立 DV 分隔器，並將它新增至篩選圖形。
2.  呼叫 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) ，將 AVI Mux 篩選器連線到檔案寫入器篩選器。
3.  呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，將 MSDV capture 篩選器連接至 DV 分隔器。 此呼叫也會將其中一個 DV 分隔器的輸出圖釘連接到 AVI Mux。
4.  再次呼叫 RenderStream，以將 DV 分隔器的其他釘選到 AVI Mux。
5.  第三次呼叫 RenderStream 以轉譯預覽資料流程。 如果不想要預覽影片，請略過此步驟。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 




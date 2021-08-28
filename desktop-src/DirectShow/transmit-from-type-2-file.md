---
description: 從類型2檔案傳輸
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: 從類型2檔案傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d1d6dec7c68cba177923dea04205d8dbc26faa8ff98cf5d6e79659fced46fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315711"
---
# <a name="transmit-from-type-2-file"></a>從類型2檔案傳輸

若要在預覽時傳輸類型2檔案，請使用下圖所示的篩選圖形。

![類型2傳輸與預覽](images/dv2-transmit.png)

類型2檔案有兩個數據流、一個音訊串流和一個 DV 編碼的影片串流。 此圖表會使用 [DV Muxer](dv-muxer-filter.md) 篩選器來合併音訊和影片串流。 它會將交錯資料流程傳送至 MSDV 篩選器，但再次分割資料流程以供預覽。

建立此圖形，如下所示：


```C++
// Add the DV Mux filter to the graph.
IBaseFilter *pDVMux;
hr = CoCreateInstance(CLSID_DVMux, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVMux));
hr = pGraph->AddFilter(pDVMux, L"DV Mux");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(L"C:\\Example2.avi", L"Source", 
    &pFileSource);

hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pTee);
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pTee, 0, 0);
```



此程式碼會對 **RenderStream** 進行數個呼叫：

前兩個將來源篩選連接到 AVI 分隔器，並將 AVI 分隔器連接至 DV Mux。 在第一個呼叫中，Capture Graph Builder 會自動將 avi 分隔器新增至圖形，並將其中一個 avi 分隔器的輸出接點連接至 DV Mux。 在第二個呼叫中，Capture Graph Builder 會尋找 AVI 分隔器的第二個輸出圖釘，並將其連接至 DV Mux。

**RenderStream** 的第三個呼叫會將 DV Muxer 連接到無限 Pin 指標的篩選準則。 下一個呼叫會將一個資料流程從無限的 Pin 碼 t 連接至 MSDV capture 篩選器。 此資料流程會傳輸到裝置。 最後一次呼叫 **RenderStream** 時，會建立圖形的預覽區段。

如果您不想要在傳輸時預覽，可以省略無限的 Pin 碼，然後直接將 DV Mux 連接到 MSDV 篩選器：


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 




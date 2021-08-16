---
description: 將 DV 捕獲到未壓縮的 RGB
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: 將 DV 捕獲到未壓縮的 RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb721dba2912774dd7cad18871484a9d578458161d78ea402261858cac03aa65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966761"
---
# <a name="capture-dv-to-uncompressed-rgb"></a>將 DV 捕獲到未壓縮的 RGB

此範例示範如何從攝影機捕獲 DV，並在預覽期間將其儲存為未壓縮 RGB 的檔案。 使用下圖所示的篩選圖形。

![將未壓縮的 rgb 捕獲至檔案](images/dv-rgb-cap.png)

DV 分隔器篩選器會將交錯的音訊/影片分割成個別的影片和音訊串流，DV 編碼的影片會進入 [Dv 影片解碼](dv-video-decoder-filter.md) 篩選器，輸出未壓縮的 RGB 影片。 RGB 影片會透過智慧型輸出篩選器，路由至適用于 capture) 的 AVI Mux 篩選器 (，以及預覽)  (的影片轉譯器。 同時，來自 DV 分隔器的音訊串流會透過無限的 Pin 指標篩選至 AVI Mux 和音訊轉譯器。 篩選 Graph 管理員會使用範例上的時間戳記和 Graph 參考時鐘，將所有這些資料流程保持同步處理。

此圖表看起來可能很複雜，但它可確保 DV 編碼的影片資料流程只會解碼一次，以將 CPU 需求降至最低。 另外也請注意，當音訊流經無限釘選的篩選器時，影片就會經過智慧型指標篩選。 Smart t 可以卸載預覽畫面來改善捕捉效能，這對影片來說很理想，但對於音訊來說則很有説明，而捨棄的範例會很明顯。 此外，因為音訊需要的頻寬遠低於影片，所以在檔案中放置音訊的機會相當少。

您必須一次在一個區段上建立這個圖形，但 RenderStream 方法仍可提供協助。 使用下列程式碼：


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



您必須建立 DV 分隔器、DV 影片解碼、智慧型指標和無限圖釘指標篩選器，並將每個篩選器新增至篩選圖形。  (為了簡潔起見，已從先前的程式碼中省略這些步驟。 ) 此範例會使用 [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法來尋找智慧 t 篩選器上的捕捉和預覽釘選;capture 一律會輸出 pin 0，而預覽是輸出針腳1。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 




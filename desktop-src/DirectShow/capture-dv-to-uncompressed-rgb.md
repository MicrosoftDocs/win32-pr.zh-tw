---
description: 將 DV 捕獲到未壓縮的 RGB
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: 將 DV 捕獲到未壓縮的 RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108597"
---
# <a name="capture-dv-to-uncompressed-rgb"></a><span data-ttu-id="6ec1d-103">將 DV 捕獲到未壓縮的 RGB</span><span class="sxs-lookup"><span data-stu-id="6ec1d-103">Capture DV to Uncompressed RGB</span></span>

<span data-ttu-id="6ec1d-104">此範例示範如何從攝影機捕獲 DV，並在預覽期間將其儲存為未壓縮 RGB 的檔案。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-104">This example shows how to capture DV from the camcorder and save it to a file as uncompressed RGB while previewing.</span></span> <span data-ttu-id="6ec1d-105">使用下圖所示的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-105">Use the filter graph shown in the following diagram.</span></span>

![將未壓縮的 rgb 捕獲至檔案](images/dv-rgb-cap.png)

<span data-ttu-id="6ec1d-107">DV 分隔器篩選器會將交錯的音訊/影片分割成個別的影片和音訊串流，DV 編碼的影片會進入 [Dv 影片解碼](dv-video-decoder-filter.md) 篩選器，輸出未壓縮的 RGB 影片。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-107">The DV Splitter filter splits the interleaved audio/video into separate video and audio streams The DV-encoded video goes to the [DV Video Decoder](dv-video-decoder-filter.md) filter, which outputs uncompressed RGB video.</span></span> <span data-ttu-id="6ec1d-108">RGB 影片會透過智慧型輸出篩選器，路由至適用于 capture) 的 AVI Mux 篩選器 (，以及預覽)  (的影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-108">The RGB video is routed through the Smart Tee filter to the AVI Mux filter (for capture) and the video renderer (for preview).</span></span> <span data-ttu-id="6ec1d-109">同時，來自 DV 分隔器的音訊串流會透過無限的 Pin 指標篩選至 AVI Mux 和音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-109">Meanwhile, the audio stream from the DV Splitter goes through the Infinite Pin Tee filter to the AVI Mux and the audio renderer.</span></span> <span data-ttu-id="6ec1d-110">篩選圖形管理員會使用範例上的時間戳記和 Graph 參考時鐘，將所有這些資料流程保持同步處理。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-110">The Filter Graph Manager keeps all of these streams synchronized, using the time stamps on the samples and the graph reference clock.</span></span>

<span data-ttu-id="6ec1d-111">此圖表看起來可能很複雜，但它可確保 DV 編碼的影片資料流程只會解碼一次，以將 CPU 需求降至最低。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-111">This graph might seem unnecessarily complicated, but it ensures that the DV-encoded video stream is decoded only once, which minimizes the CPU requirements.</span></span> <span data-ttu-id="6ec1d-112">另外也請注意，當音訊流經無限釘選的篩選器時，影片就會經過智慧型指標篩選。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-112">Also, note that the video goes through the Smart Tee filter while the audio goes through the Infinite Pin Tee filter.</span></span> <span data-ttu-id="6ec1d-113">Smart t 可以卸載預覽畫面來改善捕捉效能，這對影片來說很理想，但對於音訊來說則很有説明，而捨棄的範例會很明顯。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-113">The Smart Tee can drop preview frames to improve capture performance, which is desirable for video but not for audio, where dropped samples are highly noticeable.</span></span> <span data-ttu-id="6ec1d-114">此外，因為音訊需要的頻寬遠低於影片，所以在檔案中放置音訊的機會相當少。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-114">Also, because the audio requires much lower bandwidth than the video, there is relatively little chance of dropping audio in the file.</span></span>

<span data-ttu-id="6ec1d-115">您必須一次在一個區段上建立這個圖形，但 RenderStream 方法仍可提供協助。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-115">You must build this graph one section at a time, but the RenderStream method can still help.</span></span> <span data-ttu-id="6ec1d-116">使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="6ec1d-116">Use the following code:</span></span>


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



<span data-ttu-id="6ec1d-117">您必須建立 DV 分隔器、DV 影片解碼、智慧型指標和無限圖釘指標篩選器，並將每個篩選器新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-117">You must create the DV Splitter, DV Video Decoder, Smart Tee, and Infinite Pin Tee filters, and add each one to the filter graph.</span></span> <span data-ttu-id="6ec1d-118"> (為了簡潔起見，已從先前的程式碼中省略這些步驟。 ) 此範例會使用 [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法來尋找智慧 t 篩選器上的捕捉和預覽釘選;capture 一律會輸出 pin 0，而預覽是輸出針腳1。</span><span class="sxs-lookup"><span data-stu-id="6ec1d-118">(For brevity, these steps are omitted from the previous code.) This example uses the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to find the capture and preview pins on the Smart Tee filter; capture is always output pin 0, and preview is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ec1d-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ec1d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ec1d-120">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="6ec1d-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




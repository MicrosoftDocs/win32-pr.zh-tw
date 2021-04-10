---
description: 從類型2檔案傳輸
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: 從類型2檔案傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e15cb0b3aae5b5119739f327a84204730c9d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944436"
---
# <a name="transmit-from-type-2-file"></a><span data-ttu-id="d7a8a-103">從類型2檔案傳輸</span><span class="sxs-lookup"><span data-stu-id="d7a8a-103">Transmit from Type-2 File</span></span>

<span data-ttu-id="d7a8a-104">若要在預覽時傳輸類型2檔案，請使用下圖所示的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-104">To transmit a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![類型2傳輸與預覽](images/dv2-transmit.png)

<span data-ttu-id="d7a8a-106">類型2檔案有兩個數據流、一個音訊串流和一個 DV 編碼的影片串流。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-106">A type-2 file has two streams, one audio stream and one DV-encoded video stream.</span></span> <span data-ttu-id="d7a8a-107">此圖表會使用 [DV Muxer](dv-muxer-filter.md) 篩選器來合併音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-107">This graph uses the [DV Muxer](dv-muxer-filter.md) filter to combine the audio and video streams.</span></span> <span data-ttu-id="d7a8a-108">它會將交錯資料流程傳送至 MSDV 篩選器，但再次分割資料流程以供預覽。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-108">It sends the interleaved stream to the MSDV filter, but splits the stream again for preview.</span></span>

<span data-ttu-id="d7a8a-109">建立此圖形，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d7a8a-109">Build this graph as follows:</span></span>


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



<span data-ttu-id="d7a8a-110">此程式碼會對 **RenderStream** 進行數個呼叫：</span><span class="sxs-lookup"><span data-stu-id="d7a8a-110">This code makes several calls to **RenderStream**:</span></span>

<span data-ttu-id="d7a8a-111">前兩個將來源篩選連接到 AVI 分隔器，並將 AVI 分隔器連接至 DV Mux。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-111">The first two connect the source filter to the AVI Splitter and the AVI Splitter to the DV Mux.</span></span> <span data-ttu-id="d7a8a-112">在第一次呼叫時，「捕獲圖形產生器」會自動將 AVI 分隔器加入至圖形，並將其中一個 AVI 分隔器的輸出接點連接至 DV Mux。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-112">In the first call, the Capture Graph Builder automatically adds the AVI Splitter to the graph and connects one of the AVI Splitter's output pins to the DV Mux.</span></span> <span data-ttu-id="d7a8a-113">在第二個呼叫中，Capture Graph Builder 會尋找 AVI 分隔器的第二個輸出圖釘，並將其連接至 DV Mux。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-113">In the second call, the Capture Graph Builder finds the AVI Splitter's second output pin and connects that to the DV Mux.</span></span>

<span data-ttu-id="d7a8a-114">**RenderStream** 的第三個呼叫會將 DV Muxer 連接到無限 Pin 指標的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-114">The third call to **RenderStream** connects the DV Muxer to the Infinite Pin Tee filter.</span></span> <span data-ttu-id="d7a8a-115">下一個呼叫會將一個資料流程從無限的 Pin 碼 t 連接至 MSDV capture 篩選器。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-115">The next call connects one stream from the Infinite Pin Tee to the MSDV capture filter.</span></span> <span data-ttu-id="d7a8a-116">此資料流程會傳輸到裝置。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-116">This stream is transmitted to the device.</span></span> <span data-ttu-id="d7a8a-117">最後一次呼叫 **RenderStream** 時，會建立圖形的預覽區段。</span><span class="sxs-lookup"><span data-stu-id="d7a8a-117">The last call to **RenderStream** builds the preview section of the graph.</span></span>

<span data-ttu-id="d7a8a-118">如果您不想要在傳輸時預覽，可以省略無限的 Pin 碼，然後直接將 DV Mux 連接到 MSDV 篩選器：</span><span class="sxs-lookup"><span data-stu-id="d7a8a-118">If you do not want to preview while transmitting, you can omit the Infinite Pin Tee, and simply connect the DV Mux to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="d7a8a-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7a8a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7a8a-120">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="d7a8a-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




---
description: 關於 DirectShow 篩選
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: 關於 DirectShow 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104554026"
---
# <a name="about-directshow-filters"></a><span data-ttu-id="3ad93-103">關於 DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="3ad93-103">About DirectShow Filters</span></span>

<span data-ttu-id="3ad93-104">DirectShow 使用模組化架構，其中每個處理階段都是由稱為篩選的 COM 物件來完成。</span><span class="sxs-lookup"><span data-stu-id="3ad93-104">DirectShow uses a modular architecture, where each stage of processing is done by a COM object called a filter.</span></span> <span data-ttu-id="3ad93-105">DirectShow 針對要使用的應用程式提供一組標準篩選器，而開發人員可以撰寫自己的自訂篩選器，以擴充 DirectShow 的功能。</span><span class="sxs-lookup"><span data-stu-id="3ad93-105">DirectShow provides a set of standard filters for applications to use, and developers can write their own custom filters that extend the functionality of DirectShow.</span></span> <span data-ttu-id="3ad93-106">為了說明，以下是播放 AVI 影片檔案時所需的步驟，以及執行每個步驟的篩選：</span><span class="sxs-lookup"><span data-stu-id="3ad93-106">To illustrate, here are the steps needed to play an AVI video file, along with the filters that perform each step:</span></span>

-   <span data-ttu-id="3ad93-107">將檔案中的原始資料讀取為位元組資料流程， (檔案來源篩選) 。</span><span class="sxs-lookup"><span data-stu-id="3ad93-107">Read the raw data from the file as a byte stream (File Source filter).</span></span>
-   <span data-ttu-id="3ad93-108">檢查 AVI 標頭，並將位元組資料流程剖析為個別的影片框架和音訊範例， (AVI 分隔器篩選) 。</span><span class="sxs-lookup"><span data-stu-id="3ad93-108">Examine the AVI headers, and parse the byte stream into separate video frames and audio samples (AVI Splitter filter).</span></span>
-   <span data-ttu-id="3ad93-109">根據壓縮格式) ，將影片框架 (各種不同的解碼器篩選器。</span><span class="sxs-lookup"><span data-stu-id="3ad93-109">Decode the video frames (various decoder filters, depending on the compression format).</span></span>
-   <span data-ttu-id="3ad93-110"> (影片轉譯器篩選) 繪製影片畫面格。</span><span class="sxs-lookup"><span data-stu-id="3ad93-110">Draw the video frames (Video Renderer filter).</span></span>
-   <span data-ttu-id="3ad93-111">將音訊範例傳送至音效卡 (預設 DirectSound 裝置篩選) 。</span><span class="sxs-lookup"><span data-stu-id="3ad93-111">Send the audio samples to the sound card (Default DirectSound Device filter).</span></span>

<span data-ttu-id="3ad93-112">下圖顯示這些篩選器。</span><span class="sxs-lookup"><span data-stu-id="3ad93-112">These filters are shown in the following diagram.</span></span>

![使用壓縮影片播放 avi 檔案的篩選圖形](images/avi-filter-graph.png)

<span data-ttu-id="3ad93-114">如圖所示，每個篩選器都連接到一個或多個其他篩選器。</span><span class="sxs-lookup"><span data-stu-id="3ad93-114">As the diagram shows, each filter is connected to one or more other filters.</span></span> <span data-ttu-id="3ad93-115">連接點也是 COM 物件，稱為「 *釘* 選」。</span><span class="sxs-lookup"><span data-stu-id="3ad93-115">The connection points are also COM objects, called *pins*.</span></span> <span data-ttu-id="3ad93-116">篩選器會使用釘選，在下一個篩選器中移動資料。</span><span class="sxs-lookup"><span data-stu-id="3ad93-116">Filters use pins to move data from one filter the next.</span></span> <span data-ttu-id="3ad93-117">圖中的箭號會顯示資料的移動方向。</span><span class="sxs-lookup"><span data-stu-id="3ad93-117">The arrows in the diagram show the direction in which the data travels.</span></span> <span data-ttu-id="3ad93-118">在 DirectShow 中，一組篩選器稱為 *篩選圖形*。</span><span class="sxs-lookup"><span data-stu-id="3ad93-118">In DirectShow, a set of filters is called a *filter graph*.</span></span>

<span data-ttu-id="3ad93-119">篩選具有三種可能的狀態：執行中、已停止和已暫停。</span><span class="sxs-lookup"><span data-stu-id="3ad93-119">Filters have three possible states: running, stopped, and paused.</span></span> <span data-ttu-id="3ad93-120">當篩選準則正在執行時，它會處理媒體資料。</span><span class="sxs-lookup"><span data-stu-id="3ad93-120">When a filter is running, it processes media data.</span></span> <span data-ttu-id="3ad93-121">當它停止時，它會停止處理資料。</span><span class="sxs-lookup"><span data-stu-id="3ad93-121">When it is stopped, it stops processing data.</span></span> <span data-ttu-id="3ad93-122">暫停狀態是用來在執行之前提示資料; [篩選圖形中](data-flow-in-the-filter-graph.md) 的「資料流程」一節會更詳細地說明此概念。</span><span class="sxs-lookup"><span data-stu-id="3ad93-122">The paused state is used to cue data before running; the section [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) describes this concept in more detail.</span></span> <span data-ttu-id="3ad93-123">在極少數的例外狀況下，狀態變更會在整個篩選圖形中進行協調;圖形交換器中的所有篩選準則都有一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="3ad93-123">With very rare exceptions, state changes are coordinated throughout the entire filter graph; all the filters in the graph switch states in unison.</span></span> <span data-ttu-id="3ad93-124">因此，整個篩選圖形也稱為「正在執行」、「已停止」或「已暫停」。</span><span class="sxs-lookup"><span data-stu-id="3ad93-124">Thus, the entire filter graph is also said to be running, stopped, or paused.</span></span>

<span data-ttu-id="3ad93-125">篩選可以分為數個廣泛的類別：</span><span class="sxs-lookup"><span data-stu-id="3ad93-125">Filters can be grouped into several broad categories:</span></span>

-   <span data-ttu-id="3ad93-126">*來源* 篩選器會將資料引進圖形。</span><span class="sxs-lookup"><span data-stu-id="3ad93-126">A *source* filter introduces data into the graph.</span></span> <span data-ttu-id="3ad93-127">資料可能來自檔案、網路、相機或其他地方。</span><span class="sxs-lookup"><span data-stu-id="3ad93-127">The data might come from a file, a network, a camera, or anywhere else.</span></span> <span data-ttu-id="3ad93-128">每個來源篩選器會處理不同類型的資料來源。</span><span class="sxs-lookup"><span data-stu-id="3ad93-128">Each source filter handles a different type of data source.</span></span>
-   <span data-ttu-id="3ad93-129">*轉換* 篩選會接受輸入資料流程、處理資料，以及建立輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="3ad93-129">A *transform* filter takes an input stream, processes the data, and creates an output stream.</span></span> <span data-ttu-id="3ad93-130">編碼器和解碼器是轉換篩選準則的範例。</span><span class="sxs-lookup"><span data-stu-id="3ad93-130">Encoders and decoders are examples of transform filters.</span></span>
-   <span data-ttu-id="3ad93-131">轉譯 *器篩選* 器位於鏈結尾。</span><span class="sxs-lookup"><span data-stu-id="3ad93-131">*Renderer* filters sit at the end of the chain.</span></span> <span data-ttu-id="3ad93-132">他們會接收資料並向使用者呈現資料。</span><span class="sxs-lookup"><span data-stu-id="3ad93-132">They receive data and present it to the user.</span></span> <span data-ttu-id="3ad93-133">例如，影片轉譯器會在顯示器上繪製影片畫面;音訊轉譯器會將音訊資料傳送至音效卡;檔案寫入器篩選器會將資料寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="3ad93-133">For example, a video renderer draws video frames on the display; an audio renderer sends audio data to the sound card; and a file-writer filter writes data to a file.</span></span>
-   <span data-ttu-id="3ad93-134">*分隔* 器篩選器會將輸入資料流程分割成兩個或多個輸出，通常會在一種情況下剖析輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="3ad93-134">A *splitter* filter splits an input stream into two or more outputs, typically parsing the input stream along the way.</span></span> <span data-ttu-id="3ad93-135">例如，AVI 分隔器會將位元組資料流程剖析為個別的影片和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="3ad93-135">For example, the AVI Splitter parses a byte stream into separate video and audio streams.</span></span>
-   <span data-ttu-id="3ad93-136">*Mux* 篩選器會接受多個輸入，並將它們結合成單一資料流程。</span><span class="sxs-lookup"><span data-stu-id="3ad93-136">A *mux* filter takes multiple inputs and combines them into a single stream.</span></span> <span data-ttu-id="3ad93-137">例如，AVI Mux 會執行 AVI 分隔器的反向操作。</span><span class="sxs-lookup"><span data-stu-id="3ad93-137">For example, the AVI Mux performs the inverse operation of the AVI Splitter.</span></span> <span data-ttu-id="3ad93-138">它會取得音訊和影片串流，並產生 AVI 格式的位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="3ad93-138">It takes audio and video streams and produces an AVI-formatted byte stream.</span></span>

<span data-ttu-id="3ad93-139">這些類別之間的差異不是絕對的。</span><span class="sxs-lookup"><span data-stu-id="3ad93-139">The distinctions between these categories are not absolute.</span></span> <span data-ttu-id="3ad93-140">例如，ASF 讀取器篩選器可作為來源篩選器和分隔器篩選器。</span><span class="sxs-lookup"><span data-stu-id="3ad93-140">For example, the ASF Reader filter acts as both a source filter and a splitter filter.</span></span>

<span data-ttu-id="3ad93-141">所有的 DirectShow 濾波器都會公開 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面，而所有的釘選都會公開 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面。</span><span class="sxs-lookup"><span data-stu-id="3ad93-141">All DirectShow filters expose the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, and all pins expose the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="3ad93-142">DirectShow 也會定義許多其他支援更特定功能的介面。</span><span class="sxs-lookup"><span data-stu-id="3ad93-142">DirectShow also defines many other interfaces that support more specific functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ad93-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ad93-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ad93-144">關於篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="3ad93-144">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
</dt> <dt>

[<span data-ttu-id="3ad93-145">篩選圖形中的資料流程</span><span class="sxs-lookup"><span data-stu-id="3ad93-145">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="3ad93-146">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="3ad93-146">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




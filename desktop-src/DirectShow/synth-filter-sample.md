---
description: 合成濾波器範例
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: 合成濾波器範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852403"
---
# <a name="synth-filter-sample"></a><span data-ttu-id="e50de-103">合成濾波器範例</span><span class="sxs-lookup"><span data-stu-id="e50de-103">Synth Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="e50de-104">Description</span><span class="sxs-lookup"><span data-stu-id="e50de-104">Description</span></span>

<span data-ttu-id="e50de-105">合成濾波器是產生音訊波形的來源篩選器。</span><span class="sxs-lookup"><span data-stu-id="e50de-105">The Synth filter is a source filter that generates audio waveforms.</span></span>

<span data-ttu-id="e50de-106">此篩選器說明動態圖形建築物。</span><span class="sxs-lookup"><span data-stu-id="e50de-106">This filter illustrates dynamic graph building.</span></span> <span data-ttu-id="e50de-107">它可以在未壓縮的 PCM 音訊與壓縮的 MS ADPCM 之間切換 \_ (Microsoft 彈性 Delta 脈衝 Code 調製) 格式。</span><span class="sxs-lookup"><span data-stu-id="e50de-107">It can switch between uncompressed PCM audio and compressed MS\_ADPCM (Microsoft Adaptive Delta Pulse Code Modulation) format.</span></span>

<span data-ttu-id="e50de-108">此篩選器會以「音訊合成器篩選」的形式出現在 GraphEdit 中。</span><span class="sxs-lookup"><span data-stu-id="e50de-108">This filter appears in GraphEdit as "Audio Synthesizer Filter."</span></span>

<span data-ttu-id="e50de-109">如需動態圖形建築物的詳細資訊，請參閱 [動態圖形建築物](dynamic-graph-building.md)。</span><span class="sxs-lookup"><span data-stu-id="e50de-109">For more information about dynamic graph building, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="usage"></a><span data-ttu-id="e50de-110">使用方式</span><span class="sxs-lookup"><span data-stu-id="e50de-110">Usage</span></span>

<span data-ttu-id="e50de-111">合成篩選器可讓使用者透過屬性頁設定波形、頻率、通道數目和其他屬性。</span><span class="sxs-lookup"><span data-stu-id="e50de-111">The Synth filter enables the user to set the waveform, frequency, number of channels, and other properties through the property page.</span></span> <span data-ttu-id="e50de-112">若要設定掃描頻率範圍的上方或較低端點，請按住 SHIFT 鍵，同時調整頻率滑杆。</span><span class="sxs-lookup"><span data-stu-id="e50de-112">To set either the upper or lower endpoint of the swept frequency range, hold down SHIFT while adjusting the frequency slider.</span></span> <span data-ttu-id="e50de-113">篩選也支援自訂介面 ISynth2，以設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e50de-113">The filter also supports a custom interface, ISynth2, for setting these properties.</span></span>

<span data-ttu-id="e50de-114">若要示範動態圖形建立功能，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e50de-114">To demonstrate the dynamic graph building feature, do the following:</span></span>

1.  <span data-ttu-id="e50de-115">建立篩選器，並使用 Regsvr32 公用程式進行註冊。</span><span class="sxs-lookup"><span data-stu-id="e50de-115">Build the filter and register it with the Regsvr32 utility.</span></span>
2.  <span data-ttu-id="e50de-116">啟動 GraphEdit。</span><span class="sxs-lookup"><span data-stu-id="e50de-116">Launch GraphEdit.</span></span>
3.  <span data-ttu-id="e50de-117">插入音訊合成器篩選器。</span><span class="sxs-lookup"><span data-stu-id="e50de-117">Insert the Audio Synthesizer filter.</span></span> <span data-ttu-id="e50de-118">它會出現在 [DirectShow 篩選準則] 分類中。</span><span class="sxs-lookup"><span data-stu-id="e50de-118">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="e50de-119">轉譯篩選的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="e50de-119">Render the filter's output pin.</span></span>
5.  <span data-ttu-id="e50de-120">按一下 [ **播放** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="e50de-120">Click the **Play** button.</span></span>
6.  <span data-ttu-id="e50de-121">開啟篩選的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="e50de-121">Open the filter's property page.</span></span>
7.  <span data-ttu-id="e50de-122">在 [輸出格式] 區域中，選取 [PCM] 或 [Microsoft ADPCM]。</span><span class="sxs-lookup"><span data-stu-id="e50de-122">In the Output Format area, select PCM or Microsoft ADPCM.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="e50de-123">程式設計附注</span><span class="sxs-lookup"><span data-stu-id="e50de-123">Programming Notes</span></span>

<span data-ttu-id="e50de-124">此範例包含下列檔案：</span><span class="sxs-lookup"><span data-stu-id="e50de-124">This sample contains the following files:</span></span>

-   <span data-ttu-id="e50de-125">Dynsrc .h （Dynsrc .cpp：）包含兩個來源篩選準則的基類，這些類別支援動態圖形建立、CDynamicSource 和 CDynamicSourceStream。</span><span class="sxs-lookup"><span data-stu-id="e50de-125">Dynsrc.h, Dynsrc.cpp: Contains two base classes for source filters that support dynamic graph building, CDynamicSource and CDynamicSourceStream.</span></span>
-   <span data-ttu-id="e50de-126">ISynth：宣告用來設定篩選準則屬性的自訂 ISynth2 介面。</span><span class="sxs-lookup"><span data-stu-id="e50de-126">ISynth.h: Declares the custom ISynth2 interface for setting properties on the filter.</span></span>
-   <span data-ttu-id="e50de-127">資源 .h：包含資源常數。</span><span class="sxs-lookup"><span data-stu-id="e50de-127">Resource.h: Contains resource constants.</span></span>
-   <span data-ttu-id="e50de-128">.Def：匯出 COM 程式庫所需的 DLL 函式。</span><span class="sxs-lookup"><span data-stu-id="e50de-128">Synth.def: Exports the DLL functions needed by the COM library.</span></span>
-   <span data-ttu-id="e50de-129">CAudioSynth 類別會產生音訊資料，而 CSynthFilter 類別則是用來執行此篩選器。</span><span class="sxs-lookup"><span data-stu-id="e50de-129">Synth.h, Synth.cpp: Contains the CAudioSynth class, which generates the audio data, and the CSynthFilter class, which implements the filter.</span></span>
-   <span data-ttu-id="e50de-130">合成 .rc：包含篩選所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="e50de-130">Synth.rc: Contains resources used by the filter.</span></span>
-   <span data-ttu-id="e50de-131">Synthprp .h、Synthprp .cpp：執行篩選的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="e50de-131">Synthprp.h, Synthprp.cpp: Implements the filter's property page.</span></span>

<span data-ttu-id="e50de-132">CDynamicSource 類別是從 [**CSource**](csource.md) 基類進行調整。</span><span class="sxs-lookup"><span data-stu-id="e50de-132">The CDynamicSource class is adapted from the [**CSource**](csource.md) base class.</span></span> <span data-ttu-id="e50de-133">它會使用一個或多個衍生自 CDynamicSourceStream 類別的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="e50de-133">It uses one or more output pins derived from the CDynamicSourceStream class.</span></span> <span data-ttu-id="e50de-134">CDynamicSourceStream 類別是從 [**CSourceStream**](csourcestream.md) 類別進行調整，但衍生自 [**CDynamicOutputPin**](cdynamicoutputpin.md) 類別，而不是 [**CBaseOutputPin**](cbaseoutputpin.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="e50de-134">The CDynamicSourceStream class is adapted from the [**CSourceStream**](csourcestream.md) class, but derives from the [**CDynamicOutputPin**](cdynamicoutputpin.md) class rather than the [**CBaseOutputPin**](cbaseoutputpin.md) class.</span></span>

<span data-ttu-id="e50de-135">CDynamicSource 類別在 [**CSource**](csource.md)中找不到下列方法：</span><span class="sxs-lookup"><span data-stu-id="e50de-135">The CDynamicSource class has the following methods not found in [**CSource**](csource.md):</span></span>

-   <span data-ttu-id="e50de-136">停止：發出停止事件 ([**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) ，然後關閉背景工作執行緒以取得所有未連接的 pin。</span><span class="sxs-lookup"><span data-stu-id="e50de-136">Stop: Signals the stop event ([**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md)), and shuts down the worker thread for all unconnected pins.</span></span> <span data-ttu-id="e50de-137">在連接的釘選上，pin 的非使用中方法會關閉背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="e50de-137">On a connected pin, the pin's Inactive method will shut down the worker thread.</span></span>
-   <span data-ttu-id="e50de-138">Pause：重設停止事件。</span><span class="sxs-lookup"><span data-stu-id="e50de-138">Pause: Resets the stop event.</span></span>
-   <span data-ttu-id="e50de-139">JoinFilterGraph：呼叫每個 pin 的 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e50de-139">JoinFilterGraph: Calls the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method on each pin.</span></span>

<span data-ttu-id="e50de-140">CDynamicSourceStream 類別在 [**CSourceStream**](csourcestream.md)中找不到下列方法：</span><span class="sxs-lookup"><span data-stu-id="e50de-140">The CDynamicSourceStream class has the following methods not found in [**CSourceStream**](csourcestream.md):</span></span>

-   <span data-ttu-id="e50de-141">DestroySourceThread：關閉背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="e50de-141">DestroySourceThread: Shuts down the worker thread.</span></span>
-   <span data-ttu-id="e50de-142">FatalError：對篩選圖形管理員發出錯誤信號。</span><span class="sxs-lookup"><span data-stu-id="e50de-142">FatalError: Signals an error to the filter graph manager.</span></span>
-   <span data-ttu-id="e50de-143">OutputPinNeedsToBeReconnected：表示輸出 pin 應重新連接。</span><span class="sxs-lookup"><span data-stu-id="e50de-143">OutputPinNeedsToBeReconnected: Signals that the output pin should be reconnected.</span></span> <span data-ttu-id="e50de-144">當呼叫這個方法時，背景工作執行緒會呼叫 [**CDynamicOutputPin：:D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) 方法來重新連接釘選。</span><span class="sxs-lookup"><span data-stu-id="e50de-144">When this method is called, the worker thread calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to reconnect the pin.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="e50de-145">下載範例</span><span class="sxs-lookup"><span data-stu-id="e50de-145">Downloading the Sample</span></span>

<span data-ttu-id="e50de-146">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e50de-146">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="e50de-147">此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 濾波器 \\ 合成。</span><span class="sxs-lookup"><span data-stu-id="e50de-147">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Synth.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e50de-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="e50de-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e50de-149">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="e50de-149">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 




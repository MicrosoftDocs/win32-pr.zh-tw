---
description: Metronome 篩選範例
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Metronome 篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970501"
---
# <a name="metronome-filter-sample"></a><span data-ttu-id="b17b0-103">Metronome 篩選範例</span><span class="sxs-lookup"><span data-stu-id="b17b0-103">Metronome Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="b17b0-104">Description</span><span class="sxs-lookup"><span data-stu-id="b17b0-104">Description</span></span>

<span data-ttu-id="b17b0-105">此範例篩選會顯示如何執行參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="b17b0-105">This sample filter shows how to implement a reference clock.</span></span> <span data-ttu-id="b17b0-106">此篩選器會使用您的預設麥克風輸入來接聽音訊尖峰 (例如點擊、手拍手聲或咳嗽) ，以用來判斷時脈速率。</span><span class="sxs-lookup"><span data-stu-id="b17b0-106">The filter uses your default microphone input to listen for audio spikes (such as clicks, hand claps, or coughs), which it uses to determine a clock rate.</span></span>

## <a name="usage"></a><span data-ttu-id="b17b0-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="b17b0-107">Usage</span></span>

<span data-ttu-id="b17b0-108">建立範例專案，並將篩選 DLL (Metronom.ax) 複製到您的 Windows 系統目錄。</span><span class="sxs-lookup"><span data-stu-id="b17b0-108">Build the sample project and copy the filter DLL (Metronom.ax) to your Windows system directory.</span></span> <span data-ttu-id="b17b0-109">執行 Metronom .reg 檔案以註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="b17b0-109">Run the Metronom.reg file to register the DLL.</span></span>

<span data-ttu-id="b17b0-110">若要使用篩選準則：</span><span class="sxs-lookup"><span data-stu-id="b17b0-110">To use the filter:</span></span>

1.  <span data-ttu-id="b17b0-111">在呈現影片資料流程的 GraphEdit 中建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="b17b0-111">Build a filter graph in GraphEdit that renders a video stream.</span></span>
2.  <span data-ttu-id="b17b0-112">刪除任何呈現的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="b17b0-112">Delete any rendered audio streams.</span></span>
3.  <span data-ttu-id="b17b0-113">將 Metronome 篩選器新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="b17b0-113">Add the Metronome filter to the graph.</span></span> <span data-ttu-id="b17b0-114">它會出現在 [DirectShow 篩選準則] 分類中。</span><span class="sxs-lookup"><span data-stu-id="b17b0-114">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="b17b0-115">執行圖形。</span><span class="sxs-lookup"><span data-stu-id="b17b0-115">Run the graph.</span></span> <span data-ttu-id="b17b0-116">影片將會以正常速度開始播放。</span><span class="sxs-lookup"><span data-stu-id="b17b0-116">The video will begin playing at normal speed.</span></span>
5.  <span data-ttu-id="b17b0-117">Clap 您的手，或使用 metronome 來設定新的速度。</span><span class="sxs-lookup"><span data-stu-id="b17b0-117">Clap your hands or use a metronome to set a new speed.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="b17b0-118">程式設計附注</span><span class="sxs-lookup"><span data-stu-id="b17b0-118">Programming Notes</span></span>

<span data-ttu-id="b17b0-119">此篩選器只適用于影片。</span><span class="sxs-lookup"><span data-stu-id="b17b0-119">This filter works only for video.</span></span> <span data-ttu-id="b17b0-120">音訊轉譯器無法同步處理至截然不同的頻率。</span><span class="sxs-lookup"><span data-stu-id="b17b0-120">The audio renderer is not capable of synchronizing to radically different clock rates.</span></span>

<span data-ttu-id="b17b0-121">如果您每分鐘 clap 92 次 (每個 ~ 652 ms) 一次，則會以一般費率播放影片。</span><span class="sxs-lookup"><span data-stu-id="b17b0-121">If you clap 92 times per minute (once every ~652 ms), the video will play at the normal rate.</span></span> <span data-ttu-id="b17b0-122">您可以變更 Metronom 中的常數值來變更這個預設值 `BPM` 。</span><span class="sxs-lookup"><span data-stu-id="b17b0-122">You can change this default by changing the value of the constant `BPM` in Metronom.cpp.</span></span>

<span data-ttu-id="b17b0-123">如果您停止鼓掌一段時間，然後再重新開機鼓掌，您必須以大約相同的速度重新開機，否則篩選將會忽略它。</span><span class="sxs-lookup"><span data-stu-id="b17b0-123">If you stop clapping for a period of time and then start clapping again, you must start again at approximately the same speed, or the filter will ignore it.</span></span> <span data-ttu-id="b17b0-124">此外，影片播放速率會受限於 CPU 速度。</span><span class="sxs-lookup"><span data-stu-id="b17b0-124">Also, the video playback rate is limited by the CPU speed.</span></span> <span data-ttu-id="b17b0-125">如果您超過任何時間長度的限制，篩選準則將會停止回應速率變更。</span><span class="sxs-lookup"><span data-stu-id="b17b0-125">If you exceed the limit for any length of time, the filter will stop responding to rate changes.</span></span> <span data-ttu-id="b17b0-126">如果發生這種情況，請停止圖形並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="b17b0-126">If this happens, stop the graph and restart.</span></span>

<span data-ttu-id="b17b0-127">如果您執行自己的時鐘，最重要的規則就是參考時鐘不能反向。</span><span class="sxs-lookup"><span data-stu-id="b17b0-127">If you implement your own clock, the most important rules is that reference clocks must not go backward.</span></span> <span data-ttu-id="b17b0-128">也就是說，它們絕對不能報告時間值小於前一個時間值。</span><span class="sxs-lookup"><span data-stu-id="b17b0-128">That is, they must never report a time value less than the previous time value.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="b17b0-129">下載範例</span><span class="sxs-lookup"><span data-stu-id="b17b0-129">Downloading the Sample</span></span>

<span data-ttu-id="b17b0-130">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b17b0-130">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="b17b0-131">此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ Metronome。</span><span class="sxs-lookup"><span data-stu-id="b17b0-131">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Metronome.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b17b0-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="b17b0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b17b0-133">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="b17b0-133">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="b17b0-134">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="b17b0-134">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 




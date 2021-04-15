---
description: 範圍篩選範例
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: 範圍篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467641"
---
# <a name="scope-filter-sample"></a><span data-ttu-id="7da77-103">範圍篩選範例</span><span class="sxs-lookup"><span data-stu-id="7da77-103">Scope Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="7da77-104">Description</span><span class="sxs-lookup"><span data-stu-id="7da77-104">Description</span></span>

<span data-ttu-id="7da77-105">範圍篩選器是以 wave 形式顯示音效資料的轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="7da77-105">The Scope filter is a renderer filter that displays sound data as wave forms.</span></span>

## <a name="usage"></a><span data-ttu-id="7da77-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="7da77-106">Usage</span></span>

<span data-ttu-id="7da77-107">若要使用此篩選器，請開啟 GraphEdit，然後轉譯音訊檔案 (或包含音訊串流) 的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="7da77-107">To use this filter, open GraphEdit and render an audio file (or a video file with an audio stream).</span></span> <span data-ttu-id="7da77-108">暫時中斷音訊轉譯器的連線，並) 範例篩選器中插入 Infinite-Pin 的 t ([InfTee 濾波器範例](inftee-filter-sample.md) 。</span><span class="sxs-lookup"><span data-stu-id="7da77-108">Disconnect the audio renderer temporarily and insert the Infinite-Pin Tee ([InfTee Filter Sample](inftee-filter-sample.md)) sample filter.</span></span> <span data-ttu-id="7da77-109">重新連線音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="7da77-109">Reconnect the audio renderer.</span></span> <span data-ttu-id="7da77-110">然後將 Infinite-Pin 指標的第二個輸出圖釘連接至範圍篩選器。</span><span class="sxs-lookup"><span data-stu-id="7da77-110">Then connect the Infinite-Pin Tee filter's second output pin to the Scope filter.</span></span> <span data-ttu-id="7da77-111">現在執行圖形。</span><span class="sxs-lookup"><span data-stu-id="7da77-111">Now run the graph.</span></span>

<span data-ttu-id="7da77-112">範圍視窗會實作為對話方塊，而不是實際的視窗。</span><span class="sxs-lookup"><span data-stu-id="7da77-112">The Scope window is implemented as a dialog box, not as an actual window.</span></span> <span data-ttu-id="7da77-113">建立控制台以即時改變篩選參數的開發人員，可能會想要使用像這樣的技巧，而不是屬性頁。</span><span class="sxs-lookup"><span data-stu-id="7da77-113">Developers creating control panels to alter filter parameters in real time might want to use a technique like this rather than property pages.</span></span>

<span data-ttu-id="7da77-114">範圍篩選器會示範如何設定個別的執行緒來處理資料。</span><span class="sxs-lookup"><span data-stu-id="7da77-114">The Scope filter demonstrates setting up a separate thread to process data.</span></span> <span data-ttu-id="7da77-115">在此情況下，資料只會複製到 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法上的另一個緩衝區，然後在另一個執行緒的範圍視窗上進行繪製。</span><span class="sxs-lookup"><span data-stu-id="7da77-115">In this case, the data is just copied to a separate buffer on the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, and is then drawn on the Scope window on the separate thread.</span></span>

<span data-ttu-id="7da77-116">範圍篩選器也可讓您監視音訊輸出，以判斷您是否正在裁剪，以便調整增益。</span><span class="sxs-lookup"><span data-stu-id="7da77-116">The Scope filter also enables you to monitor audio output to determine if you are clipping, so you can adjust the gain.</span></span>

<span data-ttu-id="7da77-117">此篩選器會以 "示波器探棒" 的形式出現在 GraphEdit 中。</span><span class="sxs-lookup"><span data-stu-id="7da77-117">This filter appears in GraphEdit as "Oscilloscope."</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="7da77-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="7da77-118">Downloading the Sample</span></span>

<span data-ttu-id="7da77-119">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7da77-119">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="7da77-120">此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ 範圍。</span><span class="sxs-lookup"><span data-stu-id="7da77-120">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7da77-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="7da77-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7da77-122">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="7da77-122">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 




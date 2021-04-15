---
description: 結合影片捕獲和預覽
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: 結合影片捕獲和預覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467555"
---
# <a name="combining-video-capture-and-preview"></a><span data-ttu-id="6b9a6-103">結合影片捕獲和預覽</span><span class="sxs-lookup"><span data-stu-id="6b9a6-103">Combining Video Capture and Preview</span></span>

<span data-ttu-id="6b9a6-104">前幾節說明如何將影片捕獲到各種不同的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-104">The previous sections describe how to capture video to various file formats.</span></span> <span data-ttu-id="6b9a6-105">[預覽影片](previewing-video.md)一節說明如何建立即時預覽圖形。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-105">The section [Previewing Video](previewing-video.md) describes how to build a live preview graph.</span></span> <span data-ttu-id="6b9a6-106">不過，許多應用程式必須同時進行這兩項作業。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-106">However, many applications must do both at once.</span></span> <span data-ttu-id="6b9a6-107">若要建立合併的預覽和檔案撰寫圖形，只要對 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)進行兩個呼叫即可：</span><span class="sxs-lookup"><span data-stu-id="6b9a6-107">To build a combined preview and file-writing graph, simply make two calls to [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span></span>


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



<span data-ttu-id="6b9a6-108">在此程式碼中，[Capture Graph Builder] 會隱藏一些詳細資料：</span><span class="sxs-lookup"><span data-stu-id="6b9a6-108">In this code, the Capture Graph Builder is hiding some details:</span></span>

-   <span data-ttu-id="6b9a6-109">如果捕捉篩選具有預覽 pin 或影片埠 pin，加上捕捉釘選， [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法就會直接轉譯這兩個針腳，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-109">If the capture filter has a preview pin or video port pin, plus a capture pin, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method simply renders both pins, as shown in the following illustration.</span></span>

    ![捕獲和預覽圖形](images/vidcap04.png)

-   <span data-ttu-id="6b9a6-111">如果篩選準則只有一個捕捉 pin，則「捕獲圖形產生器」會使用 [智慧型](smart-tee-filter.md) 指標篩選器來分割 capture 資料流程。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-111">If the filter has only a capture pin, the Capture Graph Builder uses the [Smart Tee](smart-tee-filter.md) filter to split the capture stream.</span></span> <span data-ttu-id="6b9a6-112">下圖顯示具有智慧型 t 的圖形。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-112">The following illustration shows the graph with a Smart Tee.</span></span>

    ![使用智慧型 t a 濾波器來捕捉和預覽圖形](images/vidcap05.png)

<span data-ttu-id="6b9a6-114">智慧型指標篩選器具有 capture 釘選和預覽 pin。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-114">The Smart Tee filter has a capture pin and a preview pin.</span></span> <span data-ttu-id="6b9a6-115">它會從 capture 篩選器取得單一影片串流，並將其分割成兩個串流，一個用於捕獲，另一個用於預覽。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-115">It takes a single video stream from the capture filter and splits it into two streams, one for capture and one for preview.</span></span> <span data-ttu-id="6b9a6-116">為了維持捕獲 pin 的輸送量，預覽 pin 會視需要卸載畫面格。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-116">To maintain throughput on the capture pin, the preview pin drops frames as needed.</span></span> <span data-ttu-id="6b9a6-117">它也會在傳遞之前，從每個樣本中去除時間戳記，原因是「 [DirectShow 影片捕獲篩選](directshow-video-capture-filters.md)」主題中所討論的原因。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-117">It also strips the time stamps from each sample before delivering it, for the reasons discussed in the topic [DirectShow Video Capture Filters](directshow-video-capture-filters.md).</span></span>

<span data-ttu-id="6b9a6-118">雖然智慧型 t 會分割資料流程，但它並不會實際複製影片資料。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-118">Although the Smart Tee splits the stream, it does not physically duplicate the video data.</span></span> <span data-ttu-id="6b9a6-119">相反地，它會使用共用緩衝區的自訂媒體範例物件。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-119">Instead, it uses custom media sample objects that share the buffers.</span></span> <span data-ttu-id="6b9a6-120">這些範例會標示為「唯讀」，以確保下游篩選不會寫入資料。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-120">The samples are marked "read-only" to ensure that downstream filters do not write on the data.</span></span>

<span data-ttu-id="6b9a6-121">如果您的 capture graph 有預覽視窗，則有幾件事可能會導致篩選圖形管理員停止整個圖形，包括 capture 資料流程：</span><span class="sxs-lookup"><span data-stu-id="6b9a6-121">If your capture graph has a preview window, several things can cause the Filter Graph Manager to stop the entire graph, including the capture stream:</span></span>

-   <span data-ttu-id="6b9a6-122">鎖定電腦。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-122">Locking the computer.</span></span>
-   <span data-ttu-id="6b9a6-123">在屬於網域成員的電腦上按 CTRL + ALT + DELETE。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-123">Pressing CTRL+ALT+DELETE on a computer that is a member of a domain.</span></span>
-   <span data-ttu-id="6b9a6-124">執行全螢幕 Direct3D 應用程式，例如遊戲或螢幕保護裝置程式。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-124">Running a full-screen Direct3D application, such as a game or screen saver.</span></span>
-   <span data-ttu-id="6b9a6-125">切換監視器或變更顯示器解析度。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-125">Switching monitors or changing the display resolution.</span></span>
-   <span data-ttu-id="6b9a6-126">執行程式，讓 Windows 顯示 (UAC) 對話方塊中的 [使用者帳戶控制]。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-126">Running a program that causes Windows to display a User Account Control (UAC) dialog.</span></span> <span data-ttu-id="6b9a6-127"> (Windows Vista 或更新版本。 ) </span><span class="sxs-lookup"><span data-stu-id="6b9a6-127">(Windows Vista or later.)</span></span>
-   <span data-ttu-id="6b9a6-128">正在執行全螢幕 DOS 視窗。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-128">Running a full-screen DOS window.</span></span>

<span data-ttu-id="6b9a6-129">這些事件中的任何一項可能都會中斷捕捉會話，可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-129">Any of these events might interrupt the capture session, possibly causing data loss.</span></span> <span data-ttu-id="6b9a6-130"> (以下是內部發生的情況：影片轉譯器會遺失所需的 Direct3D 或 DirectDraw 資源。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-130">(Here is what happens internally: The video renderer loses the Direct3D or DirectDraw resources that it needs.</span></span> <span data-ttu-id="6b9a6-131">在復原這些資源的過程中，影片轉譯器必須重新連接上游篩選器，導致篩選圖形管理員停止圖形。 ) </span><span class="sxs-lookup"><span data-stu-id="6b9a6-131">In the process of recovering those resources, the video renderer must reconnect with the upstream filter, causing the Filter Graph Manager to stop the graph.)</span></span>

<span data-ttu-id="6b9a6-132">此問題有兩個可能的解決辦法如下：</span><span class="sxs-lookup"><span data-stu-id="6b9a6-132">Two possible solutions to this problem are the following:</span></span>

-   <span data-ttu-id="6b9a6-133">請勿包含預覽資料流程。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-133">Do not include a preview stream.</span></span> <span data-ttu-id="6b9a6-134">不過，請注意，當 capture 裝置有影片埠 pin 時， [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法會自動新增預覽視窗。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-134">However, be aware that the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically adds a preview window when the capture device has a video port pin.</span></span> <span data-ttu-id="6b9a6-135">請參閱檔案 [捕捉中的影片埠 pin](video-port-pins-in-file-capture.md)。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-135">See [Video Port Pins in File Capture](video-port-pins-in-file-capture.md).</span></span>
-   <span data-ttu-id="6b9a6-136">使用串流緩衝區引擎，將預覽資料流程傳送至另一個進程中的圖形。</span><span class="sxs-lookup"><span data-stu-id="6b9a6-136">Use the Stream Buffer Engine to send the preview stream to a graph in another process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b9a6-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b9a6-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b9a6-138">將影片捕獲至檔案</span><span class="sxs-lookup"><span data-stu-id="6b9a6-138">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 




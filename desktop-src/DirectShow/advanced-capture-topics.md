---
description: Advanced Capture 主題
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Advanced Capture 主題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109545"
---
# <a name="advanced-capture-topics"></a><span data-ttu-id="abdee-103">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="abdee-103">Advanced Capture Topics</span></span>

<span data-ttu-id="abdee-104">本節說明 DirectShow 中影片捕獲的一些先進層面。</span><span class="sxs-lookup"><span data-stu-id="abdee-104">This section describes some advanced aspects of video capture in DirectShow.</span></span> <span data-ttu-id="abdee-105">本節所述的大部分問題都會由 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面自動處理。</span><span class="sxs-lookup"><span data-stu-id="abdee-105">Most of the issues described in this section are automatically handled by the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="abdee-106">但是，如果您需要針對影片捕獲應用程式進行疑難排解，這裡的資訊可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="abdee-106">However, the information here may be useful if you need to troubleshoot a video capture application.</span></span> <span data-ttu-id="abdee-107">如果您的應用程式建立某種自訂的捕獲圖形，而且您發現 ICaptureGraphBuilder2 不符合您的需求，也應該閱讀本節。</span><span class="sxs-lookup"><span data-stu-id="abdee-107">You should also read this section if your application builds a custom capture graph of some kind and you find that ICaptureGraphBuilder2 does not suit your needs.</span></span> <span data-ttu-id="abdee-108">最後，本節包含一些有關在影片捕獲應用程式中使用影片混合轉譯器 (VMR) 篩選的資訊。</span><span class="sxs-lookup"><span data-stu-id="abdee-108">Finally, this section contains some information about using the Video Mixing Renderer (VMR) filter in a video capture application.</span></span>

<span data-ttu-id="abdee-109">您可以使用 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 方法，完全建立影片捕獲圖形。</span><span class="sxs-lookup"><span data-stu-id="abdee-109">It is possible to build a video capture graph entirely using [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods.</span></span> <span data-ttu-id="abdee-110">您也可以結合這兩個介面，並使用 ICaptureGraphBuilder2 進行某些工作，並 IGraphBuilder 其他專案。</span><span class="sxs-lookup"><span data-stu-id="abdee-110">You can also combine the two interfaces, using ICaptureGraphBuilder2 for some tasks and IGraphBuilder for others.</span></span>

<span data-ttu-id="abdee-111">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="abdee-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="abdee-112">處理影片捕獲中的重新繪製事件</span><span class="sxs-lookup"><span data-stu-id="abdee-112">Handling Repaint Events in Video Capture</span></span>](handling-repaint-events-in-video-capture.md)
-   [<span data-ttu-id="abdee-113">使用 Pin 類別</span><span class="sxs-lookup"><span data-stu-id="abdee-113">Working with Pin Categories</span></span>](working-with-pin-categories.md)
-   [<span data-ttu-id="abdee-114">使用智慧的 t a 濾波器</span><span class="sxs-lookup"><span data-stu-id="abdee-114">Using the Smart Tee Filter</span></span>](using-the-smart-tee-filter.md)
-   [<span data-ttu-id="abdee-115">使用影片捕獲中的重迭混音器</span><span class="sxs-lookup"><span data-stu-id="abdee-115">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
-   [<span data-ttu-id="abdee-116">影片埠釘選</span><span class="sxs-lookup"><span data-stu-id="abdee-116">Video Port Pins</span></span>](video-port-pins.md)
-   [<span data-ttu-id="abdee-117">VideoInfo2 格式類型</span><span class="sxs-lookup"><span data-stu-id="abdee-117">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
-   [<span data-ttu-id="abdee-118">建立 Kernel-Mode 篩選</span><span class="sxs-lookup"><span data-stu-id="abdee-118">Creating Kernel-Mode Filters</span></span>](creating-kernel-mode-filters.md)
-   [<span data-ttu-id="abdee-119">WDM 類別驅動程式篩選</span><span class="sxs-lookup"><span data-stu-id="abdee-119">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
-   [<span data-ttu-id="abdee-120">在 DirectShow 中使用 WDDM Capture</span><span class="sxs-lookup"><span data-stu-id="abdee-120">Using WDDM Capture in DirectShow</span></span>](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="abdee-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="abdee-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abdee-122">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="abdee-122">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 




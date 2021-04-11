---
description: 篩選圖形管理員
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: 篩選圖形管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845791"
---
# <a name="filter-graph-manager"></a><span data-ttu-id="3fe4c-103">篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="3fe4c-103">Filter Graph Manager</span></span>

<span data-ttu-id="3fe4c-104">篩選圖形管理員會建立和控制篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-104">The Filter Graph Manager builds and controls filter graphs.</span></span> <span data-ttu-id="3fe4c-105">此物件是 DirectShow 中的主要元件。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-105">This object is the central component in DirectShow.</span></span> <span data-ttu-id="3fe4c-106">應用程式會使用它來建立和控制篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-106">Applications use it to build and control filter graphs.</span></span> <span data-ttu-id="3fe4c-107">篩選圖形管理員也會處理同步處理、事件通知，以及控制篩選圖形的其他層面。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-107">The Filter Graph Manager also handles synchronization, event notification, and other aspects of the controlling the filter graph.</span></span> <span data-ttu-id="3fe4c-108">藉由呼叫 **CoCreateInstance** 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-108">Create this object by calling **CoCreateInstance**.</span></span>

### <a name="clsid"></a><span data-ttu-id="3fe4c-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="3fe4c-109">CLSID</span></span>

<span data-ttu-id="3fe4c-110">有兩個 Clsid 可用於建立篩選圖形管理員：</span><span class="sxs-lookup"><span data-stu-id="3fe4c-110">There are two CLSIDs for creating the Filter Graph Manager:</span></span>



| <span data-ttu-id="3fe4c-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="3fe4c-111">CLSID</span></span>                      | <span data-ttu-id="3fe4c-112">Description</span><span class="sxs-lookup"><span data-stu-id="3fe4c-112">Description</span></span>                                                 |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="3fe4c-113">CLSID \_ FilterGraph</span><span class="sxs-lookup"><span data-stu-id="3fe4c-113">CLSID\_FilterGraph</span></span>         | <span data-ttu-id="3fe4c-114">在共用背景工作執行緒上建立篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-114">Creates the Filter Graph Manager on a shared worker thread.</span></span> |
| <span data-ttu-id="3fe4c-115">CLSID \_ FilterGraphNoThread</span><span class="sxs-lookup"><span data-stu-id="3fe4c-115">CLSID\_FilterGraphNoThread</span></span> | <span data-ttu-id="3fe4c-116">在應用程式執行緒上建立篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-116">Creates the Filter Graph Manager on the application thread.</span></span> |



 

<span data-ttu-id="3fe4c-117">一般而言，應用程式應該使用 CLSID \_ FilterGraph。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-117">Generally, applications should use CLSID\_FilterGraph.</span></span> <span data-ttu-id="3fe4c-118">這兩個 Clsid 都會建立相同的物件，但會使用不同的執行緒模型：</span><span class="sxs-lookup"><span data-stu-id="3fe4c-118">Both CLSIDs create the same object, but they use different threading models:</span></span>

-   <span data-ttu-id="3fe4c-119">CLSID \_ FilterGraph 會在背景工作執行緒上建立篩選圖形管理員，該執行緒會由 \_ 相同進程內的所有 CLSID FilterGraph 實例共用。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-119">CLSID\_FilterGraph creates the Filter Graph Manager on a worker thread, which is shared by all CLSID\_FilterGraph instances within the same process.</span></span> <span data-ttu-id="3fe4c-120">執行緒會分派篩選所傳送的訊息，並控制篩選器所建立之任何視窗的存留期。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-120">The thread dispatches messages sent by filters, and controls the lifetime of any windows created by filters.</span></span>
-   <span data-ttu-id="3fe4c-121">CLSID \_ FilterGraphNoThread 會在應用程式的執行緒上建立篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-121">CLSID\_FilterGraphNoThread creates the Filter Graph Manager on the application's thread.</span></span> <span data-ttu-id="3fe4c-122">如果您使用此 CLSID，呼叫 **CoCreateInstance** 的執行緒必須有可分派訊息的訊息迴圈;否則，可能會發生鎖死。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-122">If you use this CLSID, the thread that calls **CoCreateInstance** must have a message loop that dispatches messages; otherwise, deadlocks can occur.</span></span> <span data-ttu-id="3fe4c-123">此外，在應用程式執行緒結束之前，它必須釋放篩選圖形管理員和所有繪圖物件 (例如篩選、釘選、參考時鐘等等) 。</span><span class="sxs-lookup"><span data-stu-id="3fe4c-123">Also, before the application thread exits, it must release the Filter Graph Manager and all graph objects (such as filters, pins, reference clocks, and so forth).</span></span>

### <a name="interfaces"></a><span data-ttu-id="3fe4c-124">介面</span><span class="sxs-lookup"><span data-stu-id="3fe4c-124">Interfaces</span></span>

<span data-ttu-id="3fe4c-125">篩選圖形管理員會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="3fe4c-125">The Filter Graph Manager exposes the following interfaces:</span></span>

-   [<span data-ttu-id="3fe4c-126">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-126">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [<span data-ttu-id="3fe4c-127">**IAMStats**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-127">**IAMStats**</span></span>](/windows/desktop/api/Control/nn-control-iamstats)
-   [<span data-ttu-id="3fe4c-128">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-128">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [<span data-ttu-id="3fe4c-129">**IBasicVideo**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-129">**IBasicVideo**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [<span data-ttu-id="3fe4c-130">**IBasicVideo2**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-130">**IBasicVideo2**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [<span data-ttu-id="3fe4c-131">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-131">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [<span data-ttu-id="3fe4c-132">**IFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-132">**IFilterGraph**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [<span data-ttu-id="3fe4c-133">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-133">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [<span data-ttu-id="3fe4c-134">**IFilterGraph3**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-134">**IFilterGraph3**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [<span data-ttu-id="3fe4c-135">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-135">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [<span data-ttu-id="3fe4c-136">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-136">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [<span data-ttu-id="3fe4c-137">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-137">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [<span data-ttu-id="3fe4c-138">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-138">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [<span data-ttu-id="3fe4c-139">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-139">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [<span data-ttu-id="3fe4c-140">**IMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-140">**IMediaEvent**</span></span>](/windows/desktop/api/Control/nn-control-imediaevent)
-   [<span data-ttu-id="3fe4c-141">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-141">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [<span data-ttu-id="3fe4c-142">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-142">**IMediaEventSink**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [<span data-ttu-id="3fe4c-143">**IMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-143">**IMediaFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [<span data-ttu-id="3fe4c-144">**IMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-144">**IMediaPosition**</span></span>](/windows/desktop/api/Control/nn-control-imediaposition)
-   [<span data-ttu-id="3fe4c-145">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-145">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [<span data-ttu-id="3fe4c-146">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-146">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [<span data-ttu-id="3fe4c-147">**IRegisterServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-147">**IRegisterServiceProvider**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [<span data-ttu-id="3fe4c-148">**IResourceManager**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-148">**IResourceManager**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   <span data-ttu-id="3fe4c-149">**IServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-149">**IServiceProvider**</span></span>
-   [<span data-ttu-id="3fe4c-150">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-150">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [<span data-ttu-id="3fe4c-151">**IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="3fe4c-151">**IVideoWindow**</span></span>](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a><span data-ttu-id="3fe4c-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fe4c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fe4c-153">DirectShow 物件</span><span class="sxs-lookup"><span data-stu-id="3fe4c-153">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 




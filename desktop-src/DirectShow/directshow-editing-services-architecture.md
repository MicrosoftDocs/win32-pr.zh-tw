---
description: DirectShow 編輯服務架構
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: DirectShow 編輯服務架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973735"
---
# <a name="directshow-editing-services-architecture"></a><span data-ttu-id="bd3ac-103">DirectShow 編輯服務架構</span><span class="sxs-lookup"><span data-stu-id="bd3ac-103">DirectShow Editing Services Architecture</span></span>

<span data-ttu-id="bd3ac-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bd3ac-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="bd3ac-105">下圖顯示 (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md) 的架構。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-105">The following illustration shows the architecture of [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

![directshow 編輯服務架構](images/architecture.png)

-   <span data-ttu-id="bd3ac-107">時間軸：將影片生產形式表示為來源剪輯、轉換和效果的集合，並組織成一組嵌套的軌跡。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-107">Timeline: Represents a video production as a collection of source clips, transitions, and effects, organized into a set of nested tracks.</span></span> <span data-ttu-id="bd3ac-108">如需詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-108">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>
-   <span data-ttu-id="bd3ac-109">XML 剖析器：剖析時間軸並產生輸出檔，或讀取輸入檔並產生時間軸。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-109">XML Parser: Parses the timeline and generates an output file, or reads an input file and generates a timeline.</span></span> <span data-ttu-id="bd3ac-110">DES 支援以 XML 為基礎的持續性格式。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-110">DES supports an XML-based persistence format.</span></span>
-   <span data-ttu-id="bd3ac-111">轉譯引擎：將時間軸轉譯成可轉譯為串流媒體的表單。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-111">Render engine: Translates the timeline into a form that can be rendered as streaming media.</span></span> <span data-ttu-id="bd3ac-112">根據預設，轉譯引擎會產生 DirectShow 篩選圖形 (請參閱下一節) 。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-112">By default, the render engine produces a DirectShow filter graph (see next section).</span></span>
-   <span data-ttu-id="bd3ac-113">媒體定位器：維持媒體元件位置的快取。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-113">Media locator: Maintains a cache of locations of media elements.</span></span> <span data-ttu-id="bd3ac-114">當嘗試開啟媒體元件失敗時，DES 會根據成功開啟的歷程記錄，使用快取來尋找元素。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-114">When an attempt to open a media element fails, DES uses the cache to locate the element, based on a history of successful opens.</span></span>

<span data-ttu-id="bd3ac-115">時間軸是影片編輯專案的摘要描述。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-115">The timeline is an abstract description of a video editing project.</span></span> <span data-ttu-id="bd3ac-116">它會指定專案中使用的來源剪輯、開始和停止時間、效果和轉換等等。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-116">It specifies the source clips used in the project, start and stop times, effects and transitions, and so forth.</span></span> <span data-ttu-id="bd3ac-117">但是，時間軸不會轉譯影片和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-117">The timeline does not render the video and audio streams, however.</span></span> <span data-ttu-id="bd3ac-118">相反地，轉譯引擎會將時間軸轉譯為預覽或檔案輸出的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-118">Instead, the render engine translates the timeline into a filter graph, for either preview or file output.</span></span> <span data-ttu-id="bd3ac-119">應用程式會操控時間軸，而不是直接操作篩選圖形，這會很麻煩且容易出錯。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-119">An application manipulates the timeline rather than directly manipulating the filter graph, which would be cumbersome and error prone.</span></span>

<span data-ttu-id="bd3ac-120">下表列出一般影片編輯應用程式執行的主要工作，以及支援每項工作的介面。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-120">The following table lists the main tasks that a typical video editing application performs, along with the interfaces that support each task.</span></span> <span data-ttu-id="bd3ac-121">稍後的章節會更詳細地說明這些工作和介面。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-121">Later sections describe these tasks and the interfaces in more detail.</span></span>



| <span data-ttu-id="bd3ac-122">Task</span><span class="sxs-lookup"><span data-stu-id="bd3ac-122">Task</span></span>                                     | <span data-ttu-id="bd3ac-123">介面 (s) </span><span class="sxs-lookup"><span data-stu-id="bd3ac-123">Interface(s)</span></span>                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd3ac-124">建立或修改時間軸。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-124">Construct or modify a timeline.</span></span>          | <span data-ttu-id="bd3ac-125">[**IAMTimeline**](iamtimeline.md) 和其他 **IAMTimelineXXXX** 介面</span><span class="sxs-lookup"><span data-stu-id="bd3ac-125">[**IAMTimeline**](iamtimeline.md) and the other **IAMTimelineXXXX** interfaces</span></span>          |
| <span data-ttu-id="bd3ac-126">儲存並載入專案檔。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-126">Save and load project files.</span></span>             | [<span data-ttu-id="bd3ac-127">**IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="bd3ac-127">**IXml2Dex**</span></span>](ixml2dex.md)                                                             |
| <span data-ttu-id="bd3ac-128">預覽專案或將其寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-128">Preview a project or write it to a file.</span></span> | <span data-ttu-id="bd3ac-129">[**IRenderEngine**](irenderengine.md)、 [ **ISmartRenderEngine**](ismartrenderengine.md)</span><span class="sxs-lookup"><span data-stu-id="bd3ac-129">[**IRenderEngine**](irenderengine.md), [**ISmartRenderEngine**](ismartrenderengine.md)</span></span> |



 

<span data-ttu-id="bd3ac-130">此外，應用程式可能會執行下列部分或所有的次要工作。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-130">In addition, an application might perform some or all of the following secondary tasks.</span></span>



| <span data-ttu-id="bd3ac-131">Task</span><span class="sxs-lookup"><span data-stu-id="bd3ac-131">Task</span></span>                                                                                           | <span data-ttu-id="bd3ac-132">介面 (s) </span><span class="sxs-lookup"><span data-stu-id="bd3ac-132">Interface(s)</span></span>                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bd3ac-133">取得媒體檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-133">Obtain information about media files.</span></span> <span data-ttu-id="bd3ac-134"> (的資料流程數目;每個資料流程的格式和持續時間。 ) </span><span class="sxs-lookup"><span data-stu-id="bd3ac-134">(Number of streams; format and duration of each stream.)</span></span> | [<span data-ttu-id="bd3ac-135">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="bd3ac-135">**IMediaDet**</span></span>](imediadet.md)                                               |
| <span data-ttu-id="bd3ac-136">設定轉換和效果的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-136">Set properties on transitions and effects.</span></span>                                                     | [<span data-ttu-id="bd3ac-137">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="bd3ac-137">**IPropertySetter**</span></span>](ipropertysetter.md)                                   |
| <span data-ttu-id="bd3ac-138">在轉譯期間發生錯誤時收到通知。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-138">Receive notification when errors occur during rendering.</span></span>                                       | <span data-ttu-id="bd3ac-139">[**IAMSetErrorLog**](iamseterrorlog.md)、 [ **IAMErrorLog**](iamerrorlog.md)</span><span class="sxs-lookup"><span data-stu-id="bd3ac-139">[**IAMSetErrorLog**](iamseterrorlog.md), [**IAMErrorLog**](iamerrorlog.md)</span></span> |
| <span data-ttu-id="bd3ac-140">取出海報畫面。</span><span class="sxs-lookup"><span data-stu-id="bd3ac-140">Retrieve poster frames.</span></span>                                                                        | <span data-ttu-id="bd3ac-141">[**IMediaDet**](imediadet.md)、 [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="bd3ac-141">[**IMediaDet**](imediadet.md), [**ISampleGrabber**](isamplegrabber.md)</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="bd3ac-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd3ac-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd3ac-143">使用 DirectShow 編輯服務開始使用</span><span class="sxs-lookup"><span data-stu-id="bd3ac-143">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 




---
description: Tablet PC 包含的技術，可在收集的 tablet 畫筆資料時進行互動。
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: 存取和操作手寫筆輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973188"
---
# <a name="accessing-and-manipulating-stylus-input"></a><span data-ttu-id="c5d7b-103">存取和操作手寫筆輸入</span><span class="sxs-lookup"><span data-stu-id="c5d7b-103">Accessing and Manipulating Stylus Input</span></span>

<span data-ttu-id="c5d7b-104">Tablet PC 包含的技術，可在收集的 tablet 畫筆資料時進行互動。</span><span class="sxs-lookup"><span data-stu-id="c5d7b-104">The Tablet PC includes technology for interacting with tablet pen data as it is being gathered.</span></span> <span data-ttu-id="c5d7b-105">[**RealTimeStylus**](realtimestylus-class.md)類別是 StylusInput 應用程式開發介面 (API) 的一部分，可提供 tablet 畫筆資料串流的存取權。</span><span class="sxs-lookup"><span data-stu-id="c5d7b-105">The [**RealTimeStylus**](realtimestylus-class.md) class is part of the StylusInput application programming interfaces (API), which provide access to the tablet pen data stream.</span></span> <span data-ttu-id="c5d7b-106">這些 Api 可讓您獨立地捕捉、中斷和修改資料流程，而不需要轉譯和收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="c5d7b-106">These APIs allow you to capture, interrupt, and modify the stream independently from rendering and collecting ink.</span></span>

<span data-ttu-id="c5d7b-107">StylusInput Api 的設計目的是：</span><span class="sxs-lookup"><span data-stu-id="c5d7b-107">The StylusInput APIs are designed to:</span></span>

-   <span data-ttu-id="c5d7b-108">提供 tablet 畫筆資料串流的即時存取。</span><span class="sxs-lookup"><span data-stu-id="c5d7b-108">Provide real-time access to the tablet pen data stream.</span></span>
-   <span data-ttu-id="c5d7b-109">透過將 UI 執行緒上的封包資料排入佇列，並將筆墨集合設為單一執行緒，讓使用者介面 (UI) 執行緒封鎖動態筆墨轉譯。</span><span class="sxs-lookup"><span data-stu-id="c5d7b-109">Keep the user interface (UI) thread from blocking dynamic ink rendering by queuing the packet data on the UI thread and making ink collection single threaded.</span></span>
-   <span data-ttu-id="c5d7b-110">使用 [**InkCollector**](inkcollector-class.md) 物件、 [**InkOverlay**](inkoverlay-class.md) 物件、 [InkPicture](inkpicture-control-reference.md) 控制項或 [InkEdit](inkedit-control-reference.md) 控制項來收集筆跡，以提高效能並降低整體執行緒的使用。</span><span class="sxs-lookup"><span data-stu-id="c5d7b-110">Increase the performance and lower the overall thread usage over using the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control to collect ink.</span></span>

<span data-ttu-id="c5d7b-111">StylusInput Api 不是設計來與 [**InkCollector**](inkcollector-class.md) 物件、 [**InkOverlay**](inkoverlay-class.md) 物件、 [InkPicture](inkpicture-control-reference.md) 控制項或 [InkEdit](inkedit-control-reference.md) 控制項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c5d7b-111">The StylusInput APIs are not designed to work with the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control.</span></span>

<span data-ttu-id="c5d7b-112">當您需要直接與 tablet 畫筆資料流程互動，或當應用程式可能封鎖即時筆跡時，請使用 [**RealTimeStylus**](realtimestylus-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c5d7b-112">When you need to interact directly with the tablet pen data stream or when your application may block real-time inking, use the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="c5d7b-113">當這些物件的預設行為提供您所需的行為時，請使用 [**InkCollector**](inkcollector-class.md) 物件、 [**InkOverlay**](inkoverlay-class.md) 物件、 [InkPicture](inkpicture-control-reference.md) 控制項或 [InkEdit](inkedit-control-reference.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="c5d7b-113">Use the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5d7b-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="c5d7b-114">In This Section</span></span>

<span data-ttu-id="c5d7b-115">下列各節說明 StylusInput Api 的元素：</span><span class="sxs-lookup"><span data-stu-id="c5d7b-115">The following sections describe elements of the StylusInput APIs:</span></span>

-   [<span data-ttu-id="c5d7b-116">StylusInput Api 的架構</span><span class="sxs-lookup"><span data-stu-id="c5d7b-116">Architecture of the StylusInput APIs</span></span>](architecture-of-the-stylusinput-apis.md)
-   [<span data-ttu-id="c5d7b-117">使用 StylusInput Api</span><span class="sxs-lookup"><span data-stu-id="c5d7b-117">Working with the StylusInput APIs</span></span>](working-with-the-stylusinput-apis.md)
    -   [<span data-ttu-id="c5d7b-118">使用 RealTimeStylus 類別</span><span class="sxs-lookup"><span data-stu-id="c5d7b-118">Working with the RealTimeStylus Class</span></span>](working-with-the-realtimestylus-class.md)
    -   [<span data-ttu-id="c5d7b-119">外掛程式和 RealTimeStylus 類別</span><span class="sxs-lookup"><span data-stu-id="c5d7b-119">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="c5d7b-120">外掛程式資料和 RealTimeStylus 類別</span><span class="sxs-lookup"><span data-stu-id="c5d7b-120">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="c5d7b-121">StylusInput Api 的執行注意事項</span><span class="sxs-lookup"><span data-stu-id="c5d7b-121">Implementation Notes for the StylusInput APIs</span></span>](implementation-notes-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="c5d7b-122">筆墨-集合外掛程式</span><span class="sxs-lookup"><span data-stu-id="c5d7b-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
    -   [<span data-ttu-id="c5d7b-123">動態轉譯器外掛程式</span><span class="sxs-lookup"><span data-stu-id="c5d7b-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
    -   [<span data-ttu-id="c5d7b-124">辨識器外掛程式</span><span class="sxs-lookup"><span data-stu-id="c5d7b-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)
-   [<span data-ttu-id="c5d7b-125">使用 StylusInput Api 時的考慮</span><span class="sxs-lookup"><span data-stu-id="c5d7b-125">Considerations when Using the StylusInput APIs</span></span>](considerations-when-using-the-stylusinput-apis.md)
    -   [<span data-ttu-id="c5d7b-126">StylusInput Api 的設計考慮</span><span class="sxs-lookup"><span data-stu-id="c5d7b-126">Design Considerations for the StylusInput APIs</span></span>](design-considerations-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="c5d7b-127">StylusInput Api 的執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="c5d7b-127">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)

[<span data-ttu-id="c5d7b-128">串聯的 RealTimeStylus 模型</span><span class="sxs-lookup"><span data-stu-id="c5d7b-128">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)

-   [<span data-ttu-id="c5d7b-129">StylusInput Api 的錯誤處理考慮</span><span class="sxs-lookup"><span data-stu-id="c5d7b-129">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="c5d7b-130">StylusInput Api 的效能考慮</span><span class="sxs-lookup"><span data-stu-id="c5d7b-130">Performance Considerations for the StylusInput APIs</span></span>](performance-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="c5d7b-131">StylusInput Api 的部分信任考慮</span><span class="sxs-lookup"><span data-stu-id="c5d7b-131">Partial Trust Considerations for the StylusInput APIs</span></span>](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a><span data-ttu-id="c5d7b-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5d7b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5d7b-133">RealTimeStylus 外掛程式範例</span><span class="sxs-lookup"><span data-stu-id="c5d7b-133">RealTimeStylus Plug-in Sample</span></span>](realtimestylus-plug-in-sample.md)
</dt> <dt>

[<span data-ttu-id="c5d7b-134">RealTimeStylus 筆墨集合範例</span><span class="sxs-lookup"><span data-stu-id="c5d7b-134">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 




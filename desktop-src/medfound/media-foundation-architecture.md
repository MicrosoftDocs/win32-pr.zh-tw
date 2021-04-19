---
description: 本章節描述 Microsoft 媒體基礎的一般設計。 如需使用媒體基礎進行特定程式設計工作的詳細資訊，請參閱媒體基礎程式設計指南。
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: 媒體基礎架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106997318"
---
# <a name="media-foundation-architecture"></a><span data-ttu-id="7bd80-104">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="7bd80-104">Media Foundation Architecture</span></span>

<span data-ttu-id="7bd80-105">本章節描述 Microsoft 媒體基礎的一般設計。</span><span class="sxs-lookup"><span data-stu-id="7bd80-105">This section describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="7bd80-106">如需使用媒體基礎進行特定程式設計工作的詳細資訊，請參閱 [媒體基礎程式設計指南](media-foundation-programming-guide.md)。</span><span class="sxs-lookup"><span data-stu-id="7bd80-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7bd80-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="7bd80-107">In this section</span></span>



| <span data-ttu-id="7bd80-108">主題</span><span class="sxs-lookup"><span data-stu-id="7bd80-108">Topic</span></span>                                                                                                         | <span data-ttu-id="7bd80-109">描述</span><span class="sxs-lookup"><span data-stu-id="7bd80-109">Description</span></span>                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bd80-110">媒體基礎架構的總覽</span><span class="sxs-lookup"><span data-stu-id="7bd80-110">Overview of the Media Foundation Architecture</span></span>](overview-of-the-media-foundation-architecture.md)<br/> | <span data-ttu-id="7bd80-111">提供媒體基礎架構的高層級總覽。</span><span class="sxs-lookup"><span data-stu-id="7bd80-111">Gives a high-level overview of the Media Foundation architecture.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="7bd80-112">媒體基礎基本</span><span class="sxs-lookup"><span data-stu-id="7bd80-112">Media Foundation Primitives</span></span>](media-foundation-primitives.md)<br/>                                     | <span data-ttu-id="7bd80-113">描述在媒體基礎中使用的一些基本介面。</span><span class="sxs-lookup"><span data-stu-id="7bd80-113">Describes some basic interfaces that are used throughout Media Foundation.</span></span><br/> <span data-ttu-id="7bd80-114">幾乎所有的媒體基礎應用程式都會使用這些介面。</span><span class="sxs-lookup"><span data-stu-id="7bd80-114">Almost all Media Foundation applications will use these interfaces.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="7bd80-115">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="7bd80-115">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)<br/>                               | <span data-ttu-id="7bd80-116">描述核心媒體基礎函式，例如非同步回呼和工作佇列。</span><span class="sxs-lookup"><span data-stu-id="7bd80-116">Describes core Media Foundation functions, such as asynchronous callbacks and work queues.</span></span><br/> <span data-ttu-id="7bd80-117">某些應用程式可能會使用平台層級的介面。</span><span class="sxs-lookup"><span data-stu-id="7bd80-117">Some applications might use platform-level interfaces.</span></span> <span data-ttu-id="7bd80-118">此外，自訂外掛程式（例如媒體來源和 MFTs）會使用這些介面。</span><span class="sxs-lookup"><span data-stu-id="7bd80-118">Also, custom plug-ins, such as media sources and MFTs, use these interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="7bd80-119">媒體基礎管線</span><span class="sxs-lookup"><span data-stu-id="7bd80-119">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)<br/>                                         | <span data-ttu-id="7bd80-120">媒體基礎管線層是由媒體來源、MFTs 和媒體接收器所組成。</span><span class="sxs-lookup"><span data-stu-id="7bd80-120">The Media Foundation pipeline layer consists of media sources, MFTs, and media sinks.</span></span> <span data-ttu-id="7bd80-121">大部分的應用程式不會直接在管線層呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="7bd80-121">Most applications do not call methods directly on the pipeline layer.</span></span> <span data-ttu-id="7bd80-122">相反地，應用程式會使用其中一個較高的層級，例如媒體會話或來源讀取器和接收寫入器。</span><span class="sxs-lookup"><span data-stu-id="7bd80-122">Instead, applications use one of the higher layers, such as the Media Session or the Source Reader and Sink Writer.</span></span><br/> |
| [<span data-ttu-id="7bd80-123">媒體會話</span><span class="sxs-lookup"><span data-stu-id="7bd80-123">Media Session</span></span>](media-session.md)<br/>                                                                 | <span data-ttu-id="7bd80-124">媒體會話會管理媒體基礎管線中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7bd80-124">The Media Session manages data flow in the Media Foundation pipeline.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="7bd80-125">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="7bd80-125">Source Reader</span></span>](source-reader.md)<br/>                                                                 | <span data-ttu-id="7bd80-126">來源讀取器可讓應用程式從媒體來源取得資料，而不需要直接呼叫媒體來源 Api 的 applicating。</span><span class="sxs-lookup"><span data-stu-id="7bd80-126">The Source Reader enables an application to get data from a media source, without the applicating needing to call the media source APIs directly.</span></span> <span data-ttu-id="7bd80-127">來源讀取器也可以執行壓縮資料流程的解碼。</span><span class="sxs-lookup"><span data-stu-id="7bd80-127">The Source Reader can also perform decoding of compressed streams.</span></span><br/>                                                            |
| [<span data-ttu-id="7bd80-128">受保護的媒體路徑</span><span class="sxs-lookup"><span data-stu-id="7bd80-128">Protected Media Path</span></span>](protected-media-path.md)<br/>                                                   | <span data-ttu-id="7bd80-129">受保護的媒體路徑 (PMP) 提供受保護的環境來播放 premium 影片內容。</span><span class="sxs-lookup"><span data-stu-id="7bd80-129">The protected media path (PMP) provides a protected environment for playing premium video content.</span></span> <span data-ttu-id="7bd80-130">撰寫媒體基礎的應用程式時，不需要使用 PMP。</span><span class="sxs-lookup"><span data-stu-id="7bd80-130">It is not necessary to use the PMP when writing a Media Foundation application.</span></span> <br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="7bd80-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="7bd80-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bd80-132">關於媒體基礎</span><span class="sxs-lookup"><span data-stu-id="7bd80-132">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="7bd80-133">媒體基礎：基本概念</span><span class="sxs-lookup"><span data-stu-id="7bd80-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="7bd80-134">媒體基礎和 COM</span><span class="sxs-lookup"><span data-stu-id="7bd80-134">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="7bd80-135">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="7bd80-135">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 





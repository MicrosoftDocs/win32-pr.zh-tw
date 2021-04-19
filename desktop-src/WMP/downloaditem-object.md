---
title: DownloadItem 物件
description: DownloadItem 物件
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player 線上商店，DownloadItem 物件
- 線上商店、DownloadItem 物件
- 類型2線上商店，DownloadItem 物件
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967225"
---
# <a name="downloaditem-object"></a><span data-ttu-id="94a71-107">DownloadItem 物件</span><span class="sxs-lookup"><span data-stu-id="94a71-107">DownloadItem Object</span></span>

> [!Note]  
> <span data-ttu-id="94a71-108">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="94a71-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="94a71-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="94a71-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="94a71-110">**DownloadItem** 物件代表檔案下載要求。</span><span class="sxs-lookup"><span data-stu-id="94a71-110">The **DownloadItem** object represents a file download request.</span></span> <span data-ttu-id="94a71-111">它可供在完整模式中裝載的網頁使用 Windows Media Player 而且可以存取 **外部** 物件，例如 premium services。</span><span class="sxs-lookup"><span data-stu-id="94a71-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as premium services.</span></span>

<span data-ttu-id="94a71-112">**DownloadItem** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="94a71-112">The **DownloadItem** object supports the following properties.</span></span>



| <span data-ttu-id="94a71-113">屬性</span><span class="sxs-lookup"><span data-stu-id="94a71-113">Property</span></span>                                        | <span data-ttu-id="94a71-114">描述</span><span class="sxs-lookup"><span data-stu-id="94a71-114">Description</span></span>                                      |
|-------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="94a71-115">downloadState</span><span class="sxs-lookup"><span data-stu-id="94a71-115">downloadState</span></span>](downloaditem-downloadstate.md) | <span data-ttu-id="94a71-116">捕獲下載的狀態。</span><span class="sxs-lookup"><span data-stu-id="94a71-116">Retrieves the state of the download.</span></span>             |
| [<span data-ttu-id="94a71-117">進展</span><span class="sxs-lookup"><span data-stu-id="94a71-117">progress</span></span>](downloaditem-progress.md)           | <span data-ttu-id="94a71-118">抓取下載的進度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="94a71-118">Retrieves the progress of the download in bytes.</span></span> |
| [<span data-ttu-id="94a71-119">size</span><span class="sxs-lookup"><span data-stu-id="94a71-119">size</span></span>](downloaditem-size.md)                   | <span data-ttu-id="94a71-120">抓取下載的大小。</span><span class="sxs-lookup"><span data-stu-id="94a71-120">Retrieves the size of the download.</span></span>              |
| [<span data-ttu-id="94a71-121">sourceURL</span><span class="sxs-lookup"><span data-stu-id="94a71-121">sourceURL</span></span>](downloaditem-sourceurl.md)         | <span data-ttu-id="94a71-122">抓取下載的來源 URL。</span><span class="sxs-lookup"><span data-stu-id="94a71-122">Retrieves the source URL of the download.</span></span>        |
| [<span data-ttu-id="94a71-123">type</span><span class="sxs-lookup"><span data-stu-id="94a71-123">type</span></span>](downloaditem-type.md)                   | <span data-ttu-id="94a71-124">抓取下載的類型。</span><span class="sxs-lookup"><span data-stu-id="94a71-124">Retrieves the type of the download.</span></span>              |



 

<span data-ttu-id="94a71-125">**DownloadItem** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="94a71-125">The **DownloadItem** object supports the following methods.</span></span>



| <span data-ttu-id="94a71-126">方法</span><span class="sxs-lookup"><span data-stu-id="94a71-126">Method</span></span>                                      | <span data-ttu-id="94a71-127">描述</span><span class="sxs-lookup"><span data-stu-id="94a71-127">Description</span></span>                                                |
|---------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="94a71-128">cancel</span><span class="sxs-lookup"><span data-stu-id="94a71-128">cancel</span></span>](downloaditem-cancel.md)           | <span data-ttu-id="94a71-129">取消下載。</span><span class="sxs-lookup"><span data-stu-id="94a71-129">Cancels the download.</span></span>                                      |
| [<span data-ttu-id="94a71-130">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="94a71-130">getItemInfo</span></span>](downloaditem-getiteminfo.md) | <span data-ttu-id="94a71-131">抓取下載專案的屬性值。</span><span class="sxs-lookup"><span data-stu-id="94a71-131">Retrieves the value of an attribute for the download item.</span></span> |
| [<span data-ttu-id="94a71-132">pause</span><span class="sxs-lookup"><span data-stu-id="94a71-132">pause</span></span>](downloaditem-pause.md)             | <span data-ttu-id="94a71-133">暫停下載。</span><span class="sxs-lookup"><span data-stu-id="94a71-133">Pauses the download.</span></span>                                       |
| [<span data-ttu-id="94a71-134">恢復</span><span class="sxs-lookup"><span data-stu-id="94a71-134">resume</span></span>](downloaditem-resume.md)           | <span data-ttu-id="94a71-135">繼續進行下載。</span><span class="sxs-lookup"><span data-stu-id="94a71-135">Resumes the download.</span></span>                                      |



 

<span data-ttu-id="94a71-136">**DownloadItem** 物件是透過下列屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="94a71-136">The **DownloadItem** object is accessed through the following property.</span></span>



| <span data-ttu-id="94a71-137">Object</span><span class="sxs-lookup"><span data-stu-id="94a71-137">Object</span></span>                                              | <span data-ttu-id="94a71-138">屬性</span><span class="sxs-lookup"><span data-stu-id="94a71-138">Property</span></span>                            |
|-----------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="94a71-139">DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="94a71-139">DownloadCollection</span></span>](downloadcollection-object.md) | [<span data-ttu-id="94a71-140">item</span><span class="sxs-lookup"><span data-stu-id="94a71-140">item</span></span>](downloadcollection-item.md) |



 

<span data-ttu-id="94a71-141">為了方便說明，請 **DownloadManager**。**getDownloadCollection** (*collectionId*) 。在參考語法區段中，會使用 (*itemId*) 的 **專案**。</span><span class="sxs-lookup"><span data-stu-id="94a71-141">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*).**item**(*itemId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94a71-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="94a71-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94a71-143">**類型 2 線上商店的參考**</span><span class="sxs-lookup"><span data-stu-id="94a71-143">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





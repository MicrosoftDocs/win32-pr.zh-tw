---
title: DownloadCollection 物件
description: DownloadCollection 物件
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player 線上商店，DownloadCollection 物件
- 線上商店、DownloadCollection 物件
- 類型2線上商店，DownloadCollection 物件
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964979"
---
# <a name="downloadcollection-object"></a><span data-ttu-id="72022-107">DownloadCollection 物件</span><span class="sxs-lookup"><span data-stu-id="72022-107">DownloadCollection Object</span></span>

> [!Note]  
> <span data-ttu-id="72022-108">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="72022-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="72022-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="72022-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="72022-110">**DownloadCollection** 物件包含用來處理下載專案集合的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="72022-110">The **DownloadCollection** object contains properties and methods to handle collections of download items.</span></span> <span data-ttu-id="72022-111">它可供在完整模式中裝載的網頁使用 Windows Media Player 而且可以存取 **外部** 物件，例如線上存放區。</span><span class="sxs-lookup"><span data-stu-id="72022-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as online stores.</span></span>

<span data-ttu-id="72022-112">**DownloadCollection** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="72022-112">The **DownloadCollection** object supports the following properties.</span></span>



| <span data-ttu-id="72022-113">屬性</span><span class="sxs-lookup"><span data-stu-id="72022-113">Property</span></span>                              | <span data-ttu-id="72022-114">描述</span><span class="sxs-lookup"><span data-stu-id="72022-114">Description</span></span>                                  |
|---------------------------------------|----------------------------------------------|
| [<span data-ttu-id="72022-115">計數</span><span class="sxs-lookup"><span data-stu-id="72022-115">count</span></span>](downloadcollection-count.md) | <span data-ttu-id="72022-116">抓取暫止的下載數目。</span><span class="sxs-lookup"><span data-stu-id="72022-116">Retrieves the number of pending downloads.</span></span>   |
| [<span data-ttu-id="72022-117">id</span><span class="sxs-lookup"><span data-stu-id="72022-117">id</span></span>](downloadcollection-id.md)       | <span data-ttu-id="72022-118">抓取下載集合的識別碼。</span><span class="sxs-lookup"><span data-stu-id="72022-118">Retrieves the ID of the download collection.</span></span> |



 

<span data-ttu-id="72022-119">**DownloadCollection** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="72022-119">The **DownloadCollection** object supports the following methods.</span></span>



| <span data-ttu-id="72022-120">方法</span><span class="sxs-lookup"><span data-stu-id="72022-120">Method</span></span>                                                | <span data-ttu-id="72022-121">描述</span><span class="sxs-lookup"><span data-stu-id="72022-121">Description</span></span>                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="72022-122">清除</span><span class="sxs-lookup"><span data-stu-id="72022-122">Clear</span></span>](downloadcollection-clear.md)                 | <span data-ttu-id="72022-123">從下載集合中移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="72022-123">Removes all items from a download collection.</span></span> |
| [<span data-ttu-id="72022-124">item</span><span class="sxs-lookup"><span data-stu-id="72022-124">item</span></span>](downloadcollection-item.md)                   | <span data-ttu-id="72022-125">抓取暫止的下載物件。</span><span class="sxs-lookup"><span data-stu-id="72022-125">Retrieves a pending download object.</span></span>          |
| [<span data-ttu-id="72022-126">removeItem</span><span class="sxs-lookup"><span data-stu-id="72022-126">removeItem</span></span>](downloadcollection-removeitem.md)       | <span data-ttu-id="72022-127">從集合中移除下載專案。</span><span class="sxs-lookup"><span data-stu-id="72022-127">Removes a download item from a collection.</span></span>    |
| [<span data-ttu-id="72022-128">startDownload</span><span class="sxs-lookup"><span data-stu-id="72022-128">startDownload</span></span>](downloadcollection-startdownload.md) | <span data-ttu-id="72022-129">將下載排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="72022-129">Queues a download.</span></span>                            |



 

<span data-ttu-id="72022-130">**DownloadCollection** 物件是透過下列方法來存取。</span><span class="sxs-lookup"><span data-stu-id="72022-130">The **DownloadCollection** object is accessed through the following methods.</span></span>



| <span data-ttu-id="72022-131">Object</span><span class="sxs-lookup"><span data-stu-id="72022-131">Object</span></span>                                        | <span data-ttu-id="72022-132">方法</span><span class="sxs-lookup"><span data-stu-id="72022-132">Method</span></span>                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="72022-133">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="72022-133">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="72022-134">createDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="72022-134">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) |
| [<span data-ttu-id="72022-135">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="72022-135">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="72022-136">getDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="72022-136">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       |



 

<span data-ttu-id="72022-137">為了方便說明，請 **DownloadManager**。參考語法區段中使用了 **getDownloadCollection** (*collectionId*) 。</span><span class="sxs-lookup"><span data-stu-id="72022-137">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72022-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="72022-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72022-139">**類型 2 線上商店的參考**</span><span class="sxs-lookup"><span data-stu-id="72022-139">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





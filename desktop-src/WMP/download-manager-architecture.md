---
title: 下載管理員架構
description: 下載管理員架構
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
- 下載管理員的架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671907"
---
# <a name="download-manager-architecture"></a><span data-ttu-id="0b1e8-110">下載管理員架構</span><span class="sxs-lookup"><span data-stu-id="0b1e8-110">Download Manager Architecture</span></span>

<span data-ttu-id="0b1e8-111">Windows Media Player 下載管理員使用 COM 技術。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-111">The Windows Media Player Download Manager uses COM technology.</span></span> <span data-ttu-id="0b1e8-112">這項功能是以一組程式設計介面來進行。您可以使用 Microsoft JScript 或 c + + 撰寫使用這些介面的程式設計程式碼。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-112">The functionality is distilled into a set of programming interfaces; you can write programming code that uses these interfaces by using Microsoft JScript or C++.</span></span>

<span data-ttu-id="0b1e8-113">指令碼語言會使用物件的概念來分割程式設計功能。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-113">The scripting languages use the concept of objects to divide programming functionality.</span></span> <span data-ttu-id="0b1e8-114">**DownloadManager** 物件模型會使用數個物件，將方法和屬性分割為邏輯組織，以將語義相關函數群組在一起。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-114">The **DownloadManager** object model uses several objects to divide the methods and properties into a logical organization that groups semantically related functions together.</span></span> <span data-ttu-id="0b1e8-115">下列各節包含下載管理員物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-115">The following sections contain information about the Download Manager objects.</span></span>



| <span data-ttu-id="0b1e8-116">區段</span><span class="sxs-lookup"><span data-stu-id="0b1e8-116">Section</span></span>                                                                     | <span data-ttu-id="0b1e8-117">描述</span><span class="sxs-lookup"><span data-stu-id="0b1e8-117">Description</span></span>                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b1e8-118">關於 DownloadManager 物件</span><span class="sxs-lookup"><span data-stu-id="0b1e8-118">About the DownloadManager Object</span></span>](#about-the-downloadmanager-object)       | <span data-ttu-id="0b1e8-119">**DownloadManager** 物件代表 Windows Media Player 下載管理員的根物件。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-119">The **DownloadManager** object represents the root object for the Windows Media Player Download Manager.</span></span> |
| [<span data-ttu-id="0b1e8-120">關於 DownloadCollection 物件</span><span class="sxs-lookup"><span data-stu-id="0b1e8-120">About the DownloadCollection Object</span></span>](#about-the-downloadcollection-object) | <span data-ttu-id="0b1e8-121">**DownloadCollection** 物件代表下載專案的集合。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-121">The **DownloadCollection** object represents a collection of download items.</span></span>                             |
| [<span data-ttu-id="0b1e8-122">關於 DownloadItem 物件</span><span class="sxs-lookup"><span data-stu-id="0b1e8-122">About the DownloadItem Object</span></span>](#about-the-downloaditem-object)             | <span data-ttu-id="0b1e8-123">**DownloadItem** 物件代表個別的下載要求。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-123">The **DownloadItem** object represents an individual download request.</span></span>                                   |



 

## <a name="about-the-downloadmanager-object"></a><span data-ttu-id="0b1e8-124">關於 DownloadManager 物件</span><span class="sxs-lookup"><span data-stu-id="0b1e8-124">About the DownloadManager Object</span></span>

<span data-ttu-id="0b1e8-125">**DownloadManager** 是 Windows Media Player 下載管理員的根物件。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-125">**DownloadManager** is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="0b1e8-126">所有其他物件都可透過此物件存取。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-126">All other objects are accessed through this object.</span></span> <span data-ttu-id="0b1e8-127">若要取得 **DownloadManager** 物件的存取權，請使用下列 JScript 語法：</span><span class="sxs-lookup"><span data-stu-id="0b1e8-127">To gain access to the **DownloadManager** object, use the following JScript syntax:</span></span>


```C++
var DownloadManager = external.DownloadManager;
```



<span data-ttu-id="0b1e8-128">這會建立 **DownloadManager** 物件的實例，然後用它來取出子物件。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-128">This creates an instance of the **DownloadManager** object, which can then be used to retrieve the child objects.</span></span> <span data-ttu-id="0b1e8-129">例如，下列語法會從下載集合中取出識別碼為253675的第一個專案：</span><span class="sxs-lookup"><span data-stu-id="0b1e8-129">For example, the following syntax retrieves the first item from the download collection that has id number 253675:</span></span>


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a><span data-ttu-id="0b1e8-130">關於 DownloadCollection 物件</span><span class="sxs-lookup"><span data-stu-id="0b1e8-130">About the DownloadCollection Object</span></span>

<span data-ttu-id="0b1e8-131">**DownloadCollection** 物件代表要下載的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-131">The **DownloadCollection** object represents a collection of files to be downloaded.</span></span> <span data-ttu-id="0b1e8-132">您可以使用此物件來判斷集合中有多少下載、從集合中移除專案、取出特定的下載專案，以及開始新的下載。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-132">You can use this object to determine how many downloads are in the collection, remove items from the collection, retrieve a specific download item, and to start a new download.</span></span> <span data-ttu-id="0b1e8-133">開始新的下載會自動將下載新增至集合。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-133">Starting a new download automatically adds the download to the collection.</span></span>

## <a name="about-the-downloaditem-object"></a><span data-ttu-id="0b1e8-134">關於 DownloadItem 物件</span><span class="sxs-lookup"><span data-stu-id="0b1e8-134">About the DownloadItem Object</span></span>

<span data-ttu-id="0b1e8-135">**DownloadItem** 物件代表個別下載。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-135">The **DownloadItem** object represents an individual download.</span></span> <span data-ttu-id="0b1e8-136">下載專案一律會存在作為下載集合的一部分。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-136">Download items always exist as part of a download collection.</span></span> <span data-ttu-id="0b1e8-137">您可以使用此物件來取出下載專案的相關資訊，以及暫停、繼續或取消下載進行中的工作。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-137">Use this object to retrieve information about the download item and to pause, resume, or cancel the download in progress.</span></span>

<span data-ttu-id="0b1e8-138">當您取消下載時，下載專案就會保留在其下載集合中。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-138">When you cancel a download, the download item remains in place in its download collection.</span></span> <span data-ttu-id="0b1e8-139">在此情況下， **downloadCollection**。**downloadState** 會捕獲值4，表示已取消。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-139">In this case, **downloadCollection**.**downloadState** retrieves a value of 4, meaning canceled.</span></span>

<span data-ttu-id="0b1e8-140">您可以使用 **downloadItem**。通知使用者已傳送多少檔案，或仍有多少時間可供下載的 **進度** 。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-140">You can use **downloadItem**.**progress** to inform the user about how much of the file has been transferred or how much remains to be downloaded.</span></span> <span data-ttu-id="0b1e8-141">您可以使用這個值來估計剩餘的時間。</span><span class="sxs-lookup"><span data-stu-id="0b1e8-141">You might use this value to estimate the time remaining as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b1e8-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b1e8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b1e8-143">**下載管理員**</span><span class="sxs-lookup"><span data-stu-id="0b1e8-143">**Download Manager**</span></span>](download-manager.md)
</dt> </dl>

 

 





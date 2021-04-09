---
title: DownloadManager 物件
description: DownloadManager 物件
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player 線上商店，DownloadManager 物件
- 線上商店、DownloadManager 物件
- 類型2線上商店，DownloadManager 物件
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840231"
---
# <a name="downloadmanager-object"></a><span data-ttu-id="2354e-107">DownloadManager 物件</span><span class="sxs-lookup"><span data-stu-id="2354e-107">DownloadManager Object</span></span>

> [!Note]  
> <span data-ttu-id="2354e-108">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="2354e-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2354e-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="2354e-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2354e-110">**DownloadManager** 物件是 Windows Media Player 下載管理員的根物件。</span><span class="sxs-lookup"><span data-stu-id="2354e-110">The **DownloadManager** object is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="2354e-111">它可供裝載于線上商店服務工作窗格的網頁使用。</span><span class="sxs-lookup"><span data-stu-id="2354e-111">It can be used by webpages that are hosted in online store service task panes.</span></span>

<span data-ttu-id="2354e-112">**DownloadManager** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="2354e-112">The **DownloadManager** object supports the following methods.</span></span>



| <span data-ttu-id="2354e-113">方法</span><span class="sxs-lookup"><span data-stu-id="2354e-113">Method</span></span>                                                                   | <span data-ttu-id="2354e-114">描述</span><span class="sxs-lookup"><span data-stu-id="2354e-114">Description</span></span>                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="2354e-115">createDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="2354e-115">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) | <span data-ttu-id="2354e-116">建立空的下載集合。</span><span class="sxs-lookup"><span data-stu-id="2354e-116">Creates an empty download collection.</span></span>        |
| [<span data-ttu-id="2354e-117">getDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="2354e-117">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       | <span data-ttu-id="2354e-118">抓取指定的下載集合。</span><span class="sxs-lookup"><span data-stu-id="2354e-118">Retrieves the specified download collection.</span></span> |



 

<span data-ttu-id="2354e-119">**DownloadManager** 物件是使用 external 來存取的 **。DownloadManager**。</span><span class="sxs-lookup"><span data-stu-id="2354e-119">The **DownloadManager** object is accessed by using **external.DownloadManager**.</span></span> <span data-ttu-id="2354e-120">為了方便說明，我們假設這個值已指派給名為 "DownloadManager" 的變數，此變數將用來識別參考語法區段中的這個物件。</span><span class="sxs-lookup"><span data-stu-id="2354e-120">For illustration purposes, it is assumed that this value has been assigned to a variable named "DownloadManager", which will be used to identify this object in the reference syntax sections.</span></span>

<span data-ttu-id="2354e-121">在 Windows Media Player 10 或更新版本中， **DownloadManager** 屬性和物件只能從 [線上商店服務] 工作窗格存取。</span><span class="sxs-lookup"><span data-stu-id="2354e-121">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="2354e-122">您無法使用 **外部** 物件可用之其他功能的 **DownloadManager** ，例如 HTMLView、資訊中心視圖和專輯資訊。</span><span class="sxs-lookup"><span data-stu-id="2354e-122">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2354e-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="2354e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2354e-124">**類型 2 線上商店的參考**</span><span class="sxs-lookup"><span data-stu-id="2354e-124">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





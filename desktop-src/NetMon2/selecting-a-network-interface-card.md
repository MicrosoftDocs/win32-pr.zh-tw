---
description: 網路監視器提供三個功能來選取網路介面卡 (NIC) 。 這些函式提供三種方式來列舉一組 Nic，並選取您想要使用的一組。 下表列出這些函數。
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: 選取網路介面卡
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115076"
---
# <a name="selecting-a-network-interface-card"></a><span data-ttu-id="b292f-105">選取網路介面卡</span><span class="sxs-lookup"><span data-stu-id="b292f-105">Selecting a Network Interface Card</span></span>

<span data-ttu-id="b292f-106">網路監視器提供三個功能來選取網路介面卡 (NIC) 。</span><span class="sxs-lookup"><span data-stu-id="b292f-106">Network Monitor provides three functions for selecting a network interface card (NIC).</span></span> <span data-ttu-id="b292f-107">這些函式提供三種方式來列舉一組 Nic，並選取您想要使用的一組。</span><span class="sxs-lookup"><span data-stu-id="b292f-107">These functions provide three ways to enumerate a set of NICs and select the one you want to use.</span></span> <span data-ttu-id="b292f-108">下表列出這些函數。</span><span class="sxs-lookup"><span data-stu-id="b292f-108">The following table lists these functions.</span></span>



| <span data-ttu-id="b292f-109">函式</span><span class="sxs-lookup"><span data-stu-id="b292f-109">Function</span></span>                                                 | <span data-ttu-id="b292f-110">描述</span><span class="sxs-lookup"><span data-stu-id="b292f-110">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b292f-111">**GetNPPBlobFromUI**</span><span class="sxs-lookup"><span data-stu-id="b292f-111">**GetNPPBlobFromUI**</span></span>](getnppblobfromui.md)             | <span data-ttu-id="b292f-112">使用網路監視器 UI 來顯示已註冊的 Nic，並傳回代表您感興趣之 NIC 的 NPP BLOB。</span><span class="sxs-lookup"><span data-stu-id="b292f-112">Uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you are interested in.</span></span>           |
| [<span data-ttu-id="b292f-113">**GetNPPBlobTable**</span><span class="sxs-lookup"><span data-stu-id="b292f-113">**GetNPPBlobTable**</span></span>](getnppblobtable.md)               | <span data-ttu-id="b292f-114">傳回 BLOB 資料表。</span><span class="sxs-lookup"><span data-stu-id="b292f-114">Returns a BLOB table.</span></span> <span data-ttu-id="b292f-115">應用程式必須列舉資料表並選取 NPP BLOB。</span><span class="sxs-lookup"><span data-stu-id="b292f-115">The application must enumerate the table and select an NPP BLOB.</span></span>                                                       |
| [<span data-ttu-id="b292f-116">**SelectNPPBlobFromTable**</span><span class="sxs-lookup"><span data-stu-id="b292f-116">**SelectNPPBlobFromTable**</span></span>](selectnppblobfromtable.md) | <span data-ttu-id="b292f-117">使用網路監視器介面顯示提供的 NPP Blob，並傳回代表您感興趣之 NIC 的 NPP BLOB。</span><span class="sxs-lookup"><span data-stu-id="b292f-117">Uses the Network Monitor interface to display the supplied NPP BLOBs and returns the NPP BLOB that represents the NIC you are interested in.</span></span> |



 

<span data-ttu-id="b292f-118">每個 NIC 都會以 NPP 二進位大型物件表示 (BLOB) 。</span><span class="sxs-lookup"><span data-stu-id="b292f-118">Each NIC is represented by an NPP binary large object (BLOB).</span></span> <span data-ttu-id="b292f-119">這些函式可以從電腦上註冊的 NPP BLOB、所提供之 NPP BLOB 資料表中的單一 NPP BLOB，或呼叫端必須用來選取特定 BLOB 的 NPP Blob 資料表傳回單一 BLOB。</span><span class="sxs-lookup"><span data-stu-id="b292f-119">These functions can return a single NPP BLOB from those registered on the computer, a single NPP BLOB from a supplied NPP BLOB table, or a table of NPP BLOBs that the caller must then use to select a specific BLOB.</span></span> <span data-ttu-id="b292f-120">在前兩個案例中，從已註冊的 Nic 或從提供的 NPP BLOB 資料表中選取時，網路監視器 UI 會顯示您可以選取的 Nic。</span><span class="sxs-lookup"><span data-stu-id="b292f-120">In the first two cases, when selecting from the registered NICs or from a supplied NPP BLOB table, the Network Monitor UI displays the NICs you can select.</span></span>

> [!Note]  
> <span data-ttu-id="b292f-121">網路監視器使用稱為 NPP Finder 的功能來列舉在本機電腦上註冊的 Nic。</span><span class="sxs-lookup"><span data-stu-id="b292f-121">Network Monitor uses a feature called the NPP Finder to enumerate the NICs registered on the local computer.</span></span> <span data-ttu-id="b292f-122">NPP Finder 是 Npptools.dll 的元件。</span><span class="sxs-lookup"><span data-stu-id="b292f-122">The NPP Finder is a component of Npptools.dll.</span></span>

 



| <span data-ttu-id="b292f-123">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="b292f-123">For information about</span></span>                            | <span data-ttu-id="b292f-124">請參閱</span><span class="sxs-lookup"><span data-stu-id="b292f-124">See</span></span>                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b292f-125">選取在本機電腦上註冊的 NIC</span><span class="sxs-lookup"><span data-stu-id="b292f-125">Selecting a NIC registered on the local computer</span></span> | [<span data-ttu-id="b292f-126">選取已註冊的 NIC</span><span class="sxs-lookup"><span data-stu-id="b292f-126">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="b292f-127">從提供的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="b292f-127">Selecting a NIC from a supplied NPP BLOB table</span></span>   | [<span data-ttu-id="b292f-128">從提供的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="b292f-128">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| <span data-ttu-id="b292f-129">正在抓取 NPP BLOB 資料表</span><span class="sxs-lookup"><span data-stu-id="b292f-129">Retrieving an NPP BLOB table</span></span>                     | [<span data-ttu-id="b292f-130">從傳回的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="b292f-130">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 




---
description: 若要從網路監視器所傳回的 NPP BLOB 資料表中選取 NIC，請呼叫 GetNPPBlobTable 函數。 此函式會傳回 NPP BLOB 資料表，然後您的應用程式會加以列舉，以選取您感興趣的 NIC。
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: 從傳回的 NPP BLOB 資料表選取 NIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08215bb647482ba8544d7eaa033dea7efd9a5ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849324"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a><span data-ttu-id="597af-104">從傳回的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="597af-104">Selecting a NIC from a Returned NPP BLOB table</span></span>

<span data-ttu-id="597af-105">若要從網路監視器所傳回的 NPP BLOB 資料表中選取 NIC，請呼叫 [**GetNPPBlobTable**](getnppblobtable.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="597af-105">To select a NIC from an NPP BLOB table returned by Network Monitor, call the [**GetNPPBlobTable**](getnppblobtable.md) function.</span></span> <span data-ttu-id="597af-106">此函式會傳回 NPP BLOB 資料表，然後您的應用程式會加以列舉，以選取您感興趣的 NIC。</span><span class="sxs-lookup"><span data-stu-id="597af-106">This function returns an NPP BLOB table, which can then be enumerated by your application to select the NIC you are interested in.</span></span>

<span data-ttu-id="597af-107">當您呼叫此函式時，您可以傳回在本機電腦上註冊之所有 Nic 的 BLOB 資料表，或是一組較小的篩選 Nic。</span><span class="sxs-lookup"><span data-stu-id="597af-107">When you call this function you can return either a BLOB table of all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="597af-108">若要篩選傳回的 Nic，您可以在進行呼叫時提供 [*篩選 BLOB*](f.md) 。</span><span class="sxs-lookup"><span data-stu-id="597af-108">To filter the NICs that are returned, you can provide a [*filter BLOB*](f.md) when the call is made.</span></span>



| <span data-ttu-id="597af-109">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="597af-109">For information about</span></span>                                                       | <span data-ttu-id="597af-110">請參閱</span><span class="sxs-lookup"><span data-stu-id="597af-110">See</span></span>                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="597af-111">如何指定篩選器來限制 NPP BLOB 資料表中傳回的 Nic。</span><span class="sxs-lookup"><span data-stu-id="597af-111">How to specify a filter that limits the NICs returned in an NPP BLOB table.</span></span> | [<span data-ttu-id="597af-112">指定篩選 BLOB</span><span class="sxs-lookup"><span data-stu-id="597af-112">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="597af-113">如何選取在本機電腦上註冊的 NIC。</span><span class="sxs-lookup"><span data-stu-id="597af-113">How to select a NIC registered on a local computer.</span></span>                         | [<span data-ttu-id="597af-114">選取已註冊的 NIC</span><span class="sxs-lookup"><span data-stu-id="597af-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="597af-115">如何從提供的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="597af-115">How to select a NIC from a supplied NPP BLOB table</span></span>                          | [<span data-ttu-id="597af-116">從提供的 NPP BLOB 資料表選取 NIC</span><span class="sxs-lookup"><span data-stu-id="597af-116">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 




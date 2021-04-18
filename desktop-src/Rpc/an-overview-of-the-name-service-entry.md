---
title: 名稱服務專案的總覽
description: 名稱服務專案包含三個不同的區段。
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968457"
---
# <a name="an-overview-of-the-name-service-entry"></a><span data-ttu-id="6eae3-103">名稱服務專案的總覽</span><span class="sxs-lookup"><span data-stu-id="6eae3-103">An Overview of the Name Service Entry</span></span>

<span data-ttu-id="6eae3-104">名稱服務專案包含三個不同的區段。</span><span class="sxs-lookup"><span data-stu-id="6eae3-104">The name service entry consists of three distinct sections.</span></span> <span data-ttu-id="6eae3-105">第一個區段適用于 (UUID + version) 的介面，第二個區段包含物件 Uuid，第三個區段則用於系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="6eae3-105">The first section is for interfaces (UUID + version), the second section contains the object UUIDs, and the third section is for binding handles.</span></span> <span data-ttu-id="6eae3-106">您可以提供專案的名稱，以做為識別的方式。</span><span class="sxs-lookup"><span data-stu-id="6eae3-106">You provide a name for the entry that will serve as a way to identify it.</span></span>

<span data-ttu-id="6eae3-107">當呼叫 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)時，伺服器會指定要在其中放置匯出資訊的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="6eae3-107">When calling [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), the server specifies the name of the entry in which to place the exported information.</span></span> <span data-ttu-id="6eae3-108">接著會將這個新匯出的介面新增至名稱服務專案的介面區段。</span><span class="sxs-lookup"><span data-stu-id="6eae3-108">This newly exported interface is then added to the interface section of the name service entry.</span></span> <span data-ttu-id="6eae3-109">名稱服務專案中已經存在的任何介面也會維持不變。</span><span class="sxs-lookup"><span data-stu-id="6eae3-109">Any interfaces that are already present in the name service entry remain as well.</span></span> <span data-ttu-id="6eae3-110">針對物件 Uuid 和系結控制碼，會遵循相同的程式。</span><span class="sxs-lookup"><span data-stu-id="6eae3-110">This same process is followed for object UUIDs and binding handles.</span></span>

<span data-ttu-id="6eae3-111">用戶端會呼叫 [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (或 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) 來搜尋適當的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="6eae3-111">The client calls [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (or [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) to search for an appropriate binding handle.</span></span> <span data-ttu-id="6eae3-112">專案名稱、介面控制碼和物件 UUID 會解壓縮。</span><span class="sxs-lookup"><span data-stu-id="6eae3-112">The entry name, interface handle, and an object UUID are extracted.</span></span> <span data-ttu-id="6eae3-113">這些專案會限制傳回系結控制碼的專案。</span><span class="sxs-lookup"><span data-stu-id="6eae3-113">These restrict the entries from which binding handles are returned.</span></span> <span data-ttu-id="6eae3-114">如果專案符合搜尋準則，則會從 [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)傳回該專案中的所有系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="6eae3-114">If an entry matches the search criteria, all the binding handles in that entry are returned from [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span>

 

 





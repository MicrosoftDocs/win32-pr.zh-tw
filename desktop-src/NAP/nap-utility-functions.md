---
title: NAP 公用程式函式
description: 下列公用程式函數支援 NAP API。
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672732"
---
# <a name="nap-utility-functions"></a><span data-ttu-id="1e8b6-103">NAP 公用程式函式</span><span class="sxs-lookup"><span data-stu-id="1e8b6-103">NAP Utility Functions</span></span>

> [!Note]  
> <span data-ttu-id="1e8b6-104">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="1e8b6-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1e8b6-105">下列公用程式函數支援 NAP API。</span><span class="sxs-lookup"><span data-stu-id="1e8b6-105">The following utility functions support the NAP API.</span></span>

<span data-ttu-id="1e8b6-106">NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (CoTaskMemAlloc 和 CoTaskMemFree) 。</span><span class="sxs-lookup"><span data-stu-id="1e8b6-106">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocator (CoTaskMemAlloc and CoTaskMemFree).</span></span>

-   <span data-ttu-id="1e8b6-107">IN 參數：由呼叫端配置及釋放。</span><span class="sxs-lookup"><span data-stu-id="1e8b6-107">IN parameters — allocated and freed by caller.</span></span>
-   <span data-ttu-id="1e8b6-108">由被呼叫端所配置的 OUT 參數（由呼叫者使用 CoTaskMem 釋放） \* () </span><span class="sxs-lookup"><span data-stu-id="1e8b6-108">OUT parameters — allocated by callee, freed by caller using CoTaskMem\*()</span></span>
-   <span data-ttu-id="1e8b6-109">IN/OUT 參數（由呼叫端配置）由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 CoTaskMem \* () </span><span class="sxs-lookup"><span data-stu-id="1e8b6-109">IN/OUT parameters — allocated by caller, freed and reallocated by callee, ultimately freed by caller, using CoTaskMem\*()</span></span>

<span data-ttu-id="1e8b6-110">在 FreeXxx () 函式中，也會釋放所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="1e8b6-110">In the FreeXxx() functions, all embedded pointers will also be freed.</span></span>

-   [<span data-ttu-id="1e8b6-111">**AllocConnections**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-111">**AllocConnections**</span></span>](allocconnections-func.md)
-   [<span data-ttu-id="1e8b6-112">**AllocCountedString**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-112">**AllocCountedString**</span></span>](alloccountedstring-func.md)
-   [<span data-ttu-id="1e8b6-113">**AllocFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-113">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
-   [<span data-ttu-id="1e8b6-114">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-114">**FreeConnections**</span></span>](freeconnections-func.md)
-   [<span data-ttu-id="1e8b6-115">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-115">**FreeCountedString**</span></span>](freecountedstring-func.md)
-   [<span data-ttu-id="1e8b6-116">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-116">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
-   [<span data-ttu-id="1e8b6-117">**FreeIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-117">**FreeIsolationInfo**</span></span>](freeisolationinfo-func.md)
-   [<span data-ttu-id="1e8b6-118">**FreeIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-118">**FreeIsolationInfoEx**</span></span>](freeisolationinfoex.md)
-   [<span data-ttu-id="1e8b6-119">**FreeNapComponentRegistrationInfoArray**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-119">**FreeNapComponentRegistrationInfoArray**</span></span>](freenapcomponentregistrationinfoarray-func.md)
-   [<span data-ttu-id="1e8b6-120">**FreeNetworkSoH**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-120">**FreeNetworkSoH**</span></span>](freenetworksoh-func.md)
-   [<span data-ttu-id="1e8b6-121">**FreePrivateData**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-121">**FreePrivateData**</span></span>](freeprivatedata-func.md)
-   [<span data-ttu-id="1e8b6-122">**FreeSoH**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-122">**FreeSoH**</span></span>](freesoh-func.md)
-   [<span data-ttu-id="1e8b6-123">**FreeSoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-123">**FreeSoHAttributeValue**</span></span>](freesohattributevalue-func.md)
-   [<span data-ttu-id="1e8b6-124">**FreeSystemHealthAgentState**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-124">**FreeSystemHealthAgentState**</span></span>](freesystemhealthagentstate-func.md)
-   [<span data-ttu-id="1e8b6-125">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-125">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
-   [<span data-ttu-id="1e8b6-126">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="1e8b6-126">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)

 

 





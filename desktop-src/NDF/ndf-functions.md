---
title: NDF 函式
description: 下列功能可讓軟體發展人員使用網路診斷架構 (NDF) 所提供的功能。
ms.assetid: c2774e05-82f4-4d40-a80c-ad773bb03ca7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a039768b77d69072111f814cb871115bcca24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967616"
---
# <a name="ndf-functions"></a><span data-ttu-id="6a356-103">NDF 函式</span><span class="sxs-lookup"><span data-stu-id="6a356-103">NDF Functions</span></span>

<span data-ttu-id="6a356-104">下列功能可讓軟體發展人員使用網路診斷架構 (NDF) 所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="6a356-104">The following functions enable software developers to use the functionality provided by the Network Diagnostic Framework (NDF).</span></span> <span data-ttu-id="6a356-105">當發生網路問題時，NDF 可診斷根本原因，並正常處理必要的解決方法，有時甚至是執行必要的修復。</span><span class="sxs-lookup"><span data-stu-id="6a356-105">When network issues occur, NDF can diagnose the root cause and handle the necessary resolution gracefully, sometimes even performing the necessary repairs.</span></span>

> [!Note]  
> <span data-ttu-id="6a356-106">這些函式適用于在其應用程式中執行基本 NDF 功能的開發人員。</span><span class="sxs-lookup"><span data-stu-id="6a356-106">These functions are for developers implementing basic NDF functionality in their applications.</span></span>

 

-   [<span data-ttu-id="6a356-107">**CopyHelperAttribute**</span><span class="sxs-lookup"><span data-stu-id="6a356-107">**CopyHelperAttribute**</span></span>](copyhelperattribute.md)
-   [<span data-ttu-id="6a356-108">**CopyRepairInfo**</span><span class="sxs-lookup"><span data-stu-id="6a356-108">**CopyRepairInfo**</span></span>](copyrepairinfo.md)
-   [<span data-ttu-id="6a356-109">**CopyRootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="6a356-109">**CopyRootCauseInfo**</span></span>](copyrootcauseinfo.md)
-   [<span data-ttu-id="6a356-110">**FreeRepairInfoExs**</span><span class="sxs-lookup"><span data-stu-id="6a356-110">**FreeRepairInfoExs**</span></span>](freerepairinfoexs.md)
-   [<span data-ttu-id="6a356-111">**FreeRepairInfos**</span><span class="sxs-lookup"><span data-stu-id="6a356-111">**FreeRepairInfos**</span></span>](freerepairinfos.md)
-   [<span data-ttu-id="6a356-112">**FreeRootCauseInfos**</span><span class="sxs-lookup"><span data-stu-id="6a356-112">**FreeRootCauseInfos**</span></span>](freerootcauseinfos.md)
-   [<span data-ttu-id="6a356-113">**FreeHelperAttributes**</span><span class="sxs-lookup"><span data-stu-id="6a356-113">**FreeHelperAttributes**</span></span>](freehelperattributes.md)
-   [<span data-ttu-id="6a356-114">**FreeUiInfo**</span><span class="sxs-lookup"><span data-stu-id="6a356-114">**FreeUiInfo**</span></span>](freeuiinfo.md)
-   [<span data-ttu-id="6a356-115">**NdfCancelIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-115">**NdfCancelIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident)
-   [<span data-ttu-id="6a356-116">**NdfCloseIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-116">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
-   [<span data-ttu-id="6a356-117">**NdfCreateConnectivityIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-117">**NdfCreateConnectivityIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident)
-   [<span data-ttu-id="6a356-118">**NdfCreateDNSIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-118">**NdfCreateDNSIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident)
-   [<span data-ttu-id="6a356-119">**NdfCreateGroupingIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-119">**NdfCreateGroupingIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident)
-   [<span data-ttu-id="6a356-120">**NdfCreateInboundIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-120">**NdfCreateInboundIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateinboundincident)
-   [<span data-ttu-id="6a356-121">**NdfCreateIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-121">**NdfCreateIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident)
-   [<span data-ttu-id="6a356-122">**NdfCreateNetConnectionIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-122">**NdfCreateNetConnectionIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatenetconnectionincident)
-   [<span data-ttu-id="6a356-123">**NdfCreatePnrpIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-123">**NdfCreatePnrpIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident)
-   [<span data-ttu-id="6a356-124">**NdfCreateSharingIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-124">**NdfCreateSharingIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident)
-   [<span data-ttu-id="6a356-125">**NdfCreateWebIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-125">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
-   [<span data-ttu-id="6a356-126">**NdfCreateWebIncidentEx**</span><span class="sxs-lookup"><span data-stu-id="6a356-126">**NdfCreateWebIncidentEx**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex)
-   [<span data-ttu-id="6a356-127">**NdfCreateWinSockIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-127">**NdfCreateWinSockIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)
-   [<span data-ttu-id="6a356-128">**NdfDiagnoseIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-128">**NdfDiagnoseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident)
-   [<span data-ttu-id="6a356-129">**NdfExecuteDiagnosis**</span><span class="sxs-lookup"><span data-stu-id="6a356-129">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
-   [<span data-ttu-id="6a356-130">**NdfGetTraceFile**</span><span class="sxs-lookup"><span data-stu-id="6a356-130">**NdfGetTraceFile**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile)
-   [<span data-ttu-id="6a356-131">**NdfRepairIncident**</span><span class="sxs-lookup"><span data-stu-id="6a356-131">**NdfRepairIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident)
-   [<span data-ttu-id="6a356-132">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="6a356-132">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
-   [<span data-ttu-id="6a356-133">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="6a356-133">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
-   [<span data-ttu-id="6a356-134">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="6a356-134">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)

 

 





---
title: " (BITS 的 IBackgroundCopyJob 方法) "
description: 'IBackgroundCopyJob 介面會公開下列方法。 | (BITS 的 IBackgroundCopyJob 方法) '
ms.assetid: CB1C6D64-416A-4F31-AC9D-B3C1A6818034
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a7ebeeefa90c90435f1294d78c4816cf77be3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514409"
---
# <a name="ibackgroundcopyjob-methods-bits"></a><span data-ttu-id="f5bc6-104"> (BITS 的 IBackgroundCopyJob 方法) </span><span class="sxs-lookup"><span data-stu-id="f5bc6-104">IBackgroundCopyJob Methods (BITS)</span></span>

<span data-ttu-id="f5bc6-105">[**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="f5bc6-105">The [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f5bc6-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="f5bc6-106">In this section</span></span>

-   [<span data-ttu-id="f5bc6-107">**AddFile 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-107">**AddFile Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
-   [<span data-ttu-id="f5bc6-108">**AddFileSet 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-108">**AddFileSet Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
-   [<span data-ttu-id="f5bc6-109">**Cancel 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-109">**Cancel Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   [<span data-ttu-id="f5bc6-110">**Complete 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-110">**Complete Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)
-   [<span data-ttu-id="f5bc6-111">**EnumFiles 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-111">**EnumFiles Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles)
-   [<span data-ttu-id="f5bc6-112">**GetDescription 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-112">**GetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdescription)
-   [<span data-ttu-id="f5bc6-113">**GetDisplayName 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-113">**GetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)
-   [<span data-ttu-id="f5bc6-114">**GetError 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-114">**GetError Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror)
-   [<span data-ttu-id="f5bc6-115">**GetErrorCount 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-115">**GetErrorCount Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterrorcount)
-   [<span data-ttu-id="f5bc6-116">**GetId 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-116">**GetId Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getid)
-   [<span data-ttu-id="f5bc6-117">**GetMinimumRetryDelay 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-117">**GetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay)
-   [<span data-ttu-id="f5bc6-118">**GetNoProgressTimeout 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-118">**GetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout)
-   [<span data-ttu-id="f5bc6-119">**GetNotifyFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-119">**GetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyflags)
-   [<span data-ttu-id="f5bc6-120">**GetNotifyInterface 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-120">**GetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyinterface)
-   [<span data-ttu-id="f5bc6-121">**GetOwner 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-121">**GetOwner Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner)
-   [<span data-ttu-id="f5bc6-122">**GetPriority 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-122">**GetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getpriority)
-   [<span data-ttu-id="f5bc6-123">**GetProgress 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-123">**GetProgress Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)
-   [<span data-ttu-id="f5bc6-124">**GetProxySettings 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-124">**GetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getproxysettings)
-   [<span data-ttu-id="f5bc6-125">**>getstate 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-125">**GetState Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate)
-   [<span data-ttu-id="f5bc6-126">**GetTimes 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-126">**GetTimes Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettimes)
-   [<span data-ttu-id="f5bc6-127">**GetType 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-127">**GetType Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettype)
-   [<span data-ttu-id="f5bc6-128">**Resume 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-128">**Resume Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
-   [<span data-ttu-id="f5bc6-129">**SetDescription 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-129">**SetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdescription)
-   [<span data-ttu-id="f5bc6-130">**SetDisplayName 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-130">**SetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdisplayname)
-   [<span data-ttu-id="f5bc6-131">**SetMinimumRetryDelay 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-131">**SetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay)
-   [<span data-ttu-id="f5bc6-132">**SetNoProgressTimeout 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-132">**SetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout)
-   [<span data-ttu-id="f5bc6-133">**SetNotifyFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-133">**SetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)
-   [<span data-ttu-id="f5bc6-134">**SetNotifyInterface 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-134">**SetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)
-   [<span data-ttu-id="f5bc6-135">**SetPriority 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-135">**SetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority)
-   [<span data-ttu-id="f5bc6-136">**SetProxySettings 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-136">**SetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)
-   [<span data-ttu-id="f5bc6-137">**暫止方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-137">**Suspend Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend)
-   [<span data-ttu-id="f5bc6-138">**TakeOwnership 方法**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-138">**TakeOwnership Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership)

 

 





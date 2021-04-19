---
title: 系結控制碼函數
description: 下表包含在系結控制碼上操作的 RPC 執行時間常式清單，並指定允許的系結控制碼類型。
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106991285"
---
# <a name="binding-handle-functions"></a><span data-ttu-id="037ff-103">系結控制碼函數</span><span class="sxs-lookup"><span data-stu-id="037ff-103">Binding Handle Functions</span></span>

<span data-ttu-id="037ff-104">下表包含在系結控制碼上操作的 RPC 執行時間常式清單，並指定允許的系結控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="037ff-104">The following table contains the list of RPC run-time routines that operate on binding handles and specifies the type of binding handle allowed.</span></span>



| <span data-ttu-id="037ff-105">常式傳回的值</span><span class="sxs-lookup"><span data-stu-id="037ff-105">Routine</span></span>                                                            | <span data-ttu-id="037ff-106">輸入引數</span><span class="sxs-lookup"><span data-stu-id="037ff-106">Input argument</span></span>   | <span data-ttu-id="037ff-107">Output 引數</span><span class="sxs-lookup"><span data-stu-id="037ff-107">Output argument</span></span> |
|--------------------------------------------------------------------|------------------|-----------------|
| [<span data-ttu-id="037ff-108">**RpcBindingCopy**</span><span class="sxs-lookup"><span data-stu-id="037ff-108">**RpcBindingCopy**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | <span data-ttu-id="037ff-109">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-109">Server</span></span>           | <span data-ttu-id="037ff-110">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-110">Server</span></span>          |
| [<span data-ttu-id="037ff-111">**RpcBindingFree**</span><span class="sxs-lookup"><span data-stu-id="037ff-111">**RpcBindingFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | <span data-ttu-id="037ff-112">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-112">Server</span></span>           | <span data-ttu-id="037ff-113">無</span><span class="sxs-lookup"><span data-stu-id="037ff-113">None</span></span>            |
| [<span data-ttu-id="037ff-114">**RpcBindingFromStringBinding**</span><span class="sxs-lookup"><span data-stu-id="037ff-114">**RpcBindingFromStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | <span data-ttu-id="037ff-115">無</span><span class="sxs-lookup"><span data-stu-id="037ff-115">None</span></span>             | <span data-ttu-id="037ff-116">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-116">Server</span></span>          |
| [<span data-ttu-id="037ff-117">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="037ff-117">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | <span data-ttu-id="037ff-118">用戶端</span><span class="sxs-lookup"><span data-stu-id="037ff-118">Client</span></span>           | <span data-ttu-id="037ff-119">無</span><span class="sxs-lookup"><span data-stu-id="037ff-119">None</span></span>            |
| [<span data-ttu-id="037ff-120">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="037ff-120">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | <span data-ttu-id="037ff-121">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-121">Server</span></span>           | <span data-ttu-id="037ff-122">無</span><span class="sxs-lookup"><span data-stu-id="037ff-122">None</span></span>            |
| [<span data-ttu-id="037ff-123">**RpcBindingInqObject**</span><span class="sxs-lookup"><span data-stu-id="037ff-123">**RpcBindingInqObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | <span data-ttu-id="037ff-124">伺服器或用戶端</span><span class="sxs-lookup"><span data-stu-id="037ff-124">Server or client</span></span> | <span data-ttu-id="037ff-125">無</span><span class="sxs-lookup"><span data-stu-id="037ff-125">None</span></span>            |
| [<span data-ttu-id="037ff-126">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="037ff-126">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | <span data-ttu-id="037ff-127">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-127">Server</span></span>           | <span data-ttu-id="037ff-128">無</span><span class="sxs-lookup"><span data-stu-id="037ff-128">None</span></span>            |
| [<span data-ttu-id="037ff-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="037ff-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | <span data-ttu-id="037ff-130">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-130">Server</span></span>           | <span data-ttu-id="037ff-131">無</span><span class="sxs-lookup"><span data-stu-id="037ff-131">None</span></span>            |
| [<span data-ttu-id="037ff-132">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="037ff-132">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | <span data-ttu-id="037ff-133">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-133">Server</span></span>           | <span data-ttu-id="037ff-134">無</span><span class="sxs-lookup"><span data-stu-id="037ff-134">None</span></span>            |
| [<span data-ttu-id="037ff-135">**RpcBindingToStringBinding**</span><span class="sxs-lookup"><span data-stu-id="037ff-135">**RpcBindingToStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | <span data-ttu-id="037ff-136">伺服器或用戶端</span><span class="sxs-lookup"><span data-stu-id="037ff-136">Server or client</span></span> | <span data-ttu-id="037ff-137">無</span><span class="sxs-lookup"><span data-stu-id="037ff-137">None</span></span>            |
| [<span data-ttu-id="037ff-138">**RpcBindingVectorFree**</span><span class="sxs-lookup"><span data-stu-id="037ff-138">**RpcBindingVectorFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | <span data-ttu-id="037ff-139">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-139">Server</span></span>           | <span data-ttu-id="037ff-140">無</span><span class="sxs-lookup"><span data-stu-id="037ff-140">None</span></span>            |
| [<span data-ttu-id="037ff-141">**RpcNsBindingExport**</span><span class="sxs-lookup"><span data-stu-id="037ff-141">**RpcNsBindingExport**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | <span data-ttu-id="037ff-142">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-142">Server</span></span>           | <span data-ttu-id="037ff-143">無</span><span class="sxs-lookup"><span data-stu-id="037ff-143">None</span></span>            |
| [<span data-ttu-id="037ff-144">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="037ff-144">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | <span data-ttu-id="037ff-145">無</span><span class="sxs-lookup"><span data-stu-id="037ff-145">None</span></span>             | <span data-ttu-id="037ff-146">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-146">Server</span></span>          |
| [<span data-ttu-id="037ff-147">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="037ff-147">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | <span data-ttu-id="037ff-148">無</span><span class="sxs-lookup"><span data-stu-id="037ff-148">None</span></span>             | <span data-ttu-id="037ff-149">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-149">Server</span></span>          |
| [<span data-ttu-id="037ff-150">**RpcNsBindingSelect**</span><span class="sxs-lookup"><span data-stu-id="037ff-150">**RpcNsBindingSelect**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | <span data-ttu-id="037ff-151">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-151">Server</span></span>           | <span data-ttu-id="037ff-152">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-152">Server</span></span>          |
| [<span data-ttu-id="037ff-153">**RpcServerInqBindings**</span><span class="sxs-lookup"><span data-stu-id="037ff-153">**RpcServerInqBindings**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | <span data-ttu-id="037ff-154">無</span><span class="sxs-lookup"><span data-stu-id="037ff-154">None</span></span>             | <span data-ttu-id="037ff-155">伺服器</span><span class="sxs-lookup"><span data-stu-id="037ff-155">Server</span></span>          |



 

 

 





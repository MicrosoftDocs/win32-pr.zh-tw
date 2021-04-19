---
title: 套用-群組-原則擴充許可權
description: 群組原則引擎用來判斷 GPO 是否適用于使用者或電腦的擴充許可權。
ms.assetid: f6b09ecc-0fcd-409b-adeb-a8744f811427
ms.tgt_platform: multiple
keywords:
- 套用-群組-原則擴充的正確 AD 架構
topic_type:
- apiref
api_name:
- Apply-Group-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7ee574b10a9bb4579cd3ac0f9366aeb28ed5a1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973730"
---
# <a name="apply-group-policy-extended-right"></a><span data-ttu-id="72e82-104">套用-群組-原則擴充許可權</span><span class="sxs-lookup"><span data-stu-id="72e82-104">Apply-Group-Policy extended right</span></span>

<span data-ttu-id="72e82-105">群組原則引擎用來判斷 GPO 是否適用于使用者或電腦的擴充許可權。</span><span class="sxs-lookup"><span data-stu-id="72e82-105">Extended right used by Group Policy engine to determine whether a GPO applies to a user or computer.</span></span>



| <span data-ttu-id="72e82-106">進入</span><span class="sxs-lookup"><span data-stu-id="72e82-106">Entry</span></span> | <span data-ttu-id="72e82-107">值</span><span class="sxs-lookup"><span data-stu-id="72e82-107">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="72e82-108">CN</span><span class="sxs-lookup"><span data-stu-id="72e82-108">CN</span></span>           | <span data-ttu-id="72e82-109">套用-群組-原則</span><span class="sxs-lookup"><span data-stu-id="72e82-109">Apply-Group-Policy</span></span>                   |
| <span data-ttu-id="72e82-110">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="72e82-110">Display-Name</span></span> | <span data-ttu-id="72e82-111">申請群組原則</span><span class="sxs-lookup"><span data-stu-id="72e82-111">Apply Group Policy</span></span>                   |
| <span data-ttu-id="72e82-112">許可權-GUID</span><span class="sxs-lookup"><span data-stu-id="72e82-112">Rights-GUID</span></span>  | <span data-ttu-id="72e82-113">edacfd8f-ffb3-11d1-b41d-00a0c968f939</span><span class="sxs-lookup"><span data-stu-id="72e82-113">edacfd8f-ffb3-11d1-b41d-00a0c968f939</span></span> |



## <a name="implementations"></a><span data-ttu-id="72e82-114">實作</span><span class="sxs-lookup"><span data-stu-id="72e82-114">Implementations</span></span>

-   [<span data-ttu-id="72e82-115">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="72e82-115">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="72e82-116">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72e82-116">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72e82-117">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72e82-117">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72e82-118">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72e82-118">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72e82-119">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72e82-119">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72e82-120">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72e82-120">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="72e82-121">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72e82-121">Windows 2000 Server</span></span>



| <span data-ttu-id="72e82-122">進入</span><span class="sxs-lookup"><span data-stu-id="72e82-122">Entry</span></span> | <span data-ttu-id="72e82-123">值</span><span class="sxs-lookup"><span data-stu-id="72e82-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="72e82-124">Applies-To</span><span class="sxs-lookup"><span data-stu-id="72e82-124">Applies-To</span></span>              | [<span data-ttu-id="72e82-125">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="72e82-125">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |
| <span data-ttu-id="72e82-126">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="72e82-126">Localization-Display-ID</span></span> | <span data-ttu-id="72e82-127">47</span><span class="sxs-lookup"><span data-stu-id="72e82-127">47</span></span>                                                                  |



## <a name="windows-server-2003"></a><span data-ttu-id="72e82-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72e82-128">Windows Server 2003</span></span>



| <span data-ttu-id="72e82-129">進入</span><span class="sxs-lookup"><span data-stu-id="72e82-129">Entry</span></span> | <span data-ttu-id="72e82-130">值</span><span class="sxs-lookup"><span data-stu-id="72e82-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="72e82-131">Applies-To</span><span class="sxs-lookup"><span data-stu-id="72e82-131">Applies-To</span></span>              | [<span data-ttu-id="72e82-132">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="72e82-132">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |
| <span data-ttu-id="72e82-133">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="72e82-133">Localization-Display-ID</span></span> | <span data-ttu-id="72e82-134">47</span><span class="sxs-lookup"><span data-stu-id="72e82-134">47</span></span>                                                                  |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72e82-135">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72e82-135">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72e82-136">進入</span><span class="sxs-lookup"><span data-stu-id="72e82-136">Entry</span></span> | <span data-ttu-id="72e82-137">值</span><span class="sxs-lookup"><span data-stu-id="72e82-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="72e82-138">Applies-To</span><span class="sxs-lookup"><span data-stu-id="72e82-138">Applies-To</span></span>              | [<span data-ttu-id="72e82-139">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="72e82-139">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |
| <span data-ttu-id="72e82-140">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="72e82-140">Localization-Display-ID</span></span> | <span data-ttu-id="72e82-141">47</span><span class="sxs-lookup"><span data-stu-id="72e82-141">47</span></span>                                                                  |



## <a name="windows-server-2008"></a><span data-ttu-id="72e82-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72e82-142">Windows Server 2008</span></span>



| <span data-ttu-id="72e82-143">進入</span><span class="sxs-lookup"><span data-stu-id="72e82-143">Entry</span></span> | <span data-ttu-id="72e82-144">值</span><span class="sxs-lookup"><span data-stu-id="72e82-144">Value</span></span> |
|-------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="72e82-145">Applies-To</span><span class="sxs-lookup"><span data-stu-id="72e82-145">Applies-To</span></span>              | [<span data-ttu-id="72e82-146">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="72e82-146">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |
| <span data-ttu-id="72e82-147">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="72e82-147">Localization-Display-ID</span></span> | <span data-ttu-id="72e82-148">47</span><span class="sxs-lookup"><span data-stu-id="72e82-148">47</span></span>                                                                  |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72e82-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72e82-149">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72e82-150">進入</span><span class="sxs-lookup"><span data-stu-id="72e82-150">Entry</span></span> | <span data-ttu-id="72e82-151">值</span><span class="sxs-lookup"><span data-stu-id="72e82-151">Value</span></span> |
|-------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="72e82-152">Applies-To</span><span class="sxs-lookup"><span data-stu-id="72e82-152">Applies-To</span></span>              | [<span data-ttu-id="72e82-153">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="72e82-153">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |
| <span data-ttu-id="72e82-154">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="72e82-154">Localization-Display-ID</span></span> | <span data-ttu-id="72e82-155">47</span><span class="sxs-lookup"><span data-stu-id="72e82-155">47</span></span>                                                                  |



## <a name="windows-server-2012"></a><span data-ttu-id="72e82-156">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72e82-156">Windows Server 2012</span></span>



| <span data-ttu-id="72e82-157">進入</span><span class="sxs-lookup"><span data-stu-id="72e82-157">Entry</span></span> | <span data-ttu-id="72e82-158">值</span><span class="sxs-lookup"><span data-stu-id="72e82-158">Value</span></span> |
|-------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="72e82-159">Applies-To</span><span class="sxs-lookup"><span data-stu-id="72e82-159">Applies-To</span></span>              | [<span data-ttu-id="72e82-160">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="72e82-160">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |
| <span data-ttu-id="72e82-161">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="72e82-161">Localization-Display-ID</span></span> | <span data-ttu-id="72e82-162">47</span><span class="sxs-lookup"><span data-stu-id="72e82-162">47</span></span>                                                                  |



 

 






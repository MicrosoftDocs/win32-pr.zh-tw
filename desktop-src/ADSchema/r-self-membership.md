---
title: Self-Membership 驗證的寫入
description: 已驗證的寫入權限，可讓您在新增/移除一個帳戶時，更新群組的成員資格。
ms.assetid: 180cba0c-0fe1-4a91-b41e-e7eceac41639
ms.tgt_platform: multiple
keywords:
- Self-Membership 驗證的寫入 AD 架構
topic_type:
- apiref
api_name:
- Self-Membership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24addeabd95de8b494f1ca1967fbe169d9f25341
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935221"
---
# <a name="self-membership-validated-writes"></a><span data-ttu-id="3f5d9-104">Self-Membership 驗證的寫入</span><span class="sxs-lookup"><span data-stu-id="3f5d9-104">Self-Membership validated writes</span></span>

<span data-ttu-id="3f5d9-105">已驗證的寫入權限，可讓您在新增/移除一個帳戶時，更新群組的成員資格。</span><span class="sxs-lookup"><span data-stu-id="3f5d9-105">Validated write permission to enable updating membership of a group in terms of adding/removing one's own account.</span></span>



| <span data-ttu-id="3f5d9-106">進入</span><span class="sxs-lookup"><span data-stu-id="3f5d9-106">Entry</span></span> | <span data-ttu-id="3f5d9-107">值</span><span class="sxs-lookup"><span data-stu-id="3f5d9-107">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="3f5d9-108">CN</span><span class="sxs-lookup"><span data-stu-id="3f5d9-108">CN</span></span>           | <span data-ttu-id="3f5d9-109">Self-Membership</span><span class="sxs-lookup"><span data-stu-id="3f5d9-109">Self-Membership</span></span>                      |
| <span data-ttu-id="3f5d9-110">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3f5d9-110">Display-Name</span></span> | <span data-ttu-id="3f5d9-111">新增/移除本身為成員</span><span class="sxs-lookup"><span data-stu-id="3f5d9-111">Add/Remove self as member</span></span>            |
| <span data-ttu-id="3f5d9-112">許可權-GUID</span><span class="sxs-lookup"><span data-stu-id="3f5d9-112">Rights-GUID</span></span>  | <span data-ttu-id="3f5d9-113">bf9679c0-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3f5d9-113">bf9679c0-0de6-11d0-a285-00aa003049e2</span></span> |



## <a name="implementations"></a><span data-ttu-id="3f5d9-114">實作</span><span class="sxs-lookup"><span data-stu-id="3f5d9-114">Implementations</span></span>

-   [<span data-ttu-id="3f5d9-115">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-115">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3f5d9-116">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-116">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3f5d9-117">**亞當**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-117">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3f5d9-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3f5d9-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3f5d9-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3f5d9-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3f5d9-122">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f5d9-122">Windows 2000 Server</span></span>



| <span data-ttu-id="3f5d9-123">進入</span><span class="sxs-lookup"><span data-stu-id="3f5d9-123">Entry</span></span> | <span data-ttu-id="3f5d9-124">值</span><span class="sxs-lookup"><span data-stu-id="3f5d9-124">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="3f5d9-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3f5d9-125">Applies-To</span></span>              | [<span data-ttu-id="3f5d9-126">**Group**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-126">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="3f5d9-127">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3f5d9-127">Localization-Display-ID</span></span> | <span data-ttu-id="3f5d9-128">12</span><span class="sxs-lookup"><span data-stu-id="3f5d9-128">12</span></span>                                  |



## <a name="windows-server-2003"></a><span data-ttu-id="3f5d9-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3f5d9-129">Windows Server 2003</span></span>



| <span data-ttu-id="3f5d9-130">進入</span><span class="sxs-lookup"><span data-stu-id="3f5d9-130">Entry</span></span> | <span data-ttu-id="3f5d9-131">值</span><span class="sxs-lookup"><span data-stu-id="3f5d9-131">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="3f5d9-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3f5d9-132">Applies-To</span></span>              | [<span data-ttu-id="3f5d9-133">**Group**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-133">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="3f5d9-134">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3f5d9-134">Localization-Display-ID</span></span> | <span data-ttu-id="3f5d9-135">12</span><span class="sxs-lookup"><span data-stu-id="3f5d9-135">12</span></span>                                  |



## <a name="adam"></a><span data-ttu-id="3f5d9-136">亞當</span><span class="sxs-lookup"><span data-stu-id="3f5d9-136">ADAM</span></span>



| <span data-ttu-id="3f5d9-137">進入</span><span class="sxs-lookup"><span data-stu-id="3f5d9-137">Entry</span></span> | <span data-ttu-id="3f5d9-138">值</span><span class="sxs-lookup"><span data-stu-id="3f5d9-138">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="3f5d9-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3f5d9-139">Applies-To</span></span>              | [<span data-ttu-id="3f5d9-140">**Group**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-140">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="3f5d9-141">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3f5d9-141">Localization-Display-ID</span></span> | <span data-ttu-id="3f5d9-142">12</span><span class="sxs-lookup"><span data-stu-id="3f5d9-142">12</span></span>                                  |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3f5d9-143">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3f5d9-143">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3f5d9-144">進入</span><span class="sxs-lookup"><span data-stu-id="3f5d9-144">Entry</span></span> | <span data-ttu-id="3f5d9-145">值</span><span class="sxs-lookup"><span data-stu-id="3f5d9-145">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="3f5d9-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3f5d9-146">Applies-To</span></span>              | [<span data-ttu-id="3f5d9-147">**Group**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-147">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="3f5d9-148">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3f5d9-148">Localization-Display-ID</span></span> | <span data-ttu-id="3f5d9-149">12</span><span class="sxs-lookup"><span data-stu-id="3f5d9-149">12</span></span>                                  |



## <a name="windows-server-2008"></a><span data-ttu-id="3f5d9-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f5d9-150">Windows Server 2008</span></span>



| <span data-ttu-id="3f5d9-151">進入</span><span class="sxs-lookup"><span data-stu-id="3f5d9-151">Entry</span></span> | <span data-ttu-id="3f5d9-152">值</span><span class="sxs-lookup"><span data-stu-id="3f5d9-152">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="3f5d9-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3f5d9-153">Applies-To</span></span>              | [<span data-ttu-id="3f5d9-154">**Group**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-154">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="3f5d9-155">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3f5d9-155">Localization-Display-ID</span></span> | <span data-ttu-id="3f5d9-156">12</span><span class="sxs-lookup"><span data-stu-id="3f5d9-156">12</span></span>                                  |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3f5d9-157">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f5d9-157">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3f5d9-158">進入</span><span class="sxs-lookup"><span data-stu-id="3f5d9-158">Entry</span></span> | <span data-ttu-id="3f5d9-159">值</span><span class="sxs-lookup"><span data-stu-id="3f5d9-159">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="3f5d9-160">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3f5d9-160">Applies-To</span></span>              | [<span data-ttu-id="3f5d9-161">**Group**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-161">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="3f5d9-162">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3f5d9-162">Localization-Display-ID</span></span> | <span data-ttu-id="3f5d9-163">12</span><span class="sxs-lookup"><span data-stu-id="3f5d9-163">12</span></span>                                  |



## <a name="windows-server-2012"></a><span data-ttu-id="3f5d9-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f5d9-164">Windows Server 2012</span></span>



| <span data-ttu-id="3f5d9-165">進入</span><span class="sxs-lookup"><span data-stu-id="3f5d9-165">Entry</span></span> | <span data-ttu-id="3f5d9-166">值</span><span class="sxs-lookup"><span data-stu-id="3f5d9-166">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="3f5d9-167">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3f5d9-167">Applies-To</span></span>              | [<span data-ttu-id="3f5d9-168">**Group**</span><span class="sxs-lookup"><span data-stu-id="3f5d9-168">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="3f5d9-169">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3f5d9-169">Localization-Display-ID</span></span> | <span data-ttu-id="3f5d9-170">12</span><span class="sxs-lookup"><span data-stu-id="3f5d9-170">12</span></span>                                  |



 

 






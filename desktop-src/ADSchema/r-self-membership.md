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
# <a name="self-membership-validated-writes"></a><span data-ttu-id="1eb1b-104">Self-Membership 驗證的寫入</span><span class="sxs-lookup"><span data-stu-id="1eb1b-104">Self-Membership validated writes</span></span>

<span data-ttu-id="1eb1b-105">已驗證的寫入權限，可讓您在新增/移除一個帳戶時，更新群組的成員資格。</span><span class="sxs-lookup"><span data-stu-id="1eb1b-105">Validated write permission to enable updating membership of a group in terms of adding/removing one's own account.</span></span>



| <span data-ttu-id="1eb1b-106">進入</span><span class="sxs-lookup"><span data-stu-id="1eb1b-106">Entry</span></span> | <span data-ttu-id="1eb1b-107">值</span><span class="sxs-lookup"><span data-stu-id="1eb1b-107">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="1eb1b-108">CN</span><span class="sxs-lookup"><span data-stu-id="1eb1b-108">CN</span></span>           | <span data-ttu-id="1eb1b-109">Self-Membership</span><span class="sxs-lookup"><span data-stu-id="1eb1b-109">Self-Membership</span></span>                      |
| <span data-ttu-id="1eb1b-110">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1eb1b-110">Display-Name</span></span> | <span data-ttu-id="1eb1b-111">新增/移除本身為成員</span><span class="sxs-lookup"><span data-stu-id="1eb1b-111">Add/Remove self as member</span></span>            |
| <span data-ttu-id="1eb1b-112">許可權-GUID</span><span class="sxs-lookup"><span data-stu-id="1eb1b-112">Rights-GUID</span></span>  | <span data-ttu-id="1eb1b-113">bf9679c0-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1eb1b-113">bf9679c0-0de6-11d0-a285-00aa003049e2</span></span> |



## <a name="implementations"></a><span data-ttu-id="1eb1b-114">實作</span><span class="sxs-lookup"><span data-stu-id="1eb1b-114">Implementations</span></span>

-   [<span data-ttu-id="1eb1b-115">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-115">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1eb1b-116">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-116">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1eb1b-117">**亞當**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-117">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1eb1b-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1eb1b-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1eb1b-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1eb1b-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1eb1b-122">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1eb1b-122">Windows 2000 Server</span></span>



| <span data-ttu-id="1eb1b-123">進入</span><span class="sxs-lookup"><span data-stu-id="1eb1b-123">Entry</span></span> | <span data-ttu-id="1eb1b-124">值</span><span class="sxs-lookup"><span data-stu-id="1eb1b-124">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="1eb1b-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="1eb1b-125">Applies-To</span></span>              | [<span data-ttu-id="1eb1b-126">**Group**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-126">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="1eb1b-127">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="1eb1b-127">Localization-Display-ID</span></span> | <span data-ttu-id="1eb1b-128">12</span><span class="sxs-lookup"><span data-stu-id="1eb1b-128">12</span></span>                                  |



## <a name="windows-server-2003"></a><span data-ttu-id="1eb1b-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1eb1b-129">Windows Server 2003</span></span>



| <span data-ttu-id="1eb1b-130">進入</span><span class="sxs-lookup"><span data-stu-id="1eb1b-130">Entry</span></span> | <span data-ttu-id="1eb1b-131">值</span><span class="sxs-lookup"><span data-stu-id="1eb1b-131">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="1eb1b-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="1eb1b-132">Applies-To</span></span>              | [<span data-ttu-id="1eb1b-133">**Group**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-133">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="1eb1b-134">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="1eb1b-134">Localization-Display-ID</span></span> | <span data-ttu-id="1eb1b-135">12</span><span class="sxs-lookup"><span data-stu-id="1eb1b-135">12</span></span>                                  |



## <a name="adam"></a><span data-ttu-id="1eb1b-136">亞當</span><span class="sxs-lookup"><span data-stu-id="1eb1b-136">ADAM</span></span>



| <span data-ttu-id="1eb1b-137">進入</span><span class="sxs-lookup"><span data-stu-id="1eb1b-137">Entry</span></span> | <span data-ttu-id="1eb1b-138">值</span><span class="sxs-lookup"><span data-stu-id="1eb1b-138">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="1eb1b-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="1eb1b-139">Applies-To</span></span>              | [<span data-ttu-id="1eb1b-140">**Group**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-140">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="1eb1b-141">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="1eb1b-141">Localization-Display-ID</span></span> | <span data-ttu-id="1eb1b-142">12</span><span class="sxs-lookup"><span data-stu-id="1eb1b-142">12</span></span>                                  |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1eb1b-143">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1eb1b-143">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1eb1b-144">進入</span><span class="sxs-lookup"><span data-stu-id="1eb1b-144">Entry</span></span> | <span data-ttu-id="1eb1b-145">值</span><span class="sxs-lookup"><span data-stu-id="1eb1b-145">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="1eb1b-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="1eb1b-146">Applies-To</span></span>              | [<span data-ttu-id="1eb1b-147">**Group**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-147">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="1eb1b-148">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="1eb1b-148">Localization-Display-ID</span></span> | <span data-ttu-id="1eb1b-149">12</span><span class="sxs-lookup"><span data-stu-id="1eb1b-149">12</span></span>                                  |



## <a name="windows-server-2008"></a><span data-ttu-id="1eb1b-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1eb1b-150">Windows Server 2008</span></span>



| <span data-ttu-id="1eb1b-151">進入</span><span class="sxs-lookup"><span data-stu-id="1eb1b-151">Entry</span></span> | <span data-ttu-id="1eb1b-152">值</span><span class="sxs-lookup"><span data-stu-id="1eb1b-152">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="1eb1b-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="1eb1b-153">Applies-To</span></span>              | [<span data-ttu-id="1eb1b-154">**Group**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-154">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="1eb1b-155">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="1eb1b-155">Localization-Display-ID</span></span> | <span data-ttu-id="1eb1b-156">12</span><span class="sxs-lookup"><span data-stu-id="1eb1b-156">12</span></span>                                  |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1eb1b-157">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1eb1b-157">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1eb1b-158">進入</span><span class="sxs-lookup"><span data-stu-id="1eb1b-158">Entry</span></span> | <span data-ttu-id="1eb1b-159">值</span><span class="sxs-lookup"><span data-stu-id="1eb1b-159">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="1eb1b-160">Applies-To</span><span class="sxs-lookup"><span data-stu-id="1eb1b-160">Applies-To</span></span>              | [<span data-ttu-id="1eb1b-161">**Group**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-161">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="1eb1b-162">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="1eb1b-162">Localization-Display-ID</span></span> | <span data-ttu-id="1eb1b-163">12</span><span class="sxs-lookup"><span data-stu-id="1eb1b-163">12</span></span>                                  |



## <a name="windows-server-2012"></a><span data-ttu-id="1eb1b-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1eb1b-164">Windows Server 2012</span></span>



| <span data-ttu-id="1eb1b-165">進入</span><span class="sxs-lookup"><span data-stu-id="1eb1b-165">Entry</span></span> | <span data-ttu-id="1eb1b-166">值</span><span class="sxs-lookup"><span data-stu-id="1eb1b-166">Value</span></span> |
|-------------------------|-------------------------------------|
| <span data-ttu-id="1eb1b-167">Applies-To</span><span class="sxs-lookup"><span data-stu-id="1eb1b-167">Applies-To</span></span>              | [<span data-ttu-id="1eb1b-168">**Group**</span><span class="sxs-lookup"><span data-stu-id="1eb1b-168">**Group**</span></span>](c-group.md)<br/> |
| <span data-ttu-id="1eb1b-169">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="1eb1b-169">Localization-Display-ID</span></span> | <span data-ttu-id="1eb1b-170">12</span><span class="sxs-lookup"><span data-stu-id="1eb1b-170">12</span></span>                                  |



 

 






---
title: 重新整理-群組-快取擴充許可權
description: 這不適用於 GC 登入。 沒有 GC 登入需要快取群組成員資格，而此控制存取許可權是用來授與系統管理員和操作員許可權，以立即重新整理快取，並聯系可用的 GC。
ms.assetid: 1db49a92-ccf8-4087-ac79-f4c1bcea6aa4
ms.tgt_platform: multiple
keywords:
- 重新整理-群組-快取擴充的正確 AD 架構
topic_type:
- apiref
api_name:
- Refresh-Group-Cache
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb576b5ef2310bceedb632a3b1ab8453b4d435e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844620"
---
# <a name="refresh-group-cache-extended-right"></a><span data-ttu-id="3dc7e-105">重新整理-群組-快取擴充許可權</span><span class="sxs-lookup"><span data-stu-id="3dc7e-105">Refresh-Group-Cache extended right</span></span>

<span data-ttu-id="3dc7e-106">這不適用於 GC 登入。</span><span class="sxs-lookup"><span data-stu-id="3dc7e-106">This is for no GC logon.</span></span> <span data-ttu-id="3dc7e-107">沒有 GC 登入需要快取群組成員資格，而此控制存取許可權是用來授與系統管理員和操作員許可權，以立即重新整理快取，並聯系可用的 GC。</span><span class="sxs-lookup"><span data-stu-id="3dc7e-107">No GC logon relies on caching group memberships, and this control access right is used to grant administrators and operators permission rights to cause an immediate refresh of the cache, contacting an available GC.</span></span>



| <span data-ttu-id="3dc7e-108">進入</span><span class="sxs-lookup"><span data-stu-id="3dc7e-108">Entry</span></span> | <span data-ttu-id="3dc7e-109">值</span><span class="sxs-lookup"><span data-stu-id="3dc7e-109">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="3dc7e-110">CN</span><span class="sxs-lookup"><span data-stu-id="3dc7e-110">CN</span></span>           | <span data-ttu-id="3dc7e-111">重新整理-群組-快取</span><span class="sxs-lookup"><span data-stu-id="3dc7e-111">Refresh-Group-Cache</span></span>                  |
| <span data-ttu-id="3dc7e-112">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3dc7e-112">Display-Name</span></span> | <span data-ttu-id="3dc7e-113">重新整理登入的群組快取</span><span class="sxs-lookup"><span data-stu-id="3dc7e-113">Refresh Group Cache for Logons</span></span>       |
| <span data-ttu-id="3dc7e-114">許可權-GUID</span><span class="sxs-lookup"><span data-stu-id="3dc7e-114">Rights-GUID</span></span>  | <span data-ttu-id="3dc7e-115">9432c620-033c-4db7-8b58-14ef6d0bf477</span><span class="sxs-lookup"><span data-stu-id="3dc7e-115">9432c620-033c-4db7-8b58-14ef6d0bf477</span></span> |



## <a name="implementations"></a><span data-ttu-id="3dc7e-116">實作</span><span class="sxs-lookup"><span data-stu-id="3dc7e-116">Implementations</span></span>

-   [<span data-ttu-id="3dc7e-117">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-117">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3dc7e-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3dc7e-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3dc7e-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3dc7e-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3dc7e-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3dc7e-122">Windows Server 2003</span></span>



| <span data-ttu-id="3dc7e-123">進入</span><span class="sxs-lookup"><span data-stu-id="3dc7e-123">Entry</span></span> | <span data-ttu-id="3dc7e-124">值</span><span class="sxs-lookup"><span data-stu-id="3dc7e-124">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="3dc7e-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3dc7e-125">Applies-To</span></span>              | [<span data-ttu-id="3dc7e-126">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-126">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="3dc7e-127">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3dc7e-127">Localization-Display-ID</span></span> | <span data-ttu-id="3dc7e-128">56</span><span class="sxs-lookup"><span data-stu-id="3dc7e-128">56</span></span>                                       |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3dc7e-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3dc7e-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3dc7e-130">進入</span><span class="sxs-lookup"><span data-stu-id="3dc7e-130">Entry</span></span> | <span data-ttu-id="3dc7e-131">值</span><span class="sxs-lookup"><span data-stu-id="3dc7e-131">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="3dc7e-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3dc7e-132">Applies-To</span></span>              | [<span data-ttu-id="3dc7e-133">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-133">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="3dc7e-134">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3dc7e-134">Localization-Display-ID</span></span> | <span data-ttu-id="3dc7e-135">56</span><span class="sxs-lookup"><span data-stu-id="3dc7e-135">56</span></span>                                       |



## <a name="windows-server-2008"></a><span data-ttu-id="3dc7e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3dc7e-136">Windows Server 2008</span></span>



| <span data-ttu-id="3dc7e-137">進入</span><span class="sxs-lookup"><span data-stu-id="3dc7e-137">Entry</span></span> | <span data-ttu-id="3dc7e-138">值</span><span class="sxs-lookup"><span data-stu-id="3dc7e-138">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="3dc7e-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3dc7e-139">Applies-To</span></span>              | [<span data-ttu-id="3dc7e-140">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-140">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="3dc7e-141">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3dc7e-141">Localization-Display-ID</span></span> | <span data-ttu-id="3dc7e-142">56</span><span class="sxs-lookup"><span data-stu-id="3dc7e-142">56</span></span>                                       |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3dc7e-143">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3dc7e-143">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3dc7e-144">進入</span><span class="sxs-lookup"><span data-stu-id="3dc7e-144">Entry</span></span> | <span data-ttu-id="3dc7e-145">值</span><span class="sxs-lookup"><span data-stu-id="3dc7e-145">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="3dc7e-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3dc7e-146">Applies-To</span></span>              | [<span data-ttu-id="3dc7e-147">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-147">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="3dc7e-148">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3dc7e-148">Localization-Display-ID</span></span> | <span data-ttu-id="3dc7e-149">56</span><span class="sxs-lookup"><span data-stu-id="3dc7e-149">56</span></span>                                       |



## <a name="windows-server-2012"></a><span data-ttu-id="3dc7e-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3dc7e-150">Windows Server 2012</span></span>



| <span data-ttu-id="3dc7e-151">進入</span><span class="sxs-lookup"><span data-stu-id="3dc7e-151">Entry</span></span> | <span data-ttu-id="3dc7e-152">值</span><span class="sxs-lookup"><span data-stu-id="3dc7e-152">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="3dc7e-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="3dc7e-153">Applies-To</span></span>              | [<span data-ttu-id="3dc7e-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3dc7e-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="3dc7e-155">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="3dc7e-155">Localization-Display-ID</span></span> | <span data-ttu-id="3dc7e-156">56</span><span class="sxs-lookup"><span data-stu-id="3dc7e-156">56</span></span>                                       |



 

 






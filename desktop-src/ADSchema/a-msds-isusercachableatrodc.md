---
title: ms-DS-Cachable Rodc 屬性
description: 針對 (RODC) 的 Read-Only 網域控制站，識別是否可以快取指定的使用者密碼。
ms.assetid: 1118d0a9-2219-478a-82b0-8ea4bbeae47d
ms.tgt_platform: multiple
keywords:
- ms-DS-使用者-Cachable-Rodc 屬性 AD 架構
- IsUserCachableAtRodc 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Is-User-Cachable-At-Rodc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5699208cebe4c49321186813a64611f79ec52f4b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687255"
---
# <a name="ms-ds-is-user-cachable-at-rodc-attribute"></a><span data-ttu-id="e4c8b-105">ms-DS-Cachable Rodc 屬性</span><span class="sxs-lookup"><span data-stu-id="e4c8b-105">ms-DS-Is-User-Cachable-At-Rodc attribute</span></span>

<span data-ttu-id="e4c8b-106">針對 (RODC) 的 Read-Only 網域控制站，識別是否可以快取指定的使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="e4c8b-106">For a Read-Only Domain Controller (RODC), identifies whether the specified user's secrets can be cached.</span></span>



| <span data-ttu-id="e4c8b-107">進入</span><span class="sxs-lookup"><span data-stu-id="e4c8b-107">Entry</span></span> | <span data-ttu-id="e4c8b-108">值</span><span class="sxs-lookup"><span data-stu-id="e4c8b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e4c8b-109">CN</span><span class="sxs-lookup"><span data-stu-id="e4c8b-109">CN</span></span>                | <span data-ttu-id="e4c8b-110">ms-DS-Is-User-Cachable-At-Rodc</span><span class="sxs-lookup"><span data-stu-id="e4c8b-110">ms-DS-Is-User-Cachable-At-Rodc</span></span>       |
| <span data-ttu-id="e4c8b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e4c8b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e4c8b-112">msDS-IsUserCachableAtRodc</span><span class="sxs-lookup"><span data-stu-id="e4c8b-112">msDS-IsUserCachableAtRodc</span></span>            |
| <span data-ttu-id="e4c8b-113">大小</span><span class="sxs-lookup"><span data-stu-id="e4c8b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="e4c8b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e4c8b-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e4c8b-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e4c8b-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e4c8b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e4c8b-116">Attribute-Id</span></span>      | <span data-ttu-id="e4c8b-117">1.2.840.113556.1.4.2025</span><span class="sxs-lookup"><span data-stu-id="e4c8b-117">1.2.840.113556.1.4.2025</span></span>              |
| <span data-ttu-id="e4c8b-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e4c8b-118">System-Id-Guid</span></span>    | <span data-ttu-id="e4c8b-119">fe01245a-341f-4556-951f-48c033a89050</span><span class="sxs-lookup"><span data-stu-id="e4c8b-119">fe01245a-341f-4556-951f-48c033a89050</span></span> |
| <span data-ttu-id="e4c8b-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4c8b-120">Syntax</span></span>            | [<span data-ttu-id="e4c8b-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e4c8b-122">實作</span><span class="sxs-lookup"><span data-stu-id="e4c8b-122">Implementations</span></span>

-   [<span data-ttu-id="e4c8b-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e4c8b-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e4c8b-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="e4c8b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4c8b-126">Windows Server 2008</span></span>



| <span data-ttu-id="e4c8b-127">進入</span><span class="sxs-lookup"><span data-stu-id="e4c8b-127">Entry</span></span> | <span data-ttu-id="e4c8b-128">值</span><span class="sxs-lookup"><span data-stu-id="e4c8b-128">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c8b-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e4c8b-129">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4c8b-130">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4c8b-131">System-Only</span></span>            | <span data-ttu-id="e4c8b-132">否</span><span class="sxs-lookup"><span data-stu-id="e4c8b-132">False</span></span>                                                                                                                    |
| <span data-ttu-id="e4c8b-133">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e4c8b-133">Is-Single-Valued</span></span>       | <span data-ttu-id="e4c8b-134">對</span><span class="sxs-lookup"><span data-stu-id="e4c8b-134">True</span></span>                                                                                                                     |
| <span data-ttu-id="e4c8b-135">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e4c8b-135">Is Indexed</span></span>             | <span data-ttu-id="e4c8b-136">否</span><span class="sxs-lookup"><span data-stu-id="e4c8b-136">False</span></span>                                                                                                                    |
| <span data-ttu-id="e4c8b-137">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e4c8b-137">In Global Catalog</span></span>      | <span data-ttu-id="e4c8b-138">否</span><span class="sxs-lookup"><span data-stu-id="e4c8b-138">False</span></span>                                                                                                                    |
| <span data-ttu-id="e4c8b-139">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e4c8b-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4c8b-140">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e4c8b-140">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="e4c8b-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4c8b-141">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4c8b-142">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4c8b-143">Search-Flags</span></span>           | <span data-ttu-id="e4c8b-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4c8b-144">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="e4c8b-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4c8b-145">System-Flags</span></span>           | <span data-ttu-id="e4c8b-146">0x00000014</span><span class="sxs-lookup"><span data-stu-id="e4c8b-146">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="e4c8b-147">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e4c8b-147">Classes used in</span></span>        | [<span data-ttu-id="e4c8b-148">**電腦**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-148">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e4c8b-149">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-149">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="e4c8b-150">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-150">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e4c8b-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e4c8b-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e4c8b-152">進入</span><span class="sxs-lookup"><span data-stu-id="e4c8b-152">Entry</span></span> | <span data-ttu-id="e4c8b-153">值</span><span class="sxs-lookup"><span data-stu-id="e4c8b-153">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c8b-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e4c8b-154">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4c8b-155">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4c8b-156">System-Only</span></span>            | <span data-ttu-id="e4c8b-157">否</span><span class="sxs-lookup"><span data-stu-id="e4c8b-157">False</span></span>                                                                                                                    |
| <span data-ttu-id="e4c8b-158">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e4c8b-158">Is-Single-Valued</span></span>       | <span data-ttu-id="e4c8b-159">對</span><span class="sxs-lookup"><span data-stu-id="e4c8b-159">True</span></span>                                                                                                                     |
| <span data-ttu-id="e4c8b-160">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e4c8b-160">Is Indexed</span></span>             | <span data-ttu-id="e4c8b-161">否</span><span class="sxs-lookup"><span data-stu-id="e4c8b-161">False</span></span>                                                                                                                    |
| <span data-ttu-id="e4c8b-162">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e4c8b-162">In Global Catalog</span></span>      | <span data-ttu-id="e4c8b-163">否</span><span class="sxs-lookup"><span data-stu-id="e4c8b-163">False</span></span>                                                                                                                    |
| <span data-ttu-id="e4c8b-164">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e4c8b-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4c8b-165">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e4c8b-165">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="e4c8b-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4c8b-166">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4c8b-167">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4c8b-168">Search-Flags</span></span>           | <span data-ttu-id="e4c8b-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4c8b-169">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="e4c8b-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4c8b-170">System-Flags</span></span>           | <span data-ttu-id="e4c8b-171">0x00000014</span><span class="sxs-lookup"><span data-stu-id="e4c8b-171">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="e4c8b-172">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e4c8b-172">Classes used in</span></span>        | [<span data-ttu-id="e4c8b-173">**電腦**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-173">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e4c8b-174">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-174">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="e4c8b-175">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-175">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e4c8b-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4c8b-176">Windows Server 2012</span></span>



| <span data-ttu-id="e4c8b-177">進入</span><span class="sxs-lookup"><span data-stu-id="e4c8b-177">Entry</span></span> | <span data-ttu-id="e4c8b-178">值</span><span class="sxs-lookup"><span data-stu-id="e4c8b-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c8b-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e4c8b-179">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4c8b-180">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4c8b-181">System-Only</span></span>            | <span data-ttu-id="e4c8b-182">否</span><span class="sxs-lookup"><span data-stu-id="e4c8b-182">False</span></span>                                                                                                                    |
| <span data-ttu-id="e4c8b-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e4c8b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e4c8b-184">對</span><span class="sxs-lookup"><span data-stu-id="e4c8b-184">True</span></span>                                                                                                                     |
| <span data-ttu-id="e4c8b-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e4c8b-185">Is Indexed</span></span>             | <span data-ttu-id="e4c8b-186">否</span><span class="sxs-lookup"><span data-stu-id="e4c8b-186">False</span></span>                                                                                                                    |
| <span data-ttu-id="e4c8b-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e4c8b-187">In Global Catalog</span></span>      | <span data-ttu-id="e4c8b-188">否</span><span class="sxs-lookup"><span data-stu-id="e4c8b-188">False</span></span>                                                                                                                    |
| <span data-ttu-id="e4c8b-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e4c8b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4c8b-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e4c8b-190">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="e4c8b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4c8b-191">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4c8b-192">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="e4c8b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4c8b-193">Search-Flags</span></span>           | <span data-ttu-id="e4c8b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4c8b-194">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="e4c8b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4c8b-195">System-Flags</span></span>           | <span data-ttu-id="e4c8b-196">0x00000014</span><span class="sxs-lookup"><span data-stu-id="e4c8b-196">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="e4c8b-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e4c8b-197">Classes used in</span></span>        | [<span data-ttu-id="e4c8b-198">**電腦**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-198">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="e4c8b-199">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-199">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="e4c8b-200">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="e4c8b-200">**Server**</span></span>](c-server.md)<br/> |



 

 






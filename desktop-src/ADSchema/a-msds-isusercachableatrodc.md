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
# <a name="ms-ds-is-user-cachable-at-rodc-attribute"></a><span data-ttu-id="6e2a9-105">ms-DS-Cachable Rodc 屬性</span><span class="sxs-lookup"><span data-stu-id="6e2a9-105">ms-DS-Is-User-Cachable-At-Rodc attribute</span></span>

<span data-ttu-id="6e2a9-106">針對 (RODC) 的 Read-Only 網域控制站，識別是否可以快取指定的使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-106">For a Read-Only Domain Controller (RODC), identifies whether the specified user's secrets can be cached.</span></span>



| <span data-ttu-id="6e2a9-107">進入</span><span class="sxs-lookup"><span data-stu-id="6e2a9-107">Entry</span></span> | <span data-ttu-id="6e2a9-108">值</span><span class="sxs-lookup"><span data-stu-id="6e2a9-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6e2a9-109">CN</span><span class="sxs-lookup"><span data-stu-id="6e2a9-109">CN</span></span>                | <span data-ttu-id="6e2a9-110">ms-DS-Is-User-Cachable-At-Rodc</span><span class="sxs-lookup"><span data-stu-id="6e2a9-110">ms-DS-Is-User-Cachable-At-Rodc</span></span>       |
| <span data-ttu-id="6e2a9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6e2a9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6e2a9-112">msDS-IsUserCachableAtRodc</span><span class="sxs-lookup"><span data-stu-id="6e2a9-112">msDS-IsUserCachableAtRodc</span></span>            |
| <span data-ttu-id="6e2a9-113">大小</span><span class="sxs-lookup"><span data-stu-id="6e2a9-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="6e2a9-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6e2a9-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="6e2a9-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6e2a9-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6e2a9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6e2a9-116">Attribute-Id</span></span>      | <span data-ttu-id="6e2a9-117">1.2.840.113556.1.4.2025</span><span class="sxs-lookup"><span data-stu-id="6e2a9-117">1.2.840.113556.1.4.2025</span></span>              |
| <span data-ttu-id="6e2a9-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6e2a9-118">System-Id-Guid</span></span>    | <span data-ttu-id="6e2a9-119">fe01245a-341f-4556-951f-48c033a89050</span><span class="sxs-lookup"><span data-stu-id="6e2a9-119">fe01245a-341f-4556-951f-48c033a89050</span></span> |
| <span data-ttu-id="6e2a9-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e2a9-120">Syntax</span></span>            | [<span data-ttu-id="6e2a9-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6e2a9-122">實作</span><span class="sxs-lookup"><span data-stu-id="6e2a9-122">Implementations</span></span>

-   [<span data-ttu-id="6e2a9-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6e2a9-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6e2a9-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="6e2a9-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e2a9-126">Windows Server 2008</span></span>



| <span data-ttu-id="6e2a9-127">進入</span><span class="sxs-lookup"><span data-stu-id="6e2a9-127">Entry</span></span> | <span data-ttu-id="6e2a9-128">值</span><span class="sxs-lookup"><span data-stu-id="6e2a9-128">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2a9-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e2a9-129">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e2a9-130">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e2a9-131">System-Only</span></span>            | <span data-ttu-id="6e2a9-132">否</span><span class="sxs-lookup"><span data-stu-id="6e2a9-132">False</span></span>                                                                                                                    |
| <span data-ttu-id="6e2a9-133">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e2a9-133">Is-Single-Valued</span></span>       | <span data-ttu-id="6e2a9-134">對</span><span class="sxs-lookup"><span data-stu-id="6e2a9-134">True</span></span>                                                                                                                     |
| <span data-ttu-id="6e2a9-135">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e2a9-135">Is Indexed</span></span>             | <span data-ttu-id="6e2a9-136">否</span><span class="sxs-lookup"><span data-stu-id="6e2a9-136">False</span></span>                                                                                                                    |
| <span data-ttu-id="6e2a9-137">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e2a9-137">In Global Catalog</span></span>      | <span data-ttu-id="6e2a9-138">否</span><span class="sxs-lookup"><span data-stu-id="6e2a9-138">False</span></span>                                                                                                                    |
| <span data-ttu-id="6e2a9-139">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e2a9-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e2a9-140">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e2a9-140">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="6e2a9-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e2a9-141">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e2a9-142">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e2a9-143">Search-Flags</span></span>           | <span data-ttu-id="6e2a9-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e2a9-144">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="6e2a9-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e2a9-145">System-Flags</span></span>           | <span data-ttu-id="6e2a9-146">0x00000014</span><span class="sxs-lookup"><span data-stu-id="6e2a9-146">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="6e2a9-147">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e2a9-147">Classes used in</span></span>        | [<span data-ttu-id="6e2a9-148">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-148">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="6e2a9-149">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-149">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="6e2a9-150">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-150">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6e2a9-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6e2a9-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6e2a9-152">進入</span><span class="sxs-lookup"><span data-stu-id="6e2a9-152">Entry</span></span> | <span data-ttu-id="6e2a9-153">值</span><span class="sxs-lookup"><span data-stu-id="6e2a9-153">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2a9-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e2a9-154">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e2a9-155">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e2a9-156">System-Only</span></span>            | <span data-ttu-id="6e2a9-157">否</span><span class="sxs-lookup"><span data-stu-id="6e2a9-157">False</span></span>                                                                                                                    |
| <span data-ttu-id="6e2a9-158">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e2a9-158">Is-Single-Valued</span></span>       | <span data-ttu-id="6e2a9-159">對</span><span class="sxs-lookup"><span data-stu-id="6e2a9-159">True</span></span>                                                                                                                     |
| <span data-ttu-id="6e2a9-160">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e2a9-160">Is Indexed</span></span>             | <span data-ttu-id="6e2a9-161">否</span><span class="sxs-lookup"><span data-stu-id="6e2a9-161">False</span></span>                                                                                                                    |
| <span data-ttu-id="6e2a9-162">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e2a9-162">In Global Catalog</span></span>      | <span data-ttu-id="6e2a9-163">否</span><span class="sxs-lookup"><span data-stu-id="6e2a9-163">False</span></span>                                                                                                                    |
| <span data-ttu-id="6e2a9-164">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e2a9-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e2a9-165">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e2a9-165">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="6e2a9-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e2a9-166">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e2a9-167">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e2a9-168">Search-Flags</span></span>           | <span data-ttu-id="6e2a9-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e2a9-169">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="6e2a9-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e2a9-170">System-Flags</span></span>           | <span data-ttu-id="6e2a9-171">0x00000014</span><span class="sxs-lookup"><span data-stu-id="6e2a9-171">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="6e2a9-172">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e2a9-172">Classes used in</span></span>        | [<span data-ttu-id="6e2a9-173">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-173">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="6e2a9-174">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-174">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="6e2a9-175">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-175">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6e2a9-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e2a9-176">Windows Server 2012</span></span>



| <span data-ttu-id="6e2a9-177">進入</span><span class="sxs-lookup"><span data-stu-id="6e2a9-177">Entry</span></span> | <span data-ttu-id="6e2a9-178">值</span><span class="sxs-lookup"><span data-stu-id="6e2a9-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2a9-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e2a9-179">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e2a9-180">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e2a9-181">System-Only</span></span>            | <span data-ttu-id="6e2a9-182">否</span><span class="sxs-lookup"><span data-stu-id="6e2a9-182">False</span></span>                                                                                                                    |
| <span data-ttu-id="6e2a9-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e2a9-183">Is-Single-Valued</span></span>       | <span data-ttu-id="6e2a9-184">對</span><span class="sxs-lookup"><span data-stu-id="6e2a9-184">True</span></span>                                                                                                                     |
| <span data-ttu-id="6e2a9-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e2a9-185">Is Indexed</span></span>             | <span data-ttu-id="6e2a9-186">否</span><span class="sxs-lookup"><span data-stu-id="6e2a9-186">False</span></span>                                                                                                                    |
| <span data-ttu-id="6e2a9-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e2a9-187">In Global Catalog</span></span>      | <span data-ttu-id="6e2a9-188">否</span><span class="sxs-lookup"><span data-stu-id="6e2a9-188">False</span></span>                                                                                                                    |
| <span data-ttu-id="6e2a9-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e2a9-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e2a9-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e2a9-190">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="6e2a9-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e2a9-191">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e2a9-192">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="6e2a9-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e2a9-193">Search-Flags</span></span>           | <span data-ttu-id="6e2a9-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e2a9-194">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="6e2a9-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e2a9-195">System-Flags</span></span>           | <span data-ttu-id="6e2a9-196">0x00000014</span><span class="sxs-lookup"><span data-stu-id="6e2a9-196">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="6e2a9-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e2a9-197">Classes used in</span></span>        | [<span data-ttu-id="6e2a9-198">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-198">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="6e2a9-199">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-199">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="6e2a9-200">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-200">**Server**</span></span>](c-server.md)<br/> |



 

 






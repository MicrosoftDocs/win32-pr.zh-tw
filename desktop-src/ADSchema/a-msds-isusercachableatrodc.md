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
# <a name="ms-ds-is-user-cachable-at-rodc-attribute"></a><span data-ttu-id="a50a0-105">ms-DS-Cachable Rodc 屬性</span><span class="sxs-lookup"><span data-stu-id="a50a0-105">ms-DS-Is-User-Cachable-At-Rodc attribute</span></span>

<span data-ttu-id="a50a0-106">針對 (RODC) 的 Read-Only 網域控制站，識別是否可以快取指定的使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="a50a0-106">For a Read-Only Domain Controller (RODC), identifies whether the specified user's secrets can be cached.</span></span>



| <span data-ttu-id="a50a0-107">進入</span><span class="sxs-lookup"><span data-stu-id="a50a0-107">Entry</span></span> | <span data-ttu-id="a50a0-108">值</span><span class="sxs-lookup"><span data-stu-id="a50a0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a50a0-109">CN</span><span class="sxs-lookup"><span data-stu-id="a50a0-109">CN</span></span>                | <span data-ttu-id="a50a0-110">ms-DS-Is-User-Cachable-At-Rodc</span><span class="sxs-lookup"><span data-stu-id="a50a0-110">ms-DS-Is-User-Cachable-At-Rodc</span></span>       |
| <span data-ttu-id="a50a0-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a50a0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a50a0-112">msDS-IsUserCachableAtRodc</span><span class="sxs-lookup"><span data-stu-id="a50a0-112">msDS-IsUserCachableAtRodc</span></span>            |
| <span data-ttu-id="a50a0-113">大小</span><span class="sxs-lookup"><span data-stu-id="a50a0-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="a50a0-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a50a0-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a50a0-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a50a0-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a50a0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a50a0-116">Attribute-Id</span></span>      | <span data-ttu-id="a50a0-117">1.2.840.113556.1.4.2025</span><span class="sxs-lookup"><span data-stu-id="a50a0-117">1.2.840.113556.1.4.2025</span></span>              |
| <span data-ttu-id="a50a0-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a50a0-118">System-Id-Guid</span></span>    | <span data-ttu-id="a50a0-119">fe01245a-341f-4556-951f-48c033a89050</span><span class="sxs-lookup"><span data-stu-id="a50a0-119">fe01245a-341f-4556-951f-48c033a89050</span></span> |
| <span data-ttu-id="a50a0-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="a50a0-120">Syntax</span></span>            | [<span data-ttu-id="a50a0-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="a50a0-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a50a0-122">實作</span><span class="sxs-lookup"><span data-stu-id="a50a0-122">Implementations</span></span>

-   [<span data-ttu-id="a50a0-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a50a0-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a50a0-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a50a0-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a50a0-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a50a0-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="a50a0-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a50a0-126">Windows Server 2008</span></span>



| <span data-ttu-id="a50a0-127">進入</span><span class="sxs-lookup"><span data-stu-id="a50a0-127">Entry</span></span> | <span data-ttu-id="a50a0-128">值</span><span class="sxs-lookup"><span data-stu-id="a50a0-128">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a50a0-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a50a0-129">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="a50a0-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a50a0-130">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="a50a0-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="a50a0-131">System-Only</span></span>            | <span data-ttu-id="a50a0-132">否</span><span class="sxs-lookup"><span data-stu-id="a50a0-132">False</span></span>                                                                                                                    |
| <span data-ttu-id="a50a0-133">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a50a0-133">Is-Single-Valued</span></span>       | <span data-ttu-id="a50a0-134">對</span><span class="sxs-lookup"><span data-stu-id="a50a0-134">True</span></span>                                                                                                                     |
| <span data-ttu-id="a50a0-135">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a50a0-135">Is Indexed</span></span>             | <span data-ttu-id="a50a0-136">否</span><span class="sxs-lookup"><span data-stu-id="a50a0-136">False</span></span>                                                                                                                    |
| <span data-ttu-id="a50a0-137">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a50a0-137">In Global Catalog</span></span>      | <span data-ttu-id="a50a0-138">否</span><span class="sxs-lookup"><span data-stu-id="a50a0-138">False</span></span>                                                                                                                    |
| <span data-ttu-id="a50a0-139">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a50a0-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="a50a0-140">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a50a0-140">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="a50a0-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a50a0-141">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="a50a0-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a50a0-142">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="a50a0-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a50a0-143">Search-Flags</span></span>           | <span data-ttu-id="a50a0-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a50a0-144">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="a50a0-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a50a0-145">System-Flags</span></span>           | <span data-ttu-id="a50a0-146">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a50a0-146">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="a50a0-147">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a50a0-147">Classes used in</span></span>        | [<span data-ttu-id="a50a0-148">**電腦**</span><span class="sxs-lookup"><span data-stu-id="a50a0-148">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="a50a0-149">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a50a0-149">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a50a0-150">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a50a0-150">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a50a0-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a50a0-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a50a0-152">進入</span><span class="sxs-lookup"><span data-stu-id="a50a0-152">Entry</span></span> | <span data-ttu-id="a50a0-153">值</span><span class="sxs-lookup"><span data-stu-id="a50a0-153">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a50a0-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a50a0-154">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="a50a0-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a50a0-155">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="a50a0-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="a50a0-156">System-Only</span></span>            | <span data-ttu-id="a50a0-157">否</span><span class="sxs-lookup"><span data-stu-id="a50a0-157">False</span></span>                                                                                                                    |
| <span data-ttu-id="a50a0-158">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a50a0-158">Is-Single-Valued</span></span>       | <span data-ttu-id="a50a0-159">對</span><span class="sxs-lookup"><span data-stu-id="a50a0-159">True</span></span>                                                                                                                     |
| <span data-ttu-id="a50a0-160">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a50a0-160">Is Indexed</span></span>             | <span data-ttu-id="a50a0-161">否</span><span class="sxs-lookup"><span data-stu-id="a50a0-161">False</span></span>                                                                                                                    |
| <span data-ttu-id="a50a0-162">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a50a0-162">In Global Catalog</span></span>      | <span data-ttu-id="a50a0-163">否</span><span class="sxs-lookup"><span data-stu-id="a50a0-163">False</span></span>                                                                                                                    |
| <span data-ttu-id="a50a0-164">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a50a0-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="a50a0-165">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a50a0-165">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="a50a0-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a50a0-166">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="a50a0-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a50a0-167">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="a50a0-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a50a0-168">Search-Flags</span></span>           | <span data-ttu-id="a50a0-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a50a0-169">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="a50a0-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a50a0-170">System-Flags</span></span>           | <span data-ttu-id="a50a0-171">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a50a0-171">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="a50a0-172">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a50a0-172">Classes used in</span></span>        | [<span data-ttu-id="a50a0-173">**電腦**</span><span class="sxs-lookup"><span data-stu-id="a50a0-173">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="a50a0-174">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a50a0-174">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a50a0-175">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a50a0-175">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a50a0-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a50a0-176">Windows Server 2012</span></span>



| <span data-ttu-id="a50a0-177">進入</span><span class="sxs-lookup"><span data-stu-id="a50a0-177">Entry</span></span> | <span data-ttu-id="a50a0-178">值</span><span class="sxs-lookup"><span data-stu-id="a50a0-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a50a0-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a50a0-179">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="a50a0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a50a0-180">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="a50a0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a50a0-181">System-Only</span></span>            | <span data-ttu-id="a50a0-182">否</span><span class="sxs-lookup"><span data-stu-id="a50a0-182">False</span></span>                                                                                                                    |
| <span data-ttu-id="a50a0-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a50a0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a50a0-184">對</span><span class="sxs-lookup"><span data-stu-id="a50a0-184">True</span></span>                                                                                                                     |
| <span data-ttu-id="a50a0-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a50a0-185">Is Indexed</span></span>             | <span data-ttu-id="a50a0-186">否</span><span class="sxs-lookup"><span data-stu-id="a50a0-186">False</span></span>                                                                                                                    |
| <span data-ttu-id="a50a0-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a50a0-187">In Global Catalog</span></span>      | <span data-ttu-id="a50a0-188">否</span><span class="sxs-lookup"><span data-stu-id="a50a0-188">False</span></span>                                                                                                                    |
| <span data-ttu-id="a50a0-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a50a0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a50a0-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a50a0-190">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="a50a0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a50a0-191">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="a50a0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a50a0-192">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="a50a0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a50a0-193">Search-Flags</span></span>           | <span data-ttu-id="a50a0-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a50a0-194">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="a50a0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a50a0-195">System-Flags</span></span>           | <span data-ttu-id="a50a0-196">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a50a0-196">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="a50a0-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a50a0-197">Classes used in</span></span>        | [<span data-ttu-id="a50a0-198">**電腦**</span><span class="sxs-lookup"><span data-stu-id="a50a0-198">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="a50a0-199">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a50a0-199">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a50a0-200">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a50a0-200">**Server**</span></span>](c-server.md)<br/> |



 

 






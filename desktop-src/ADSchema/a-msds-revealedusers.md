---
title: ms-DS-顯示使用者屬性
description: 與 Rodc 搭配使用，以識別其秘密已洩漏至該 RODC 的使用者物件。
ms.assetid: 92f6d8a9-7829-4400-9b60-f1afe8653bc0
ms.tgt_platform: multiple
keywords:
- ms-DS-顯示使用者屬性 AD 架構
- RevealedUsers 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Revealed-Users
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4900fea126fc45119e5d5825431d788d170ff0bd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973115"
---
# <a name="ms-ds-revealed-users-attribute"></a><span data-ttu-id="c3e70-105">ms-DS-顯示使用者屬性</span><span class="sxs-lookup"><span data-stu-id="c3e70-105">ms-DS-Revealed-Users attribute</span></span>

<span data-ttu-id="c3e70-106">與 Rodc 搭配使用，以識別其秘密已洩漏至該 RODC 的使用者物件。</span><span class="sxs-lookup"><span data-stu-id="c3e70-106">Used with RODCs to identify the user objects whose secrets have been disclosed to that RODC.</span></span>



| <span data-ttu-id="c3e70-107">進入</span><span class="sxs-lookup"><span data-stu-id="c3e70-107">Entry</span></span> | <span data-ttu-id="c3e70-108">值</span><span class="sxs-lookup"><span data-stu-id="c3e70-108">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="c3e70-109">CN</span><span class="sxs-lookup"><span data-stu-id="c3e70-109">CN</span></span>                | <span data-ttu-id="c3e70-110">ms-DS-Revealed-Users</span><span class="sxs-lookup"><span data-stu-id="c3e70-110">ms-DS-Revealed-Users</span></span>                            |
| <span data-ttu-id="c3e70-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c3e70-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c3e70-112">msDS-RevealedUsers</span><span class="sxs-lookup"><span data-stu-id="c3e70-112">msDS-RevealedUsers</span></span>                              |
| <span data-ttu-id="c3e70-113">大小</span><span class="sxs-lookup"><span data-stu-id="c3e70-113">Size</span></span>              | \-                                              |
| <span data-ttu-id="c3e70-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c3e70-114">Update Privilege</span></span>  | \-                                              |
| <span data-ttu-id="c3e70-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c3e70-115">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="c3e70-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3e70-116">Attribute-Id</span></span>      | <span data-ttu-id="c3e70-117">1.2.840.113556.1.4.1924</span><span class="sxs-lookup"><span data-stu-id="c3e70-117">1.2.840.113556.1.4.1924</span></span>                         |
| <span data-ttu-id="c3e70-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c3e70-118">System-Id-Guid</span></span>    | <span data-ttu-id="c3e70-119">185c7821-3749-443a-bd6a-288899071adb</span><span class="sxs-lookup"><span data-stu-id="c3e70-119">185c7821-3749-443a-bd6a-288899071adb</span></span>            |
| <span data-ttu-id="c3e70-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3e70-120">Syntax</span></span>            | [<span data-ttu-id="c3e70-121">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="c3e70-121">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="c3e70-122">實作</span><span class="sxs-lookup"><span data-stu-id="c3e70-122">Implementations</span></span>

-   [<span data-ttu-id="c3e70-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3e70-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3e70-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3e70-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3e70-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3e70-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="c3e70-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3e70-126">Windows Server 2008</span></span>



| <span data-ttu-id="c3e70-127">進入</span><span class="sxs-lookup"><span data-stu-id="c3e70-127">Entry</span></span> | <span data-ttu-id="c3e70-128">值</span><span class="sxs-lookup"><span data-stu-id="c3e70-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e70-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3e70-129">Link-Id</span></span>                | <span data-ttu-id="c3e70-130">2102</span><span class="sxs-lookup"><span data-stu-id="c3e70-130">2102</span></span>                                                                               |
| <span data-ttu-id="c3e70-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3e70-131">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="c3e70-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3e70-132">System-Only</span></span>            | <span data-ttu-id="c3e70-133">對</span><span class="sxs-lookup"><span data-stu-id="c3e70-133">True</span></span>                                                                               |
| <span data-ttu-id="c3e70-134">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3e70-134">Is-Single-Valued</span></span>       | <span data-ttu-id="c3e70-135">否</span><span class="sxs-lookup"><span data-stu-id="c3e70-135">False</span></span>                                                                              |
| <span data-ttu-id="c3e70-136">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3e70-136">Is Indexed</span></span>             | <span data-ttu-id="c3e70-137">否</span><span class="sxs-lookup"><span data-stu-id="c3e70-137">False</span></span>                                                                              |
| <span data-ttu-id="c3e70-138">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3e70-138">In Global Catalog</span></span>      | <span data-ttu-id="c3e70-139">否</span><span class="sxs-lookup"><span data-stu-id="c3e70-139">False</span></span>                                                                              |
| <span data-ttu-id="c3e70-140">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3e70-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3e70-141">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3e70-141">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="c3e70-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3e70-142">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="c3e70-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3e70-143">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="c3e70-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e70-144">Search-Flags</span></span>           | <span data-ttu-id="c3e70-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3e70-145">0x00000000</span></span>                                                                         |
| <span data-ttu-id="c3e70-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e70-146">System-Flags</span></span>           | <span data-ttu-id="c3e70-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3e70-147">0x00000010</span></span>                                                                         |
| <span data-ttu-id="c3e70-148">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3e70-148">Classes used in</span></span>        | [<span data-ttu-id="c3e70-149">**電腦**</span><span class="sxs-lookup"><span data-stu-id="c3e70-149">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c3e70-150">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c3e70-150">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3e70-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3e70-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3e70-152">進入</span><span class="sxs-lookup"><span data-stu-id="c3e70-152">Entry</span></span> | <span data-ttu-id="c3e70-153">值</span><span class="sxs-lookup"><span data-stu-id="c3e70-153">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e70-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3e70-154">Link-Id</span></span>                | <span data-ttu-id="c3e70-155">2102</span><span class="sxs-lookup"><span data-stu-id="c3e70-155">2102</span></span>                                                                               |
| <span data-ttu-id="c3e70-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3e70-156">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="c3e70-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3e70-157">System-Only</span></span>            | <span data-ttu-id="c3e70-158">對</span><span class="sxs-lookup"><span data-stu-id="c3e70-158">True</span></span>                                                                               |
| <span data-ttu-id="c3e70-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3e70-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c3e70-160">否</span><span class="sxs-lookup"><span data-stu-id="c3e70-160">False</span></span>                                                                              |
| <span data-ttu-id="c3e70-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3e70-161">Is Indexed</span></span>             | <span data-ttu-id="c3e70-162">否</span><span class="sxs-lookup"><span data-stu-id="c3e70-162">False</span></span>                                                                              |
| <span data-ttu-id="c3e70-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3e70-163">In Global Catalog</span></span>      | <span data-ttu-id="c3e70-164">否</span><span class="sxs-lookup"><span data-stu-id="c3e70-164">False</span></span>                                                                              |
| <span data-ttu-id="c3e70-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3e70-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3e70-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3e70-166">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="c3e70-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3e70-167">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="c3e70-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3e70-168">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="c3e70-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e70-169">Search-Flags</span></span>           | <span data-ttu-id="c3e70-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3e70-170">0x00000000</span></span>                                                                         |
| <span data-ttu-id="c3e70-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e70-171">System-Flags</span></span>           | <span data-ttu-id="c3e70-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3e70-172">0x00000010</span></span>                                                                         |
| <span data-ttu-id="c3e70-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3e70-173">Classes used in</span></span>        | [<span data-ttu-id="c3e70-174">**電腦**</span><span class="sxs-lookup"><span data-stu-id="c3e70-174">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c3e70-175">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c3e70-175">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3e70-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3e70-176">Windows Server 2012</span></span>



| <span data-ttu-id="c3e70-177">進入</span><span class="sxs-lookup"><span data-stu-id="c3e70-177">Entry</span></span> | <span data-ttu-id="c3e70-178">值</span><span class="sxs-lookup"><span data-stu-id="c3e70-178">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e70-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3e70-179">Link-Id</span></span>                | <span data-ttu-id="c3e70-180">2102</span><span class="sxs-lookup"><span data-stu-id="c3e70-180">2102</span></span>                                                                               |
| <span data-ttu-id="c3e70-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3e70-181">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="c3e70-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3e70-182">System-Only</span></span>            | <span data-ttu-id="c3e70-183">對</span><span class="sxs-lookup"><span data-stu-id="c3e70-183">True</span></span>                                                                               |
| <span data-ttu-id="c3e70-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3e70-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c3e70-185">否</span><span class="sxs-lookup"><span data-stu-id="c3e70-185">False</span></span>                                                                              |
| <span data-ttu-id="c3e70-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3e70-186">Is Indexed</span></span>             | <span data-ttu-id="c3e70-187">否</span><span class="sxs-lookup"><span data-stu-id="c3e70-187">False</span></span>                                                                              |
| <span data-ttu-id="c3e70-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3e70-188">In Global Catalog</span></span>      | <span data-ttu-id="c3e70-189">否</span><span class="sxs-lookup"><span data-stu-id="c3e70-189">False</span></span>                                                                              |
| <span data-ttu-id="c3e70-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3e70-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3e70-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3e70-191">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="c3e70-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3e70-192">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="c3e70-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3e70-193">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="c3e70-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e70-194">Search-Flags</span></span>           | <span data-ttu-id="c3e70-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3e70-195">0x00000000</span></span>                                                                         |
| <span data-ttu-id="c3e70-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e70-196">System-Flags</span></span>           | <span data-ttu-id="c3e70-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3e70-197">0x00000010</span></span>                                                                         |
| <span data-ttu-id="c3e70-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3e70-198">Classes used in</span></span>        | [<span data-ttu-id="c3e70-199">**電腦**</span><span class="sxs-lookup"><span data-stu-id="c3e70-199">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c3e70-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c3e70-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 






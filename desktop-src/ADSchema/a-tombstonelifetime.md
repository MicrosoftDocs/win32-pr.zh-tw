---
title: Tombstone-Lifetime 屬性
description: 從目錄服務移除已刪除物件之前的天數。
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Tombstone-Lifetime 屬性 AD 架構
- tombstoneLifetime 屬性 AD 架構
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845279"
---
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="809fd-105">Tombstone-Lifetime 屬性</span><span class="sxs-lookup"><span data-stu-id="809fd-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="809fd-106">從目錄服務移除已刪除物件之前的天數。</span><span class="sxs-lookup"><span data-stu-id="809fd-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="809fd-107">這有助於從複寫的伺服器中移除物件，並防止還原重新介紹基於已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="809fd-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="809fd-108">此值位於 configuration NIC 的目錄服務物件中。</span><span class="sxs-lookup"><span data-stu-id="809fd-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="809fd-109">進入</span><span class="sxs-lookup"><span data-stu-id="809fd-109">Entry</span></span> | <span data-ttu-id="809fd-110">值</span><span class="sxs-lookup"><span data-stu-id="809fd-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="809fd-111">CN</span><span class="sxs-lookup"><span data-stu-id="809fd-111">CN</span></span>                | <span data-ttu-id="809fd-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="809fd-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="809fd-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="809fd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="809fd-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="809fd-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="809fd-115">大小</span><span class="sxs-lookup"><span data-stu-id="809fd-115">Size</span></span>              | <span data-ttu-id="809fd-116">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="809fd-116">4 bytes.</span></span> <span data-ttu-id="809fd-117">未輸入任何值時，預設值為60天。</span><span class="sxs-lookup"><span data-stu-id="809fd-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="809fd-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="809fd-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="809fd-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="809fd-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="809fd-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="809fd-120">Attribute-Id</span></span>      | <span data-ttu-id="809fd-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="809fd-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="809fd-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="809fd-122">System-Id-Guid</span></span>    | <span data-ttu-id="809fd-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="809fd-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="809fd-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="809fd-124">Syntax</span></span>            | [<span data-ttu-id="809fd-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="809fd-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="809fd-126">實作</span><span class="sxs-lookup"><span data-stu-id="809fd-126">Implementations</span></span>

-   [<span data-ttu-id="809fd-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="809fd-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="809fd-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="809fd-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="809fd-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="809fd-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="809fd-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="809fd-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="809fd-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="809fd-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="809fd-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="809fd-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="809fd-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="809fd-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="809fd-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="809fd-134">Windows 2000 Server</span></span>



| <span data-ttu-id="809fd-135">進入</span><span class="sxs-lookup"><span data-stu-id="809fd-135">Entry</span></span> | <span data-ttu-id="809fd-136">值</span><span class="sxs-lookup"><span data-stu-id="809fd-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="809fd-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="809fd-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="809fd-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="809fd-138">MAPI-Id</span></span>                | <span data-ttu-id="809fd-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="809fd-139">0x8145</span></span>                                           |
| <span data-ttu-id="809fd-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="809fd-140">System-Only</span></span>            | <span data-ttu-id="809fd-141">否</span><span class="sxs-lookup"><span data-stu-id="809fd-141">False</span></span>                                            |
| <span data-ttu-id="809fd-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="809fd-142">Is-Single-Valued</span></span>       | <span data-ttu-id="809fd-143">對</span><span class="sxs-lookup"><span data-stu-id="809fd-143">True</span></span>                                             |
| <span data-ttu-id="809fd-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="809fd-144">Is Indexed</span></span>             | <span data-ttu-id="809fd-145">否</span><span class="sxs-lookup"><span data-stu-id="809fd-145">False</span></span>                                            |
| <span data-ttu-id="809fd-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="809fd-146">In Global Catalog</span></span>      | <span data-ttu-id="809fd-147">否</span><span class="sxs-lookup"><span data-stu-id="809fd-147">False</span></span>                                            |
| <span data-ttu-id="809fd-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="809fd-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="809fd-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="809fd-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="809fd-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="809fd-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="809fd-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="809fd-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="809fd-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-152">Search-Flags</span></span>           | <span data-ttu-id="809fd-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="809fd-153">0x00000000</span></span>                                       |
| <span data-ttu-id="809fd-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-154">System-Flags</span></span>           | <span data-ttu-id="809fd-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="809fd-155">0x00000010</span></span>                                       |
| <span data-ttu-id="809fd-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="809fd-156">Classes used in</span></span>        | [<span data-ttu-id="809fd-157">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="809fd-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="809fd-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="809fd-158">Windows Server 2003</span></span>



| <span data-ttu-id="809fd-159">進入</span><span class="sxs-lookup"><span data-stu-id="809fd-159">Entry</span></span> | <span data-ttu-id="809fd-160">值</span><span class="sxs-lookup"><span data-stu-id="809fd-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="809fd-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="809fd-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="809fd-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="809fd-162">MAPI-Id</span></span>                | <span data-ttu-id="809fd-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="809fd-163">0x8145</span></span>                                           |
| <span data-ttu-id="809fd-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="809fd-164">System-Only</span></span>            | <span data-ttu-id="809fd-165">否</span><span class="sxs-lookup"><span data-stu-id="809fd-165">False</span></span>                                            |
| <span data-ttu-id="809fd-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="809fd-166">Is-Single-Valued</span></span>       | <span data-ttu-id="809fd-167">對</span><span class="sxs-lookup"><span data-stu-id="809fd-167">True</span></span>                                             |
| <span data-ttu-id="809fd-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="809fd-168">Is Indexed</span></span>             | <span data-ttu-id="809fd-169">否</span><span class="sxs-lookup"><span data-stu-id="809fd-169">False</span></span>                                            |
| <span data-ttu-id="809fd-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="809fd-170">In Global Catalog</span></span>      | <span data-ttu-id="809fd-171">否</span><span class="sxs-lookup"><span data-stu-id="809fd-171">False</span></span>                                            |
| <span data-ttu-id="809fd-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="809fd-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="809fd-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="809fd-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="809fd-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="809fd-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="809fd-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="809fd-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="809fd-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-176">Search-Flags</span></span>           | <span data-ttu-id="809fd-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="809fd-177">0x00000000</span></span>                                       |
| <span data-ttu-id="809fd-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-178">System-Flags</span></span>           | <span data-ttu-id="809fd-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="809fd-179">0x00000010</span></span>                                       |
| <span data-ttu-id="809fd-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="809fd-180">Classes used in</span></span>        | [<span data-ttu-id="809fd-181">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="809fd-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="809fd-182">亞當</span><span class="sxs-lookup"><span data-stu-id="809fd-182">ADAM</span></span>



| <span data-ttu-id="809fd-183">進入</span><span class="sxs-lookup"><span data-stu-id="809fd-183">Entry</span></span> | <span data-ttu-id="809fd-184">值</span><span class="sxs-lookup"><span data-stu-id="809fd-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="809fd-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="809fd-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="809fd-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="809fd-186">MAPI-Id</span></span>                | <span data-ttu-id="809fd-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="809fd-187">0x8145</span></span>                                           |
| <span data-ttu-id="809fd-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="809fd-188">System-Only</span></span>            | <span data-ttu-id="809fd-189">否</span><span class="sxs-lookup"><span data-stu-id="809fd-189">False</span></span>                                            |
| <span data-ttu-id="809fd-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="809fd-190">Is-Single-Valued</span></span>       | <span data-ttu-id="809fd-191">對</span><span class="sxs-lookup"><span data-stu-id="809fd-191">True</span></span>                                             |
| <span data-ttu-id="809fd-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="809fd-192">Is Indexed</span></span>             | <span data-ttu-id="809fd-193">否</span><span class="sxs-lookup"><span data-stu-id="809fd-193">False</span></span>                                            |
| <span data-ttu-id="809fd-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="809fd-194">In Global Catalog</span></span>      | <span data-ttu-id="809fd-195">否</span><span class="sxs-lookup"><span data-stu-id="809fd-195">False</span></span>                                            |
| <span data-ttu-id="809fd-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="809fd-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="809fd-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="809fd-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="809fd-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="809fd-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="809fd-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="809fd-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="809fd-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-200">Search-Flags</span></span>           | <span data-ttu-id="809fd-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="809fd-201">0x00000000</span></span>                                       |
| <span data-ttu-id="809fd-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-202">System-Flags</span></span>           | <span data-ttu-id="809fd-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="809fd-203">0x00000010</span></span>                                       |
| <span data-ttu-id="809fd-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="809fd-204">Classes used in</span></span>        | [<span data-ttu-id="809fd-205">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="809fd-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="809fd-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="809fd-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="809fd-207">進入</span><span class="sxs-lookup"><span data-stu-id="809fd-207">Entry</span></span> | <span data-ttu-id="809fd-208">值</span><span class="sxs-lookup"><span data-stu-id="809fd-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="809fd-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="809fd-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="809fd-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="809fd-210">MAPI-Id</span></span>                | <span data-ttu-id="809fd-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="809fd-211">0x8145</span></span>                                           |
| <span data-ttu-id="809fd-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="809fd-212">System-Only</span></span>            | <span data-ttu-id="809fd-213">否</span><span class="sxs-lookup"><span data-stu-id="809fd-213">False</span></span>                                            |
| <span data-ttu-id="809fd-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="809fd-214">Is-Single-Valued</span></span>       | <span data-ttu-id="809fd-215">對</span><span class="sxs-lookup"><span data-stu-id="809fd-215">True</span></span>                                             |
| <span data-ttu-id="809fd-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="809fd-216">Is Indexed</span></span>             | <span data-ttu-id="809fd-217">否</span><span class="sxs-lookup"><span data-stu-id="809fd-217">False</span></span>                                            |
| <span data-ttu-id="809fd-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="809fd-218">In Global Catalog</span></span>      | <span data-ttu-id="809fd-219">否</span><span class="sxs-lookup"><span data-stu-id="809fd-219">False</span></span>                                            |
| <span data-ttu-id="809fd-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="809fd-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="809fd-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="809fd-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="809fd-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="809fd-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="809fd-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="809fd-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="809fd-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-224">Search-Flags</span></span>           | <span data-ttu-id="809fd-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="809fd-225">0x00000000</span></span>                                       |
| <span data-ttu-id="809fd-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-226">System-Flags</span></span>           | <span data-ttu-id="809fd-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="809fd-227">0x00000010</span></span>                                       |
| <span data-ttu-id="809fd-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="809fd-228">Classes used in</span></span>        | [<span data-ttu-id="809fd-229">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="809fd-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="809fd-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="809fd-230">Windows Server 2008</span></span>



| <span data-ttu-id="809fd-231">進入</span><span class="sxs-lookup"><span data-stu-id="809fd-231">Entry</span></span> | <span data-ttu-id="809fd-232">值</span><span class="sxs-lookup"><span data-stu-id="809fd-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="809fd-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="809fd-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="809fd-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="809fd-234">MAPI-Id</span></span>                | <span data-ttu-id="809fd-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="809fd-235">0x8145</span></span>                                           |
| <span data-ttu-id="809fd-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="809fd-236">System-Only</span></span>            | <span data-ttu-id="809fd-237">否</span><span class="sxs-lookup"><span data-stu-id="809fd-237">False</span></span>                                            |
| <span data-ttu-id="809fd-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="809fd-238">Is-Single-Valued</span></span>       | <span data-ttu-id="809fd-239">對</span><span class="sxs-lookup"><span data-stu-id="809fd-239">True</span></span>                                             |
| <span data-ttu-id="809fd-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="809fd-240">Is Indexed</span></span>             | <span data-ttu-id="809fd-241">否</span><span class="sxs-lookup"><span data-stu-id="809fd-241">False</span></span>                                            |
| <span data-ttu-id="809fd-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="809fd-242">In Global Catalog</span></span>      | <span data-ttu-id="809fd-243">否</span><span class="sxs-lookup"><span data-stu-id="809fd-243">False</span></span>                                            |
| <span data-ttu-id="809fd-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="809fd-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="809fd-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="809fd-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="809fd-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="809fd-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="809fd-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="809fd-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="809fd-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-248">Search-Flags</span></span>           | <span data-ttu-id="809fd-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="809fd-249">0x00000000</span></span>                                       |
| <span data-ttu-id="809fd-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-250">System-Flags</span></span>           | <span data-ttu-id="809fd-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="809fd-251">0x00000010</span></span>                                       |
| <span data-ttu-id="809fd-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="809fd-252">Classes used in</span></span>        | [<span data-ttu-id="809fd-253">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="809fd-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="809fd-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="809fd-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="809fd-255">進入</span><span class="sxs-lookup"><span data-stu-id="809fd-255">Entry</span></span> | <span data-ttu-id="809fd-256">值</span><span class="sxs-lookup"><span data-stu-id="809fd-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="809fd-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="809fd-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="809fd-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="809fd-258">MAPI-Id</span></span>                | <span data-ttu-id="809fd-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="809fd-259">0x8145</span></span>                                           |
| <span data-ttu-id="809fd-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="809fd-260">System-Only</span></span>            | <span data-ttu-id="809fd-261">否</span><span class="sxs-lookup"><span data-stu-id="809fd-261">False</span></span>                                            |
| <span data-ttu-id="809fd-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="809fd-262">Is-Single-Valued</span></span>       | <span data-ttu-id="809fd-263">對</span><span class="sxs-lookup"><span data-stu-id="809fd-263">True</span></span>                                             |
| <span data-ttu-id="809fd-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="809fd-264">Is Indexed</span></span>             | <span data-ttu-id="809fd-265">否</span><span class="sxs-lookup"><span data-stu-id="809fd-265">False</span></span>                                            |
| <span data-ttu-id="809fd-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="809fd-266">In Global Catalog</span></span>      | <span data-ttu-id="809fd-267">否</span><span class="sxs-lookup"><span data-stu-id="809fd-267">False</span></span>                                            |
| <span data-ttu-id="809fd-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="809fd-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="809fd-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="809fd-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="809fd-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="809fd-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="809fd-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="809fd-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="809fd-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-272">Search-Flags</span></span>           | <span data-ttu-id="809fd-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="809fd-273">0x00000000</span></span>                                       |
| <span data-ttu-id="809fd-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-274">System-Flags</span></span>           | <span data-ttu-id="809fd-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="809fd-275">0x00000010</span></span>                                       |
| <span data-ttu-id="809fd-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="809fd-276">Classes used in</span></span>        | [<span data-ttu-id="809fd-277">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="809fd-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="809fd-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="809fd-278">Windows Server 2012</span></span>



| <span data-ttu-id="809fd-279">進入</span><span class="sxs-lookup"><span data-stu-id="809fd-279">Entry</span></span> | <span data-ttu-id="809fd-280">值</span><span class="sxs-lookup"><span data-stu-id="809fd-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="809fd-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="809fd-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="809fd-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="809fd-282">MAPI-Id</span></span>                | <span data-ttu-id="809fd-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="809fd-283">0x8145</span></span>                                           |
| <span data-ttu-id="809fd-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="809fd-284">System-Only</span></span>            | <span data-ttu-id="809fd-285">否</span><span class="sxs-lookup"><span data-stu-id="809fd-285">False</span></span>                                            |
| <span data-ttu-id="809fd-286">是-單一值</span><span class="sxs-lookup"><span data-stu-id="809fd-286">Is-Single-Valued</span></span>       | <span data-ttu-id="809fd-287">對</span><span class="sxs-lookup"><span data-stu-id="809fd-287">True</span></span>                                             |
| <span data-ttu-id="809fd-288">已編制索引</span><span class="sxs-lookup"><span data-stu-id="809fd-288">Is Indexed</span></span>             | <span data-ttu-id="809fd-289">否</span><span class="sxs-lookup"><span data-stu-id="809fd-289">False</span></span>                                            |
| <span data-ttu-id="809fd-290">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="809fd-290">In Global Catalog</span></span>      | <span data-ttu-id="809fd-291">否</span><span class="sxs-lookup"><span data-stu-id="809fd-291">False</span></span>                                            |
| <span data-ttu-id="809fd-292">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="809fd-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="809fd-293">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="809fd-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="809fd-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="809fd-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="809fd-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="809fd-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="809fd-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-296">Search-Flags</span></span>           | <span data-ttu-id="809fd-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="809fd-297">0x00000000</span></span>                                       |
| <span data-ttu-id="809fd-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="809fd-298">System-Flags</span></span>           | <span data-ttu-id="809fd-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="809fd-299">0x00000010</span></span>                                       |
| <span data-ttu-id="809fd-300">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="809fd-300">Classes used in</span></span>        | [<span data-ttu-id="809fd-301">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="809fd-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 






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
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="42d55-105">Tombstone-Lifetime 屬性</span><span class="sxs-lookup"><span data-stu-id="42d55-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="42d55-106">從目錄服務移除已刪除物件之前的天數。</span><span class="sxs-lookup"><span data-stu-id="42d55-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="42d55-107">這有助於從複寫的伺服器中移除物件，並防止還原重新介紹基於已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="42d55-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="42d55-108">此值位於 configuration NIC 的目錄服務物件中。</span><span class="sxs-lookup"><span data-stu-id="42d55-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="42d55-109">進入</span><span class="sxs-lookup"><span data-stu-id="42d55-109">Entry</span></span> | <span data-ttu-id="42d55-110">值</span><span class="sxs-lookup"><span data-stu-id="42d55-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="42d55-111">CN</span><span class="sxs-lookup"><span data-stu-id="42d55-111">CN</span></span>                | <span data-ttu-id="42d55-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="42d55-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="42d55-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="42d55-113">Ldap-Display-Name</span></span> | <span data-ttu-id="42d55-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="42d55-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="42d55-115">大小</span><span class="sxs-lookup"><span data-stu-id="42d55-115">Size</span></span>              | <span data-ttu-id="42d55-116">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="42d55-116">4 bytes.</span></span> <span data-ttu-id="42d55-117">未輸入任何值時，預設值為60天。</span><span class="sxs-lookup"><span data-stu-id="42d55-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="42d55-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="42d55-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="42d55-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="42d55-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="42d55-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="42d55-120">Attribute-Id</span></span>      | <span data-ttu-id="42d55-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="42d55-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="42d55-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="42d55-122">System-Id-Guid</span></span>    | <span data-ttu-id="42d55-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="42d55-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="42d55-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="42d55-124">Syntax</span></span>            | [<span data-ttu-id="42d55-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="42d55-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="42d55-126">實作</span><span class="sxs-lookup"><span data-stu-id="42d55-126">Implementations</span></span>

-   [<span data-ttu-id="42d55-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="42d55-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="42d55-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="42d55-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="42d55-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="42d55-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="42d55-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="42d55-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="42d55-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="42d55-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="42d55-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="42d55-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="42d55-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="42d55-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="42d55-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42d55-134">Windows 2000 Server</span></span>



| <span data-ttu-id="42d55-135">進入</span><span class="sxs-lookup"><span data-stu-id="42d55-135">Entry</span></span> | <span data-ttu-id="42d55-136">值</span><span class="sxs-lookup"><span data-stu-id="42d55-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42d55-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42d55-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42d55-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42d55-138">MAPI-Id</span></span>                | <span data-ttu-id="42d55-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="42d55-139">0x8145</span></span>                                           |
| <span data-ttu-id="42d55-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="42d55-140">System-Only</span></span>            | <span data-ttu-id="42d55-141">否</span><span class="sxs-lookup"><span data-stu-id="42d55-141">False</span></span>                                            |
| <span data-ttu-id="42d55-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42d55-142">Is-Single-Valued</span></span>       | <span data-ttu-id="42d55-143">對</span><span class="sxs-lookup"><span data-stu-id="42d55-143">True</span></span>                                             |
| <span data-ttu-id="42d55-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42d55-144">Is Indexed</span></span>             | <span data-ttu-id="42d55-145">否</span><span class="sxs-lookup"><span data-stu-id="42d55-145">False</span></span>                                            |
| <span data-ttu-id="42d55-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42d55-146">In Global Catalog</span></span>      | <span data-ttu-id="42d55-147">否</span><span class="sxs-lookup"><span data-stu-id="42d55-147">False</span></span>                                            |
| <span data-ttu-id="42d55-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42d55-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="42d55-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42d55-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42d55-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42d55-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42d55-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42d55-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42d55-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-152">Search-Flags</span></span>           | <span data-ttu-id="42d55-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42d55-153">0x00000000</span></span>                                       |
| <span data-ttu-id="42d55-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-154">System-Flags</span></span>           | <span data-ttu-id="42d55-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42d55-155">0x00000010</span></span>                                       |
| <span data-ttu-id="42d55-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42d55-156">Classes used in</span></span>        | [<span data-ttu-id="42d55-157">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="42d55-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="42d55-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42d55-158">Windows Server 2003</span></span>



| <span data-ttu-id="42d55-159">進入</span><span class="sxs-lookup"><span data-stu-id="42d55-159">Entry</span></span> | <span data-ttu-id="42d55-160">值</span><span class="sxs-lookup"><span data-stu-id="42d55-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42d55-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42d55-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42d55-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42d55-162">MAPI-Id</span></span>                | <span data-ttu-id="42d55-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="42d55-163">0x8145</span></span>                                           |
| <span data-ttu-id="42d55-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="42d55-164">System-Only</span></span>            | <span data-ttu-id="42d55-165">否</span><span class="sxs-lookup"><span data-stu-id="42d55-165">False</span></span>                                            |
| <span data-ttu-id="42d55-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42d55-166">Is-Single-Valued</span></span>       | <span data-ttu-id="42d55-167">對</span><span class="sxs-lookup"><span data-stu-id="42d55-167">True</span></span>                                             |
| <span data-ttu-id="42d55-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42d55-168">Is Indexed</span></span>             | <span data-ttu-id="42d55-169">否</span><span class="sxs-lookup"><span data-stu-id="42d55-169">False</span></span>                                            |
| <span data-ttu-id="42d55-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42d55-170">In Global Catalog</span></span>      | <span data-ttu-id="42d55-171">否</span><span class="sxs-lookup"><span data-stu-id="42d55-171">False</span></span>                                            |
| <span data-ttu-id="42d55-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42d55-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="42d55-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42d55-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42d55-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42d55-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42d55-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42d55-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42d55-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-176">Search-Flags</span></span>           | <span data-ttu-id="42d55-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42d55-177">0x00000000</span></span>                                       |
| <span data-ttu-id="42d55-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-178">System-Flags</span></span>           | <span data-ttu-id="42d55-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42d55-179">0x00000010</span></span>                                       |
| <span data-ttu-id="42d55-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42d55-180">Classes used in</span></span>        | [<span data-ttu-id="42d55-181">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="42d55-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="42d55-182">亞當</span><span class="sxs-lookup"><span data-stu-id="42d55-182">ADAM</span></span>



| <span data-ttu-id="42d55-183">進入</span><span class="sxs-lookup"><span data-stu-id="42d55-183">Entry</span></span> | <span data-ttu-id="42d55-184">值</span><span class="sxs-lookup"><span data-stu-id="42d55-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42d55-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42d55-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42d55-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42d55-186">MAPI-Id</span></span>                | <span data-ttu-id="42d55-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="42d55-187">0x8145</span></span>                                           |
| <span data-ttu-id="42d55-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="42d55-188">System-Only</span></span>            | <span data-ttu-id="42d55-189">否</span><span class="sxs-lookup"><span data-stu-id="42d55-189">False</span></span>                                            |
| <span data-ttu-id="42d55-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42d55-190">Is-Single-Valued</span></span>       | <span data-ttu-id="42d55-191">對</span><span class="sxs-lookup"><span data-stu-id="42d55-191">True</span></span>                                             |
| <span data-ttu-id="42d55-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42d55-192">Is Indexed</span></span>             | <span data-ttu-id="42d55-193">否</span><span class="sxs-lookup"><span data-stu-id="42d55-193">False</span></span>                                            |
| <span data-ttu-id="42d55-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42d55-194">In Global Catalog</span></span>      | <span data-ttu-id="42d55-195">否</span><span class="sxs-lookup"><span data-stu-id="42d55-195">False</span></span>                                            |
| <span data-ttu-id="42d55-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42d55-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="42d55-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42d55-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42d55-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42d55-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42d55-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42d55-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42d55-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-200">Search-Flags</span></span>           | <span data-ttu-id="42d55-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42d55-201">0x00000000</span></span>                                       |
| <span data-ttu-id="42d55-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-202">System-Flags</span></span>           | <span data-ttu-id="42d55-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42d55-203">0x00000010</span></span>                                       |
| <span data-ttu-id="42d55-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42d55-204">Classes used in</span></span>        | [<span data-ttu-id="42d55-205">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="42d55-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="42d55-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="42d55-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="42d55-207">進入</span><span class="sxs-lookup"><span data-stu-id="42d55-207">Entry</span></span> | <span data-ttu-id="42d55-208">值</span><span class="sxs-lookup"><span data-stu-id="42d55-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42d55-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42d55-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42d55-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42d55-210">MAPI-Id</span></span>                | <span data-ttu-id="42d55-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="42d55-211">0x8145</span></span>                                           |
| <span data-ttu-id="42d55-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="42d55-212">System-Only</span></span>            | <span data-ttu-id="42d55-213">否</span><span class="sxs-lookup"><span data-stu-id="42d55-213">False</span></span>                                            |
| <span data-ttu-id="42d55-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42d55-214">Is-Single-Valued</span></span>       | <span data-ttu-id="42d55-215">對</span><span class="sxs-lookup"><span data-stu-id="42d55-215">True</span></span>                                             |
| <span data-ttu-id="42d55-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42d55-216">Is Indexed</span></span>             | <span data-ttu-id="42d55-217">否</span><span class="sxs-lookup"><span data-stu-id="42d55-217">False</span></span>                                            |
| <span data-ttu-id="42d55-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42d55-218">In Global Catalog</span></span>      | <span data-ttu-id="42d55-219">否</span><span class="sxs-lookup"><span data-stu-id="42d55-219">False</span></span>                                            |
| <span data-ttu-id="42d55-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42d55-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="42d55-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42d55-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42d55-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42d55-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42d55-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42d55-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42d55-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-224">Search-Flags</span></span>           | <span data-ttu-id="42d55-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42d55-225">0x00000000</span></span>                                       |
| <span data-ttu-id="42d55-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-226">System-Flags</span></span>           | <span data-ttu-id="42d55-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42d55-227">0x00000010</span></span>                                       |
| <span data-ttu-id="42d55-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42d55-228">Classes used in</span></span>        | [<span data-ttu-id="42d55-229">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="42d55-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="42d55-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42d55-230">Windows Server 2008</span></span>



| <span data-ttu-id="42d55-231">進入</span><span class="sxs-lookup"><span data-stu-id="42d55-231">Entry</span></span> | <span data-ttu-id="42d55-232">值</span><span class="sxs-lookup"><span data-stu-id="42d55-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42d55-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42d55-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42d55-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42d55-234">MAPI-Id</span></span>                | <span data-ttu-id="42d55-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="42d55-235">0x8145</span></span>                                           |
| <span data-ttu-id="42d55-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="42d55-236">System-Only</span></span>            | <span data-ttu-id="42d55-237">否</span><span class="sxs-lookup"><span data-stu-id="42d55-237">False</span></span>                                            |
| <span data-ttu-id="42d55-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42d55-238">Is-Single-Valued</span></span>       | <span data-ttu-id="42d55-239">對</span><span class="sxs-lookup"><span data-stu-id="42d55-239">True</span></span>                                             |
| <span data-ttu-id="42d55-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42d55-240">Is Indexed</span></span>             | <span data-ttu-id="42d55-241">否</span><span class="sxs-lookup"><span data-stu-id="42d55-241">False</span></span>                                            |
| <span data-ttu-id="42d55-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42d55-242">In Global Catalog</span></span>      | <span data-ttu-id="42d55-243">否</span><span class="sxs-lookup"><span data-stu-id="42d55-243">False</span></span>                                            |
| <span data-ttu-id="42d55-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42d55-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="42d55-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42d55-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42d55-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42d55-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42d55-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42d55-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42d55-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-248">Search-Flags</span></span>           | <span data-ttu-id="42d55-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42d55-249">0x00000000</span></span>                                       |
| <span data-ttu-id="42d55-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-250">System-Flags</span></span>           | <span data-ttu-id="42d55-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42d55-251">0x00000010</span></span>                                       |
| <span data-ttu-id="42d55-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42d55-252">Classes used in</span></span>        | [<span data-ttu-id="42d55-253">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="42d55-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="42d55-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42d55-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="42d55-255">進入</span><span class="sxs-lookup"><span data-stu-id="42d55-255">Entry</span></span> | <span data-ttu-id="42d55-256">值</span><span class="sxs-lookup"><span data-stu-id="42d55-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42d55-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42d55-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42d55-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42d55-258">MAPI-Id</span></span>                | <span data-ttu-id="42d55-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="42d55-259">0x8145</span></span>                                           |
| <span data-ttu-id="42d55-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="42d55-260">System-Only</span></span>            | <span data-ttu-id="42d55-261">否</span><span class="sxs-lookup"><span data-stu-id="42d55-261">False</span></span>                                            |
| <span data-ttu-id="42d55-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42d55-262">Is-Single-Valued</span></span>       | <span data-ttu-id="42d55-263">對</span><span class="sxs-lookup"><span data-stu-id="42d55-263">True</span></span>                                             |
| <span data-ttu-id="42d55-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42d55-264">Is Indexed</span></span>             | <span data-ttu-id="42d55-265">否</span><span class="sxs-lookup"><span data-stu-id="42d55-265">False</span></span>                                            |
| <span data-ttu-id="42d55-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42d55-266">In Global Catalog</span></span>      | <span data-ttu-id="42d55-267">否</span><span class="sxs-lookup"><span data-stu-id="42d55-267">False</span></span>                                            |
| <span data-ttu-id="42d55-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42d55-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="42d55-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42d55-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42d55-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42d55-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42d55-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42d55-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42d55-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-272">Search-Flags</span></span>           | <span data-ttu-id="42d55-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42d55-273">0x00000000</span></span>                                       |
| <span data-ttu-id="42d55-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-274">System-Flags</span></span>           | <span data-ttu-id="42d55-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42d55-275">0x00000010</span></span>                                       |
| <span data-ttu-id="42d55-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42d55-276">Classes used in</span></span>        | [<span data-ttu-id="42d55-277">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="42d55-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="42d55-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42d55-278">Windows Server 2012</span></span>



| <span data-ttu-id="42d55-279">進入</span><span class="sxs-lookup"><span data-stu-id="42d55-279">Entry</span></span> | <span data-ttu-id="42d55-280">值</span><span class="sxs-lookup"><span data-stu-id="42d55-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42d55-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42d55-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42d55-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42d55-282">MAPI-Id</span></span>                | <span data-ttu-id="42d55-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="42d55-283">0x8145</span></span>                                           |
| <span data-ttu-id="42d55-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="42d55-284">System-Only</span></span>            | <span data-ttu-id="42d55-285">否</span><span class="sxs-lookup"><span data-stu-id="42d55-285">False</span></span>                                            |
| <span data-ttu-id="42d55-286">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42d55-286">Is-Single-Valued</span></span>       | <span data-ttu-id="42d55-287">對</span><span class="sxs-lookup"><span data-stu-id="42d55-287">True</span></span>                                             |
| <span data-ttu-id="42d55-288">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42d55-288">Is Indexed</span></span>             | <span data-ttu-id="42d55-289">否</span><span class="sxs-lookup"><span data-stu-id="42d55-289">False</span></span>                                            |
| <span data-ttu-id="42d55-290">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42d55-290">In Global Catalog</span></span>      | <span data-ttu-id="42d55-291">否</span><span class="sxs-lookup"><span data-stu-id="42d55-291">False</span></span>                                            |
| <span data-ttu-id="42d55-292">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42d55-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="42d55-293">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42d55-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42d55-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42d55-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42d55-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42d55-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42d55-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-296">Search-Flags</span></span>           | <span data-ttu-id="42d55-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42d55-297">0x00000000</span></span>                                       |
| <span data-ttu-id="42d55-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42d55-298">System-Flags</span></span>           | <span data-ttu-id="42d55-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42d55-299">0x00000010</span></span>                                       |
| <span data-ttu-id="42d55-300">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42d55-300">Classes used in</span></span>        | [<span data-ttu-id="42d55-301">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="42d55-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 






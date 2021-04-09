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
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="ec9dd-105">Tombstone-Lifetime 屬性</span><span class="sxs-lookup"><span data-stu-id="ec9dd-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="ec9dd-106">從目錄服務移除已刪除物件之前的天數。</span><span class="sxs-lookup"><span data-stu-id="ec9dd-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="ec9dd-107">這有助於從複寫的伺服器中移除物件，並防止還原重新介紹基於已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="ec9dd-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="ec9dd-108">此值位於 configuration NIC 的目錄服務物件中。</span><span class="sxs-lookup"><span data-stu-id="ec9dd-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="ec9dd-109">進入</span><span class="sxs-lookup"><span data-stu-id="ec9dd-109">Entry</span></span> | <span data-ttu-id="ec9dd-110">值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="ec9dd-111">CN</span><span class="sxs-lookup"><span data-stu-id="ec9dd-111">CN</span></span>                | <span data-ttu-id="ec9dd-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="ec9dd-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="ec9dd-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ec9dd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ec9dd-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="ec9dd-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="ec9dd-115">大小</span><span class="sxs-lookup"><span data-stu-id="ec9dd-115">Size</span></span>              | <span data-ttu-id="ec9dd-116">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="ec9dd-116">4 bytes.</span></span> <span data-ttu-id="ec9dd-117">未輸入任何值時，預設值為60天。</span><span class="sxs-lookup"><span data-stu-id="ec9dd-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="ec9dd-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ec9dd-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="ec9dd-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ec9dd-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="ec9dd-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec9dd-120">Attribute-Id</span></span>      | <span data-ttu-id="ec9dd-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="ec9dd-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="ec9dd-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ec9dd-122">System-Id-Guid</span></span>    | <span data-ttu-id="ec9dd-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="ec9dd-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="ec9dd-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec9dd-124">Syntax</span></span>            | [<span data-ttu-id="ec9dd-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="ec9dd-126">實作</span><span class="sxs-lookup"><span data-stu-id="ec9dd-126">Implementations</span></span>

-   [<span data-ttu-id="ec9dd-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec9dd-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec9dd-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ec9dd-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec9dd-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec9dd-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec9dd-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec9dd-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec9dd-134">Windows 2000 Server</span></span>



| <span data-ttu-id="ec9dd-135">進入</span><span class="sxs-lookup"><span data-stu-id="ec9dd-135">Entry</span></span> | <span data-ttu-id="ec9dd-136">值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ec9dd-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec9dd-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ec9dd-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec9dd-138">MAPI-Id</span></span>                | <span data-ttu-id="ec9dd-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="ec9dd-139">0x8145</span></span>                                           |
| <span data-ttu-id="ec9dd-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec9dd-140">System-Only</span></span>            | <span data-ttu-id="ec9dd-141">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-141">False</span></span>                                            |
| <span data-ttu-id="ec9dd-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-142">Is-Single-Valued</span></span>       | <span data-ttu-id="ec9dd-143">對</span><span class="sxs-lookup"><span data-stu-id="ec9dd-143">True</span></span>                                             |
| <span data-ttu-id="ec9dd-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec9dd-144">Is Indexed</span></span>             | <span data-ttu-id="ec9dd-145">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-145">False</span></span>                                            |
| <span data-ttu-id="ec9dd-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec9dd-146">In Global Catalog</span></span>      | <span data-ttu-id="ec9dd-147">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-147">False</span></span>                                            |
| <span data-ttu-id="ec9dd-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec9dd-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec9dd-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec9dd-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ec9dd-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec9dd-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec9dd-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-152">Search-Flags</span></span>           | <span data-ttu-id="ec9dd-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec9dd-153">0x00000000</span></span>                                       |
| <span data-ttu-id="ec9dd-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-154">System-Flags</span></span>           | <span data-ttu-id="ec9dd-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec9dd-155">0x00000010</span></span>                                       |
| <span data-ttu-id="ec9dd-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec9dd-156">Classes used in</span></span>        | [<span data-ttu-id="ec9dd-157">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec9dd-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec9dd-158">Windows Server 2003</span></span>



| <span data-ttu-id="ec9dd-159">進入</span><span class="sxs-lookup"><span data-stu-id="ec9dd-159">Entry</span></span> | <span data-ttu-id="ec9dd-160">值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ec9dd-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec9dd-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ec9dd-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec9dd-162">MAPI-Id</span></span>                | <span data-ttu-id="ec9dd-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="ec9dd-163">0x8145</span></span>                                           |
| <span data-ttu-id="ec9dd-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec9dd-164">System-Only</span></span>            | <span data-ttu-id="ec9dd-165">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-165">False</span></span>                                            |
| <span data-ttu-id="ec9dd-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-166">Is-Single-Valued</span></span>       | <span data-ttu-id="ec9dd-167">對</span><span class="sxs-lookup"><span data-stu-id="ec9dd-167">True</span></span>                                             |
| <span data-ttu-id="ec9dd-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec9dd-168">Is Indexed</span></span>             | <span data-ttu-id="ec9dd-169">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-169">False</span></span>                                            |
| <span data-ttu-id="ec9dd-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec9dd-170">In Global Catalog</span></span>      | <span data-ttu-id="ec9dd-171">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-171">False</span></span>                                            |
| <span data-ttu-id="ec9dd-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec9dd-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec9dd-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec9dd-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ec9dd-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec9dd-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec9dd-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-176">Search-Flags</span></span>           | <span data-ttu-id="ec9dd-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec9dd-177">0x00000000</span></span>                                       |
| <span data-ttu-id="ec9dd-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-178">System-Flags</span></span>           | <span data-ttu-id="ec9dd-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec9dd-179">0x00000010</span></span>                                       |
| <span data-ttu-id="ec9dd-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec9dd-180">Classes used in</span></span>        | [<span data-ttu-id="ec9dd-181">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ec9dd-182">亞當</span><span class="sxs-lookup"><span data-stu-id="ec9dd-182">ADAM</span></span>



| <span data-ttu-id="ec9dd-183">進入</span><span class="sxs-lookup"><span data-stu-id="ec9dd-183">Entry</span></span> | <span data-ttu-id="ec9dd-184">值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ec9dd-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec9dd-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ec9dd-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec9dd-186">MAPI-Id</span></span>                | <span data-ttu-id="ec9dd-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="ec9dd-187">0x8145</span></span>                                           |
| <span data-ttu-id="ec9dd-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec9dd-188">System-Only</span></span>            | <span data-ttu-id="ec9dd-189">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-189">False</span></span>                                            |
| <span data-ttu-id="ec9dd-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-190">Is-Single-Valued</span></span>       | <span data-ttu-id="ec9dd-191">對</span><span class="sxs-lookup"><span data-stu-id="ec9dd-191">True</span></span>                                             |
| <span data-ttu-id="ec9dd-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec9dd-192">Is Indexed</span></span>             | <span data-ttu-id="ec9dd-193">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-193">False</span></span>                                            |
| <span data-ttu-id="ec9dd-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec9dd-194">In Global Catalog</span></span>      | <span data-ttu-id="ec9dd-195">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-195">False</span></span>                                            |
| <span data-ttu-id="ec9dd-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec9dd-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec9dd-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec9dd-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ec9dd-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec9dd-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec9dd-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-200">Search-Flags</span></span>           | <span data-ttu-id="ec9dd-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec9dd-201">0x00000000</span></span>                                       |
| <span data-ttu-id="ec9dd-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-202">System-Flags</span></span>           | <span data-ttu-id="ec9dd-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec9dd-203">0x00000010</span></span>                                       |
| <span data-ttu-id="ec9dd-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec9dd-204">Classes used in</span></span>        | [<span data-ttu-id="ec9dd-205">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec9dd-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec9dd-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec9dd-207">進入</span><span class="sxs-lookup"><span data-stu-id="ec9dd-207">Entry</span></span> | <span data-ttu-id="ec9dd-208">值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ec9dd-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec9dd-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ec9dd-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec9dd-210">MAPI-Id</span></span>                | <span data-ttu-id="ec9dd-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="ec9dd-211">0x8145</span></span>                                           |
| <span data-ttu-id="ec9dd-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec9dd-212">System-Only</span></span>            | <span data-ttu-id="ec9dd-213">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-213">False</span></span>                                            |
| <span data-ttu-id="ec9dd-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-214">Is-Single-Valued</span></span>       | <span data-ttu-id="ec9dd-215">對</span><span class="sxs-lookup"><span data-stu-id="ec9dd-215">True</span></span>                                             |
| <span data-ttu-id="ec9dd-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec9dd-216">Is Indexed</span></span>             | <span data-ttu-id="ec9dd-217">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-217">False</span></span>                                            |
| <span data-ttu-id="ec9dd-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec9dd-218">In Global Catalog</span></span>      | <span data-ttu-id="ec9dd-219">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-219">False</span></span>                                            |
| <span data-ttu-id="ec9dd-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec9dd-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec9dd-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec9dd-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ec9dd-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec9dd-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec9dd-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-224">Search-Flags</span></span>           | <span data-ttu-id="ec9dd-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec9dd-225">0x00000000</span></span>                                       |
| <span data-ttu-id="ec9dd-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-226">System-Flags</span></span>           | <span data-ttu-id="ec9dd-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec9dd-227">0x00000010</span></span>                                       |
| <span data-ttu-id="ec9dd-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec9dd-228">Classes used in</span></span>        | [<span data-ttu-id="ec9dd-229">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec9dd-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec9dd-230">Windows Server 2008</span></span>



| <span data-ttu-id="ec9dd-231">進入</span><span class="sxs-lookup"><span data-stu-id="ec9dd-231">Entry</span></span> | <span data-ttu-id="ec9dd-232">值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ec9dd-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec9dd-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ec9dd-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec9dd-234">MAPI-Id</span></span>                | <span data-ttu-id="ec9dd-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="ec9dd-235">0x8145</span></span>                                           |
| <span data-ttu-id="ec9dd-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec9dd-236">System-Only</span></span>            | <span data-ttu-id="ec9dd-237">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-237">False</span></span>                                            |
| <span data-ttu-id="ec9dd-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-238">Is-Single-Valued</span></span>       | <span data-ttu-id="ec9dd-239">對</span><span class="sxs-lookup"><span data-stu-id="ec9dd-239">True</span></span>                                             |
| <span data-ttu-id="ec9dd-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec9dd-240">Is Indexed</span></span>             | <span data-ttu-id="ec9dd-241">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-241">False</span></span>                                            |
| <span data-ttu-id="ec9dd-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec9dd-242">In Global Catalog</span></span>      | <span data-ttu-id="ec9dd-243">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-243">False</span></span>                                            |
| <span data-ttu-id="ec9dd-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec9dd-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec9dd-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec9dd-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ec9dd-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec9dd-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec9dd-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-248">Search-Flags</span></span>           | <span data-ttu-id="ec9dd-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec9dd-249">0x00000000</span></span>                                       |
| <span data-ttu-id="ec9dd-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-250">System-Flags</span></span>           | <span data-ttu-id="ec9dd-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec9dd-251">0x00000010</span></span>                                       |
| <span data-ttu-id="ec9dd-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec9dd-252">Classes used in</span></span>        | [<span data-ttu-id="ec9dd-253">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec9dd-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec9dd-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec9dd-255">進入</span><span class="sxs-lookup"><span data-stu-id="ec9dd-255">Entry</span></span> | <span data-ttu-id="ec9dd-256">值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ec9dd-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec9dd-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ec9dd-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec9dd-258">MAPI-Id</span></span>                | <span data-ttu-id="ec9dd-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="ec9dd-259">0x8145</span></span>                                           |
| <span data-ttu-id="ec9dd-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec9dd-260">System-Only</span></span>            | <span data-ttu-id="ec9dd-261">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-261">False</span></span>                                            |
| <span data-ttu-id="ec9dd-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-262">Is-Single-Valued</span></span>       | <span data-ttu-id="ec9dd-263">對</span><span class="sxs-lookup"><span data-stu-id="ec9dd-263">True</span></span>                                             |
| <span data-ttu-id="ec9dd-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec9dd-264">Is Indexed</span></span>             | <span data-ttu-id="ec9dd-265">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-265">False</span></span>                                            |
| <span data-ttu-id="ec9dd-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec9dd-266">In Global Catalog</span></span>      | <span data-ttu-id="ec9dd-267">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-267">False</span></span>                                            |
| <span data-ttu-id="ec9dd-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec9dd-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec9dd-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec9dd-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ec9dd-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec9dd-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec9dd-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-272">Search-Flags</span></span>           | <span data-ttu-id="ec9dd-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec9dd-273">0x00000000</span></span>                                       |
| <span data-ttu-id="ec9dd-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-274">System-Flags</span></span>           | <span data-ttu-id="ec9dd-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec9dd-275">0x00000010</span></span>                                       |
| <span data-ttu-id="ec9dd-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec9dd-276">Classes used in</span></span>        | [<span data-ttu-id="ec9dd-277">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec9dd-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec9dd-278">Windows Server 2012</span></span>



| <span data-ttu-id="ec9dd-279">進入</span><span class="sxs-lookup"><span data-stu-id="ec9dd-279">Entry</span></span> | <span data-ttu-id="ec9dd-280">值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ec9dd-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec9dd-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ec9dd-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec9dd-282">MAPI-Id</span></span>                | <span data-ttu-id="ec9dd-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="ec9dd-283">0x8145</span></span>                                           |
| <span data-ttu-id="ec9dd-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec9dd-284">System-Only</span></span>            | <span data-ttu-id="ec9dd-285">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-285">False</span></span>                                            |
| <span data-ttu-id="ec9dd-286">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec9dd-286">Is-Single-Valued</span></span>       | <span data-ttu-id="ec9dd-287">對</span><span class="sxs-lookup"><span data-stu-id="ec9dd-287">True</span></span>                                             |
| <span data-ttu-id="ec9dd-288">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec9dd-288">Is Indexed</span></span>             | <span data-ttu-id="ec9dd-289">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-289">False</span></span>                                            |
| <span data-ttu-id="ec9dd-290">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec9dd-290">In Global Catalog</span></span>      | <span data-ttu-id="ec9dd-291">否</span><span class="sxs-lookup"><span data-stu-id="ec9dd-291">False</span></span>                                            |
| <span data-ttu-id="ec9dd-292">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec9dd-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec9dd-293">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec9dd-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ec9dd-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec9dd-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec9dd-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ec9dd-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-296">Search-Flags</span></span>           | <span data-ttu-id="ec9dd-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec9dd-297">0x00000000</span></span>                                       |
| <span data-ttu-id="ec9dd-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec9dd-298">System-Flags</span></span>           | <span data-ttu-id="ec9dd-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec9dd-299">0x00000010</span></span>                                       |
| <span data-ttu-id="ec9dd-300">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec9dd-300">Classes used in</span></span>        | [<span data-ttu-id="ec9dd-301">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="ec9dd-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 






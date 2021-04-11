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
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="75c3b-105">Tombstone-Lifetime 屬性</span><span class="sxs-lookup"><span data-stu-id="75c3b-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="75c3b-106">從目錄服務移除已刪除物件之前的天數。</span><span class="sxs-lookup"><span data-stu-id="75c3b-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="75c3b-107">這有助於從複寫的伺服器中移除物件，並防止還原重新介紹基於已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="75c3b-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="75c3b-108">此值位於 configuration NIC 的目錄服務物件中。</span><span class="sxs-lookup"><span data-stu-id="75c3b-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="75c3b-109">進入</span><span class="sxs-lookup"><span data-stu-id="75c3b-109">Entry</span></span> | <span data-ttu-id="75c3b-110">值</span><span class="sxs-lookup"><span data-stu-id="75c3b-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="75c3b-111">CN</span><span class="sxs-lookup"><span data-stu-id="75c3b-111">CN</span></span>                | <span data-ttu-id="75c3b-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="75c3b-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="75c3b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="75c3b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="75c3b-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="75c3b-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="75c3b-115">大小</span><span class="sxs-lookup"><span data-stu-id="75c3b-115">Size</span></span>              | <span data-ttu-id="75c3b-116">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="75c3b-116">4 bytes.</span></span> <span data-ttu-id="75c3b-117">未輸入任何值時，預設值為60天。</span><span class="sxs-lookup"><span data-stu-id="75c3b-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="75c3b-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="75c3b-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="75c3b-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="75c3b-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="75c3b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="75c3b-120">Attribute-Id</span></span>      | <span data-ttu-id="75c3b-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="75c3b-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="75c3b-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="75c3b-122">System-Id-Guid</span></span>    | <span data-ttu-id="75c3b-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="75c3b-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="75c3b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="75c3b-124">Syntax</span></span>            | [<span data-ttu-id="75c3b-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="75c3b-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="75c3b-126">實作</span><span class="sxs-lookup"><span data-stu-id="75c3b-126">Implementations</span></span>

-   [<span data-ttu-id="75c3b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="75c3b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="75c3b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="75c3b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="75c3b-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="75c3b-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="75c3b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="75c3b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="75c3b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="75c3b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="75c3b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="75c3b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="75c3b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="75c3b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="75c3b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75c3b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="75c3b-135">進入</span><span class="sxs-lookup"><span data-stu-id="75c3b-135">Entry</span></span> | <span data-ttu-id="75c3b-136">值</span><span class="sxs-lookup"><span data-stu-id="75c3b-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="75c3b-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75c3b-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="75c3b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c3b-138">MAPI-Id</span></span>                | <span data-ttu-id="75c3b-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="75c3b-139">0x8145</span></span>                                           |
| <span data-ttu-id="75c3b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c3b-140">System-Only</span></span>            | <span data-ttu-id="75c3b-141">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-141">False</span></span>                                            |
| <span data-ttu-id="75c3b-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75c3b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="75c3b-143">對</span><span class="sxs-lookup"><span data-stu-id="75c3b-143">True</span></span>                                             |
| <span data-ttu-id="75c3b-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75c3b-144">Is Indexed</span></span>             | <span data-ttu-id="75c3b-145">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-145">False</span></span>                                            |
| <span data-ttu-id="75c3b-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75c3b-146">In Global Catalog</span></span>      | <span data-ttu-id="75c3b-147">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-147">False</span></span>                                            |
| <span data-ttu-id="75c3b-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75c3b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c3b-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75c3b-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="75c3b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c3b-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c3b-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-152">Search-Flags</span></span>           | <span data-ttu-id="75c3b-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c3b-153">0x00000000</span></span>                                       |
| <span data-ttu-id="75c3b-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-154">System-Flags</span></span>           | <span data-ttu-id="75c3b-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c3b-155">0x00000010</span></span>                                       |
| <span data-ttu-id="75c3b-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75c3b-156">Classes used in</span></span>        | [<span data-ttu-id="75c3b-157">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="75c3b-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="75c3b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75c3b-158">Windows Server 2003</span></span>



| <span data-ttu-id="75c3b-159">進入</span><span class="sxs-lookup"><span data-stu-id="75c3b-159">Entry</span></span> | <span data-ttu-id="75c3b-160">值</span><span class="sxs-lookup"><span data-stu-id="75c3b-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="75c3b-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75c3b-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="75c3b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c3b-162">MAPI-Id</span></span>                | <span data-ttu-id="75c3b-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="75c3b-163">0x8145</span></span>                                           |
| <span data-ttu-id="75c3b-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c3b-164">System-Only</span></span>            | <span data-ttu-id="75c3b-165">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-165">False</span></span>                                            |
| <span data-ttu-id="75c3b-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75c3b-166">Is-Single-Valued</span></span>       | <span data-ttu-id="75c3b-167">對</span><span class="sxs-lookup"><span data-stu-id="75c3b-167">True</span></span>                                             |
| <span data-ttu-id="75c3b-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75c3b-168">Is Indexed</span></span>             | <span data-ttu-id="75c3b-169">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-169">False</span></span>                                            |
| <span data-ttu-id="75c3b-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75c3b-170">In Global Catalog</span></span>      | <span data-ttu-id="75c3b-171">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-171">False</span></span>                                            |
| <span data-ttu-id="75c3b-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75c3b-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c3b-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75c3b-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="75c3b-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c3b-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c3b-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-176">Search-Flags</span></span>           | <span data-ttu-id="75c3b-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c3b-177">0x00000000</span></span>                                       |
| <span data-ttu-id="75c3b-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-178">System-Flags</span></span>           | <span data-ttu-id="75c3b-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c3b-179">0x00000010</span></span>                                       |
| <span data-ttu-id="75c3b-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75c3b-180">Classes used in</span></span>        | [<span data-ttu-id="75c3b-181">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="75c3b-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="75c3b-182">亞當</span><span class="sxs-lookup"><span data-stu-id="75c3b-182">ADAM</span></span>



| <span data-ttu-id="75c3b-183">進入</span><span class="sxs-lookup"><span data-stu-id="75c3b-183">Entry</span></span> | <span data-ttu-id="75c3b-184">值</span><span class="sxs-lookup"><span data-stu-id="75c3b-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="75c3b-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75c3b-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="75c3b-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c3b-186">MAPI-Id</span></span>                | <span data-ttu-id="75c3b-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="75c3b-187">0x8145</span></span>                                           |
| <span data-ttu-id="75c3b-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c3b-188">System-Only</span></span>            | <span data-ttu-id="75c3b-189">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-189">False</span></span>                                            |
| <span data-ttu-id="75c3b-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75c3b-190">Is-Single-Valued</span></span>       | <span data-ttu-id="75c3b-191">對</span><span class="sxs-lookup"><span data-stu-id="75c3b-191">True</span></span>                                             |
| <span data-ttu-id="75c3b-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75c3b-192">Is Indexed</span></span>             | <span data-ttu-id="75c3b-193">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-193">False</span></span>                                            |
| <span data-ttu-id="75c3b-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75c3b-194">In Global Catalog</span></span>      | <span data-ttu-id="75c3b-195">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-195">False</span></span>                                            |
| <span data-ttu-id="75c3b-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75c3b-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c3b-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75c3b-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="75c3b-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c3b-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c3b-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-200">Search-Flags</span></span>           | <span data-ttu-id="75c3b-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c3b-201">0x00000000</span></span>                                       |
| <span data-ttu-id="75c3b-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-202">System-Flags</span></span>           | <span data-ttu-id="75c3b-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c3b-203">0x00000010</span></span>                                       |
| <span data-ttu-id="75c3b-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75c3b-204">Classes used in</span></span>        | [<span data-ttu-id="75c3b-205">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="75c3b-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="75c3b-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="75c3b-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="75c3b-207">進入</span><span class="sxs-lookup"><span data-stu-id="75c3b-207">Entry</span></span> | <span data-ttu-id="75c3b-208">值</span><span class="sxs-lookup"><span data-stu-id="75c3b-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="75c3b-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75c3b-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="75c3b-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c3b-210">MAPI-Id</span></span>                | <span data-ttu-id="75c3b-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="75c3b-211">0x8145</span></span>                                           |
| <span data-ttu-id="75c3b-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c3b-212">System-Only</span></span>            | <span data-ttu-id="75c3b-213">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-213">False</span></span>                                            |
| <span data-ttu-id="75c3b-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75c3b-214">Is-Single-Valued</span></span>       | <span data-ttu-id="75c3b-215">對</span><span class="sxs-lookup"><span data-stu-id="75c3b-215">True</span></span>                                             |
| <span data-ttu-id="75c3b-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75c3b-216">Is Indexed</span></span>             | <span data-ttu-id="75c3b-217">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-217">False</span></span>                                            |
| <span data-ttu-id="75c3b-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75c3b-218">In Global Catalog</span></span>      | <span data-ttu-id="75c3b-219">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-219">False</span></span>                                            |
| <span data-ttu-id="75c3b-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75c3b-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c3b-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75c3b-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="75c3b-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c3b-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c3b-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-224">Search-Flags</span></span>           | <span data-ttu-id="75c3b-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c3b-225">0x00000000</span></span>                                       |
| <span data-ttu-id="75c3b-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-226">System-Flags</span></span>           | <span data-ttu-id="75c3b-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c3b-227">0x00000010</span></span>                                       |
| <span data-ttu-id="75c3b-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75c3b-228">Classes used in</span></span>        | [<span data-ttu-id="75c3b-229">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="75c3b-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="75c3b-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75c3b-230">Windows Server 2008</span></span>



| <span data-ttu-id="75c3b-231">進入</span><span class="sxs-lookup"><span data-stu-id="75c3b-231">Entry</span></span> | <span data-ttu-id="75c3b-232">值</span><span class="sxs-lookup"><span data-stu-id="75c3b-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="75c3b-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75c3b-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="75c3b-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c3b-234">MAPI-Id</span></span>                | <span data-ttu-id="75c3b-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="75c3b-235">0x8145</span></span>                                           |
| <span data-ttu-id="75c3b-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c3b-236">System-Only</span></span>            | <span data-ttu-id="75c3b-237">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-237">False</span></span>                                            |
| <span data-ttu-id="75c3b-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75c3b-238">Is-Single-Valued</span></span>       | <span data-ttu-id="75c3b-239">對</span><span class="sxs-lookup"><span data-stu-id="75c3b-239">True</span></span>                                             |
| <span data-ttu-id="75c3b-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75c3b-240">Is Indexed</span></span>             | <span data-ttu-id="75c3b-241">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-241">False</span></span>                                            |
| <span data-ttu-id="75c3b-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75c3b-242">In Global Catalog</span></span>      | <span data-ttu-id="75c3b-243">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-243">False</span></span>                                            |
| <span data-ttu-id="75c3b-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75c3b-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c3b-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75c3b-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="75c3b-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c3b-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c3b-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-248">Search-Flags</span></span>           | <span data-ttu-id="75c3b-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c3b-249">0x00000000</span></span>                                       |
| <span data-ttu-id="75c3b-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-250">System-Flags</span></span>           | <span data-ttu-id="75c3b-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c3b-251">0x00000010</span></span>                                       |
| <span data-ttu-id="75c3b-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75c3b-252">Classes used in</span></span>        | [<span data-ttu-id="75c3b-253">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="75c3b-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="75c3b-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75c3b-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="75c3b-255">進入</span><span class="sxs-lookup"><span data-stu-id="75c3b-255">Entry</span></span> | <span data-ttu-id="75c3b-256">值</span><span class="sxs-lookup"><span data-stu-id="75c3b-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="75c3b-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75c3b-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="75c3b-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c3b-258">MAPI-Id</span></span>                | <span data-ttu-id="75c3b-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="75c3b-259">0x8145</span></span>                                           |
| <span data-ttu-id="75c3b-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c3b-260">System-Only</span></span>            | <span data-ttu-id="75c3b-261">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-261">False</span></span>                                            |
| <span data-ttu-id="75c3b-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75c3b-262">Is-Single-Valued</span></span>       | <span data-ttu-id="75c3b-263">對</span><span class="sxs-lookup"><span data-stu-id="75c3b-263">True</span></span>                                             |
| <span data-ttu-id="75c3b-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75c3b-264">Is Indexed</span></span>             | <span data-ttu-id="75c3b-265">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-265">False</span></span>                                            |
| <span data-ttu-id="75c3b-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75c3b-266">In Global Catalog</span></span>      | <span data-ttu-id="75c3b-267">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-267">False</span></span>                                            |
| <span data-ttu-id="75c3b-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75c3b-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c3b-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75c3b-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="75c3b-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c3b-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c3b-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-272">Search-Flags</span></span>           | <span data-ttu-id="75c3b-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c3b-273">0x00000000</span></span>                                       |
| <span data-ttu-id="75c3b-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-274">System-Flags</span></span>           | <span data-ttu-id="75c3b-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c3b-275">0x00000010</span></span>                                       |
| <span data-ttu-id="75c3b-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75c3b-276">Classes used in</span></span>        | [<span data-ttu-id="75c3b-277">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="75c3b-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="75c3b-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75c3b-278">Windows Server 2012</span></span>



| <span data-ttu-id="75c3b-279">進入</span><span class="sxs-lookup"><span data-stu-id="75c3b-279">Entry</span></span> | <span data-ttu-id="75c3b-280">值</span><span class="sxs-lookup"><span data-stu-id="75c3b-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="75c3b-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75c3b-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="75c3b-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c3b-282">MAPI-Id</span></span>                | <span data-ttu-id="75c3b-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="75c3b-283">0x8145</span></span>                                           |
| <span data-ttu-id="75c3b-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c3b-284">System-Only</span></span>            | <span data-ttu-id="75c3b-285">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-285">False</span></span>                                            |
| <span data-ttu-id="75c3b-286">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75c3b-286">Is-Single-Valued</span></span>       | <span data-ttu-id="75c3b-287">對</span><span class="sxs-lookup"><span data-stu-id="75c3b-287">True</span></span>                                             |
| <span data-ttu-id="75c3b-288">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75c3b-288">Is Indexed</span></span>             | <span data-ttu-id="75c3b-289">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-289">False</span></span>                                            |
| <span data-ttu-id="75c3b-290">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75c3b-290">In Global Catalog</span></span>      | <span data-ttu-id="75c3b-291">否</span><span class="sxs-lookup"><span data-stu-id="75c3b-291">False</span></span>                                            |
| <span data-ttu-id="75c3b-292">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75c3b-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c3b-293">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75c3b-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="75c3b-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c3b-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c3b-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="75c3b-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-296">Search-Flags</span></span>           | <span data-ttu-id="75c3b-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c3b-297">0x00000000</span></span>                                       |
| <span data-ttu-id="75c3b-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c3b-298">System-Flags</span></span>           | <span data-ttu-id="75c3b-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c3b-299">0x00000010</span></span>                                       |
| <span data-ttu-id="75c3b-300">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75c3b-300">Classes used in</span></span>        | [<span data-ttu-id="75c3b-301">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="75c3b-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 






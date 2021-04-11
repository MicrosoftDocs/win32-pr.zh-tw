---
title: ms DS-複寫-通知-第一個-DSA-延遲屬性
description: 這個屬性會控制對 DS 的變更之間的延遲時間，以及 NC 第一個複本夥伴的通知。
ms.assetid: 58474bf9-9069-402a-a94b-4d1b6df0810e
ms.tgt_platform: multiple
keywords:
- ms DS-複寫-通知-第一個-DSA-延遲屬性 AD 架構
- 複寫-通知-第一個-DSA-延遲屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Replication-Notify-First-DSA-Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a981ff257562e701b12e3855b279b7995721e39
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845132"
---
# <a name="ms-ds-replication-notify-first-dsa-delay-attribute"></a><span data-ttu-id="e384b-105">ms DS-複寫-通知-第一個-DSA-延遲屬性</span><span class="sxs-lookup"><span data-stu-id="e384b-105">ms-DS-Replication-Notify-First-DSA-Delay attribute</span></span>

<span data-ttu-id="e384b-106">這個屬性會控制對 DS 的變更之間的延遲時間，以及 NC 第一個複本夥伴的通知。</span><span class="sxs-lookup"><span data-stu-id="e384b-106">This attribute controls the delay in time between changes to the DS, and notification of the first replica partner for an NC.</span></span>



| <span data-ttu-id="e384b-107">進入</span><span class="sxs-lookup"><span data-stu-id="e384b-107">Entry</span></span> | <span data-ttu-id="e384b-108">值</span><span class="sxs-lookup"><span data-stu-id="e384b-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="e384b-109">CN</span><span class="sxs-lookup"><span data-stu-id="e384b-109">CN</span></span>                | <span data-ttu-id="e384b-110">ms DS-複寫-通知-第一個-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="e384b-110">ms-DS-Replication-Notify-First-DSA-Delay</span></span> |
| <span data-ttu-id="e384b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e384b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e384b-112">複寫-通知-第一個-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="e384b-112">msDS-Replication-Notify-First-DSA-Delay</span></span>  |
| <span data-ttu-id="e384b-113">大小</span><span class="sxs-lookup"><span data-stu-id="e384b-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="e384b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e384b-114">Update Privilege</span></span>  | <span data-ttu-id="e384b-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="e384b-115">This value is set by the system.</span></span>         |
| <span data-ttu-id="e384b-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e384b-116">Update Frequency</span></span>  | \-                                       |
| <span data-ttu-id="e384b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e384b-117">Attribute-Id</span></span>      | <span data-ttu-id="e384b-118">1.2.840.113556.1.4.1663</span><span class="sxs-lookup"><span data-stu-id="e384b-118">1.2.840.113556.1.4.1663</span></span>                  |
| <span data-ttu-id="e384b-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e384b-119">System-Id-Guid</span></span>    | <span data-ttu-id="e384b-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span><span class="sxs-lookup"><span data-stu-id="e384b-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span></span>     |
| <span data-ttu-id="e384b-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e384b-121">Syntax</span></span>            | [<span data-ttu-id="e384b-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="e384b-122">**Enumeration**</span></span>](s-enumeration.md)     |



## <a name="implementations"></a><span data-ttu-id="e384b-123">實作</span><span class="sxs-lookup"><span data-stu-id="e384b-123">Implementations</span></span>

-   [<span data-ttu-id="e384b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e384b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e384b-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e384b-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e384b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e384b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e384b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e384b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e384b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e384b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e384b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e384b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e384b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e384b-130">Windows Server 2003</span></span>



| <span data-ttu-id="e384b-131">進入</span><span class="sxs-lookup"><span data-stu-id="e384b-131">Entry</span></span> | <span data-ttu-id="e384b-132">值</span><span class="sxs-lookup"><span data-stu-id="e384b-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e384b-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e384b-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e384b-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e384b-135">System-Only</span></span>            | <span data-ttu-id="e384b-136">否</span><span class="sxs-lookup"><span data-stu-id="e384b-136">False</span></span>                                      |
| <span data-ttu-id="e384b-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e384b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e384b-138">對</span><span class="sxs-lookup"><span data-stu-id="e384b-138">True</span></span>                                       |
| <span data-ttu-id="e384b-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e384b-139">Is Indexed</span></span>             | <span data-ttu-id="e384b-140">否</span><span class="sxs-lookup"><span data-stu-id="e384b-140">False</span></span>                                      |
| <span data-ttu-id="e384b-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e384b-141">In Global Catalog</span></span>      | <span data-ttu-id="e384b-142">否</span><span class="sxs-lookup"><span data-stu-id="e384b-142">False</span></span>                                      |
| <span data-ttu-id="e384b-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e384b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e384b-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e384b-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e384b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e384b-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e384b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e384b-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e384b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-147">Search-Flags</span></span>           | <span data-ttu-id="e384b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e384b-148">0x00000000</span></span>                                 |
| <span data-ttu-id="e384b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-149">System-Flags</span></span>           | <span data-ttu-id="e384b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e384b-150">0x00000010</span></span>                                 |
| <span data-ttu-id="e384b-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e384b-151">Classes used in</span></span>        | [<span data-ttu-id="e384b-152">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e384b-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e384b-153">亞當</span><span class="sxs-lookup"><span data-stu-id="e384b-153">ADAM</span></span>



| <span data-ttu-id="e384b-154">進入</span><span class="sxs-lookup"><span data-stu-id="e384b-154">Entry</span></span> | <span data-ttu-id="e384b-155">值</span><span class="sxs-lookup"><span data-stu-id="e384b-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e384b-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e384b-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e384b-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e384b-158">System-Only</span></span>            | <span data-ttu-id="e384b-159">否</span><span class="sxs-lookup"><span data-stu-id="e384b-159">False</span></span>                                      |
| <span data-ttu-id="e384b-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e384b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e384b-161">對</span><span class="sxs-lookup"><span data-stu-id="e384b-161">True</span></span>                                       |
| <span data-ttu-id="e384b-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e384b-162">Is Indexed</span></span>             | <span data-ttu-id="e384b-163">否</span><span class="sxs-lookup"><span data-stu-id="e384b-163">False</span></span>                                      |
| <span data-ttu-id="e384b-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e384b-164">In Global Catalog</span></span>      | <span data-ttu-id="e384b-165">否</span><span class="sxs-lookup"><span data-stu-id="e384b-165">False</span></span>                                      |
| <span data-ttu-id="e384b-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e384b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e384b-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e384b-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e384b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e384b-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e384b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e384b-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e384b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-170">Search-Flags</span></span>           | <span data-ttu-id="e384b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e384b-171">0x00000000</span></span>                                 |
| <span data-ttu-id="e384b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-172">System-Flags</span></span>           | <span data-ttu-id="e384b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e384b-173">0x00000010</span></span>                                 |
| <span data-ttu-id="e384b-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e384b-174">Classes used in</span></span>        | [<span data-ttu-id="e384b-175">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e384b-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e384b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e384b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e384b-177">進入</span><span class="sxs-lookup"><span data-stu-id="e384b-177">Entry</span></span> | <span data-ttu-id="e384b-178">值</span><span class="sxs-lookup"><span data-stu-id="e384b-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e384b-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e384b-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e384b-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e384b-181">System-Only</span></span>            | <span data-ttu-id="e384b-182">否</span><span class="sxs-lookup"><span data-stu-id="e384b-182">False</span></span>                                      |
| <span data-ttu-id="e384b-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e384b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e384b-184">對</span><span class="sxs-lookup"><span data-stu-id="e384b-184">True</span></span>                                       |
| <span data-ttu-id="e384b-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e384b-185">Is Indexed</span></span>             | <span data-ttu-id="e384b-186">否</span><span class="sxs-lookup"><span data-stu-id="e384b-186">False</span></span>                                      |
| <span data-ttu-id="e384b-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e384b-187">In Global Catalog</span></span>      | <span data-ttu-id="e384b-188">否</span><span class="sxs-lookup"><span data-stu-id="e384b-188">False</span></span>                                      |
| <span data-ttu-id="e384b-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e384b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e384b-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e384b-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e384b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e384b-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e384b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e384b-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e384b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-193">Search-Flags</span></span>           | <span data-ttu-id="e384b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e384b-194">0x00000000</span></span>                                 |
| <span data-ttu-id="e384b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-195">System-Flags</span></span>           | <span data-ttu-id="e384b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e384b-196">0x00000010</span></span>                                 |
| <span data-ttu-id="e384b-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e384b-197">Classes used in</span></span>        | [<span data-ttu-id="e384b-198">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e384b-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e384b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e384b-199">Windows Server 2008</span></span>



| <span data-ttu-id="e384b-200">進入</span><span class="sxs-lookup"><span data-stu-id="e384b-200">Entry</span></span> | <span data-ttu-id="e384b-201">值</span><span class="sxs-lookup"><span data-stu-id="e384b-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e384b-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e384b-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e384b-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e384b-204">System-Only</span></span>            | <span data-ttu-id="e384b-205">否</span><span class="sxs-lookup"><span data-stu-id="e384b-205">False</span></span>                                      |
| <span data-ttu-id="e384b-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e384b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e384b-207">對</span><span class="sxs-lookup"><span data-stu-id="e384b-207">True</span></span>                                       |
| <span data-ttu-id="e384b-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e384b-208">Is Indexed</span></span>             | <span data-ttu-id="e384b-209">否</span><span class="sxs-lookup"><span data-stu-id="e384b-209">False</span></span>                                      |
| <span data-ttu-id="e384b-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e384b-210">In Global Catalog</span></span>      | <span data-ttu-id="e384b-211">否</span><span class="sxs-lookup"><span data-stu-id="e384b-211">False</span></span>                                      |
| <span data-ttu-id="e384b-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e384b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e384b-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e384b-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e384b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e384b-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e384b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e384b-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e384b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-216">Search-Flags</span></span>           | <span data-ttu-id="e384b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e384b-217">0x00000000</span></span>                                 |
| <span data-ttu-id="e384b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-218">System-Flags</span></span>           | <span data-ttu-id="e384b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e384b-219">0x00000010</span></span>                                 |
| <span data-ttu-id="e384b-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e384b-220">Classes used in</span></span>        | [<span data-ttu-id="e384b-221">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e384b-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e384b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e384b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e384b-223">進入</span><span class="sxs-lookup"><span data-stu-id="e384b-223">Entry</span></span> | <span data-ttu-id="e384b-224">值</span><span class="sxs-lookup"><span data-stu-id="e384b-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e384b-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e384b-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e384b-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e384b-227">System-Only</span></span>            | <span data-ttu-id="e384b-228">否</span><span class="sxs-lookup"><span data-stu-id="e384b-228">False</span></span>                                      |
| <span data-ttu-id="e384b-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e384b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e384b-230">對</span><span class="sxs-lookup"><span data-stu-id="e384b-230">True</span></span>                                       |
| <span data-ttu-id="e384b-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e384b-231">Is Indexed</span></span>             | <span data-ttu-id="e384b-232">否</span><span class="sxs-lookup"><span data-stu-id="e384b-232">False</span></span>                                      |
| <span data-ttu-id="e384b-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e384b-233">In Global Catalog</span></span>      | <span data-ttu-id="e384b-234">否</span><span class="sxs-lookup"><span data-stu-id="e384b-234">False</span></span>                                      |
| <span data-ttu-id="e384b-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e384b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e384b-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e384b-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e384b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e384b-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e384b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e384b-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e384b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-239">Search-Flags</span></span>           | <span data-ttu-id="e384b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e384b-240">0x00000000</span></span>                                 |
| <span data-ttu-id="e384b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-241">System-Flags</span></span>           | <span data-ttu-id="e384b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e384b-242">0x00000010</span></span>                                 |
| <span data-ttu-id="e384b-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e384b-243">Classes used in</span></span>        | [<span data-ttu-id="e384b-244">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e384b-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e384b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e384b-245">Windows Server 2012</span></span>



| <span data-ttu-id="e384b-246">進入</span><span class="sxs-lookup"><span data-stu-id="e384b-246">Entry</span></span> | <span data-ttu-id="e384b-247">值</span><span class="sxs-lookup"><span data-stu-id="e384b-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e384b-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e384b-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e384b-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e384b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e384b-250">System-Only</span></span>            | <span data-ttu-id="e384b-251">否</span><span class="sxs-lookup"><span data-stu-id="e384b-251">False</span></span>                                      |
| <span data-ttu-id="e384b-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e384b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e384b-253">對</span><span class="sxs-lookup"><span data-stu-id="e384b-253">True</span></span>                                       |
| <span data-ttu-id="e384b-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e384b-254">Is Indexed</span></span>             | <span data-ttu-id="e384b-255">否</span><span class="sxs-lookup"><span data-stu-id="e384b-255">False</span></span>                                      |
| <span data-ttu-id="e384b-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e384b-256">In Global Catalog</span></span>      | <span data-ttu-id="e384b-257">否</span><span class="sxs-lookup"><span data-stu-id="e384b-257">False</span></span>                                      |
| <span data-ttu-id="e384b-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e384b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e384b-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e384b-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e384b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e384b-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e384b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e384b-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e384b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-262">Search-Flags</span></span>           | <span data-ttu-id="e384b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e384b-263">0x00000000</span></span>                                 |
| <span data-ttu-id="e384b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e384b-264">System-Flags</span></span>           | <span data-ttu-id="e384b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e384b-265">0x00000010</span></span>                                 |
| <span data-ttu-id="e384b-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e384b-266">Classes used in</span></span>        | [<span data-ttu-id="e384b-267">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e384b-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






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
# <a name="ms-ds-replication-notify-first-dsa-delay-attribute"></a><span data-ttu-id="50527-105">ms DS-複寫-通知-第一個-DSA-延遲屬性</span><span class="sxs-lookup"><span data-stu-id="50527-105">ms-DS-Replication-Notify-First-DSA-Delay attribute</span></span>

<span data-ttu-id="50527-106">這個屬性會控制對 DS 的變更之間的延遲時間，以及 NC 第一個複本夥伴的通知。</span><span class="sxs-lookup"><span data-stu-id="50527-106">This attribute controls the delay in time between changes to the DS, and notification of the first replica partner for an NC.</span></span>



| <span data-ttu-id="50527-107">進入</span><span class="sxs-lookup"><span data-stu-id="50527-107">Entry</span></span> | <span data-ttu-id="50527-108">值</span><span class="sxs-lookup"><span data-stu-id="50527-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="50527-109">CN</span><span class="sxs-lookup"><span data-stu-id="50527-109">CN</span></span>                | <span data-ttu-id="50527-110">ms DS-複寫-通知-第一個-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="50527-110">ms-DS-Replication-Notify-First-DSA-Delay</span></span> |
| <span data-ttu-id="50527-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="50527-111">Ldap-Display-Name</span></span> | <span data-ttu-id="50527-112">複寫-通知-第一個-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="50527-112">msDS-Replication-Notify-First-DSA-Delay</span></span>  |
| <span data-ttu-id="50527-113">大小</span><span class="sxs-lookup"><span data-stu-id="50527-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="50527-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="50527-114">Update Privilege</span></span>  | <span data-ttu-id="50527-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="50527-115">This value is set by the system.</span></span>         |
| <span data-ttu-id="50527-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="50527-116">Update Frequency</span></span>  | \-                                       |
| <span data-ttu-id="50527-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="50527-117">Attribute-Id</span></span>      | <span data-ttu-id="50527-118">1.2.840.113556.1.4.1663</span><span class="sxs-lookup"><span data-stu-id="50527-118">1.2.840.113556.1.4.1663</span></span>                  |
| <span data-ttu-id="50527-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="50527-119">System-Id-Guid</span></span>    | <span data-ttu-id="50527-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span><span class="sxs-lookup"><span data-stu-id="50527-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span></span>     |
| <span data-ttu-id="50527-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="50527-121">Syntax</span></span>            | [<span data-ttu-id="50527-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="50527-122">**Enumeration**</span></span>](s-enumeration.md)     |



## <a name="implementations"></a><span data-ttu-id="50527-123">實作</span><span class="sxs-lookup"><span data-stu-id="50527-123">Implementations</span></span>

-   [<span data-ttu-id="50527-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="50527-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="50527-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="50527-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="50527-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="50527-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="50527-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="50527-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="50527-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50527-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="50527-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50527-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="50527-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50527-130">Windows Server 2003</span></span>



| <span data-ttu-id="50527-131">進入</span><span class="sxs-lookup"><span data-stu-id="50527-131">Entry</span></span> | <span data-ttu-id="50527-132">值</span><span class="sxs-lookup"><span data-stu-id="50527-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="50527-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50527-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50527-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="50527-135">System-Only</span></span>            | <span data-ttu-id="50527-136">否</span><span class="sxs-lookup"><span data-stu-id="50527-136">False</span></span>                                      |
| <span data-ttu-id="50527-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50527-137">Is-Single-Valued</span></span>       | <span data-ttu-id="50527-138">對</span><span class="sxs-lookup"><span data-stu-id="50527-138">True</span></span>                                       |
| <span data-ttu-id="50527-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50527-139">Is Indexed</span></span>             | <span data-ttu-id="50527-140">否</span><span class="sxs-lookup"><span data-stu-id="50527-140">False</span></span>                                      |
| <span data-ttu-id="50527-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50527-141">In Global Catalog</span></span>      | <span data-ttu-id="50527-142">否</span><span class="sxs-lookup"><span data-stu-id="50527-142">False</span></span>                                      |
| <span data-ttu-id="50527-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50527-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="50527-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50527-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="50527-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50527-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="50527-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50527-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="50527-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-147">Search-Flags</span></span>           | <span data-ttu-id="50527-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50527-148">0x00000000</span></span>                                 |
| <span data-ttu-id="50527-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-149">System-Flags</span></span>           | <span data-ttu-id="50527-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50527-150">0x00000010</span></span>                                 |
| <span data-ttu-id="50527-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50527-151">Classes used in</span></span>        | [<span data-ttu-id="50527-152">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50527-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="50527-153">亞當</span><span class="sxs-lookup"><span data-stu-id="50527-153">ADAM</span></span>



| <span data-ttu-id="50527-154">進入</span><span class="sxs-lookup"><span data-stu-id="50527-154">Entry</span></span> | <span data-ttu-id="50527-155">值</span><span class="sxs-lookup"><span data-stu-id="50527-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="50527-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50527-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50527-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="50527-158">System-Only</span></span>            | <span data-ttu-id="50527-159">否</span><span class="sxs-lookup"><span data-stu-id="50527-159">False</span></span>                                      |
| <span data-ttu-id="50527-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50527-160">Is-Single-Valued</span></span>       | <span data-ttu-id="50527-161">對</span><span class="sxs-lookup"><span data-stu-id="50527-161">True</span></span>                                       |
| <span data-ttu-id="50527-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50527-162">Is Indexed</span></span>             | <span data-ttu-id="50527-163">否</span><span class="sxs-lookup"><span data-stu-id="50527-163">False</span></span>                                      |
| <span data-ttu-id="50527-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50527-164">In Global Catalog</span></span>      | <span data-ttu-id="50527-165">否</span><span class="sxs-lookup"><span data-stu-id="50527-165">False</span></span>                                      |
| <span data-ttu-id="50527-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50527-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="50527-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50527-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="50527-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50527-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="50527-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50527-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="50527-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-170">Search-Flags</span></span>           | <span data-ttu-id="50527-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50527-171">0x00000000</span></span>                                 |
| <span data-ttu-id="50527-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-172">System-Flags</span></span>           | <span data-ttu-id="50527-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50527-173">0x00000010</span></span>                                 |
| <span data-ttu-id="50527-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50527-174">Classes used in</span></span>        | [<span data-ttu-id="50527-175">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50527-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="50527-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="50527-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="50527-177">進入</span><span class="sxs-lookup"><span data-stu-id="50527-177">Entry</span></span> | <span data-ttu-id="50527-178">值</span><span class="sxs-lookup"><span data-stu-id="50527-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="50527-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50527-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50527-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="50527-181">System-Only</span></span>            | <span data-ttu-id="50527-182">否</span><span class="sxs-lookup"><span data-stu-id="50527-182">False</span></span>                                      |
| <span data-ttu-id="50527-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50527-183">Is-Single-Valued</span></span>       | <span data-ttu-id="50527-184">對</span><span class="sxs-lookup"><span data-stu-id="50527-184">True</span></span>                                       |
| <span data-ttu-id="50527-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50527-185">Is Indexed</span></span>             | <span data-ttu-id="50527-186">否</span><span class="sxs-lookup"><span data-stu-id="50527-186">False</span></span>                                      |
| <span data-ttu-id="50527-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50527-187">In Global Catalog</span></span>      | <span data-ttu-id="50527-188">否</span><span class="sxs-lookup"><span data-stu-id="50527-188">False</span></span>                                      |
| <span data-ttu-id="50527-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50527-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="50527-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50527-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="50527-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50527-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="50527-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50527-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="50527-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-193">Search-Flags</span></span>           | <span data-ttu-id="50527-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50527-194">0x00000000</span></span>                                 |
| <span data-ttu-id="50527-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-195">System-Flags</span></span>           | <span data-ttu-id="50527-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50527-196">0x00000010</span></span>                                 |
| <span data-ttu-id="50527-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50527-197">Classes used in</span></span>        | [<span data-ttu-id="50527-198">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50527-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="50527-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50527-199">Windows Server 2008</span></span>



| <span data-ttu-id="50527-200">進入</span><span class="sxs-lookup"><span data-stu-id="50527-200">Entry</span></span> | <span data-ttu-id="50527-201">值</span><span class="sxs-lookup"><span data-stu-id="50527-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="50527-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50527-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50527-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="50527-204">System-Only</span></span>            | <span data-ttu-id="50527-205">否</span><span class="sxs-lookup"><span data-stu-id="50527-205">False</span></span>                                      |
| <span data-ttu-id="50527-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50527-206">Is-Single-Valued</span></span>       | <span data-ttu-id="50527-207">對</span><span class="sxs-lookup"><span data-stu-id="50527-207">True</span></span>                                       |
| <span data-ttu-id="50527-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50527-208">Is Indexed</span></span>             | <span data-ttu-id="50527-209">否</span><span class="sxs-lookup"><span data-stu-id="50527-209">False</span></span>                                      |
| <span data-ttu-id="50527-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50527-210">In Global Catalog</span></span>      | <span data-ttu-id="50527-211">否</span><span class="sxs-lookup"><span data-stu-id="50527-211">False</span></span>                                      |
| <span data-ttu-id="50527-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50527-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="50527-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50527-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="50527-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50527-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="50527-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50527-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="50527-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-216">Search-Flags</span></span>           | <span data-ttu-id="50527-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50527-217">0x00000000</span></span>                                 |
| <span data-ttu-id="50527-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-218">System-Flags</span></span>           | <span data-ttu-id="50527-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50527-219">0x00000010</span></span>                                 |
| <span data-ttu-id="50527-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50527-220">Classes used in</span></span>        | [<span data-ttu-id="50527-221">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50527-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="50527-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50527-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="50527-223">進入</span><span class="sxs-lookup"><span data-stu-id="50527-223">Entry</span></span> | <span data-ttu-id="50527-224">值</span><span class="sxs-lookup"><span data-stu-id="50527-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="50527-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50527-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50527-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="50527-227">System-Only</span></span>            | <span data-ttu-id="50527-228">否</span><span class="sxs-lookup"><span data-stu-id="50527-228">False</span></span>                                      |
| <span data-ttu-id="50527-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50527-229">Is-Single-Valued</span></span>       | <span data-ttu-id="50527-230">對</span><span class="sxs-lookup"><span data-stu-id="50527-230">True</span></span>                                       |
| <span data-ttu-id="50527-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50527-231">Is Indexed</span></span>             | <span data-ttu-id="50527-232">否</span><span class="sxs-lookup"><span data-stu-id="50527-232">False</span></span>                                      |
| <span data-ttu-id="50527-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50527-233">In Global Catalog</span></span>      | <span data-ttu-id="50527-234">否</span><span class="sxs-lookup"><span data-stu-id="50527-234">False</span></span>                                      |
| <span data-ttu-id="50527-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50527-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="50527-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50527-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="50527-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50527-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="50527-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50527-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="50527-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-239">Search-Flags</span></span>           | <span data-ttu-id="50527-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50527-240">0x00000000</span></span>                                 |
| <span data-ttu-id="50527-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-241">System-Flags</span></span>           | <span data-ttu-id="50527-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50527-242">0x00000010</span></span>                                 |
| <span data-ttu-id="50527-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50527-243">Classes used in</span></span>        | [<span data-ttu-id="50527-244">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50527-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="50527-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50527-245">Windows Server 2012</span></span>



| <span data-ttu-id="50527-246">進入</span><span class="sxs-lookup"><span data-stu-id="50527-246">Entry</span></span> | <span data-ttu-id="50527-247">值</span><span class="sxs-lookup"><span data-stu-id="50527-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="50527-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50527-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50527-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="50527-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="50527-250">System-Only</span></span>            | <span data-ttu-id="50527-251">否</span><span class="sxs-lookup"><span data-stu-id="50527-251">False</span></span>                                      |
| <span data-ttu-id="50527-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50527-252">Is-Single-Valued</span></span>       | <span data-ttu-id="50527-253">對</span><span class="sxs-lookup"><span data-stu-id="50527-253">True</span></span>                                       |
| <span data-ttu-id="50527-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50527-254">Is Indexed</span></span>             | <span data-ttu-id="50527-255">否</span><span class="sxs-lookup"><span data-stu-id="50527-255">False</span></span>                                      |
| <span data-ttu-id="50527-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50527-256">In Global Catalog</span></span>      | <span data-ttu-id="50527-257">否</span><span class="sxs-lookup"><span data-stu-id="50527-257">False</span></span>                                      |
| <span data-ttu-id="50527-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50527-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="50527-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50527-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="50527-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50527-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="50527-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50527-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="50527-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-262">Search-Flags</span></span>           | <span data-ttu-id="50527-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50527-263">0x00000000</span></span>                                 |
| <span data-ttu-id="50527-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50527-264">System-Flags</span></span>           | <span data-ttu-id="50527-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50527-265">0x00000010</span></span>                                 |
| <span data-ttu-id="50527-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50527-266">Classes used in</span></span>        | [<span data-ttu-id="50527-267">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50527-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






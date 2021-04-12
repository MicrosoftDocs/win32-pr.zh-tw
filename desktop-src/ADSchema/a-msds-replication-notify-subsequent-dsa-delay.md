---
title: ms DS-複寫-通知-後續的 DSA 延遲屬性
description: 這個屬性會控制 NC 的每個後續複本夥伴之間的通知之間的延遲時間。
ms.assetid: 6bd9fed7-2003-4156-b1a0-da8622dc2ca8
ms.tgt_platform: multiple
keywords:
- ms DS-複寫-通知-後續的 DSA 延遲屬性 AD 架構
- 複寫-通知-後續的 DSA 延遲屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Replication-Notify-Subsequent-DSA-Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd8b267309fa8d017ace926f7497ca210fb2b00
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509698"
---
# <a name="ms-ds-replication-notify-subsequent-dsa-delay-attribute"></a><span data-ttu-id="d335c-105">ms DS-複寫-通知-後續的 DSA 延遲屬性</span><span class="sxs-lookup"><span data-stu-id="d335c-105">ms-DS-Replication-Notify-Subsequent-DSA-Delay attribute</span></span>

<span data-ttu-id="d335c-106">這個屬性會控制 NC 的每個後續複本夥伴之間的通知之間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="d335c-106">This attribute controls the delay in time between notification of each subsequent replica partner for an NC.</span></span>



| <span data-ttu-id="d335c-107">進入</span><span class="sxs-lookup"><span data-stu-id="d335c-107">Entry</span></span> | <span data-ttu-id="d335c-108">值</span><span class="sxs-lookup"><span data-stu-id="d335c-108">Value</span></span> |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="d335c-109">CN</span><span class="sxs-lookup"><span data-stu-id="d335c-109">CN</span></span>                | <span data-ttu-id="d335c-110">ms DS-複寫-通知-後續-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="d335c-110">ms-DS-Replication-Notify-Subsequent-DSA-Delay</span></span> |
| <span data-ttu-id="d335c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d335c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d335c-112">複寫-通知-後續-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="d335c-112">msDS-Replication-Notify-Subsequent-DSA-Delay</span></span>  |
| <span data-ttu-id="d335c-113">大小</span><span class="sxs-lookup"><span data-stu-id="d335c-113">Size</span></span>              | \-                                            |
| <span data-ttu-id="d335c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d335c-114">Update Privilege</span></span>  | <span data-ttu-id="d335c-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="d335c-115">This value is set by the system.</span></span>              |
| <span data-ttu-id="d335c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d335c-116">Update Frequency</span></span>  | \-                                            |
| <span data-ttu-id="d335c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d335c-117">Attribute-Id</span></span>      | <span data-ttu-id="d335c-118">1.2.840.113556.1.4.1664</span><span class="sxs-lookup"><span data-stu-id="d335c-118">1.2.840.113556.1.4.1664</span></span>                       |
| <span data-ttu-id="d335c-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d335c-119">System-Id-Guid</span></span>    | <span data-ttu-id="d335c-120">d63db385-dd92-4b52-b1d8-0d3ecc0e86b6</span><span class="sxs-lookup"><span data-stu-id="d335c-120">d63db385-dd92-4b52-b1d8-0d3ecc0e86b6</span></span>          |
| <span data-ttu-id="d335c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="d335c-121">Syntax</span></span>            | [<span data-ttu-id="d335c-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="d335c-122">**Enumeration**</span></span>](s-enumeration.md)          |



## <a name="implementations"></a><span data-ttu-id="d335c-123">實作</span><span class="sxs-lookup"><span data-stu-id="d335c-123">Implementations</span></span>

-   [<span data-ttu-id="d335c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d335c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d335c-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="d335c-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d335c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d335c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d335c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d335c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d335c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d335c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d335c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d335c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d335c-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d335c-130">Windows Server 2003</span></span>



| <span data-ttu-id="d335c-131">進入</span><span class="sxs-lookup"><span data-stu-id="d335c-131">Entry</span></span> | <span data-ttu-id="d335c-132">值</span><span class="sxs-lookup"><span data-stu-id="d335c-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d335c-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d335c-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d335c-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d335c-135">System-Only</span></span>            | <span data-ttu-id="d335c-136">否</span><span class="sxs-lookup"><span data-stu-id="d335c-136">False</span></span>                                      |
| <span data-ttu-id="d335c-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d335c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d335c-138">對</span><span class="sxs-lookup"><span data-stu-id="d335c-138">True</span></span>                                       |
| <span data-ttu-id="d335c-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d335c-139">Is Indexed</span></span>             | <span data-ttu-id="d335c-140">否</span><span class="sxs-lookup"><span data-stu-id="d335c-140">False</span></span>                                      |
| <span data-ttu-id="d335c-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d335c-141">In Global Catalog</span></span>      | <span data-ttu-id="d335c-142">否</span><span class="sxs-lookup"><span data-stu-id="d335c-142">False</span></span>                                      |
| <span data-ttu-id="d335c-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d335c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d335c-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d335c-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d335c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d335c-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d335c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d335c-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d335c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-147">Search-Flags</span></span>           | <span data-ttu-id="d335c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d335c-148">0x00000000</span></span>                                 |
| <span data-ttu-id="d335c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-149">System-Flags</span></span>           | <span data-ttu-id="d335c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d335c-150">0x00000010</span></span>                                 |
| <span data-ttu-id="d335c-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d335c-151">Classes used in</span></span>        | [<span data-ttu-id="d335c-152">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d335c-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d335c-153">亞當</span><span class="sxs-lookup"><span data-stu-id="d335c-153">ADAM</span></span>



| <span data-ttu-id="d335c-154">進入</span><span class="sxs-lookup"><span data-stu-id="d335c-154">Entry</span></span> | <span data-ttu-id="d335c-155">值</span><span class="sxs-lookup"><span data-stu-id="d335c-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d335c-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d335c-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d335c-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d335c-158">System-Only</span></span>            | <span data-ttu-id="d335c-159">否</span><span class="sxs-lookup"><span data-stu-id="d335c-159">False</span></span>                                      |
| <span data-ttu-id="d335c-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d335c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d335c-161">對</span><span class="sxs-lookup"><span data-stu-id="d335c-161">True</span></span>                                       |
| <span data-ttu-id="d335c-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d335c-162">Is Indexed</span></span>             | <span data-ttu-id="d335c-163">否</span><span class="sxs-lookup"><span data-stu-id="d335c-163">False</span></span>                                      |
| <span data-ttu-id="d335c-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d335c-164">In Global Catalog</span></span>      | <span data-ttu-id="d335c-165">否</span><span class="sxs-lookup"><span data-stu-id="d335c-165">False</span></span>                                      |
| <span data-ttu-id="d335c-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d335c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d335c-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d335c-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d335c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d335c-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d335c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d335c-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d335c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-170">Search-Flags</span></span>           | <span data-ttu-id="d335c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d335c-171">0x00000000</span></span>                                 |
| <span data-ttu-id="d335c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-172">System-Flags</span></span>           | <span data-ttu-id="d335c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d335c-173">0x00000010</span></span>                                 |
| <span data-ttu-id="d335c-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d335c-174">Classes used in</span></span>        | [<span data-ttu-id="d335c-175">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d335c-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d335c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d335c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d335c-177">進入</span><span class="sxs-lookup"><span data-stu-id="d335c-177">Entry</span></span> | <span data-ttu-id="d335c-178">值</span><span class="sxs-lookup"><span data-stu-id="d335c-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d335c-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d335c-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d335c-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d335c-181">System-Only</span></span>            | <span data-ttu-id="d335c-182">否</span><span class="sxs-lookup"><span data-stu-id="d335c-182">False</span></span>                                      |
| <span data-ttu-id="d335c-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d335c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d335c-184">對</span><span class="sxs-lookup"><span data-stu-id="d335c-184">True</span></span>                                       |
| <span data-ttu-id="d335c-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d335c-185">Is Indexed</span></span>             | <span data-ttu-id="d335c-186">否</span><span class="sxs-lookup"><span data-stu-id="d335c-186">False</span></span>                                      |
| <span data-ttu-id="d335c-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d335c-187">In Global Catalog</span></span>      | <span data-ttu-id="d335c-188">否</span><span class="sxs-lookup"><span data-stu-id="d335c-188">False</span></span>                                      |
| <span data-ttu-id="d335c-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d335c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d335c-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d335c-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d335c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d335c-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d335c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d335c-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d335c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-193">Search-Flags</span></span>           | <span data-ttu-id="d335c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d335c-194">0x00000000</span></span>                                 |
| <span data-ttu-id="d335c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-195">System-Flags</span></span>           | <span data-ttu-id="d335c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d335c-196">0x00000010</span></span>                                 |
| <span data-ttu-id="d335c-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d335c-197">Classes used in</span></span>        | [<span data-ttu-id="d335c-198">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d335c-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d335c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d335c-199">Windows Server 2008</span></span>



| <span data-ttu-id="d335c-200">進入</span><span class="sxs-lookup"><span data-stu-id="d335c-200">Entry</span></span> | <span data-ttu-id="d335c-201">值</span><span class="sxs-lookup"><span data-stu-id="d335c-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d335c-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d335c-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d335c-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d335c-204">System-Only</span></span>            | <span data-ttu-id="d335c-205">否</span><span class="sxs-lookup"><span data-stu-id="d335c-205">False</span></span>                                      |
| <span data-ttu-id="d335c-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d335c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d335c-207">對</span><span class="sxs-lookup"><span data-stu-id="d335c-207">True</span></span>                                       |
| <span data-ttu-id="d335c-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d335c-208">Is Indexed</span></span>             | <span data-ttu-id="d335c-209">否</span><span class="sxs-lookup"><span data-stu-id="d335c-209">False</span></span>                                      |
| <span data-ttu-id="d335c-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d335c-210">In Global Catalog</span></span>      | <span data-ttu-id="d335c-211">否</span><span class="sxs-lookup"><span data-stu-id="d335c-211">False</span></span>                                      |
| <span data-ttu-id="d335c-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d335c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d335c-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d335c-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d335c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d335c-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d335c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d335c-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d335c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-216">Search-Flags</span></span>           | <span data-ttu-id="d335c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d335c-217">0x00000000</span></span>                                 |
| <span data-ttu-id="d335c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-218">System-Flags</span></span>           | <span data-ttu-id="d335c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d335c-219">0x00000010</span></span>                                 |
| <span data-ttu-id="d335c-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d335c-220">Classes used in</span></span>        | [<span data-ttu-id="d335c-221">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d335c-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d335c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d335c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d335c-223">進入</span><span class="sxs-lookup"><span data-stu-id="d335c-223">Entry</span></span> | <span data-ttu-id="d335c-224">值</span><span class="sxs-lookup"><span data-stu-id="d335c-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d335c-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d335c-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d335c-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d335c-227">System-Only</span></span>            | <span data-ttu-id="d335c-228">否</span><span class="sxs-lookup"><span data-stu-id="d335c-228">False</span></span>                                      |
| <span data-ttu-id="d335c-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d335c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d335c-230">對</span><span class="sxs-lookup"><span data-stu-id="d335c-230">True</span></span>                                       |
| <span data-ttu-id="d335c-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d335c-231">Is Indexed</span></span>             | <span data-ttu-id="d335c-232">否</span><span class="sxs-lookup"><span data-stu-id="d335c-232">False</span></span>                                      |
| <span data-ttu-id="d335c-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d335c-233">In Global Catalog</span></span>      | <span data-ttu-id="d335c-234">否</span><span class="sxs-lookup"><span data-stu-id="d335c-234">False</span></span>                                      |
| <span data-ttu-id="d335c-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d335c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d335c-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d335c-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d335c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d335c-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d335c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d335c-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d335c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-239">Search-Flags</span></span>           | <span data-ttu-id="d335c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d335c-240">0x00000000</span></span>                                 |
| <span data-ttu-id="d335c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-241">System-Flags</span></span>           | <span data-ttu-id="d335c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d335c-242">0x00000010</span></span>                                 |
| <span data-ttu-id="d335c-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d335c-243">Classes used in</span></span>        | [<span data-ttu-id="d335c-244">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d335c-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d335c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d335c-245">Windows Server 2012</span></span>



| <span data-ttu-id="d335c-246">進入</span><span class="sxs-lookup"><span data-stu-id="d335c-246">Entry</span></span> | <span data-ttu-id="d335c-247">值</span><span class="sxs-lookup"><span data-stu-id="d335c-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d335c-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d335c-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d335c-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d335c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d335c-250">System-Only</span></span>            | <span data-ttu-id="d335c-251">否</span><span class="sxs-lookup"><span data-stu-id="d335c-251">False</span></span>                                      |
| <span data-ttu-id="d335c-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d335c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d335c-253">對</span><span class="sxs-lookup"><span data-stu-id="d335c-253">True</span></span>                                       |
| <span data-ttu-id="d335c-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d335c-254">Is Indexed</span></span>             | <span data-ttu-id="d335c-255">否</span><span class="sxs-lookup"><span data-stu-id="d335c-255">False</span></span>                                      |
| <span data-ttu-id="d335c-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d335c-256">In Global Catalog</span></span>      | <span data-ttu-id="d335c-257">否</span><span class="sxs-lookup"><span data-stu-id="d335c-257">False</span></span>                                      |
| <span data-ttu-id="d335c-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d335c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d335c-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d335c-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d335c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d335c-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d335c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d335c-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d335c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-262">Search-Flags</span></span>           | <span data-ttu-id="d335c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d335c-263">0x00000000</span></span>                                 |
| <span data-ttu-id="d335c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d335c-264">System-Flags</span></span>           | <span data-ttu-id="d335c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d335c-265">0x00000010</span></span>                                 |
| <span data-ttu-id="d335c-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d335c-266">Classes used in</span></span>        | [<span data-ttu-id="d335c-267">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d335c-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






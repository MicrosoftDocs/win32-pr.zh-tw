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
# <a name="ms-ds-replication-notify-first-dsa-delay-attribute"></a><span data-ttu-id="7b00d-105">ms DS-複寫-通知-第一個-DSA-延遲屬性</span><span class="sxs-lookup"><span data-stu-id="7b00d-105">ms-DS-Replication-Notify-First-DSA-Delay attribute</span></span>

<span data-ttu-id="7b00d-106">這個屬性會控制對 DS 的變更之間的延遲時間，以及 NC 第一個複本夥伴的通知。</span><span class="sxs-lookup"><span data-stu-id="7b00d-106">This attribute controls the delay in time between changes to the DS, and notification of the first replica partner for an NC.</span></span>



| <span data-ttu-id="7b00d-107">進入</span><span class="sxs-lookup"><span data-stu-id="7b00d-107">Entry</span></span> | <span data-ttu-id="7b00d-108">值</span><span class="sxs-lookup"><span data-stu-id="7b00d-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="7b00d-109">CN</span><span class="sxs-lookup"><span data-stu-id="7b00d-109">CN</span></span>                | <span data-ttu-id="7b00d-110">ms DS-複寫-通知-第一個-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="7b00d-110">ms-DS-Replication-Notify-First-DSA-Delay</span></span> |
| <span data-ttu-id="7b00d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7b00d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7b00d-112">複寫-通知-第一個-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="7b00d-112">msDS-Replication-Notify-First-DSA-Delay</span></span>  |
| <span data-ttu-id="7b00d-113">大小</span><span class="sxs-lookup"><span data-stu-id="7b00d-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="7b00d-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7b00d-114">Update Privilege</span></span>  | <span data-ttu-id="7b00d-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7b00d-115">This value is set by the system.</span></span>         |
| <span data-ttu-id="7b00d-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7b00d-116">Update Frequency</span></span>  | \-                                       |
| <span data-ttu-id="7b00d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7b00d-117">Attribute-Id</span></span>      | <span data-ttu-id="7b00d-118">1.2.840.113556.1.4.1663</span><span class="sxs-lookup"><span data-stu-id="7b00d-118">1.2.840.113556.1.4.1663</span></span>                  |
| <span data-ttu-id="7b00d-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7b00d-119">System-Id-Guid</span></span>    | <span data-ttu-id="7b00d-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span><span class="sxs-lookup"><span data-stu-id="7b00d-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span></span>     |
| <span data-ttu-id="7b00d-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b00d-121">Syntax</span></span>            | [<span data-ttu-id="7b00d-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="7b00d-122">**Enumeration**</span></span>](s-enumeration.md)     |



## <a name="implementations"></a><span data-ttu-id="7b00d-123">實作</span><span class="sxs-lookup"><span data-stu-id="7b00d-123">Implementations</span></span>

-   [<span data-ttu-id="7b00d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7b00d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7b00d-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7b00d-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7b00d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7b00d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7b00d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7b00d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7b00d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7b00d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7b00d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7b00d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7b00d-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7b00d-130">Windows Server 2003</span></span>



| <span data-ttu-id="7b00d-131">進入</span><span class="sxs-lookup"><span data-stu-id="7b00d-131">Entry</span></span> | <span data-ttu-id="7b00d-132">值</span><span class="sxs-lookup"><span data-stu-id="7b00d-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7b00d-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b00d-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b00d-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b00d-135">System-Only</span></span>            | <span data-ttu-id="7b00d-136">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-136">False</span></span>                                      |
| <span data-ttu-id="7b00d-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b00d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7b00d-138">對</span><span class="sxs-lookup"><span data-stu-id="7b00d-138">True</span></span>                                       |
| <span data-ttu-id="7b00d-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b00d-139">Is Indexed</span></span>             | <span data-ttu-id="7b00d-140">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-140">False</span></span>                                      |
| <span data-ttu-id="7b00d-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b00d-141">In Global Catalog</span></span>      | <span data-ttu-id="7b00d-142">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-142">False</span></span>                                      |
| <span data-ttu-id="7b00d-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b00d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b00d-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b00d-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7b00d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b00d-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b00d-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-147">Search-Flags</span></span>           | <span data-ttu-id="7b00d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b00d-148">0x00000000</span></span>                                 |
| <span data-ttu-id="7b00d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-149">System-Flags</span></span>           | <span data-ttu-id="7b00d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b00d-150">0x00000010</span></span>                                 |
| <span data-ttu-id="7b00d-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b00d-151">Classes used in</span></span>        | [<span data-ttu-id="7b00d-152">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="7b00d-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7b00d-153">亞當</span><span class="sxs-lookup"><span data-stu-id="7b00d-153">ADAM</span></span>



| <span data-ttu-id="7b00d-154">進入</span><span class="sxs-lookup"><span data-stu-id="7b00d-154">Entry</span></span> | <span data-ttu-id="7b00d-155">值</span><span class="sxs-lookup"><span data-stu-id="7b00d-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7b00d-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b00d-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b00d-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b00d-158">System-Only</span></span>            | <span data-ttu-id="7b00d-159">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-159">False</span></span>                                      |
| <span data-ttu-id="7b00d-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b00d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7b00d-161">對</span><span class="sxs-lookup"><span data-stu-id="7b00d-161">True</span></span>                                       |
| <span data-ttu-id="7b00d-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b00d-162">Is Indexed</span></span>             | <span data-ttu-id="7b00d-163">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-163">False</span></span>                                      |
| <span data-ttu-id="7b00d-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b00d-164">In Global Catalog</span></span>      | <span data-ttu-id="7b00d-165">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-165">False</span></span>                                      |
| <span data-ttu-id="7b00d-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b00d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b00d-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b00d-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7b00d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b00d-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b00d-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-170">Search-Flags</span></span>           | <span data-ttu-id="7b00d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b00d-171">0x00000000</span></span>                                 |
| <span data-ttu-id="7b00d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-172">System-Flags</span></span>           | <span data-ttu-id="7b00d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b00d-173">0x00000010</span></span>                                 |
| <span data-ttu-id="7b00d-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b00d-174">Classes used in</span></span>        | [<span data-ttu-id="7b00d-175">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="7b00d-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7b00d-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7b00d-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7b00d-177">進入</span><span class="sxs-lookup"><span data-stu-id="7b00d-177">Entry</span></span> | <span data-ttu-id="7b00d-178">值</span><span class="sxs-lookup"><span data-stu-id="7b00d-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7b00d-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b00d-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b00d-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b00d-181">System-Only</span></span>            | <span data-ttu-id="7b00d-182">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-182">False</span></span>                                      |
| <span data-ttu-id="7b00d-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b00d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7b00d-184">對</span><span class="sxs-lookup"><span data-stu-id="7b00d-184">True</span></span>                                       |
| <span data-ttu-id="7b00d-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b00d-185">Is Indexed</span></span>             | <span data-ttu-id="7b00d-186">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-186">False</span></span>                                      |
| <span data-ttu-id="7b00d-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b00d-187">In Global Catalog</span></span>      | <span data-ttu-id="7b00d-188">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-188">False</span></span>                                      |
| <span data-ttu-id="7b00d-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b00d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b00d-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b00d-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7b00d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b00d-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b00d-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-193">Search-Flags</span></span>           | <span data-ttu-id="7b00d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b00d-194">0x00000000</span></span>                                 |
| <span data-ttu-id="7b00d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-195">System-Flags</span></span>           | <span data-ttu-id="7b00d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b00d-196">0x00000010</span></span>                                 |
| <span data-ttu-id="7b00d-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b00d-197">Classes used in</span></span>        | [<span data-ttu-id="7b00d-198">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="7b00d-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7b00d-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b00d-199">Windows Server 2008</span></span>



| <span data-ttu-id="7b00d-200">進入</span><span class="sxs-lookup"><span data-stu-id="7b00d-200">Entry</span></span> | <span data-ttu-id="7b00d-201">值</span><span class="sxs-lookup"><span data-stu-id="7b00d-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7b00d-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b00d-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b00d-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b00d-204">System-Only</span></span>            | <span data-ttu-id="7b00d-205">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-205">False</span></span>                                      |
| <span data-ttu-id="7b00d-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b00d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7b00d-207">對</span><span class="sxs-lookup"><span data-stu-id="7b00d-207">True</span></span>                                       |
| <span data-ttu-id="7b00d-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b00d-208">Is Indexed</span></span>             | <span data-ttu-id="7b00d-209">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-209">False</span></span>                                      |
| <span data-ttu-id="7b00d-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b00d-210">In Global Catalog</span></span>      | <span data-ttu-id="7b00d-211">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-211">False</span></span>                                      |
| <span data-ttu-id="7b00d-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b00d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b00d-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b00d-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7b00d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b00d-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b00d-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-216">Search-Flags</span></span>           | <span data-ttu-id="7b00d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b00d-217">0x00000000</span></span>                                 |
| <span data-ttu-id="7b00d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-218">System-Flags</span></span>           | <span data-ttu-id="7b00d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b00d-219">0x00000010</span></span>                                 |
| <span data-ttu-id="7b00d-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b00d-220">Classes used in</span></span>        | [<span data-ttu-id="7b00d-221">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="7b00d-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7b00d-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b00d-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7b00d-223">進入</span><span class="sxs-lookup"><span data-stu-id="7b00d-223">Entry</span></span> | <span data-ttu-id="7b00d-224">值</span><span class="sxs-lookup"><span data-stu-id="7b00d-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7b00d-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b00d-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b00d-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b00d-227">System-Only</span></span>            | <span data-ttu-id="7b00d-228">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-228">False</span></span>                                      |
| <span data-ttu-id="7b00d-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b00d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7b00d-230">對</span><span class="sxs-lookup"><span data-stu-id="7b00d-230">True</span></span>                                       |
| <span data-ttu-id="7b00d-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b00d-231">Is Indexed</span></span>             | <span data-ttu-id="7b00d-232">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-232">False</span></span>                                      |
| <span data-ttu-id="7b00d-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b00d-233">In Global Catalog</span></span>      | <span data-ttu-id="7b00d-234">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-234">False</span></span>                                      |
| <span data-ttu-id="7b00d-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b00d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b00d-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b00d-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7b00d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b00d-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b00d-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-239">Search-Flags</span></span>           | <span data-ttu-id="7b00d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b00d-240">0x00000000</span></span>                                 |
| <span data-ttu-id="7b00d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-241">System-Flags</span></span>           | <span data-ttu-id="7b00d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b00d-242">0x00000010</span></span>                                 |
| <span data-ttu-id="7b00d-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b00d-243">Classes used in</span></span>        | [<span data-ttu-id="7b00d-244">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="7b00d-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7b00d-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b00d-245">Windows Server 2012</span></span>



| <span data-ttu-id="7b00d-246">進入</span><span class="sxs-lookup"><span data-stu-id="7b00d-246">Entry</span></span> | <span data-ttu-id="7b00d-247">值</span><span class="sxs-lookup"><span data-stu-id="7b00d-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7b00d-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b00d-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b00d-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7b00d-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b00d-250">System-Only</span></span>            | <span data-ttu-id="7b00d-251">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-251">False</span></span>                                      |
| <span data-ttu-id="7b00d-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b00d-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7b00d-253">對</span><span class="sxs-lookup"><span data-stu-id="7b00d-253">True</span></span>                                       |
| <span data-ttu-id="7b00d-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b00d-254">Is Indexed</span></span>             | <span data-ttu-id="7b00d-255">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-255">False</span></span>                                      |
| <span data-ttu-id="7b00d-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b00d-256">In Global Catalog</span></span>      | <span data-ttu-id="7b00d-257">否</span><span class="sxs-lookup"><span data-stu-id="7b00d-257">False</span></span>                                      |
| <span data-ttu-id="7b00d-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b00d-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b00d-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b00d-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7b00d-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b00d-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b00d-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7b00d-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-262">Search-Flags</span></span>           | <span data-ttu-id="7b00d-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b00d-263">0x00000000</span></span>                                 |
| <span data-ttu-id="7b00d-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b00d-264">System-Flags</span></span>           | <span data-ttu-id="7b00d-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b00d-265">0x00000010</span></span>                                 |
| <span data-ttu-id="7b00d-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b00d-266">Classes used in</span></span>        | [<span data-ttu-id="7b00d-267">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="7b00d-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






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
# <a name="ms-ds-replication-notify-first-dsa-delay-attribute"></a><span data-ttu-id="d3b5a-105">ms DS-複寫-通知-第一個-DSA-延遲屬性</span><span class="sxs-lookup"><span data-stu-id="d3b5a-105">ms-DS-Replication-Notify-First-DSA-Delay attribute</span></span>

<span data-ttu-id="d3b5a-106">這個屬性會控制對 DS 的變更之間的延遲時間，以及 NC 第一個複本夥伴的通知。</span><span class="sxs-lookup"><span data-stu-id="d3b5a-106">This attribute controls the delay in time between changes to the DS, and notification of the first replica partner for an NC.</span></span>



| <span data-ttu-id="d3b5a-107">進入</span><span class="sxs-lookup"><span data-stu-id="d3b5a-107">Entry</span></span> | <span data-ttu-id="d3b5a-108">值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="d3b5a-109">CN</span><span class="sxs-lookup"><span data-stu-id="d3b5a-109">CN</span></span>                | <span data-ttu-id="d3b5a-110">ms DS-複寫-通知-第一個-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="d3b5a-110">ms-DS-Replication-Notify-First-DSA-Delay</span></span> |
| <span data-ttu-id="d3b5a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d3b5a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d3b5a-112">複寫-通知-第一個-DSA-延遲</span><span class="sxs-lookup"><span data-stu-id="d3b5a-112">msDS-Replication-Notify-First-DSA-Delay</span></span>  |
| <span data-ttu-id="d3b5a-113">大小</span><span class="sxs-lookup"><span data-stu-id="d3b5a-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="d3b5a-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d3b5a-114">Update Privilege</span></span>  | <span data-ttu-id="d3b5a-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="d3b5a-115">This value is set by the system.</span></span>         |
| <span data-ttu-id="d3b5a-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d3b5a-116">Update Frequency</span></span>  | \-                                       |
| <span data-ttu-id="d3b5a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d3b5a-117">Attribute-Id</span></span>      | <span data-ttu-id="d3b5a-118">1.2.840.113556.1.4.1663</span><span class="sxs-lookup"><span data-stu-id="d3b5a-118">1.2.840.113556.1.4.1663</span></span>                  |
| <span data-ttu-id="d3b5a-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d3b5a-119">System-Id-Guid</span></span>    | <span data-ttu-id="d3b5a-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span><span class="sxs-lookup"><span data-stu-id="d3b5a-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span></span>     |
| <span data-ttu-id="d3b5a-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3b5a-121">Syntax</span></span>            | [<span data-ttu-id="d3b5a-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-122">**Enumeration**</span></span>](s-enumeration.md)     |



## <a name="implementations"></a><span data-ttu-id="d3b5a-123">實作</span><span class="sxs-lookup"><span data-stu-id="d3b5a-123">Implementations</span></span>

-   [<span data-ttu-id="d3b5a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d3b5a-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d3b5a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d3b5a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d3b5a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d3b5a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d3b5a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3b5a-130">Windows Server 2003</span></span>



| <span data-ttu-id="d3b5a-131">進入</span><span class="sxs-lookup"><span data-stu-id="d3b5a-131">Entry</span></span> | <span data-ttu-id="d3b5a-132">值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d3b5a-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b5a-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b5a-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b5a-135">System-Only</span></span>            | <span data-ttu-id="d3b5a-136">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-136">False</span></span>                                      |
| <span data-ttu-id="d3b5a-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b5a-138">對</span><span class="sxs-lookup"><span data-stu-id="d3b5a-138">True</span></span>                                       |
| <span data-ttu-id="d3b5a-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b5a-139">Is Indexed</span></span>             | <span data-ttu-id="d3b5a-140">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-140">False</span></span>                                      |
| <span data-ttu-id="d3b5a-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b5a-141">In Global Catalog</span></span>      | <span data-ttu-id="d3b5a-142">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-142">False</span></span>                                      |
| <span data-ttu-id="d3b5a-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b5a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b5a-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b5a-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d3b5a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b5a-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b5a-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-147">Search-Flags</span></span>           | <span data-ttu-id="d3b5a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b5a-148">0x00000000</span></span>                                 |
| <span data-ttu-id="d3b5a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-149">System-Flags</span></span>           | <span data-ttu-id="d3b5a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b5a-150">0x00000010</span></span>                                 |
| <span data-ttu-id="d3b5a-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b5a-151">Classes used in</span></span>        | [<span data-ttu-id="d3b5a-152">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d3b5a-153">亞當</span><span class="sxs-lookup"><span data-stu-id="d3b5a-153">ADAM</span></span>



| <span data-ttu-id="d3b5a-154">進入</span><span class="sxs-lookup"><span data-stu-id="d3b5a-154">Entry</span></span> | <span data-ttu-id="d3b5a-155">值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d3b5a-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b5a-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b5a-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b5a-158">System-Only</span></span>            | <span data-ttu-id="d3b5a-159">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-159">False</span></span>                                      |
| <span data-ttu-id="d3b5a-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b5a-161">對</span><span class="sxs-lookup"><span data-stu-id="d3b5a-161">True</span></span>                                       |
| <span data-ttu-id="d3b5a-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b5a-162">Is Indexed</span></span>             | <span data-ttu-id="d3b5a-163">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-163">False</span></span>                                      |
| <span data-ttu-id="d3b5a-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b5a-164">In Global Catalog</span></span>      | <span data-ttu-id="d3b5a-165">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-165">False</span></span>                                      |
| <span data-ttu-id="d3b5a-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b5a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b5a-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b5a-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d3b5a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b5a-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b5a-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-170">Search-Flags</span></span>           | <span data-ttu-id="d3b5a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b5a-171">0x00000000</span></span>                                 |
| <span data-ttu-id="d3b5a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-172">System-Flags</span></span>           | <span data-ttu-id="d3b5a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b5a-173">0x00000010</span></span>                                 |
| <span data-ttu-id="d3b5a-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b5a-174">Classes used in</span></span>        | [<span data-ttu-id="d3b5a-175">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d3b5a-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d3b5a-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d3b5a-177">進入</span><span class="sxs-lookup"><span data-stu-id="d3b5a-177">Entry</span></span> | <span data-ttu-id="d3b5a-178">值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d3b5a-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b5a-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b5a-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b5a-181">System-Only</span></span>            | <span data-ttu-id="d3b5a-182">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-182">False</span></span>                                      |
| <span data-ttu-id="d3b5a-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b5a-184">對</span><span class="sxs-lookup"><span data-stu-id="d3b5a-184">True</span></span>                                       |
| <span data-ttu-id="d3b5a-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b5a-185">Is Indexed</span></span>             | <span data-ttu-id="d3b5a-186">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-186">False</span></span>                                      |
| <span data-ttu-id="d3b5a-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b5a-187">In Global Catalog</span></span>      | <span data-ttu-id="d3b5a-188">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-188">False</span></span>                                      |
| <span data-ttu-id="d3b5a-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b5a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b5a-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b5a-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d3b5a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b5a-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b5a-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-193">Search-Flags</span></span>           | <span data-ttu-id="d3b5a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b5a-194">0x00000000</span></span>                                 |
| <span data-ttu-id="d3b5a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-195">System-Flags</span></span>           | <span data-ttu-id="d3b5a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b5a-196">0x00000010</span></span>                                 |
| <span data-ttu-id="d3b5a-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b5a-197">Classes used in</span></span>        | [<span data-ttu-id="d3b5a-198">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d3b5a-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3b5a-199">Windows Server 2008</span></span>



| <span data-ttu-id="d3b5a-200">進入</span><span class="sxs-lookup"><span data-stu-id="d3b5a-200">Entry</span></span> | <span data-ttu-id="d3b5a-201">值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d3b5a-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b5a-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b5a-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b5a-204">System-Only</span></span>            | <span data-ttu-id="d3b5a-205">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-205">False</span></span>                                      |
| <span data-ttu-id="d3b5a-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b5a-207">對</span><span class="sxs-lookup"><span data-stu-id="d3b5a-207">True</span></span>                                       |
| <span data-ttu-id="d3b5a-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b5a-208">Is Indexed</span></span>             | <span data-ttu-id="d3b5a-209">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-209">False</span></span>                                      |
| <span data-ttu-id="d3b5a-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b5a-210">In Global Catalog</span></span>      | <span data-ttu-id="d3b5a-211">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-211">False</span></span>                                      |
| <span data-ttu-id="d3b5a-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b5a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b5a-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b5a-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d3b5a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b5a-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b5a-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-216">Search-Flags</span></span>           | <span data-ttu-id="d3b5a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b5a-217">0x00000000</span></span>                                 |
| <span data-ttu-id="d3b5a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-218">System-Flags</span></span>           | <span data-ttu-id="d3b5a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b5a-219">0x00000010</span></span>                                 |
| <span data-ttu-id="d3b5a-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b5a-220">Classes used in</span></span>        | [<span data-ttu-id="d3b5a-221">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d3b5a-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3b5a-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d3b5a-223">進入</span><span class="sxs-lookup"><span data-stu-id="d3b5a-223">Entry</span></span> | <span data-ttu-id="d3b5a-224">值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d3b5a-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b5a-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b5a-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b5a-227">System-Only</span></span>            | <span data-ttu-id="d3b5a-228">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-228">False</span></span>                                      |
| <span data-ttu-id="d3b5a-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b5a-230">對</span><span class="sxs-lookup"><span data-stu-id="d3b5a-230">True</span></span>                                       |
| <span data-ttu-id="d3b5a-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b5a-231">Is Indexed</span></span>             | <span data-ttu-id="d3b5a-232">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-232">False</span></span>                                      |
| <span data-ttu-id="d3b5a-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b5a-233">In Global Catalog</span></span>      | <span data-ttu-id="d3b5a-234">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-234">False</span></span>                                      |
| <span data-ttu-id="d3b5a-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b5a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b5a-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b5a-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d3b5a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b5a-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b5a-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-239">Search-Flags</span></span>           | <span data-ttu-id="d3b5a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b5a-240">0x00000000</span></span>                                 |
| <span data-ttu-id="d3b5a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-241">System-Flags</span></span>           | <span data-ttu-id="d3b5a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b5a-242">0x00000010</span></span>                                 |
| <span data-ttu-id="d3b5a-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b5a-243">Classes used in</span></span>        | [<span data-ttu-id="d3b5a-244">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d3b5a-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3b5a-245">Windows Server 2012</span></span>



| <span data-ttu-id="d3b5a-246">進入</span><span class="sxs-lookup"><span data-stu-id="d3b5a-246">Entry</span></span> | <span data-ttu-id="d3b5a-247">值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="d3b5a-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b5a-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b5a-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="d3b5a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b5a-250">System-Only</span></span>            | <span data-ttu-id="d3b5a-251">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-251">False</span></span>                                      |
| <span data-ttu-id="d3b5a-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b5a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b5a-253">對</span><span class="sxs-lookup"><span data-stu-id="d3b5a-253">True</span></span>                                       |
| <span data-ttu-id="d3b5a-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b5a-254">Is Indexed</span></span>             | <span data-ttu-id="d3b5a-255">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-255">False</span></span>                                      |
| <span data-ttu-id="d3b5a-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b5a-256">In Global Catalog</span></span>      | <span data-ttu-id="d3b5a-257">否</span><span class="sxs-lookup"><span data-stu-id="d3b5a-257">False</span></span>                                      |
| <span data-ttu-id="d3b5a-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b5a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b5a-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b5a-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="d3b5a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b5a-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b5a-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="d3b5a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-262">Search-Flags</span></span>           | <span data-ttu-id="d3b5a-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b5a-263">0x00000000</span></span>                                 |
| <span data-ttu-id="d3b5a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b5a-264">System-Flags</span></span>           | <span data-ttu-id="d3b5a-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b5a-265">0x00000010</span></span>                                 |
| <span data-ttu-id="d3b5a-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b5a-266">Classes used in</span></span>        | [<span data-ttu-id="d3b5a-267">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="d3b5a-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






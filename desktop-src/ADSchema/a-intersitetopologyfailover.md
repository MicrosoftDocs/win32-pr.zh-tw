---
title: 網站間拓撲-容錯移轉屬性
description: 表示在網站間拓撲產生器的上一次保持運作之後，必須經過多少時間才會被視為失效。
ms.assetid: d351dbec-d5a3-46e1-87a9-0856d19e07c6
ms.tgt_platform: multiple
keywords:
- 網站間拓撲-容錯移轉屬性 AD 架構
- interSiteTopologyFailover 屬性 AD 架構
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Failover
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4e9cad98bade7fd69178a8fce795d0b92f35b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467308"
---
# <a name="inter-site-topology-failover-attribute"></a><span data-ttu-id="ba063-105">網站間拓撲-容錯移轉屬性</span><span class="sxs-lookup"><span data-stu-id="ba063-105">Inter-Site-Topology-Failover attribute</span></span>

<span data-ttu-id="ba063-106">表示在網站間拓撲產生器的上一次保持運作之後，必須經過多少時間才會被視為失效。</span><span class="sxs-lookup"><span data-stu-id="ba063-106">Indicates how much time must transpire since the last keep-alive for the inter-site topology generator to be considered dead.</span></span>



| <span data-ttu-id="ba063-107">進入</span><span class="sxs-lookup"><span data-stu-id="ba063-107">Entry</span></span> | <span data-ttu-id="ba063-108">值</span><span class="sxs-lookup"><span data-stu-id="ba063-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ba063-109">CN</span><span class="sxs-lookup"><span data-stu-id="ba063-109">CN</span></span>                | <span data-ttu-id="ba063-110">網站間拓撲-容錯移轉</span><span class="sxs-lookup"><span data-stu-id="ba063-110">Inter-Site-Topology-Failover</span></span>         |
| <span data-ttu-id="ba063-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ba063-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ba063-112">interSiteTopologyFailover</span><span class="sxs-lookup"><span data-stu-id="ba063-112">interSiteTopologyFailover</span></span>            |
| <span data-ttu-id="ba063-113">大小</span><span class="sxs-lookup"><span data-stu-id="ba063-113">Size</span></span>              | <span data-ttu-id="ba063-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ba063-114">4 bytes</span></span>                              |
| <span data-ttu-id="ba063-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ba063-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ba063-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ba063-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ba063-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ba063-117">Attribute-Id</span></span>      | <span data-ttu-id="ba063-118">1.2.840.113556.1.4.1248</span><span class="sxs-lookup"><span data-stu-id="ba063-118">1.2.840.113556.1.4.1248</span></span>              |
| <span data-ttu-id="ba063-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ba063-119">System-Id-Guid</span></span>    | <span data-ttu-id="ba063-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="ba063-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="ba063-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba063-121">Syntax</span></span>            | [<span data-ttu-id="ba063-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ba063-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ba063-123">實作</span><span class="sxs-lookup"><span data-stu-id="ba063-123">Implementations</span></span>

-   [<span data-ttu-id="ba063-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ba063-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ba063-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ba063-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ba063-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ba063-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ba063-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ba063-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ba063-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ba063-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ba063-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ba063-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ba063-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ba063-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ba063-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ba063-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ba063-132">進入</span><span class="sxs-lookup"><span data-stu-id="ba063-132">Entry</span></span> | <span data-ttu-id="ba063-133">值</span><span class="sxs-lookup"><span data-stu-id="ba063-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ba063-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba063-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba063-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba063-136">System-Only</span></span>            | <span data-ttu-id="ba063-137">否</span><span class="sxs-lookup"><span data-stu-id="ba063-137">False</span></span>                                                       |
| <span data-ttu-id="ba063-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba063-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ba063-139">對</span><span class="sxs-lookup"><span data-stu-id="ba063-139">True</span></span>                                                        |
| <span data-ttu-id="ba063-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba063-140">Is Indexed</span></span>             | <span data-ttu-id="ba063-141">否</span><span class="sxs-lookup"><span data-stu-id="ba063-141">False</span></span>                                                       |
| <span data-ttu-id="ba063-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba063-142">In Global Catalog</span></span>      | <span data-ttu-id="ba063-143">否</span><span class="sxs-lookup"><span data-stu-id="ba063-143">False</span></span>                                                       |
| <span data-ttu-id="ba063-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba063-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba063-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba063-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="ba063-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba063-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba063-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-148">Search-Flags</span></span>           | <span data-ttu-id="ba063-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba063-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="ba063-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-150">System-Flags</span></span>           | <span data-ttu-id="ba063-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba063-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="ba063-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba063-152">Classes used in</span></span>        | [<span data-ttu-id="ba063-153">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="ba063-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ba063-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba063-154">Windows Server 2003</span></span>



| <span data-ttu-id="ba063-155">進入</span><span class="sxs-lookup"><span data-stu-id="ba063-155">Entry</span></span> | <span data-ttu-id="ba063-156">值</span><span class="sxs-lookup"><span data-stu-id="ba063-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ba063-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba063-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba063-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba063-159">System-Only</span></span>            | <span data-ttu-id="ba063-160">否</span><span class="sxs-lookup"><span data-stu-id="ba063-160">False</span></span>                                                       |
| <span data-ttu-id="ba063-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba063-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ba063-162">對</span><span class="sxs-lookup"><span data-stu-id="ba063-162">True</span></span>                                                        |
| <span data-ttu-id="ba063-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba063-163">Is Indexed</span></span>             | <span data-ttu-id="ba063-164">否</span><span class="sxs-lookup"><span data-stu-id="ba063-164">False</span></span>                                                       |
| <span data-ttu-id="ba063-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba063-165">In Global Catalog</span></span>      | <span data-ttu-id="ba063-166">否</span><span class="sxs-lookup"><span data-stu-id="ba063-166">False</span></span>                                                       |
| <span data-ttu-id="ba063-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba063-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba063-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba063-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="ba063-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba063-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba063-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-171">Search-Flags</span></span>           | <span data-ttu-id="ba063-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba063-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="ba063-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-173">System-Flags</span></span>           | <span data-ttu-id="ba063-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba063-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="ba063-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba063-175">Classes used in</span></span>        | [<span data-ttu-id="ba063-176">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="ba063-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ba063-177">亞當</span><span class="sxs-lookup"><span data-stu-id="ba063-177">ADAM</span></span>



| <span data-ttu-id="ba063-178">進入</span><span class="sxs-lookup"><span data-stu-id="ba063-178">Entry</span></span> | <span data-ttu-id="ba063-179">值</span><span class="sxs-lookup"><span data-stu-id="ba063-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ba063-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba063-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba063-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba063-182">System-Only</span></span>            | <span data-ttu-id="ba063-183">否</span><span class="sxs-lookup"><span data-stu-id="ba063-183">False</span></span>                                                       |
| <span data-ttu-id="ba063-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba063-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ba063-185">對</span><span class="sxs-lookup"><span data-stu-id="ba063-185">True</span></span>                                                        |
| <span data-ttu-id="ba063-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba063-186">Is Indexed</span></span>             | <span data-ttu-id="ba063-187">否</span><span class="sxs-lookup"><span data-stu-id="ba063-187">False</span></span>                                                       |
| <span data-ttu-id="ba063-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba063-188">In Global Catalog</span></span>      | <span data-ttu-id="ba063-189">否</span><span class="sxs-lookup"><span data-stu-id="ba063-189">False</span></span>                                                       |
| <span data-ttu-id="ba063-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba063-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba063-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba063-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="ba063-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba063-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba063-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-194">Search-Flags</span></span>           | <span data-ttu-id="ba063-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba063-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="ba063-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-196">System-Flags</span></span>           | <span data-ttu-id="ba063-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba063-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="ba063-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba063-198">Classes used in</span></span>        | [<span data-ttu-id="ba063-199">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="ba063-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ba063-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ba063-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ba063-201">進入</span><span class="sxs-lookup"><span data-stu-id="ba063-201">Entry</span></span> | <span data-ttu-id="ba063-202">值</span><span class="sxs-lookup"><span data-stu-id="ba063-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ba063-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba063-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba063-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba063-205">System-Only</span></span>            | <span data-ttu-id="ba063-206">否</span><span class="sxs-lookup"><span data-stu-id="ba063-206">False</span></span>                                                       |
| <span data-ttu-id="ba063-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba063-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ba063-208">對</span><span class="sxs-lookup"><span data-stu-id="ba063-208">True</span></span>                                                        |
| <span data-ttu-id="ba063-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba063-209">Is Indexed</span></span>             | <span data-ttu-id="ba063-210">否</span><span class="sxs-lookup"><span data-stu-id="ba063-210">False</span></span>                                                       |
| <span data-ttu-id="ba063-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba063-211">In Global Catalog</span></span>      | <span data-ttu-id="ba063-212">否</span><span class="sxs-lookup"><span data-stu-id="ba063-212">False</span></span>                                                       |
| <span data-ttu-id="ba063-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba063-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba063-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba063-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="ba063-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba063-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba063-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-217">Search-Flags</span></span>           | <span data-ttu-id="ba063-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba063-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="ba063-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-219">System-Flags</span></span>           | <span data-ttu-id="ba063-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba063-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="ba063-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba063-221">Classes used in</span></span>        | [<span data-ttu-id="ba063-222">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="ba063-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ba063-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba063-223">Windows Server 2008</span></span>



| <span data-ttu-id="ba063-224">進入</span><span class="sxs-lookup"><span data-stu-id="ba063-224">Entry</span></span> | <span data-ttu-id="ba063-225">值</span><span class="sxs-lookup"><span data-stu-id="ba063-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ba063-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba063-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba063-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba063-228">System-Only</span></span>            | <span data-ttu-id="ba063-229">否</span><span class="sxs-lookup"><span data-stu-id="ba063-229">False</span></span>                                                       |
| <span data-ttu-id="ba063-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba063-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ba063-231">對</span><span class="sxs-lookup"><span data-stu-id="ba063-231">True</span></span>                                                        |
| <span data-ttu-id="ba063-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba063-232">Is Indexed</span></span>             | <span data-ttu-id="ba063-233">否</span><span class="sxs-lookup"><span data-stu-id="ba063-233">False</span></span>                                                       |
| <span data-ttu-id="ba063-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba063-234">In Global Catalog</span></span>      | <span data-ttu-id="ba063-235">否</span><span class="sxs-lookup"><span data-stu-id="ba063-235">False</span></span>                                                       |
| <span data-ttu-id="ba063-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba063-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba063-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba063-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="ba063-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba063-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba063-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-240">Search-Flags</span></span>           | <span data-ttu-id="ba063-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba063-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="ba063-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-242">System-Flags</span></span>           | <span data-ttu-id="ba063-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba063-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="ba063-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba063-244">Classes used in</span></span>        | [<span data-ttu-id="ba063-245">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="ba063-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ba063-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba063-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ba063-247">進入</span><span class="sxs-lookup"><span data-stu-id="ba063-247">Entry</span></span> | <span data-ttu-id="ba063-248">值</span><span class="sxs-lookup"><span data-stu-id="ba063-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ba063-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba063-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba063-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba063-251">System-Only</span></span>            | <span data-ttu-id="ba063-252">否</span><span class="sxs-lookup"><span data-stu-id="ba063-252">False</span></span>                                                       |
| <span data-ttu-id="ba063-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba063-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ba063-254">對</span><span class="sxs-lookup"><span data-stu-id="ba063-254">True</span></span>                                                        |
| <span data-ttu-id="ba063-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba063-255">Is Indexed</span></span>             | <span data-ttu-id="ba063-256">否</span><span class="sxs-lookup"><span data-stu-id="ba063-256">False</span></span>                                                       |
| <span data-ttu-id="ba063-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba063-257">In Global Catalog</span></span>      | <span data-ttu-id="ba063-258">否</span><span class="sxs-lookup"><span data-stu-id="ba063-258">False</span></span>                                                       |
| <span data-ttu-id="ba063-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba063-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba063-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba063-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="ba063-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba063-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba063-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-263">Search-Flags</span></span>           | <span data-ttu-id="ba063-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba063-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="ba063-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-265">System-Flags</span></span>           | <span data-ttu-id="ba063-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba063-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="ba063-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba063-267">Classes used in</span></span>        | [<span data-ttu-id="ba063-268">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="ba063-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ba063-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ba063-269">Windows Server 2012</span></span>



| <span data-ttu-id="ba063-270">進入</span><span class="sxs-lookup"><span data-stu-id="ba063-270">Entry</span></span> | <span data-ttu-id="ba063-271">值</span><span class="sxs-lookup"><span data-stu-id="ba063-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ba063-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba063-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba063-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="ba063-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba063-274">System-Only</span></span>            | <span data-ttu-id="ba063-275">否</span><span class="sxs-lookup"><span data-stu-id="ba063-275">False</span></span>                                                       |
| <span data-ttu-id="ba063-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba063-276">Is-Single-Valued</span></span>       | <span data-ttu-id="ba063-277">對</span><span class="sxs-lookup"><span data-stu-id="ba063-277">True</span></span>                                                        |
| <span data-ttu-id="ba063-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba063-278">Is Indexed</span></span>             | <span data-ttu-id="ba063-279">否</span><span class="sxs-lookup"><span data-stu-id="ba063-279">False</span></span>                                                       |
| <span data-ttu-id="ba063-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba063-280">In Global Catalog</span></span>      | <span data-ttu-id="ba063-281">否</span><span class="sxs-lookup"><span data-stu-id="ba063-281">False</span></span>                                                       |
| <span data-ttu-id="ba063-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba063-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba063-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba063-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="ba063-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba063-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba063-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="ba063-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-286">Search-Flags</span></span>           | <span data-ttu-id="ba063-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba063-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="ba063-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba063-288">System-Flags</span></span>           | <span data-ttu-id="ba063-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba063-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="ba063-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba063-290">Classes used in</span></span>        | [<span data-ttu-id="ba063-291">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="ba063-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 






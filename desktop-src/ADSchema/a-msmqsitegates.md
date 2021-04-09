---
title: MSMQ-網站-閘道屬性
description: MSMQ 路由伺服器的 DNs 清單，所有網站之間的流量都必須路由傳送。
ms.assetid: 4c00553e-6439-4fad-974c-3bfbb61d8f2d
ms.tgt_platform: multiple
keywords:
- MSMQ-網站-閘道屬性 AD 架構
- mSMQSiteGates 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Site-Gates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b970c979bb34ef0854755e042b6d36457c999be0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845076"
---
# <a name="msmq-site-gates-attribute"></a><span data-ttu-id="9604e-105">MSMQ-網站-閘道屬性</span><span class="sxs-lookup"><span data-stu-id="9604e-105">MSMQ-Site-Gates attribute</span></span>

<span data-ttu-id="9604e-106">MSMQ 路由伺服器的 DNs 清單，所有網站之間的流量都必須路由傳送。</span><span class="sxs-lookup"><span data-stu-id="9604e-106">The list of DNs for MSMQ routing servers, through which all traffic between sites must be routed.</span></span>



| <span data-ttu-id="9604e-107">進入</span><span class="sxs-lookup"><span data-stu-id="9604e-107">Entry</span></span> | <span data-ttu-id="9604e-108">值</span><span class="sxs-lookup"><span data-stu-id="9604e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="9604e-109">CN</span><span class="sxs-lookup"><span data-stu-id="9604e-109">CN</span></span>                | <span data-ttu-id="9604e-110">MSMQ-網站-閘道</span><span class="sxs-lookup"><span data-stu-id="9604e-110">MSMQ-Site-Gates</span></span>                         |
| <span data-ttu-id="9604e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9604e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9604e-112">mSMQSiteGates</span><span class="sxs-lookup"><span data-stu-id="9604e-112">mSMQSiteGates</span></span>                           |
| <span data-ttu-id="9604e-113">大小</span><span class="sxs-lookup"><span data-stu-id="9604e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="9604e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9604e-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="9604e-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9604e-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="9604e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9604e-116">Attribute-Id</span></span>      | <span data-ttu-id="9604e-117">1.2.840.113556.1.4.945</span><span class="sxs-lookup"><span data-stu-id="9604e-117">1.2.840.113556.1.4.945</span></span>                  |
| <span data-ttu-id="9604e-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9604e-118">System-Id-Guid</span></span>    | <span data-ttu-id="9604e-119">9a0dc339-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="9604e-119">9a0dc339-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="9604e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="9604e-120">Syntax</span></span>            | [<span data-ttu-id="9604e-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9604e-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="9604e-122">實作</span><span class="sxs-lookup"><span data-stu-id="9604e-122">Implementations</span></span>

-   [<span data-ttu-id="9604e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9604e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9604e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9604e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9604e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9604e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9604e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9604e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9604e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9604e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9604e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9604e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9604e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9604e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9604e-130">進入</span><span class="sxs-lookup"><span data-stu-id="9604e-130">Entry</span></span> | <span data-ttu-id="9604e-131">值</span><span class="sxs-lookup"><span data-stu-id="9604e-131">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="9604e-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9604e-132">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9604e-133">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9604e-134">System-Only</span></span>            | <span data-ttu-id="9604e-135">否</span><span class="sxs-lookup"><span data-stu-id="9604e-135">False</span></span>                                               |
| <span data-ttu-id="9604e-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9604e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9604e-137">否</span><span class="sxs-lookup"><span data-stu-id="9604e-137">False</span></span>                                               |
| <span data-ttu-id="9604e-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9604e-138">Is Indexed</span></span>             | <span data-ttu-id="9604e-139">否</span><span class="sxs-lookup"><span data-stu-id="9604e-139">False</span></span>                                               |
| <span data-ttu-id="9604e-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9604e-140">In Global Catalog</span></span>      | <span data-ttu-id="9604e-141">否</span><span class="sxs-lookup"><span data-stu-id="9604e-141">False</span></span>                                               |
| <span data-ttu-id="9604e-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9604e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9604e-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9604e-143">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="9604e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9604e-144">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9604e-145">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-146">Search-Flags</span></span>           | <span data-ttu-id="9604e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9604e-147">0x00000000</span></span>                                          |
| <span data-ttu-id="9604e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-148">System-Flags</span></span>           | <span data-ttu-id="9604e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9604e-149">0x00000010</span></span>                                          |
| <span data-ttu-id="9604e-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9604e-150">Classes used in</span></span>        | [<span data-ttu-id="9604e-151">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="9604e-151">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9604e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9604e-152">Windows Server 2003</span></span>



| <span data-ttu-id="9604e-153">進入</span><span class="sxs-lookup"><span data-stu-id="9604e-153">Entry</span></span> | <span data-ttu-id="9604e-154">值</span><span class="sxs-lookup"><span data-stu-id="9604e-154">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="9604e-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9604e-155">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9604e-156">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9604e-157">System-Only</span></span>            | <span data-ttu-id="9604e-158">否</span><span class="sxs-lookup"><span data-stu-id="9604e-158">False</span></span>                                               |
| <span data-ttu-id="9604e-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9604e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9604e-160">否</span><span class="sxs-lookup"><span data-stu-id="9604e-160">False</span></span>                                               |
| <span data-ttu-id="9604e-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9604e-161">Is Indexed</span></span>             | <span data-ttu-id="9604e-162">否</span><span class="sxs-lookup"><span data-stu-id="9604e-162">False</span></span>                                               |
| <span data-ttu-id="9604e-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9604e-163">In Global Catalog</span></span>      | <span data-ttu-id="9604e-164">否</span><span class="sxs-lookup"><span data-stu-id="9604e-164">False</span></span>                                               |
| <span data-ttu-id="9604e-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9604e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9604e-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9604e-166">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="9604e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9604e-167">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9604e-168">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-169">Search-Flags</span></span>           | <span data-ttu-id="9604e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9604e-170">0x00000000</span></span>                                          |
| <span data-ttu-id="9604e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-171">System-Flags</span></span>           | <span data-ttu-id="9604e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9604e-172">0x00000010</span></span>                                          |
| <span data-ttu-id="9604e-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9604e-173">Classes used in</span></span>        | [<span data-ttu-id="9604e-174">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="9604e-174">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9604e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9604e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9604e-176">進入</span><span class="sxs-lookup"><span data-stu-id="9604e-176">Entry</span></span> | <span data-ttu-id="9604e-177">值</span><span class="sxs-lookup"><span data-stu-id="9604e-177">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="9604e-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9604e-178">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9604e-179">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9604e-180">System-Only</span></span>            | <span data-ttu-id="9604e-181">否</span><span class="sxs-lookup"><span data-stu-id="9604e-181">False</span></span>                                               |
| <span data-ttu-id="9604e-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9604e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9604e-183">否</span><span class="sxs-lookup"><span data-stu-id="9604e-183">False</span></span>                                               |
| <span data-ttu-id="9604e-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9604e-184">Is Indexed</span></span>             | <span data-ttu-id="9604e-185">否</span><span class="sxs-lookup"><span data-stu-id="9604e-185">False</span></span>                                               |
| <span data-ttu-id="9604e-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9604e-186">In Global Catalog</span></span>      | <span data-ttu-id="9604e-187">否</span><span class="sxs-lookup"><span data-stu-id="9604e-187">False</span></span>                                               |
| <span data-ttu-id="9604e-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9604e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9604e-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9604e-189">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="9604e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9604e-190">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9604e-191">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-192">Search-Flags</span></span>           | <span data-ttu-id="9604e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9604e-193">0x00000000</span></span>                                          |
| <span data-ttu-id="9604e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-194">System-Flags</span></span>           | <span data-ttu-id="9604e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9604e-195">0x00000010</span></span>                                          |
| <span data-ttu-id="9604e-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9604e-196">Classes used in</span></span>        | [<span data-ttu-id="9604e-197">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="9604e-197">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9604e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9604e-198">Windows Server 2008</span></span>



| <span data-ttu-id="9604e-199">進入</span><span class="sxs-lookup"><span data-stu-id="9604e-199">Entry</span></span> | <span data-ttu-id="9604e-200">值</span><span class="sxs-lookup"><span data-stu-id="9604e-200">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="9604e-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9604e-201">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9604e-202">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9604e-203">System-Only</span></span>            | <span data-ttu-id="9604e-204">否</span><span class="sxs-lookup"><span data-stu-id="9604e-204">False</span></span>                                               |
| <span data-ttu-id="9604e-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9604e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9604e-206">否</span><span class="sxs-lookup"><span data-stu-id="9604e-206">False</span></span>                                               |
| <span data-ttu-id="9604e-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9604e-207">Is Indexed</span></span>             | <span data-ttu-id="9604e-208">否</span><span class="sxs-lookup"><span data-stu-id="9604e-208">False</span></span>                                               |
| <span data-ttu-id="9604e-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9604e-209">In Global Catalog</span></span>      | <span data-ttu-id="9604e-210">否</span><span class="sxs-lookup"><span data-stu-id="9604e-210">False</span></span>                                               |
| <span data-ttu-id="9604e-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9604e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9604e-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9604e-212">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="9604e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9604e-213">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9604e-214">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-215">Search-Flags</span></span>           | <span data-ttu-id="9604e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9604e-216">0x00000000</span></span>                                          |
| <span data-ttu-id="9604e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-217">System-Flags</span></span>           | <span data-ttu-id="9604e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9604e-218">0x00000010</span></span>                                          |
| <span data-ttu-id="9604e-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9604e-219">Classes used in</span></span>        | [<span data-ttu-id="9604e-220">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="9604e-220">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9604e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9604e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9604e-222">進入</span><span class="sxs-lookup"><span data-stu-id="9604e-222">Entry</span></span> | <span data-ttu-id="9604e-223">值</span><span class="sxs-lookup"><span data-stu-id="9604e-223">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="9604e-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9604e-224">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9604e-225">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="9604e-226">System-Only</span></span>            | <span data-ttu-id="9604e-227">否</span><span class="sxs-lookup"><span data-stu-id="9604e-227">False</span></span>                                               |
| <span data-ttu-id="9604e-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9604e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="9604e-229">否</span><span class="sxs-lookup"><span data-stu-id="9604e-229">False</span></span>                                               |
| <span data-ttu-id="9604e-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9604e-230">Is Indexed</span></span>             | <span data-ttu-id="9604e-231">否</span><span class="sxs-lookup"><span data-stu-id="9604e-231">False</span></span>                                               |
| <span data-ttu-id="9604e-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9604e-232">In Global Catalog</span></span>      | <span data-ttu-id="9604e-233">否</span><span class="sxs-lookup"><span data-stu-id="9604e-233">False</span></span>                                               |
| <span data-ttu-id="9604e-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9604e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="9604e-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9604e-235">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="9604e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9604e-236">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9604e-237">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-238">Search-Flags</span></span>           | <span data-ttu-id="9604e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9604e-239">0x00000000</span></span>                                          |
| <span data-ttu-id="9604e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-240">System-Flags</span></span>           | <span data-ttu-id="9604e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9604e-241">0x00000010</span></span>                                          |
| <span data-ttu-id="9604e-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9604e-242">Classes used in</span></span>        | [<span data-ttu-id="9604e-243">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="9604e-243">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9604e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9604e-244">Windows Server 2012</span></span>



| <span data-ttu-id="9604e-245">進入</span><span class="sxs-lookup"><span data-stu-id="9604e-245">Entry</span></span> | <span data-ttu-id="9604e-246">值</span><span class="sxs-lookup"><span data-stu-id="9604e-246">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="9604e-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9604e-247">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9604e-248">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="9604e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="9604e-249">System-Only</span></span>            | <span data-ttu-id="9604e-250">否</span><span class="sxs-lookup"><span data-stu-id="9604e-250">False</span></span>                                               |
| <span data-ttu-id="9604e-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9604e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="9604e-252">否</span><span class="sxs-lookup"><span data-stu-id="9604e-252">False</span></span>                                               |
| <span data-ttu-id="9604e-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9604e-253">Is Indexed</span></span>             | <span data-ttu-id="9604e-254">否</span><span class="sxs-lookup"><span data-stu-id="9604e-254">False</span></span>                                               |
| <span data-ttu-id="9604e-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9604e-255">In Global Catalog</span></span>      | <span data-ttu-id="9604e-256">否</span><span class="sxs-lookup"><span data-stu-id="9604e-256">False</span></span>                                               |
| <span data-ttu-id="9604e-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9604e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="9604e-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9604e-258">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="9604e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9604e-259">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9604e-260">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="9604e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-261">Search-Flags</span></span>           | <span data-ttu-id="9604e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9604e-262">0x00000000</span></span>                                          |
| <span data-ttu-id="9604e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9604e-263">System-Flags</span></span>           | <span data-ttu-id="9604e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9604e-264">0x00000010</span></span>                                          |
| <span data-ttu-id="9604e-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9604e-265">Classes used in</span></span>        | [<span data-ttu-id="9604e-266">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="9604e-266">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



 

 






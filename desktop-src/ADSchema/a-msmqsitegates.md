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
# <a name="msmq-site-gates-attribute"></a><span data-ttu-id="f5a93-105">MSMQ-網站-閘道屬性</span><span class="sxs-lookup"><span data-stu-id="f5a93-105">MSMQ-Site-Gates attribute</span></span>

<span data-ttu-id="f5a93-106">MSMQ 路由伺服器的 DNs 清單，所有網站之間的流量都必須路由傳送。</span><span class="sxs-lookup"><span data-stu-id="f5a93-106">The list of DNs for MSMQ routing servers, through which all traffic between sites must be routed.</span></span>



| <span data-ttu-id="f5a93-107">進入</span><span class="sxs-lookup"><span data-stu-id="f5a93-107">Entry</span></span> | <span data-ttu-id="f5a93-108">值</span><span class="sxs-lookup"><span data-stu-id="f5a93-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f5a93-109">CN</span><span class="sxs-lookup"><span data-stu-id="f5a93-109">CN</span></span>                | <span data-ttu-id="f5a93-110">MSMQ-網站-閘道</span><span class="sxs-lookup"><span data-stu-id="f5a93-110">MSMQ-Site-Gates</span></span>                         |
| <span data-ttu-id="f5a93-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f5a93-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f5a93-112">mSMQSiteGates</span><span class="sxs-lookup"><span data-stu-id="f5a93-112">mSMQSiteGates</span></span>                           |
| <span data-ttu-id="f5a93-113">大小</span><span class="sxs-lookup"><span data-stu-id="f5a93-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f5a93-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f5a93-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="f5a93-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f5a93-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f5a93-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f5a93-116">Attribute-Id</span></span>      | <span data-ttu-id="f5a93-117">1.2.840.113556.1.4.945</span><span class="sxs-lookup"><span data-stu-id="f5a93-117">1.2.840.113556.1.4.945</span></span>                  |
| <span data-ttu-id="f5a93-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f5a93-118">System-Id-Guid</span></span>    | <span data-ttu-id="f5a93-119">9a0dc339-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="f5a93-119">9a0dc339-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="f5a93-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5a93-120">Syntax</span></span>            | [<span data-ttu-id="f5a93-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f5a93-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f5a93-122">實作</span><span class="sxs-lookup"><span data-stu-id="f5a93-122">Implementations</span></span>

-   [<span data-ttu-id="f5a93-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f5a93-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f5a93-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f5a93-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f5a93-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f5a93-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f5a93-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f5a93-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f5a93-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f5a93-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f5a93-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f5a93-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f5a93-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5a93-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f5a93-130">進入</span><span class="sxs-lookup"><span data-stu-id="f5a93-130">Entry</span></span> | <span data-ttu-id="f5a93-131">值</span><span class="sxs-lookup"><span data-stu-id="f5a93-131">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="f5a93-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f5a93-132">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5a93-133">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5a93-134">System-Only</span></span>            | <span data-ttu-id="f5a93-135">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-135">False</span></span>                                               |
| <span data-ttu-id="f5a93-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f5a93-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f5a93-137">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-137">False</span></span>                                               |
| <span data-ttu-id="f5a93-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f5a93-138">Is Indexed</span></span>             | <span data-ttu-id="f5a93-139">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-139">False</span></span>                                               |
| <span data-ttu-id="f5a93-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f5a93-140">In Global Catalog</span></span>      | <span data-ttu-id="f5a93-141">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-141">False</span></span>                                               |
| <span data-ttu-id="f5a93-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f5a93-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5a93-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f5a93-143">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="f5a93-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5a93-144">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5a93-145">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-146">Search-Flags</span></span>           | <span data-ttu-id="f5a93-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5a93-147">0x00000000</span></span>                                          |
| <span data-ttu-id="f5a93-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-148">System-Flags</span></span>           | <span data-ttu-id="f5a93-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5a93-149">0x00000010</span></span>                                          |
| <span data-ttu-id="f5a93-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f5a93-150">Classes used in</span></span>        | [<span data-ttu-id="f5a93-151">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="f5a93-151">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f5a93-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f5a93-152">Windows Server 2003</span></span>



| <span data-ttu-id="f5a93-153">進入</span><span class="sxs-lookup"><span data-stu-id="f5a93-153">Entry</span></span> | <span data-ttu-id="f5a93-154">值</span><span class="sxs-lookup"><span data-stu-id="f5a93-154">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="f5a93-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f5a93-155">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5a93-156">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5a93-157">System-Only</span></span>            | <span data-ttu-id="f5a93-158">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-158">False</span></span>                                               |
| <span data-ttu-id="f5a93-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f5a93-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f5a93-160">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-160">False</span></span>                                               |
| <span data-ttu-id="f5a93-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f5a93-161">Is Indexed</span></span>             | <span data-ttu-id="f5a93-162">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-162">False</span></span>                                               |
| <span data-ttu-id="f5a93-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f5a93-163">In Global Catalog</span></span>      | <span data-ttu-id="f5a93-164">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-164">False</span></span>                                               |
| <span data-ttu-id="f5a93-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f5a93-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5a93-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f5a93-166">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="f5a93-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5a93-167">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5a93-168">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-169">Search-Flags</span></span>           | <span data-ttu-id="f5a93-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5a93-170">0x00000000</span></span>                                          |
| <span data-ttu-id="f5a93-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-171">System-Flags</span></span>           | <span data-ttu-id="f5a93-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5a93-172">0x00000010</span></span>                                          |
| <span data-ttu-id="f5a93-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f5a93-173">Classes used in</span></span>        | [<span data-ttu-id="f5a93-174">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="f5a93-174">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f5a93-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f5a93-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f5a93-176">進入</span><span class="sxs-lookup"><span data-stu-id="f5a93-176">Entry</span></span> | <span data-ttu-id="f5a93-177">值</span><span class="sxs-lookup"><span data-stu-id="f5a93-177">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="f5a93-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f5a93-178">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5a93-179">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5a93-180">System-Only</span></span>            | <span data-ttu-id="f5a93-181">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-181">False</span></span>                                               |
| <span data-ttu-id="f5a93-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f5a93-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f5a93-183">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-183">False</span></span>                                               |
| <span data-ttu-id="f5a93-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f5a93-184">Is Indexed</span></span>             | <span data-ttu-id="f5a93-185">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-185">False</span></span>                                               |
| <span data-ttu-id="f5a93-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f5a93-186">In Global Catalog</span></span>      | <span data-ttu-id="f5a93-187">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-187">False</span></span>                                               |
| <span data-ttu-id="f5a93-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f5a93-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5a93-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f5a93-189">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="f5a93-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5a93-190">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5a93-191">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-192">Search-Flags</span></span>           | <span data-ttu-id="f5a93-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5a93-193">0x00000000</span></span>                                          |
| <span data-ttu-id="f5a93-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-194">System-Flags</span></span>           | <span data-ttu-id="f5a93-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5a93-195">0x00000010</span></span>                                          |
| <span data-ttu-id="f5a93-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f5a93-196">Classes used in</span></span>        | [<span data-ttu-id="f5a93-197">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="f5a93-197">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f5a93-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5a93-198">Windows Server 2008</span></span>



| <span data-ttu-id="f5a93-199">進入</span><span class="sxs-lookup"><span data-stu-id="f5a93-199">Entry</span></span> | <span data-ttu-id="f5a93-200">值</span><span class="sxs-lookup"><span data-stu-id="f5a93-200">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="f5a93-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f5a93-201">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5a93-202">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5a93-203">System-Only</span></span>            | <span data-ttu-id="f5a93-204">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-204">False</span></span>                                               |
| <span data-ttu-id="f5a93-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f5a93-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f5a93-206">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-206">False</span></span>                                               |
| <span data-ttu-id="f5a93-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f5a93-207">Is Indexed</span></span>             | <span data-ttu-id="f5a93-208">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-208">False</span></span>                                               |
| <span data-ttu-id="f5a93-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f5a93-209">In Global Catalog</span></span>      | <span data-ttu-id="f5a93-210">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-210">False</span></span>                                               |
| <span data-ttu-id="f5a93-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f5a93-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5a93-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f5a93-212">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="f5a93-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5a93-213">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5a93-214">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-215">Search-Flags</span></span>           | <span data-ttu-id="f5a93-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5a93-216">0x00000000</span></span>                                          |
| <span data-ttu-id="f5a93-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-217">System-Flags</span></span>           | <span data-ttu-id="f5a93-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5a93-218">0x00000010</span></span>                                          |
| <span data-ttu-id="f5a93-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f5a93-219">Classes used in</span></span>        | [<span data-ttu-id="f5a93-220">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="f5a93-220">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f5a93-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f5a93-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f5a93-222">進入</span><span class="sxs-lookup"><span data-stu-id="f5a93-222">Entry</span></span> | <span data-ttu-id="f5a93-223">值</span><span class="sxs-lookup"><span data-stu-id="f5a93-223">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="f5a93-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f5a93-224">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5a93-225">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5a93-226">System-Only</span></span>            | <span data-ttu-id="f5a93-227">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-227">False</span></span>                                               |
| <span data-ttu-id="f5a93-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f5a93-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f5a93-229">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-229">False</span></span>                                               |
| <span data-ttu-id="f5a93-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f5a93-230">Is Indexed</span></span>             | <span data-ttu-id="f5a93-231">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-231">False</span></span>                                               |
| <span data-ttu-id="f5a93-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f5a93-232">In Global Catalog</span></span>      | <span data-ttu-id="f5a93-233">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-233">False</span></span>                                               |
| <span data-ttu-id="f5a93-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f5a93-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5a93-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f5a93-235">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="f5a93-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5a93-236">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5a93-237">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-238">Search-Flags</span></span>           | <span data-ttu-id="f5a93-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5a93-239">0x00000000</span></span>                                          |
| <span data-ttu-id="f5a93-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-240">System-Flags</span></span>           | <span data-ttu-id="f5a93-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5a93-241">0x00000010</span></span>                                          |
| <span data-ttu-id="f5a93-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f5a93-242">Classes used in</span></span>        | [<span data-ttu-id="f5a93-243">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="f5a93-243">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f5a93-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5a93-244">Windows Server 2012</span></span>



| <span data-ttu-id="f5a93-245">進入</span><span class="sxs-lookup"><span data-stu-id="f5a93-245">Entry</span></span> | <span data-ttu-id="f5a93-246">值</span><span class="sxs-lookup"><span data-stu-id="f5a93-246">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="f5a93-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f5a93-247">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5a93-248">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="f5a93-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5a93-249">System-Only</span></span>            | <span data-ttu-id="f5a93-250">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-250">False</span></span>                                               |
| <span data-ttu-id="f5a93-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f5a93-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f5a93-252">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-252">False</span></span>                                               |
| <span data-ttu-id="f5a93-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f5a93-253">Is Indexed</span></span>             | <span data-ttu-id="f5a93-254">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-254">False</span></span>                                               |
| <span data-ttu-id="f5a93-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f5a93-255">In Global Catalog</span></span>      | <span data-ttu-id="f5a93-256">否</span><span class="sxs-lookup"><span data-stu-id="f5a93-256">False</span></span>                                               |
| <span data-ttu-id="f5a93-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f5a93-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5a93-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f5a93-258">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="f5a93-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5a93-259">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5a93-260">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="f5a93-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-261">Search-Flags</span></span>           | <span data-ttu-id="f5a93-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5a93-262">0x00000000</span></span>                                          |
| <span data-ttu-id="f5a93-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5a93-263">System-Flags</span></span>           | <span data-ttu-id="f5a93-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5a93-264">0x00000010</span></span>                                          |
| <span data-ttu-id="f5a93-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f5a93-265">Classes used in</span></span>        | [<span data-ttu-id="f5a93-266">**MSMQ-網站連結**</span><span class="sxs-lookup"><span data-stu-id="f5a93-266">**MSMQ-Site-Link**</span></span>](c-msmqsitelink.md)<br/> |



 

 






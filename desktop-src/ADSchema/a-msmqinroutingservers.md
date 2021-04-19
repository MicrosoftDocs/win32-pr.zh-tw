---
title: MSMQ 路由-伺服器屬性
description: MSMQ 路由伺服器的 DN 連結，此伺服器會透過這些伺服器來路由傳送至此電腦的所有連入流量。
ms.assetid: a54d79a7-52f2-49ac-b23f-c3365a1f6921
ms.tgt_platform: multiple
keywords:
- MSMQ 路由伺服器屬性 AD 架構
- mSMQInRoutingServers 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-In-Routing-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46bd9f21552362ad4dceb5110af84b09bb096d5c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973926"
---
# <a name="msmq-in-routing-servers-attribute"></a><span data-ttu-id="d87ac-105">MSMQ 路由-伺服器屬性</span><span class="sxs-lookup"><span data-stu-id="d87ac-105">MSMQ-In-Routing-Servers attribute</span></span>

<span data-ttu-id="d87ac-106">MSMQ 路由伺服器的 DN 連結，此伺服器會透過這些伺服器來路由傳送至此電腦的所有連入流量。</span><span class="sxs-lookup"><span data-stu-id="d87ac-106">DN links to MSMQ routing servers through which all incoming traffic to this computer should be routed.</span></span>



| <span data-ttu-id="d87ac-107">進入</span><span class="sxs-lookup"><span data-stu-id="d87ac-107">Entry</span></span> | <span data-ttu-id="d87ac-108">值</span><span class="sxs-lookup"><span data-stu-id="d87ac-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d87ac-109">CN</span><span class="sxs-lookup"><span data-stu-id="d87ac-109">CN</span></span>                | <span data-ttu-id="d87ac-110">MSMQ 路由傳送伺服器</span><span class="sxs-lookup"><span data-stu-id="d87ac-110">MSMQ-In-Routing-Servers</span></span>                 |
| <span data-ttu-id="d87ac-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d87ac-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d87ac-112">mSMQInRoutingServers</span><span class="sxs-lookup"><span data-stu-id="d87ac-112">mSMQInRoutingServers</span></span>                    |
| <span data-ttu-id="d87ac-113">大小</span><span class="sxs-lookup"><span data-stu-id="d87ac-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="d87ac-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d87ac-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="d87ac-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d87ac-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="d87ac-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d87ac-116">Attribute-Id</span></span>      | <span data-ttu-id="d87ac-117">1.2.840.113556.1.4.929</span><span class="sxs-lookup"><span data-stu-id="d87ac-117">1.2.840.113556.1.4.929</span></span>                  |
| <span data-ttu-id="d87ac-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d87ac-118">System-Id-Guid</span></span>    | <span data-ttu-id="d87ac-119">9a0dc32c-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="d87ac-119">9a0dc32c-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="d87ac-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="d87ac-120">Syntax</span></span>            | [<span data-ttu-id="d87ac-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d87ac-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d87ac-122">實作</span><span class="sxs-lookup"><span data-stu-id="d87ac-122">Implementations</span></span>

-   [<span data-ttu-id="d87ac-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d87ac-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d87ac-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d87ac-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d87ac-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d87ac-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d87ac-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d87ac-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d87ac-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d87ac-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d87ac-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d87ac-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d87ac-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d87ac-129">Windows 2000 Server</span></span>



| <span data-ttu-id="d87ac-130">進入</span><span class="sxs-lookup"><span data-stu-id="d87ac-130">Entry</span></span> | <span data-ttu-id="d87ac-131">值</span><span class="sxs-lookup"><span data-stu-id="d87ac-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d87ac-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d87ac-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d87ac-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="d87ac-134">System-Only</span></span>            | <span data-ttu-id="d87ac-135">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-135">False</span></span>                                                        |
| <span data-ttu-id="d87ac-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d87ac-136">Is-Single-Valued</span></span>       | <span data-ttu-id="d87ac-137">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-137">False</span></span>                                                        |
| <span data-ttu-id="d87ac-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d87ac-138">Is Indexed</span></span>             | <span data-ttu-id="d87ac-139">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-139">False</span></span>                                                        |
| <span data-ttu-id="d87ac-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d87ac-140">In Global Catalog</span></span>      | <span data-ttu-id="d87ac-141">對</span><span class="sxs-lookup"><span data-stu-id="d87ac-141">True</span></span>                                                         |
| <span data-ttu-id="d87ac-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d87ac-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="d87ac-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d87ac-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d87ac-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d87ac-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d87ac-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-146">Search-Flags</span></span>           | <span data-ttu-id="d87ac-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d87ac-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="d87ac-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-148">System-Flags</span></span>           | <span data-ttu-id="d87ac-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d87ac-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="d87ac-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d87ac-150">Classes used in</span></span>        | [<span data-ttu-id="d87ac-151">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="d87ac-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d87ac-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d87ac-152">Windows Server 2003</span></span>



| <span data-ttu-id="d87ac-153">進入</span><span class="sxs-lookup"><span data-stu-id="d87ac-153">Entry</span></span> | <span data-ttu-id="d87ac-154">值</span><span class="sxs-lookup"><span data-stu-id="d87ac-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d87ac-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d87ac-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d87ac-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="d87ac-157">System-Only</span></span>            | <span data-ttu-id="d87ac-158">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-158">False</span></span>                                                        |
| <span data-ttu-id="d87ac-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d87ac-159">Is-Single-Valued</span></span>       | <span data-ttu-id="d87ac-160">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-160">False</span></span>                                                        |
| <span data-ttu-id="d87ac-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d87ac-161">Is Indexed</span></span>             | <span data-ttu-id="d87ac-162">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-162">False</span></span>                                                        |
| <span data-ttu-id="d87ac-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d87ac-163">In Global Catalog</span></span>      | <span data-ttu-id="d87ac-164">對</span><span class="sxs-lookup"><span data-stu-id="d87ac-164">True</span></span>                                                         |
| <span data-ttu-id="d87ac-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d87ac-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="d87ac-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d87ac-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d87ac-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d87ac-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d87ac-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-169">Search-Flags</span></span>           | <span data-ttu-id="d87ac-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d87ac-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="d87ac-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-171">System-Flags</span></span>           | <span data-ttu-id="d87ac-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d87ac-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="d87ac-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d87ac-173">Classes used in</span></span>        | [<span data-ttu-id="d87ac-174">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="d87ac-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d87ac-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d87ac-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d87ac-176">進入</span><span class="sxs-lookup"><span data-stu-id="d87ac-176">Entry</span></span> | <span data-ttu-id="d87ac-177">值</span><span class="sxs-lookup"><span data-stu-id="d87ac-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d87ac-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d87ac-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d87ac-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="d87ac-180">System-Only</span></span>            | <span data-ttu-id="d87ac-181">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-181">False</span></span>                                                        |
| <span data-ttu-id="d87ac-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d87ac-182">Is-Single-Valued</span></span>       | <span data-ttu-id="d87ac-183">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-183">False</span></span>                                                        |
| <span data-ttu-id="d87ac-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d87ac-184">Is Indexed</span></span>             | <span data-ttu-id="d87ac-185">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-185">False</span></span>                                                        |
| <span data-ttu-id="d87ac-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d87ac-186">In Global Catalog</span></span>      | <span data-ttu-id="d87ac-187">對</span><span class="sxs-lookup"><span data-stu-id="d87ac-187">True</span></span>                                                         |
| <span data-ttu-id="d87ac-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d87ac-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="d87ac-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d87ac-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d87ac-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d87ac-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d87ac-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-192">Search-Flags</span></span>           | <span data-ttu-id="d87ac-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d87ac-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="d87ac-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-194">System-Flags</span></span>           | <span data-ttu-id="d87ac-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d87ac-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="d87ac-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d87ac-196">Classes used in</span></span>        | [<span data-ttu-id="d87ac-197">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="d87ac-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d87ac-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d87ac-198">Windows Server 2008</span></span>



| <span data-ttu-id="d87ac-199">進入</span><span class="sxs-lookup"><span data-stu-id="d87ac-199">Entry</span></span> | <span data-ttu-id="d87ac-200">值</span><span class="sxs-lookup"><span data-stu-id="d87ac-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d87ac-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d87ac-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d87ac-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="d87ac-203">System-Only</span></span>            | <span data-ttu-id="d87ac-204">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-204">False</span></span>                                                        |
| <span data-ttu-id="d87ac-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d87ac-205">Is-Single-Valued</span></span>       | <span data-ttu-id="d87ac-206">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-206">False</span></span>                                                        |
| <span data-ttu-id="d87ac-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d87ac-207">Is Indexed</span></span>             | <span data-ttu-id="d87ac-208">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-208">False</span></span>                                                        |
| <span data-ttu-id="d87ac-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d87ac-209">In Global Catalog</span></span>      | <span data-ttu-id="d87ac-210">對</span><span class="sxs-lookup"><span data-stu-id="d87ac-210">True</span></span>                                                         |
| <span data-ttu-id="d87ac-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d87ac-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="d87ac-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d87ac-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d87ac-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d87ac-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d87ac-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-215">Search-Flags</span></span>           | <span data-ttu-id="d87ac-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d87ac-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="d87ac-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-217">System-Flags</span></span>           | <span data-ttu-id="d87ac-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d87ac-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="d87ac-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d87ac-219">Classes used in</span></span>        | [<span data-ttu-id="d87ac-220">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="d87ac-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d87ac-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d87ac-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d87ac-222">進入</span><span class="sxs-lookup"><span data-stu-id="d87ac-222">Entry</span></span> | <span data-ttu-id="d87ac-223">值</span><span class="sxs-lookup"><span data-stu-id="d87ac-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d87ac-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d87ac-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d87ac-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="d87ac-226">System-Only</span></span>            | <span data-ttu-id="d87ac-227">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-227">False</span></span>                                                        |
| <span data-ttu-id="d87ac-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d87ac-228">Is-Single-Valued</span></span>       | <span data-ttu-id="d87ac-229">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-229">False</span></span>                                                        |
| <span data-ttu-id="d87ac-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d87ac-230">Is Indexed</span></span>             | <span data-ttu-id="d87ac-231">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-231">False</span></span>                                                        |
| <span data-ttu-id="d87ac-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d87ac-232">In Global Catalog</span></span>      | <span data-ttu-id="d87ac-233">對</span><span class="sxs-lookup"><span data-stu-id="d87ac-233">True</span></span>                                                         |
| <span data-ttu-id="d87ac-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d87ac-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="d87ac-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d87ac-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d87ac-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d87ac-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d87ac-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-238">Search-Flags</span></span>           | <span data-ttu-id="d87ac-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d87ac-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="d87ac-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-240">System-Flags</span></span>           | <span data-ttu-id="d87ac-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d87ac-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="d87ac-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d87ac-242">Classes used in</span></span>        | [<span data-ttu-id="d87ac-243">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="d87ac-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d87ac-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d87ac-244">Windows Server 2012</span></span>



| <span data-ttu-id="d87ac-245">進入</span><span class="sxs-lookup"><span data-stu-id="d87ac-245">Entry</span></span> | <span data-ttu-id="d87ac-246">值</span><span class="sxs-lookup"><span data-stu-id="d87ac-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d87ac-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d87ac-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d87ac-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d87ac-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="d87ac-249">System-Only</span></span>            | <span data-ttu-id="d87ac-250">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-250">False</span></span>                                                        |
| <span data-ttu-id="d87ac-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d87ac-251">Is-Single-Valued</span></span>       | <span data-ttu-id="d87ac-252">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-252">False</span></span>                                                        |
| <span data-ttu-id="d87ac-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d87ac-253">Is Indexed</span></span>             | <span data-ttu-id="d87ac-254">否</span><span class="sxs-lookup"><span data-stu-id="d87ac-254">False</span></span>                                                        |
| <span data-ttu-id="d87ac-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d87ac-255">In Global Catalog</span></span>      | <span data-ttu-id="d87ac-256">對</span><span class="sxs-lookup"><span data-stu-id="d87ac-256">True</span></span>                                                         |
| <span data-ttu-id="d87ac-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d87ac-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="d87ac-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d87ac-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d87ac-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d87ac-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d87ac-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d87ac-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-261">Search-Flags</span></span>           | <span data-ttu-id="d87ac-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d87ac-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="d87ac-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d87ac-263">System-Flags</span></span>           | <span data-ttu-id="d87ac-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d87ac-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="d87ac-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d87ac-265">Classes used in</span></span>        | [<span data-ttu-id="d87ac-266">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="d87ac-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 






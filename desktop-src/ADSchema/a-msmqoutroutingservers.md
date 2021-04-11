---
title: MSMQ 輸出路由-伺服器屬性
description: MSMQ 路由伺服器的 DN 連結，此電腦的所有連出流量都應路由傳送。
ms.assetid: 169558e4-d2a6-4555-bc5f-7e6a89e51789
ms.tgt_platform: multiple
keywords:
- MSMQ 輸出路由伺服器屬性 AD 架構
- mSMQOutRoutingServers 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Out-Routing-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc2265b2d809b7a73cd19faace87473552471a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845091"
---
# <a name="msmq-out-routing-servers-attribute"></a><span data-ttu-id="c97c4-105">MSMQ 輸出路由-伺服器屬性</span><span class="sxs-lookup"><span data-stu-id="c97c4-105">MSMQ-Out-Routing-Servers attribute</span></span>

<span data-ttu-id="c97c4-106">MSMQ 路由伺服器的 DN 連結，此電腦的所有連出流量都應路由傳送。</span><span class="sxs-lookup"><span data-stu-id="c97c4-106">DN links to MSMQ routing servers through which all outgoing traffic for this computer should be routed.</span></span>



| <span data-ttu-id="c97c4-107">進入</span><span class="sxs-lookup"><span data-stu-id="c97c4-107">Entry</span></span> | <span data-ttu-id="c97c4-108">值</span><span class="sxs-lookup"><span data-stu-id="c97c4-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c97c4-109">CN</span><span class="sxs-lookup"><span data-stu-id="c97c4-109">CN</span></span>                | <span data-ttu-id="c97c4-110">MSMQ 輸出路由-伺服器</span><span class="sxs-lookup"><span data-stu-id="c97c4-110">MSMQ-Out-Routing-Servers</span></span>                |
| <span data-ttu-id="c97c4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c97c4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c97c4-112">mSMQOutRoutingServers</span><span class="sxs-lookup"><span data-stu-id="c97c4-112">mSMQOutRoutingServers</span></span>                   |
| <span data-ttu-id="c97c4-113">大小</span><span class="sxs-lookup"><span data-stu-id="c97c4-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c97c4-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c97c4-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c97c4-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c97c4-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c97c4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c97c4-116">Attribute-Id</span></span>      | <span data-ttu-id="c97c4-117">1.2.840.113556.1.4.928</span><span class="sxs-lookup"><span data-stu-id="c97c4-117">1.2.840.113556.1.4.928</span></span>                  |
| <span data-ttu-id="c97c4-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c97c4-118">System-Id-Guid</span></span>    | <span data-ttu-id="c97c4-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="c97c4-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="c97c4-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97c4-120">Syntax</span></span>            | [<span data-ttu-id="c97c4-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c97c4-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c97c4-122">實作</span><span class="sxs-lookup"><span data-stu-id="c97c4-122">Implementations</span></span>

-   [<span data-ttu-id="c97c4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c97c4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c97c4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c97c4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c97c4-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c97c4-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c97c4-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c97c4-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c97c4-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c97c4-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c97c4-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c97c4-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c97c4-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c97c4-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c97c4-130">進入</span><span class="sxs-lookup"><span data-stu-id="c97c4-130">Entry</span></span> | <span data-ttu-id="c97c4-131">值</span><span class="sxs-lookup"><span data-stu-id="c97c4-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c97c4-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c97c4-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c4-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c4-134">System-Only</span></span>            | <span data-ttu-id="c97c4-135">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-135">False</span></span>                                                        |
| <span data-ttu-id="c97c4-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c97c4-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c4-137">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-137">False</span></span>                                                        |
| <span data-ttu-id="c97c4-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c97c4-138">Is Indexed</span></span>             | <span data-ttu-id="c97c4-139">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-139">False</span></span>                                                        |
| <span data-ttu-id="c97c4-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c97c4-140">In Global Catalog</span></span>      | <span data-ttu-id="c97c4-141">對</span><span class="sxs-lookup"><span data-stu-id="c97c4-141">True</span></span>                                                         |
| <span data-ttu-id="c97c4-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c97c4-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c4-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c97c4-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c97c4-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c4-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c4-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-146">Search-Flags</span></span>           | <span data-ttu-id="c97c4-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c97c4-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="c97c4-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-148">System-Flags</span></span>           | <span data-ttu-id="c97c4-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c4-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="c97c4-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c97c4-150">Classes used in</span></span>        | [<span data-ttu-id="c97c4-151">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="c97c4-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c97c4-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c97c4-152">Windows Server 2003</span></span>



| <span data-ttu-id="c97c4-153">進入</span><span class="sxs-lookup"><span data-stu-id="c97c4-153">Entry</span></span> | <span data-ttu-id="c97c4-154">值</span><span class="sxs-lookup"><span data-stu-id="c97c4-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c97c4-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c97c4-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c4-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c4-157">System-Only</span></span>            | <span data-ttu-id="c97c4-158">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-158">False</span></span>                                                        |
| <span data-ttu-id="c97c4-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c97c4-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c4-160">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-160">False</span></span>                                                        |
| <span data-ttu-id="c97c4-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c97c4-161">Is Indexed</span></span>             | <span data-ttu-id="c97c4-162">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-162">False</span></span>                                                        |
| <span data-ttu-id="c97c4-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c97c4-163">In Global Catalog</span></span>      | <span data-ttu-id="c97c4-164">對</span><span class="sxs-lookup"><span data-stu-id="c97c4-164">True</span></span>                                                         |
| <span data-ttu-id="c97c4-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c97c4-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c4-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c97c4-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c97c4-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c4-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c4-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-169">Search-Flags</span></span>           | <span data-ttu-id="c97c4-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c97c4-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="c97c4-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-171">System-Flags</span></span>           | <span data-ttu-id="c97c4-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c4-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="c97c4-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c97c4-173">Classes used in</span></span>        | [<span data-ttu-id="c97c4-174">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="c97c4-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c97c4-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c97c4-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c97c4-176">進入</span><span class="sxs-lookup"><span data-stu-id="c97c4-176">Entry</span></span> | <span data-ttu-id="c97c4-177">值</span><span class="sxs-lookup"><span data-stu-id="c97c4-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c97c4-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c97c4-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c4-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c4-180">System-Only</span></span>            | <span data-ttu-id="c97c4-181">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-181">False</span></span>                                                        |
| <span data-ttu-id="c97c4-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c97c4-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c4-183">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-183">False</span></span>                                                        |
| <span data-ttu-id="c97c4-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c97c4-184">Is Indexed</span></span>             | <span data-ttu-id="c97c4-185">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-185">False</span></span>                                                        |
| <span data-ttu-id="c97c4-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c97c4-186">In Global Catalog</span></span>      | <span data-ttu-id="c97c4-187">對</span><span class="sxs-lookup"><span data-stu-id="c97c4-187">True</span></span>                                                         |
| <span data-ttu-id="c97c4-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c97c4-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c4-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c97c4-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c97c4-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c4-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c4-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-192">Search-Flags</span></span>           | <span data-ttu-id="c97c4-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c97c4-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="c97c4-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-194">System-Flags</span></span>           | <span data-ttu-id="c97c4-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c4-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="c97c4-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c97c4-196">Classes used in</span></span>        | [<span data-ttu-id="c97c4-197">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="c97c4-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c97c4-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c97c4-198">Windows Server 2008</span></span>



| <span data-ttu-id="c97c4-199">進入</span><span class="sxs-lookup"><span data-stu-id="c97c4-199">Entry</span></span> | <span data-ttu-id="c97c4-200">值</span><span class="sxs-lookup"><span data-stu-id="c97c4-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c97c4-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c97c4-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c4-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c4-203">System-Only</span></span>            | <span data-ttu-id="c97c4-204">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-204">False</span></span>                                                        |
| <span data-ttu-id="c97c4-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c97c4-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c4-206">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-206">False</span></span>                                                        |
| <span data-ttu-id="c97c4-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c97c4-207">Is Indexed</span></span>             | <span data-ttu-id="c97c4-208">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-208">False</span></span>                                                        |
| <span data-ttu-id="c97c4-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c97c4-209">In Global Catalog</span></span>      | <span data-ttu-id="c97c4-210">對</span><span class="sxs-lookup"><span data-stu-id="c97c4-210">True</span></span>                                                         |
| <span data-ttu-id="c97c4-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c97c4-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c4-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c97c4-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c97c4-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c4-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c4-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-215">Search-Flags</span></span>           | <span data-ttu-id="c97c4-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c97c4-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="c97c4-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-217">System-Flags</span></span>           | <span data-ttu-id="c97c4-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c4-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="c97c4-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c97c4-219">Classes used in</span></span>        | [<span data-ttu-id="c97c4-220">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="c97c4-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c97c4-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c97c4-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c97c4-222">進入</span><span class="sxs-lookup"><span data-stu-id="c97c4-222">Entry</span></span> | <span data-ttu-id="c97c4-223">值</span><span class="sxs-lookup"><span data-stu-id="c97c4-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c97c4-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c97c4-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c4-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c4-226">System-Only</span></span>            | <span data-ttu-id="c97c4-227">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-227">False</span></span>                                                        |
| <span data-ttu-id="c97c4-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c97c4-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c4-229">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-229">False</span></span>                                                        |
| <span data-ttu-id="c97c4-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c97c4-230">Is Indexed</span></span>             | <span data-ttu-id="c97c4-231">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-231">False</span></span>                                                        |
| <span data-ttu-id="c97c4-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c97c4-232">In Global Catalog</span></span>      | <span data-ttu-id="c97c4-233">對</span><span class="sxs-lookup"><span data-stu-id="c97c4-233">True</span></span>                                                         |
| <span data-ttu-id="c97c4-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c97c4-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c4-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c97c4-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c97c4-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c4-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c4-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-238">Search-Flags</span></span>           | <span data-ttu-id="c97c4-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c97c4-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="c97c4-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-240">System-Flags</span></span>           | <span data-ttu-id="c97c4-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c4-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="c97c4-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c97c4-242">Classes used in</span></span>        | [<span data-ttu-id="c97c4-243">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="c97c4-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c97c4-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c97c4-244">Windows Server 2012</span></span>



| <span data-ttu-id="c97c4-245">進入</span><span class="sxs-lookup"><span data-stu-id="c97c4-245">Entry</span></span> | <span data-ttu-id="c97c4-246">值</span><span class="sxs-lookup"><span data-stu-id="c97c4-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c97c4-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c97c4-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c97c4-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c97c4-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c97c4-249">System-Only</span></span>            | <span data-ttu-id="c97c4-250">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-250">False</span></span>                                                        |
| <span data-ttu-id="c97c4-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c97c4-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c97c4-252">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-252">False</span></span>                                                        |
| <span data-ttu-id="c97c4-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c97c4-253">Is Indexed</span></span>             | <span data-ttu-id="c97c4-254">否</span><span class="sxs-lookup"><span data-stu-id="c97c4-254">False</span></span>                                                        |
| <span data-ttu-id="c97c4-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c97c4-255">In Global Catalog</span></span>      | <span data-ttu-id="c97c4-256">對</span><span class="sxs-lookup"><span data-stu-id="c97c4-256">True</span></span>                                                         |
| <span data-ttu-id="c97c4-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c97c4-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c97c4-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c97c4-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c97c4-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c97c4-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c97c4-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c97c4-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-261">Search-Flags</span></span>           | <span data-ttu-id="c97c4-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c97c4-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="c97c4-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c97c4-263">System-Flags</span></span>           | <span data-ttu-id="c97c4-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c97c4-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="c97c4-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c97c4-265">Classes used in</span></span>        | [<span data-ttu-id="c97c4-266">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="c97c4-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 






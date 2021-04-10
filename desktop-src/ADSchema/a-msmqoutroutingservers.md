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
# <a name="msmq-out-routing-servers-attribute"></a><span data-ttu-id="1dd4e-105">MSMQ 輸出路由-伺服器屬性</span><span class="sxs-lookup"><span data-stu-id="1dd4e-105">MSMQ-Out-Routing-Servers attribute</span></span>

<span data-ttu-id="1dd4e-106">MSMQ 路由伺服器的 DN 連結，此電腦的所有連出流量都應路由傳送。</span><span class="sxs-lookup"><span data-stu-id="1dd4e-106">DN links to MSMQ routing servers through which all outgoing traffic for this computer should be routed.</span></span>



| <span data-ttu-id="1dd4e-107">進入</span><span class="sxs-lookup"><span data-stu-id="1dd4e-107">Entry</span></span> | <span data-ttu-id="1dd4e-108">值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="1dd4e-109">CN</span><span class="sxs-lookup"><span data-stu-id="1dd4e-109">CN</span></span>                | <span data-ttu-id="1dd4e-110">MSMQ 輸出路由-伺服器</span><span class="sxs-lookup"><span data-stu-id="1dd4e-110">MSMQ-Out-Routing-Servers</span></span>                |
| <span data-ttu-id="1dd4e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1dd4e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1dd4e-112">mSMQOutRoutingServers</span><span class="sxs-lookup"><span data-stu-id="1dd4e-112">mSMQOutRoutingServers</span></span>                   |
| <span data-ttu-id="1dd4e-113">大小</span><span class="sxs-lookup"><span data-stu-id="1dd4e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="1dd4e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1dd4e-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="1dd4e-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1dd4e-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="1dd4e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1dd4e-116">Attribute-Id</span></span>      | <span data-ttu-id="1dd4e-117">1.2.840.113556.1.4.928</span><span class="sxs-lookup"><span data-stu-id="1dd4e-117">1.2.840.113556.1.4.928</span></span>                  |
| <span data-ttu-id="1dd4e-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1dd4e-118">System-Id-Guid</span></span>    | <span data-ttu-id="1dd4e-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="1dd4e-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="1dd4e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dd4e-120">Syntax</span></span>            | [<span data-ttu-id="1dd4e-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="1dd4e-122">實作</span><span class="sxs-lookup"><span data-stu-id="1dd4e-122">Implementations</span></span>

-   [<span data-ttu-id="1dd4e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1dd4e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1dd4e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1dd4e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1dd4e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1dd4e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1dd4e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1dd4e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1dd4e-130">進入</span><span class="sxs-lookup"><span data-stu-id="1dd4e-130">Entry</span></span> | <span data-ttu-id="1dd4e-131">值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="1dd4e-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1dd4e-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dd4e-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dd4e-134">System-Only</span></span>            | <span data-ttu-id="1dd4e-135">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-135">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1dd4e-137">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-137">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1dd4e-138">Is Indexed</span></span>             | <span data-ttu-id="1dd4e-139">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-139">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1dd4e-140">In Global Catalog</span></span>      | <span data-ttu-id="1dd4e-141">對</span><span class="sxs-lookup"><span data-stu-id="1dd4e-141">True</span></span>                                                         |
| <span data-ttu-id="1dd4e-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1dd4e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dd4e-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1dd4e-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="1dd4e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dd4e-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dd4e-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-146">Search-Flags</span></span>           | <span data-ttu-id="1dd4e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dd4e-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="1dd4e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-148">System-Flags</span></span>           | <span data-ttu-id="1dd4e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dd4e-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="1dd4e-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1dd4e-150">Classes used in</span></span>        | [<span data-ttu-id="1dd4e-151">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1dd4e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1dd4e-152">Windows Server 2003</span></span>



| <span data-ttu-id="1dd4e-153">進入</span><span class="sxs-lookup"><span data-stu-id="1dd4e-153">Entry</span></span> | <span data-ttu-id="1dd4e-154">值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="1dd4e-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1dd4e-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dd4e-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dd4e-157">System-Only</span></span>            | <span data-ttu-id="1dd4e-158">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-158">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="1dd4e-160">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-160">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1dd4e-161">Is Indexed</span></span>             | <span data-ttu-id="1dd4e-162">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-162">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1dd4e-163">In Global Catalog</span></span>      | <span data-ttu-id="1dd4e-164">對</span><span class="sxs-lookup"><span data-stu-id="1dd4e-164">True</span></span>                                                         |
| <span data-ttu-id="1dd4e-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1dd4e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dd4e-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1dd4e-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="1dd4e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dd4e-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dd4e-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-169">Search-Flags</span></span>           | <span data-ttu-id="1dd4e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dd4e-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="1dd4e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-171">System-Flags</span></span>           | <span data-ttu-id="1dd4e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dd4e-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="1dd4e-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1dd4e-173">Classes used in</span></span>        | [<span data-ttu-id="1dd4e-174">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1dd4e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1dd4e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1dd4e-176">進入</span><span class="sxs-lookup"><span data-stu-id="1dd4e-176">Entry</span></span> | <span data-ttu-id="1dd4e-177">值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="1dd4e-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1dd4e-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dd4e-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dd4e-180">System-Only</span></span>            | <span data-ttu-id="1dd4e-181">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-181">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="1dd4e-183">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-183">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1dd4e-184">Is Indexed</span></span>             | <span data-ttu-id="1dd4e-185">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-185">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1dd4e-186">In Global Catalog</span></span>      | <span data-ttu-id="1dd4e-187">對</span><span class="sxs-lookup"><span data-stu-id="1dd4e-187">True</span></span>                                                         |
| <span data-ttu-id="1dd4e-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1dd4e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dd4e-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1dd4e-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="1dd4e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dd4e-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dd4e-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-192">Search-Flags</span></span>           | <span data-ttu-id="1dd4e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dd4e-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="1dd4e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-194">System-Flags</span></span>           | <span data-ttu-id="1dd4e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dd4e-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="1dd4e-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1dd4e-196">Classes used in</span></span>        | [<span data-ttu-id="1dd4e-197">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1dd4e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dd4e-198">Windows Server 2008</span></span>



| <span data-ttu-id="1dd4e-199">進入</span><span class="sxs-lookup"><span data-stu-id="1dd4e-199">Entry</span></span> | <span data-ttu-id="1dd4e-200">值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="1dd4e-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1dd4e-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dd4e-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dd4e-203">System-Only</span></span>            | <span data-ttu-id="1dd4e-204">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-204">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="1dd4e-206">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-206">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1dd4e-207">Is Indexed</span></span>             | <span data-ttu-id="1dd4e-208">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-208">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1dd4e-209">In Global Catalog</span></span>      | <span data-ttu-id="1dd4e-210">對</span><span class="sxs-lookup"><span data-stu-id="1dd4e-210">True</span></span>                                                         |
| <span data-ttu-id="1dd4e-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1dd4e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dd4e-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1dd4e-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="1dd4e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dd4e-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dd4e-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-215">Search-Flags</span></span>           | <span data-ttu-id="1dd4e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dd4e-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="1dd4e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-217">System-Flags</span></span>           | <span data-ttu-id="1dd4e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dd4e-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="1dd4e-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1dd4e-219">Classes used in</span></span>        | [<span data-ttu-id="1dd4e-220">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1dd4e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1dd4e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1dd4e-222">進入</span><span class="sxs-lookup"><span data-stu-id="1dd4e-222">Entry</span></span> | <span data-ttu-id="1dd4e-223">值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="1dd4e-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1dd4e-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dd4e-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dd4e-226">System-Only</span></span>            | <span data-ttu-id="1dd4e-227">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-227">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="1dd4e-229">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-229">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1dd4e-230">Is Indexed</span></span>             | <span data-ttu-id="1dd4e-231">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-231">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1dd4e-232">In Global Catalog</span></span>      | <span data-ttu-id="1dd4e-233">對</span><span class="sxs-lookup"><span data-stu-id="1dd4e-233">True</span></span>                                                         |
| <span data-ttu-id="1dd4e-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1dd4e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dd4e-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1dd4e-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="1dd4e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dd4e-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dd4e-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-238">Search-Flags</span></span>           | <span data-ttu-id="1dd4e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dd4e-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="1dd4e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-240">System-Flags</span></span>           | <span data-ttu-id="1dd4e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dd4e-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="1dd4e-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1dd4e-242">Classes used in</span></span>        | [<span data-ttu-id="1dd4e-243">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1dd4e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1dd4e-244">Windows Server 2012</span></span>



| <span data-ttu-id="1dd4e-245">進入</span><span class="sxs-lookup"><span data-stu-id="1dd4e-245">Entry</span></span> | <span data-ttu-id="1dd4e-246">值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="1dd4e-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1dd4e-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dd4e-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="1dd4e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dd4e-249">System-Only</span></span>            | <span data-ttu-id="1dd4e-250">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-250">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1dd4e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="1dd4e-252">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-252">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1dd4e-253">Is Indexed</span></span>             | <span data-ttu-id="1dd4e-254">否</span><span class="sxs-lookup"><span data-stu-id="1dd4e-254">False</span></span>                                                        |
| <span data-ttu-id="1dd4e-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1dd4e-255">In Global Catalog</span></span>      | <span data-ttu-id="1dd4e-256">對</span><span class="sxs-lookup"><span data-stu-id="1dd4e-256">True</span></span>                                                         |
| <span data-ttu-id="1dd4e-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1dd4e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dd4e-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1dd4e-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="1dd4e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dd4e-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dd4e-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="1dd4e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-261">Search-Flags</span></span>           | <span data-ttu-id="1dd4e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dd4e-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="1dd4e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dd4e-263">System-Flags</span></span>           | <span data-ttu-id="1dd4e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1dd4e-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="1dd4e-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1dd4e-265">Classes used in</span></span>        | [<span data-ttu-id="1dd4e-266">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="1dd4e-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 






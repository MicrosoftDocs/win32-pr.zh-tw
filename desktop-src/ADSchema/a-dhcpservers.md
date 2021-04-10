---
title: dhcp 伺服器屬性
description: 包含企業中已授權的伺服器清單。
ms.assetid: f712b2d2-ff9c-4ee2-aede-b68023e3e6b6
ms.tgt_platform: multiple
keywords:
- dhcp 伺服器屬性 AD 架構
- dhcpServers 屬性 AD 架構
topic_type:
- apiref
api_name:
- dhcp-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e43018c91e5bb495ee39476f07f40756cfcf097
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935261"
---
# <a name="dhcp-servers-attribute"></a><span data-ttu-id="9f643-105">dhcp 伺服器屬性</span><span class="sxs-lookup"><span data-stu-id="9f643-105">dhcp-Servers attribute</span></span>

<span data-ttu-id="9f643-106">包含企業中已授權的伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="9f643-106">Contains a list of servers that are authorized in the enterprise.</span></span>



| <span data-ttu-id="9f643-107">進入</span><span class="sxs-lookup"><span data-stu-id="9f643-107">Entry</span></span> | <span data-ttu-id="9f643-108">值</span><span class="sxs-lookup"><span data-stu-id="9f643-108">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="9f643-109">CN</span><span class="sxs-lookup"><span data-stu-id="9f643-109">CN</span></span>                | <span data-ttu-id="9f643-110">dhcp 伺服器</span><span class="sxs-lookup"><span data-stu-id="9f643-110">dhcp-Servers</span></span>                                           |
| <span data-ttu-id="9f643-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9f643-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9f643-112">dhcpServers</span><span class="sxs-lookup"><span data-stu-id="9f643-112">dhcpServers</span></span>                                            |
| <span data-ttu-id="9f643-113">大小</span><span class="sxs-lookup"><span data-stu-id="9f643-113">Size</span></span>              | \-                                                     |
| <span data-ttu-id="9f643-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9f643-114">Update Privilege</span></span>  | <span data-ttu-id="9f643-115">網域系統管理員。</span><span class="sxs-lookup"><span data-stu-id="9f643-115">Domain administrator.</span></span>                                  |
| <span data-ttu-id="9f643-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9f643-116">Update Frequency</span></span>  | <span data-ttu-id="9f643-117">在樹系中新增或移除新的伺服器時。</span><span class="sxs-lookup"><span data-stu-id="9f643-117">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="9f643-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9f643-118">Attribute-Id</span></span>      | <span data-ttu-id="9f643-119">1.2.840.113556.1.4.704</span><span class="sxs-lookup"><span data-stu-id="9f643-119">1.2.840.113556.1.4.704</span></span>                                 |
| <span data-ttu-id="9f643-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9f643-120">System-Id-Guid</span></span>    | <span data-ttu-id="9f643-121">963d2745-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9f643-121">963d2745-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="9f643-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f643-122">Syntax</span></span>            | [<span data-ttu-id="9f643-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="9f643-123">**String(IA5)**</span></span>](s-string-ia5.md)                    |



## <a name="implementations"></a><span data-ttu-id="9f643-124">實作</span><span class="sxs-lookup"><span data-stu-id="9f643-124">Implementations</span></span>

-   [<span data-ttu-id="9f643-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9f643-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9f643-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9f643-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9f643-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9f643-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9f643-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9f643-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9f643-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9f643-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9f643-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9f643-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9f643-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f643-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9f643-132">進入</span><span class="sxs-lookup"><span data-stu-id="9f643-132">Entry</span></span> | <span data-ttu-id="9f643-133">值</span><span class="sxs-lookup"><span data-stu-id="9f643-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9f643-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f643-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f643-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f643-136">System-Only</span></span>            | <span data-ttu-id="9f643-137">否</span><span class="sxs-lookup"><span data-stu-id="9f643-137">False</span></span>                                        |
| <span data-ttu-id="9f643-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f643-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9f643-139">否</span><span class="sxs-lookup"><span data-stu-id="9f643-139">False</span></span>                                        |
| <span data-ttu-id="9f643-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f643-140">Is Indexed</span></span>             | <span data-ttu-id="9f643-141">否</span><span class="sxs-lookup"><span data-stu-id="9f643-141">False</span></span>                                        |
| <span data-ttu-id="9f643-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f643-142">In Global Catalog</span></span>      | <span data-ttu-id="9f643-143">否</span><span class="sxs-lookup"><span data-stu-id="9f643-143">False</span></span>                                        |
| <span data-ttu-id="9f643-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f643-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f643-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f643-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9f643-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f643-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9f643-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f643-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9f643-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-148">Search-Flags</span></span>           | <span data-ttu-id="9f643-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f643-149">0x00000000</span></span>                                   |
| <span data-ttu-id="9f643-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-150">System-Flags</span></span>           | <span data-ttu-id="9f643-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f643-151">0x00000010</span></span>                                   |
| <span data-ttu-id="9f643-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f643-152">Classes used in</span></span>        | [<span data-ttu-id="9f643-153">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="9f643-153">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9f643-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f643-154">Windows Server 2003</span></span>



| <span data-ttu-id="9f643-155">進入</span><span class="sxs-lookup"><span data-stu-id="9f643-155">Entry</span></span> | <span data-ttu-id="9f643-156">值</span><span class="sxs-lookup"><span data-stu-id="9f643-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9f643-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f643-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f643-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f643-159">System-Only</span></span>            | <span data-ttu-id="9f643-160">否</span><span class="sxs-lookup"><span data-stu-id="9f643-160">False</span></span>                                        |
| <span data-ttu-id="9f643-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f643-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9f643-162">否</span><span class="sxs-lookup"><span data-stu-id="9f643-162">False</span></span>                                        |
| <span data-ttu-id="9f643-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f643-163">Is Indexed</span></span>             | <span data-ttu-id="9f643-164">否</span><span class="sxs-lookup"><span data-stu-id="9f643-164">False</span></span>                                        |
| <span data-ttu-id="9f643-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f643-165">In Global Catalog</span></span>      | <span data-ttu-id="9f643-166">否</span><span class="sxs-lookup"><span data-stu-id="9f643-166">False</span></span>                                        |
| <span data-ttu-id="9f643-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f643-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f643-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f643-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9f643-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f643-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9f643-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f643-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9f643-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-171">Search-Flags</span></span>           | <span data-ttu-id="9f643-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f643-172">0x00000000</span></span>                                   |
| <span data-ttu-id="9f643-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-173">System-Flags</span></span>           | <span data-ttu-id="9f643-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f643-174">0x00000010</span></span>                                   |
| <span data-ttu-id="9f643-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f643-175">Classes used in</span></span>        | [<span data-ttu-id="9f643-176">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="9f643-176">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9f643-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9f643-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9f643-178">進入</span><span class="sxs-lookup"><span data-stu-id="9f643-178">Entry</span></span> | <span data-ttu-id="9f643-179">值</span><span class="sxs-lookup"><span data-stu-id="9f643-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9f643-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f643-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f643-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f643-182">System-Only</span></span>            | <span data-ttu-id="9f643-183">否</span><span class="sxs-lookup"><span data-stu-id="9f643-183">False</span></span>                                        |
| <span data-ttu-id="9f643-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f643-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9f643-185">否</span><span class="sxs-lookup"><span data-stu-id="9f643-185">False</span></span>                                        |
| <span data-ttu-id="9f643-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f643-186">Is Indexed</span></span>             | <span data-ttu-id="9f643-187">否</span><span class="sxs-lookup"><span data-stu-id="9f643-187">False</span></span>                                        |
| <span data-ttu-id="9f643-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f643-188">In Global Catalog</span></span>      | <span data-ttu-id="9f643-189">否</span><span class="sxs-lookup"><span data-stu-id="9f643-189">False</span></span>                                        |
| <span data-ttu-id="9f643-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f643-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f643-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f643-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9f643-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f643-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9f643-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f643-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9f643-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-194">Search-Flags</span></span>           | <span data-ttu-id="9f643-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f643-195">0x00000000</span></span>                                   |
| <span data-ttu-id="9f643-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-196">System-Flags</span></span>           | <span data-ttu-id="9f643-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f643-197">0x00000010</span></span>                                   |
| <span data-ttu-id="9f643-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f643-198">Classes used in</span></span>        | [<span data-ttu-id="9f643-199">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="9f643-199">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9f643-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f643-200">Windows Server 2008</span></span>



| <span data-ttu-id="9f643-201">進入</span><span class="sxs-lookup"><span data-stu-id="9f643-201">Entry</span></span> | <span data-ttu-id="9f643-202">值</span><span class="sxs-lookup"><span data-stu-id="9f643-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9f643-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f643-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f643-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f643-205">System-Only</span></span>            | <span data-ttu-id="9f643-206">否</span><span class="sxs-lookup"><span data-stu-id="9f643-206">False</span></span>                                        |
| <span data-ttu-id="9f643-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f643-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9f643-208">否</span><span class="sxs-lookup"><span data-stu-id="9f643-208">False</span></span>                                        |
| <span data-ttu-id="9f643-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f643-209">Is Indexed</span></span>             | <span data-ttu-id="9f643-210">否</span><span class="sxs-lookup"><span data-stu-id="9f643-210">False</span></span>                                        |
| <span data-ttu-id="9f643-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f643-211">In Global Catalog</span></span>      | <span data-ttu-id="9f643-212">否</span><span class="sxs-lookup"><span data-stu-id="9f643-212">False</span></span>                                        |
| <span data-ttu-id="9f643-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f643-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f643-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f643-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9f643-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f643-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9f643-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f643-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9f643-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-217">Search-Flags</span></span>           | <span data-ttu-id="9f643-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f643-218">0x00000000</span></span>                                   |
| <span data-ttu-id="9f643-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-219">System-Flags</span></span>           | <span data-ttu-id="9f643-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f643-220">0x00000010</span></span>                                   |
| <span data-ttu-id="9f643-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f643-221">Classes used in</span></span>        | [<span data-ttu-id="9f643-222">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="9f643-222">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9f643-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f643-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9f643-224">進入</span><span class="sxs-lookup"><span data-stu-id="9f643-224">Entry</span></span> | <span data-ttu-id="9f643-225">值</span><span class="sxs-lookup"><span data-stu-id="9f643-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9f643-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f643-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f643-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f643-228">System-Only</span></span>            | <span data-ttu-id="9f643-229">否</span><span class="sxs-lookup"><span data-stu-id="9f643-229">False</span></span>                                        |
| <span data-ttu-id="9f643-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f643-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9f643-231">否</span><span class="sxs-lookup"><span data-stu-id="9f643-231">False</span></span>                                        |
| <span data-ttu-id="9f643-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f643-232">Is Indexed</span></span>             | <span data-ttu-id="9f643-233">否</span><span class="sxs-lookup"><span data-stu-id="9f643-233">False</span></span>                                        |
| <span data-ttu-id="9f643-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f643-234">In Global Catalog</span></span>      | <span data-ttu-id="9f643-235">否</span><span class="sxs-lookup"><span data-stu-id="9f643-235">False</span></span>                                        |
| <span data-ttu-id="9f643-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f643-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f643-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f643-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9f643-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f643-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9f643-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f643-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9f643-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-240">Search-Flags</span></span>           | <span data-ttu-id="9f643-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f643-241">0x00000000</span></span>                                   |
| <span data-ttu-id="9f643-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-242">System-Flags</span></span>           | <span data-ttu-id="9f643-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f643-243">0x00000010</span></span>                                   |
| <span data-ttu-id="9f643-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f643-244">Classes used in</span></span>        | [<span data-ttu-id="9f643-245">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="9f643-245">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9f643-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f643-246">Windows Server 2012</span></span>



| <span data-ttu-id="9f643-247">進入</span><span class="sxs-lookup"><span data-stu-id="9f643-247">Entry</span></span> | <span data-ttu-id="9f643-248">值</span><span class="sxs-lookup"><span data-stu-id="9f643-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9f643-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f643-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f643-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9f643-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f643-251">System-Only</span></span>            | <span data-ttu-id="9f643-252">否</span><span class="sxs-lookup"><span data-stu-id="9f643-252">False</span></span>                                        |
| <span data-ttu-id="9f643-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f643-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9f643-254">否</span><span class="sxs-lookup"><span data-stu-id="9f643-254">False</span></span>                                        |
| <span data-ttu-id="9f643-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f643-255">Is Indexed</span></span>             | <span data-ttu-id="9f643-256">否</span><span class="sxs-lookup"><span data-stu-id="9f643-256">False</span></span>                                        |
| <span data-ttu-id="9f643-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f643-257">In Global Catalog</span></span>      | <span data-ttu-id="9f643-258">否</span><span class="sxs-lookup"><span data-stu-id="9f643-258">False</span></span>                                        |
| <span data-ttu-id="9f643-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f643-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f643-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f643-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9f643-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f643-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9f643-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f643-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9f643-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-263">Search-Flags</span></span>           | <span data-ttu-id="9f643-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f643-264">0x00000000</span></span>                                   |
| <span data-ttu-id="9f643-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f643-265">System-Flags</span></span>           | <span data-ttu-id="9f643-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f643-266">0x00000010</span></span>                                   |
| <span data-ttu-id="9f643-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f643-267">Classes used in</span></span>        | [<span data-ttu-id="9f643-268">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="9f643-268">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 






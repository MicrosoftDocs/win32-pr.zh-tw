---
title: 初始驗證-傳入屬性
description: 包含用戶端對這部伺服器的初始連入驗證要求的相關資訊。 此伺服器會接著將此要求傳送到網域的驗證服務器。
ms.assetid: d49d45ae-87fe-415d-8110-79b2b321f2b6
ms.tgt_platform: multiple
keywords:
- 初始驗證-傳入屬性 AD 架構
- initialAuthIncoming 屬性 AD 架構
topic_type:
- apiref
api_name:
- Initial-Auth-Incoming
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973b00abd5b77b713fc03b5efb3d4cf45b97fc19
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687096"
---
# <a name="initial-auth-incoming-attribute"></a><span data-ttu-id="674fd-106">初始驗證-傳入屬性</span><span class="sxs-lookup"><span data-stu-id="674fd-106">Initial-Auth-Incoming attribute</span></span>

<span data-ttu-id="674fd-107">包含用戶端對這部伺服器的初始連入驗證要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="674fd-107">Contains information about an initial incoming authentication request by a client to this server.</span></span> <span data-ttu-id="674fd-108">此伺服器會接著將此要求傳送到網域的驗證服務器。</span><span class="sxs-lookup"><span data-stu-id="674fd-108">This request is then sent by this server to the authentication server for the domain.</span></span>



| <span data-ttu-id="674fd-109">進入</span><span class="sxs-lookup"><span data-stu-id="674fd-109">Entry</span></span> | <span data-ttu-id="674fd-110">值</span><span class="sxs-lookup"><span data-stu-id="674fd-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="674fd-111">CN</span><span class="sxs-lookup"><span data-stu-id="674fd-111">CN</span></span>                | <span data-ttu-id="674fd-112">初始-驗證-傳入</span><span class="sxs-lookup"><span data-stu-id="674fd-112">Initial-Auth-Incoming</span></span>                       |
| <span data-ttu-id="674fd-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="674fd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="674fd-114">initialAuthIncoming</span><span class="sxs-lookup"><span data-stu-id="674fd-114">initialAuthIncoming</span></span>                         |
| <span data-ttu-id="674fd-115">大小</span><span class="sxs-lookup"><span data-stu-id="674fd-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="674fd-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="674fd-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="674fd-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="674fd-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="674fd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="674fd-118">Attribute-Id</span></span>      | <span data-ttu-id="674fd-119">1.2.840.113556.1.4.539</span><span class="sxs-lookup"><span data-stu-id="674fd-119">1.2.840.113556.1.4.539</span></span>                      |
| <span data-ttu-id="674fd-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="674fd-120">System-Id-Guid</span></span>    | <span data-ttu-id="674fd-121">52458023-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="674fd-121">52458023-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="674fd-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="674fd-122">Syntax</span></span>            | [<span data-ttu-id="674fd-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="674fd-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="674fd-124">實作</span><span class="sxs-lookup"><span data-stu-id="674fd-124">Implementations</span></span>

-   [<span data-ttu-id="674fd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="674fd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="674fd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="674fd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="674fd-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="674fd-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="674fd-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="674fd-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="674fd-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="674fd-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="674fd-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="674fd-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="674fd-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="674fd-131">Windows 2000 Server</span></span>



| <span data-ttu-id="674fd-132">進入</span><span class="sxs-lookup"><span data-stu-id="674fd-132">Entry</span></span> | <span data-ttu-id="674fd-133">值</span><span class="sxs-lookup"><span data-stu-id="674fd-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="674fd-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="674fd-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674fd-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="674fd-136">System-Only</span></span>            | <span data-ttu-id="674fd-137">否</span><span class="sxs-lookup"><span data-stu-id="674fd-137">False</span></span>                                                |
| <span data-ttu-id="674fd-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="674fd-138">Is-Single-Valued</span></span>       | <span data-ttu-id="674fd-139">對</span><span class="sxs-lookup"><span data-stu-id="674fd-139">True</span></span>                                                 |
| <span data-ttu-id="674fd-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="674fd-140">Is Indexed</span></span>             | <span data-ttu-id="674fd-141">否</span><span class="sxs-lookup"><span data-stu-id="674fd-141">False</span></span>                                                |
| <span data-ttu-id="674fd-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="674fd-142">In Global Catalog</span></span>      | <span data-ttu-id="674fd-143">否</span><span class="sxs-lookup"><span data-stu-id="674fd-143">False</span></span>                                                |
| <span data-ttu-id="674fd-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="674fd-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="674fd-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="674fd-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="674fd-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674fd-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674fd-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-148">Search-Flags</span></span>           | <span data-ttu-id="674fd-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674fd-149">0x00000000</span></span>                                           |
| <span data-ttu-id="674fd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-150">System-Flags</span></span>           | <span data-ttu-id="674fd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674fd-151">0x00000010</span></span>                                           |
| <span data-ttu-id="674fd-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="674fd-152">Classes used in</span></span>        | [<span data-ttu-id="674fd-153">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="674fd-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="674fd-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="674fd-154">Windows Server 2003</span></span>



| <span data-ttu-id="674fd-155">進入</span><span class="sxs-lookup"><span data-stu-id="674fd-155">Entry</span></span> | <span data-ttu-id="674fd-156">值</span><span class="sxs-lookup"><span data-stu-id="674fd-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="674fd-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="674fd-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674fd-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="674fd-159">System-Only</span></span>            | <span data-ttu-id="674fd-160">否</span><span class="sxs-lookup"><span data-stu-id="674fd-160">False</span></span>                                                |
| <span data-ttu-id="674fd-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="674fd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="674fd-162">對</span><span class="sxs-lookup"><span data-stu-id="674fd-162">True</span></span>                                                 |
| <span data-ttu-id="674fd-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="674fd-163">Is Indexed</span></span>             | <span data-ttu-id="674fd-164">否</span><span class="sxs-lookup"><span data-stu-id="674fd-164">False</span></span>                                                |
| <span data-ttu-id="674fd-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="674fd-165">In Global Catalog</span></span>      | <span data-ttu-id="674fd-166">否</span><span class="sxs-lookup"><span data-stu-id="674fd-166">False</span></span>                                                |
| <span data-ttu-id="674fd-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="674fd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="674fd-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="674fd-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="674fd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674fd-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674fd-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-171">Search-Flags</span></span>           | <span data-ttu-id="674fd-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674fd-172">0x00000000</span></span>                                           |
| <span data-ttu-id="674fd-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-173">System-Flags</span></span>           | <span data-ttu-id="674fd-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674fd-174">0x00000010</span></span>                                           |
| <span data-ttu-id="674fd-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="674fd-175">Classes used in</span></span>        | [<span data-ttu-id="674fd-176">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="674fd-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="674fd-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="674fd-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="674fd-178">進入</span><span class="sxs-lookup"><span data-stu-id="674fd-178">Entry</span></span> | <span data-ttu-id="674fd-179">值</span><span class="sxs-lookup"><span data-stu-id="674fd-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="674fd-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="674fd-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674fd-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="674fd-182">System-Only</span></span>            | <span data-ttu-id="674fd-183">否</span><span class="sxs-lookup"><span data-stu-id="674fd-183">False</span></span>                                                |
| <span data-ttu-id="674fd-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="674fd-184">Is-Single-Valued</span></span>       | <span data-ttu-id="674fd-185">對</span><span class="sxs-lookup"><span data-stu-id="674fd-185">True</span></span>                                                 |
| <span data-ttu-id="674fd-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="674fd-186">Is Indexed</span></span>             | <span data-ttu-id="674fd-187">否</span><span class="sxs-lookup"><span data-stu-id="674fd-187">False</span></span>                                                |
| <span data-ttu-id="674fd-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="674fd-188">In Global Catalog</span></span>      | <span data-ttu-id="674fd-189">否</span><span class="sxs-lookup"><span data-stu-id="674fd-189">False</span></span>                                                |
| <span data-ttu-id="674fd-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="674fd-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="674fd-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="674fd-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="674fd-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674fd-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674fd-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-194">Search-Flags</span></span>           | <span data-ttu-id="674fd-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674fd-195">0x00000000</span></span>                                           |
| <span data-ttu-id="674fd-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-196">System-Flags</span></span>           | <span data-ttu-id="674fd-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674fd-197">0x00000010</span></span>                                           |
| <span data-ttu-id="674fd-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="674fd-198">Classes used in</span></span>        | [<span data-ttu-id="674fd-199">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="674fd-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="674fd-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="674fd-200">Windows Server 2008</span></span>



| <span data-ttu-id="674fd-201">進入</span><span class="sxs-lookup"><span data-stu-id="674fd-201">Entry</span></span> | <span data-ttu-id="674fd-202">值</span><span class="sxs-lookup"><span data-stu-id="674fd-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="674fd-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="674fd-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674fd-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="674fd-205">System-Only</span></span>            | <span data-ttu-id="674fd-206">否</span><span class="sxs-lookup"><span data-stu-id="674fd-206">False</span></span>                                                |
| <span data-ttu-id="674fd-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="674fd-207">Is-Single-Valued</span></span>       | <span data-ttu-id="674fd-208">對</span><span class="sxs-lookup"><span data-stu-id="674fd-208">True</span></span>                                                 |
| <span data-ttu-id="674fd-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="674fd-209">Is Indexed</span></span>             | <span data-ttu-id="674fd-210">否</span><span class="sxs-lookup"><span data-stu-id="674fd-210">False</span></span>                                                |
| <span data-ttu-id="674fd-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="674fd-211">In Global Catalog</span></span>      | <span data-ttu-id="674fd-212">否</span><span class="sxs-lookup"><span data-stu-id="674fd-212">False</span></span>                                                |
| <span data-ttu-id="674fd-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="674fd-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="674fd-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="674fd-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="674fd-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674fd-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674fd-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-217">Search-Flags</span></span>           | <span data-ttu-id="674fd-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674fd-218">0x00000000</span></span>                                           |
| <span data-ttu-id="674fd-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-219">System-Flags</span></span>           | <span data-ttu-id="674fd-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674fd-220">0x00000010</span></span>                                           |
| <span data-ttu-id="674fd-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="674fd-221">Classes used in</span></span>        | [<span data-ttu-id="674fd-222">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="674fd-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="674fd-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="674fd-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="674fd-224">進入</span><span class="sxs-lookup"><span data-stu-id="674fd-224">Entry</span></span> | <span data-ttu-id="674fd-225">值</span><span class="sxs-lookup"><span data-stu-id="674fd-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="674fd-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="674fd-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674fd-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="674fd-228">System-Only</span></span>            | <span data-ttu-id="674fd-229">否</span><span class="sxs-lookup"><span data-stu-id="674fd-229">False</span></span>                                                |
| <span data-ttu-id="674fd-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="674fd-230">Is-Single-Valued</span></span>       | <span data-ttu-id="674fd-231">對</span><span class="sxs-lookup"><span data-stu-id="674fd-231">True</span></span>                                                 |
| <span data-ttu-id="674fd-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="674fd-232">Is Indexed</span></span>             | <span data-ttu-id="674fd-233">否</span><span class="sxs-lookup"><span data-stu-id="674fd-233">False</span></span>                                                |
| <span data-ttu-id="674fd-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="674fd-234">In Global Catalog</span></span>      | <span data-ttu-id="674fd-235">否</span><span class="sxs-lookup"><span data-stu-id="674fd-235">False</span></span>                                                |
| <span data-ttu-id="674fd-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="674fd-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="674fd-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="674fd-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="674fd-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674fd-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674fd-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-240">Search-Flags</span></span>           | <span data-ttu-id="674fd-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674fd-241">0x00000000</span></span>                                           |
| <span data-ttu-id="674fd-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-242">System-Flags</span></span>           | <span data-ttu-id="674fd-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674fd-243">0x00000010</span></span>                                           |
| <span data-ttu-id="674fd-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="674fd-244">Classes used in</span></span>        | [<span data-ttu-id="674fd-245">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="674fd-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="674fd-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="674fd-246">Windows Server 2012</span></span>



| <span data-ttu-id="674fd-247">進入</span><span class="sxs-lookup"><span data-stu-id="674fd-247">Entry</span></span> | <span data-ttu-id="674fd-248">值</span><span class="sxs-lookup"><span data-stu-id="674fd-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="674fd-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="674fd-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="674fd-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="674fd-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="674fd-251">System-Only</span></span>            | <span data-ttu-id="674fd-252">否</span><span class="sxs-lookup"><span data-stu-id="674fd-252">False</span></span>                                                |
| <span data-ttu-id="674fd-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="674fd-253">Is-Single-Valued</span></span>       | <span data-ttu-id="674fd-254">對</span><span class="sxs-lookup"><span data-stu-id="674fd-254">True</span></span>                                                 |
| <span data-ttu-id="674fd-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="674fd-255">Is Indexed</span></span>             | <span data-ttu-id="674fd-256">否</span><span class="sxs-lookup"><span data-stu-id="674fd-256">False</span></span>                                                |
| <span data-ttu-id="674fd-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="674fd-257">In Global Catalog</span></span>      | <span data-ttu-id="674fd-258">否</span><span class="sxs-lookup"><span data-stu-id="674fd-258">False</span></span>                                                |
| <span data-ttu-id="674fd-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="674fd-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="674fd-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="674fd-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="674fd-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="674fd-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="674fd-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="674fd-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-263">Search-Flags</span></span>           | <span data-ttu-id="674fd-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="674fd-264">0x00000000</span></span>                                           |
| <span data-ttu-id="674fd-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="674fd-265">System-Flags</span></span>           | <span data-ttu-id="674fd-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="674fd-266">0x00000010</span></span>                                           |
| <span data-ttu-id="674fd-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="674fd-267">Classes used in</span></span>        | [<span data-ttu-id="674fd-268">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="674fd-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






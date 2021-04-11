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
# <a name="initial-auth-incoming-attribute"></a><span data-ttu-id="0e42a-106">初始驗證-傳入屬性</span><span class="sxs-lookup"><span data-stu-id="0e42a-106">Initial-Auth-Incoming attribute</span></span>

<span data-ttu-id="0e42a-107">包含用戶端對這部伺服器的初始連入驗證要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0e42a-107">Contains information about an initial incoming authentication request by a client to this server.</span></span> <span data-ttu-id="0e42a-108">此伺服器會接著將此要求傳送到網域的驗證服務器。</span><span class="sxs-lookup"><span data-stu-id="0e42a-108">This request is then sent by this server to the authentication server for the domain.</span></span>



| <span data-ttu-id="0e42a-109">進入</span><span class="sxs-lookup"><span data-stu-id="0e42a-109">Entry</span></span> | <span data-ttu-id="0e42a-110">值</span><span class="sxs-lookup"><span data-stu-id="0e42a-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0e42a-111">CN</span><span class="sxs-lookup"><span data-stu-id="0e42a-111">CN</span></span>                | <span data-ttu-id="0e42a-112">初始-驗證-傳入</span><span class="sxs-lookup"><span data-stu-id="0e42a-112">Initial-Auth-Incoming</span></span>                       |
| <span data-ttu-id="0e42a-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0e42a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0e42a-114">initialAuthIncoming</span><span class="sxs-lookup"><span data-stu-id="0e42a-114">initialAuthIncoming</span></span>                         |
| <span data-ttu-id="0e42a-115">大小</span><span class="sxs-lookup"><span data-stu-id="0e42a-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="0e42a-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0e42a-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="0e42a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0e42a-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="0e42a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0e42a-118">Attribute-Id</span></span>      | <span data-ttu-id="0e42a-119">1.2.840.113556.1.4.539</span><span class="sxs-lookup"><span data-stu-id="0e42a-119">1.2.840.113556.1.4.539</span></span>                      |
| <span data-ttu-id="0e42a-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0e42a-120">System-Id-Guid</span></span>    | <span data-ttu-id="0e42a-121">52458023-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0e42a-121">52458023-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="0e42a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e42a-122">Syntax</span></span>            | [<span data-ttu-id="0e42a-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0e42a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0e42a-124">實作</span><span class="sxs-lookup"><span data-stu-id="0e42a-124">Implementations</span></span>

-   [<span data-ttu-id="0e42a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0e42a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0e42a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0e42a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0e42a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0e42a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0e42a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0e42a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0e42a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0e42a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0e42a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0e42a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0e42a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0e42a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0e42a-132">進入</span><span class="sxs-lookup"><span data-stu-id="0e42a-132">Entry</span></span> | <span data-ttu-id="0e42a-133">值</span><span class="sxs-lookup"><span data-stu-id="0e42a-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0e42a-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e42a-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e42a-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e42a-136">System-Only</span></span>            | <span data-ttu-id="0e42a-137">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-137">False</span></span>                                                |
| <span data-ttu-id="0e42a-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e42a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0e42a-139">對</span><span class="sxs-lookup"><span data-stu-id="0e42a-139">True</span></span>                                                 |
| <span data-ttu-id="0e42a-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e42a-140">Is Indexed</span></span>             | <span data-ttu-id="0e42a-141">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-141">False</span></span>                                                |
| <span data-ttu-id="0e42a-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e42a-142">In Global Catalog</span></span>      | <span data-ttu-id="0e42a-143">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-143">False</span></span>                                                |
| <span data-ttu-id="0e42a-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e42a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e42a-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e42a-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0e42a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e42a-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e42a-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-148">Search-Flags</span></span>           | <span data-ttu-id="0e42a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e42a-149">0x00000000</span></span>                                           |
| <span data-ttu-id="0e42a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-150">System-Flags</span></span>           | <span data-ttu-id="0e42a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e42a-151">0x00000010</span></span>                                           |
| <span data-ttu-id="0e42a-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e42a-152">Classes used in</span></span>        | [<span data-ttu-id="0e42a-153">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="0e42a-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0e42a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0e42a-154">Windows Server 2003</span></span>



| <span data-ttu-id="0e42a-155">進入</span><span class="sxs-lookup"><span data-stu-id="0e42a-155">Entry</span></span> | <span data-ttu-id="0e42a-156">值</span><span class="sxs-lookup"><span data-stu-id="0e42a-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0e42a-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e42a-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e42a-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e42a-159">System-Only</span></span>            | <span data-ttu-id="0e42a-160">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-160">False</span></span>                                                |
| <span data-ttu-id="0e42a-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e42a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0e42a-162">對</span><span class="sxs-lookup"><span data-stu-id="0e42a-162">True</span></span>                                                 |
| <span data-ttu-id="0e42a-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e42a-163">Is Indexed</span></span>             | <span data-ttu-id="0e42a-164">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-164">False</span></span>                                                |
| <span data-ttu-id="0e42a-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e42a-165">In Global Catalog</span></span>      | <span data-ttu-id="0e42a-166">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-166">False</span></span>                                                |
| <span data-ttu-id="0e42a-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e42a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e42a-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e42a-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0e42a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e42a-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e42a-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-171">Search-Flags</span></span>           | <span data-ttu-id="0e42a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e42a-172">0x00000000</span></span>                                           |
| <span data-ttu-id="0e42a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-173">System-Flags</span></span>           | <span data-ttu-id="0e42a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e42a-174">0x00000010</span></span>                                           |
| <span data-ttu-id="0e42a-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e42a-175">Classes used in</span></span>        | [<span data-ttu-id="0e42a-176">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="0e42a-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0e42a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0e42a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0e42a-178">進入</span><span class="sxs-lookup"><span data-stu-id="0e42a-178">Entry</span></span> | <span data-ttu-id="0e42a-179">值</span><span class="sxs-lookup"><span data-stu-id="0e42a-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0e42a-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e42a-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e42a-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e42a-182">System-Only</span></span>            | <span data-ttu-id="0e42a-183">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-183">False</span></span>                                                |
| <span data-ttu-id="0e42a-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e42a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0e42a-185">對</span><span class="sxs-lookup"><span data-stu-id="0e42a-185">True</span></span>                                                 |
| <span data-ttu-id="0e42a-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e42a-186">Is Indexed</span></span>             | <span data-ttu-id="0e42a-187">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-187">False</span></span>                                                |
| <span data-ttu-id="0e42a-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e42a-188">In Global Catalog</span></span>      | <span data-ttu-id="0e42a-189">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-189">False</span></span>                                                |
| <span data-ttu-id="0e42a-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e42a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e42a-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e42a-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0e42a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e42a-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e42a-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-194">Search-Flags</span></span>           | <span data-ttu-id="0e42a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e42a-195">0x00000000</span></span>                                           |
| <span data-ttu-id="0e42a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-196">System-Flags</span></span>           | <span data-ttu-id="0e42a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e42a-197">0x00000010</span></span>                                           |
| <span data-ttu-id="0e42a-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e42a-198">Classes used in</span></span>        | [<span data-ttu-id="0e42a-199">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="0e42a-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0e42a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e42a-200">Windows Server 2008</span></span>



| <span data-ttu-id="0e42a-201">進入</span><span class="sxs-lookup"><span data-stu-id="0e42a-201">Entry</span></span> | <span data-ttu-id="0e42a-202">值</span><span class="sxs-lookup"><span data-stu-id="0e42a-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0e42a-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e42a-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e42a-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e42a-205">System-Only</span></span>            | <span data-ttu-id="0e42a-206">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-206">False</span></span>                                                |
| <span data-ttu-id="0e42a-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e42a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0e42a-208">對</span><span class="sxs-lookup"><span data-stu-id="0e42a-208">True</span></span>                                                 |
| <span data-ttu-id="0e42a-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e42a-209">Is Indexed</span></span>             | <span data-ttu-id="0e42a-210">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-210">False</span></span>                                                |
| <span data-ttu-id="0e42a-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e42a-211">In Global Catalog</span></span>      | <span data-ttu-id="0e42a-212">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-212">False</span></span>                                                |
| <span data-ttu-id="0e42a-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e42a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e42a-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e42a-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0e42a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e42a-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e42a-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-217">Search-Flags</span></span>           | <span data-ttu-id="0e42a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e42a-218">0x00000000</span></span>                                           |
| <span data-ttu-id="0e42a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-219">System-Flags</span></span>           | <span data-ttu-id="0e42a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e42a-220">0x00000010</span></span>                                           |
| <span data-ttu-id="0e42a-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e42a-221">Classes used in</span></span>        | [<span data-ttu-id="0e42a-222">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="0e42a-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0e42a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e42a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0e42a-224">進入</span><span class="sxs-lookup"><span data-stu-id="0e42a-224">Entry</span></span> | <span data-ttu-id="0e42a-225">值</span><span class="sxs-lookup"><span data-stu-id="0e42a-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0e42a-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e42a-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e42a-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e42a-228">System-Only</span></span>            | <span data-ttu-id="0e42a-229">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-229">False</span></span>                                                |
| <span data-ttu-id="0e42a-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e42a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0e42a-231">對</span><span class="sxs-lookup"><span data-stu-id="0e42a-231">True</span></span>                                                 |
| <span data-ttu-id="0e42a-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e42a-232">Is Indexed</span></span>             | <span data-ttu-id="0e42a-233">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-233">False</span></span>                                                |
| <span data-ttu-id="0e42a-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e42a-234">In Global Catalog</span></span>      | <span data-ttu-id="0e42a-235">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-235">False</span></span>                                                |
| <span data-ttu-id="0e42a-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e42a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e42a-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e42a-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0e42a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e42a-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e42a-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-240">Search-Flags</span></span>           | <span data-ttu-id="0e42a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e42a-241">0x00000000</span></span>                                           |
| <span data-ttu-id="0e42a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-242">System-Flags</span></span>           | <span data-ttu-id="0e42a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e42a-243">0x00000010</span></span>                                           |
| <span data-ttu-id="0e42a-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e42a-244">Classes used in</span></span>        | [<span data-ttu-id="0e42a-245">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="0e42a-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0e42a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e42a-246">Windows Server 2012</span></span>



| <span data-ttu-id="0e42a-247">進入</span><span class="sxs-lookup"><span data-stu-id="0e42a-247">Entry</span></span> | <span data-ttu-id="0e42a-248">值</span><span class="sxs-lookup"><span data-stu-id="0e42a-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0e42a-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e42a-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e42a-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0e42a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e42a-251">System-Only</span></span>            | <span data-ttu-id="0e42a-252">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-252">False</span></span>                                                |
| <span data-ttu-id="0e42a-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e42a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0e42a-254">對</span><span class="sxs-lookup"><span data-stu-id="0e42a-254">True</span></span>                                                 |
| <span data-ttu-id="0e42a-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e42a-255">Is Indexed</span></span>             | <span data-ttu-id="0e42a-256">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-256">False</span></span>                                                |
| <span data-ttu-id="0e42a-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e42a-257">In Global Catalog</span></span>      | <span data-ttu-id="0e42a-258">否</span><span class="sxs-lookup"><span data-stu-id="0e42a-258">False</span></span>                                                |
| <span data-ttu-id="0e42a-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e42a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e42a-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e42a-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0e42a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e42a-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e42a-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0e42a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-263">Search-Flags</span></span>           | <span data-ttu-id="0e42a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e42a-264">0x00000000</span></span>                                           |
| <span data-ttu-id="0e42a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e42a-265">System-Flags</span></span>           | <span data-ttu-id="0e42a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e42a-266">0x00000010</span></span>                                           |
| <span data-ttu-id="0e42a-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e42a-267">Classes used in</span></span>        | [<span data-ttu-id="0e42a-268">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="0e42a-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






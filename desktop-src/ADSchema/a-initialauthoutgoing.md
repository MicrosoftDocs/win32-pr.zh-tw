---
title: 初始-驗證-傳出屬性
description: 包含驗證服務器對要求驗證的用戶端所傳送之初始傳出驗證的相關資訊。
ms.assetid: cc5ceb14-0424-4caa-bcd9-1e48988af67a
ms.tgt_platform: multiple
keywords:
- 初始-驗證-外寄屬性 AD 架構
- initialAuthOutgoing 屬性 AD 架構
topic_type:
- apiref
api_name:
- Initial-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84faaa443c9589e04f4998dc41d72fe870b5f2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107045"
---
# <a name="initial-auth-outgoing-attribute"></a><span data-ttu-id="92927-105">初始-驗證-傳出屬性</span><span class="sxs-lookup"><span data-stu-id="92927-105">Initial-Auth-Outgoing attribute</span></span>

<span data-ttu-id="92927-106">包含驗證服務器對要求驗證的用戶端所傳送之初始傳出驗證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="92927-106">Contains information about an initial outgoing authentication sent by the authentication server for this domain to the client that requested authentication.</span></span> <span data-ttu-id="92927-107">使用這個屬性的伺服器會接收來自驗證服務器的授權，並將其傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="92927-107">The server that uses this attribute receives the authorization from the authentication server and sends it to the client.</span></span>



| <span data-ttu-id="92927-108">進入</span><span class="sxs-lookup"><span data-stu-id="92927-108">Entry</span></span> | <span data-ttu-id="92927-109">值</span><span class="sxs-lookup"><span data-stu-id="92927-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="92927-110">CN</span><span class="sxs-lookup"><span data-stu-id="92927-110">CN</span></span>                | <span data-ttu-id="92927-111">初始-驗證-外寄</span><span class="sxs-lookup"><span data-stu-id="92927-111">Initial-Auth-Outgoing</span></span>                       |
| <span data-ttu-id="92927-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="92927-112">Ldap-Display-Name</span></span> | <span data-ttu-id="92927-113">initialAuthOutgoing</span><span class="sxs-lookup"><span data-stu-id="92927-113">initialAuthOutgoing</span></span>                         |
| <span data-ttu-id="92927-114">大小</span><span class="sxs-lookup"><span data-stu-id="92927-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="92927-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="92927-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="92927-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="92927-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="92927-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92927-117">Attribute-Id</span></span>      | <span data-ttu-id="92927-118">1.2.840.113556.1.4.540</span><span class="sxs-lookup"><span data-stu-id="92927-118">1.2.840.113556.1.4.540</span></span>                      |
| <span data-ttu-id="92927-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="92927-119">System-Id-Guid</span></span>    | <span data-ttu-id="92927-120">52458024-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="92927-120">52458024-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="92927-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="92927-121">Syntax</span></span>            | [<span data-ttu-id="92927-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="92927-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="92927-123">實作</span><span class="sxs-lookup"><span data-stu-id="92927-123">Implementations</span></span>

-   [<span data-ttu-id="92927-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="92927-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="92927-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="92927-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="92927-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="92927-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="92927-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="92927-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="92927-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="92927-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="92927-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92927-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="92927-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="92927-130">Windows 2000 Server</span></span>



| <span data-ttu-id="92927-131">進入</span><span class="sxs-lookup"><span data-stu-id="92927-131">Entry</span></span> | <span data-ttu-id="92927-132">值</span><span class="sxs-lookup"><span data-stu-id="92927-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="92927-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92927-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92927-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="92927-135">System-Only</span></span>            | <span data-ttu-id="92927-136">否</span><span class="sxs-lookup"><span data-stu-id="92927-136">False</span></span>                                                |
| <span data-ttu-id="92927-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92927-137">Is-Single-Valued</span></span>       | <span data-ttu-id="92927-138">對</span><span class="sxs-lookup"><span data-stu-id="92927-138">True</span></span>                                                 |
| <span data-ttu-id="92927-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92927-139">Is Indexed</span></span>             | <span data-ttu-id="92927-140">否</span><span class="sxs-lookup"><span data-stu-id="92927-140">False</span></span>                                                |
| <span data-ttu-id="92927-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92927-141">In Global Catalog</span></span>      | <span data-ttu-id="92927-142">否</span><span class="sxs-lookup"><span data-stu-id="92927-142">False</span></span>                                                |
| <span data-ttu-id="92927-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92927-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="92927-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92927-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="92927-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92927-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="92927-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92927-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="92927-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-147">Search-Flags</span></span>           | <span data-ttu-id="92927-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92927-148">0x00000000</span></span>                                           |
| <span data-ttu-id="92927-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-149">System-Flags</span></span>           | <span data-ttu-id="92927-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92927-150">0x00000010</span></span>                                           |
| <span data-ttu-id="92927-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92927-151">Classes used in</span></span>        | [<span data-ttu-id="92927-152">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="92927-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="92927-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92927-153">Windows Server 2003</span></span>



| <span data-ttu-id="92927-154">進入</span><span class="sxs-lookup"><span data-stu-id="92927-154">Entry</span></span> | <span data-ttu-id="92927-155">值</span><span class="sxs-lookup"><span data-stu-id="92927-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="92927-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92927-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92927-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="92927-158">System-Only</span></span>            | <span data-ttu-id="92927-159">否</span><span class="sxs-lookup"><span data-stu-id="92927-159">False</span></span>                                                |
| <span data-ttu-id="92927-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92927-160">Is-Single-Valued</span></span>       | <span data-ttu-id="92927-161">對</span><span class="sxs-lookup"><span data-stu-id="92927-161">True</span></span>                                                 |
| <span data-ttu-id="92927-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92927-162">Is Indexed</span></span>             | <span data-ttu-id="92927-163">否</span><span class="sxs-lookup"><span data-stu-id="92927-163">False</span></span>                                                |
| <span data-ttu-id="92927-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92927-164">In Global Catalog</span></span>      | <span data-ttu-id="92927-165">否</span><span class="sxs-lookup"><span data-stu-id="92927-165">False</span></span>                                                |
| <span data-ttu-id="92927-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92927-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="92927-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92927-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="92927-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92927-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="92927-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92927-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="92927-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-170">Search-Flags</span></span>           | <span data-ttu-id="92927-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92927-171">0x00000000</span></span>                                           |
| <span data-ttu-id="92927-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-172">System-Flags</span></span>           | <span data-ttu-id="92927-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92927-173">0x00000010</span></span>                                           |
| <span data-ttu-id="92927-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92927-174">Classes used in</span></span>        | [<span data-ttu-id="92927-175">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="92927-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="92927-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="92927-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="92927-177">進入</span><span class="sxs-lookup"><span data-stu-id="92927-177">Entry</span></span> | <span data-ttu-id="92927-178">值</span><span class="sxs-lookup"><span data-stu-id="92927-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="92927-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92927-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92927-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="92927-181">System-Only</span></span>            | <span data-ttu-id="92927-182">否</span><span class="sxs-lookup"><span data-stu-id="92927-182">False</span></span>                                                |
| <span data-ttu-id="92927-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92927-183">Is-Single-Valued</span></span>       | <span data-ttu-id="92927-184">對</span><span class="sxs-lookup"><span data-stu-id="92927-184">True</span></span>                                                 |
| <span data-ttu-id="92927-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92927-185">Is Indexed</span></span>             | <span data-ttu-id="92927-186">否</span><span class="sxs-lookup"><span data-stu-id="92927-186">False</span></span>                                                |
| <span data-ttu-id="92927-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92927-187">In Global Catalog</span></span>      | <span data-ttu-id="92927-188">否</span><span class="sxs-lookup"><span data-stu-id="92927-188">False</span></span>                                                |
| <span data-ttu-id="92927-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92927-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="92927-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92927-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="92927-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92927-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="92927-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92927-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="92927-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-193">Search-Flags</span></span>           | <span data-ttu-id="92927-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92927-194">0x00000000</span></span>                                           |
| <span data-ttu-id="92927-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-195">System-Flags</span></span>           | <span data-ttu-id="92927-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92927-196">0x00000010</span></span>                                           |
| <span data-ttu-id="92927-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92927-197">Classes used in</span></span>        | [<span data-ttu-id="92927-198">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="92927-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="92927-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92927-199">Windows Server 2008</span></span>



| <span data-ttu-id="92927-200">進入</span><span class="sxs-lookup"><span data-stu-id="92927-200">Entry</span></span> | <span data-ttu-id="92927-201">值</span><span class="sxs-lookup"><span data-stu-id="92927-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="92927-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92927-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92927-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="92927-204">System-Only</span></span>            | <span data-ttu-id="92927-205">否</span><span class="sxs-lookup"><span data-stu-id="92927-205">False</span></span>                                                |
| <span data-ttu-id="92927-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92927-206">Is-Single-Valued</span></span>       | <span data-ttu-id="92927-207">對</span><span class="sxs-lookup"><span data-stu-id="92927-207">True</span></span>                                                 |
| <span data-ttu-id="92927-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92927-208">Is Indexed</span></span>             | <span data-ttu-id="92927-209">否</span><span class="sxs-lookup"><span data-stu-id="92927-209">False</span></span>                                                |
| <span data-ttu-id="92927-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92927-210">In Global Catalog</span></span>      | <span data-ttu-id="92927-211">否</span><span class="sxs-lookup"><span data-stu-id="92927-211">False</span></span>                                                |
| <span data-ttu-id="92927-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92927-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="92927-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92927-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="92927-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92927-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="92927-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92927-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="92927-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-216">Search-Flags</span></span>           | <span data-ttu-id="92927-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92927-217">0x00000000</span></span>                                           |
| <span data-ttu-id="92927-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-218">System-Flags</span></span>           | <span data-ttu-id="92927-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92927-219">0x00000010</span></span>                                           |
| <span data-ttu-id="92927-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92927-220">Classes used in</span></span>        | [<span data-ttu-id="92927-221">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="92927-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="92927-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92927-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="92927-223">進入</span><span class="sxs-lookup"><span data-stu-id="92927-223">Entry</span></span> | <span data-ttu-id="92927-224">值</span><span class="sxs-lookup"><span data-stu-id="92927-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="92927-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92927-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92927-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="92927-227">System-Only</span></span>            | <span data-ttu-id="92927-228">否</span><span class="sxs-lookup"><span data-stu-id="92927-228">False</span></span>                                                |
| <span data-ttu-id="92927-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92927-229">Is-Single-Valued</span></span>       | <span data-ttu-id="92927-230">對</span><span class="sxs-lookup"><span data-stu-id="92927-230">True</span></span>                                                 |
| <span data-ttu-id="92927-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92927-231">Is Indexed</span></span>             | <span data-ttu-id="92927-232">否</span><span class="sxs-lookup"><span data-stu-id="92927-232">False</span></span>                                                |
| <span data-ttu-id="92927-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92927-233">In Global Catalog</span></span>      | <span data-ttu-id="92927-234">否</span><span class="sxs-lookup"><span data-stu-id="92927-234">False</span></span>                                                |
| <span data-ttu-id="92927-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92927-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="92927-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92927-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="92927-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92927-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="92927-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92927-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="92927-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-239">Search-Flags</span></span>           | <span data-ttu-id="92927-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92927-240">0x00000000</span></span>                                           |
| <span data-ttu-id="92927-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-241">System-Flags</span></span>           | <span data-ttu-id="92927-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92927-242">0x00000010</span></span>                                           |
| <span data-ttu-id="92927-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92927-243">Classes used in</span></span>        | [<span data-ttu-id="92927-244">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="92927-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="92927-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92927-245">Windows Server 2012</span></span>



| <span data-ttu-id="92927-246">進入</span><span class="sxs-lookup"><span data-stu-id="92927-246">Entry</span></span> | <span data-ttu-id="92927-247">值</span><span class="sxs-lookup"><span data-stu-id="92927-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="92927-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92927-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92927-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="92927-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="92927-250">System-Only</span></span>            | <span data-ttu-id="92927-251">否</span><span class="sxs-lookup"><span data-stu-id="92927-251">False</span></span>                                                |
| <span data-ttu-id="92927-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92927-252">Is-Single-Valued</span></span>       | <span data-ttu-id="92927-253">對</span><span class="sxs-lookup"><span data-stu-id="92927-253">True</span></span>                                                 |
| <span data-ttu-id="92927-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92927-254">Is Indexed</span></span>             | <span data-ttu-id="92927-255">否</span><span class="sxs-lookup"><span data-stu-id="92927-255">False</span></span>                                                |
| <span data-ttu-id="92927-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92927-256">In Global Catalog</span></span>      | <span data-ttu-id="92927-257">否</span><span class="sxs-lookup"><span data-stu-id="92927-257">False</span></span>                                                |
| <span data-ttu-id="92927-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92927-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="92927-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92927-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="92927-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92927-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="92927-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92927-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="92927-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-262">Search-Flags</span></span>           | <span data-ttu-id="92927-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92927-263">0x00000000</span></span>                                           |
| <span data-ttu-id="92927-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92927-264">System-Flags</span></span>           | <span data-ttu-id="92927-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92927-265">0x00000010</span></span>                                           |
| <span data-ttu-id="92927-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92927-266">Classes used in</span></span>        | [<span data-ttu-id="92927-267">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="92927-267">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






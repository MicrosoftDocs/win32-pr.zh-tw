---
title: 信任-驗證-外寄屬性
description: 信任之外寄部分的驗證資訊。
ms.assetid: 0b63554b-b57e-4ca5-8a78-2bce5ebfea2f
ms.tgt_platform: multiple
keywords:
- 信任-驗證-外寄屬性 AD 架構
- trustAuthOutgoing 屬性 AD 架構
topic_type:
- apiref
api_name:
- Trust-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1d462767f5ad756c936eb30f455c7982663ec0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687116"
---
# <a name="trust-auth-outgoing-attribute"></a><span data-ttu-id="17009-105">信任-驗證-外寄屬性</span><span class="sxs-lookup"><span data-stu-id="17009-105">Trust-Auth-Outgoing attribute</span></span>

<span data-ttu-id="17009-106">信任之外寄部分的驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="17009-106">Authentication information for the outgoing portion of a trust.</span></span>



| <span data-ttu-id="17009-107">進入</span><span class="sxs-lookup"><span data-stu-id="17009-107">Entry</span></span> | <span data-ttu-id="17009-108">值</span><span class="sxs-lookup"><span data-stu-id="17009-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="17009-109">CN</span><span class="sxs-lookup"><span data-stu-id="17009-109">CN</span></span>                | <span data-ttu-id="17009-110">信任-驗證-外寄</span><span class="sxs-lookup"><span data-stu-id="17009-110">Trust-Auth-Outgoing</span></span>                                   |
| <span data-ttu-id="17009-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="17009-111">Ldap-Display-Name</span></span> | <span data-ttu-id="17009-112">trustAuthOutgoing</span><span class="sxs-lookup"><span data-stu-id="17009-112">trustAuthOutgoing</span></span>                                     |
| <span data-ttu-id="17009-113">大小</span><span class="sxs-lookup"><span data-stu-id="17009-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="17009-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="17009-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="17009-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="17009-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="17009-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17009-116">Attribute-Id</span></span>      | <span data-ttu-id="17009-117">1.2.840.113556.1.4.135</span><span class="sxs-lookup"><span data-stu-id="17009-117">1.2.840.113556.1.4.135</span></span>                                |
| <span data-ttu-id="17009-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="17009-118">System-Id-Guid</span></span>    | <span data-ttu-id="17009-119">bf967a5f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="17009-119">bf967a5f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="17009-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="17009-120">Syntax</span></span>            | [<span data-ttu-id="17009-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="17009-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="17009-122">實作</span><span class="sxs-lookup"><span data-stu-id="17009-122">Implementations</span></span>

-   [<span data-ttu-id="17009-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="17009-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="17009-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17009-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17009-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17009-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17009-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17009-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17009-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17009-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17009-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17009-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="17009-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17009-129">Windows 2000 Server</span></span>



| <span data-ttu-id="17009-130">進入</span><span class="sxs-lookup"><span data-stu-id="17009-130">Entry</span></span> | <span data-ttu-id="17009-131">值</span><span class="sxs-lookup"><span data-stu-id="17009-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="17009-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17009-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17009-133">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="17009-134">System-Only</span></span>            | <span data-ttu-id="17009-135">否</span><span class="sxs-lookup"><span data-stu-id="17009-135">False</span></span>                                                |
| <span data-ttu-id="17009-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17009-136">Is-Single-Valued</span></span>       | <span data-ttu-id="17009-137">對</span><span class="sxs-lookup"><span data-stu-id="17009-137">True</span></span>                                                 |
| <span data-ttu-id="17009-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17009-138">Is Indexed</span></span>             | <span data-ttu-id="17009-139">否</span><span class="sxs-lookup"><span data-stu-id="17009-139">False</span></span>                                                |
| <span data-ttu-id="17009-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17009-140">In Global Catalog</span></span>      | <span data-ttu-id="17009-141">否</span><span class="sxs-lookup"><span data-stu-id="17009-141">False</span></span>                                                |
| <span data-ttu-id="17009-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17009-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="17009-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17009-143">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="17009-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17009-144">Range-Lower</span></span>            | <span data-ttu-id="17009-145">0</span><span class="sxs-lookup"><span data-stu-id="17009-145">0</span></span>                                                    |
| <span data-ttu-id="17009-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17009-146">Range-Upper</span></span>            | <span data-ttu-id="17009-147">32767</span><span class="sxs-lookup"><span data-stu-id="17009-147">32767</span></span>                                                |
| <span data-ttu-id="17009-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-148">Search-Flags</span></span>           | <span data-ttu-id="17009-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17009-149">0x00000000</span></span>                                           |
| <span data-ttu-id="17009-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-150">System-Flags</span></span>           | <span data-ttu-id="17009-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17009-151">0x00000010</span></span>                                           |
| <span data-ttu-id="17009-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17009-152">Classes used in</span></span>        | [<span data-ttu-id="17009-153">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="17009-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="17009-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17009-154">Windows Server 2003</span></span>



| <span data-ttu-id="17009-155">進入</span><span class="sxs-lookup"><span data-stu-id="17009-155">Entry</span></span> | <span data-ttu-id="17009-156">值</span><span class="sxs-lookup"><span data-stu-id="17009-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="17009-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17009-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17009-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="17009-159">System-Only</span></span>            | <span data-ttu-id="17009-160">否</span><span class="sxs-lookup"><span data-stu-id="17009-160">False</span></span>                                                |
| <span data-ttu-id="17009-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17009-161">Is-Single-Valued</span></span>       | <span data-ttu-id="17009-162">對</span><span class="sxs-lookup"><span data-stu-id="17009-162">True</span></span>                                                 |
| <span data-ttu-id="17009-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17009-163">Is Indexed</span></span>             | <span data-ttu-id="17009-164">否</span><span class="sxs-lookup"><span data-stu-id="17009-164">False</span></span>                                                |
| <span data-ttu-id="17009-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17009-165">In Global Catalog</span></span>      | <span data-ttu-id="17009-166">否</span><span class="sxs-lookup"><span data-stu-id="17009-166">False</span></span>                                                |
| <span data-ttu-id="17009-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17009-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="17009-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17009-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="17009-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17009-169">Range-Lower</span></span>            | <span data-ttu-id="17009-170">0</span><span class="sxs-lookup"><span data-stu-id="17009-170">0</span></span>                                                    |
| <span data-ttu-id="17009-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17009-171">Range-Upper</span></span>            | <span data-ttu-id="17009-172">32767</span><span class="sxs-lookup"><span data-stu-id="17009-172">32767</span></span>                                                |
| <span data-ttu-id="17009-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-173">Search-Flags</span></span>           | <span data-ttu-id="17009-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17009-174">0x00000000</span></span>                                           |
| <span data-ttu-id="17009-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-175">System-Flags</span></span>           | <span data-ttu-id="17009-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17009-176">0x00000010</span></span>                                           |
| <span data-ttu-id="17009-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17009-177">Classes used in</span></span>        | [<span data-ttu-id="17009-178">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="17009-178">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17009-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17009-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17009-180">進入</span><span class="sxs-lookup"><span data-stu-id="17009-180">Entry</span></span> | <span data-ttu-id="17009-181">值</span><span class="sxs-lookup"><span data-stu-id="17009-181">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="17009-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17009-182">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17009-183">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="17009-184">System-Only</span></span>            | <span data-ttu-id="17009-185">否</span><span class="sxs-lookup"><span data-stu-id="17009-185">False</span></span>                                                |
| <span data-ttu-id="17009-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17009-186">Is-Single-Valued</span></span>       | <span data-ttu-id="17009-187">對</span><span class="sxs-lookup"><span data-stu-id="17009-187">True</span></span>                                                 |
| <span data-ttu-id="17009-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17009-188">Is Indexed</span></span>             | <span data-ttu-id="17009-189">否</span><span class="sxs-lookup"><span data-stu-id="17009-189">False</span></span>                                                |
| <span data-ttu-id="17009-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17009-190">In Global Catalog</span></span>      | <span data-ttu-id="17009-191">否</span><span class="sxs-lookup"><span data-stu-id="17009-191">False</span></span>                                                |
| <span data-ttu-id="17009-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17009-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="17009-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17009-193">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="17009-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17009-194">Range-Lower</span></span>            | <span data-ttu-id="17009-195">0</span><span class="sxs-lookup"><span data-stu-id="17009-195">0</span></span>                                                    |
| <span data-ttu-id="17009-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17009-196">Range-Upper</span></span>            | <span data-ttu-id="17009-197">32767</span><span class="sxs-lookup"><span data-stu-id="17009-197">32767</span></span>                                                |
| <span data-ttu-id="17009-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-198">Search-Flags</span></span>           | <span data-ttu-id="17009-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17009-199">0x00000000</span></span>                                           |
| <span data-ttu-id="17009-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-200">System-Flags</span></span>           | <span data-ttu-id="17009-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17009-201">0x00000010</span></span>                                           |
| <span data-ttu-id="17009-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17009-202">Classes used in</span></span>        | [<span data-ttu-id="17009-203">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="17009-203">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17009-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17009-204">Windows Server 2008</span></span>



| <span data-ttu-id="17009-205">進入</span><span class="sxs-lookup"><span data-stu-id="17009-205">Entry</span></span> | <span data-ttu-id="17009-206">值</span><span class="sxs-lookup"><span data-stu-id="17009-206">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="17009-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17009-207">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17009-208">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="17009-209">System-Only</span></span>            | <span data-ttu-id="17009-210">否</span><span class="sxs-lookup"><span data-stu-id="17009-210">False</span></span>                                                |
| <span data-ttu-id="17009-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17009-211">Is-Single-Valued</span></span>       | <span data-ttu-id="17009-212">對</span><span class="sxs-lookup"><span data-stu-id="17009-212">True</span></span>                                                 |
| <span data-ttu-id="17009-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17009-213">Is Indexed</span></span>             | <span data-ttu-id="17009-214">否</span><span class="sxs-lookup"><span data-stu-id="17009-214">False</span></span>                                                |
| <span data-ttu-id="17009-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17009-215">In Global Catalog</span></span>      | <span data-ttu-id="17009-216">否</span><span class="sxs-lookup"><span data-stu-id="17009-216">False</span></span>                                                |
| <span data-ttu-id="17009-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17009-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="17009-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17009-218">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="17009-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17009-219">Range-Lower</span></span>            | <span data-ttu-id="17009-220">0</span><span class="sxs-lookup"><span data-stu-id="17009-220">0</span></span>                                                    |
| <span data-ttu-id="17009-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17009-221">Range-Upper</span></span>            | <span data-ttu-id="17009-222">32767</span><span class="sxs-lookup"><span data-stu-id="17009-222">32767</span></span>                                                |
| <span data-ttu-id="17009-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-223">Search-Flags</span></span>           | <span data-ttu-id="17009-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17009-224">0x00000000</span></span>                                           |
| <span data-ttu-id="17009-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-225">System-Flags</span></span>           | <span data-ttu-id="17009-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17009-226">0x00000010</span></span>                                           |
| <span data-ttu-id="17009-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17009-227">Classes used in</span></span>        | [<span data-ttu-id="17009-228">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="17009-228">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17009-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17009-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17009-230">進入</span><span class="sxs-lookup"><span data-stu-id="17009-230">Entry</span></span> | <span data-ttu-id="17009-231">值</span><span class="sxs-lookup"><span data-stu-id="17009-231">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="17009-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17009-232">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17009-233">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="17009-234">System-Only</span></span>            | <span data-ttu-id="17009-235">否</span><span class="sxs-lookup"><span data-stu-id="17009-235">False</span></span>                                                |
| <span data-ttu-id="17009-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17009-236">Is-Single-Valued</span></span>       | <span data-ttu-id="17009-237">對</span><span class="sxs-lookup"><span data-stu-id="17009-237">True</span></span>                                                 |
| <span data-ttu-id="17009-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17009-238">Is Indexed</span></span>             | <span data-ttu-id="17009-239">否</span><span class="sxs-lookup"><span data-stu-id="17009-239">False</span></span>                                                |
| <span data-ttu-id="17009-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17009-240">In Global Catalog</span></span>      | <span data-ttu-id="17009-241">否</span><span class="sxs-lookup"><span data-stu-id="17009-241">False</span></span>                                                |
| <span data-ttu-id="17009-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17009-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="17009-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17009-243">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="17009-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17009-244">Range-Lower</span></span>            | <span data-ttu-id="17009-245">0</span><span class="sxs-lookup"><span data-stu-id="17009-245">0</span></span>                                                    |
| <span data-ttu-id="17009-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17009-246">Range-Upper</span></span>            | <span data-ttu-id="17009-247">32767</span><span class="sxs-lookup"><span data-stu-id="17009-247">32767</span></span>                                                |
| <span data-ttu-id="17009-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-248">Search-Flags</span></span>           | <span data-ttu-id="17009-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17009-249">0x00000000</span></span>                                           |
| <span data-ttu-id="17009-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-250">System-Flags</span></span>           | <span data-ttu-id="17009-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17009-251">0x00000010</span></span>                                           |
| <span data-ttu-id="17009-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17009-252">Classes used in</span></span>        | [<span data-ttu-id="17009-253">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="17009-253">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17009-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17009-254">Windows Server 2012</span></span>



| <span data-ttu-id="17009-255">進入</span><span class="sxs-lookup"><span data-stu-id="17009-255">Entry</span></span> | <span data-ttu-id="17009-256">值</span><span class="sxs-lookup"><span data-stu-id="17009-256">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="17009-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17009-257">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17009-258">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="17009-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="17009-259">System-Only</span></span>            | <span data-ttu-id="17009-260">否</span><span class="sxs-lookup"><span data-stu-id="17009-260">False</span></span>                                                |
| <span data-ttu-id="17009-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17009-261">Is-Single-Valued</span></span>       | <span data-ttu-id="17009-262">對</span><span class="sxs-lookup"><span data-stu-id="17009-262">True</span></span>                                                 |
| <span data-ttu-id="17009-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17009-263">Is Indexed</span></span>             | <span data-ttu-id="17009-264">否</span><span class="sxs-lookup"><span data-stu-id="17009-264">False</span></span>                                                |
| <span data-ttu-id="17009-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17009-265">In Global Catalog</span></span>      | <span data-ttu-id="17009-266">否</span><span class="sxs-lookup"><span data-stu-id="17009-266">False</span></span>                                                |
| <span data-ttu-id="17009-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17009-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="17009-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17009-268">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="17009-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17009-269">Range-Lower</span></span>            | <span data-ttu-id="17009-270">0</span><span class="sxs-lookup"><span data-stu-id="17009-270">0</span></span>                                                    |
| <span data-ttu-id="17009-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17009-271">Range-Upper</span></span>            | <span data-ttu-id="17009-272">32767</span><span class="sxs-lookup"><span data-stu-id="17009-272">32767</span></span>                                                |
| <span data-ttu-id="17009-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-273">Search-Flags</span></span>           | <span data-ttu-id="17009-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17009-274">0x00000000</span></span>                                           |
| <span data-ttu-id="17009-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17009-275">System-Flags</span></span>           | <span data-ttu-id="17009-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17009-276">0x00000010</span></span>                                           |
| <span data-ttu-id="17009-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17009-277">Classes used in</span></span>        | [<span data-ttu-id="17009-278">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="17009-278">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






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
# <a name="trust-auth-outgoing-attribute"></a><span data-ttu-id="b3e35-105">信任-驗證-外寄屬性</span><span class="sxs-lookup"><span data-stu-id="b3e35-105">Trust-Auth-Outgoing attribute</span></span>

<span data-ttu-id="b3e35-106">信任之外寄部分的驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="b3e35-106">Authentication information for the outgoing portion of a trust.</span></span>



| <span data-ttu-id="b3e35-107">進入</span><span class="sxs-lookup"><span data-stu-id="b3e35-107">Entry</span></span> | <span data-ttu-id="b3e35-108">值</span><span class="sxs-lookup"><span data-stu-id="b3e35-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b3e35-109">CN</span><span class="sxs-lookup"><span data-stu-id="b3e35-109">CN</span></span>                | <span data-ttu-id="b3e35-110">信任-驗證-外寄</span><span class="sxs-lookup"><span data-stu-id="b3e35-110">Trust-Auth-Outgoing</span></span>                                   |
| <span data-ttu-id="b3e35-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b3e35-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b3e35-112">trustAuthOutgoing</span><span class="sxs-lookup"><span data-stu-id="b3e35-112">trustAuthOutgoing</span></span>                                     |
| <span data-ttu-id="b3e35-113">大小</span><span class="sxs-lookup"><span data-stu-id="b3e35-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b3e35-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b3e35-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="b3e35-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b3e35-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b3e35-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b3e35-116">Attribute-Id</span></span>      | <span data-ttu-id="b3e35-117">1.2.840.113556.1.4.135</span><span class="sxs-lookup"><span data-stu-id="b3e35-117">1.2.840.113556.1.4.135</span></span>                                |
| <span data-ttu-id="b3e35-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b3e35-118">System-Id-Guid</span></span>    | <span data-ttu-id="b3e35-119">bf967a5f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b3e35-119">bf967a5f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="b3e35-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3e35-120">Syntax</span></span>            | [<span data-ttu-id="b3e35-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b3e35-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b3e35-122">實作</span><span class="sxs-lookup"><span data-stu-id="b3e35-122">Implementations</span></span>

-   [<span data-ttu-id="b3e35-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b3e35-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b3e35-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b3e35-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b3e35-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b3e35-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b3e35-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b3e35-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b3e35-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b3e35-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b3e35-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b3e35-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b3e35-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3e35-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b3e35-130">進入</span><span class="sxs-lookup"><span data-stu-id="b3e35-130">Entry</span></span> | <span data-ttu-id="b3e35-131">值</span><span class="sxs-lookup"><span data-stu-id="b3e35-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b3e35-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3e35-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3e35-133">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3e35-134">System-Only</span></span>            | <span data-ttu-id="b3e35-135">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-135">False</span></span>                                                |
| <span data-ttu-id="b3e35-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3e35-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b3e35-137">對</span><span class="sxs-lookup"><span data-stu-id="b3e35-137">True</span></span>                                                 |
| <span data-ttu-id="b3e35-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3e35-138">Is Indexed</span></span>             | <span data-ttu-id="b3e35-139">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-139">False</span></span>                                                |
| <span data-ttu-id="b3e35-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3e35-140">In Global Catalog</span></span>      | <span data-ttu-id="b3e35-141">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-141">False</span></span>                                                |
| <span data-ttu-id="b3e35-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3e35-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3e35-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3e35-143">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b3e35-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3e35-144">Range-Lower</span></span>            | <span data-ttu-id="b3e35-145">0</span><span class="sxs-lookup"><span data-stu-id="b3e35-145">0</span></span>                                                    |
| <span data-ttu-id="b3e35-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3e35-146">Range-Upper</span></span>            | <span data-ttu-id="b3e35-147">32767</span><span class="sxs-lookup"><span data-stu-id="b3e35-147">32767</span></span>                                                |
| <span data-ttu-id="b3e35-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-148">Search-Flags</span></span>           | <span data-ttu-id="b3e35-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3e35-149">0x00000000</span></span>                                           |
| <span data-ttu-id="b3e35-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-150">System-Flags</span></span>           | <span data-ttu-id="b3e35-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3e35-151">0x00000010</span></span>                                           |
| <span data-ttu-id="b3e35-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3e35-152">Classes used in</span></span>        | [<span data-ttu-id="b3e35-153">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="b3e35-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b3e35-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b3e35-154">Windows Server 2003</span></span>



| <span data-ttu-id="b3e35-155">進入</span><span class="sxs-lookup"><span data-stu-id="b3e35-155">Entry</span></span> | <span data-ttu-id="b3e35-156">值</span><span class="sxs-lookup"><span data-stu-id="b3e35-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b3e35-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3e35-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3e35-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3e35-159">System-Only</span></span>            | <span data-ttu-id="b3e35-160">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-160">False</span></span>                                                |
| <span data-ttu-id="b3e35-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3e35-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b3e35-162">對</span><span class="sxs-lookup"><span data-stu-id="b3e35-162">True</span></span>                                                 |
| <span data-ttu-id="b3e35-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3e35-163">Is Indexed</span></span>             | <span data-ttu-id="b3e35-164">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-164">False</span></span>                                                |
| <span data-ttu-id="b3e35-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3e35-165">In Global Catalog</span></span>      | <span data-ttu-id="b3e35-166">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-166">False</span></span>                                                |
| <span data-ttu-id="b3e35-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3e35-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3e35-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3e35-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b3e35-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3e35-169">Range-Lower</span></span>            | <span data-ttu-id="b3e35-170">0</span><span class="sxs-lookup"><span data-stu-id="b3e35-170">0</span></span>                                                    |
| <span data-ttu-id="b3e35-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3e35-171">Range-Upper</span></span>            | <span data-ttu-id="b3e35-172">32767</span><span class="sxs-lookup"><span data-stu-id="b3e35-172">32767</span></span>                                                |
| <span data-ttu-id="b3e35-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-173">Search-Flags</span></span>           | <span data-ttu-id="b3e35-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3e35-174">0x00000000</span></span>                                           |
| <span data-ttu-id="b3e35-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-175">System-Flags</span></span>           | <span data-ttu-id="b3e35-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3e35-176">0x00000010</span></span>                                           |
| <span data-ttu-id="b3e35-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3e35-177">Classes used in</span></span>        | [<span data-ttu-id="b3e35-178">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="b3e35-178">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b3e35-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b3e35-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b3e35-180">進入</span><span class="sxs-lookup"><span data-stu-id="b3e35-180">Entry</span></span> | <span data-ttu-id="b3e35-181">值</span><span class="sxs-lookup"><span data-stu-id="b3e35-181">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b3e35-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3e35-182">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3e35-183">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3e35-184">System-Only</span></span>            | <span data-ttu-id="b3e35-185">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-185">False</span></span>                                                |
| <span data-ttu-id="b3e35-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3e35-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b3e35-187">對</span><span class="sxs-lookup"><span data-stu-id="b3e35-187">True</span></span>                                                 |
| <span data-ttu-id="b3e35-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3e35-188">Is Indexed</span></span>             | <span data-ttu-id="b3e35-189">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-189">False</span></span>                                                |
| <span data-ttu-id="b3e35-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3e35-190">In Global Catalog</span></span>      | <span data-ttu-id="b3e35-191">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-191">False</span></span>                                                |
| <span data-ttu-id="b3e35-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3e35-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3e35-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3e35-193">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b3e35-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3e35-194">Range-Lower</span></span>            | <span data-ttu-id="b3e35-195">0</span><span class="sxs-lookup"><span data-stu-id="b3e35-195">0</span></span>                                                    |
| <span data-ttu-id="b3e35-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3e35-196">Range-Upper</span></span>            | <span data-ttu-id="b3e35-197">32767</span><span class="sxs-lookup"><span data-stu-id="b3e35-197">32767</span></span>                                                |
| <span data-ttu-id="b3e35-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-198">Search-Flags</span></span>           | <span data-ttu-id="b3e35-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3e35-199">0x00000000</span></span>                                           |
| <span data-ttu-id="b3e35-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-200">System-Flags</span></span>           | <span data-ttu-id="b3e35-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3e35-201">0x00000010</span></span>                                           |
| <span data-ttu-id="b3e35-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3e35-202">Classes used in</span></span>        | [<span data-ttu-id="b3e35-203">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="b3e35-203">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b3e35-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3e35-204">Windows Server 2008</span></span>



| <span data-ttu-id="b3e35-205">進入</span><span class="sxs-lookup"><span data-stu-id="b3e35-205">Entry</span></span> | <span data-ttu-id="b3e35-206">值</span><span class="sxs-lookup"><span data-stu-id="b3e35-206">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b3e35-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3e35-207">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3e35-208">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3e35-209">System-Only</span></span>            | <span data-ttu-id="b3e35-210">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-210">False</span></span>                                                |
| <span data-ttu-id="b3e35-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3e35-211">Is-Single-Valued</span></span>       | <span data-ttu-id="b3e35-212">對</span><span class="sxs-lookup"><span data-stu-id="b3e35-212">True</span></span>                                                 |
| <span data-ttu-id="b3e35-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3e35-213">Is Indexed</span></span>             | <span data-ttu-id="b3e35-214">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-214">False</span></span>                                                |
| <span data-ttu-id="b3e35-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3e35-215">In Global Catalog</span></span>      | <span data-ttu-id="b3e35-216">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-216">False</span></span>                                                |
| <span data-ttu-id="b3e35-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3e35-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3e35-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3e35-218">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b3e35-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3e35-219">Range-Lower</span></span>            | <span data-ttu-id="b3e35-220">0</span><span class="sxs-lookup"><span data-stu-id="b3e35-220">0</span></span>                                                    |
| <span data-ttu-id="b3e35-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3e35-221">Range-Upper</span></span>            | <span data-ttu-id="b3e35-222">32767</span><span class="sxs-lookup"><span data-stu-id="b3e35-222">32767</span></span>                                                |
| <span data-ttu-id="b3e35-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-223">Search-Flags</span></span>           | <span data-ttu-id="b3e35-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3e35-224">0x00000000</span></span>                                           |
| <span data-ttu-id="b3e35-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-225">System-Flags</span></span>           | <span data-ttu-id="b3e35-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3e35-226">0x00000010</span></span>                                           |
| <span data-ttu-id="b3e35-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3e35-227">Classes used in</span></span>        | [<span data-ttu-id="b3e35-228">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="b3e35-228">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b3e35-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3e35-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b3e35-230">進入</span><span class="sxs-lookup"><span data-stu-id="b3e35-230">Entry</span></span> | <span data-ttu-id="b3e35-231">值</span><span class="sxs-lookup"><span data-stu-id="b3e35-231">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b3e35-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3e35-232">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3e35-233">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3e35-234">System-Only</span></span>            | <span data-ttu-id="b3e35-235">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-235">False</span></span>                                                |
| <span data-ttu-id="b3e35-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3e35-236">Is-Single-Valued</span></span>       | <span data-ttu-id="b3e35-237">對</span><span class="sxs-lookup"><span data-stu-id="b3e35-237">True</span></span>                                                 |
| <span data-ttu-id="b3e35-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3e35-238">Is Indexed</span></span>             | <span data-ttu-id="b3e35-239">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-239">False</span></span>                                                |
| <span data-ttu-id="b3e35-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3e35-240">In Global Catalog</span></span>      | <span data-ttu-id="b3e35-241">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-241">False</span></span>                                                |
| <span data-ttu-id="b3e35-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3e35-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3e35-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3e35-243">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b3e35-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3e35-244">Range-Lower</span></span>            | <span data-ttu-id="b3e35-245">0</span><span class="sxs-lookup"><span data-stu-id="b3e35-245">0</span></span>                                                    |
| <span data-ttu-id="b3e35-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3e35-246">Range-Upper</span></span>            | <span data-ttu-id="b3e35-247">32767</span><span class="sxs-lookup"><span data-stu-id="b3e35-247">32767</span></span>                                                |
| <span data-ttu-id="b3e35-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-248">Search-Flags</span></span>           | <span data-ttu-id="b3e35-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3e35-249">0x00000000</span></span>                                           |
| <span data-ttu-id="b3e35-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-250">System-Flags</span></span>           | <span data-ttu-id="b3e35-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3e35-251">0x00000010</span></span>                                           |
| <span data-ttu-id="b3e35-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3e35-252">Classes used in</span></span>        | [<span data-ttu-id="b3e35-253">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="b3e35-253">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b3e35-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3e35-254">Windows Server 2012</span></span>



| <span data-ttu-id="b3e35-255">進入</span><span class="sxs-lookup"><span data-stu-id="b3e35-255">Entry</span></span> | <span data-ttu-id="b3e35-256">值</span><span class="sxs-lookup"><span data-stu-id="b3e35-256">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b3e35-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3e35-257">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3e35-258">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b3e35-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3e35-259">System-Only</span></span>            | <span data-ttu-id="b3e35-260">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-260">False</span></span>                                                |
| <span data-ttu-id="b3e35-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3e35-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b3e35-262">對</span><span class="sxs-lookup"><span data-stu-id="b3e35-262">True</span></span>                                                 |
| <span data-ttu-id="b3e35-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3e35-263">Is Indexed</span></span>             | <span data-ttu-id="b3e35-264">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-264">False</span></span>                                                |
| <span data-ttu-id="b3e35-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3e35-265">In Global Catalog</span></span>      | <span data-ttu-id="b3e35-266">否</span><span class="sxs-lookup"><span data-stu-id="b3e35-266">False</span></span>                                                |
| <span data-ttu-id="b3e35-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3e35-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3e35-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3e35-268">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b3e35-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3e35-269">Range-Lower</span></span>            | <span data-ttu-id="b3e35-270">0</span><span class="sxs-lookup"><span data-stu-id="b3e35-270">0</span></span>                                                    |
| <span data-ttu-id="b3e35-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3e35-271">Range-Upper</span></span>            | <span data-ttu-id="b3e35-272">32767</span><span class="sxs-lookup"><span data-stu-id="b3e35-272">32767</span></span>                                                |
| <span data-ttu-id="b3e35-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-273">Search-Flags</span></span>           | <span data-ttu-id="b3e35-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3e35-274">0x00000000</span></span>                                           |
| <span data-ttu-id="b3e35-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3e35-275">System-Flags</span></span>           | <span data-ttu-id="b3e35-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3e35-276">0x00000010</span></span>                                           |
| <span data-ttu-id="b3e35-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3e35-277">Classes used in</span></span>        | [<span data-ttu-id="b3e35-278">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="b3e35-278">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






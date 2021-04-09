---
title: 內建-已修改-計數屬性
description: 內建修改計數屬性可用來支援 Windows NT 4.0 網域的複寫。
ms.assetid: e5a0f299-1e69-4b47-a0b1-e5bcf7bd47eb
ms.tgt_platform: multiple
keywords:
- 內建-已修改-計數屬性 AD 架構
- builtinModifiedCount 屬性 AD 架構
topic_type:
- apiref
api_name:
- Builtin-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731cd27ef5cb5d25dcd4bced4dbc5932225ba5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108232"
---
# <a name="builtin-modified-count-attribute"></a><span data-ttu-id="565bd-105">內建-已修改-計數屬性</span><span class="sxs-lookup"><span data-stu-id="565bd-105">Builtin-Modified-Count attribute</span></span>

<span data-ttu-id="565bd-106">內 **建修改計數** 屬性可用來支援 Windows NT 4.0 網域的複寫。</span><span class="sxs-lookup"><span data-stu-id="565bd-106">The **Builtin-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="565bd-107">進入</span><span class="sxs-lookup"><span data-stu-id="565bd-107">Entry</span></span> | <span data-ttu-id="565bd-108">值</span><span class="sxs-lookup"><span data-stu-id="565bd-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="565bd-109">CN</span><span class="sxs-lookup"><span data-stu-id="565bd-109">CN</span></span>                | <span data-ttu-id="565bd-110">內建-已修改-計數</span><span class="sxs-lookup"><span data-stu-id="565bd-110">Builtin-Modified-Count</span></span>               |
| <span data-ttu-id="565bd-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="565bd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="565bd-112">builtinModifiedCount</span><span class="sxs-lookup"><span data-stu-id="565bd-112">builtinModifiedCount</span></span>                 |
| <span data-ttu-id="565bd-113">大小</span><span class="sxs-lookup"><span data-stu-id="565bd-113">Size</span></span>              | <span data-ttu-id="565bd-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="565bd-114">8 bytes</span></span>                              |
| <span data-ttu-id="565bd-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="565bd-115">Update Privilege</span></span>  | <span data-ttu-id="565bd-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="565bd-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="565bd-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="565bd-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="565bd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="565bd-118">Attribute-Id</span></span>      | <span data-ttu-id="565bd-119">1.2.840.113556.1.4.14</span><span class="sxs-lookup"><span data-stu-id="565bd-119">1.2.840.113556.1.4.14</span></span>                |
| <span data-ttu-id="565bd-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="565bd-120">System-Id-Guid</span></span>    | <span data-ttu-id="565bd-121">bf967930-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="565bd-121">bf967930-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="565bd-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="565bd-122">Syntax</span></span>            | [<span data-ttu-id="565bd-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="565bd-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="565bd-124">實作</span><span class="sxs-lookup"><span data-stu-id="565bd-124">Implementations</span></span>

-   [<span data-ttu-id="565bd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="565bd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="565bd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="565bd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="565bd-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="565bd-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="565bd-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="565bd-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="565bd-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="565bd-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="565bd-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="565bd-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="565bd-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="565bd-131">Windows 2000 Server</span></span>



| <span data-ttu-id="565bd-132">進入</span><span class="sxs-lookup"><span data-stu-id="565bd-132">Entry</span></span> | <span data-ttu-id="565bd-133">值</span><span class="sxs-lookup"><span data-stu-id="565bd-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="565bd-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="565bd-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="565bd-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="565bd-136">System-Only</span></span>            | <span data-ttu-id="565bd-137">否</span><span class="sxs-lookup"><span data-stu-id="565bd-137">False</span></span>                                        |
| <span data-ttu-id="565bd-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="565bd-138">Is-Single-Valued</span></span>       | <span data-ttu-id="565bd-139">對</span><span class="sxs-lookup"><span data-stu-id="565bd-139">True</span></span>                                         |
| <span data-ttu-id="565bd-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="565bd-140">Is Indexed</span></span>             | <span data-ttu-id="565bd-141">否</span><span class="sxs-lookup"><span data-stu-id="565bd-141">False</span></span>                                        |
| <span data-ttu-id="565bd-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="565bd-142">In Global Catalog</span></span>      | <span data-ttu-id="565bd-143">否</span><span class="sxs-lookup"><span data-stu-id="565bd-143">False</span></span>                                        |
| <span data-ttu-id="565bd-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="565bd-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="565bd-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="565bd-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="565bd-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="565bd-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="565bd-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="565bd-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="565bd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-148">Search-Flags</span></span>           | <span data-ttu-id="565bd-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="565bd-149">0x00000000</span></span>                                   |
| <span data-ttu-id="565bd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-150">System-Flags</span></span>           | <span data-ttu-id="565bd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="565bd-151">0x00000010</span></span>                                   |
| <span data-ttu-id="565bd-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="565bd-152">Classes used in</span></span>        | [<span data-ttu-id="565bd-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="565bd-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="565bd-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="565bd-154">Windows Server 2003</span></span>



| <span data-ttu-id="565bd-155">進入</span><span class="sxs-lookup"><span data-stu-id="565bd-155">Entry</span></span> | <span data-ttu-id="565bd-156">值</span><span class="sxs-lookup"><span data-stu-id="565bd-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="565bd-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="565bd-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="565bd-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="565bd-159">System-Only</span></span>            | <span data-ttu-id="565bd-160">否</span><span class="sxs-lookup"><span data-stu-id="565bd-160">False</span></span>                                        |
| <span data-ttu-id="565bd-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="565bd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="565bd-162">對</span><span class="sxs-lookup"><span data-stu-id="565bd-162">True</span></span>                                         |
| <span data-ttu-id="565bd-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="565bd-163">Is Indexed</span></span>             | <span data-ttu-id="565bd-164">否</span><span class="sxs-lookup"><span data-stu-id="565bd-164">False</span></span>                                        |
| <span data-ttu-id="565bd-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="565bd-165">In Global Catalog</span></span>      | <span data-ttu-id="565bd-166">否</span><span class="sxs-lookup"><span data-stu-id="565bd-166">False</span></span>                                        |
| <span data-ttu-id="565bd-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="565bd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="565bd-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="565bd-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="565bd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="565bd-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="565bd-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="565bd-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="565bd-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-171">Search-Flags</span></span>           | <span data-ttu-id="565bd-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="565bd-172">0x00000000</span></span>                                   |
| <span data-ttu-id="565bd-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-173">System-Flags</span></span>           | <span data-ttu-id="565bd-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="565bd-174">0x00000010</span></span>                                   |
| <span data-ttu-id="565bd-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="565bd-175">Classes used in</span></span>        | [<span data-ttu-id="565bd-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="565bd-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="565bd-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="565bd-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="565bd-178">進入</span><span class="sxs-lookup"><span data-stu-id="565bd-178">Entry</span></span> | <span data-ttu-id="565bd-179">值</span><span class="sxs-lookup"><span data-stu-id="565bd-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="565bd-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="565bd-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="565bd-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="565bd-182">System-Only</span></span>            | <span data-ttu-id="565bd-183">否</span><span class="sxs-lookup"><span data-stu-id="565bd-183">False</span></span>                                        |
| <span data-ttu-id="565bd-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="565bd-184">Is-Single-Valued</span></span>       | <span data-ttu-id="565bd-185">對</span><span class="sxs-lookup"><span data-stu-id="565bd-185">True</span></span>                                         |
| <span data-ttu-id="565bd-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="565bd-186">Is Indexed</span></span>             | <span data-ttu-id="565bd-187">否</span><span class="sxs-lookup"><span data-stu-id="565bd-187">False</span></span>                                        |
| <span data-ttu-id="565bd-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="565bd-188">In Global Catalog</span></span>      | <span data-ttu-id="565bd-189">否</span><span class="sxs-lookup"><span data-stu-id="565bd-189">False</span></span>                                        |
| <span data-ttu-id="565bd-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="565bd-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="565bd-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="565bd-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="565bd-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="565bd-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="565bd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="565bd-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="565bd-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-194">Search-Flags</span></span>           | <span data-ttu-id="565bd-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="565bd-195">0x00000000</span></span>                                   |
| <span data-ttu-id="565bd-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-196">System-Flags</span></span>           | <span data-ttu-id="565bd-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="565bd-197">0x00000010</span></span>                                   |
| <span data-ttu-id="565bd-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="565bd-198">Classes used in</span></span>        | [<span data-ttu-id="565bd-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="565bd-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="565bd-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="565bd-200">Windows Server 2008</span></span>



| <span data-ttu-id="565bd-201">進入</span><span class="sxs-lookup"><span data-stu-id="565bd-201">Entry</span></span> | <span data-ttu-id="565bd-202">值</span><span class="sxs-lookup"><span data-stu-id="565bd-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="565bd-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="565bd-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="565bd-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="565bd-205">System-Only</span></span>            | <span data-ttu-id="565bd-206">否</span><span class="sxs-lookup"><span data-stu-id="565bd-206">False</span></span>                                        |
| <span data-ttu-id="565bd-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="565bd-207">Is-Single-Valued</span></span>       | <span data-ttu-id="565bd-208">對</span><span class="sxs-lookup"><span data-stu-id="565bd-208">True</span></span>                                         |
| <span data-ttu-id="565bd-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="565bd-209">Is Indexed</span></span>             | <span data-ttu-id="565bd-210">否</span><span class="sxs-lookup"><span data-stu-id="565bd-210">False</span></span>                                        |
| <span data-ttu-id="565bd-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="565bd-211">In Global Catalog</span></span>      | <span data-ttu-id="565bd-212">否</span><span class="sxs-lookup"><span data-stu-id="565bd-212">False</span></span>                                        |
| <span data-ttu-id="565bd-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="565bd-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="565bd-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="565bd-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="565bd-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="565bd-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="565bd-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="565bd-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="565bd-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-217">Search-Flags</span></span>           | <span data-ttu-id="565bd-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="565bd-218">0x00000000</span></span>                                   |
| <span data-ttu-id="565bd-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-219">System-Flags</span></span>           | <span data-ttu-id="565bd-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="565bd-220">0x00000010</span></span>                                   |
| <span data-ttu-id="565bd-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="565bd-221">Classes used in</span></span>        | [<span data-ttu-id="565bd-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="565bd-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="565bd-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="565bd-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="565bd-224">進入</span><span class="sxs-lookup"><span data-stu-id="565bd-224">Entry</span></span> | <span data-ttu-id="565bd-225">值</span><span class="sxs-lookup"><span data-stu-id="565bd-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="565bd-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="565bd-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="565bd-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="565bd-228">System-Only</span></span>            | <span data-ttu-id="565bd-229">否</span><span class="sxs-lookup"><span data-stu-id="565bd-229">False</span></span>                                        |
| <span data-ttu-id="565bd-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="565bd-230">Is-Single-Valued</span></span>       | <span data-ttu-id="565bd-231">對</span><span class="sxs-lookup"><span data-stu-id="565bd-231">True</span></span>                                         |
| <span data-ttu-id="565bd-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="565bd-232">Is Indexed</span></span>             | <span data-ttu-id="565bd-233">否</span><span class="sxs-lookup"><span data-stu-id="565bd-233">False</span></span>                                        |
| <span data-ttu-id="565bd-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="565bd-234">In Global Catalog</span></span>      | <span data-ttu-id="565bd-235">否</span><span class="sxs-lookup"><span data-stu-id="565bd-235">False</span></span>                                        |
| <span data-ttu-id="565bd-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="565bd-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="565bd-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="565bd-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="565bd-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="565bd-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="565bd-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="565bd-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="565bd-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-240">Search-Flags</span></span>           | <span data-ttu-id="565bd-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="565bd-241">0x00000000</span></span>                                   |
| <span data-ttu-id="565bd-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-242">System-Flags</span></span>           | <span data-ttu-id="565bd-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="565bd-243">0x00000010</span></span>                                   |
| <span data-ttu-id="565bd-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="565bd-244">Classes used in</span></span>        | [<span data-ttu-id="565bd-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="565bd-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="565bd-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="565bd-246">Windows Server 2012</span></span>



| <span data-ttu-id="565bd-247">進入</span><span class="sxs-lookup"><span data-stu-id="565bd-247">Entry</span></span> | <span data-ttu-id="565bd-248">值</span><span class="sxs-lookup"><span data-stu-id="565bd-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="565bd-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="565bd-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="565bd-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="565bd-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="565bd-251">System-Only</span></span>            | <span data-ttu-id="565bd-252">否</span><span class="sxs-lookup"><span data-stu-id="565bd-252">False</span></span>                                        |
| <span data-ttu-id="565bd-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="565bd-253">Is-Single-Valued</span></span>       | <span data-ttu-id="565bd-254">對</span><span class="sxs-lookup"><span data-stu-id="565bd-254">True</span></span>                                         |
| <span data-ttu-id="565bd-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="565bd-255">Is Indexed</span></span>             | <span data-ttu-id="565bd-256">否</span><span class="sxs-lookup"><span data-stu-id="565bd-256">False</span></span>                                        |
| <span data-ttu-id="565bd-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="565bd-257">In Global Catalog</span></span>      | <span data-ttu-id="565bd-258">否</span><span class="sxs-lookup"><span data-stu-id="565bd-258">False</span></span>                                        |
| <span data-ttu-id="565bd-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="565bd-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="565bd-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="565bd-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="565bd-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="565bd-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="565bd-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="565bd-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="565bd-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-263">Search-Flags</span></span>           | <span data-ttu-id="565bd-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="565bd-264">0x00000000</span></span>                                   |
| <span data-ttu-id="565bd-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="565bd-265">System-Flags</span></span>           | <span data-ttu-id="565bd-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="565bd-266">0x00000010</span></span>                                   |
| <span data-ttu-id="565bd-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="565bd-267">Classes used in</span></span>        | [<span data-ttu-id="565bd-268">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="565bd-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






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
# <a name="builtin-modified-count-attribute"></a><span data-ttu-id="2a8e1-105">內建-已修改-計數屬性</span><span class="sxs-lookup"><span data-stu-id="2a8e1-105">Builtin-Modified-Count attribute</span></span>

<span data-ttu-id="2a8e1-106">內 **建修改計數** 屬性可用來支援 Windows NT 4.0 網域的複寫。</span><span class="sxs-lookup"><span data-stu-id="2a8e1-106">The **Builtin-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="2a8e1-107">進入</span><span class="sxs-lookup"><span data-stu-id="2a8e1-107">Entry</span></span> | <span data-ttu-id="2a8e1-108">值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2a8e1-109">CN</span><span class="sxs-lookup"><span data-stu-id="2a8e1-109">CN</span></span>                | <span data-ttu-id="2a8e1-110">內建-已修改-計數</span><span class="sxs-lookup"><span data-stu-id="2a8e1-110">Builtin-Modified-Count</span></span>               |
| <span data-ttu-id="2a8e1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2a8e1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2a8e1-112">builtinModifiedCount</span><span class="sxs-lookup"><span data-stu-id="2a8e1-112">builtinModifiedCount</span></span>                 |
| <span data-ttu-id="2a8e1-113">大小</span><span class="sxs-lookup"><span data-stu-id="2a8e1-113">Size</span></span>              | <span data-ttu-id="2a8e1-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="2a8e1-114">8 bytes</span></span>                              |
| <span data-ttu-id="2a8e1-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2a8e1-115">Update Privilege</span></span>  | <span data-ttu-id="2a8e1-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="2a8e1-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="2a8e1-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2a8e1-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2a8e1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2a8e1-118">Attribute-Id</span></span>      | <span data-ttu-id="2a8e1-119">1.2.840.113556.1.4.14</span><span class="sxs-lookup"><span data-stu-id="2a8e1-119">1.2.840.113556.1.4.14</span></span>                |
| <span data-ttu-id="2a8e1-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2a8e1-120">System-Id-Guid</span></span>    | <span data-ttu-id="2a8e1-121">bf967930-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2a8e1-121">bf967930-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="2a8e1-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a8e1-122">Syntax</span></span>            | [<span data-ttu-id="2a8e1-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2a8e1-124">實作</span><span class="sxs-lookup"><span data-stu-id="2a8e1-124">Implementations</span></span>

-   [<span data-ttu-id="2a8e1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2a8e1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2a8e1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2a8e1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2a8e1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2a8e1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2a8e1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a8e1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2a8e1-132">進入</span><span class="sxs-lookup"><span data-stu-id="2a8e1-132">Entry</span></span> | <span data-ttu-id="2a8e1-133">值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2a8e1-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a8e1-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8e1-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8e1-136">System-Only</span></span>            | <span data-ttu-id="2a8e1-137">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-137">False</span></span>                                        |
| <span data-ttu-id="2a8e1-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8e1-139">對</span><span class="sxs-lookup"><span data-stu-id="2a8e1-139">True</span></span>                                         |
| <span data-ttu-id="2a8e1-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a8e1-140">Is Indexed</span></span>             | <span data-ttu-id="2a8e1-141">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-141">False</span></span>                                        |
| <span data-ttu-id="2a8e1-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a8e1-142">In Global Catalog</span></span>      | <span data-ttu-id="2a8e1-143">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-143">False</span></span>                                        |
| <span data-ttu-id="2a8e1-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a8e1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8e1-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a8e1-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2a8e1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8e1-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8e1-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-148">Search-Flags</span></span>           | <span data-ttu-id="2a8e1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8e1-149">0x00000000</span></span>                                   |
| <span data-ttu-id="2a8e1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-150">System-Flags</span></span>           | <span data-ttu-id="2a8e1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8e1-151">0x00000010</span></span>                                   |
| <span data-ttu-id="2a8e1-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a8e1-152">Classes used in</span></span>        | [<span data-ttu-id="2a8e1-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2a8e1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a8e1-154">Windows Server 2003</span></span>



| <span data-ttu-id="2a8e1-155">進入</span><span class="sxs-lookup"><span data-stu-id="2a8e1-155">Entry</span></span> | <span data-ttu-id="2a8e1-156">值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2a8e1-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a8e1-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8e1-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8e1-159">System-Only</span></span>            | <span data-ttu-id="2a8e1-160">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-160">False</span></span>                                        |
| <span data-ttu-id="2a8e1-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8e1-162">對</span><span class="sxs-lookup"><span data-stu-id="2a8e1-162">True</span></span>                                         |
| <span data-ttu-id="2a8e1-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a8e1-163">Is Indexed</span></span>             | <span data-ttu-id="2a8e1-164">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-164">False</span></span>                                        |
| <span data-ttu-id="2a8e1-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a8e1-165">In Global Catalog</span></span>      | <span data-ttu-id="2a8e1-166">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-166">False</span></span>                                        |
| <span data-ttu-id="2a8e1-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a8e1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8e1-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a8e1-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2a8e1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8e1-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8e1-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-171">Search-Flags</span></span>           | <span data-ttu-id="2a8e1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8e1-172">0x00000000</span></span>                                   |
| <span data-ttu-id="2a8e1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-173">System-Flags</span></span>           | <span data-ttu-id="2a8e1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8e1-174">0x00000010</span></span>                                   |
| <span data-ttu-id="2a8e1-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a8e1-175">Classes used in</span></span>        | [<span data-ttu-id="2a8e1-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2a8e1-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2a8e1-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2a8e1-178">進入</span><span class="sxs-lookup"><span data-stu-id="2a8e1-178">Entry</span></span> | <span data-ttu-id="2a8e1-179">值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2a8e1-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a8e1-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8e1-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8e1-182">System-Only</span></span>            | <span data-ttu-id="2a8e1-183">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-183">False</span></span>                                        |
| <span data-ttu-id="2a8e1-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8e1-185">對</span><span class="sxs-lookup"><span data-stu-id="2a8e1-185">True</span></span>                                         |
| <span data-ttu-id="2a8e1-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a8e1-186">Is Indexed</span></span>             | <span data-ttu-id="2a8e1-187">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-187">False</span></span>                                        |
| <span data-ttu-id="2a8e1-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a8e1-188">In Global Catalog</span></span>      | <span data-ttu-id="2a8e1-189">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-189">False</span></span>                                        |
| <span data-ttu-id="2a8e1-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a8e1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8e1-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a8e1-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2a8e1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8e1-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8e1-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-194">Search-Flags</span></span>           | <span data-ttu-id="2a8e1-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8e1-195">0x00000000</span></span>                                   |
| <span data-ttu-id="2a8e1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-196">System-Flags</span></span>           | <span data-ttu-id="2a8e1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8e1-197">0x00000010</span></span>                                   |
| <span data-ttu-id="2a8e1-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a8e1-198">Classes used in</span></span>        | [<span data-ttu-id="2a8e1-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2a8e1-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a8e1-200">Windows Server 2008</span></span>



| <span data-ttu-id="2a8e1-201">進入</span><span class="sxs-lookup"><span data-stu-id="2a8e1-201">Entry</span></span> | <span data-ttu-id="2a8e1-202">值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2a8e1-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a8e1-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8e1-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8e1-205">System-Only</span></span>            | <span data-ttu-id="2a8e1-206">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-206">False</span></span>                                        |
| <span data-ttu-id="2a8e1-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8e1-208">對</span><span class="sxs-lookup"><span data-stu-id="2a8e1-208">True</span></span>                                         |
| <span data-ttu-id="2a8e1-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a8e1-209">Is Indexed</span></span>             | <span data-ttu-id="2a8e1-210">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-210">False</span></span>                                        |
| <span data-ttu-id="2a8e1-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a8e1-211">In Global Catalog</span></span>      | <span data-ttu-id="2a8e1-212">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-212">False</span></span>                                        |
| <span data-ttu-id="2a8e1-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a8e1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8e1-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a8e1-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2a8e1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8e1-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8e1-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-217">Search-Flags</span></span>           | <span data-ttu-id="2a8e1-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8e1-218">0x00000000</span></span>                                   |
| <span data-ttu-id="2a8e1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-219">System-Flags</span></span>           | <span data-ttu-id="2a8e1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8e1-220">0x00000010</span></span>                                   |
| <span data-ttu-id="2a8e1-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a8e1-221">Classes used in</span></span>        | [<span data-ttu-id="2a8e1-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2a8e1-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a8e1-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2a8e1-224">進入</span><span class="sxs-lookup"><span data-stu-id="2a8e1-224">Entry</span></span> | <span data-ttu-id="2a8e1-225">值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2a8e1-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a8e1-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8e1-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8e1-228">System-Only</span></span>            | <span data-ttu-id="2a8e1-229">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-229">False</span></span>                                        |
| <span data-ttu-id="2a8e1-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8e1-231">對</span><span class="sxs-lookup"><span data-stu-id="2a8e1-231">True</span></span>                                         |
| <span data-ttu-id="2a8e1-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a8e1-232">Is Indexed</span></span>             | <span data-ttu-id="2a8e1-233">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-233">False</span></span>                                        |
| <span data-ttu-id="2a8e1-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a8e1-234">In Global Catalog</span></span>      | <span data-ttu-id="2a8e1-235">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-235">False</span></span>                                        |
| <span data-ttu-id="2a8e1-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a8e1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8e1-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a8e1-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2a8e1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8e1-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8e1-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-240">Search-Flags</span></span>           | <span data-ttu-id="2a8e1-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8e1-241">0x00000000</span></span>                                   |
| <span data-ttu-id="2a8e1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-242">System-Flags</span></span>           | <span data-ttu-id="2a8e1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8e1-243">0x00000010</span></span>                                   |
| <span data-ttu-id="2a8e1-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a8e1-244">Classes used in</span></span>        | [<span data-ttu-id="2a8e1-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2a8e1-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a8e1-246">Windows Server 2012</span></span>



| <span data-ttu-id="2a8e1-247">進入</span><span class="sxs-lookup"><span data-stu-id="2a8e1-247">Entry</span></span> | <span data-ttu-id="2a8e1-248">值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2a8e1-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a8e1-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a8e1-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2a8e1-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a8e1-251">System-Only</span></span>            | <span data-ttu-id="2a8e1-252">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-252">False</span></span>                                        |
| <span data-ttu-id="2a8e1-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a8e1-253">Is-Single-Valued</span></span>       | <span data-ttu-id="2a8e1-254">對</span><span class="sxs-lookup"><span data-stu-id="2a8e1-254">True</span></span>                                         |
| <span data-ttu-id="2a8e1-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a8e1-255">Is Indexed</span></span>             | <span data-ttu-id="2a8e1-256">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-256">False</span></span>                                        |
| <span data-ttu-id="2a8e1-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a8e1-257">In Global Catalog</span></span>      | <span data-ttu-id="2a8e1-258">否</span><span class="sxs-lookup"><span data-stu-id="2a8e1-258">False</span></span>                                        |
| <span data-ttu-id="2a8e1-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a8e1-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a8e1-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a8e1-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2a8e1-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a8e1-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a8e1-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2a8e1-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-263">Search-Flags</span></span>           | <span data-ttu-id="2a8e1-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a8e1-264">0x00000000</span></span>                                   |
| <span data-ttu-id="2a8e1-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a8e1-265">System-Flags</span></span>           | <span data-ttu-id="2a8e1-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a8e1-266">0x00000010</span></span>                                   |
| <span data-ttu-id="2a8e1-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a8e1-267">Classes used in</span></span>        | [<span data-ttu-id="2a8e1-268">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="2a8e1-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






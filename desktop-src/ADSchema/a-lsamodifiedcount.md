---
title: LSA-已修改-計數屬性
description: LSA 修改計數屬性是用來支援 Windows NT 4.0 網域的複寫。
ms.assetid: 6af5931c-5d4f-4061-81a1-e8947d760abc
ms.tgt_platform: multiple
keywords:
- LSA-已修改-計數屬性 AD 架構
- lSAModifiedCount 屬性 AD 架構
topic_type:
- apiref
api_name:
- LSA-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042d4d52974457eb1853a3705adb87cc24a7dc3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973324"
---
# <a name="lsa-modified-count-attribute"></a><span data-ttu-id="7b598-105">LSA-已修改-計數屬性</span><span class="sxs-lookup"><span data-stu-id="7b598-105">LSA-Modified-Count attribute</span></span>

<span data-ttu-id="7b598-106">**LSA 修改計數** 屬性是用來支援 Windows NT 4.0 網域的複寫。</span><span class="sxs-lookup"><span data-stu-id="7b598-106">The **LSA-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="7b598-107">進入</span><span class="sxs-lookup"><span data-stu-id="7b598-107">Entry</span></span> | <span data-ttu-id="7b598-108">值</span><span class="sxs-lookup"><span data-stu-id="7b598-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7b598-109">CN</span><span class="sxs-lookup"><span data-stu-id="7b598-109">CN</span></span>                | <span data-ttu-id="7b598-110">LSA-已修改-計數</span><span class="sxs-lookup"><span data-stu-id="7b598-110">LSA-Modified-Count</span></span>                   |
| <span data-ttu-id="7b598-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7b598-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7b598-112">lSAModifiedCount</span><span class="sxs-lookup"><span data-stu-id="7b598-112">lSAModifiedCount</span></span>                     |
| <span data-ttu-id="7b598-113">大小</span><span class="sxs-lookup"><span data-stu-id="7b598-113">Size</span></span>              | <span data-ttu-id="7b598-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="7b598-114">8 bytes</span></span>                              |
| <span data-ttu-id="7b598-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7b598-115">Update Privilege</span></span>  | <span data-ttu-id="7b598-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7b598-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="7b598-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7b598-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7b598-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7b598-118">Attribute-Id</span></span>      | <span data-ttu-id="7b598-119">1.2.840.113556.1.4.67</span><span class="sxs-lookup"><span data-stu-id="7b598-119">1.2.840.113556.1.4.67</span></span>                |
| <span data-ttu-id="7b598-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7b598-120">System-Id-Guid</span></span>    | <span data-ttu-id="7b598-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7b598-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7b598-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b598-122">Syntax</span></span>            | [<span data-ttu-id="7b598-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="7b598-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7b598-124">實作</span><span class="sxs-lookup"><span data-stu-id="7b598-124">Implementations</span></span>

-   [<span data-ttu-id="7b598-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7b598-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7b598-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7b598-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7b598-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7b598-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7b598-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7b598-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7b598-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7b598-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7b598-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7b598-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7b598-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7b598-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7b598-132">進入</span><span class="sxs-lookup"><span data-stu-id="7b598-132">Entry</span></span> | <span data-ttu-id="7b598-133">值</span><span class="sxs-lookup"><span data-stu-id="7b598-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7b598-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b598-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b598-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b598-136">System-Only</span></span>            | <span data-ttu-id="7b598-137">否</span><span class="sxs-lookup"><span data-stu-id="7b598-137">False</span></span>                                        |
| <span data-ttu-id="7b598-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b598-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7b598-139">對</span><span class="sxs-lookup"><span data-stu-id="7b598-139">True</span></span>                                         |
| <span data-ttu-id="7b598-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b598-140">Is Indexed</span></span>             | <span data-ttu-id="7b598-141">否</span><span class="sxs-lookup"><span data-stu-id="7b598-141">False</span></span>                                        |
| <span data-ttu-id="7b598-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b598-142">In Global Catalog</span></span>      | <span data-ttu-id="7b598-143">否</span><span class="sxs-lookup"><span data-stu-id="7b598-143">False</span></span>                                        |
| <span data-ttu-id="7b598-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b598-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b598-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b598-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7b598-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b598-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7b598-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b598-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7b598-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-148">Search-Flags</span></span>           | <span data-ttu-id="7b598-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b598-149">0x00000000</span></span>                                   |
| <span data-ttu-id="7b598-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-150">System-Flags</span></span>           | <span data-ttu-id="7b598-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b598-151">0x00000010</span></span>                                   |
| <span data-ttu-id="7b598-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b598-152">Classes used in</span></span>        | [<span data-ttu-id="7b598-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7b598-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7b598-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7b598-154">Windows Server 2003</span></span>



| <span data-ttu-id="7b598-155">進入</span><span class="sxs-lookup"><span data-stu-id="7b598-155">Entry</span></span> | <span data-ttu-id="7b598-156">值</span><span class="sxs-lookup"><span data-stu-id="7b598-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7b598-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b598-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b598-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b598-159">System-Only</span></span>            | <span data-ttu-id="7b598-160">否</span><span class="sxs-lookup"><span data-stu-id="7b598-160">False</span></span>                                        |
| <span data-ttu-id="7b598-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b598-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7b598-162">對</span><span class="sxs-lookup"><span data-stu-id="7b598-162">True</span></span>                                         |
| <span data-ttu-id="7b598-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b598-163">Is Indexed</span></span>             | <span data-ttu-id="7b598-164">否</span><span class="sxs-lookup"><span data-stu-id="7b598-164">False</span></span>                                        |
| <span data-ttu-id="7b598-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b598-165">In Global Catalog</span></span>      | <span data-ttu-id="7b598-166">否</span><span class="sxs-lookup"><span data-stu-id="7b598-166">False</span></span>                                        |
| <span data-ttu-id="7b598-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b598-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b598-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b598-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7b598-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b598-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7b598-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b598-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7b598-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-171">Search-Flags</span></span>           | <span data-ttu-id="7b598-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b598-172">0x00000000</span></span>                                   |
| <span data-ttu-id="7b598-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-173">System-Flags</span></span>           | <span data-ttu-id="7b598-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b598-174">0x00000010</span></span>                                   |
| <span data-ttu-id="7b598-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b598-175">Classes used in</span></span>        | [<span data-ttu-id="7b598-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7b598-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7b598-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7b598-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7b598-178">進入</span><span class="sxs-lookup"><span data-stu-id="7b598-178">Entry</span></span> | <span data-ttu-id="7b598-179">值</span><span class="sxs-lookup"><span data-stu-id="7b598-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7b598-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b598-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b598-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b598-182">System-Only</span></span>            | <span data-ttu-id="7b598-183">否</span><span class="sxs-lookup"><span data-stu-id="7b598-183">False</span></span>                                        |
| <span data-ttu-id="7b598-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b598-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7b598-185">對</span><span class="sxs-lookup"><span data-stu-id="7b598-185">True</span></span>                                         |
| <span data-ttu-id="7b598-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b598-186">Is Indexed</span></span>             | <span data-ttu-id="7b598-187">否</span><span class="sxs-lookup"><span data-stu-id="7b598-187">False</span></span>                                        |
| <span data-ttu-id="7b598-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b598-188">In Global Catalog</span></span>      | <span data-ttu-id="7b598-189">否</span><span class="sxs-lookup"><span data-stu-id="7b598-189">False</span></span>                                        |
| <span data-ttu-id="7b598-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b598-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b598-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b598-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7b598-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b598-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7b598-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b598-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7b598-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-194">Search-Flags</span></span>           | <span data-ttu-id="7b598-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b598-195">0x00000000</span></span>                                   |
| <span data-ttu-id="7b598-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-196">System-Flags</span></span>           | <span data-ttu-id="7b598-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b598-197">0x00000010</span></span>                                   |
| <span data-ttu-id="7b598-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b598-198">Classes used in</span></span>        | [<span data-ttu-id="7b598-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7b598-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7b598-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b598-200">Windows Server 2008</span></span>



| <span data-ttu-id="7b598-201">進入</span><span class="sxs-lookup"><span data-stu-id="7b598-201">Entry</span></span> | <span data-ttu-id="7b598-202">值</span><span class="sxs-lookup"><span data-stu-id="7b598-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7b598-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b598-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b598-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b598-205">System-Only</span></span>            | <span data-ttu-id="7b598-206">否</span><span class="sxs-lookup"><span data-stu-id="7b598-206">False</span></span>                                        |
| <span data-ttu-id="7b598-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b598-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7b598-208">對</span><span class="sxs-lookup"><span data-stu-id="7b598-208">True</span></span>                                         |
| <span data-ttu-id="7b598-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b598-209">Is Indexed</span></span>             | <span data-ttu-id="7b598-210">否</span><span class="sxs-lookup"><span data-stu-id="7b598-210">False</span></span>                                        |
| <span data-ttu-id="7b598-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b598-211">In Global Catalog</span></span>      | <span data-ttu-id="7b598-212">否</span><span class="sxs-lookup"><span data-stu-id="7b598-212">False</span></span>                                        |
| <span data-ttu-id="7b598-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b598-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b598-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b598-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7b598-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b598-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7b598-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b598-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7b598-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-217">Search-Flags</span></span>           | <span data-ttu-id="7b598-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b598-218">0x00000000</span></span>                                   |
| <span data-ttu-id="7b598-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-219">System-Flags</span></span>           | <span data-ttu-id="7b598-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b598-220">0x00000010</span></span>                                   |
| <span data-ttu-id="7b598-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b598-221">Classes used in</span></span>        | [<span data-ttu-id="7b598-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7b598-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7b598-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b598-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7b598-224">進入</span><span class="sxs-lookup"><span data-stu-id="7b598-224">Entry</span></span> | <span data-ttu-id="7b598-225">值</span><span class="sxs-lookup"><span data-stu-id="7b598-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7b598-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b598-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b598-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b598-228">System-Only</span></span>            | <span data-ttu-id="7b598-229">否</span><span class="sxs-lookup"><span data-stu-id="7b598-229">False</span></span>                                        |
| <span data-ttu-id="7b598-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b598-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7b598-231">對</span><span class="sxs-lookup"><span data-stu-id="7b598-231">True</span></span>                                         |
| <span data-ttu-id="7b598-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b598-232">Is Indexed</span></span>             | <span data-ttu-id="7b598-233">否</span><span class="sxs-lookup"><span data-stu-id="7b598-233">False</span></span>                                        |
| <span data-ttu-id="7b598-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b598-234">In Global Catalog</span></span>      | <span data-ttu-id="7b598-235">否</span><span class="sxs-lookup"><span data-stu-id="7b598-235">False</span></span>                                        |
| <span data-ttu-id="7b598-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b598-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b598-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b598-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7b598-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b598-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7b598-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b598-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7b598-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-240">Search-Flags</span></span>           | <span data-ttu-id="7b598-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b598-241">0x00000000</span></span>                                   |
| <span data-ttu-id="7b598-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-242">System-Flags</span></span>           | <span data-ttu-id="7b598-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b598-243">0x00000010</span></span>                                   |
| <span data-ttu-id="7b598-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b598-244">Classes used in</span></span>        | [<span data-ttu-id="7b598-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7b598-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7b598-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b598-246">Windows Server 2012</span></span>



| <span data-ttu-id="7b598-247">進入</span><span class="sxs-lookup"><span data-stu-id="7b598-247">Entry</span></span> | <span data-ttu-id="7b598-248">值</span><span class="sxs-lookup"><span data-stu-id="7b598-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7b598-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b598-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b598-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7b598-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b598-251">System-Only</span></span>            | <span data-ttu-id="7b598-252">否</span><span class="sxs-lookup"><span data-stu-id="7b598-252">False</span></span>                                        |
| <span data-ttu-id="7b598-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b598-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7b598-254">對</span><span class="sxs-lookup"><span data-stu-id="7b598-254">True</span></span>                                         |
| <span data-ttu-id="7b598-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b598-255">Is Indexed</span></span>             | <span data-ttu-id="7b598-256">否</span><span class="sxs-lookup"><span data-stu-id="7b598-256">False</span></span>                                        |
| <span data-ttu-id="7b598-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b598-257">In Global Catalog</span></span>      | <span data-ttu-id="7b598-258">否</span><span class="sxs-lookup"><span data-stu-id="7b598-258">False</span></span>                                        |
| <span data-ttu-id="7b598-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b598-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b598-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b598-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7b598-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b598-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7b598-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b598-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7b598-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-263">Search-Flags</span></span>           | <span data-ttu-id="7b598-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b598-264">0x00000000</span></span>                                   |
| <span data-ttu-id="7b598-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b598-265">System-Flags</span></span>           | <span data-ttu-id="7b598-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b598-266">0x00000010</span></span>                                   |
| <span data-ttu-id="7b598-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b598-267">Classes used in</span></span>        | [<span data-ttu-id="7b598-268">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7b598-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






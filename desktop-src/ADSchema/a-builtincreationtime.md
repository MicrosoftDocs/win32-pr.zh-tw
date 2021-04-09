---
title: 內建-建立時間屬性
description: 內建的建立時間屬性是用來支援 Windows NT 4.0 網域的複寫。
ms.assetid: b3da9913-8c7b-481b-ae47-6b124544f1e2
ms.tgt_platform: multiple
keywords:
- 內建-建立時間屬性 AD 架構
- builtinCreationTime 屬性 AD 架構
topic_type:
- apiref
api_name:
- Builtin-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d5b6d37ee0242999afd47415cb067abe26e7fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845620"
---
# <a name="builtin-creation-time-attribute"></a><span data-ttu-id="e92b0-105">內建-建立時間屬性</span><span class="sxs-lookup"><span data-stu-id="e92b0-105">Builtin-Creation-Time attribute</span></span>

<span data-ttu-id="e92b0-106">內 **建的建立時間** 屬性是用來支援 Windows NT 4.0 網域的複寫。</span><span class="sxs-lookup"><span data-stu-id="e92b0-106">The **Builtin-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="e92b0-107">進入</span><span class="sxs-lookup"><span data-stu-id="e92b0-107">Entry</span></span> | <span data-ttu-id="e92b0-108">值</span><span class="sxs-lookup"><span data-stu-id="e92b0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e92b0-109">CN</span><span class="sxs-lookup"><span data-stu-id="e92b0-109">CN</span></span>                | <span data-ttu-id="e92b0-110">內建-建立時間</span><span class="sxs-lookup"><span data-stu-id="e92b0-110">Builtin-Creation-Time</span></span>                |
| <span data-ttu-id="e92b0-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e92b0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e92b0-112">builtinCreationTime</span><span class="sxs-lookup"><span data-stu-id="e92b0-112">builtinCreationTime</span></span>                  |
| <span data-ttu-id="e92b0-113">大小</span><span class="sxs-lookup"><span data-stu-id="e92b0-113">Size</span></span>              | <span data-ttu-id="e92b0-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="e92b0-114">8 bytes</span></span>                              |
| <span data-ttu-id="e92b0-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e92b0-115">Update Privilege</span></span>  | <span data-ttu-id="e92b0-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="e92b0-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="e92b0-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e92b0-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e92b0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e92b0-118">Attribute-Id</span></span>      | <span data-ttu-id="e92b0-119">1.2.840.113556.1.4.13</span><span class="sxs-lookup"><span data-stu-id="e92b0-119">1.2.840.113556.1.4.13</span></span>                |
| <span data-ttu-id="e92b0-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e92b0-120">System-Id-Guid</span></span>    | <span data-ttu-id="e92b0-121">bf96792f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e92b0-121">bf96792f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e92b0-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e92b0-122">Syntax</span></span>            | [<span data-ttu-id="e92b0-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="e92b0-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e92b0-124">實作</span><span class="sxs-lookup"><span data-stu-id="e92b0-124">Implementations</span></span>

-   [<span data-ttu-id="e92b0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e92b0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e92b0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e92b0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e92b0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e92b0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e92b0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e92b0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e92b0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e92b0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e92b0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e92b0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e92b0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e92b0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e92b0-132">進入</span><span class="sxs-lookup"><span data-stu-id="e92b0-132">Entry</span></span> | <span data-ttu-id="e92b0-133">值</span><span class="sxs-lookup"><span data-stu-id="e92b0-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e92b0-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e92b0-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e92b0-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e92b0-136">System-Only</span></span>            | <span data-ttu-id="e92b0-137">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-137">False</span></span>                                        |
| <span data-ttu-id="e92b0-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e92b0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e92b0-139">對</span><span class="sxs-lookup"><span data-stu-id="e92b0-139">True</span></span>                                         |
| <span data-ttu-id="e92b0-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e92b0-140">Is Indexed</span></span>             | <span data-ttu-id="e92b0-141">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-141">False</span></span>                                        |
| <span data-ttu-id="e92b0-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e92b0-142">In Global Catalog</span></span>      | <span data-ttu-id="e92b0-143">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-143">False</span></span>                                        |
| <span data-ttu-id="e92b0-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e92b0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e92b0-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e92b0-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e92b0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e92b0-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e92b0-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-148">Search-Flags</span></span>           | <span data-ttu-id="e92b0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e92b0-149">0x00000000</span></span>                                   |
| <span data-ttu-id="e92b0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-150">System-Flags</span></span>           | <span data-ttu-id="e92b0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e92b0-151">0x00000010</span></span>                                   |
| <span data-ttu-id="e92b0-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e92b0-152">Classes used in</span></span>        | [<span data-ttu-id="e92b0-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="e92b0-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e92b0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e92b0-154">Windows Server 2003</span></span>



| <span data-ttu-id="e92b0-155">進入</span><span class="sxs-lookup"><span data-stu-id="e92b0-155">Entry</span></span> | <span data-ttu-id="e92b0-156">值</span><span class="sxs-lookup"><span data-stu-id="e92b0-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e92b0-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e92b0-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e92b0-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e92b0-159">System-Only</span></span>            | <span data-ttu-id="e92b0-160">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-160">False</span></span>                                        |
| <span data-ttu-id="e92b0-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e92b0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e92b0-162">對</span><span class="sxs-lookup"><span data-stu-id="e92b0-162">True</span></span>                                         |
| <span data-ttu-id="e92b0-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e92b0-163">Is Indexed</span></span>             | <span data-ttu-id="e92b0-164">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-164">False</span></span>                                        |
| <span data-ttu-id="e92b0-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e92b0-165">In Global Catalog</span></span>      | <span data-ttu-id="e92b0-166">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-166">False</span></span>                                        |
| <span data-ttu-id="e92b0-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e92b0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e92b0-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e92b0-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e92b0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e92b0-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e92b0-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-171">Search-Flags</span></span>           | <span data-ttu-id="e92b0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e92b0-172">0x00000000</span></span>                                   |
| <span data-ttu-id="e92b0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-173">System-Flags</span></span>           | <span data-ttu-id="e92b0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e92b0-174">0x00000010</span></span>                                   |
| <span data-ttu-id="e92b0-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e92b0-175">Classes used in</span></span>        | [<span data-ttu-id="e92b0-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="e92b0-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e92b0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e92b0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e92b0-178">進入</span><span class="sxs-lookup"><span data-stu-id="e92b0-178">Entry</span></span> | <span data-ttu-id="e92b0-179">值</span><span class="sxs-lookup"><span data-stu-id="e92b0-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e92b0-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e92b0-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e92b0-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e92b0-182">System-Only</span></span>            | <span data-ttu-id="e92b0-183">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-183">False</span></span>                                        |
| <span data-ttu-id="e92b0-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e92b0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e92b0-185">對</span><span class="sxs-lookup"><span data-stu-id="e92b0-185">True</span></span>                                         |
| <span data-ttu-id="e92b0-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e92b0-186">Is Indexed</span></span>             | <span data-ttu-id="e92b0-187">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-187">False</span></span>                                        |
| <span data-ttu-id="e92b0-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e92b0-188">In Global Catalog</span></span>      | <span data-ttu-id="e92b0-189">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-189">False</span></span>                                        |
| <span data-ttu-id="e92b0-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e92b0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e92b0-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e92b0-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e92b0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e92b0-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e92b0-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-194">Search-Flags</span></span>           | <span data-ttu-id="e92b0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e92b0-195">0x00000000</span></span>                                   |
| <span data-ttu-id="e92b0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-196">System-Flags</span></span>           | <span data-ttu-id="e92b0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e92b0-197">0x00000010</span></span>                                   |
| <span data-ttu-id="e92b0-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e92b0-198">Classes used in</span></span>        | [<span data-ttu-id="e92b0-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="e92b0-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e92b0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e92b0-200">Windows Server 2008</span></span>



| <span data-ttu-id="e92b0-201">進入</span><span class="sxs-lookup"><span data-stu-id="e92b0-201">Entry</span></span> | <span data-ttu-id="e92b0-202">值</span><span class="sxs-lookup"><span data-stu-id="e92b0-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e92b0-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e92b0-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e92b0-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e92b0-205">System-Only</span></span>            | <span data-ttu-id="e92b0-206">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-206">False</span></span>                                        |
| <span data-ttu-id="e92b0-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e92b0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e92b0-208">對</span><span class="sxs-lookup"><span data-stu-id="e92b0-208">True</span></span>                                         |
| <span data-ttu-id="e92b0-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e92b0-209">Is Indexed</span></span>             | <span data-ttu-id="e92b0-210">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-210">False</span></span>                                        |
| <span data-ttu-id="e92b0-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e92b0-211">In Global Catalog</span></span>      | <span data-ttu-id="e92b0-212">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-212">False</span></span>                                        |
| <span data-ttu-id="e92b0-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e92b0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e92b0-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e92b0-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e92b0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e92b0-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e92b0-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-217">Search-Flags</span></span>           | <span data-ttu-id="e92b0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e92b0-218">0x00000000</span></span>                                   |
| <span data-ttu-id="e92b0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-219">System-Flags</span></span>           | <span data-ttu-id="e92b0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e92b0-220">0x00000010</span></span>                                   |
| <span data-ttu-id="e92b0-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e92b0-221">Classes used in</span></span>        | [<span data-ttu-id="e92b0-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="e92b0-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e92b0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e92b0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e92b0-224">進入</span><span class="sxs-lookup"><span data-stu-id="e92b0-224">Entry</span></span> | <span data-ttu-id="e92b0-225">值</span><span class="sxs-lookup"><span data-stu-id="e92b0-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e92b0-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e92b0-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e92b0-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e92b0-228">System-Only</span></span>            | <span data-ttu-id="e92b0-229">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-229">False</span></span>                                        |
| <span data-ttu-id="e92b0-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e92b0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e92b0-231">對</span><span class="sxs-lookup"><span data-stu-id="e92b0-231">True</span></span>                                         |
| <span data-ttu-id="e92b0-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e92b0-232">Is Indexed</span></span>             | <span data-ttu-id="e92b0-233">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-233">False</span></span>                                        |
| <span data-ttu-id="e92b0-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e92b0-234">In Global Catalog</span></span>      | <span data-ttu-id="e92b0-235">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-235">False</span></span>                                        |
| <span data-ttu-id="e92b0-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e92b0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e92b0-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e92b0-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e92b0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e92b0-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e92b0-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-240">Search-Flags</span></span>           | <span data-ttu-id="e92b0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e92b0-241">0x00000000</span></span>                                   |
| <span data-ttu-id="e92b0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-242">System-Flags</span></span>           | <span data-ttu-id="e92b0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e92b0-243">0x00000010</span></span>                                   |
| <span data-ttu-id="e92b0-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e92b0-244">Classes used in</span></span>        | [<span data-ttu-id="e92b0-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="e92b0-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e92b0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e92b0-246">Windows Server 2012</span></span>



| <span data-ttu-id="e92b0-247">進入</span><span class="sxs-lookup"><span data-stu-id="e92b0-247">Entry</span></span> | <span data-ttu-id="e92b0-248">值</span><span class="sxs-lookup"><span data-stu-id="e92b0-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e92b0-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e92b0-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e92b0-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e92b0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e92b0-251">System-Only</span></span>            | <span data-ttu-id="e92b0-252">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-252">False</span></span>                                        |
| <span data-ttu-id="e92b0-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e92b0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e92b0-254">對</span><span class="sxs-lookup"><span data-stu-id="e92b0-254">True</span></span>                                         |
| <span data-ttu-id="e92b0-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e92b0-255">Is Indexed</span></span>             | <span data-ttu-id="e92b0-256">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-256">False</span></span>                                        |
| <span data-ttu-id="e92b0-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e92b0-257">In Global Catalog</span></span>      | <span data-ttu-id="e92b0-258">否</span><span class="sxs-lookup"><span data-stu-id="e92b0-258">False</span></span>                                        |
| <span data-ttu-id="e92b0-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e92b0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e92b0-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e92b0-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e92b0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e92b0-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e92b0-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e92b0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-263">Search-Flags</span></span>           | <span data-ttu-id="e92b0-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e92b0-264">0x00000000</span></span>                                   |
| <span data-ttu-id="e92b0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e92b0-265">System-Flags</span></span>           | <span data-ttu-id="e92b0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e92b0-266">0x00000010</span></span>                                   |
| <span data-ttu-id="e92b0-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e92b0-267">Classes used in</span></span>        | [<span data-ttu-id="e92b0-268">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="e92b0-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






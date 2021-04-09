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
# <a name="builtin-creation-time-attribute"></a><span data-ttu-id="b8e86-105">內建-建立時間屬性</span><span class="sxs-lookup"><span data-stu-id="b8e86-105">Builtin-Creation-Time attribute</span></span>

<span data-ttu-id="b8e86-106">內 **建的建立時間** 屬性是用來支援 Windows NT 4.0 網域的複寫。</span><span class="sxs-lookup"><span data-stu-id="b8e86-106">The **Builtin-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="b8e86-107">進入</span><span class="sxs-lookup"><span data-stu-id="b8e86-107">Entry</span></span> | <span data-ttu-id="b8e86-108">值</span><span class="sxs-lookup"><span data-stu-id="b8e86-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b8e86-109">CN</span><span class="sxs-lookup"><span data-stu-id="b8e86-109">CN</span></span>                | <span data-ttu-id="b8e86-110">內建-建立時間</span><span class="sxs-lookup"><span data-stu-id="b8e86-110">Builtin-Creation-Time</span></span>                |
| <span data-ttu-id="b8e86-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b8e86-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b8e86-112">builtinCreationTime</span><span class="sxs-lookup"><span data-stu-id="b8e86-112">builtinCreationTime</span></span>                  |
| <span data-ttu-id="b8e86-113">大小</span><span class="sxs-lookup"><span data-stu-id="b8e86-113">Size</span></span>              | <span data-ttu-id="b8e86-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="b8e86-114">8 bytes</span></span>                              |
| <span data-ttu-id="b8e86-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b8e86-115">Update Privilege</span></span>  | <span data-ttu-id="b8e86-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="b8e86-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="b8e86-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b8e86-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b8e86-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8e86-118">Attribute-Id</span></span>      | <span data-ttu-id="b8e86-119">1.2.840.113556.1.4.13</span><span class="sxs-lookup"><span data-stu-id="b8e86-119">1.2.840.113556.1.4.13</span></span>                |
| <span data-ttu-id="b8e86-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b8e86-120">System-Id-Guid</span></span>    | <span data-ttu-id="b8e86-121">bf96792f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b8e86-121">bf96792f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b8e86-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8e86-122">Syntax</span></span>            | [<span data-ttu-id="b8e86-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="b8e86-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b8e86-124">實作</span><span class="sxs-lookup"><span data-stu-id="b8e86-124">Implementations</span></span>

-   [<span data-ttu-id="b8e86-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8e86-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8e86-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8e86-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8e86-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8e86-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8e86-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8e86-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8e86-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8e86-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8e86-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8e86-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8e86-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8e86-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b8e86-132">進入</span><span class="sxs-lookup"><span data-stu-id="b8e86-132">Entry</span></span> | <span data-ttu-id="b8e86-133">值</span><span class="sxs-lookup"><span data-stu-id="b8e86-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b8e86-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8e86-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8e86-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8e86-136">System-Only</span></span>            | <span data-ttu-id="b8e86-137">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-137">False</span></span>                                        |
| <span data-ttu-id="b8e86-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8e86-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b8e86-139">對</span><span class="sxs-lookup"><span data-stu-id="b8e86-139">True</span></span>                                         |
| <span data-ttu-id="b8e86-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8e86-140">Is Indexed</span></span>             | <span data-ttu-id="b8e86-141">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-141">False</span></span>                                        |
| <span data-ttu-id="b8e86-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8e86-142">In Global Catalog</span></span>      | <span data-ttu-id="b8e86-143">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-143">False</span></span>                                        |
| <span data-ttu-id="b8e86-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8e86-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8e86-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8e86-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b8e86-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8e86-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8e86-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-148">Search-Flags</span></span>           | <span data-ttu-id="b8e86-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8e86-149">0x00000000</span></span>                                   |
| <span data-ttu-id="b8e86-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-150">System-Flags</span></span>           | <span data-ttu-id="b8e86-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8e86-151">0x00000010</span></span>                                   |
| <span data-ttu-id="b8e86-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8e86-152">Classes used in</span></span>        | [<span data-ttu-id="b8e86-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b8e86-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8e86-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8e86-154">Windows Server 2003</span></span>



| <span data-ttu-id="b8e86-155">進入</span><span class="sxs-lookup"><span data-stu-id="b8e86-155">Entry</span></span> | <span data-ttu-id="b8e86-156">值</span><span class="sxs-lookup"><span data-stu-id="b8e86-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b8e86-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8e86-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8e86-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8e86-159">System-Only</span></span>            | <span data-ttu-id="b8e86-160">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-160">False</span></span>                                        |
| <span data-ttu-id="b8e86-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8e86-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b8e86-162">對</span><span class="sxs-lookup"><span data-stu-id="b8e86-162">True</span></span>                                         |
| <span data-ttu-id="b8e86-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8e86-163">Is Indexed</span></span>             | <span data-ttu-id="b8e86-164">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-164">False</span></span>                                        |
| <span data-ttu-id="b8e86-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8e86-165">In Global Catalog</span></span>      | <span data-ttu-id="b8e86-166">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-166">False</span></span>                                        |
| <span data-ttu-id="b8e86-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8e86-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8e86-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8e86-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b8e86-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8e86-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8e86-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-171">Search-Flags</span></span>           | <span data-ttu-id="b8e86-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8e86-172">0x00000000</span></span>                                   |
| <span data-ttu-id="b8e86-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-173">System-Flags</span></span>           | <span data-ttu-id="b8e86-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8e86-174">0x00000010</span></span>                                   |
| <span data-ttu-id="b8e86-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8e86-175">Classes used in</span></span>        | [<span data-ttu-id="b8e86-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b8e86-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8e86-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8e86-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8e86-178">進入</span><span class="sxs-lookup"><span data-stu-id="b8e86-178">Entry</span></span> | <span data-ttu-id="b8e86-179">值</span><span class="sxs-lookup"><span data-stu-id="b8e86-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b8e86-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8e86-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8e86-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8e86-182">System-Only</span></span>            | <span data-ttu-id="b8e86-183">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-183">False</span></span>                                        |
| <span data-ttu-id="b8e86-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8e86-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b8e86-185">對</span><span class="sxs-lookup"><span data-stu-id="b8e86-185">True</span></span>                                         |
| <span data-ttu-id="b8e86-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8e86-186">Is Indexed</span></span>             | <span data-ttu-id="b8e86-187">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-187">False</span></span>                                        |
| <span data-ttu-id="b8e86-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8e86-188">In Global Catalog</span></span>      | <span data-ttu-id="b8e86-189">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-189">False</span></span>                                        |
| <span data-ttu-id="b8e86-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8e86-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8e86-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8e86-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b8e86-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8e86-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8e86-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-194">Search-Flags</span></span>           | <span data-ttu-id="b8e86-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8e86-195">0x00000000</span></span>                                   |
| <span data-ttu-id="b8e86-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-196">System-Flags</span></span>           | <span data-ttu-id="b8e86-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8e86-197">0x00000010</span></span>                                   |
| <span data-ttu-id="b8e86-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8e86-198">Classes used in</span></span>        | [<span data-ttu-id="b8e86-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b8e86-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8e86-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8e86-200">Windows Server 2008</span></span>



| <span data-ttu-id="b8e86-201">進入</span><span class="sxs-lookup"><span data-stu-id="b8e86-201">Entry</span></span> | <span data-ttu-id="b8e86-202">值</span><span class="sxs-lookup"><span data-stu-id="b8e86-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b8e86-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8e86-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8e86-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8e86-205">System-Only</span></span>            | <span data-ttu-id="b8e86-206">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-206">False</span></span>                                        |
| <span data-ttu-id="b8e86-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8e86-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b8e86-208">對</span><span class="sxs-lookup"><span data-stu-id="b8e86-208">True</span></span>                                         |
| <span data-ttu-id="b8e86-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8e86-209">Is Indexed</span></span>             | <span data-ttu-id="b8e86-210">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-210">False</span></span>                                        |
| <span data-ttu-id="b8e86-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8e86-211">In Global Catalog</span></span>      | <span data-ttu-id="b8e86-212">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-212">False</span></span>                                        |
| <span data-ttu-id="b8e86-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8e86-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8e86-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8e86-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b8e86-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8e86-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8e86-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-217">Search-Flags</span></span>           | <span data-ttu-id="b8e86-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8e86-218">0x00000000</span></span>                                   |
| <span data-ttu-id="b8e86-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-219">System-Flags</span></span>           | <span data-ttu-id="b8e86-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8e86-220">0x00000010</span></span>                                   |
| <span data-ttu-id="b8e86-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8e86-221">Classes used in</span></span>        | [<span data-ttu-id="b8e86-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b8e86-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8e86-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8e86-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8e86-224">進入</span><span class="sxs-lookup"><span data-stu-id="b8e86-224">Entry</span></span> | <span data-ttu-id="b8e86-225">值</span><span class="sxs-lookup"><span data-stu-id="b8e86-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b8e86-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8e86-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8e86-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8e86-228">System-Only</span></span>            | <span data-ttu-id="b8e86-229">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-229">False</span></span>                                        |
| <span data-ttu-id="b8e86-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8e86-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b8e86-231">對</span><span class="sxs-lookup"><span data-stu-id="b8e86-231">True</span></span>                                         |
| <span data-ttu-id="b8e86-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8e86-232">Is Indexed</span></span>             | <span data-ttu-id="b8e86-233">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-233">False</span></span>                                        |
| <span data-ttu-id="b8e86-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8e86-234">In Global Catalog</span></span>      | <span data-ttu-id="b8e86-235">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-235">False</span></span>                                        |
| <span data-ttu-id="b8e86-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8e86-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8e86-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8e86-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b8e86-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8e86-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8e86-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-240">Search-Flags</span></span>           | <span data-ttu-id="b8e86-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8e86-241">0x00000000</span></span>                                   |
| <span data-ttu-id="b8e86-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-242">System-Flags</span></span>           | <span data-ttu-id="b8e86-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8e86-243">0x00000010</span></span>                                   |
| <span data-ttu-id="b8e86-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8e86-244">Classes used in</span></span>        | [<span data-ttu-id="b8e86-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b8e86-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8e86-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8e86-246">Windows Server 2012</span></span>



| <span data-ttu-id="b8e86-247">進入</span><span class="sxs-lookup"><span data-stu-id="b8e86-247">Entry</span></span> | <span data-ttu-id="b8e86-248">值</span><span class="sxs-lookup"><span data-stu-id="b8e86-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b8e86-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8e86-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8e86-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b8e86-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8e86-251">System-Only</span></span>            | <span data-ttu-id="b8e86-252">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-252">False</span></span>                                        |
| <span data-ttu-id="b8e86-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8e86-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b8e86-254">對</span><span class="sxs-lookup"><span data-stu-id="b8e86-254">True</span></span>                                         |
| <span data-ttu-id="b8e86-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8e86-255">Is Indexed</span></span>             | <span data-ttu-id="b8e86-256">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-256">False</span></span>                                        |
| <span data-ttu-id="b8e86-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8e86-257">In Global Catalog</span></span>      | <span data-ttu-id="b8e86-258">否</span><span class="sxs-lookup"><span data-stu-id="b8e86-258">False</span></span>                                        |
| <span data-ttu-id="b8e86-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8e86-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8e86-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8e86-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b8e86-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8e86-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8e86-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b8e86-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-263">Search-Flags</span></span>           | <span data-ttu-id="b8e86-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8e86-264">0x00000000</span></span>                                   |
| <span data-ttu-id="b8e86-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8e86-265">System-Flags</span></span>           | <span data-ttu-id="b8e86-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8e86-266">0x00000010</span></span>                                   |
| <span data-ttu-id="b8e86-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8e86-267">Classes used in</span></span>        | [<span data-ttu-id="b8e86-268">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b8e86-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






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
# <a name="builtin-creation-time-attribute"></a><span data-ttu-id="13b8f-105">內建-建立時間屬性</span><span class="sxs-lookup"><span data-stu-id="13b8f-105">Builtin-Creation-Time attribute</span></span>

<span data-ttu-id="13b8f-106">內 **建的建立時間** 屬性是用來支援 Windows NT 4.0 網域的複寫。</span><span class="sxs-lookup"><span data-stu-id="13b8f-106">The **Builtin-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="13b8f-107">進入</span><span class="sxs-lookup"><span data-stu-id="13b8f-107">Entry</span></span> | <span data-ttu-id="13b8f-108">值</span><span class="sxs-lookup"><span data-stu-id="13b8f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="13b8f-109">CN</span><span class="sxs-lookup"><span data-stu-id="13b8f-109">CN</span></span>                | <span data-ttu-id="13b8f-110">內建-建立時間</span><span class="sxs-lookup"><span data-stu-id="13b8f-110">Builtin-Creation-Time</span></span>                |
| <span data-ttu-id="13b8f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="13b8f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="13b8f-112">builtinCreationTime</span><span class="sxs-lookup"><span data-stu-id="13b8f-112">builtinCreationTime</span></span>                  |
| <span data-ttu-id="13b8f-113">大小</span><span class="sxs-lookup"><span data-stu-id="13b8f-113">Size</span></span>              | <span data-ttu-id="13b8f-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="13b8f-114">8 bytes</span></span>                              |
| <span data-ttu-id="13b8f-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="13b8f-115">Update Privilege</span></span>  | <span data-ttu-id="13b8f-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="13b8f-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="13b8f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="13b8f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="13b8f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13b8f-118">Attribute-Id</span></span>      | <span data-ttu-id="13b8f-119">1.2.840.113556.1.4.13</span><span class="sxs-lookup"><span data-stu-id="13b8f-119">1.2.840.113556.1.4.13</span></span>                |
| <span data-ttu-id="13b8f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="13b8f-120">System-Id-Guid</span></span>    | <span data-ttu-id="13b8f-121">bf96792f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="13b8f-121">bf96792f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="13b8f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="13b8f-122">Syntax</span></span>            | [<span data-ttu-id="13b8f-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="13b8f-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="13b8f-124">實作</span><span class="sxs-lookup"><span data-stu-id="13b8f-124">Implementations</span></span>

-   [<span data-ttu-id="13b8f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="13b8f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="13b8f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="13b8f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="13b8f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="13b8f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="13b8f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13b8f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13b8f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13b8f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13b8f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13b8f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="13b8f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13b8f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="13b8f-132">進入</span><span class="sxs-lookup"><span data-stu-id="13b8f-132">Entry</span></span> | <span data-ttu-id="13b8f-133">值</span><span class="sxs-lookup"><span data-stu-id="13b8f-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13b8f-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13b8f-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13b8f-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="13b8f-136">System-Only</span></span>            | <span data-ttu-id="13b8f-137">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-137">False</span></span>                                        |
| <span data-ttu-id="13b8f-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13b8f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="13b8f-139">對</span><span class="sxs-lookup"><span data-stu-id="13b8f-139">True</span></span>                                         |
| <span data-ttu-id="13b8f-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13b8f-140">Is Indexed</span></span>             | <span data-ttu-id="13b8f-141">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-141">False</span></span>                                        |
| <span data-ttu-id="13b8f-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13b8f-142">In Global Catalog</span></span>      | <span data-ttu-id="13b8f-143">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-143">False</span></span>                                        |
| <span data-ttu-id="13b8f-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13b8f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="13b8f-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13b8f-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13b8f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13b8f-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13b8f-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-148">Search-Flags</span></span>           | <span data-ttu-id="13b8f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13b8f-149">0x00000000</span></span>                                   |
| <span data-ttu-id="13b8f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-150">System-Flags</span></span>           | <span data-ttu-id="13b8f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13b8f-151">0x00000010</span></span>                                   |
| <span data-ttu-id="13b8f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13b8f-152">Classes used in</span></span>        | [<span data-ttu-id="13b8f-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="13b8f-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="13b8f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13b8f-154">Windows Server 2003</span></span>



| <span data-ttu-id="13b8f-155">進入</span><span class="sxs-lookup"><span data-stu-id="13b8f-155">Entry</span></span> | <span data-ttu-id="13b8f-156">值</span><span class="sxs-lookup"><span data-stu-id="13b8f-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13b8f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13b8f-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13b8f-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="13b8f-159">System-Only</span></span>            | <span data-ttu-id="13b8f-160">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-160">False</span></span>                                        |
| <span data-ttu-id="13b8f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13b8f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="13b8f-162">對</span><span class="sxs-lookup"><span data-stu-id="13b8f-162">True</span></span>                                         |
| <span data-ttu-id="13b8f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13b8f-163">Is Indexed</span></span>             | <span data-ttu-id="13b8f-164">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-164">False</span></span>                                        |
| <span data-ttu-id="13b8f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13b8f-165">In Global Catalog</span></span>      | <span data-ttu-id="13b8f-166">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-166">False</span></span>                                        |
| <span data-ttu-id="13b8f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13b8f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="13b8f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13b8f-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13b8f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13b8f-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13b8f-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-171">Search-Flags</span></span>           | <span data-ttu-id="13b8f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13b8f-172">0x00000000</span></span>                                   |
| <span data-ttu-id="13b8f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-173">System-Flags</span></span>           | <span data-ttu-id="13b8f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13b8f-174">0x00000010</span></span>                                   |
| <span data-ttu-id="13b8f-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13b8f-175">Classes used in</span></span>        | [<span data-ttu-id="13b8f-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="13b8f-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="13b8f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="13b8f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="13b8f-178">進入</span><span class="sxs-lookup"><span data-stu-id="13b8f-178">Entry</span></span> | <span data-ttu-id="13b8f-179">值</span><span class="sxs-lookup"><span data-stu-id="13b8f-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13b8f-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13b8f-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13b8f-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="13b8f-182">System-Only</span></span>            | <span data-ttu-id="13b8f-183">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-183">False</span></span>                                        |
| <span data-ttu-id="13b8f-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13b8f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="13b8f-185">對</span><span class="sxs-lookup"><span data-stu-id="13b8f-185">True</span></span>                                         |
| <span data-ttu-id="13b8f-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13b8f-186">Is Indexed</span></span>             | <span data-ttu-id="13b8f-187">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-187">False</span></span>                                        |
| <span data-ttu-id="13b8f-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13b8f-188">In Global Catalog</span></span>      | <span data-ttu-id="13b8f-189">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-189">False</span></span>                                        |
| <span data-ttu-id="13b8f-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13b8f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="13b8f-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13b8f-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13b8f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13b8f-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13b8f-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-194">Search-Flags</span></span>           | <span data-ttu-id="13b8f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13b8f-195">0x00000000</span></span>                                   |
| <span data-ttu-id="13b8f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-196">System-Flags</span></span>           | <span data-ttu-id="13b8f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13b8f-197">0x00000010</span></span>                                   |
| <span data-ttu-id="13b8f-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13b8f-198">Classes used in</span></span>        | [<span data-ttu-id="13b8f-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="13b8f-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="13b8f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13b8f-200">Windows Server 2008</span></span>



| <span data-ttu-id="13b8f-201">進入</span><span class="sxs-lookup"><span data-stu-id="13b8f-201">Entry</span></span> | <span data-ttu-id="13b8f-202">值</span><span class="sxs-lookup"><span data-stu-id="13b8f-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13b8f-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13b8f-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13b8f-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="13b8f-205">System-Only</span></span>            | <span data-ttu-id="13b8f-206">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-206">False</span></span>                                        |
| <span data-ttu-id="13b8f-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13b8f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="13b8f-208">對</span><span class="sxs-lookup"><span data-stu-id="13b8f-208">True</span></span>                                         |
| <span data-ttu-id="13b8f-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13b8f-209">Is Indexed</span></span>             | <span data-ttu-id="13b8f-210">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-210">False</span></span>                                        |
| <span data-ttu-id="13b8f-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13b8f-211">In Global Catalog</span></span>      | <span data-ttu-id="13b8f-212">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-212">False</span></span>                                        |
| <span data-ttu-id="13b8f-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13b8f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="13b8f-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13b8f-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13b8f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13b8f-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13b8f-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-217">Search-Flags</span></span>           | <span data-ttu-id="13b8f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13b8f-218">0x00000000</span></span>                                   |
| <span data-ttu-id="13b8f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-219">System-Flags</span></span>           | <span data-ttu-id="13b8f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13b8f-220">0x00000010</span></span>                                   |
| <span data-ttu-id="13b8f-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13b8f-221">Classes used in</span></span>        | [<span data-ttu-id="13b8f-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="13b8f-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13b8f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13b8f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13b8f-224">進入</span><span class="sxs-lookup"><span data-stu-id="13b8f-224">Entry</span></span> | <span data-ttu-id="13b8f-225">值</span><span class="sxs-lookup"><span data-stu-id="13b8f-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13b8f-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13b8f-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13b8f-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="13b8f-228">System-Only</span></span>            | <span data-ttu-id="13b8f-229">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-229">False</span></span>                                        |
| <span data-ttu-id="13b8f-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13b8f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="13b8f-231">對</span><span class="sxs-lookup"><span data-stu-id="13b8f-231">True</span></span>                                         |
| <span data-ttu-id="13b8f-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13b8f-232">Is Indexed</span></span>             | <span data-ttu-id="13b8f-233">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-233">False</span></span>                                        |
| <span data-ttu-id="13b8f-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13b8f-234">In Global Catalog</span></span>      | <span data-ttu-id="13b8f-235">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-235">False</span></span>                                        |
| <span data-ttu-id="13b8f-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13b8f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="13b8f-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13b8f-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13b8f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13b8f-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13b8f-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-240">Search-Flags</span></span>           | <span data-ttu-id="13b8f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13b8f-241">0x00000000</span></span>                                   |
| <span data-ttu-id="13b8f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-242">System-Flags</span></span>           | <span data-ttu-id="13b8f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13b8f-243">0x00000010</span></span>                                   |
| <span data-ttu-id="13b8f-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13b8f-244">Classes used in</span></span>        | [<span data-ttu-id="13b8f-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="13b8f-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13b8f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13b8f-246">Windows Server 2012</span></span>



| <span data-ttu-id="13b8f-247">進入</span><span class="sxs-lookup"><span data-stu-id="13b8f-247">Entry</span></span> | <span data-ttu-id="13b8f-248">值</span><span class="sxs-lookup"><span data-stu-id="13b8f-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13b8f-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13b8f-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13b8f-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13b8f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="13b8f-251">System-Only</span></span>            | <span data-ttu-id="13b8f-252">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-252">False</span></span>                                        |
| <span data-ttu-id="13b8f-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13b8f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="13b8f-254">對</span><span class="sxs-lookup"><span data-stu-id="13b8f-254">True</span></span>                                         |
| <span data-ttu-id="13b8f-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13b8f-255">Is Indexed</span></span>             | <span data-ttu-id="13b8f-256">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-256">False</span></span>                                        |
| <span data-ttu-id="13b8f-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13b8f-257">In Global Catalog</span></span>      | <span data-ttu-id="13b8f-258">否</span><span class="sxs-lookup"><span data-stu-id="13b8f-258">False</span></span>                                        |
| <span data-ttu-id="13b8f-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13b8f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="13b8f-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13b8f-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13b8f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13b8f-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13b8f-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13b8f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-263">Search-Flags</span></span>           | <span data-ttu-id="13b8f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13b8f-264">0x00000000</span></span>                                   |
| <span data-ttu-id="13b8f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13b8f-265">System-Flags</span></span>           | <span data-ttu-id="13b8f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13b8f-266">0x00000010</span></span>                                   |
| <span data-ttu-id="13b8f-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13b8f-267">Classes used in</span></span>        | [<span data-ttu-id="13b8f-268">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="13b8f-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






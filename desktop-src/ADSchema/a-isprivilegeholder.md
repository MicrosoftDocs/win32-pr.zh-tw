---
title: 是-許可權-持有者屬性
description: 指定主體所持有之許可權的反向連結。
ms.assetid: 94355fbc-f7d8-460b-a516-1576629ca63e
ms.tgt_platform: multiple
keywords:
- 是-許可權-持有者屬性 AD 架構
- isPrivilegeHolder 屬性 AD 架構
topic_type:
- apiref
api_name:
- Is-Privilege-Holder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895a0202f6ca51ffe7982f33c1fc9f02d021d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973922"
---
# <a name="is-privilege-holder-attribute"></a><span data-ttu-id="c2023-105">是-許可權-持有者屬性</span><span class="sxs-lookup"><span data-stu-id="c2023-105">Is-Privilege-Holder attribute</span></span>

<span data-ttu-id="c2023-106">指定主體所持有之許可權的反向連結。</span><span class="sxs-lookup"><span data-stu-id="c2023-106">Backward link to privileges held by a given principal.</span></span>



| <span data-ttu-id="c2023-107">進入</span><span class="sxs-lookup"><span data-stu-id="c2023-107">Entry</span></span> | <span data-ttu-id="c2023-108">值</span><span class="sxs-lookup"><span data-stu-id="c2023-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c2023-109">CN</span><span class="sxs-lookup"><span data-stu-id="c2023-109">CN</span></span>                | <span data-ttu-id="c2023-110">是-許可權-持有者</span><span class="sxs-lookup"><span data-stu-id="c2023-110">Is-Privilege-Holder</span></span>                     |
| <span data-ttu-id="c2023-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c2023-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c2023-112">isPrivilegeHolder</span><span class="sxs-lookup"><span data-stu-id="c2023-112">isPrivilegeHolder</span></span>                       |
| <span data-ttu-id="c2023-113">大小</span><span class="sxs-lookup"><span data-stu-id="c2023-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c2023-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c2023-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c2023-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c2023-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c2023-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c2023-116">Attribute-Id</span></span>      | <span data-ttu-id="c2023-117">1.2.840.113556.1.4.638</span><span class="sxs-lookup"><span data-stu-id="c2023-117">1.2.840.113556.1.4.638</span></span>                  |
| <span data-ttu-id="c2023-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c2023-118">System-Id-Guid</span></span>    | <span data-ttu-id="c2023-119">19405b9c-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c2023-119">19405b9c-3cfa-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="c2023-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2023-120">Syntax</span></span>            | [<span data-ttu-id="c2023-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c2023-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c2023-122">實作</span><span class="sxs-lookup"><span data-stu-id="c2023-122">Implementations</span></span>

-   [<span data-ttu-id="c2023-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c2023-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c2023-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c2023-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c2023-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c2023-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c2023-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c2023-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c2023-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c2023-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c2023-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c2023-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c2023-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2023-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c2023-130">進入</span><span class="sxs-lookup"><span data-stu-id="c2023-130">Entry</span></span> | <span data-ttu-id="c2023-131">值</span><span class="sxs-lookup"><span data-stu-id="c2023-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2023-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2023-132">Link-Id</span></span>                | <span data-ttu-id="c2023-133">71</span><span class="sxs-lookup"><span data-stu-id="c2023-133">71</span></span>                              |
| <span data-ttu-id="c2023-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2023-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2023-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2023-135">System-Only</span></span>            | <span data-ttu-id="c2023-136">對</span><span class="sxs-lookup"><span data-stu-id="c2023-136">True</span></span>                            |
| <span data-ttu-id="c2023-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2023-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c2023-138">否</span><span class="sxs-lookup"><span data-stu-id="c2023-138">False</span></span>                           |
| <span data-ttu-id="c2023-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2023-139">Is Indexed</span></span>             | <span data-ttu-id="c2023-140">否</span><span class="sxs-lookup"><span data-stu-id="c2023-140">False</span></span>                           |
| <span data-ttu-id="c2023-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2023-141">In Global Catalog</span></span>      | <span data-ttu-id="c2023-142">否</span><span class="sxs-lookup"><span data-stu-id="c2023-142">False</span></span>                           |
| <span data-ttu-id="c2023-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2023-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2023-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2023-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2023-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2023-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2023-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2023-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2023-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-147">Search-Flags</span></span>           | <span data-ttu-id="c2023-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2023-148">0x00000000</span></span>                      |
| <span data-ttu-id="c2023-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-149">System-Flags</span></span>           | <span data-ttu-id="c2023-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2023-150">0x00000010</span></span>                      |
| <span data-ttu-id="c2023-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2023-151">Classes used in</span></span>        | [<span data-ttu-id="c2023-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c2023-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c2023-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2023-153">Windows Server 2003</span></span>



| <span data-ttu-id="c2023-154">進入</span><span class="sxs-lookup"><span data-stu-id="c2023-154">Entry</span></span> | <span data-ttu-id="c2023-155">值</span><span class="sxs-lookup"><span data-stu-id="c2023-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2023-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2023-156">Link-Id</span></span>                | <span data-ttu-id="c2023-157">71</span><span class="sxs-lookup"><span data-stu-id="c2023-157">71</span></span>                              |
| <span data-ttu-id="c2023-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2023-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2023-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2023-159">System-Only</span></span>            | <span data-ttu-id="c2023-160">對</span><span class="sxs-lookup"><span data-stu-id="c2023-160">True</span></span>                            |
| <span data-ttu-id="c2023-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2023-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c2023-162">否</span><span class="sxs-lookup"><span data-stu-id="c2023-162">False</span></span>                           |
| <span data-ttu-id="c2023-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2023-163">Is Indexed</span></span>             | <span data-ttu-id="c2023-164">否</span><span class="sxs-lookup"><span data-stu-id="c2023-164">False</span></span>                           |
| <span data-ttu-id="c2023-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2023-165">In Global Catalog</span></span>      | <span data-ttu-id="c2023-166">否</span><span class="sxs-lookup"><span data-stu-id="c2023-166">False</span></span>                           |
| <span data-ttu-id="c2023-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2023-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2023-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2023-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2023-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2023-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2023-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2023-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2023-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-171">Search-Flags</span></span>           | <span data-ttu-id="c2023-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2023-172">0x00000000</span></span>                      |
| <span data-ttu-id="c2023-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-173">System-Flags</span></span>           | <span data-ttu-id="c2023-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2023-174">0x00000010</span></span>                      |
| <span data-ttu-id="c2023-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2023-175">Classes used in</span></span>        | [<span data-ttu-id="c2023-176">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c2023-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c2023-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c2023-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c2023-178">進入</span><span class="sxs-lookup"><span data-stu-id="c2023-178">Entry</span></span> | <span data-ttu-id="c2023-179">值</span><span class="sxs-lookup"><span data-stu-id="c2023-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2023-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2023-180">Link-Id</span></span>                | <span data-ttu-id="c2023-181">71</span><span class="sxs-lookup"><span data-stu-id="c2023-181">71</span></span>                              |
| <span data-ttu-id="c2023-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2023-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2023-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2023-183">System-Only</span></span>            | <span data-ttu-id="c2023-184">對</span><span class="sxs-lookup"><span data-stu-id="c2023-184">True</span></span>                            |
| <span data-ttu-id="c2023-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2023-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c2023-186">否</span><span class="sxs-lookup"><span data-stu-id="c2023-186">False</span></span>                           |
| <span data-ttu-id="c2023-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2023-187">Is Indexed</span></span>             | <span data-ttu-id="c2023-188">否</span><span class="sxs-lookup"><span data-stu-id="c2023-188">False</span></span>                           |
| <span data-ttu-id="c2023-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2023-189">In Global Catalog</span></span>      | <span data-ttu-id="c2023-190">否</span><span class="sxs-lookup"><span data-stu-id="c2023-190">False</span></span>                           |
| <span data-ttu-id="c2023-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2023-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2023-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2023-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2023-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2023-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2023-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2023-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2023-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-195">Search-Flags</span></span>           | <span data-ttu-id="c2023-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2023-196">0x00000000</span></span>                      |
| <span data-ttu-id="c2023-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-197">System-Flags</span></span>           | <span data-ttu-id="c2023-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2023-198">0x00000010</span></span>                      |
| <span data-ttu-id="c2023-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2023-199">Classes used in</span></span>        | [<span data-ttu-id="c2023-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c2023-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c2023-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2023-201">Windows Server 2008</span></span>



| <span data-ttu-id="c2023-202">進入</span><span class="sxs-lookup"><span data-stu-id="c2023-202">Entry</span></span> | <span data-ttu-id="c2023-203">值</span><span class="sxs-lookup"><span data-stu-id="c2023-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2023-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2023-204">Link-Id</span></span>                | <span data-ttu-id="c2023-205">71</span><span class="sxs-lookup"><span data-stu-id="c2023-205">71</span></span>                              |
| <span data-ttu-id="c2023-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2023-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2023-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2023-207">System-Only</span></span>            | <span data-ttu-id="c2023-208">對</span><span class="sxs-lookup"><span data-stu-id="c2023-208">True</span></span>                            |
| <span data-ttu-id="c2023-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2023-209">Is-Single-Valued</span></span>       | <span data-ttu-id="c2023-210">否</span><span class="sxs-lookup"><span data-stu-id="c2023-210">False</span></span>                           |
| <span data-ttu-id="c2023-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2023-211">Is Indexed</span></span>             | <span data-ttu-id="c2023-212">否</span><span class="sxs-lookup"><span data-stu-id="c2023-212">False</span></span>                           |
| <span data-ttu-id="c2023-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2023-213">In Global Catalog</span></span>      | <span data-ttu-id="c2023-214">否</span><span class="sxs-lookup"><span data-stu-id="c2023-214">False</span></span>                           |
| <span data-ttu-id="c2023-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2023-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2023-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2023-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2023-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2023-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2023-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2023-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2023-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-219">Search-Flags</span></span>           | <span data-ttu-id="c2023-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2023-220">0x00000000</span></span>                      |
| <span data-ttu-id="c2023-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-221">System-Flags</span></span>           | <span data-ttu-id="c2023-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2023-222">0x00000010</span></span>                      |
| <span data-ttu-id="c2023-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2023-223">Classes used in</span></span>        | [<span data-ttu-id="c2023-224">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c2023-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c2023-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2023-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c2023-226">進入</span><span class="sxs-lookup"><span data-stu-id="c2023-226">Entry</span></span> | <span data-ttu-id="c2023-227">值</span><span class="sxs-lookup"><span data-stu-id="c2023-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2023-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2023-228">Link-Id</span></span>                | <span data-ttu-id="c2023-229">71</span><span class="sxs-lookup"><span data-stu-id="c2023-229">71</span></span>                              |
| <span data-ttu-id="c2023-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2023-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2023-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2023-231">System-Only</span></span>            | <span data-ttu-id="c2023-232">對</span><span class="sxs-lookup"><span data-stu-id="c2023-232">True</span></span>                            |
| <span data-ttu-id="c2023-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2023-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c2023-234">否</span><span class="sxs-lookup"><span data-stu-id="c2023-234">False</span></span>                           |
| <span data-ttu-id="c2023-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2023-235">Is Indexed</span></span>             | <span data-ttu-id="c2023-236">否</span><span class="sxs-lookup"><span data-stu-id="c2023-236">False</span></span>                           |
| <span data-ttu-id="c2023-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2023-237">In Global Catalog</span></span>      | <span data-ttu-id="c2023-238">否</span><span class="sxs-lookup"><span data-stu-id="c2023-238">False</span></span>                           |
| <span data-ttu-id="c2023-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2023-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2023-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2023-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2023-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2023-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2023-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2023-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2023-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-243">Search-Flags</span></span>           | <span data-ttu-id="c2023-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2023-244">0x00000000</span></span>                      |
| <span data-ttu-id="c2023-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-245">System-Flags</span></span>           | <span data-ttu-id="c2023-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2023-246">0x00000010</span></span>                      |
| <span data-ttu-id="c2023-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2023-247">Classes used in</span></span>        | [<span data-ttu-id="c2023-248">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c2023-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c2023-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2023-249">Windows Server 2012</span></span>



| <span data-ttu-id="c2023-250">進入</span><span class="sxs-lookup"><span data-stu-id="c2023-250">Entry</span></span> | <span data-ttu-id="c2023-251">值</span><span class="sxs-lookup"><span data-stu-id="c2023-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c2023-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2023-252">Link-Id</span></span>                | <span data-ttu-id="c2023-253">71</span><span class="sxs-lookup"><span data-stu-id="c2023-253">71</span></span>                              |
| <span data-ttu-id="c2023-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2023-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c2023-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2023-255">System-Only</span></span>            | <span data-ttu-id="c2023-256">對</span><span class="sxs-lookup"><span data-stu-id="c2023-256">True</span></span>                            |
| <span data-ttu-id="c2023-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2023-257">Is-Single-Valued</span></span>       | <span data-ttu-id="c2023-258">否</span><span class="sxs-lookup"><span data-stu-id="c2023-258">False</span></span>                           |
| <span data-ttu-id="c2023-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2023-259">Is Indexed</span></span>             | <span data-ttu-id="c2023-260">否</span><span class="sxs-lookup"><span data-stu-id="c2023-260">False</span></span>                           |
| <span data-ttu-id="c2023-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2023-261">In Global Catalog</span></span>      | <span data-ttu-id="c2023-262">否</span><span class="sxs-lookup"><span data-stu-id="c2023-262">False</span></span>                           |
| <span data-ttu-id="c2023-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2023-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2023-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2023-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c2023-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2023-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c2023-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2023-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c2023-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-267">Search-Flags</span></span>           | <span data-ttu-id="c2023-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2023-268">0x00000000</span></span>                      |
| <span data-ttu-id="c2023-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2023-269">System-Flags</span></span>           | <span data-ttu-id="c2023-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2023-270">0x00000010</span></span>                      |
| <span data-ttu-id="c2023-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2023-271">Classes used in</span></span>        | [<span data-ttu-id="c2023-272">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c2023-272">**Top**</span></span>](c-top.md)<br/> |



 

 






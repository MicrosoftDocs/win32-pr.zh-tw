---
title: NT 群組-Members 屬性
description: 未使用此屬性。 |NT 群組-Members 屬性
ms.assetid: e7f7cf82-eff9-429f-ab3d-a35b9385362a
ms.tgt_platform: multiple
keywords:
- NT-Group-Members 屬性 AD 架構
- nTGroupMembers 屬性 AD 架構
topic_type:
- apiref
api_name:
- NT-Group-Members
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f212da06992c367a4221cc49eb7217a309886745
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321948"
---
# <a name="nt-group-members-attribute"></a><span data-ttu-id="9e0da-106">NT 群組-Members 屬性</span><span class="sxs-lookup"><span data-stu-id="9e0da-106">NT-Group-Members attribute</span></span>

<span data-ttu-id="9e0da-107">未使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="9e0da-107">This attribute is not used.</span></span>

<span data-ttu-id="9e0da-108">[**成員**](a-member.md)屬性是用來包含群組的成員。</span><span class="sxs-lookup"><span data-stu-id="9e0da-108">The [**member**](a-member.md) attribute is used to contain the members of a group.</span></span>



| <span data-ttu-id="9e0da-109">進入</span><span class="sxs-lookup"><span data-stu-id="9e0da-109">Entry</span></span> | <span data-ttu-id="9e0da-110">值</span><span class="sxs-lookup"><span data-stu-id="9e0da-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="9e0da-111">CN</span><span class="sxs-lookup"><span data-stu-id="9e0da-111">CN</span></span>                | <span data-ttu-id="9e0da-112">NT 群組-成員</span><span class="sxs-lookup"><span data-stu-id="9e0da-112">NT-Group-Members</span></span>                                      |
| <span data-ttu-id="9e0da-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9e0da-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9e0da-114">nTGroupMembers</span><span class="sxs-lookup"><span data-stu-id="9e0da-114">nTGroupMembers</span></span>                                        |
| <span data-ttu-id="9e0da-115">大小</span><span class="sxs-lookup"><span data-stu-id="9e0da-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="9e0da-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9e0da-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="9e0da-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9e0da-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="9e0da-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9e0da-118">Attribute-Id</span></span>      | <span data-ttu-id="9e0da-119">1.2.840.113556.1.4.89</span><span class="sxs-lookup"><span data-stu-id="9e0da-119">1.2.840.113556.1.4.89</span></span>                                 |
| <span data-ttu-id="9e0da-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9e0da-120">System-Id-Guid</span></span>    | <span data-ttu-id="9e0da-121">bf9679df-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9e0da-121">bf9679df-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="9e0da-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e0da-122">Syntax</span></span>            | [<span data-ttu-id="9e0da-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="9e0da-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="9e0da-124">實作</span><span class="sxs-lookup"><span data-stu-id="9e0da-124">Implementations</span></span>

-   [<span data-ttu-id="9e0da-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9e0da-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9e0da-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9e0da-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9e0da-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9e0da-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9e0da-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9e0da-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9e0da-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9e0da-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9e0da-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9e0da-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9e0da-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e0da-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9e0da-132">進入</span><span class="sxs-lookup"><span data-stu-id="9e0da-132">Entry</span></span> | <span data-ttu-id="9e0da-133">值</span><span class="sxs-lookup"><span data-stu-id="9e0da-133">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="9e0da-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e0da-134">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e0da-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e0da-136">System-Only</span></span>            | <span data-ttu-id="9e0da-137">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-137">False</span></span>                               |
| <span data-ttu-id="9e0da-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e0da-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9e0da-139">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-139">False</span></span>                               |
| <span data-ttu-id="9e0da-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e0da-140">Is Indexed</span></span>             | <span data-ttu-id="9e0da-141">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-141">False</span></span>                               |
| <span data-ttu-id="9e0da-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e0da-142">In Global Catalog</span></span>      | <span data-ttu-id="9e0da-143">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-143">False</span></span>                               |
| <span data-ttu-id="9e0da-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e0da-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e0da-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e0da-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="9e0da-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e0da-146">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e0da-147">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-148">Search-Flags</span></span>           | <span data-ttu-id="9e0da-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e0da-149">0x00000000</span></span>                          |
| <span data-ttu-id="9e0da-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-150">System-Flags</span></span>           | <span data-ttu-id="9e0da-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e0da-151">0x00000010</span></span>                          |
| <span data-ttu-id="9e0da-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e0da-152">Classes used in</span></span>        | [<span data-ttu-id="9e0da-153">**Group**</span><span class="sxs-lookup"><span data-stu-id="9e0da-153">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9e0da-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e0da-154">Windows Server 2003</span></span>



| <span data-ttu-id="9e0da-155">進入</span><span class="sxs-lookup"><span data-stu-id="9e0da-155">Entry</span></span> | <span data-ttu-id="9e0da-156">值</span><span class="sxs-lookup"><span data-stu-id="9e0da-156">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="9e0da-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e0da-157">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e0da-158">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e0da-159">System-Only</span></span>            | <span data-ttu-id="9e0da-160">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-160">False</span></span>                               |
| <span data-ttu-id="9e0da-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e0da-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9e0da-162">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-162">False</span></span>                               |
| <span data-ttu-id="9e0da-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e0da-163">Is Indexed</span></span>             | <span data-ttu-id="9e0da-164">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-164">False</span></span>                               |
| <span data-ttu-id="9e0da-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e0da-165">In Global Catalog</span></span>      | <span data-ttu-id="9e0da-166">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-166">False</span></span>                               |
| <span data-ttu-id="9e0da-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e0da-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e0da-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e0da-168">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="9e0da-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e0da-169">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e0da-170">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-171">Search-Flags</span></span>           | <span data-ttu-id="9e0da-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e0da-172">0x00000000</span></span>                          |
| <span data-ttu-id="9e0da-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-173">System-Flags</span></span>           | <span data-ttu-id="9e0da-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e0da-174">0x00000010</span></span>                          |
| <span data-ttu-id="9e0da-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e0da-175">Classes used in</span></span>        | [<span data-ttu-id="9e0da-176">**Group**</span><span class="sxs-lookup"><span data-stu-id="9e0da-176">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9e0da-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9e0da-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9e0da-178">進入</span><span class="sxs-lookup"><span data-stu-id="9e0da-178">Entry</span></span> | <span data-ttu-id="9e0da-179">值</span><span class="sxs-lookup"><span data-stu-id="9e0da-179">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="9e0da-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e0da-180">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e0da-181">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e0da-182">System-Only</span></span>            | <span data-ttu-id="9e0da-183">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-183">False</span></span>                               |
| <span data-ttu-id="9e0da-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e0da-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9e0da-185">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-185">False</span></span>                               |
| <span data-ttu-id="9e0da-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e0da-186">Is Indexed</span></span>             | <span data-ttu-id="9e0da-187">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-187">False</span></span>                               |
| <span data-ttu-id="9e0da-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e0da-188">In Global Catalog</span></span>      | <span data-ttu-id="9e0da-189">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-189">False</span></span>                               |
| <span data-ttu-id="9e0da-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e0da-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e0da-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e0da-191">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="9e0da-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e0da-192">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e0da-193">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-194">Search-Flags</span></span>           | <span data-ttu-id="9e0da-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e0da-195">0x00000000</span></span>                          |
| <span data-ttu-id="9e0da-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-196">System-Flags</span></span>           | <span data-ttu-id="9e0da-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e0da-197">0x00000010</span></span>                          |
| <span data-ttu-id="9e0da-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e0da-198">Classes used in</span></span>        | [<span data-ttu-id="9e0da-199">**Group**</span><span class="sxs-lookup"><span data-stu-id="9e0da-199">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9e0da-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e0da-200">Windows Server 2008</span></span>



| <span data-ttu-id="9e0da-201">進入</span><span class="sxs-lookup"><span data-stu-id="9e0da-201">Entry</span></span> | <span data-ttu-id="9e0da-202">值</span><span class="sxs-lookup"><span data-stu-id="9e0da-202">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="9e0da-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e0da-203">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e0da-204">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e0da-205">System-Only</span></span>            | <span data-ttu-id="9e0da-206">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-206">False</span></span>                               |
| <span data-ttu-id="9e0da-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e0da-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9e0da-208">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-208">False</span></span>                               |
| <span data-ttu-id="9e0da-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e0da-209">Is Indexed</span></span>             | <span data-ttu-id="9e0da-210">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-210">False</span></span>                               |
| <span data-ttu-id="9e0da-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e0da-211">In Global Catalog</span></span>      | <span data-ttu-id="9e0da-212">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-212">False</span></span>                               |
| <span data-ttu-id="9e0da-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e0da-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e0da-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e0da-214">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="9e0da-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e0da-215">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e0da-216">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-217">Search-Flags</span></span>           | <span data-ttu-id="9e0da-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e0da-218">0x00000000</span></span>                          |
| <span data-ttu-id="9e0da-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-219">System-Flags</span></span>           | <span data-ttu-id="9e0da-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e0da-220">0x00000010</span></span>                          |
| <span data-ttu-id="9e0da-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e0da-221">Classes used in</span></span>        | [<span data-ttu-id="9e0da-222">**Group**</span><span class="sxs-lookup"><span data-stu-id="9e0da-222">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9e0da-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e0da-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9e0da-224">進入</span><span class="sxs-lookup"><span data-stu-id="9e0da-224">Entry</span></span> | <span data-ttu-id="9e0da-225">值</span><span class="sxs-lookup"><span data-stu-id="9e0da-225">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="9e0da-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e0da-226">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e0da-227">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e0da-228">System-Only</span></span>            | <span data-ttu-id="9e0da-229">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-229">False</span></span>                               |
| <span data-ttu-id="9e0da-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e0da-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9e0da-231">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-231">False</span></span>                               |
| <span data-ttu-id="9e0da-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e0da-232">Is Indexed</span></span>             | <span data-ttu-id="9e0da-233">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-233">False</span></span>                               |
| <span data-ttu-id="9e0da-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e0da-234">In Global Catalog</span></span>      | <span data-ttu-id="9e0da-235">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-235">False</span></span>                               |
| <span data-ttu-id="9e0da-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e0da-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e0da-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e0da-237">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="9e0da-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e0da-238">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e0da-239">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-240">Search-Flags</span></span>           | <span data-ttu-id="9e0da-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e0da-241">0x00000000</span></span>                          |
| <span data-ttu-id="9e0da-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-242">System-Flags</span></span>           | <span data-ttu-id="9e0da-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e0da-243">0x00000010</span></span>                          |
| <span data-ttu-id="9e0da-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e0da-244">Classes used in</span></span>        | [<span data-ttu-id="9e0da-245">**Group**</span><span class="sxs-lookup"><span data-stu-id="9e0da-245">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9e0da-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e0da-246">Windows Server 2012</span></span>



| <span data-ttu-id="9e0da-247">進入</span><span class="sxs-lookup"><span data-stu-id="9e0da-247">Entry</span></span> | <span data-ttu-id="9e0da-248">值</span><span class="sxs-lookup"><span data-stu-id="9e0da-248">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="9e0da-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e0da-249">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e0da-250">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="9e0da-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e0da-251">System-Only</span></span>            | <span data-ttu-id="9e0da-252">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-252">False</span></span>                               |
| <span data-ttu-id="9e0da-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e0da-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9e0da-254">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-254">False</span></span>                               |
| <span data-ttu-id="9e0da-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e0da-255">Is Indexed</span></span>             | <span data-ttu-id="9e0da-256">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-256">False</span></span>                               |
| <span data-ttu-id="9e0da-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e0da-257">In Global Catalog</span></span>      | <span data-ttu-id="9e0da-258">否</span><span class="sxs-lookup"><span data-stu-id="9e0da-258">False</span></span>                               |
| <span data-ttu-id="9e0da-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e0da-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e0da-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e0da-260">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="9e0da-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e0da-261">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e0da-262">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="9e0da-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-263">Search-Flags</span></span>           | <span data-ttu-id="9e0da-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e0da-264">0x00000000</span></span>                          |
| <span data-ttu-id="9e0da-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e0da-265">System-Flags</span></span>           | <span data-ttu-id="9e0da-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e0da-266">0x00000010</span></span>                          |
| <span data-ttu-id="9e0da-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e0da-267">Classes used in</span></span>        | [<span data-ttu-id="9e0da-268">**Group**</span><span class="sxs-lookup"><span data-stu-id="9e0da-268">**Group**</span></span>](c-group.md)<br/> |



 

 






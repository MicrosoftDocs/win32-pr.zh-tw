---
title: ms DS-非成員屬性
description: 這個屬性的用途與非安全性成員屬性相同，但套用了範圍規則。
ms.assetid: 11d3d030-3643-4ed2-a52e-a57f32e9597f
ms.tgt_platform: multiple
keywords:
- ms DS-非成員屬性 AD 架構
- 的非成員屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Non-Members
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8ca19af90f2f534f974863aa7d766f6be4624b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845152"
---
# <a name="ms-ds-non-members-attribute"></a><span data-ttu-id="b68d3-105">ms DS-非成員屬性</span><span class="sxs-lookup"><span data-stu-id="b68d3-105">ms-DS-Non-Members attribute</span></span>

<span data-ttu-id="b68d3-106">這個屬性的用途與非安全性成員屬性相同，但套用了範圍規則。</span><span class="sxs-lookup"><span data-stu-id="b68d3-106">This attribute serves the same purpose as the Non-Security-Member attribute but with scoping rules applied.</span></span>



| <span data-ttu-id="b68d3-107">進入</span><span class="sxs-lookup"><span data-stu-id="b68d3-107">Entry</span></span> | <span data-ttu-id="b68d3-108">值</span><span class="sxs-lookup"><span data-stu-id="b68d3-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b68d3-109">CN</span><span class="sxs-lookup"><span data-stu-id="b68d3-109">CN</span></span>                | <span data-ttu-id="b68d3-110">ms DS-非成員</span><span class="sxs-lookup"><span data-stu-id="b68d3-110">ms-DS-Non-Members</span></span>                       |
| <span data-ttu-id="b68d3-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b68d3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b68d3-112">非成員</span><span class="sxs-lookup"><span data-stu-id="b68d3-112">msDS-NonMembers</span></span>                         |
| <span data-ttu-id="b68d3-113">大小</span><span class="sxs-lookup"><span data-stu-id="b68d3-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="b68d3-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b68d3-114">Update Privilege</span></span>  | <span data-ttu-id="b68d3-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="b68d3-115">AzRoles Admin</span></span>                           |
| <span data-ttu-id="b68d3-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b68d3-116">Update Frequency</span></span>  | <span data-ttu-id="b68d3-117">在初始化和原則變更時。</span><span class="sxs-lookup"><span data-stu-id="b68d3-117">At initialization and policy change.</span></span>    |
| <span data-ttu-id="b68d3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b68d3-118">Attribute-Id</span></span>      | <span data-ttu-id="b68d3-119">1.2.840.113556.1.4.1793</span><span class="sxs-lookup"><span data-stu-id="b68d3-119">1.2.840.113556.1.4.1793</span></span>                 |
| <span data-ttu-id="b68d3-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b68d3-120">System-Id-Guid</span></span>    | <span data-ttu-id="b68d3-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span><span class="sxs-lookup"><span data-stu-id="b68d3-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span></span>    |
| <span data-ttu-id="b68d3-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b68d3-122">Syntax</span></span>            | [<span data-ttu-id="b68d3-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b68d3-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="b68d3-124">實作</span><span class="sxs-lookup"><span data-stu-id="b68d3-124">Implementations</span></span>

-   [<span data-ttu-id="b68d3-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b68d3-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b68d3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b68d3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b68d3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b68d3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b68d3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b68d3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b68d3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b68d3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b68d3-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b68d3-130">Windows Server 2003</span></span>



| <span data-ttu-id="b68d3-131">進入</span><span class="sxs-lookup"><span data-stu-id="b68d3-131">Entry</span></span> | <span data-ttu-id="b68d3-132">值</span><span class="sxs-lookup"><span data-stu-id="b68d3-132">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b68d3-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b68d3-133">Link-Id</span></span>                | <span data-ttu-id="b68d3-134">2014</span><span class="sxs-lookup"><span data-stu-id="b68d3-134">2014</span></span>                                |
| <span data-ttu-id="b68d3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68d3-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b68d3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68d3-136">System-Only</span></span>            | <span data-ttu-id="b68d3-137">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-137">False</span></span>                               |
| <span data-ttu-id="b68d3-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b68d3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b68d3-139">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-139">False</span></span>                               |
| <span data-ttu-id="b68d3-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b68d3-140">Is Indexed</span></span>             | <span data-ttu-id="b68d3-141">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-141">False</span></span>                               |
| <span data-ttu-id="b68d3-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b68d3-142">In Global Catalog</span></span>      | <span data-ttu-id="b68d3-143">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-143">False</span></span>                               |
| <span data-ttu-id="b68d3-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b68d3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68d3-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b68d3-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b68d3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68d3-146">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68d3-147">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-148">Search-Flags</span></span>           | <span data-ttu-id="b68d3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68d3-149">0x00000000</span></span>                          |
| <span data-ttu-id="b68d3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-150">System-Flags</span></span>           | <span data-ttu-id="b68d3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b68d3-151">0x00000010</span></span>                          |
| <span data-ttu-id="b68d3-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b68d3-152">Classes used in</span></span>        | [<span data-ttu-id="b68d3-153">**Group**</span><span class="sxs-lookup"><span data-stu-id="b68d3-153">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b68d3-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b68d3-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b68d3-155">進入</span><span class="sxs-lookup"><span data-stu-id="b68d3-155">Entry</span></span> | <span data-ttu-id="b68d3-156">值</span><span class="sxs-lookup"><span data-stu-id="b68d3-156">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b68d3-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b68d3-157">Link-Id</span></span>                | <span data-ttu-id="b68d3-158">2014</span><span class="sxs-lookup"><span data-stu-id="b68d3-158">2014</span></span>                                |
| <span data-ttu-id="b68d3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68d3-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b68d3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68d3-160">System-Only</span></span>            | <span data-ttu-id="b68d3-161">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-161">False</span></span>                               |
| <span data-ttu-id="b68d3-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b68d3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b68d3-163">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-163">False</span></span>                               |
| <span data-ttu-id="b68d3-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b68d3-164">Is Indexed</span></span>             | <span data-ttu-id="b68d3-165">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-165">False</span></span>                               |
| <span data-ttu-id="b68d3-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b68d3-166">In Global Catalog</span></span>      | <span data-ttu-id="b68d3-167">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-167">False</span></span>                               |
| <span data-ttu-id="b68d3-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b68d3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68d3-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b68d3-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b68d3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68d3-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68d3-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-172">Search-Flags</span></span>           | <span data-ttu-id="b68d3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68d3-173">0x00000000</span></span>                          |
| <span data-ttu-id="b68d3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-174">System-Flags</span></span>           | <span data-ttu-id="b68d3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b68d3-175">0x00000010</span></span>                          |
| <span data-ttu-id="b68d3-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b68d3-176">Classes used in</span></span>        | [<span data-ttu-id="b68d3-177">**Group**</span><span class="sxs-lookup"><span data-stu-id="b68d3-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b68d3-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b68d3-178">Windows Server 2008</span></span>



| <span data-ttu-id="b68d3-179">進入</span><span class="sxs-lookup"><span data-stu-id="b68d3-179">Entry</span></span> | <span data-ttu-id="b68d3-180">值</span><span class="sxs-lookup"><span data-stu-id="b68d3-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b68d3-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b68d3-181">Link-Id</span></span>                | <span data-ttu-id="b68d3-182">2014</span><span class="sxs-lookup"><span data-stu-id="b68d3-182">2014</span></span>                                |
| <span data-ttu-id="b68d3-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68d3-183">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b68d3-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68d3-184">System-Only</span></span>            | <span data-ttu-id="b68d3-185">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-185">False</span></span>                               |
| <span data-ttu-id="b68d3-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b68d3-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b68d3-187">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-187">False</span></span>                               |
| <span data-ttu-id="b68d3-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b68d3-188">Is Indexed</span></span>             | <span data-ttu-id="b68d3-189">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-189">False</span></span>                               |
| <span data-ttu-id="b68d3-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b68d3-190">In Global Catalog</span></span>      | <span data-ttu-id="b68d3-191">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-191">False</span></span>                               |
| <span data-ttu-id="b68d3-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b68d3-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68d3-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b68d3-193">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b68d3-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68d3-194">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68d3-195">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-196">Search-Flags</span></span>           | <span data-ttu-id="b68d3-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68d3-197">0x00000000</span></span>                          |
| <span data-ttu-id="b68d3-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-198">System-Flags</span></span>           | <span data-ttu-id="b68d3-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b68d3-199">0x00000010</span></span>                          |
| <span data-ttu-id="b68d3-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b68d3-200">Classes used in</span></span>        | [<span data-ttu-id="b68d3-201">**Group**</span><span class="sxs-lookup"><span data-stu-id="b68d3-201">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b68d3-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b68d3-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b68d3-203">進入</span><span class="sxs-lookup"><span data-stu-id="b68d3-203">Entry</span></span> | <span data-ttu-id="b68d3-204">值</span><span class="sxs-lookup"><span data-stu-id="b68d3-204">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b68d3-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b68d3-205">Link-Id</span></span>                | <span data-ttu-id="b68d3-206">2014</span><span class="sxs-lookup"><span data-stu-id="b68d3-206">2014</span></span>                                |
| <span data-ttu-id="b68d3-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68d3-207">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b68d3-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68d3-208">System-Only</span></span>            | <span data-ttu-id="b68d3-209">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-209">False</span></span>                               |
| <span data-ttu-id="b68d3-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b68d3-210">Is-Single-Valued</span></span>       | <span data-ttu-id="b68d3-211">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-211">False</span></span>                               |
| <span data-ttu-id="b68d3-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b68d3-212">Is Indexed</span></span>             | <span data-ttu-id="b68d3-213">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-213">False</span></span>                               |
| <span data-ttu-id="b68d3-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b68d3-214">In Global Catalog</span></span>      | <span data-ttu-id="b68d3-215">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-215">False</span></span>                               |
| <span data-ttu-id="b68d3-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b68d3-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68d3-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b68d3-217">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b68d3-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68d3-218">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68d3-219">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-220">Search-Flags</span></span>           | <span data-ttu-id="b68d3-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68d3-221">0x00000000</span></span>                          |
| <span data-ttu-id="b68d3-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-222">System-Flags</span></span>           | <span data-ttu-id="b68d3-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b68d3-223">0x00000010</span></span>                          |
| <span data-ttu-id="b68d3-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b68d3-224">Classes used in</span></span>        | [<span data-ttu-id="b68d3-225">**Group**</span><span class="sxs-lookup"><span data-stu-id="b68d3-225">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b68d3-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b68d3-226">Windows Server 2012</span></span>



| <span data-ttu-id="b68d3-227">進入</span><span class="sxs-lookup"><span data-stu-id="b68d3-227">Entry</span></span> | <span data-ttu-id="b68d3-228">值</span><span class="sxs-lookup"><span data-stu-id="b68d3-228">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b68d3-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b68d3-229">Link-Id</span></span>                | <span data-ttu-id="b68d3-230">2014</span><span class="sxs-lookup"><span data-stu-id="b68d3-230">2014</span></span>                                |
| <span data-ttu-id="b68d3-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68d3-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b68d3-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68d3-232">System-Only</span></span>            | <span data-ttu-id="b68d3-233">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-233">False</span></span>                               |
| <span data-ttu-id="b68d3-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b68d3-234">Is-Single-Valued</span></span>       | <span data-ttu-id="b68d3-235">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-235">False</span></span>                               |
| <span data-ttu-id="b68d3-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b68d3-236">Is Indexed</span></span>             | <span data-ttu-id="b68d3-237">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-237">False</span></span>                               |
| <span data-ttu-id="b68d3-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b68d3-238">In Global Catalog</span></span>      | <span data-ttu-id="b68d3-239">否</span><span class="sxs-lookup"><span data-stu-id="b68d3-239">False</span></span>                               |
| <span data-ttu-id="b68d3-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b68d3-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68d3-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b68d3-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b68d3-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68d3-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68d3-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="b68d3-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-244">Search-Flags</span></span>           | <span data-ttu-id="b68d3-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68d3-245">0x00000000</span></span>                          |
| <span data-ttu-id="b68d3-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68d3-246">System-Flags</span></span>           | <span data-ttu-id="b68d3-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b68d3-247">0x00000010</span></span>                          |
| <span data-ttu-id="b68d3-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b68d3-248">Classes used in</span></span>        | [<span data-ttu-id="b68d3-249">**Group**</span><span class="sxs-lookup"><span data-stu-id="b68d3-249">**Group**</span></span>](c-group.md)<br/> |



 

 






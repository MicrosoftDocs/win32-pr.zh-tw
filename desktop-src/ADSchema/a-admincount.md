---
title: Admin-Count 屬性
description: 指出指定的物件已將其 Acl 變更為系統中較安全的值，因為它是直接或可轉移)  (其中一個系統管理群組的成員。
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Admin-Count 屬性 AD 架構
- adminCount 屬性 AD 架構
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b953aebaa39bb3fc3e4c9cf96632f32a37850
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687331"
---
# <a name="admin-count-attribute"></a><span data-ttu-id="0d502-105">Admin-Count 屬性</span><span class="sxs-lookup"><span data-stu-id="0d502-105">Admin-Count attribute</span></span>

<span data-ttu-id="0d502-106">指出指定的物件已將其 Acl 變更為系統中較安全的值，因為它是直接或可轉移)  (其中一個系統管理群組的成員。</span><span class="sxs-lookup"><span data-stu-id="0d502-106">Indicates that a given object has had its ACLs changed to a more secure value by the system because it was a member of one of the administrative groups (directly or transitively).</span></span>



| <span data-ttu-id="0d502-107">進入</span><span class="sxs-lookup"><span data-stu-id="0d502-107">Entry</span></span> | <span data-ttu-id="0d502-108">值</span><span class="sxs-lookup"><span data-stu-id="0d502-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="0d502-109">CN</span><span class="sxs-lookup"><span data-stu-id="0d502-109">CN</span></span>                | <span data-ttu-id="0d502-110">Admin-Count</span><span class="sxs-lookup"><span data-stu-id="0d502-110">Admin-Count</span></span>                                         |
| <span data-ttu-id="0d502-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0d502-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0d502-112">adminCount</span><span class="sxs-lookup"><span data-stu-id="0d502-112">adminCount</span></span>                                          |
| <span data-ttu-id="0d502-113">大小</span><span class="sxs-lookup"><span data-stu-id="0d502-113">Size</span></span>              | <span data-ttu-id="0d502-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="0d502-114">4 bytes</span></span>                                             |
| <span data-ttu-id="0d502-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0d502-115">Update Privilege</span></span>  | <span data-ttu-id="0d502-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="0d502-116">This value is set by the system.</span></span>                    |
| <span data-ttu-id="0d502-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0d502-117">Update Frequency</span></span>  | <span data-ttu-id="0d502-118">當物件加入至系統管理群組時。</span><span class="sxs-lookup"><span data-stu-id="0d502-118">When an object is added to an administrative group.</span></span> |
| <span data-ttu-id="0d502-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0d502-119">Attribute-Id</span></span>      | <span data-ttu-id="0d502-120">1.2.840.113556.1.4.150</span><span class="sxs-lookup"><span data-stu-id="0d502-120">1.2.840.113556.1.4.150</span></span>                              |
| <span data-ttu-id="0d502-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0d502-121">System-Id-Guid</span></span>    | <span data-ttu-id="0d502-122">bf967918-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0d502-122">bf967918-0de6-11d0-a285-00aa003049e2</span></span>                |
| <span data-ttu-id="0d502-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d502-123">Syntax</span></span>            | [<span data-ttu-id="0d502-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="0d502-124">**Enumeration**</span></span>](s-enumeration.md)                |



## <a name="implementations"></a><span data-ttu-id="0d502-125">實作</span><span class="sxs-lookup"><span data-stu-id="0d502-125">Implementations</span></span>

-   [<span data-ttu-id="0d502-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0d502-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0d502-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0d502-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0d502-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0d502-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0d502-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0d502-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0d502-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0d502-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0d502-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0d502-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0d502-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0d502-132">Windows 2000 Server</span></span>



| <span data-ttu-id="0d502-133">進入</span><span class="sxs-lookup"><span data-stu-id="0d502-133">Entry</span></span> | <span data-ttu-id="0d502-134">值</span><span class="sxs-lookup"><span data-stu-id="0d502-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0d502-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d502-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d502-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d502-137">System-Only</span></span>            | <span data-ttu-id="0d502-138">否</span><span class="sxs-lookup"><span data-stu-id="0d502-138">False</span></span>                                                                 |
| <span data-ttu-id="0d502-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d502-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0d502-140">對</span><span class="sxs-lookup"><span data-stu-id="0d502-140">True</span></span>                                                                  |
| <span data-ttu-id="0d502-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d502-141">Is Indexed</span></span>             | <span data-ttu-id="0d502-142">否</span><span class="sxs-lookup"><span data-stu-id="0d502-142">False</span></span>                                                                 |
| <span data-ttu-id="0d502-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d502-143">In Global Catalog</span></span>      | <span data-ttu-id="0d502-144">否</span><span class="sxs-lookup"><span data-stu-id="0d502-144">False</span></span>                                                                 |
| <span data-ttu-id="0d502-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d502-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d502-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d502-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="0d502-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d502-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d502-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-149">Search-Flags</span></span>           | <span data-ttu-id="0d502-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d502-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="0d502-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-151">System-Flags</span></span>           | <span data-ttu-id="0d502-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d502-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="0d502-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d502-153">Classes used in</span></span>        | [<span data-ttu-id="0d502-154">**Group**</span><span class="sxs-lookup"><span data-stu-id="0d502-154">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="0d502-155">**User**</span><span class="sxs-lookup"><span data-stu-id="0d502-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0d502-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d502-156">Windows Server 2003</span></span>



| <span data-ttu-id="0d502-157">進入</span><span class="sxs-lookup"><span data-stu-id="0d502-157">Entry</span></span> | <span data-ttu-id="0d502-158">值</span><span class="sxs-lookup"><span data-stu-id="0d502-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0d502-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d502-159">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d502-160">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d502-161">System-Only</span></span>            | <span data-ttu-id="0d502-162">否</span><span class="sxs-lookup"><span data-stu-id="0d502-162">False</span></span>                                                                 |
| <span data-ttu-id="0d502-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d502-163">Is-Single-Valued</span></span>       | <span data-ttu-id="0d502-164">對</span><span class="sxs-lookup"><span data-stu-id="0d502-164">True</span></span>                                                                  |
| <span data-ttu-id="0d502-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d502-165">Is Indexed</span></span>             | <span data-ttu-id="0d502-166">否</span><span class="sxs-lookup"><span data-stu-id="0d502-166">False</span></span>                                                                 |
| <span data-ttu-id="0d502-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d502-167">In Global Catalog</span></span>      | <span data-ttu-id="0d502-168">否</span><span class="sxs-lookup"><span data-stu-id="0d502-168">False</span></span>                                                                 |
| <span data-ttu-id="0d502-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d502-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d502-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d502-170">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="0d502-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d502-171">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d502-172">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-173">Search-Flags</span></span>           | <span data-ttu-id="0d502-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d502-174">0x00000000</span></span>                                                            |
| <span data-ttu-id="0d502-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-175">System-Flags</span></span>           | <span data-ttu-id="0d502-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d502-176">0x00000010</span></span>                                                            |
| <span data-ttu-id="0d502-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d502-177">Classes used in</span></span>        | [<span data-ttu-id="0d502-178">**Group**</span><span class="sxs-lookup"><span data-stu-id="0d502-178">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="0d502-179">**User**</span><span class="sxs-lookup"><span data-stu-id="0d502-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0d502-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0d502-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0d502-181">進入</span><span class="sxs-lookup"><span data-stu-id="0d502-181">Entry</span></span> | <span data-ttu-id="0d502-182">值</span><span class="sxs-lookup"><span data-stu-id="0d502-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0d502-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d502-183">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d502-184">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d502-185">System-Only</span></span>            | <span data-ttu-id="0d502-186">否</span><span class="sxs-lookup"><span data-stu-id="0d502-186">False</span></span>                                                                 |
| <span data-ttu-id="0d502-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d502-187">Is-Single-Valued</span></span>       | <span data-ttu-id="0d502-188">對</span><span class="sxs-lookup"><span data-stu-id="0d502-188">True</span></span>                                                                  |
| <span data-ttu-id="0d502-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d502-189">Is Indexed</span></span>             | <span data-ttu-id="0d502-190">否</span><span class="sxs-lookup"><span data-stu-id="0d502-190">False</span></span>                                                                 |
| <span data-ttu-id="0d502-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d502-191">In Global Catalog</span></span>      | <span data-ttu-id="0d502-192">否</span><span class="sxs-lookup"><span data-stu-id="0d502-192">False</span></span>                                                                 |
| <span data-ttu-id="0d502-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d502-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d502-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d502-194">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="0d502-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d502-195">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d502-196">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-197">Search-Flags</span></span>           | <span data-ttu-id="0d502-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d502-198">0x00000000</span></span>                                                            |
| <span data-ttu-id="0d502-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-199">System-Flags</span></span>           | <span data-ttu-id="0d502-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d502-200">0x00000010</span></span>                                                            |
| <span data-ttu-id="0d502-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d502-201">Classes used in</span></span>        | [<span data-ttu-id="0d502-202">**Group**</span><span class="sxs-lookup"><span data-stu-id="0d502-202">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="0d502-203">**User**</span><span class="sxs-lookup"><span data-stu-id="0d502-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0d502-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d502-204">Windows Server 2008</span></span>



| <span data-ttu-id="0d502-205">進入</span><span class="sxs-lookup"><span data-stu-id="0d502-205">Entry</span></span> | <span data-ttu-id="0d502-206">值</span><span class="sxs-lookup"><span data-stu-id="0d502-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0d502-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d502-207">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d502-208">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d502-209">System-Only</span></span>            | <span data-ttu-id="0d502-210">否</span><span class="sxs-lookup"><span data-stu-id="0d502-210">False</span></span>                                                                 |
| <span data-ttu-id="0d502-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d502-211">Is-Single-Valued</span></span>       | <span data-ttu-id="0d502-212">對</span><span class="sxs-lookup"><span data-stu-id="0d502-212">True</span></span>                                                                  |
| <span data-ttu-id="0d502-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d502-213">Is Indexed</span></span>             | <span data-ttu-id="0d502-214">否</span><span class="sxs-lookup"><span data-stu-id="0d502-214">False</span></span>                                                                 |
| <span data-ttu-id="0d502-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d502-215">In Global Catalog</span></span>      | <span data-ttu-id="0d502-216">否</span><span class="sxs-lookup"><span data-stu-id="0d502-216">False</span></span>                                                                 |
| <span data-ttu-id="0d502-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d502-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d502-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d502-218">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="0d502-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d502-219">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d502-220">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-221">Search-Flags</span></span>           | <span data-ttu-id="0d502-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d502-222">0x00000000</span></span>                                                            |
| <span data-ttu-id="0d502-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-223">System-Flags</span></span>           | <span data-ttu-id="0d502-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d502-224">0x00000010</span></span>                                                            |
| <span data-ttu-id="0d502-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d502-225">Classes used in</span></span>        | [<span data-ttu-id="0d502-226">**Group**</span><span class="sxs-lookup"><span data-stu-id="0d502-226">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="0d502-227">**User**</span><span class="sxs-lookup"><span data-stu-id="0d502-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0d502-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0d502-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0d502-229">進入</span><span class="sxs-lookup"><span data-stu-id="0d502-229">Entry</span></span> | <span data-ttu-id="0d502-230">值</span><span class="sxs-lookup"><span data-stu-id="0d502-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0d502-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d502-231">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d502-232">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d502-233">System-Only</span></span>            | <span data-ttu-id="0d502-234">否</span><span class="sxs-lookup"><span data-stu-id="0d502-234">False</span></span>                                                                 |
| <span data-ttu-id="0d502-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d502-235">Is-Single-Valued</span></span>       | <span data-ttu-id="0d502-236">對</span><span class="sxs-lookup"><span data-stu-id="0d502-236">True</span></span>                                                                  |
| <span data-ttu-id="0d502-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d502-237">Is Indexed</span></span>             | <span data-ttu-id="0d502-238">否</span><span class="sxs-lookup"><span data-stu-id="0d502-238">False</span></span>                                                                 |
| <span data-ttu-id="0d502-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d502-239">In Global Catalog</span></span>      | <span data-ttu-id="0d502-240">否</span><span class="sxs-lookup"><span data-stu-id="0d502-240">False</span></span>                                                                 |
| <span data-ttu-id="0d502-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d502-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d502-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d502-242">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="0d502-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d502-243">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d502-244">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-245">Search-Flags</span></span>           | <span data-ttu-id="0d502-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d502-246">0x00000000</span></span>                                                            |
| <span data-ttu-id="0d502-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-247">System-Flags</span></span>           | <span data-ttu-id="0d502-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d502-248">0x00000010</span></span>                                                            |
| <span data-ttu-id="0d502-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d502-249">Classes used in</span></span>        | [<span data-ttu-id="0d502-250">**Group**</span><span class="sxs-lookup"><span data-stu-id="0d502-250">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="0d502-251">**User**</span><span class="sxs-lookup"><span data-stu-id="0d502-251">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0d502-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d502-252">Windows Server 2012</span></span>



| <span data-ttu-id="0d502-253">進入</span><span class="sxs-lookup"><span data-stu-id="0d502-253">Entry</span></span> | <span data-ttu-id="0d502-254">值</span><span class="sxs-lookup"><span data-stu-id="0d502-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0d502-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d502-255">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d502-256">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="0d502-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d502-257">System-Only</span></span>            | <span data-ttu-id="0d502-258">否</span><span class="sxs-lookup"><span data-stu-id="0d502-258">False</span></span>                                                                 |
| <span data-ttu-id="0d502-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d502-259">Is-Single-Valued</span></span>       | <span data-ttu-id="0d502-260">對</span><span class="sxs-lookup"><span data-stu-id="0d502-260">True</span></span>                                                                  |
| <span data-ttu-id="0d502-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d502-261">Is Indexed</span></span>             | <span data-ttu-id="0d502-262">否</span><span class="sxs-lookup"><span data-stu-id="0d502-262">False</span></span>                                                                 |
| <span data-ttu-id="0d502-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d502-263">In Global Catalog</span></span>      | <span data-ttu-id="0d502-264">否</span><span class="sxs-lookup"><span data-stu-id="0d502-264">False</span></span>                                                                 |
| <span data-ttu-id="0d502-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d502-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d502-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d502-266">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="0d502-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d502-267">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d502-268">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="0d502-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-269">Search-Flags</span></span>           | <span data-ttu-id="0d502-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d502-270">0x00000000</span></span>                                                            |
| <span data-ttu-id="0d502-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d502-271">System-Flags</span></span>           | <span data-ttu-id="0d502-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d502-272">0x00000010</span></span>                                                            |
| <span data-ttu-id="0d502-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d502-273">Classes used in</span></span>        | [<span data-ttu-id="0d502-274">**Group**</span><span class="sxs-lookup"><span data-stu-id="0d502-274">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="0d502-275">**User**</span><span class="sxs-lookup"><span data-stu-id="0d502-275">**User**</span></span>](c-user.md)<br/> |



 

 






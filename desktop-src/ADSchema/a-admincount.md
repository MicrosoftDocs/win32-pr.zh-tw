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
# <a name="admin-count-attribute"></a><span data-ttu-id="c0398-105">Admin-Count 屬性</span><span class="sxs-lookup"><span data-stu-id="c0398-105">Admin-Count attribute</span></span>

<span data-ttu-id="c0398-106">指出指定的物件已將其 Acl 變更為系統中較安全的值，因為它是直接或可轉移)  (其中一個系統管理群組的成員。</span><span class="sxs-lookup"><span data-stu-id="c0398-106">Indicates that a given object has had its ACLs changed to a more secure value by the system because it was a member of one of the administrative groups (directly or transitively).</span></span>



| <span data-ttu-id="c0398-107">進入</span><span class="sxs-lookup"><span data-stu-id="c0398-107">Entry</span></span> | <span data-ttu-id="c0398-108">值</span><span class="sxs-lookup"><span data-stu-id="c0398-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="c0398-109">CN</span><span class="sxs-lookup"><span data-stu-id="c0398-109">CN</span></span>                | <span data-ttu-id="c0398-110">Admin-Count</span><span class="sxs-lookup"><span data-stu-id="c0398-110">Admin-Count</span></span>                                         |
| <span data-ttu-id="c0398-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c0398-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c0398-112">adminCount</span><span class="sxs-lookup"><span data-stu-id="c0398-112">adminCount</span></span>                                          |
| <span data-ttu-id="c0398-113">大小</span><span class="sxs-lookup"><span data-stu-id="c0398-113">Size</span></span>              | <span data-ttu-id="c0398-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="c0398-114">4 bytes</span></span>                                             |
| <span data-ttu-id="c0398-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c0398-115">Update Privilege</span></span>  | <span data-ttu-id="c0398-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="c0398-116">This value is set by the system.</span></span>                    |
| <span data-ttu-id="c0398-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c0398-117">Update Frequency</span></span>  | <span data-ttu-id="c0398-118">當物件加入至系統管理群組時。</span><span class="sxs-lookup"><span data-stu-id="c0398-118">When an object is added to an administrative group.</span></span> |
| <span data-ttu-id="c0398-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c0398-119">Attribute-Id</span></span>      | <span data-ttu-id="c0398-120">1.2.840.113556.1.4.150</span><span class="sxs-lookup"><span data-stu-id="c0398-120">1.2.840.113556.1.4.150</span></span>                              |
| <span data-ttu-id="c0398-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c0398-121">System-Id-Guid</span></span>    | <span data-ttu-id="c0398-122">bf967918-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c0398-122">bf967918-0de6-11d0-a285-00aa003049e2</span></span>                |
| <span data-ttu-id="c0398-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0398-123">Syntax</span></span>            | [<span data-ttu-id="c0398-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="c0398-124">**Enumeration**</span></span>](s-enumeration.md)                |



## <a name="implementations"></a><span data-ttu-id="c0398-125">實作</span><span class="sxs-lookup"><span data-stu-id="c0398-125">Implementations</span></span>

-   [<span data-ttu-id="c0398-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c0398-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c0398-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c0398-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c0398-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c0398-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c0398-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c0398-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c0398-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c0398-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c0398-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c0398-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c0398-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c0398-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c0398-133">進入</span><span class="sxs-lookup"><span data-stu-id="c0398-133">Entry</span></span> | <span data-ttu-id="c0398-134">值</span><span class="sxs-lookup"><span data-stu-id="c0398-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c0398-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c0398-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0398-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0398-137">System-Only</span></span>            | <span data-ttu-id="c0398-138">否</span><span class="sxs-lookup"><span data-stu-id="c0398-138">False</span></span>                                                                 |
| <span data-ttu-id="c0398-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c0398-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c0398-140">對</span><span class="sxs-lookup"><span data-stu-id="c0398-140">True</span></span>                                                                  |
| <span data-ttu-id="c0398-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c0398-141">Is Indexed</span></span>             | <span data-ttu-id="c0398-142">否</span><span class="sxs-lookup"><span data-stu-id="c0398-142">False</span></span>                                                                 |
| <span data-ttu-id="c0398-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c0398-143">In Global Catalog</span></span>      | <span data-ttu-id="c0398-144">否</span><span class="sxs-lookup"><span data-stu-id="c0398-144">False</span></span>                                                                 |
| <span data-ttu-id="c0398-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c0398-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0398-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c0398-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c0398-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0398-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0398-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-149">Search-Flags</span></span>           | <span data-ttu-id="c0398-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0398-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="c0398-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-151">System-Flags</span></span>           | <span data-ttu-id="c0398-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0398-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="c0398-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c0398-153">Classes used in</span></span>        | [<span data-ttu-id="c0398-154">**Group**</span><span class="sxs-lookup"><span data-stu-id="c0398-154">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c0398-155">**User**</span><span class="sxs-lookup"><span data-stu-id="c0398-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c0398-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0398-156">Windows Server 2003</span></span>



| <span data-ttu-id="c0398-157">進入</span><span class="sxs-lookup"><span data-stu-id="c0398-157">Entry</span></span> | <span data-ttu-id="c0398-158">值</span><span class="sxs-lookup"><span data-stu-id="c0398-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c0398-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c0398-159">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0398-160">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0398-161">System-Only</span></span>            | <span data-ttu-id="c0398-162">否</span><span class="sxs-lookup"><span data-stu-id="c0398-162">False</span></span>                                                                 |
| <span data-ttu-id="c0398-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c0398-163">Is-Single-Valued</span></span>       | <span data-ttu-id="c0398-164">對</span><span class="sxs-lookup"><span data-stu-id="c0398-164">True</span></span>                                                                  |
| <span data-ttu-id="c0398-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c0398-165">Is Indexed</span></span>             | <span data-ttu-id="c0398-166">否</span><span class="sxs-lookup"><span data-stu-id="c0398-166">False</span></span>                                                                 |
| <span data-ttu-id="c0398-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c0398-167">In Global Catalog</span></span>      | <span data-ttu-id="c0398-168">否</span><span class="sxs-lookup"><span data-stu-id="c0398-168">False</span></span>                                                                 |
| <span data-ttu-id="c0398-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c0398-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0398-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c0398-170">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c0398-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0398-171">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0398-172">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-173">Search-Flags</span></span>           | <span data-ttu-id="c0398-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0398-174">0x00000000</span></span>                                                            |
| <span data-ttu-id="c0398-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-175">System-Flags</span></span>           | <span data-ttu-id="c0398-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0398-176">0x00000010</span></span>                                                            |
| <span data-ttu-id="c0398-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c0398-177">Classes used in</span></span>        | [<span data-ttu-id="c0398-178">**Group**</span><span class="sxs-lookup"><span data-stu-id="c0398-178">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c0398-179">**User**</span><span class="sxs-lookup"><span data-stu-id="c0398-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c0398-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c0398-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c0398-181">進入</span><span class="sxs-lookup"><span data-stu-id="c0398-181">Entry</span></span> | <span data-ttu-id="c0398-182">值</span><span class="sxs-lookup"><span data-stu-id="c0398-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c0398-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c0398-183">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0398-184">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0398-185">System-Only</span></span>            | <span data-ttu-id="c0398-186">否</span><span class="sxs-lookup"><span data-stu-id="c0398-186">False</span></span>                                                                 |
| <span data-ttu-id="c0398-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c0398-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c0398-188">對</span><span class="sxs-lookup"><span data-stu-id="c0398-188">True</span></span>                                                                  |
| <span data-ttu-id="c0398-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c0398-189">Is Indexed</span></span>             | <span data-ttu-id="c0398-190">否</span><span class="sxs-lookup"><span data-stu-id="c0398-190">False</span></span>                                                                 |
| <span data-ttu-id="c0398-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c0398-191">In Global Catalog</span></span>      | <span data-ttu-id="c0398-192">否</span><span class="sxs-lookup"><span data-stu-id="c0398-192">False</span></span>                                                                 |
| <span data-ttu-id="c0398-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c0398-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0398-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c0398-194">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c0398-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0398-195">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0398-196">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-197">Search-Flags</span></span>           | <span data-ttu-id="c0398-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0398-198">0x00000000</span></span>                                                            |
| <span data-ttu-id="c0398-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-199">System-Flags</span></span>           | <span data-ttu-id="c0398-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0398-200">0x00000010</span></span>                                                            |
| <span data-ttu-id="c0398-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c0398-201">Classes used in</span></span>        | [<span data-ttu-id="c0398-202">**Group**</span><span class="sxs-lookup"><span data-stu-id="c0398-202">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c0398-203">**User**</span><span class="sxs-lookup"><span data-stu-id="c0398-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c0398-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0398-204">Windows Server 2008</span></span>



| <span data-ttu-id="c0398-205">進入</span><span class="sxs-lookup"><span data-stu-id="c0398-205">Entry</span></span> | <span data-ttu-id="c0398-206">值</span><span class="sxs-lookup"><span data-stu-id="c0398-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c0398-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c0398-207">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0398-208">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0398-209">System-Only</span></span>            | <span data-ttu-id="c0398-210">否</span><span class="sxs-lookup"><span data-stu-id="c0398-210">False</span></span>                                                                 |
| <span data-ttu-id="c0398-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c0398-211">Is-Single-Valued</span></span>       | <span data-ttu-id="c0398-212">對</span><span class="sxs-lookup"><span data-stu-id="c0398-212">True</span></span>                                                                  |
| <span data-ttu-id="c0398-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c0398-213">Is Indexed</span></span>             | <span data-ttu-id="c0398-214">否</span><span class="sxs-lookup"><span data-stu-id="c0398-214">False</span></span>                                                                 |
| <span data-ttu-id="c0398-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c0398-215">In Global Catalog</span></span>      | <span data-ttu-id="c0398-216">否</span><span class="sxs-lookup"><span data-stu-id="c0398-216">False</span></span>                                                                 |
| <span data-ttu-id="c0398-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c0398-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0398-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c0398-218">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c0398-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0398-219">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0398-220">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-221">Search-Flags</span></span>           | <span data-ttu-id="c0398-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0398-222">0x00000000</span></span>                                                            |
| <span data-ttu-id="c0398-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-223">System-Flags</span></span>           | <span data-ttu-id="c0398-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0398-224">0x00000010</span></span>                                                            |
| <span data-ttu-id="c0398-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c0398-225">Classes used in</span></span>        | [<span data-ttu-id="c0398-226">**Group**</span><span class="sxs-lookup"><span data-stu-id="c0398-226">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c0398-227">**User**</span><span class="sxs-lookup"><span data-stu-id="c0398-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c0398-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c0398-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c0398-229">進入</span><span class="sxs-lookup"><span data-stu-id="c0398-229">Entry</span></span> | <span data-ttu-id="c0398-230">值</span><span class="sxs-lookup"><span data-stu-id="c0398-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c0398-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c0398-231">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0398-232">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0398-233">System-Only</span></span>            | <span data-ttu-id="c0398-234">否</span><span class="sxs-lookup"><span data-stu-id="c0398-234">False</span></span>                                                                 |
| <span data-ttu-id="c0398-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c0398-235">Is-Single-Valued</span></span>       | <span data-ttu-id="c0398-236">對</span><span class="sxs-lookup"><span data-stu-id="c0398-236">True</span></span>                                                                  |
| <span data-ttu-id="c0398-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c0398-237">Is Indexed</span></span>             | <span data-ttu-id="c0398-238">否</span><span class="sxs-lookup"><span data-stu-id="c0398-238">False</span></span>                                                                 |
| <span data-ttu-id="c0398-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c0398-239">In Global Catalog</span></span>      | <span data-ttu-id="c0398-240">否</span><span class="sxs-lookup"><span data-stu-id="c0398-240">False</span></span>                                                                 |
| <span data-ttu-id="c0398-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c0398-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0398-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c0398-242">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c0398-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0398-243">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0398-244">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-245">Search-Flags</span></span>           | <span data-ttu-id="c0398-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0398-246">0x00000000</span></span>                                                            |
| <span data-ttu-id="c0398-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-247">System-Flags</span></span>           | <span data-ttu-id="c0398-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0398-248">0x00000010</span></span>                                                            |
| <span data-ttu-id="c0398-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c0398-249">Classes used in</span></span>        | [<span data-ttu-id="c0398-250">**Group**</span><span class="sxs-lookup"><span data-stu-id="c0398-250">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c0398-251">**User**</span><span class="sxs-lookup"><span data-stu-id="c0398-251">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c0398-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0398-252">Windows Server 2012</span></span>



| <span data-ttu-id="c0398-253">進入</span><span class="sxs-lookup"><span data-stu-id="c0398-253">Entry</span></span> | <span data-ttu-id="c0398-254">值</span><span class="sxs-lookup"><span data-stu-id="c0398-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c0398-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c0398-255">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0398-256">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c0398-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0398-257">System-Only</span></span>            | <span data-ttu-id="c0398-258">否</span><span class="sxs-lookup"><span data-stu-id="c0398-258">False</span></span>                                                                 |
| <span data-ttu-id="c0398-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c0398-259">Is-Single-Valued</span></span>       | <span data-ttu-id="c0398-260">對</span><span class="sxs-lookup"><span data-stu-id="c0398-260">True</span></span>                                                                  |
| <span data-ttu-id="c0398-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c0398-261">Is Indexed</span></span>             | <span data-ttu-id="c0398-262">否</span><span class="sxs-lookup"><span data-stu-id="c0398-262">False</span></span>                                                                 |
| <span data-ttu-id="c0398-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c0398-263">In Global Catalog</span></span>      | <span data-ttu-id="c0398-264">否</span><span class="sxs-lookup"><span data-stu-id="c0398-264">False</span></span>                                                                 |
| <span data-ttu-id="c0398-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c0398-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0398-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c0398-266">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c0398-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0398-267">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0398-268">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c0398-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-269">Search-Flags</span></span>           | <span data-ttu-id="c0398-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0398-270">0x00000000</span></span>                                                            |
| <span data-ttu-id="c0398-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0398-271">System-Flags</span></span>           | <span data-ttu-id="c0398-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0398-272">0x00000010</span></span>                                                            |
| <span data-ttu-id="c0398-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c0398-273">Classes used in</span></span>        | [<span data-ttu-id="c0398-274">**Group**</span><span class="sxs-lookup"><span data-stu-id="c0398-274">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c0398-275">**User**</span><span class="sxs-lookup"><span data-stu-id="c0398-275">**User**</span></span>](c-user.md)<br/> |



 

 






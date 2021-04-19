---
title: Is-Deleted 屬性
description: 若為 TRUE，表示此物件已標示為要刪除，無法具現化。 在標記期間過期之後，系統就會將它從系統中移除。
ms.assetid: 549b5161-5d2f-47d7-8192-4480334ef13d
ms.tgt_platform: multiple
keywords:
- Is-Deleted 屬性 AD 架構
- isDeleted 屬性 AD 架構
topic_type:
- apiref
api_name:
- Is-Deleted
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b30dec5ed139da60853324b82cc6e0f55fcc70
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970467"
---
# <a name="is-deleted-attribute"></a><span data-ttu-id="b8106-106">Is-Deleted 屬性</span><span class="sxs-lookup"><span data-stu-id="b8106-106">Is-Deleted attribute</span></span>

<span data-ttu-id="b8106-107">若 **為 TRUE**，表示此物件已標示為要刪除，無法具現化。</span><span class="sxs-lookup"><span data-stu-id="b8106-107">If **TRUE**, this object has been marked for deletion and cannot be instantiated.</span></span> <span data-ttu-id="b8106-108">在標記期間過期之後，系統就會將它從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="b8106-108">After the tombstone period has expired, it will be removed from the system.</span></span>



| <span data-ttu-id="b8106-109">進入</span><span class="sxs-lookup"><span data-stu-id="b8106-109">Entry</span></span> | <span data-ttu-id="b8106-110">值</span><span class="sxs-lookup"><span data-stu-id="b8106-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b8106-111">CN</span><span class="sxs-lookup"><span data-stu-id="b8106-111">CN</span></span>                | <span data-ttu-id="b8106-112">Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="b8106-112">Is-Deleted</span></span>                           |
| <span data-ttu-id="b8106-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b8106-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b8106-114">isDeleted</span><span class="sxs-lookup"><span data-stu-id="b8106-114">isDeleted</span></span>                            |
| <span data-ttu-id="b8106-115">大小</span><span class="sxs-lookup"><span data-stu-id="b8106-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="b8106-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b8106-116">Update Privilege</span></span>  | <span data-ttu-id="b8106-117">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="b8106-117">Domain administrator</span></span>                 |
| <span data-ttu-id="b8106-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b8106-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b8106-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8106-119">Attribute-Id</span></span>      | <span data-ttu-id="b8106-120">1.2.840.113556.1.2.48</span><span class="sxs-lookup"><span data-stu-id="b8106-120">1.2.840.113556.1.2.48</span></span>                |
| <span data-ttu-id="b8106-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b8106-121">System-Id-Guid</span></span>    | <span data-ttu-id="b8106-122">bf96798f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b8106-122">bf96798f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b8106-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8106-123">Syntax</span></span>            | [<span data-ttu-id="b8106-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b8106-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="b8106-125">實作</span><span class="sxs-lookup"><span data-stu-id="b8106-125">Implementations</span></span>

-   [<span data-ttu-id="b8106-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8106-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8106-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8106-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8106-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b8106-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b8106-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8106-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8106-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8106-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8106-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8106-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8106-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8106-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8106-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8106-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b8106-134">進入</span><span class="sxs-lookup"><span data-stu-id="b8106-134">Entry</span></span> | <span data-ttu-id="b8106-135">值</span><span class="sxs-lookup"><span data-stu-id="b8106-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8106-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8106-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8106-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8106-137">MAPI-Id</span></span>                | <span data-ttu-id="b8106-138">0x80C0</span><span class="sxs-lookup"><span data-stu-id="b8106-138">0x80C0</span></span>                          |
| <span data-ttu-id="b8106-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8106-139">System-Only</span></span>            | <span data-ttu-id="b8106-140">對</span><span class="sxs-lookup"><span data-stu-id="b8106-140">True</span></span>                            |
| <span data-ttu-id="b8106-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8106-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b8106-142">對</span><span class="sxs-lookup"><span data-stu-id="b8106-142">True</span></span>                            |
| <span data-ttu-id="b8106-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8106-143">Is Indexed</span></span>             | <span data-ttu-id="b8106-144">否</span><span class="sxs-lookup"><span data-stu-id="b8106-144">False</span></span>                           |
| <span data-ttu-id="b8106-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8106-145">In Global Catalog</span></span>      | <span data-ttu-id="b8106-146">對</span><span class="sxs-lookup"><span data-stu-id="b8106-146">True</span></span>                            |
| <span data-ttu-id="b8106-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8106-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8106-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8106-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8106-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8106-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8106-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8106-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8106-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-151">Search-Flags</span></span>           | <span data-ttu-id="b8106-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8106-152">0x00000000</span></span>                      |
| <span data-ttu-id="b8106-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-153">System-Flags</span></span>           | <span data-ttu-id="b8106-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b8106-154">0x00000012</span></span>                      |
| <span data-ttu-id="b8106-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8106-155">Classes used in</span></span>        | [<span data-ttu-id="b8106-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b8106-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8106-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8106-157">Windows Server 2003</span></span>



| <span data-ttu-id="b8106-158">進入</span><span class="sxs-lookup"><span data-stu-id="b8106-158">Entry</span></span> | <span data-ttu-id="b8106-159">值</span><span class="sxs-lookup"><span data-stu-id="b8106-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8106-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8106-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8106-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8106-161">MAPI-Id</span></span>                | <span data-ttu-id="b8106-162">0x80C0</span><span class="sxs-lookup"><span data-stu-id="b8106-162">0x80C0</span></span>                          |
| <span data-ttu-id="b8106-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8106-163">System-Only</span></span>            | <span data-ttu-id="b8106-164">對</span><span class="sxs-lookup"><span data-stu-id="b8106-164">True</span></span>                            |
| <span data-ttu-id="b8106-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8106-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b8106-166">對</span><span class="sxs-lookup"><span data-stu-id="b8106-166">True</span></span>                            |
| <span data-ttu-id="b8106-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8106-167">Is Indexed</span></span>             | <span data-ttu-id="b8106-168">否</span><span class="sxs-lookup"><span data-stu-id="b8106-168">False</span></span>                           |
| <span data-ttu-id="b8106-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8106-169">In Global Catalog</span></span>      | <span data-ttu-id="b8106-170">對</span><span class="sxs-lookup"><span data-stu-id="b8106-170">True</span></span>                            |
| <span data-ttu-id="b8106-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8106-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8106-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8106-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8106-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8106-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8106-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8106-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8106-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-175">Search-Flags</span></span>           | <span data-ttu-id="b8106-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8106-176">0x00000000</span></span>                      |
| <span data-ttu-id="b8106-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-177">System-Flags</span></span>           | <span data-ttu-id="b8106-178">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b8106-178">0x00000012</span></span>                      |
| <span data-ttu-id="b8106-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8106-179">Classes used in</span></span>        | [<span data-ttu-id="b8106-180">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b8106-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b8106-181">亞當</span><span class="sxs-lookup"><span data-stu-id="b8106-181">ADAM</span></span>



| <span data-ttu-id="b8106-182">進入</span><span class="sxs-lookup"><span data-stu-id="b8106-182">Entry</span></span> | <span data-ttu-id="b8106-183">值</span><span class="sxs-lookup"><span data-stu-id="b8106-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8106-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8106-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8106-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8106-185">MAPI-Id</span></span>                | <span data-ttu-id="b8106-186">0x80C0</span><span class="sxs-lookup"><span data-stu-id="b8106-186">0x80C0</span></span>                          |
| <span data-ttu-id="b8106-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8106-187">System-Only</span></span>            | <span data-ttu-id="b8106-188">對</span><span class="sxs-lookup"><span data-stu-id="b8106-188">True</span></span>                            |
| <span data-ttu-id="b8106-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8106-189">Is-Single-Valued</span></span>       | <span data-ttu-id="b8106-190">對</span><span class="sxs-lookup"><span data-stu-id="b8106-190">True</span></span>                            |
| <span data-ttu-id="b8106-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8106-191">Is Indexed</span></span>             | <span data-ttu-id="b8106-192">否</span><span class="sxs-lookup"><span data-stu-id="b8106-192">False</span></span>                           |
| <span data-ttu-id="b8106-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8106-193">In Global Catalog</span></span>      | <span data-ttu-id="b8106-194">對</span><span class="sxs-lookup"><span data-stu-id="b8106-194">True</span></span>                            |
| <span data-ttu-id="b8106-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8106-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8106-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8106-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8106-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8106-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8106-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8106-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8106-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-199">Search-Flags</span></span>           | <span data-ttu-id="b8106-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8106-200">0x00000000</span></span>                      |
| <span data-ttu-id="b8106-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-201">System-Flags</span></span>           | <span data-ttu-id="b8106-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b8106-202">0x00000012</span></span>                      |
| <span data-ttu-id="b8106-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8106-203">Classes used in</span></span>        | [<span data-ttu-id="b8106-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b8106-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8106-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8106-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8106-206">進入</span><span class="sxs-lookup"><span data-stu-id="b8106-206">Entry</span></span> | <span data-ttu-id="b8106-207">值</span><span class="sxs-lookup"><span data-stu-id="b8106-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8106-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8106-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8106-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8106-209">MAPI-Id</span></span>                | <span data-ttu-id="b8106-210">0x80C0</span><span class="sxs-lookup"><span data-stu-id="b8106-210">0x80C0</span></span>                          |
| <span data-ttu-id="b8106-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8106-211">System-Only</span></span>            | <span data-ttu-id="b8106-212">對</span><span class="sxs-lookup"><span data-stu-id="b8106-212">True</span></span>                            |
| <span data-ttu-id="b8106-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8106-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b8106-214">對</span><span class="sxs-lookup"><span data-stu-id="b8106-214">True</span></span>                            |
| <span data-ttu-id="b8106-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8106-215">Is Indexed</span></span>             | <span data-ttu-id="b8106-216">否</span><span class="sxs-lookup"><span data-stu-id="b8106-216">False</span></span>                           |
| <span data-ttu-id="b8106-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8106-217">In Global Catalog</span></span>      | <span data-ttu-id="b8106-218">對</span><span class="sxs-lookup"><span data-stu-id="b8106-218">True</span></span>                            |
| <span data-ttu-id="b8106-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8106-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8106-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8106-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8106-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8106-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8106-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8106-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8106-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-223">Search-Flags</span></span>           | <span data-ttu-id="b8106-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8106-224">0x00000000</span></span>                      |
| <span data-ttu-id="b8106-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-225">System-Flags</span></span>           | <span data-ttu-id="b8106-226">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b8106-226">0x00000012</span></span>                      |
| <span data-ttu-id="b8106-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8106-227">Classes used in</span></span>        | [<span data-ttu-id="b8106-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b8106-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8106-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8106-229">Windows Server 2008</span></span>



| <span data-ttu-id="b8106-230">進入</span><span class="sxs-lookup"><span data-stu-id="b8106-230">Entry</span></span> | <span data-ttu-id="b8106-231">值</span><span class="sxs-lookup"><span data-stu-id="b8106-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8106-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8106-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8106-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8106-233">MAPI-Id</span></span>                | <span data-ttu-id="b8106-234">0x80C0</span><span class="sxs-lookup"><span data-stu-id="b8106-234">0x80C0</span></span>                          |
| <span data-ttu-id="b8106-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8106-235">System-Only</span></span>            | <span data-ttu-id="b8106-236">對</span><span class="sxs-lookup"><span data-stu-id="b8106-236">True</span></span>                            |
| <span data-ttu-id="b8106-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8106-237">Is-Single-Valued</span></span>       | <span data-ttu-id="b8106-238">對</span><span class="sxs-lookup"><span data-stu-id="b8106-238">True</span></span>                            |
| <span data-ttu-id="b8106-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8106-239">Is Indexed</span></span>             | <span data-ttu-id="b8106-240">否</span><span class="sxs-lookup"><span data-stu-id="b8106-240">False</span></span>                           |
| <span data-ttu-id="b8106-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8106-241">In Global Catalog</span></span>      | <span data-ttu-id="b8106-242">對</span><span class="sxs-lookup"><span data-stu-id="b8106-242">True</span></span>                            |
| <span data-ttu-id="b8106-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8106-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8106-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8106-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8106-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8106-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8106-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8106-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8106-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-247">Search-Flags</span></span>           | <span data-ttu-id="b8106-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8106-248">0x00000000</span></span>                      |
| <span data-ttu-id="b8106-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-249">System-Flags</span></span>           | <span data-ttu-id="b8106-250">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b8106-250">0x00000012</span></span>                      |
| <span data-ttu-id="b8106-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8106-251">Classes used in</span></span>        | [<span data-ttu-id="b8106-252">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b8106-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8106-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8106-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8106-254">進入</span><span class="sxs-lookup"><span data-stu-id="b8106-254">Entry</span></span> | <span data-ttu-id="b8106-255">值</span><span class="sxs-lookup"><span data-stu-id="b8106-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8106-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8106-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8106-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8106-257">MAPI-Id</span></span>                | <span data-ttu-id="b8106-258">0x80C0</span><span class="sxs-lookup"><span data-stu-id="b8106-258">0x80C0</span></span>                          |
| <span data-ttu-id="b8106-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8106-259">System-Only</span></span>            | <span data-ttu-id="b8106-260">對</span><span class="sxs-lookup"><span data-stu-id="b8106-260">True</span></span>                            |
| <span data-ttu-id="b8106-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8106-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b8106-262">對</span><span class="sxs-lookup"><span data-stu-id="b8106-262">True</span></span>                            |
| <span data-ttu-id="b8106-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8106-263">Is Indexed</span></span>             | <span data-ttu-id="b8106-264">否</span><span class="sxs-lookup"><span data-stu-id="b8106-264">False</span></span>                           |
| <span data-ttu-id="b8106-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8106-265">In Global Catalog</span></span>      | <span data-ttu-id="b8106-266">對</span><span class="sxs-lookup"><span data-stu-id="b8106-266">True</span></span>                            |
| <span data-ttu-id="b8106-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8106-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8106-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8106-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8106-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8106-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8106-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8106-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8106-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-271">Search-Flags</span></span>           | <span data-ttu-id="b8106-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8106-272">0x00000000</span></span>                      |
| <span data-ttu-id="b8106-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-273">System-Flags</span></span>           | <span data-ttu-id="b8106-274">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b8106-274">0x00000012</span></span>                      |
| <span data-ttu-id="b8106-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8106-275">Classes used in</span></span>        | [<span data-ttu-id="b8106-276">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b8106-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8106-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8106-277">Windows Server 2012</span></span>



| <span data-ttu-id="b8106-278">進入</span><span class="sxs-lookup"><span data-stu-id="b8106-278">Entry</span></span> | <span data-ttu-id="b8106-279">值</span><span class="sxs-lookup"><span data-stu-id="b8106-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8106-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8106-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8106-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8106-281">MAPI-Id</span></span>                | <span data-ttu-id="b8106-282">0x80C0</span><span class="sxs-lookup"><span data-stu-id="b8106-282">0x80C0</span></span>                          |
| <span data-ttu-id="b8106-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8106-283">System-Only</span></span>            | <span data-ttu-id="b8106-284">對</span><span class="sxs-lookup"><span data-stu-id="b8106-284">True</span></span>                            |
| <span data-ttu-id="b8106-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8106-285">Is-Single-Valued</span></span>       | <span data-ttu-id="b8106-286">對</span><span class="sxs-lookup"><span data-stu-id="b8106-286">True</span></span>                            |
| <span data-ttu-id="b8106-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8106-287">Is Indexed</span></span>             | <span data-ttu-id="b8106-288">否</span><span class="sxs-lookup"><span data-stu-id="b8106-288">False</span></span>                           |
| <span data-ttu-id="b8106-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8106-289">In Global Catalog</span></span>      | <span data-ttu-id="b8106-290">對</span><span class="sxs-lookup"><span data-stu-id="b8106-290">True</span></span>                            |
| <span data-ttu-id="b8106-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8106-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8106-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8106-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8106-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8106-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8106-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8106-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8106-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-295">Search-Flags</span></span>           | <span data-ttu-id="b8106-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8106-296">0x00000000</span></span>                      |
| <span data-ttu-id="b8106-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8106-297">System-Flags</span></span>           | <span data-ttu-id="b8106-298">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b8106-298">0x00000012</span></span>                      |
| <span data-ttu-id="b8106-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8106-299">Classes used in</span></span>        | [<span data-ttu-id="b8106-300">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b8106-300">**Top**</span></span>](c-top.md)<br/> |



 

 






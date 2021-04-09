---
title: 權杖群組-無 GC-可接受的屬性
description: 由於指定使用者或電腦上的可轉移群組成員資格擴充作業，此屬性包含 Sid 的清單。 如果沒有通用類別目錄可以取出可轉移的反向成員資格，則無法抓取權杖群組。
ms.assetid: 08718c69-6339-40dc-8486-a7cd72028ed1
ms.tgt_platform: multiple
keywords:
- 權杖群組-無 GC-可接受的屬性 AD 架構
- tokenGroupsNoGCAcceptable 屬性 AD 架構
topic_type:
- apiref
api_name:
- Token-Groups-No-GC-Acceptable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87c4b8996586c8c35ed4c815b954dad02b5db03
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844903"
---
# <a name="token-groups-no-gc-acceptable-attribute"></a><span data-ttu-id="b978f-106">權杖群組-無 GC-可接受的屬性</span><span class="sxs-lookup"><span data-stu-id="b978f-106">Token-Groups-No-GC-Acceptable attribute</span></span>

<span data-ttu-id="b978f-107">由於指定使用者或電腦上的可轉移群組成員資格擴充作業，此屬性包含 Sid 的清單。</span><span class="sxs-lookup"><span data-stu-id="b978f-107">This attribute contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="b978f-108">如果沒有通用類別目錄可以取出可轉移的反向成員資格，則無法抓取權杖群組。</span><span class="sxs-lookup"><span data-stu-id="b978f-108">Token groups cannot be retrieved if a Global Catalog is not present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="b978f-109">進入</span><span class="sxs-lookup"><span data-stu-id="b978f-109">Entry</span></span> | <span data-ttu-id="b978f-110">值</span><span class="sxs-lookup"><span data-stu-id="b978f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b978f-111">CN</span><span class="sxs-lookup"><span data-stu-id="b978f-111">CN</span></span>                | <span data-ttu-id="b978f-112">權杖群組-無-GC-可接受</span><span class="sxs-lookup"><span data-stu-id="b978f-112">Token-Groups-No-GC-Acceptable</span></span>        |
| <span data-ttu-id="b978f-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b978f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b978f-114">tokenGroupsNoGCAcceptable</span><span class="sxs-lookup"><span data-stu-id="b978f-114">tokenGroupsNoGCAcceptable</span></span>            |
| <span data-ttu-id="b978f-115">大小</span><span class="sxs-lookup"><span data-stu-id="b978f-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="b978f-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b978f-116">Update Privilege</span></span>  | <span data-ttu-id="b978f-117">系統會設定此值。</span><span class="sxs-lookup"><span data-stu-id="b978f-117">The system sets this value.</span></span>          |
| <span data-ttu-id="b978f-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b978f-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b978f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b978f-119">Attribute-Id</span></span>      | <span data-ttu-id="b978f-120">1.2.840.113556.1.4.1303</span><span class="sxs-lookup"><span data-stu-id="b978f-120">1.2.840.113556.1.4.1303</span></span>              |
| <span data-ttu-id="b978f-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b978f-121">System-Id-Guid</span></span>    | <span data-ttu-id="b978f-122">040fc392-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="b978f-122">040fc392-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="b978f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b978f-123">Syntax</span></span>            | [<span data-ttu-id="b978f-124">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="b978f-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="b978f-125">實作</span><span class="sxs-lookup"><span data-stu-id="b978f-125">Implementations</span></span>

-   [<span data-ttu-id="b978f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b978f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b978f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b978f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b978f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b978f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b978f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b978f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b978f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b978f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b978f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b978f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b978f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b978f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b978f-133">進入</span><span class="sxs-lookup"><span data-stu-id="b978f-133">Entry</span></span> | <span data-ttu-id="b978f-134">值</span><span class="sxs-lookup"><span data-stu-id="b978f-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b978f-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b978f-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b978f-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b978f-137">System-Only</span></span>            | <span data-ttu-id="b978f-138">否</span><span class="sxs-lookup"><span data-stu-id="b978f-138">False</span></span>                                                        |
| <span data-ttu-id="b978f-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b978f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b978f-140">否</span><span class="sxs-lookup"><span data-stu-id="b978f-140">False</span></span>                                                        |
| <span data-ttu-id="b978f-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b978f-141">Is Indexed</span></span>             | <span data-ttu-id="b978f-142">否</span><span class="sxs-lookup"><span data-stu-id="b978f-142">False</span></span>                                                        |
| <span data-ttu-id="b978f-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b978f-143">In Global Catalog</span></span>      | <span data-ttu-id="b978f-144">否</span><span class="sxs-lookup"><span data-stu-id="b978f-144">False</span></span>                                                        |
| <span data-ttu-id="b978f-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b978f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b978f-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b978f-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b978f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b978f-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b978f-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-149">Search-Flags</span></span>           | <span data-ttu-id="b978f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b978f-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="b978f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-151">System-Flags</span></span>           | <span data-ttu-id="b978f-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b978f-152">0x08000014</span></span>                                                   |
| <span data-ttu-id="b978f-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b978f-153">Classes used in</span></span>        | [<span data-ttu-id="b978f-154">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="b978f-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b978f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b978f-155">Windows Server 2003</span></span>



| <span data-ttu-id="b978f-156">進入</span><span class="sxs-lookup"><span data-stu-id="b978f-156">Entry</span></span> | <span data-ttu-id="b978f-157">值</span><span class="sxs-lookup"><span data-stu-id="b978f-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b978f-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b978f-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b978f-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b978f-160">System-Only</span></span>            | <span data-ttu-id="b978f-161">否</span><span class="sxs-lookup"><span data-stu-id="b978f-161">False</span></span>                                                        |
| <span data-ttu-id="b978f-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b978f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b978f-163">否</span><span class="sxs-lookup"><span data-stu-id="b978f-163">False</span></span>                                                        |
| <span data-ttu-id="b978f-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b978f-164">Is Indexed</span></span>             | <span data-ttu-id="b978f-165">否</span><span class="sxs-lookup"><span data-stu-id="b978f-165">False</span></span>                                                        |
| <span data-ttu-id="b978f-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b978f-166">In Global Catalog</span></span>      | <span data-ttu-id="b978f-167">否</span><span class="sxs-lookup"><span data-stu-id="b978f-167">False</span></span>                                                        |
| <span data-ttu-id="b978f-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b978f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b978f-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b978f-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b978f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b978f-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b978f-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-172">Search-Flags</span></span>           | <span data-ttu-id="b978f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b978f-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="b978f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-174">System-Flags</span></span>           | <span data-ttu-id="b978f-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b978f-175">0x08000014</span></span>                                                   |
| <span data-ttu-id="b978f-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b978f-176">Classes used in</span></span>        | [<span data-ttu-id="b978f-177">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="b978f-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b978f-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b978f-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b978f-179">進入</span><span class="sxs-lookup"><span data-stu-id="b978f-179">Entry</span></span> | <span data-ttu-id="b978f-180">值</span><span class="sxs-lookup"><span data-stu-id="b978f-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b978f-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b978f-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b978f-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b978f-183">System-Only</span></span>            | <span data-ttu-id="b978f-184">否</span><span class="sxs-lookup"><span data-stu-id="b978f-184">False</span></span>                                                        |
| <span data-ttu-id="b978f-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b978f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b978f-186">否</span><span class="sxs-lookup"><span data-stu-id="b978f-186">False</span></span>                                                        |
| <span data-ttu-id="b978f-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b978f-187">Is Indexed</span></span>             | <span data-ttu-id="b978f-188">否</span><span class="sxs-lookup"><span data-stu-id="b978f-188">False</span></span>                                                        |
| <span data-ttu-id="b978f-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b978f-189">In Global Catalog</span></span>      | <span data-ttu-id="b978f-190">否</span><span class="sxs-lookup"><span data-stu-id="b978f-190">False</span></span>                                                        |
| <span data-ttu-id="b978f-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b978f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b978f-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b978f-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b978f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b978f-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b978f-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-195">Search-Flags</span></span>           | <span data-ttu-id="b978f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b978f-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="b978f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-197">System-Flags</span></span>           | <span data-ttu-id="b978f-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b978f-198">0x08000014</span></span>                                                   |
| <span data-ttu-id="b978f-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b978f-199">Classes used in</span></span>        | [<span data-ttu-id="b978f-200">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="b978f-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b978f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b978f-201">Windows Server 2008</span></span>



| <span data-ttu-id="b978f-202">進入</span><span class="sxs-lookup"><span data-stu-id="b978f-202">Entry</span></span> | <span data-ttu-id="b978f-203">值</span><span class="sxs-lookup"><span data-stu-id="b978f-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b978f-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b978f-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b978f-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b978f-206">System-Only</span></span>            | <span data-ttu-id="b978f-207">否</span><span class="sxs-lookup"><span data-stu-id="b978f-207">False</span></span>                                                        |
| <span data-ttu-id="b978f-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b978f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b978f-209">否</span><span class="sxs-lookup"><span data-stu-id="b978f-209">False</span></span>                                                        |
| <span data-ttu-id="b978f-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b978f-210">Is Indexed</span></span>             | <span data-ttu-id="b978f-211">否</span><span class="sxs-lookup"><span data-stu-id="b978f-211">False</span></span>                                                        |
| <span data-ttu-id="b978f-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b978f-212">In Global Catalog</span></span>      | <span data-ttu-id="b978f-213">否</span><span class="sxs-lookup"><span data-stu-id="b978f-213">False</span></span>                                                        |
| <span data-ttu-id="b978f-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b978f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b978f-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b978f-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b978f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b978f-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b978f-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-218">Search-Flags</span></span>           | <span data-ttu-id="b978f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b978f-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="b978f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-220">System-Flags</span></span>           | <span data-ttu-id="b978f-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b978f-221">0x08000014</span></span>                                                   |
| <span data-ttu-id="b978f-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b978f-222">Classes used in</span></span>        | [<span data-ttu-id="b978f-223">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="b978f-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b978f-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b978f-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b978f-225">進入</span><span class="sxs-lookup"><span data-stu-id="b978f-225">Entry</span></span> | <span data-ttu-id="b978f-226">值</span><span class="sxs-lookup"><span data-stu-id="b978f-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b978f-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b978f-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b978f-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b978f-229">System-Only</span></span>            | <span data-ttu-id="b978f-230">否</span><span class="sxs-lookup"><span data-stu-id="b978f-230">False</span></span>                                                        |
| <span data-ttu-id="b978f-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b978f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b978f-232">否</span><span class="sxs-lookup"><span data-stu-id="b978f-232">False</span></span>                                                        |
| <span data-ttu-id="b978f-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b978f-233">Is Indexed</span></span>             | <span data-ttu-id="b978f-234">否</span><span class="sxs-lookup"><span data-stu-id="b978f-234">False</span></span>                                                        |
| <span data-ttu-id="b978f-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b978f-235">In Global Catalog</span></span>      | <span data-ttu-id="b978f-236">否</span><span class="sxs-lookup"><span data-stu-id="b978f-236">False</span></span>                                                        |
| <span data-ttu-id="b978f-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b978f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b978f-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b978f-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b978f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b978f-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b978f-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-241">Search-Flags</span></span>           | <span data-ttu-id="b978f-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b978f-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="b978f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-243">System-Flags</span></span>           | <span data-ttu-id="b978f-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b978f-244">0x08000014</span></span>                                                   |
| <span data-ttu-id="b978f-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b978f-245">Classes used in</span></span>        | [<span data-ttu-id="b978f-246">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="b978f-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b978f-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b978f-247">Windows Server 2012</span></span>



| <span data-ttu-id="b978f-248">進入</span><span class="sxs-lookup"><span data-stu-id="b978f-248">Entry</span></span> | <span data-ttu-id="b978f-249">值</span><span class="sxs-lookup"><span data-stu-id="b978f-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b978f-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b978f-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b978f-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b978f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b978f-252">System-Only</span></span>            | <span data-ttu-id="b978f-253">否</span><span class="sxs-lookup"><span data-stu-id="b978f-253">False</span></span>                                                        |
| <span data-ttu-id="b978f-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b978f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b978f-255">否</span><span class="sxs-lookup"><span data-stu-id="b978f-255">False</span></span>                                                        |
| <span data-ttu-id="b978f-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b978f-256">Is Indexed</span></span>             | <span data-ttu-id="b978f-257">否</span><span class="sxs-lookup"><span data-stu-id="b978f-257">False</span></span>                                                        |
| <span data-ttu-id="b978f-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b978f-258">In Global Catalog</span></span>      | <span data-ttu-id="b978f-259">否</span><span class="sxs-lookup"><span data-stu-id="b978f-259">False</span></span>                                                        |
| <span data-ttu-id="b978f-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b978f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b978f-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b978f-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b978f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b978f-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b978f-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b978f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-264">Search-Flags</span></span>           | <span data-ttu-id="b978f-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b978f-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="b978f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b978f-266">System-Flags</span></span>           | <span data-ttu-id="b978f-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b978f-267">0x08000014</span></span>                                                   |
| <span data-ttu-id="b978f-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b978f-268">Classes used in</span></span>        | [<span data-ttu-id="b978f-269">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="b978f-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 






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
# <a name="token-groups-no-gc-acceptable-attribute"></a><span data-ttu-id="df7ed-106">權杖群組-無 GC-可接受的屬性</span><span class="sxs-lookup"><span data-stu-id="df7ed-106">Token-Groups-No-GC-Acceptable attribute</span></span>

<span data-ttu-id="df7ed-107">由於指定使用者或電腦上的可轉移群組成員資格擴充作業，此屬性包含 Sid 的清單。</span><span class="sxs-lookup"><span data-stu-id="df7ed-107">This attribute contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="df7ed-108">如果沒有通用類別目錄可以取出可轉移的反向成員資格，則無法抓取權杖群組。</span><span class="sxs-lookup"><span data-stu-id="df7ed-108">Token groups cannot be retrieved if a Global Catalog is not present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="df7ed-109">進入</span><span class="sxs-lookup"><span data-stu-id="df7ed-109">Entry</span></span> | <span data-ttu-id="df7ed-110">值</span><span class="sxs-lookup"><span data-stu-id="df7ed-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="df7ed-111">CN</span><span class="sxs-lookup"><span data-stu-id="df7ed-111">CN</span></span>                | <span data-ttu-id="df7ed-112">權杖群組-無-GC-可接受</span><span class="sxs-lookup"><span data-stu-id="df7ed-112">Token-Groups-No-GC-Acceptable</span></span>        |
| <span data-ttu-id="df7ed-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="df7ed-113">Ldap-Display-Name</span></span> | <span data-ttu-id="df7ed-114">tokenGroupsNoGCAcceptable</span><span class="sxs-lookup"><span data-stu-id="df7ed-114">tokenGroupsNoGCAcceptable</span></span>            |
| <span data-ttu-id="df7ed-115">大小</span><span class="sxs-lookup"><span data-stu-id="df7ed-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="df7ed-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="df7ed-116">Update Privilege</span></span>  | <span data-ttu-id="df7ed-117">系統會設定此值。</span><span class="sxs-lookup"><span data-stu-id="df7ed-117">The system sets this value.</span></span>          |
| <span data-ttu-id="df7ed-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="df7ed-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="df7ed-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df7ed-119">Attribute-Id</span></span>      | <span data-ttu-id="df7ed-120">1.2.840.113556.1.4.1303</span><span class="sxs-lookup"><span data-stu-id="df7ed-120">1.2.840.113556.1.4.1303</span></span>              |
| <span data-ttu-id="df7ed-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="df7ed-121">System-Id-Guid</span></span>    | <span data-ttu-id="df7ed-122">040fc392-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="df7ed-122">040fc392-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="df7ed-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="df7ed-123">Syntax</span></span>            | [<span data-ttu-id="df7ed-124">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="df7ed-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="df7ed-125">實作</span><span class="sxs-lookup"><span data-stu-id="df7ed-125">Implementations</span></span>

-   [<span data-ttu-id="df7ed-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="df7ed-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="df7ed-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df7ed-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df7ed-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df7ed-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df7ed-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df7ed-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df7ed-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df7ed-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df7ed-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df7ed-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="df7ed-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df7ed-132">Windows 2000 Server</span></span>



| <span data-ttu-id="df7ed-133">進入</span><span class="sxs-lookup"><span data-stu-id="df7ed-133">Entry</span></span> | <span data-ttu-id="df7ed-134">值</span><span class="sxs-lookup"><span data-stu-id="df7ed-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df7ed-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df7ed-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df7ed-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="df7ed-137">System-Only</span></span>            | <span data-ttu-id="df7ed-138">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-138">False</span></span>                                                        |
| <span data-ttu-id="df7ed-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df7ed-139">Is-Single-Valued</span></span>       | <span data-ttu-id="df7ed-140">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-140">False</span></span>                                                        |
| <span data-ttu-id="df7ed-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df7ed-141">Is Indexed</span></span>             | <span data-ttu-id="df7ed-142">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-142">False</span></span>                                                        |
| <span data-ttu-id="df7ed-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df7ed-143">In Global Catalog</span></span>      | <span data-ttu-id="df7ed-144">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-144">False</span></span>                                                        |
| <span data-ttu-id="df7ed-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df7ed-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="df7ed-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df7ed-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df7ed-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df7ed-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df7ed-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-149">Search-Flags</span></span>           | <span data-ttu-id="df7ed-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df7ed-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="df7ed-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-151">System-Flags</span></span>           | <span data-ttu-id="df7ed-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="df7ed-152">0x08000014</span></span>                                                   |
| <span data-ttu-id="df7ed-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df7ed-153">Classes used in</span></span>        | [<span data-ttu-id="df7ed-154">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="df7ed-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="df7ed-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df7ed-155">Windows Server 2003</span></span>



| <span data-ttu-id="df7ed-156">進入</span><span class="sxs-lookup"><span data-stu-id="df7ed-156">Entry</span></span> | <span data-ttu-id="df7ed-157">值</span><span class="sxs-lookup"><span data-stu-id="df7ed-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df7ed-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df7ed-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df7ed-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="df7ed-160">System-Only</span></span>            | <span data-ttu-id="df7ed-161">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-161">False</span></span>                                                        |
| <span data-ttu-id="df7ed-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df7ed-162">Is-Single-Valued</span></span>       | <span data-ttu-id="df7ed-163">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-163">False</span></span>                                                        |
| <span data-ttu-id="df7ed-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df7ed-164">Is Indexed</span></span>             | <span data-ttu-id="df7ed-165">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-165">False</span></span>                                                        |
| <span data-ttu-id="df7ed-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df7ed-166">In Global Catalog</span></span>      | <span data-ttu-id="df7ed-167">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-167">False</span></span>                                                        |
| <span data-ttu-id="df7ed-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df7ed-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="df7ed-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df7ed-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df7ed-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df7ed-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df7ed-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-172">Search-Flags</span></span>           | <span data-ttu-id="df7ed-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df7ed-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="df7ed-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-174">System-Flags</span></span>           | <span data-ttu-id="df7ed-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="df7ed-175">0x08000014</span></span>                                                   |
| <span data-ttu-id="df7ed-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df7ed-176">Classes used in</span></span>        | [<span data-ttu-id="df7ed-177">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="df7ed-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df7ed-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df7ed-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df7ed-179">進入</span><span class="sxs-lookup"><span data-stu-id="df7ed-179">Entry</span></span> | <span data-ttu-id="df7ed-180">值</span><span class="sxs-lookup"><span data-stu-id="df7ed-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df7ed-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df7ed-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df7ed-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="df7ed-183">System-Only</span></span>            | <span data-ttu-id="df7ed-184">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-184">False</span></span>                                                        |
| <span data-ttu-id="df7ed-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df7ed-185">Is-Single-Valued</span></span>       | <span data-ttu-id="df7ed-186">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-186">False</span></span>                                                        |
| <span data-ttu-id="df7ed-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df7ed-187">Is Indexed</span></span>             | <span data-ttu-id="df7ed-188">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-188">False</span></span>                                                        |
| <span data-ttu-id="df7ed-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df7ed-189">In Global Catalog</span></span>      | <span data-ttu-id="df7ed-190">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-190">False</span></span>                                                        |
| <span data-ttu-id="df7ed-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df7ed-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="df7ed-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df7ed-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df7ed-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df7ed-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df7ed-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-195">Search-Flags</span></span>           | <span data-ttu-id="df7ed-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df7ed-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="df7ed-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-197">System-Flags</span></span>           | <span data-ttu-id="df7ed-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="df7ed-198">0x08000014</span></span>                                                   |
| <span data-ttu-id="df7ed-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df7ed-199">Classes used in</span></span>        | [<span data-ttu-id="df7ed-200">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="df7ed-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df7ed-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df7ed-201">Windows Server 2008</span></span>



| <span data-ttu-id="df7ed-202">進入</span><span class="sxs-lookup"><span data-stu-id="df7ed-202">Entry</span></span> | <span data-ttu-id="df7ed-203">值</span><span class="sxs-lookup"><span data-stu-id="df7ed-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df7ed-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df7ed-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df7ed-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="df7ed-206">System-Only</span></span>            | <span data-ttu-id="df7ed-207">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-207">False</span></span>                                                        |
| <span data-ttu-id="df7ed-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df7ed-208">Is-Single-Valued</span></span>       | <span data-ttu-id="df7ed-209">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-209">False</span></span>                                                        |
| <span data-ttu-id="df7ed-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df7ed-210">Is Indexed</span></span>             | <span data-ttu-id="df7ed-211">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-211">False</span></span>                                                        |
| <span data-ttu-id="df7ed-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df7ed-212">In Global Catalog</span></span>      | <span data-ttu-id="df7ed-213">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-213">False</span></span>                                                        |
| <span data-ttu-id="df7ed-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df7ed-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="df7ed-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df7ed-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df7ed-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df7ed-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df7ed-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-218">Search-Flags</span></span>           | <span data-ttu-id="df7ed-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df7ed-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="df7ed-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-220">System-Flags</span></span>           | <span data-ttu-id="df7ed-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="df7ed-221">0x08000014</span></span>                                                   |
| <span data-ttu-id="df7ed-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df7ed-222">Classes used in</span></span>        | [<span data-ttu-id="df7ed-223">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="df7ed-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df7ed-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df7ed-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df7ed-225">進入</span><span class="sxs-lookup"><span data-stu-id="df7ed-225">Entry</span></span> | <span data-ttu-id="df7ed-226">值</span><span class="sxs-lookup"><span data-stu-id="df7ed-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df7ed-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df7ed-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df7ed-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="df7ed-229">System-Only</span></span>            | <span data-ttu-id="df7ed-230">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-230">False</span></span>                                                        |
| <span data-ttu-id="df7ed-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df7ed-231">Is-Single-Valued</span></span>       | <span data-ttu-id="df7ed-232">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-232">False</span></span>                                                        |
| <span data-ttu-id="df7ed-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df7ed-233">Is Indexed</span></span>             | <span data-ttu-id="df7ed-234">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-234">False</span></span>                                                        |
| <span data-ttu-id="df7ed-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df7ed-235">In Global Catalog</span></span>      | <span data-ttu-id="df7ed-236">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-236">False</span></span>                                                        |
| <span data-ttu-id="df7ed-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df7ed-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="df7ed-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df7ed-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df7ed-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df7ed-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df7ed-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-241">Search-Flags</span></span>           | <span data-ttu-id="df7ed-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df7ed-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="df7ed-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-243">System-Flags</span></span>           | <span data-ttu-id="df7ed-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="df7ed-244">0x08000014</span></span>                                                   |
| <span data-ttu-id="df7ed-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df7ed-245">Classes used in</span></span>        | [<span data-ttu-id="df7ed-246">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="df7ed-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df7ed-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df7ed-247">Windows Server 2012</span></span>



| <span data-ttu-id="df7ed-248">進入</span><span class="sxs-lookup"><span data-stu-id="df7ed-248">Entry</span></span> | <span data-ttu-id="df7ed-249">值</span><span class="sxs-lookup"><span data-stu-id="df7ed-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="df7ed-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df7ed-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df7ed-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="df7ed-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="df7ed-252">System-Only</span></span>            | <span data-ttu-id="df7ed-253">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-253">False</span></span>                                                        |
| <span data-ttu-id="df7ed-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df7ed-254">Is-Single-Valued</span></span>       | <span data-ttu-id="df7ed-255">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-255">False</span></span>                                                        |
| <span data-ttu-id="df7ed-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df7ed-256">Is Indexed</span></span>             | <span data-ttu-id="df7ed-257">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-257">False</span></span>                                                        |
| <span data-ttu-id="df7ed-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df7ed-258">In Global Catalog</span></span>      | <span data-ttu-id="df7ed-259">否</span><span class="sxs-lookup"><span data-stu-id="df7ed-259">False</span></span>                                                        |
| <span data-ttu-id="df7ed-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df7ed-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="df7ed-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df7ed-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="df7ed-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df7ed-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df7ed-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="df7ed-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-264">Search-Flags</span></span>           | <span data-ttu-id="df7ed-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df7ed-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="df7ed-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df7ed-266">System-Flags</span></span>           | <span data-ttu-id="df7ed-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="df7ed-267">0x08000014</span></span>                                                   |
| <span data-ttu-id="df7ed-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df7ed-268">Classes used in</span></span>        | [<span data-ttu-id="df7ed-269">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="df7ed-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 






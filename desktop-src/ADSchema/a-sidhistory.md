---
title: SID-History 屬性
description: 如果物件是從另一個網域移出，則包含用於物件的先前 Sid。
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- SID-History 屬性 AD 架構
- sIDHistory 屬性 AD 架構
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467241"
---
# <a name="sid-history-attribute"></a><span data-ttu-id="d2199-105">SID-History 屬性</span><span class="sxs-lookup"><span data-stu-id="d2199-105">SID-History attribute</span></span>

<span data-ttu-id="d2199-106">如果物件是從另一個網域移出，則包含用於物件的先前 Sid。</span><span class="sxs-lookup"><span data-stu-id="d2199-106">Contains previous SIDs used for the object if the object was moved from another domain.</span></span> <span data-ttu-id="d2199-107">每當物件從一個網域移到另一個網域時，就會建立新的 SID，而新的 SID 就會變成 objectSID。</span><span class="sxs-lookup"><span data-stu-id="d2199-107">Whenever an object is moved from one domain to another, a new SID is created and that new SID becomes the objectSID.</span></span> <span data-ttu-id="d2199-108">先前的 SID 會新增至 sIDHistory 屬性。</span><span class="sxs-lookup"><span data-stu-id="d2199-108">The previous SID is added to the sIDHistory property.</span></span>



| <span data-ttu-id="d2199-109">進入</span><span class="sxs-lookup"><span data-stu-id="d2199-109">Entry</span></span> | <span data-ttu-id="d2199-110">值</span><span class="sxs-lookup"><span data-stu-id="d2199-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="d2199-111">CN</span><span class="sxs-lookup"><span data-stu-id="d2199-111">CN</span></span>                | <span data-ttu-id="d2199-112">SID-History</span><span class="sxs-lookup"><span data-stu-id="d2199-112">SID-History</span></span>                                    |
| <span data-ttu-id="d2199-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d2199-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d2199-114">sIDHistory</span><span class="sxs-lookup"><span data-stu-id="d2199-114">sIDHistory</span></span>                                     |
| <span data-ttu-id="d2199-115">大小</span><span class="sxs-lookup"><span data-stu-id="d2199-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="d2199-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d2199-116">Update Privilege</span></span>  | <span data-ttu-id="d2199-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="d2199-117">This value is set by the system.</span></span>               |
| <span data-ttu-id="d2199-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d2199-118">Update Frequency</span></span>  | <span data-ttu-id="d2199-119">每次物件移至新的網域時。</span><span class="sxs-lookup"><span data-stu-id="d2199-119">Each time the object is moved to a new domain.</span></span> |
| <span data-ttu-id="d2199-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2199-120">Attribute-Id</span></span>      | <span data-ttu-id="d2199-121">1.2.840.113556.1.4.609</span><span class="sxs-lookup"><span data-stu-id="d2199-121">1.2.840.113556.1.4.609</span></span>                         |
| <span data-ttu-id="d2199-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d2199-122">System-Id-Guid</span></span>    | <span data-ttu-id="d2199-123">17eb4278-d167-11d0-b002-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d2199-123">17eb4278-d167-11d0-b002-0000f80367c1</span></span>           |
| <span data-ttu-id="d2199-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2199-124">Syntax</span></span>            | [<span data-ttu-id="d2199-125">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="d2199-125">**String(Sid)**</span></span>](s-string-sid.md)            |



## <a name="implementations"></a><span data-ttu-id="d2199-126">實作</span><span class="sxs-lookup"><span data-stu-id="d2199-126">Implementations</span></span>

-   [<span data-ttu-id="d2199-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d2199-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d2199-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2199-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2199-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2199-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2199-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2199-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2199-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2199-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2199-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2199-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d2199-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2199-133">Windows 2000 Server</span></span>



| <span data-ttu-id="d2199-134">進入</span><span class="sxs-lookup"><span data-stu-id="d2199-134">Entry</span></span> | <span data-ttu-id="d2199-135">值</span><span class="sxs-lookup"><span data-stu-id="d2199-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d2199-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2199-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2199-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2199-138">System-Only</span></span>            | <span data-ttu-id="d2199-139">對</span><span class="sxs-lookup"><span data-stu-id="d2199-139">True</span></span>                                                         |
| <span data-ttu-id="d2199-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2199-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d2199-141">否</span><span class="sxs-lookup"><span data-stu-id="d2199-141">False</span></span>                                                        |
| <span data-ttu-id="d2199-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2199-142">Is Indexed</span></span>             | <span data-ttu-id="d2199-143">對</span><span class="sxs-lookup"><span data-stu-id="d2199-143">True</span></span>                                                         |
| <span data-ttu-id="d2199-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2199-144">In Global Catalog</span></span>      | <span data-ttu-id="d2199-145">對</span><span class="sxs-lookup"><span data-stu-id="d2199-145">True</span></span>                                                         |
| <span data-ttu-id="d2199-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2199-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2199-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2199-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d2199-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2199-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2199-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-150">Search-Flags</span></span>           | <span data-ttu-id="d2199-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d2199-151">0x00000001</span></span>                                                   |
| <span data-ttu-id="d2199-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-152">System-Flags</span></span>           | <span data-ttu-id="d2199-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d2199-153">0x00000012</span></span>                                                   |
| <span data-ttu-id="d2199-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2199-154">Classes used in</span></span>        | [<span data-ttu-id="d2199-155">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d2199-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d2199-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2199-156">Windows Server 2003</span></span>



| <span data-ttu-id="d2199-157">進入</span><span class="sxs-lookup"><span data-stu-id="d2199-157">Entry</span></span> | <span data-ttu-id="d2199-158">值</span><span class="sxs-lookup"><span data-stu-id="d2199-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d2199-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2199-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2199-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2199-161">System-Only</span></span>            | <span data-ttu-id="d2199-162">否</span><span class="sxs-lookup"><span data-stu-id="d2199-162">False</span></span>                                                        |
| <span data-ttu-id="d2199-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2199-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d2199-164">否</span><span class="sxs-lookup"><span data-stu-id="d2199-164">False</span></span>                                                        |
| <span data-ttu-id="d2199-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2199-165">Is Indexed</span></span>             | <span data-ttu-id="d2199-166">對</span><span class="sxs-lookup"><span data-stu-id="d2199-166">True</span></span>                                                         |
| <span data-ttu-id="d2199-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2199-167">In Global Catalog</span></span>      | <span data-ttu-id="d2199-168">對</span><span class="sxs-lookup"><span data-stu-id="d2199-168">True</span></span>                                                         |
| <span data-ttu-id="d2199-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2199-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2199-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2199-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d2199-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2199-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2199-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-173">Search-Flags</span></span>           | <span data-ttu-id="d2199-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d2199-174">0x00000001</span></span>                                                   |
| <span data-ttu-id="d2199-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-175">System-Flags</span></span>           | <span data-ttu-id="d2199-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d2199-176">0x00000012</span></span>                                                   |
| <span data-ttu-id="d2199-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2199-177">Classes used in</span></span>        | [<span data-ttu-id="d2199-178">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d2199-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2199-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2199-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2199-180">進入</span><span class="sxs-lookup"><span data-stu-id="d2199-180">Entry</span></span> | <span data-ttu-id="d2199-181">值</span><span class="sxs-lookup"><span data-stu-id="d2199-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d2199-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2199-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2199-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2199-184">System-Only</span></span>            | <span data-ttu-id="d2199-185">否</span><span class="sxs-lookup"><span data-stu-id="d2199-185">False</span></span>                                                        |
| <span data-ttu-id="d2199-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2199-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d2199-187">否</span><span class="sxs-lookup"><span data-stu-id="d2199-187">False</span></span>                                                        |
| <span data-ttu-id="d2199-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2199-188">Is Indexed</span></span>             | <span data-ttu-id="d2199-189">對</span><span class="sxs-lookup"><span data-stu-id="d2199-189">True</span></span>                                                         |
| <span data-ttu-id="d2199-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2199-190">In Global Catalog</span></span>      | <span data-ttu-id="d2199-191">對</span><span class="sxs-lookup"><span data-stu-id="d2199-191">True</span></span>                                                         |
| <span data-ttu-id="d2199-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2199-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2199-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2199-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d2199-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2199-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2199-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-196">Search-Flags</span></span>           | <span data-ttu-id="d2199-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d2199-197">0x00000001</span></span>                                                   |
| <span data-ttu-id="d2199-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-198">System-Flags</span></span>           | <span data-ttu-id="d2199-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d2199-199">0x00000012</span></span>                                                   |
| <span data-ttu-id="d2199-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2199-200">Classes used in</span></span>        | [<span data-ttu-id="d2199-201">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d2199-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2199-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2199-202">Windows Server 2008</span></span>



| <span data-ttu-id="d2199-203">進入</span><span class="sxs-lookup"><span data-stu-id="d2199-203">Entry</span></span> | <span data-ttu-id="d2199-204">值</span><span class="sxs-lookup"><span data-stu-id="d2199-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d2199-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2199-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2199-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2199-207">System-Only</span></span>            | <span data-ttu-id="d2199-208">否</span><span class="sxs-lookup"><span data-stu-id="d2199-208">False</span></span>                                                        |
| <span data-ttu-id="d2199-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2199-209">Is-Single-Valued</span></span>       | <span data-ttu-id="d2199-210">否</span><span class="sxs-lookup"><span data-stu-id="d2199-210">False</span></span>                                                        |
| <span data-ttu-id="d2199-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2199-211">Is Indexed</span></span>             | <span data-ttu-id="d2199-212">對</span><span class="sxs-lookup"><span data-stu-id="d2199-212">True</span></span>                                                         |
| <span data-ttu-id="d2199-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2199-213">In Global Catalog</span></span>      | <span data-ttu-id="d2199-214">對</span><span class="sxs-lookup"><span data-stu-id="d2199-214">True</span></span>                                                         |
| <span data-ttu-id="d2199-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2199-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2199-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2199-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d2199-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2199-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2199-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-219">Search-Flags</span></span>           | <span data-ttu-id="d2199-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d2199-220">0x00000001</span></span>                                                   |
| <span data-ttu-id="d2199-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-221">System-Flags</span></span>           | <span data-ttu-id="d2199-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d2199-222">0x00000012</span></span>                                                   |
| <span data-ttu-id="d2199-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2199-223">Classes used in</span></span>        | [<span data-ttu-id="d2199-224">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d2199-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2199-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2199-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2199-226">進入</span><span class="sxs-lookup"><span data-stu-id="d2199-226">Entry</span></span> | <span data-ttu-id="d2199-227">值</span><span class="sxs-lookup"><span data-stu-id="d2199-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d2199-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2199-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2199-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2199-230">System-Only</span></span>            | <span data-ttu-id="d2199-231">否</span><span class="sxs-lookup"><span data-stu-id="d2199-231">False</span></span>                                                        |
| <span data-ttu-id="d2199-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2199-232">Is-Single-Valued</span></span>       | <span data-ttu-id="d2199-233">否</span><span class="sxs-lookup"><span data-stu-id="d2199-233">False</span></span>                                                        |
| <span data-ttu-id="d2199-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2199-234">Is Indexed</span></span>             | <span data-ttu-id="d2199-235">對</span><span class="sxs-lookup"><span data-stu-id="d2199-235">True</span></span>                                                         |
| <span data-ttu-id="d2199-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2199-236">In Global Catalog</span></span>      | <span data-ttu-id="d2199-237">對</span><span class="sxs-lookup"><span data-stu-id="d2199-237">True</span></span>                                                         |
| <span data-ttu-id="d2199-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2199-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2199-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2199-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d2199-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2199-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2199-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-242">Search-Flags</span></span>           | <span data-ttu-id="d2199-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d2199-243">0x00000001</span></span>                                                   |
| <span data-ttu-id="d2199-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-244">System-Flags</span></span>           | <span data-ttu-id="d2199-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d2199-245">0x00000012</span></span>                                                   |
| <span data-ttu-id="d2199-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2199-246">Classes used in</span></span>        | [<span data-ttu-id="d2199-247">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d2199-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2199-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2199-248">Windows Server 2012</span></span>



| <span data-ttu-id="d2199-249">進入</span><span class="sxs-lookup"><span data-stu-id="d2199-249">Entry</span></span> | <span data-ttu-id="d2199-250">值</span><span class="sxs-lookup"><span data-stu-id="d2199-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d2199-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2199-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2199-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d2199-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2199-253">System-Only</span></span>            | <span data-ttu-id="d2199-254">否</span><span class="sxs-lookup"><span data-stu-id="d2199-254">False</span></span>                                                        |
| <span data-ttu-id="d2199-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2199-255">Is-Single-Valued</span></span>       | <span data-ttu-id="d2199-256">否</span><span class="sxs-lookup"><span data-stu-id="d2199-256">False</span></span>                                                        |
| <span data-ttu-id="d2199-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2199-257">Is Indexed</span></span>             | <span data-ttu-id="d2199-258">對</span><span class="sxs-lookup"><span data-stu-id="d2199-258">True</span></span>                                                         |
| <span data-ttu-id="d2199-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2199-259">In Global Catalog</span></span>      | <span data-ttu-id="d2199-260">對</span><span class="sxs-lookup"><span data-stu-id="d2199-260">True</span></span>                                                         |
| <span data-ttu-id="d2199-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2199-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2199-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2199-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d2199-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2199-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2199-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d2199-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-265">Search-Flags</span></span>           | <span data-ttu-id="d2199-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d2199-266">0x00000001</span></span>                                                   |
| <span data-ttu-id="d2199-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2199-267">System-Flags</span></span>           | <span data-ttu-id="d2199-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d2199-268">0x00000012</span></span>                                                   |
| <span data-ttu-id="d2199-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2199-269">Classes used in</span></span>        | [<span data-ttu-id="d2199-270">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d2199-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 






---
title: Object-Guid 屬性
description: 物件的唯一識別碼。
ms.assetid: fc2d65a3-7472-41ef-9780-d1a7ec965804
ms.tgt_platform: multiple
keywords:
- Object-Guid 屬性 AD 架構
- objectGUID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Object-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e3715c38b629869296e6f8df5dbebd9a515d1b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845375"
---
# <a name="object-guid-attribute"></a><span data-ttu-id="fff2b-105">Object-Guid 屬性</span><span class="sxs-lookup"><span data-stu-id="fff2b-105">Object-Guid attribute</span></span>

<span data-ttu-id="fff2b-106">物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fff2b-106">The unique identifier for an object.</span></span>



| <span data-ttu-id="fff2b-107">進入</span><span class="sxs-lookup"><span data-stu-id="fff2b-107">Entry</span></span> | <span data-ttu-id="fff2b-108">值</span><span class="sxs-lookup"><span data-stu-id="fff2b-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fff2b-109">CN</span><span class="sxs-lookup"><span data-stu-id="fff2b-109">CN</span></span>                | <span data-ttu-id="fff2b-110">Object-Guid</span><span class="sxs-lookup"><span data-stu-id="fff2b-110">Object-Guid</span></span>                                                         |
| <span data-ttu-id="fff2b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fff2b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fff2b-112">objectGUID</span><span class="sxs-lookup"><span data-stu-id="fff2b-112">objectGUID</span></span>                                                          |
| <span data-ttu-id="fff2b-113">大小</span><span class="sxs-lookup"><span data-stu-id="fff2b-113">Size</span></span>              | <span data-ttu-id="fff2b-114">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="fff2b-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="fff2b-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fff2b-115">Update Privilege</span></span>  | <span data-ttu-id="fff2b-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="fff2b-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="fff2b-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fff2b-117">Update Frequency</span></span>  | <span data-ttu-id="fff2b-118">此值是在建立物件時設定的，而且無法變更。</span><span class="sxs-lookup"><span data-stu-id="fff2b-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="fff2b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fff2b-119">Attribute-Id</span></span>      | <span data-ttu-id="fff2b-120">1.2.840.113556.1.4.2</span><span class="sxs-lookup"><span data-stu-id="fff2b-120">1.2.840.113556.1.4.2</span></span>                                                |
| <span data-ttu-id="fff2b-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fff2b-121">System-Id-Guid</span></span>    | <span data-ttu-id="fff2b-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="fff2b-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="fff2b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="fff2b-123">Syntax</span></span>            | [<span data-ttu-id="fff2b-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="fff2b-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="fff2b-125">實作</span><span class="sxs-lookup"><span data-stu-id="fff2b-125">Implementations</span></span>

-   [<span data-ttu-id="fff2b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fff2b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fff2b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fff2b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fff2b-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="fff2b-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fff2b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fff2b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fff2b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fff2b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fff2b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fff2b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fff2b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fff2b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fff2b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fff2b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="fff2b-134">進入</span><span class="sxs-lookup"><span data-stu-id="fff2b-134">Entry</span></span> | <span data-ttu-id="fff2b-135">值</span><span class="sxs-lookup"><span data-stu-id="fff2b-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fff2b-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fff2b-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fff2b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fff2b-137">MAPI-Id</span></span>                | <span data-ttu-id="fff2b-138">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="fff2b-138">0x8C6D</span></span>                          |
| <span data-ttu-id="fff2b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="fff2b-139">System-Only</span></span>            | <span data-ttu-id="fff2b-140">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-140">True</span></span>                            |
| <span data-ttu-id="fff2b-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fff2b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="fff2b-142">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-142">True</span></span>                            |
| <span data-ttu-id="fff2b-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fff2b-143">Is Indexed</span></span>             | <span data-ttu-id="fff2b-144">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-144">True</span></span>                            |
| <span data-ttu-id="fff2b-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fff2b-145">In Global Catalog</span></span>      | <span data-ttu-id="fff2b-146">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-146">True</span></span>                            |
| <span data-ttu-id="fff2b-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fff2b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="fff2b-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fff2b-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fff2b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fff2b-149">Range-Lower</span></span>            | <span data-ttu-id="fff2b-150">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-150">16</span></span>                              |
| <span data-ttu-id="fff2b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fff2b-151">Range-Upper</span></span>            | <span data-ttu-id="fff2b-152">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-152">16</span></span>                              |
| <span data-ttu-id="fff2b-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-153">Search-Flags</span></span>           | <span data-ttu-id="fff2b-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="fff2b-154">0x00000009</span></span>                      |
| <span data-ttu-id="fff2b-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-155">System-Flags</span></span>           | <span data-ttu-id="fff2b-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="fff2b-156">0x00000013</span></span>                      |
| <span data-ttu-id="fff2b-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fff2b-157">Classes used in</span></span>        | [<span data-ttu-id="fff2b-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fff2b-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fff2b-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fff2b-159">Windows Server 2003</span></span>



| <span data-ttu-id="fff2b-160">進入</span><span class="sxs-lookup"><span data-stu-id="fff2b-160">Entry</span></span> | <span data-ttu-id="fff2b-161">值</span><span class="sxs-lookup"><span data-stu-id="fff2b-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fff2b-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fff2b-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fff2b-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fff2b-163">MAPI-Id</span></span>                | <span data-ttu-id="fff2b-164">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="fff2b-164">0x8C6D</span></span>                          |
| <span data-ttu-id="fff2b-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="fff2b-165">System-Only</span></span>            | <span data-ttu-id="fff2b-166">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-166">True</span></span>                            |
| <span data-ttu-id="fff2b-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fff2b-167">Is-Single-Valued</span></span>       | <span data-ttu-id="fff2b-168">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-168">True</span></span>                            |
| <span data-ttu-id="fff2b-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fff2b-169">Is Indexed</span></span>             | <span data-ttu-id="fff2b-170">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-170">True</span></span>                            |
| <span data-ttu-id="fff2b-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fff2b-171">In Global Catalog</span></span>      | <span data-ttu-id="fff2b-172">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-172">True</span></span>                            |
| <span data-ttu-id="fff2b-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fff2b-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="fff2b-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fff2b-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fff2b-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fff2b-175">Range-Lower</span></span>            | <span data-ttu-id="fff2b-176">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-176">16</span></span>                              |
| <span data-ttu-id="fff2b-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fff2b-177">Range-Upper</span></span>            | <span data-ttu-id="fff2b-178">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-178">16</span></span>                              |
| <span data-ttu-id="fff2b-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-179">Search-Flags</span></span>           | <span data-ttu-id="fff2b-180">0x00000009</span><span class="sxs-lookup"><span data-stu-id="fff2b-180">0x00000009</span></span>                      |
| <span data-ttu-id="fff2b-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-181">System-Flags</span></span>           | <span data-ttu-id="fff2b-182">0x00000013</span><span class="sxs-lookup"><span data-stu-id="fff2b-182">0x00000013</span></span>                      |
| <span data-ttu-id="fff2b-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fff2b-183">Classes used in</span></span>        | [<span data-ttu-id="fff2b-184">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fff2b-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fff2b-185">亞當</span><span class="sxs-lookup"><span data-stu-id="fff2b-185">ADAM</span></span>



| <span data-ttu-id="fff2b-186">進入</span><span class="sxs-lookup"><span data-stu-id="fff2b-186">Entry</span></span> | <span data-ttu-id="fff2b-187">值</span><span class="sxs-lookup"><span data-stu-id="fff2b-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fff2b-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fff2b-188">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fff2b-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fff2b-189">MAPI-Id</span></span>                | <span data-ttu-id="fff2b-190">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="fff2b-190">0x8C6D</span></span>                          |
| <span data-ttu-id="fff2b-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="fff2b-191">System-Only</span></span>            | <span data-ttu-id="fff2b-192">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-192">True</span></span>                            |
| <span data-ttu-id="fff2b-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fff2b-193">Is-Single-Valued</span></span>       | <span data-ttu-id="fff2b-194">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-194">True</span></span>                            |
| <span data-ttu-id="fff2b-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fff2b-195">Is Indexed</span></span>             | <span data-ttu-id="fff2b-196">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-196">True</span></span>                            |
| <span data-ttu-id="fff2b-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fff2b-197">In Global Catalog</span></span>      | <span data-ttu-id="fff2b-198">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-198">True</span></span>                            |
| <span data-ttu-id="fff2b-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fff2b-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="fff2b-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fff2b-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fff2b-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fff2b-201">Range-Lower</span></span>            | <span data-ttu-id="fff2b-202">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-202">16</span></span>                              |
| <span data-ttu-id="fff2b-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fff2b-203">Range-Upper</span></span>            | <span data-ttu-id="fff2b-204">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-204">16</span></span>                              |
| <span data-ttu-id="fff2b-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-205">Search-Flags</span></span>           | <span data-ttu-id="fff2b-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="fff2b-206">0x00000009</span></span>                      |
| <span data-ttu-id="fff2b-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-207">System-Flags</span></span>           | <span data-ttu-id="fff2b-208">0x00000013</span><span class="sxs-lookup"><span data-stu-id="fff2b-208">0x00000013</span></span>                      |
| <span data-ttu-id="fff2b-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fff2b-209">Classes used in</span></span>        | [<span data-ttu-id="fff2b-210">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fff2b-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fff2b-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fff2b-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fff2b-212">進入</span><span class="sxs-lookup"><span data-stu-id="fff2b-212">Entry</span></span> | <span data-ttu-id="fff2b-213">值</span><span class="sxs-lookup"><span data-stu-id="fff2b-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fff2b-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fff2b-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fff2b-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fff2b-215">MAPI-Id</span></span>                | <span data-ttu-id="fff2b-216">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="fff2b-216">0x8C6D</span></span>                          |
| <span data-ttu-id="fff2b-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="fff2b-217">System-Only</span></span>            | <span data-ttu-id="fff2b-218">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-218">True</span></span>                            |
| <span data-ttu-id="fff2b-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fff2b-219">Is-Single-Valued</span></span>       | <span data-ttu-id="fff2b-220">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-220">True</span></span>                            |
| <span data-ttu-id="fff2b-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fff2b-221">Is Indexed</span></span>             | <span data-ttu-id="fff2b-222">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-222">True</span></span>                            |
| <span data-ttu-id="fff2b-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fff2b-223">In Global Catalog</span></span>      | <span data-ttu-id="fff2b-224">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-224">True</span></span>                            |
| <span data-ttu-id="fff2b-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fff2b-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="fff2b-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fff2b-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fff2b-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fff2b-227">Range-Lower</span></span>            | <span data-ttu-id="fff2b-228">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-228">16</span></span>                              |
| <span data-ttu-id="fff2b-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fff2b-229">Range-Upper</span></span>            | <span data-ttu-id="fff2b-230">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-230">16</span></span>                              |
| <span data-ttu-id="fff2b-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-231">Search-Flags</span></span>           | <span data-ttu-id="fff2b-232">0x00000009</span><span class="sxs-lookup"><span data-stu-id="fff2b-232">0x00000009</span></span>                      |
| <span data-ttu-id="fff2b-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-233">System-Flags</span></span>           | <span data-ttu-id="fff2b-234">0x00000013</span><span class="sxs-lookup"><span data-stu-id="fff2b-234">0x00000013</span></span>                      |
| <span data-ttu-id="fff2b-235">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fff2b-235">Classes used in</span></span>        | [<span data-ttu-id="fff2b-236">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fff2b-236">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fff2b-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fff2b-237">Windows Server 2008</span></span>



| <span data-ttu-id="fff2b-238">進入</span><span class="sxs-lookup"><span data-stu-id="fff2b-238">Entry</span></span> | <span data-ttu-id="fff2b-239">值</span><span class="sxs-lookup"><span data-stu-id="fff2b-239">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fff2b-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fff2b-240">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fff2b-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fff2b-241">MAPI-Id</span></span>                | <span data-ttu-id="fff2b-242">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="fff2b-242">0x8C6D</span></span>                          |
| <span data-ttu-id="fff2b-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="fff2b-243">System-Only</span></span>            | <span data-ttu-id="fff2b-244">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-244">True</span></span>                            |
| <span data-ttu-id="fff2b-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fff2b-245">Is-Single-Valued</span></span>       | <span data-ttu-id="fff2b-246">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-246">True</span></span>                            |
| <span data-ttu-id="fff2b-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fff2b-247">Is Indexed</span></span>             | <span data-ttu-id="fff2b-248">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-248">True</span></span>                            |
| <span data-ttu-id="fff2b-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fff2b-249">In Global Catalog</span></span>      | <span data-ttu-id="fff2b-250">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-250">True</span></span>                            |
| <span data-ttu-id="fff2b-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fff2b-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="fff2b-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fff2b-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fff2b-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fff2b-253">Range-Lower</span></span>            | <span data-ttu-id="fff2b-254">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-254">16</span></span>                              |
| <span data-ttu-id="fff2b-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fff2b-255">Range-Upper</span></span>            | <span data-ttu-id="fff2b-256">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-256">16</span></span>                              |
| <span data-ttu-id="fff2b-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-257">Search-Flags</span></span>           | <span data-ttu-id="fff2b-258">0x00000009</span><span class="sxs-lookup"><span data-stu-id="fff2b-258">0x00000009</span></span>                      |
| <span data-ttu-id="fff2b-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-259">System-Flags</span></span>           | <span data-ttu-id="fff2b-260">0x00000013</span><span class="sxs-lookup"><span data-stu-id="fff2b-260">0x00000013</span></span>                      |
| <span data-ttu-id="fff2b-261">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fff2b-261">Classes used in</span></span>        | [<span data-ttu-id="fff2b-262">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fff2b-262">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fff2b-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fff2b-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fff2b-264">進入</span><span class="sxs-lookup"><span data-stu-id="fff2b-264">Entry</span></span> | <span data-ttu-id="fff2b-265">值</span><span class="sxs-lookup"><span data-stu-id="fff2b-265">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fff2b-266">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fff2b-266">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fff2b-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fff2b-267">MAPI-Id</span></span>                | <span data-ttu-id="fff2b-268">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="fff2b-268">0x8C6D</span></span>                          |
| <span data-ttu-id="fff2b-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="fff2b-269">System-Only</span></span>            | <span data-ttu-id="fff2b-270">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-270">True</span></span>                            |
| <span data-ttu-id="fff2b-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fff2b-271">Is-Single-Valued</span></span>       | <span data-ttu-id="fff2b-272">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-272">True</span></span>                            |
| <span data-ttu-id="fff2b-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fff2b-273">Is Indexed</span></span>             | <span data-ttu-id="fff2b-274">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-274">True</span></span>                            |
| <span data-ttu-id="fff2b-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fff2b-275">In Global Catalog</span></span>      | <span data-ttu-id="fff2b-276">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-276">True</span></span>                            |
| <span data-ttu-id="fff2b-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fff2b-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="fff2b-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fff2b-278">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fff2b-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fff2b-279">Range-Lower</span></span>            | <span data-ttu-id="fff2b-280">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-280">16</span></span>                              |
| <span data-ttu-id="fff2b-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fff2b-281">Range-Upper</span></span>            | <span data-ttu-id="fff2b-282">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-282">16</span></span>                              |
| <span data-ttu-id="fff2b-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-283">Search-Flags</span></span>           | <span data-ttu-id="fff2b-284">0x00000009</span><span class="sxs-lookup"><span data-stu-id="fff2b-284">0x00000009</span></span>                      |
| <span data-ttu-id="fff2b-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-285">System-Flags</span></span>           | <span data-ttu-id="fff2b-286">0x00000013</span><span class="sxs-lookup"><span data-stu-id="fff2b-286">0x00000013</span></span>                      |
| <span data-ttu-id="fff2b-287">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fff2b-287">Classes used in</span></span>        | [<span data-ttu-id="fff2b-288">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fff2b-288">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fff2b-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fff2b-289">Windows Server 2012</span></span>



| <span data-ttu-id="fff2b-290">進入</span><span class="sxs-lookup"><span data-stu-id="fff2b-290">Entry</span></span> | <span data-ttu-id="fff2b-291">值</span><span class="sxs-lookup"><span data-stu-id="fff2b-291">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fff2b-292">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fff2b-292">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fff2b-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fff2b-293">MAPI-Id</span></span>                | <span data-ttu-id="fff2b-294">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="fff2b-294">0x8C6D</span></span>                          |
| <span data-ttu-id="fff2b-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="fff2b-295">System-Only</span></span>            | <span data-ttu-id="fff2b-296">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-296">True</span></span>                            |
| <span data-ttu-id="fff2b-297">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fff2b-297">Is-Single-Valued</span></span>       | <span data-ttu-id="fff2b-298">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-298">True</span></span>                            |
| <span data-ttu-id="fff2b-299">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fff2b-299">Is Indexed</span></span>             | <span data-ttu-id="fff2b-300">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-300">True</span></span>                            |
| <span data-ttu-id="fff2b-301">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fff2b-301">In Global Catalog</span></span>      | <span data-ttu-id="fff2b-302">對</span><span class="sxs-lookup"><span data-stu-id="fff2b-302">True</span></span>                            |
| <span data-ttu-id="fff2b-303">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fff2b-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="fff2b-304">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fff2b-304">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fff2b-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fff2b-305">Range-Lower</span></span>            | <span data-ttu-id="fff2b-306">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-306">16</span></span>                              |
| <span data-ttu-id="fff2b-307">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fff2b-307">Range-Upper</span></span>            | <span data-ttu-id="fff2b-308">16</span><span class="sxs-lookup"><span data-stu-id="fff2b-308">16</span></span>                              |
| <span data-ttu-id="fff2b-309">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-309">Search-Flags</span></span>           | <span data-ttu-id="fff2b-310">0x00000009</span><span class="sxs-lookup"><span data-stu-id="fff2b-310">0x00000009</span></span>                      |
| <span data-ttu-id="fff2b-311">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fff2b-311">System-Flags</span></span>           | <span data-ttu-id="fff2b-312">0x00000013</span><span class="sxs-lookup"><span data-stu-id="fff2b-312">0x00000013</span></span>                      |
| <span data-ttu-id="fff2b-313">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fff2b-313">Classes used in</span></span>        | [<span data-ttu-id="fff2b-314">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fff2b-314">**Top**</span></span>](c-top.md)<br/> |



 

 






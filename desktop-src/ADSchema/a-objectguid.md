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
# <a name="object-guid-attribute"></a><span data-ttu-id="b4240-105">Object-Guid 屬性</span><span class="sxs-lookup"><span data-stu-id="b4240-105">Object-Guid attribute</span></span>

<span data-ttu-id="b4240-106">物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4240-106">The unique identifier for an object.</span></span>



| <span data-ttu-id="b4240-107">進入</span><span class="sxs-lookup"><span data-stu-id="b4240-107">Entry</span></span> | <span data-ttu-id="b4240-108">值</span><span class="sxs-lookup"><span data-stu-id="b4240-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b4240-109">CN</span><span class="sxs-lookup"><span data-stu-id="b4240-109">CN</span></span>                | <span data-ttu-id="b4240-110">Object-Guid</span><span class="sxs-lookup"><span data-stu-id="b4240-110">Object-Guid</span></span>                                                         |
| <span data-ttu-id="b4240-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b4240-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b4240-112">objectGUID</span><span class="sxs-lookup"><span data-stu-id="b4240-112">objectGUID</span></span>                                                          |
| <span data-ttu-id="b4240-113">大小</span><span class="sxs-lookup"><span data-stu-id="b4240-113">Size</span></span>              | <span data-ttu-id="b4240-114">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="b4240-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="b4240-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b4240-115">Update Privilege</span></span>  | <span data-ttu-id="b4240-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="b4240-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="b4240-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b4240-117">Update Frequency</span></span>  | <span data-ttu-id="b4240-118">此值是在建立物件時設定的，而且無法變更。</span><span class="sxs-lookup"><span data-stu-id="b4240-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="b4240-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4240-119">Attribute-Id</span></span>      | <span data-ttu-id="b4240-120">1.2.840.113556.1.4.2</span><span class="sxs-lookup"><span data-stu-id="b4240-120">1.2.840.113556.1.4.2</span></span>                                                |
| <span data-ttu-id="b4240-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b4240-121">System-Id-Guid</span></span>    | <span data-ttu-id="b4240-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b4240-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="b4240-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4240-123">Syntax</span></span>            | [<span data-ttu-id="b4240-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b4240-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="b4240-125">實作</span><span class="sxs-lookup"><span data-stu-id="b4240-125">Implementations</span></span>

-   [<span data-ttu-id="b4240-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4240-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4240-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4240-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4240-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b4240-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b4240-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4240-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4240-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4240-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4240-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4240-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4240-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4240-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4240-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4240-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b4240-134">進入</span><span class="sxs-lookup"><span data-stu-id="b4240-134">Entry</span></span> | <span data-ttu-id="b4240-135">值</span><span class="sxs-lookup"><span data-stu-id="b4240-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4240-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4240-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4240-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4240-137">MAPI-Id</span></span>                | <span data-ttu-id="b4240-138">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="b4240-138">0x8C6D</span></span>                          |
| <span data-ttu-id="b4240-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4240-139">System-Only</span></span>            | <span data-ttu-id="b4240-140">對</span><span class="sxs-lookup"><span data-stu-id="b4240-140">True</span></span>                            |
| <span data-ttu-id="b4240-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4240-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b4240-142">對</span><span class="sxs-lookup"><span data-stu-id="b4240-142">True</span></span>                            |
| <span data-ttu-id="b4240-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4240-143">Is Indexed</span></span>             | <span data-ttu-id="b4240-144">對</span><span class="sxs-lookup"><span data-stu-id="b4240-144">True</span></span>                            |
| <span data-ttu-id="b4240-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4240-145">In Global Catalog</span></span>      | <span data-ttu-id="b4240-146">對</span><span class="sxs-lookup"><span data-stu-id="b4240-146">True</span></span>                            |
| <span data-ttu-id="b4240-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4240-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4240-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4240-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4240-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4240-149">Range-Lower</span></span>            | <span data-ttu-id="b4240-150">16</span><span class="sxs-lookup"><span data-stu-id="b4240-150">16</span></span>                              |
| <span data-ttu-id="b4240-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4240-151">Range-Upper</span></span>            | <span data-ttu-id="b4240-152">16</span><span class="sxs-lookup"><span data-stu-id="b4240-152">16</span></span>                              |
| <span data-ttu-id="b4240-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-153">Search-Flags</span></span>           | <span data-ttu-id="b4240-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b4240-154">0x00000009</span></span>                      |
| <span data-ttu-id="b4240-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-155">System-Flags</span></span>           | <span data-ttu-id="b4240-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b4240-156">0x00000013</span></span>                      |
| <span data-ttu-id="b4240-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4240-157">Classes used in</span></span>        | [<span data-ttu-id="b4240-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b4240-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4240-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4240-159">Windows Server 2003</span></span>



| <span data-ttu-id="b4240-160">進入</span><span class="sxs-lookup"><span data-stu-id="b4240-160">Entry</span></span> | <span data-ttu-id="b4240-161">值</span><span class="sxs-lookup"><span data-stu-id="b4240-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4240-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4240-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4240-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4240-163">MAPI-Id</span></span>                | <span data-ttu-id="b4240-164">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="b4240-164">0x8C6D</span></span>                          |
| <span data-ttu-id="b4240-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4240-165">System-Only</span></span>            | <span data-ttu-id="b4240-166">對</span><span class="sxs-lookup"><span data-stu-id="b4240-166">True</span></span>                            |
| <span data-ttu-id="b4240-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4240-167">Is-Single-Valued</span></span>       | <span data-ttu-id="b4240-168">對</span><span class="sxs-lookup"><span data-stu-id="b4240-168">True</span></span>                            |
| <span data-ttu-id="b4240-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4240-169">Is Indexed</span></span>             | <span data-ttu-id="b4240-170">對</span><span class="sxs-lookup"><span data-stu-id="b4240-170">True</span></span>                            |
| <span data-ttu-id="b4240-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4240-171">In Global Catalog</span></span>      | <span data-ttu-id="b4240-172">對</span><span class="sxs-lookup"><span data-stu-id="b4240-172">True</span></span>                            |
| <span data-ttu-id="b4240-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4240-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4240-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4240-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4240-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4240-175">Range-Lower</span></span>            | <span data-ttu-id="b4240-176">16</span><span class="sxs-lookup"><span data-stu-id="b4240-176">16</span></span>                              |
| <span data-ttu-id="b4240-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4240-177">Range-Upper</span></span>            | <span data-ttu-id="b4240-178">16</span><span class="sxs-lookup"><span data-stu-id="b4240-178">16</span></span>                              |
| <span data-ttu-id="b4240-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-179">Search-Flags</span></span>           | <span data-ttu-id="b4240-180">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b4240-180">0x00000009</span></span>                      |
| <span data-ttu-id="b4240-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-181">System-Flags</span></span>           | <span data-ttu-id="b4240-182">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b4240-182">0x00000013</span></span>                      |
| <span data-ttu-id="b4240-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4240-183">Classes used in</span></span>        | [<span data-ttu-id="b4240-184">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b4240-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b4240-185">亞當</span><span class="sxs-lookup"><span data-stu-id="b4240-185">ADAM</span></span>



| <span data-ttu-id="b4240-186">進入</span><span class="sxs-lookup"><span data-stu-id="b4240-186">Entry</span></span> | <span data-ttu-id="b4240-187">值</span><span class="sxs-lookup"><span data-stu-id="b4240-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4240-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4240-188">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4240-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4240-189">MAPI-Id</span></span>                | <span data-ttu-id="b4240-190">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="b4240-190">0x8C6D</span></span>                          |
| <span data-ttu-id="b4240-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4240-191">System-Only</span></span>            | <span data-ttu-id="b4240-192">對</span><span class="sxs-lookup"><span data-stu-id="b4240-192">True</span></span>                            |
| <span data-ttu-id="b4240-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4240-193">Is-Single-Valued</span></span>       | <span data-ttu-id="b4240-194">對</span><span class="sxs-lookup"><span data-stu-id="b4240-194">True</span></span>                            |
| <span data-ttu-id="b4240-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4240-195">Is Indexed</span></span>             | <span data-ttu-id="b4240-196">對</span><span class="sxs-lookup"><span data-stu-id="b4240-196">True</span></span>                            |
| <span data-ttu-id="b4240-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4240-197">In Global Catalog</span></span>      | <span data-ttu-id="b4240-198">對</span><span class="sxs-lookup"><span data-stu-id="b4240-198">True</span></span>                            |
| <span data-ttu-id="b4240-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4240-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4240-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4240-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4240-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4240-201">Range-Lower</span></span>            | <span data-ttu-id="b4240-202">16</span><span class="sxs-lookup"><span data-stu-id="b4240-202">16</span></span>                              |
| <span data-ttu-id="b4240-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4240-203">Range-Upper</span></span>            | <span data-ttu-id="b4240-204">16</span><span class="sxs-lookup"><span data-stu-id="b4240-204">16</span></span>                              |
| <span data-ttu-id="b4240-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-205">Search-Flags</span></span>           | <span data-ttu-id="b4240-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b4240-206">0x00000009</span></span>                      |
| <span data-ttu-id="b4240-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-207">System-Flags</span></span>           | <span data-ttu-id="b4240-208">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b4240-208">0x00000013</span></span>                      |
| <span data-ttu-id="b4240-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4240-209">Classes used in</span></span>        | [<span data-ttu-id="b4240-210">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b4240-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4240-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4240-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4240-212">進入</span><span class="sxs-lookup"><span data-stu-id="b4240-212">Entry</span></span> | <span data-ttu-id="b4240-213">值</span><span class="sxs-lookup"><span data-stu-id="b4240-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4240-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4240-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4240-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4240-215">MAPI-Id</span></span>                | <span data-ttu-id="b4240-216">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="b4240-216">0x8C6D</span></span>                          |
| <span data-ttu-id="b4240-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4240-217">System-Only</span></span>            | <span data-ttu-id="b4240-218">對</span><span class="sxs-lookup"><span data-stu-id="b4240-218">True</span></span>                            |
| <span data-ttu-id="b4240-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4240-219">Is-Single-Valued</span></span>       | <span data-ttu-id="b4240-220">對</span><span class="sxs-lookup"><span data-stu-id="b4240-220">True</span></span>                            |
| <span data-ttu-id="b4240-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4240-221">Is Indexed</span></span>             | <span data-ttu-id="b4240-222">對</span><span class="sxs-lookup"><span data-stu-id="b4240-222">True</span></span>                            |
| <span data-ttu-id="b4240-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4240-223">In Global Catalog</span></span>      | <span data-ttu-id="b4240-224">對</span><span class="sxs-lookup"><span data-stu-id="b4240-224">True</span></span>                            |
| <span data-ttu-id="b4240-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4240-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4240-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4240-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4240-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4240-227">Range-Lower</span></span>            | <span data-ttu-id="b4240-228">16</span><span class="sxs-lookup"><span data-stu-id="b4240-228">16</span></span>                              |
| <span data-ttu-id="b4240-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4240-229">Range-Upper</span></span>            | <span data-ttu-id="b4240-230">16</span><span class="sxs-lookup"><span data-stu-id="b4240-230">16</span></span>                              |
| <span data-ttu-id="b4240-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-231">Search-Flags</span></span>           | <span data-ttu-id="b4240-232">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b4240-232">0x00000009</span></span>                      |
| <span data-ttu-id="b4240-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-233">System-Flags</span></span>           | <span data-ttu-id="b4240-234">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b4240-234">0x00000013</span></span>                      |
| <span data-ttu-id="b4240-235">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4240-235">Classes used in</span></span>        | [<span data-ttu-id="b4240-236">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b4240-236">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4240-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4240-237">Windows Server 2008</span></span>



| <span data-ttu-id="b4240-238">進入</span><span class="sxs-lookup"><span data-stu-id="b4240-238">Entry</span></span> | <span data-ttu-id="b4240-239">值</span><span class="sxs-lookup"><span data-stu-id="b4240-239">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4240-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4240-240">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4240-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4240-241">MAPI-Id</span></span>                | <span data-ttu-id="b4240-242">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="b4240-242">0x8C6D</span></span>                          |
| <span data-ttu-id="b4240-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4240-243">System-Only</span></span>            | <span data-ttu-id="b4240-244">對</span><span class="sxs-lookup"><span data-stu-id="b4240-244">True</span></span>                            |
| <span data-ttu-id="b4240-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4240-245">Is-Single-Valued</span></span>       | <span data-ttu-id="b4240-246">對</span><span class="sxs-lookup"><span data-stu-id="b4240-246">True</span></span>                            |
| <span data-ttu-id="b4240-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4240-247">Is Indexed</span></span>             | <span data-ttu-id="b4240-248">對</span><span class="sxs-lookup"><span data-stu-id="b4240-248">True</span></span>                            |
| <span data-ttu-id="b4240-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4240-249">In Global Catalog</span></span>      | <span data-ttu-id="b4240-250">對</span><span class="sxs-lookup"><span data-stu-id="b4240-250">True</span></span>                            |
| <span data-ttu-id="b4240-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4240-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4240-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4240-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4240-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4240-253">Range-Lower</span></span>            | <span data-ttu-id="b4240-254">16</span><span class="sxs-lookup"><span data-stu-id="b4240-254">16</span></span>                              |
| <span data-ttu-id="b4240-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4240-255">Range-Upper</span></span>            | <span data-ttu-id="b4240-256">16</span><span class="sxs-lookup"><span data-stu-id="b4240-256">16</span></span>                              |
| <span data-ttu-id="b4240-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-257">Search-Flags</span></span>           | <span data-ttu-id="b4240-258">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b4240-258">0x00000009</span></span>                      |
| <span data-ttu-id="b4240-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-259">System-Flags</span></span>           | <span data-ttu-id="b4240-260">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b4240-260">0x00000013</span></span>                      |
| <span data-ttu-id="b4240-261">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4240-261">Classes used in</span></span>        | [<span data-ttu-id="b4240-262">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b4240-262">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4240-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4240-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4240-264">進入</span><span class="sxs-lookup"><span data-stu-id="b4240-264">Entry</span></span> | <span data-ttu-id="b4240-265">值</span><span class="sxs-lookup"><span data-stu-id="b4240-265">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4240-266">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4240-266">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4240-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4240-267">MAPI-Id</span></span>                | <span data-ttu-id="b4240-268">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="b4240-268">0x8C6D</span></span>                          |
| <span data-ttu-id="b4240-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4240-269">System-Only</span></span>            | <span data-ttu-id="b4240-270">對</span><span class="sxs-lookup"><span data-stu-id="b4240-270">True</span></span>                            |
| <span data-ttu-id="b4240-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4240-271">Is-Single-Valued</span></span>       | <span data-ttu-id="b4240-272">對</span><span class="sxs-lookup"><span data-stu-id="b4240-272">True</span></span>                            |
| <span data-ttu-id="b4240-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4240-273">Is Indexed</span></span>             | <span data-ttu-id="b4240-274">對</span><span class="sxs-lookup"><span data-stu-id="b4240-274">True</span></span>                            |
| <span data-ttu-id="b4240-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4240-275">In Global Catalog</span></span>      | <span data-ttu-id="b4240-276">對</span><span class="sxs-lookup"><span data-stu-id="b4240-276">True</span></span>                            |
| <span data-ttu-id="b4240-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4240-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4240-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4240-278">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4240-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4240-279">Range-Lower</span></span>            | <span data-ttu-id="b4240-280">16</span><span class="sxs-lookup"><span data-stu-id="b4240-280">16</span></span>                              |
| <span data-ttu-id="b4240-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4240-281">Range-Upper</span></span>            | <span data-ttu-id="b4240-282">16</span><span class="sxs-lookup"><span data-stu-id="b4240-282">16</span></span>                              |
| <span data-ttu-id="b4240-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-283">Search-Flags</span></span>           | <span data-ttu-id="b4240-284">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b4240-284">0x00000009</span></span>                      |
| <span data-ttu-id="b4240-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-285">System-Flags</span></span>           | <span data-ttu-id="b4240-286">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b4240-286">0x00000013</span></span>                      |
| <span data-ttu-id="b4240-287">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4240-287">Classes used in</span></span>        | [<span data-ttu-id="b4240-288">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b4240-288">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4240-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4240-289">Windows Server 2012</span></span>



| <span data-ttu-id="b4240-290">進入</span><span class="sxs-lookup"><span data-stu-id="b4240-290">Entry</span></span> | <span data-ttu-id="b4240-291">值</span><span class="sxs-lookup"><span data-stu-id="b4240-291">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4240-292">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4240-292">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4240-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4240-293">MAPI-Id</span></span>                | <span data-ttu-id="b4240-294">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="b4240-294">0x8C6D</span></span>                          |
| <span data-ttu-id="b4240-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4240-295">System-Only</span></span>            | <span data-ttu-id="b4240-296">對</span><span class="sxs-lookup"><span data-stu-id="b4240-296">True</span></span>                            |
| <span data-ttu-id="b4240-297">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4240-297">Is-Single-Valued</span></span>       | <span data-ttu-id="b4240-298">對</span><span class="sxs-lookup"><span data-stu-id="b4240-298">True</span></span>                            |
| <span data-ttu-id="b4240-299">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4240-299">Is Indexed</span></span>             | <span data-ttu-id="b4240-300">對</span><span class="sxs-lookup"><span data-stu-id="b4240-300">True</span></span>                            |
| <span data-ttu-id="b4240-301">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4240-301">In Global Catalog</span></span>      | <span data-ttu-id="b4240-302">對</span><span class="sxs-lookup"><span data-stu-id="b4240-302">True</span></span>                            |
| <span data-ttu-id="b4240-303">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4240-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4240-304">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4240-304">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4240-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4240-305">Range-Lower</span></span>            | <span data-ttu-id="b4240-306">16</span><span class="sxs-lookup"><span data-stu-id="b4240-306">16</span></span>                              |
| <span data-ttu-id="b4240-307">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4240-307">Range-Upper</span></span>            | <span data-ttu-id="b4240-308">16</span><span class="sxs-lookup"><span data-stu-id="b4240-308">16</span></span>                              |
| <span data-ttu-id="b4240-309">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-309">Search-Flags</span></span>           | <span data-ttu-id="b4240-310">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b4240-310">0x00000009</span></span>                      |
| <span data-ttu-id="b4240-311">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4240-311">System-Flags</span></span>           | <span data-ttu-id="b4240-312">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b4240-312">0x00000013</span></span>                      |
| <span data-ttu-id="b4240-313">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4240-313">Classes used in</span></span>        | [<span data-ttu-id="b4240-314">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b4240-314">**Top**</span></span>](c-top.md)<br/> |



 

 






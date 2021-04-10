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
# <a name="object-guid-attribute"></a><span data-ttu-id="7fefc-105">Object-Guid 屬性</span><span class="sxs-lookup"><span data-stu-id="7fefc-105">Object-Guid attribute</span></span>

<span data-ttu-id="7fefc-106">物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fefc-106">The unique identifier for an object.</span></span>



| <span data-ttu-id="7fefc-107">進入</span><span class="sxs-lookup"><span data-stu-id="7fefc-107">Entry</span></span> | <span data-ttu-id="7fefc-108">值</span><span class="sxs-lookup"><span data-stu-id="7fefc-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7fefc-109">CN</span><span class="sxs-lookup"><span data-stu-id="7fefc-109">CN</span></span>                | <span data-ttu-id="7fefc-110">Object-Guid</span><span class="sxs-lookup"><span data-stu-id="7fefc-110">Object-Guid</span></span>                                                         |
| <span data-ttu-id="7fefc-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7fefc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7fefc-112">objectGUID</span><span class="sxs-lookup"><span data-stu-id="7fefc-112">objectGUID</span></span>                                                          |
| <span data-ttu-id="7fefc-113">大小</span><span class="sxs-lookup"><span data-stu-id="7fefc-113">Size</span></span>              | <span data-ttu-id="7fefc-114">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="7fefc-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="7fefc-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7fefc-115">Update Privilege</span></span>  | <span data-ttu-id="7fefc-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7fefc-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="7fefc-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7fefc-117">Update Frequency</span></span>  | <span data-ttu-id="7fefc-118">此值是在建立物件時設定的，而且無法變更。</span><span class="sxs-lookup"><span data-stu-id="7fefc-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="7fefc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7fefc-119">Attribute-Id</span></span>      | <span data-ttu-id="7fefc-120">1.2.840.113556.1.4.2</span><span class="sxs-lookup"><span data-stu-id="7fefc-120">1.2.840.113556.1.4.2</span></span>                                                |
| <span data-ttu-id="7fefc-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7fefc-121">System-Id-Guid</span></span>    | <span data-ttu-id="7fefc-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7fefc-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="7fefc-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fefc-123">Syntax</span></span>            | [<span data-ttu-id="7fefc-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="7fefc-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="7fefc-125">實作</span><span class="sxs-lookup"><span data-stu-id="7fefc-125">Implementations</span></span>

-   [<span data-ttu-id="7fefc-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7fefc-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7fefc-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7fefc-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7fefc-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7fefc-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7fefc-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7fefc-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7fefc-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7fefc-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7fefc-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7fefc-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7fefc-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7fefc-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7fefc-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7fefc-133">Windows 2000 Server</span></span>



| <span data-ttu-id="7fefc-134">進入</span><span class="sxs-lookup"><span data-stu-id="7fefc-134">Entry</span></span> | <span data-ttu-id="7fefc-135">值</span><span class="sxs-lookup"><span data-stu-id="7fefc-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7fefc-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fefc-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7fefc-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fefc-137">MAPI-Id</span></span>                | <span data-ttu-id="7fefc-138">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="7fefc-138">0x8C6D</span></span>                          |
| <span data-ttu-id="7fefc-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fefc-139">System-Only</span></span>            | <span data-ttu-id="7fefc-140">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-140">True</span></span>                            |
| <span data-ttu-id="7fefc-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fefc-141">Is-Single-Valued</span></span>       | <span data-ttu-id="7fefc-142">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-142">True</span></span>                            |
| <span data-ttu-id="7fefc-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fefc-143">Is Indexed</span></span>             | <span data-ttu-id="7fefc-144">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-144">True</span></span>                            |
| <span data-ttu-id="7fefc-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fefc-145">In Global Catalog</span></span>      | <span data-ttu-id="7fefc-146">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-146">True</span></span>                            |
| <span data-ttu-id="7fefc-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fefc-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fefc-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fefc-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7fefc-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fefc-149">Range-Lower</span></span>            | <span data-ttu-id="7fefc-150">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-150">16</span></span>                              |
| <span data-ttu-id="7fefc-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fefc-151">Range-Upper</span></span>            | <span data-ttu-id="7fefc-152">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-152">16</span></span>                              |
| <span data-ttu-id="7fefc-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-153">Search-Flags</span></span>           | <span data-ttu-id="7fefc-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7fefc-154">0x00000009</span></span>                      |
| <span data-ttu-id="7fefc-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-155">System-Flags</span></span>           | <span data-ttu-id="7fefc-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7fefc-156">0x00000013</span></span>                      |
| <span data-ttu-id="7fefc-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fefc-157">Classes used in</span></span>        | [<span data-ttu-id="7fefc-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7fefc-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7fefc-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7fefc-159">Windows Server 2003</span></span>



| <span data-ttu-id="7fefc-160">進入</span><span class="sxs-lookup"><span data-stu-id="7fefc-160">Entry</span></span> | <span data-ttu-id="7fefc-161">值</span><span class="sxs-lookup"><span data-stu-id="7fefc-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7fefc-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fefc-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7fefc-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fefc-163">MAPI-Id</span></span>                | <span data-ttu-id="7fefc-164">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="7fefc-164">0x8C6D</span></span>                          |
| <span data-ttu-id="7fefc-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fefc-165">System-Only</span></span>            | <span data-ttu-id="7fefc-166">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-166">True</span></span>                            |
| <span data-ttu-id="7fefc-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fefc-167">Is-Single-Valued</span></span>       | <span data-ttu-id="7fefc-168">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-168">True</span></span>                            |
| <span data-ttu-id="7fefc-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fefc-169">Is Indexed</span></span>             | <span data-ttu-id="7fefc-170">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-170">True</span></span>                            |
| <span data-ttu-id="7fefc-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fefc-171">In Global Catalog</span></span>      | <span data-ttu-id="7fefc-172">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-172">True</span></span>                            |
| <span data-ttu-id="7fefc-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fefc-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fefc-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fefc-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7fefc-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fefc-175">Range-Lower</span></span>            | <span data-ttu-id="7fefc-176">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-176">16</span></span>                              |
| <span data-ttu-id="7fefc-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fefc-177">Range-Upper</span></span>            | <span data-ttu-id="7fefc-178">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-178">16</span></span>                              |
| <span data-ttu-id="7fefc-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-179">Search-Flags</span></span>           | <span data-ttu-id="7fefc-180">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7fefc-180">0x00000009</span></span>                      |
| <span data-ttu-id="7fefc-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-181">System-Flags</span></span>           | <span data-ttu-id="7fefc-182">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7fefc-182">0x00000013</span></span>                      |
| <span data-ttu-id="7fefc-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fefc-183">Classes used in</span></span>        | [<span data-ttu-id="7fefc-184">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7fefc-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7fefc-185">亞當</span><span class="sxs-lookup"><span data-stu-id="7fefc-185">ADAM</span></span>



| <span data-ttu-id="7fefc-186">進入</span><span class="sxs-lookup"><span data-stu-id="7fefc-186">Entry</span></span> | <span data-ttu-id="7fefc-187">值</span><span class="sxs-lookup"><span data-stu-id="7fefc-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7fefc-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fefc-188">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7fefc-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fefc-189">MAPI-Id</span></span>                | <span data-ttu-id="7fefc-190">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="7fefc-190">0x8C6D</span></span>                          |
| <span data-ttu-id="7fefc-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fefc-191">System-Only</span></span>            | <span data-ttu-id="7fefc-192">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-192">True</span></span>                            |
| <span data-ttu-id="7fefc-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fefc-193">Is-Single-Valued</span></span>       | <span data-ttu-id="7fefc-194">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-194">True</span></span>                            |
| <span data-ttu-id="7fefc-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fefc-195">Is Indexed</span></span>             | <span data-ttu-id="7fefc-196">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-196">True</span></span>                            |
| <span data-ttu-id="7fefc-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fefc-197">In Global Catalog</span></span>      | <span data-ttu-id="7fefc-198">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-198">True</span></span>                            |
| <span data-ttu-id="7fefc-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fefc-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fefc-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fefc-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7fefc-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fefc-201">Range-Lower</span></span>            | <span data-ttu-id="7fefc-202">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-202">16</span></span>                              |
| <span data-ttu-id="7fefc-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fefc-203">Range-Upper</span></span>            | <span data-ttu-id="7fefc-204">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-204">16</span></span>                              |
| <span data-ttu-id="7fefc-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-205">Search-Flags</span></span>           | <span data-ttu-id="7fefc-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7fefc-206">0x00000009</span></span>                      |
| <span data-ttu-id="7fefc-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-207">System-Flags</span></span>           | <span data-ttu-id="7fefc-208">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7fefc-208">0x00000013</span></span>                      |
| <span data-ttu-id="7fefc-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fefc-209">Classes used in</span></span>        | [<span data-ttu-id="7fefc-210">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7fefc-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7fefc-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7fefc-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7fefc-212">進入</span><span class="sxs-lookup"><span data-stu-id="7fefc-212">Entry</span></span> | <span data-ttu-id="7fefc-213">值</span><span class="sxs-lookup"><span data-stu-id="7fefc-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7fefc-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fefc-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7fefc-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fefc-215">MAPI-Id</span></span>                | <span data-ttu-id="7fefc-216">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="7fefc-216">0x8C6D</span></span>                          |
| <span data-ttu-id="7fefc-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fefc-217">System-Only</span></span>            | <span data-ttu-id="7fefc-218">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-218">True</span></span>                            |
| <span data-ttu-id="7fefc-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fefc-219">Is-Single-Valued</span></span>       | <span data-ttu-id="7fefc-220">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-220">True</span></span>                            |
| <span data-ttu-id="7fefc-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fefc-221">Is Indexed</span></span>             | <span data-ttu-id="7fefc-222">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-222">True</span></span>                            |
| <span data-ttu-id="7fefc-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fefc-223">In Global Catalog</span></span>      | <span data-ttu-id="7fefc-224">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-224">True</span></span>                            |
| <span data-ttu-id="7fefc-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fefc-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fefc-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fefc-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7fefc-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fefc-227">Range-Lower</span></span>            | <span data-ttu-id="7fefc-228">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-228">16</span></span>                              |
| <span data-ttu-id="7fefc-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fefc-229">Range-Upper</span></span>            | <span data-ttu-id="7fefc-230">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-230">16</span></span>                              |
| <span data-ttu-id="7fefc-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-231">Search-Flags</span></span>           | <span data-ttu-id="7fefc-232">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7fefc-232">0x00000009</span></span>                      |
| <span data-ttu-id="7fefc-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-233">System-Flags</span></span>           | <span data-ttu-id="7fefc-234">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7fefc-234">0x00000013</span></span>                      |
| <span data-ttu-id="7fefc-235">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fefc-235">Classes used in</span></span>        | [<span data-ttu-id="7fefc-236">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7fefc-236">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7fefc-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fefc-237">Windows Server 2008</span></span>



| <span data-ttu-id="7fefc-238">進入</span><span class="sxs-lookup"><span data-stu-id="7fefc-238">Entry</span></span> | <span data-ttu-id="7fefc-239">值</span><span class="sxs-lookup"><span data-stu-id="7fefc-239">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7fefc-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fefc-240">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7fefc-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fefc-241">MAPI-Id</span></span>                | <span data-ttu-id="7fefc-242">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="7fefc-242">0x8C6D</span></span>                          |
| <span data-ttu-id="7fefc-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fefc-243">System-Only</span></span>            | <span data-ttu-id="7fefc-244">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-244">True</span></span>                            |
| <span data-ttu-id="7fefc-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fefc-245">Is-Single-Valued</span></span>       | <span data-ttu-id="7fefc-246">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-246">True</span></span>                            |
| <span data-ttu-id="7fefc-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fefc-247">Is Indexed</span></span>             | <span data-ttu-id="7fefc-248">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-248">True</span></span>                            |
| <span data-ttu-id="7fefc-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fefc-249">In Global Catalog</span></span>      | <span data-ttu-id="7fefc-250">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-250">True</span></span>                            |
| <span data-ttu-id="7fefc-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fefc-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fefc-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fefc-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7fefc-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fefc-253">Range-Lower</span></span>            | <span data-ttu-id="7fefc-254">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-254">16</span></span>                              |
| <span data-ttu-id="7fefc-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fefc-255">Range-Upper</span></span>            | <span data-ttu-id="7fefc-256">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-256">16</span></span>                              |
| <span data-ttu-id="7fefc-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-257">Search-Flags</span></span>           | <span data-ttu-id="7fefc-258">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7fefc-258">0x00000009</span></span>                      |
| <span data-ttu-id="7fefc-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-259">System-Flags</span></span>           | <span data-ttu-id="7fefc-260">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7fefc-260">0x00000013</span></span>                      |
| <span data-ttu-id="7fefc-261">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fefc-261">Classes used in</span></span>        | [<span data-ttu-id="7fefc-262">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7fefc-262">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7fefc-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7fefc-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7fefc-264">進入</span><span class="sxs-lookup"><span data-stu-id="7fefc-264">Entry</span></span> | <span data-ttu-id="7fefc-265">值</span><span class="sxs-lookup"><span data-stu-id="7fefc-265">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7fefc-266">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fefc-266">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7fefc-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fefc-267">MAPI-Id</span></span>                | <span data-ttu-id="7fefc-268">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="7fefc-268">0x8C6D</span></span>                          |
| <span data-ttu-id="7fefc-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fefc-269">System-Only</span></span>            | <span data-ttu-id="7fefc-270">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-270">True</span></span>                            |
| <span data-ttu-id="7fefc-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fefc-271">Is-Single-Valued</span></span>       | <span data-ttu-id="7fefc-272">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-272">True</span></span>                            |
| <span data-ttu-id="7fefc-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fefc-273">Is Indexed</span></span>             | <span data-ttu-id="7fefc-274">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-274">True</span></span>                            |
| <span data-ttu-id="7fefc-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fefc-275">In Global Catalog</span></span>      | <span data-ttu-id="7fefc-276">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-276">True</span></span>                            |
| <span data-ttu-id="7fefc-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fefc-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fefc-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fefc-278">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7fefc-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fefc-279">Range-Lower</span></span>            | <span data-ttu-id="7fefc-280">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-280">16</span></span>                              |
| <span data-ttu-id="7fefc-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fefc-281">Range-Upper</span></span>            | <span data-ttu-id="7fefc-282">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-282">16</span></span>                              |
| <span data-ttu-id="7fefc-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-283">Search-Flags</span></span>           | <span data-ttu-id="7fefc-284">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7fefc-284">0x00000009</span></span>                      |
| <span data-ttu-id="7fefc-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-285">System-Flags</span></span>           | <span data-ttu-id="7fefc-286">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7fefc-286">0x00000013</span></span>                      |
| <span data-ttu-id="7fefc-287">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fefc-287">Classes used in</span></span>        | [<span data-ttu-id="7fefc-288">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7fefc-288">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7fefc-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7fefc-289">Windows Server 2012</span></span>



| <span data-ttu-id="7fefc-290">進入</span><span class="sxs-lookup"><span data-stu-id="7fefc-290">Entry</span></span> | <span data-ttu-id="7fefc-291">值</span><span class="sxs-lookup"><span data-stu-id="7fefc-291">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7fefc-292">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fefc-292">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7fefc-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fefc-293">MAPI-Id</span></span>                | <span data-ttu-id="7fefc-294">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="7fefc-294">0x8C6D</span></span>                          |
| <span data-ttu-id="7fefc-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fefc-295">System-Only</span></span>            | <span data-ttu-id="7fefc-296">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-296">True</span></span>                            |
| <span data-ttu-id="7fefc-297">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fefc-297">Is-Single-Valued</span></span>       | <span data-ttu-id="7fefc-298">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-298">True</span></span>                            |
| <span data-ttu-id="7fefc-299">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fefc-299">Is Indexed</span></span>             | <span data-ttu-id="7fefc-300">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-300">True</span></span>                            |
| <span data-ttu-id="7fefc-301">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fefc-301">In Global Catalog</span></span>      | <span data-ttu-id="7fefc-302">對</span><span class="sxs-lookup"><span data-stu-id="7fefc-302">True</span></span>                            |
| <span data-ttu-id="7fefc-303">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fefc-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fefc-304">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fefc-304">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7fefc-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fefc-305">Range-Lower</span></span>            | <span data-ttu-id="7fefc-306">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-306">16</span></span>                              |
| <span data-ttu-id="7fefc-307">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fefc-307">Range-Upper</span></span>            | <span data-ttu-id="7fefc-308">16</span><span class="sxs-lookup"><span data-stu-id="7fefc-308">16</span></span>                              |
| <span data-ttu-id="7fefc-309">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-309">Search-Flags</span></span>           | <span data-ttu-id="7fefc-310">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7fefc-310">0x00000009</span></span>                      |
| <span data-ttu-id="7fefc-311">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fefc-311">System-Flags</span></span>           | <span data-ttu-id="7fefc-312">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7fefc-312">0x00000013</span></span>                      |
| <span data-ttu-id="7fefc-313">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fefc-313">Classes used in</span></span>        | [<span data-ttu-id="7fefc-314">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7fefc-314">**Top**</span></span>](c-top.md)<br/> |



 

 






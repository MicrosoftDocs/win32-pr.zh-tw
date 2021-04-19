---
title: From-Entry 屬性
description: 如果物件是可寫入的，則此為已建立的屬性，如果是唯讀的，則為 FALSE，例如，GC 複本實例。
ms.assetid: b43e979d-15f9-4425-8a58-c9ed71bab1e4
ms.tgt_platform: multiple
keywords:
- From-Entry 屬性 AD 架構
- fromEntry 屬性 AD 架構
topic_type:
- apiref
api_name:
- From-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5f5e45e2897b917ad442f1b1b5d77246fa079c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971885"
---
# <a name="from-entry-attribute"></a><span data-ttu-id="fb20b-105">From-Entry 屬性</span><span class="sxs-lookup"><span data-stu-id="fb20b-105">From-Entry attribute</span></span>

<span data-ttu-id="fb20b-106">如果物件是可寫入的，則此為已建立的屬性，如果是唯讀的 **，則為** **FALSE** ，例如，GC 複本實例。</span><span class="sxs-lookup"><span data-stu-id="fb20b-106">This is a constructed attribute that is **TRUE** if the object is writable and **FALSE** if it is read-only, for example, a GC replica instance.</span></span>



| <span data-ttu-id="fb20b-107">進入</span><span class="sxs-lookup"><span data-stu-id="fb20b-107">Entry</span></span> | <span data-ttu-id="fb20b-108">值</span><span class="sxs-lookup"><span data-stu-id="fb20b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fb20b-109">CN</span><span class="sxs-lookup"><span data-stu-id="fb20b-109">CN</span></span>                | <span data-ttu-id="fb20b-110">From-Entry</span><span class="sxs-lookup"><span data-stu-id="fb20b-110">From-Entry</span></span>                           |
| <span data-ttu-id="fb20b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fb20b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fb20b-112">fromEntry</span><span class="sxs-lookup"><span data-stu-id="fb20b-112">fromEntry</span></span>                            |
| <span data-ttu-id="fb20b-113">大小</span><span class="sxs-lookup"><span data-stu-id="fb20b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="fb20b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fb20b-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fb20b-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fb20b-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fb20b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fb20b-116">Attribute-Id</span></span>      | <span data-ttu-id="fb20b-117">1.2.840.113556.1.4.910</span><span class="sxs-lookup"><span data-stu-id="fb20b-117">1.2.840.113556.1.4.910</span></span>               |
| <span data-ttu-id="fb20b-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fb20b-118">System-Id-Guid</span></span>    | <span data-ttu-id="fb20b-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="fb20b-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span></span> |
| <span data-ttu-id="fb20b-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb20b-120">Syntax</span></span>            | [<span data-ttu-id="fb20b-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fb20b-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="fb20b-122">實作</span><span class="sxs-lookup"><span data-stu-id="fb20b-122">Implementations</span></span>

-   [<span data-ttu-id="fb20b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fb20b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fb20b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fb20b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fb20b-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="fb20b-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fb20b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fb20b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fb20b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fb20b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fb20b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fb20b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fb20b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fb20b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fb20b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fb20b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="fb20b-131">進入</span><span class="sxs-lookup"><span data-stu-id="fb20b-131">Entry</span></span> | <span data-ttu-id="fb20b-132">值</span><span class="sxs-lookup"><span data-stu-id="fb20b-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fb20b-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb20b-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb20b-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb20b-135">System-Only</span></span>            | <span data-ttu-id="fb20b-136">對</span><span class="sxs-lookup"><span data-stu-id="fb20b-136">True</span></span>                            |
| <span data-ttu-id="fb20b-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb20b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fb20b-138">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-138">False</span></span>                           |
| <span data-ttu-id="fb20b-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb20b-139">Is Indexed</span></span>             | <span data-ttu-id="fb20b-140">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-140">False</span></span>                           |
| <span data-ttu-id="fb20b-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb20b-141">In Global Catalog</span></span>      | <span data-ttu-id="fb20b-142">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-142">False</span></span>                           |
| <span data-ttu-id="fb20b-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb20b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb20b-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb20b-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fb20b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb20b-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fb20b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb20b-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fb20b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-147">Search-Flags</span></span>           | <span data-ttu-id="fb20b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb20b-148">0x00000000</span></span>                      |
| <span data-ttu-id="fb20b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-149">System-Flags</span></span>           | <span data-ttu-id="fb20b-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fb20b-150">0x08000014</span></span>                      |
| <span data-ttu-id="fb20b-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb20b-151">Classes used in</span></span>        | [<span data-ttu-id="fb20b-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fb20b-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fb20b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb20b-153">Windows Server 2003</span></span>



| <span data-ttu-id="fb20b-154">進入</span><span class="sxs-lookup"><span data-stu-id="fb20b-154">Entry</span></span> | <span data-ttu-id="fb20b-155">值</span><span class="sxs-lookup"><span data-stu-id="fb20b-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fb20b-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb20b-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb20b-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb20b-158">System-Only</span></span>            | <span data-ttu-id="fb20b-159">對</span><span class="sxs-lookup"><span data-stu-id="fb20b-159">True</span></span>                            |
| <span data-ttu-id="fb20b-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb20b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="fb20b-161">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-161">False</span></span>                           |
| <span data-ttu-id="fb20b-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb20b-162">Is Indexed</span></span>             | <span data-ttu-id="fb20b-163">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-163">False</span></span>                           |
| <span data-ttu-id="fb20b-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb20b-164">In Global Catalog</span></span>      | <span data-ttu-id="fb20b-165">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-165">False</span></span>                           |
| <span data-ttu-id="fb20b-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb20b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb20b-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb20b-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fb20b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb20b-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fb20b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb20b-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fb20b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-170">Search-Flags</span></span>           | <span data-ttu-id="fb20b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb20b-171">0x00000000</span></span>                      |
| <span data-ttu-id="fb20b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-172">System-Flags</span></span>           | <span data-ttu-id="fb20b-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fb20b-173">0x08000014</span></span>                      |
| <span data-ttu-id="fb20b-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb20b-174">Classes used in</span></span>        | [<span data-ttu-id="fb20b-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fb20b-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fb20b-176">亞當</span><span class="sxs-lookup"><span data-stu-id="fb20b-176">ADAM</span></span>



| <span data-ttu-id="fb20b-177">進入</span><span class="sxs-lookup"><span data-stu-id="fb20b-177">Entry</span></span> | <span data-ttu-id="fb20b-178">值</span><span class="sxs-lookup"><span data-stu-id="fb20b-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fb20b-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb20b-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb20b-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb20b-181">System-Only</span></span>            | <span data-ttu-id="fb20b-182">對</span><span class="sxs-lookup"><span data-stu-id="fb20b-182">True</span></span>                            |
| <span data-ttu-id="fb20b-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb20b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="fb20b-184">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-184">False</span></span>                           |
| <span data-ttu-id="fb20b-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb20b-185">Is Indexed</span></span>             | <span data-ttu-id="fb20b-186">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-186">False</span></span>                           |
| <span data-ttu-id="fb20b-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb20b-187">In Global Catalog</span></span>      | <span data-ttu-id="fb20b-188">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-188">False</span></span>                           |
| <span data-ttu-id="fb20b-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb20b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb20b-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb20b-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fb20b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb20b-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fb20b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb20b-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fb20b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-193">Search-Flags</span></span>           | <span data-ttu-id="fb20b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb20b-194">0x00000000</span></span>                      |
| <span data-ttu-id="fb20b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-195">System-Flags</span></span>           | <span data-ttu-id="fb20b-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fb20b-196">0x08000014</span></span>                      |
| <span data-ttu-id="fb20b-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb20b-197">Classes used in</span></span>        | [<span data-ttu-id="fb20b-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fb20b-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fb20b-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fb20b-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fb20b-200">進入</span><span class="sxs-lookup"><span data-stu-id="fb20b-200">Entry</span></span> | <span data-ttu-id="fb20b-201">值</span><span class="sxs-lookup"><span data-stu-id="fb20b-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fb20b-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb20b-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb20b-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb20b-204">System-Only</span></span>            | <span data-ttu-id="fb20b-205">對</span><span class="sxs-lookup"><span data-stu-id="fb20b-205">True</span></span>                            |
| <span data-ttu-id="fb20b-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb20b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="fb20b-207">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-207">False</span></span>                           |
| <span data-ttu-id="fb20b-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb20b-208">Is Indexed</span></span>             | <span data-ttu-id="fb20b-209">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-209">False</span></span>                           |
| <span data-ttu-id="fb20b-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb20b-210">In Global Catalog</span></span>      | <span data-ttu-id="fb20b-211">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-211">False</span></span>                           |
| <span data-ttu-id="fb20b-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb20b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb20b-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb20b-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fb20b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb20b-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fb20b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb20b-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fb20b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-216">Search-Flags</span></span>           | <span data-ttu-id="fb20b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb20b-217">0x00000000</span></span>                      |
| <span data-ttu-id="fb20b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-218">System-Flags</span></span>           | <span data-ttu-id="fb20b-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fb20b-219">0x08000014</span></span>                      |
| <span data-ttu-id="fb20b-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb20b-220">Classes used in</span></span>        | [<span data-ttu-id="fb20b-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fb20b-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fb20b-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb20b-222">Windows Server 2008</span></span>



| <span data-ttu-id="fb20b-223">進入</span><span class="sxs-lookup"><span data-stu-id="fb20b-223">Entry</span></span> | <span data-ttu-id="fb20b-224">值</span><span class="sxs-lookup"><span data-stu-id="fb20b-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fb20b-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb20b-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb20b-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb20b-227">System-Only</span></span>            | <span data-ttu-id="fb20b-228">對</span><span class="sxs-lookup"><span data-stu-id="fb20b-228">True</span></span>                            |
| <span data-ttu-id="fb20b-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb20b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="fb20b-230">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-230">False</span></span>                           |
| <span data-ttu-id="fb20b-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb20b-231">Is Indexed</span></span>             | <span data-ttu-id="fb20b-232">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-232">False</span></span>                           |
| <span data-ttu-id="fb20b-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb20b-233">In Global Catalog</span></span>      | <span data-ttu-id="fb20b-234">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-234">False</span></span>                           |
| <span data-ttu-id="fb20b-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb20b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb20b-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb20b-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fb20b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb20b-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fb20b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb20b-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fb20b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-239">Search-Flags</span></span>           | <span data-ttu-id="fb20b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb20b-240">0x00000000</span></span>                      |
| <span data-ttu-id="fb20b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-241">System-Flags</span></span>           | <span data-ttu-id="fb20b-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fb20b-242">0x08000014</span></span>                      |
| <span data-ttu-id="fb20b-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb20b-243">Classes used in</span></span>        | [<span data-ttu-id="fb20b-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fb20b-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fb20b-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb20b-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fb20b-246">進入</span><span class="sxs-lookup"><span data-stu-id="fb20b-246">Entry</span></span> | <span data-ttu-id="fb20b-247">值</span><span class="sxs-lookup"><span data-stu-id="fb20b-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fb20b-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb20b-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb20b-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb20b-250">System-Only</span></span>            | <span data-ttu-id="fb20b-251">對</span><span class="sxs-lookup"><span data-stu-id="fb20b-251">True</span></span>                            |
| <span data-ttu-id="fb20b-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb20b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="fb20b-253">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-253">False</span></span>                           |
| <span data-ttu-id="fb20b-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb20b-254">Is Indexed</span></span>             | <span data-ttu-id="fb20b-255">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-255">False</span></span>                           |
| <span data-ttu-id="fb20b-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb20b-256">In Global Catalog</span></span>      | <span data-ttu-id="fb20b-257">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-257">False</span></span>                           |
| <span data-ttu-id="fb20b-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb20b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb20b-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb20b-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fb20b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb20b-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fb20b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb20b-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fb20b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-262">Search-Flags</span></span>           | <span data-ttu-id="fb20b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb20b-263">0x00000000</span></span>                      |
| <span data-ttu-id="fb20b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-264">System-Flags</span></span>           | <span data-ttu-id="fb20b-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fb20b-265">0x08000014</span></span>                      |
| <span data-ttu-id="fb20b-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb20b-266">Classes used in</span></span>        | [<span data-ttu-id="fb20b-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fb20b-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fb20b-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb20b-268">Windows Server 2012</span></span>



| <span data-ttu-id="fb20b-269">進入</span><span class="sxs-lookup"><span data-stu-id="fb20b-269">Entry</span></span> | <span data-ttu-id="fb20b-270">值</span><span class="sxs-lookup"><span data-stu-id="fb20b-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fb20b-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb20b-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb20b-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fb20b-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb20b-273">System-Only</span></span>            | <span data-ttu-id="fb20b-274">對</span><span class="sxs-lookup"><span data-stu-id="fb20b-274">True</span></span>                            |
| <span data-ttu-id="fb20b-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb20b-275">Is-Single-Valued</span></span>       | <span data-ttu-id="fb20b-276">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-276">False</span></span>                           |
| <span data-ttu-id="fb20b-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb20b-277">Is Indexed</span></span>             | <span data-ttu-id="fb20b-278">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-278">False</span></span>                           |
| <span data-ttu-id="fb20b-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb20b-279">In Global Catalog</span></span>      | <span data-ttu-id="fb20b-280">否</span><span class="sxs-lookup"><span data-stu-id="fb20b-280">False</span></span>                           |
| <span data-ttu-id="fb20b-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb20b-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb20b-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb20b-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fb20b-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb20b-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fb20b-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb20b-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fb20b-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-285">Search-Flags</span></span>           | <span data-ttu-id="fb20b-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb20b-286">0x00000000</span></span>                      |
| <span data-ttu-id="fb20b-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb20b-287">System-Flags</span></span>           | <span data-ttu-id="fb20b-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fb20b-288">0x08000014</span></span>                      |
| <span data-ttu-id="fb20b-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb20b-289">Classes used in</span></span>        | [<span data-ttu-id="fb20b-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="fb20b-290">**Top**</span></span>](c-top.md)<br/> |



 

 






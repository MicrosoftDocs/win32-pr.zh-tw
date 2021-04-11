---
title: 建立時間戳記屬性
description: 此物件的建立日期。 此值為已複寫。
ms.assetid: 7b957a44-7185-49fa-a219-7c7f4b3e9fce
ms.tgt_platform: multiple
keywords:
- 建立時間戳記屬性 AD 架構
- createTimeStamp 屬性 AD 架構
topic_type:
- apiref
api_name:
- Create-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66714aeb035667bc858b7a2e888f6334e7d09c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687311"
---
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="1918c-106">建立時間戳記屬性</span><span class="sxs-lookup"><span data-stu-id="1918c-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="1918c-107">此物件的建立日期。</span><span class="sxs-lookup"><span data-stu-id="1918c-107">The date when this object was created.</span></span> <span data-ttu-id="1918c-108">此值為已複寫。</span><span class="sxs-lookup"><span data-stu-id="1918c-108">This value is replicated.</span></span>



| <span data-ttu-id="1918c-109">進入</span><span class="sxs-lookup"><span data-stu-id="1918c-109">Entry</span></span> | <span data-ttu-id="1918c-110">值</span><span class="sxs-lookup"><span data-stu-id="1918c-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="1918c-111">CN</span><span class="sxs-lookup"><span data-stu-id="1918c-111">CN</span></span>                | <span data-ttu-id="1918c-112">建立時間戳記</span><span class="sxs-lookup"><span data-stu-id="1918c-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="1918c-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1918c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1918c-114">createTimeStamp</span><span class="sxs-lookup"><span data-stu-id="1918c-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="1918c-115">大小</span><span class="sxs-lookup"><span data-stu-id="1918c-115">Size</span></span>              | <span data-ttu-id="1918c-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="1918c-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="1918c-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1918c-117">Update Privilege</span></span>  | <span data-ttu-id="1918c-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="1918c-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="1918c-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1918c-119">Update Frequency</span></span>  | <span data-ttu-id="1918c-120">建立物件時。</span><span class="sxs-lookup"><span data-stu-id="1918c-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="1918c-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1918c-121">Attribute-Id</span></span>      | <span data-ttu-id="1918c-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="1918c-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="1918c-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1918c-123">System-Id-Guid</span></span>    | <span data-ttu-id="1918c-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="1918c-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="1918c-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="1918c-125">Syntax</span></span>            | [<span data-ttu-id="1918c-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="1918c-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="1918c-127">實作</span><span class="sxs-lookup"><span data-stu-id="1918c-127">Implementations</span></span>

-   [<span data-ttu-id="1918c-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1918c-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1918c-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1918c-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1918c-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="1918c-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1918c-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1918c-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1918c-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1918c-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1918c-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1918c-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1918c-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1918c-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1918c-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1918c-135">Windows 2000 Server</span></span>



| <span data-ttu-id="1918c-136">進入</span><span class="sxs-lookup"><span data-stu-id="1918c-136">Entry</span></span> | <span data-ttu-id="1918c-137">值</span><span class="sxs-lookup"><span data-stu-id="1918c-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1918c-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1918c-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1918c-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1918c-140">System-Only</span></span>            | <span data-ttu-id="1918c-141">對</span><span class="sxs-lookup"><span data-stu-id="1918c-141">True</span></span>                            |
| <span data-ttu-id="1918c-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1918c-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1918c-143">對</span><span class="sxs-lookup"><span data-stu-id="1918c-143">True</span></span>                            |
| <span data-ttu-id="1918c-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1918c-144">Is Indexed</span></span>             | <span data-ttu-id="1918c-145">否</span><span class="sxs-lookup"><span data-stu-id="1918c-145">False</span></span>                           |
| <span data-ttu-id="1918c-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1918c-146">In Global Catalog</span></span>      | <span data-ttu-id="1918c-147">否</span><span class="sxs-lookup"><span data-stu-id="1918c-147">False</span></span>                           |
| <span data-ttu-id="1918c-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1918c-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1918c-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1918c-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1918c-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1918c-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1918c-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1918c-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1918c-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-152">Search-Flags</span></span>           | <span data-ttu-id="1918c-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1918c-153">0x00000000</span></span>                      |
| <span data-ttu-id="1918c-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-154">System-Flags</span></span>           | <span data-ttu-id="1918c-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1918c-155">0x08000014</span></span>                      |
| <span data-ttu-id="1918c-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1918c-156">Classes used in</span></span>        | [<span data-ttu-id="1918c-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1918c-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1918c-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1918c-158">Windows Server 2003</span></span>



| <span data-ttu-id="1918c-159">進入</span><span class="sxs-lookup"><span data-stu-id="1918c-159">Entry</span></span> | <span data-ttu-id="1918c-160">值</span><span class="sxs-lookup"><span data-stu-id="1918c-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1918c-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1918c-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1918c-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1918c-163">System-Only</span></span>            | <span data-ttu-id="1918c-164">對</span><span class="sxs-lookup"><span data-stu-id="1918c-164">True</span></span>                            |
| <span data-ttu-id="1918c-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1918c-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1918c-166">對</span><span class="sxs-lookup"><span data-stu-id="1918c-166">True</span></span>                            |
| <span data-ttu-id="1918c-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1918c-167">Is Indexed</span></span>             | <span data-ttu-id="1918c-168">否</span><span class="sxs-lookup"><span data-stu-id="1918c-168">False</span></span>                           |
| <span data-ttu-id="1918c-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1918c-169">In Global Catalog</span></span>      | <span data-ttu-id="1918c-170">否</span><span class="sxs-lookup"><span data-stu-id="1918c-170">False</span></span>                           |
| <span data-ttu-id="1918c-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1918c-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1918c-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1918c-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1918c-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1918c-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1918c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1918c-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1918c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-175">Search-Flags</span></span>           | <span data-ttu-id="1918c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1918c-176">0x00000000</span></span>                      |
| <span data-ttu-id="1918c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-177">System-Flags</span></span>           | <span data-ttu-id="1918c-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1918c-178">0x08000014</span></span>                      |
| <span data-ttu-id="1918c-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1918c-179">Classes used in</span></span>        | [<span data-ttu-id="1918c-180">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1918c-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1918c-181">亞當</span><span class="sxs-lookup"><span data-stu-id="1918c-181">ADAM</span></span>



| <span data-ttu-id="1918c-182">進入</span><span class="sxs-lookup"><span data-stu-id="1918c-182">Entry</span></span> | <span data-ttu-id="1918c-183">值</span><span class="sxs-lookup"><span data-stu-id="1918c-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1918c-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1918c-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1918c-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="1918c-186">System-Only</span></span>            | <span data-ttu-id="1918c-187">對</span><span class="sxs-lookup"><span data-stu-id="1918c-187">True</span></span>                            |
| <span data-ttu-id="1918c-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1918c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="1918c-189">對</span><span class="sxs-lookup"><span data-stu-id="1918c-189">True</span></span>                            |
| <span data-ttu-id="1918c-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1918c-190">Is Indexed</span></span>             | <span data-ttu-id="1918c-191">否</span><span class="sxs-lookup"><span data-stu-id="1918c-191">False</span></span>                           |
| <span data-ttu-id="1918c-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1918c-192">In Global Catalog</span></span>      | <span data-ttu-id="1918c-193">否</span><span class="sxs-lookup"><span data-stu-id="1918c-193">False</span></span>                           |
| <span data-ttu-id="1918c-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1918c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="1918c-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1918c-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1918c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1918c-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1918c-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1918c-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1918c-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-198">Search-Flags</span></span>           | <span data-ttu-id="1918c-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1918c-199">0x00000000</span></span>                      |
| <span data-ttu-id="1918c-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-200">System-Flags</span></span>           | <span data-ttu-id="1918c-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1918c-201">0x08000014</span></span>                      |
| <span data-ttu-id="1918c-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1918c-202">Classes used in</span></span>        | [<span data-ttu-id="1918c-203">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1918c-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1918c-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1918c-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1918c-205">進入</span><span class="sxs-lookup"><span data-stu-id="1918c-205">Entry</span></span> | <span data-ttu-id="1918c-206">值</span><span class="sxs-lookup"><span data-stu-id="1918c-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1918c-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1918c-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1918c-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1918c-209">System-Only</span></span>            | <span data-ttu-id="1918c-210">對</span><span class="sxs-lookup"><span data-stu-id="1918c-210">True</span></span>                            |
| <span data-ttu-id="1918c-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1918c-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1918c-212">對</span><span class="sxs-lookup"><span data-stu-id="1918c-212">True</span></span>                            |
| <span data-ttu-id="1918c-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1918c-213">Is Indexed</span></span>             | <span data-ttu-id="1918c-214">否</span><span class="sxs-lookup"><span data-stu-id="1918c-214">False</span></span>                           |
| <span data-ttu-id="1918c-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1918c-215">In Global Catalog</span></span>      | <span data-ttu-id="1918c-216">否</span><span class="sxs-lookup"><span data-stu-id="1918c-216">False</span></span>                           |
| <span data-ttu-id="1918c-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1918c-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1918c-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1918c-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1918c-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1918c-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1918c-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1918c-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1918c-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-221">Search-Flags</span></span>           | <span data-ttu-id="1918c-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1918c-222">0x00000000</span></span>                      |
| <span data-ttu-id="1918c-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-223">System-Flags</span></span>           | <span data-ttu-id="1918c-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1918c-224">0x08000014</span></span>                      |
| <span data-ttu-id="1918c-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1918c-225">Classes used in</span></span>        | [<span data-ttu-id="1918c-226">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1918c-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1918c-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1918c-227">Windows Server 2008</span></span>



| <span data-ttu-id="1918c-228">進入</span><span class="sxs-lookup"><span data-stu-id="1918c-228">Entry</span></span> | <span data-ttu-id="1918c-229">值</span><span class="sxs-lookup"><span data-stu-id="1918c-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1918c-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1918c-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1918c-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="1918c-232">System-Only</span></span>            | <span data-ttu-id="1918c-233">對</span><span class="sxs-lookup"><span data-stu-id="1918c-233">True</span></span>                            |
| <span data-ttu-id="1918c-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1918c-234">Is-Single-Valued</span></span>       | <span data-ttu-id="1918c-235">對</span><span class="sxs-lookup"><span data-stu-id="1918c-235">True</span></span>                            |
| <span data-ttu-id="1918c-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1918c-236">Is Indexed</span></span>             | <span data-ttu-id="1918c-237">否</span><span class="sxs-lookup"><span data-stu-id="1918c-237">False</span></span>                           |
| <span data-ttu-id="1918c-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1918c-238">In Global Catalog</span></span>      | <span data-ttu-id="1918c-239">否</span><span class="sxs-lookup"><span data-stu-id="1918c-239">False</span></span>                           |
| <span data-ttu-id="1918c-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1918c-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="1918c-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1918c-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1918c-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1918c-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1918c-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1918c-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1918c-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-244">Search-Flags</span></span>           | <span data-ttu-id="1918c-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1918c-245">0x00000000</span></span>                      |
| <span data-ttu-id="1918c-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-246">System-Flags</span></span>           | <span data-ttu-id="1918c-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1918c-247">0x08000014</span></span>                      |
| <span data-ttu-id="1918c-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1918c-248">Classes used in</span></span>        | [<span data-ttu-id="1918c-249">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1918c-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1918c-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1918c-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1918c-251">進入</span><span class="sxs-lookup"><span data-stu-id="1918c-251">Entry</span></span> | <span data-ttu-id="1918c-252">值</span><span class="sxs-lookup"><span data-stu-id="1918c-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1918c-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1918c-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1918c-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="1918c-255">System-Only</span></span>            | <span data-ttu-id="1918c-256">對</span><span class="sxs-lookup"><span data-stu-id="1918c-256">True</span></span>                            |
| <span data-ttu-id="1918c-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1918c-257">Is-Single-Valued</span></span>       | <span data-ttu-id="1918c-258">對</span><span class="sxs-lookup"><span data-stu-id="1918c-258">True</span></span>                            |
| <span data-ttu-id="1918c-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1918c-259">Is Indexed</span></span>             | <span data-ttu-id="1918c-260">否</span><span class="sxs-lookup"><span data-stu-id="1918c-260">False</span></span>                           |
| <span data-ttu-id="1918c-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1918c-261">In Global Catalog</span></span>      | <span data-ttu-id="1918c-262">否</span><span class="sxs-lookup"><span data-stu-id="1918c-262">False</span></span>                           |
| <span data-ttu-id="1918c-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1918c-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="1918c-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1918c-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1918c-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1918c-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1918c-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1918c-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1918c-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-267">Search-Flags</span></span>           | <span data-ttu-id="1918c-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1918c-268">0x00000000</span></span>                      |
| <span data-ttu-id="1918c-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-269">System-Flags</span></span>           | <span data-ttu-id="1918c-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1918c-270">0x08000014</span></span>                      |
| <span data-ttu-id="1918c-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1918c-271">Classes used in</span></span>        | [<span data-ttu-id="1918c-272">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1918c-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1918c-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1918c-273">Windows Server 2012</span></span>



| <span data-ttu-id="1918c-274">進入</span><span class="sxs-lookup"><span data-stu-id="1918c-274">Entry</span></span> | <span data-ttu-id="1918c-275">值</span><span class="sxs-lookup"><span data-stu-id="1918c-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1918c-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1918c-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1918c-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1918c-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="1918c-278">System-Only</span></span>            | <span data-ttu-id="1918c-279">對</span><span class="sxs-lookup"><span data-stu-id="1918c-279">True</span></span>                            |
| <span data-ttu-id="1918c-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1918c-280">Is-Single-Valued</span></span>       | <span data-ttu-id="1918c-281">對</span><span class="sxs-lookup"><span data-stu-id="1918c-281">True</span></span>                            |
| <span data-ttu-id="1918c-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1918c-282">Is Indexed</span></span>             | <span data-ttu-id="1918c-283">否</span><span class="sxs-lookup"><span data-stu-id="1918c-283">False</span></span>                           |
| <span data-ttu-id="1918c-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1918c-284">In Global Catalog</span></span>      | <span data-ttu-id="1918c-285">否</span><span class="sxs-lookup"><span data-stu-id="1918c-285">False</span></span>                           |
| <span data-ttu-id="1918c-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1918c-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="1918c-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1918c-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1918c-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1918c-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1918c-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1918c-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1918c-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-290">Search-Flags</span></span>           | <span data-ttu-id="1918c-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1918c-291">0x00000000</span></span>                      |
| <span data-ttu-id="1918c-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1918c-292">System-Flags</span></span>           | <span data-ttu-id="1918c-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1918c-293">0x08000014</span></span>                      |
| <span data-ttu-id="1918c-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1918c-294">Classes used in</span></span>        | [<span data-ttu-id="1918c-295">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1918c-295">**Top**</span></span>](c-top.md)<br/> |



 

 






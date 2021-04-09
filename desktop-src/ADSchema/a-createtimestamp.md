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
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="cdcf6-106">建立時間戳記屬性</span><span class="sxs-lookup"><span data-stu-id="cdcf6-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="cdcf6-107">此物件的建立日期。</span><span class="sxs-lookup"><span data-stu-id="cdcf6-107">The date when this object was created.</span></span> <span data-ttu-id="cdcf6-108">此值為已複寫。</span><span class="sxs-lookup"><span data-stu-id="cdcf6-108">This value is replicated.</span></span>



| <span data-ttu-id="cdcf6-109">進入</span><span class="sxs-lookup"><span data-stu-id="cdcf6-109">Entry</span></span> | <span data-ttu-id="cdcf6-110">值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="cdcf6-111">CN</span><span class="sxs-lookup"><span data-stu-id="cdcf6-111">CN</span></span>                | <span data-ttu-id="cdcf6-112">建立時間戳記</span><span class="sxs-lookup"><span data-stu-id="cdcf6-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="cdcf6-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="cdcf6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cdcf6-114">createTimeStamp</span><span class="sxs-lookup"><span data-stu-id="cdcf6-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="cdcf6-115">大小</span><span class="sxs-lookup"><span data-stu-id="cdcf6-115">Size</span></span>              | <span data-ttu-id="cdcf6-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="cdcf6-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="cdcf6-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="cdcf6-117">Update Privilege</span></span>  | <span data-ttu-id="cdcf6-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="cdcf6-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="cdcf6-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="cdcf6-119">Update Frequency</span></span>  | <span data-ttu-id="cdcf6-120">建立物件時。</span><span class="sxs-lookup"><span data-stu-id="cdcf6-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="cdcf6-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cdcf6-121">Attribute-Id</span></span>      | <span data-ttu-id="cdcf6-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="cdcf6-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="cdcf6-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="cdcf6-123">System-Id-Guid</span></span>    | <span data-ttu-id="cdcf6-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="cdcf6-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="cdcf6-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdcf6-125">Syntax</span></span>            | [<span data-ttu-id="cdcf6-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="cdcf6-127">實作</span><span class="sxs-lookup"><span data-stu-id="cdcf6-127">Implementations</span></span>

-   [<span data-ttu-id="cdcf6-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cdcf6-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cdcf6-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cdcf6-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cdcf6-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cdcf6-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cdcf6-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cdcf6-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cdcf6-135">Windows 2000 Server</span></span>



| <span data-ttu-id="cdcf6-136">進入</span><span class="sxs-lookup"><span data-stu-id="cdcf6-136">Entry</span></span> | <span data-ttu-id="cdcf6-137">值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdcf6-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cdcf6-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdcf6-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdcf6-140">System-Only</span></span>            | <span data-ttu-id="cdcf6-141">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-141">True</span></span>                            |
| <span data-ttu-id="cdcf6-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-142">Is-Single-Valued</span></span>       | <span data-ttu-id="cdcf6-143">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-143">True</span></span>                            |
| <span data-ttu-id="cdcf6-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cdcf6-144">Is Indexed</span></span>             | <span data-ttu-id="cdcf6-145">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-145">False</span></span>                           |
| <span data-ttu-id="cdcf6-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cdcf6-146">In Global Catalog</span></span>      | <span data-ttu-id="cdcf6-147">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-147">False</span></span>                           |
| <span data-ttu-id="cdcf6-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cdcf6-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdcf6-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cdcf6-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdcf6-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdcf6-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdcf6-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-152">Search-Flags</span></span>           | <span data-ttu-id="cdcf6-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdcf6-153">0x00000000</span></span>                      |
| <span data-ttu-id="cdcf6-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-154">System-Flags</span></span>           | <span data-ttu-id="cdcf6-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdcf6-155">0x08000014</span></span>                      |
| <span data-ttu-id="cdcf6-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cdcf6-156">Classes used in</span></span>        | [<span data-ttu-id="cdcf6-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cdcf6-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cdcf6-158">Windows Server 2003</span></span>



| <span data-ttu-id="cdcf6-159">進入</span><span class="sxs-lookup"><span data-stu-id="cdcf6-159">Entry</span></span> | <span data-ttu-id="cdcf6-160">值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdcf6-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cdcf6-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdcf6-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdcf6-163">System-Only</span></span>            | <span data-ttu-id="cdcf6-164">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-164">True</span></span>                            |
| <span data-ttu-id="cdcf6-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-165">Is-Single-Valued</span></span>       | <span data-ttu-id="cdcf6-166">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-166">True</span></span>                            |
| <span data-ttu-id="cdcf6-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cdcf6-167">Is Indexed</span></span>             | <span data-ttu-id="cdcf6-168">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-168">False</span></span>                           |
| <span data-ttu-id="cdcf6-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cdcf6-169">In Global Catalog</span></span>      | <span data-ttu-id="cdcf6-170">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-170">False</span></span>                           |
| <span data-ttu-id="cdcf6-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cdcf6-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdcf6-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cdcf6-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdcf6-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdcf6-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdcf6-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-175">Search-Flags</span></span>           | <span data-ttu-id="cdcf6-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdcf6-176">0x00000000</span></span>                      |
| <span data-ttu-id="cdcf6-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-177">System-Flags</span></span>           | <span data-ttu-id="cdcf6-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdcf6-178">0x08000014</span></span>                      |
| <span data-ttu-id="cdcf6-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cdcf6-179">Classes used in</span></span>        | [<span data-ttu-id="cdcf6-180">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cdcf6-181">亞當</span><span class="sxs-lookup"><span data-stu-id="cdcf6-181">ADAM</span></span>



| <span data-ttu-id="cdcf6-182">進入</span><span class="sxs-lookup"><span data-stu-id="cdcf6-182">Entry</span></span> | <span data-ttu-id="cdcf6-183">值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdcf6-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cdcf6-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdcf6-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdcf6-186">System-Only</span></span>            | <span data-ttu-id="cdcf6-187">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-187">True</span></span>                            |
| <span data-ttu-id="cdcf6-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-188">Is-Single-Valued</span></span>       | <span data-ttu-id="cdcf6-189">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-189">True</span></span>                            |
| <span data-ttu-id="cdcf6-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cdcf6-190">Is Indexed</span></span>             | <span data-ttu-id="cdcf6-191">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-191">False</span></span>                           |
| <span data-ttu-id="cdcf6-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cdcf6-192">In Global Catalog</span></span>      | <span data-ttu-id="cdcf6-193">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-193">False</span></span>                           |
| <span data-ttu-id="cdcf6-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cdcf6-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdcf6-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cdcf6-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdcf6-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdcf6-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdcf6-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-198">Search-Flags</span></span>           | <span data-ttu-id="cdcf6-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdcf6-199">0x00000000</span></span>                      |
| <span data-ttu-id="cdcf6-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-200">System-Flags</span></span>           | <span data-ttu-id="cdcf6-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdcf6-201">0x08000014</span></span>                      |
| <span data-ttu-id="cdcf6-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cdcf6-202">Classes used in</span></span>        | [<span data-ttu-id="cdcf6-203">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cdcf6-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cdcf6-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cdcf6-205">進入</span><span class="sxs-lookup"><span data-stu-id="cdcf6-205">Entry</span></span> | <span data-ttu-id="cdcf6-206">值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdcf6-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cdcf6-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdcf6-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdcf6-209">System-Only</span></span>            | <span data-ttu-id="cdcf6-210">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-210">True</span></span>                            |
| <span data-ttu-id="cdcf6-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-211">Is-Single-Valued</span></span>       | <span data-ttu-id="cdcf6-212">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-212">True</span></span>                            |
| <span data-ttu-id="cdcf6-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cdcf6-213">Is Indexed</span></span>             | <span data-ttu-id="cdcf6-214">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-214">False</span></span>                           |
| <span data-ttu-id="cdcf6-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cdcf6-215">In Global Catalog</span></span>      | <span data-ttu-id="cdcf6-216">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-216">False</span></span>                           |
| <span data-ttu-id="cdcf6-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cdcf6-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdcf6-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cdcf6-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdcf6-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdcf6-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdcf6-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-221">Search-Flags</span></span>           | <span data-ttu-id="cdcf6-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdcf6-222">0x00000000</span></span>                      |
| <span data-ttu-id="cdcf6-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-223">System-Flags</span></span>           | <span data-ttu-id="cdcf6-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdcf6-224">0x08000014</span></span>                      |
| <span data-ttu-id="cdcf6-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cdcf6-225">Classes used in</span></span>        | [<span data-ttu-id="cdcf6-226">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cdcf6-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdcf6-227">Windows Server 2008</span></span>



| <span data-ttu-id="cdcf6-228">進入</span><span class="sxs-lookup"><span data-stu-id="cdcf6-228">Entry</span></span> | <span data-ttu-id="cdcf6-229">值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdcf6-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cdcf6-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdcf6-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdcf6-232">System-Only</span></span>            | <span data-ttu-id="cdcf6-233">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-233">True</span></span>                            |
| <span data-ttu-id="cdcf6-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-234">Is-Single-Valued</span></span>       | <span data-ttu-id="cdcf6-235">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-235">True</span></span>                            |
| <span data-ttu-id="cdcf6-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cdcf6-236">Is Indexed</span></span>             | <span data-ttu-id="cdcf6-237">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-237">False</span></span>                           |
| <span data-ttu-id="cdcf6-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cdcf6-238">In Global Catalog</span></span>      | <span data-ttu-id="cdcf6-239">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-239">False</span></span>                           |
| <span data-ttu-id="cdcf6-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cdcf6-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdcf6-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cdcf6-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdcf6-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdcf6-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdcf6-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-244">Search-Flags</span></span>           | <span data-ttu-id="cdcf6-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdcf6-245">0x00000000</span></span>                      |
| <span data-ttu-id="cdcf6-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-246">System-Flags</span></span>           | <span data-ttu-id="cdcf6-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdcf6-247">0x08000014</span></span>                      |
| <span data-ttu-id="cdcf6-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cdcf6-248">Classes used in</span></span>        | [<span data-ttu-id="cdcf6-249">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cdcf6-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cdcf6-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cdcf6-251">進入</span><span class="sxs-lookup"><span data-stu-id="cdcf6-251">Entry</span></span> | <span data-ttu-id="cdcf6-252">值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdcf6-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cdcf6-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdcf6-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdcf6-255">System-Only</span></span>            | <span data-ttu-id="cdcf6-256">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-256">True</span></span>                            |
| <span data-ttu-id="cdcf6-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-257">Is-Single-Valued</span></span>       | <span data-ttu-id="cdcf6-258">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-258">True</span></span>                            |
| <span data-ttu-id="cdcf6-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cdcf6-259">Is Indexed</span></span>             | <span data-ttu-id="cdcf6-260">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-260">False</span></span>                           |
| <span data-ttu-id="cdcf6-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cdcf6-261">In Global Catalog</span></span>      | <span data-ttu-id="cdcf6-262">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-262">False</span></span>                           |
| <span data-ttu-id="cdcf6-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cdcf6-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdcf6-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cdcf6-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdcf6-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdcf6-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdcf6-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-267">Search-Flags</span></span>           | <span data-ttu-id="cdcf6-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdcf6-268">0x00000000</span></span>                      |
| <span data-ttu-id="cdcf6-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-269">System-Flags</span></span>           | <span data-ttu-id="cdcf6-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdcf6-270">0x08000014</span></span>                      |
| <span data-ttu-id="cdcf6-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cdcf6-271">Classes used in</span></span>        | [<span data-ttu-id="cdcf6-272">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cdcf6-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cdcf6-273">Windows Server 2012</span></span>



| <span data-ttu-id="cdcf6-274">進入</span><span class="sxs-lookup"><span data-stu-id="cdcf6-274">Entry</span></span> | <span data-ttu-id="cdcf6-275">值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cdcf6-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cdcf6-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cdcf6-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cdcf6-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="cdcf6-278">System-Only</span></span>            | <span data-ttu-id="cdcf6-279">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-279">True</span></span>                            |
| <span data-ttu-id="cdcf6-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cdcf6-280">Is-Single-Valued</span></span>       | <span data-ttu-id="cdcf6-281">對</span><span class="sxs-lookup"><span data-stu-id="cdcf6-281">True</span></span>                            |
| <span data-ttu-id="cdcf6-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cdcf6-282">Is Indexed</span></span>             | <span data-ttu-id="cdcf6-283">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-283">False</span></span>                           |
| <span data-ttu-id="cdcf6-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cdcf6-284">In Global Catalog</span></span>      | <span data-ttu-id="cdcf6-285">否</span><span class="sxs-lookup"><span data-stu-id="cdcf6-285">False</span></span>                           |
| <span data-ttu-id="cdcf6-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cdcf6-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="cdcf6-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cdcf6-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cdcf6-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cdcf6-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cdcf6-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cdcf6-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-290">Search-Flags</span></span>           | <span data-ttu-id="cdcf6-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdcf6-291">0x00000000</span></span>                      |
| <span data-ttu-id="cdcf6-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cdcf6-292">System-Flags</span></span>           | <span data-ttu-id="cdcf6-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cdcf6-293">0x08000014</span></span>                      |
| <span data-ttu-id="cdcf6-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cdcf6-294">Classes used in</span></span>        | [<span data-ttu-id="cdcf6-295">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="cdcf6-295">**Top**</span></span>](c-top.md)<br/> |



 

 






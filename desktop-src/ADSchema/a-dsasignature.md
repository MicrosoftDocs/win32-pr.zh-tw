---
title: DSA-Signature 屬性
description: 物件的 DSA-Signature 是要修改物件之最後一個目錄的調用識別碼。
ms.assetid: 7ae65f15-b0c9-4d73-8a65-92c23d0a239b
ms.tgt_platform: multiple
keywords:
- DSA-Signature 屬性 AD 架構
- dSASignature 屬性 AD 架構
topic_type:
- apiref
api_name:
- DSA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfed9e2cb871f3418c8bdbf4401d03c1e78492b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966552"
---
# <a name="dsa-signature-attribute"></a><span data-ttu-id="676b9-105">DSA-Signature 屬性</span><span class="sxs-lookup"><span data-stu-id="676b9-105">DSA-Signature attribute</span></span>

<span data-ttu-id="676b9-106">物件的 DSA-Signature 是要修改物件之最後一個目錄的調用識別碼。</span><span class="sxs-lookup"><span data-stu-id="676b9-106">The DSA-Signature of an object is the Invocation-ID of the last directory to modify the object.</span></span>



| <span data-ttu-id="676b9-107">進入</span><span class="sxs-lookup"><span data-stu-id="676b9-107">Entry</span></span> | <span data-ttu-id="676b9-108">值</span><span class="sxs-lookup"><span data-stu-id="676b9-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="676b9-109">CN</span><span class="sxs-lookup"><span data-stu-id="676b9-109">CN</span></span>                | <span data-ttu-id="676b9-110">DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="676b9-110">DSA-Signature</span></span>                                         |
| <span data-ttu-id="676b9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="676b9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="676b9-112">dSASignature</span><span class="sxs-lookup"><span data-stu-id="676b9-112">dSASignature</span></span>                                          |
| <span data-ttu-id="676b9-113">大小</span><span class="sxs-lookup"><span data-stu-id="676b9-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="676b9-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="676b9-114">Update Privilege</span></span>  | <span data-ttu-id="676b9-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="676b9-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="676b9-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="676b9-116">Update Frequency</span></span>  | <span data-ttu-id="676b9-117">每次修改物件時。</span><span class="sxs-lookup"><span data-stu-id="676b9-117">Whenever an object is modified.</span></span>                       |
| <span data-ttu-id="676b9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="676b9-118">Attribute-Id</span></span>      | <span data-ttu-id="676b9-119">1.2.840.113556.1.2.74</span><span class="sxs-lookup"><span data-stu-id="676b9-119">1.2.840.113556.1.2.74</span></span>                                 |
| <span data-ttu-id="676b9-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="676b9-120">System-Id-Guid</span></span>    | <span data-ttu-id="676b9-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="676b9-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="676b9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="676b9-122">Syntax</span></span>            | [<span data-ttu-id="676b9-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="676b9-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="676b9-124">實作</span><span class="sxs-lookup"><span data-stu-id="676b9-124">Implementations</span></span>

-   [<span data-ttu-id="676b9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="676b9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="676b9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="676b9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="676b9-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="676b9-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="676b9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="676b9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="676b9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="676b9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="676b9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="676b9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="676b9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="676b9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="676b9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="676b9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="676b9-133">進入</span><span class="sxs-lookup"><span data-stu-id="676b9-133">Entry</span></span> | <span data-ttu-id="676b9-134">值</span><span class="sxs-lookup"><span data-stu-id="676b9-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676b9-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="676b9-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676b9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676b9-136">MAPI-Id</span></span>                | <span data-ttu-id="676b9-137">0x8077</span><span class="sxs-lookup"><span data-stu-id="676b9-137">0x8077</span></span>                          |
| <span data-ttu-id="676b9-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="676b9-138">System-Only</span></span>            | <span data-ttu-id="676b9-139">否</span><span class="sxs-lookup"><span data-stu-id="676b9-139">False</span></span>                           |
| <span data-ttu-id="676b9-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="676b9-140">Is-Single-Valued</span></span>       | <span data-ttu-id="676b9-141">對</span><span class="sxs-lookup"><span data-stu-id="676b9-141">True</span></span>                            |
| <span data-ttu-id="676b9-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="676b9-142">Is Indexed</span></span>             | <span data-ttu-id="676b9-143">否</span><span class="sxs-lookup"><span data-stu-id="676b9-143">False</span></span>                           |
| <span data-ttu-id="676b9-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="676b9-144">In Global Catalog</span></span>      | <span data-ttu-id="676b9-145">否</span><span class="sxs-lookup"><span data-stu-id="676b9-145">False</span></span>                           |
| <span data-ttu-id="676b9-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="676b9-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="676b9-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="676b9-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676b9-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676b9-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676b9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676b9-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676b9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-150">Search-Flags</span></span>           | <span data-ttu-id="676b9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676b9-151">0x00000000</span></span>                      |
| <span data-ttu-id="676b9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-152">System-Flags</span></span>           | <span data-ttu-id="676b9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676b9-153">0x00000010</span></span>                      |
| <span data-ttu-id="676b9-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="676b9-154">Classes used in</span></span>        | [<span data-ttu-id="676b9-155">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="676b9-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="676b9-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="676b9-156">Windows Server 2003</span></span>



| <span data-ttu-id="676b9-157">進入</span><span class="sxs-lookup"><span data-stu-id="676b9-157">Entry</span></span> | <span data-ttu-id="676b9-158">值</span><span class="sxs-lookup"><span data-stu-id="676b9-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676b9-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="676b9-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676b9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676b9-160">MAPI-Id</span></span>                | <span data-ttu-id="676b9-161">0x8077</span><span class="sxs-lookup"><span data-stu-id="676b9-161">0x8077</span></span>                          |
| <span data-ttu-id="676b9-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="676b9-162">System-Only</span></span>            | <span data-ttu-id="676b9-163">否</span><span class="sxs-lookup"><span data-stu-id="676b9-163">False</span></span>                           |
| <span data-ttu-id="676b9-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="676b9-164">Is-Single-Valued</span></span>       | <span data-ttu-id="676b9-165">對</span><span class="sxs-lookup"><span data-stu-id="676b9-165">True</span></span>                            |
| <span data-ttu-id="676b9-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="676b9-166">Is Indexed</span></span>             | <span data-ttu-id="676b9-167">否</span><span class="sxs-lookup"><span data-stu-id="676b9-167">False</span></span>                           |
| <span data-ttu-id="676b9-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="676b9-168">In Global Catalog</span></span>      | <span data-ttu-id="676b9-169">否</span><span class="sxs-lookup"><span data-stu-id="676b9-169">False</span></span>                           |
| <span data-ttu-id="676b9-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="676b9-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="676b9-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="676b9-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676b9-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676b9-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676b9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676b9-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676b9-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-174">Search-Flags</span></span>           | <span data-ttu-id="676b9-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676b9-175">0x00000000</span></span>                      |
| <span data-ttu-id="676b9-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-176">System-Flags</span></span>           | <span data-ttu-id="676b9-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676b9-177">0x00000010</span></span>                      |
| <span data-ttu-id="676b9-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="676b9-178">Classes used in</span></span>        | [<span data-ttu-id="676b9-179">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="676b9-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="676b9-180">亞當</span><span class="sxs-lookup"><span data-stu-id="676b9-180">ADAM</span></span>



| <span data-ttu-id="676b9-181">進入</span><span class="sxs-lookup"><span data-stu-id="676b9-181">Entry</span></span> | <span data-ttu-id="676b9-182">值</span><span class="sxs-lookup"><span data-stu-id="676b9-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676b9-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="676b9-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676b9-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676b9-184">MAPI-Id</span></span>                | <span data-ttu-id="676b9-185">0x8077</span><span class="sxs-lookup"><span data-stu-id="676b9-185">0x8077</span></span>                          |
| <span data-ttu-id="676b9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="676b9-186">System-Only</span></span>            | <span data-ttu-id="676b9-187">否</span><span class="sxs-lookup"><span data-stu-id="676b9-187">False</span></span>                           |
| <span data-ttu-id="676b9-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="676b9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="676b9-189">對</span><span class="sxs-lookup"><span data-stu-id="676b9-189">True</span></span>                            |
| <span data-ttu-id="676b9-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="676b9-190">Is Indexed</span></span>             | <span data-ttu-id="676b9-191">否</span><span class="sxs-lookup"><span data-stu-id="676b9-191">False</span></span>                           |
| <span data-ttu-id="676b9-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="676b9-192">In Global Catalog</span></span>      | <span data-ttu-id="676b9-193">否</span><span class="sxs-lookup"><span data-stu-id="676b9-193">False</span></span>                           |
| <span data-ttu-id="676b9-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="676b9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="676b9-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="676b9-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676b9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676b9-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676b9-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676b9-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676b9-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-198">Search-Flags</span></span>           | <span data-ttu-id="676b9-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676b9-199">0x00000000</span></span>                      |
| <span data-ttu-id="676b9-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-200">System-Flags</span></span>           | <span data-ttu-id="676b9-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676b9-201">0x00000010</span></span>                      |
| <span data-ttu-id="676b9-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="676b9-202">Classes used in</span></span>        | [<span data-ttu-id="676b9-203">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="676b9-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="676b9-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="676b9-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="676b9-205">進入</span><span class="sxs-lookup"><span data-stu-id="676b9-205">Entry</span></span> | <span data-ttu-id="676b9-206">值</span><span class="sxs-lookup"><span data-stu-id="676b9-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676b9-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="676b9-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676b9-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676b9-208">MAPI-Id</span></span>                | <span data-ttu-id="676b9-209">0x8077</span><span class="sxs-lookup"><span data-stu-id="676b9-209">0x8077</span></span>                          |
| <span data-ttu-id="676b9-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="676b9-210">System-Only</span></span>            | <span data-ttu-id="676b9-211">否</span><span class="sxs-lookup"><span data-stu-id="676b9-211">False</span></span>                           |
| <span data-ttu-id="676b9-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="676b9-212">Is-Single-Valued</span></span>       | <span data-ttu-id="676b9-213">對</span><span class="sxs-lookup"><span data-stu-id="676b9-213">True</span></span>                            |
| <span data-ttu-id="676b9-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="676b9-214">Is Indexed</span></span>             | <span data-ttu-id="676b9-215">否</span><span class="sxs-lookup"><span data-stu-id="676b9-215">False</span></span>                           |
| <span data-ttu-id="676b9-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="676b9-216">In Global Catalog</span></span>      | <span data-ttu-id="676b9-217">否</span><span class="sxs-lookup"><span data-stu-id="676b9-217">False</span></span>                           |
| <span data-ttu-id="676b9-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="676b9-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="676b9-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="676b9-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676b9-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676b9-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676b9-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676b9-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676b9-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-222">Search-Flags</span></span>           | <span data-ttu-id="676b9-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676b9-223">0x00000000</span></span>                      |
| <span data-ttu-id="676b9-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-224">System-Flags</span></span>           | <span data-ttu-id="676b9-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676b9-225">0x00000010</span></span>                      |
| <span data-ttu-id="676b9-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="676b9-226">Classes used in</span></span>        | [<span data-ttu-id="676b9-227">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="676b9-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="676b9-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="676b9-228">Windows Server 2008</span></span>



| <span data-ttu-id="676b9-229">進入</span><span class="sxs-lookup"><span data-stu-id="676b9-229">Entry</span></span> | <span data-ttu-id="676b9-230">值</span><span class="sxs-lookup"><span data-stu-id="676b9-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676b9-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="676b9-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676b9-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676b9-232">MAPI-Id</span></span>                | <span data-ttu-id="676b9-233">0x8077</span><span class="sxs-lookup"><span data-stu-id="676b9-233">0x8077</span></span>                          |
| <span data-ttu-id="676b9-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="676b9-234">System-Only</span></span>            | <span data-ttu-id="676b9-235">否</span><span class="sxs-lookup"><span data-stu-id="676b9-235">False</span></span>                           |
| <span data-ttu-id="676b9-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="676b9-236">Is-Single-Valued</span></span>       | <span data-ttu-id="676b9-237">對</span><span class="sxs-lookup"><span data-stu-id="676b9-237">True</span></span>                            |
| <span data-ttu-id="676b9-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="676b9-238">Is Indexed</span></span>             | <span data-ttu-id="676b9-239">否</span><span class="sxs-lookup"><span data-stu-id="676b9-239">False</span></span>                           |
| <span data-ttu-id="676b9-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="676b9-240">In Global Catalog</span></span>      | <span data-ttu-id="676b9-241">否</span><span class="sxs-lookup"><span data-stu-id="676b9-241">False</span></span>                           |
| <span data-ttu-id="676b9-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="676b9-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="676b9-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="676b9-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676b9-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676b9-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676b9-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676b9-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676b9-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-246">Search-Flags</span></span>           | <span data-ttu-id="676b9-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676b9-247">0x00000000</span></span>                      |
| <span data-ttu-id="676b9-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-248">System-Flags</span></span>           | <span data-ttu-id="676b9-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676b9-249">0x00000010</span></span>                      |
| <span data-ttu-id="676b9-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="676b9-250">Classes used in</span></span>        | [<span data-ttu-id="676b9-251">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="676b9-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="676b9-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="676b9-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="676b9-253">進入</span><span class="sxs-lookup"><span data-stu-id="676b9-253">Entry</span></span> | <span data-ttu-id="676b9-254">值</span><span class="sxs-lookup"><span data-stu-id="676b9-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676b9-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="676b9-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676b9-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676b9-256">MAPI-Id</span></span>                | <span data-ttu-id="676b9-257">0x8077</span><span class="sxs-lookup"><span data-stu-id="676b9-257">0x8077</span></span>                          |
| <span data-ttu-id="676b9-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="676b9-258">System-Only</span></span>            | <span data-ttu-id="676b9-259">否</span><span class="sxs-lookup"><span data-stu-id="676b9-259">False</span></span>                           |
| <span data-ttu-id="676b9-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="676b9-260">Is-Single-Valued</span></span>       | <span data-ttu-id="676b9-261">對</span><span class="sxs-lookup"><span data-stu-id="676b9-261">True</span></span>                            |
| <span data-ttu-id="676b9-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="676b9-262">Is Indexed</span></span>             | <span data-ttu-id="676b9-263">否</span><span class="sxs-lookup"><span data-stu-id="676b9-263">False</span></span>                           |
| <span data-ttu-id="676b9-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="676b9-264">In Global Catalog</span></span>      | <span data-ttu-id="676b9-265">否</span><span class="sxs-lookup"><span data-stu-id="676b9-265">False</span></span>                           |
| <span data-ttu-id="676b9-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="676b9-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="676b9-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="676b9-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676b9-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676b9-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676b9-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676b9-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676b9-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-270">Search-Flags</span></span>           | <span data-ttu-id="676b9-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676b9-271">0x00000000</span></span>                      |
| <span data-ttu-id="676b9-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-272">System-Flags</span></span>           | <span data-ttu-id="676b9-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676b9-273">0x00000010</span></span>                      |
| <span data-ttu-id="676b9-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="676b9-274">Classes used in</span></span>        | [<span data-ttu-id="676b9-275">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="676b9-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="676b9-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="676b9-276">Windows Server 2012</span></span>



| <span data-ttu-id="676b9-277">進入</span><span class="sxs-lookup"><span data-stu-id="676b9-277">Entry</span></span> | <span data-ttu-id="676b9-278">值</span><span class="sxs-lookup"><span data-stu-id="676b9-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676b9-279">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="676b9-279">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676b9-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676b9-280">MAPI-Id</span></span>                | <span data-ttu-id="676b9-281">0x8077</span><span class="sxs-lookup"><span data-stu-id="676b9-281">0x8077</span></span>                          |
| <span data-ttu-id="676b9-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="676b9-282">System-Only</span></span>            | <span data-ttu-id="676b9-283">否</span><span class="sxs-lookup"><span data-stu-id="676b9-283">False</span></span>                           |
| <span data-ttu-id="676b9-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="676b9-284">Is-Single-Valued</span></span>       | <span data-ttu-id="676b9-285">對</span><span class="sxs-lookup"><span data-stu-id="676b9-285">True</span></span>                            |
| <span data-ttu-id="676b9-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="676b9-286">Is Indexed</span></span>             | <span data-ttu-id="676b9-287">否</span><span class="sxs-lookup"><span data-stu-id="676b9-287">False</span></span>                           |
| <span data-ttu-id="676b9-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="676b9-288">In Global Catalog</span></span>      | <span data-ttu-id="676b9-289">否</span><span class="sxs-lookup"><span data-stu-id="676b9-289">False</span></span>                           |
| <span data-ttu-id="676b9-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="676b9-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="676b9-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="676b9-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676b9-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676b9-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676b9-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676b9-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676b9-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-294">Search-Flags</span></span>           | <span data-ttu-id="676b9-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676b9-295">0x00000000</span></span>                      |
| <span data-ttu-id="676b9-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676b9-296">System-Flags</span></span>           | <span data-ttu-id="676b9-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="676b9-297">0x00000010</span></span>                      |
| <span data-ttu-id="676b9-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="676b9-298">Classes used in</span></span>        | [<span data-ttu-id="676b9-299">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="676b9-299">**Top**</span></span>](c-top.md)<br/> |



 

 






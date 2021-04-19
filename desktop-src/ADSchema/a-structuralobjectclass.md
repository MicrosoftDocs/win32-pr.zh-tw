---
title: 結構物件類別屬性
description: 這個建立的屬性會儲存包含在類別階層中的類別清單，包括抽象類別。 這份清單包含動態連結的輔助類別。
ms.assetid: f7311cb9-4816-4caa-9cae-cbcd61b93d27
ms.tgt_platform: multiple
keywords:
- 結構物件類別屬性 AD 架構
- structuralObjectClass 屬性 AD 架構
topic_type:
- apiref
api_name:
- Structural-Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdcc236c0c65aa365400894dd6ccfb845af04b55
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966988"
---
# <a name="structural-object-class-attribute"></a><span data-ttu-id="ed2fc-106">結構物件類別屬性</span><span class="sxs-lookup"><span data-stu-id="ed2fc-106">Structural-Object-Class attribute</span></span>

<span data-ttu-id="ed2fc-107">這個建立的屬性會儲存包含在類別階層中的類別清單，包括抽象類別。</span><span class="sxs-lookup"><span data-stu-id="ed2fc-107">This constructed attribute stores a list of classes contained in a class hierarchy, including abstract classes.</span></span> <span data-ttu-id="ed2fc-108">這份清單包含動態連結的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="ed2fc-108">This list does contain dynamically linked auxiliary classes.</span></span>



| <span data-ttu-id="ed2fc-109">進入</span><span class="sxs-lookup"><span data-stu-id="ed2fc-109">Entry</span></span> | <span data-ttu-id="ed2fc-110">值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ed2fc-111">CN</span><span class="sxs-lookup"><span data-stu-id="ed2fc-111">CN</span></span>                | <span data-ttu-id="ed2fc-112">結構物件類別</span><span class="sxs-lookup"><span data-stu-id="ed2fc-112">Structural-Object-Class</span></span>                                         |
| <span data-ttu-id="ed2fc-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ed2fc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ed2fc-114">structuralObjectClass</span><span class="sxs-lookup"><span data-stu-id="ed2fc-114">structuralObjectClass</span></span>                                           |
| <span data-ttu-id="ed2fc-115">大小</span><span class="sxs-lookup"><span data-stu-id="ed2fc-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="ed2fc-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ed2fc-116">Update Privilege</span></span>  | <span data-ttu-id="ed2fc-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="ed2fc-117">This value is set by the system.</span></span>                                |
| <span data-ttu-id="ed2fc-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ed2fc-118">Update Frequency</span></span>  | <span data-ttu-id="ed2fc-119">在類別建立時。</span><span class="sxs-lookup"><span data-stu-id="ed2fc-119">At class creation.</span></span>                                              |
| <span data-ttu-id="ed2fc-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ed2fc-120">Attribute-Id</span></span>      | <span data-ttu-id="ed2fc-121">2.5.21.9</span><span class="sxs-lookup"><span data-stu-id="ed2fc-121">2.5.21.9</span></span>                                                        |
| <span data-ttu-id="ed2fc-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ed2fc-122">System-Id-Guid</span></span>    | <span data-ttu-id="ed2fc-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span><span class="sxs-lookup"><span data-stu-id="ed2fc-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span></span>                            |
| <span data-ttu-id="ed2fc-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed2fc-124">Syntax</span></span>            | [<span data-ttu-id="ed2fc-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="ed2fc-126">實作</span><span class="sxs-lookup"><span data-stu-id="ed2fc-126">Implementations</span></span>

-   [<span data-ttu-id="ed2fc-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ed2fc-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ed2fc-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ed2fc-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ed2fc-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ed2fc-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ed2fc-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ed2fc-133">Windows Server 2003</span></span>



| <span data-ttu-id="ed2fc-134">進入</span><span class="sxs-lookup"><span data-stu-id="ed2fc-134">Entry</span></span> | <span data-ttu-id="ed2fc-135">值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ed2fc-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed2fc-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed2fc-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed2fc-138">System-Only</span></span>            | <span data-ttu-id="ed2fc-139">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-139">False</span></span>                           |
| <span data-ttu-id="ed2fc-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ed2fc-141">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-141">False</span></span>                           |
| <span data-ttu-id="ed2fc-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed2fc-142">Is Indexed</span></span>             | <span data-ttu-id="ed2fc-143">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-143">False</span></span>                           |
| <span data-ttu-id="ed2fc-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed2fc-144">In Global Catalog</span></span>      | <span data-ttu-id="ed2fc-145">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-145">False</span></span>                           |
| <span data-ttu-id="ed2fc-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed2fc-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed2fc-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed2fc-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ed2fc-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed2fc-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed2fc-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-150">Search-Flags</span></span>           | <span data-ttu-id="ed2fc-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed2fc-151">0x00000000</span></span>                      |
| <span data-ttu-id="ed2fc-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-152">System-Flags</span></span>           | <span data-ttu-id="ed2fc-153">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ed2fc-153">0x00000014</span></span>                      |
| <span data-ttu-id="ed2fc-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed2fc-154">Classes used in</span></span>        | [<span data-ttu-id="ed2fc-155">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ed2fc-156">亞當</span><span class="sxs-lookup"><span data-stu-id="ed2fc-156">ADAM</span></span>



| <span data-ttu-id="ed2fc-157">進入</span><span class="sxs-lookup"><span data-stu-id="ed2fc-157">Entry</span></span> | <span data-ttu-id="ed2fc-158">值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ed2fc-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed2fc-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed2fc-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed2fc-161">System-Only</span></span>            | <span data-ttu-id="ed2fc-162">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-162">False</span></span>                           |
| <span data-ttu-id="ed2fc-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ed2fc-164">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-164">False</span></span>                           |
| <span data-ttu-id="ed2fc-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed2fc-165">Is Indexed</span></span>             | <span data-ttu-id="ed2fc-166">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-166">False</span></span>                           |
| <span data-ttu-id="ed2fc-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed2fc-167">In Global Catalog</span></span>      | <span data-ttu-id="ed2fc-168">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-168">False</span></span>                           |
| <span data-ttu-id="ed2fc-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed2fc-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed2fc-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed2fc-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ed2fc-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed2fc-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed2fc-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-173">Search-Flags</span></span>           | <span data-ttu-id="ed2fc-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed2fc-174">0x00000000</span></span>                      |
| <span data-ttu-id="ed2fc-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-175">System-Flags</span></span>           | <span data-ttu-id="ed2fc-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ed2fc-176">0x00000014</span></span>                      |
| <span data-ttu-id="ed2fc-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed2fc-177">Classes used in</span></span>        | [<span data-ttu-id="ed2fc-178">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ed2fc-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ed2fc-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ed2fc-180">進入</span><span class="sxs-lookup"><span data-stu-id="ed2fc-180">Entry</span></span> | <span data-ttu-id="ed2fc-181">值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ed2fc-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed2fc-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed2fc-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed2fc-184">System-Only</span></span>            | <span data-ttu-id="ed2fc-185">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-185">False</span></span>                           |
| <span data-ttu-id="ed2fc-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ed2fc-187">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-187">False</span></span>                           |
| <span data-ttu-id="ed2fc-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed2fc-188">Is Indexed</span></span>             | <span data-ttu-id="ed2fc-189">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-189">False</span></span>                           |
| <span data-ttu-id="ed2fc-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed2fc-190">In Global Catalog</span></span>      | <span data-ttu-id="ed2fc-191">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-191">False</span></span>                           |
| <span data-ttu-id="ed2fc-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed2fc-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed2fc-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed2fc-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ed2fc-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed2fc-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed2fc-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-196">Search-Flags</span></span>           | <span data-ttu-id="ed2fc-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed2fc-197">0x00000000</span></span>                      |
| <span data-ttu-id="ed2fc-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-198">System-Flags</span></span>           | <span data-ttu-id="ed2fc-199">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ed2fc-199">0x00000014</span></span>                      |
| <span data-ttu-id="ed2fc-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed2fc-200">Classes used in</span></span>        | [<span data-ttu-id="ed2fc-201">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ed2fc-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed2fc-202">Windows Server 2008</span></span>



| <span data-ttu-id="ed2fc-203">進入</span><span class="sxs-lookup"><span data-stu-id="ed2fc-203">Entry</span></span> | <span data-ttu-id="ed2fc-204">值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ed2fc-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed2fc-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed2fc-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed2fc-207">System-Only</span></span>            | <span data-ttu-id="ed2fc-208">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-208">False</span></span>                           |
| <span data-ttu-id="ed2fc-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-209">Is-Single-Valued</span></span>       | <span data-ttu-id="ed2fc-210">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-210">False</span></span>                           |
| <span data-ttu-id="ed2fc-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed2fc-211">Is Indexed</span></span>             | <span data-ttu-id="ed2fc-212">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-212">False</span></span>                           |
| <span data-ttu-id="ed2fc-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed2fc-213">In Global Catalog</span></span>      | <span data-ttu-id="ed2fc-214">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-214">False</span></span>                           |
| <span data-ttu-id="ed2fc-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed2fc-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed2fc-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed2fc-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ed2fc-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed2fc-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed2fc-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-219">Search-Flags</span></span>           | <span data-ttu-id="ed2fc-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed2fc-220">0x00000000</span></span>                      |
| <span data-ttu-id="ed2fc-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-221">System-Flags</span></span>           | <span data-ttu-id="ed2fc-222">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ed2fc-222">0x00000014</span></span>                      |
| <span data-ttu-id="ed2fc-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed2fc-223">Classes used in</span></span>        | [<span data-ttu-id="ed2fc-224">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ed2fc-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ed2fc-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ed2fc-226">進入</span><span class="sxs-lookup"><span data-stu-id="ed2fc-226">Entry</span></span> | <span data-ttu-id="ed2fc-227">值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ed2fc-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed2fc-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed2fc-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed2fc-230">System-Only</span></span>            | <span data-ttu-id="ed2fc-231">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-231">False</span></span>                           |
| <span data-ttu-id="ed2fc-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-232">Is-Single-Valued</span></span>       | <span data-ttu-id="ed2fc-233">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-233">False</span></span>                           |
| <span data-ttu-id="ed2fc-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed2fc-234">Is Indexed</span></span>             | <span data-ttu-id="ed2fc-235">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-235">False</span></span>                           |
| <span data-ttu-id="ed2fc-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed2fc-236">In Global Catalog</span></span>      | <span data-ttu-id="ed2fc-237">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-237">False</span></span>                           |
| <span data-ttu-id="ed2fc-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed2fc-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed2fc-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed2fc-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ed2fc-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed2fc-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed2fc-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-242">Search-Flags</span></span>           | <span data-ttu-id="ed2fc-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed2fc-243">0x00000000</span></span>                      |
| <span data-ttu-id="ed2fc-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-244">System-Flags</span></span>           | <span data-ttu-id="ed2fc-245">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ed2fc-245">0x00000014</span></span>                      |
| <span data-ttu-id="ed2fc-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed2fc-246">Classes used in</span></span>        | [<span data-ttu-id="ed2fc-247">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ed2fc-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed2fc-248">Windows Server 2012</span></span>



| <span data-ttu-id="ed2fc-249">進入</span><span class="sxs-lookup"><span data-stu-id="ed2fc-249">Entry</span></span> | <span data-ttu-id="ed2fc-250">值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ed2fc-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed2fc-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed2fc-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ed2fc-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed2fc-253">System-Only</span></span>            | <span data-ttu-id="ed2fc-254">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-254">False</span></span>                           |
| <span data-ttu-id="ed2fc-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed2fc-255">Is-Single-Valued</span></span>       | <span data-ttu-id="ed2fc-256">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-256">False</span></span>                           |
| <span data-ttu-id="ed2fc-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed2fc-257">Is Indexed</span></span>             | <span data-ttu-id="ed2fc-258">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-258">False</span></span>                           |
| <span data-ttu-id="ed2fc-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed2fc-259">In Global Catalog</span></span>      | <span data-ttu-id="ed2fc-260">否</span><span class="sxs-lookup"><span data-stu-id="ed2fc-260">False</span></span>                           |
| <span data-ttu-id="ed2fc-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed2fc-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed2fc-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed2fc-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ed2fc-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed2fc-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed2fc-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ed2fc-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-265">Search-Flags</span></span>           | <span data-ttu-id="ed2fc-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed2fc-266">0x00000000</span></span>                      |
| <span data-ttu-id="ed2fc-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed2fc-267">System-Flags</span></span>           | <span data-ttu-id="ed2fc-268">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ed2fc-268">0x00000014</span></span>                      |
| <span data-ttu-id="ed2fc-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed2fc-269">Classes used in</span></span>        | [<span data-ttu-id="ed2fc-270">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ed2fc-270">**Top**</span></span>](c-top.md)<br/> |



 

 






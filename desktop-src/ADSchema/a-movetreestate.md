---
title: 移動樹狀結構狀態屬性
description: 此屬性包含正在移動之目錄樹狀結構的狀態資訊。
ms.assetid: 13ec6d05-ed17-4a38-b2ae-7ad175f17b52
ms.tgt_platform: multiple
keywords:
- 移動樹狀結構狀態屬性 AD 架構
- moveTreeState 屬性 AD 架構
topic_type:
- apiref
api_name:
- Move-Tree-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3041d54dfcdb97d7c9e1629162908fab1577b60c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467296"
---
# <a name="move-tree-state-attribute"></a><span data-ttu-id="dcad5-105">移動樹狀結構狀態屬性</span><span class="sxs-lookup"><span data-stu-id="dcad5-105">Move-Tree-State attribute</span></span>

<span data-ttu-id="dcad5-106">此屬性包含正在移動之目錄樹狀結構的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="dcad5-106">This attribute contains state information for a directory tree that is being moved.</span></span>



| <span data-ttu-id="dcad5-107">進入</span><span class="sxs-lookup"><span data-stu-id="dcad5-107">Entry</span></span> | <span data-ttu-id="dcad5-108">值</span><span class="sxs-lookup"><span data-stu-id="dcad5-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="dcad5-109">CN</span><span class="sxs-lookup"><span data-stu-id="dcad5-109">CN</span></span>                | <span data-ttu-id="dcad5-110">移動樹狀結構狀態</span><span class="sxs-lookup"><span data-stu-id="dcad5-110">Move-Tree-State</span></span>                                       |
| <span data-ttu-id="dcad5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dcad5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dcad5-112">moveTreeState</span><span class="sxs-lookup"><span data-stu-id="dcad5-112">moveTreeState</span></span>                                         |
| <span data-ttu-id="dcad5-113">大小</span><span class="sxs-lookup"><span data-stu-id="dcad5-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="dcad5-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dcad5-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="dcad5-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dcad5-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="dcad5-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dcad5-116">Attribute-Id</span></span>      | <span data-ttu-id="dcad5-117">1.2.840.113556.1.4.1305</span><span class="sxs-lookup"><span data-stu-id="dcad5-117">1.2.840.113556.1.4.1305</span></span>                               |
| <span data-ttu-id="dcad5-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dcad5-118">System-Id-Guid</span></span>    | <span data-ttu-id="dcad5-119">1f2ac2c8-3b71-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="dcad5-119">1f2ac2c8-3b71-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="dcad5-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcad5-120">Syntax</span></span>            | [<span data-ttu-id="dcad5-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="dcad5-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="dcad5-122">實作</span><span class="sxs-lookup"><span data-stu-id="dcad5-122">Implementations</span></span>

-   [<span data-ttu-id="dcad5-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dcad5-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dcad5-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dcad5-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dcad5-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="dcad5-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dcad5-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dcad5-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dcad5-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dcad5-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dcad5-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dcad5-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dcad5-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dcad5-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dcad5-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dcad5-130">Windows 2000 Server</span></span>



| <span data-ttu-id="dcad5-131">進入</span><span class="sxs-lookup"><span data-stu-id="dcad5-131">Entry</span></span> | <span data-ttu-id="dcad5-132">值</span><span class="sxs-lookup"><span data-stu-id="dcad5-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="dcad5-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dcad5-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcad5-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcad5-135">System-Only</span></span>            | <span data-ttu-id="dcad5-136">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-136">False</span></span>                                               |
| <span data-ttu-id="dcad5-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dcad5-137">Is-Single-Valued</span></span>       | <span data-ttu-id="dcad5-138">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-138">False</span></span>                                               |
| <span data-ttu-id="dcad5-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dcad5-139">Is Indexed</span></span>             | <span data-ttu-id="dcad5-140">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-140">False</span></span>                                               |
| <span data-ttu-id="dcad5-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dcad5-141">In Global Catalog</span></span>      | <span data-ttu-id="dcad5-142">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-142">False</span></span>                                               |
| <span data-ttu-id="dcad5-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dcad5-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcad5-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dcad5-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="dcad5-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcad5-145">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcad5-146">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-147">Search-Flags</span></span>           | <span data-ttu-id="dcad5-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcad5-148">0x00000000</span></span>                                          |
| <span data-ttu-id="dcad5-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-149">System-Flags</span></span>           | <span data-ttu-id="dcad5-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcad5-150">0x00000010</span></span>                                          |
| <span data-ttu-id="dcad5-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dcad5-151">Classes used in</span></span>        | [<span data-ttu-id="dcad5-152">**遺失並找出**</span><span class="sxs-lookup"><span data-stu-id="dcad5-152">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dcad5-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dcad5-153">Windows Server 2003</span></span>



| <span data-ttu-id="dcad5-154">進入</span><span class="sxs-lookup"><span data-stu-id="dcad5-154">Entry</span></span> | <span data-ttu-id="dcad5-155">值</span><span class="sxs-lookup"><span data-stu-id="dcad5-155">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="dcad5-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dcad5-156">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcad5-157">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcad5-158">System-Only</span></span>            | <span data-ttu-id="dcad5-159">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-159">False</span></span>                                               |
| <span data-ttu-id="dcad5-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dcad5-160">Is-Single-Valued</span></span>       | <span data-ttu-id="dcad5-161">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-161">False</span></span>                                               |
| <span data-ttu-id="dcad5-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dcad5-162">Is Indexed</span></span>             | <span data-ttu-id="dcad5-163">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-163">False</span></span>                                               |
| <span data-ttu-id="dcad5-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dcad5-164">In Global Catalog</span></span>      | <span data-ttu-id="dcad5-165">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-165">False</span></span>                                               |
| <span data-ttu-id="dcad5-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dcad5-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcad5-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dcad5-167">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="dcad5-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcad5-168">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcad5-169">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-170">Search-Flags</span></span>           | <span data-ttu-id="dcad5-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcad5-171">0x00000000</span></span>                                          |
| <span data-ttu-id="dcad5-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-172">System-Flags</span></span>           | <span data-ttu-id="dcad5-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcad5-173">0x00000010</span></span>                                          |
| <span data-ttu-id="dcad5-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dcad5-174">Classes used in</span></span>        | [<span data-ttu-id="dcad5-175">**遺失並找出**</span><span class="sxs-lookup"><span data-stu-id="dcad5-175">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dcad5-176">亞當</span><span class="sxs-lookup"><span data-stu-id="dcad5-176">ADAM</span></span>



| <span data-ttu-id="dcad5-177">進入</span><span class="sxs-lookup"><span data-stu-id="dcad5-177">Entry</span></span> | <span data-ttu-id="dcad5-178">值</span><span class="sxs-lookup"><span data-stu-id="dcad5-178">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="dcad5-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dcad5-179">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcad5-180">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcad5-181">System-Only</span></span>            | <span data-ttu-id="dcad5-182">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-182">False</span></span>                                               |
| <span data-ttu-id="dcad5-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dcad5-183">Is-Single-Valued</span></span>       | <span data-ttu-id="dcad5-184">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-184">False</span></span>                                               |
| <span data-ttu-id="dcad5-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dcad5-185">Is Indexed</span></span>             | <span data-ttu-id="dcad5-186">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-186">False</span></span>                                               |
| <span data-ttu-id="dcad5-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dcad5-187">In Global Catalog</span></span>      | <span data-ttu-id="dcad5-188">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-188">False</span></span>                                               |
| <span data-ttu-id="dcad5-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dcad5-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcad5-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dcad5-190">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="dcad5-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcad5-191">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcad5-192">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-193">Search-Flags</span></span>           | <span data-ttu-id="dcad5-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcad5-194">0x00000000</span></span>                                          |
| <span data-ttu-id="dcad5-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-195">System-Flags</span></span>           | <span data-ttu-id="dcad5-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcad5-196">0x00000010</span></span>                                          |
| <span data-ttu-id="dcad5-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dcad5-197">Classes used in</span></span>        | [<span data-ttu-id="dcad5-198">**遺失並找出**</span><span class="sxs-lookup"><span data-stu-id="dcad5-198">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dcad5-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dcad5-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dcad5-200">進入</span><span class="sxs-lookup"><span data-stu-id="dcad5-200">Entry</span></span> | <span data-ttu-id="dcad5-201">值</span><span class="sxs-lookup"><span data-stu-id="dcad5-201">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="dcad5-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dcad5-202">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcad5-203">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcad5-204">System-Only</span></span>            | <span data-ttu-id="dcad5-205">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-205">False</span></span>                                               |
| <span data-ttu-id="dcad5-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dcad5-206">Is-Single-Valued</span></span>       | <span data-ttu-id="dcad5-207">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-207">False</span></span>                                               |
| <span data-ttu-id="dcad5-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dcad5-208">Is Indexed</span></span>             | <span data-ttu-id="dcad5-209">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-209">False</span></span>                                               |
| <span data-ttu-id="dcad5-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dcad5-210">In Global Catalog</span></span>      | <span data-ttu-id="dcad5-211">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-211">False</span></span>                                               |
| <span data-ttu-id="dcad5-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dcad5-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcad5-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dcad5-213">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="dcad5-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcad5-214">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcad5-215">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-216">Search-Flags</span></span>           | <span data-ttu-id="dcad5-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcad5-217">0x00000000</span></span>                                          |
| <span data-ttu-id="dcad5-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-218">System-Flags</span></span>           | <span data-ttu-id="dcad5-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcad5-219">0x00000010</span></span>                                          |
| <span data-ttu-id="dcad5-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dcad5-220">Classes used in</span></span>        | [<span data-ttu-id="dcad5-221">**遺失並找出**</span><span class="sxs-lookup"><span data-stu-id="dcad5-221">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dcad5-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcad5-222">Windows Server 2008</span></span>



| <span data-ttu-id="dcad5-223">進入</span><span class="sxs-lookup"><span data-stu-id="dcad5-223">Entry</span></span> | <span data-ttu-id="dcad5-224">值</span><span class="sxs-lookup"><span data-stu-id="dcad5-224">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="dcad5-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dcad5-225">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcad5-226">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcad5-227">System-Only</span></span>            | <span data-ttu-id="dcad5-228">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-228">False</span></span>                                               |
| <span data-ttu-id="dcad5-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dcad5-229">Is-Single-Valued</span></span>       | <span data-ttu-id="dcad5-230">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-230">False</span></span>                                               |
| <span data-ttu-id="dcad5-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dcad5-231">Is Indexed</span></span>             | <span data-ttu-id="dcad5-232">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-232">False</span></span>                                               |
| <span data-ttu-id="dcad5-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dcad5-233">In Global Catalog</span></span>      | <span data-ttu-id="dcad5-234">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-234">False</span></span>                                               |
| <span data-ttu-id="dcad5-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dcad5-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcad5-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dcad5-236">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="dcad5-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcad5-237">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcad5-238">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-239">Search-Flags</span></span>           | <span data-ttu-id="dcad5-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcad5-240">0x00000000</span></span>                                          |
| <span data-ttu-id="dcad5-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-241">System-Flags</span></span>           | <span data-ttu-id="dcad5-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcad5-242">0x00000010</span></span>                                          |
| <span data-ttu-id="dcad5-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dcad5-243">Classes used in</span></span>        | [<span data-ttu-id="dcad5-244">**遺失並找出**</span><span class="sxs-lookup"><span data-stu-id="dcad5-244">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dcad5-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dcad5-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dcad5-246">進入</span><span class="sxs-lookup"><span data-stu-id="dcad5-246">Entry</span></span> | <span data-ttu-id="dcad5-247">值</span><span class="sxs-lookup"><span data-stu-id="dcad5-247">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="dcad5-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dcad5-248">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcad5-249">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcad5-250">System-Only</span></span>            | <span data-ttu-id="dcad5-251">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-251">False</span></span>                                               |
| <span data-ttu-id="dcad5-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dcad5-252">Is-Single-Valued</span></span>       | <span data-ttu-id="dcad5-253">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-253">False</span></span>                                               |
| <span data-ttu-id="dcad5-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dcad5-254">Is Indexed</span></span>             | <span data-ttu-id="dcad5-255">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-255">False</span></span>                                               |
| <span data-ttu-id="dcad5-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dcad5-256">In Global Catalog</span></span>      | <span data-ttu-id="dcad5-257">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-257">False</span></span>                                               |
| <span data-ttu-id="dcad5-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dcad5-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcad5-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dcad5-259">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="dcad5-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcad5-260">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcad5-261">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-262">Search-Flags</span></span>           | <span data-ttu-id="dcad5-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcad5-263">0x00000000</span></span>                                          |
| <span data-ttu-id="dcad5-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-264">System-Flags</span></span>           | <span data-ttu-id="dcad5-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcad5-265">0x00000010</span></span>                                          |
| <span data-ttu-id="dcad5-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dcad5-266">Classes used in</span></span>        | [<span data-ttu-id="dcad5-267">**遺失並找出**</span><span class="sxs-lookup"><span data-stu-id="dcad5-267">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dcad5-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dcad5-268">Windows Server 2012</span></span>



| <span data-ttu-id="dcad5-269">進入</span><span class="sxs-lookup"><span data-stu-id="dcad5-269">Entry</span></span> | <span data-ttu-id="dcad5-270">值</span><span class="sxs-lookup"><span data-stu-id="dcad5-270">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="dcad5-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dcad5-271">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dcad5-272">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="dcad5-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="dcad5-273">System-Only</span></span>            | <span data-ttu-id="dcad5-274">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-274">False</span></span>                                               |
| <span data-ttu-id="dcad5-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dcad5-275">Is-Single-Valued</span></span>       | <span data-ttu-id="dcad5-276">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-276">False</span></span>                                               |
| <span data-ttu-id="dcad5-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dcad5-277">Is Indexed</span></span>             | <span data-ttu-id="dcad5-278">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-278">False</span></span>                                               |
| <span data-ttu-id="dcad5-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dcad5-279">In Global Catalog</span></span>      | <span data-ttu-id="dcad5-280">否</span><span class="sxs-lookup"><span data-stu-id="dcad5-280">False</span></span>                                               |
| <span data-ttu-id="dcad5-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dcad5-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="dcad5-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dcad5-282">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="dcad5-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dcad5-283">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dcad5-284">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="dcad5-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-285">Search-Flags</span></span>           | <span data-ttu-id="dcad5-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dcad5-286">0x00000000</span></span>                                          |
| <span data-ttu-id="dcad5-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dcad5-287">System-Flags</span></span>           | <span data-ttu-id="dcad5-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dcad5-288">0x00000010</span></span>                                          |
| <span data-ttu-id="dcad5-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dcad5-289">Classes used in</span></span>        | [<span data-ttu-id="dcad5-290">**遺失並找出**</span><span class="sxs-lookup"><span data-stu-id="dcad5-290">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



 

 






---
title: Reps-To 屬性
description: 列出目錄將會通知變更的伺服器，以及目錄將對定義之命名內容的要求傳送變更的伺服器。
ms.assetid: d7fd5a57-a0e1-4c69-9b9a-1cdad87610b1
ms.tgt_platform: multiple
keywords:
- Reps-To 屬性 AD 架構
- repsTo 屬性 AD 架構
topic_type:
- apiref
api_name:
- Reps-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5c39d19eb12bb801d7ca7fb9b22ed665d59d10
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935496"
---
# <a name="reps-to-attribute"></a><span data-ttu-id="72e18-105">Reps-To 屬性</span><span class="sxs-lookup"><span data-stu-id="72e18-105">Reps-To attribute</span></span>

<span data-ttu-id="72e18-106">列出目錄將會通知變更的伺服器，以及目錄將對定義之命名內容的要求傳送變更的伺服器。</span><span class="sxs-lookup"><span data-stu-id="72e18-106">Lists the servers that the directory will notify of changes and servers to which the directory will send changes on Request for the defined naming context.</span></span>



| <span data-ttu-id="72e18-107">進入</span><span class="sxs-lookup"><span data-stu-id="72e18-107">Entry</span></span> | <span data-ttu-id="72e18-108">值</span><span class="sxs-lookup"><span data-stu-id="72e18-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="72e18-109">CN</span><span class="sxs-lookup"><span data-stu-id="72e18-109">CN</span></span>                | <span data-ttu-id="72e18-110">Reps-To</span><span class="sxs-lookup"><span data-stu-id="72e18-110">Reps-To</span></span>                                               |
| <span data-ttu-id="72e18-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="72e18-111">Ldap-Display-Name</span></span> | <span data-ttu-id="72e18-112">repsTo</span><span class="sxs-lookup"><span data-stu-id="72e18-112">repsTo</span></span>                                                |
| <span data-ttu-id="72e18-113">大小</span><span class="sxs-lookup"><span data-stu-id="72e18-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="72e18-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="72e18-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="72e18-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="72e18-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="72e18-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72e18-116">Attribute-Id</span></span>      | <span data-ttu-id="72e18-117">1.2.840.113556.1.2.83</span><span class="sxs-lookup"><span data-stu-id="72e18-117">1.2.840.113556.1.2.83</span></span>                                 |
| <span data-ttu-id="72e18-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="72e18-118">System-Id-Guid</span></span>    | <span data-ttu-id="72e18-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="72e18-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="72e18-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e18-120">Syntax</span></span>            | [<span data-ttu-id="72e18-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="72e18-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="72e18-122">實作</span><span class="sxs-lookup"><span data-stu-id="72e18-122">Implementations</span></span>

-   [<span data-ttu-id="72e18-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="72e18-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="72e18-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72e18-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72e18-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="72e18-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="72e18-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72e18-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72e18-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72e18-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72e18-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72e18-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72e18-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72e18-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="72e18-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72e18-130">Windows 2000 Server</span></span>



| <span data-ttu-id="72e18-131">進入</span><span class="sxs-lookup"><span data-stu-id="72e18-131">Entry</span></span> | <span data-ttu-id="72e18-132">值</span><span class="sxs-lookup"><span data-stu-id="72e18-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72e18-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72e18-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e18-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e18-135">System-Only</span></span>            | <span data-ttu-id="72e18-136">對</span><span class="sxs-lookup"><span data-stu-id="72e18-136">True</span></span>                            |
| <span data-ttu-id="72e18-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72e18-137">Is-Single-Valued</span></span>       | <span data-ttu-id="72e18-138">否</span><span class="sxs-lookup"><span data-stu-id="72e18-138">False</span></span>                           |
| <span data-ttu-id="72e18-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72e18-139">Is Indexed</span></span>             | <span data-ttu-id="72e18-140">否</span><span class="sxs-lookup"><span data-stu-id="72e18-140">False</span></span>                           |
| <span data-ttu-id="72e18-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72e18-141">In Global Catalog</span></span>      | <span data-ttu-id="72e18-142">對</span><span class="sxs-lookup"><span data-stu-id="72e18-142">True</span></span>                            |
| <span data-ttu-id="72e18-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72e18-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e18-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72e18-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72e18-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e18-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72e18-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e18-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72e18-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-147">Search-Flags</span></span>           | <span data-ttu-id="72e18-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e18-148">0x00000000</span></span>                      |
| <span data-ttu-id="72e18-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-149">System-Flags</span></span>           | <span data-ttu-id="72e18-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="72e18-150">0x00000013</span></span>                      |
| <span data-ttu-id="72e18-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72e18-151">Classes used in</span></span>        | [<span data-ttu-id="72e18-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="72e18-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="72e18-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72e18-153">Windows Server 2003</span></span>



| <span data-ttu-id="72e18-154">進入</span><span class="sxs-lookup"><span data-stu-id="72e18-154">Entry</span></span> | <span data-ttu-id="72e18-155">值</span><span class="sxs-lookup"><span data-stu-id="72e18-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72e18-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72e18-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e18-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e18-158">System-Only</span></span>            | <span data-ttu-id="72e18-159">對</span><span class="sxs-lookup"><span data-stu-id="72e18-159">True</span></span>                            |
| <span data-ttu-id="72e18-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72e18-160">Is-Single-Valued</span></span>       | <span data-ttu-id="72e18-161">否</span><span class="sxs-lookup"><span data-stu-id="72e18-161">False</span></span>                           |
| <span data-ttu-id="72e18-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72e18-162">Is Indexed</span></span>             | <span data-ttu-id="72e18-163">否</span><span class="sxs-lookup"><span data-stu-id="72e18-163">False</span></span>                           |
| <span data-ttu-id="72e18-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72e18-164">In Global Catalog</span></span>      | <span data-ttu-id="72e18-165">對</span><span class="sxs-lookup"><span data-stu-id="72e18-165">True</span></span>                            |
| <span data-ttu-id="72e18-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72e18-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e18-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72e18-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72e18-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e18-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72e18-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e18-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72e18-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-170">Search-Flags</span></span>           | <span data-ttu-id="72e18-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e18-171">0x00000000</span></span>                      |
| <span data-ttu-id="72e18-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-172">System-Flags</span></span>           | <span data-ttu-id="72e18-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="72e18-173">0x00000013</span></span>                      |
| <span data-ttu-id="72e18-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72e18-174">Classes used in</span></span>        | [<span data-ttu-id="72e18-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="72e18-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="72e18-176">亞當</span><span class="sxs-lookup"><span data-stu-id="72e18-176">ADAM</span></span>



| <span data-ttu-id="72e18-177">進入</span><span class="sxs-lookup"><span data-stu-id="72e18-177">Entry</span></span> | <span data-ttu-id="72e18-178">值</span><span class="sxs-lookup"><span data-stu-id="72e18-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72e18-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72e18-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e18-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e18-181">System-Only</span></span>            | <span data-ttu-id="72e18-182">對</span><span class="sxs-lookup"><span data-stu-id="72e18-182">True</span></span>                            |
| <span data-ttu-id="72e18-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72e18-183">Is-Single-Valued</span></span>       | <span data-ttu-id="72e18-184">否</span><span class="sxs-lookup"><span data-stu-id="72e18-184">False</span></span>                           |
| <span data-ttu-id="72e18-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72e18-185">Is Indexed</span></span>             | <span data-ttu-id="72e18-186">否</span><span class="sxs-lookup"><span data-stu-id="72e18-186">False</span></span>                           |
| <span data-ttu-id="72e18-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72e18-187">In Global Catalog</span></span>      | <span data-ttu-id="72e18-188">對</span><span class="sxs-lookup"><span data-stu-id="72e18-188">True</span></span>                            |
| <span data-ttu-id="72e18-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72e18-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e18-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72e18-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72e18-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e18-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72e18-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e18-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72e18-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-193">Search-Flags</span></span>           | <span data-ttu-id="72e18-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e18-194">0x00000000</span></span>                      |
| <span data-ttu-id="72e18-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-195">System-Flags</span></span>           | <span data-ttu-id="72e18-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="72e18-196">0x00000013</span></span>                      |
| <span data-ttu-id="72e18-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72e18-197">Classes used in</span></span>        | [<span data-ttu-id="72e18-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="72e18-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72e18-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72e18-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72e18-200">進入</span><span class="sxs-lookup"><span data-stu-id="72e18-200">Entry</span></span> | <span data-ttu-id="72e18-201">值</span><span class="sxs-lookup"><span data-stu-id="72e18-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72e18-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72e18-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e18-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e18-204">System-Only</span></span>            | <span data-ttu-id="72e18-205">對</span><span class="sxs-lookup"><span data-stu-id="72e18-205">True</span></span>                            |
| <span data-ttu-id="72e18-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72e18-206">Is-Single-Valued</span></span>       | <span data-ttu-id="72e18-207">否</span><span class="sxs-lookup"><span data-stu-id="72e18-207">False</span></span>                           |
| <span data-ttu-id="72e18-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72e18-208">Is Indexed</span></span>             | <span data-ttu-id="72e18-209">否</span><span class="sxs-lookup"><span data-stu-id="72e18-209">False</span></span>                           |
| <span data-ttu-id="72e18-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72e18-210">In Global Catalog</span></span>      | <span data-ttu-id="72e18-211">對</span><span class="sxs-lookup"><span data-stu-id="72e18-211">True</span></span>                            |
| <span data-ttu-id="72e18-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72e18-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e18-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72e18-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72e18-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e18-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72e18-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e18-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72e18-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-216">Search-Flags</span></span>           | <span data-ttu-id="72e18-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e18-217">0x00000000</span></span>                      |
| <span data-ttu-id="72e18-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-218">System-Flags</span></span>           | <span data-ttu-id="72e18-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="72e18-219">0x00000013</span></span>                      |
| <span data-ttu-id="72e18-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72e18-220">Classes used in</span></span>        | [<span data-ttu-id="72e18-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="72e18-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72e18-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72e18-222">Windows Server 2008</span></span>



| <span data-ttu-id="72e18-223">進入</span><span class="sxs-lookup"><span data-stu-id="72e18-223">Entry</span></span> | <span data-ttu-id="72e18-224">值</span><span class="sxs-lookup"><span data-stu-id="72e18-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72e18-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72e18-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e18-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e18-227">System-Only</span></span>            | <span data-ttu-id="72e18-228">對</span><span class="sxs-lookup"><span data-stu-id="72e18-228">True</span></span>                            |
| <span data-ttu-id="72e18-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72e18-229">Is-Single-Valued</span></span>       | <span data-ttu-id="72e18-230">否</span><span class="sxs-lookup"><span data-stu-id="72e18-230">False</span></span>                           |
| <span data-ttu-id="72e18-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72e18-231">Is Indexed</span></span>             | <span data-ttu-id="72e18-232">否</span><span class="sxs-lookup"><span data-stu-id="72e18-232">False</span></span>                           |
| <span data-ttu-id="72e18-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72e18-233">In Global Catalog</span></span>      | <span data-ttu-id="72e18-234">對</span><span class="sxs-lookup"><span data-stu-id="72e18-234">True</span></span>                            |
| <span data-ttu-id="72e18-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72e18-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e18-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72e18-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72e18-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e18-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72e18-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e18-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72e18-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-239">Search-Flags</span></span>           | <span data-ttu-id="72e18-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e18-240">0x00000000</span></span>                      |
| <span data-ttu-id="72e18-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-241">System-Flags</span></span>           | <span data-ttu-id="72e18-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="72e18-242">0x00000013</span></span>                      |
| <span data-ttu-id="72e18-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72e18-243">Classes used in</span></span>        | [<span data-ttu-id="72e18-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="72e18-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72e18-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72e18-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72e18-246">進入</span><span class="sxs-lookup"><span data-stu-id="72e18-246">Entry</span></span> | <span data-ttu-id="72e18-247">值</span><span class="sxs-lookup"><span data-stu-id="72e18-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72e18-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72e18-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e18-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e18-250">System-Only</span></span>            | <span data-ttu-id="72e18-251">對</span><span class="sxs-lookup"><span data-stu-id="72e18-251">True</span></span>                            |
| <span data-ttu-id="72e18-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72e18-252">Is-Single-Valued</span></span>       | <span data-ttu-id="72e18-253">否</span><span class="sxs-lookup"><span data-stu-id="72e18-253">False</span></span>                           |
| <span data-ttu-id="72e18-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72e18-254">Is Indexed</span></span>             | <span data-ttu-id="72e18-255">否</span><span class="sxs-lookup"><span data-stu-id="72e18-255">False</span></span>                           |
| <span data-ttu-id="72e18-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72e18-256">In Global Catalog</span></span>      | <span data-ttu-id="72e18-257">對</span><span class="sxs-lookup"><span data-stu-id="72e18-257">True</span></span>                            |
| <span data-ttu-id="72e18-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72e18-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e18-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72e18-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72e18-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e18-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72e18-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e18-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72e18-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-262">Search-Flags</span></span>           | <span data-ttu-id="72e18-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e18-263">0x00000000</span></span>                      |
| <span data-ttu-id="72e18-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-264">System-Flags</span></span>           | <span data-ttu-id="72e18-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="72e18-265">0x00000013</span></span>                      |
| <span data-ttu-id="72e18-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72e18-266">Classes used in</span></span>        | [<span data-ttu-id="72e18-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="72e18-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72e18-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72e18-268">Windows Server 2012</span></span>



| <span data-ttu-id="72e18-269">進入</span><span class="sxs-lookup"><span data-stu-id="72e18-269">Entry</span></span> | <span data-ttu-id="72e18-270">值</span><span class="sxs-lookup"><span data-stu-id="72e18-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72e18-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72e18-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e18-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="72e18-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e18-273">System-Only</span></span>            | <span data-ttu-id="72e18-274">對</span><span class="sxs-lookup"><span data-stu-id="72e18-274">True</span></span>                            |
| <span data-ttu-id="72e18-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72e18-275">Is-Single-Valued</span></span>       | <span data-ttu-id="72e18-276">否</span><span class="sxs-lookup"><span data-stu-id="72e18-276">False</span></span>                           |
| <span data-ttu-id="72e18-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72e18-277">Is Indexed</span></span>             | <span data-ttu-id="72e18-278">否</span><span class="sxs-lookup"><span data-stu-id="72e18-278">False</span></span>                           |
| <span data-ttu-id="72e18-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72e18-279">In Global Catalog</span></span>      | <span data-ttu-id="72e18-280">對</span><span class="sxs-lookup"><span data-stu-id="72e18-280">True</span></span>                            |
| <span data-ttu-id="72e18-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72e18-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e18-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72e18-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72e18-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e18-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72e18-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e18-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72e18-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-285">Search-Flags</span></span>           | <span data-ttu-id="72e18-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e18-286">0x00000000</span></span>                      |
| <span data-ttu-id="72e18-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e18-287">System-Flags</span></span>           | <span data-ttu-id="72e18-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="72e18-288">0x00000013</span></span>                      |
| <span data-ttu-id="72e18-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72e18-289">Classes used in</span></span>        | [<span data-ttu-id="72e18-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="72e18-290">**Top**</span></span>](c-top.md)<br/> |



 

 






---
title: Reps-From 屬性
description: 列出目錄將接受所定義命名內容變更的伺服器。
ms.assetid: 2e18410b-d383-4838-aeaf-dd479be5f44d
ms.tgt_platform: multiple
keywords:
- Reps-From 屬性 AD 架構
- repsFrom 屬性 AD 架構
topic_type:
- apiref
api_name:
- Reps-From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc6981b71b6ec251eb27af0e7570fe1558d1ff20
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106967788"
---
# <a name="reps-from-attribute"></a><span data-ttu-id="dccdf-105">Reps-From 屬性</span><span class="sxs-lookup"><span data-stu-id="dccdf-105">Reps-From attribute</span></span>

<span data-ttu-id="dccdf-106">列出目錄將接受所定義命名內容變更的伺服器。</span><span class="sxs-lookup"><span data-stu-id="dccdf-106">Lists the servers from which the directory will accept changes for the defined naming context.</span></span>



| <span data-ttu-id="dccdf-107">進入</span><span class="sxs-lookup"><span data-stu-id="dccdf-107">Entry</span></span> | <span data-ttu-id="dccdf-108">值</span><span class="sxs-lookup"><span data-stu-id="dccdf-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="dccdf-109">CN</span><span class="sxs-lookup"><span data-stu-id="dccdf-109">CN</span></span>                | <span data-ttu-id="dccdf-110">Reps-From</span><span class="sxs-lookup"><span data-stu-id="dccdf-110">Reps-From</span></span>                                             |
| <span data-ttu-id="dccdf-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dccdf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dccdf-112">repsFrom</span><span class="sxs-lookup"><span data-stu-id="dccdf-112">repsFrom</span></span>                                              |
| <span data-ttu-id="dccdf-113">大小</span><span class="sxs-lookup"><span data-stu-id="dccdf-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="dccdf-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dccdf-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="dccdf-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dccdf-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="dccdf-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dccdf-116">Attribute-Id</span></span>      | <span data-ttu-id="dccdf-117">1.2.840.113556.1.2.91</span><span class="sxs-lookup"><span data-stu-id="dccdf-117">1.2.840.113556.1.2.91</span></span>                                 |
| <span data-ttu-id="dccdf-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dccdf-118">System-Id-Guid</span></span>    | <span data-ttu-id="dccdf-119">bf967a1d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dccdf-119">bf967a1d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="dccdf-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="dccdf-120">Syntax</span></span>            | [<span data-ttu-id="dccdf-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="dccdf-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="dccdf-122">實作</span><span class="sxs-lookup"><span data-stu-id="dccdf-122">Implementations</span></span>

-   [<span data-ttu-id="dccdf-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dccdf-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dccdf-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dccdf-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dccdf-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="dccdf-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dccdf-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dccdf-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dccdf-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dccdf-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dccdf-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dccdf-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dccdf-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dccdf-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dccdf-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dccdf-130">Windows 2000 Server</span></span>



| <span data-ttu-id="dccdf-131">進入</span><span class="sxs-lookup"><span data-stu-id="dccdf-131">Entry</span></span> | <span data-ttu-id="dccdf-132">值</span><span class="sxs-lookup"><span data-stu-id="dccdf-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dccdf-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dccdf-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dccdf-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="dccdf-135">System-Only</span></span>            | <span data-ttu-id="dccdf-136">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-136">True</span></span>                            |
| <span data-ttu-id="dccdf-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dccdf-137">Is-Single-Valued</span></span>       | <span data-ttu-id="dccdf-138">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-138">False</span></span>                           |
| <span data-ttu-id="dccdf-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dccdf-139">Is Indexed</span></span>             | <span data-ttu-id="dccdf-140">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-140">False</span></span>                           |
| <span data-ttu-id="dccdf-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dccdf-141">In Global Catalog</span></span>      | <span data-ttu-id="dccdf-142">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-142">True</span></span>                            |
| <span data-ttu-id="dccdf-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dccdf-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="dccdf-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dccdf-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dccdf-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dccdf-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dccdf-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dccdf-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dccdf-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-147">Search-Flags</span></span>           | <span data-ttu-id="dccdf-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dccdf-148">0x00000000</span></span>                      |
| <span data-ttu-id="dccdf-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-149">System-Flags</span></span>           | <span data-ttu-id="dccdf-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dccdf-150">0x00000013</span></span>                      |
| <span data-ttu-id="dccdf-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dccdf-151">Classes used in</span></span>        | [<span data-ttu-id="dccdf-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dccdf-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dccdf-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dccdf-153">Windows Server 2003</span></span>



| <span data-ttu-id="dccdf-154">進入</span><span class="sxs-lookup"><span data-stu-id="dccdf-154">Entry</span></span> | <span data-ttu-id="dccdf-155">值</span><span class="sxs-lookup"><span data-stu-id="dccdf-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dccdf-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dccdf-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dccdf-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="dccdf-158">System-Only</span></span>            | <span data-ttu-id="dccdf-159">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-159">True</span></span>                            |
| <span data-ttu-id="dccdf-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dccdf-160">Is-Single-Valued</span></span>       | <span data-ttu-id="dccdf-161">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-161">False</span></span>                           |
| <span data-ttu-id="dccdf-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dccdf-162">Is Indexed</span></span>             | <span data-ttu-id="dccdf-163">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-163">False</span></span>                           |
| <span data-ttu-id="dccdf-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dccdf-164">In Global Catalog</span></span>      | <span data-ttu-id="dccdf-165">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-165">True</span></span>                            |
| <span data-ttu-id="dccdf-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dccdf-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="dccdf-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dccdf-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dccdf-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dccdf-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dccdf-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dccdf-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dccdf-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-170">Search-Flags</span></span>           | <span data-ttu-id="dccdf-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dccdf-171">0x00000000</span></span>                      |
| <span data-ttu-id="dccdf-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-172">System-Flags</span></span>           | <span data-ttu-id="dccdf-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dccdf-173">0x00000013</span></span>                      |
| <span data-ttu-id="dccdf-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dccdf-174">Classes used in</span></span>        | [<span data-ttu-id="dccdf-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dccdf-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dccdf-176">亞當</span><span class="sxs-lookup"><span data-stu-id="dccdf-176">ADAM</span></span>



| <span data-ttu-id="dccdf-177">進入</span><span class="sxs-lookup"><span data-stu-id="dccdf-177">Entry</span></span> | <span data-ttu-id="dccdf-178">值</span><span class="sxs-lookup"><span data-stu-id="dccdf-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dccdf-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dccdf-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dccdf-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="dccdf-181">System-Only</span></span>            | <span data-ttu-id="dccdf-182">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-182">True</span></span>                            |
| <span data-ttu-id="dccdf-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dccdf-183">Is-Single-Valued</span></span>       | <span data-ttu-id="dccdf-184">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-184">False</span></span>                           |
| <span data-ttu-id="dccdf-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dccdf-185">Is Indexed</span></span>             | <span data-ttu-id="dccdf-186">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-186">False</span></span>                           |
| <span data-ttu-id="dccdf-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dccdf-187">In Global Catalog</span></span>      | <span data-ttu-id="dccdf-188">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-188">True</span></span>                            |
| <span data-ttu-id="dccdf-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dccdf-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="dccdf-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dccdf-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dccdf-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dccdf-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dccdf-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dccdf-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dccdf-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-193">Search-Flags</span></span>           | <span data-ttu-id="dccdf-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dccdf-194">0x00000000</span></span>                      |
| <span data-ttu-id="dccdf-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-195">System-Flags</span></span>           | <span data-ttu-id="dccdf-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dccdf-196">0x00000013</span></span>                      |
| <span data-ttu-id="dccdf-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dccdf-197">Classes used in</span></span>        | [<span data-ttu-id="dccdf-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dccdf-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dccdf-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dccdf-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dccdf-200">進入</span><span class="sxs-lookup"><span data-stu-id="dccdf-200">Entry</span></span> | <span data-ttu-id="dccdf-201">值</span><span class="sxs-lookup"><span data-stu-id="dccdf-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dccdf-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dccdf-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dccdf-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="dccdf-204">System-Only</span></span>            | <span data-ttu-id="dccdf-205">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-205">True</span></span>                            |
| <span data-ttu-id="dccdf-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dccdf-206">Is-Single-Valued</span></span>       | <span data-ttu-id="dccdf-207">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-207">False</span></span>                           |
| <span data-ttu-id="dccdf-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dccdf-208">Is Indexed</span></span>             | <span data-ttu-id="dccdf-209">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-209">False</span></span>                           |
| <span data-ttu-id="dccdf-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dccdf-210">In Global Catalog</span></span>      | <span data-ttu-id="dccdf-211">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-211">True</span></span>                            |
| <span data-ttu-id="dccdf-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dccdf-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="dccdf-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dccdf-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dccdf-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dccdf-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dccdf-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dccdf-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dccdf-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-216">Search-Flags</span></span>           | <span data-ttu-id="dccdf-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dccdf-217">0x00000000</span></span>                      |
| <span data-ttu-id="dccdf-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-218">System-Flags</span></span>           | <span data-ttu-id="dccdf-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dccdf-219">0x00000013</span></span>                      |
| <span data-ttu-id="dccdf-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dccdf-220">Classes used in</span></span>        | [<span data-ttu-id="dccdf-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dccdf-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dccdf-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dccdf-222">Windows Server 2008</span></span>



| <span data-ttu-id="dccdf-223">進入</span><span class="sxs-lookup"><span data-stu-id="dccdf-223">Entry</span></span> | <span data-ttu-id="dccdf-224">值</span><span class="sxs-lookup"><span data-stu-id="dccdf-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dccdf-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dccdf-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dccdf-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="dccdf-227">System-Only</span></span>            | <span data-ttu-id="dccdf-228">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-228">True</span></span>                            |
| <span data-ttu-id="dccdf-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dccdf-229">Is-Single-Valued</span></span>       | <span data-ttu-id="dccdf-230">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-230">False</span></span>                           |
| <span data-ttu-id="dccdf-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dccdf-231">Is Indexed</span></span>             | <span data-ttu-id="dccdf-232">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-232">False</span></span>                           |
| <span data-ttu-id="dccdf-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dccdf-233">In Global Catalog</span></span>      | <span data-ttu-id="dccdf-234">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-234">True</span></span>                            |
| <span data-ttu-id="dccdf-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dccdf-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="dccdf-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dccdf-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dccdf-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dccdf-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dccdf-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dccdf-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dccdf-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-239">Search-Flags</span></span>           | <span data-ttu-id="dccdf-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dccdf-240">0x00000000</span></span>                      |
| <span data-ttu-id="dccdf-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-241">System-Flags</span></span>           | <span data-ttu-id="dccdf-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dccdf-242">0x00000013</span></span>                      |
| <span data-ttu-id="dccdf-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dccdf-243">Classes used in</span></span>        | [<span data-ttu-id="dccdf-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dccdf-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dccdf-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dccdf-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dccdf-246">進入</span><span class="sxs-lookup"><span data-stu-id="dccdf-246">Entry</span></span> | <span data-ttu-id="dccdf-247">值</span><span class="sxs-lookup"><span data-stu-id="dccdf-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dccdf-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dccdf-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dccdf-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="dccdf-250">System-Only</span></span>            | <span data-ttu-id="dccdf-251">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-251">True</span></span>                            |
| <span data-ttu-id="dccdf-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dccdf-252">Is-Single-Valued</span></span>       | <span data-ttu-id="dccdf-253">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-253">False</span></span>                           |
| <span data-ttu-id="dccdf-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dccdf-254">Is Indexed</span></span>             | <span data-ttu-id="dccdf-255">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-255">False</span></span>                           |
| <span data-ttu-id="dccdf-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dccdf-256">In Global Catalog</span></span>      | <span data-ttu-id="dccdf-257">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-257">True</span></span>                            |
| <span data-ttu-id="dccdf-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dccdf-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="dccdf-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dccdf-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dccdf-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dccdf-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dccdf-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dccdf-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dccdf-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-262">Search-Flags</span></span>           | <span data-ttu-id="dccdf-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dccdf-263">0x00000000</span></span>                      |
| <span data-ttu-id="dccdf-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-264">System-Flags</span></span>           | <span data-ttu-id="dccdf-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dccdf-265">0x00000013</span></span>                      |
| <span data-ttu-id="dccdf-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dccdf-266">Classes used in</span></span>        | [<span data-ttu-id="dccdf-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dccdf-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dccdf-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dccdf-268">Windows Server 2012</span></span>



| <span data-ttu-id="dccdf-269">進入</span><span class="sxs-lookup"><span data-stu-id="dccdf-269">Entry</span></span> | <span data-ttu-id="dccdf-270">值</span><span class="sxs-lookup"><span data-stu-id="dccdf-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dccdf-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dccdf-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dccdf-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dccdf-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="dccdf-273">System-Only</span></span>            | <span data-ttu-id="dccdf-274">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-274">True</span></span>                            |
| <span data-ttu-id="dccdf-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dccdf-275">Is-Single-Valued</span></span>       | <span data-ttu-id="dccdf-276">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-276">False</span></span>                           |
| <span data-ttu-id="dccdf-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dccdf-277">Is Indexed</span></span>             | <span data-ttu-id="dccdf-278">否</span><span class="sxs-lookup"><span data-stu-id="dccdf-278">False</span></span>                           |
| <span data-ttu-id="dccdf-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dccdf-279">In Global Catalog</span></span>      | <span data-ttu-id="dccdf-280">對</span><span class="sxs-lookup"><span data-stu-id="dccdf-280">True</span></span>                            |
| <span data-ttu-id="dccdf-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dccdf-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="dccdf-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dccdf-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dccdf-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dccdf-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dccdf-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dccdf-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dccdf-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-285">Search-Flags</span></span>           | <span data-ttu-id="dccdf-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dccdf-286">0x00000000</span></span>                      |
| <span data-ttu-id="dccdf-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dccdf-287">System-Flags</span></span>           | <span data-ttu-id="dccdf-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dccdf-288">0x00000013</span></span>                      |
| <span data-ttu-id="dccdf-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dccdf-289">Classes used in</span></span>        | [<span data-ttu-id="dccdf-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dccdf-290">**Top**</span></span>](c-top.md)<br/> |



 

 






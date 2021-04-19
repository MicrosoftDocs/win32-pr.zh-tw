---
title: DS-核心-傳播-資料屬性
description: DS-核心-傳播-資料屬性僅供內部使用。
ms.assetid: 6483890a-b1ef-4c8d-941d-8f25f722a305
ms.tgt_platform: multiple
keywords:
- DS-核心-傳播-資料屬性 AD 架構
- dSCorePropagationData 屬性 AD 架構
topic_type:
- apiref
api_name:
- DS-Core-Propagation-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324e3db3c71d11f47cb0a7afec875b9d129fa2d9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971064"
---
# <a name="ds-core-propagation-data-attribute"></a><span data-ttu-id="85d09-105">DS-核心-傳播-資料屬性</span><span class="sxs-lookup"><span data-stu-id="85d09-105">DS-Core-Propagation-Data attribute</span></span>

<span data-ttu-id="85d09-106">**DS-核心-傳播-資料** 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="85d09-106">The **DS-Core-Propagation-Data** attribute is for internal use only.</span></span>



| <span data-ttu-id="85d09-107">進入</span><span class="sxs-lookup"><span data-stu-id="85d09-107">Entry</span></span> | <span data-ttu-id="85d09-108">值</span><span class="sxs-lookup"><span data-stu-id="85d09-108">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="85d09-109">CN</span><span class="sxs-lookup"><span data-stu-id="85d09-109">CN</span></span>                | <span data-ttu-id="85d09-110">DS-核心-傳播-資料</span><span class="sxs-lookup"><span data-stu-id="85d09-110">DS-Core-Propagation-Data</span></span>                                      |
| <span data-ttu-id="85d09-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="85d09-111">Ldap-Display-Name</span></span> | <span data-ttu-id="85d09-112">dSCorePropagationData</span><span class="sxs-lookup"><span data-stu-id="85d09-112">dSCorePropagationData</span></span>                                         |
| <span data-ttu-id="85d09-113">大小</span><span class="sxs-lookup"><span data-stu-id="85d09-113">Size</span></span>              | \-                                                            |
| <span data-ttu-id="85d09-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="85d09-114">Update Privilege</span></span>  | \-                                                            |
| <span data-ttu-id="85d09-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="85d09-115">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="85d09-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="85d09-116">Attribute-Id</span></span>      | <span data-ttu-id="85d09-117">1.2.840.113556.1.4.1357</span><span class="sxs-lookup"><span data-stu-id="85d09-117">1.2.840.113556.1.4.1357</span></span>                                       |
| <span data-ttu-id="85d09-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="85d09-118">System-Id-Guid</span></span>    | <span data-ttu-id="85d09-119">d167aa4b-8b08-11d2-9939-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="85d09-119">d167aa4b-8b08-11d2-9939-0000f87a57d4</span></span>                          |
| <span data-ttu-id="85d09-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="85d09-120">Syntax</span></span>            | [<span data-ttu-id="85d09-121">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="85d09-121">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="85d09-122">實作</span><span class="sxs-lookup"><span data-stu-id="85d09-122">Implementations</span></span>

-   [<span data-ttu-id="85d09-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="85d09-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="85d09-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="85d09-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="85d09-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="85d09-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="85d09-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="85d09-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="85d09-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="85d09-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="85d09-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="85d09-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="85d09-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="85d09-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="85d09-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85d09-130">Windows 2000 Server</span></span>



| <span data-ttu-id="85d09-131">進入</span><span class="sxs-lookup"><span data-stu-id="85d09-131">Entry</span></span> | <span data-ttu-id="85d09-132">值</span><span class="sxs-lookup"><span data-stu-id="85d09-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="85d09-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="85d09-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85d09-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="85d09-135">System-Only</span></span>            | <span data-ttu-id="85d09-136">對</span><span class="sxs-lookup"><span data-stu-id="85d09-136">True</span></span>                            |
| <span data-ttu-id="85d09-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="85d09-137">Is-Single-Valued</span></span>       | <span data-ttu-id="85d09-138">否</span><span class="sxs-lookup"><span data-stu-id="85d09-138">False</span></span>                           |
| <span data-ttu-id="85d09-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="85d09-139">Is Indexed</span></span>             | <span data-ttu-id="85d09-140">否</span><span class="sxs-lookup"><span data-stu-id="85d09-140">False</span></span>                           |
| <span data-ttu-id="85d09-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="85d09-141">In Global Catalog</span></span>      | <span data-ttu-id="85d09-142">對</span><span class="sxs-lookup"><span data-stu-id="85d09-142">True</span></span>                            |
| <span data-ttu-id="85d09-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="85d09-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="85d09-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="85d09-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="85d09-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85d09-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="85d09-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85d09-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="85d09-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-147">Search-Flags</span></span>           | <span data-ttu-id="85d09-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85d09-148">0x00000000</span></span>                      |
| <span data-ttu-id="85d09-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-149">System-Flags</span></span>           | <span data-ttu-id="85d09-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="85d09-150">0x00000013</span></span>                      |
| <span data-ttu-id="85d09-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="85d09-151">Classes used in</span></span>        | [<span data-ttu-id="85d09-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="85d09-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="85d09-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="85d09-153">Windows Server 2003</span></span>



| <span data-ttu-id="85d09-154">進入</span><span class="sxs-lookup"><span data-stu-id="85d09-154">Entry</span></span> | <span data-ttu-id="85d09-155">值</span><span class="sxs-lookup"><span data-stu-id="85d09-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="85d09-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="85d09-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85d09-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="85d09-158">System-Only</span></span>            | <span data-ttu-id="85d09-159">對</span><span class="sxs-lookup"><span data-stu-id="85d09-159">True</span></span>                            |
| <span data-ttu-id="85d09-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="85d09-160">Is-Single-Valued</span></span>       | <span data-ttu-id="85d09-161">否</span><span class="sxs-lookup"><span data-stu-id="85d09-161">False</span></span>                           |
| <span data-ttu-id="85d09-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="85d09-162">Is Indexed</span></span>             | <span data-ttu-id="85d09-163">否</span><span class="sxs-lookup"><span data-stu-id="85d09-163">False</span></span>                           |
| <span data-ttu-id="85d09-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="85d09-164">In Global Catalog</span></span>      | <span data-ttu-id="85d09-165">對</span><span class="sxs-lookup"><span data-stu-id="85d09-165">True</span></span>                            |
| <span data-ttu-id="85d09-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="85d09-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="85d09-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="85d09-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="85d09-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85d09-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="85d09-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85d09-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="85d09-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-170">Search-Flags</span></span>           | <span data-ttu-id="85d09-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85d09-171">0x00000000</span></span>                      |
| <span data-ttu-id="85d09-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-172">System-Flags</span></span>           | <span data-ttu-id="85d09-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="85d09-173">0x00000013</span></span>                      |
| <span data-ttu-id="85d09-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="85d09-174">Classes used in</span></span>        | [<span data-ttu-id="85d09-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="85d09-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="85d09-176">亞當</span><span class="sxs-lookup"><span data-stu-id="85d09-176">ADAM</span></span>



| <span data-ttu-id="85d09-177">進入</span><span class="sxs-lookup"><span data-stu-id="85d09-177">Entry</span></span> | <span data-ttu-id="85d09-178">值</span><span class="sxs-lookup"><span data-stu-id="85d09-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="85d09-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="85d09-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85d09-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="85d09-181">System-Only</span></span>            | <span data-ttu-id="85d09-182">對</span><span class="sxs-lookup"><span data-stu-id="85d09-182">True</span></span>                            |
| <span data-ttu-id="85d09-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="85d09-183">Is-Single-Valued</span></span>       | <span data-ttu-id="85d09-184">否</span><span class="sxs-lookup"><span data-stu-id="85d09-184">False</span></span>                           |
| <span data-ttu-id="85d09-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="85d09-185">Is Indexed</span></span>             | <span data-ttu-id="85d09-186">否</span><span class="sxs-lookup"><span data-stu-id="85d09-186">False</span></span>                           |
| <span data-ttu-id="85d09-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="85d09-187">In Global Catalog</span></span>      | <span data-ttu-id="85d09-188">對</span><span class="sxs-lookup"><span data-stu-id="85d09-188">True</span></span>                            |
| <span data-ttu-id="85d09-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="85d09-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="85d09-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="85d09-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="85d09-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85d09-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="85d09-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85d09-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="85d09-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-193">Search-Flags</span></span>           | <span data-ttu-id="85d09-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85d09-194">0x00000000</span></span>                      |
| <span data-ttu-id="85d09-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-195">System-Flags</span></span>           | <span data-ttu-id="85d09-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="85d09-196">0x00000013</span></span>                      |
| <span data-ttu-id="85d09-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="85d09-197">Classes used in</span></span>        | [<span data-ttu-id="85d09-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="85d09-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="85d09-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="85d09-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="85d09-200">進入</span><span class="sxs-lookup"><span data-stu-id="85d09-200">Entry</span></span> | <span data-ttu-id="85d09-201">值</span><span class="sxs-lookup"><span data-stu-id="85d09-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="85d09-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="85d09-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85d09-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="85d09-204">System-Only</span></span>            | <span data-ttu-id="85d09-205">對</span><span class="sxs-lookup"><span data-stu-id="85d09-205">True</span></span>                            |
| <span data-ttu-id="85d09-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="85d09-206">Is-Single-Valued</span></span>       | <span data-ttu-id="85d09-207">否</span><span class="sxs-lookup"><span data-stu-id="85d09-207">False</span></span>                           |
| <span data-ttu-id="85d09-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="85d09-208">Is Indexed</span></span>             | <span data-ttu-id="85d09-209">否</span><span class="sxs-lookup"><span data-stu-id="85d09-209">False</span></span>                           |
| <span data-ttu-id="85d09-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="85d09-210">In Global Catalog</span></span>      | <span data-ttu-id="85d09-211">對</span><span class="sxs-lookup"><span data-stu-id="85d09-211">True</span></span>                            |
| <span data-ttu-id="85d09-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="85d09-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="85d09-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="85d09-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="85d09-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85d09-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="85d09-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85d09-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="85d09-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-216">Search-Flags</span></span>           | <span data-ttu-id="85d09-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85d09-217">0x00000000</span></span>                      |
| <span data-ttu-id="85d09-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-218">System-Flags</span></span>           | <span data-ttu-id="85d09-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="85d09-219">0x00000013</span></span>                      |
| <span data-ttu-id="85d09-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="85d09-220">Classes used in</span></span>        | [<span data-ttu-id="85d09-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="85d09-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="85d09-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85d09-222">Windows Server 2008</span></span>



| <span data-ttu-id="85d09-223">進入</span><span class="sxs-lookup"><span data-stu-id="85d09-223">Entry</span></span> | <span data-ttu-id="85d09-224">值</span><span class="sxs-lookup"><span data-stu-id="85d09-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="85d09-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="85d09-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85d09-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="85d09-227">System-Only</span></span>            | <span data-ttu-id="85d09-228">對</span><span class="sxs-lookup"><span data-stu-id="85d09-228">True</span></span>                            |
| <span data-ttu-id="85d09-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="85d09-229">Is-Single-Valued</span></span>       | <span data-ttu-id="85d09-230">否</span><span class="sxs-lookup"><span data-stu-id="85d09-230">False</span></span>                           |
| <span data-ttu-id="85d09-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="85d09-231">Is Indexed</span></span>             | <span data-ttu-id="85d09-232">否</span><span class="sxs-lookup"><span data-stu-id="85d09-232">False</span></span>                           |
| <span data-ttu-id="85d09-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="85d09-233">In Global Catalog</span></span>      | <span data-ttu-id="85d09-234">對</span><span class="sxs-lookup"><span data-stu-id="85d09-234">True</span></span>                            |
| <span data-ttu-id="85d09-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="85d09-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="85d09-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="85d09-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="85d09-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85d09-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="85d09-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85d09-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="85d09-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-239">Search-Flags</span></span>           | <span data-ttu-id="85d09-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85d09-240">0x00000000</span></span>                      |
| <span data-ttu-id="85d09-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-241">System-Flags</span></span>           | <span data-ttu-id="85d09-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="85d09-242">0x00000013</span></span>                      |
| <span data-ttu-id="85d09-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="85d09-243">Classes used in</span></span>        | [<span data-ttu-id="85d09-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="85d09-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="85d09-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85d09-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="85d09-246">進入</span><span class="sxs-lookup"><span data-stu-id="85d09-246">Entry</span></span> | <span data-ttu-id="85d09-247">值</span><span class="sxs-lookup"><span data-stu-id="85d09-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="85d09-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="85d09-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85d09-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="85d09-250">System-Only</span></span>            | <span data-ttu-id="85d09-251">對</span><span class="sxs-lookup"><span data-stu-id="85d09-251">True</span></span>                            |
| <span data-ttu-id="85d09-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="85d09-252">Is-Single-Valued</span></span>       | <span data-ttu-id="85d09-253">否</span><span class="sxs-lookup"><span data-stu-id="85d09-253">False</span></span>                           |
| <span data-ttu-id="85d09-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="85d09-254">Is Indexed</span></span>             | <span data-ttu-id="85d09-255">否</span><span class="sxs-lookup"><span data-stu-id="85d09-255">False</span></span>                           |
| <span data-ttu-id="85d09-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="85d09-256">In Global Catalog</span></span>      | <span data-ttu-id="85d09-257">對</span><span class="sxs-lookup"><span data-stu-id="85d09-257">True</span></span>                            |
| <span data-ttu-id="85d09-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="85d09-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="85d09-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="85d09-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="85d09-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85d09-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="85d09-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85d09-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="85d09-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-262">Search-Flags</span></span>           | <span data-ttu-id="85d09-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85d09-263">0x00000000</span></span>                      |
| <span data-ttu-id="85d09-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-264">System-Flags</span></span>           | <span data-ttu-id="85d09-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="85d09-265">0x00000013</span></span>                      |
| <span data-ttu-id="85d09-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="85d09-266">Classes used in</span></span>        | [<span data-ttu-id="85d09-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="85d09-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="85d09-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85d09-268">Windows Server 2012</span></span>



| <span data-ttu-id="85d09-269">進入</span><span class="sxs-lookup"><span data-stu-id="85d09-269">Entry</span></span> | <span data-ttu-id="85d09-270">值</span><span class="sxs-lookup"><span data-stu-id="85d09-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="85d09-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="85d09-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85d09-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="85d09-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="85d09-273">System-Only</span></span>            | <span data-ttu-id="85d09-274">對</span><span class="sxs-lookup"><span data-stu-id="85d09-274">True</span></span>                            |
| <span data-ttu-id="85d09-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="85d09-275">Is-Single-Valued</span></span>       | <span data-ttu-id="85d09-276">否</span><span class="sxs-lookup"><span data-stu-id="85d09-276">False</span></span>                           |
| <span data-ttu-id="85d09-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="85d09-277">Is Indexed</span></span>             | <span data-ttu-id="85d09-278">否</span><span class="sxs-lookup"><span data-stu-id="85d09-278">False</span></span>                           |
| <span data-ttu-id="85d09-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="85d09-279">In Global Catalog</span></span>      | <span data-ttu-id="85d09-280">對</span><span class="sxs-lookup"><span data-stu-id="85d09-280">True</span></span>                            |
| <span data-ttu-id="85d09-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="85d09-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="85d09-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="85d09-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="85d09-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85d09-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="85d09-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85d09-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="85d09-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-285">Search-Flags</span></span>           | <span data-ttu-id="85d09-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85d09-286">0x00000000</span></span>                      |
| <span data-ttu-id="85d09-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85d09-287">System-Flags</span></span>           | <span data-ttu-id="85d09-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="85d09-288">0x00000013</span></span>                      |
| <span data-ttu-id="85d09-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="85d09-289">Classes used in</span></span>        | [<span data-ttu-id="85d09-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="85d09-290">**Top**</span></span>](c-top.md)<br/> |



 

 






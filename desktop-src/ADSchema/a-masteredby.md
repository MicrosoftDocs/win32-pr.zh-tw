---
title: Mastered-By 屬性
description: Nc 屬性的後置連結。 其 NTDS 設定物件的分辨名稱。
ms.assetid: bd14998c-1691-4167-83c4-3c1ec1181b7f
ms.tgt_platform: multiple
keywords:
- Mastered-By 屬性 AD 架構
- masteredBy 屬性 AD 架構
topic_type:
- apiref
api_name:
- Mastered-By
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85cf02f78363e1e8db06bddfb2c389cc78077090
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107225"
---
# <a name="mastered-by-attribute"></a><span data-ttu-id="abc7a-106">Mastered-By 屬性</span><span class="sxs-lookup"><span data-stu-id="abc7a-106">Mastered-By attribute</span></span>

<span data-ttu-id="abc7a-107">Nc 屬性的後置連結。</span><span class="sxs-lookup"><span data-stu-id="abc7a-107">Backward link for Has-Master-NCs attribute.</span></span> <span data-ttu-id="abc7a-108">其 NTDS 設定物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="abc7a-108">The distinguished name for its NTDS Settings objects.</span></span>



| <span data-ttu-id="abc7a-109">進入</span><span class="sxs-lookup"><span data-stu-id="abc7a-109">Entry</span></span> | <span data-ttu-id="abc7a-110">值</span><span class="sxs-lookup"><span data-stu-id="abc7a-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="abc7a-111">CN</span><span class="sxs-lookup"><span data-stu-id="abc7a-111">CN</span></span>                | <span data-ttu-id="abc7a-112">Mastered-By</span><span class="sxs-lookup"><span data-stu-id="abc7a-112">Mastered-By</span></span>                             |
| <span data-ttu-id="abc7a-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="abc7a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="abc7a-114">masteredBy</span><span class="sxs-lookup"><span data-stu-id="abc7a-114">masteredBy</span></span>                              |
| <span data-ttu-id="abc7a-115">大小</span><span class="sxs-lookup"><span data-stu-id="abc7a-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="abc7a-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="abc7a-116">Update Privilege</span></span>  | <span data-ttu-id="abc7a-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="abc7a-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="abc7a-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="abc7a-118">Update Frequency</span></span>  | <span data-ttu-id="abc7a-119">當命名內容建立時。</span><span class="sxs-lookup"><span data-stu-id="abc7a-119">When the Naming Context is created.</span></span>     |
| <span data-ttu-id="abc7a-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="abc7a-120">Attribute-Id</span></span>      | <span data-ttu-id="abc7a-121">1.2.840.113556.1.4.1409</span><span class="sxs-lookup"><span data-stu-id="abc7a-121">1.2.840.113556.1.4.1409</span></span>                 |
| <span data-ttu-id="abc7a-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="abc7a-122">System-Id-Guid</span></span>    | <span data-ttu-id="abc7a-123">e48e64e0-12c9-11d3-9102-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="abc7a-123">e48e64e0-12c9-11d3-9102-00c04fd91ab1</span></span>    |
| <span data-ttu-id="abc7a-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="abc7a-124">Syntax</span></span>            | [<span data-ttu-id="abc7a-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="abc7a-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="abc7a-126">實作</span><span class="sxs-lookup"><span data-stu-id="abc7a-126">Implementations</span></span>

-   [<span data-ttu-id="abc7a-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="abc7a-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="abc7a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="abc7a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="abc7a-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="abc7a-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="abc7a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="abc7a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="abc7a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="abc7a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="abc7a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="abc7a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="abc7a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="abc7a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="abc7a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="abc7a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="abc7a-135">進入</span><span class="sxs-lookup"><span data-stu-id="abc7a-135">Entry</span></span> | <span data-ttu-id="abc7a-136">值</span><span class="sxs-lookup"><span data-stu-id="abc7a-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="abc7a-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="abc7a-137">Link-Id</span></span>                | <span data-ttu-id="abc7a-138">77</span><span class="sxs-lookup"><span data-stu-id="abc7a-138">77</span></span>                              |
| <span data-ttu-id="abc7a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abc7a-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="abc7a-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="abc7a-140">System-Only</span></span>            | <span data-ttu-id="abc7a-141">對</span><span class="sxs-lookup"><span data-stu-id="abc7a-141">True</span></span>                            |
| <span data-ttu-id="abc7a-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="abc7a-142">Is-Single-Valued</span></span>       | <span data-ttu-id="abc7a-143">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-143">False</span></span>                           |
| <span data-ttu-id="abc7a-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="abc7a-144">Is Indexed</span></span>             | <span data-ttu-id="abc7a-145">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-145">False</span></span>                           |
| <span data-ttu-id="abc7a-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="abc7a-146">In Global Catalog</span></span>      | <span data-ttu-id="abc7a-147">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-147">False</span></span>                           |
| <span data-ttu-id="abc7a-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="abc7a-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="abc7a-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="abc7a-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="abc7a-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abc7a-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="abc7a-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abc7a-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="abc7a-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-152">Search-Flags</span></span>           | <span data-ttu-id="abc7a-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abc7a-153">0x00000000</span></span>                      |
| <span data-ttu-id="abc7a-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-154">System-Flags</span></span>           | <span data-ttu-id="abc7a-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abc7a-155">0x00000010</span></span>                      |
| <span data-ttu-id="abc7a-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="abc7a-156">Classes used in</span></span>        | [<span data-ttu-id="abc7a-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="abc7a-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="abc7a-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="abc7a-158">Windows Server 2003</span></span>



| <span data-ttu-id="abc7a-159">進入</span><span class="sxs-lookup"><span data-stu-id="abc7a-159">Entry</span></span> | <span data-ttu-id="abc7a-160">值</span><span class="sxs-lookup"><span data-stu-id="abc7a-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="abc7a-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="abc7a-161">Link-Id</span></span>                | <span data-ttu-id="abc7a-162">77</span><span class="sxs-lookup"><span data-stu-id="abc7a-162">77</span></span>                              |
| <span data-ttu-id="abc7a-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abc7a-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="abc7a-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="abc7a-164">System-Only</span></span>            | <span data-ttu-id="abc7a-165">對</span><span class="sxs-lookup"><span data-stu-id="abc7a-165">True</span></span>                            |
| <span data-ttu-id="abc7a-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="abc7a-166">Is-Single-Valued</span></span>       | <span data-ttu-id="abc7a-167">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-167">False</span></span>                           |
| <span data-ttu-id="abc7a-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="abc7a-168">Is Indexed</span></span>             | <span data-ttu-id="abc7a-169">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-169">False</span></span>                           |
| <span data-ttu-id="abc7a-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="abc7a-170">In Global Catalog</span></span>      | <span data-ttu-id="abc7a-171">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-171">False</span></span>                           |
| <span data-ttu-id="abc7a-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="abc7a-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="abc7a-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="abc7a-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="abc7a-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abc7a-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="abc7a-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abc7a-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="abc7a-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-176">Search-Flags</span></span>           | <span data-ttu-id="abc7a-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abc7a-177">0x00000000</span></span>                      |
| <span data-ttu-id="abc7a-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-178">System-Flags</span></span>           | <span data-ttu-id="abc7a-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abc7a-179">0x00000010</span></span>                      |
| <span data-ttu-id="abc7a-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="abc7a-180">Classes used in</span></span>        | [<span data-ttu-id="abc7a-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="abc7a-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="abc7a-182">亞當</span><span class="sxs-lookup"><span data-stu-id="abc7a-182">ADAM</span></span>



| <span data-ttu-id="abc7a-183">進入</span><span class="sxs-lookup"><span data-stu-id="abc7a-183">Entry</span></span> | <span data-ttu-id="abc7a-184">值</span><span class="sxs-lookup"><span data-stu-id="abc7a-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="abc7a-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="abc7a-185">Link-Id</span></span>                | <span data-ttu-id="abc7a-186">77</span><span class="sxs-lookup"><span data-stu-id="abc7a-186">77</span></span>                              |
| <span data-ttu-id="abc7a-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abc7a-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="abc7a-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="abc7a-188">System-Only</span></span>            | <span data-ttu-id="abc7a-189">對</span><span class="sxs-lookup"><span data-stu-id="abc7a-189">True</span></span>                            |
| <span data-ttu-id="abc7a-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="abc7a-190">Is-Single-Valued</span></span>       | <span data-ttu-id="abc7a-191">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-191">False</span></span>                           |
| <span data-ttu-id="abc7a-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="abc7a-192">Is Indexed</span></span>             | <span data-ttu-id="abc7a-193">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-193">False</span></span>                           |
| <span data-ttu-id="abc7a-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="abc7a-194">In Global Catalog</span></span>      | <span data-ttu-id="abc7a-195">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-195">False</span></span>                           |
| <span data-ttu-id="abc7a-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="abc7a-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="abc7a-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="abc7a-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="abc7a-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abc7a-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="abc7a-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abc7a-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="abc7a-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-200">Search-Flags</span></span>           | <span data-ttu-id="abc7a-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abc7a-201">0x00000000</span></span>                      |
| <span data-ttu-id="abc7a-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-202">System-Flags</span></span>           | <span data-ttu-id="abc7a-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abc7a-203">0x00000010</span></span>                      |
| <span data-ttu-id="abc7a-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="abc7a-204">Classes used in</span></span>        | [<span data-ttu-id="abc7a-205">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="abc7a-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="abc7a-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="abc7a-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="abc7a-207">進入</span><span class="sxs-lookup"><span data-stu-id="abc7a-207">Entry</span></span> | <span data-ttu-id="abc7a-208">值</span><span class="sxs-lookup"><span data-stu-id="abc7a-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="abc7a-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="abc7a-209">Link-Id</span></span>                | <span data-ttu-id="abc7a-210">77</span><span class="sxs-lookup"><span data-stu-id="abc7a-210">77</span></span>                              |
| <span data-ttu-id="abc7a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abc7a-211">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="abc7a-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="abc7a-212">System-Only</span></span>            | <span data-ttu-id="abc7a-213">對</span><span class="sxs-lookup"><span data-stu-id="abc7a-213">True</span></span>                            |
| <span data-ttu-id="abc7a-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="abc7a-214">Is-Single-Valued</span></span>       | <span data-ttu-id="abc7a-215">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-215">False</span></span>                           |
| <span data-ttu-id="abc7a-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="abc7a-216">Is Indexed</span></span>             | <span data-ttu-id="abc7a-217">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-217">False</span></span>                           |
| <span data-ttu-id="abc7a-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="abc7a-218">In Global Catalog</span></span>      | <span data-ttu-id="abc7a-219">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-219">False</span></span>                           |
| <span data-ttu-id="abc7a-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="abc7a-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="abc7a-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="abc7a-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="abc7a-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abc7a-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="abc7a-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abc7a-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="abc7a-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-224">Search-Flags</span></span>           | <span data-ttu-id="abc7a-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abc7a-225">0x00000000</span></span>                      |
| <span data-ttu-id="abc7a-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-226">System-Flags</span></span>           | <span data-ttu-id="abc7a-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abc7a-227">0x00000010</span></span>                      |
| <span data-ttu-id="abc7a-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="abc7a-228">Classes used in</span></span>        | [<span data-ttu-id="abc7a-229">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="abc7a-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="abc7a-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abc7a-230">Windows Server 2008</span></span>



| <span data-ttu-id="abc7a-231">進入</span><span class="sxs-lookup"><span data-stu-id="abc7a-231">Entry</span></span> | <span data-ttu-id="abc7a-232">值</span><span class="sxs-lookup"><span data-stu-id="abc7a-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="abc7a-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="abc7a-233">Link-Id</span></span>                | <span data-ttu-id="abc7a-234">77</span><span class="sxs-lookup"><span data-stu-id="abc7a-234">77</span></span>                              |
| <span data-ttu-id="abc7a-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abc7a-235">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="abc7a-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="abc7a-236">System-Only</span></span>            | <span data-ttu-id="abc7a-237">對</span><span class="sxs-lookup"><span data-stu-id="abc7a-237">True</span></span>                            |
| <span data-ttu-id="abc7a-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="abc7a-238">Is-Single-Valued</span></span>       | <span data-ttu-id="abc7a-239">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-239">False</span></span>                           |
| <span data-ttu-id="abc7a-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="abc7a-240">Is Indexed</span></span>             | <span data-ttu-id="abc7a-241">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-241">False</span></span>                           |
| <span data-ttu-id="abc7a-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="abc7a-242">In Global Catalog</span></span>      | <span data-ttu-id="abc7a-243">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-243">False</span></span>                           |
| <span data-ttu-id="abc7a-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="abc7a-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="abc7a-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="abc7a-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="abc7a-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abc7a-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="abc7a-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abc7a-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="abc7a-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-248">Search-Flags</span></span>           | <span data-ttu-id="abc7a-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abc7a-249">0x00000000</span></span>                      |
| <span data-ttu-id="abc7a-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-250">System-Flags</span></span>           | <span data-ttu-id="abc7a-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abc7a-251">0x00000010</span></span>                      |
| <span data-ttu-id="abc7a-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="abc7a-252">Classes used in</span></span>        | [<span data-ttu-id="abc7a-253">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="abc7a-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="abc7a-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="abc7a-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="abc7a-255">進入</span><span class="sxs-lookup"><span data-stu-id="abc7a-255">Entry</span></span> | <span data-ttu-id="abc7a-256">值</span><span class="sxs-lookup"><span data-stu-id="abc7a-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="abc7a-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="abc7a-257">Link-Id</span></span>                | <span data-ttu-id="abc7a-258">77</span><span class="sxs-lookup"><span data-stu-id="abc7a-258">77</span></span>                              |
| <span data-ttu-id="abc7a-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abc7a-259">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="abc7a-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="abc7a-260">System-Only</span></span>            | <span data-ttu-id="abc7a-261">對</span><span class="sxs-lookup"><span data-stu-id="abc7a-261">True</span></span>                            |
| <span data-ttu-id="abc7a-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="abc7a-262">Is-Single-Valued</span></span>       | <span data-ttu-id="abc7a-263">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-263">False</span></span>                           |
| <span data-ttu-id="abc7a-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="abc7a-264">Is Indexed</span></span>             | <span data-ttu-id="abc7a-265">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-265">False</span></span>                           |
| <span data-ttu-id="abc7a-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="abc7a-266">In Global Catalog</span></span>      | <span data-ttu-id="abc7a-267">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-267">False</span></span>                           |
| <span data-ttu-id="abc7a-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="abc7a-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="abc7a-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="abc7a-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="abc7a-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abc7a-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="abc7a-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abc7a-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="abc7a-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-272">Search-Flags</span></span>           | <span data-ttu-id="abc7a-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abc7a-273">0x00000000</span></span>                      |
| <span data-ttu-id="abc7a-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-274">System-Flags</span></span>           | <span data-ttu-id="abc7a-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abc7a-275">0x00000010</span></span>                      |
| <span data-ttu-id="abc7a-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="abc7a-276">Classes used in</span></span>        | [<span data-ttu-id="abc7a-277">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="abc7a-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="abc7a-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abc7a-278">Windows Server 2012</span></span>



| <span data-ttu-id="abc7a-279">進入</span><span class="sxs-lookup"><span data-stu-id="abc7a-279">Entry</span></span> | <span data-ttu-id="abc7a-280">值</span><span class="sxs-lookup"><span data-stu-id="abc7a-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="abc7a-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="abc7a-281">Link-Id</span></span>                | <span data-ttu-id="abc7a-282">77</span><span class="sxs-lookup"><span data-stu-id="abc7a-282">77</span></span>                              |
| <span data-ttu-id="abc7a-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abc7a-283">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="abc7a-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="abc7a-284">System-Only</span></span>            | <span data-ttu-id="abc7a-285">對</span><span class="sxs-lookup"><span data-stu-id="abc7a-285">True</span></span>                            |
| <span data-ttu-id="abc7a-286">是-單一值</span><span class="sxs-lookup"><span data-stu-id="abc7a-286">Is-Single-Valued</span></span>       | <span data-ttu-id="abc7a-287">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-287">False</span></span>                           |
| <span data-ttu-id="abc7a-288">已編制索引</span><span class="sxs-lookup"><span data-stu-id="abc7a-288">Is Indexed</span></span>             | <span data-ttu-id="abc7a-289">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-289">False</span></span>                           |
| <span data-ttu-id="abc7a-290">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="abc7a-290">In Global Catalog</span></span>      | <span data-ttu-id="abc7a-291">否</span><span class="sxs-lookup"><span data-stu-id="abc7a-291">False</span></span>                           |
| <span data-ttu-id="abc7a-292">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="abc7a-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="abc7a-293">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="abc7a-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="abc7a-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abc7a-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="abc7a-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abc7a-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="abc7a-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-296">Search-Flags</span></span>           | <span data-ttu-id="abc7a-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abc7a-297">0x00000000</span></span>                      |
| <span data-ttu-id="abc7a-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abc7a-298">System-Flags</span></span>           | <span data-ttu-id="abc7a-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abc7a-299">0x00000010</span></span>                      |
| <span data-ttu-id="abc7a-300">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="abc7a-300">Classes used in</span></span>        | [<span data-ttu-id="abc7a-301">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="abc7a-301">**Top**</span></span>](c-top.md)<br/> |



 

 






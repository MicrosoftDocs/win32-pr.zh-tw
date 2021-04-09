---
title: Trust-Parent 屬性
description: KERBEROS 信任階層中的父系。
ms.assetid: 738cf509-42a2-40b6-a525-6df34c02d0f0
ms.tgt_platform: multiple
keywords:
- Trust-Parent 屬性 AD 架構
- trustParent 屬性 AD 架構
topic_type:
- apiref
api_name:
- Trust-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8be971c7597b14daf7a694e41c9d67714e5f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687115"
---
# <a name="trust-parent-attribute"></a><span data-ttu-id="4addb-105">Trust-Parent 屬性</span><span class="sxs-lookup"><span data-stu-id="4addb-105">Trust-Parent attribute</span></span>

<span data-ttu-id="4addb-106">KERBEROS 信任階層中的父系。</span><span class="sxs-lookup"><span data-stu-id="4addb-106">The parent in KERBEROS trust hierarchy.</span></span>



| <span data-ttu-id="4addb-107">進入</span><span class="sxs-lookup"><span data-stu-id="4addb-107">Entry</span></span> | <span data-ttu-id="4addb-108">值</span><span class="sxs-lookup"><span data-stu-id="4addb-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="4addb-109">CN</span><span class="sxs-lookup"><span data-stu-id="4addb-109">CN</span></span>                | <span data-ttu-id="4addb-110">Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="4addb-110">Trust-Parent</span></span>                            |
| <span data-ttu-id="4addb-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4addb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4addb-112">trustParent</span><span class="sxs-lookup"><span data-stu-id="4addb-112">trustParent</span></span>                             |
| <span data-ttu-id="4addb-113">大小</span><span class="sxs-lookup"><span data-stu-id="4addb-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="4addb-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4addb-114">Update Privilege</span></span>  | <span data-ttu-id="4addb-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="4addb-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="4addb-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4addb-116">Update Frequency</span></span>  | <span data-ttu-id="4addb-117">當子域建立時。</span><span class="sxs-lookup"><span data-stu-id="4addb-117">When a child domain is created.</span></span>         |
| <span data-ttu-id="4addb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4addb-118">Attribute-Id</span></span>      | <span data-ttu-id="4addb-119">1.2.840.113556.1.4.471</span><span class="sxs-lookup"><span data-stu-id="4addb-119">1.2.840.113556.1.4.471</span></span>                  |
| <span data-ttu-id="4addb-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4addb-120">System-Id-Guid</span></span>    | <span data-ttu-id="4addb-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="4addb-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="4addb-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4addb-122">Syntax</span></span>            | [<span data-ttu-id="4addb-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="4addb-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="4addb-124">實作</span><span class="sxs-lookup"><span data-stu-id="4addb-124">Implementations</span></span>

-   [<span data-ttu-id="4addb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4addb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4addb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4addb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4addb-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="4addb-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4addb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4addb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4addb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4addb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4addb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4addb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4addb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4addb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4addb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4addb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="4addb-133">進入</span><span class="sxs-lookup"><span data-stu-id="4addb-133">Entry</span></span> | <span data-ttu-id="4addb-134">值</span><span class="sxs-lookup"><span data-stu-id="4addb-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4addb-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4addb-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4addb-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="4addb-137">System-Only</span></span>            | <span data-ttu-id="4addb-138">否</span><span class="sxs-lookup"><span data-stu-id="4addb-138">False</span></span>                                      |
| <span data-ttu-id="4addb-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4addb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="4addb-140">對</span><span class="sxs-lookup"><span data-stu-id="4addb-140">True</span></span>                                       |
| <span data-ttu-id="4addb-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4addb-141">Is Indexed</span></span>             | <span data-ttu-id="4addb-142">否</span><span class="sxs-lookup"><span data-stu-id="4addb-142">False</span></span>                                      |
| <span data-ttu-id="4addb-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4addb-143">In Global Catalog</span></span>      | <span data-ttu-id="4addb-144">否</span><span class="sxs-lookup"><span data-stu-id="4addb-144">False</span></span>                                      |
| <span data-ttu-id="4addb-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4addb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="4addb-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4addb-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4addb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4addb-147">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4addb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4addb-148">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4addb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-149">Search-Flags</span></span>           | <span data-ttu-id="4addb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4addb-150">0x00000000</span></span>                                 |
| <span data-ttu-id="4addb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-151">System-Flags</span></span>           | <span data-ttu-id="4addb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4addb-152">0x00000010</span></span>                                 |
| <span data-ttu-id="4addb-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4addb-153">Classes used in</span></span>        | [<span data-ttu-id="4addb-154">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="4addb-154">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4addb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4addb-155">Windows Server 2003</span></span>



| <span data-ttu-id="4addb-156">進入</span><span class="sxs-lookup"><span data-stu-id="4addb-156">Entry</span></span> | <span data-ttu-id="4addb-157">值</span><span class="sxs-lookup"><span data-stu-id="4addb-157">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4addb-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4addb-158">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4addb-159">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="4addb-160">System-Only</span></span>            | <span data-ttu-id="4addb-161">否</span><span class="sxs-lookup"><span data-stu-id="4addb-161">False</span></span>                                      |
| <span data-ttu-id="4addb-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4addb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="4addb-163">對</span><span class="sxs-lookup"><span data-stu-id="4addb-163">True</span></span>                                       |
| <span data-ttu-id="4addb-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4addb-164">Is Indexed</span></span>             | <span data-ttu-id="4addb-165">否</span><span class="sxs-lookup"><span data-stu-id="4addb-165">False</span></span>                                      |
| <span data-ttu-id="4addb-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4addb-166">In Global Catalog</span></span>      | <span data-ttu-id="4addb-167">否</span><span class="sxs-lookup"><span data-stu-id="4addb-167">False</span></span>                                      |
| <span data-ttu-id="4addb-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4addb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="4addb-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4addb-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4addb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4addb-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4addb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4addb-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4addb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-172">Search-Flags</span></span>           | <span data-ttu-id="4addb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4addb-173">0x00000000</span></span>                                 |
| <span data-ttu-id="4addb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-174">System-Flags</span></span>           | <span data-ttu-id="4addb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4addb-175">0x00000010</span></span>                                 |
| <span data-ttu-id="4addb-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4addb-176">Classes used in</span></span>        | [<span data-ttu-id="4addb-177">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="4addb-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4addb-178">亞當</span><span class="sxs-lookup"><span data-stu-id="4addb-178">ADAM</span></span>



| <span data-ttu-id="4addb-179">進入</span><span class="sxs-lookup"><span data-stu-id="4addb-179">Entry</span></span> | <span data-ttu-id="4addb-180">值</span><span class="sxs-lookup"><span data-stu-id="4addb-180">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4addb-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4addb-181">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4addb-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="4addb-183">System-Only</span></span>            | <span data-ttu-id="4addb-184">否</span><span class="sxs-lookup"><span data-stu-id="4addb-184">False</span></span>                                      |
| <span data-ttu-id="4addb-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4addb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="4addb-186">對</span><span class="sxs-lookup"><span data-stu-id="4addb-186">True</span></span>                                       |
| <span data-ttu-id="4addb-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4addb-187">Is Indexed</span></span>             | <span data-ttu-id="4addb-188">否</span><span class="sxs-lookup"><span data-stu-id="4addb-188">False</span></span>                                      |
| <span data-ttu-id="4addb-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4addb-189">In Global Catalog</span></span>      | <span data-ttu-id="4addb-190">否</span><span class="sxs-lookup"><span data-stu-id="4addb-190">False</span></span>                                      |
| <span data-ttu-id="4addb-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4addb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="4addb-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4addb-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4addb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4addb-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4addb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4addb-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4addb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-195">Search-Flags</span></span>           | <span data-ttu-id="4addb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4addb-196">0x00000000</span></span>                                 |
| <span data-ttu-id="4addb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-197">System-Flags</span></span>           | <span data-ttu-id="4addb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4addb-198">0x00000010</span></span>                                 |
| <span data-ttu-id="4addb-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4addb-199">Classes used in</span></span>        | [<span data-ttu-id="4addb-200">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="4addb-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4addb-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4addb-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4addb-202">進入</span><span class="sxs-lookup"><span data-stu-id="4addb-202">Entry</span></span> | <span data-ttu-id="4addb-203">值</span><span class="sxs-lookup"><span data-stu-id="4addb-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4addb-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4addb-204">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4addb-205">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="4addb-206">System-Only</span></span>            | <span data-ttu-id="4addb-207">否</span><span class="sxs-lookup"><span data-stu-id="4addb-207">False</span></span>                                      |
| <span data-ttu-id="4addb-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4addb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="4addb-209">對</span><span class="sxs-lookup"><span data-stu-id="4addb-209">True</span></span>                                       |
| <span data-ttu-id="4addb-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4addb-210">Is Indexed</span></span>             | <span data-ttu-id="4addb-211">否</span><span class="sxs-lookup"><span data-stu-id="4addb-211">False</span></span>                                      |
| <span data-ttu-id="4addb-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4addb-212">In Global Catalog</span></span>      | <span data-ttu-id="4addb-213">否</span><span class="sxs-lookup"><span data-stu-id="4addb-213">False</span></span>                                      |
| <span data-ttu-id="4addb-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4addb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="4addb-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4addb-215">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4addb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4addb-216">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4addb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4addb-217">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4addb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-218">Search-Flags</span></span>           | <span data-ttu-id="4addb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4addb-219">0x00000000</span></span>                                 |
| <span data-ttu-id="4addb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-220">System-Flags</span></span>           | <span data-ttu-id="4addb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4addb-221">0x00000010</span></span>                                 |
| <span data-ttu-id="4addb-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4addb-222">Classes used in</span></span>        | [<span data-ttu-id="4addb-223">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="4addb-223">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4addb-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4addb-224">Windows Server 2008</span></span>



| <span data-ttu-id="4addb-225">進入</span><span class="sxs-lookup"><span data-stu-id="4addb-225">Entry</span></span> | <span data-ttu-id="4addb-226">值</span><span class="sxs-lookup"><span data-stu-id="4addb-226">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4addb-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4addb-227">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4addb-228">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="4addb-229">System-Only</span></span>            | <span data-ttu-id="4addb-230">否</span><span class="sxs-lookup"><span data-stu-id="4addb-230">False</span></span>                                      |
| <span data-ttu-id="4addb-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4addb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="4addb-232">對</span><span class="sxs-lookup"><span data-stu-id="4addb-232">True</span></span>                                       |
| <span data-ttu-id="4addb-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4addb-233">Is Indexed</span></span>             | <span data-ttu-id="4addb-234">否</span><span class="sxs-lookup"><span data-stu-id="4addb-234">False</span></span>                                      |
| <span data-ttu-id="4addb-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4addb-235">In Global Catalog</span></span>      | <span data-ttu-id="4addb-236">否</span><span class="sxs-lookup"><span data-stu-id="4addb-236">False</span></span>                                      |
| <span data-ttu-id="4addb-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4addb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="4addb-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4addb-238">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4addb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4addb-239">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4addb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4addb-240">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4addb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-241">Search-Flags</span></span>           | <span data-ttu-id="4addb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4addb-242">0x00000000</span></span>                                 |
| <span data-ttu-id="4addb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-243">System-Flags</span></span>           | <span data-ttu-id="4addb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4addb-244">0x00000010</span></span>                                 |
| <span data-ttu-id="4addb-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4addb-245">Classes used in</span></span>        | [<span data-ttu-id="4addb-246">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="4addb-246">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4addb-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4addb-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4addb-248">進入</span><span class="sxs-lookup"><span data-stu-id="4addb-248">Entry</span></span> | <span data-ttu-id="4addb-249">值</span><span class="sxs-lookup"><span data-stu-id="4addb-249">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4addb-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4addb-250">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4addb-251">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="4addb-252">System-Only</span></span>            | <span data-ttu-id="4addb-253">否</span><span class="sxs-lookup"><span data-stu-id="4addb-253">False</span></span>                                      |
| <span data-ttu-id="4addb-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4addb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="4addb-255">對</span><span class="sxs-lookup"><span data-stu-id="4addb-255">True</span></span>                                       |
| <span data-ttu-id="4addb-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4addb-256">Is Indexed</span></span>             | <span data-ttu-id="4addb-257">否</span><span class="sxs-lookup"><span data-stu-id="4addb-257">False</span></span>                                      |
| <span data-ttu-id="4addb-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4addb-258">In Global Catalog</span></span>      | <span data-ttu-id="4addb-259">否</span><span class="sxs-lookup"><span data-stu-id="4addb-259">False</span></span>                                      |
| <span data-ttu-id="4addb-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4addb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="4addb-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4addb-261">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4addb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4addb-262">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4addb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4addb-263">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4addb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-264">Search-Flags</span></span>           | <span data-ttu-id="4addb-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4addb-265">0x00000000</span></span>                                 |
| <span data-ttu-id="4addb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-266">System-Flags</span></span>           | <span data-ttu-id="4addb-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4addb-267">0x00000010</span></span>                                 |
| <span data-ttu-id="4addb-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4addb-268">Classes used in</span></span>        | [<span data-ttu-id="4addb-269">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="4addb-269">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4addb-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4addb-270">Windows Server 2012</span></span>



| <span data-ttu-id="4addb-271">進入</span><span class="sxs-lookup"><span data-stu-id="4addb-271">Entry</span></span> | <span data-ttu-id="4addb-272">值</span><span class="sxs-lookup"><span data-stu-id="4addb-272">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4addb-273">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4addb-273">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4addb-274">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4addb-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="4addb-275">System-Only</span></span>            | <span data-ttu-id="4addb-276">否</span><span class="sxs-lookup"><span data-stu-id="4addb-276">False</span></span>                                      |
| <span data-ttu-id="4addb-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4addb-277">Is-Single-Valued</span></span>       | <span data-ttu-id="4addb-278">對</span><span class="sxs-lookup"><span data-stu-id="4addb-278">True</span></span>                                       |
| <span data-ttu-id="4addb-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4addb-279">Is Indexed</span></span>             | <span data-ttu-id="4addb-280">否</span><span class="sxs-lookup"><span data-stu-id="4addb-280">False</span></span>                                      |
| <span data-ttu-id="4addb-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4addb-281">In Global Catalog</span></span>      | <span data-ttu-id="4addb-282">否</span><span class="sxs-lookup"><span data-stu-id="4addb-282">False</span></span>                                      |
| <span data-ttu-id="4addb-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4addb-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="4addb-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4addb-284">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4addb-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4addb-285">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4addb-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4addb-286">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4addb-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-287">Search-Flags</span></span>           | <span data-ttu-id="4addb-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4addb-288">0x00000000</span></span>                                 |
| <span data-ttu-id="4addb-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4addb-289">System-Flags</span></span>           | <span data-ttu-id="4addb-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4addb-290">0x00000010</span></span>                                 |
| <span data-ttu-id="4addb-291">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4addb-291">Classes used in</span></span>        | [<span data-ttu-id="4addb-292">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="4addb-292">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






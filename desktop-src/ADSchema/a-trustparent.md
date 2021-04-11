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
# <a name="trust-parent-attribute"></a><span data-ttu-id="c63dc-105">Trust-Parent 屬性</span><span class="sxs-lookup"><span data-stu-id="c63dc-105">Trust-Parent attribute</span></span>

<span data-ttu-id="c63dc-106">KERBEROS 信任階層中的父系。</span><span class="sxs-lookup"><span data-stu-id="c63dc-106">The parent in KERBEROS trust hierarchy.</span></span>



| <span data-ttu-id="c63dc-107">進入</span><span class="sxs-lookup"><span data-stu-id="c63dc-107">Entry</span></span> | <span data-ttu-id="c63dc-108">值</span><span class="sxs-lookup"><span data-stu-id="c63dc-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c63dc-109">CN</span><span class="sxs-lookup"><span data-stu-id="c63dc-109">CN</span></span>                | <span data-ttu-id="c63dc-110">Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="c63dc-110">Trust-Parent</span></span>                            |
| <span data-ttu-id="c63dc-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c63dc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c63dc-112">trustParent</span><span class="sxs-lookup"><span data-stu-id="c63dc-112">trustParent</span></span>                             |
| <span data-ttu-id="c63dc-113">大小</span><span class="sxs-lookup"><span data-stu-id="c63dc-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c63dc-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c63dc-114">Update Privilege</span></span>  | <span data-ttu-id="c63dc-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="c63dc-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="c63dc-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c63dc-116">Update Frequency</span></span>  | <span data-ttu-id="c63dc-117">當子域建立時。</span><span class="sxs-lookup"><span data-stu-id="c63dc-117">When a child domain is created.</span></span>         |
| <span data-ttu-id="c63dc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c63dc-118">Attribute-Id</span></span>      | <span data-ttu-id="c63dc-119">1.2.840.113556.1.4.471</span><span class="sxs-lookup"><span data-stu-id="c63dc-119">1.2.840.113556.1.4.471</span></span>                  |
| <span data-ttu-id="c63dc-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c63dc-120">System-Id-Guid</span></span>    | <span data-ttu-id="c63dc-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c63dc-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="c63dc-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c63dc-122">Syntax</span></span>            | [<span data-ttu-id="c63dc-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c63dc-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c63dc-124">實作</span><span class="sxs-lookup"><span data-stu-id="c63dc-124">Implementations</span></span>

-   [<span data-ttu-id="c63dc-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c63dc-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c63dc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c63dc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c63dc-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="c63dc-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c63dc-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c63dc-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c63dc-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c63dc-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c63dc-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c63dc-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c63dc-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c63dc-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c63dc-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c63dc-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c63dc-133">進入</span><span class="sxs-lookup"><span data-stu-id="c63dc-133">Entry</span></span> | <span data-ttu-id="c63dc-134">值</span><span class="sxs-lookup"><span data-stu-id="c63dc-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c63dc-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c63dc-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63dc-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63dc-137">System-Only</span></span>            | <span data-ttu-id="c63dc-138">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-138">False</span></span>                                      |
| <span data-ttu-id="c63dc-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c63dc-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c63dc-140">對</span><span class="sxs-lookup"><span data-stu-id="c63dc-140">True</span></span>                                       |
| <span data-ttu-id="c63dc-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c63dc-141">Is Indexed</span></span>             | <span data-ttu-id="c63dc-142">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-142">False</span></span>                                      |
| <span data-ttu-id="c63dc-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c63dc-143">In Global Catalog</span></span>      | <span data-ttu-id="c63dc-144">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-144">False</span></span>                                      |
| <span data-ttu-id="c63dc-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c63dc-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63dc-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c63dc-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c63dc-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63dc-147">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63dc-148">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-149">Search-Flags</span></span>           | <span data-ttu-id="c63dc-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63dc-150">0x00000000</span></span>                                 |
| <span data-ttu-id="c63dc-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-151">System-Flags</span></span>           | <span data-ttu-id="c63dc-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63dc-152">0x00000010</span></span>                                 |
| <span data-ttu-id="c63dc-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c63dc-153">Classes used in</span></span>        | [<span data-ttu-id="c63dc-154">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="c63dc-154">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c63dc-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c63dc-155">Windows Server 2003</span></span>



| <span data-ttu-id="c63dc-156">進入</span><span class="sxs-lookup"><span data-stu-id="c63dc-156">Entry</span></span> | <span data-ttu-id="c63dc-157">值</span><span class="sxs-lookup"><span data-stu-id="c63dc-157">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c63dc-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c63dc-158">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63dc-159">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63dc-160">System-Only</span></span>            | <span data-ttu-id="c63dc-161">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-161">False</span></span>                                      |
| <span data-ttu-id="c63dc-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c63dc-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c63dc-163">對</span><span class="sxs-lookup"><span data-stu-id="c63dc-163">True</span></span>                                       |
| <span data-ttu-id="c63dc-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c63dc-164">Is Indexed</span></span>             | <span data-ttu-id="c63dc-165">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-165">False</span></span>                                      |
| <span data-ttu-id="c63dc-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c63dc-166">In Global Catalog</span></span>      | <span data-ttu-id="c63dc-167">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-167">False</span></span>                                      |
| <span data-ttu-id="c63dc-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c63dc-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63dc-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c63dc-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c63dc-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63dc-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63dc-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-172">Search-Flags</span></span>           | <span data-ttu-id="c63dc-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63dc-173">0x00000000</span></span>                                 |
| <span data-ttu-id="c63dc-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-174">System-Flags</span></span>           | <span data-ttu-id="c63dc-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63dc-175">0x00000010</span></span>                                 |
| <span data-ttu-id="c63dc-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c63dc-176">Classes used in</span></span>        | [<span data-ttu-id="c63dc-177">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="c63dc-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c63dc-178">亞當</span><span class="sxs-lookup"><span data-stu-id="c63dc-178">ADAM</span></span>



| <span data-ttu-id="c63dc-179">進入</span><span class="sxs-lookup"><span data-stu-id="c63dc-179">Entry</span></span> | <span data-ttu-id="c63dc-180">值</span><span class="sxs-lookup"><span data-stu-id="c63dc-180">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c63dc-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c63dc-181">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63dc-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63dc-183">System-Only</span></span>            | <span data-ttu-id="c63dc-184">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-184">False</span></span>                                      |
| <span data-ttu-id="c63dc-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c63dc-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c63dc-186">對</span><span class="sxs-lookup"><span data-stu-id="c63dc-186">True</span></span>                                       |
| <span data-ttu-id="c63dc-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c63dc-187">Is Indexed</span></span>             | <span data-ttu-id="c63dc-188">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-188">False</span></span>                                      |
| <span data-ttu-id="c63dc-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c63dc-189">In Global Catalog</span></span>      | <span data-ttu-id="c63dc-190">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-190">False</span></span>                                      |
| <span data-ttu-id="c63dc-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c63dc-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63dc-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c63dc-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c63dc-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63dc-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63dc-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-195">Search-Flags</span></span>           | <span data-ttu-id="c63dc-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63dc-196">0x00000000</span></span>                                 |
| <span data-ttu-id="c63dc-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-197">System-Flags</span></span>           | <span data-ttu-id="c63dc-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63dc-198">0x00000010</span></span>                                 |
| <span data-ttu-id="c63dc-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c63dc-199">Classes used in</span></span>        | [<span data-ttu-id="c63dc-200">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="c63dc-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c63dc-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c63dc-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c63dc-202">進入</span><span class="sxs-lookup"><span data-stu-id="c63dc-202">Entry</span></span> | <span data-ttu-id="c63dc-203">值</span><span class="sxs-lookup"><span data-stu-id="c63dc-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c63dc-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c63dc-204">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63dc-205">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63dc-206">System-Only</span></span>            | <span data-ttu-id="c63dc-207">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-207">False</span></span>                                      |
| <span data-ttu-id="c63dc-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c63dc-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c63dc-209">對</span><span class="sxs-lookup"><span data-stu-id="c63dc-209">True</span></span>                                       |
| <span data-ttu-id="c63dc-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c63dc-210">Is Indexed</span></span>             | <span data-ttu-id="c63dc-211">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-211">False</span></span>                                      |
| <span data-ttu-id="c63dc-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c63dc-212">In Global Catalog</span></span>      | <span data-ttu-id="c63dc-213">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-213">False</span></span>                                      |
| <span data-ttu-id="c63dc-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c63dc-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63dc-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c63dc-215">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c63dc-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63dc-216">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63dc-217">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-218">Search-Flags</span></span>           | <span data-ttu-id="c63dc-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63dc-219">0x00000000</span></span>                                 |
| <span data-ttu-id="c63dc-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-220">System-Flags</span></span>           | <span data-ttu-id="c63dc-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63dc-221">0x00000010</span></span>                                 |
| <span data-ttu-id="c63dc-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c63dc-222">Classes used in</span></span>        | [<span data-ttu-id="c63dc-223">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="c63dc-223">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c63dc-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c63dc-224">Windows Server 2008</span></span>



| <span data-ttu-id="c63dc-225">進入</span><span class="sxs-lookup"><span data-stu-id="c63dc-225">Entry</span></span> | <span data-ttu-id="c63dc-226">值</span><span class="sxs-lookup"><span data-stu-id="c63dc-226">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c63dc-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c63dc-227">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63dc-228">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63dc-229">System-Only</span></span>            | <span data-ttu-id="c63dc-230">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-230">False</span></span>                                      |
| <span data-ttu-id="c63dc-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c63dc-231">Is-Single-Valued</span></span>       | <span data-ttu-id="c63dc-232">對</span><span class="sxs-lookup"><span data-stu-id="c63dc-232">True</span></span>                                       |
| <span data-ttu-id="c63dc-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c63dc-233">Is Indexed</span></span>             | <span data-ttu-id="c63dc-234">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-234">False</span></span>                                      |
| <span data-ttu-id="c63dc-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c63dc-235">In Global Catalog</span></span>      | <span data-ttu-id="c63dc-236">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-236">False</span></span>                                      |
| <span data-ttu-id="c63dc-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c63dc-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63dc-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c63dc-238">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c63dc-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63dc-239">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63dc-240">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-241">Search-Flags</span></span>           | <span data-ttu-id="c63dc-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63dc-242">0x00000000</span></span>                                 |
| <span data-ttu-id="c63dc-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-243">System-Flags</span></span>           | <span data-ttu-id="c63dc-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63dc-244">0x00000010</span></span>                                 |
| <span data-ttu-id="c63dc-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c63dc-245">Classes used in</span></span>        | [<span data-ttu-id="c63dc-246">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="c63dc-246">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c63dc-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c63dc-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c63dc-248">進入</span><span class="sxs-lookup"><span data-stu-id="c63dc-248">Entry</span></span> | <span data-ttu-id="c63dc-249">值</span><span class="sxs-lookup"><span data-stu-id="c63dc-249">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c63dc-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c63dc-250">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63dc-251">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63dc-252">System-Only</span></span>            | <span data-ttu-id="c63dc-253">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-253">False</span></span>                                      |
| <span data-ttu-id="c63dc-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c63dc-254">Is-Single-Valued</span></span>       | <span data-ttu-id="c63dc-255">對</span><span class="sxs-lookup"><span data-stu-id="c63dc-255">True</span></span>                                       |
| <span data-ttu-id="c63dc-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c63dc-256">Is Indexed</span></span>             | <span data-ttu-id="c63dc-257">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-257">False</span></span>                                      |
| <span data-ttu-id="c63dc-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c63dc-258">In Global Catalog</span></span>      | <span data-ttu-id="c63dc-259">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-259">False</span></span>                                      |
| <span data-ttu-id="c63dc-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c63dc-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63dc-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c63dc-261">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c63dc-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63dc-262">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63dc-263">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-264">Search-Flags</span></span>           | <span data-ttu-id="c63dc-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63dc-265">0x00000000</span></span>                                 |
| <span data-ttu-id="c63dc-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-266">System-Flags</span></span>           | <span data-ttu-id="c63dc-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63dc-267">0x00000010</span></span>                                 |
| <span data-ttu-id="c63dc-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c63dc-268">Classes used in</span></span>        | [<span data-ttu-id="c63dc-269">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="c63dc-269">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c63dc-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c63dc-270">Windows Server 2012</span></span>



| <span data-ttu-id="c63dc-271">進入</span><span class="sxs-lookup"><span data-stu-id="c63dc-271">Entry</span></span> | <span data-ttu-id="c63dc-272">值</span><span class="sxs-lookup"><span data-stu-id="c63dc-272">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="c63dc-273">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c63dc-273">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63dc-274">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="c63dc-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63dc-275">System-Only</span></span>            | <span data-ttu-id="c63dc-276">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-276">False</span></span>                                      |
| <span data-ttu-id="c63dc-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c63dc-277">Is-Single-Valued</span></span>       | <span data-ttu-id="c63dc-278">對</span><span class="sxs-lookup"><span data-stu-id="c63dc-278">True</span></span>                                       |
| <span data-ttu-id="c63dc-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c63dc-279">Is Indexed</span></span>             | <span data-ttu-id="c63dc-280">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-280">False</span></span>                                      |
| <span data-ttu-id="c63dc-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c63dc-281">In Global Catalog</span></span>      | <span data-ttu-id="c63dc-282">否</span><span class="sxs-lookup"><span data-stu-id="c63dc-282">False</span></span>                                      |
| <span data-ttu-id="c63dc-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c63dc-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63dc-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c63dc-284">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="c63dc-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63dc-285">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63dc-286">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="c63dc-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-287">Search-Flags</span></span>           | <span data-ttu-id="c63dc-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63dc-288">0x00000000</span></span>                                 |
| <span data-ttu-id="c63dc-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63dc-289">System-Flags</span></span>           | <span data-ttu-id="c63dc-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63dc-290">0x00000010</span></span>                                 |
| <span data-ttu-id="c63dc-291">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c63dc-291">Classes used in</span></span>        | [<span data-ttu-id="c63dc-292">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="c63dc-292">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






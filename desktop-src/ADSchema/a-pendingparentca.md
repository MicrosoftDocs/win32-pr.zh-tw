---
title: 暫止-父系-CA 屬性
description: 參考為此憑證授權單位單位發出暫止憑證的憑證授權單位單位。
ms.assetid: 9cdac673-aecd-4a42-93f5-c869fa136186
ms.tgt_platform: multiple
keywords:
- 暫止-父系-CA 屬性 AD 架構
- pendingParentCA 屬性 AD 架構
topic_type:
- apiref
api_name:
- Pending-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5e100a18980780f4086f09ce39a060703462ae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973327"
---
# <a name="pending-parent-ca-attribute"></a><span data-ttu-id="62762-105">暫止-父系-CA 屬性</span><span class="sxs-lookup"><span data-stu-id="62762-105">Pending-Parent-CA attribute</span></span>

<span data-ttu-id="62762-106">參考為此憑證授權單位單位發出暫止憑證的憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="62762-106">Reference to the certification authorities that issued the pending certificates for this certification authority.</span></span>



| <span data-ttu-id="62762-107">進入</span><span class="sxs-lookup"><span data-stu-id="62762-107">Entry</span></span> | <span data-ttu-id="62762-108">值</span><span class="sxs-lookup"><span data-stu-id="62762-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="62762-109">CN</span><span class="sxs-lookup"><span data-stu-id="62762-109">CN</span></span>                | <span data-ttu-id="62762-110">暫止-父系-CA</span><span class="sxs-lookup"><span data-stu-id="62762-110">Pending-Parent-CA</span></span>                       |
| <span data-ttu-id="62762-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="62762-111">Ldap-Display-Name</span></span> | <span data-ttu-id="62762-112">pendingParentCA</span><span class="sxs-lookup"><span data-stu-id="62762-112">pendingParentCA</span></span>                         |
| <span data-ttu-id="62762-113">大小</span><span class="sxs-lookup"><span data-stu-id="62762-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="62762-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="62762-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="62762-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="62762-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="62762-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="62762-116">Attribute-Id</span></span>      | <span data-ttu-id="62762-117">1.2.840.113556.1.4.695</span><span class="sxs-lookup"><span data-stu-id="62762-117">1.2.840.113556.1.4.695</span></span>                  |
| <span data-ttu-id="62762-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="62762-118">System-Id-Guid</span></span>    | <span data-ttu-id="62762-119">963d273e-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="62762-119">963d273e-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="62762-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="62762-120">Syntax</span></span>            | [<span data-ttu-id="62762-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="62762-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="62762-122">實作</span><span class="sxs-lookup"><span data-stu-id="62762-122">Implementations</span></span>

-   [<span data-ttu-id="62762-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="62762-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="62762-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="62762-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="62762-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="62762-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="62762-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="62762-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="62762-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="62762-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="62762-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="62762-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="62762-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="62762-129">Windows 2000 Server</span></span>



| <span data-ttu-id="62762-130">進入</span><span class="sxs-lookup"><span data-stu-id="62762-130">Entry</span></span> | <span data-ttu-id="62762-131">值</span><span class="sxs-lookup"><span data-stu-id="62762-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="62762-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="62762-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62762-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="62762-134">System-Only</span></span>            | <span data-ttu-id="62762-135">否</span><span class="sxs-lookup"><span data-stu-id="62762-135">False</span></span>                                                                  |
| <span data-ttu-id="62762-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="62762-136">Is-Single-Valued</span></span>       | <span data-ttu-id="62762-137">否</span><span class="sxs-lookup"><span data-stu-id="62762-137">False</span></span>                                                                  |
| <span data-ttu-id="62762-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="62762-138">Is Indexed</span></span>             | <span data-ttu-id="62762-139">否</span><span class="sxs-lookup"><span data-stu-id="62762-139">False</span></span>                                                                  |
| <span data-ttu-id="62762-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="62762-140">In Global Catalog</span></span>      | <span data-ttu-id="62762-141">否</span><span class="sxs-lookup"><span data-stu-id="62762-141">False</span></span>                                                                  |
| <span data-ttu-id="62762-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="62762-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="62762-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="62762-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="62762-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62762-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62762-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-146">Search-Flags</span></span>           | <span data-ttu-id="62762-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62762-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="62762-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-148">System-Flags</span></span>           | <span data-ttu-id="62762-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62762-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="62762-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="62762-150">Classes used in</span></span>        | [<span data-ttu-id="62762-151">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="62762-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="62762-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="62762-152">Windows Server 2003</span></span>



| <span data-ttu-id="62762-153">進入</span><span class="sxs-lookup"><span data-stu-id="62762-153">Entry</span></span> | <span data-ttu-id="62762-154">值</span><span class="sxs-lookup"><span data-stu-id="62762-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="62762-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="62762-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62762-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="62762-157">System-Only</span></span>            | <span data-ttu-id="62762-158">否</span><span class="sxs-lookup"><span data-stu-id="62762-158">False</span></span>                                                                  |
| <span data-ttu-id="62762-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="62762-159">Is-Single-Valued</span></span>       | <span data-ttu-id="62762-160">否</span><span class="sxs-lookup"><span data-stu-id="62762-160">False</span></span>                                                                  |
| <span data-ttu-id="62762-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="62762-161">Is Indexed</span></span>             | <span data-ttu-id="62762-162">否</span><span class="sxs-lookup"><span data-stu-id="62762-162">False</span></span>                                                                  |
| <span data-ttu-id="62762-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="62762-163">In Global Catalog</span></span>      | <span data-ttu-id="62762-164">否</span><span class="sxs-lookup"><span data-stu-id="62762-164">False</span></span>                                                                  |
| <span data-ttu-id="62762-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="62762-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="62762-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="62762-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="62762-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62762-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62762-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-169">Search-Flags</span></span>           | <span data-ttu-id="62762-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62762-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="62762-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-171">System-Flags</span></span>           | <span data-ttu-id="62762-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62762-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="62762-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="62762-173">Classes used in</span></span>        | [<span data-ttu-id="62762-174">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="62762-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="62762-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="62762-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="62762-176">進入</span><span class="sxs-lookup"><span data-stu-id="62762-176">Entry</span></span> | <span data-ttu-id="62762-177">值</span><span class="sxs-lookup"><span data-stu-id="62762-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="62762-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="62762-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62762-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="62762-180">System-Only</span></span>            | <span data-ttu-id="62762-181">否</span><span class="sxs-lookup"><span data-stu-id="62762-181">False</span></span>                                                                  |
| <span data-ttu-id="62762-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="62762-182">Is-Single-Valued</span></span>       | <span data-ttu-id="62762-183">否</span><span class="sxs-lookup"><span data-stu-id="62762-183">False</span></span>                                                                  |
| <span data-ttu-id="62762-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="62762-184">Is Indexed</span></span>             | <span data-ttu-id="62762-185">否</span><span class="sxs-lookup"><span data-stu-id="62762-185">False</span></span>                                                                  |
| <span data-ttu-id="62762-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="62762-186">In Global Catalog</span></span>      | <span data-ttu-id="62762-187">否</span><span class="sxs-lookup"><span data-stu-id="62762-187">False</span></span>                                                                  |
| <span data-ttu-id="62762-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="62762-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="62762-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="62762-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="62762-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62762-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62762-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-192">Search-Flags</span></span>           | <span data-ttu-id="62762-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62762-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="62762-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-194">System-Flags</span></span>           | <span data-ttu-id="62762-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62762-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="62762-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="62762-196">Classes used in</span></span>        | [<span data-ttu-id="62762-197">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="62762-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="62762-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62762-198">Windows Server 2008</span></span>



| <span data-ttu-id="62762-199">進入</span><span class="sxs-lookup"><span data-stu-id="62762-199">Entry</span></span> | <span data-ttu-id="62762-200">值</span><span class="sxs-lookup"><span data-stu-id="62762-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="62762-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="62762-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62762-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="62762-203">System-Only</span></span>            | <span data-ttu-id="62762-204">否</span><span class="sxs-lookup"><span data-stu-id="62762-204">False</span></span>                                                                  |
| <span data-ttu-id="62762-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="62762-205">Is-Single-Valued</span></span>       | <span data-ttu-id="62762-206">否</span><span class="sxs-lookup"><span data-stu-id="62762-206">False</span></span>                                                                  |
| <span data-ttu-id="62762-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="62762-207">Is Indexed</span></span>             | <span data-ttu-id="62762-208">否</span><span class="sxs-lookup"><span data-stu-id="62762-208">False</span></span>                                                                  |
| <span data-ttu-id="62762-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="62762-209">In Global Catalog</span></span>      | <span data-ttu-id="62762-210">否</span><span class="sxs-lookup"><span data-stu-id="62762-210">False</span></span>                                                                  |
| <span data-ttu-id="62762-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="62762-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="62762-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="62762-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="62762-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62762-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62762-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-215">Search-Flags</span></span>           | <span data-ttu-id="62762-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62762-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="62762-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-217">System-Flags</span></span>           | <span data-ttu-id="62762-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62762-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="62762-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="62762-219">Classes used in</span></span>        | [<span data-ttu-id="62762-220">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="62762-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="62762-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="62762-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="62762-222">進入</span><span class="sxs-lookup"><span data-stu-id="62762-222">Entry</span></span> | <span data-ttu-id="62762-223">值</span><span class="sxs-lookup"><span data-stu-id="62762-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="62762-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="62762-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62762-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="62762-226">System-Only</span></span>            | <span data-ttu-id="62762-227">否</span><span class="sxs-lookup"><span data-stu-id="62762-227">False</span></span>                                                                  |
| <span data-ttu-id="62762-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="62762-228">Is-Single-Valued</span></span>       | <span data-ttu-id="62762-229">否</span><span class="sxs-lookup"><span data-stu-id="62762-229">False</span></span>                                                                  |
| <span data-ttu-id="62762-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="62762-230">Is Indexed</span></span>             | <span data-ttu-id="62762-231">否</span><span class="sxs-lookup"><span data-stu-id="62762-231">False</span></span>                                                                  |
| <span data-ttu-id="62762-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="62762-232">In Global Catalog</span></span>      | <span data-ttu-id="62762-233">否</span><span class="sxs-lookup"><span data-stu-id="62762-233">False</span></span>                                                                  |
| <span data-ttu-id="62762-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="62762-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="62762-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="62762-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="62762-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62762-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62762-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-238">Search-Flags</span></span>           | <span data-ttu-id="62762-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62762-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="62762-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-240">System-Flags</span></span>           | <span data-ttu-id="62762-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62762-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="62762-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="62762-242">Classes used in</span></span>        | [<span data-ttu-id="62762-243">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="62762-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="62762-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62762-244">Windows Server 2012</span></span>



| <span data-ttu-id="62762-245">進入</span><span class="sxs-lookup"><span data-stu-id="62762-245">Entry</span></span> | <span data-ttu-id="62762-246">值</span><span class="sxs-lookup"><span data-stu-id="62762-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="62762-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="62762-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62762-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="62762-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="62762-249">System-Only</span></span>            | <span data-ttu-id="62762-250">否</span><span class="sxs-lookup"><span data-stu-id="62762-250">False</span></span>                                                                  |
| <span data-ttu-id="62762-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="62762-251">Is-Single-Valued</span></span>       | <span data-ttu-id="62762-252">否</span><span class="sxs-lookup"><span data-stu-id="62762-252">False</span></span>                                                                  |
| <span data-ttu-id="62762-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="62762-253">Is Indexed</span></span>             | <span data-ttu-id="62762-254">否</span><span class="sxs-lookup"><span data-stu-id="62762-254">False</span></span>                                                                  |
| <span data-ttu-id="62762-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="62762-255">In Global Catalog</span></span>      | <span data-ttu-id="62762-256">否</span><span class="sxs-lookup"><span data-stu-id="62762-256">False</span></span>                                                                  |
| <span data-ttu-id="62762-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="62762-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="62762-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="62762-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="62762-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62762-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62762-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="62762-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-261">Search-Flags</span></span>           | <span data-ttu-id="62762-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62762-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="62762-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62762-263">System-Flags</span></span>           | <span data-ttu-id="62762-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62762-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="62762-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="62762-265">Classes used in</span></span>        | [<span data-ttu-id="62762-266">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="62762-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 






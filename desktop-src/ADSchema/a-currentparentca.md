---
title: Current-父系-CA 屬性
description: 參考為憑證授權單位單位發出目前憑證的憑證授權單位單位。
ms.assetid: 9b851a7f-4a69-46f2-b7e2-6ee0b2d8eec1
ms.tgt_platform: multiple
keywords:
- Current-父系-CA 屬性 AD 架構
- currentParentCA 屬性 AD 架構
topic_type:
- apiref
api_name:
- Current-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26be2ccda41d998ed2b2b2c5dcddb1fcd2dcb2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935294"
---
# <a name="current-parent-ca-attribute"></a><span data-ttu-id="44131-105">Current-父系-CA 屬性</span><span class="sxs-lookup"><span data-stu-id="44131-105">Current-Parent-CA attribute</span></span>

<span data-ttu-id="44131-106">參考為憑證授權單位單位發出目前憑證的憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="44131-106">Reference to the certification authorities that issued the current certificates for a certification authority.</span></span>



| <span data-ttu-id="44131-107">進入</span><span class="sxs-lookup"><span data-stu-id="44131-107">Entry</span></span> | <span data-ttu-id="44131-108">值</span><span class="sxs-lookup"><span data-stu-id="44131-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="44131-109">CN</span><span class="sxs-lookup"><span data-stu-id="44131-109">CN</span></span>                | <span data-ttu-id="44131-110">Current-父系-CA</span><span class="sxs-lookup"><span data-stu-id="44131-110">Current-Parent-CA</span></span>                       |
| <span data-ttu-id="44131-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="44131-111">Ldap-Display-Name</span></span> | <span data-ttu-id="44131-112">currentParentCA</span><span class="sxs-lookup"><span data-stu-id="44131-112">currentParentCA</span></span>                         |
| <span data-ttu-id="44131-113">大小</span><span class="sxs-lookup"><span data-stu-id="44131-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="44131-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="44131-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="44131-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="44131-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="44131-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="44131-116">Attribute-Id</span></span>      | <span data-ttu-id="44131-117">1.2.840.113556.1.4.696</span><span class="sxs-lookup"><span data-stu-id="44131-117">1.2.840.113556.1.4.696</span></span>                  |
| <span data-ttu-id="44131-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="44131-118">System-Id-Guid</span></span>    | <span data-ttu-id="44131-119">963d273f-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="44131-119">963d273f-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="44131-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="44131-120">Syntax</span></span>            | [<span data-ttu-id="44131-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="44131-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="44131-122">實作</span><span class="sxs-lookup"><span data-stu-id="44131-122">Implementations</span></span>

-   [<span data-ttu-id="44131-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="44131-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="44131-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="44131-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="44131-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="44131-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="44131-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="44131-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="44131-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="44131-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="44131-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="44131-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="44131-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44131-129">Windows 2000 Server</span></span>



| <span data-ttu-id="44131-130">進入</span><span class="sxs-lookup"><span data-stu-id="44131-130">Entry</span></span> | <span data-ttu-id="44131-131">值</span><span class="sxs-lookup"><span data-stu-id="44131-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="44131-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="44131-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44131-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="44131-134">System-Only</span></span>            | <span data-ttu-id="44131-135">否</span><span class="sxs-lookup"><span data-stu-id="44131-135">False</span></span>                                                                  |
| <span data-ttu-id="44131-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="44131-136">Is-Single-Valued</span></span>       | <span data-ttu-id="44131-137">否</span><span class="sxs-lookup"><span data-stu-id="44131-137">False</span></span>                                                                  |
| <span data-ttu-id="44131-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="44131-138">Is Indexed</span></span>             | <span data-ttu-id="44131-139">否</span><span class="sxs-lookup"><span data-stu-id="44131-139">False</span></span>                                                                  |
| <span data-ttu-id="44131-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="44131-140">In Global Catalog</span></span>      | <span data-ttu-id="44131-141">否</span><span class="sxs-lookup"><span data-stu-id="44131-141">False</span></span>                                                                  |
| <span data-ttu-id="44131-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="44131-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="44131-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="44131-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="44131-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44131-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44131-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-146">Search-Flags</span></span>           | <span data-ttu-id="44131-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44131-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="44131-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-148">System-Flags</span></span>           | <span data-ttu-id="44131-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44131-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="44131-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="44131-150">Classes used in</span></span>        | [<span data-ttu-id="44131-151">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="44131-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="44131-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="44131-152">Windows Server 2003</span></span>



| <span data-ttu-id="44131-153">進入</span><span class="sxs-lookup"><span data-stu-id="44131-153">Entry</span></span> | <span data-ttu-id="44131-154">值</span><span class="sxs-lookup"><span data-stu-id="44131-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="44131-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="44131-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44131-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="44131-157">System-Only</span></span>            | <span data-ttu-id="44131-158">否</span><span class="sxs-lookup"><span data-stu-id="44131-158">False</span></span>                                                                  |
| <span data-ttu-id="44131-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="44131-159">Is-Single-Valued</span></span>       | <span data-ttu-id="44131-160">否</span><span class="sxs-lookup"><span data-stu-id="44131-160">False</span></span>                                                                  |
| <span data-ttu-id="44131-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="44131-161">Is Indexed</span></span>             | <span data-ttu-id="44131-162">否</span><span class="sxs-lookup"><span data-stu-id="44131-162">False</span></span>                                                                  |
| <span data-ttu-id="44131-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="44131-163">In Global Catalog</span></span>      | <span data-ttu-id="44131-164">否</span><span class="sxs-lookup"><span data-stu-id="44131-164">False</span></span>                                                                  |
| <span data-ttu-id="44131-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="44131-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="44131-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="44131-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="44131-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44131-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44131-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-169">Search-Flags</span></span>           | <span data-ttu-id="44131-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44131-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="44131-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-171">System-Flags</span></span>           | <span data-ttu-id="44131-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44131-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="44131-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="44131-173">Classes used in</span></span>        | [<span data-ttu-id="44131-174">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="44131-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="44131-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="44131-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="44131-176">進入</span><span class="sxs-lookup"><span data-stu-id="44131-176">Entry</span></span> | <span data-ttu-id="44131-177">值</span><span class="sxs-lookup"><span data-stu-id="44131-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="44131-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="44131-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44131-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="44131-180">System-Only</span></span>            | <span data-ttu-id="44131-181">否</span><span class="sxs-lookup"><span data-stu-id="44131-181">False</span></span>                                                                  |
| <span data-ttu-id="44131-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="44131-182">Is-Single-Valued</span></span>       | <span data-ttu-id="44131-183">否</span><span class="sxs-lookup"><span data-stu-id="44131-183">False</span></span>                                                                  |
| <span data-ttu-id="44131-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="44131-184">Is Indexed</span></span>             | <span data-ttu-id="44131-185">否</span><span class="sxs-lookup"><span data-stu-id="44131-185">False</span></span>                                                                  |
| <span data-ttu-id="44131-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="44131-186">In Global Catalog</span></span>      | <span data-ttu-id="44131-187">否</span><span class="sxs-lookup"><span data-stu-id="44131-187">False</span></span>                                                                  |
| <span data-ttu-id="44131-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="44131-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="44131-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="44131-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="44131-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44131-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44131-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-192">Search-Flags</span></span>           | <span data-ttu-id="44131-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44131-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="44131-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-194">System-Flags</span></span>           | <span data-ttu-id="44131-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44131-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="44131-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="44131-196">Classes used in</span></span>        | [<span data-ttu-id="44131-197">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="44131-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="44131-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44131-198">Windows Server 2008</span></span>



| <span data-ttu-id="44131-199">進入</span><span class="sxs-lookup"><span data-stu-id="44131-199">Entry</span></span> | <span data-ttu-id="44131-200">值</span><span class="sxs-lookup"><span data-stu-id="44131-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="44131-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="44131-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44131-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="44131-203">System-Only</span></span>            | <span data-ttu-id="44131-204">否</span><span class="sxs-lookup"><span data-stu-id="44131-204">False</span></span>                                                                  |
| <span data-ttu-id="44131-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="44131-205">Is-Single-Valued</span></span>       | <span data-ttu-id="44131-206">否</span><span class="sxs-lookup"><span data-stu-id="44131-206">False</span></span>                                                                  |
| <span data-ttu-id="44131-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="44131-207">Is Indexed</span></span>             | <span data-ttu-id="44131-208">否</span><span class="sxs-lookup"><span data-stu-id="44131-208">False</span></span>                                                                  |
| <span data-ttu-id="44131-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="44131-209">In Global Catalog</span></span>      | <span data-ttu-id="44131-210">否</span><span class="sxs-lookup"><span data-stu-id="44131-210">False</span></span>                                                                  |
| <span data-ttu-id="44131-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="44131-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="44131-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="44131-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="44131-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44131-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44131-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-215">Search-Flags</span></span>           | <span data-ttu-id="44131-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44131-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="44131-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-217">System-Flags</span></span>           | <span data-ttu-id="44131-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44131-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="44131-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="44131-219">Classes used in</span></span>        | [<span data-ttu-id="44131-220">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="44131-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="44131-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="44131-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="44131-222">進入</span><span class="sxs-lookup"><span data-stu-id="44131-222">Entry</span></span> | <span data-ttu-id="44131-223">值</span><span class="sxs-lookup"><span data-stu-id="44131-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="44131-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="44131-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44131-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="44131-226">System-Only</span></span>            | <span data-ttu-id="44131-227">否</span><span class="sxs-lookup"><span data-stu-id="44131-227">False</span></span>                                                                  |
| <span data-ttu-id="44131-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="44131-228">Is-Single-Valued</span></span>       | <span data-ttu-id="44131-229">否</span><span class="sxs-lookup"><span data-stu-id="44131-229">False</span></span>                                                                  |
| <span data-ttu-id="44131-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="44131-230">Is Indexed</span></span>             | <span data-ttu-id="44131-231">否</span><span class="sxs-lookup"><span data-stu-id="44131-231">False</span></span>                                                                  |
| <span data-ttu-id="44131-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="44131-232">In Global Catalog</span></span>      | <span data-ttu-id="44131-233">否</span><span class="sxs-lookup"><span data-stu-id="44131-233">False</span></span>                                                                  |
| <span data-ttu-id="44131-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="44131-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="44131-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="44131-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="44131-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44131-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44131-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-238">Search-Flags</span></span>           | <span data-ttu-id="44131-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44131-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="44131-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-240">System-Flags</span></span>           | <span data-ttu-id="44131-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44131-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="44131-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="44131-242">Classes used in</span></span>        | [<span data-ttu-id="44131-243">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="44131-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="44131-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44131-244">Windows Server 2012</span></span>



| <span data-ttu-id="44131-245">進入</span><span class="sxs-lookup"><span data-stu-id="44131-245">Entry</span></span> | <span data-ttu-id="44131-246">值</span><span class="sxs-lookup"><span data-stu-id="44131-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="44131-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="44131-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44131-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="44131-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="44131-249">System-Only</span></span>            | <span data-ttu-id="44131-250">否</span><span class="sxs-lookup"><span data-stu-id="44131-250">False</span></span>                                                                  |
| <span data-ttu-id="44131-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="44131-251">Is-Single-Valued</span></span>       | <span data-ttu-id="44131-252">否</span><span class="sxs-lookup"><span data-stu-id="44131-252">False</span></span>                                                                  |
| <span data-ttu-id="44131-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="44131-253">Is Indexed</span></span>             | <span data-ttu-id="44131-254">否</span><span class="sxs-lookup"><span data-stu-id="44131-254">False</span></span>                                                                  |
| <span data-ttu-id="44131-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="44131-255">In Global Catalog</span></span>      | <span data-ttu-id="44131-256">否</span><span class="sxs-lookup"><span data-stu-id="44131-256">False</span></span>                                                                  |
| <span data-ttu-id="44131-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="44131-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="44131-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="44131-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="44131-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44131-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44131-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="44131-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-261">Search-Flags</span></span>           | <span data-ttu-id="44131-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44131-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="44131-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44131-263">System-Flags</span></span>           | <span data-ttu-id="44131-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44131-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="44131-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="44131-265">Classes used in</span></span>        | [<span data-ttu-id="44131-266">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="44131-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 






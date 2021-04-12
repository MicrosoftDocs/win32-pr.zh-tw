---
title: 網域識別碼屬性
description: 參考與憑證授權單位單位相關聯的網域。
ms.assetid: dd2f0822-cf94-485b-8d21-8954dddb81ad
ms.tgt_platform: multiple
keywords:
- 網域識別碼屬性 AD 架構
- domainID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Domain-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6c321fdea062ccbca907e22a2d72b06c26110ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385358"
---
# <a name="domain-id-attribute"></a><span data-ttu-id="7838c-105">網域識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="7838c-105">Domain-ID attribute</span></span>

<span data-ttu-id="7838c-106">參考與憑證授權單位單位相關聯的網域。</span><span class="sxs-lookup"><span data-stu-id="7838c-106">Reference to a domain that is associated with a certification authority.</span></span>



| <span data-ttu-id="7838c-107">進入</span><span class="sxs-lookup"><span data-stu-id="7838c-107">Entry</span></span> | <span data-ttu-id="7838c-108">值</span><span class="sxs-lookup"><span data-stu-id="7838c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7838c-109">CN</span><span class="sxs-lookup"><span data-stu-id="7838c-109">CN</span></span>                | <span data-ttu-id="7838c-110">網域識別碼</span><span class="sxs-lookup"><span data-stu-id="7838c-110">Domain-ID</span></span>                               |
| <span data-ttu-id="7838c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7838c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7838c-112">domainID</span><span class="sxs-lookup"><span data-stu-id="7838c-112">domainID</span></span>                                |
| <span data-ttu-id="7838c-113">大小</span><span class="sxs-lookup"><span data-stu-id="7838c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7838c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7838c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="7838c-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7838c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7838c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7838c-116">Attribute-Id</span></span>      | <span data-ttu-id="7838c-117">1.2.840.113556.1.4.686</span><span class="sxs-lookup"><span data-stu-id="7838c-117">1.2.840.113556.1.4.686</span></span>                  |
| <span data-ttu-id="7838c-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7838c-118">System-Id-Guid</span></span>    | <span data-ttu-id="7838c-119">963d2734-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7838c-119">963d2734-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="7838c-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="7838c-120">Syntax</span></span>            | [<span data-ttu-id="7838c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7838c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7838c-122">實作</span><span class="sxs-lookup"><span data-stu-id="7838c-122">Implementations</span></span>

-   [<span data-ttu-id="7838c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7838c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7838c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7838c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7838c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7838c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7838c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7838c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7838c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7838c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7838c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7838c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7838c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7838c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="7838c-130">進入</span><span class="sxs-lookup"><span data-stu-id="7838c-130">Entry</span></span> | <span data-ttu-id="7838c-131">值</span><span class="sxs-lookup"><span data-stu-id="7838c-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="7838c-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7838c-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7838c-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="7838c-134">System-Only</span></span>            | <span data-ttu-id="7838c-135">否</span><span class="sxs-lookup"><span data-stu-id="7838c-135">False</span></span>                                                                  |
| <span data-ttu-id="7838c-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7838c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="7838c-137">對</span><span class="sxs-lookup"><span data-stu-id="7838c-137">True</span></span>                                                                   |
| <span data-ttu-id="7838c-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7838c-138">Is Indexed</span></span>             | <span data-ttu-id="7838c-139">否</span><span class="sxs-lookup"><span data-stu-id="7838c-139">False</span></span>                                                                  |
| <span data-ttu-id="7838c-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7838c-140">In Global Catalog</span></span>      | <span data-ttu-id="7838c-141">否</span><span class="sxs-lookup"><span data-stu-id="7838c-141">False</span></span>                                                                  |
| <span data-ttu-id="7838c-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7838c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="7838c-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7838c-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="7838c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7838c-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7838c-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-146">Search-Flags</span></span>           | <span data-ttu-id="7838c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7838c-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="7838c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-148">System-Flags</span></span>           | <span data-ttu-id="7838c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7838c-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="7838c-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7838c-150">Classes used in</span></span>        | [<span data-ttu-id="7838c-151">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="7838c-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7838c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7838c-152">Windows Server 2003</span></span>



| <span data-ttu-id="7838c-153">進入</span><span class="sxs-lookup"><span data-stu-id="7838c-153">Entry</span></span> | <span data-ttu-id="7838c-154">值</span><span class="sxs-lookup"><span data-stu-id="7838c-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="7838c-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7838c-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7838c-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="7838c-157">System-Only</span></span>            | <span data-ttu-id="7838c-158">否</span><span class="sxs-lookup"><span data-stu-id="7838c-158">False</span></span>                                                                  |
| <span data-ttu-id="7838c-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7838c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="7838c-160">對</span><span class="sxs-lookup"><span data-stu-id="7838c-160">True</span></span>                                                                   |
| <span data-ttu-id="7838c-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7838c-161">Is Indexed</span></span>             | <span data-ttu-id="7838c-162">否</span><span class="sxs-lookup"><span data-stu-id="7838c-162">False</span></span>                                                                  |
| <span data-ttu-id="7838c-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7838c-163">In Global Catalog</span></span>      | <span data-ttu-id="7838c-164">否</span><span class="sxs-lookup"><span data-stu-id="7838c-164">False</span></span>                                                                  |
| <span data-ttu-id="7838c-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7838c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="7838c-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7838c-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="7838c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7838c-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7838c-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-169">Search-Flags</span></span>           | <span data-ttu-id="7838c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7838c-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="7838c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-171">System-Flags</span></span>           | <span data-ttu-id="7838c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7838c-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="7838c-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7838c-173">Classes used in</span></span>        | [<span data-ttu-id="7838c-174">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="7838c-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7838c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7838c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7838c-176">進入</span><span class="sxs-lookup"><span data-stu-id="7838c-176">Entry</span></span> | <span data-ttu-id="7838c-177">值</span><span class="sxs-lookup"><span data-stu-id="7838c-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="7838c-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7838c-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7838c-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="7838c-180">System-Only</span></span>            | <span data-ttu-id="7838c-181">否</span><span class="sxs-lookup"><span data-stu-id="7838c-181">False</span></span>                                                                  |
| <span data-ttu-id="7838c-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7838c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="7838c-183">對</span><span class="sxs-lookup"><span data-stu-id="7838c-183">True</span></span>                                                                   |
| <span data-ttu-id="7838c-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7838c-184">Is Indexed</span></span>             | <span data-ttu-id="7838c-185">否</span><span class="sxs-lookup"><span data-stu-id="7838c-185">False</span></span>                                                                  |
| <span data-ttu-id="7838c-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7838c-186">In Global Catalog</span></span>      | <span data-ttu-id="7838c-187">否</span><span class="sxs-lookup"><span data-stu-id="7838c-187">False</span></span>                                                                  |
| <span data-ttu-id="7838c-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7838c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="7838c-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7838c-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="7838c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7838c-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7838c-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-192">Search-Flags</span></span>           | <span data-ttu-id="7838c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7838c-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="7838c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-194">System-Flags</span></span>           | <span data-ttu-id="7838c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7838c-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="7838c-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7838c-196">Classes used in</span></span>        | [<span data-ttu-id="7838c-197">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="7838c-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7838c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7838c-198">Windows Server 2008</span></span>



| <span data-ttu-id="7838c-199">進入</span><span class="sxs-lookup"><span data-stu-id="7838c-199">Entry</span></span> | <span data-ttu-id="7838c-200">值</span><span class="sxs-lookup"><span data-stu-id="7838c-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="7838c-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7838c-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7838c-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="7838c-203">System-Only</span></span>            | <span data-ttu-id="7838c-204">否</span><span class="sxs-lookup"><span data-stu-id="7838c-204">False</span></span>                                                                  |
| <span data-ttu-id="7838c-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7838c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="7838c-206">對</span><span class="sxs-lookup"><span data-stu-id="7838c-206">True</span></span>                                                                   |
| <span data-ttu-id="7838c-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7838c-207">Is Indexed</span></span>             | <span data-ttu-id="7838c-208">否</span><span class="sxs-lookup"><span data-stu-id="7838c-208">False</span></span>                                                                  |
| <span data-ttu-id="7838c-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7838c-209">In Global Catalog</span></span>      | <span data-ttu-id="7838c-210">否</span><span class="sxs-lookup"><span data-stu-id="7838c-210">False</span></span>                                                                  |
| <span data-ttu-id="7838c-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7838c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="7838c-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7838c-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="7838c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7838c-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7838c-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-215">Search-Flags</span></span>           | <span data-ttu-id="7838c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7838c-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="7838c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-217">System-Flags</span></span>           | <span data-ttu-id="7838c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7838c-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="7838c-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7838c-219">Classes used in</span></span>        | [<span data-ttu-id="7838c-220">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="7838c-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7838c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7838c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7838c-222">進入</span><span class="sxs-lookup"><span data-stu-id="7838c-222">Entry</span></span> | <span data-ttu-id="7838c-223">值</span><span class="sxs-lookup"><span data-stu-id="7838c-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="7838c-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7838c-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7838c-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="7838c-226">System-Only</span></span>            | <span data-ttu-id="7838c-227">否</span><span class="sxs-lookup"><span data-stu-id="7838c-227">False</span></span>                                                                  |
| <span data-ttu-id="7838c-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7838c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="7838c-229">對</span><span class="sxs-lookup"><span data-stu-id="7838c-229">True</span></span>                                                                   |
| <span data-ttu-id="7838c-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7838c-230">Is Indexed</span></span>             | <span data-ttu-id="7838c-231">否</span><span class="sxs-lookup"><span data-stu-id="7838c-231">False</span></span>                                                                  |
| <span data-ttu-id="7838c-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7838c-232">In Global Catalog</span></span>      | <span data-ttu-id="7838c-233">否</span><span class="sxs-lookup"><span data-stu-id="7838c-233">False</span></span>                                                                  |
| <span data-ttu-id="7838c-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7838c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="7838c-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7838c-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="7838c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7838c-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7838c-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-238">Search-Flags</span></span>           | <span data-ttu-id="7838c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7838c-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="7838c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-240">System-Flags</span></span>           | <span data-ttu-id="7838c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7838c-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="7838c-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7838c-242">Classes used in</span></span>        | [<span data-ttu-id="7838c-243">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="7838c-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7838c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7838c-244">Windows Server 2012</span></span>



| <span data-ttu-id="7838c-245">進入</span><span class="sxs-lookup"><span data-stu-id="7838c-245">Entry</span></span> | <span data-ttu-id="7838c-246">值</span><span class="sxs-lookup"><span data-stu-id="7838c-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="7838c-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7838c-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7838c-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="7838c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="7838c-249">System-Only</span></span>            | <span data-ttu-id="7838c-250">否</span><span class="sxs-lookup"><span data-stu-id="7838c-250">False</span></span>                                                                  |
| <span data-ttu-id="7838c-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7838c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="7838c-252">對</span><span class="sxs-lookup"><span data-stu-id="7838c-252">True</span></span>                                                                   |
| <span data-ttu-id="7838c-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7838c-253">Is Indexed</span></span>             | <span data-ttu-id="7838c-254">否</span><span class="sxs-lookup"><span data-stu-id="7838c-254">False</span></span>                                                                  |
| <span data-ttu-id="7838c-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7838c-255">In Global Catalog</span></span>      | <span data-ttu-id="7838c-256">否</span><span class="sxs-lookup"><span data-stu-id="7838c-256">False</span></span>                                                                  |
| <span data-ttu-id="7838c-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7838c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="7838c-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7838c-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="7838c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7838c-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7838c-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="7838c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-261">Search-Flags</span></span>           | <span data-ttu-id="7838c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7838c-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="7838c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7838c-263">System-Flags</span></span>           | <span data-ttu-id="7838c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7838c-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="7838c-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7838c-265">Classes used in</span></span>        | [<span data-ttu-id="7838c-266">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="7838c-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 






---
title: ms RRAS-廠商-屬性-Entry 屬性
description: 字串，可讓廠商將路由器屬性新增至要在查詢中使用的 DS，格式為 AttributeName vendorID AttributeType。
ms.assetid: 07bc4d9b-eba9-456b-be21-cd7bb8a5b0b6
ms.tgt_platform: multiple
keywords:
- ms RRAS-廠商-屬性-輸入屬性 AD 架構
- msRRASVendorAttributeEntry 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-RRAS-Vendor-Attribute-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28ee353122107db5b1247860e9799db861b4d6bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467267"
---
# <a name="ms-rras-vendor-attribute-entry-attribute"></a><span data-ttu-id="c1392-105">ms RRAS-廠商-屬性-Entry 屬性</span><span class="sxs-lookup"><span data-stu-id="c1392-105">ms-RRAS-Vendor-Attribute-Entry attribute</span></span>

<span data-ttu-id="c1392-106">字串，可讓廠商將路由器屬性新增至 DS 以用於查詢，格式為 AttributeName： vendorID： AttributeType。</span><span class="sxs-lookup"><span data-stu-id="c1392-106">A string that enables vendors to add router attributes to the DS for use in queries, in the form AttributeName:vendorID:AttributeType.</span></span>



| <span data-ttu-id="c1392-107">進入</span><span class="sxs-lookup"><span data-stu-id="c1392-107">Entry</span></span> | <span data-ttu-id="c1392-108">值</span><span class="sxs-lookup"><span data-stu-id="c1392-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c1392-109">CN</span><span class="sxs-lookup"><span data-stu-id="c1392-109">CN</span></span>                | <span data-ttu-id="c1392-110">ms RRAS-廠商-屬性-Entry</span><span class="sxs-lookup"><span data-stu-id="c1392-110">ms-RRAS-Vendor-Attribute-Entry</span></span>              |
| <span data-ttu-id="c1392-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c1392-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c1392-112">msRRASVendorAttributeEntry</span><span class="sxs-lookup"><span data-stu-id="c1392-112">msRRASVendorAttributeEntry</span></span>                  |
| <span data-ttu-id="c1392-113">大小</span><span class="sxs-lookup"><span data-stu-id="c1392-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c1392-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c1392-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="c1392-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c1392-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c1392-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c1392-116">Attribute-Id</span></span>      | <span data-ttu-id="c1392-117">1.2.840.113556.1.4.883</span><span class="sxs-lookup"><span data-stu-id="c1392-117">1.2.840.113556.1.4.883</span></span>                      |
| <span data-ttu-id="c1392-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c1392-118">System-Id-Guid</span></span>    | <span data-ttu-id="c1392-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c1392-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span></span>        |
| <span data-ttu-id="c1392-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1392-120">Syntax</span></span>            | [<span data-ttu-id="c1392-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c1392-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c1392-122">實作</span><span class="sxs-lookup"><span data-stu-id="c1392-122">Implementations</span></span>

-   [<span data-ttu-id="c1392-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c1392-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c1392-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c1392-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c1392-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c1392-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c1392-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c1392-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c1392-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c1392-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c1392-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c1392-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c1392-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1392-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c1392-130">進入</span><span class="sxs-lookup"><span data-stu-id="c1392-130">Entry</span></span> | <span data-ttu-id="c1392-131">值</span><span class="sxs-lookup"><span data-stu-id="c1392-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1392-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1392-132">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1392-133">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1392-134">System-Only</span></span>            | <span data-ttu-id="c1392-135">否</span><span class="sxs-lookup"><span data-stu-id="c1392-135">False</span></span>                                                                               |
| <span data-ttu-id="c1392-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1392-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c1392-137">否</span><span class="sxs-lookup"><span data-stu-id="c1392-137">False</span></span>                                                                               |
| <span data-ttu-id="c1392-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1392-138">Is Indexed</span></span>             | <span data-ttu-id="c1392-139">否</span><span class="sxs-lookup"><span data-stu-id="c1392-139">False</span></span>                                                                               |
| <span data-ttu-id="c1392-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1392-140">In Global Catalog</span></span>      | <span data-ttu-id="c1392-141">否</span><span class="sxs-lookup"><span data-stu-id="c1392-141">False</span></span>                                                                               |
| <span data-ttu-id="c1392-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1392-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1392-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1392-143">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="c1392-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1392-144">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1392-145">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-146">Search-Flags</span></span>           | <span data-ttu-id="c1392-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1392-147">0x00000000</span></span>                                                                          |
| <span data-ttu-id="c1392-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-148">System-Flags</span></span>           | <span data-ttu-id="c1392-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1392-149">0x00000010</span></span>                                                                          |
| <span data-ttu-id="c1392-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1392-150">Classes used in</span></span>        | [<span data-ttu-id="c1392-151">**RRAS-管理-字典**</span><span class="sxs-lookup"><span data-stu-id="c1392-151">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c1392-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1392-152">Windows Server 2003</span></span>



| <span data-ttu-id="c1392-153">進入</span><span class="sxs-lookup"><span data-stu-id="c1392-153">Entry</span></span> | <span data-ttu-id="c1392-154">值</span><span class="sxs-lookup"><span data-stu-id="c1392-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1392-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1392-155">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1392-156">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1392-157">System-Only</span></span>            | <span data-ttu-id="c1392-158">否</span><span class="sxs-lookup"><span data-stu-id="c1392-158">False</span></span>                                                                               |
| <span data-ttu-id="c1392-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1392-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c1392-160">否</span><span class="sxs-lookup"><span data-stu-id="c1392-160">False</span></span>                                                                               |
| <span data-ttu-id="c1392-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1392-161">Is Indexed</span></span>             | <span data-ttu-id="c1392-162">否</span><span class="sxs-lookup"><span data-stu-id="c1392-162">False</span></span>                                                                               |
| <span data-ttu-id="c1392-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1392-163">In Global Catalog</span></span>      | <span data-ttu-id="c1392-164">否</span><span class="sxs-lookup"><span data-stu-id="c1392-164">False</span></span>                                                                               |
| <span data-ttu-id="c1392-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1392-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1392-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1392-166">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="c1392-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1392-167">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1392-168">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-169">Search-Flags</span></span>           | <span data-ttu-id="c1392-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1392-170">0x00000000</span></span>                                                                          |
| <span data-ttu-id="c1392-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-171">System-Flags</span></span>           | <span data-ttu-id="c1392-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1392-172">0x00000010</span></span>                                                                          |
| <span data-ttu-id="c1392-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1392-173">Classes used in</span></span>        | [<span data-ttu-id="c1392-174">**RRAS-管理-字典**</span><span class="sxs-lookup"><span data-stu-id="c1392-174">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c1392-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c1392-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c1392-176">進入</span><span class="sxs-lookup"><span data-stu-id="c1392-176">Entry</span></span> | <span data-ttu-id="c1392-177">值</span><span class="sxs-lookup"><span data-stu-id="c1392-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1392-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1392-178">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1392-179">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1392-180">System-Only</span></span>            | <span data-ttu-id="c1392-181">否</span><span class="sxs-lookup"><span data-stu-id="c1392-181">False</span></span>                                                                               |
| <span data-ttu-id="c1392-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1392-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c1392-183">否</span><span class="sxs-lookup"><span data-stu-id="c1392-183">False</span></span>                                                                               |
| <span data-ttu-id="c1392-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1392-184">Is Indexed</span></span>             | <span data-ttu-id="c1392-185">否</span><span class="sxs-lookup"><span data-stu-id="c1392-185">False</span></span>                                                                               |
| <span data-ttu-id="c1392-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1392-186">In Global Catalog</span></span>      | <span data-ttu-id="c1392-187">否</span><span class="sxs-lookup"><span data-stu-id="c1392-187">False</span></span>                                                                               |
| <span data-ttu-id="c1392-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1392-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1392-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1392-189">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="c1392-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1392-190">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1392-191">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-192">Search-Flags</span></span>           | <span data-ttu-id="c1392-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1392-193">0x00000000</span></span>                                                                          |
| <span data-ttu-id="c1392-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-194">System-Flags</span></span>           | <span data-ttu-id="c1392-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1392-195">0x00000010</span></span>                                                                          |
| <span data-ttu-id="c1392-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1392-196">Classes used in</span></span>        | [<span data-ttu-id="c1392-197">**RRAS-管理-字典**</span><span class="sxs-lookup"><span data-stu-id="c1392-197">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c1392-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1392-198">Windows Server 2008</span></span>



| <span data-ttu-id="c1392-199">進入</span><span class="sxs-lookup"><span data-stu-id="c1392-199">Entry</span></span> | <span data-ttu-id="c1392-200">值</span><span class="sxs-lookup"><span data-stu-id="c1392-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1392-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1392-201">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1392-202">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1392-203">System-Only</span></span>            | <span data-ttu-id="c1392-204">否</span><span class="sxs-lookup"><span data-stu-id="c1392-204">False</span></span>                                                                               |
| <span data-ttu-id="c1392-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1392-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c1392-206">否</span><span class="sxs-lookup"><span data-stu-id="c1392-206">False</span></span>                                                                               |
| <span data-ttu-id="c1392-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1392-207">Is Indexed</span></span>             | <span data-ttu-id="c1392-208">否</span><span class="sxs-lookup"><span data-stu-id="c1392-208">False</span></span>                                                                               |
| <span data-ttu-id="c1392-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1392-209">In Global Catalog</span></span>      | <span data-ttu-id="c1392-210">否</span><span class="sxs-lookup"><span data-stu-id="c1392-210">False</span></span>                                                                               |
| <span data-ttu-id="c1392-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1392-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1392-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1392-212">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="c1392-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1392-213">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1392-214">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-215">Search-Flags</span></span>           | <span data-ttu-id="c1392-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1392-216">0x00000000</span></span>                                                                          |
| <span data-ttu-id="c1392-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-217">System-Flags</span></span>           | <span data-ttu-id="c1392-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1392-218">0x00000010</span></span>                                                                          |
| <span data-ttu-id="c1392-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1392-219">Classes used in</span></span>        | [<span data-ttu-id="c1392-220">**RRAS-管理-字典**</span><span class="sxs-lookup"><span data-stu-id="c1392-220">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c1392-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1392-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c1392-222">進入</span><span class="sxs-lookup"><span data-stu-id="c1392-222">Entry</span></span> | <span data-ttu-id="c1392-223">值</span><span class="sxs-lookup"><span data-stu-id="c1392-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1392-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1392-224">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1392-225">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1392-226">System-Only</span></span>            | <span data-ttu-id="c1392-227">否</span><span class="sxs-lookup"><span data-stu-id="c1392-227">False</span></span>                                                                               |
| <span data-ttu-id="c1392-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1392-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c1392-229">否</span><span class="sxs-lookup"><span data-stu-id="c1392-229">False</span></span>                                                                               |
| <span data-ttu-id="c1392-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1392-230">Is Indexed</span></span>             | <span data-ttu-id="c1392-231">否</span><span class="sxs-lookup"><span data-stu-id="c1392-231">False</span></span>                                                                               |
| <span data-ttu-id="c1392-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1392-232">In Global Catalog</span></span>      | <span data-ttu-id="c1392-233">否</span><span class="sxs-lookup"><span data-stu-id="c1392-233">False</span></span>                                                                               |
| <span data-ttu-id="c1392-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1392-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1392-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1392-235">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="c1392-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1392-236">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1392-237">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-238">Search-Flags</span></span>           | <span data-ttu-id="c1392-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1392-239">0x00000000</span></span>                                                                          |
| <span data-ttu-id="c1392-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-240">System-Flags</span></span>           | <span data-ttu-id="c1392-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1392-241">0x00000010</span></span>                                                                          |
| <span data-ttu-id="c1392-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1392-242">Classes used in</span></span>        | [<span data-ttu-id="c1392-243">**RRAS-管理-字典**</span><span class="sxs-lookup"><span data-stu-id="c1392-243">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c1392-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1392-244">Windows Server 2012</span></span>



| <span data-ttu-id="c1392-245">進入</span><span class="sxs-lookup"><span data-stu-id="c1392-245">Entry</span></span> | <span data-ttu-id="c1392-246">值</span><span class="sxs-lookup"><span data-stu-id="c1392-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1392-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1392-247">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1392-248">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="c1392-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1392-249">System-Only</span></span>            | <span data-ttu-id="c1392-250">否</span><span class="sxs-lookup"><span data-stu-id="c1392-250">False</span></span>                                                                               |
| <span data-ttu-id="c1392-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1392-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c1392-252">否</span><span class="sxs-lookup"><span data-stu-id="c1392-252">False</span></span>                                                                               |
| <span data-ttu-id="c1392-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1392-253">Is Indexed</span></span>             | <span data-ttu-id="c1392-254">否</span><span class="sxs-lookup"><span data-stu-id="c1392-254">False</span></span>                                                                               |
| <span data-ttu-id="c1392-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1392-255">In Global Catalog</span></span>      | <span data-ttu-id="c1392-256">否</span><span class="sxs-lookup"><span data-stu-id="c1392-256">False</span></span>                                                                               |
| <span data-ttu-id="c1392-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1392-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1392-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1392-258">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="c1392-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1392-259">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1392-260">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="c1392-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-261">Search-Flags</span></span>           | <span data-ttu-id="c1392-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1392-262">0x00000000</span></span>                                                                          |
| <span data-ttu-id="c1392-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1392-263">System-Flags</span></span>           | <span data-ttu-id="c1392-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1392-264">0x00000010</span></span>                                                                          |
| <span data-ttu-id="c1392-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1392-265">Classes used in</span></span>        | [<span data-ttu-id="c1392-266">**RRAS-管理-字典**</span><span class="sxs-lookup"><span data-stu-id="c1392-266">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



 

 






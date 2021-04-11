---
title: ms-PKI-RA-原則屬性
description: 包含簽署註冊要求之註冊授權單位中的必要原則 Oid 清單。
ms.assetid: ebbdf95e-05c8-4b54-b7a5-4bb81d425225
ms.tgt_platform: multiple
keywords:
- ms-PKI-RA-原則屬性 AD 架構
- Mspki-certificate-name-flag-RA-原則屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-RA-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b948dac7a95ae8b46972ace4d1ab46260b476da
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935524"
---
# <a name="ms-pki-ra-policies-attribute"></a><span data-ttu-id="76464-105">ms-PKI-RA-原則屬性</span><span class="sxs-lookup"><span data-stu-id="76464-105">ms-PKI-RA-Policies attribute</span></span>

<span data-ttu-id="76464-106">包含簽署註冊要求之註冊授權單位中的必要原則 Oid 清單。</span><span class="sxs-lookup"><span data-stu-id="76464-106">Contains the list of required policy OIDs from registration authorities who sign the enrollment request.</span></span>



| <span data-ttu-id="76464-107">進入</span><span class="sxs-lookup"><span data-stu-id="76464-107">Entry</span></span> | <span data-ttu-id="76464-108">值</span><span class="sxs-lookup"><span data-stu-id="76464-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76464-109">CN</span><span class="sxs-lookup"><span data-stu-id="76464-109">CN</span></span>                | <span data-ttu-id="76464-110">ms-PKI-RA-原則</span><span class="sxs-lookup"><span data-stu-id="76464-110">ms-PKI-RA-Policies</span></span>                                                                                |
| <span data-ttu-id="76464-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="76464-111">Ldap-Display-Name</span></span> | <span data-ttu-id="76464-112">Mspki-certificate-name-flag-RA-原則</span><span class="sxs-lookup"><span data-stu-id="76464-112">msPKI-RA-Policies</span></span>                                                                                 |
| <span data-ttu-id="76464-113">大小</span><span class="sxs-lookup"><span data-stu-id="76464-113">Size</span></span>              | <span data-ttu-id="76464-114">專案數目的64位元組倍。</span><span class="sxs-lookup"><span data-stu-id="76464-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="76464-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="76464-115">Update Privilege</span></span>  | <span data-ttu-id="76464-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="76464-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="76464-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="76464-117">Update Frequency</span></span>  | <span data-ttu-id="76464-118">當您編輯、建立或複製憑證範本時 (ms-PKI-憑證範本) 物件。</span><span class="sxs-lookup"><span data-stu-id="76464-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="76464-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="76464-119">Attribute-Id</span></span>      | <span data-ttu-id="76464-120">1.2.840.113556.1.4.1438</span><span class="sxs-lookup"><span data-stu-id="76464-120">1.2.840.113556.1.4.1438</span></span>                                                                           |
| <span data-ttu-id="76464-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="76464-121">System-Id-Guid</span></span>    | <span data-ttu-id="76464-122">d546ae22-0951-4d47-817e-1c9f96faad46</span><span class="sxs-lookup"><span data-stu-id="76464-122">d546ae22-0951-4d47-817e-1c9f96faad46</span></span>                                                              |
| <span data-ttu-id="76464-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="76464-123">Syntax</span></span>            | [<span data-ttu-id="76464-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="76464-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="76464-125">實作</span><span class="sxs-lookup"><span data-stu-id="76464-125">Implementations</span></span>

-   [<span data-ttu-id="76464-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="76464-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="76464-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="76464-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="76464-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="76464-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="76464-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="76464-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="76464-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="76464-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="76464-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76464-131">Windows Server 2003</span></span>



| <span data-ttu-id="76464-132">進入</span><span class="sxs-lookup"><span data-stu-id="76464-132">Entry</span></span> | <span data-ttu-id="76464-133">值</span><span class="sxs-lookup"><span data-stu-id="76464-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="76464-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76464-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76464-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="76464-136">System-Only</span></span>            | <span data-ttu-id="76464-137">否</span><span class="sxs-lookup"><span data-stu-id="76464-137">False</span></span>                                                                   |
| <span data-ttu-id="76464-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76464-138">Is-Single-Valued</span></span>       | <span data-ttu-id="76464-139">否</span><span class="sxs-lookup"><span data-stu-id="76464-139">False</span></span>                                                                   |
| <span data-ttu-id="76464-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76464-140">Is Indexed</span></span>             | <span data-ttu-id="76464-141">否</span><span class="sxs-lookup"><span data-stu-id="76464-141">False</span></span>                                                                   |
| <span data-ttu-id="76464-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76464-142">In Global Catalog</span></span>      | <span data-ttu-id="76464-143">否</span><span class="sxs-lookup"><span data-stu-id="76464-143">False</span></span>                                                                   |
| <span data-ttu-id="76464-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76464-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="76464-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76464-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="76464-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76464-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76464-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-148">Search-Flags</span></span>           | <span data-ttu-id="76464-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76464-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="76464-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-150">System-Flags</span></span>           | <span data-ttu-id="76464-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76464-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="76464-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76464-152">Classes used in</span></span>        | [<span data-ttu-id="76464-153">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="76464-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="76464-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="76464-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="76464-155">進入</span><span class="sxs-lookup"><span data-stu-id="76464-155">Entry</span></span> | <span data-ttu-id="76464-156">值</span><span class="sxs-lookup"><span data-stu-id="76464-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="76464-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76464-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76464-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="76464-159">System-Only</span></span>            | <span data-ttu-id="76464-160">否</span><span class="sxs-lookup"><span data-stu-id="76464-160">False</span></span>                                                                   |
| <span data-ttu-id="76464-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76464-161">Is-Single-Valued</span></span>       | <span data-ttu-id="76464-162">否</span><span class="sxs-lookup"><span data-stu-id="76464-162">False</span></span>                                                                   |
| <span data-ttu-id="76464-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76464-163">Is Indexed</span></span>             | <span data-ttu-id="76464-164">否</span><span class="sxs-lookup"><span data-stu-id="76464-164">False</span></span>                                                                   |
| <span data-ttu-id="76464-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76464-165">In Global Catalog</span></span>      | <span data-ttu-id="76464-166">否</span><span class="sxs-lookup"><span data-stu-id="76464-166">False</span></span>                                                                   |
| <span data-ttu-id="76464-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76464-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="76464-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76464-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="76464-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76464-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76464-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-171">Search-Flags</span></span>           | <span data-ttu-id="76464-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76464-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="76464-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-173">System-Flags</span></span>           | <span data-ttu-id="76464-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76464-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="76464-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76464-175">Classes used in</span></span>        | [<span data-ttu-id="76464-176">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="76464-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="76464-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76464-177">Windows Server 2008</span></span>



| <span data-ttu-id="76464-178">進入</span><span class="sxs-lookup"><span data-stu-id="76464-178">Entry</span></span> | <span data-ttu-id="76464-179">值</span><span class="sxs-lookup"><span data-stu-id="76464-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="76464-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76464-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76464-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="76464-182">System-Only</span></span>            | <span data-ttu-id="76464-183">否</span><span class="sxs-lookup"><span data-stu-id="76464-183">False</span></span>                                                                   |
| <span data-ttu-id="76464-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76464-184">Is-Single-Valued</span></span>       | <span data-ttu-id="76464-185">否</span><span class="sxs-lookup"><span data-stu-id="76464-185">False</span></span>                                                                   |
| <span data-ttu-id="76464-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76464-186">Is Indexed</span></span>             | <span data-ttu-id="76464-187">否</span><span class="sxs-lookup"><span data-stu-id="76464-187">False</span></span>                                                                   |
| <span data-ttu-id="76464-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76464-188">In Global Catalog</span></span>      | <span data-ttu-id="76464-189">否</span><span class="sxs-lookup"><span data-stu-id="76464-189">False</span></span>                                                                   |
| <span data-ttu-id="76464-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76464-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="76464-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76464-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="76464-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76464-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76464-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-194">Search-Flags</span></span>           | <span data-ttu-id="76464-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76464-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="76464-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-196">System-Flags</span></span>           | <span data-ttu-id="76464-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76464-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="76464-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76464-198">Classes used in</span></span>        | [<span data-ttu-id="76464-199">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="76464-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="76464-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76464-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="76464-201">進入</span><span class="sxs-lookup"><span data-stu-id="76464-201">Entry</span></span> | <span data-ttu-id="76464-202">值</span><span class="sxs-lookup"><span data-stu-id="76464-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="76464-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76464-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76464-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="76464-205">System-Only</span></span>            | <span data-ttu-id="76464-206">否</span><span class="sxs-lookup"><span data-stu-id="76464-206">False</span></span>                                                                   |
| <span data-ttu-id="76464-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76464-207">Is-Single-Valued</span></span>       | <span data-ttu-id="76464-208">否</span><span class="sxs-lookup"><span data-stu-id="76464-208">False</span></span>                                                                   |
| <span data-ttu-id="76464-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76464-209">Is Indexed</span></span>             | <span data-ttu-id="76464-210">否</span><span class="sxs-lookup"><span data-stu-id="76464-210">False</span></span>                                                                   |
| <span data-ttu-id="76464-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76464-211">In Global Catalog</span></span>      | <span data-ttu-id="76464-212">否</span><span class="sxs-lookup"><span data-stu-id="76464-212">False</span></span>                                                                   |
| <span data-ttu-id="76464-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76464-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="76464-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76464-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="76464-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76464-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76464-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-217">Search-Flags</span></span>           | <span data-ttu-id="76464-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76464-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="76464-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-219">System-Flags</span></span>           | <span data-ttu-id="76464-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76464-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="76464-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76464-221">Classes used in</span></span>        | [<span data-ttu-id="76464-222">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="76464-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="76464-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76464-223">Windows Server 2012</span></span>



| <span data-ttu-id="76464-224">進入</span><span class="sxs-lookup"><span data-stu-id="76464-224">Entry</span></span> | <span data-ttu-id="76464-225">值</span><span class="sxs-lookup"><span data-stu-id="76464-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="76464-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76464-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76464-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="76464-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="76464-228">System-Only</span></span>            | <span data-ttu-id="76464-229">否</span><span class="sxs-lookup"><span data-stu-id="76464-229">False</span></span>                                                                   |
| <span data-ttu-id="76464-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76464-230">Is-Single-Valued</span></span>       | <span data-ttu-id="76464-231">否</span><span class="sxs-lookup"><span data-stu-id="76464-231">False</span></span>                                                                   |
| <span data-ttu-id="76464-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76464-232">Is Indexed</span></span>             | <span data-ttu-id="76464-233">否</span><span class="sxs-lookup"><span data-stu-id="76464-233">False</span></span>                                                                   |
| <span data-ttu-id="76464-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76464-234">In Global Catalog</span></span>      | <span data-ttu-id="76464-235">否</span><span class="sxs-lookup"><span data-stu-id="76464-235">False</span></span>                                                                   |
| <span data-ttu-id="76464-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76464-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="76464-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76464-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="76464-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76464-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76464-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="76464-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-240">Search-Flags</span></span>           | <span data-ttu-id="76464-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76464-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="76464-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76464-242">System-Flags</span></span>           | <span data-ttu-id="76464-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76464-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="76464-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76464-244">Classes used in</span></span>        | [<span data-ttu-id="76464-245">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="76464-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






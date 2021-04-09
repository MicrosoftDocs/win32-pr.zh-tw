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
# <a name="ms-pki-ra-policies-attribute"></a><span data-ttu-id="5cbae-105">ms-PKI-RA-原則屬性</span><span class="sxs-lookup"><span data-stu-id="5cbae-105">ms-PKI-RA-Policies attribute</span></span>

<span data-ttu-id="5cbae-106">包含簽署註冊要求之註冊授權單位中的必要原則 Oid 清單。</span><span class="sxs-lookup"><span data-stu-id="5cbae-106">Contains the list of required policy OIDs from registration authorities who sign the enrollment request.</span></span>



| <span data-ttu-id="5cbae-107">進入</span><span class="sxs-lookup"><span data-stu-id="5cbae-107">Entry</span></span> | <span data-ttu-id="5cbae-108">值</span><span class="sxs-lookup"><span data-stu-id="5cbae-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cbae-109">CN</span><span class="sxs-lookup"><span data-stu-id="5cbae-109">CN</span></span>                | <span data-ttu-id="5cbae-110">ms-PKI-RA-原則</span><span class="sxs-lookup"><span data-stu-id="5cbae-110">ms-PKI-RA-Policies</span></span>                                                                                |
| <span data-ttu-id="5cbae-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5cbae-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5cbae-112">Mspki-certificate-name-flag-RA-原則</span><span class="sxs-lookup"><span data-stu-id="5cbae-112">msPKI-RA-Policies</span></span>                                                                                 |
| <span data-ttu-id="5cbae-113">大小</span><span class="sxs-lookup"><span data-stu-id="5cbae-113">Size</span></span>              | <span data-ttu-id="5cbae-114">專案數目的64位元組倍。</span><span class="sxs-lookup"><span data-stu-id="5cbae-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="5cbae-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5cbae-115">Update Privilege</span></span>  | <span data-ttu-id="5cbae-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="5cbae-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="5cbae-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5cbae-117">Update Frequency</span></span>  | <span data-ttu-id="5cbae-118">當您編輯、建立或複製憑證範本時 (ms-PKI-憑證範本) 物件。</span><span class="sxs-lookup"><span data-stu-id="5cbae-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="5cbae-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5cbae-119">Attribute-Id</span></span>      | <span data-ttu-id="5cbae-120">1.2.840.113556.1.4.1438</span><span class="sxs-lookup"><span data-stu-id="5cbae-120">1.2.840.113556.1.4.1438</span></span>                                                                           |
| <span data-ttu-id="5cbae-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5cbae-121">System-Id-Guid</span></span>    | <span data-ttu-id="5cbae-122">d546ae22-0951-4d47-817e-1c9f96faad46</span><span class="sxs-lookup"><span data-stu-id="5cbae-122">d546ae22-0951-4d47-817e-1c9f96faad46</span></span>                                                              |
| <span data-ttu-id="5cbae-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cbae-123">Syntax</span></span>            | [<span data-ttu-id="5cbae-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5cbae-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="5cbae-125">實作</span><span class="sxs-lookup"><span data-stu-id="5cbae-125">Implementations</span></span>

-   [<span data-ttu-id="5cbae-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5cbae-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5cbae-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5cbae-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5cbae-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5cbae-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5cbae-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5cbae-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5cbae-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5cbae-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5cbae-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5cbae-131">Windows Server 2003</span></span>



| <span data-ttu-id="5cbae-132">進入</span><span class="sxs-lookup"><span data-stu-id="5cbae-132">Entry</span></span> | <span data-ttu-id="5cbae-133">值</span><span class="sxs-lookup"><span data-stu-id="5cbae-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5cbae-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5cbae-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cbae-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cbae-136">System-Only</span></span>            | <span data-ttu-id="5cbae-137">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-137">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5cbae-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5cbae-139">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-139">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5cbae-140">Is Indexed</span></span>             | <span data-ttu-id="5cbae-141">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-141">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5cbae-142">In Global Catalog</span></span>      | <span data-ttu-id="5cbae-143">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-143">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5cbae-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cbae-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5cbae-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5cbae-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cbae-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cbae-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-148">Search-Flags</span></span>           | <span data-ttu-id="5cbae-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cbae-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="5cbae-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-150">System-Flags</span></span>           | <span data-ttu-id="5cbae-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cbae-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="5cbae-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5cbae-152">Classes used in</span></span>        | [<span data-ttu-id="5cbae-153">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="5cbae-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5cbae-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5cbae-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5cbae-155">進入</span><span class="sxs-lookup"><span data-stu-id="5cbae-155">Entry</span></span> | <span data-ttu-id="5cbae-156">值</span><span class="sxs-lookup"><span data-stu-id="5cbae-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5cbae-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5cbae-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cbae-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cbae-159">System-Only</span></span>            | <span data-ttu-id="5cbae-160">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-160">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5cbae-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5cbae-162">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-162">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5cbae-163">Is Indexed</span></span>             | <span data-ttu-id="5cbae-164">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-164">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5cbae-165">In Global Catalog</span></span>      | <span data-ttu-id="5cbae-166">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-166">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5cbae-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cbae-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5cbae-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5cbae-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cbae-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cbae-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-171">Search-Flags</span></span>           | <span data-ttu-id="5cbae-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cbae-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="5cbae-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-173">System-Flags</span></span>           | <span data-ttu-id="5cbae-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cbae-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="5cbae-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5cbae-175">Classes used in</span></span>        | [<span data-ttu-id="5cbae-176">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="5cbae-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5cbae-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cbae-177">Windows Server 2008</span></span>



| <span data-ttu-id="5cbae-178">進入</span><span class="sxs-lookup"><span data-stu-id="5cbae-178">Entry</span></span> | <span data-ttu-id="5cbae-179">值</span><span class="sxs-lookup"><span data-stu-id="5cbae-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5cbae-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5cbae-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cbae-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cbae-182">System-Only</span></span>            | <span data-ttu-id="5cbae-183">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-183">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5cbae-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5cbae-185">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-185">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5cbae-186">Is Indexed</span></span>             | <span data-ttu-id="5cbae-187">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-187">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5cbae-188">In Global Catalog</span></span>      | <span data-ttu-id="5cbae-189">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-189">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5cbae-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cbae-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5cbae-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5cbae-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cbae-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cbae-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-194">Search-Flags</span></span>           | <span data-ttu-id="5cbae-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cbae-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="5cbae-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-196">System-Flags</span></span>           | <span data-ttu-id="5cbae-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cbae-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="5cbae-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5cbae-198">Classes used in</span></span>        | [<span data-ttu-id="5cbae-199">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="5cbae-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5cbae-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5cbae-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5cbae-201">進入</span><span class="sxs-lookup"><span data-stu-id="5cbae-201">Entry</span></span> | <span data-ttu-id="5cbae-202">值</span><span class="sxs-lookup"><span data-stu-id="5cbae-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5cbae-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5cbae-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cbae-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cbae-205">System-Only</span></span>            | <span data-ttu-id="5cbae-206">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-206">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5cbae-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5cbae-208">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-208">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5cbae-209">Is Indexed</span></span>             | <span data-ttu-id="5cbae-210">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-210">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5cbae-211">In Global Catalog</span></span>      | <span data-ttu-id="5cbae-212">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-212">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5cbae-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cbae-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5cbae-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5cbae-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cbae-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cbae-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-217">Search-Flags</span></span>           | <span data-ttu-id="5cbae-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cbae-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="5cbae-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-219">System-Flags</span></span>           | <span data-ttu-id="5cbae-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cbae-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="5cbae-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5cbae-221">Classes used in</span></span>        | [<span data-ttu-id="5cbae-222">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="5cbae-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5cbae-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5cbae-223">Windows Server 2012</span></span>



| <span data-ttu-id="5cbae-224">進入</span><span class="sxs-lookup"><span data-stu-id="5cbae-224">Entry</span></span> | <span data-ttu-id="5cbae-225">值</span><span class="sxs-lookup"><span data-stu-id="5cbae-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5cbae-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5cbae-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cbae-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="5cbae-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cbae-228">System-Only</span></span>            | <span data-ttu-id="5cbae-229">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-229">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5cbae-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5cbae-231">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-231">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5cbae-232">Is Indexed</span></span>             | <span data-ttu-id="5cbae-233">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-233">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5cbae-234">In Global Catalog</span></span>      | <span data-ttu-id="5cbae-235">否</span><span class="sxs-lookup"><span data-stu-id="5cbae-235">False</span></span>                                                                   |
| <span data-ttu-id="5cbae-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5cbae-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cbae-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5cbae-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="5cbae-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cbae-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cbae-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="5cbae-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-240">Search-Flags</span></span>           | <span data-ttu-id="5cbae-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cbae-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="5cbae-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cbae-242">System-Flags</span></span>           | <span data-ttu-id="5cbae-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5cbae-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="5cbae-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5cbae-244">Classes used in</span></span>        | [<span data-ttu-id="5cbae-245">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="5cbae-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






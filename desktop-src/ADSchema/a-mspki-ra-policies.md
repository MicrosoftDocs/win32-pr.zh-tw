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
# <a name="ms-pki-ra-policies-attribute"></a><span data-ttu-id="e273f-105">ms-PKI-RA-原則屬性</span><span class="sxs-lookup"><span data-stu-id="e273f-105">ms-PKI-RA-Policies attribute</span></span>

<span data-ttu-id="e273f-106">包含簽署註冊要求之註冊授權單位中的必要原則 Oid 清單。</span><span class="sxs-lookup"><span data-stu-id="e273f-106">Contains the list of required policy OIDs from registration authorities who sign the enrollment request.</span></span>



| <span data-ttu-id="e273f-107">進入</span><span class="sxs-lookup"><span data-stu-id="e273f-107">Entry</span></span> | <span data-ttu-id="e273f-108">值</span><span class="sxs-lookup"><span data-stu-id="e273f-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e273f-109">CN</span><span class="sxs-lookup"><span data-stu-id="e273f-109">CN</span></span>                | <span data-ttu-id="e273f-110">ms-PKI-RA-原則</span><span class="sxs-lookup"><span data-stu-id="e273f-110">ms-PKI-RA-Policies</span></span>                                                                                |
| <span data-ttu-id="e273f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e273f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e273f-112">Mspki-certificate-name-flag-RA-原則</span><span class="sxs-lookup"><span data-stu-id="e273f-112">msPKI-RA-Policies</span></span>                                                                                 |
| <span data-ttu-id="e273f-113">大小</span><span class="sxs-lookup"><span data-stu-id="e273f-113">Size</span></span>              | <span data-ttu-id="e273f-114">專案數目的64位元組倍。</span><span class="sxs-lookup"><span data-stu-id="e273f-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="e273f-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e273f-115">Update Privilege</span></span>  | <span data-ttu-id="e273f-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="e273f-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="e273f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e273f-117">Update Frequency</span></span>  | <span data-ttu-id="e273f-118">當您編輯、建立或複製憑證範本時 (ms-PKI-憑證範本) 物件。</span><span class="sxs-lookup"><span data-stu-id="e273f-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="e273f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e273f-119">Attribute-Id</span></span>      | <span data-ttu-id="e273f-120">1.2.840.113556.1.4.1438</span><span class="sxs-lookup"><span data-stu-id="e273f-120">1.2.840.113556.1.4.1438</span></span>                                                                           |
| <span data-ttu-id="e273f-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e273f-121">System-Id-Guid</span></span>    | <span data-ttu-id="e273f-122">d546ae22-0951-4d47-817e-1c9f96faad46</span><span class="sxs-lookup"><span data-stu-id="e273f-122">d546ae22-0951-4d47-817e-1c9f96faad46</span></span>                                                              |
| <span data-ttu-id="e273f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e273f-123">Syntax</span></span>            | [<span data-ttu-id="e273f-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e273f-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="e273f-125">實作</span><span class="sxs-lookup"><span data-stu-id="e273f-125">Implementations</span></span>

-   [<span data-ttu-id="e273f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e273f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e273f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e273f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e273f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e273f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e273f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e273f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e273f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e273f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e273f-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e273f-131">Windows Server 2003</span></span>



| <span data-ttu-id="e273f-132">進入</span><span class="sxs-lookup"><span data-stu-id="e273f-132">Entry</span></span> | <span data-ttu-id="e273f-133">值</span><span class="sxs-lookup"><span data-stu-id="e273f-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e273f-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e273f-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e273f-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e273f-136">System-Only</span></span>            | <span data-ttu-id="e273f-137">否</span><span class="sxs-lookup"><span data-stu-id="e273f-137">False</span></span>                                                                   |
| <span data-ttu-id="e273f-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e273f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e273f-139">否</span><span class="sxs-lookup"><span data-stu-id="e273f-139">False</span></span>                                                                   |
| <span data-ttu-id="e273f-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e273f-140">Is Indexed</span></span>             | <span data-ttu-id="e273f-141">否</span><span class="sxs-lookup"><span data-stu-id="e273f-141">False</span></span>                                                                   |
| <span data-ttu-id="e273f-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e273f-142">In Global Catalog</span></span>      | <span data-ttu-id="e273f-143">否</span><span class="sxs-lookup"><span data-stu-id="e273f-143">False</span></span>                                                                   |
| <span data-ttu-id="e273f-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e273f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e273f-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e273f-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e273f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e273f-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e273f-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-148">Search-Flags</span></span>           | <span data-ttu-id="e273f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e273f-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="e273f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-150">System-Flags</span></span>           | <span data-ttu-id="e273f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e273f-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="e273f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e273f-152">Classes used in</span></span>        | [<span data-ttu-id="e273f-153">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e273f-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e273f-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e273f-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e273f-155">進入</span><span class="sxs-lookup"><span data-stu-id="e273f-155">Entry</span></span> | <span data-ttu-id="e273f-156">值</span><span class="sxs-lookup"><span data-stu-id="e273f-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e273f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e273f-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e273f-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e273f-159">System-Only</span></span>            | <span data-ttu-id="e273f-160">否</span><span class="sxs-lookup"><span data-stu-id="e273f-160">False</span></span>                                                                   |
| <span data-ttu-id="e273f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e273f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e273f-162">否</span><span class="sxs-lookup"><span data-stu-id="e273f-162">False</span></span>                                                                   |
| <span data-ttu-id="e273f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e273f-163">Is Indexed</span></span>             | <span data-ttu-id="e273f-164">否</span><span class="sxs-lookup"><span data-stu-id="e273f-164">False</span></span>                                                                   |
| <span data-ttu-id="e273f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e273f-165">In Global Catalog</span></span>      | <span data-ttu-id="e273f-166">否</span><span class="sxs-lookup"><span data-stu-id="e273f-166">False</span></span>                                                                   |
| <span data-ttu-id="e273f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e273f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e273f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e273f-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e273f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e273f-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e273f-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-171">Search-Flags</span></span>           | <span data-ttu-id="e273f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e273f-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="e273f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-173">System-Flags</span></span>           | <span data-ttu-id="e273f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e273f-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="e273f-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e273f-175">Classes used in</span></span>        | [<span data-ttu-id="e273f-176">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e273f-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e273f-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e273f-177">Windows Server 2008</span></span>



| <span data-ttu-id="e273f-178">進入</span><span class="sxs-lookup"><span data-stu-id="e273f-178">Entry</span></span> | <span data-ttu-id="e273f-179">值</span><span class="sxs-lookup"><span data-stu-id="e273f-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e273f-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e273f-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e273f-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e273f-182">System-Only</span></span>            | <span data-ttu-id="e273f-183">否</span><span class="sxs-lookup"><span data-stu-id="e273f-183">False</span></span>                                                                   |
| <span data-ttu-id="e273f-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e273f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e273f-185">否</span><span class="sxs-lookup"><span data-stu-id="e273f-185">False</span></span>                                                                   |
| <span data-ttu-id="e273f-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e273f-186">Is Indexed</span></span>             | <span data-ttu-id="e273f-187">否</span><span class="sxs-lookup"><span data-stu-id="e273f-187">False</span></span>                                                                   |
| <span data-ttu-id="e273f-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e273f-188">In Global Catalog</span></span>      | <span data-ttu-id="e273f-189">否</span><span class="sxs-lookup"><span data-stu-id="e273f-189">False</span></span>                                                                   |
| <span data-ttu-id="e273f-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e273f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e273f-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e273f-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e273f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e273f-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e273f-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-194">Search-Flags</span></span>           | <span data-ttu-id="e273f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e273f-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="e273f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-196">System-Flags</span></span>           | <span data-ttu-id="e273f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e273f-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="e273f-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e273f-198">Classes used in</span></span>        | [<span data-ttu-id="e273f-199">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e273f-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e273f-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e273f-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e273f-201">進入</span><span class="sxs-lookup"><span data-stu-id="e273f-201">Entry</span></span> | <span data-ttu-id="e273f-202">值</span><span class="sxs-lookup"><span data-stu-id="e273f-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e273f-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e273f-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e273f-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e273f-205">System-Only</span></span>            | <span data-ttu-id="e273f-206">否</span><span class="sxs-lookup"><span data-stu-id="e273f-206">False</span></span>                                                                   |
| <span data-ttu-id="e273f-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e273f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e273f-208">否</span><span class="sxs-lookup"><span data-stu-id="e273f-208">False</span></span>                                                                   |
| <span data-ttu-id="e273f-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e273f-209">Is Indexed</span></span>             | <span data-ttu-id="e273f-210">否</span><span class="sxs-lookup"><span data-stu-id="e273f-210">False</span></span>                                                                   |
| <span data-ttu-id="e273f-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e273f-211">In Global Catalog</span></span>      | <span data-ttu-id="e273f-212">否</span><span class="sxs-lookup"><span data-stu-id="e273f-212">False</span></span>                                                                   |
| <span data-ttu-id="e273f-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e273f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e273f-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e273f-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e273f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e273f-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e273f-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-217">Search-Flags</span></span>           | <span data-ttu-id="e273f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e273f-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="e273f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-219">System-Flags</span></span>           | <span data-ttu-id="e273f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e273f-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="e273f-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e273f-221">Classes used in</span></span>        | [<span data-ttu-id="e273f-222">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e273f-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e273f-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e273f-223">Windows Server 2012</span></span>



| <span data-ttu-id="e273f-224">進入</span><span class="sxs-lookup"><span data-stu-id="e273f-224">Entry</span></span> | <span data-ttu-id="e273f-225">值</span><span class="sxs-lookup"><span data-stu-id="e273f-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e273f-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e273f-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e273f-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e273f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e273f-228">System-Only</span></span>            | <span data-ttu-id="e273f-229">否</span><span class="sxs-lookup"><span data-stu-id="e273f-229">False</span></span>                                                                   |
| <span data-ttu-id="e273f-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e273f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e273f-231">否</span><span class="sxs-lookup"><span data-stu-id="e273f-231">False</span></span>                                                                   |
| <span data-ttu-id="e273f-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e273f-232">Is Indexed</span></span>             | <span data-ttu-id="e273f-233">否</span><span class="sxs-lookup"><span data-stu-id="e273f-233">False</span></span>                                                                   |
| <span data-ttu-id="e273f-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e273f-234">In Global Catalog</span></span>      | <span data-ttu-id="e273f-235">否</span><span class="sxs-lookup"><span data-stu-id="e273f-235">False</span></span>                                                                   |
| <span data-ttu-id="e273f-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e273f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e273f-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e273f-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e273f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e273f-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e273f-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e273f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-240">Search-Flags</span></span>           | <span data-ttu-id="e273f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e273f-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="e273f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e273f-242">System-Flags</span></span>           | <span data-ttu-id="e273f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e273f-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="e273f-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e273f-244">Classes used in</span></span>        | [<span data-ttu-id="e273f-245">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e273f-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






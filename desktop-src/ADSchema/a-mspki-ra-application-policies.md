---
title: ms-PKI-RA-應用程式原則屬性
description: 憑證要求的計數器簽章中所需的 RA 應用程式原則 OID。
ms.assetid: 1ce61107-01aa-4a03-8a00-21890fb610d7
ms.tgt_platform: multiple
keywords:
- ms-PKI-RA-應用程式原則屬性 AD 架構
- Mspki-certificate-name-flag-RA-應用程式原則屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-RA-Application-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01aab7c8da5c6267efe954cac71dc8c9c98c18f4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104187334"
---
# <a name="ms-pki-ra-application-policies-attribute"></a><span data-ttu-id="d2f12-105">ms-PKI-RA-應用程式原則屬性</span><span class="sxs-lookup"><span data-stu-id="d2f12-105">ms-PKI-RA-Application-Policies attribute</span></span>

<span data-ttu-id="d2f12-106">憑證要求的計數器簽章中所需的 RA 應用程式原則 OID。</span><span class="sxs-lookup"><span data-stu-id="d2f12-106">The required RA application policy OID in the counter signatures of the certificate request.</span></span>



| <span data-ttu-id="d2f12-107">進入</span><span class="sxs-lookup"><span data-stu-id="d2f12-107">Entry</span></span> | <span data-ttu-id="d2f12-108">值</span><span class="sxs-lookup"><span data-stu-id="d2f12-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f12-109">CN</span><span class="sxs-lookup"><span data-stu-id="d2f12-109">CN</span></span>                | <span data-ttu-id="d2f12-110">ms-PKI-RA-應用程式原則</span><span class="sxs-lookup"><span data-stu-id="d2f12-110">ms-PKI-RA-Application-Policies</span></span>                                                             |
| <span data-ttu-id="d2f12-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d2f12-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d2f12-112">Mspki-certificate-name-flag-RA-應用程式原則</span><span class="sxs-lookup"><span data-stu-id="d2f12-112">msPKI-RA-Application-Policies</span></span>                                                              |
| <span data-ttu-id="d2f12-113">大小</span><span class="sxs-lookup"><span data-stu-id="d2f12-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="d2f12-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d2f12-114">Update Privilege</span></span>  | <span data-ttu-id="d2f12-115">企業系統管理員</span><span class="sxs-lookup"><span data-stu-id="d2f12-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="d2f12-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d2f12-116">Update Frequency</span></span>  | <span data-ttu-id="d2f12-117">每次建立新範本，或編輯現有範本的屬性時。</span><span class="sxs-lookup"><span data-stu-id="d2f12-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="d2f12-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2f12-118">Attribute-Id</span></span>      | <span data-ttu-id="d2f12-119">1.2.840.113556.1.4.1675</span><span class="sxs-lookup"><span data-stu-id="d2f12-119">1.2.840.113556.1.4.1675</span></span>                                                                    |
| <span data-ttu-id="d2f12-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d2f12-120">System-Id-Guid</span></span>    | <span data-ttu-id="d2f12-121">3c91fbbf-4773-4ccd-a87b-85d53e7bcf6a</span><span class="sxs-lookup"><span data-stu-id="d2f12-121">3c91fbbf-4773-4ccd-a87b-85d53e7bcf6a</span></span>                                                       |
| <span data-ttu-id="d2f12-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2f12-122">Syntax</span></span>            | [<span data-ttu-id="d2f12-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d2f12-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="d2f12-124">實作</span><span class="sxs-lookup"><span data-stu-id="d2f12-124">Implementations</span></span>

-   [<span data-ttu-id="d2f12-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2f12-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2f12-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2f12-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2f12-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2f12-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2f12-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2f12-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2f12-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2f12-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d2f12-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2f12-130">Windows Server 2003</span></span>



| <span data-ttu-id="d2f12-131">進入</span><span class="sxs-lookup"><span data-stu-id="d2f12-131">Entry</span></span> | <span data-ttu-id="d2f12-132">值</span><span class="sxs-lookup"><span data-stu-id="d2f12-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d2f12-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2f12-133">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f12-134">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f12-135">System-Only</span></span>            | <span data-ttu-id="d2f12-136">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-136">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2f12-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f12-138">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-138">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2f12-139">Is Indexed</span></span>             | <span data-ttu-id="d2f12-140">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-140">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2f12-141">In Global Catalog</span></span>      | <span data-ttu-id="d2f12-142">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-142">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2f12-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f12-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2f12-144">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d2f12-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f12-145">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f12-146">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-147">Search-Flags</span></span>           | <span data-ttu-id="d2f12-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f12-148">0x00000000</span></span>                                                              |
| <span data-ttu-id="d2f12-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-149">System-Flags</span></span>           | <span data-ttu-id="d2f12-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f12-150">0x00000010</span></span>                                                              |
| <span data-ttu-id="d2f12-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2f12-151">Classes used in</span></span>        | [<span data-ttu-id="d2f12-152">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="d2f12-152">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2f12-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2f12-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2f12-154">進入</span><span class="sxs-lookup"><span data-stu-id="d2f12-154">Entry</span></span> | <span data-ttu-id="d2f12-155">值</span><span class="sxs-lookup"><span data-stu-id="d2f12-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d2f12-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2f12-156">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f12-157">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f12-158">System-Only</span></span>            | <span data-ttu-id="d2f12-159">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-159">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2f12-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f12-161">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-161">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2f12-162">Is Indexed</span></span>             | <span data-ttu-id="d2f12-163">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-163">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2f12-164">In Global Catalog</span></span>      | <span data-ttu-id="d2f12-165">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-165">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2f12-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f12-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2f12-167">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d2f12-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f12-168">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f12-169">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-170">Search-Flags</span></span>           | <span data-ttu-id="d2f12-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f12-171">0x00000000</span></span>                                                              |
| <span data-ttu-id="d2f12-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-172">System-Flags</span></span>           | <span data-ttu-id="d2f12-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f12-173">0x00000010</span></span>                                                              |
| <span data-ttu-id="d2f12-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2f12-174">Classes used in</span></span>        | [<span data-ttu-id="d2f12-175">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="d2f12-175">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2f12-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2f12-176">Windows Server 2008</span></span>



| <span data-ttu-id="d2f12-177">進入</span><span class="sxs-lookup"><span data-stu-id="d2f12-177">Entry</span></span> | <span data-ttu-id="d2f12-178">值</span><span class="sxs-lookup"><span data-stu-id="d2f12-178">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d2f12-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2f12-179">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f12-180">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f12-181">System-Only</span></span>            | <span data-ttu-id="d2f12-182">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-182">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2f12-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f12-184">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-184">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2f12-185">Is Indexed</span></span>             | <span data-ttu-id="d2f12-186">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-186">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2f12-187">In Global Catalog</span></span>      | <span data-ttu-id="d2f12-188">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-188">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2f12-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f12-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2f12-190">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d2f12-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f12-191">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f12-192">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-193">Search-Flags</span></span>           | <span data-ttu-id="d2f12-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f12-194">0x00000000</span></span>                                                              |
| <span data-ttu-id="d2f12-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-195">System-Flags</span></span>           | <span data-ttu-id="d2f12-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f12-196">0x00000010</span></span>                                                              |
| <span data-ttu-id="d2f12-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2f12-197">Classes used in</span></span>        | [<span data-ttu-id="d2f12-198">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="d2f12-198">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2f12-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2f12-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2f12-200">進入</span><span class="sxs-lookup"><span data-stu-id="d2f12-200">Entry</span></span> | <span data-ttu-id="d2f12-201">值</span><span class="sxs-lookup"><span data-stu-id="d2f12-201">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d2f12-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2f12-202">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f12-203">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f12-204">System-Only</span></span>            | <span data-ttu-id="d2f12-205">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-205">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2f12-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f12-207">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-207">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2f12-208">Is Indexed</span></span>             | <span data-ttu-id="d2f12-209">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-209">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2f12-210">In Global Catalog</span></span>      | <span data-ttu-id="d2f12-211">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-211">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2f12-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f12-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2f12-213">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d2f12-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f12-214">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f12-215">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-216">Search-Flags</span></span>           | <span data-ttu-id="d2f12-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f12-217">0x00000000</span></span>                                                              |
| <span data-ttu-id="d2f12-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-218">System-Flags</span></span>           | <span data-ttu-id="d2f12-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f12-219">0x00000010</span></span>                                                              |
| <span data-ttu-id="d2f12-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2f12-220">Classes used in</span></span>        | [<span data-ttu-id="d2f12-221">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="d2f12-221">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2f12-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2f12-222">Windows Server 2012</span></span>



| <span data-ttu-id="d2f12-223">進入</span><span class="sxs-lookup"><span data-stu-id="d2f12-223">Entry</span></span> | <span data-ttu-id="d2f12-224">值</span><span class="sxs-lookup"><span data-stu-id="d2f12-224">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d2f12-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d2f12-225">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f12-226">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="d2f12-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f12-227">System-Only</span></span>            | <span data-ttu-id="d2f12-228">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-228">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d2f12-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f12-230">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-230">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d2f12-231">Is Indexed</span></span>             | <span data-ttu-id="d2f12-232">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-232">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d2f12-233">In Global Catalog</span></span>      | <span data-ttu-id="d2f12-234">否</span><span class="sxs-lookup"><span data-stu-id="d2f12-234">False</span></span>                                                                   |
| <span data-ttu-id="d2f12-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d2f12-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f12-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d2f12-236">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="d2f12-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f12-237">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f12-238">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="d2f12-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-239">Search-Flags</span></span>           | <span data-ttu-id="d2f12-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f12-240">0x00000000</span></span>                                                              |
| <span data-ttu-id="d2f12-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f12-241">System-Flags</span></span>           | <span data-ttu-id="d2f12-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f12-242">0x00000010</span></span>                                                              |
| <span data-ttu-id="d2f12-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d2f12-243">Classes used in</span></span>        | [<span data-ttu-id="d2f12-244">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="d2f12-244">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






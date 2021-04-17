---
title: ms-PKI-憑證-應用程式原則屬性
description: 憑證中的應用程式原則 OID。
ms.assetid: 91e98ec9-0e8d-4950-a62c-9b6901ec4d97
ms.tgt_platform: multiple
keywords:
- ms-PKI-憑證-應用程式-原則屬性 AD 架構
- Mspki-certificate-name-flag-憑證-應用程式-原則屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Application-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9436415fb9361454fc5f872802516fa455ff980b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385386"
---
# <a name="ms-pki-certificate-application-policy-attribute"></a><span data-ttu-id="a0dd6-105">ms-PKI-憑證-應用程式原則屬性</span><span class="sxs-lookup"><span data-stu-id="a0dd6-105">ms-PKI-Certificate-Application-Policy attribute</span></span>

<span data-ttu-id="a0dd6-106">憑證中的應用程式原則 OID。</span><span class="sxs-lookup"><span data-stu-id="a0dd6-106">The application policy OID's in a certificate.</span></span>



| <span data-ttu-id="a0dd6-107">進入</span><span class="sxs-lookup"><span data-stu-id="a0dd6-107">Entry</span></span> | <span data-ttu-id="a0dd6-108">值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0dd6-109">CN</span><span class="sxs-lookup"><span data-stu-id="a0dd6-109">CN</span></span>                | <span data-ttu-id="a0dd6-110">ms-PKI-憑證-應用程式-原則</span><span class="sxs-lookup"><span data-stu-id="a0dd6-110">ms-PKI-Certificate-Application-Policy</span></span>                                                      |
| <span data-ttu-id="a0dd6-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a0dd6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a0dd6-112">Mspki-certificate-name-flag-憑證-應用程式-原則</span><span class="sxs-lookup"><span data-stu-id="a0dd6-112">msPKI-Certificate-Application-Policy</span></span>                                                       |
| <span data-ttu-id="a0dd6-113">大小</span><span class="sxs-lookup"><span data-stu-id="a0dd6-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="a0dd6-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a0dd6-114">Update Privilege</span></span>  | <span data-ttu-id="a0dd6-115">企業系統管理員</span><span class="sxs-lookup"><span data-stu-id="a0dd6-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="a0dd6-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a0dd6-116">Update Frequency</span></span>  | <span data-ttu-id="a0dd6-117">每次建立新範本，或編輯現有範本的屬性時。</span><span class="sxs-lookup"><span data-stu-id="a0dd6-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="a0dd6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a0dd6-118">Attribute-Id</span></span>      | <span data-ttu-id="a0dd6-119">1.2.840.113556.1.4.1674</span><span class="sxs-lookup"><span data-stu-id="a0dd6-119">1.2.840.113556.1.4.1674</span></span>                                                                    |
| <span data-ttu-id="a0dd6-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a0dd6-120">System-Id-Guid</span></span>    | <span data-ttu-id="a0dd6-121">dbd90548-aa37-4202-9966-8c537ba5ce32</span><span class="sxs-lookup"><span data-stu-id="a0dd6-121">dbd90548-aa37-4202-9966-8c537ba5ce32</span></span>                                                       |
| <span data-ttu-id="a0dd6-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0dd6-122">Syntax</span></span>            | [<span data-ttu-id="a0dd6-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="a0dd6-124">實作</span><span class="sxs-lookup"><span data-stu-id="a0dd6-124">Implementations</span></span>

-   [<span data-ttu-id="a0dd6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a0dd6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a0dd6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a0dd6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a0dd6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a0dd6-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0dd6-130">Windows Server 2003</span></span>



| <span data-ttu-id="a0dd6-131">進入</span><span class="sxs-lookup"><span data-stu-id="a0dd6-131">Entry</span></span> | <span data-ttu-id="a0dd6-132">值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a0dd6-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0dd6-133">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0dd6-134">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0dd6-135">System-Only</span></span>            | <span data-ttu-id="a0dd6-136">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-136">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a0dd6-138">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-138">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0dd6-139">Is Indexed</span></span>             | <span data-ttu-id="a0dd6-140">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-140">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0dd6-141">In Global Catalog</span></span>      | <span data-ttu-id="a0dd6-142">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-142">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0dd6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0dd6-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0dd6-144">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a0dd6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0dd6-145">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0dd6-146">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-147">Search-Flags</span></span>           | <span data-ttu-id="a0dd6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0dd6-148">0x00000000</span></span>                                                              |
| <span data-ttu-id="a0dd6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-149">System-Flags</span></span>           | <span data-ttu-id="a0dd6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0dd6-150">0x00000010</span></span>                                                              |
| <span data-ttu-id="a0dd6-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0dd6-151">Classes used in</span></span>        | [<span data-ttu-id="a0dd6-152">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-152">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a0dd6-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a0dd6-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a0dd6-154">進入</span><span class="sxs-lookup"><span data-stu-id="a0dd6-154">Entry</span></span> | <span data-ttu-id="a0dd6-155">值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a0dd6-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0dd6-156">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0dd6-157">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0dd6-158">System-Only</span></span>            | <span data-ttu-id="a0dd6-159">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-159">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a0dd6-161">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-161">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0dd6-162">Is Indexed</span></span>             | <span data-ttu-id="a0dd6-163">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-163">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0dd6-164">In Global Catalog</span></span>      | <span data-ttu-id="a0dd6-165">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-165">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0dd6-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0dd6-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0dd6-167">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a0dd6-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0dd6-168">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0dd6-169">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-170">Search-Flags</span></span>           | <span data-ttu-id="a0dd6-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0dd6-171">0x00000000</span></span>                                                              |
| <span data-ttu-id="a0dd6-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-172">System-Flags</span></span>           | <span data-ttu-id="a0dd6-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0dd6-173">0x00000010</span></span>                                                              |
| <span data-ttu-id="a0dd6-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0dd6-174">Classes used in</span></span>        | [<span data-ttu-id="a0dd6-175">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-175">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a0dd6-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0dd6-176">Windows Server 2008</span></span>



| <span data-ttu-id="a0dd6-177">進入</span><span class="sxs-lookup"><span data-stu-id="a0dd6-177">Entry</span></span> | <span data-ttu-id="a0dd6-178">值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-178">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a0dd6-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0dd6-179">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0dd6-180">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0dd6-181">System-Only</span></span>            | <span data-ttu-id="a0dd6-182">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-182">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a0dd6-184">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-184">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0dd6-185">Is Indexed</span></span>             | <span data-ttu-id="a0dd6-186">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-186">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0dd6-187">In Global Catalog</span></span>      | <span data-ttu-id="a0dd6-188">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-188">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0dd6-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0dd6-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0dd6-190">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a0dd6-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0dd6-191">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0dd6-192">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-193">Search-Flags</span></span>           | <span data-ttu-id="a0dd6-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0dd6-194">0x00000000</span></span>                                                              |
| <span data-ttu-id="a0dd6-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-195">System-Flags</span></span>           | <span data-ttu-id="a0dd6-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0dd6-196">0x00000010</span></span>                                                              |
| <span data-ttu-id="a0dd6-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0dd6-197">Classes used in</span></span>        | [<span data-ttu-id="a0dd6-198">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-198">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a0dd6-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a0dd6-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a0dd6-200">進入</span><span class="sxs-lookup"><span data-stu-id="a0dd6-200">Entry</span></span> | <span data-ttu-id="a0dd6-201">值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-201">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a0dd6-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0dd6-202">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0dd6-203">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0dd6-204">System-Only</span></span>            | <span data-ttu-id="a0dd6-205">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-205">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a0dd6-207">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-207">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0dd6-208">Is Indexed</span></span>             | <span data-ttu-id="a0dd6-209">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-209">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0dd6-210">In Global Catalog</span></span>      | <span data-ttu-id="a0dd6-211">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-211">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0dd6-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0dd6-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0dd6-213">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a0dd6-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0dd6-214">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0dd6-215">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-216">Search-Flags</span></span>           | <span data-ttu-id="a0dd6-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0dd6-217">0x00000000</span></span>                                                              |
| <span data-ttu-id="a0dd6-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-218">System-Flags</span></span>           | <span data-ttu-id="a0dd6-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0dd6-219">0x00000010</span></span>                                                              |
| <span data-ttu-id="a0dd6-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0dd6-220">Classes used in</span></span>        | [<span data-ttu-id="a0dd6-221">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-221">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a0dd6-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0dd6-222">Windows Server 2012</span></span>



| <span data-ttu-id="a0dd6-223">進入</span><span class="sxs-lookup"><span data-stu-id="a0dd6-223">Entry</span></span> | <span data-ttu-id="a0dd6-224">值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-224">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a0dd6-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0dd6-225">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0dd6-226">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a0dd6-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0dd6-227">System-Only</span></span>            | <span data-ttu-id="a0dd6-228">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-228">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0dd6-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a0dd6-230">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-230">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0dd6-231">Is Indexed</span></span>             | <span data-ttu-id="a0dd6-232">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-232">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0dd6-233">In Global Catalog</span></span>      | <span data-ttu-id="a0dd6-234">否</span><span class="sxs-lookup"><span data-stu-id="a0dd6-234">False</span></span>                                                                   |
| <span data-ttu-id="a0dd6-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0dd6-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0dd6-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0dd6-236">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a0dd6-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0dd6-237">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0dd6-238">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a0dd6-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-239">Search-Flags</span></span>           | <span data-ttu-id="a0dd6-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0dd6-240">0x00000000</span></span>                                                              |
| <span data-ttu-id="a0dd6-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0dd6-241">System-Flags</span></span>           | <span data-ttu-id="a0dd6-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0dd6-242">0x00000010</span></span>                                                              |
| <span data-ttu-id="a0dd6-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0dd6-243">Classes used in</span></span>        | [<span data-ttu-id="a0dd6-244">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="a0dd6-244">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






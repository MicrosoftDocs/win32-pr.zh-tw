---
title: ms-PKI-憑證-原則屬性
description: 包含在已發行的憑證中的原則 Oid 和其選擇性 Csp 的清單。
ms.assetid: bc84c5ff-9cb1-406c-825c-97fa479d52eb
ms.tgt_platform: multiple
keywords:
- ms-PKI-憑證-原則屬性 AD 架構
- Mspki-certificate-name-flag-憑證-原則屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2d6857b6035cc72271c7276b679b8a497aaab9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845067"
---
# <a name="ms-pki-certificate-policy-attribute"></a><span data-ttu-id="db136-105">ms-PKI-憑證-原則屬性</span><span class="sxs-lookup"><span data-stu-id="db136-105">ms-PKI-Certificate-Policy attribute</span></span>

<span data-ttu-id="db136-106">包含在已發行的憑證中的原則 Oid 和其選擇性 Csp 的清單。</span><span class="sxs-lookup"><span data-stu-id="db136-106">Contains the list of policy OIDs and their optional CSPs in the issued certificate.</span></span>



| <span data-ttu-id="db136-107">進入</span><span class="sxs-lookup"><span data-stu-id="db136-107">Entry</span></span> | <span data-ttu-id="db136-108">值</span><span class="sxs-lookup"><span data-stu-id="db136-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db136-109">CN</span><span class="sxs-lookup"><span data-stu-id="db136-109">CN</span></span>                | <span data-ttu-id="db136-110">ms-PKI-憑證-原則</span><span class="sxs-lookup"><span data-stu-id="db136-110">ms-PKI-Certificate-Policy</span></span>                                                                         |
| <span data-ttu-id="db136-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="db136-111">Ldap-Display-Name</span></span> | <span data-ttu-id="db136-112">Mspki-certificate-name-flag-憑證-原則</span><span class="sxs-lookup"><span data-stu-id="db136-112">msPKI-Certificate-Policy</span></span>                                                                          |
| <span data-ttu-id="db136-113">大小</span><span class="sxs-lookup"><span data-stu-id="db136-113">Size</span></span>              | <span data-ttu-id="db136-114">專案數目的64位元組倍。</span><span class="sxs-lookup"><span data-stu-id="db136-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="db136-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="db136-115">Update Privilege</span></span>  | <span data-ttu-id="db136-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="db136-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="db136-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="db136-117">Update Frequency</span></span>  | <span data-ttu-id="db136-118">當您編輯、建立或複製憑證範本時 (ms-PKI-憑證範本) 物件。</span><span class="sxs-lookup"><span data-stu-id="db136-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="db136-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="db136-119">Attribute-Id</span></span>      | <span data-ttu-id="db136-120">1.2.840.113556.1.4.1439</span><span class="sxs-lookup"><span data-stu-id="db136-120">1.2.840.113556.1.4.1439</span></span>                                                                           |
| <span data-ttu-id="db136-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="db136-121">System-Id-Guid</span></span>    | <span data-ttu-id="db136-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span><span class="sxs-lookup"><span data-stu-id="db136-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span></span>                                                              |
| <span data-ttu-id="db136-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="db136-123">Syntax</span></span>            | [<span data-ttu-id="db136-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="db136-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="db136-125">實作</span><span class="sxs-lookup"><span data-stu-id="db136-125">Implementations</span></span>

-   [<span data-ttu-id="db136-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="db136-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="db136-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="db136-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="db136-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="db136-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="db136-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="db136-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="db136-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="db136-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="db136-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db136-131">Windows Server 2003</span></span>



| <span data-ttu-id="db136-132">進入</span><span class="sxs-lookup"><span data-stu-id="db136-132">Entry</span></span> | <span data-ttu-id="db136-133">值</span><span class="sxs-lookup"><span data-stu-id="db136-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="db136-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-136">System-Only</span></span>            | <span data-ttu-id="db136-137">否</span><span class="sxs-lookup"><span data-stu-id="db136-137">False</span></span>                                                                   |
| <span data-ttu-id="db136-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-138">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-139">否</span><span class="sxs-lookup"><span data-stu-id="db136-139">False</span></span>                                                                   |
| <span data-ttu-id="db136-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-140">Is Indexed</span></span>             | <span data-ttu-id="db136-141">否</span><span class="sxs-lookup"><span data-stu-id="db136-141">False</span></span>                                                                   |
| <span data-ttu-id="db136-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-142">In Global Catalog</span></span>      | <span data-ttu-id="db136-143">否</span><span class="sxs-lookup"><span data-stu-id="db136-143">False</span></span>                                                                   |
| <span data-ttu-id="db136-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="db136-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-148">Search-Flags</span></span>           | <span data-ttu-id="db136-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="db136-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-150">System-Flags</span></span>           | <span data-ttu-id="db136-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="db136-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-152">Classes used in</span></span>        | [<span data-ttu-id="db136-153">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="db136-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="db136-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="db136-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="db136-155">進入</span><span class="sxs-lookup"><span data-stu-id="db136-155">Entry</span></span> | <span data-ttu-id="db136-156">值</span><span class="sxs-lookup"><span data-stu-id="db136-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="db136-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-159">System-Only</span></span>            | <span data-ttu-id="db136-160">否</span><span class="sxs-lookup"><span data-stu-id="db136-160">False</span></span>                                                                   |
| <span data-ttu-id="db136-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-161">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-162">否</span><span class="sxs-lookup"><span data-stu-id="db136-162">False</span></span>                                                                   |
| <span data-ttu-id="db136-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-163">Is Indexed</span></span>             | <span data-ttu-id="db136-164">否</span><span class="sxs-lookup"><span data-stu-id="db136-164">False</span></span>                                                                   |
| <span data-ttu-id="db136-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-165">In Global Catalog</span></span>      | <span data-ttu-id="db136-166">否</span><span class="sxs-lookup"><span data-stu-id="db136-166">False</span></span>                                                                   |
| <span data-ttu-id="db136-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="db136-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-171">Search-Flags</span></span>           | <span data-ttu-id="db136-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="db136-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-173">System-Flags</span></span>           | <span data-ttu-id="db136-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="db136-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-175">Classes used in</span></span>        | [<span data-ttu-id="db136-176">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="db136-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="db136-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db136-177">Windows Server 2008</span></span>



| <span data-ttu-id="db136-178">進入</span><span class="sxs-lookup"><span data-stu-id="db136-178">Entry</span></span> | <span data-ttu-id="db136-179">值</span><span class="sxs-lookup"><span data-stu-id="db136-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="db136-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-182">System-Only</span></span>            | <span data-ttu-id="db136-183">否</span><span class="sxs-lookup"><span data-stu-id="db136-183">False</span></span>                                                                   |
| <span data-ttu-id="db136-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-184">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-185">否</span><span class="sxs-lookup"><span data-stu-id="db136-185">False</span></span>                                                                   |
| <span data-ttu-id="db136-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-186">Is Indexed</span></span>             | <span data-ttu-id="db136-187">否</span><span class="sxs-lookup"><span data-stu-id="db136-187">False</span></span>                                                                   |
| <span data-ttu-id="db136-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-188">In Global Catalog</span></span>      | <span data-ttu-id="db136-189">否</span><span class="sxs-lookup"><span data-stu-id="db136-189">False</span></span>                                                                   |
| <span data-ttu-id="db136-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="db136-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-194">Search-Flags</span></span>           | <span data-ttu-id="db136-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="db136-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-196">System-Flags</span></span>           | <span data-ttu-id="db136-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="db136-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-198">Classes used in</span></span>        | [<span data-ttu-id="db136-199">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="db136-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="db136-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db136-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="db136-201">進入</span><span class="sxs-lookup"><span data-stu-id="db136-201">Entry</span></span> | <span data-ttu-id="db136-202">值</span><span class="sxs-lookup"><span data-stu-id="db136-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="db136-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-205">System-Only</span></span>            | <span data-ttu-id="db136-206">否</span><span class="sxs-lookup"><span data-stu-id="db136-206">False</span></span>                                                                   |
| <span data-ttu-id="db136-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-207">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-208">否</span><span class="sxs-lookup"><span data-stu-id="db136-208">False</span></span>                                                                   |
| <span data-ttu-id="db136-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-209">Is Indexed</span></span>             | <span data-ttu-id="db136-210">否</span><span class="sxs-lookup"><span data-stu-id="db136-210">False</span></span>                                                                   |
| <span data-ttu-id="db136-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-211">In Global Catalog</span></span>      | <span data-ttu-id="db136-212">否</span><span class="sxs-lookup"><span data-stu-id="db136-212">False</span></span>                                                                   |
| <span data-ttu-id="db136-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="db136-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-217">Search-Flags</span></span>           | <span data-ttu-id="db136-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="db136-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-219">System-Flags</span></span>           | <span data-ttu-id="db136-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="db136-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-221">Classes used in</span></span>        | [<span data-ttu-id="db136-222">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="db136-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="db136-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db136-223">Windows Server 2012</span></span>



| <span data-ttu-id="db136-224">進入</span><span class="sxs-lookup"><span data-stu-id="db136-224">Entry</span></span> | <span data-ttu-id="db136-225">值</span><span class="sxs-lookup"><span data-stu-id="db136-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="db136-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="db136-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-228">System-Only</span></span>            | <span data-ttu-id="db136-229">否</span><span class="sxs-lookup"><span data-stu-id="db136-229">False</span></span>                                                                   |
| <span data-ttu-id="db136-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-230">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-231">否</span><span class="sxs-lookup"><span data-stu-id="db136-231">False</span></span>                                                                   |
| <span data-ttu-id="db136-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-232">Is Indexed</span></span>             | <span data-ttu-id="db136-233">否</span><span class="sxs-lookup"><span data-stu-id="db136-233">False</span></span>                                                                   |
| <span data-ttu-id="db136-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-234">In Global Catalog</span></span>      | <span data-ttu-id="db136-235">否</span><span class="sxs-lookup"><span data-stu-id="db136-235">False</span></span>                                                                   |
| <span data-ttu-id="db136-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="db136-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="db136-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-240">Search-Flags</span></span>           | <span data-ttu-id="db136-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="db136-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-242">System-Flags</span></span>           | <span data-ttu-id="db136-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="db136-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-244">Classes used in</span></span>        | [<span data-ttu-id="db136-245">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="db136-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






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
# <a name="ms-pki-certificate-policy-attribute"></a><span data-ttu-id="6f5e5-105">ms-PKI-憑證-原則屬性</span><span class="sxs-lookup"><span data-stu-id="6f5e5-105">ms-PKI-Certificate-Policy attribute</span></span>

<span data-ttu-id="6f5e5-106">包含在已發行的憑證中的原則 Oid 和其選擇性 Csp 的清單。</span><span class="sxs-lookup"><span data-stu-id="6f5e5-106">Contains the list of policy OIDs and their optional CSPs in the issued certificate.</span></span>



| <span data-ttu-id="6f5e5-107">進入</span><span class="sxs-lookup"><span data-stu-id="6f5e5-107">Entry</span></span> | <span data-ttu-id="6f5e5-108">值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5e5-109">CN</span><span class="sxs-lookup"><span data-stu-id="6f5e5-109">CN</span></span>                | <span data-ttu-id="6f5e5-110">ms-PKI-憑證-原則</span><span class="sxs-lookup"><span data-stu-id="6f5e5-110">ms-PKI-Certificate-Policy</span></span>                                                                         |
| <span data-ttu-id="6f5e5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6f5e5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6f5e5-112">Mspki-certificate-name-flag-憑證-原則</span><span class="sxs-lookup"><span data-stu-id="6f5e5-112">msPKI-Certificate-Policy</span></span>                                                                          |
| <span data-ttu-id="6f5e5-113">大小</span><span class="sxs-lookup"><span data-stu-id="6f5e5-113">Size</span></span>              | <span data-ttu-id="6f5e5-114">專案數目的64位元組倍。</span><span class="sxs-lookup"><span data-stu-id="6f5e5-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="6f5e5-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6f5e5-115">Update Privilege</span></span>  | <span data-ttu-id="6f5e5-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="6f5e5-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="6f5e5-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6f5e5-117">Update Frequency</span></span>  | <span data-ttu-id="6f5e5-118">當您編輯、建立或複製憑證範本時 (ms-PKI-憑證範本) 物件。</span><span class="sxs-lookup"><span data-stu-id="6f5e5-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="6f5e5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6f5e5-119">Attribute-Id</span></span>      | <span data-ttu-id="6f5e5-120">1.2.840.113556.1.4.1439</span><span class="sxs-lookup"><span data-stu-id="6f5e5-120">1.2.840.113556.1.4.1439</span></span>                                                                           |
| <span data-ttu-id="6f5e5-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6f5e5-121">System-Id-Guid</span></span>    | <span data-ttu-id="6f5e5-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span><span class="sxs-lookup"><span data-stu-id="6f5e5-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span></span>                                                              |
| <span data-ttu-id="6f5e5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f5e5-123">Syntax</span></span>            | [<span data-ttu-id="6f5e5-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="6f5e5-125">實作</span><span class="sxs-lookup"><span data-stu-id="6f5e5-125">Implementations</span></span>

-   [<span data-ttu-id="6f5e5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6f5e5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6f5e5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6f5e5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6f5e5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6f5e5-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f5e5-131">Windows Server 2003</span></span>



| <span data-ttu-id="6f5e5-132">進入</span><span class="sxs-lookup"><span data-stu-id="6f5e5-132">Entry</span></span> | <span data-ttu-id="6f5e5-133">值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6f5e5-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f5e5-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f5e5-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f5e5-136">System-Only</span></span>            | <span data-ttu-id="6f5e5-137">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-137">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6f5e5-139">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-139">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f5e5-140">Is Indexed</span></span>             | <span data-ttu-id="6f5e5-141">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-141">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f5e5-142">In Global Catalog</span></span>      | <span data-ttu-id="6f5e5-143">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-143">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f5e5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f5e5-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f5e5-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6f5e5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f5e5-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f5e5-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-148">Search-Flags</span></span>           | <span data-ttu-id="6f5e5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f5e5-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="6f5e5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-150">System-Flags</span></span>           | <span data-ttu-id="6f5e5-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f5e5-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="6f5e5-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f5e5-152">Classes used in</span></span>        | [<span data-ttu-id="6f5e5-153">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6f5e5-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f5e5-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6f5e5-155">進入</span><span class="sxs-lookup"><span data-stu-id="6f5e5-155">Entry</span></span> | <span data-ttu-id="6f5e5-156">值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6f5e5-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f5e5-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f5e5-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f5e5-159">System-Only</span></span>            | <span data-ttu-id="6f5e5-160">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-160">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6f5e5-162">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-162">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f5e5-163">Is Indexed</span></span>             | <span data-ttu-id="6f5e5-164">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-164">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f5e5-165">In Global Catalog</span></span>      | <span data-ttu-id="6f5e5-166">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-166">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f5e5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f5e5-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f5e5-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6f5e5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f5e5-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f5e5-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-171">Search-Flags</span></span>           | <span data-ttu-id="6f5e5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f5e5-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="6f5e5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-173">System-Flags</span></span>           | <span data-ttu-id="6f5e5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f5e5-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="6f5e5-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f5e5-175">Classes used in</span></span>        | [<span data-ttu-id="6f5e5-176">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6f5e5-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f5e5-177">Windows Server 2008</span></span>



| <span data-ttu-id="6f5e5-178">進入</span><span class="sxs-lookup"><span data-stu-id="6f5e5-178">Entry</span></span> | <span data-ttu-id="6f5e5-179">值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6f5e5-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f5e5-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f5e5-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f5e5-182">System-Only</span></span>            | <span data-ttu-id="6f5e5-183">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-183">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6f5e5-185">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-185">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f5e5-186">Is Indexed</span></span>             | <span data-ttu-id="6f5e5-187">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-187">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f5e5-188">In Global Catalog</span></span>      | <span data-ttu-id="6f5e5-189">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-189">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f5e5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f5e5-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f5e5-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6f5e5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f5e5-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f5e5-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-194">Search-Flags</span></span>           | <span data-ttu-id="6f5e5-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f5e5-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="6f5e5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-196">System-Flags</span></span>           | <span data-ttu-id="6f5e5-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f5e5-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="6f5e5-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f5e5-198">Classes used in</span></span>        | [<span data-ttu-id="6f5e5-199">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6f5e5-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f5e5-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6f5e5-201">進入</span><span class="sxs-lookup"><span data-stu-id="6f5e5-201">Entry</span></span> | <span data-ttu-id="6f5e5-202">值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6f5e5-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f5e5-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f5e5-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f5e5-205">System-Only</span></span>            | <span data-ttu-id="6f5e5-206">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-206">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6f5e5-208">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-208">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f5e5-209">Is Indexed</span></span>             | <span data-ttu-id="6f5e5-210">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-210">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f5e5-211">In Global Catalog</span></span>      | <span data-ttu-id="6f5e5-212">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-212">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f5e5-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f5e5-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f5e5-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6f5e5-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f5e5-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f5e5-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-217">Search-Flags</span></span>           | <span data-ttu-id="6f5e5-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f5e5-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="6f5e5-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-219">System-Flags</span></span>           | <span data-ttu-id="6f5e5-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f5e5-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="6f5e5-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f5e5-221">Classes used in</span></span>        | [<span data-ttu-id="6f5e5-222">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6f5e5-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f5e5-223">Windows Server 2012</span></span>



| <span data-ttu-id="6f5e5-224">進入</span><span class="sxs-lookup"><span data-stu-id="6f5e5-224">Entry</span></span> | <span data-ttu-id="6f5e5-225">值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6f5e5-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f5e5-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f5e5-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6f5e5-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f5e5-228">System-Only</span></span>            | <span data-ttu-id="6f5e5-229">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-229">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f5e5-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6f5e5-231">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-231">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f5e5-232">Is Indexed</span></span>             | <span data-ttu-id="6f5e5-233">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-233">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f5e5-234">In Global Catalog</span></span>      | <span data-ttu-id="6f5e5-235">否</span><span class="sxs-lookup"><span data-stu-id="6f5e5-235">False</span></span>                                                                   |
| <span data-ttu-id="6f5e5-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f5e5-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f5e5-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f5e5-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6f5e5-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f5e5-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f5e5-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6f5e5-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-240">Search-Flags</span></span>           | <span data-ttu-id="6f5e5-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f5e5-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="6f5e5-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f5e5-242">System-Flags</span></span>           | <span data-ttu-id="6f5e5-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f5e5-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="6f5e5-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f5e5-244">Classes used in</span></span>        | [<span data-ttu-id="6f5e5-245">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="6f5e5-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






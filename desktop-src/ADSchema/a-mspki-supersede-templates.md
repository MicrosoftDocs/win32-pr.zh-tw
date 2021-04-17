---
title: ms-PKI-取代範本屬性
description: 指定目前範本所取代的憑證範本名稱。
ms.assetid: 4e247932-1c50-4bfb-b723-52b7c36a8571
ms.tgt_platform: multiple
keywords:
- ms-PKI-取代-範本屬性 AD 架構
- Mspki-certificate-name-flag-取代-範本屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-Supersede-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd11ac2b96846912b0c6b1e8d01c6fd558f5f6db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509602"
---
# <a name="ms-pki-supersede-templates-attribute"></a><span data-ttu-id="015a5-105">ms-PKI-取代範本屬性</span><span class="sxs-lookup"><span data-stu-id="015a5-105">ms-PKI-Supersede-Templates attribute</span></span>

<span data-ttu-id="015a5-106">指定目前範本所取代的憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="015a5-106">Specifies the names of the certificate templates that are superseded by the current template.</span></span>



| <span data-ttu-id="015a5-107">進入</span><span class="sxs-lookup"><span data-stu-id="015a5-107">Entry</span></span> | <span data-ttu-id="015a5-108">值</span><span class="sxs-lookup"><span data-stu-id="015a5-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="015a5-109">CN</span><span class="sxs-lookup"><span data-stu-id="015a5-109">CN</span></span>                | <span data-ttu-id="015a5-110">ms-PKI-取代-範本</span><span class="sxs-lookup"><span data-stu-id="015a5-110">ms-PKI-Supersede-Templates</span></span>                                                                        |
| <span data-ttu-id="015a5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="015a5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="015a5-112">Mspki-certificate-name-flag-取代-範本</span><span class="sxs-lookup"><span data-stu-id="015a5-112">msPKI-Supersede-Templates</span></span>                                                                         |
| <span data-ttu-id="015a5-113">大小</span><span class="sxs-lookup"><span data-stu-id="015a5-113">Size</span></span>              | <span data-ttu-id="015a5-114">64位元組</span><span class="sxs-lookup"><span data-stu-id="015a5-114">64 bytes</span></span>                                                                                          |
| <span data-ttu-id="015a5-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="015a5-115">Update Privilege</span></span>  | <span data-ttu-id="015a5-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="015a5-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="015a5-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="015a5-117">Update Frequency</span></span>  | <span data-ttu-id="015a5-118">當您編輯、建立或複製憑證範本時 (ms-PKI-憑證範本) 物件。</span><span class="sxs-lookup"><span data-stu-id="015a5-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="015a5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="015a5-119">Attribute-Id</span></span>      | <span data-ttu-id="015a5-120">1.2.840.113556.1.4.1437</span><span class="sxs-lookup"><span data-stu-id="015a5-120">1.2.840.113556.1.4.1437</span></span>                                                                           |
| <span data-ttu-id="015a5-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="015a5-121">System-Id-Guid</span></span>    | <span data-ttu-id="015a5-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span><span class="sxs-lookup"><span data-stu-id="015a5-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span></span>                                                              |
| <span data-ttu-id="015a5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="015a5-123">Syntax</span></span>            | [<span data-ttu-id="015a5-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="015a5-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="015a5-125">實作</span><span class="sxs-lookup"><span data-stu-id="015a5-125">Implementations</span></span>

-   [<span data-ttu-id="015a5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="015a5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="015a5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="015a5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="015a5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="015a5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="015a5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="015a5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="015a5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="015a5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="015a5-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="015a5-131">Windows Server 2003</span></span>



| <span data-ttu-id="015a5-132">進入</span><span class="sxs-lookup"><span data-stu-id="015a5-132">Entry</span></span> | <span data-ttu-id="015a5-133">值</span><span class="sxs-lookup"><span data-stu-id="015a5-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="015a5-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="015a5-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="015a5-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="015a5-136">System-Only</span></span>            | <span data-ttu-id="015a5-137">否</span><span class="sxs-lookup"><span data-stu-id="015a5-137">False</span></span>                                                                   |
| <span data-ttu-id="015a5-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="015a5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="015a5-139">否</span><span class="sxs-lookup"><span data-stu-id="015a5-139">False</span></span>                                                                   |
| <span data-ttu-id="015a5-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="015a5-140">Is Indexed</span></span>             | <span data-ttu-id="015a5-141">否</span><span class="sxs-lookup"><span data-stu-id="015a5-141">False</span></span>                                                                   |
| <span data-ttu-id="015a5-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="015a5-142">In Global Catalog</span></span>      | <span data-ttu-id="015a5-143">否</span><span class="sxs-lookup"><span data-stu-id="015a5-143">False</span></span>                                                                   |
| <span data-ttu-id="015a5-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="015a5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="015a5-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="015a5-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="015a5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="015a5-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="015a5-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-148">Search-Flags</span></span>           | <span data-ttu-id="015a5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="015a5-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="015a5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-150">System-Flags</span></span>           | <span data-ttu-id="015a5-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="015a5-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="015a5-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="015a5-152">Classes used in</span></span>        | [<span data-ttu-id="015a5-153">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="015a5-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="015a5-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="015a5-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="015a5-155">進入</span><span class="sxs-lookup"><span data-stu-id="015a5-155">Entry</span></span> | <span data-ttu-id="015a5-156">值</span><span class="sxs-lookup"><span data-stu-id="015a5-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="015a5-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="015a5-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="015a5-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="015a5-159">System-Only</span></span>            | <span data-ttu-id="015a5-160">否</span><span class="sxs-lookup"><span data-stu-id="015a5-160">False</span></span>                                                                   |
| <span data-ttu-id="015a5-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="015a5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="015a5-162">否</span><span class="sxs-lookup"><span data-stu-id="015a5-162">False</span></span>                                                                   |
| <span data-ttu-id="015a5-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="015a5-163">Is Indexed</span></span>             | <span data-ttu-id="015a5-164">否</span><span class="sxs-lookup"><span data-stu-id="015a5-164">False</span></span>                                                                   |
| <span data-ttu-id="015a5-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="015a5-165">In Global Catalog</span></span>      | <span data-ttu-id="015a5-166">否</span><span class="sxs-lookup"><span data-stu-id="015a5-166">False</span></span>                                                                   |
| <span data-ttu-id="015a5-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="015a5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="015a5-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="015a5-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="015a5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="015a5-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="015a5-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-171">Search-Flags</span></span>           | <span data-ttu-id="015a5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="015a5-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="015a5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-173">System-Flags</span></span>           | <span data-ttu-id="015a5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="015a5-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="015a5-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="015a5-175">Classes used in</span></span>        | [<span data-ttu-id="015a5-176">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="015a5-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="015a5-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="015a5-177">Windows Server 2008</span></span>



| <span data-ttu-id="015a5-178">進入</span><span class="sxs-lookup"><span data-stu-id="015a5-178">Entry</span></span> | <span data-ttu-id="015a5-179">值</span><span class="sxs-lookup"><span data-stu-id="015a5-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="015a5-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="015a5-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="015a5-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="015a5-182">System-Only</span></span>            | <span data-ttu-id="015a5-183">否</span><span class="sxs-lookup"><span data-stu-id="015a5-183">False</span></span>                                                                   |
| <span data-ttu-id="015a5-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="015a5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="015a5-185">否</span><span class="sxs-lookup"><span data-stu-id="015a5-185">False</span></span>                                                                   |
| <span data-ttu-id="015a5-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="015a5-186">Is Indexed</span></span>             | <span data-ttu-id="015a5-187">否</span><span class="sxs-lookup"><span data-stu-id="015a5-187">False</span></span>                                                                   |
| <span data-ttu-id="015a5-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="015a5-188">In Global Catalog</span></span>      | <span data-ttu-id="015a5-189">否</span><span class="sxs-lookup"><span data-stu-id="015a5-189">False</span></span>                                                                   |
| <span data-ttu-id="015a5-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="015a5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="015a5-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="015a5-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="015a5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="015a5-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="015a5-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-194">Search-Flags</span></span>           | <span data-ttu-id="015a5-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="015a5-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="015a5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-196">System-Flags</span></span>           | <span data-ttu-id="015a5-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="015a5-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="015a5-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="015a5-198">Classes used in</span></span>        | [<span data-ttu-id="015a5-199">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="015a5-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="015a5-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="015a5-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="015a5-201">進入</span><span class="sxs-lookup"><span data-stu-id="015a5-201">Entry</span></span> | <span data-ttu-id="015a5-202">值</span><span class="sxs-lookup"><span data-stu-id="015a5-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="015a5-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="015a5-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="015a5-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="015a5-205">System-Only</span></span>            | <span data-ttu-id="015a5-206">否</span><span class="sxs-lookup"><span data-stu-id="015a5-206">False</span></span>                                                                   |
| <span data-ttu-id="015a5-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="015a5-207">Is-Single-Valued</span></span>       | <span data-ttu-id="015a5-208">否</span><span class="sxs-lookup"><span data-stu-id="015a5-208">False</span></span>                                                                   |
| <span data-ttu-id="015a5-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="015a5-209">Is Indexed</span></span>             | <span data-ttu-id="015a5-210">否</span><span class="sxs-lookup"><span data-stu-id="015a5-210">False</span></span>                                                                   |
| <span data-ttu-id="015a5-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="015a5-211">In Global Catalog</span></span>      | <span data-ttu-id="015a5-212">否</span><span class="sxs-lookup"><span data-stu-id="015a5-212">False</span></span>                                                                   |
| <span data-ttu-id="015a5-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="015a5-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="015a5-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="015a5-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="015a5-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="015a5-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="015a5-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-217">Search-Flags</span></span>           | <span data-ttu-id="015a5-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="015a5-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="015a5-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-219">System-Flags</span></span>           | <span data-ttu-id="015a5-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="015a5-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="015a5-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="015a5-221">Classes used in</span></span>        | [<span data-ttu-id="015a5-222">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="015a5-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="015a5-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="015a5-223">Windows Server 2012</span></span>



| <span data-ttu-id="015a5-224">進入</span><span class="sxs-lookup"><span data-stu-id="015a5-224">Entry</span></span> | <span data-ttu-id="015a5-225">值</span><span class="sxs-lookup"><span data-stu-id="015a5-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="015a5-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="015a5-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="015a5-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="015a5-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="015a5-228">System-Only</span></span>            | <span data-ttu-id="015a5-229">否</span><span class="sxs-lookup"><span data-stu-id="015a5-229">False</span></span>                                                                   |
| <span data-ttu-id="015a5-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="015a5-230">Is-Single-Valued</span></span>       | <span data-ttu-id="015a5-231">否</span><span class="sxs-lookup"><span data-stu-id="015a5-231">False</span></span>                                                                   |
| <span data-ttu-id="015a5-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="015a5-232">Is Indexed</span></span>             | <span data-ttu-id="015a5-233">否</span><span class="sxs-lookup"><span data-stu-id="015a5-233">False</span></span>                                                                   |
| <span data-ttu-id="015a5-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="015a5-234">In Global Catalog</span></span>      | <span data-ttu-id="015a5-235">否</span><span class="sxs-lookup"><span data-stu-id="015a5-235">False</span></span>                                                                   |
| <span data-ttu-id="015a5-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="015a5-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="015a5-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="015a5-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="015a5-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="015a5-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="015a5-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="015a5-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-240">Search-Flags</span></span>           | <span data-ttu-id="015a5-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="015a5-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="015a5-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="015a5-242">System-Flags</span></span>           | <span data-ttu-id="015a5-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="015a5-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="015a5-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="015a5-244">Classes used in</span></span>        | [<span data-ttu-id="015a5-245">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="015a5-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






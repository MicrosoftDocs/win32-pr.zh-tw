---
title: ms-PKI-RA-Signature 屬性
description: 指定註冊要求中所需的註冊註冊授權單位簽章數目。
ms.assetid: da9d9357-6826-4511-b589-594c73114713
ms.tgt_platform: multiple
keywords:
- ms-PKI-RA-Signature 屬性 AD 架構
- Mspki-certificate-name-flag-RA-Signature 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-RA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 170793e46095e16a62d8e025ec16b67bf2be7131
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972896"
---
# <a name="ms-pki-ra-signature-attribute"></a><span data-ttu-id="74b12-105">ms-PKI-RA-Signature 屬性</span><span class="sxs-lookup"><span data-stu-id="74b12-105">ms-PKI-RA-Signature attribute</span></span>

<span data-ttu-id="74b12-106">指定註冊要求中所需的註冊註冊授權單位簽章數目。</span><span class="sxs-lookup"><span data-stu-id="74b12-106">Specifies the number of enrollment registration authority signatures that are required in an enrollment request.</span></span>



| <span data-ttu-id="74b12-107">進入</span><span class="sxs-lookup"><span data-stu-id="74b12-107">Entry</span></span> | <span data-ttu-id="74b12-108">值</span><span class="sxs-lookup"><span data-stu-id="74b12-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b12-109">CN</span><span class="sxs-lookup"><span data-stu-id="74b12-109">CN</span></span>                | <span data-ttu-id="74b12-110">ms-PKI-RA-簽章</span><span class="sxs-lookup"><span data-stu-id="74b12-110">ms-PKI-RA-Signature</span></span>                                                                               |
| <span data-ttu-id="74b12-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="74b12-111">Ldap-Display-Name</span></span> | <span data-ttu-id="74b12-112">Mspki-certificate-name-flag-RA-簽章</span><span class="sxs-lookup"><span data-stu-id="74b12-112">msPKI-RA-Signature</span></span>                                                                                |
| <span data-ttu-id="74b12-113">大小</span><span class="sxs-lookup"><span data-stu-id="74b12-113">Size</span></span>              | <span data-ttu-id="74b12-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="74b12-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="74b12-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="74b12-115">Update Privilege</span></span>  | <span data-ttu-id="74b12-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="74b12-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="74b12-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="74b12-117">Update Frequency</span></span>  | <span data-ttu-id="74b12-118">當您編輯、建立或複製憑證範本時 (ms-PKI-憑證範本) 物件。</span><span class="sxs-lookup"><span data-stu-id="74b12-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="74b12-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="74b12-119">Attribute-Id</span></span>      | <span data-ttu-id="74b12-120">1.2.840.113556.1.4.1429</span><span class="sxs-lookup"><span data-stu-id="74b12-120">1.2.840.113556.1.4.1429</span></span>                                                                           |
| <span data-ttu-id="74b12-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="74b12-121">System-Id-Guid</span></span>    | <span data-ttu-id="74b12-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span><span class="sxs-lookup"><span data-stu-id="74b12-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span></span>                                                              |
| <span data-ttu-id="74b12-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="74b12-123">Syntax</span></span>            | [<span data-ttu-id="74b12-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="74b12-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="74b12-125">實作</span><span class="sxs-lookup"><span data-stu-id="74b12-125">Implementations</span></span>

-   [<span data-ttu-id="74b12-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="74b12-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="74b12-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="74b12-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="74b12-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="74b12-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="74b12-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="74b12-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="74b12-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="74b12-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="74b12-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74b12-131">Windows Server 2003</span></span>



| <span data-ttu-id="74b12-132">進入</span><span class="sxs-lookup"><span data-stu-id="74b12-132">Entry</span></span> | <span data-ttu-id="74b12-133">值</span><span class="sxs-lookup"><span data-stu-id="74b12-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="74b12-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74b12-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b12-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b12-136">System-Only</span></span>            | <span data-ttu-id="74b12-137">否</span><span class="sxs-lookup"><span data-stu-id="74b12-137">False</span></span>                                                                   |
| <span data-ttu-id="74b12-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74b12-138">Is-Single-Valued</span></span>       | <span data-ttu-id="74b12-139">對</span><span class="sxs-lookup"><span data-stu-id="74b12-139">True</span></span>                                                                    |
| <span data-ttu-id="74b12-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74b12-140">Is Indexed</span></span>             | <span data-ttu-id="74b12-141">否</span><span class="sxs-lookup"><span data-stu-id="74b12-141">False</span></span>                                                                   |
| <span data-ttu-id="74b12-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74b12-142">In Global Catalog</span></span>      | <span data-ttu-id="74b12-143">否</span><span class="sxs-lookup"><span data-stu-id="74b12-143">False</span></span>                                                                   |
| <span data-ttu-id="74b12-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74b12-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b12-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74b12-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="74b12-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b12-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b12-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-148">Search-Flags</span></span>           | <span data-ttu-id="74b12-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b12-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="74b12-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-150">System-Flags</span></span>           | <span data-ttu-id="74b12-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b12-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="74b12-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74b12-152">Classes used in</span></span>        | [<span data-ttu-id="74b12-153">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="74b12-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="74b12-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="74b12-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="74b12-155">進入</span><span class="sxs-lookup"><span data-stu-id="74b12-155">Entry</span></span> | <span data-ttu-id="74b12-156">值</span><span class="sxs-lookup"><span data-stu-id="74b12-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="74b12-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74b12-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b12-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b12-159">System-Only</span></span>            | <span data-ttu-id="74b12-160">否</span><span class="sxs-lookup"><span data-stu-id="74b12-160">False</span></span>                                                                   |
| <span data-ttu-id="74b12-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74b12-161">Is-Single-Valued</span></span>       | <span data-ttu-id="74b12-162">對</span><span class="sxs-lookup"><span data-stu-id="74b12-162">True</span></span>                                                                    |
| <span data-ttu-id="74b12-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74b12-163">Is Indexed</span></span>             | <span data-ttu-id="74b12-164">否</span><span class="sxs-lookup"><span data-stu-id="74b12-164">False</span></span>                                                                   |
| <span data-ttu-id="74b12-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74b12-165">In Global Catalog</span></span>      | <span data-ttu-id="74b12-166">否</span><span class="sxs-lookup"><span data-stu-id="74b12-166">False</span></span>                                                                   |
| <span data-ttu-id="74b12-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74b12-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b12-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74b12-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="74b12-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b12-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b12-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-171">Search-Flags</span></span>           | <span data-ttu-id="74b12-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b12-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="74b12-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-173">System-Flags</span></span>           | <span data-ttu-id="74b12-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b12-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="74b12-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74b12-175">Classes used in</span></span>        | [<span data-ttu-id="74b12-176">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="74b12-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="74b12-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74b12-177">Windows Server 2008</span></span>



| <span data-ttu-id="74b12-178">進入</span><span class="sxs-lookup"><span data-stu-id="74b12-178">Entry</span></span> | <span data-ttu-id="74b12-179">值</span><span class="sxs-lookup"><span data-stu-id="74b12-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="74b12-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74b12-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b12-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b12-182">System-Only</span></span>            | <span data-ttu-id="74b12-183">否</span><span class="sxs-lookup"><span data-stu-id="74b12-183">False</span></span>                                                                   |
| <span data-ttu-id="74b12-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74b12-184">Is-Single-Valued</span></span>       | <span data-ttu-id="74b12-185">對</span><span class="sxs-lookup"><span data-stu-id="74b12-185">True</span></span>                                                                    |
| <span data-ttu-id="74b12-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74b12-186">Is Indexed</span></span>             | <span data-ttu-id="74b12-187">否</span><span class="sxs-lookup"><span data-stu-id="74b12-187">False</span></span>                                                                   |
| <span data-ttu-id="74b12-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74b12-188">In Global Catalog</span></span>      | <span data-ttu-id="74b12-189">否</span><span class="sxs-lookup"><span data-stu-id="74b12-189">False</span></span>                                                                   |
| <span data-ttu-id="74b12-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74b12-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b12-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74b12-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="74b12-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b12-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b12-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-194">Search-Flags</span></span>           | <span data-ttu-id="74b12-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b12-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="74b12-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-196">System-Flags</span></span>           | <span data-ttu-id="74b12-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b12-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="74b12-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74b12-198">Classes used in</span></span>        | [<span data-ttu-id="74b12-199">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="74b12-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="74b12-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="74b12-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="74b12-201">進入</span><span class="sxs-lookup"><span data-stu-id="74b12-201">Entry</span></span> | <span data-ttu-id="74b12-202">值</span><span class="sxs-lookup"><span data-stu-id="74b12-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="74b12-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74b12-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b12-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b12-205">System-Only</span></span>            | <span data-ttu-id="74b12-206">否</span><span class="sxs-lookup"><span data-stu-id="74b12-206">False</span></span>                                                                   |
| <span data-ttu-id="74b12-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74b12-207">Is-Single-Valued</span></span>       | <span data-ttu-id="74b12-208">對</span><span class="sxs-lookup"><span data-stu-id="74b12-208">True</span></span>                                                                    |
| <span data-ttu-id="74b12-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74b12-209">Is Indexed</span></span>             | <span data-ttu-id="74b12-210">否</span><span class="sxs-lookup"><span data-stu-id="74b12-210">False</span></span>                                                                   |
| <span data-ttu-id="74b12-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74b12-211">In Global Catalog</span></span>      | <span data-ttu-id="74b12-212">否</span><span class="sxs-lookup"><span data-stu-id="74b12-212">False</span></span>                                                                   |
| <span data-ttu-id="74b12-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74b12-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b12-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74b12-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="74b12-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b12-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b12-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-217">Search-Flags</span></span>           | <span data-ttu-id="74b12-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b12-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="74b12-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-219">System-Flags</span></span>           | <span data-ttu-id="74b12-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b12-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="74b12-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74b12-221">Classes used in</span></span>        | [<span data-ttu-id="74b12-222">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="74b12-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="74b12-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74b12-223">Windows Server 2012</span></span>



| <span data-ttu-id="74b12-224">進入</span><span class="sxs-lookup"><span data-stu-id="74b12-224">Entry</span></span> | <span data-ttu-id="74b12-225">值</span><span class="sxs-lookup"><span data-stu-id="74b12-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="74b12-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74b12-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b12-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="74b12-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b12-228">System-Only</span></span>            | <span data-ttu-id="74b12-229">否</span><span class="sxs-lookup"><span data-stu-id="74b12-229">False</span></span>                                                                   |
| <span data-ttu-id="74b12-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74b12-230">Is-Single-Valued</span></span>       | <span data-ttu-id="74b12-231">對</span><span class="sxs-lookup"><span data-stu-id="74b12-231">True</span></span>                                                                    |
| <span data-ttu-id="74b12-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74b12-232">Is Indexed</span></span>             | <span data-ttu-id="74b12-233">否</span><span class="sxs-lookup"><span data-stu-id="74b12-233">False</span></span>                                                                   |
| <span data-ttu-id="74b12-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74b12-234">In Global Catalog</span></span>      | <span data-ttu-id="74b12-235">否</span><span class="sxs-lookup"><span data-stu-id="74b12-235">False</span></span>                                                                   |
| <span data-ttu-id="74b12-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74b12-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b12-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74b12-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="74b12-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b12-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b12-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="74b12-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-240">Search-Flags</span></span>           | <span data-ttu-id="74b12-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b12-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="74b12-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b12-242">System-Flags</span></span>           | <span data-ttu-id="74b12-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b12-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="74b12-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74b12-244">Classes used in</span></span>        | [<span data-ttu-id="74b12-245">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="74b12-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






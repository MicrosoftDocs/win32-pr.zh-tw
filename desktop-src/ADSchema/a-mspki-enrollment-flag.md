---
title: ms-PKI-註冊-旗標屬性
description: 包含註冊相關的旗標。
ms.assetid: e854acb1-75f4-4379-b404-8fa096419ee6
ms.tgt_platform: multiple
keywords:
- ms-PKI-註冊-旗標屬性 AD 架構
- Mspki-certificate-name-flag-註冊-旗標屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-Enrollment-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2df092e28633bd5825c422e306bf7a65982b32a8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935396"
---
# <a name="ms-pki-enrollment-flag-attribute"></a><span data-ttu-id="e31e5-105">ms-PKI-註冊-旗標屬性</span><span class="sxs-lookup"><span data-stu-id="e31e5-105">ms-PKI-Enrollment-Flag attribute</span></span>

<span data-ttu-id="e31e5-106">包含註冊相關的旗標。</span><span class="sxs-lookup"><span data-stu-id="e31e5-106">Contains the enrollment related flags.</span></span>



| <span data-ttu-id="e31e5-107">進入</span><span class="sxs-lookup"><span data-stu-id="e31e5-107">Entry</span></span> | <span data-ttu-id="e31e5-108">值</span><span class="sxs-lookup"><span data-stu-id="e31e5-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31e5-109">CN</span><span class="sxs-lookup"><span data-stu-id="e31e5-109">CN</span></span>                | <span data-ttu-id="e31e5-110">ms-PKI-註冊-旗標</span><span class="sxs-lookup"><span data-stu-id="e31e5-110">ms-PKI-Enrollment-Flag</span></span>                                                                            |
| <span data-ttu-id="e31e5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e31e5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e31e5-112">Mspki-certificate-name-flag-註冊-旗標</span><span class="sxs-lookup"><span data-stu-id="e31e5-112">msPKI-Enrollment-Flag</span></span>                                                                             |
| <span data-ttu-id="e31e5-113">大小</span><span class="sxs-lookup"><span data-stu-id="e31e5-113">Size</span></span>              | <span data-ttu-id="e31e5-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="e31e5-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="e31e5-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e31e5-115">Update Privilege</span></span>  | <span data-ttu-id="e31e5-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="e31e5-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="e31e5-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e31e5-117">Update Frequency</span></span>  | <span data-ttu-id="e31e5-118">當您編輯、建立或複製憑證範本時 (ms-PKI-憑證範本) 物件。</span><span class="sxs-lookup"><span data-stu-id="e31e5-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="e31e5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e31e5-119">Attribute-Id</span></span>      | <span data-ttu-id="e31e5-120">1.2.840.113556.1.4.1430</span><span class="sxs-lookup"><span data-stu-id="e31e5-120">1.2.840.113556.1.4.1430</span></span>                                                                           |
| <span data-ttu-id="e31e5-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e31e5-121">System-Id-Guid</span></span>    | <span data-ttu-id="e31e5-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span><span class="sxs-lookup"><span data-stu-id="e31e5-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span></span>                                                              |
| <span data-ttu-id="e31e5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e31e5-123">Syntax</span></span>            | [<span data-ttu-id="e31e5-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="e31e5-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="e31e5-125">實作</span><span class="sxs-lookup"><span data-stu-id="e31e5-125">Implementations</span></span>

-   [<span data-ttu-id="e31e5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e31e5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e31e5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e31e5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e31e5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e31e5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e31e5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e31e5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e31e5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e31e5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e31e5-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e31e5-131">Windows Server 2003</span></span>



| <span data-ttu-id="e31e5-132">進入</span><span class="sxs-lookup"><span data-stu-id="e31e5-132">Entry</span></span> | <span data-ttu-id="e31e5-133">值</span><span class="sxs-lookup"><span data-stu-id="e31e5-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e31e5-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31e5-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31e5-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31e5-136">System-Only</span></span>            | <span data-ttu-id="e31e5-137">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-137">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31e5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e31e5-139">對</span><span class="sxs-lookup"><span data-stu-id="e31e5-139">True</span></span>                                                                    |
| <span data-ttu-id="e31e5-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31e5-140">Is Indexed</span></span>             | <span data-ttu-id="e31e5-141">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-141">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31e5-142">In Global Catalog</span></span>      | <span data-ttu-id="e31e5-143">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-143">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31e5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31e5-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31e5-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e31e5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31e5-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31e5-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-148">Search-Flags</span></span>           | <span data-ttu-id="e31e5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31e5-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="e31e5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-150">System-Flags</span></span>           | <span data-ttu-id="e31e5-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31e5-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="e31e5-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31e5-152">Classes used in</span></span>        | [<span data-ttu-id="e31e5-153">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e31e5-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e31e5-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e31e5-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e31e5-155">進入</span><span class="sxs-lookup"><span data-stu-id="e31e5-155">Entry</span></span> | <span data-ttu-id="e31e5-156">值</span><span class="sxs-lookup"><span data-stu-id="e31e5-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e31e5-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31e5-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31e5-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31e5-159">System-Only</span></span>            | <span data-ttu-id="e31e5-160">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-160">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31e5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e31e5-162">對</span><span class="sxs-lookup"><span data-stu-id="e31e5-162">True</span></span>                                                                    |
| <span data-ttu-id="e31e5-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31e5-163">Is Indexed</span></span>             | <span data-ttu-id="e31e5-164">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-164">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31e5-165">In Global Catalog</span></span>      | <span data-ttu-id="e31e5-166">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-166">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31e5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31e5-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31e5-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e31e5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31e5-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31e5-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-171">Search-Flags</span></span>           | <span data-ttu-id="e31e5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31e5-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="e31e5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-173">System-Flags</span></span>           | <span data-ttu-id="e31e5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31e5-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="e31e5-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31e5-175">Classes used in</span></span>        | [<span data-ttu-id="e31e5-176">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e31e5-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e31e5-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e31e5-177">Windows Server 2008</span></span>



| <span data-ttu-id="e31e5-178">進入</span><span class="sxs-lookup"><span data-stu-id="e31e5-178">Entry</span></span> | <span data-ttu-id="e31e5-179">值</span><span class="sxs-lookup"><span data-stu-id="e31e5-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e31e5-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31e5-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31e5-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31e5-182">System-Only</span></span>            | <span data-ttu-id="e31e5-183">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-183">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31e5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e31e5-185">對</span><span class="sxs-lookup"><span data-stu-id="e31e5-185">True</span></span>                                                                    |
| <span data-ttu-id="e31e5-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31e5-186">Is Indexed</span></span>             | <span data-ttu-id="e31e5-187">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-187">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31e5-188">In Global Catalog</span></span>      | <span data-ttu-id="e31e5-189">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-189">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31e5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31e5-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31e5-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e31e5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31e5-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31e5-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-194">Search-Flags</span></span>           | <span data-ttu-id="e31e5-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31e5-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="e31e5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-196">System-Flags</span></span>           | <span data-ttu-id="e31e5-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31e5-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="e31e5-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31e5-198">Classes used in</span></span>        | [<span data-ttu-id="e31e5-199">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e31e5-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e31e5-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e31e5-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e31e5-201">進入</span><span class="sxs-lookup"><span data-stu-id="e31e5-201">Entry</span></span> | <span data-ttu-id="e31e5-202">值</span><span class="sxs-lookup"><span data-stu-id="e31e5-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e31e5-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31e5-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31e5-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31e5-205">System-Only</span></span>            | <span data-ttu-id="e31e5-206">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-206">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31e5-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e31e5-208">對</span><span class="sxs-lookup"><span data-stu-id="e31e5-208">True</span></span>                                                                    |
| <span data-ttu-id="e31e5-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31e5-209">Is Indexed</span></span>             | <span data-ttu-id="e31e5-210">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-210">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31e5-211">In Global Catalog</span></span>      | <span data-ttu-id="e31e5-212">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-212">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31e5-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31e5-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31e5-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e31e5-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31e5-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31e5-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-217">Search-Flags</span></span>           | <span data-ttu-id="e31e5-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31e5-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="e31e5-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-219">System-Flags</span></span>           | <span data-ttu-id="e31e5-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31e5-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="e31e5-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31e5-221">Classes used in</span></span>        | [<span data-ttu-id="e31e5-222">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e31e5-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e31e5-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e31e5-223">Windows Server 2012</span></span>



| <span data-ttu-id="e31e5-224">進入</span><span class="sxs-lookup"><span data-stu-id="e31e5-224">Entry</span></span> | <span data-ttu-id="e31e5-225">值</span><span class="sxs-lookup"><span data-stu-id="e31e5-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e31e5-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31e5-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31e5-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="e31e5-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31e5-228">System-Only</span></span>            | <span data-ttu-id="e31e5-229">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-229">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31e5-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e31e5-231">對</span><span class="sxs-lookup"><span data-stu-id="e31e5-231">True</span></span>                                                                    |
| <span data-ttu-id="e31e5-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31e5-232">Is Indexed</span></span>             | <span data-ttu-id="e31e5-233">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-233">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31e5-234">In Global Catalog</span></span>      | <span data-ttu-id="e31e5-235">否</span><span class="sxs-lookup"><span data-stu-id="e31e5-235">False</span></span>                                                                   |
| <span data-ttu-id="e31e5-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31e5-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31e5-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31e5-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="e31e5-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31e5-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31e5-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="e31e5-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-240">Search-Flags</span></span>           | <span data-ttu-id="e31e5-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31e5-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="e31e5-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31e5-242">System-Flags</span></span>           | <span data-ttu-id="e31e5-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31e5-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="e31e5-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31e5-244">Classes used in</span></span>        | [<span data-ttu-id="e31e5-245">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="e31e5-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






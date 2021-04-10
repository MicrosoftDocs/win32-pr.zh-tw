---
title: ms-PKI-基本金鑰大小屬性
description: 指出最小私用金鑰大小。
ms.assetid: e38fbab5-14db-40d1-80c4-c14477c6f0da
ms.tgt_platform: multiple
keywords:
- ms-PKI-基本金鑰大小的屬性 AD 架構
- Mspki-certificate-name-flag-基本金鑰大小屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-Minimal-Key-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb1a3f168393bb203f7c590ba52924670d3dab2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107723"
---
# <a name="ms-pki-minimal-key-size-attribute"></a><span data-ttu-id="9f376-105">ms-PKI-基本金鑰大小屬性</span><span class="sxs-lookup"><span data-stu-id="9f376-105">ms-PKI-Minimal-Key-Size attribute</span></span>

<span data-ttu-id="9f376-106">指出最小私用金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="9f376-106">Indicates the minimum private key size.</span></span>



| <span data-ttu-id="9f376-107">進入</span><span class="sxs-lookup"><span data-stu-id="9f376-107">Entry</span></span> | <span data-ttu-id="9f376-108">值</span><span class="sxs-lookup"><span data-stu-id="9f376-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f376-109">CN</span><span class="sxs-lookup"><span data-stu-id="9f376-109">CN</span></span>                | <span data-ttu-id="9f376-110">ms-PKI-基本金鑰大小</span><span class="sxs-lookup"><span data-stu-id="9f376-110">ms-PKI-Minimal-Key-Size</span></span>                                                                           |
| <span data-ttu-id="9f376-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9f376-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9f376-112">Mspki-certificate-name-flag-基本-索引鍵大小</span><span class="sxs-lookup"><span data-stu-id="9f376-112">msPKI-Minimal-Key-Size</span></span>                                                                            |
| <span data-ttu-id="9f376-113">大小</span><span class="sxs-lookup"><span data-stu-id="9f376-113">Size</span></span>              | <span data-ttu-id="9f376-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="9f376-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="9f376-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9f376-115">Update Privilege</span></span>  | <span data-ttu-id="9f376-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="9f376-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="9f376-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9f376-117">Update Frequency</span></span>  | <span data-ttu-id="9f376-118">當您編輯、建立或複製憑證範本時 (ms-PKI-憑證範本) 物件。</span><span class="sxs-lookup"><span data-stu-id="9f376-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="9f376-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9f376-119">Attribute-Id</span></span>      | <span data-ttu-id="9f376-120">1.2.840.113556.1.4.1433</span><span class="sxs-lookup"><span data-stu-id="9f376-120">1.2.840.113556.1.4.1433</span></span>                                                                           |
| <span data-ttu-id="9f376-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9f376-121">System-Id-Guid</span></span>    | <span data-ttu-id="9f376-122">e96a63f5-417f-46d3-be52-db7703c503df</span><span class="sxs-lookup"><span data-stu-id="9f376-122">e96a63f5-417f-46d3-be52-db7703c503df</span></span>                                                              |
| <span data-ttu-id="9f376-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f376-123">Syntax</span></span>            | [<span data-ttu-id="9f376-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="9f376-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="9f376-125">實作</span><span class="sxs-lookup"><span data-stu-id="9f376-125">Implementations</span></span>

-   [<span data-ttu-id="9f376-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9f376-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9f376-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9f376-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9f376-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9f376-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9f376-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9f376-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9f376-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9f376-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9f376-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f376-131">Windows Server 2003</span></span>



| <span data-ttu-id="9f376-132">進入</span><span class="sxs-lookup"><span data-stu-id="9f376-132">Entry</span></span> | <span data-ttu-id="9f376-133">值</span><span class="sxs-lookup"><span data-stu-id="9f376-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9f376-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f376-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f376-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f376-136">System-Only</span></span>            | <span data-ttu-id="9f376-137">否</span><span class="sxs-lookup"><span data-stu-id="9f376-137">False</span></span>                                                                   |
| <span data-ttu-id="9f376-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f376-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9f376-139">對</span><span class="sxs-lookup"><span data-stu-id="9f376-139">True</span></span>                                                                    |
| <span data-ttu-id="9f376-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f376-140">Is Indexed</span></span>             | <span data-ttu-id="9f376-141">否</span><span class="sxs-lookup"><span data-stu-id="9f376-141">False</span></span>                                                                   |
| <span data-ttu-id="9f376-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f376-142">In Global Catalog</span></span>      | <span data-ttu-id="9f376-143">否</span><span class="sxs-lookup"><span data-stu-id="9f376-143">False</span></span>                                                                   |
| <span data-ttu-id="9f376-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f376-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f376-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f376-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9f376-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f376-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f376-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-148">Search-Flags</span></span>           | <span data-ttu-id="9f376-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f376-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="9f376-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-150">System-Flags</span></span>           | <span data-ttu-id="9f376-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f376-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="9f376-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f376-152">Classes used in</span></span>        | [<span data-ttu-id="9f376-153">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="9f376-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9f376-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9f376-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9f376-155">進入</span><span class="sxs-lookup"><span data-stu-id="9f376-155">Entry</span></span> | <span data-ttu-id="9f376-156">值</span><span class="sxs-lookup"><span data-stu-id="9f376-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9f376-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f376-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f376-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f376-159">System-Only</span></span>            | <span data-ttu-id="9f376-160">否</span><span class="sxs-lookup"><span data-stu-id="9f376-160">False</span></span>                                                                   |
| <span data-ttu-id="9f376-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f376-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9f376-162">對</span><span class="sxs-lookup"><span data-stu-id="9f376-162">True</span></span>                                                                    |
| <span data-ttu-id="9f376-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f376-163">Is Indexed</span></span>             | <span data-ttu-id="9f376-164">否</span><span class="sxs-lookup"><span data-stu-id="9f376-164">False</span></span>                                                                   |
| <span data-ttu-id="9f376-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f376-165">In Global Catalog</span></span>      | <span data-ttu-id="9f376-166">否</span><span class="sxs-lookup"><span data-stu-id="9f376-166">False</span></span>                                                                   |
| <span data-ttu-id="9f376-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f376-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f376-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f376-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9f376-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f376-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f376-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-171">Search-Flags</span></span>           | <span data-ttu-id="9f376-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f376-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="9f376-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-173">System-Flags</span></span>           | <span data-ttu-id="9f376-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f376-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="9f376-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f376-175">Classes used in</span></span>        | [<span data-ttu-id="9f376-176">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="9f376-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9f376-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f376-177">Windows Server 2008</span></span>



| <span data-ttu-id="9f376-178">進入</span><span class="sxs-lookup"><span data-stu-id="9f376-178">Entry</span></span> | <span data-ttu-id="9f376-179">值</span><span class="sxs-lookup"><span data-stu-id="9f376-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9f376-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f376-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f376-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f376-182">System-Only</span></span>            | <span data-ttu-id="9f376-183">否</span><span class="sxs-lookup"><span data-stu-id="9f376-183">False</span></span>                                                                   |
| <span data-ttu-id="9f376-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f376-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9f376-185">對</span><span class="sxs-lookup"><span data-stu-id="9f376-185">True</span></span>                                                                    |
| <span data-ttu-id="9f376-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f376-186">Is Indexed</span></span>             | <span data-ttu-id="9f376-187">否</span><span class="sxs-lookup"><span data-stu-id="9f376-187">False</span></span>                                                                   |
| <span data-ttu-id="9f376-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f376-188">In Global Catalog</span></span>      | <span data-ttu-id="9f376-189">否</span><span class="sxs-lookup"><span data-stu-id="9f376-189">False</span></span>                                                                   |
| <span data-ttu-id="9f376-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f376-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f376-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f376-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9f376-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f376-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f376-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-194">Search-Flags</span></span>           | <span data-ttu-id="9f376-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f376-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="9f376-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-196">System-Flags</span></span>           | <span data-ttu-id="9f376-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f376-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="9f376-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f376-198">Classes used in</span></span>        | [<span data-ttu-id="9f376-199">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="9f376-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9f376-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f376-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9f376-201">進入</span><span class="sxs-lookup"><span data-stu-id="9f376-201">Entry</span></span> | <span data-ttu-id="9f376-202">值</span><span class="sxs-lookup"><span data-stu-id="9f376-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9f376-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f376-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f376-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f376-205">System-Only</span></span>            | <span data-ttu-id="9f376-206">否</span><span class="sxs-lookup"><span data-stu-id="9f376-206">False</span></span>                                                                   |
| <span data-ttu-id="9f376-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f376-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9f376-208">對</span><span class="sxs-lookup"><span data-stu-id="9f376-208">True</span></span>                                                                    |
| <span data-ttu-id="9f376-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f376-209">Is Indexed</span></span>             | <span data-ttu-id="9f376-210">否</span><span class="sxs-lookup"><span data-stu-id="9f376-210">False</span></span>                                                                   |
| <span data-ttu-id="9f376-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f376-211">In Global Catalog</span></span>      | <span data-ttu-id="9f376-212">否</span><span class="sxs-lookup"><span data-stu-id="9f376-212">False</span></span>                                                                   |
| <span data-ttu-id="9f376-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f376-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f376-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f376-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9f376-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f376-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f376-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-217">Search-Flags</span></span>           | <span data-ttu-id="9f376-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f376-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="9f376-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-219">System-Flags</span></span>           | <span data-ttu-id="9f376-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f376-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="9f376-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f376-221">Classes used in</span></span>        | [<span data-ttu-id="9f376-222">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="9f376-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9f376-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f376-223">Windows Server 2012</span></span>



| <span data-ttu-id="9f376-224">進入</span><span class="sxs-lookup"><span data-stu-id="9f376-224">Entry</span></span> | <span data-ttu-id="9f376-225">值</span><span class="sxs-lookup"><span data-stu-id="9f376-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9f376-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f376-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f376-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9f376-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f376-228">System-Only</span></span>            | <span data-ttu-id="9f376-229">否</span><span class="sxs-lookup"><span data-stu-id="9f376-229">False</span></span>                                                                   |
| <span data-ttu-id="9f376-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f376-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9f376-231">對</span><span class="sxs-lookup"><span data-stu-id="9f376-231">True</span></span>                                                                    |
| <span data-ttu-id="9f376-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f376-232">Is Indexed</span></span>             | <span data-ttu-id="9f376-233">否</span><span class="sxs-lookup"><span data-stu-id="9f376-233">False</span></span>                                                                   |
| <span data-ttu-id="9f376-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f376-234">In Global Catalog</span></span>      | <span data-ttu-id="9f376-235">否</span><span class="sxs-lookup"><span data-stu-id="9f376-235">False</span></span>                                                                   |
| <span data-ttu-id="9f376-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f376-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f376-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f376-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9f376-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f376-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f376-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9f376-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-240">Search-Flags</span></span>           | <span data-ttu-id="9f376-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f376-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="9f376-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f376-242">System-Flags</span></span>           | <span data-ttu-id="9f376-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f376-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="9f376-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f376-244">Classes used in</span></span>        | [<span data-ttu-id="9f376-245">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="9f376-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






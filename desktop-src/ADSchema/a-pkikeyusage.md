---
title: PKI-金鑰使用方式屬性
description: 憑證範本的金鑰使用方式延伸模組。
ms.assetid: 9b3bb28e-7519-4911-9777-f9612bff2d51
ms.tgt_platform: multiple
keywords:
- PKI-金鑰使用方式屬性 AD 架構
- pKIKeyUsage 屬性 AD 架構
topic_type:
- apiref
api_name:
- PKI-Key-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08c5c5b72091060fb475f3becba4f230293c875
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844963"
---
# <a name="pki-key-usage-attribute"></a><span data-ttu-id="2e06b-105">PKI-金鑰使用方式屬性</span><span class="sxs-lookup"><span data-stu-id="2e06b-105">PKI-Key-Usage attribute</span></span>

<span data-ttu-id="2e06b-106">憑證範本的金鑰使用方式延伸模組。</span><span class="sxs-lookup"><span data-stu-id="2e06b-106">The key usage extension for the certificate template.</span></span>



| <span data-ttu-id="2e06b-107">進入</span><span class="sxs-lookup"><span data-stu-id="2e06b-107">Entry</span></span> | <span data-ttu-id="2e06b-108">值</span><span class="sxs-lookup"><span data-stu-id="2e06b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2e06b-109">CN</span><span class="sxs-lookup"><span data-stu-id="2e06b-109">CN</span></span>                | <span data-ttu-id="2e06b-110">PKI-金鑰-使用方式</span><span class="sxs-lookup"><span data-stu-id="2e06b-110">PKI-Key-Usage</span></span>                                         |
| <span data-ttu-id="2e06b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2e06b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2e06b-112">pKIKeyUsage</span><span class="sxs-lookup"><span data-stu-id="2e06b-112">pKIKeyUsage</span></span>                                           |
| <span data-ttu-id="2e06b-113">大小</span><span class="sxs-lookup"><span data-stu-id="2e06b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="2e06b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2e06b-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="2e06b-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2e06b-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="2e06b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e06b-116">Attribute-Id</span></span>      | <span data-ttu-id="2e06b-117">1.2.840.113556.1.4.1328</span><span class="sxs-lookup"><span data-stu-id="2e06b-117">1.2.840.113556.1.4.1328</span></span>                               |
| <span data-ttu-id="2e06b-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2e06b-118">System-Id-Guid</span></span>    | <span data-ttu-id="2e06b-119">e9b0a87e-3b9d-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="2e06b-119">e9b0a87e-3b9d-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="2e06b-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e06b-120">Syntax</span></span>            | [<span data-ttu-id="2e06b-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="2e06b-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="2e06b-122">實作</span><span class="sxs-lookup"><span data-stu-id="2e06b-122">Implementations</span></span>

-   [<span data-ttu-id="2e06b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e06b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e06b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e06b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e06b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e06b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e06b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e06b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e06b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e06b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e06b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e06b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e06b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e06b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2e06b-130">進入</span><span class="sxs-lookup"><span data-stu-id="2e06b-130">Entry</span></span> | <span data-ttu-id="2e06b-131">值</span><span class="sxs-lookup"><span data-stu-id="2e06b-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2e06b-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2e06b-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e06b-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e06b-134">System-Only</span></span>            | <span data-ttu-id="2e06b-135">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-135">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2e06b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2e06b-137">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-137">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2e06b-138">Is Indexed</span></span>             | <span data-ttu-id="2e06b-139">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-139">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2e06b-140">In Global Catalog</span></span>      | <span data-ttu-id="2e06b-141">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-141">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2e06b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e06b-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2e06b-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2e06b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e06b-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e06b-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-146">Search-Flags</span></span>           | <span data-ttu-id="2e06b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e06b-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="2e06b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-148">System-Flags</span></span>           | <span data-ttu-id="2e06b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e06b-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="2e06b-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2e06b-150">Classes used in</span></span>        | [<span data-ttu-id="2e06b-151">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2e06b-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e06b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e06b-152">Windows Server 2003</span></span>



| <span data-ttu-id="2e06b-153">進入</span><span class="sxs-lookup"><span data-stu-id="2e06b-153">Entry</span></span> | <span data-ttu-id="2e06b-154">值</span><span class="sxs-lookup"><span data-stu-id="2e06b-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2e06b-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2e06b-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e06b-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e06b-157">System-Only</span></span>            | <span data-ttu-id="2e06b-158">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-158">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2e06b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="2e06b-160">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-160">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2e06b-161">Is Indexed</span></span>             | <span data-ttu-id="2e06b-162">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-162">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2e06b-163">In Global Catalog</span></span>      | <span data-ttu-id="2e06b-164">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-164">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2e06b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e06b-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2e06b-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2e06b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e06b-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e06b-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-169">Search-Flags</span></span>           | <span data-ttu-id="2e06b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e06b-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="2e06b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-171">System-Flags</span></span>           | <span data-ttu-id="2e06b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e06b-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="2e06b-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2e06b-173">Classes used in</span></span>        | [<span data-ttu-id="2e06b-174">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2e06b-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e06b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e06b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e06b-176">進入</span><span class="sxs-lookup"><span data-stu-id="2e06b-176">Entry</span></span> | <span data-ttu-id="2e06b-177">值</span><span class="sxs-lookup"><span data-stu-id="2e06b-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2e06b-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2e06b-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e06b-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e06b-180">System-Only</span></span>            | <span data-ttu-id="2e06b-181">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-181">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2e06b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="2e06b-183">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-183">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2e06b-184">Is Indexed</span></span>             | <span data-ttu-id="2e06b-185">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-185">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2e06b-186">In Global Catalog</span></span>      | <span data-ttu-id="2e06b-187">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-187">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2e06b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e06b-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2e06b-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2e06b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e06b-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e06b-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-192">Search-Flags</span></span>           | <span data-ttu-id="2e06b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e06b-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="2e06b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-194">System-Flags</span></span>           | <span data-ttu-id="2e06b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e06b-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="2e06b-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2e06b-196">Classes used in</span></span>        | [<span data-ttu-id="2e06b-197">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2e06b-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e06b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e06b-198">Windows Server 2008</span></span>



| <span data-ttu-id="2e06b-199">進入</span><span class="sxs-lookup"><span data-stu-id="2e06b-199">Entry</span></span> | <span data-ttu-id="2e06b-200">值</span><span class="sxs-lookup"><span data-stu-id="2e06b-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2e06b-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2e06b-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e06b-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e06b-203">System-Only</span></span>            | <span data-ttu-id="2e06b-204">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-204">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2e06b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2e06b-206">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-206">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2e06b-207">Is Indexed</span></span>             | <span data-ttu-id="2e06b-208">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-208">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2e06b-209">In Global Catalog</span></span>      | <span data-ttu-id="2e06b-210">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-210">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2e06b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e06b-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2e06b-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2e06b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e06b-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e06b-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-215">Search-Flags</span></span>           | <span data-ttu-id="2e06b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e06b-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="2e06b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-217">System-Flags</span></span>           | <span data-ttu-id="2e06b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e06b-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="2e06b-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2e06b-219">Classes used in</span></span>        | [<span data-ttu-id="2e06b-220">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2e06b-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e06b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e06b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e06b-222">進入</span><span class="sxs-lookup"><span data-stu-id="2e06b-222">Entry</span></span> | <span data-ttu-id="2e06b-223">值</span><span class="sxs-lookup"><span data-stu-id="2e06b-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2e06b-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2e06b-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e06b-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e06b-226">System-Only</span></span>            | <span data-ttu-id="2e06b-227">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-227">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2e06b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="2e06b-229">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-229">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2e06b-230">Is Indexed</span></span>             | <span data-ttu-id="2e06b-231">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-231">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2e06b-232">In Global Catalog</span></span>      | <span data-ttu-id="2e06b-233">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-233">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2e06b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e06b-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2e06b-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2e06b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e06b-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e06b-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-238">Search-Flags</span></span>           | <span data-ttu-id="2e06b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e06b-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="2e06b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-240">System-Flags</span></span>           | <span data-ttu-id="2e06b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e06b-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="2e06b-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2e06b-242">Classes used in</span></span>        | [<span data-ttu-id="2e06b-243">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2e06b-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e06b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e06b-244">Windows Server 2012</span></span>



| <span data-ttu-id="2e06b-245">進入</span><span class="sxs-lookup"><span data-stu-id="2e06b-245">Entry</span></span> | <span data-ttu-id="2e06b-246">值</span><span class="sxs-lookup"><span data-stu-id="2e06b-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2e06b-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2e06b-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e06b-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2e06b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e06b-249">System-Only</span></span>            | <span data-ttu-id="2e06b-250">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-250">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2e06b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="2e06b-252">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-252">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2e06b-253">Is Indexed</span></span>             | <span data-ttu-id="2e06b-254">否</span><span class="sxs-lookup"><span data-stu-id="2e06b-254">False</span></span>                                                                   |
| <span data-ttu-id="2e06b-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2e06b-255">In Global Catalog</span></span>      | <span data-ttu-id="2e06b-256">對</span><span class="sxs-lookup"><span data-stu-id="2e06b-256">True</span></span>                                                                    |
| <span data-ttu-id="2e06b-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2e06b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e06b-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2e06b-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2e06b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e06b-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e06b-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2e06b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-261">Search-Flags</span></span>           | <span data-ttu-id="2e06b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e06b-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="2e06b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e06b-263">System-Flags</span></span>           | <span data-ttu-id="2e06b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e06b-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="2e06b-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2e06b-265">Classes used in</span></span>        | [<span data-ttu-id="2e06b-266">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2e06b-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






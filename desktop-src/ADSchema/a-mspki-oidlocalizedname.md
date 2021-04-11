---
title: ms-PKI-OID-LocalizedName 屬性
description: 包含用來依地區設定描述 OID 的顯示名稱清單。
ms.assetid: 0f0b296d-d17d-4783-9476-6faa5818b8b1
ms.tgt_platform: multiple
keywords:
- ms-PKI-LocalizedName 屬性 AD 架構
- Mspki-certificate-name-flag-OIDLocalizedName 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-OID-LocalizedName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afcd548a95ff4c8ca580692bb0eede947488a1ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845063"
---
# <a name="ms-pki-oid-localizedname-attribute"></a><span data-ttu-id="18faa-105">ms-PKI-OID-LocalizedName 屬性</span><span class="sxs-lookup"><span data-stu-id="18faa-105">ms-PKI-OID-LocalizedName attribute</span></span>

<span data-ttu-id="18faa-106">包含用來依地區設定描述 OID 的顯示名稱清單。</span><span class="sxs-lookup"><span data-stu-id="18faa-106">Contains a list of display names used to describe an OID by locale.</span></span>



| <span data-ttu-id="18faa-107">進入</span><span class="sxs-lookup"><span data-stu-id="18faa-107">Entry</span></span> | <span data-ttu-id="18faa-108">值</span><span class="sxs-lookup"><span data-stu-id="18faa-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="18faa-109">CN</span><span class="sxs-lookup"><span data-stu-id="18faa-109">CN</span></span>                | <span data-ttu-id="18faa-110">ms-PKI-OID-LocalizedName</span><span class="sxs-lookup"><span data-stu-id="18faa-110">ms-PKI-OID-LocalizedName</span></span>                    |
| <span data-ttu-id="18faa-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="18faa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18faa-112">Mspki-certificate-name-flag-OIDLocalizedName</span><span class="sxs-lookup"><span data-stu-id="18faa-112">msPKI-OIDLocalizedName</span></span>                      |
| <span data-ttu-id="18faa-113">大小</span><span class="sxs-lookup"><span data-stu-id="18faa-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="18faa-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="18faa-114">Update Privilege</span></span>  | <span data-ttu-id="18faa-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="18faa-115">Domain administrator</span></span>                        |
| <span data-ttu-id="18faa-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="18faa-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="18faa-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18faa-117">Attribute-Id</span></span>      | <span data-ttu-id="18faa-118">1.2.840.113556.1.4.1712</span><span class="sxs-lookup"><span data-stu-id="18faa-118">1.2.840.113556.1.4.1712</span></span>                     |
| <span data-ttu-id="18faa-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="18faa-119">System-Id-Guid</span></span>    | <span data-ttu-id="18faa-120">7d59a816-bb05-4a72-971f-5c1331f67559</span><span class="sxs-lookup"><span data-stu-id="18faa-120">7d59a816-bb05-4a72-971f-5c1331f67559</span></span>        |
| <span data-ttu-id="18faa-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="18faa-121">Syntax</span></span>            | [<span data-ttu-id="18faa-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="18faa-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="18faa-123">實作</span><span class="sxs-lookup"><span data-stu-id="18faa-123">Implementations</span></span>

-   [<span data-ttu-id="18faa-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18faa-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18faa-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18faa-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18faa-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18faa-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18faa-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18faa-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18faa-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18faa-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="18faa-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18faa-129">Windows Server 2003</span></span>



| <span data-ttu-id="18faa-130">進入</span><span class="sxs-lookup"><span data-stu-id="18faa-130">Entry</span></span> | <span data-ttu-id="18faa-131">值</span><span class="sxs-lookup"><span data-stu-id="18faa-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="18faa-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18faa-132">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18faa-133">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="18faa-134">System-Only</span></span>            | <span data-ttu-id="18faa-135">否</span><span class="sxs-lookup"><span data-stu-id="18faa-135">False</span></span>                                                              |
| <span data-ttu-id="18faa-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18faa-136">Is-Single-Valued</span></span>       | <span data-ttu-id="18faa-137">否</span><span class="sxs-lookup"><span data-stu-id="18faa-137">False</span></span>                                                              |
| <span data-ttu-id="18faa-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18faa-138">Is Indexed</span></span>             | <span data-ttu-id="18faa-139">否</span><span class="sxs-lookup"><span data-stu-id="18faa-139">False</span></span>                                                              |
| <span data-ttu-id="18faa-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18faa-140">In Global Catalog</span></span>      | <span data-ttu-id="18faa-141">否</span><span class="sxs-lookup"><span data-stu-id="18faa-141">False</span></span>                                                              |
| <span data-ttu-id="18faa-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18faa-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="18faa-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18faa-143">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="18faa-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18faa-144">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18faa-145">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-146">Search-Flags</span></span>           | <span data-ttu-id="18faa-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18faa-147">0x00000000</span></span>                                                         |
| <span data-ttu-id="18faa-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-148">System-Flags</span></span>           | <span data-ttu-id="18faa-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18faa-149">0x00000010</span></span>                                                         |
| <span data-ttu-id="18faa-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18faa-150">Classes used in</span></span>        | [<span data-ttu-id="18faa-151">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="18faa-151">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18faa-152">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18faa-152">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18faa-153">進入</span><span class="sxs-lookup"><span data-stu-id="18faa-153">Entry</span></span> | <span data-ttu-id="18faa-154">值</span><span class="sxs-lookup"><span data-stu-id="18faa-154">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="18faa-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18faa-155">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18faa-156">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="18faa-157">System-Only</span></span>            | <span data-ttu-id="18faa-158">否</span><span class="sxs-lookup"><span data-stu-id="18faa-158">False</span></span>                                                              |
| <span data-ttu-id="18faa-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18faa-159">Is-Single-Valued</span></span>       | <span data-ttu-id="18faa-160">否</span><span class="sxs-lookup"><span data-stu-id="18faa-160">False</span></span>                                                              |
| <span data-ttu-id="18faa-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18faa-161">Is Indexed</span></span>             | <span data-ttu-id="18faa-162">否</span><span class="sxs-lookup"><span data-stu-id="18faa-162">False</span></span>                                                              |
| <span data-ttu-id="18faa-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18faa-163">In Global Catalog</span></span>      | <span data-ttu-id="18faa-164">否</span><span class="sxs-lookup"><span data-stu-id="18faa-164">False</span></span>                                                              |
| <span data-ttu-id="18faa-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18faa-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="18faa-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18faa-166">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="18faa-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18faa-167">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18faa-168">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-169">Search-Flags</span></span>           | <span data-ttu-id="18faa-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18faa-170">0x00000000</span></span>                                                         |
| <span data-ttu-id="18faa-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-171">System-Flags</span></span>           | <span data-ttu-id="18faa-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18faa-172">0x00000010</span></span>                                                         |
| <span data-ttu-id="18faa-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18faa-173">Classes used in</span></span>        | [<span data-ttu-id="18faa-174">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="18faa-174">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18faa-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18faa-175">Windows Server 2008</span></span>



| <span data-ttu-id="18faa-176">進入</span><span class="sxs-lookup"><span data-stu-id="18faa-176">Entry</span></span> | <span data-ttu-id="18faa-177">值</span><span class="sxs-lookup"><span data-stu-id="18faa-177">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="18faa-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18faa-178">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18faa-179">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="18faa-180">System-Only</span></span>            | <span data-ttu-id="18faa-181">否</span><span class="sxs-lookup"><span data-stu-id="18faa-181">False</span></span>                                                              |
| <span data-ttu-id="18faa-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18faa-182">Is-Single-Valued</span></span>       | <span data-ttu-id="18faa-183">否</span><span class="sxs-lookup"><span data-stu-id="18faa-183">False</span></span>                                                              |
| <span data-ttu-id="18faa-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18faa-184">Is Indexed</span></span>             | <span data-ttu-id="18faa-185">否</span><span class="sxs-lookup"><span data-stu-id="18faa-185">False</span></span>                                                              |
| <span data-ttu-id="18faa-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18faa-186">In Global Catalog</span></span>      | <span data-ttu-id="18faa-187">否</span><span class="sxs-lookup"><span data-stu-id="18faa-187">False</span></span>                                                              |
| <span data-ttu-id="18faa-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18faa-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="18faa-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18faa-189">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="18faa-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18faa-190">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18faa-191">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-192">Search-Flags</span></span>           | <span data-ttu-id="18faa-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18faa-193">0x00000000</span></span>                                                         |
| <span data-ttu-id="18faa-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-194">System-Flags</span></span>           | <span data-ttu-id="18faa-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18faa-195">0x00000010</span></span>                                                         |
| <span data-ttu-id="18faa-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18faa-196">Classes used in</span></span>        | [<span data-ttu-id="18faa-197">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="18faa-197">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18faa-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18faa-198">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18faa-199">進入</span><span class="sxs-lookup"><span data-stu-id="18faa-199">Entry</span></span> | <span data-ttu-id="18faa-200">值</span><span class="sxs-lookup"><span data-stu-id="18faa-200">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="18faa-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18faa-201">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18faa-202">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="18faa-203">System-Only</span></span>            | <span data-ttu-id="18faa-204">否</span><span class="sxs-lookup"><span data-stu-id="18faa-204">False</span></span>                                                              |
| <span data-ttu-id="18faa-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18faa-205">Is-Single-Valued</span></span>       | <span data-ttu-id="18faa-206">否</span><span class="sxs-lookup"><span data-stu-id="18faa-206">False</span></span>                                                              |
| <span data-ttu-id="18faa-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18faa-207">Is Indexed</span></span>             | <span data-ttu-id="18faa-208">否</span><span class="sxs-lookup"><span data-stu-id="18faa-208">False</span></span>                                                              |
| <span data-ttu-id="18faa-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18faa-209">In Global Catalog</span></span>      | <span data-ttu-id="18faa-210">否</span><span class="sxs-lookup"><span data-stu-id="18faa-210">False</span></span>                                                              |
| <span data-ttu-id="18faa-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18faa-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="18faa-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18faa-212">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="18faa-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18faa-213">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18faa-214">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-215">Search-Flags</span></span>           | <span data-ttu-id="18faa-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18faa-216">0x00000000</span></span>                                                         |
| <span data-ttu-id="18faa-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-217">System-Flags</span></span>           | <span data-ttu-id="18faa-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18faa-218">0x00000010</span></span>                                                         |
| <span data-ttu-id="18faa-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18faa-219">Classes used in</span></span>        | [<span data-ttu-id="18faa-220">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="18faa-220">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18faa-221">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18faa-221">Windows Server 2012</span></span>



| <span data-ttu-id="18faa-222">進入</span><span class="sxs-lookup"><span data-stu-id="18faa-222">Entry</span></span> | <span data-ttu-id="18faa-223">值</span><span class="sxs-lookup"><span data-stu-id="18faa-223">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="18faa-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18faa-224">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18faa-225">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="18faa-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="18faa-226">System-Only</span></span>            | <span data-ttu-id="18faa-227">否</span><span class="sxs-lookup"><span data-stu-id="18faa-227">False</span></span>                                                              |
| <span data-ttu-id="18faa-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18faa-228">Is-Single-Valued</span></span>       | <span data-ttu-id="18faa-229">否</span><span class="sxs-lookup"><span data-stu-id="18faa-229">False</span></span>                                                              |
| <span data-ttu-id="18faa-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18faa-230">Is Indexed</span></span>             | <span data-ttu-id="18faa-231">否</span><span class="sxs-lookup"><span data-stu-id="18faa-231">False</span></span>                                                              |
| <span data-ttu-id="18faa-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18faa-232">In Global Catalog</span></span>      | <span data-ttu-id="18faa-233">否</span><span class="sxs-lookup"><span data-stu-id="18faa-233">False</span></span>                                                              |
| <span data-ttu-id="18faa-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18faa-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="18faa-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18faa-235">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="18faa-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18faa-236">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18faa-237">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="18faa-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-238">Search-Flags</span></span>           | <span data-ttu-id="18faa-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18faa-239">0x00000000</span></span>                                                         |
| <span data-ttu-id="18faa-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18faa-240">System-Flags</span></span>           | <span data-ttu-id="18faa-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18faa-241">0x00000010</span></span>                                                         |
| <span data-ttu-id="18faa-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18faa-242">Classes used in</span></span>        | [<span data-ttu-id="18faa-243">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="18faa-243">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



 

 






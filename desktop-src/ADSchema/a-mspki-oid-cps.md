---
title: ms-PKI-OID-CPS 屬性
description: CPS (「企業簽發者原則」 OID 的憑證原則聲明) 。
ms.assetid: 94c5115e-a8d2-49d1-9fd2-f362e95550dc
ms.tgt_platform: multiple
keywords:
- ms-PKI-OID-CPS 屬性 AD 架構
- Mspki-certificate-name-flag-OID-CPS 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-PKI-OID-CPS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 218fc0eabe7311f46dba769f84b972a495138d3a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845064"
---
# <a name="ms-pki-oid-cps-attribute"></a><span data-ttu-id="cad8c-105">ms-PKI-OID-CPS 屬性</span><span class="sxs-lookup"><span data-stu-id="cad8c-105">ms-PKI-OID-CPS attribute</span></span>

<span data-ttu-id="cad8c-106">CPS (「企業簽發者原則」 OID 的憑證原則聲明) 。</span><span class="sxs-lookup"><span data-stu-id="cad8c-106">The CPS (Certificate Policy Statement) for the enterprise issuer policy OID.</span></span>



| <span data-ttu-id="cad8c-107">進入</span><span class="sxs-lookup"><span data-stu-id="cad8c-107">Entry</span></span> | <span data-ttu-id="cad8c-108">值</span><span class="sxs-lookup"><span data-stu-id="cad8c-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cad8c-109">CN</span><span class="sxs-lookup"><span data-stu-id="cad8c-109">CN</span></span>                | <span data-ttu-id="cad8c-110">ms-PKI-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="cad8c-110">ms-PKI-OID-CPS</span></span>                                                                             |
| <span data-ttu-id="cad8c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="cad8c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cad8c-112">Mspki-certificate-name-flag-OID-CPS</span><span class="sxs-lookup"><span data-stu-id="cad8c-112">msPKI-OID-CPS</span></span>                                                                              |
| <span data-ttu-id="cad8c-113">大小</span><span class="sxs-lookup"><span data-stu-id="cad8c-113">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="cad8c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="cad8c-114">Update Privilege</span></span>  | <span data-ttu-id="cad8c-115">企業系統管理員</span><span class="sxs-lookup"><span data-stu-id="cad8c-115">Enterprise administrator</span></span>                                                                   |
| <span data-ttu-id="cad8c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="cad8c-116">Update Frequency</span></span>  | <span data-ttu-id="cad8c-117">每次建立新範本，或編輯現有範本的屬性時。</span><span class="sxs-lookup"><span data-stu-id="cad8c-117">Whenever a new template is created, or the attributes of an existing templates are edited.</span></span> |
| <span data-ttu-id="cad8c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cad8c-118">Attribute-Id</span></span>      | <span data-ttu-id="cad8c-119">1.2.840.113556.1.4.1672</span><span class="sxs-lookup"><span data-stu-id="cad8c-119">1.2.840.113556.1.4.1672</span></span>                                                                    |
| <span data-ttu-id="cad8c-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="cad8c-120">System-Id-Guid</span></span>    | <span data-ttu-id="cad8c-121">5f49940e-a79f-4a51-bb6f-3d446a54dc6b</span><span class="sxs-lookup"><span data-stu-id="cad8c-121">5f49940e-a79f-4a51-bb6f-3d446a54dc6b</span></span>                                                       |
| <span data-ttu-id="cad8c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="cad8c-122">Syntax</span></span>            | [<span data-ttu-id="cad8c-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cad8c-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="cad8c-124">實作</span><span class="sxs-lookup"><span data-stu-id="cad8c-124">Implementations</span></span>

-   [<span data-ttu-id="cad8c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cad8c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cad8c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cad8c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cad8c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cad8c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cad8c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cad8c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cad8c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cad8c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cad8c-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cad8c-130">Windows Server 2003</span></span>



| <span data-ttu-id="cad8c-131">進入</span><span class="sxs-lookup"><span data-stu-id="cad8c-131">Entry</span></span> | <span data-ttu-id="cad8c-132">值</span><span class="sxs-lookup"><span data-stu-id="cad8c-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cad8c-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cad8c-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cad8c-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cad8c-135">System-Only</span></span>            | <span data-ttu-id="cad8c-136">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-136">False</span></span>                                                              |
| <span data-ttu-id="cad8c-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cad8c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cad8c-138">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-138">False</span></span>                                                              |
| <span data-ttu-id="cad8c-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cad8c-139">Is Indexed</span></span>             | <span data-ttu-id="cad8c-140">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-140">False</span></span>                                                              |
| <span data-ttu-id="cad8c-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cad8c-141">In Global Catalog</span></span>      | <span data-ttu-id="cad8c-142">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-142">False</span></span>                                                              |
| <span data-ttu-id="cad8c-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cad8c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cad8c-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cad8c-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cad8c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cad8c-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cad8c-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-147">Search-Flags</span></span>           | <span data-ttu-id="cad8c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cad8c-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="cad8c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-149">System-Flags</span></span>           | <span data-ttu-id="cad8c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cad8c-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="cad8c-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cad8c-151">Classes used in</span></span>        | [<span data-ttu-id="cad8c-152">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="cad8c-152">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cad8c-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cad8c-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cad8c-154">進入</span><span class="sxs-lookup"><span data-stu-id="cad8c-154">Entry</span></span> | <span data-ttu-id="cad8c-155">值</span><span class="sxs-lookup"><span data-stu-id="cad8c-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cad8c-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cad8c-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cad8c-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cad8c-158">System-Only</span></span>            | <span data-ttu-id="cad8c-159">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-159">False</span></span>                                                              |
| <span data-ttu-id="cad8c-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cad8c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cad8c-161">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-161">False</span></span>                                                              |
| <span data-ttu-id="cad8c-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cad8c-162">Is Indexed</span></span>             | <span data-ttu-id="cad8c-163">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-163">False</span></span>                                                              |
| <span data-ttu-id="cad8c-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cad8c-164">In Global Catalog</span></span>      | <span data-ttu-id="cad8c-165">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-165">False</span></span>                                                              |
| <span data-ttu-id="cad8c-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cad8c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cad8c-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cad8c-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cad8c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cad8c-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cad8c-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-170">Search-Flags</span></span>           | <span data-ttu-id="cad8c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cad8c-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="cad8c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-172">System-Flags</span></span>           | <span data-ttu-id="cad8c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cad8c-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="cad8c-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cad8c-174">Classes used in</span></span>        | [<span data-ttu-id="cad8c-175">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="cad8c-175">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cad8c-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cad8c-176">Windows Server 2008</span></span>



| <span data-ttu-id="cad8c-177">進入</span><span class="sxs-lookup"><span data-stu-id="cad8c-177">Entry</span></span> | <span data-ttu-id="cad8c-178">值</span><span class="sxs-lookup"><span data-stu-id="cad8c-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cad8c-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cad8c-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cad8c-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cad8c-181">System-Only</span></span>            | <span data-ttu-id="cad8c-182">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-182">False</span></span>                                                              |
| <span data-ttu-id="cad8c-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cad8c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cad8c-184">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-184">False</span></span>                                                              |
| <span data-ttu-id="cad8c-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cad8c-185">Is Indexed</span></span>             | <span data-ttu-id="cad8c-186">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-186">False</span></span>                                                              |
| <span data-ttu-id="cad8c-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cad8c-187">In Global Catalog</span></span>      | <span data-ttu-id="cad8c-188">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-188">False</span></span>                                                              |
| <span data-ttu-id="cad8c-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cad8c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cad8c-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cad8c-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cad8c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cad8c-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cad8c-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-193">Search-Flags</span></span>           | <span data-ttu-id="cad8c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cad8c-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="cad8c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-195">System-Flags</span></span>           | <span data-ttu-id="cad8c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cad8c-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="cad8c-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cad8c-197">Classes used in</span></span>        | [<span data-ttu-id="cad8c-198">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="cad8c-198">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cad8c-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cad8c-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cad8c-200">進入</span><span class="sxs-lookup"><span data-stu-id="cad8c-200">Entry</span></span> | <span data-ttu-id="cad8c-201">值</span><span class="sxs-lookup"><span data-stu-id="cad8c-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cad8c-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cad8c-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cad8c-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cad8c-204">System-Only</span></span>            | <span data-ttu-id="cad8c-205">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-205">False</span></span>                                                              |
| <span data-ttu-id="cad8c-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cad8c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cad8c-207">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-207">False</span></span>                                                              |
| <span data-ttu-id="cad8c-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cad8c-208">Is Indexed</span></span>             | <span data-ttu-id="cad8c-209">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-209">False</span></span>                                                              |
| <span data-ttu-id="cad8c-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cad8c-210">In Global Catalog</span></span>      | <span data-ttu-id="cad8c-211">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-211">False</span></span>                                                              |
| <span data-ttu-id="cad8c-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cad8c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cad8c-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cad8c-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cad8c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cad8c-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cad8c-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-216">Search-Flags</span></span>           | <span data-ttu-id="cad8c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cad8c-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="cad8c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-218">System-Flags</span></span>           | <span data-ttu-id="cad8c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cad8c-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="cad8c-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cad8c-220">Classes used in</span></span>        | [<span data-ttu-id="cad8c-221">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="cad8c-221">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cad8c-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cad8c-222">Windows Server 2012</span></span>



| <span data-ttu-id="cad8c-223">進入</span><span class="sxs-lookup"><span data-stu-id="cad8c-223">Entry</span></span> | <span data-ttu-id="cad8c-224">值</span><span class="sxs-lookup"><span data-stu-id="cad8c-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cad8c-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cad8c-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cad8c-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cad8c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cad8c-227">System-Only</span></span>            | <span data-ttu-id="cad8c-228">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-228">False</span></span>                                                              |
| <span data-ttu-id="cad8c-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cad8c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cad8c-230">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-230">False</span></span>                                                              |
| <span data-ttu-id="cad8c-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cad8c-231">Is Indexed</span></span>             | <span data-ttu-id="cad8c-232">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-232">False</span></span>                                                              |
| <span data-ttu-id="cad8c-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cad8c-233">In Global Catalog</span></span>      | <span data-ttu-id="cad8c-234">否</span><span class="sxs-lookup"><span data-stu-id="cad8c-234">False</span></span>                                                              |
| <span data-ttu-id="cad8c-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cad8c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cad8c-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cad8c-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cad8c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cad8c-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cad8c-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cad8c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-239">Search-Flags</span></span>           | <span data-ttu-id="cad8c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cad8c-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="cad8c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cad8c-241">System-Flags</span></span>           | <span data-ttu-id="cad8c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cad8c-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="cad8c-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cad8c-243">Classes used in</span></span>        | [<span data-ttu-id="cad8c-244">**ms-PKI-企業-Oid**</span><span class="sxs-lookup"><span data-stu-id="cad8c-244">**ms-PKI-Enterprise-Oid**</span></span>](c-mspki-enterprise-oid.md)<br/> |



 

 






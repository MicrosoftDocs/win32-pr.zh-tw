---
title: 授權單位-撤銷清單屬性
description: 交叉憑證，憑證撤銷清單。
ms.assetid: a9bc7ed3-4600-41a7-bbe5-4ec546a421fa
ms.tgt_platform: multiple
keywords:
- 授權單位-撤銷清單屬性 AD 架構
- authorityRevocationList 屬性 AD 架構
topic_type:
- apiref
api_name:
- Authority-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fccc08cfb43bf4175bb51f2324e22c247d01f042
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108292"
---
# <a name="authority-revocation-list-attribute"></a><span data-ttu-id="0b81b-105">授權單位-撤銷清單屬性</span><span class="sxs-lookup"><span data-stu-id="0b81b-105">Authority-Revocation-List attribute</span></span>

<span data-ttu-id="0b81b-106">交叉憑證，憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="0b81b-106">Cross certificate, Certificate Revocation List.</span></span>



| <span data-ttu-id="0b81b-107">進入</span><span class="sxs-lookup"><span data-stu-id="0b81b-107">Entry</span></span> | <span data-ttu-id="0b81b-108">值</span><span class="sxs-lookup"><span data-stu-id="0b81b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0b81b-109">CN</span><span class="sxs-lookup"><span data-stu-id="0b81b-109">CN</span></span>                | <span data-ttu-id="0b81b-110">授權單位-撤銷清單</span><span class="sxs-lookup"><span data-stu-id="0b81b-110">Authority-Revocation-List</span></span>                             |
| <span data-ttu-id="0b81b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0b81b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0b81b-112">authorityRevocationList</span><span class="sxs-lookup"><span data-stu-id="0b81b-112">authorityRevocationList</span></span>                               |
| <span data-ttu-id="0b81b-113">大小</span><span class="sxs-lookup"><span data-stu-id="0b81b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="0b81b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0b81b-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="0b81b-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0b81b-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="0b81b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b81b-116">Attribute-Id</span></span>      | <span data-ttu-id="0b81b-117">2.5.4.38</span><span class="sxs-lookup"><span data-stu-id="0b81b-117">2.5.4.38</span></span>                                              |
| <span data-ttu-id="0b81b-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0b81b-118">System-Id-Guid</span></span>    | <span data-ttu-id="0b81b-119">1677578d-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0b81b-119">1677578d-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="0b81b-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b81b-120">Syntax</span></span>            | [<span data-ttu-id="0b81b-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="0b81b-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0b81b-122">實作</span><span class="sxs-lookup"><span data-stu-id="0b81b-122">Implementations</span></span>

-   [<span data-ttu-id="0b81b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0b81b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0b81b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b81b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b81b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b81b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b81b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b81b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b81b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b81b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b81b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b81b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0b81b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b81b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="0b81b-130">進入</span><span class="sxs-lookup"><span data-stu-id="0b81b-130">Entry</span></span> | <span data-ttu-id="0b81b-131">值</span><span class="sxs-lookup"><span data-stu-id="0b81b-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b81b-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b81b-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b81b-133">MAPI-Id</span></span>                | <span data-ttu-id="0b81b-134">0x8026</span><span class="sxs-lookup"><span data-stu-id="0b81b-134">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="0b81b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b81b-135">System-Only</span></span>            | <span data-ttu-id="0b81b-136">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b81b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="0b81b-138">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b81b-139">Is Indexed</span></span>             | <span data-ttu-id="0b81b-140">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b81b-141">In Global Catalog</span></span>      | <span data-ttu-id="0b81b-142">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b81b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b81b-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b81b-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="0b81b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b81b-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b81b-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-147">Search-Flags</span></span>           | <span data-ttu-id="0b81b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b81b-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-149">System-Flags</span></span>           | <span data-ttu-id="0b81b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b81b-150">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b81b-151">Classes used in</span></span>        | [<span data-ttu-id="0b81b-152">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="0b81b-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="0b81b-153">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="0b81b-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0b81b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b81b-154">Windows Server 2003</span></span>



| <span data-ttu-id="0b81b-155">進入</span><span class="sxs-lookup"><span data-stu-id="0b81b-155">Entry</span></span> | <span data-ttu-id="0b81b-156">值</span><span class="sxs-lookup"><span data-stu-id="0b81b-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b81b-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b81b-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b81b-158">MAPI-Id</span></span>                | <span data-ttu-id="0b81b-159">0x8026</span><span class="sxs-lookup"><span data-stu-id="0b81b-159">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="0b81b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b81b-160">System-Only</span></span>            | <span data-ttu-id="0b81b-161">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b81b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0b81b-163">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b81b-164">Is Indexed</span></span>             | <span data-ttu-id="0b81b-165">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b81b-166">In Global Catalog</span></span>      | <span data-ttu-id="0b81b-167">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b81b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b81b-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b81b-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="0b81b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b81b-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b81b-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-172">Search-Flags</span></span>           | <span data-ttu-id="0b81b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b81b-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-174">System-Flags</span></span>           | <span data-ttu-id="0b81b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b81b-175">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b81b-176">Classes used in</span></span>        | [<span data-ttu-id="0b81b-177">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="0b81b-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="0b81b-178">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="0b81b-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b81b-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b81b-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b81b-180">進入</span><span class="sxs-lookup"><span data-stu-id="0b81b-180">Entry</span></span> | <span data-ttu-id="0b81b-181">值</span><span class="sxs-lookup"><span data-stu-id="0b81b-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b81b-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b81b-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b81b-183">MAPI-Id</span></span>                | <span data-ttu-id="0b81b-184">0x8026</span><span class="sxs-lookup"><span data-stu-id="0b81b-184">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="0b81b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b81b-185">System-Only</span></span>            | <span data-ttu-id="0b81b-186">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b81b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="0b81b-188">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b81b-189">Is Indexed</span></span>             | <span data-ttu-id="0b81b-190">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b81b-191">In Global Catalog</span></span>      | <span data-ttu-id="0b81b-192">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b81b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b81b-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b81b-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="0b81b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b81b-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b81b-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-197">Search-Flags</span></span>           | <span data-ttu-id="0b81b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b81b-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-199">System-Flags</span></span>           | <span data-ttu-id="0b81b-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b81b-200">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b81b-201">Classes used in</span></span>        | [<span data-ttu-id="0b81b-202">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="0b81b-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="0b81b-203">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="0b81b-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b81b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b81b-204">Windows Server 2008</span></span>



| <span data-ttu-id="0b81b-205">進入</span><span class="sxs-lookup"><span data-stu-id="0b81b-205">Entry</span></span> | <span data-ttu-id="0b81b-206">值</span><span class="sxs-lookup"><span data-stu-id="0b81b-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b81b-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b81b-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b81b-208">MAPI-Id</span></span>                | <span data-ttu-id="0b81b-209">0x8026</span><span class="sxs-lookup"><span data-stu-id="0b81b-209">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="0b81b-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b81b-210">System-Only</span></span>            | <span data-ttu-id="0b81b-211">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b81b-212">Is-Single-Valued</span></span>       | <span data-ttu-id="0b81b-213">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b81b-214">Is Indexed</span></span>             | <span data-ttu-id="0b81b-215">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b81b-216">In Global Catalog</span></span>      | <span data-ttu-id="0b81b-217">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b81b-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b81b-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b81b-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="0b81b-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b81b-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b81b-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-222">Search-Flags</span></span>           | <span data-ttu-id="0b81b-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b81b-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-224">System-Flags</span></span>           | <span data-ttu-id="0b81b-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b81b-225">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b81b-226">Classes used in</span></span>        | [<span data-ttu-id="0b81b-227">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="0b81b-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="0b81b-228">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="0b81b-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b81b-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b81b-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b81b-230">進入</span><span class="sxs-lookup"><span data-stu-id="0b81b-230">Entry</span></span> | <span data-ttu-id="0b81b-231">值</span><span class="sxs-lookup"><span data-stu-id="0b81b-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b81b-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b81b-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b81b-233">MAPI-Id</span></span>                | <span data-ttu-id="0b81b-234">0x8026</span><span class="sxs-lookup"><span data-stu-id="0b81b-234">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="0b81b-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b81b-235">System-Only</span></span>            | <span data-ttu-id="0b81b-236">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b81b-237">Is-Single-Valued</span></span>       | <span data-ttu-id="0b81b-238">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b81b-239">Is Indexed</span></span>             | <span data-ttu-id="0b81b-240">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b81b-241">In Global Catalog</span></span>      | <span data-ttu-id="0b81b-242">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b81b-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b81b-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b81b-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="0b81b-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b81b-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b81b-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-247">Search-Flags</span></span>           | <span data-ttu-id="0b81b-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b81b-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-249">System-Flags</span></span>           | <span data-ttu-id="0b81b-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b81b-250">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b81b-251">Classes used in</span></span>        | [<span data-ttu-id="0b81b-252">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="0b81b-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="0b81b-253">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="0b81b-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b81b-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b81b-254">Windows Server 2012</span></span>



| <span data-ttu-id="0b81b-255">進入</span><span class="sxs-lookup"><span data-stu-id="0b81b-255">Entry</span></span> | <span data-ttu-id="0b81b-256">值</span><span class="sxs-lookup"><span data-stu-id="0b81b-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b81b-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b81b-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b81b-258">MAPI-Id</span></span>                | <span data-ttu-id="0b81b-259">0x8026</span><span class="sxs-lookup"><span data-stu-id="0b81b-259">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="0b81b-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b81b-260">System-Only</span></span>            | <span data-ttu-id="0b81b-261">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b81b-262">Is-Single-Valued</span></span>       | <span data-ttu-id="0b81b-263">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b81b-264">Is Indexed</span></span>             | <span data-ttu-id="0b81b-265">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b81b-266">In Global Catalog</span></span>      | <span data-ttu-id="0b81b-267">否</span><span class="sxs-lookup"><span data-stu-id="0b81b-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="0b81b-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b81b-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b81b-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b81b-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="0b81b-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b81b-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b81b-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="0b81b-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-272">Search-Flags</span></span>           | <span data-ttu-id="0b81b-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b81b-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b81b-274">System-Flags</span></span>           | <span data-ttu-id="0b81b-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b81b-275">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="0b81b-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b81b-276">Classes used in</span></span>        | [<span data-ttu-id="0b81b-277">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="0b81b-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="0b81b-278">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="0b81b-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 






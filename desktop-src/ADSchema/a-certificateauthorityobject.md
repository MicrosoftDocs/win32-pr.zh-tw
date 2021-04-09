---
title: 憑證授權單位單位-物件屬性
description: 參考與憑證撤銷清單發佈點相關聯的憑證授權單位單位。
ms.assetid: 8dfd4441-6b45-4dc4-aed8-e33aa7fd099f
ms.tgt_platform: multiple
keywords:
- 憑證授權單位單位-物件屬性 AD 架構
- certificateAuthorityObject 屬性 AD 架構
topic_type:
- apiref
api_name:
- Certificate-Authority-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65ffceb810cd6a4ef3033834dbf0f3c489f1506e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845615"
---
# <a name="certificate-authority-object-attribute"></a><span data-ttu-id="727c2-105">憑證授權單位單位-物件屬性</span><span class="sxs-lookup"><span data-stu-id="727c2-105">Certificate-Authority-Object attribute</span></span>

<span data-ttu-id="727c2-106">參考與憑證撤銷清單發佈點相關聯的憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="727c2-106">Reference to the certification authority associated with a Certificate Revocation List distribution point.</span></span>



| <span data-ttu-id="727c2-107">進入</span><span class="sxs-lookup"><span data-stu-id="727c2-107">Entry</span></span> | <span data-ttu-id="727c2-108">值</span><span class="sxs-lookup"><span data-stu-id="727c2-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="727c2-109">CN</span><span class="sxs-lookup"><span data-stu-id="727c2-109">CN</span></span>                | <span data-ttu-id="727c2-110">憑證授權單位單位-物件</span><span class="sxs-lookup"><span data-stu-id="727c2-110">Certificate-Authority-Object</span></span>            |
| <span data-ttu-id="727c2-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="727c2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="727c2-112">certificateAuthorityObject</span><span class="sxs-lookup"><span data-stu-id="727c2-112">certificateAuthorityObject</span></span>              |
| <span data-ttu-id="727c2-113">大小</span><span class="sxs-lookup"><span data-stu-id="727c2-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="727c2-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="727c2-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="727c2-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="727c2-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="727c2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="727c2-116">Attribute-Id</span></span>      | <span data-ttu-id="727c2-117">1.2.840.113556.1.4.684</span><span class="sxs-lookup"><span data-stu-id="727c2-117">1.2.840.113556.1.4.684</span></span>                  |
| <span data-ttu-id="727c2-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="727c2-118">System-Id-Guid</span></span>    | <span data-ttu-id="727c2-119">963d2732-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="727c2-119">963d2732-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="727c2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="727c2-120">Syntax</span></span>            | [<span data-ttu-id="727c2-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="727c2-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="727c2-122">實作</span><span class="sxs-lookup"><span data-stu-id="727c2-122">Implementations</span></span>

-   [<span data-ttu-id="727c2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="727c2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="727c2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="727c2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="727c2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="727c2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="727c2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="727c2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="727c2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="727c2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="727c2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="727c2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="727c2-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="727c2-129">Windows 2000 Server</span></span>



| <span data-ttu-id="727c2-130">進入</span><span class="sxs-lookup"><span data-stu-id="727c2-130">Entry</span></span> | <span data-ttu-id="727c2-131">值</span><span class="sxs-lookup"><span data-stu-id="727c2-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="727c2-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="727c2-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="727c2-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="727c2-134">System-Only</span></span>            | <span data-ttu-id="727c2-135">否</span><span class="sxs-lookup"><span data-stu-id="727c2-135">False</span></span>                                                               |
| <span data-ttu-id="727c2-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="727c2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="727c2-137">對</span><span class="sxs-lookup"><span data-stu-id="727c2-137">True</span></span>                                                                |
| <span data-ttu-id="727c2-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="727c2-138">Is Indexed</span></span>             | <span data-ttu-id="727c2-139">否</span><span class="sxs-lookup"><span data-stu-id="727c2-139">False</span></span>                                                               |
| <span data-ttu-id="727c2-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="727c2-140">In Global Catalog</span></span>      | <span data-ttu-id="727c2-141">否</span><span class="sxs-lookup"><span data-stu-id="727c2-141">False</span></span>                                                               |
| <span data-ttu-id="727c2-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="727c2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="727c2-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="727c2-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="727c2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="727c2-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="727c2-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-146">Search-Flags</span></span>           | <span data-ttu-id="727c2-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="727c2-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="727c2-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-148">System-Flags</span></span>           | <span data-ttu-id="727c2-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="727c2-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="727c2-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="727c2-150">Classes used in</span></span>        | [<span data-ttu-id="727c2-151">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="727c2-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="727c2-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="727c2-152">Windows Server 2003</span></span>



| <span data-ttu-id="727c2-153">進入</span><span class="sxs-lookup"><span data-stu-id="727c2-153">Entry</span></span> | <span data-ttu-id="727c2-154">值</span><span class="sxs-lookup"><span data-stu-id="727c2-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="727c2-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="727c2-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="727c2-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="727c2-157">System-Only</span></span>            | <span data-ttu-id="727c2-158">否</span><span class="sxs-lookup"><span data-stu-id="727c2-158">False</span></span>                                                               |
| <span data-ttu-id="727c2-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="727c2-159">Is-Single-Valued</span></span>       | <span data-ttu-id="727c2-160">對</span><span class="sxs-lookup"><span data-stu-id="727c2-160">True</span></span>                                                                |
| <span data-ttu-id="727c2-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="727c2-161">Is Indexed</span></span>             | <span data-ttu-id="727c2-162">否</span><span class="sxs-lookup"><span data-stu-id="727c2-162">False</span></span>                                                               |
| <span data-ttu-id="727c2-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="727c2-163">In Global Catalog</span></span>      | <span data-ttu-id="727c2-164">否</span><span class="sxs-lookup"><span data-stu-id="727c2-164">False</span></span>                                                               |
| <span data-ttu-id="727c2-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="727c2-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="727c2-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="727c2-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="727c2-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="727c2-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="727c2-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-169">Search-Flags</span></span>           | <span data-ttu-id="727c2-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="727c2-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="727c2-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-171">System-Flags</span></span>           | <span data-ttu-id="727c2-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="727c2-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="727c2-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="727c2-173">Classes used in</span></span>        | [<span data-ttu-id="727c2-174">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="727c2-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="727c2-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="727c2-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="727c2-176">進入</span><span class="sxs-lookup"><span data-stu-id="727c2-176">Entry</span></span> | <span data-ttu-id="727c2-177">值</span><span class="sxs-lookup"><span data-stu-id="727c2-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="727c2-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="727c2-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="727c2-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="727c2-180">System-Only</span></span>            | <span data-ttu-id="727c2-181">否</span><span class="sxs-lookup"><span data-stu-id="727c2-181">False</span></span>                                                               |
| <span data-ttu-id="727c2-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="727c2-182">Is-Single-Valued</span></span>       | <span data-ttu-id="727c2-183">對</span><span class="sxs-lookup"><span data-stu-id="727c2-183">True</span></span>                                                                |
| <span data-ttu-id="727c2-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="727c2-184">Is Indexed</span></span>             | <span data-ttu-id="727c2-185">否</span><span class="sxs-lookup"><span data-stu-id="727c2-185">False</span></span>                                                               |
| <span data-ttu-id="727c2-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="727c2-186">In Global Catalog</span></span>      | <span data-ttu-id="727c2-187">否</span><span class="sxs-lookup"><span data-stu-id="727c2-187">False</span></span>                                                               |
| <span data-ttu-id="727c2-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="727c2-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="727c2-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="727c2-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="727c2-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="727c2-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="727c2-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-192">Search-Flags</span></span>           | <span data-ttu-id="727c2-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="727c2-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="727c2-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-194">System-Flags</span></span>           | <span data-ttu-id="727c2-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="727c2-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="727c2-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="727c2-196">Classes used in</span></span>        | [<span data-ttu-id="727c2-197">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="727c2-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="727c2-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="727c2-198">Windows Server 2008</span></span>



| <span data-ttu-id="727c2-199">進入</span><span class="sxs-lookup"><span data-stu-id="727c2-199">Entry</span></span> | <span data-ttu-id="727c2-200">值</span><span class="sxs-lookup"><span data-stu-id="727c2-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="727c2-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="727c2-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="727c2-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="727c2-203">System-Only</span></span>            | <span data-ttu-id="727c2-204">否</span><span class="sxs-lookup"><span data-stu-id="727c2-204">False</span></span>                                                               |
| <span data-ttu-id="727c2-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="727c2-205">Is-Single-Valued</span></span>       | <span data-ttu-id="727c2-206">對</span><span class="sxs-lookup"><span data-stu-id="727c2-206">True</span></span>                                                                |
| <span data-ttu-id="727c2-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="727c2-207">Is Indexed</span></span>             | <span data-ttu-id="727c2-208">否</span><span class="sxs-lookup"><span data-stu-id="727c2-208">False</span></span>                                                               |
| <span data-ttu-id="727c2-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="727c2-209">In Global Catalog</span></span>      | <span data-ttu-id="727c2-210">否</span><span class="sxs-lookup"><span data-stu-id="727c2-210">False</span></span>                                                               |
| <span data-ttu-id="727c2-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="727c2-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="727c2-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="727c2-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="727c2-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="727c2-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="727c2-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-215">Search-Flags</span></span>           | <span data-ttu-id="727c2-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="727c2-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="727c2-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-217">System-Flags</span></span>           | <span data-ttu-id="727c2-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="727c2-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="727c2-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="727c2-219">Classes used in</span></span>        | [<span data-ttu-id="727c2-220">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="727c2-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="727c2-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="727c2-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="727c2-222">進入</span><span class="sxs-lookup"><span data-stu-id="727c2-222">Entry</span></span> | <span data-ttu-id="727c2-223">值</span><span class="sxs-lookup"><span data-stu-id="727c2-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="727c2-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="727c2-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="727c2-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="727c2-226">System-Only</span></span>            | <span data-ttu-id="727c2-227">否</span><span class="sxs-lookup"><span data-stu-id="727c2-227">False</span></span>                                                               |
| <span data-ttu-id="727c2-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="727c2-228">Is-Single-Valued</span></span>       | <span data-ttu-id="727c2-229">對</span><span class="sxs-lookup"><span data-stu-id="727c2-229">True</span></span>                                                                |
| <span data-ttu-id="727c2-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="727c2-230">Is Indexed</span></span>             | <span data-ttu-id="727c2-231">否</span><span class="sxs-lookup"><span data-stu-id="727c2-231">False</span></span>                                                               |
| <span data-ttu-id="727c2-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="727c2-232">In Global Catalog</span></span>      | <span data-ttu-id="727c2-233">否</span><span class="sxs-lookup"><span data-stu-id="727c2-233">False</span></span>                                                               |
| <span data-ttu-id="727c2-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="727c2-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="727c2-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="727c2-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="727c2-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="727c2-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="727c2-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-238">Search-Flags</span></span>           | <span data-ttu-id="727c2-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="727c2-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="727c2-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-240">System-Flags</span></span>           | <span data-ttu-id="727c2-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="727c2-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="727c2-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="727c2-242">Classes used in</span></span>        | [<span data-ttu-id="727c2-243">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="727c2-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="727c2-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="727c2-244">Windows Server 2012</span></span>



| <span data-ttu-id="727c2-245">進入</span><span class="sxs-lookup"><span data-stu-id="727c2-245">Entry</span></span> | <span data-ttu-id="727c2-246">值</span><span class="sxs-lookup"><span data-stu-id="727c2-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="727c2-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="727c2-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="727c2-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="727c2-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="727c2-249">System-Only</span></span>            | <span data-ttu-id="727c2-250">否</span><span class="sxs-lookup"><span data-stu-id="727c2-250">False</span></span>                                                               |
| <span data-ttu-id="727c2-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="727c2-251">Is-Single-Valued</span></span>       | <span data-ttu-id="727c2-252">對</span><span class="sxs-lookup"><span data-stu-id="727c2-252">True</span></span>                                                                |
| <span data-ttu-id="727c2-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="727c2-253">Is Indexed</span></span>             | <span data-ttu-id="727c2-254">否</span><span class="sxs-lookup"><span data-stu-id="727c2-254">False</span></span>                                                               |
| <span data-ttu-id="727c2-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="727c2-255">In Global Catalog</span></span>      | <span data-ttu-id="727c2-256">否</span><span class="sxs-lookup"><span data-stu-id="727c2-256">False</span></span>                                                               |
| <span data-ttu-id="727c2-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="727c2-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="727c2-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="727c2-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="727c2-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="727c2-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="727c2-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="727c2-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-261">Search-Flags</span></span>           | <span data-ttu-id="727c2-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="727c2-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="727c2-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="727c2-263">System-Flags</span></span>           | <span data-ttu-id="727c2-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="727c2-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="727c2-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="727c2-265">Classes used in</span></span>        | [<span data-ttu-id="727c2-266">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="727c2-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 






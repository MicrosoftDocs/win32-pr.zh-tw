---
title: 差異-撤銷清單屬性
description: 自上次差異更新後撤銷的憑證清單。
ms.assetid: fc755c22-6d4f-4509-abb8-47c4f2f37545
ms.tgt_platform: multiple
keywords:
- 差異-撤銷清單屬性 AD 架構
- deltaRevocationList 屬性 AD 架構
topic_type:
- apiref
api_name:
- Delta-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e866090dfb754c11fb4a25bbe904d5922a8fafd6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107136"
---
# <a name="delta-revocation-list-attribute"></a><span data-ttu-id="3cff2-105">差異-撤銷清單屬性</span><span class="sxs-lookup"><span data-stu-id="3cff2-105">Delta-Revocation-List attribute</span></span>

<span data-ttu-id="3cff2-106">自上次差異更新後撤銷的憑證清單。</span><span class="sxs-lookup"><span data-stu-id="3cff2-106">List of certificates that have been revoked since the last delta update.</span></span>



| <span data-ttu-id="3cff2-107">進入</span><span class="sxs-lookup"><span data-stu-id="3cff2-107">Entry</span></span> | <span data-ttu-id="3cff2-108">值</span><span class="sxs-lookup"><span data-stu-id="3cff2-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="3cff2-109">CN</span><span class="sxs-lookup"><span data-stu-id="3cff2-109">CN</span></span>                | <span data-ttu-id="3cff2-110">差異-撤銷清單</span><span class="sxs-lookup"><span data-stu-id="3cff2-110">Delta-Revocation-List</span></span>                                 |
| <span data-ttu-id="3cff2-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3cff2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3cff2-112">deltaRevocationList</span><span class="sxs-lookup"><span data-stu-id="3cff2-112">deltaRevocationList</span></span>                                   |
| <span data-ttu-id="3cff2-113">大小</span><span class="sxs-lookup"><span data-stu-id="3cff2-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="3cff2-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3cff2-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="3cff2-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3cff2-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="3cff2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3cff2-116">Attribute-Id</span></span>      | <span data-ttu-id="3cff2-117">2.5.4.53</span><span class="sxs-lookup"><span data-stu-id="3cff2-117">2.5.4.53</span></span>                                              |
| <span data-ttu-id="3cff2-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3cff2-118">System-Id-Guid</span></span>    | <span data-ttu-id="3cff2-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3cff2-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="3cff2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cff2-120">Syntax</span></span>            | [<span data-ttu-id="3cff2-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="3cff2-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="3cff2-122">實作</span><span class="sxs-lookup"><span data-stu-id="3cff2-122">Implementations</span></span>

-   [<span data-ttu-id="3cff2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3cff2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3cff2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3cff2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3cff2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3cff2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3cff2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3cff2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3cff2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3cff2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3cff2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3cff2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3cff2-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3cff2-129">Windows 2000 Server</span></span>



| <span data-ttu-id="3cff2-130">進入</span><span class="sxs-lookup"><span data-stu-id="3cff2-130">Entry</span></span> | <span data-ttu-id="3cff2-131">值</span><span class="sxs-lookup"><span data-stu-id="3cff2-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cff2-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3cff2-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cff2-133">MAPI-Id</span></span>                | <span data-ttu-id="3cff2-134">0x8C46</span><span class="sxs-lookup"><span data-stu-id="3cff2-134">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="3cff2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cff2-135">System-Only</span></span>            | <span data-ttu-id="3cff2-136">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3cff2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3cff2-138">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3cff2-139">Is Indexed</span></span>             | <span data-ttu-id="3cff2-140">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3cff2-141">In Global Catalog</span></span>      | <span data-ttu-id="3cff2-142">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3cff2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cff2-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3cff2-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3cff2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cff2-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cff2-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-147">Search-Flags</span></span>           | <span data-ttu-id="3cff2-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-149">System-Flags</span></span>           | <span data-ttu-id="3cff2-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-150">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3cff2-151">Classes used in</span></span>        | [<span data-ttu-id="3cff2-152">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="3cff2-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="3cff2-153">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="3cff2-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3cff2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3cff2-154">Windows Server 2003</span></span>



| <span data-ttu-id="3cff2-155">進入</span><span class="sxs-lookup"><span data-stu-id="3cff2-155">Entry</span></span> | <span data-ttu-id="3cff2-156">值</span><span class="sxs-lookup"><span data-stu-id="3cff2-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cff2-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3cff2-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cff2-158">MAPI-Id</span></span>                | <span data-ttu-id="3cff2-159">0x8C46</span><span class="sxs-lookup"><span data-stu-id="3cff2-159">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="3cff2-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cff2-160">System-Only</span></span>            | <span data-ttu-id="3cff2-161">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3cff2-162">Is-Single-Valued</span></span>       | <span data-ttu-id="3cff2-163">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3cff2-164">Is Indexed</span></span>             | <span data-ttu-id="3cff2-165">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3cff2-166">In Global Catalog</span></span>      | <span data-ttu-id="3cff2-167">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3cff2-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cff2-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3cff2-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3cff2-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cff2-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cff2-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-172">Search-Flags</span></span>           | <span data-ttu-id="3cff2-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-174">System-Flags</span></span>           | <span data-ttu-id="3cff2-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-175">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3cff2-176">Classes used in</span></span>        | [<span data-ttu-id="3cff2-177">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="3cff2-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="3cff2-178">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="3cff2-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3cff2-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3cff2-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3cff2-180">進入</span><span class="sxs-lookup"><span data-stu-id="3cff2-180">Entry</span></span> | <span data-ttu-id="3cff2-181">值</span><span class="sxs-lookup"><span data-stu-id="3cff2-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cff2-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3cff2-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cff2-183">MAPI-Id</span></span>                | <span data-ttu-id="3cff2-184">0x8C46</span><span class="sxs-lookup"><span data-stu-id="3cff2-184">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="3cff2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cff2-185">System-Only</span></span>            | <span data-ttu-id="3cff2-186">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3cff2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3cff2-188">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3cff2-189">Is Indexed</span></span>             | <span data-ttu-id="3cff2-190">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3cff2-191">In Global Catalog</span></span>      | <span data-ttu-id="3cff2-192">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3cff2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cff2-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3cff2-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3cff2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cff2-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cff2-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-197">Search-Flags</span></span>           | <span data-ttu-id="3cff2-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-199">System-Flags</span></span>           | <span data-ttu-id="3cff2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-200">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3cff2-201">Classes used in</span></span>        | [<span data-ttu-id="3cff2-202">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="3cff2-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="3cff2-203">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="3cff2-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3cff2-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cff2-204">Windows Server 2008</span></span>



| <span data-ttu-id="3cff2-205">進入</span><span class="sxs-lookup"><span data-stu-id="3cff2-205">Entry</span></span> | <span data-ttu-id="3cff2-206">值</span><span class="sxs-lookup"><span data-stu-id="3cff2-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cff2-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3cff2-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cff2-208">MAPI-Id</span></span>                | <span data-ttu-id="3cff2-209">0x8C46</span><span class="sxs-lookup"><span data-stu-id="3cff2-209">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="3cff2-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cff2-210">System-Only</span></span>            | <span data-ttu-id="3cff2-211">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3cff2-212">Is-Single-Valued</span></span>       | <span data-ttu-id="3cff2-213">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3cff2-214">Is Indexed</span></span>             | <span data-ttu-id="3cff2-215">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3cff2-216">In Global Catalog</span></span>      | <span data-ttu-id="3cff2-217">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3cff2-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cff2-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3cff2-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3cff2-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cff2-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cff2-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-222">Search-Flags</span></span>           | <span data-ttu-id="3cff2-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-224">System-Flags</span></span>           | <span data-ttu-id="3cff2-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-225">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3cff2-226">Classes used in</span></span>        | [<span data-ttu-id="3cff2-227">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="3cff2-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="3cff2-228">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="3cff2-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3cff2-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3cff2-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3cff2-230">進入</span><span class="sxs-lookup"><span data-stu-id="3cff2-230">Entry</span></span> | <span data-ttu-id="3cff2-231">值</span><span class="sxs-lookup"><span data-stu-id="3cff2-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cff2-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3cff2-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cff2-233">MAPI-Id</span></span>                | <span data-ttu-id="3cff2-234">0x8C46</span><span class="sxs-lookup"><span data-stu-id="3cff2-234">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="3cff2-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cff2-235">System-Only</span></span>            | <span data-ttu-id="3cff2-236">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3cff2-237">Is-Single-Valued</span></span>       | <span data-ttu-id="3cff2-238">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3cff2-239">Is Indexed</span></span>             | <span data-ttu-id="3cff2-240">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3cff2-241">In Global Catalog</span></span>      | <span data-ttu-id="3cff2-242">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3cff2-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cff2-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3cff2-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3cff2-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cff2-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cff2-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-247">Search-Flags</span></span>           | <span data-ttu-id="3cff2-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-249">System-Flags</span></span>           | <span data-ttu-id="3cff2-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-250">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3cff2-251">Classes used in</span></span>        | [<span data-ttu-id="3cff2-252">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="3cff2-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="3cff2-253">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="3cff2-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3cff2-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3cff2-254">Windows Server 2012</span></span>



| <span data-ttu-id="3cff2-255">進入</span><span class="sxs-lookup"><span data-stu-id="3cff2-255">Entry</span></span> | <span data-ttu-id="3cff2-256">值</span><span class="sxs-lookup"><span data-stu-id="3cff2-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cff2-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3cff2-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cff2-258">MAPI-Id</span></span>                | <span data-ttu-id="3cff2-259">0x8C46</span><span class="sxs-lookup"><span data-stu-id="3cff2-259">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="3cff2-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cff2-260">System-Only</span></span>            | <span data-ttu-id="3cff2-261">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3cff2-262">Is-Single-Valued</span></span>       | <span data-ttu-id="3cff2-263">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3cff2-264">Is Indexed</span></span>             | <span data-ttu-id="3cff2-265">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3cff2-266">In Global Catalog</span></span>      | <span data-ttu-id="3cff2-267">否</span><span class="sxs-lookup"><span data-stu-id="3cff2-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="3cff2-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3cff2-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cff2-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3cff2-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="3cff2-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cff2-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cff2-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="3cff2-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-272">Search-Flags</span></span>           | <span data-ttu-id="3cff2-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cff2-274">System-Flags</span></span>           | <span data-ttu-id="3cff2-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cff2-275">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="3cff2-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3cff2-276">Classes used in</span></span>        | [<span data-ttu-id="3cff2-277">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="3cff2-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="3cff2-278">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="3cff2-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 






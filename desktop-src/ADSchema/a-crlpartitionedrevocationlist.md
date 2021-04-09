---
title: CRL-資料分割-撤銷清單屬性
description: 公開金鑰基礎結構 \ 8211; 撤銷清單。
ms.assetid: ecee7ee6-21e7-4861-a7f5-5e8e3579978a
ms.tgt_platform: multiple
keywords:
- CRL-資料分割-撤銷清單屬性 AD 架構
- cRLPartitionedRevocationList 屬性 AD 架構
topic_type:
- apiref
api_name:
- CRL-Partitioned-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6c19629cab11e9e6e02069213487135bea4d2aa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845611"
---
# <a name="crl-partitioned-revocation-list-attribute"></a><span data-ttu-id="cd1c0-105">CRL-資料分割-撤銷清單屬性</span><span class="sxs-lookup"><span data-stu-id="cd1c0-105">CRL-Partitioned-Revocation-List attribute</span></span>

<span data-ttu-id="cd1c0-106">公開金鑰基礎結構撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="cd1c0-106">Public Key Infrastructure revocation lists.</span></span>



| <span data-ttu-id="cd1c0-107">進入</span><span class="sxs-lookup"><span data-stu-id="cd1c0-107">Entry</span></span> | <span data-ttu-id="cd1c0-108">值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="cd1c0-109">CN</span><span class="sxs-lookup"><span data-stu-id="cd1c0-109">CN</span></span>                | <span data-ttu-id="cd1c0-110">CRL-資料分割-撤銷清單</span><span class="sxs-lookup"><span data-stu-id="cd1c0-110">CRL-Partitioned-Revocation-List</span></span>                       |
| <span data-ttu-id="cd1c0-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="cd1c0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cd1c0-112">cRLPartitionedRevocationList</span><span class="sxs-lookup"><span data-stu-id="cd1c0-112">cRLPartitionedRevocationList</span></span>                          |
| <span data-ttu-id="cd1c0-113">大小</span><span class="sxs-lookup"><span data-stu-id="cd1c0-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="cd1c0-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="cd1c0-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="cd1c0-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="cd1c0-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="cd1c0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd1c0-116">Attribute-Id</span></span>      | <span data-ttu-id="cd1c0-117">1.2.840.113556.1.4.683</span><span class="sxs-lookup"><span data-stu-id="cd1c0-117">1.2.840.113556.1.4.683</span></span>                                |
| <span data-ttu-id="cd1c0-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="cd1c0-118">System-Id-Guid</span></span>    | <span data-ttu-id="cd1c0-119">963d2731-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="cd1c0-119">963d2731-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="cd1c0-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd1c0-120">Syntax</span></span>            | [<span data-ttu-id="cd1c0-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="cd1c0-122">實作</span><span class="sxs-lookup"><span data-stu-id="cd1c0-122">Implementations</span></span>

-   [<span data-ttu-id="cd1c0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cd1c0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cd1c0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cd1c0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd1c0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd1c0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cd1c0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cd1c0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="cd1c0-130">進入</span><span class="sxs-lookup"><span data-stu-id="cd1c0-130">Entry</span></span> | <span data-ttu-id="cd1c0-131">值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cd1c0-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cd1c0-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1c0-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1c0-134">System-Only</span></span>            | <span data-ttu-id="cd1c0-135">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-135">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-136">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1c0-137">對</span><span class="sxs-lookup"><span data-stu-id="cd1c0-137">True</span></span>                                                                |
| <span data-ttu-id="cd1c0-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cd1c0-138">Is Indexed</span></span>             | <span data-ttu-id="cd1c0-139">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-139">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cd1c0-140">In Global Catalog</span></span>      | <span data-ttu-id="cd1c0-141">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-141">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cd1c0-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1c0-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cd1c0-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cd1c0-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1c0-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1c0-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-146">Search-Flags</span></span>           | <span data-ttu-id="cd1c0-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1c0-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="cd1c0-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-148">System-Flags</span></span>           | <span data-ttu-id="cd1c0-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1c0-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="cd1c0-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cd1c0-150">Classes used in</span></span>        | [<span data-ttu-id="cd1c0-151">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cd1c0-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd1c0-152">Windows Server 2003</span></span>



| <span data-ttu-id="cd1c0-153">進入</span><span class="sxs-lookup"><span data-stu-id="cd1c0-153">Entry</span></span> | <span data-ttu-id="cd1c0-154">值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cd1c0-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cd1c0-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1c0-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1c0-157">System-Only</span></span>            | <span data-ttu-id="cd1c0-158">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-158">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-159">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1c0-160">對</span><span class="sxs-lookup"><span data-stu-id="cd1c0-160">True</span></span>                                                                |
| <span data-ttu-id="cd1c0-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cd1c0-161">Is Indexed</span></span>             | <span data-ttu-id="cd1c0-162">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-162">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cd1c0-163">In Global Catalog</span></span>      | <span data-ttu-id="cd1c0-164">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-164">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cd1c0-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1c0-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cd1c0-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cd1c0-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1c0-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1c0-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-169">Search-Flags</span></span>           | <span data-ttu-id="cd1c0-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1c0-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="cd1c0-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-171">System-Flags</span></span>           | <span data-ttu-id="cd1c0-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1c0-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="cd1c0-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cd1c0-173">Classes used in</span></span>        | [<span data-ttu-id="cd1c0-174">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cd1c0-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cd1c0-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cd1c0-176">進入</span><span class="sxs-lookup"><span data-stu-id="cd1c0-176">Entry</span></span> | <span data-ttu-id="cd1c0-177">值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cd1c0-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cd1c0-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1c0-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1c0-180">System-Only</span></span>            | <span data-ttu-id="cd1c0-181">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-181">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-182">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1c0-183">對</span><span class="sxs-lookup"><span data-stu-id="cd1c0-183">True</span></span>                                                                |
| <span data-ttu-id="cd1c0-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cd1c0-184">Is Indexed</span></span>             | <span data-ttu-id="cd1c0-185">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-185">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cd1c0-186">In Global Catalog</span></span>      | <span data-ttu-id="cd1c0-187">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-187">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cd1c0-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1c0-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cd1c0-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cd1c0-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1c0-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1c0-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-192">Search-Flags</span></span>           | <span data-ttu-id="cd1c0-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1c0-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="cd1c0-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-194">System-Flags</span></span>           | <span data-ttu-id="cd1c0-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1c0-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="cd1c0-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cd1c0-196">Classes used in</span></span>        | [<span data-ttu-id="cd1c0-197">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cd1c0-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd1c0-198">Windows Server 2008</span></span>



| <span data-ttu-id="cd1c0-199">進入</span><span class="sxs-lookup"><span data-stu-id="cd1c0-199">Entry</span></span> | <span data-ttu-id="cd1c0-200">值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cd1c0-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cd1c0-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1c0-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1c0-203">System-Only</span></span>            | <span data-ttu-id="cd1c0-204">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-204">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-205">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1c0-206">對</span><span class="sxs-lookup"><span data-stu-id="cd1c0-206">True</span></span>                                                                |
| <span data-ttu-id="cd1c0-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cd1c0-207">Is Indexed</span></span>             | <span data-ttu-id="cd1c0-208">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-208">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cd1c0-209">In Global Catalog</span></span>      | <span data-ttu-id="cd1c0-210">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-210">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cd1c0-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1c0-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cd1c0-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cd1c0-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1c0-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1c0-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-215">Search-Flags</span></span>           | <span data-ttu-id="cd1c0-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1c0-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="cd1c0-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-217">System-Flags</span></span>           | <span data-ttu-id="cd1c0-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1c0-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="cd1c0-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cd1c0-219">Classes used in</span></span>        | [<span data-ttu-id="cd1c0-220">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd1c0-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd1c0-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd1c0-222">進入</span><span class="sxs-lookup"><span data-stu-id="cd1c0-222">Entry</span></span> | <span data-ttu-id="cd1c0-223">值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cd1c0-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cd1c0-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1c0-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1c0-226">System-Only</span></span>            | <span data-ttu-id="cd1c0-227">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-227">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-228">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1c0-229">對</span><span class="sxs-lookup"><span data-stu-id="cd1c0-229">True</span></span>                                                                |
| <span data-ttu-id="cd1c0-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cd1c0-230">Is Indexed</span></span>             | <span data-ttu-id="cd1c0-231">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-231">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cd1c0-232">In Global Catalog</span></span>      | <span data-ttu-id="cd1c0-233">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-233">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cd1c0-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1c0-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cd1c0-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cd1c0-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1c0-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1c0-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-238">Search-Flags</span></span>           | <span data-ttu-id="cd1c0-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1c0-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="cd1c0-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-240">System-Flags</span></span>           | <span data-ttu-id="cd1c0-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1c0-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="cd1c0-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cd1c0-242">Classes used in</span></span>        | [<span data-ttu-id="cd1c0-243">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd1c0-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd1c0-244">Windows Server 2012</span></span>



| <span data-ttu-id="cd1c0-245">進入</span><span class="sxs-lookup"><span data-stu-id="cd1c0-245">Entry</span></span> | <span data-ttu-id="cd1c0-246">值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cd1c0-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cd1c0-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd1c0-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cd1c0-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd1c0-249">System-Only</span></span>            | <span data-ttu-id="cd1c0-250">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-250">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cd1c0-251">Is-Single-Valued</span></span>       | <span data-ttu-id="cd1c0-252">對</span><span class="sxs-lookup"><span data-stu-id="cd1c0-252">True</span></span>                                                                |
| <span data-ttu-id="cd1c0-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cd1c0-253">Is Indexed</span></span>             | <span data-ttu-id="cd1c0-254">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-254">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cd1c0-255">In Global Catalog</span></span>      | <span data-ttu-id="cd1c0-256">否</span><span class="sxs-lookup"><span data-stu-id="cd1c0-256">False</span></span>                                                               |
| <span data-ttu-id="cd1c0-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cd1c0-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd1c0-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cd1c0-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cd1c0-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd1c0-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd1c0-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cd1c0-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-261">Search-Flags</span></span>           | <span data-ttu-id="cd1c0-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd1c0-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="cd1c0-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd1c0-263">System-Flags</span></span>           | <span data-ttu-id="cd1c0-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd1c0-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="cd1c0-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cd1c0-265">Classes used in</span></span>        | [<span data-ttu-id="cd1c0-266">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="cd1c0-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 






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
# <a name="crl-partitioned-revocation-list-attribute"></a><span data-ttu-id="54e65-105">CRL-資料分割-撤銷清單屬性</span><span class="sxs-lookup"><span data-stu-id="54e65-105">CRL-Partitioned-Revocation-List attribute</span></span>

<span data-ttu-id="54e65-106">公開金鑰基礎結構撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="54e65-106">Public Key Infrastructure revocation lists.</span></span>



| <span data-ttu-id="54e65-107">進入</span><span class="sxs-lookup"><span data-stu-id="54e65-107">Entry</span></span> | <span data-ttu-id="54e65-108">值</span><span class="sxs-lookup"><span data-stu-id="54e65-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="54e65-109">CN</span><span class="sxs-lookup"><span data-stu-id="54e65-109">CN</span></span>                | <span data-ttu-id="54e65-110">CRL-資料分割-撤銷清單</span><span class="sxs-lookup"><span data-stu-id="54e65-110">CRL-Partitioned-Revocation-List</span></span>                       |
| <span data-ttu-id="54e65-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="54e65-111">Ldap-Display-Name</span></span> | <span data-ttu-id="54e65-112">cRLPartitionedRevocationList</span><span class="sxs-lookup"><span data-stu-id="54e65-112">cRLPartitionedRevocationList</span></span>                          |
| <span data-ttu-id="54e65-113">大小</span><span class="sxs-lookup"><span data-stu-id="54e65-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="54e65-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="54e65-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="54e65-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="54e65-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="54e65-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="54e65-116">Attribute-Id</span></span>      | <span data-ttu-id="54e65-117">1.2.840.113556.1.4.683</span><span class="sxs-lookup"><span data-stu-id="54e65-117">1.2.840.113556.1.4.683</span></span>                                |
| <span data-ttu-id="54e65-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="54e65-118">System-Id-Guid</span></span>    | <span data-ttu-id="54e65-119">963d2731-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="54e65-119">963d2731-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="54e65-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="54e65-120">Syntax</span></span>            | [<span data-ttu-id="54e65-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="54e65-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="54e65-122">實作</span><span class="sxs-lookup"><span data-stu-id="54e65-122">Implementations</span></span>

-   [<span data-ttu-id="54e65-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="54e65-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="54e65-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="54e65-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="54e65-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="54e65-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="54e65-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="54e65-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="54e65-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="54e65-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="54e65-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="54e65-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="54e65-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="54e65-129">Windows 2000 Server</span></span>



| <span data-ttu-id="54e65-130">進入</span><span class="sxs-lookup"><span data-stu-id="54e65-130">Entry</span></span> | <span data-ttu-id="54e65-131">值</span><span class="sxs-lookup"><span data-stu-id="54e65-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="54e65-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54e65-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54e65-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="54e65-134">System-Only</span></span>            | <span data-ttu-id="54e65-135">否</span><span class="sxs-lookup"><span data-stu-id="54e65-135">False</span></span>                                                               |
| <span data-ttu-id="54e65-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54e65-136">Is-Single-Valued</span></span>       | <span data-ttu-id="54e65-137">對</span><span class="sxs-lookup"><span data-stu-id="54e65-137">True</span></span>                                                                |
| <span data-ttu-id="54e65-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54e65-138">Is Indexed</span></span>             | <span data-ttu-id="54e65-139">否</span><span class="sxs-lookup"><span data-stu-id="54e65-139">False</span></span>                                                               |
| <span data-ttu-id="54e65-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54e65-140">In Global Catalog</span></span>      | <span data-ttu-id="54e65-141">否</span><span class="sxs-lookup"><span data-stu-id="54e65-141">False</span></span>                                                               |
| <span data-ttu-id="54e65-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54e65-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="54e65-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54e65-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="54e65-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54e65-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54e65-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-146">Search-Flags</span></span>           | <span data-ttu-id="54e65-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54e65-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="54e65-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-148">System-Flags</span></span>           | <span data-ttu-id="54e65-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54e65-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="54e65-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54e65-150">Classes used in</span></span>        | [<span data-ttu-id="54e65-151">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="54e65-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="54e65-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="54e65-152">Windows Server 2003</span></span>



| <span data-ttu-id="54e65-153">進入</span><span class="sxs-lookup"><span data-stu-id="54e65-153">Entry</span></span> | <span data-ttu-id="54e65-154">值</span><span class="sxs-lookup"><span data-stu-id="54e65-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="54e65-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54e65-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54e65-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="54e65-157">System-Only</span></span>            | <span data-ttu-id="54e65-158">否</span><span class="sxs-lookup"><span data-stu-id="54e65-158">False</span></span>                                                               |
| <span data-ttu-id="54e65-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54e65-159">Is-Single-Valued</span></span>       | <span data-ttu-id="54e65-160">對</span><span class="sxs-lookup"><span data-stu-id="54e65-160">True</span></span>                                                                |
| <span data-ttu-id="54e65-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54e65-161">Is Indexed</span></span>             | <span data-ttu-id="54e65-162">否</span><span class="sxs-lookup"><span data-stu-id="54e65-162">False</span></span>                                                               |
| <span data-ttu-id="54e65-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54e65-163">In Global Catalog</span></span>      | <span data-ttu-id="54e65-164">否</span><span class="sxs-lookup"><span data-stu-id="54e65-164">False</span></span>                                                               |
| <span data-ttu-id="54e65-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54e65-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="54e65-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54e65-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="54e65-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54e65-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54e65-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-169">Search-Flags</span></span>           | <span data-ttu-id="54e65-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54e65-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="54e65-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-171">System-Flags</span></span>           | <span data-ttu-id="54e65-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54e65-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="54e65-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54e65-173">Classes used in</span></span>        | [<span data-ttu-id="54e65-174">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="54e65-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="54e65-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="54e65-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="54e65-176">進入</span><span class="sxs-lookup"><span data-stu-id="54e65-176">Entry</span></span> | <span data-ttu-id="54e65-177">值</span><span class="sxs-lookup"><span data-stu-id="54e65-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="54e65-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54e65-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54e65-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="54e65-180">System-Only</span></span>            | <span data-ttu-id="54e65-181">否</span><span class="sxs-lookup"><span data-stu-id="54e65-181">False</span></span>                                                               |
| <span data-ttu-id="54e65-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54e65-182">Is-Single-Valued</span></span>       | <span data-ttu-id="54e65-183">對</span><span class="sxs-lookup"><span data-stu-id="54e65-183">True</span></span>                                                                |
| <span data-ttu-id="54e65-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54e65-184">Is Indexed</span></span>             | <span data-ttu-id="54e65-185">否</span><span class="sxs-lookup"><span data-stu-id="54e65-185">False</span></span>                                                               |
| <span data-ttu-id="54e65-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54e65-186">In Global Catalog</span></span>      | <span data-ttu-id="54e65-187">否</span><span class="sxs-lookup"><span data-stu-id="54e65-187">False</span></span>                                                               |
| <span data-ttu-id="54e65-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54e65-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="54e65-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54e65-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="54e65-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54e65-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54e65-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-192">Search-Flags</span></span>           | <span data-ttu-id="54e65-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54e65-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="54e65-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-194">System-Flags</span></span>           | <span data-ttu-id="54e65-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54e65-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="54e65-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54e65-196">Classes used in</span></span>        | [<span data-ttu-id="54e65-197">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="54e65-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="54e65-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54e65-198">Windows Server 2008</span></span>



| <span data-ttu-id="54e65-199">進入</span><span class="sxs-lookup"><span data-stu-id="54e65-199">Entry</span></span> | <span data-ttu-id="54e65-200">值</span><span class="sxs-lookup"><span data-stu-id="54e65-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="54e65-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54e65-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54e65-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="54e65-203">System-Only</span></span>            | <span data-ttu-id="54e65-204">否</span><span class="sxs-lookup"><span data-stu-id="54e65-204">False</span></span>                                                               |
| <span data-ttu-id="54e65-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54e65-205">Is-Single-Valued</span></span>       | <span data-ttu-id="54e65-206">對</span><span class="sxs-lookup"><span data-stu-id="54e65-206">True</span></span>                                                                |
| <span data-ttu-id="54e65-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54e65-207">Is Indexed</span></span>             | <span data-ttu-id="54e65-208">否</span><span class="sxs-lookup"><span data-stu-id="54e65-208">False</span></span>                                                               |
| <span data-ttu-id="54e65-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54e65-209">In Global Catalog</span></span>      | <span data-ttu-id="54e65-210">否</span><span class="sxs-lookup"><span data-stu-id="54e65-210">False</span></span>                                                               |
| <span data-ttu-id="54e65-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54e65-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="54e65-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54e65-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="54e65-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54e65-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54e65-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-215">Search-Flags</span></span>           | <span data-ttu-id="54e65-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54e65-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="54e65-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-217">System-Flags</span></span>           | <span data-ttu-id="54e65-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54e65-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="54e65-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54e65-219">Classes used in</span></span>        | [<span data-ttu-id="54e65-220">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="54e65-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="54e65-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54e65-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="54e65-222">進入</span><span class="sxs-lookup"><span data-stu-id="54e65-222">Entry</span></span> | <span data-ttu-id="54e65-223">值</span><span class="sxs-lookup"><span data-stu-id="54e65-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="54e65-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54e65-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54e65-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="54e65-226">System-Only</span></span>            | <span data-ttu-id="54e65-227">否</span><span class="sxs-lookup"><span data-stu-id="54e65-227">False</span></span>                                                               |
| <span data-ttu-id="54e65-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54e65-228">Is-Single-Valued</span></span>       | <span data-ttu-id="54e65-229">對</span><span class="sxs-lookup"><span data-stu-id="54e65-229">True</span></span>                                                                |
| <span data-ttu-id="54e65-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54e65-230">Is Indexed</span></span>             | <span data-ttu-id="54e65-231">否</span><span class="sxs-lookup"><span data-stu-id="54e65-231">False</span></span>                                                               |
| <span data-ttu-id="54e65-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54e65-232">In Global Catalog</span></span>      | <span data-ttu-id="54e65-233">否</span><span class="sxs-lookup"><span data-stu-id="54e65-233">False</span></span>                                                               |
| <span data-ttu-id="54e65-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54e65-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="54e65-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54e65-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="54e65-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54e65-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54e65-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-238">Search-Flags</span></span>           | <span data-ttu-id="54e65-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54e65-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="54e65-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-240">System-Flags</span></span>           | <span data-ttu-id="54e65-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54e65-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="54e65-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54e65-242">Classes used in</span></span>        | [<span data-ttu-id="54e65-243">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="54e65-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="54e65-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54e65-244">Windows Server 2012</span></span>



| <span data-ttu-id="54e65-245">進入</span><span class="sxs-lookup"><span data-stu-id="54e65-245">Entry</span></span> | <span data-ttu-id="54e65-246">值</span><span class="sxs-lookup"><span data-stu-id="54e65-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="54e65-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54e65-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54e65-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="54e65-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="54e65-249">System-Only</span></span>            | <span data-ttu-id="54e65-250">否</span><span class="sxs-lookup"><span data-stu-id="54e65-250">False</span></span>                                                               |
| <span data-ttu-id="54e65-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54e65-251">Is-Single-Valued</span></span>       | <span data-ttu-id="54e65-252">對</span><span class="sxs-lookup"><span data-stu-id="54e65-252">True</span></span>                                                                |
| <span data-ttu-id="54e65-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54e65-253">Is Indexed</span></span>             | <span data-ttu-id="54e65-254">否</span><span class="sxs-lookup"><span data-stu-id="54e65-254">False</span></span>                                                               |
| <span data-ttu-id="54e65-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54e65-255">In Global Catalog</span></span>      | <span data-ttu-id="54e65-256">否</span><span class="sxs-lookup"><span data-stu-id="54e65-256">False</span></span>                                                               |
| <span data-ttu-id="54e65-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54e65-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="54e65-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54e65-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="54e65-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54e65-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54e65-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="54e65-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-261">Search-Flags</span></span>           | <span data-ttu-id="54e65-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54e65-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="54e65-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54e65-263">System-Flags</span></span>           | <span data-ttu-id="54e65-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54e65-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="54e65-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54e65-265">Classes used in</span></span>        | [<span data-ttu-id="54e65-266">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="54e65-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 






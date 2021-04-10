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
# <a name="crl-partitioned-revocation-list-attribute"></a><span data-ttu-id="18b27-105">CRL-資料分割-撤銷清單屬性</span><span class="sxs-lookup"><span data-stu-id="18b27-105">CRL-Partitioned-Revocation-List attribute</span></span>

<span data-ttu-id="18b27-106">公開金鑰基礎結構撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="18b27-106">Public Key Infrastructure revocation lists.</span></span>



| <span data-ttu-id="18b27-107">進入</span><span class="sxs-lookup"><span data-stu-id="18b27-107">Entry</span></span> | <span data-ttu-id="18b27-108">值</span><span class="sxs-lookup"><span data-stu-id="18b27-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="18b27-109">CN</span><span class="sxs-lookup"><span data-stu-id="18b27-109">CN</span></span>                | <span data-ttu-id="18b27-110">CRL-資料分割-撤銷清單</span><span class="sxs-lookup"><span data-stu-id="18b27-110">CRL-Partitioned-Revocation-List</span></span>                       |
| <span data-ttu-id="18b27-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="18b27-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18b27-112">cRLPartitionedRevocationList</span><span class="sxs-lookup"><span data-stu-id="18b27-112">cRLPartitionedRevocationList</span></span>                          |
| <span data-ttu-id="18b27-113">大小</span><span class="sxs-lookup"><span data-stu-id="18b27-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="18b27-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="18b27-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="18b27-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="18b27-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="18b27-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18b27-116">Attribute-Id</span></span>      | <span data-ttu-id="18b27-117">1.2.840.113556.1.4.683</span><span class="sxs-lookup"><span data-stu-id="18b27-117">1.2.840.113556.1.4.683</span></span>                                |
| <span data-ttu-id="18b27-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="18b27-118">System-Id-Guid</span></span>    | <span data-ttu-id="18b27-119">963d2731-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="18b27-119">963d2731-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="18b27-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="18b27-120">Syntax</span></span>            | [<span data-ttu-id="18b27-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="18b27-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="18b27-122">實作</span><span class="sxs-lookup"><span data-stu-id="18b27-122">Implementations</span></span>

-   [<span data-ttu-id="18b27-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="18b27-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="18b27-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18b27-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18b27-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18b27-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18b27-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18b27-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18b27-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18b27-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18b27-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18b27-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="18b27-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18b27-129">Windows 2000 Server</span></span>



| <span data-ttu-id="18b27-130">進入</span><span class="sxs-lookup"><span data-stu-id="18b27-130">Entry</span></span> | <span data-ttu-id="18b27-131">值</span><span class="sxs-lookup"><span data-stu-id="18b27-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="18b27-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18b27-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b27-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b27-134">System-Only</span></span>            | <span data-ttu-id="18b27-135">否</span><span class="sxs-lookup"><span data-stu-id="18b27-135">False</span></span>                                                               |
| <span data-ttu-id="18b27-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18b27-136">Is-Single-Valued</span></span>       | <span data-ttu-id="18b27-137">對</span><span class="sxs-lookup"><span data-stu-id="18b27-137">True</span></span>                                                                |
| <span data-ttu-id="18b27-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18b27-138">Is Indexed</span></span>             | <span data-ttu-id="18b27-139">否</span><span class="sxs-lookup"><span data-stu-id="18b27-139">False</span></span>                                                               |
| <span data-ttu-id="18b27-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18b27-140">In Global Catalog</span></span>      | <span data-ttu-id="18b27-141">否</span><span class="sxs-lookup"><span data-stu-id="18b27-141">False</span></span>                                                               |
| <span data-ttu-id="18b27-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18b27-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b27-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18b27-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="18b27-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b27-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b27-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-146">Search-Flags</span></span>           | <span data-ttu-id="18b27-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18b27-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="18b27-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-148">System-Flags</span></span>           | <span data-ttu-id="18b27-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b27-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="18b27-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18b27-150">Classes used in</span></span>        | [<span data-ttu-id="18b27-151">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="18b27-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="18b27-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18b27-152">Windows Server 2003</span></span>



| <span data-ttu-id="18b27-153">進入</span><span class="sxs-lookup"><span data-stu-id="18b27-153">Entry</span></span> | <span data-ttu-id="18b27-154">值</span><span class="sxs-lookup"><span data-stu-id="18b27-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="18b27-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18b27-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b27-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b27-157">System-Only</span></span>            | <span data-ttu-id="18b27-158">否</span><span class="sxs-lookup"><span data-stu-id="18b27-158">False</span></span>                                                               |
| <span data-ttu-id="18b27-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18b27-159">Is-Single-Valued</span></span>       | <span data-ttu-id="18b27-160">對</span><span class="sxs-lookup"><span data-stu-id="18b27-160">True</span></span>                                                                |
| <span data-ttu-id="18b27-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18b27-161">Is Indexed</span></span>             | <span data-ttu-id="18b27-162">否</span><span class="sxs-lookup"><span data-stu-id="18b27-162">False</span></span>                                                               |
| <span data-ttu-id="18b27-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18b27-163">In Global Catalog</span></span>      | <span data-ttu-id="18b27-164">否</span><span class="sxs-lookup"><span data-stu-id="18b27-164">False</span></span>                                                               |
| <span data-ttu-id="18b27-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18b27-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b27-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18b27-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="18b27-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b27-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b27-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-169">Search-Flags</span></span>           | <span data-ttu-id="18b27-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18b27-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="18b27-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-171">System-Flags</span></span>           | <span data-ttu-id="18b27-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b27-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="18b27-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18b27-173">Classes used in</span></span>        | [<span data-ttu-id="18b27-174">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="18b27-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18b27-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18b27-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18b27-176">進入</span><span class="sxs-lookup"><span data-stu-id="18b27-176">Entry</span></span> | <span data-ttu-id="18b27-177">值</span><span class="sxs-lookup"><span data-stu-id="18b27-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="18b27-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18b27-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b27-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b27-180">System-Only</span></span>            | <span data-ttu-id="18b27-181">否</span><span class="sxs-lookup"><span data-stu-id="18b27-181">False</span></span>                                                               |
| <span data-ttu-id="18b27-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18b27-182">Is-Single-Valued</span></span>       | <span data-ttu-id="18b27-183">對</span><span class="sxs-lookup"><span data-stu-id="18b27-183">True</span></span>                                                                |
| <span data-ttu-id="18b27-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18b27-184">Is Indexed</span></span>             | <span data-ttu-id="18b27-185">否</span><span class="sxs-lookup"><span data-stu-id="18b27-185">False</span></span>                                                               |
| <span data-ttu-id="18b27-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18b27-186">In Global Catalog</span></span>      | <span data-ttu-id="18b27-187">否</span><span class="sxs-lookup"><span data-stu-id="18b27-187">False</span></span>                                                               |
| <span data-ttu-id="18b27-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18b27-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b27-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18b27-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="18b27-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b27-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b27-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-192">Search-Flags</span></span>           | <span data-ttu-id="18b27-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18b27-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="18b27-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-194">System-Flags</span></span>           | <span data-ttu-id="18b27-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b27-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="18b27-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18b27-196">Classes used in</span></span>        | [<span data-ttu-id="18b27-197">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="18b27-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18b27-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18b27-198">Windows Server 2008</span></span>



| <span data-ttu-id="18b27-199">進入</span><span class="sxs-lookup"><span data-stu-id="18b27-199">Entry</span></span> | <span data-ttu-id="18b27-200">值</span><span class="sxs-lookup"><span data-stu-id="18b27-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="18b27-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18b27-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b27-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b27-203">System-Only</span></span>            | <span data-ttu-id="18b27-204">否</span><span class="sxs-lookup"><span data-stu-id="18b27-204">False</span></span>                                                               |
| <span data-ttu-id="18b27-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18b27-205">Is-Single-Valued</span></span>       | <span data-ttu-id="18b27-206">對</span><span class="sxs-lookup"><span data-stu-id="18b27-206">True</span></span>                                                                |
| <span data-ttu-id="18b27-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18b27-207">Is Indexed</span></span>             | <span data-ttu-id="18b27-208">否</span><span class="sxs-lookup"><span data-stu-id="18b27-208">False</span></span>                                                               |
| <span data-ttu-id="18b27-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18b27-209">In Global Catalog</span></span>      | <span data-ttu-id="18b27-210">否</span><span class="sxs-lookup"><span data-stu-id="18b27-210">False</span></span>                                                               |
| <span data-ttu-id="18b27-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18b27-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b27-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18b27-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="18b27-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b27-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b27-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-215">Search-Flags</span></span>           | <span data-ttu-id="18b27-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18b27-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="18b27-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-217">System-Flags</span></span>           | <span data-ttu-id="18b27-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b27-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="18b27-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18b27-219">Classes used in</span></span>        | [<span data-ttu-id="18b27-220">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="18b27-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18b27-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18b27-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18b27-222">進入</span><span class="sxs-lookup"><span data-stu-id="18b27-222">Entry</span></span> | <span data-ttu-id="18b27-223">值</span><span class="sxs-lookup"><span data-stu-id="18b27-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="18b27-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18b27-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b27-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b27-226">System-Only</span></span>            | <span data-ttu-id="18b27-227">否</span><span class="sxs-lookup"><span data-stu-id="18b27-227">False</span></span>                                                               |
| <span data-ttu-id="18b27-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18b27-228">Is-Single-Valued</span></span>       | <span data-ttu-id="18b27-229">對</span><span class="sxs-lookup"><span data-stu-id="18b27-229">True</span></span>                                                                |
| <span data-ttu-id="18b27-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18b27-230">Is Indexed</span></span>             | <span data-ttu-id="18b27-231">否</span><span class="sxs-lookup"><span data-stu-id="18b27-231">False</span></span>                                                               |
| <span data-ttu-id="18b27-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18b27-232">In Global Catalog</span></span>      | <span data-ttu-id="18b27-233">否</span><span class="sxs-lookup"><span data-stu-id="18b27-233">False</span></span>                                                               |
| <span data-ttu-id="18b27-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18b27-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b27-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18b27-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="18b27-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b27-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b27-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-238">Search-Flags</span></span>           | <span data-ttu-id="18b27-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18b27-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="18b27-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-240">System-Flags</span></span>           | <span data-ttu-id="18b27-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b27-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="18b27-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18b27-242">Classes used in</span></span>        | [<span data-ttu-id="18b27-243">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="18b27-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18b27-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18b27-244">Windows Server 2012</span></span>



| <span data-ttu-id="18b27-245">進入</span><span class="sxs-lookup"><span data-stu-id="18b27-245">Entry</span></span> | <span data-ttu-id="18b27-246">值</span><span class="sxs-lookup"><span data-stu-id="18b27-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="18b27-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18b27-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b27-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="18b27-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b27-249">System-Only</span></span>            | <span data-ttu-id="18b27-250">否</span><span class="sxs-lookup"><span data-stu-id="18b27-250">False</span></span>                                                               |
| <span data-ttu-id="18b27-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18b27-251">Is-Single-Valued</span></span>       | <span data-ttu-id="18b27-252">對</span><span class="sxs-lookup"><span data-stu-id="18b27-252">True</span></span>                                                                |
| <span data-ttu-id="18b27-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18b27-253">Is Indexed</span></span>             | <span data-ttu-id="18b27-254">否</span><span class="sxs-lookup"><span data-stu-id="18b27-254">False</span></span>                                                               |
| <span data-ttu-id="18b27-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18b27-255">In Global Catalog</span></span>      | <span data-ttu-id="18b27-256">否</span><span class="sxs-lookup"><span data-stu-id="18b27-256">False</span></span>                                                               |
| <span data-ttu-id="18b27-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18b27-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b27-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18b27-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="18b27-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b27-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b27-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="18b27-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-261">Search-Flags</span></span>           | <span data-ttu-id="18b27-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18b27-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="18b27-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b27-263">System-Flags</span></span>           | <span data-ttu-id="18b27-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b27-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="18b27-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18b27-265">Classes used in</span></span>        | [<span data-ttu-id="18b27-266">**CRL-發佈點**</span><span class="sxs-lookup"><span data-stu-id="18b27-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 






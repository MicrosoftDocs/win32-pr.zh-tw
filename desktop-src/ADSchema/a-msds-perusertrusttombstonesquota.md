---
title: 每位使用者-信任----配額屬性
description: 用來在授權根據比對使用者 SID 時，強制刪除 Trusted-Domain 物件的每一使用者配額。
ms.assetid: 4db98754-a2d1-43a4-b9cb-0e3fcbbf3ed9
ms.tgt_platform: multiple
keywords:
- 每位使用者-信任-----配額屬性 AD 架構
- PerUserTrustTombstonesQuota 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Tombstones-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c94bb62b822552a863df99dac83e98462514c42
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106996591"
---
# <a name="ms-ds-per-user-trust-tombstones-quota-attribute"></a><span data-ttu-id="3d804-105">每位使用者-信任----配額屬性</span><span class="sxs-lookup"><span data-stu-id="3d804-105">MS-DS-Per-User-Trust-Tombstones-Quota attribute</span></span>

<span data-ttu-id="3d804-106">用來在授權根據比對使用者 SID 時，強制刪除 Trusted-Domain 物件的每一使用者配額。</span><span class="sxs-lookup"><span data-stu-id="3d804-106">Used to enforce a per-user quota for deleting Trusted-Domain objects when authorization is based on matching the user's SID.</span></span>



| <span data-ttu-id="3d804-107">進入</span><span class="sxs-lookup"><span data-stu-id="3d804-107">Entry</span></span> | <span data-ttu-id="3d804-108">值</span><span class="sxs-lookup"><span data-stu-id="3d804-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="3d804-109">CN</span><span class="sxs-lookup"><span data-stu-id="3d804-109">CN</span></span>                | <span data-ttu-id="3d804-110">每一使用者的 MS DS-信任</span><span class="sxs-lookup"><span data-stu-id="3d804-110">MS-DS-Per-User-Trust-Tombstones-Quota</span></span>     |
| <span data-ttu-id="3d804-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3d804-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3d804-112">PerUserTrustTombstonesQuota</span><span class="sxs-lookup"><span data-stu-id="3d804-112">msDS-PerUserTrustTombstonesQuota</span></span>          |
| <span data-ttu-id="3d804-113">大小</span><span class="sxs-lookup"><span data-stu-id="3d804-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="3d804-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3d804-114">Update Privilege</span></span>  | <span data-ttu-id="3d804-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="3d804-115">Domain administrator</span></span>                      |
| <span data-ttu-id="3d804-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3d804-116">Update Frequency</span></span>  | <span data-ttu-id="3d804-117">在建立樹系時，很少發生。</span><span class="sxs-lookup"><span data-stu-id="3d804-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="3d804-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d804-118">Attribute-Id</span></span>      | <span data-ttu-id="3d804-119">1.2.840.113556.1.4.1790</span><span class="sxs-lookup"><span data-stu-id="3d804-119">1.2.840.113556.1.4.1790</span></span>                   |
| <span data-ttu-id="3d804-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3d804-120">System-Id-Guid</span></span>    | <span data-ttu-id="3d804-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span><span class="sxs-lookup"><span data-stu-id="3d804-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span></span>      |
| <span data-ttu-id="3d804-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d804-122">Syntax</span></span>            | [<span data-ttu-id="3d804-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="3d804-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="3d804-124">實作</span><span class="sxs-lookup"><span data-stu-id="3d804-124">Implementations</span></span>

-   [<span data-ttu-id="3d804-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d804-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d804-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d804-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d804-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d804-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d804-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d804-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d804-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d804-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3d804-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d804-130">Windows Server 2003</span></span>



| <span data-ttu-id="3d804-131">進入</span><span class="sxs-lookup"><span data-stu-id="3d804-131">Entry</span></span> | <span data-ttu-id="3d804-132">值</span><span class="sxs-lookup"><span data-stu-id="3d804-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d804-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d804-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d804-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d804-135">System-Only</span></span>            | <span data-ttu-id="3d804-136">否</span><span class="sxs-lookup"><span data-stu-id="3d804-136">False</span></span>                                        |
| <span data-ttu-id="3d804-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d804-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3d804-138">對</span><span class="sxs-lookup"><span data-stu-id="3d804-138">True</span></span>                                         |
| <span data-ttu-id="3d804-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d804-139">Is Indexed</span></span>             | <span data-ttu-id="3d804-140">否</span><span class="sxs-lookup"><span data-stu-id="3d804-140">False</span></span>                                        |
| <span data-ttu-id="3d804-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d804-141">In Global Catalog</span></span>      | <span data-ttu-id="3d804-142">否</span><span class="sxs-lookup"><span data-stu-id="3d804-142">False</span></span>                                        |
| <span data-ttu-id="3d804-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d804-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d804-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d804-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d804-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d804-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d804-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d804-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d804-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-147">Search-Flags</span></span>           | <span data-ttu-id="3d804-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d804-148">0x00000000</span></span>                                   |
| <span data-ttu-id="3d804-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-149">System-Flags</span></span>           | <span data-ttu-id="3d804-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d804-150">0x00000010</span></span>                                   |
| <span data-ttu-id="3d804-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d804-151">Classes used in</span></span>        | [<span data-ttu-id="3d804-152">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="3d804-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d804-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d804-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d804-154">進入</span><span class="sxs-lookup"><span data-stu-id="3d804-154">Entry</span></span> | <span data-ttu-id="3d804-155">值</span><span class="sxs-lookup"><span data-stu-id="3d804-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d804-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d804-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d804-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d804-158">System-Only</span></span>            | <span data-ttu-id="3d804-159">否</span><span class="sxs-lookup"><span data-stu-id="3d804-159">False</span></span>                                        |
| <span data-ttu-id="3d804-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d804-160">Is-Single-Valued</span></span>       | <span data-ttu-id="3d804-161">對</span><span class="sxs-lookup"><span data-stu-id="3d804-161">True</span></span>                                         |
| <span data-ttu-id="3d804-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d804-162">Is Indexed</span></span>             | <span data-ttu-id="3d804-163">否</span><span class="sxs-lookup"><span data-stu-id="3d804-163">False</span></span>                                        |
| <span data-ttu-id="3d804-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d804-164">In Global Catalog</span></span>      | <span data-ttu-id="3d804-165">否</span><span class="sxs-lookup"><span data-stu-id="3d804-165">False</span></span>                                        |
| <span data-ttu-id="3d804-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d804-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d804-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d804-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d804-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d804-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d804-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d804-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d804-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-170">Search-Flags</span></span>           | <span data-ttu-id="3d804-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d804-171">0x00000000</span></span>                                   |
| <span data-ttu-id="3d804-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-172">System-Flags</span></span>           | <span data-ttu-id="3d804-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d804-173">0x00000010</span></span>                                   |
| <span data-ttu-id="3d804-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d804-174">Classes used in</span></span>        | [<span data-ttu-id="3d804-175">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="3d804-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d804-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d804-176">Windows Server 2008</span></span>



| <span data-ttu-id="3d804-177">進入</span><span class="sxs-lookup"><span data-stu-id="3d804-177">Entry</span></span> | <span data-ttu-id="3d804-178">值</span><span class="sxs-lookup"><span data-stu-id="3d804-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d804-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d804-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d804-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d804-181">System-Only</span></span>            | <span data-ttu-id="3d804-182">否</span><span class="sxs-lookup"><span data-stu-id="3d804-182">False</span></span>                                        |
| <span data-ttu-id="3d804-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d804-183">Is-Single-Valued</span></span>       | <span data-ttu-id="3d804-184">對</span><span class="sxs-lookup"><span data-stu-id="3d804-184">True</span></span>                                         |
| <span data-ttu-id="3d804-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d804-185">Is Indexed</span></span>             | <span data-ttu-id="3d804-186">否</span><span class="sxs-lookup"><span data-stu-id="3d804-186">False</span></span>                                        |
| <span data-ttu-id="3d804-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d804-187">In Global Catalog</span></span>      | <span data-ttu-id="3d804-188">否</span><span class="sxs-lookup"><span data-stu-id="3d804-188">False</span></span>                                        |
| <span data-ttu-id="3d804-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d804-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d804-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d804-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d804-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d804-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d804-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d804-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d804-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-193">Search-Flags</span></span>           | <span data-ttu-id="3d804-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d804-194">0x00000000</span></span>                                   |
| <span data-ttu-id="3d804-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-195">System-Flags</span></span>           | <span data-ttu-id="3d804-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d804-196">0x00000010</span></span>                                   |
| <span data-ttu-id="3d804-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d804-197">Classes used in</span></span>        | [<span data-ttu-id="3d804-198">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="3d804-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d804-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d804-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d804-200">進入</span><span class="sxs-lookup"><span data-stu-id="3d804-200">Entry</span></span> | <span data-ttu-id="3d804-201">值</span><span class="sxs-lookup"><span data-stu-id="3d804-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d804-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d804-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d804-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d804-204">System-Only</span></span>            | <span data-ttu-id="3d804-205">否</span><span class="sxs-lookup"><span data-stu-id="3d804-205">False</span></span>                                        |
| <span data-ttu-id="3d804-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d804-206">Is-Single-Valued</span></span>       | <span data-ttu-id="3d804-207">對</span><span class="sxs-lookup"><span data-stu-id="3d804-207">True</span></span>                                         |
| <span data-ttu-id="3d804-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d804-208">Is Indexed</span></span>             | <span data-ttu-id="3d804-209">否</span><span class="sxs-lookup"><span data-stu-id="3d804-209">False</span></span>                                        |
| <span data-ttu-id="3d804-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d804-210">In Global Catalog</span></span>      | <span data-ttu-id="3d804-211">否</span><span class="sxs-lookup"><span data-stu-id="3d804-211">False</span></span>                                        |
| <span data-ttu-id="3d804-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d804-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d804-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d804-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d804-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d804-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d804-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d804-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d804-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-216">Search-Flags</span></span>           | <span data-ttu-id="3d804-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d804-217">0x00000000</span></span>                                   |
| <span data-ttu-id="3d804-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-218">System-Flags</span></span>           | <span data-ttu-id="3d804-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d804-219">0x00000010</span></span>                                   |
| <span data-ttu-id="3d804-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d804-220">Classes used in</span></span>        | [<span data-ttu-id="3d804-221">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="3d804-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d804-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d804-222">Windows Server 2012</span></span>



| <span data-ttu-id="3d804-223">進入</span><span class="sxs-lookup"><span data-stu-id="3d804-223">Entry</span></span> | <span data-ttu-id="3d804-224">值</span><span class="sxs-lookup"><span data-stu-id="3d804-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d804-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d804-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d804-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d804-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d804-227">System-Only</span></span>            | <span data-ttu-id="3d804-228">否</span><span class="sxs-lookup"><span data-stu-id="3d804-228">False</span></span>                                        |
| <span data-ttu-id="3d804-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d804-229">Is-Single-Valued</span></span>       | <span data-ttu-id="3d804-230">對</span><span class="sxs-lookup"><span data-stu-id="3d804-230">True</span></span>                                         |
| <span data-ttu-id="3d804-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d804-231">Is Indexed</span></span>             | <span data-ttu-id="3d804-232">否</span><span class="sxs-lookup"><span data-stu-id="3d804-232">False</span></span>                                        |
| <span data-ttu-id="3d804-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d804-233">In Global Catalog</span></span>      | <span data-ttu-id="3d804-234">否</span><span class="sxs-lookup"><span data-stu-id="3d804-234">False</span></span>                                        |
| <span data-ttu-id="3d804-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d804-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d804-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d804-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d804-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d804-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d804-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d804-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d804-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-239">Search-Flags</span></span>           | <span data-ttu-id="3d804-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d804-240">0x00000000</span></span>                                   |
| <span data-ttu-id="3d804-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d804-241">System-Flags</span></span>           | <span data-ttu-id="3d804-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d804-242">0x00000010</span></span>                                   |
| <span data-ttu-id="3d804-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d804-243">Classes used in</span></span>        | [<span data-ttu-id="3d804-244">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="3d804-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






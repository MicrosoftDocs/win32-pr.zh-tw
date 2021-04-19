---
title: ms DS 快取-成員資格時間戳記屬性
description: 在權杖評估期間，安全性帳戶管理員會使用以 ms DS 快取的成員資格時間戳記屬性進行群組擴充。
ms.assetid: cb096f79-a57b-4001-b197-e75522904734
ms.tgt_platform: multiple
keywords:
- ms DS-快取-成員資格時間戳記屬性 AD 架構
- 預先快取-成員資格時間戳記屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 403e87288d906587a11f2a140a9f447ce8236aca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972500"
---
# <a name="ms-ds-cached-membership-time-stamp-attribute"></a><span data-ttu-id="ffd4a-105">ms DS 快取-成員資格時間戳記屬性</span><span class="sxs-lookup"><span data-stu-id="ffd4a-105">ms-DS-Cached-Membership-Time-Stamp attribute</span></span>

<span data-ttu-id="ffd4a-106">在權杖評估期間，安全性帳戶管理員會使用以 ms DS 快取的 **成員資格時間戳記** 屬性進行群組擴充。</span><span class="sxs-lookup"><span data-stu-id="ffd4a-106">The **ms-DS-Cached-Membership-Time-Stamp** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="ffd4a-107">進入</span><span class="sxs-lookup"><span data-stu-id="ffd4a-107">Entry</span></span> | <span data-ttu-id="ffd4a-108">值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ffd4a-109">CN</span><span class="sxs-lookup"><span data-stu-id="ffd4a-109">CN</span></span>                | <span data-ttu-id="ffd4a-110">ms DS 快取-成員資格時間戳記</span><span class="sxs-lookup"><span data-stu-id="ffd4a-110">ms-DS-Cached-Membership-Time-Stamp</span></span>   |
| <span data-ttu-id="ffd4a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ffd4a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ffd4a-112">預先快取-成員資格時間戳記</span><span class="sxs-lookup"><span data-stu-id="ffd4a-112">msDS-Cached-Membership-Time-Stamp</span></span>    |
| <span data-ttu-id="ffd4a-113">大小</span><span class="sxs-lookup"><span data-stu-id="ffd4a-113">Size</span></span>              | <span data-ttu-id="ffd4a-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="ffd4a-114">8 bytes</span></span>                              |
| <span data-ttu-id="ffd4a-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ffd4a-115">Update Privilege</span></span>  | <span data-ttu-id="ffd4a-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="ffd4a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="ffd4a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ffd4a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ffd4a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ffd4a-118">Attribute-Id</span></span>      | <span data-ttu-id="ffd4a-119">1.2.840.113556.1.4.1442</span><span class="sxs-lookup"><span data-stu-id="ffd4a-119">1.2.840.113556.1.4.1442</span></span>              |
| <span data-ttu-id="ffd4a-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ffd4a-120">System-Id-Guid</span></span>    | <span data-ttu-id="ffd4a-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span><span class="sxs-lookup"><span data-stu-id="ffd4a-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span></span> |
| <span data-ttu-id="ffd4a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffd4a-122">Syntax</span></span>            | [<span data-ttu-id="ffd4a-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ffd4a-124">實作</span><span class="sxs-lookup"><span data-stu-id="ffd4a-124">Implementations</span></span>

-   [<span data-ttu-id="ffd4a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ffd4a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ffd4a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ffd4a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ffd4a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ffd4a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ffd4a-130">Windows Server 2003</span></span>



| <span data-ttu-id="ffd4a-131">進入</span><span class="sxs-lookup"><span data-stu-id="ffd4a-131">Entry</span></span> | <span data-ttu-id="ffd4a-132">值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ffd4a-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd4a-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd4a-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd4a-135">System-Only</span></span>            | <span data-ttu-id="ffd4a-136">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-136">False</span></span>                             |
| <span data-ttu-id="ffd4a-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd4a-138">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-138">True</span></span>                              |
| <span data-ttu-id="ffd4a-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd4a-139">Is Indexed</span></span>             | <span data-ttu-id="ffd4a-140">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-140">True</span></span>                              |
| <span data-ttu-id="ffd4a-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd4a-141">In Global Catalog</span></span>      | <span data-ttu-id="ffd4a-142">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-142">False</span></span>                             |
| <span data-ttu-id="ffd4a-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd4a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd4a-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd4a-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ffd4a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd4a-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd4a-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-147">Search-Flags</span></span>           | <span data-ttu-id="ffd4a-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffd4a-148">0x00000001</span></span>                        |
| <span data-ttu-id="ffd4a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-149">System-Flags</span></span>           | <span data-ttu-id="ffd4a-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ffd4a-150">0x00000011</span></span>                        |
| <span data-ttu-id="ffd4a-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd4a-151">Classes used in</span></span>        | [<span data-ttu-id="ffd4a-152">**User**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ffd4a-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ffd4a-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ffd4a-154">進入</span><span class="sxs-lookup"><span data-stu-id="ffd4a-154">Entry</span></span> | <span data-ttu-id="ffd4a-155">值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ffd4a-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd4a-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd4a-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd4a-158">System-Only</span></span>            | <span data-ttu-id="ffd4a-159">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-159">False</span></span>                             |
| <span data-ttu-id="ffd4a-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd4a-161">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-161">True</span></span>                              |
| <span data-ttu-id="ffd4a-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd4a-162">Is Indexed</span></span>             | <span data-ttu-id="ffd4a-163">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-163">True</span></span>                              |
| <span data-ttu-id="ffd4a-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd4a-164">In Global Catalog</span></span>      | <span data-ttu-id="ffd4a-165">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-165">False</span></span>                             |
| <span data-ttu-id="ffd4a-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd4a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd4a-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd4a-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ffd4a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd4a-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd4a-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-170">Search-Flags</span></span>           | <span data-ttu-id="ffd4a-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffd4a-171">0x00000001</span></span>                        |
| <span data-ttu-id="ffd4a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-172">System-Flags</span></span>           | <span data-ttu-id="ffd4a-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ffd4a-173">0x00000011</span></span>                        |
| <span data-ttu-id="ffd4a-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd4a-174">Classes used in</span></span>        | [<span data-ttu-id="ffd4a-175">**User**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ffd4a-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffd4a-176">Windows Server 2008</span></span>



| <span data-ttu-id="ffd4a-177">進入</span><span class="sxs-lookup"><span data-stu-id="ffd4a-177">Entry</span></span> | <span data-ttu-id="ffd4a-178">值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ffd4a-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd4a-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd4a-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd4a-181">System-Only</span></span>            | <span data-ttu-id="ffd4a-182">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-182">False</span></span>                             |
| <span data-ttu-id="ffd4a-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd4a-184">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-184">True</span></span>                              |
| <span data-ttu-id="ffd4a-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd4a-185">Is Indexed</span></span>             | <span data-ttu-id="ffd4a-186">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-186">True</span></span>                              |
| <span data-ttu-id="ffd4a-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd4a-187">In Global Catalog</span></span>      | <span data-ttu-id="ffd4a-188">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-188">False</span></span>                             |
| <span data-ttu-id="ffd4a-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd4a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd4a-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd4a-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ffd4a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd4a-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd4a-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-193">Search-Flags</span></span>           | <span data-ttu-id="ffd4a-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffd4a-194">0x00000001</span></span>                        |
| <span data-ttu-id="ffd4a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-195">System-Flags</span></span>           | <span data-ttu-id="ffd4a-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ffd4a-196">0x00000011</span></span>                        |
| <span data-ttu-id="ffd4a-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd4a-197">Classes used in</span></span>        | [<span data-ttu-id="ffd4a-198">**User**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ffd4a-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffd4a-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ffd4a-200">進入</span><span class="sxs-lookup"><span data-stu-id="ffd4a-200">Entry</span></span> | <span data-ttu-id="ffd4a-201">值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ffd4a-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd4a-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd4a-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd4a-204">System-Only</span></span>            | <span data-ttu-id="ffd4a-205">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-205">False</span></span>                             |
| <span data-ttu-id="ffd4a-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd4a-207">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-207">True</span></span>                              |
| <span data-ttu-id="ffd4a-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd4a-208">Is Indexed</span></span>             | <span data-ttu-id="ffd4a-209">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-209">True</span></span>                              |
| <span data-ttu-id="ffd4a-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd4a-210">In Global Catalog</span></span>      | <span data-ttu-id="ffd4a-211">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-211">False</span></span>                             |
| <span data-ttu-id="ffd4a-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd4a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd4a-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd4a-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ffd4a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd4a-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd4a-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-216">Search-Flags</span></span>           | <span data-ttu-id="ffd4a-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffd4a-217">0x00000001</span></span>                        |
| <span data-ttu-id="ffd4a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-218">System-Flags</span></span>           | <span data-ttu-id="ffd4a-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ffd4a-219">0x00000011</span></span>                        |
| <span data-ttu-id="ffd4a-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd4a-220">Classes used in</span></span>        | [<span data-ttu-id="ffd4a-221">**User**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ffd4a-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffd4a-222">Windows Server 2012</span></span>



| <span data-ttu-id="ffd4a-223">進入</span><span class="sxs-lookup"><span data-stu-id="ffd4a-223">Entry</span></span> | <span data-ttu-id="ffd4a-224">值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ffd4a-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd4a-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd4a-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ffd4a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd4a-227">System-Only</span></span>            | <span data-ttu-id="ffd4a-228">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-228">False</span></span>                             |
| <span data-ttu-id="ffd4a-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd4a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd4a-230">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-230">True</span></span>                              |
| <span data-ttu-id="ffd4a-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd4a-231">Is Indexed</span></span>             | <span data-ttu-id="ffd4a-232">對</span><span class="sxs-lookup"><span data-stu-id="ffd4a-232">True</span></span>                              |
| <span data-ttu-id="ffd4a-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd4a-233">In Global Catalog</span></span>      | <span data-ttu-id="ffd4a-234">否</span><span class="sxs-lookup"><span data-stu-id="ffd4a-234">False</span></span>                             |
| <span data-ttu-id="ffd4a-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd4a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd4a-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd4a-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ffd4a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd4a-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd4a-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ffd4a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-239">Search-Flags</span></span>           | <span data-ttu-id="ffd4a-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffd4a-240">0x00000001</span></span>                        |
| <span data-ttu-id="ffd4a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd4a-241">System-Flags</span></span>           | <span data-ttu-id="ffd4a-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ffd4a-242">0x00000011</span></span>                        |
| <span data-ttu-id="ffd4a-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd4a-243">Classes used in</span></span>        | [<span data-ttu-id="ffd4a-244">**User**</span><span class="sxs-lookup"><span data-stu-id="ffd4a-244">**User**</span></span>](c-user.md)<br/> |



 

 






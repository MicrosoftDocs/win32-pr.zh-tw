---
title: ms DS 快取-成員資格屬性
description: 在權杖評估期間，安全性帳戶管理員會使用 ms DS 快取成員資格屬性進行群組擴充。
ms.assetid: e54c5d55-d292-4a6e-942a-3818f5d75301
ms.tgt_platform: multiple
keywords:
- ms DS-快取-成員資格屬性 AD 架構
- 預先快取-成員資格屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936c5c21d33d19ee51dba7f1dec0b03299cee346
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509706"
---
# <a name="ms-ds-cached-membership-attribute"></a><span data-ttu-id="b4452-105">ms DS 快取-成員資格屬性</span><span class="sxs-lookup"><span data-stu-id="b4452-105">ms-DS-Cached-Membership attribute</span></span>

<span data-ttu-id="b4452-106">在權杖評估期間，安全性帳戶管理員會使用 **MS DS 快取成員資格** 屬性進行群組擴充。</span><span class="sxs-lookup"><span data-stu-id="b4452-106">The **ms-DS-Cached-Membership** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="b4452-107">進入</span><span class="sxs-lookup"><span data-stu-id="b4452-107">Entry</span></span> | <span data-ttu-id="b4452-108">值</span><span class="sxs-lookup"><span data-stu-id="b4452-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b4452-109">CN</span><span class="sxs-lookup"><span data-stu-id="b4452-109">CN</span></span>                | <span data-ttu-id="b4452-110">ms DS-快取-成員資格</span><span class="sxs-lookup"><span data-stu-id="b4452-110">ms-DS-Cached-Membership</span></span>                               |
| <span data-ttu-id="b4452-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b4452-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b4452-112">預先快取-成員資格</span><span class="sxs-lookup"><span data-stu-id="b4452-112">msDS-Cached-Membership</span></span>                                |
| <span data-ttu-id="b4452-113">大小</span><span class="sxs-lookup"><span data-stu-id="b4452-113">Size</span></span>              | <span data-ttu-id="b4452-114">最多 3 kb 的二進位 BLOB。</span><span class="sxs-lookup"><span data-stu-id="b4452-114">Binary BLOB of up to 3 kilobytes.</span></span>                     |
| <span data-ttu-id="b4452-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b4452-115">Update Privilege</span></span>  | <span data-ttu-id="b4452-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="b4452-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="b4452-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b4452-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b4452-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4452-118">Attribute-Id</span></span>      | <span data-ttu-id="b4452-119">1.2.840.113556.1.4.1441</span><span class="sxs-lookup"><span data-stu-id="b4452-119">1.2.840.113556.1.4.1441</span></span>                               |
| <span data-ttu-id="b4452-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b4452-120">System-Id-Guid</span></span>    | <span data-ttu-id="b4452-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span><span class="sxs-lookup"><span data-stu-id="b4452-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span></span>                  |
| <span data-ttu-id="b4452-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4452-122">Syntax</span></span>            | [<span data-ttu-id="b4452-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b4452-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b4452-124">實作</span><span class="sxs-lookup"><span data-stu-id="b4452-124">Implementations</span></span>

-   [<span data-ttu-id="b4452-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4452-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4452-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4452-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4452-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4452-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4452-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4452-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4452-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4452-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b4452-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4452-130">Windows Server 2003</span></span>



| <span data-ttu-id="b4452-131">進入</span><span class="sxs-lookup"><span data-stu-id="b4452-131">Entry</span></span> | <span data-ttu-id="b4452-132">值</span><span class="sxs-lookup"><span data-stu-id="b4452-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b4452-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4452-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4452-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4452-135">System-Only</span></span>            | <span data-ttu-id="b4452-136">否</span><span class="sxs-lookup"><span data-stu-id="b4452-136">False</span></span>                             |
| <span data-ttu-id="b4452-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4452-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b4452-138">對</span><span class="sxs-lookup"><span data-stu-id="b4452-138">True</span></span>                              |
| <span data-ttu-id="b4452-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4452-139">Is Indexed</span></span>             | <span data-ttu-id="b4452-140">否</span><span class="sxs-lookup"><span data-stu-id="b4452-140">False</span></span>                             |
| <span data-ttu-id="b4452-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4452-141">In Global Catalog</span></span>      | <span data-ttu-id="b4452-142">否</span><span class="sxs-lookup"><span data-stu-id="b4452-142">False</span></span>                             |
| <span data-ttu-id="b4452-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4452-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4452-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4452-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b4452-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4452-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b4452-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4452-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b4452-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-147">Search-Flags</span></span>           | <span data-ttu-id="b4452-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4452-148">0x00000000</span></span>                        |
| <span data-ttu-id="b4452-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-149">System-Flags</span></span>           | <span data-ttu-id="b4452-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b4452-150">0x00000011</span></span>                        |
| <span data-ttu-id="b4452-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4452-151">Classes used in</span></span>        | [<span data-ttu-id="b4452-152">**User**</span><span class="sxs-lookup"><span data-stu-id="b4452-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4452-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4452-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4452-154">進入</span><span class="sxs-lookup"><span data-stu-id="b4452-154">Entry</span></span> | <span data-ttu-id="b4452-155">值</span><span class="sxs-lookup"><span data-stu-id="b4452-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b4452-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4452-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4452-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4452-158">System-Only</span></span>            | <span data-ttu-id="b4452-159">否</span><span class="sxs-lookup"><span data-stu-id="b4452-159">False</span></span>                             |
| <span data-ttu-id="b4452-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4452-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b4452-161">對</span><span class="sxs-lookup"><span data-stu-id="b4452-161">True</span></span>                              |
| <span data-ttu-id="b4452-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4452-162">Is Indexed</span></span>             | <span data-ttu-id="b4452-163">否</span><span class="sxs-lookup"><span data-stu-id="b4452-163">False</span></span>                             |
| <span data-ttu-id="b4452-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4452-164">In Global Catalog</span></span>      | <span data-ttu-id="b4452-165">否</span><span class="sxs-lookup"><span data-stu-id="b4452-165">False</span></span>                             |
| <span data-ttu-id="b4452-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4452-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4452-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4452-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b4452-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4452-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b4452-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4452-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b4452-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-170">Search-Flags</span></span>           | <span data-ttu-id="b4452-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4452-171">0x00000000</span></span>                        |
| <span data-ttu-id="b4452-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-172">System-Flags</span></span>           | <span data-ttu-id="b4452-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b4452-173">0x00000011</span></span>                        |
| <span data-ttu-id="b4452-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4452-174">Classes used in</span></span>        | [<span data-ttu-id="b4452-175">**User**</span><span class="sxs-lookup"><span data-stu-id="b4452-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4452-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4452-176">Windows Server 2008</span></span>



| <span data-ttu-id="b4452-177">進入</span><span class="sxs-lookup"><span data-stu-id="b4452-177">Entry</span></span> | <span data-ttu-id="b4452-178">值</span><span class="sxs-lookup"><span data-stu-id="b4452-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b4452-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4452-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4452-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4452-181">System-Only</span></span>            | <span data-ttu-id="b4452-182">否</span><span class="sxs-lookup"><span data-stu-id="b4452-182">False</span></span>                             |
| <span data-ttu-id="b4452-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4452-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b4452-184">對</span><span class="sxs-lookup"><span data-stu-id="b4452-184">True</span></span>                              |
| <span data-ttu-id="b4452-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4452-185">Is Indexed</span></span>             | <span data-ttu-id="b4452-186">否</span><span class="sxs-lookup"><span data-stu-id="b4452-186">False</span></span>                             |
| <span data-ttu-id="b4452-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4452-187">In Global Catalog</span></span>      | <span data-ttu-id="b4452-188">否</span><span class="sxs-lookup"><span data-stu-id="b4452-188">False</span></span>                             |
| <span data-ttu-id="b4452-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4452-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4452-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4452-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b4452-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4452-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b4452-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4452-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b4452-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-193">Search-Flags</span></span>           | <span data-ttu-id="b4452-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4452-194">0x00000000</span></span>                        |
| <span data-ttu-id="b4452-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-195">System-Flags</span></span>           | <span data-ttu-id="b4452-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b4452-196">0x00000011</span></span>                        |
| <span data-ttu-id="b4452-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4452-197">Classes used in</span></span>        | [<span data-ttu-id="b4452-198">**User**</span><span class="sxs-lookup"><span data-stu-id="b4452-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4452-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4452-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4452-200">進入</span><span class="sxs-lookup"><span data-stu-id="b4452-200">Entry</span></span> | <span data-ttu-id="b4452-201">值</span><span class="sxs-lookup"><span data-stu-id="b4452-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b4452-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4452-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4452-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4452-204">System-Only</span></span>            | <span data-ttu-id="b4452-205">否</span><span class="sxs-lookup"><span data-stu-id="b4452-205">False</span></span>                             |
| <span data-ttu-id="b4452-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4452-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b4452-207">對</span><span class="sxs-lookup"><span data-stu-id="b4452-207">True</span></span>                              |
| <span data-ttu-id="b4452-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4452-208">Is Indexed</span></span>             | <span data-ttu-id="b4452-209">否</span><span class="sxs-lookup"><span data-stu-id="b4452-209">False</span></span>                             |
| <span data-ttu-id="b4452-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4452-210">In Global Catalog</span></span>      | <span data-ttu-id="b4452-211">否</span><span class="sxs-lookup"><span data-stu-id="b4452-211">False</span></span>                             |
| <span data-ttu-id="b4452-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4452-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4452-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4452-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b4452-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4452-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b4452-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4452-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b4452-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-216">Search-Flags</span></span>           | <span data-ttu-id="b4452-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4452-217">0x00000000</span></span>                        |
| <span data-ttu-id="b4452-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-218">System-Flags</span></span>           | <span data-ttu-id="b4452-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b4452-219">0x00000011</span></span>                        |
| <span data-ttu-id="b4452-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4452-220">Classes used in</span></span>        | [<span data-ttu-id="b4452-221">**User**</span><span class="sxs-lookup"><span data-stu-id="b4452-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4452-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4452-222">Windows Server 2012</span></span>



| <span data-ttu-id="b4452-223">進入</span><span class="sxs-lookup"><span data-stu-id="b4452-223">Entry</span></span> | <span data-ttu-id="b4452-224">值</span><span class="sxs-lookup"><span data-stu-id="b4452-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b4452-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4452-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4452-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b4452-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4452-227">System-Only</span></span>            | <span data-ttu-id="b4452-228">否</span><span class="sxs-lookup"><span data-stu-id="b4452-228">False</span></span>                             |
| <span data-ttu-id="b4452-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4452-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b4452-230">對</span><span class="sxs-lookup"><span data-stu-id="b4452-230">True</span></span>                              |
| <span data-ttu-id="b4452-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4452-231">Is Indexed</span></span>             | <span data-ttu-id="b4452-232">否</span><span class="sxs-lookup"><span data-stu-id="b4452-232">False</span></span>                             |
| <span data-ttu-id="b4452-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4452-233">In Global Catalog</span></span>      | <span data-ttu-id="b4452-234">否</span><span class="sxs-lookup"><span data-stu-id="b4452-234">False</span></span>                             |
| <span data-ttu-id="b4452-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4452-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4452-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4452-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b4452-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4452-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b4452-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4452-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b4452-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-239">Search-Flags</span></span>           | <span data-ttu-id="b4452-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4452-240">0x00000000</span></span>                        |
| <span data-ttu-id="b4452-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4452-241">System-Flags</span></span>           | <span data-ttu-id="b4452-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b4452-242">0x00000011</span></span>                        |
| <span data-ttu-id="b4452-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4452-243">Classes used in</span></span>        | [<span data-ttu-id="b4452-244">**User**</span><span class="sxs-lookup"><span data-stu-id="b4452-244">**User**</span></span>](c-user.md)<br/> |



 

 






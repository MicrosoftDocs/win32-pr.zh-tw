---
title: 每一使用者的 MS-信任配額屬性
description: 用來強制執行每個使用者的配額，以建立新的 control 存取權限所授權的 Trusted-Domain 物件，建立--------------樹系信任。
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- 每一使用者的 MS DS-信任配額屬性 AD 架構
- PerUserTrustQuota 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3bd6ffcac01de8997f806e6aa8a8e3bd6afbb66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970667"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a><span data-ttu-id="7d998-105">每一使用者的 MS-信任配額屬性</span><span class="sxs-lookup"><span data-stu-id="7d998-105">MS-DS-Per-User-Trust-Quota attribute</span></span>

<span data-ttu-id="7d998-106">用來強制執行每個使用者的配額，以建立新的 control 存取權限所授權的 Trusted-Domain 物件，建立--------------樹系信任。</span><span class="sxs-lookup"><span data-stu-id="7d998-106">Used to enforce a per-user quota for creating Trusted-Domain objects that are authorized by the new control access right, Create-Inbound-Forest-Trust.</span></span> <span data-ttu-id="7d998-107">這個屬性會限制單一非系統管理員使用者可以建立的 Trusted-Domain 物件數目。</span><span class="sxs-lookup"><span data-stu-id="7d998-107">This attribute limits the number of Trusted-Domain objects that can be created by a single non-admin user.</span></span>



| <span data-ttu-id="7d998-108">進入</span><span class="sxs-lookup"><span data-stu-id="7d998-108">Entry</span></span> | <span data-ttu-id="7d998-109">值</span><span class="sxs-lookup"><span data-stu-id="7d998-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="7d998-110">CN</span><span class="sxs-lookup"><span data-stu-id="7d998-110">CN</span></span>                | <span data-ttu-id="7d998-111">每一使用者的 MS-信任-配額</span><span class="sxs-lookup"><span data-stu-id="7d998-111">MS-DS-Per-User-Trust-Quota</span></span>                |
| <span data-ttu-id="7d998-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7d998-112">Ldap-Display-Name</span></span> | <span data-ttu-id="7d998-113">PerUserTrustQuota</span><span class="sxs-lookup"><span data-stu-id="7d998-113">msDS-PerUserTrustQuota</span></span>                    |
| <span data-ttu-id="7d998-114">大小</span><span class="sxs-lookup"><span data-stu-id="7d998-114">Size</span></span>              | \-                                        |
| <span data-ttu-id="7d998-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7d998-115">Update Privilege</span></span>  | <span data-ttu-id="7d998-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="7d998-116">Domain administrator</span></span>                      |
| <span data-ttu-id="7d998-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7d998-117">Update Frequency</span></span>  | <span data-ttu-id="7d998-118">在建立樹系時，很少發生。</span><span class="sxs-lookup"><span data-stu-id="7d998-118">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="7d998-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7d998-119">Attribute-Id</span></span>      | <span data-ttu-id="7d998-120">1.2.840.113556.1.4.1788</span><span class="sxs-lookup"><span data-stu-id="7d998-120">1.2.840.113556.1.4.1788</span></span>                   |
| <span data-ttu-id="7d998-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7d998-121">System-Id-Guid</span></span>    | <span data-ttu-id="7d998-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span><span class="sxs-lookup"><span data-stu-id="7d998-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span></span>      |
| <span data-ttu-id="7d998-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d998-123">Syntax</span></span>            | [<span data-ttu-id="7d998-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="7d998-124">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="7d998-125">實作</span><span class="sxs-lookup"><span data-stu-id="7d998-125">Implementations</span></span>

-   [<span data-ttu-id="7d998-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7d998-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7d998-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7d998-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7d998-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7d998-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7d998-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7d998-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7d998-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7d998-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7d998-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7d998-131">Windows Server 2003</span></span>



| <span data-ttu-id="7d998-132">進入</span><span class="sxs-lookup"><span data-stu-id="7d998-132">Entry</span></span> | <span data-ttu-id="7d998-133">值</span><span class="sxs-lookup"><span data-stu-id="7d998-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7d998-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d998-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d998-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d998-136">System-Only</span></span>            | <span data-ttu-id="7d998-137">否</span><span class="sxs-lookup"><span data-stu-id="7d998-137">False</span></span>                                        |
| <span data-ttu-id="7d998-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d998-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7d998-139">對</span><span class="sxs-lookup"><span data-stu-id="7d998-139">True</span></span>                                         |
| <span data-ttu-id="7d998-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d998-140">Is Indexed</span></span>             | <span data-ttu-id="7d998-141">否</span><span class="sxs-lookup"><span data-stu-id="7d998-141">False</span></span>                                        |
| <span data-ttu-id="7d998-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d998-142">In Global Catalog</span></span>      | <span data-ttu-id="7d998-143">否</span><span class="sxs-lookup"><span data-stu-id="7d998-143">False</span></span>                                        |
| <span data-ttu-id="7d998-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d998-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d998-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d998-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7d998-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d998-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7d998-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d998-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7d998-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-148">Search-Flags</span></span>           | <span data-ttu-id="7d998-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d998-149">0x00000000</span></span>                                   |
| <span data-ttu-id="7d998-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-150">System-Flags</span></span>           | <span data-ttu-id="7d998-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d998-151">0x00000010</span></span>                                   |
| <span data-ttu-id="7d998-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d998-152">Classes used in</span></span>        | [<span data-ttu-id="7d998-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7d998-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7d998-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7d998-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7d998-155">進入</span><span class="sxs-lookup"><span data-stu-id="7d998-155">Entry</span></span> | <span data-ttu-id="7d998-156">值</span><span class="sxs-lookup"><span data-stu-id="7d998-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7d998-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d998-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d998-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d998-159">System-Only</span></span>            | <span data-ttu-id="7d998-160">否</span><span class="sxs-lookup"><span data-stu-id="7d998-160">False</span></span>                                        |
| <span data-ttu-id="7d998-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d998-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7d998-162">對</span><span class="sxs-lookup"><span data-stu-id="7d998-162">True</span></span>                                         |
| <span data-ttu-id="7d998-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d998-163">Is Indexed</span></span>             | <span data-ttu-id="7d998-164">否</span><span class="sxs-lookup"><span data-stu-id="7d998-164">False</span></span>                                        |
| <span data-ttu-id="7d998-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d998-165">In Global Catalog</span></span>      | <span data-ttu-id="7d998-166">否</span><span class="sxs-lookup"><span data-stu-id="7d998-166">False</span></span>                                        |
| <span data-ttu-id="7d998-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d998-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d998-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d998-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7d998-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d998-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7d998-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d998-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7d998-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-171">Search-Flags</span></span>           | <span data-ttu-id="7d998-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d998-172">0x00000000</span></span>                                   |
| <span data-ttu-id="7d998-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-173">System-Flags</span></span>           | <span data-ttu-id="7d998-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d998-174">0x00000010</span></span>                                   |
| <span data-ttu-id="7d998-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d998-175">Classes used in</span></span>        | [<span data-ttu-id="7d998-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7d998-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7d998-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d998-177">Windows Server 2008</span></span>



| <span data-ttu-id="7d998-178">進入</span><span class="sxs-lookup"><span data-stu-id="7d998-178">Entry</span></span> | <span data-ttu-id="7d998-179">值</span><span class="sxs-lookup"><span data-stu-id="7d998-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7d998-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d998-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d998-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d998-182">System-Only</span></span>            | <span data-ttu-id="7d998-183">否</span><span class="sxs-lookup"><span data-stu-id="7d998-183">False</span></span>                                        |
| <span data-ttu-id="7d998-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d998-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7d998-185">對</span><span class="sxs-lookup"><span data-stu-id="7d998-185">True</span></span>                                         |
| <span data-ttu-id="7d998-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d998-186">Is Indexed</span></span>             | <span data-ttu-id="7d998-187">否</span><span class="sxs-lookup"><span data-stu-id="7d998-187">False</span></span>                                        |
| <span data-ttu-id="7d998-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d998-188">In Global Catalog</span></span>      | <span data-ttu-id="7d998-189">否</span><span class="sxs-lookup"><span data-stu-id="7d998-189">False</span></span>                                        |
| <span data-ttu-id="7d998-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d998-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d998-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d998-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7d998-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d998-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7d998-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d998-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7d998-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-194">Search-Flags</span></span>           | <span data-ttu-id="7d998-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d998-195">0x00000000</span></span>                                   |
| <span data-ttu-id="7d998-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-196">System-Flags</span></span>           | <span data-ttu-id="7d998-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d998-197">0x00000010</span></span>                                   |
| <span data-ttu-id="7d998-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d998-198">Classes used in</span></span>        | [<span data-ttu-id="7d998-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7d998-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7d998-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d998-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7d998-201">進入</span><span class="sxs-lookup"><span data-stu-id="7d998-201">Entry</span></span> | <span data-ttu-id="7d998-202">值</span><span class="sxs-lookup"><span data-stu-id="7d998-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7d998-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d998-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d998-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d998-205">System-Only</span></span>            | <span data-ttu-id="7d998-206">否</span><span class="sxs-lookup"><span data-stu-id="7d998-206">False</span></span>                                        |
| <span data-ttu-id="7d998-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d998-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7d998-208">對</span><span class="sxs-lookup"><span data-stu-id="7d998-208">True</span></span>                                         |
| <span data-ttu-id="7d998-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d998-209">Is Indexed</span></span>             | <span data-ttu-id="7d998-210">否</span><span class="sxs-lookup"><span data-stu-id="7d998-210">False</span></span>                                        |
| <span data-ttu-id="7d998-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d998-211">In Global Catalog</span></span>      | <span data-ttu-id="7d998-212">否</span><span class="sxs-lookup"><span data-stu-id="7d998-212">False</span></span>                                        |
| <span data-ttu-id="7d998-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d998-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d998-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d998-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7d998-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d998-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7d998-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d998-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7d998-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-217">Search-Flags</span></span>           | <span data-ttu-id="7d998-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d998-218">0x00000000</span></span>                                   |
| <span data-ttu-id="7d998-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-219">System-Flags</span></span>           | <span data-ttu-id="7d998-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d998-220">0x00000010</span></span>                                   |
| <span data-ttu-id="7d998-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d998-221">Classes used in</span></span>        | [<span data-ttu-id="7d998-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7d998-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7d998-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d998-223">Windows Server 2012</span></span>



| <span data-ttu-id="7d998-224">進入</span><span class="sxs-lookup"><span data-stu-id="7d998-224">Entry</span></span> | <span data-ttu-id="7d998-225">值</span><span class="sxs-lookup"><span data-stu-id="7d998-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7d998-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d998-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d998-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7d998-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d998-228">System-Only</span></span>            | <span data-ttu-id="7d998-229">否</span><span class="sxs-lookup"><span data-stu-id="7d998-229">False</span></span>                                        |
| <span data-ttu-id="7d998-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d998-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7d998-231">對</span><span class="sxs-lookup"><span data-stu-id="7d998-231">True</span></span>                                         |
| <span data-ttu-id="7d998-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d998-232">Is Indexed</span></span>             | <span data-ttu-id="7d998-233">否</span><span class="sxs-lookup"><span data-stu-id="7d998-233">False</span></span>                                        |
| <span data-ttu-id="7d998-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d998-234">In Global Catalog</span></span>      | <span data-ttu-id="7d998-235">否</span><span class="sxs-lookup"><span data-stu-id="7d998-235">False</span></span>                                        |
| <span data-ttu-id="7d998-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d998-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d998-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d998-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7d998-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d998-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7d998-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d998-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7d998-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-240">Search-Flags</span></span>           | <span data-ttu-id="7d998-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d998-241">0x00000000</span></span>                                   |
| <span data-ttu-id="7d998-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d998-242">System-Flags</span></span>           | <span data-ttu-id="7d998-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d998-243">0x00000010</span></span>                                   |
| <span data-ttu-id="7d998-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d998-244">Classes used in</span></span>        | [<span data-ttu-id="7d998-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="7d998-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






---
title: MS DS-所有使用者-信任-配額屬性
description: 用來強制合併的使用者使用新的 control 存取權限建立的 Trusted-Domain 物件總數，建立-------------------樹系信任。
ms.assetid: 77e70a26-99b4-4b49-a984-6809d02f6fb8
ms.tgt_platform: multiple
keywords:
- MS DS-所有使用者-信任-配額屬性 AD 架構
- AllUsersTrustQuota 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-All-Users-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0538ff38f1eb57f339a8e0e244a378a36dd92498
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687271"
---
# <a name="ms-ds-all-users-trust-quota-attribute"></a><span data-ttu-id="090b9-105">MS DS-所有使用者-信任-配額屬性</span><span class="sxs-lookup"><span data-stu-id="090b9-105">MS-DS-All-Users-Trust-Quota attribute</span></span>

<span data-ttu-id="090b9-106">用來強制合併的使用者使用新的 control 存取權限建立的 Trusted-Domain 物件總數，建立-------------------樹系信任。</span><span class="sxs-lookup"><span data-stu-id="090b9-106">Used to enforce a combined users quota on the total number of Trusted-Domain objects created by using the new control access right, Create-Inbound-Forest-Trust.</span></span>



| <span data-ttu-id="090b9-107">進入</span><span class="sxs-lookup"><span data-stu-id="090b9-107">Entry</span></span> | <span data-ttu-id="090b9-108">值</span><span class="sxs-lookup"><span data-stu-id="090b9-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="090b9-109">CN</span><span class="sxs-lookup"><span data-stu-id="090b9-109">CN</span></span>                | <span data-ttu-id="090b9-110">MS-DS-所有使用者-信任-配額</span><span class="sxs-lookup"><span data-stu-id="090b9-110">MS-DS-All-Users-Trust-Quota</span></span>               |
| <span data-ttu-id="090b9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="090b9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="090b9-112">AllUsersTrustQuota</span><span class="sxs-lookup"><span data-stu-id="090b9-112">msDS-AllUsersTrustQuota</span></span>                   |
| <span data-ttu-id="090b9-113">大小</span><span class="sxs-lookup"><span data-stu-id="090b9-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="090b9-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="090b9-114">Update Privilege</span></span>  | <span data-ttu-id="090b9-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="090b9-115">Domain administrator</span></span>                      |
| <span data-ttu-id="090b9-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="090b9-116">Update Frequency</span></span>  | <span data-ttu-id="090b9-117">在建立樹系時，很少發生。</span><span class="sxs-lookup"><span data-stu-id="090b9-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="090b9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="090b9-118">Attribute-Id</span></span>      | <span data-ttu-id="090b9-119">1.2.840.113556.1.4.1789</span><span class="sxs-lookup"><span data-stu-id="090b9-119">1.2.840.113556.1.4.1789</span></span>                   |
| <span data-ttu-id="090b9-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="090b9-120">System-Id-Guid</span></span>    | <span data-ttu-id="090b9-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span><span class="sxs-lookup"><span data-stu-id="090b9-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span></span>      |
| <span data-ttu-id="090b9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="090b9-122">Syntax</span></span>            | [<span data-ttu-id="090b9-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="090b9-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="090b9-124">實作</span><span class="sxs-lookup"><span data-stu-id="090b9-124">Implementations</span></span>

-   [<span data-ttu-id="090b9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="090b9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="090b9-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="090b9-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="090b9-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="090b9-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="090b9-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="090b9-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="090b9-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="090b9-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="090b9-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="090b9-130">Windows Server 2003</span></span>



| <span data-ttu-id="090b9-131">進入</span><span class="sxs-lookup"><span data-stu-id="090b9-131">Entry</span></span> | <span data-ttu-id="090b9-132">值</span><span class="sxs-lookup"><span data-stu-id="090b9-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="090b9-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="090b9-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="090b9-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="090b9-135">System-Only</span></span>            | <span data-ttu-id="090b9-136">否</span><span class="sxs-lookup"><span data-stu-id="090b9-136">False</span></span>                                        |
| <span data-ttu-id="090b9-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="090b9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="090b9-138">對</span><span class="sxs-lookup"><span data-stu-id="090b9-138">True</span></span>                                         |
| <span data-ttu-id="090b9-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="090b9-139">Is Indexed</span></span>             | <span data-ttu-id="090b9-140">否</span><span class="sxs-lookup"><span data-stu-id="090b9-140">False</span></span>                                        |
| <span data-ttu-id="090b9-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="090b9-141">In Global Catalog</span></span>      | <span data-ttu-id="090b9-142">否</span><span class="sxs-lookup"><span data-stu-id="090b9-142">False</span></span>                                        |
| <span data-ttu-id="090b9-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="090b9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="090b9-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="090b9-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="090b9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="090b9-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="090b9-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="090b9-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="090b9-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-147">Search-Flags</span></span>           | <span data-ttu-id="090b9-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="090b9-148">0x00000000</span></span>                                   |
| <span data-ttu-id="090b9-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-149">System-Flags</span></span>           | <span data-ttu-id="090b9-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="090b9-150">0x00000010</span></span>                                   |
| <span data-ttu-id="090b9-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="090b9-151">Classes used in</span></span>        | [<span data-ttu-id="090b9-152">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="090b9-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="090b9-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="090b9-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="090b9-154">進入</span><span class="sxs-lookup"><span data-stu-id="090b9-154">Entry</span></span> | <span data-ttu-id="090b9-155">值</span><span class="sxs-lookup"><span data-stu-id="090b9-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="090b9-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="090b9-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="090b9-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="090b9-158">System-Only</span></span>            | <span data-ttu-id="090b9-159">否</span><span class="sxs-lookup"><span data-stu-id="090b9-159">False</span></span>                                        |
| <span data-ttu-id="090b9-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="090b9-160">Is-Single-Valued</span></span>       | <span data-ttu-id="090b9-161">對</span><span class="sxs-lookup"><span data-stu-id="090b9-161">True</span></span>                                         |
| <span data-ttu-id="090b9-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="090b9-162">Is Indexed</span></span>             | <span data-ttu-id="090b9-163">否</span><span class="sxs-lookup"><span data-stu-id="090b9-163">False</span></span>                                        |
| <span data-ttu-id="090b9-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="090b9-164">In Global Catalog</span></span>      | <span data-ttu-id="090b9-165">否</span><span class="sxs-lookup"><span data-stu-id="090b9-165">False</span></span>                                        |
| <span data-ttu-id="090b9-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="090b9-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="090b9-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="090b9-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="090b9-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="090b9-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="090b9-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="090b9-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="090b9-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-170">Search-Flags</span></span>           | <span data-ttu-id="090b9-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="090b9-171">0x00000000</span></span>                                   |
| <span data-ttu-id="090b9-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-172">System-Flags</span></span>           | <span data-ttu-id="090b9-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="090b9-173">0x00000010</span></span>                                   |
| <span data-ttu-id="090b9-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="090b9-174">Classes used in</span></span>        | [<span data-ttu-id="090b9-175">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="090b9-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="090b9-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="090b9-176">Windows Server 2008</span></span>



| <span data-ttu-id="090b9-177">進入</span><span class="sxs-lookup"><span data-stu-id="090b9-177">Entry</span></span> | <span data-ttu-id="090b9-178">值</span><span class="sxs-lookup"><span data-stu-id="090b9-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="090b9-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="090b9-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="090b9-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="090b9-181">System-Only</span></span>            | <span data-ttu-id="090b9-182">否</span><span class="sxs-lookup"><span data-stu-id="090b9-182">False</span></span>                                        |
| <span data-ttu-id="090b9-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="090b9-183">Is-Single-Valued</span></span>       | <span data-ttu-id="090b9-184">對</span><span class="sxs-lookup"><span data-stu-id="090b9-184">True</span></span>                                         |
| <span data-ttu-id="090b9-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="090b9-185">Is Indexed</span></span>             | <span data-ttu-id="090b9-186">否</span><span class="sxs-lookup"><span data-stu-id="090b9-186">False</span></span>                                        |
| <span data-ttu-id="090b9-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="090b9-187">In Global Catalog</span></span>      | <span data-ttu-id="090b9-188">否</span><span class="sxs-lookup"><span data-stu-id="090b9-188">False</span></span>                                        |
| <span data-ttu-id="090b9-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="090b9-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="090b9-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="090b9-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="090b9-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="090b9-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="090b9-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="090b9-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="090b9-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-193">Search-Flags</span></span>           | <span data-ttu-id="090b9-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="090b9-194">0x00000000</span></span>                                   |
| <span data-ttu-id="090b9-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-195">System-Flags</span></span>           | <span data-ttu-id="090b9-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="090b9-196">0x00000010</span></span>                                   |
| <span data-ttu-id="090b9-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="090b9-197">Classes used in</span></span>        | [<span data-ttu-id="090b9-198">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="090b9-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="090b9-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="090b9-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="090b9-200">進入</span><span class="sxs-lookup"><span data-stu-id="090b9-200">Entry</span></span> | <span data-ttu-id="090b9-201">值</span><span class="sxs-lookup"><span data-stu-id="090b9-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="090b9-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="090b9-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="090b9-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="090b9-204">System-Only</span></span>            | <span data-ttu-id="090b9-205">否</span><span class="sxs-lookup"><span data-stu-id="090b9-205">False</span></span>                                        |
| <span data-ttu-id="090b9-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="090b9-206">Is-Single-Valued</span></span>       | <span data-ttu-id="090b9-207">對</span><span class="sxs-lookup"><span data-stu-id="090b9-207">True</span></span>                                         |
| <span data-ttu-id="090b9-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="090b9-208">Is Indexed</span></span>             | <span data-ttu-id="090b9-209">否</span><span class="sxs-lookup"><span data-stu-id="090b9-209">False</span></span>                                        |
| <span data-ttu-id="090b9-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="090b9-210">In Global Catalog</span></span>      | <span data-ttu-id="090b9-211">否</span><span class="sxs-lookup"><span data-stu-id="090b9-211">False</span></span>                                        |
| <span data-ttu-id="090b9-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="090b9-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="090b9-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="090b9-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="090b9-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="090b9-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="090b9-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="090b9-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="090b9-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-216">Search-Flags</span></span>           | <span data-ttu-id="090b9-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="090b9-217">0x00000000</span></span>                                   |
| <span data-ttu-id="090b9-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-218">System-Flags</span></span>           | <span data-ttu-id="090b9-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="090b9-219">0x00000010</span></span>                                   |
| <span data-ttu-id="090b9-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="090b9-220">Classes used in</span></span>        | [<span data-ttu-id="090b9-221">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="090b9-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="090b9-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="090b9-222">Windows Server 2012</span></span>



| <span data-ttu-id="090b9-223">進入</span><span class="sxs-lookup"><span data-stu-id="090b9-223">Entry</span></span> | <span data-ttu-id="090b9-224">值</span><span class="sxs-lookup"><span data-stu-id="090b9-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="090b9-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="090b9-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="090b9-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="090b9-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="090b9-227">System-Only</span></span>            | <span data-ttu-id="090b9-228">否</span><span class="sxs-lookup"><span data-stu-id="090b9-228">False</span></span>                                        |
| <span data-ttu-id="090b9-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="090b9-229">Is-Single-Valued</span></span>       | <span data-ttu-id="090b9-230">對</span><span class="sxs-lookup"><span data-stu-id="090b9-230">True</span></span>                                         |
| <span data-ttu-id="090b9-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="090b9-231">Is Indexed</span></span>             | <span data-ttu-id="090b9-232">否</span><span class="sxs-lookup"><span data-stu-id="090b9-232">False</span></span>                                        |
| <span data-ttu-id="090b9-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="090b9-233">In Global Catalog</span></span>      | <span data-ttu-id="090b9-234">否</span><span class="sxs-lookup"><span data-stu-id="090b9-234">False</span></span>                                        |
| <span data-ttu-id="090b9-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="090b9-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="090b9-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="090b9-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="090b9-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="090b9-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="090b9-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="090b9-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="090b9-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-239">Search-Flags</span></span>           | <span data-ttu-id="090b9-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="090b9-240">0x00000000</span></span>                                   |
| <span data-ttu-id="090b9-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="090b9-241">System-Flags</span></span>           | <span data-ttu-id="090b9-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="090b9-242">0x00000010</span></span>                                   |
| <span data-ttu-id="090b9-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="090b9-243">Classes used in</span></span>        | [<span data-ttu-id="090b9-244">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="090b9-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






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
# <a name="ms-ds-all-users-trust-quota-attribute"></a><span data-ttu-id="78b88-105">MS DS-所有使用者-信任-配額屬性</span><span class="sxs-lookup"><span data-stu-id="78b88-105">MS-DS-All-Users-Trust-Quota attribute</span></span>

<span data-ttu-id="78b88-106">用來強制合併的使用者使用新的 control 存取權限建立的 Trusted-Domain 物件總數，建立-------------------樹系信任。</span><span class="sxs-lookup"><span data-stu-id="78b88-106">Used to enforce a combined users quota on the total number of Trusted-Domain objects created by using the new control access right, Create-Inbound-Forest-Trust.</span></span>



| <span data-ttu-id="78b88-107">進入</span><span class="sxs-lookup"><span data-stu-id="78b88-107">Entry</span></span> | <span data-ttu-id="78b88-108">值</span><span class="sxs-lookup"><span data-stu-id="78b88-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="78b88-109">CN</span><span class="sxs-lookup"><span data-stu-id="78b88-109">CN</span></span>                | <span data-ttu-id="78b88-110">MS-DS-所有使用者-信任-配額</span><span class="sxs-lookup"><span data-stu-id="78b88-110">MS-DS-All-Users-Trust-Quota</span></span>               |
| <span data-ttu-id="78b88-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="78b88-111">Ldap-Display-Name</span></span> | <span data-ttu-id="78b88-112">AllUsersTrustQuota</span><span class="sxs-lookup"><span data-stu-id="78b88-112">msDS-AllUsersTrustQuota</span></span>                   |
| <span data-ttu-id="78b88-113">大小</span><span class="sxs-lookup"><span data-stu-id="78b88-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="78b88-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="78b88-114">Update Privilege</span></span>  | <span data-ttu-id="78b88-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="78b88-115">Domain administrator</span></span>                      |
| <span data-ttu-id="78b88-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="78b88-116">Update Frequency</span></span>  | <span data-ttu-id="78b88-117">在建立樹系時，很少發生。</span><span class="sxs-lookup"><span data-stu-id="78b88-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="78b88-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78b88-118">Attribute-Id</span></span>      | <span data-ttu-id="78b88-119">1.2.840.113556.1.4.1789</span><span class="sxs-lookup"><span data-stu-id="78b88-119">1.2.840.113556.1.4.1789</span></span>                   |
| <span data-ttu-id="78b88-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="78b88-120">System-Id-Guid</span></span>    | <span data-ttu-id="78b88-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span><span class="sxs-lookup"><span data-stu-id="78b88-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span></span>      |
| <span data-ttu-id="78b88-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="78b88-122">Syntax</span></span>            | [<span data-ttu-id="78b88-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="78b88-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="78b88-124">實作</span><span class="sxs-lookup"><span data-stu-id="78b88-124">Implementations</span></span>

-   [<span data-ttu-id="78b88-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78b88-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78b88-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78b88-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78b88-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78b88-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78b88-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78b88-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78b88-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78b88-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="78b88-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78b88-130">Windows Server 2003</span></span>



| <span data-ttu-id="78b88-131">進入</span><span class="sxs-lookup"><span data-stu-id="78b88-131">Entry</span></span> | <span data-ttu-id="78b88-132">值</span><span class="sxs-lookup"><span data-stu-id="78b88-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="78b88-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b88-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b88-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b88-135">System-Only</span></span>            | <span data-ttu-id="78b88-136">否</span><span class="sxs-lookup"><span data-stu-id="78b88-136">False</span></span>                                        |
| <span data-ttu-id="78b88-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b88-137">Is-Single-Valued</span></span>       | <span data-ttu-id="78b88-138">對</span><span class="sxs-lookup"><span data-stu-id="78b88-138">True</span></span>                                         |
| <span data-ttu-id="78b88-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b88-139">Is Indexed</span></span>             | <span data-ttu-id="78b88-140">否</span><span class="sxs-lookup"><span data-stu-id="78b88-140">False</span></span>                                        |
| <span data-ttu-id="78b88-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b88-141">In Global Catalog</span></span>      | <span data-ttu-id="78b88-142">否</span><span class="sxs-lookup"><span data-stu-id="78b88-142">False</span></span>                                        |
| <span data-ttu-id="78b88-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b88-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b88-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b88-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="78b88-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b88-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="78b88-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b88-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="78b88-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-147">Search-Flags</span></span>           | <span data-ttu-id="78b88-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b88-148">0x00000000</span></span>                                   |
| <span data-ttu-id="78b88-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-149">System-Flags</span></span>           | <span data-ttu-id="78b88-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b88-150">0x00000010</span></span>                                   |
| <span data-ttu-id="78b88-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b88-151">Classes used in</span></span>        | [<span data-ttu-id="78b88-152">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="78b88-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78b88-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78b88-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78b88-154">進入</span><span class="sxs-lookup"><span data-stu-id="78b88-154">Entry</span></span> | <span data-ttu-id="78b88-155">值</span><span class="sxs-lookup"><span data-stu-id="78b88-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="78b88-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b88-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b88-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b88-158">System-Only</span></span>            | <span data-ttu-id="78b88-159">否</span><span class="sxs-lookup"><span data-stu-id="78b88-159">False</span></span>                                        |
| <span data-ttu-id="78b88-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b88-160">Is-Single-Valued</span></span>       | <span data-ttu-id="78b88-161">對</span><span class="sxs-lookup"><span data-stu-id="78b88-161">True</span></span>                                         |
| <span data-ttu-id="78b88-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b88-162">Is Indexed</span></span>             | <span data-ttu-id="78b88-163">否</span><span class="sxs-lookup"><span data-stu-id="78b88-163">False</span></span>                                        |
| <span data-ttu-id="78b88-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b88-164">In Global Catalog</span></span>      | <span data-ttu-id="78b88-165">否</span><span class="sxs-lookup"><span data-stu-id="78b88-165">False</span></span>                                        |
| <span data-ttu-id="78b88-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b88-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b88-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b88-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="78b88-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b88-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="78b88-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b88-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="78b88-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-170">Search-Flags</span></span>           | <span data-ttu-id="78b88-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b88-171">0x00000000</span></span>                                   |
| <span data-ttu-id="78b88-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-172">System-Flags</span></span>           | <span data-ttu-id="78b88-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b88-173">0x00000010</span></span>                                   |
| <span data-ttu-id="78b88-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b88-174">Classes used in</span></span>        | [<span data-ttu-id="78b88-175">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="78b88-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78b88-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78b88-176">Windows Server 2008</span></span>



| <span data-ttu-id="78b88-177">進入</span><span class="sxs-lookup"><span data-stu-id="78b88-177">Entry</span></span> | <span data-ttu-id="78b88-178">值</span><span class="sxs-lookup"><span data-stu-id="78b88-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="78b88-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b88-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b88-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b88-181">System-Only</span></span>            | <span data-ttu-id="78b88-182">否</span><span class="sxs-lookup"><span data-stu-id="78b88-182">False</span></span>                                        |
| <span data-ttu-id="78b88-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b88-183">Is-Single-Valued</span></span>       | <span data-ttu-id="78b88-184">對</span><span class="sxs-lookup"><span data-stu-id="78b88-184">True</span></span>                                         |
| <span data-ttu-id="78b88-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b88-185">Is Indexed</span></span>             | <span data-ttu-id="78b88-186">否</span><span class="sxs-lookup"><span data-stu-id="78b88-186">False</span></span>                                        |
| <span data-ttu-id="78b88-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b88-187">In Global Catalog</span></span>      | <span data-ttu-id="78b88-188">否</span><span class="sxs-lookup"><span data-stu-id="78b88-188">False</span></span>                                        |
| <span data-ttu-id="78b88-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b88-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b88-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b88-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="78b88-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b88-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="78b88-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b88-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="78b88-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-193">Search-Flags</span></span>           | <span data-ttu-id="78b88-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b88-194">0x00000000</span></span>                                   |
| <span data-ttu-id="78b88-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-195">System-Flags</span></span>           | <span data-ttu-id="78b88-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b88-196">0x00000010</span></span>                                   |
| <span data-ttu-id="78b88-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b88-197">Classes used in</span></span>        | [<span data-ttu-id="78b88-198">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="78b88-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78b88-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78b88-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78b88-200">進入</span><span class="sxs-lookup"><span data-stu-id="78b88-200">Entry</span></span> | <span data-ttu-id="78b88-201">值</span><span class="sxs-lookup"><span data-stu-id="78b88-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="78b88-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b88-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b88-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b88-204">System-Only</span></span>            | <span data-ttu-id="78b88-205">否</span><span class="sxs-lookup"><span data-stu-id="78b88-205">False</span></span>                                        |
| <span data-ttu-id="78b88-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b88-206">Is-Single-Valued</span></span>       | <span data-ttu-id="78b88-207">對</span><span class="sxs-lookup"><span data-stu-id="78b88-207">True</span></span>                                         |
| <span data-ttu-id="78b88-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b88-208">Is Indexed</span></span>             | <span data-ttu-id="78b88-209">否</span><span class="sxs-lookup"><span data-stu-id="78b88-209">False</span></span>                                        |
| <span data-ttu-id="78b88-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b88-210">In Global Catalog</span></span>      | <span data-ttu-id="78b88-211">否</span><span class="sxs-lookup"><span data-stu-id="78b88-211">False</span></span>                                        |
| <span data-ttu-id="78b88-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b88-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b88-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b88-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="78b88-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b88-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="78b88-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b88-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="78b88-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-216">Search-Flags</span></span>           | <span data-ttu-id="78b88-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b88-217">0x00000000</span></span>                                   |
| <span data-ttu-id="78b88-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-218">System-Flags</span></span>           | <span data-ttu-id="78b88-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b88-219">0x00000010</span></span>                                   |
| <span data-ttu-id="78b88-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b88-220">Classes used in</span></span>        | [<span data-ttu-id="78b88-221">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="78b88-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78b88-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78b88-222">Windows Server 2012</span></span>



| <span data-ttu-id="78b88-223">進入</span><span class="sxs-lookup"><span data-stu-id="78b88-223">Entry</span></span> | <span data-ttu-id="78b88-224">值</span><span class="sxs-lookup"><span data-stu-id="78b88-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="78b88-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b88-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b88-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="78b88-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b88-227">System-Only</span></span>            | <span data-ttu-id="78b88-228">否</span><span class="sxs-lookup"><span data-stu-id="78b88-228">False</span></span>                                        |
| <span data-ttu-id="78b88-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b88-229">Is-Single-Valued</span></span>       | <span data-ttu-id="78b88-230">對</span><span class="sxs-lookup"><span data-stu-id="78b88-230">True</span></span>                                         |
| <span data-ttu-id="78b88-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b88-231">Is Indexed</span></span>             | <span data-ttu-id="78b88-232">否</span><span class="sxs-lookup"><span data-stu-id="78b88-232">False</span></span>                                        |
| <span data-ttu-id="78b88-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b88-233">In Global Catalog</span></span>      | <span data-ttu-id="78b88-234">否</span><span class="sxs-lookup"><span data-stu-id="78b88-234">False</span></span>                                        |
| <span data-ttu-id="78b88-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b88-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b88-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b88-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="78b88-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b88-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="78b88-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b88-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="78b88-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-239">Search-Flags</span></span>           | <span data-ttu-id="78b88-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b88-240">0x00000000</span></span>                                   |
| <span data-ttu-id="78b88-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b88-241">System-Flags</span></span>           | <span data-ttu-id="78b88-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b88-242">0x00000010</span></span>                                   |
| <span data-ttu-id="78b88-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b88-243">Classes used in</span></span>        | [<span data-ttu-id="78b88-244">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="78b88-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






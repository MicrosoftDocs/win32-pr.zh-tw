---
title: ms-DS-網站親和性屬性
description: 在權杖評估期間，安全性帳戶管理員會使用 ms DS 網站親和性屬性進行群組擴充。
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- ms-DS-網站親和性屬性 AD 架構
- 網站親和性屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd3ed17b07c73d9e7a6a2d93d93463e1dea40fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845452"
---
# <a name="ms-ds-site-affinity-attribute"></a><span data-ttu-id="01cbd-105">ms-DS-網站親和性屬性</span><span class="sxs-lookup"><span data-stu-id="01cbd-105">ms-DS-Site-Affinity attribute</span></span>

<span data-ttu-id="01cbd-106">在權杖評估期間，安全性帳戶管理員會使用 **MS DS 網站親和性** 屬性進行群組擴充。</span><span class="sxs-lookup"><span data-stu-id="01cbd-106">The **ms-DS-Site-Affinity** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="01cbd-107">進入</span><span class="sxs-lookup"><span data-stu-id="01cbd-107">Entry</span></span> | <span data-ttu-id="01cbd-108">值</span><span class="sxs-lookup"><span data-stu-id="01cbd-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01cbd-109">CN</span><span class="sxs-lookup"><span data-stu-id="01cbd-109">CN</span></span>                | <span data-ttu-id="01cbd-110">ms-DS-網站-親和性</span><span class="sxs-lookup"><span data-stu-id="01cbd-110">ms-DS-Site-Affinity</span></span>                                                                     |
| <span data-ttu-id="01cbd-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="01cbd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="01cbd-112">網站親和性</span><span class="sxs-lookup"><span data-stu-id="01cbd-112">msDS-Site-Affinity</span></span>                                                                      |
| <span data-ttu-id="01cbd-113">大小</span><span class="sxs-lookup"><span data-stu-id="01cbd-113">Size</span></span>              | <span data-ttu-id="01cbd-114">多重值二進位 BLOB，其中每個值都是 sizeof (GUID) + sizeof (大 \_ 整數) 。</span><span class="sxs-lookup"><span data-stu-id="01cbd-114">Multiple-valued binary BLOB, where each value is sizeof(GUID) + sizeof(LARGE\_INTEGER).</span></span> |
| <span data-ttu-id="01cbd-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="01cbd-115">Update Privilege</span></span>  | \-                                                                                      |
| <span data-ttu-id="01cbd-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="01cbd-116">Update Frequency</span></span>  | <span data-ttu-id="01cbd-117">依預設，每隔三個月一次。</span><span class="sxs-lookup"><span data-stu-id="01cbd-117">By default once every three months.</span></span>                                                     |
| <span data-ttu-id="01cbd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="01cbd-118">Attribute-Id</span></span>      | <span data-ttu-id="01cbd-119">1.2.840.113556.1.4.1443</span><span class="sxs-lookup"><span data-stu-id="01cbd-119">1.2.840.113556.1.4.1443</span></span>                                                                 |
| <span data-ttu-id="01cbd-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="01cbd-120">System-Id-Guid</span></span>    | <span data-ttu-id="01cbd-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span><span class="sxs-lookup"><span data-stu-id="01cbd-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span></span>                                                    |
| <span data-ttu-id="01cbd-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="01cbd-122">Syntax</span></span>            | [<span data-ttu-id="01cbd-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="01cbd-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                   |



## <a name="implementations"></a><span data-ttu-id="01cbd-124">實作</span><span class="sxs-lookup"><span data-stu-id="01cbd-124">Implementations</span></span>

-   [<span data-ttu-id="01cbd-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="01cbd-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="01cbd-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="01cbd-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="01cbd-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="01cbd-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="01cbd-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="01cbd-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="01cbd-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="01cbd-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="01cbd-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01cbd-130">Windows Server 2003</span></span>



| <span data-ttu-id="01cbd-131">進入</span><span class="sxs-lookup"><span data-stu-id="01cbd-131">Entry</span></span> | <span data-ttu-id="01cbd-132">值</span><span class="sxs-lookup"><span data-stu-id="01cbd-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01cbd-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01cbd-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01cbd-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="01cbd-135">System-Only</span></span>            | <span data-ttu-id="01cbd-136">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-136">False</span></span>                             |
| <span data-ttu-id="01cbd-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01cbd-137">Is-Single-Valued</span></span>       | <span data-ttu-id="01cbd-138">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-138">False</span></span>                             |
| <span data-ttu-id="01cbd-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01cbd-139">Is Indexed</span></span>             | <span data-ttu-id="01cbd-140">對</span><span class="sxs-lookup"><span data-stu-id="01cbd-140">True</span></span>                              |
| <span data-ttu-id="01cbd-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01cbd-141">In Global Catalog</span></span>      | <span data-ttu-id="01cbd-142">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-142">False</span></span>                             |
| <span data-ttu-id="01cbd-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01cbd-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="01cbd-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01cbd-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01cbd-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01cbd-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01cbd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01cbd-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01cbd-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-147">Search-Flags</span></span>           | <span data-ttu-id="01cbd-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="01cbd-148">0x00000001</span></span>                        |
| <span data-ttu-id="01cbd-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-149">System-Flags</span></span>           | <span data-ttu-id="01cbd-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01cbd-150">0x00000010</span></span>                        |
| <span data-ttu-id="01cbd-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01cbd-151">Classes used in</span></span>        | [<span data-ttu-id="01cbd-152">**User**</span><span class="sxs-lookup"><span data-stu-id="01cbd-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="01cbd-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01cbd-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="01cbd-154">進入</span><span class="sxs-lookup"><span data-stu-id="01cbd-154">Entry</span></span> | <span data-ttu-id="01cbd-155">值</span><span class="sxs-lookup"><span data-stu-id="01cbd-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01cbd-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01cbd-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01cbd-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="01cbd-158">System-Only</span></span>            | <span data-ttu-id="01cbd-159">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-159">False</span></span>                             |
| <span data-ttu-id="01cbd-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01cbd-160">Is-Single-Valued</span></span>       | <span data-ttu-id="01cbd-161">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-161">False</span></span>                             |
| <span data-ttu-id="01cbd-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01cbd-162">Is Indexed</span></span>             | <span data-ttu-id="01cbd-163">對</span><span class="sxs-lookup"><span data-stu-id="01cbd-163">True</span></span>                              |
| <span data-ttu-id="01cbd-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01cbd-164">In Global Catalog</span></span>      | <span data-ttu-id="01cbd-165">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-165">False</span></span>                             |
| <span data-ttu-id="01cbd-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01cbd-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="01cbd-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01cbd-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01cbd-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01cbd-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01cbd-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01cbd-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01cbd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-170">Search-Flags</span></span>           | <span data-ttu-id="01cbd-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="01cbd-171">0x00000001</span></span>                        |
| <span data-ttu-id="01cbd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-172">System-Flags</span></span>           | <span data-ttu-id="01cbd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01cbd-173">0x00000010</span></span>                        |
| <span data-ttu-id="01cbd-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01cbd-174">Classes used in</span></span>        | [<span data-ttu-id="01cbd-175">**User**</span><span class="sxs-lookup"><span data-stu-id="01cbd-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="01cbd-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01cbd-176">Windows Server 2008</span></span>



| <span data-ttu-id="01cbd-177">進入</span><span class="sxs-lookup"><span data-stu-id="01cbd-177">Entry</span></span> | <span data-ttu-id="01cbd-178">值</span><span class="sxs-lookup"><span data-stu-id="01cbd-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01cbd-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01cbd-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01cbd-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="01cbd-181">System-Only</span></span>            | <span data-ttu-id="01cbd-182">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-182">False</span></span>                             |
| <span data-ttu-id="01cbd-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01cbd-183">Is-Single-Valued</span></span>       | <span data-ttu-id="01cbd-184">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-184">False</span></span>                             |
| <span data-ttu-id="01cbd-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01cbd-185">Is Indexed</span></span>             | <span data-ttu-id="01cbd-186">對</span><span class="sxs-lookup"><span data-stu-id="01cbd-186">True</span></span>                              |
| <span data-ttu-id="01cbd-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01cbd-187">In Global Catalog</span></span>      | <span data-ttu-id="01cbd-188">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-188">False</span></span>                             |
| <span data-ttu-id="01cbd-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01cbd-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="01cbd-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01cbd-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01cbd-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01cbd-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01cbd-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01cbd-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01cbd-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-193">Search-Flags</span></span>           | <span data-ttu-id="01cbd-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="01cbd-194">0x00000001</span></span>                        |
| <span data-ttu-id="01cbd-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-195">System-Flags</span></span>           | <span data-ttu-id="01cbd-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01cbd-196">0x00000010</span></span>                        |
| <span data-ttu-id="01cbd-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01cbd-197">Classes used in</span></span>        | [<span data-ttu-id="01cbd-198">**User**</span><span class="sxs-lookup"><span data-stu-id="01cbd-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="01cbd-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01cbd-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="01cbd-200">進入</span><span class="sxs-lookup"><span data-stu-id="01cbd-200">Entry</span></span> | <span data-ttu-id="01cbd-201">值</span><span class="sxs-lookup"><span data-stu-id="01cbd-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01cbd-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01cbd-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01cbd-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="01cbd-204">System-Only</span></span>            | <span data-ttu-id="01cbd-205">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-205">False</span></span>                             |
| <span data-ttu-id="01cbd-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01cbd-206">Is-Single-Valued</span></span>       | <span data-ttu-id="01cbd-207">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-207">False</span></span>                             |
| <span data-ttu-id="01cbd-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01cbd-208">Is Indexed</span></span>             | <span data-ttu-id="01cbd-209">對</span><span class="sxs-lookup"><span data-stu-id="01cbd-209">True</span></span>                              |
| <span data-ttu-id="01cbd-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01cbd-210">In Global Catalog</span></span>      | <span data-ttu-id="01cbd-211">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-211">False</span></span>                             |
| <span data-ttu-id="01cbd-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01cbd-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="01cbd-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01cbd-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01cbd-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01cbd-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01cbd-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01cbd-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01cbd-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-216">Search-Flags</span></span>           | <span data-ttu-id="01cbd-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="01cbd-217">0x00000001</span></span>                        |
| <span data-ttu-id="01cbd-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-218">System-Flags</span></span>           | <span data-ttu-id="01cbd-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01cbd-219">0x00000010</span></span>                        |
| <span data-ttu-id="01cbd-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01cbd-220">Classes used in</span></span>        | [<span data-ttu-id="01cbd-221">**User**</span><span class="sxs-lookup"><span data-stu-id="01cbd-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="01cbd-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01cbd-222">Windows Server 2012</span></span>



| <span data-ttu-id="01cbd-223">進入</span><span class="sxs-lookup"><span data-stu-id="01cbd-223">Entry</span></span> | <span data-ttu-id="01cbd-224">值</span><span class="sxs-lookup"><span data-stu-id="01cbd-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="01cbd-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01cbd-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01cbd-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="01cbd-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="01cbd-227">System-Only</span></span>            | <span data-ttu-id="01cbd-228">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-228">False</span></span>                             |
| <span data-ttu-id="01cbd-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01cbd-229">Is-Single-Valued</span></span>       | <span data-ttu-id="01cbd-230">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-230">False</span></span>                             |
| <span data-ttu-id="01cbd-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01cbd-231">Is Indexed</span></span>             | <span data-ttu-id="01cbd-232">對</span><span class="sxs-lookup"><span data-stu-id="01cbd-232">True</span></span>                              |
| <span data-ttu-id="01cbd-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01cbd-233">In Global Catalog</span></span>      | <span data-ttu-id="01cbd-234">否</span><span class="sxs-lookup"><span data-stu-id="01cbd-234">False</span></span>                             |
| <span data-ttu-id="01cbd-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01cbd-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="01cbd-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01cbd-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="01cbd-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01cbd-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="01cbd-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01cbd-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="01cbd-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-239">Search-Flags</span></span>           | <span data-ttu-id="01cbd-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="01cbd-240">0x00000001</span></span>                        |
| <span data-ttu-id="01cbd-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01cbd-241">System-Flags</span></span>           | <span data-ttu-id="01cbd-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01cbd-242">0x00000010</span></span>                        |
| <span data-ttu-id="01cbd-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01cbd-243">Classes used in</span></span>        | [<span data-ttu-id="01cbd-244">**User**</span><span class="sxs-lookup"><span data-stu-id="01cbd-244">**User**</span></span>](c-user.md)<br/> |



 

 






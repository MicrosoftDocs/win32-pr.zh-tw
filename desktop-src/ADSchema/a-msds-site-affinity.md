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
# <a name="ms-ds-site-affinity-attribute"></a><span data-ttu-id="29463-105">ms-DS-網站親和性屬性</span><span class="sxs-lookup"><span data-stu-id="29463-105">ms-DS-Site-Affinity attribute</span></span>

<span data-ttu-id="29463-106">在權杖評估期間，安全性帳戶管理員會使用 **MS DS 網站親和性** 屬性進行群組擴充。</span><span class="sxs-lookup"><span data-stu-id="29463-106">The **ms-DS-Site-Affinity** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="29463-107">進入</span><span class="sxs-lookup"><span data-stu-id="29463-107">Entry</span></span> | <span data-ttu-id="29463-108">值</span><span class="sxs-lookup"><span data-stu-id="29463-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29463-109">CN</span><span class="sxs-lookup"><span data-stu-id="29463-109">CN</span></span>                | <span data-ttu-id="29463-110">ms-DS-網站-親和性</span><span class="sxs-lookup"><span data-stu-id="29463-110">ms-DS-Site-Affinity</span></span>                                                                     |
| <span data-ttu-id="29463-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="29463-111">Ldap-Display-Name</span></span> | <span data-ttu-id="29463-112">網站親和性</span><span class="sxs-lookup"><span data-stu-id="29463-112">msDS-Site-Affinity</span></span>                                                                      |
| <span data-ttu-id="29463-113">大小</span><span class="sxs-lookup"><span data-stu-id="29463-113">Size</span></span>              | <span data-ttu-id="29463-114">多重值二進位 BLOB，其中每個值都是 sizeof (GUID) + sizeof (大 \_ 整數) 。</span><span class="sxs-lookup"><span data-stu-id="29463-114">Multiple-valued binary BLOB, where each value is sizeof(GUID) + sizeof(LARGE\_INTEGER).</span></span> |
| <span data-ttu-id="29463-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="29463-115">Update Privilege</span></span>  | \-                                                                                      |
| <span data-ttu-id="29463-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="29463-116">Update Frequency</span></span>  | <span data-ttu-id="29463-117">依預設，每隔三個月一次。</span><span class="sxs-lookup"><span data-stu-id="29463-117">By default once every three months.</span></span>                                                     |
| <span data-ttu-id="29463-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29463-118">Attribute-Id</span></span>      | <span data-ttu-id="29463-119">1.2.840.113556.1.4.1443</span><span class="sxs-lookup"><span data-stu-id="29463-119">1.2.840.113556.1.4.1443</span></span>                                                                 |
| <span data-ttu-id="29463-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="29463-120">System-Id-Guid</span></span>    | <span data-ttu-id="29463-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span><span class="sxs-lookup"><span data-stu-id="29463-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span></span>                                                    |
| <span data-ttu-id="29463-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="29463-122">Syntax</span></span>            | [<span data-ttu-id="29463-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="29463-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                   |



## <a name="implementations"></a><span data-ttu-id="29463-124">實作</span><span class="sxs-lookup"><span data-stu-id="29463-124">Implementations</span></span>

-   [<span data-ttu-id="29463-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="29463-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="29463-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="29463-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="29463-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29463-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29463-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29463-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29463-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29463-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="29463-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29463-130">Windows Server 2003</span></span>



| <span data-ttu-id="29463-131">進入</span><span class="sxs-lookup"><span data-stu-id="29463-131">Entry</span></span> | <span data-ttu-id="29463-132">值</span><span class="sxs-lookup"><span data-stu-id="29463-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29463-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29463-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29463-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="29463-135">System-Only</span></span>            | <span data-ttu-id="29463-136">否</span><span class="sxs-lookup"><span data-stu-id="29463-136">False</span></span>                             |
| <span data-ttu-id="29463-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29463-137">Is-Single-Valued</span></span>       | <span data-ttu-id="29463-138">否</span><span class="sxs-lookup"><span data-stu-id="29463-138">False</span></span>                             |
| <span data-ttu-id="29463-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29463-139">Is Indexed</span></span>             | <span data-ttu-id="29463-140">對</span><span class="sxs-lookup"><span data-stu-id="29463-140">True</span></span>                              |
| <span data-ttu-id="29463-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29463-141">In Global Catalog</span></span>      | <span data-ttu-id="29463-142">否</span><span class="sxs-lookup"><span data-stu-id="29463-142">False</span></span>                             |
| <span data-ttu-id="29463-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29463-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="29463-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29463-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29463-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29463-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29463-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29463-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29463-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-147">Search-Flags</span></span>           | <span data-ttu-id="29463-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="29463-148">0x00000001</span></span>                        |
| <span data-ttu-id="29463-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-149">System-Flags</span></span>           | <span data-ttu-id="29463-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29463-150">0x00000010</span></span>                        |
| <span data-ttu-id="29463-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29463-151">Classes used in</span></span>        | [<span data-ttu-id="29463-152">**User**</span><span class="sxs-lookup"><span data-stu-id="29463-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="29463-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="29463-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="29463-154">進入</span><span class="sxs-lookup"><span data-stu-id="29463-154">Entry</span></span> | <span data-ttu-id="29463-155">值</span><span class="sxs-lookup"><span data-stu-id="29463-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29463-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29463-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29463-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="29463-158">System-Only</span></span>            | <span data-ttu-id="29463-159">否</span><span class="sxs-lookup"><span data-stu-id="29463-159">False</span></span>                             |
| <span data-ttu-id="29463-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29463-160">Is-Single-Valued</span></span>       | <span data-ttu-id="29463-161">否</span><span class="sxs-lookup"><span data-stu-id="29463-161">False</span></span>                             |
| <span data-ttu-id="29463-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29463-162">Is Indexed</span></span>             | <span data-ttu-id="29463-163">對</span><span class="sxs-lookup"><span data-stu-id="29463-163">True</span></span>                              |
| <span data-ttu-id="29463-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29463-164">In Global Catalog</span></span>      | <span data-ttu-id="29463-165">否</span><span class="sxs-lookup"><span data-stu-id="29463-165">False</span></span>                             |
| <span data-ttu-id="29463-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29463-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="29463-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29463-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29463-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29463-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29463-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29463-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29463-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-170">Search-Flags</span></span>           | <span data-ttu-id="29463-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="29463-171">0x00000001</span></span>                        |
| <span data-ttu-id="29463-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-172">System-Flags</span></span>           | <span data-ttu-id="29463-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29463-173">0x00000010</span></span>                        |
| <span data-ttu-id="29463-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29463-174">Classes used in</span></span>        | [<span data-ttu-id="29463-175">**User**</span><span class="sxs-lookup"><span data-stu-id="29463-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="29463-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29463-176">Windows Server 2008</span></span>



| <span data-ttu-id="29463-177">進入</span><span class="sxs-lookup"><span data-stu-id="29463-177">Entry</span></span> | <span data-ttu-id="29463-178">值</span><span class="sxs-lookup"><span data-stu-id="29463-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29463-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29463-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29463-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="29463-181">System-Only</span></span>            | <span data-ttu-id="29463-182">否</span><span class="sxs-lookup"><span data-stu-id="29463-182">False</span></span>                             |
| <span data-ttu-id="29463-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29463-183">Is-Single-Valued</span></span>       | <span data-ttu-id="29463-184">否</span><span class="sxs-lookup"><span data-stu-id="29463-184">False</span></span>                             |
| <span data-ttu-id="29463-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29463-185">Is Indexed</span></span>             | <span data-ttu-id="29463-186">對</span><span class="sxs-lookup"><span data-stu-id="29463-186">True</span></span>                              |
| <span data-ttu-id="29463-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29463-187">In Global Catalog</span></span>      | <span data-ttu-id="29463-188">否</span><span class="sxs-lookup"><span data-stu-id="29463-188">False</span></span>                             |
| <span data-ttu-id="29463-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29463-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="29463-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29463-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29463-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29463-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29463-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29463-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29463-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-193">Search-Flags</span></span>           | <span data-ttu-id="29463-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="29463-194">0x00000001</span></span>                        |
| <span data-ttu-id="29463-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-195">System-Flags</span></span>           | <span data-ttu-id="29463-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29463-196">0x00000010</span></span>                        |
| <span data-ttu-id="29463-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29463-197">Classes used in</span></span>        | [<span data-ttu-id="29463-198">**User**</span><span class="sxs-lookup"><span data-stu-id="29463-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29463-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29463-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29463-200">進入</span><span class="sxs-lookup"><span data-stu-id="29463-200">Entry</span></span> | <span data-ttu-id="29463-201">值</span><span class="sxs-lookup"><span data-stu-id="29463-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29463-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29463-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29463-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="29463-204">System-Only</span></span>            | <span data-ttu-id="29463-205">否</span><span class="sxs-lookup"><span data-stu-id="29463-205">False</span></span>                             |
| <span data-ttu-id="29463-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29463-206">Is-Single-Valued</span></span>       | <span data-ttu-id="29463-207">否</span><span class="sxs-lookup"><span data-stu-id="29463-207">False</span></span>                             |
| <span data-ttu-id="29463-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29463-208">Is Indexed</span></span>             | <span data-ttu-id="29463-209">對</span><span class="sxs-lookup"><span data-stu-id="29463-209">True</span></span>                              |
| <span data-ttu-id="29463-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29463-210">In Global Catalog</span></span>      | <span data-ttu-id="29463-211">否</span><span class="sxs-lookup"><span data-stu-id="29463-211">False</span></span>                             |
| <span data-ttu-id="29463-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29463-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="29463-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29463-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29463-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29463-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29463-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29463-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29463-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-216">Search-Flags</span></span>           | <span data-ttu-id="29463-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="29463-217">0x00000001</span></span>                        |
| <span data-ttu-id="29463-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-218">System-Flags</span></span>           | <span data-ttu-id="29463-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29463-219">0x00000010</span></span>                        |
| <span data-ttu-id="29463-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29463-220">Classes used in</span></span>        | [<span data-ttu-id="29463-221">**User**</span><span class="sxs-lookup"><span data-stu-id="29463-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29463-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29463-222">Windows Server 2012</span></span>



| <span data-ttu-id="29463-223">進入</span><span class="sxs-lookup"><span data-stu-id="29463-223">Entry</span></span> | <span data-ttu-id="29463-224">值</span><span class="sxs-lookup"><span data-stu-id="29463-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29463-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29463-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29463-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29463-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="29463-227">System-Only</span></span>            | <span data-ttu-id="29463-228">否</span><span class="sxs-lookup"><span data-stu-id="29463-228">False</span></span>                             |
| <span data-ttu-id="29463-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29463-229">Is-Single-Valued</span></span>       | <span data-ttu-id="29463-230">否</span><span class="sxs-lookup"><span data-stu-id="29463-230">False</span></span>                             |
| <span data-ttu-id="29463-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29463-231">Is Indexed</span></span>             | <span data-ttu-id="29463-232">對</span><span class="sxs-lookup"><span data-stu-id="29463-232">True</span></span>                              |
| <span data-ttu-id="29463-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29463-233">In Global Catalog</span></span>      | <span data-ttu-id="29463-234">否</span><span class="sxs-lookup"><span data-stu-id="29463-234">False</span></span>                             |
| <span data-ttu-id="29463-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29463-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="29463-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29463-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29463-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29463-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29463-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29463-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29463-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-239">Search-Flags</span></span>           | <span data-ttu-id="29463-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="29463-240">0x00000001</span></span>                        |
| <span data-ttu-id="29463-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29463-241">System-Flags</span></span>           | <span data-ttu-id="29463-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29463-242">0x00000010</span></span>                        |
| <span data-ttu-id="29463-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29463-243">Classes used in</span></span>        | [<span data-ttu-id="29463-244">**User**</span><span class="sxs-lookup"><span data-stu-id="29463-244">**User**</span></span>](c-user.md)<br/> |



 

 






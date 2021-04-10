---
title: ms-DS-信任-樹系信任資訊屬性
description: 包含樹系信任資訊 (系統用於 Trusted-Domain 物件的二進位 BLOB) 。
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- ms-DS-信任-樹系信任資訊屬性 AD 架構
- TrustForestTrustInfo 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e259abaeae4d99b80b8ff6a390901f1c9f51e6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687016"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="a7932-105">ms-DS-信任-樹系信任資訊屬性</span><span class="sxs-lookup"><span data-stu-id="a7932-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="a7932-106">包含樹系信任資訊 (系統用於 Trusted-Domain 物件的二進位 BLOB) 。</span><span class="sxs-lookup"><span data-stu-id="a7932-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="a7932-107">進入</span><span class="sxs-lookup"><span data-stu-id="a7932-107">Entry</span></span> | <span data-ttu-id="a7932-108">值</span><span class="sxs-lookup"><span data-stu-id="a7932-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7932-109">CN</span><span class="sxs-lookup"><span data-stu-id="a7932-109">CN</span></span>                | <span data-ttu-id="a7932-110">ms-DS-信任-樹系信任資訊</span><span class="sxs-lookup"><span data-stu-id="a7932-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="a7932-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a7932-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a7932-112">TrustForestTrustInfo</span><span class="sxs-lookup"><span data-stu-id="a7932-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="a7932-113">大小</span><span class="sxs-lookup"><span data-stu-id="a7932-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="a7932-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a7932-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="a7932-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a7932-115">Update Frequency</span></span>  | <span data-ttu-id="a7932-116">只有在樹系之間的信任關係變更時才會發生。</span><span class="sxs-lookup"><span data-stu-id="a7932-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="a7932-117">如果信任樹系的拓撲變更，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="a7932-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="a7932-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a7932-118">Attribute-Id</span></span>      | <span data-ttu-id="a7932-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="a7932-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="a7932-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a7932-120">System-Id-Guid</span></span>    | <span data-ttu-id="a7932-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="a7932-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="a7932-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7932-122">Syntax</span></span>            | [<span data-ttu-id="a7932-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="a7932-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="a7932-124">實作</span><span class="sxs-lookup"><span data-stu-id="a7932-124">Implementations</span></span>

-   [<span data-ttu-id="a7932-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a7932-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a7932-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a7932-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a7932-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a7932-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a7932-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a7932-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a7932-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a7932-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a7932-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7932-130">Windows Server 2003</span></span>



| <span data-ttu-id="a7932-131">進入</span><span class="sxs-lookup"><span data-stu-id="a7932-131">Entry</span></span> | <span data-ttu-id="a7932-132">值</span><span class="sxs-lookup"><span data-stu-id="a7932-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a7932-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7932-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7932-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7932-135">System-Only</span></span>            | <span data-ttu-id="a7932-136">否</span><span class="sxs-lookup"><span data-stu-id="a7932-136">False</span></span>                                                |
| <span data-ttu-id="a7932-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7932-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a7932-138">對</span><span class="sxs-lookup"><span data-stu-id="a7932-138">True</span></span>                                                 |
| <span data-ttu-id="a7932-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7932-139">Is Indexed</span></span>             | <span data-ttu-id="a7932-140">否</span><span class="sxs-lookup"><span data-stu-id="a7932-140">False</span></span>                                                |
| <span data-ttu-id="a7932-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7932-141">In Global Catalog</span></span>      | <span data-ttu-id="a7932-142">對</span><span class="sxs-lookup"><span data-stu-id="a7932-142">True</span></span>                                                 |
| <span data-ttu-id="a7932-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7932-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7932-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7932-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a7932-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7932-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7932-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-147">Search-Flags</span></span>           | <span data-ttu-id="a7932-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7932-148">0x00000000</span></span>                                           |
| <span data-ttu-id="a7932-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-149">System-Flags</span></span>           | <span data-ttu-id="a7932-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7932-150">0x00000010</span></span>                                           |
| <span data-ttu-id="a7932-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7932-151">Classes used in</span></span>        | [<span data-ttu-id="a7932-152">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a7932-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a7932-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a7932-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a7932-154">進入</span><span class="sxs-lookup"><span data-stu-id="a7932-154">Entry</span></span> | <span data-ttu-id="a7932-155">值</span><span class="sxs-lookup"><span data-stu-id="a7932-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a7932-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7932-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7932-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7932-158">System-Only</span></span>            | <span data-ttu-id="a7932-159">否</span><span class="sxs-lookup"><span data-stu-id="a7932-159">False</span></span>                                                |
| <span data-ttu-id="a7932-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7932-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a7932-161">對</span><span class="sxs-lookup"><span data-stu-id="a7932-161">True</span></span>                                                 |
| <span data-ttu-id="a7932-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7932-162">Is Indexed</span></span>             | <span data-ttu-id="a7932-163">否</span><span class="sxs-lookup"><span data-stu-id="a7932-163">False</span></span>                                                |
| <span data-ttu-id="a7932-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7932-164">In Global Catalog</span></span>      | <span data-ttu-id="a7932-165">對</span><span class="sxs-lookup"><span data-stu-id="a7932-165">True</span></span>                                                 |
| <span data-ttu-id="a7932-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7932-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7932-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7932-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a7932-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7932-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7932-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-170">Search-Flags</span></span>           | <span data-ttu-id="a7932-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7932-171">0x00000000</span></span>                                           |
| <span data-ttu-id="a7932-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-172">System-Flags</span></span>           | <span data-ttu-id="a7932-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7932-173">0x00000010</span></span>                                           |
| <span data-ttu-id="a7932-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7932-174">Classes used in</span></span>        | [<span data-ttu-id="a7932-175">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a7932-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a7932-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7932-176">Windows Server 2008</span></span>



| <span data-ttu-id="a7932-177">進入</span><span class="sxs-lookup"><span data-stu-id="a7932-177">Entry</span></span> | <span data-ttu-id="a7932-178">值</span><span class="sxs-lookup"><span data-stu-id="a7932-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a7932-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7932-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7932-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7932-181">System-Only</span></span>            | <span data-ttu-id="a7932-182">否</span><span class="sxs-lookup"><span data-stu-id="a7932-182">False</span></span>                                                |
| <span data-ttu-id="a7932-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7932-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a7932-184">對</span><span class="sxs-lookup"><span data-stu-id="a7932-184">True</span></span>                                                 |
| <span data-ttu-id="a7932-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7932-185">Is Indexed</span></span>             | <span data-ttu-id="a7932-186">否</span><span class="sxs-lookup"><span data-stu-id="a7932-186">False</span></span>                                                |
| <span data-ttu-id="a7932-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7932-187">In Global Catalog</span></span>      | <span data-ttu-id="a7932-188">對</span><span class="sxs-lookup"><span data-stu-id="a7932-188">True</span></span>                                                 |
| <span data-ttu-id="a7932-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7932-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7932-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7932-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a7932-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7932-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7932-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-193">Search-Flags</span></span>           | <span data-ttu-id="a7932-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7932-194">0x00000000</span></span>                                           |
| <span data-ttu-id="a7932-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-195">System-Flags</span></span>           | <span data-ttu-id="a7932-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7932-196">0x00000010</span></span>                                           |
| <span data-ttu-id="a7932-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7932-197">Classes used in</span></span>        | [<span data-ttu-id="a7932-198">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a7932-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a7932-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7932-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a7932-200">進入</span><span class="sxs-lookup"><span data-stu-id="a7932-200">Entry</span></span> | <span data-ttu-id="a7932-201">值</span><span class="sxs-lookup"><span data-stu-id="a7932-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a7932-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7932-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7932-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7932-204">System-Only</span></span>            | <span data-ttu-id="a7932-205">否</span><span class="sxs-lookup"><span data-stu-id="a7932-205">False</span></span>                                                |
| <span data-ttu-id="a7932-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7932-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a7932-207">對</span><span class="sxs-lookup"><span data-stu-id="a7932-207">True</span></span>                                                 |
| <span data-ttu-id="a7932-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7932-208">Is Indexed</span></span>             | <span data-ttu-id="a7932-209">否</span><span class="sxs-lookup"><span data-stu-id="a7932-209">False</span></span>                                                |
| <span data-ttu-id="a7932-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7932-210">In Global Catalog</span></span>      | <span data-ttu-id="a7932-211">對</span><span class="sxs-lookup"><span data-stu-id="a7932-211">True</span></span>                                                 |
| <span data-ttu-id="a7932-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7932-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7932-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7932-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a7932-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7932-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7932-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-216">Search-Flags</span></span>           | <span data-ttu-id="a7932-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7932-217">0x00000000</span></span>                                           |
| <span data-ttu-id="a7932-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-218">System-Flags</span></span>           | <span data-ttu-id="a7932-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7932-219">0x00000010</span></span>                                           |
| <span data-ttu-id="a7932-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7932-220">Classes used in</span></span>        | [<span data-ttu-id="a7932-221">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a7932-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a7932-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7932-222">Windows Server 2012</span></span>



| <span data-ttu-id="a7932-223">進入</span><span class="sxs-lookup"><span data-stu-id="a7932-223">Entry</span></span> | <span data-ttu-id="a7932-224">值</span><span class="sxs-lookup"><span data-stu-id="a7932-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a7932-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7932-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7932-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a7932-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7932-227">System-Only</span></span>            | <span data-ttu-id="a7932-228">否</span><span class="sxs-lookup"><span data-stu-id="a7932-228">False</span></span>                                                |
| <span data-ttu-id="a7932-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7932-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a7932-230">對</span><span class="sxs-lookup"><span data-stu-id="a7932-230">True</span></span>                                                 |
| <span data-ttu-id="a7932-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7932-231">Is Indexed</span></span>             | <span data-ttu-id="a7932-232">否</span><span class="sxs-lookup"><span data-stu-id="a7932-232">False</span></span>                                                |
| <span data-ttu-id="a7932-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7932-233">In Global Catalog</span></span>      | <span data-ttu-id="a7932-234">對</span><span class="sxs-lookup"><span data-stu-id="a7932-234">True</span></span>                                                 |
| <span data-ttu-id="a7932-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7932-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7932-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7932-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a7932-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7932-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7932-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a7932-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-239">Search-Flags</span></span>           | <span data-ttu-id="a7932-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7932-240">0x00000000</span></span>                                           |
| <span data-ttu-id="a7932-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7932-241">System-Flags</span></span>           | <span data-ttu-id="a7932-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7932-242">0x00000010</span></span>                                           |
| <span data-ttu-id="a7932-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7932-243">Classes used in</span></span>        | [<span data-ttu-id="a7932-244">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a7932-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






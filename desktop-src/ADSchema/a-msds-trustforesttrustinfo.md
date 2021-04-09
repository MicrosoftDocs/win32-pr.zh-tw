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
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="65ee4-105">ms-DS-信任-樹系信任資訊屬性</span><span class="sxs-lookup"><span data-stu-id="65ee4-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="65ee4-106">包含樹系信任資訊 (系統用於 Trusted-Domain 物件的二進位 BLOB) 。</span><span class="sxs-lookup"><span data-stu-id="65ee4-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="65ee4-107">進入</span><span class="sxs-lookup"><span data-stu-id="65ee4-107">Entry</span></span> | <span data-ttu-id="65ee4-108">值</span><span class="sxs-lookup"><span data-stu-id="65ee4-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ee4-109">CN</span><span class="sxs-lookup"><span data-stu-id="65ee4-109">CN</span></span>                | <span data-ttu-id="65ee4-110">ms-DS-信任-樹系信任資訊</span><span class="sxs-lookup"><span data-stu-id="65ee4-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="65ee4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="65ee4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="65ee4-112">TrustForestTrustInfo</span><span class="sxs-lookup"><span data-stu-id="65ee4-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="65ee4-113">大小</span><span class="sxs-lookup"><span data-stu-id="65ee4-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="65ee4-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="65ee4-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="65ee4-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="65ee4-115">Update Frequency</span></span>  | <span data-ttu-id="65ee4-116">只有在樹系之間的信任關係變更時才會發生。</span><span class="sxs-lookup"><span data-stu-id="65ee4-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="65ee4-117">如果信任樹系的拓撲變更，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="65ee4-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="65ee4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="65ee4-118">Attribute-Id</span></span>      | <span data-ttu-id="65ee4-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="65ee4-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="65ee4-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="65ee4-120">System-Id-Guid</span></span>    | <span data-ttu-id="65ee4-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="65ee4-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="65ee4-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="65ee4-122">Syntax</span></span>            | [<span data-ttu-id="65ee4-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="65ee4-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="65ee4-124">實作</span><span class="sxs-lookup"><span data-stu-id="65ee4-124">Implementations</span></span>

-   [<span data-ttu-id="65ee4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="65ee4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="65ee4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="65ee4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="65ee4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="65ee4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="65ee4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="65ee4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="65ee4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="65ee4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="65ee4-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65ee4-130">Windows Server 2003</span></span>



| <span data-ttu-id="65ee4-131">進入</span><span class="sxs-lookup"><span data-stu-id="65ee4-131">Entry</span></span> | <span data-ttu-id="65ee4-132">值</span><span class="sxs-lookup"><span data-stu-id="65ee4-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="65ee4-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65ee4-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65ee4-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="65ee4-135">System-Only</span></span>            | <span data-ttu-id="65ee4-136">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-136">False</span></span>                                                |
| <span data-ttu-id="65ee4-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65ee4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="65ee4-138">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-138">True</span></span>                                                 |
| <span data-ttu-id="65ee4-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65ee4-139">Is Indexed</span></span>             | <span data-ttu-id="65ee4-140">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-140">False</span></span>                                                |
| <span data-ttu-id="65ee4-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65ee4-141">In Global Catalog</span></span>      | <span data-ttu-id="65ee4-142">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-142">True</span></span>                                                 |
| <span data-ttu-id="65ee4-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65ee4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="65ee4-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65ee4-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="65ee4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65ee4-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65ee4-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-147">Search-Flags</span></span>           | <span data-ttu-id="65ee4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65ee4-148">0x00000000</span></span>                                           |
| <span data-ttu-id="65ee4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-149">System-Flags</span></span>           | <span data-ttu-id="65ee4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65ee4-150">0x00000010</span></span>                                           |
| <span data-ttu-id="65ee4-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65ee4-151">Classes used in</span></span>        | [<span data-ttu-id="65ee4-152">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="65ee4-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="65ee4-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="65ee4-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="65ee4-154">進入</span><span class="sxs-lookup"><span data-stu-id="65ee4-154">Entry</span></span> | <span data-ttu-id="65ee4-155">值</span><span class="sxs-lookup"><span data-stu-id="65ee4-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="65ee4-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65ee4-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65ee4-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="65ee4-158">System-Only</span></span>            | <span data-ttu-id="65ee4-159">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-159">False</span></span>                                                |
| <span data-ttu-id="65ee4-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65ee4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="65ee4-161">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-161">True</span></span>                                                 |
| <span data-ttu-id="65ee4-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65ee4-162">Is Indexed</span></span>             | <span data-ttu-id="65ee4-163">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-163">False</span></span>                                                |
| <span data-ttu-id="65ee4-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65ee4-164">In Global Catalog</span></span>      | <span data-ttu-id="65ee4-165">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-165">True</span></span>                                                 |
| <span data-ttu-id="65ee4-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65ee4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="65ee4-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65ee4-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="65ee4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65ee4-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65ee4-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-170">Search-Flags</span></span>           | <span data-ttu-id="65ee4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65ee4-171">0x00000000</span></span>                                           |
| <span data-ttu-id="65ee4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-172">System-Flags</span></span>           | <span data-ttu-id="65ee4-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65ee4-173">0x00000010</span></span>                                           |
| <span data-ttu-id="65ee4-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65ee4-174">Classes used in</span></span>        | [<span data-ttu-id="65ee4-175">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="65ee4-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="65ee4-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65ee4-176">Windows Server 2008</span></span>



| <span data-ttu-id="65ee4-177">進入</span><span class="sxs-lookup"><span data-stu-id="65ee4-177">Entry</span></span> | <span data-ttu-id="65ee4-178">值</span><span class="sxs-lookup"><span data-stu-id="65ee4-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="65ee4-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65ee4-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65ee4-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="65ee4-181">System-Only</span></span>            | <span data-ttu-id="65ee4-182">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-182">False</span></span>                                                |
| <span data-ttu-id="65ee4-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65ee4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="65ee4-184">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-184">True</span></span>                                                 |
| <span data-ttu-id="65ee4-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65ee4-185">Is Indexed</span></span>             | <span data-ttu-id="65ee4-186">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-186">False</span></span>                                                |
| <span data-ttu-id="65ee4-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65ee4-187">In Global Catalog</span></span>      | <span data-ttu-id="65ee4-188">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-188">True</span></span>                                                 |
| <span data-ttu-id="65ee4-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65ee4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="65ee4-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65ee4-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="65ee4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65ee4-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65ee4-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-193">Search-Flags</span></span>           | <span data-ttu-id="65ee4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65ee4-194">0x00000000</span></span>                                           |
| <span data-ttu-id="65ee4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-195">System-Flags</span></span>           | <span data-ttu-id="65ee4-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65ee4-196">0x00000010</span></span>                                           |
| <span data-ttu-id="65ee4-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65ee4-197">Classes used in</span></span>        | [<span data-ttu-id="65ee4-198">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="65ee4-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="65ee4-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65ee4-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="65ee4-200">進入</span><span class="sxs-lookup"><span data-stu-id="65ee4-200">Entry</span></span> | <span data-ttu-id="65ee4-201">值</span><span class="sxs-lookup"><span data-stu-id="65ee4-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="65ee4-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65ee4-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65ee4-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="65ee4-204">System-Only</span></span>            | <span data-ttu-id="65ee4-205">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-205">False</span></span>                                                |
| <span data-ttu-id="65ee4-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65ee4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="65ee4-207">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-207">True</span></span>                                                 |
| <span data-ttu-id="65ee4-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65ee4-208">Is Indexed</span></span>             | <span data-ttu-id="65ee4-209">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-209">False</span></span>                                                |
| <span data-ttu-id="65ee4-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65ee4-210">In Global Catalog</span></span>      | <span data-ttu-id="65ee4-211">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-211">True</span></span>                                                 |
| <span data-ttu-id="65ee4-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65ee4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="65ee4-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65ee4-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="65ee4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65ee4-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65ee4-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-216">Search-Flags</span></span>           | <span data-ttu-id="65ee4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65ee4-217">0x00000000</span></span>                                           |
| <span data-ttu-id="65ee4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-218">System-Flags</span></span>           | <span data-ttu-id="65ee4-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65ee4-219">0x00000010</span></span>                                           |
| <span data-ttu-id="65ee4-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65ee4-220">Classes used in</span></span>        | [<span data-ttu-id="65ee4-221">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="65ee4-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="65ee4-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65ee4-222">Windows Server 2012</span></span>



| <span data-ttu-id="65ee4-223">進入</span><span class="sxs-lookup"><span data-stu-id="65ee4-223">Entry</span></span> | <span data-ttu-id="65ee4-224">值</span><span class="sxs-lookup"><span data-stu-id="65ee4-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="65ee4-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65ee4-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65ee4-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="65ee4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="65ee4-227">System-Only</span></span>            | <span data-ttu-id="65ee4-228">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-228">False</span></span>                                                |
| <span data-ttu-id="65ee4-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65ee4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="65ee4-230">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-230">True</span></span>                                                 |
| <span data-ttu-id="65ee4-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65ee4-231">Is Indexed</span></span>             | <span data-ttu-id="65ee4-232">否</span><span class="sxs-lookup"><span data-stu-id="65ee4-232">False</span></span>                                                |
| <span data-ttu-id="65ee4-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65ee4-233">In Global Catalog</span></span>      | <span data-ttu-id="65ee4-234">對</span><span class="sxs-lookup"><span data-stu-id="65ee4-234">True</span></span>                                                 |
| <span data-ttu-id="65ee4-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65ee4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="65ee4-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65ee4-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="65ee4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65ee4-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65ee4-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="65ee4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-239">Search-Flags</span></span>           | <span data-ttu-id="65ee4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65ee4-240">0x00000000</span></span>                                           |
| <span data-ttu-id="65ee4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65ee4-241">System-Flags</span></span>           | <span data-ttu-id="65ee4-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65ee4-242">0x00000010</span></span>                                           |
| <span data-ttu-id="65ee4-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65ee4-243">Classes used in</span></span>        | [<span data-ttu-id="65ee4-244">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="65ee4-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






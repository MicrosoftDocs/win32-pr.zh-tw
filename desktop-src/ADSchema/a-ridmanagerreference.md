---
title: RID 管理員-Reference 屬性
description: 物件之 RID 管理員的分辨名稱。
ms.assetid: ff4b7e0b-da6d-4033-847b-30da58a4a004
ms.tgt_platform: multiple
keywords:
- RID 管理員-參考屬性 AD 架構
- rIDManagerReference 屬性 AD 架構
topic_type:
- apiref
api_name:
- RID-Manager-Reference
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02ffe4a3689dcab4da66e85340e7efc3a56c6074
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106991320"
---
# <a name="rid-manager-reference-attribute"></a><span data-ttu-id="66b1c-105">RID 管理員-Reference 屬性</span><span class="sxs-lookup"><span data-stu-id="66b1c-105">RID-Manager-Reference attribute</span></span>

<span data-ttu-id="66b1c-106">物件之 RID 管理員的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="66b1c-106">The Distinguished Name for the RID Manager of an object.</span></span>



| <span data-ttu-id="66b1c-107">進入</span><span class="sxs-lookup"><span data-stu-id="66b1c-107">Entry</span></span> | <span data-ttu-id="66b1c-108">值</span><span class="sxs-lookup"><span data-stu-id="66b1c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="66b1c-109">CN</span><span class="sxs-lookup"><span data-stu-id="66b1c-109">CN</span></span>                | <span data-ttu-id="66b1c-110">RID 管理員-參考</span><span class="sxs-lookup"><span data-stu-id="66b1c-110">RID-Manager-Reference</span></span>                   |
| <span data-ttu-id="66b1c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="66b1c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="66b1c-112">rIDManagerReference</span><span class="sxs-lookup"><span data-stu-id="66b1c-112">rIDManagerReference</span></span>                     |
| <span data-ttu-id="66b1c-113">大小</span><span class="sxs-lookup"><span data-stu-id="66b1c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="66b1c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="66b1c-114">Update Privilege</span></span>  | <span data-ttu-id="66b1c-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="66b1c-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="66b1c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="66b1c-116">Update Frequency</span></span>  | <span data-ttu-id="66b1c-117">每次 RID 管理員變更時。</span><span class="sxs-lookup"><span data-stu-id="66b1c-117">Whenever the RID Manager changes.</span></span>       |
| <span data-ttu-id="66b1c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="66b1c-118">Attribute-Id</span></span>      | <span data-ttu-id="66b1c-119">1.2.840.113556.1.4.368</span><span class="sxs-lookup"><span data-stu-id="66b1c-119">1.2.840.113556.1.4.368</span></span>                  |
| <span data-ttu-id="66b1c-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="66b1c-120">System-Id-Guid</span></span>    | <span data-ttu-id="66b1c-121">66171886-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="66b1c-121">66171886-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="66b1c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="66b1c-122">Syntax</span></span>            | [<span data-ttu-id="66b1c-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="66b1c-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="66b1c-124">實作</span><span class="sxs-lookup"><span data-stu-id="66b1c-124">Implementations</span></span>

-   [<span data-ttu-id="66b1c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="66b1c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="66b1c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="66b1c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="66b1c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="66b1c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="66b1c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="66b1c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="66b1c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="66b1c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="66b1c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="66b1c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="66b1c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66b1c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="66b1c-132">進入</span><span class="sxs-lookup"><span data-stu-id="66b1c-132">Entry</span></span> | <span data-ttu-id="66b1c-133">值</span><span class="sxs-lookup"><span data-stu-id="66b1c-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="66b1c-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="66b1c-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66b1c-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="66b1c-136">System-Only</span></span>            | <span data-ttu-id="66b1c-137">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-137">True</span></span>                                         |
| <span data-ttu-id="66b1c-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="66b1c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="66b1c-139">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-139">True</span></span>                                         |
| <span data-ttu-id="66b1c-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="66b1c-140">Is Indexed</span></span>             | <span data-ttu-id="66b1c-141">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-141">False</span></span>                                        |
| <span data-ttu-id="66b1c-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="66b1c-142">In Global Catalog</span></span>      | <span data-ttu-id="66b1c-143">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-143">False</span></span>                                        |
| <span data-ttu-id="66b1c-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="66b1c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="66b1c-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="66b1c-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="66b1c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66b1c-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66b1c-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-148">Search-Flags</span></span>           | <span data-ttu-id="66b1c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66b1c-149">0x00000000</span></span>                                   |
| <span data-ttu-id="66b1c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-150">System-Flags</span></span>           | <span data-ttu-id="66b1c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66b1c-151">0x00000010</span></span>                                   |
| <span data-ttu-id="66b1c-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="66b1c-152">Classes used in</span></span>        | [<span data-ttu-id="66b1c-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="66b1c-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="66b1c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66b1c-154">Windows Server 2003</span></span>



| <span data-ttu-id="66b1c-155">進入</span><span class="sxs-lookup"><span data-stu-id="66b1c-155">Entry</span></span> | <span data-ttu-id="66b1c-156">值</span><span class="sxs-lookup"><span data-stu-id="66b1c-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="66b1c-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="66b1c-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66b1c-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="66b1c-159">System-Only</span></span>            | <span data-ttu-id="66b1c-160">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-160">True</span></span>                                         |
| <span data-ttu-id="66b1c-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="66b1c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="66b1c-162">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-162">True</span></span>                                         |
| <span data-ttu-id="66b1c-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="66b1c-163">Is Indexed</span></span>             | <span data-ttu-id="66b1c-164">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-164">False</span></span>                                        |
| <span data-ttu-id="66b1c-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="66b1c-165">In Global Catalog</span></span>      | <span data-ttu-id="66b1c-166">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-166">False</span></span>                                        |
| <span data-ttu-id="66b1c-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="66b1c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="66b1c-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="66b1c-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="66b1c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66b1c-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66b1c-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-171">Search-Flags</span></span>           | <span data-ttu-id="66b1c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66b1c-172">0x00000000</span></span>                                   |
| <span data-ttu-id="66b1c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-173">System-Flags</span></span>           | <span data-ttu-id="66b1c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66b1c-174">0x00000010</span></span>                                   |
| <span data-ttu-id="66b1c-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="66b1c-175">Classes used in</span></span>        | [<span data-ttu-id="66b1c-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="66b1c-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="66b1c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="66b1c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="66b1c-178">進入</span><span class="sxs-lookup"><span data-stu-id="66b1c-178">Entry</span></span> | <span data-ttu-id="66b1c-179">值</span><span class="sxs-lookup"><span data-stu-id="66b1c-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="66b1c-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="66b1c-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66b1c-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="66b1c-182">System-Only</span></span>            | <span data-ttu-id="66b1c-183">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-183">True</span></span>                                         |
| <span data-ttu-id="66b1c-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="66b1c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="66b1c-185">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-185">True</span></span>                                         |
| <span data-ttu-id="66b1c-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="66b1c-186">Is Indexed</span></span>             | <span data-ttu-id="66b1c-187">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-187">False</span></span>                                        |
| <span data-ttu-id="66b1c-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="66b1c-188">In Global Catalog</span></span>      | <span data-ttu-id="66b1c-189">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-189">False</span></span>                                        |
| <span data-ttu-id="66b1c-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="66b1c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="66b1c-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="66b1c-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="66b1c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66b1c-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66b1c-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-194">Search-Flags</span></span>           | <span data-ttu-id="66b1c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66b1c-195">0x00000000</span></span>                                   |
| <span data-ttu-id="66b1c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-196">System-Flags</span></span>           | <span data-ttu-id="66b1c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66b1c-197">0x00000010</span></span>                                   |
| <span data-ttu-id="66b1c-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="66b1c-198">Classes used in</span></span>        | [<span data-ttu-id="66b1c-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="66b1c-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="66b1c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66b1c-200">Windows Server 2008</span></span>



| <span data-ttu-id="66b1c-201">進入</span><span class="sxs-lookup"><span data-stu-id="66b1c-201">Entry</span></span> | <span data-ttu-id="66b1c-202">值</span><span class="sxs-lookup"><span data-stu-id="66b1c-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="66b1c-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="66b1c-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66b1c-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="66b1c-205">System-Only</span></span>            | <span data-ttu-id="66b1c-206">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-206">True</span></span>                                         |
| <span data-ttu-id="66b1c-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="66b1c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="66b1c-208">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-208">True</span></span>                                         |
| <span data-ttu-id="66b1c-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="66b1c-209">Is Indexed</span></span>             | <span data-ttu-id="66b1c-210">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-210">False</span></span>                                        |
| <span data-ttu-id="66b1c-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="66b1c-211">In Global Catalog</span></span>      | <span data-ttu-id="66b1c-212">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-212">False</span></span>                                        |
| <span data-ttu-id="66b1c-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="66b1c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="66b1c-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="66b1c-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="66b1c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66b1c-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66b1c-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-217">Search-Flags</span></span>           | <span data-ttu-id="66b1c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66b1c-218">0x00000000</span></span>                                   |
| <span data-ttu-id="66b1c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-219">System-Flags</span></span>           | <span data-ttu-id="66b1c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66b1c-220">0x00000010</span></span>                                   |
| <span data-ttu-id="66b1c-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="66b1c-221">Classes used in</span></span>        | [<span data-ttu-id="66b1c-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="66b1c-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="66b1c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66b1c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="66b1c-224">進入</span><span class="sxs-lookup"><span data-stu-id="66b1c-224">Entry</span></span> | <span data-ttu-id="66b1c-225">值</span><span class="sxs-lookup"><span data-stu-id="66b1c-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="66b1c-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="66b1c-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66b1c-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="66b1c-228">System-Only</span></span>            | <span data-ttu-id="66b1c-229">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-229">True</span></span>                                         |
| <span data-ttu-id="66b1c-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="66b1c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="66b1c-231">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-231">True</span></span>                                         |
| <span data-ttu-id="66b1c-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="66b1c-232">Is Indexed</span></span>             | <span data-ttu-id="66b1c-233">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-233">False</span></span>                                        |
| <span data-ttu-id="66b1c-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="66b1c-234">In Global Catalog</span></span>      | <span data-ttu-id="66b1c-235">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-235">False</span></span>                                        |
| <span data-ttu-id="66b1c-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="66b1c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="66b1c-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="66b1c-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="66b1c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66b1c-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66b1c-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-240">Search-Flags</span></span>           | <span data-ttu-id="66b1c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66b1c-241">0x00000000</span></span>                                   |
| <span data-ttu-id="66b1c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-242">System-Flags</span></span>           | <span data-ttu-id="66b1c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66b1c-243">0x00000010</span></span>                                   |
| <span data-ttu-id="66b1c-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="66b1c-244">Classes used in</span></span>        | [<span data-ttu-id="66b1c-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="66b1c-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="66b1c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66b1c-246">Windows Server 2012</span></span>



| <span data-ttu-id="66b1c-247">進入</span><span class="sxs-lookup"><span data-stu-id="66b1c-247">Entry</span></span> | <span data-ttu-id="66b1c-248">值</span><span class="sxs-lookup"><span data-stu-id="66b1c-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="66b1c-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="66b1c-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66b1c-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="66b1c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="66b1c-251">System-Only</span></span>            | <span data-ttu-id="66b1c-252">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-252">True</span></span>                                         |
| <span data-ttu-id="66b1c-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="66b1c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="66b1c-254">對</span><span class="sxs-lookup"><span data-stu-id="66b1c-254">True</span></span>                                         |
| <span data-ttu-id="66b1c-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="66b1c-255">Is Indexed</span></span>             | <span data-ttu-id="66b1c-256">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-256">False</span></span>                                        |
| <span data-ttu-id="66b1c-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="66b1c-257">In Global Catalog</span></span>      | <span data-ttu-id="66b1c-258">否</span><span class="sxs-lookup"><span data-stu-id="66b1c-258">False</span></span>                                        |
| <span data-ttu-id="66b1c-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="66b1c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="66b1c-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="66b1c-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="66b1c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66b1c-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66b1c-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="66b1c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-263">Search-Flags</span></span>           | <span data-ttu-id="66b1c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66b1c-264">0x00000000</span></span>                                   |
| <span data-ttu-id="66b1c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66b1c-265">System-Flags</span></span>           | <span data-ttu-id="66b1c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66b1c-266">0x00000010</span></span>                                   |
| <span data-ttu-id="66b1c-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="66b1c-267">Classes used in</span></span>        | [<span data-ttu-id="66b1c-268">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="66b1c-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






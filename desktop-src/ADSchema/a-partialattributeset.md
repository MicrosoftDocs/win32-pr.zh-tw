---
title: 部分屬性集屬性
description: 追蹤部分複本的內部複寫狀態 (也就是在 Gc) 上。 部分複本 NC 物件的屬性。 定義特定部分複本 NC 上存在的屬性集。
ms.assetid: 2840d2b7-e186-4ef2-9107-f1e5c0c2f760
ms.tgt_platform: multiple
keywords:
- 部分屬性集屬性的 AD 架構
- partialAttributeSet 屬性 AD 架構
topic_type:
- apiref
api_name:
- Partial-Attribute-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932c07b0d4a8e3ea8f30f504194093d61912b7b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970262"
---
# <a name="partial-attribute-set-attribute"></a><span data-ttu-id="1ac4e-107">部分屬性集屬性</span><span class="sxs-lookup"><span data-stu-id="1ac4e-107">Partial-Attribute-Set attribute</span></span>

<span data-ttu-id="1ac4e-108">追蹤部分複本的內部複寫狀態 (也就是在 Gc) 上。</span><span class="sxs-lookup"><span data-stu-id="1ac4e-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="1ac4e-109">部分複本 NC 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ac4e-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="1ac4e-110">定義特定部分複本 NC 上存在的屬性集。</span><span class="sxs-lookup"><span data-stu-id="1ac4e-110">Defines the set of attributes present on a particular partial replica NC.</span></span>



| <span data-ttu-id="1ac4e-111">進入</span><span class="sxs-lookup"><span data-stu-id="1ac4e-111">Entry</span></span> | <span data-ttu-id="1ac4e-112">值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="1ac4e-113">CN</span><span class="sxs-lookup"><span data-stu-id="1ac4e-113">CN</span></span>                | <span data-ttu-id="1ac4e-114">部分屬性集</span><span class="sxs-lookup"><span data-stu-id="1ac4e-114">Partial-Attribute-Set</span></span>                                 |
| <span data-ttu-id="1ac4e-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1ac4e-115">Ldap-Display-Name</span></span> | <span data-ttu-id="1ac4e-116">partialAttributeSet</span><span class="sxs-lookup"><span data-stu-id="1ac4e-116">partialAttributeSet</span></span>                                   |
| <span data-ttu-id="1ac4e-117">大小</span><span class="sxs-lookup"><span data-stu-id="1ac4e-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="1ac4e-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1ac4e-118">Update Privilege</span></span>  | <span data-ttu-id="1ac4e-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="1ac4e-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="1ac4e-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1ac4e-120">Update Frequency</span></span>  | <span data-ttu-id="1ac4e-121">複寫期間</span><span class="sxs-lookup"><span data-stu-id="1ac4e-121">During replication</span></span>                                    |
| <span data-ttu-id="1ac4e-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ac4e-122">Attribute-Id</span></span>      | <span data-ttu-id="1ac4e-123">1.2.840.113556.1.4.640</span><span class="sxs-lookup"><span data-stu-id="1ac4e-123">1.2.840.113556.1.4.640</span></span>                                |
| <span data-ttu-id="1ac4e-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1ac4e-124">System-Id-Guid</span></span>    | <span data-ttu-id="1ac4e-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1ac4e-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span></span>                  |
| <span data-ttu-id="1ac4e-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ac4e-126">Syntax</span></span>            | [<span data-ttu-id="1ac4e-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="1ac4e-128">實作</span><span class="sxs-lookup"><span data-stu-id="1ac4e-128">Implementations</span></span>

-   [<span data-ttu-id="1ac4e-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1ac4e-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ac4e-131">**亞當**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1ac4e-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ac4e-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ac4e-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ac4e-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1ac4e-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ac4e-136">Windows 2000 Server</span></span>



| <span data-ttu-id="1ac4e-137">進入</span><span class="sxs-lookup"><span data-stu-id="1ac4e-137">Entry</span></span> | <span data-ttu-id="1ac4e-138">值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1ac4e-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ac4e-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ac4e-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ac4e-141">System-Only</span></span>            | <span data-ttu-id="1ac4e-142">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-142">True</span></span>                            |
| <span data-ttu-id="1ac4e-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-143">Is-Single-Valued</span></span>       | <span data-ttu-id="1ac4e-144">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-144">True</span></span>                            |
| <span data-ttu-id="1ac4e-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ac4e-145">Is Indexed</span></span>             | <span data-ttu-id="1ac4e-146">否</span><span class="sxs-lookup"><span data-stu-id="1ac4e-146">False</span></span>                           |
| <span data-ttu-id="1ac4e-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ac4e-147">In Global Catalog</span></span>      | <span data-ttu-id="1ac4e-148">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-148">True</span></span>                            |
| <span data-ttu-id="1ac4e-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ac4e-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ac4e-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ac4e-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1ac4e-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ac4e-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ac4e-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-153">Search-Flags</span></span>           | <span data-ttu-id="1ac4e-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ac4e-154">0x00000000</span></span>                      |
| <span data-ttu-id="1ac4e-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-155">System-Flags</span></span>           | <span data-ttu-id="1ac4e-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1ac4e-156">0x00000013</span></span>                      |
| <span data-ttu-id="1ac4e-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ac4e-157">Classes used in</span></span>        | [<span data-ttu-id="1ac4e-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1ac4e-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ac4e-159">Windows Server 2003</span></span>



| <span data-ttu-id="1ac4e-160">進入</span><span class="sxs-lookup"><span data-stu-id="1ac4e-160">Entry</span></span> | <span data-ttu-id="1ac4e-161">值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1ac4e-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ac4e-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ac4e-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ac4e-164">System-Only</span></span>            | <span data-ttu-id="1ac4e-165">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-165">True</span></span>                            |
| <span data-ttu-id="1ac4e-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-166">Is-Single-Valued</span></span>       | <span data-ttu-id="1ac4e-167">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-167">True</span></span>                            |
| <span data-ttu-id="1ac4e-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ac4e-168">Is Indexed</span></span>             | <span data-ttu-id="1ac4e-169">否</span><span class="sxs-lookup"><span data-stu-id="1ac4e-169">False</span></span>                           |
| <span data-ttu-id="1ac4e-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ac4e-170">In Global Catalog</span></span>      | <span data-ttu-id="1ac4e-171">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-171">True</span></span>                            |
| <span data-ttu-id="1ac4e-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ac4e-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ac4e-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ac4e-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1ac4e-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ac4e-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ac4e-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-176">Search-Flags</span></span>           | <span data-ttu-id="1ac4e-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ac4e-177">0x00000000</span></span>                      |
| <span data-ttu-id="1ac4e-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-178">System-Flags</span></span>           | <span data-ttu-id="1ac4e-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1ac4e-179">0x00000013</span></span>                      |
| <span data-ttu-id="1ac4e-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ac4e-180">Classes used in</span></span>        | [<span data-ttu-id="1ac4e-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1ac4e-182">亞當</span><span class="sxs-lookup"><span data-stu-id="1ac4e-182">ADAM</span></span>



| <span data-ttu-id="1ac4e-183">進入</span><span class="sxs-lookup"><span data-stu-id="1ac4e-183">Entry</span></span> | <span data-ttu-id="1ac4e-184">值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1ac4e-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ac4e-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ac4e-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ac4e-187">System-Only</span></span>            | <span data-ttu-id="1ac4e-188">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-188">True</span></span>                            |
| <span data-ttu-id="1ac4e-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-189">Is-Single-Valued</span></span>       | <span data-ttu-id="1ac4e-190">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-190">True</span></span>                            |
| <span data-ttu-id="1ac4e-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ac4e-191">Is Indexed</span></span>             | <span data-ttu-id="1ac4e-192">否</span><span class="sxs-lookup"><span data-stu-id="1ac4e-192">False</span></span>                           |
| <span data-ttu-id="1ac4e-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ac4e-193">In Global Catalog</span></span>      | <span data-ttu-id="1ac4e-194">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-194">True</span></span>                            |
| <span data-ttu-id="1ac4e-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ac4e-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ac4e-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ac4e-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1ac4e-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ac4e-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ac4e-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-199">Search-Flags</span></span>           | <span data-ttu-id="1ac4e-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ac4e-200">0x00000000</span></span>                      |
| <span data-ttu-id="1ac4e-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-201">System-Flags</span></span>           | <span data-ttu-id="1ac4e-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1ac4e-202">0x00000013</span></span>                      |
| <span data-ttu-id="1ac4e-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ac4e-203">Classes used in</span></span>        | [<span data-ttu-id="1ac4e-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ac4e-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ac4e-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ac4e-206">進入</span><span class="sxs-lookup"><span data-stu-id="1ac4e-206">Entry</span></span> | <span data-ttu-id="1ac4e-207">值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1ac4e-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ac4e-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ac4e-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ac4e-210">System-Only</span></span>            | <span data-ttu-id="1ac4e-211">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-211">True</span></span>                            |
| <span data-ttu-id="1ac4e-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="1ac4e-213">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-213">True</span></span>                            |
| <span data-ttu-id="1ac4e-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ac4e-214">Is Indexed</span></span>             | <span data-ttu-id="1ac4e-215">否</span><span class="sxs-lookup"><span data-stu-id="1ac4e-215">False</span></span>                           |
| <span data-ttu-id="1ac4e-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ac4e-216">In Global Catalog</span></span>      | <span data-ttu-id="1ac4e-217">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-217">True</span></span>                            |
| <span data-ttu-id="1ac4e-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ac4e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ac4e-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ac4e-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1ac4e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ac4e-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ac4e-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-222">Search-Flags</span></span>           | <span data-ttu-id="1ac4e-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ac4e-223">0x00000000</span></span>                      |
| <span data-ttu-id="1ac4e-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-224">System-Flags</span></span>           | <span data-ttu-id="1ac4e-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1ac4e-225">0x00000013</span></span>                      |
| <span data-ttu-id="1ac4e-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ac4e-226">Classes used in</span></span>        | [<span data-ttu-id="1ac4e-227">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ac4e-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ac4e-228">Windows Server 2008</span></span>



| <span data-ttu-id="1ac4e-229">進入</span><span class="sxs-lookup"><span data-stu-id="1ac4e-229">Entry</span></span> | <span data-ttu-id="1ac4e-230">值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1ac4e-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ac4e-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ac4e-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ac4e-233">System-Only</span></span>            | <span data-ttu-id="1ac4e-234">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-234">True</span></span>                            |
| <span data-ttu-id="1ac4e-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-235">Is-Single-Valued</span></span>       | <span data-ttu-id="1ac4e-236">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-236">True</span></span>                            |
| <span data-ttu-id="1ac4e-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ac4e-237">Is Indexed</span></span>             | <span data-ttu-id="1ac4e-238">否</span><span class="sxs-lookup"><span data-stu-id="1ac4e-238">False</span></span>                           |
| <span data-ttu-id="1ac4e-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ac4e-239">In Global Catalog</span></span>      | <span data-ttu-id="1ac4e-240">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-240">True</span></span>                            |
| <span data-ttu-id="1ac4e-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ac4e-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ac4e-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ac4e-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1ac4e-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ac4e-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ac4e-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-245">Search-Flags</span></span>           | <span data-ttu-id="1ac4e-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ac4e-246">0x00000000</span></span>                      |
| <span data-ttu-id="1ac4e-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-247">System-Flags</span></span>           | <span data-ttu-id="1ac4e-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1ac4e-248">0x00000013</span></span>                      |
| <span data-ttu-id="1ac4e-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ac4e-249">Classes used in</span></span>        | [<span data-ttu-id="1ac4e-250">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ac4e-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ac4e-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ac4e-252">進入</span><span class="sxs-lookup"><span data-stu-id="1ac4e-252">Entry</span></span> | <span data-ttu-id="1ac4e-253">值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1ac4e-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ac4e-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ac4e-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ac4e-256">System-Only</span></span>            | <span data-ttu-id="1ac4e-257">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-257">True</span></span>                            |
| <span data-ttu-id="1ac4e-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-258">Is-Single-Valued</span></span>       | <span data-ttu-id="1ac4e-259">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-259">True</span></span>                            |
| <span data-ttu-id="1ac4e-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ac4e-260">Is Indexed</span></span>             | <span data-ttu-id="1ac4e-261">否</span><span class="sxs-lookup"><span data-stu-id="1ac4e-261">False</span></span>                           |
| <span data-ttu-id="1ac4e-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ac4e-262">In Global Catalog</span></span>      | <span data-ttu-id="1ac4e-263">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-263">True</span></span>                            |
| <span data-ttu-id="1ac4e-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ac4e-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ac4e-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ac4e-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1ac4e-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ac4e-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ac4e-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-268">Search-Flags</span></span>           | <span data-ttu-id="1ac4e-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ac4e-269">0x00000000</span></span>                      |
| <span data-ttu-id="1ac4e-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-270">System-Flags</span></span>           | <span data-ttu-id="1ac4e-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1ac4e-271">0x00000013</span></span>                      |
| <span data-ttu-id="1ac4e-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ac4e-272">Classes used in</span></span>        | [<span data-ttu-id="1ac4e-273">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ac4e-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ac4e-274">Windows Server 2012</span></span>



| <span data-ttu-id="1ac4e-275">進入</span><span class="sxs-lookup"><span data-stu-id="1ac4e-275">Entry</span></span> | <span data-ttu-id="1ac4e-276">值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1ac4e-277">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ac4e-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ac4e-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1ac4e-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ac4e-279">System-Only</span></span>            | <span data-ttu-id="1ac4e-280">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-280">True</span></span>                            |
| <span data-ttu-id="1ac4e-281">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ac4e-281">Is-Single-Valued</span></span>       | <span data-ttu-id="1ac4e-282">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-282">True</span></span>                            |
| <span data-ttu-id="1ac4e-283">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ac4e-283">Is Indexed</span></span>             | <span data-ttu-id="1ac4e-284">否</span><span class="sxs-lookup"><span data-stu-id="1ac4e-284">False</span></span>                           |
| <span data-ttu-id="1ac4e-285">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ac4e-285">In Global Catalog</span></span>      | <span data-ttu-id="1ac4e-286">對</span><span class="sxs-lookup"><span data-stu-id="1ac4e-286">True</span></span>                            |
| <span data-ttu-id="1ac4e-287">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ac4e-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ac4e-288">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ac4e-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1ac4e-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ac4e-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ac4e-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1ac4e-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-291">Search-Flags</span></span>           | <span data-ttu-id="1ac4e-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ac4e-292">0x00000000</span></span>                      |
| <span data-ttu-id="1ac4e-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ac4e-293">System-Flags</span></span>           | <span data-ttu-id="1ac4e-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1ac4e-294">0x00000013</span></span>                      |
| <span data-ttu-id="1ac4e-295">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ac4e-295">Classes used in</span></span>        | [<span data-ttu-id="1ac4e-296">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="1ac4e-296">**Top**</span></span>](c-top.md)<br/> |



 

 






---
title: Dns-Record 屬性
description: 用來將二進位 DNS 資源記錄儲存在 DNS 物件上。
ms.assetid: 2d5a17da-0efc-450e-b247-3ab6d2de3a5d
ms.tgt_platform: multiple
keywords:
- Dns-Record 屬性 AD 架構
- dnsRecord 屬性 AD 架構
topic_type:
- apiref
api_name:
- Dns-Record
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 013fa5ef4a9fcec151f996c347cdfd525438aa7d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108213"
---
# <a name="dns-record-attribute"></a><span data-ttu-id="0e028-105">Dns-Record 屬性</span><span class="sxs-lookup"><span data-stu-id="0e028-105">Dns-Record attribute</span></span>

<span data-ttu-id="0e028-106">用來將二進位 DNS 資源記錄儲存在 DNS 物件上。</span><span class="sxs-lookup"><span data-stu-id="0e028-106">Used to store binary DNS resource records on DNS objects.</span></span>



| <span data-ttu-id="0e028-107">進入</span><span class="sxs-lookup"><span data-stu-id="0e028-107">Entry</span></span> | <span data-ttu-id="0e028-108">值</span><span class="sxs-lookup"><span data-stu-id="0e028-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0e028-109">CN</span><span class="sxs-lookup"><span data-stu-id="0e028-109">CN</span></span>                | <span data-ttu-id="0e028-110">Dns-Record</span><span class="sxs-lookup"><span data-stu-id="0e028-110">Dns-Record</span></span>                                            |
| <span data-ttu-id="0e028-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0e028-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0e028-112">dnsRecord</span><span class="sxs-lookup"><span data-stu-id="0e028-112">dnsRecord</span></span>                                             |
| <span data-ttu-id="0e028-113">大小</span><span class="sxs-lookup"><span data-stu-id="0e028-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="0e028-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0e028-114">Update Privilege</span></span>  | <span data-ttu-id="0e028-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="0e028-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="0e028-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0e028-116">Update Frequency</span></span>  | <span data-ttu-id="0e028-117">DNS 資源記錄變更時。</span><span class="sxs-lookup"><span data-stu-id="0e028-117">Whenever DNS resource records change.</span></span>                 |
| <span data-ttu-id="0e028-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0e028-118">Attribute-Id</span></span>      | <span data-ttu-id="0e028-119">1.2.840.113556.1.4.382</span><span class="sxs-lookup"><span data-stu-id="0e028-119">1.2.840.113556.1.4.382</span></span>                                |
| <span data-ttu-id="0e028-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0e028-120">System-Id-Guid</span></span>    | <span data-ttu-id="0e028-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="0e028-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="0e028-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e028-122">Syntax</span></span>            | [<span data-ttu-id="0e028-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="0e028-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0e028-124">實作</span><span class="sxs-lookup"><span data-stu-id="0e028-124">Implementations</span></span>

-   [<span data-ttu-id="0e028-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0e028-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0e028-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0e028-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0e028-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0e028-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0e028-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0e028-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0e028-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0e028-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0e028-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0e028-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0e028-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0e028-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0e028-132">進入</span><span class="sxs-lookup"><span data-stu-id="0e028-132">Entry</span></span> | <span data-ttu-id="0e028-133">值</span><span class="sxs-lookup"><span data-stu-id="0e028-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e028-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e028-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e028-135">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e028-136">System-Only</span></span>            | <span data-ttu-id="0e028-137">否</span><span class="sxs-lookup"><span data-stu-id="0e028-137">False</span></span>                                    |
| <span data-ttu-id="0e028-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e028-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0e028-139">否</span><span class="sxs-lookup"><span data-stu-id="0e028-139">False</span></span>                                    |
| <span data-ttu-id="0e028-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e028-140">Is Indexed</span></span>             | <span data-ttu-id="0e028-141">否</span><span class="sxs-lookup"><span data-stu-id="0e028-141">False</span></span>                                    |
| <span data-ttu-id="0e028-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e028-142">In Global Catalog</span></span>      | <span data-ttu-id="0e028-143">否</span><span class="sxs-lookup"><span data-stu-id="0e028-143">False</span></span>                                    |
| <span data-ttu-id="0e028-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e028-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e028-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e028-145">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e028-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e028-146">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e028-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e028-147">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e028-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-148">Search-Flags</span></span>           | <span data-ttu-id="0e028-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e028-149">0x00000000</span></span>                               |
| <span data-ttu-id="0e028-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-150">System-Flags</span></span>           | <span data-ttu-id="0e028-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e028-151">0x00000010</span></span>                               |
| <span data-ttu-id="0e028-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e028-152">Classes used in</span></span>        | [<span data-ttu-id="0e028-153">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="0e028-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0e028-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0e028-154">Windows Server 2003</span></span>



| <span data-ttu-id="0e028-155">進入</span><span class="sxs-lookup"><span data-stu-id="0e028-155">Entry</span></span> | <span data-ttu-id="0e028-156">值</span><span class="sxs-lookup"><span data-stu-id="0e028-156">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e028-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e028-157">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e028-158">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e028-159">System-Only</span></span>            | <span data-ttu-id="0e028-160">否</span><span class="sxs-lookup"><span data-stu-id="0e028-160">False</span></span>                                    |
| <span data-ttu-id="0e028-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e028-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0e028-162">否</span><span class="sxs-lookup"><span data-stu-id="0e028-162">False</span></span>                                    |
| <span data-ttu-id="0e028-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e028-163">Is Indexed</span></span>             | <span data-ttu-id="0e028-164">否</span><span class="sxs-lookup"><span data-stu-id="0e028-164">False</span></span>                                    |
| <span data-ttu-id="0e028-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e028-165">In Global Catalog</span></span>      | <span data-ttu-id="0e028-166">否</span><span class="sxs-lookup"><span data-stu-id="0e028-166">False</span></span>                                    |
| <span data-ttu-id="0e028-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e028-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e028-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e028-168">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e028-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e028-169">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e028-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e028-170">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e028-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-171">Search-Flags</span></span>           | <span data-ttu-id="0e028-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e028-172">0x00000000</span></span>                               |
| <span data-ttu-id="0e028-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-173">System-Flags</span></span>           | <span data-ttu-id="0e028-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e028-174">0x00000010</span></span>                               |
| <span data-ttu-id="0e028-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e028-175">Classes used in</span></span>        | [<span data-ttu-id="0e028-176">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="0e028-176">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0e028-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0e028-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0e028-178">進入</span><span class="sxs-lookup"><span data-stu-id="0e028-178">Entry</span></span> | <span data-ttu-id="0e028-179">值</span><span class="sxs-lookup"><span data-stu-id="0e028-179">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e028-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e028-180">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e028-181">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e028-182">System-Only</span></span>            | <span data-ttu-id="0e028-183">否</span><span class="sxs-lookup"><span data-stu-id="0e028-183">False</span></span>                                    |
| <span data-ttu-id="0e028-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e028-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0e028-185">否</span><span class="sxs-lookup"><span data-stu-id="0e028-185">False</span></span>                                    |
| <span data-ttu-id="0e028-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e028-186">Is Indexed</span></span>             | <span data-ttu-id="0e028-187">否</span><span class="sxs-lookup"><span data-stu-id="0e028-187">False</span></span>                                    |
| <span data-ttu-id="0e028-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e028-188">In Global Catalog</span></span>      | <span data-ttu-id="0e028-189">否</span><span class="sxs-lookup"><span data-stu-id="0e028-189">False</span></span>                                    |
| <span data-ttu-id="0e028-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e028-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e028-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e028-191">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e028-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e028-192">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e028-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e028-193">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e028-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-194">Search-Flags</span></span>           | <span data-ttu-id="0e028-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e028-195">0x00000000</span></span>                               |
| <span data-ttu-id="0e028-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-196">System-Flags</span></span>           | <span data-ttu-id="0e028-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e028-197">0x00000010</span></span>                               |
| <span data-ttu-id="0e028-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e028-198">Classes used in</span></span>        | [<span data-ttu-id="0e028-199">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="0e028-199">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0e028-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e028-200">Windows Server 2008</span></span>



| <span data-ttu-id="0e028-201">進入</span><span class="sxs-lookup"><span data-stu-id="0e028-201">Entry</span></span> | <span data-ttu-id="0e028-202">值</span><span class="sxs-lookup"><span data-stu-id="0e028-202">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e028-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e028-203">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e028-204">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e028-205">System-Only</span></span>            | <span data-ttu-id="0e028-206">否</span><span class="sxs-lookup"><span data-stu-id="0e028-206">False</span></span>                                    |
| <span data-ttu-id="0e028-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e028-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0e028-208">否</span><span class="sxs-lookup"><span data-stu-id="0e028-208">False</span></span>                                    |
| <span data-ttu-id="0e028-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e028-209">Is Indexed</span></span>             | <span data-ttu-id="0e028-210">否</span><span class="sxs-lookup"><span data-stu-id="0e028-210">False</span></span>                                    |
| <span data-ttu-id="0e028-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e028-211">In Global Catalog</span></span>      | <span data-ttu-id="0e028-212">否</span><span class="sxs-lookup"><span data-stu-id="0e028-212">False</span></span>                                    |
| <span data-ttu-id="0e028-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e028-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e028-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e028-214">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e028-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e028-215">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e028-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e028-216">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e028-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-217">Search-Flags</span></span>           | <span data-ttu-id="0e028-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e028-218">0x00000000</span></span>                               |
| <span data-ttu-id="0e028-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-219">System-Flags</span></span>           | <span data-ttu-id="0e028-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e028-220">0x00000010</span></span>                               |
| <span data-ttu-id="0e028-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e028-221">Classes used in</span></span>        | [<span data-ttu-id="0e028-222">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="0e028-222">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0e028-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e028-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0e028-224">進入</span><span class="sxs-lookup"><span data-stu-id="0e028-224">Entry</span></span> | <span data-ttu-id="0e028-225">值</span><span class="sxs-lookup"><span data-stu-id="0e028-225">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e028-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e028-226">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e028-227">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e028-228">System-Only</span></span>            | <span data-ttu-id="0e028-229">否</span><span class="sxs-lookup"><span data-stu-id="0e028-229">False</span></span>                                    |
| <span data-ttu-id="0e028-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e028-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0e028-231">否</span><span class="sxs-lookup"><span data-stu-id="0e028-231">False</span></span>                                    |
| <span data-ttu-id="0e028-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e028-232">Is Indexed</span></span>             | <span data-ttu-id="0e028-233">否</span><span class="sxs-lookup"><span data-stu-id="0e028-233">False</span></span>                                    |
| <span data-ttu-id="0e028-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e028-234">In Global Catalog</span></span>      | <span data-ttu-id="0e028-235">否</span><span class="sxs-lookup"><span data-stu-id="0e028-235">False</span></span>                                    |
| <span data-ttu-id="0e028-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e028-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e028-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e028-237">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e028-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e028-238">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e028-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e028-239">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e028-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-240">Search-Flags</span></span>           | <span data-ttu-id="0e028-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e028-241">0x00000000</span></span>                               |
| <span data-ttu-id="0e028-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-242">System-Flags</span></span>           | <span data-ttu-id="0e028-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e028-243">0x00000010</span></span>                               |
| <span data-ttu-id="0e028-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e028-244">Classes used in</span></span>        | [<span data-ttu-id="0e028-245">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="0e028-245">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0e028-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e028-246">Windows Server 2012</span></span>



| <span data-ttu-id="0e028-247">進入</span><span class="sxs-lookup"><span data-stu-id="0e028-247">Entry</span></span> | <span data-ttu-id="0e028-248">值</span><span class="sxs-lookup"><span data-stu-id="0e028-248">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e028-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e028-249">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e028-250">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e028-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e028-251">System-Only</span></span>            | <span data-ttu-id="0e028-252">否</span><span class="sxs-lookup"><span data-stu-id="0e028-252">False</span></span>                                    |
| <span data-ttu-id="0e028-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e028-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0e028-254">否</span><span class="sxs-lookup"><span data-stu-id="0e028-254">False</span></span>                                    |
| <span data-ttu-id="0e028-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e028-255">Is Indexed</span></span>             | <span data-ttu-id="0e028-256">否</span><span class="sxs-lookup"><span data-stu-id="0e028-256">False</span></span>                                    |
| <span data-ttu-id="0e028-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e028-257">In Global Catalog</span></span>      | <span data-ttu-id="0e028-258">否</span><span class="sxs-lookup"><span data-stu-id="0e028-258">False</span></span>                                    |
| <span data-ttu-id="0e028-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e028-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e028-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e028-260">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e028-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e028-261">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e028-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e028-262">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e028-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-263">Search-Flags</span></span>           | <span data-ttu-id="0e028-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e028-264">0x00000000</span></span>                               |
| <span data-ttu-id="0e028-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e028-265">System-Flags</span></span>           | <span data-ttu-id="0e028-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e028-266">0x00000010</span></span>                               |
| <span data-ttu-id="0e028-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e028-267">Classes used in</span></span>        | [<span data-ttu-id="0e028-268">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="0e028-268">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 






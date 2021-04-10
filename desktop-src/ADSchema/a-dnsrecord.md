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
# <a name="dns-record-attribute"></a><span data-ttu-id="4ccdf-105">Dns-Record 屬性</span><span class="sxs-lookup"><span data-stu-id="4ccdf-105">Dns-Record attribute</span></span>

<span data-ttu-id="4ccdf-106">用來將二進位 DNS 資源記錄儲存在 DNS 物件上。</span><span class="sxs-lookup"><span data-stu-id="4ccdf-106">Used to store binary DNS resource records on DNS objects.</span></span>



| <span data-ttu-id="4ccdf-107">進入</span><span class="sxs-lookup"><span data-stu-id="4ccdf-107">Entry</span></span> | <span data-ttu-id="4ccdf-108">值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="4ccdf-109">CN</span><span class="sxs-lookup"><span data-stu-id="4ccdf-109">CN</span></span>                | <span data-ttu-id="4ccdf-110">Dns-Record</span><span class="sxs-lookup"><span data-stu-id="4ccdf-110">Dns-Record</span></span>                                            |
| <span data-ttu-id="4ccdf-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4ccdf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4ccdf-112">dnsRecord</span><span class="sxs-lookup"><span data-stu-id="4ccdf-112">dnsRecord</span></span>                                             |
| <span data-ttu-id="4ccdf-113">大小</span><span class="sxs-lookup"><span data-stu-id="4ccdf-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="4ccdf-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4ccdf-114">Update Privilege</span></span>  | <span data-ttu-id="4ccdf-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="4ccdf-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="4ccdf-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4ccdf-116">Update Frequency</span></span>  | <span data-ttu-id="4ccdf-117">DNS 資源記錄變更時。</span><span class="sxs-lookup"><span data-stu-id="4ccdf-117">Whenever DNS resource records change.</span></span>                 |
| <span data-ttu-id="4ccdf-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4ccdf-118">Attribute-Id</span></span>      | <span data-ttu-id="4ccdf-119">1.2.840.113556.1.4.382</span><span class="sxs-lookup"><span data-stu-id="4ccdf-119">1.2.840.113556.1.4.382</span></span>                                |
| <span data-ttu-id="4ccdf-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4ccdf-120">System-Id-Guid</span></span>    | <span data-ttu-id="4ccdf-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="4ccdf-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="4ccdf-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ccdf-122">Syntax</span></span>            | [<span data-ttu-id="4ccdf-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="4ccdf-124">實作</span><span class="sxs-lookup"><span data-stu-id="4ccdf-124">Implementations</span></span>

-   [<span data-ttu-id="4ccdf-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4ccdf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4ccdf-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4ccdf-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4ccdf-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4ccdf-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4ccdf-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ccdf-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4ccdf-132">進入</span><span class="sxs-lookup"><span data-stu-id="4ccdf-132">Entry</span></span> | <span data-ttu-id="4ccdf-133">值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4ccdf-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ccdf-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ccdf-135">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ccdf-136">System-Only</span></span>            | <span data-ttu-id="4ccdf-137">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-137">False</span></span>                                    |
| <span data-ttu-id="4ccdf-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4ccdf-139">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-139">False</span></span>                                    |
| <span data-ttu-id="4ccdf-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ccdf-140">Is Indexed</span></span>             | <span data-ttu-id="4ccdf-141">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-141">False</span></span>                                    |
| <span data-ttu-id="4ccdf-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ccdf-142">In Global Catalog</span></span>      | <span data-ttu-id="4ccdf-143">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-143">False</span></span>                                    |
| <span data-ttu-id="4ccdf-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ccdf-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ccdf-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ccdf-145">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4ccdf-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ccdf-146">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ccdf-147">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-148">Search-Flags</span></span>           | <span data-ttu-id="4ccdf-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ccdf-149">0x00000000</span></span>                               |
| <span data-ttu-id="4ccdf-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-150">System-Flags</span></span>           | <span data-ttu-id="4ccdf-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ccdf-151">0x00000010</span></span>                               |
| <span data-ttu-id="4ccdf-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ccdf-152">Classes used in</span></span>        | [<span data-ttu-id="4ccdf-153">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4ccdf-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ccdf-154">Windows Server 2003</span></span>



| <span data-ttu-id="4ccdf-155">進入</span><span class="sxs-lookup"><span data-stu-id="4ccdf-155">Entry</span></span> | <span data-ttu-id="4ccdf-156">值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-156">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4ccdf-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ccdf-157">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ccdf-158">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ccdf-159">System-Only</span></span>            | <span data-ttu-id="4ccdf-160">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-160">False</span></span>                                    |
| <span data-ttu-id="4ccdf-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4ccdf-162">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-162">False</span></span>                                    |
| <span data-ttu-id="4ccdf-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ccdf-163">Is Indexed</span></span>             | <span data-ttu-id="4ccdf-164">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-164">False</span></span>                                    |
| <span data-ttu-id="4ccdf-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ccdf-165">In Global Catalog</span></span>      | <span data-ttu-id="4ccdf-166">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-166">False</span></span>                                    |
| <span data-ttu-id="4ccdf-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ccdf-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ccdf-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ccdf-168">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4ccdf-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ccdf-169">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ccdf-170">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-171">Search-Flags</span></span>           | <span data-ttu-id="4ccdf-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ccdf-172">0x00000000</span></span>                               |
| <span data-ttu-id="4ccdf-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-173">System-Flags</span></span>           | <span data-ttu-id="4ccdf-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ccdf-174">0x00000010</span></span>                               |
| <span data-ttu-id="4ccdf-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ccdf-175">Classes used in</span></span>        | [<span data-ttu-id="4ccdf-176">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-176">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4ccdf-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4ccdf-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4ccdf-178">進入</span><span class="sxs-lookup"><span data-stu-id="4ccdf-178">Entry</span></span> | <span data-ttu-id="4ccdf-179">值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-179">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4ccdf-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ccdf-180">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ccdf-181">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ccdf-182">System-Only</span></span>            | <span data-ttu-id="4ccdf-183">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-183">False</span></span>                                    |
| <span data-ttu-id="4ccdf-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4ccdf-185">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-185">False</span></span>                                    |
| <span data-ttu-id="4ccdf-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ccdf-186">Is Indexed</span></span>             | <span data-ttu-id="4ccdf-187">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-187">False</span></span>                                    |
| <span data-ttu-id="4ccdf-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ccdf-188">In Global Catalog</span></span>      | <span data-ttu-id="4ccdf-189">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-189">False</span></span>                                    |
| <span data-ttu-id="4ccdf-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ccdf-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ccdf-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ccdf-191">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4ccdf-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ccdf-192">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ccdf-193">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-194">Search-Flags</span></span>           | <span data-ttu-id="4ccdf-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ccdf-195">0x00000000</span></span>                               |
| <span data-ttu-id="4ccdf-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-196">System-Flags</span></span>           | <span data-ttu-id="4ccdf-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ccdf-197">0x00000010</span></span>                               |
| <span data-ttu-id="4ccdf-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ccdf-198">Classes used in</span></span>        | [<span data-ttu-id="4ccdf-199">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-199">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4ccdf-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ccdf-200">Windows Server 2008</span></span>



| <span data-ttu-id="4ccdf-201">進入</span><span class="sxs-lookup"><span data-stu-id="4ccdf-201">Entry</span></span> | <span data-ttu-id="4ccdf-202">值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-202">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4ccdf-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ccdf-203">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ccdf-204">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ccdf-205">System-Only</span></span>            | <span data-ttu-id="4ccdf-206">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-206">False</span></span>                                    |
| <span data-ttu-id="4ccdf-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4ccdf-208">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-208">False</span></span>                                    |
| <span data-ttu-id="4ccdf-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ccdf-209">Is Indexed</span></span>             | <span data-ttu-id="4ccdf-210">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-210">False</span></span>                                    |
| <span data-ttu-id="4ccdf-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ccdf-211">In Global Catalog</span></span>      | <span data-ttu-id="4ccdf-212">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-212">False</span></span>                                    |
| <span data-ttu-id="4ccdf-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ccdf-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ccdf-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ccdf-214">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4ccdf-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ccdf-215">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ccdf-216">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-217">Search-Flags</span></span>           | <span data-ttu-id="4ccdf-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ccdf-218">0x00000000</span></span>                               |
| <span data-ttu-id="4ccdf-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-219">System-Flags</span></span>           | <span data-ttu-id="4ccdf-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ccdf-220">0x00000010</span></span>                               |
| <span data-ttu-id="4ccdf-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ccdf-221">Classes used in</span></span>        | [<span data-ttu-id="4ccdf-222">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-222">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4ccdf-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ccdf-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4ccdf-224">進入</span><span class="sxs-lookup"><span data-stu-id="4ccdf-224">Entry</span></span> | <span data-ttu-id="4ccdf-225">值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-225">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4ccdf-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ccdf-226">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ccdf-227">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ccdf-228">System-Only</span></span>            | <span data-ttu-id="4ccdf-229">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-229">False</span></span>                                    |
| <span data-ttu-id="4ccdf-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4ccdf-231">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-231">False</span></span>                                    |
| <span data-ttu-id="4ccdf-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ccdf-232">Is Indexed</span></span>             | <span data-ttu-id="4ccdf-233">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-233">False</span></span>                                    |
| <span data-ttu-id="4ccdf-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ccdf-234">In Global Catalog</span></span>      | <span data-ttu-id="4ccdf-235">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-235">False</span></span>                                    |
| <span data-ttu-id="4ccdf-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ccdf-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ccdf-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ccdf-237">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4ccdf-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ccdf-238">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ccdf-239">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-240">Search-Flags</span></span>           | <span data-ttu-id="4ccdf-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ccdf-241">0x00000000</span></span>                               |
| <span data-ttu-id="4ccdf-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-242">System-Flags</span></span>           | <span data-ttu-id="4ccdf-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ccdf-243">0x00000010</span></span>                               |
| <span data-ttu-id="4ccdf-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ccdf-244">Classes used in</span></span>        | [<span data-ttu-id="4ccdf-245">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-245">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4ccdf-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ccdf-246">Windows Server 2012</span></span>



| <span data-ttu-id="4ccdf-247">進入</span><span class="sxs-lookup"><span data-stu-id="4ccdf-247">Entry</span></span> | <span data-ttu-id="4ccdf-248">值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-248">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4ccdf-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ccdf-249">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ccdf-250">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4ccdf-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ccdf-251">System-Only</span></span>            | <span data-ttu-id="4ccdf-252">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-252">False</span></span>                                    |
| <span data-ttu-id="4ccdf-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ccdf-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4ccdf-254">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-254">False</span></span>                                    |
| <span data-ttu-id="4ccdf-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ccdf-255">Is Indexed</span></span>             | <span data-ttu-id="4ccdf-256">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-256">False</span></span>                                    |
| <span data-ttu-id="4ccdf-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ccdf-257">In Global Catalog</span></span>      | <span data-ttu-id="4ccdf-258">否</span><span class="sxs-lookup"><span data-stu-id="4ccdf-258">False</span></span>                                    |
| <span data-ttu-id="4ccdf-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ccdf-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ccdf-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ccdf-260">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4ccdf-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ccdf-261">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ccdf-262">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4ccdf-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-263">Search-Flags</span></span>           | <span data-ttu-id="4ccdf-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ccdf-264">0x00000000</span></span>                               |
| <span data-ttu-id="4ccdf-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ccdf-265">System-Flags</span></span>           | <span data-ttu-id="4ccdf-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ccdf-266">0x00000010</span></span>                               |
| <span data-ttu-id="4ccdf-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ccdf-267">Classes used in</span></span>        | [<span data-ttu-id="4ccdf-268">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="4ccdf-268">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 






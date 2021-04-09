---
title: Domain-Replica 屬性
description: Unicode 字串屬性，提供 Windows NT 4.0 複寫網域控制站的清單。
ms.assetid: 973fe504-0c3e-4a7f-9a9e-0e5274ac7817
ms.tgt_platform: multiple
keywords:
- Domain-Replica 屬性 AD 架構
- domainReplica 屬性 AD 架構
topic_type:
- apiref
api_name:
- Domain-Replica
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfc5119c15047fc6d3b7c15947d996b7f387957
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844755"
---
# <a name="domain-replica-attribute"></a><span data-ttu-id="9df3a-105">Domain-Replica 屬性</span><span class="sxs-lookup"><span data-stu-id="9df3a-105">Domain-Replica attribute</span></span>

<span data-ttu-id="9df3a-106">Unicode 字串屬性，提供 Windows NT 4.0 複寫網域控制站的清單。</span><span class="sxs-lookup"><span data-stu-id="9df3a-106">Unicode String Attribute, gives the list of Windows NT 4.0 Replication Domain Controllers.</span></span>



| <span data-ttu-id="9df3a-107">進入</span><span class="sxs-lookup"><span data-stu-id="9df3a-107">Entry</span></span> | <span data-ttu-id="9df3a-108">值</span><span class="sxs-lookup"><span data-stu-id="9df3a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9df3a-109">CN</span><span class="sxs-lookup"><span data-stu-id="9df3a-109">CN</span></span>                | <span data-ttu-id="9df3a-110">Domain-Replica</span><span class="sxs-lookup"><span data-stu-id="9df3a-110">Domain-Replica</span></span>                              |
| <span data-ttu-id="9df3a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9df3a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9df3a-112">domainReplica</span><span class="sxs-lookup"><span data-stu-id="9df3a-112">domainReplica</span></span>                               |
| <span data-ttu-id="9df3a-113">大小</span><span class="sxs-lookup"><span data-stu-id="9df3a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9df3a-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9df3a-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9df3a-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9df3a-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9df3a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9df3a-116">Attribute-Id</span></span>      | <span data-ttu-id="9df3a-117">1.2.840.113556.1.4.158</span><span class="sxs-lookup"><span data-stu-id="9df3a-117">1.2.840.113556.1.4.158</span></span>                      |
| <span data-ttu-id="9df3a-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9df3a-118">System-Id-Guid</span></span>    | <span data-ttu-id="9df3a-119">bf96795e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9df3a-119">bf96795e-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="9df3a-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="9df3a-120">Syntax</span></span>            | [<span data-ttu-id="9df3a-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9df3a-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9df3a-122">實作</span><span class="sxs-lookup"><span data-stu-id="9df3a-122">Implementations</span></span>

-   [<span data-ttu-id="9df3a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9df3a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9df3a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9df3a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9df3a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9df3a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9df3a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9df3a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9df3a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9df3a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9df3a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9df3a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9df3a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9df3a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9df3a-130">進入</span><span class="sxs-lookup"><span data-stu-id="9df3a-130">Entry</span></span> | <span data-ttu-id="9df3a-131">值</span><span class="sxs-lookup"><span data-stu-id="9df3a-131">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="9df3a-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9df3a-132">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9df3a-133">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9df3a-134">System-Only</span></span>            | <span data-ttu-id="9df3a-135">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-135">False</span></span>                                                 |
| <span data-ttu-id="9df3a-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9df3a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9df3a-137">對</span><span class="sxs-lookup"><span data-stu-id="9df3a-137">True</span></span>                                                  |
| <span data-ttu-id="9df3a-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9df3a-138">Is Indexed</span></span>             | <span data-ttu-id="9df3a-139">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-139">False</span></span>                                                 |
| <span data-ttu-id="9df3a-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9df3a-140">In Global Catalog</span></span>      | <span data-ttu-id="9df3a-141">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-141">False</span></span>                                                 |
| <span data-ttu-id="9df3a-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9df3a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9df3a-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9df3a-143">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="9df3a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9df3a-144">Range-Lower</span></span>            | <span data-ttu-id="9df3a-145">0</span><span class="sxs-lookup"><span data-stu-id="9df3a-145">0</span></span>                                                     |
| <span data-ttu-id="9df3a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9df3a-146">Range-Upper</span></span>            | <span data-ttu-id="9df3a-147">32767</span><span class="sxs-lookup"><span data-stu-id="9df3a-147">32767</span></span>                                                 |
| <span data-ttu-id="9df3a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-148">Search-Flags</span></span>           | <span data-ttu-id="9df3a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9df3a-149">0x00000000</span></span>                                            |
| <span data-ttu-id="9df3a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-150">System-Flags</span></span>           | <span data-ttu-id="9df3a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9df3a-151">0x00000010</span></span>                                            |
| <span data-ttu-id="9df3a-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9df3a-152">Classes used in</span></span>        | [<span data-ttu-id="9df3a-153">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="9df3a-153">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9df3a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9df3a-154">Windows Server 2003</span></span>



| <span data-ttu-id="9df3a-155">進入</span><span class="sxs-lookup"><span data-stu-id="9df3a-155">Entry</span></span> | <span data-ttu-id="9df3a-156">值</span><span class="sxs-lookup"><span data-stu-id="9df3a-156">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="9df3a-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9df3a-157">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9df3a-158">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9df3a-159">System-Only</span></span>            | <span data-ttu-id="9df3a-160">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-160">False</span></span>                                                 |
| <span data-ttu-id="9df3a-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9df3a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9df3a-162">對</span><span class="sxs-lookup"><span data-stu-id="9df3a-162">True</span></span>                                                  |
| <span data-ttu-id="9df3a-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9df3a-163">Is Indexed</span></span>             | <span data-ttu-id="9df3a-164">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-164">False</span></span>                                                 |
| <span data-ttu-id="9df3a-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9df3a-165">In Global Catalog</span></span>      | <span data-ttu-id="9df3a-166">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-166">False</span></span>                                                 |
| <span data-ttu-id="9df3a-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9df3a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9df3a-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9df3a-168">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="9df3a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9df3a-169">Range-Lower</span></span>            | <span data-ttu-id="9df3a-170">0</span><span class="sxs-lookup"><span data-stu-id="9df3a-170">0</span></span>                                                     |
| <span data-ttu-id="9df3a-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9df3a-171">Range-Upper</span></span>            | <span data-ttu-id="9df3a-172">32767</span><span class="sxs-lookup"><span data-stu-id="9df3a-172">32767</span></span>                                                 |
| <span data-ttu-id="9df3a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-173">Search-Flags</span></span>           | <span data-ttu-id="9df3a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9df3a-174">0x00000000</span></span>                                            |
| <span data-ttu-id="9df3a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-175">System-Flags</span></span>           | <span data-ttu-id="9df3a-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9df3a-176">0x00000010</span></span>                                            |
| <span data-ttu-id="9df3a-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9df3a-177">Classes used in</span></span>        | [<span data-ttu-id="9df3a-178">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="9df3a-178">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9df3a-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9df3a-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9df3a-180">進入</span><span class="sxs-lookup"><span data-stu-id="9df3a-180">Entry</span></span> | <span data-ttu-id="9df3a-181">值</span><span class="sxs-lookup"><span data-stu-id="9df3a-181">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="9df3a-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9df3a-182">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9df3a-183">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9df3a-184">System-Only</span></span>            | <span data-ttu-id="9df3a-185">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-185">False</span></span>                                                 |
| <span data-ttu-id="9df3a-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9df3a-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9df3a-187">對</span><span class="sxs-lookup"><span data-stu-id="9df3a-187">True</span></span>                                                  |
| <span data-ttu-id="9df3a-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9df3a-188">Is Indexed</span></span>             | <span data-ttu-id="9df3a-189">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-189">False</span></span>                                                 |
| <span data-ttu-id="9df3a-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9df3a-190">In Global Catalog</span></span>      | <span data-ttu-id="9df3a-191">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-191">False</span></span>                                                 |
| <span data-ttu-id="9df3a-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9df3a-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9df3a-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9df3a-193">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="9df3a-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9df3a-194">Range-Lower</span></span>            | <span data-ttu-id="9df3a-195">0</span><span class="sxs-lookup"><span data-stu-id="9df3a-195">0</span></span>                                                     |
| <span data-ttu-id="9df3a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9df3a-196">Range-Upper</span></span>            | <span data-ttu-id="9df3a-197">32767</span><span class="sxs-lookup"><span data-stu-id="9df3a-197">32767</span></span>                                                 |
| <span data-ttu-id="9df3a-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-198">Search-Flags</span></span>           | <span data-ttu-id="9df3a-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9df3a-199">0x00000000</span></span>                                            |
| <span data-ttu-id="9df3a-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-200">System-Flags</span></span>           | <span data-ttu-id="9df3a-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9df3a-201">0x00000010</span></span>                                            |
| <span data-ttu-id="9df3a-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9df3a-202">Classes used in</span></span>        | [<span data-ttu-id="9df3a-203">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="9df3a-203">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9df3a-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9df3a-204">Windows Server 2008</span></span>



| <span data-ttu-id="9df3a-205">進入</span><span class="sxs-lookup"><span data-stu-id="9df3a-205">Entry</span></span> | <span data-ttu-id="9df3a-206">值</span><span class="sxs-lookup"><span data-stu-id="9df3a-206">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="9df3a-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9df3a-207">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9df3a-208">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="9df3a-209">System-Only</span></span>            | <span data-ttu-id="9df3a-210">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-210">False</span></span>                                                 |
| <span data-ttu-id="9df3a-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9df3a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="9df3a-212">對</span><span class="sxs-lookup"><span data-stu-id="9df3a-212">True</span></span>                                                  |
| <span data-ttu-id="9df3a-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9df3a-213">Is Indexed</span></span>             | <span data-ttu-id="9df3a-214">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-214">False</span></span>                                                 |
| <span data-ttu-id="9df3a-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9df3a-215">In Global Catalog</span></span>      | <span data-ttu-id="9df3a-216">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-216">False</span></span>                                                 |
| <span data-ttu-id="9df3a-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9df3a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="9df3a-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9df3a-218">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="9df3a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9df3a-219">Range-Lower</span></span>            | <span data-ttu-id="9df3a-220">0</span><span class="sxs-lookup"><span data-stu-id="9df3a-220">0</span></span>                                                     |
| <span data-ttu-id="9df3a-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9df3a-221">Range-Upper</span></span>            | <span data-ttu-id="9df3a-222">32767</span><span class="sxs-lookup"><span data-stu-id="9df3a-222">32767</span></span>                                                 |
| <span data-ttu-id="9df3a-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-223">Search-Flags</span></span>           | <span data-ttu-id="9df3a-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9df3a-224">0x00000000</span></span>                                            |
| <span data-ttu-id="9df3a-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-225">System-Flags</span></span>           | <span data-ttu-id="9df3a-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9df3a-226">0x00000010</span></span>                                            |
| <span data-ttu-id="9df3a-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9df3a-227">Classes used in</span></span>        | [<span data-ttu-id="9df3a-228">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="9df3a-228">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9df3a-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9df3a-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9df3a-230">進入</span><span class="sxs-lookup"><span data-stu-id="9df3a-230">Entry</span></span> | <span data-ttu-id="9df3a-231">值</span><span class="sxs-lookup"><span data-stu-id="9df3a-231">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="9df3a-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9df3a-232">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9df3a-233">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="9df3a-234">System-Only</span></span>            | <span data-ttu-id="9df3a-235">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-235">False</span></span>                                                 |
| <span data-ttu-id="9df3a-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9df3a-236">Is-Single-Valued</span></span>       | <span data-ttu-id="9df3a-237">對</span><span class="sxs-lookup"><span data-stu-id="9df3a-237">True</span></span>                                                  |
| <span data-ttu-id="9df3a-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9df3a-238">Is Indexed</span></span>             | <span data-ttu-id="9df3a-239">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-239">False</span></span>                                                 |
| <span data-ttu-id="9df3a-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9df3a-240">In Global Catalog</span></span>      | <span data-ttu-id="9df3a-241">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-241">False</span></span>                                                 |
| <span data-ttu-id="9df3a-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9df3a-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="9df3a-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9df3a-243">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="9df3a-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9df3a-244">Range-Lower</span></span>            | <span data-ttu-id="9df3a-245">0</span><span class="sxs-lookup"><span data-stu-id="9df3a-245">0</span></span>                                                     |
| <span data-ttu-id="9df3a-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9df3a-246">Range-Upper</span></span>            | <span data-ttu-id="9df3a-247">32767</span><span class="sxs-lookup"><span data-stu-id="9df3a-247">32767</span></span>                                                 |
| <span data-ttu-id="9df3a-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-248">Search-Flags</span></span>           | <span data-ttu-id="9df3a-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9df3a-249">0x00000000</span></span>                                            |
| <span data-ttu-id="9df3a-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-250">System-Flags</span></span>           | <span data-ttu-id="9df3a-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9df3a-251">0x00000010</span></span>                                            |
| <span data-ttu-id="9df3a-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9df3a-252">Classes used in</span></span>        | [<span data-ttu-id="9df3a-253">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="9df3a-253">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9df3a-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9df3a-254">Windows Server 2012</span></span>



| <span data-ttu-id="9df3a-255">進入</span><span class="sxs-lookup"><span data-stu-id="9df3a-255">Entry</span></span> | <span data-ttu-id="9df3a-256">值</span><span class="sxs-lookup"><span data-stu-id="9df3a-256">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="9df3a-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9df3a-257">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9df3a-258">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="9df3a-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="9df3a-259">System-Only</span></span>            | <span data-ttu-id="9df3a-260">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-260">False</span></span>                                                 |
| <span data-ttu-id="9df3a-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9df3a-261">Is-Single-Valued</span></span>       | <span data-ttu-id="9df3a-262">對</span><span class="sxs-lookup"><span data-stu-id="9df3a-262">True</span></span>                                                  |
| <span data-ttu-id="9df3a-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9df3a-263">Is Indexed</span></span>             | <span data-ttu-id="9df3a-264">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-264">False</span></span>                                                 |
| <span data-ttu-id="9df3a-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9df3a-265">In Global Catalog</span></span>      | <span data-ttu-id="9df3a-266">否</span><span class="sxs-lookup"><span data-stu-id="9df3a-266">False</span></span>                                                 |
| <span data-ttu-id="9df3a-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9df3a-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="9df3a-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9df3a-268">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="9df3a-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9df3a-269">Range-Lower</span></span>            | <span data-ttu-id="9df3a-270">0</span><span class="sxs-lookup"><span data-stu-id="9df3a-270">0</span></span>                                                     |
| <span data-ttu-id="9df3a-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9df3a-271">Range-Upper</span></span>            | <span data-ttu-id="9df3a-272">32767</span><span class="sxs-lookup"><span data-stu-id="9df3a-272">32767</span></span>                                                 |
| <span data-ttu-id="9df3a-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-273">Search-Flags</span></span>           | <span data-ttu-id="9df3a-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9df3a-274">0x00000000</span></span>                                            |
| <span data-ttu-id="9df3a-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9df3a-275">System-Flags</span></span>           | <span data-ttu-id="9df3a-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9df3a-276">0x00000010</span></span>                                            |
| <span data-ttu-id="9df3a-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9df3a-277">Classes used in</span></span>        | [<span data-ttu-id="9df3a-278">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="9df3a-278">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 






---
title: 網域交互參考屬性
description: 這是從信任的網域物件到受信任網域的交互參照物件的參考。
ms.assetid: aa6fe6f9-a45c-448c-9fc5-17bc2994c764
ms.tgt_platform: multiple
keywords:
- 網域交互參考屬性 AD 架構
- domainCrossRef 屬性 AD 架構
topic_type:
- apiref
api_name:
- Domain-Cross-Ref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b85e1293ce8141a3614c9401dbb34c1031de5935
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106965130"
---
# <a name="domain-cross-ref-attribute"></a><span data-ttu-id="a8868-105">網域交互參考屬性</span><span class="sxs-lookup"><span data-stu-id="a8868-105">Domain-Cross-Ref attribute</span></span>

<span data-ttu-id="a8868-106">這是從信任的網域物件到受信任網域的交互參照物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a8868-106">This is a reference from a trusted domain object to the cross reference object of the trusted domain.</span></span>



| <span data-ttu-id="a8868-107">進入</span><span class="sxs-lookup"><span data-stu-id="a8868-107">Entry</span></span> | <span data-ttu-id="a8868-108">值</span><span class="sxs-lookup"><span data-stu-id="a8868-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a8868-109">CN</span><span class="sxs-lookup"><span data-stu-id="a8868-109">CN</span></span>                | <span data-ttu-id="a8868-110">網域交互參考</span><span class="sxs-lookup"><span data-stu-id="a8868-110">Domain-Cross-Ref</span></span>                        |
| <span data-ttu-id="a8868-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a8868-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a8868-112">domainCrossRef</span><span class="sxs-lookup"><span data-stu-id="a8868-112">domainCrossRef</span></span>                          |
| <span data-ttu-id="a8868-113">大小</span><span class="sxs-lookup"><span data-stu-id="a8868-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="a8868-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a8868-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="a8868-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a8868-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="a8868-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a8868-116">Attribute-Id</span></span>      | <span data-ttu-id="a8868-117">1.2.840.113556.1.4.472</span><span class="sxs-lookup"><span data-stu-id="a8868-117">1.2.840.113556.1.4.472</span></span>                  |
| <span data-ttu-id="a8868-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a8868-118">System-Id-Guid</span></span>    | <span data-ttu-id="a8868-119">b000ea7b-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="a8868-119">b000ea7b-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="a8868-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8868-120">Syntax</span></span>            | [<span data-ttu-id="a8868-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a8868-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a8868-122">實作</span><span class="sxs-lookup"><span data-stu-id="a8868-122">Implementations</span></span>

-   [<span data-ttu-id="a8868-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a8868-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a8868-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a8868-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a8868-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a8868-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a8868-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a8868-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a8868-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a8868-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a8868-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a8868-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a8868-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a8868-129">Windows 2000 Server</span></span>



| <span data-ttu-id="a8868-130">進入</span><span class="sxs-lookup"><span data-stu-id="a8868-130">Entry</span></span> | <span data-ttu-id="a8868-131">值</span><span class="sxs-lookup"><span data-stu-id="a8868-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a8868-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8868-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8868-133">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8868-134">System-Only</span></span>            | <span data-ttu-id="a8868-135">否</span><span class="sxs-lookup"><span data-stu-id="a8868-135">False</span></span>                                                |
| <span data-ttu-id="a8868-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8868-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a8868-137">對</span><span class="sxs-lookup"><span data-stu-id="a8868-137">True</span></span>                                                 |
| <span data-ttu-id="a8868-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8868-138">Is Indexed</span></span>             | <span data-ttu-id="a8868-139">否</span><span class="sxs-lookup"><span data-stu-id="a8868-139">False</span></span>                                                |
| <span data-ttu-id="a8868-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8868-140">In Global Catalog</span></span>      | <span data-ttu-id="a8868-141">否</span><span class="sxs-lookup"><span data-stu-id="a8868-141">False</span></span>                                                |
| <span data-ttu-id="a8868-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8868-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8868-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8868-143">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a8868-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8868-144">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8868-145">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-146">Search-Flags</span></span>           | <span data-ttu-id="a8868-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8868-147">0x00000000</span></span>                                           |
| <span data-ttu-id="a8868-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-148">System-Flags</span></span>           | <span data-ttu-id="a8868-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8868-149">0x00000010</span></span>                                           |
| <span data-ttu-id="a8868-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8868-150">Classes used in</span></span>        | [<span data-ttu-id="a8868-151">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a8868-151">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a8868-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8868-152">Windows Server 2003</span></span>



| <span data-ttu-id="a8868-153">進入</span><span class="sxs-lookup"><span data-stu-id="a8868-153">Entry</span></span> | <span data-ttu-id="a8868-154">值</span><span class="sxs-lookup"><span data-stu-id="a8868-154">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a8868-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8868-155">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8868-156">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8868-157">System-Only</span></span>            | <span data-ttu-id="a8868-158">否</span><span class="sxs-lookup"><span data-stu-id="a8868-158">False</span></span>                                                |
| <span data-ttu-id="a8868-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8868-159">Is-Single-Valued</span></span>       | <span data-ttu-id="a8868-160">對</span><span class="sxs-lookup"><span data-stu-id="a8868-160">True</span></span>                                                 |
| <span data-ttu-id="a8868-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8868-161">Is Indexed</span></span>             | <span data-ttu-id="a8868-162">否</span><span class="sxs-lookup"><span data-stu-id="a8868-162">False</span></span>                                                |
| <span data-ttu-id="a8868-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8868-163">In Global Catalog</span></span>      | <span data-ttu-id="a8868-164">否</span><span class="sxs-lookup"><span data-stu-id="a8868-164">False</span></span>                                                |
| <span data-ttu-id="a8868-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8868-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8868-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8868-166">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a8868-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8868-167">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8868-168">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-169">Search-Flags</span></span>           | <span data-ttu-id="a8868-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8868-170">0x00000000</span></span>                                           |
| <span data-ttu-id="a8868-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-171">System-Flags</span></span>           | <span data-ttu-id="a8868-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8868-172">0x00000010</span></span>                                           |
| <span data-ttu-id="a8868-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8868-173">Classes used in</span></span>        | [<span data-ttu-id="a8868-174">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a8868-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a8868-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a8868-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a8868-176">進入</span><span class="sxs-lookup"><span data-stu-id="a8868-176">Entry</span></span> | <span data-ttu-id="a8868-177">值</span><span class="sxs-lookup"><span data-stu-id="a8868-177">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a8868-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8868-178">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8868-179">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8868-180">System-Only</span></span>            | <span data-ttu-id="a8868-181">否</span><span class="sxs-lookup"><span data-stu-id="a8868-181">False</span></span>                                                |
| <span data-ttu-id="a8868-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8868-182">Is-Single-Valued</span></span>       | <span data-ttu-id="a8868-183">對</span><span class="sxs-lookup"><span data-stu-id="a8868-183">True</span></span>                                                 |
| <span data-ttu-id="a8868-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8868-184">Is Indexed</span></span>             | <span data-ttu-id="a8868-185">否</span><span class="sxs-lookup"><span data-stu-id="a8868-185">False</span></span>                                                |
| <span data-ttu-id="a8868-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8868-186">In Global Catalog</span></span>      | <span data-ttu-id="a8868-187">否</span><span class="sxs-lookup"><span data-stu-id="a8868-187">False</span></span>                                                |
| <span data-ttu-id="a8868-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8868-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8868-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8868-189">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a8868-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8868-190">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8868-191">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-192">Search-Flags</span></span>           | <span data-ttu-id="a8868-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8868-193">0x00000000</span></span>                                           |
| <span data-ttu-id="a8868-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-194">System-Flags</span></span>           | <span data-ttu-id="a8868-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8868-195">0x00000010</span></span>                                           |
| <span data-ttu-id="a8868-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8868-196">Classes used in</span></span>        | [<span data-ttu-id="a8868-197">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a8868-197">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a8868-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8868-198">Windows Server 2008</span></span>



| <span data-ttu-id="a8868-199">進入</span><span class="sxs-lookup"><span data-stu-id="a8868-199">Entry</span></span> | <span data-ttu-id="a8868-200">值</span><span class="sxs-lookup"><span data-stu-id="a8868-200">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a8868-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8868-201">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8868-202">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8868-203">System-Only</span></span>            | <span data-ttu-id="a8868-204">否</span><span class="sxs-lookup"><span data-stu-id="a8868-204">False</span></span>                                                |
| <span data-ttu-id="a8868-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8868-205">Is-Single-Valued</span></span>       | <span data-ttu-id="a8868-206">對</span><span class="sxs-lookup"><span data-stu-id="a8868-206">True</span></span>                                                 |
| <span data-ttu-id="a8868-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8868-207">Is Indexed</span></span>             | <span data-ttu-id="a8868-208">否</span><span class="sxs-lookup"><span data-stu-id="a8868-208">False</span></span>                                                |
| <span data-ttu-id="a8868-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8868-209">In Global Catalog</span></span>      | <span data-ttu-id="a8868-210">否</span><span class="sxs-lookup"><span data-stu-id="a8868-210">False</span></span>                                                |
| <span data-ttu-id="a8868-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8868-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8868-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8868-212">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a8868-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8868-213">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8868-214">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-215">Search-Flags</span></span>           | <span data-ttu-id="a8868-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8868-216">0x00000000</span></span>                                           |
| <span data-ttu-id="a8868-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-217">System-Flags</span></span>           | <span data-ttu-id="a8868-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8868-218">0x00000010</span></span>                                           |
| <span data-ttu-id="a8868-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8868-219">Classes used in</span></span>        | [<span data-ttu-id="a8868-220">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a8868-220">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a8868-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8868-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a8868-222">進入</span><span class="sxs-lookup"><span data-stu-id="a8868-222">Entry</span></span> | <span data-ttu-id="a8868-223">值</span><span class="sxs-lookup"><span data-stu-id="a8868-223">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a8868-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8868-224">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8868-225">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8868-226">System-Only</span></span>            | <span data-ttu-id="a8868-227">否</span><span class="sxs-lookup"><span data-stu-id="a8868-227">False</span></span>                                                |
| <span data-ttu-id="a8868-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8868-228">Is-Single-Valued</span></span>       | <span data-ttu-id="a8868-229">對</span><span class="sxs-lookup"><span data-stu-id="a8868-229">True</span></span>                                                 |
| <span data-ttu-id="a8868-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8868-230">Is Indexed</span></span>             | <span data-ttu-id="a8868-231">否</span><span class="sxs-lookup"><span data-stu-id="a8868-231">False</span></span>                                                |
| <span data-ttu-id="a8868-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8868-232">In Global Catalog</span></span>      | <span data-ttu-id="a8868-233">否</span><span class="sxs-lookup"><span data-stu-id="a8868-233">False</span></span>                                                |
| <span data-ttu-id="a8868-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8868-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8868-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8868-235">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a8868-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8868-236">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8868-237">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-238">Search-Flags</span></span>           | <span data-ttu-id="a8868-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8868-239">0x00000000</span></span>                                           |
| <span data-ttu-id="a8868-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-240">System-Flags</span></span>           | <span data-ttu-id="a8868-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8868-241">0x00000010</span></span>                                           |
| <span data-ttu-id="a8868-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8868-242">Classes used in</span></span>        | [<span data-ttu-id="a8868-243">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a8868-243">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a8868-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8868-244">Windows Server 2012</span></span>



| <span data-ttu-id="a8868-245">進入</span><span class="sxs-lookup"><span data-stu-id="a8868-245">Entry</span></span> | <span data-ttu-id="a8868-246">值</span><span class="sxs-lookup"><span data-stu-id="a8868-246">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a8868-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8868-247">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8868-248">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a8868-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8868-249">System-Only</span></span>            | <span data-ttu-id="a8868-250">否</span><span class="sxs-lookup"><span data-stu-id="a8868-250">False</span></span>                                                |
| <span data-ttu-id="a8868-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8868-251">Is-Single-Valued</span></span>       | <span data-ttu-id="a8868-252">對</span><span class="sxs-lookup"><span data-stu-id="a8868-252">True</span></span>                                                 |
| <span data-ttu-id="a8868-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8868-253">Is Indexed</span></span>             | <span data-ttu-id="a8868-254">否</span><span class="sxs-lookup"><span data-stu-id="a8868-254">False</span></span>                                                |
| <span data-ttu-id="a8868-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8868-255">In Global Catalog</span></span>      | <span data-ttu-id="a8868-256">否</span><span class="sxs-lookup"><span data-stu-id="a8868-256">False</span></span>                                                |
| <span data-ttu-id="a8868-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8868-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8868-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8868-258">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a8868-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8868-259">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8868-260">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a8868-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-261">Search-Flags</span></span>           | <span data-ttu-id="a8868-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8868-262">0x00000000</span></span>                                           |
| <span data-ttu-id="a8868-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8868-263">System-Flags</span></span>           | <span data-ttu-id="a8868-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8868-264">0x00000010</span></span>                                           |
| <span data-ttu-id="a8868-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8868-265">Classes used in</span></span>        | [<span data-ttu-id="a8868-266">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a8868-266">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






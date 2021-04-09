---
title: Trust-Attributes 屬性
description: 這個屬性會儲存受信任網域的信任屬性。
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Trust-Attributes 屬性 AD 架構
- trustAttributes 屬性 AD 架構
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687119"
---
# <a name="trust-attributes-attribute"></a><span data-ttu-id="356ea-105">Trust-Attributes 屬性</span><span class="sxs-lookup"><span data-stu-id="356ea-105">Trust-Attributes attribute</span></span>

<span data-ttu-id="356ea-106">這個屬性會儲存受信任網域的信任屬性。</span><span class="sxs-lookup"><span data-stu-id="356ea-106">This attribute stores the trust attributes for a trusted domain.</span></span> <span data-ttu-id="356ea-107">可能的屬性值如下所示：</span><span class="sxs-lookup"><span data-stu-id="356ea-107">Possible attribute values are as follows:</span></span>

-   <span data-ttu-id="356ea-108">信任 \_ 屬性 \_ 非可 \_ 轉移停用轉移。</span><span class="sxs-lookup"><span data-stu-id="356ea-108">TRUST\_ATTRIBUTE\_NON\_TRANSITIVE Disable transitivity.</span></span>
-   <span data-ttu-id="356ea-109">信任 \_ 屬性 \_ 樹狀目錄 \_ 父系信任設定為組織樹狀目錄父系。</span><span class="sxs-lookup"><span data-stu-id="356ea-109">TRUST\_ATTRIBUTE\_TREE\_PARENT Trust is set to the organization tree parent.</span></span>
-   <span data-ttu-id="356ea-110">信任 \_ 屬性 \_ 樹狀結構 \_ 根信任設定為樹系中的另一個樹狀目錄根。</span><span class="sxs-lookup"><span data-stu-id="356ea-110">TRUST\_ATTRIBUTE\_TREE\_ROOT Trust set to another tree root in the forest.</span></span>
-   <span data-ttu-id="356ea-111">信任 \_ 屬性 \_ 僅 \_ 限上層僅限上層用戶端的受信任連結有效。</span><span class="sxs-lookup"><span data-stu-id="356ea-111">TRUST\_ATTRIBUTE\_UPLEVEL\_ONLY Trusted link valid only for uplevel client.</span></span>



| <span data-ttu-id="356ea-112">進入</span><span class="sxs-lookup"><span data-stu-id="356ea-112">Entry</span></span> | <span data-ttu-id="356ea-113">值</span><span class="sxs-lookup"><span data-stu-id="356ea-113">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="356ea-114">CN</span><span class="sxs-lookup"><span data-stu-id="356ea-114">CN</span></span>                | <span data-ttu-id="356ea-115">Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="356ea-115">Trust-Attributes</span></span>                     |
| <span data-ttu-id="356ea-116">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="356ea-116">Ldap-Display-Name</span></span> | <span data-ttu-id="356ea-117">trustAttributes</span><span class="sxs-lookup"><span data-stu-id="356ea-117">trustAttributes</span></span>                      |
| <span data-ttu-id="356ea-118">大小</span><span class="sxs-lookup"><span data-stu-id="356ea-118">Size</span></span>              | \-                                   |
| <span data-ttu-id="356ea-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="356ea-119">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="356ea-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="356ea-120">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="356ea-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="356ea-121">Attribute-Id</span></span>      | <span data-ttu-id="356ea-122">1.2.840.113556.1.4.470</span><span class="sxs-lookup"><span data-stu-id="356ea-122">1.2.840.113556.1.4.470</span></span>               |
| <span data-ttu-id="356ea-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="356ea-123">System-Id-Guid</span></span>    | <span data-ttu-id="356ea-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="356ea-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span></span> |
| <span data-ttu-id="356ea-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="356ea-125">Syntax</span></span>            | [<span data-ttu-id="356ea-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="356ea-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="356ea-127">實作</span><span class="sxs-lookup"><span data-stu-id="356ea-127">Implementations</span></span>

-   [<span data-ttu-id="356ea-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="356ea-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="356ea-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="356ea-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="356ea-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="356ea-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="356ea-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="356ea-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="356ea-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="356ea-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="356ea-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="356ea-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="356ea-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="356ea-134">Windows 2000 Server</span></span>



| <span data-ttu-id="356ea-135">進入</span><span class="sxs-lookup"><span data-stu-id="356ea-135">Entry</span></span> | <span data-ttu-id="356ea-136">值</span><span class="sxs-lookup"><span data-stu-id="356ea-136">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="356ea-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="356ea-137">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="356ea-138">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="356ea-139">System-Only</span></span>            | <span data-ttu-id="356ea-140">否</span><span class="sxs-lookup"><span data-stu-id="356ea-140">False</span></span>                                                |
| <span data-ttu-id="356ea-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="356ea-141">Is-Single-Valued</span></span>       | <span data-ttu-id="356ea-142">對</span><span class="sxs-lookup"><span data-stu-id="356ea-142">True</span></span>                                                 |
| <span data-ttu-id="356ea-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="356ea-143">Is Indexed</span></span>             | <span data-ttu-id="356ea-144">否</span><span class="sxs-lookup"><span data-stu-id="356ea-144">False</span></span>                                                |
| <span data-ttu-id="356ea-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="356ea-145">In Global Catalog</span></span>      | <span data-ttu-id="356ea-146">否</span><span class="sxs-lookup"><span data-stu-id="356ea-146">False</span></span>                                                |
| <span data-ttu-id="356ea-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="356ea-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="356ea-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="356ea-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="356ea-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="356ea-149">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="356ea-150">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-151">Search-Flags</span></span>           | <span data-ttu-id="356ea-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="356ea-152">0x00000000</span></span>                                           |
| <span data-ttu-id="356ea-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-153">System-Flags</span></span>           | <span data-ttu-id="356ea-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="356ea-154">0x00000010</span></span>                                           |
| <span data-ttu-id="356ea-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="356ea-155">Classes used in</span></span>        | [<span data-ttu-id="356ea-156">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="356ea-156">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="356ea-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="356ea-157">Windows Server 2003</span></span>



| <span data-ttu-id="356ea-158">進入</span><span class="sxs-lookup"><span data-stu-id="356ea-158">Entry</span></span> | <span data-ttu-id="356ea-159">值</span><span class="sxs-lookup"><span data-stu-id="356ea-159">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="356ea-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="356ea-160">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="356ea-161">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="356ea-162">System-Only</span></span>            | <span data-ttu-id="356ea-163">否</span><span class="sxs-lookup"><span data-stu-id="356ea-163">False</span></span>                                                |
| <span data-ttu-id="356ea-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="356ea-164">Is-Single-Valued</span></span>       | <span data-ttu-id="356ea-165">對</span><span class="sxs-lookup"><span data-stu-id="356ea-165">True</span></span>                                                 |
| <span data-ttu-id="356ea-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="356ea-166">Is Indexed</span></span>             | <span data-ttu-id="356ea-167">否</span><span class="sxs-lookup"><span data-stu-id="356ea-167">False</span></span>                                                |
| <span data-ttu-id="356ea-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="356ea-168">In Global Catalog</span></span>      | <span data-ttu-id="356ea-169">對</span><span class="sxs-lookup"><span data-stu-id="356ea-169">True</span></span>                                                 |
| <span data-ttu-id="356ea-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="356ea-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="356ea-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="356ea-171">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="356ea-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="356ea-172">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="356ea-173">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-174">Search-Flags</span></span>           | <span data-ttu-id="356ea-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="356ea-175">0x00000000</span></span>                                           |
| <span data-ttu-id="356ea-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-176">System-Flags</span></span>           | <span data-ttu-id="356ea-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="356ea-177">0x00000010</span></span>                                           |
| <span data-ttu-id="356ea-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="356ea-178">Classes used in</span></span>        | [<span data-ttu-id="356ea-179">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="356ea-179">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="356ea-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="356ea-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="356ea-181">進入</span><span class="sxs-lookup"><span data-stu-id="356ea-181">Entry</span></span> | <span data-ttu-id="356ea-182">值</span><span class="sxs-lookup"><span data-stu-id="356ea-182">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="356ea-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="356ea-183">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="356ea-184">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="356ea-185">System-Only</span></span>            | <span data-ttu-id="356ea-186">否</span><span class="sxs-lookup"><span data-stu-id="356ea-186">False</span></span>                                                |
| <span data-ttu-id="356ea-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="356ea-187">Is-Single-Valued</span></span>       | <span data-ttu-id="356ea-188">對</span><span class="sxs-lookup"><span data-stu-id="356ea-188">True</span></span>                                                 |
| <span data-ttu-id="356ea-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="356ea-189">Is Indexed</span></span>             | <span data-ttu-id="356ea-190">否</span><span class="sxs-lookup"><span data-stu-id="356ea-190">False</span></span>                                                |
| <span data-ttu-id="356ea-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="356ea-191">In Global Catalog</span></span>      | <span data-ttu-id="356ea-192">對</span><span class="sxs-lookup"><span data-stu-id="356ea-192">True</span></span>                                                 |
| <span data-ttu-id="356ea-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="356ea-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="356ea-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="356ea-194">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="356ea-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="356ea-195">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="356ea-196">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-197">Search-Flags</span></span>           | <span data-ttu-id="356ea-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="356ea-198">0x00000000</span></span>                                           |
| <span data-ttu-id="356ea-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-199">System-Flags</span></span>           | <span data-ttu-id="356ea-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="356ea-200">0x00000010</span></span>                                           |
| <span data-ttu-id="356ea-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="356ea-201">Classes used in</span></span>        | [<span data-ttu-id="356ea-202">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="356ea-202">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="356ea-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="356ea-203">Windows Server 2008</span></span>



| <span data-ttu-id="356ea-204">進入</span><span class="sxs-lookup"><span data-stu-id="356ea-204">Entry</span></span> | <span data-ttu-id="356ea-205">值</span><span class="sxs-lookup"><span data-stu-id="356ea-205">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="356ea-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="356ea-206">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="356ea-207">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="356ea-208">System-Only</span></span>            | <span data-ttu-id="356ea-209">否</span><span class="sxs-lookup"><span data-stu-id="356ea-209">False</span></span>                                                |
| <span data-ttu-id="356ea-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="356ea-210">Is-Single-Valued</span></span>       | <span data-ttu-id="356ea-211">對</span><span class="sxs-lookup"><span data-stu-id="356ea-211">True</span></span>                                                 |
| <span data-ttu-id="356ea-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="356ea-212">Is Indexed</span></span>             | <span data-ttu-id="356ea-213">否</span><span class="sxs-lookup"><span data-stu-id="356ea-213">False</span></span>                                                |
| <span data-ttu-id="356ea-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="356ea-214">In Global Catalog</span></span>      | <span data-ttu-id="356ea-215">對</span><span class="sxs-lookup"><span data-stu-id="356ea-215">True</span></span>                                                 |
| <span data-ttu-id="356ea-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="356ea-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="356ea-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="356ea-217">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="356ea-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="356ea-218">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="356ea-219">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-220">Search-Flags</span></span>           | <span data-ttu-id="356ea-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="356ea-221">0x00000000</span></span>                                           |
| <span data-ttu-id="356ea-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-222">System-Flags</span></span>           | <span data-ttu-id="356ea-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="356ea-223">0x00000010</span></span>                                           |
| <span data-ttu-id="356ea-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="356ea-224">Classes used in</span></span>        | [<span data-ttu-id="356ea-225">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="356ea-225">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="356ea-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="356ea-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="356ea-227">進入</span><span class="sxs-lookup"><span data-stu-id="356ea-227">Entry</span></span> | <span data-ttu-id="356ea-228">值</span><span class="sxs-lookup"><span data-stu-id="356ea-228">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="356ea-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="356ea-229">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="356ea-230">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="356ea-231">System-Only</span></span>            | <span data-ttu-id="356ea-232">否</span><span class="sxs-lookup"><span data-stu-id="356ea-232">False</span></span>                                                |
| <span data-ttu-id="356ea-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="356ea-233">Is-Single-Valued</span></span>       | <span data-ttu-id="356ea-234">對</span><span class="sxs-lookup"><span data-stu-id="356ea-234">True</span></span>                                                 |
| <span data-ttu-id="356ea-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="356ea-235">Is Indexed</span></span>             | <span data-ttu-id="356ea-236">否</span><span class="sxs-lookup"><span data-stu-id="356ea-236">False</span></span>                                                |
| <span data-ttu-id="356ea-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="356ea-237">In Global Catalog</span></span>      | <span data-ttu-id="356ea-238">對</span><span class="sxs-lookup"><span data-stu-id="356ea-238">True</span></span>                                                 |
| <span data-ttu-id="356ea-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="356ea-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="356ea-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="356ea-240">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="356ea-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="356ea-241">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="356ea-242">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-243">Search-Flags</span></span>           | <span data-ttu-id="356ea-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="356ea-244">0x00000000</span></span>                                           |
| <span data-ttu-id="356ea-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-245">System-Flags</span></span>           | <span data-ttu-id="356ea-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="356ea-246">0x00000010</span></span>                                           |
| <span data-ttu-id="356ea-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="356ea-247">Classes used in</span></span>        | [<span data-ttu-id="356ea-248">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="356ea-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="356ea-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="356ea-249">Windows Server 2012</span></span>



| <span data-ttu-id="356ea-250">進入</span><span class="sxs-lookup"><span data-stu-id="356ea-250">Entry</span></span> | <span data-ttu-id="356ea-251">值</span><span class="sxs-lookup"><span data-stu-id="356ea-251">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="356ea-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="356ea-252">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="356ea-253">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="356ea-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="356ea-254">System-Only</span></span>            | <span data-ttu-id="356ea-255">否</span><span class="sxs-lookup"><span data-stu-id="356ea-255">False</span></span>                                                |
| <span data-ttu-id="356ea-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="356ea-256">Is-Single-Valued</span></span>       | <span data-ttu-id="356ea-257">對</span><span class="sxs-lookup"><span data-stu-id="356ea-257">True</span></span>                                                 |
| <span data-ttu-id="356ea-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="356ea-258">Is Indexed</span></span>             | <span data-ttu-id="356ea-259">否</span><span class="sxs-lookup"><span data-stu-id="356ea-259">False</span></span>                                                |
| <span data-ttu-id="356ea-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="356ea-260">In Global Catalog</span></span>      | <span data-ttu-id="356ea-261">對</span><span class="sxs-lookup"><span data-stu-id="356ea-261">True</span></span>                                                 |
| <span data-ttu-id="356ea-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="356ea-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="356ea-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="356ea-263">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="356ea-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="356ea-264">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="356ea-265">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="356ea-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-266">Search-Flags</span></span>           | <span data-ttu-id="356ea-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="356ea-267">0x00000000</span></span>                                           |
| <span data-ttu-id="356ea-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="356ea-268">System-Flags</span></span>           | <span data-ttu-id="356ea-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="356ea-269">0x00000010</span></span>                                           |
| <span data-ttu-id="356ea-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="356ea-270">Classes used in</span></span>        | [<span data-ttu-id="356ea-271">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="356ea-271">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






---
title: dhcp 類型屬性
description: DHCP 伺服器的類型。
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- dhcp 類型屬性 AD 架構
- dhcpType 屬性 AD 架構
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935259"
---
# <a name="dhcp-type-attribute"></a><span data-ttu-id="ba5f9-105">dhcp 類型屬性</span><span class="sxs-lookup"><span data-stu-id="ba5f9-105">dhcp-Type attribute</span></span>

<span data-ttu-id="ba5f9-106">DHCP 伺服器的類型。</span><span class="sxs-lookup"><span data-stu-id="ba5f9-106">The type of DHCP server.</span></span> <span data-ttu-id="ba5f9-107">這個屬性是在 objectClass [**dHCPClass**](c-dhcpclass.md)的所有物件上設定的。</span><span class="sxs-lookup"><span data-stu-id="ba5f9-107">This attribute is set on all objects of objectClass [**dHCPClass**](c-dhcpclass.md).</span></span> <span data-ttu-id="ba5f9-108">它的值會定義物件的類型：</span><span class="sxs-lookup"><span data-stu-id="ba5f9-108">Its value defines the type of object:</span></span>

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| <span data-ttu-id="ba5f9-109">進入</span><span class="sxs-lookup"><span data-stu-id="ba5f9-109">Entry</span></span> | <span data-ttu-id="ba5f9-110">值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-110">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="ba5f9-111">CN</span><span class="sxs-lookup"><span data-stu-id="ba5f9-111">CN</span></span>                | <span data-ttu-id="ba5f9-112">dhcp 類型</span><span class="sxs-lookup"><span data-stu-id="ba5f9-112">dhcp-Type</span></span>                                              |
| <span data-ttu-id="ba5f9-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ba5f9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ba5f9-114">dhcpType</span><span class="sxs-lookup"><span data-stu-id="ba5f9-114">dhcpType</span></span>                                               |
| <span data-ttu-id="ba5f9-115">大小</span><span class="sxs-lookup"><span data-stu-id="ba5f9-115">Size</span></span>              | <span data-ttu-id="ba5f9-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ba5f9-116">4 bytes</span></span>                                                |
| <span data-ttu-id="ba5f9-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ba5f9-117">Update Privilege</span></span>  | <span data-ttu-id="ba5f9-118">網域系統管理員。</span><span class="sxs-lookup"><span data-stu-id="ba5f9-118">Domain administrator.</span></span>                                  |
| <span data-ttu-id="ba5f9-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ba5f9-119">Update Frequency</span></span>  | <span data-ttu-id="ba5f9-120">在樹系中新增或移除新的伺服器時。</span><span class="sxs-lookup"><span data-stu-id="ba5f9-120">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="ba5f9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ba5f9-121">Attribute-Id</span></span>      | <span data-ttu-id="ba5f9-122">1.2.840.113556.1.4.699</span><span class="sxs-lookup"><span data-stu-id="ba5f9-122">1.2.840.113556.1.4.699</span></span>                                 |
| <span data-ttu-id="ba5f9-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ba5f9-123">System-Id-Guid</span></span>    | <span data-ttu-id="ba5f9-124">963d273b-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ba5f9-124">963d273b-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="ba5f9-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba5f9-125">Syntax</span></span>            | [<span data-ttu-id="ba5f9-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-126">**Enumeration**</span></span>](s-enumeration.md)                   |



## <a name="implementations"></a><span data-ttu-id="ba5f9-127">實作</span><span class="sxs-lookup"><span data-stu-id="ba5f9-127">Implementations</span></span>

-   [<span data-ttu-id="ba5f9-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ba5f9-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ba5f9-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ba5f9-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ba5f9-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ba5f9-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ba5f9-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ba5f9-134">Windows 2000 Server</span></span>



| <span data-ttu-id="ba5f9-135">進入</span><span class="sxs-lookup"><span data-stu-id="ba5f9-135">Entry</span></span> | <span data-ttu-id="ba5f9-136">值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-136">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba5f9-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba5f9-137">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba5f9-138">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba5f9-139">System-Only</span></span>            | <span data-ttu-id="ba5f9-140">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-140">False</span></span>                                        |
| <span data-ttu-id="ba5f9-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ba5f9-142">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-142">True</span></span>                                         |
| <span data-ttu-id="ba5f9-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba5f9-143">Is Indexed</span></span>             | <span data-ttu-id="ba5f9-144">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-144">True</span></span>                                         |
| <span data-ttu-id="ba5f9-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba5f9-145">In Global Catalog</span></span>      | <span data-ttu-id="ba5f9-146">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-146">False</span></span>                                        |
| <span data-ttu-id="ba5f9-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba5f9-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba5f9-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba5f9-148">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba5f9-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba5f9-149">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba5f9-150">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-151">Search-Flags</span></span>           | <span data-ttu-id="ba5f9-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ba5f9-152">0x00000001</span></span>                                   |
| <span data-ttu-id="ba5f9-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-153">System-Flags</span></span>           | <span data-ttu-id="ba5f9-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba5f9-154">0x00000010</span></span>                                   |
| <span data-ttu-id="ba5f9-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba5f9-155">Classes used in</span></span>        | [<span data-ttu-id="ba5f9-156">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-156">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ba5f9-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba5f9-157">Windows Server 2003</span></span>



| <span data-ttu-id="ba5f9-158">進入</span><span class="sxs-lookup"><span data-stu-id="ba5f9-158">Entry</span></span> | <span data-ttu-id="ba5f9-159">值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-159">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba5f9-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba5f9-160">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba5f9-161">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba5f9-162">System-Only</span></span>            | <span data-ttu-id="ba5f9-163">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-163">False</span></span>                                        |
| <span data-ttu-id="ba5f9-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ba5f9-165">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-165">True</span></span>                                         |
| <span data-ttu-id="ba5f9-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba5f9-166">Is Indexed</span></span>             | <span data-ttu-id="ba5f9-167">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-167">True</span></span>                                         |
| <span data-ttu-id="ba5f9-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba5f9-168">In Global Catalog</span></span>      | <span data-ttu-id="ba5f9-169">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-169">False</span></span>                                        |
| <span data-ttu-id="ba5f9-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba5f9-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba5f9-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba5f9-171">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba5f9-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba5f9-172">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba5f9-173">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-174">Search-Flags</span></span>           | <span data-ttu-id="ba5f9-175">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ba5f9-175">0x00000001</span></span>                                   |
| <span data-ttu-id="ba5f9-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-176">System-Flags</span></span>           | <span data-ttu-id="ba5f9-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba5f9-177">0x00000010</span></span>                                   |
| <span data-ttu-id="ba5f9-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba5f9-178">Classes used in</span></span>        | [<span data-ttu-id="ba5f9-179">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-179">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ba5f9-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ba5f9-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ba5f9-181">進入</span><span class="sxs-lookup"><span data-stu-id="ba5f9-181">Entry</span></span> | <span data-ttu-id="ba5f9-182">值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba5f9-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba5f9-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba5f9-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba5f9-185">System-Only</span></span>            | <span data-ttu-id="ba5f9-186">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-186">False</span></span>                                        |
| <span data-ttu-id="ba5f9-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ba5f9-188">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-188">True</span></span>                                         |
| <span data-ttu-id="ba5f9-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba5f9-189">Is Indexed</span></span>             | <span data-ttu-id="ba5f9-190">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-190">True</span></span>                                         |
| <span data-ttu-id="ba5f9-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba5f9-191">In Global Catalog</span></span>      | <span data-ttu-id="ba5f9-192">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-192">False</span></span>                                        |
| <span data-ttu-id="ba5f9-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba5f9-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba5f9-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba5f9-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba5f9-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba5f9-195">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba5f9-196">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-197">Search-Flags</span></span>           | <span data-ttu-id="ba5f9-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ba5f9-198">0x00000001</span></span>                                   |
| <span data-ttu-id="ba5f9-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-199">System-Flags</span></span>           | <span data-ttu-id="ba5f9-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba5f9-200">0x00000010</span></span>                                   |
| <span data-ttu-id="ba5f9-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba5f9-201">Classes used in</span></span>        | [<span data-ttu-id="ba5f9-202">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-202">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ba5f9-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba5f9-203">Windows Server 2008</span></span>



| <span data-ttu-id="ba5f9-204">進入</span><span class="sxs-lookup"><span data-stu-id="ba5f9-204">Entry</span></span> | <span data-ttu-id="ba5f9-205">值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-205">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba5f9-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba5f9-206">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba5f9-207">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba5f9-208">System-Only</span></span>            | <span data-ttu-id="ba5f9-209">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-209">False</span></span>                                        |
| <span data-ttu-id="ba5f9-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ba5f9-211">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-211">True</span></span>                                         |
| <span data-ttu-id="ba5f9-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba5f9-212">Is Indexed</span></span>             | <span data-ttu-id="ba5f9-213">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-213">True</span></span>                                         |
| <span data-ttu-id="ba5f9-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba5f9-214">In Global Catalog</span></span>      | <span data-ttu-id="ba5f9-215">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-215">False</span></span>                                        |
| <span data-ttu-id="ba5f9-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba5f9-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba5f9-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba5f9-217">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba5f9-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba5f9-218">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba5f9-219">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-220">Search-Flags</span></span>           | <span data-ttu-id="ba5f9-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ba5f9-221">0x00000001</span></span>                                   |
| <span data-ttu-id="ba5f9-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-222">System-Flags</span></span>           | <span data-ttu-id="ba5f9-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba5f9-223">0x00000010</span></span>                                   |
| <span data-ttu-id="ba5f9-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba5f9-224">Classes used in</span></span>        | [<span data-ttu-id="ba5f9-225">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-225">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ba5f9-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba5f9-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ba5f9-227">進入</span><span class="sxs-lookup"><span data-stu-id="ba5f9-227">Entry</span></span> | <span data-ttu-id="ba5f9-228">值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-228">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba5f9-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba5f9-229">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba5f9-230">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba5f9-231">System-Only</span></span>            | <span data-ttu-id="ba5f9-232">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-232">False</span></span>                                        |
| <span data-ttu-id="ba5f9-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-233">Is-Single-Valued</span></span>       | <span data-ttu-id="ba5f9-234">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-234">True</span></span>                                         |
| <span data-ttu-id="ba5f9-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba5f9-235">Is Indexed</span></span>             | <span data-ttu-id="ba5f9-236">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-236">True</span></span>                                         |
| <span data-ttu-id="ba5f9-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba5f9-237">In Global Catalog</span></span>      | <span data-ttu-id="ba5f9-238">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-238">False</span></span>                                        |
| <span data-ttu-id="ba5f9-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba5f9-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba5f9-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba5f9-240">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba5f9-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba5f9-241">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba5f9-242">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-243">Search-Flags</span></span>           | <span data-ttu-id="ba5f9-244">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ba5f9-244">0x00000001</span></span>                                   |
| <span data-ttu-id="ba5f9-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-245">System-Flags</span></span>           | <span data-ttu-id="ba5f9-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba5f9-246">0x00000010</span></span>                                   |
| <span data-ttu-id="ba5f9-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba5f9-247">Classes used in</span></span>        | [<span data-ttu-id="ba5f9-248">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-248">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ba5f9-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ba5f9-249">Windows Server 2012</span></span>



| <span data-ttu-id="ba5f9-250">進入</span><span class="sxs-lookup"><span data-stu-id="ba5f9-250">Entry</span></span> | <span data-ttu-id="ba5f9-251">值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-251">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ba5f9-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba5f9-252">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba5f9-253">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ba5f9-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba5f9-254">System-Only</span></span>            | <span data-ttu-id="ba5f9-255">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-255">False</span></span>                                        |
| <span data-ttu-id="ba5f9-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba5f9-256">Is-Single-Valued</span></span>       | <span data-ttu-id="ba5f9-257">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-257">True</span></span>                                         |
| <span data-ttu-id="ba5f9-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba5f9-258">Is Indexed</span></span>             | <span data-ttu-id="ba5f9-259">對</span><span class="sxs-lookup"><span data-stu-id="ba5f9-259">True</span></span>                                         |
| <span data-ttu-id="ba5f9-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba5f9-260">In Global Catalog</span></span>      | <span data-ttu-id="ba5f9-261">否</span><span class="sxs-lookup"><span data-stu-id="ba5f9-261">False</span></span>                                        |
| <span data-ttu-id="ba5f9-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba5f9-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba5f9-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba5f9-263">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ba5f9-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba5f9-264">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba5f9-265">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ba5f9-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-266">Search-Flags</span></span>           | <span data-ttu-id="ba5f9-267">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ba5f9-267">0x00000001</span></span>                                   |
| <span data-ttu-id="ba5f9-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba5f9-268">System-Flags</span></span>           | <span data-ttu-id="ba5f9-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba5f9-269">0x00000010</span></span>                                   |
| <span data-ttu-id="ba5f9-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba5f9-270">Classes used in</span></span>        | [<span data-ttu-id="ba5f9-271">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="ba5f9-271">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 






---
title: 屬性-安全性-GUID 屬性
description: 用來將安全性認證套用至一組物件的 GUID。
ms.assetid: df4709ec-273d-4294-8094-f396c10c06e2
ms.tgt_platform: multiple
keywords:
- 屬性-安全性-GUID 屬性 AD 架構
- attributeSecurityGUID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Attribute-Security-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b2ada7c6c806bec1c524b0408750144ca1fd8b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104187364"
---
# <a name="attribute-security-guid-attribute"></a><span data-ttu-id="8cf6c-105">屬性-安全性-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="8cf6c-105">Attribute-Security-GUID attribute</span></span>

<span data-ttu-id="8cf6c-106">用來將安全性認證套用至一組物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8cf6c-106">The GUID to be used to apply security credentials to a set of objects.</span></span>



| <span data-ttu-id="8cf6c-107">進入</span><span class="sxs-lookup"><span data-stu-id="8cf6c-107">Entry</span></span> | <span data-ttu-id="8cf6c-108">值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="8cf6c-109">CN</span><span class="sxs-lookup"><span data-stu-id="8cf6c-109">CN</span></span>                | <span data-ttu-id="8cf6c-110">屬性-安全性-GUID</span><span class="sxs-lookup"><span data-stu-id="8cf6c-110">Attribute-Security-GUID</span></span>                               |
| <span data-ttu-id="8cf6c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8cf6c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8cf6c-112">attributeSecurityGUID</span><span class="sxs-lookup"><span data-stu-id="8cf6c-112">attributeSecurityGUID</span></span>                                 |
| <span data-ttu-id="8cf6c-113">大小</span><span class="sxs-lookup"><span data-stu-id="8cf6c-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="8cf6c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8cf6c-114">Update Privilege</span></span>  | <span data-ttu-id="8cf6c-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="8cf6c-115">Schema administrator</span></span>                                  |
| <span data-ttu-id="8cf6c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8cf6c-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="8cf6c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8cf6c-117">Attribute-Id</span></span>      | <span data-ttu-id="8cf6c-118">1.2.840.113556.1.4.149</span><span class="sxs-lookup"><span data-stu-id="8cf6c-118">1.2.840.113556.1.4.149</span></span>                                |
| <span data-ttu-id="8cf6c-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8cf6c-119">System-Id-Guid</span></span>    | <span data-ttu-id="8cf6c-120">bf967924-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8cf6c-120">bf967924-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="8cf6c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cf6c-121">Syntax</span></span>            | [<span data-ttu-id="8cf6c-122">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="8cf6c-123">實作</span><span class="sxs-lookup"><span data-stu-id="8cf6c-123">Implementations</span></span>

-   [<span data-ttu-id="8cf6c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8cf6c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8cf6c-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8cf6c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8cf6c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8cf6c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8cf6c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8cf6c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8cf6c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8cf6c-132">進入</span><span class="sxs-lookup"><span data-stu-id="8cf6c-132">Entry</span></span> | <span data-ttu-id="8cf6c-133">值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="8cf6c-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8cf6c-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf6c-135">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf6c-136">System-Only</span></span>            | <span data-ttu-id="8cf6c-137">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-137">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf6c-139">對</span><span class="sxs-lookup"><span data-stu-id="8cf6c-139">True</span></span>                                                     |
| <span data-ttu-id="8cf6c-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8cf6c-140">Is Indexed</span></span>             | <span data-ttu-id="8cf6c-141">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-141">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8cf6c-142">In Global Catalog</span></span>      | <span data-ttu-id="8cf6c-143">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-143">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8cf6c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf6c-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8cf6c-145">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="8cf6c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf6c-146">Range-Lower</span></span>            | <span data-ttu-id="8cf6c-147">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-147">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf6c-148">Range-Upper</span></span>            | <span data-ttu-id="8cf6c-149">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-149">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-150">Search-Flags</span></span>           | <span data-ttu-id="8cf6c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf6c-151">0x00000000</span></span>                                               |
| <span data-ttu-id="8cf6c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-152">System-Flags</span></span>           | <span data-ttu-id="8cf6c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf6c-153">0x00000010</span></span>                                               |
| <span data-ttu-id="8cf6c-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8cf6c-154">Classes used in</span></span>        | [<span data-ttu-id="8cf6c-155">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8cf6c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cf6c-156">Windows Server 2003</span></span>



| <span data-ttu-id="8cf6c-157">進入</span><span class="sxs-lookup"><span data-stu-id="8cf6c-157">Entry</span></span> | <span data-ttu-id="8cf6c-158">值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="8cf6c-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8cf6c-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf6c-160">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf6c-161">System-Only</span></span>            | <span data-ttu-id="8cf6c-162">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-162">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf6c-164">對</span><span class="sxs-lookup"><span data-stu-id="8cf6c-164">True</span></span>                                                     |
| <span data-ttu-id="8cf6c-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8cf6c-165">Is Indexed</span></span>             | <span data-ttu-id="8cf6c-166">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-166">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8cf6c-167">In Global Catalog</span></span>      | <span data-ttu-id="8cf6c-168">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-168">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8cf6c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf6c-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8cf6c-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="8cf6c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf6c-171">Range-Lower</span></span>            | <span data-ttu-id="8cf6c-172">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-172">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf6c-173">Range-Upper</span></span>            | <span data-ttu-id="8cf6c-174">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-174">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-175">Search-Flags</span></span>           | <span data-ttu-id="8cf6c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf6c-176">0x00000000</span></span>                                               |
| <span data-ttu-id="8cf6c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-177">System-Flags</span></span>           | <span data-ttu-id="8cf6c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf6c-178">0x00000010</span></span>                                               |
| <span data-ttu-id="8cf6c-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8cf6c-179">Classes used in</span></span>        | [<span data-ttu-id="8cf6c-180">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8cf6c-181">亞當</span><span class="sxs-lookup"><span data-stu-id="8cf6c-181">ADAM</span></span>



| <span data-ttu-id="8cf6c-182">進入</span><span class="sxs-lookup"><span data-stu-id="8cf6c-182">Entry</span></span> | <span data-ttu-id="8cf6c-183">值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="8cf6c-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8cf6c-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf6c-185">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf6c-186">System-Only</span></span>            | <span data-ttu-id="8cf6c-187">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-187">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf6c-189">對</span><span class="sxs-lookup"><span data-stu-id="8cf6c-189">True</span></span>                                                     |
| <span data-ttu-id="8cf6c-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8cf6c-190">Is Indexed</span></span>             | <span data-ttu-id="8cf6c-191">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-191">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8cf6c-192">In Global Catalog</span></span>      | <span data-ttu-id="8cf6c-193">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-193">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8cf6c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf6c-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8cf6c-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="8cf6c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf6c-196">Range-Lower</span></span>            | <span data-ttu-id="8cf6c-197">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-197">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf6c-198">Range-Upper</span></span>            | <span data-ttu-id="8cf6c-199">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-199">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-200">Search-Flags</span></span>           | <span data-ttu-id="8cf6c-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf6c-201">0x00000000</span></span>                                               |
| <span data-ttu-id="8cf6c-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-202">System-Flags</span></span>           | <span data-ttu-id="8cf6c-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf6c-203">0x00000010</span></span>                                               |
| <span data-ttu-id="8cf6c-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8cf6c-204">Classes used in</span></span>        | [<span data-ttu-id="8cf6c-205">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-205">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8cf6c-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8cf6c-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8cf6c-207">進入</span><span class="sxs-lookup"><span data-stu-id="8cf6c-207">Entry</span></span> | <span data-ttu-id="8cf6c-208">值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-208">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="8cf6c-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8cf6c-209">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf6c-210">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf6c-211">System-Only</span></span>            | <span data-ttu-id="8cf6c-212">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-212">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf6c-214">對</span><span class="sxs-lookup"><span data-stu-id="8cf6c-214">True</span></span>                                                     |
| <span data-ttu-id="8cf6c-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8cf6c-215">Is Indexed</span></span>             | <span data-ttu-id="8cf6c-216">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-216">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8cf6c-217">In Global Catalog</span></span>      | <span data-ttu-id="8cf6c-218">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-218">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8cf6c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf6c-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8cf6c-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="8cf6c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf6c-221">Range-Lower</span></span>            | <span data-ttu-id="8cf6c-222">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-222">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf6c-223">Range-Upper</span></span>            | <span data-ttu-id="8cf6c-224">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-224">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-225">Search-Flags</span></span>           | <span data-ttu-id="8cf6c-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf6c-226">0x00000000</span></span>                                               |
| <span data-ttu-id="8cf6c-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-227">System-Flags</span></span>           | <span data-ttu-id="8cf6c-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf6c-228">0x00000010</span></span>                                               |
| <span data-ttu-id="8cf6c-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8cf6c-229">Classes used in</span></span>        | [<span data-ttu-id="8cf6c-230">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-230">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8cf6c-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cf6c-231">Windows Server 2008</span></span>



| <span data-ttu-id="8cf6c-232">進入</span><span class="sxs-lookup"><span data-stu-id="8cf6c-232">Entry</span></span> | <span data-ttu-id="8cf6c-233">值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-233">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="8cf6c-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8cf6c-234">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf6c-235">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf6c-236">System-Only</span></span>            | <span data-ttu-id="8cf6c-237">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-237">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-238">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf6c-239">對</span><span class="sxs-lookup"><span data-stu-id="8cf6c-239">True</span></span>                                                     |
| <span data-ttu-id="8cf6c-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8cf6c-240">Is Indexed</span></span>             | <span data-ttu-id="8cf6c-241">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-241">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8cf6c-242">In Global Catalog</span></span>      | <span data-ttu-id="8cf6c-243">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-243">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8cf6c-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf6c-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8cf6c-245">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="8cf6c-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf6c-246">Range-Lower</span></span>            | <span data-ttu-id="8cf6c-247">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-247">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf6c-248">Range-Upper</span></span>            | <span data-ttu-id="8cf6c-249">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-249">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-250">Search-Flags</span></span>           | <span data-ttu-id="8cf6c-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf6c-251">0x00000000</span></span>                                               |
| <span data-ttu-id="8cf6c-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-252">System-Flags</span></span>           | <span data-ttu-id="8cf6c-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf6c-253">0x00000010</span></span>                                               |
| <span data-ttu-id="8cf6c-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8cf6c-254">Classes used in</span></span>        | [<span data-ttu-id="8cf6c-255">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-255">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8cf6c-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8cf6c-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8cf6c-257">進入</span><span class="sxs-lookup"><span data-stu-id="8cf6c-257">Entry</span></span> | <span data-ttu-id="8cf6c-258">值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-258">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="8cf6c-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8cf6c-259">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf6c-260">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf6c-261">System-Only</span></span>            | <span data-ttu-id="8cf6c-262">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-262">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-263">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf6c-264">對</span><span class="sxs-lookup"><span data-stu-id="8cf6c-264">True</span></span>                                                     |
| <span data-ttu-id="8cf6c-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8cf6c-265">Is Indexed</span></span>             | <span data-ttu-id="8cf6c-266">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-266">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8cf6c-267">In Global Catalog</span></span>      | <span data-ttu-id="8cf6c-268">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-268">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8cf6c-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf6c-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8cf6c-270">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="8cf6c-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf6c-271">Range-Lower</span></span>            | <span data-ttu-id="8cf6c-272">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-272">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf6c-273">Range-Upper</span></span>            | <span data-ttu-id="8cf6c-274">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-274">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-275">Search-Flags</span></span>           | <span data-ttu-id="8cf6c-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf6c-276">0x00000000</span></span>                                               |
| <span data-ttu-id="8cf6c-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-277">System-Flags</span></span>           | <span data-ttu-id="8cf6c-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf6c-278">0x00000010</span></span>                                               |
| <span data-ttu-id="8cf6c-279">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8cf6c-279">Classes used in</span></span>        | [<span data-ttu-id="8cf6c-280">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-280">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8cf6c-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8cf6c-281">Windows Server 2012</span></span>



| <span data-ttu-id="8cf6c-282">進入</span><span class="sxs-lookup"><span data-stu-id="8cf6c-282">Entry</span></span> | <span data-ttu-id="8cf6c-283">值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-283">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="8cf6c-284">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8cf6c-284">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cf6c-285">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="8cf6c-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cf6c-286">System-Only</span></span>            | <span data-ttu-id="8cf6c-287">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-287">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-288">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8cf6c-288">Is-Single-Valued</span></span>       | <span data-ttu-id="8cf6c-289">對</span><span class="sxs-lookup"><span data-stu-id="8cf6c-289">True</span></span>                                                     |
| <span data-ttu-id="8cf6c-290">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8cf6c-290">Is Indexed</span></span>             | <span data-ttu-id="8cf6c-291">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-291">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-292">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8cf6c-292">In Global Catalog</span></span>      | <span data-ttu-id="8cf6c-293">否</span><span class="sxs-lookup"><span data-stu-id="8cf6c-293">False</span></span>                                                    |
| <span data-ttu-id="8cf6c-294">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8cf6c-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cf6c-295">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8cf6c-295">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="8cf6c-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cf6c-296">Range-Lower</span></span>            | <span data-ttu-id="8cf6c-297">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-297">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cf6c-298">Range-Upper</span></span>            | <span data-ttu-id="8cf6c-299">16</span><span class="sxs-lookup"><span data-stu-id="8cf6c-299">16</span></span>                                                       |
| <span data-ttu-id="8cf6c-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-300">Search-Flags</span></span>           | <span data-ttu-id="8cf6c-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cf6c-301">0x00000000</span></span>                                               |
| <span data-ttu-id="8cf6c-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cf6c-302">System-Flags</span></span>           | <span data-ttu-id="8cf6c-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cf6c-303">0x00000010</span></span>                                               |
| <span data-ttu-id="8cf6c-304">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8cf6c-304">Classes used in</span></span>        | [<span data-ttu-id="8cf6c-305">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="8cf6c-305">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 






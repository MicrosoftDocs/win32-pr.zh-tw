---
title: 架構識別碼-GUID 屬性
description: 屬性的唯一識別碼。
ms.assetid: 50f0a4b6-dded-42db-9ac5-123f2885c658
ms.tgt_platform: multiple
keywords:
- 架構識別碼-GUID 屬性 AD 架構
- schemaIDGUID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Schema-ID-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f0b16cc45ecfbcd03e2104cbc6c5b5b41bd813
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107544"
---
# <a name="schema-id-guid-attribute"></a><span data-ttu-id="0b6d2-105">架構識別碼-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="0b6d2-105">Schema-ID-GUID attribute</span></span>

<span data-ttu-id="0b6d2-106">屬性的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b6d2-106">The unique identifier for an attribute.</span></span>



| <span data-ttu-id="0b6d2-107">進入</span><span class="sxs-lookup"><span data-stu-id="0b6d2-107">Entry</span></span> | <span data-ttu-id="0b6d2-108">值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0b6d2-109">CN</span><span class="sxs-lookup"><span data-stu-id="0b6d2-109">CN</span></span>                | <span data-ttu-id="0b6d2-110">架構識別碼-GUID</span><span class="sxs-lookup"><span data-stu-id="0b6d2-110">Schema-ID-GUID</span></span>                                                      |
| <span data-ttu-id="0b6d2-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0b6d2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0b6d2-112">schemaIDGUID</span><span class="sxs-lookup"><span data-stu-id="0b6d2-112">schemaIDGUID</span></span>                                                        |
| <span data-ttu-id="0b6d2-113">大小</span><span class="sxs-lookup"><span data-stu-id="0b6d2-113">Size</span></span>              | <span data-ttu-id="0b6d2-114">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="0b6d2-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="0b6d2-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0b6d2-115">Update Privilege</span></span>  | <span data-ttu-id="0b6d2-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="0b6d2-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="0b6d2-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0b6d2-117">Update Frequency</span></span>  | <span data-ttu-id="0b6d2-118">此值是在建立物件時設定的，而且無法變更。</span><span class="sxs-lookup"><span data-stu-id="0b6d2-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="0b6d2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b6d2-119">Attribute-Id</span></span>      | <span data-ttu-id="0b6d2-120">1.2.840.113556.1.4.148</span><span class="sxs-lookup"><span data-stu-id="0b6d2-120">1.2.840.113556.1.4.148</span></span>                                              |
| <span data-ttu-id="0b6d2-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0b6d2-121">System-Id-Guid</span></span>    | <span data-ttu-id="0b6d2-122">bf967923-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0b6d2-122">bf967923-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="0b6d2-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b6d2-123">Syntax</span></span>            | [<span data-ttu-id="0b6d2-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="0b6d2-125">實作</span><span class="sxs-lookup"><span data-stu-id="0b6d2-125">Implementations</span></span>

-   [<span data-ttu-id="0b6d2-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0b6d2-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b6d2-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0b6d2-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b6d2-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b6d2-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b6d2-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0b6d2-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b6d2-133">Windows 2000 Server</span></span>



| <span data-ttu-id="0b6d2-134">進入</span><span class="sxs-lookup"><span data-stu-id="0b6d2-134">Entry</span></span> | <span data-ttu-id="0b6d2-135">值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6d2-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b6d2-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b6d2-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b6d2-138">System-Only</span></span>            | <span data-ttu-id="0b6d2-139">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-139">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-140">Is-Single-Valued</span></span>       | <span data-ttu-id="0b6d2-141">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-141">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b6d2-142">Is Indexed</span></span>             | <span data-ttu-id="0b6d2-143">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-143">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b6d2-144">In Global Catalog</span></span>      | <span data-ttu-id="0b6d2-145">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-145">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b6d2-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b6d2-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b6d2-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0b6d2-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b6d2-148">Range-Lower</span></span>            | <span data-ttu-id="0b6d2-149">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-149">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b6d2-150">Range-Upper</span></span>            | <span data-ttu-id="0b6d2-151">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-151">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-152">Search-Flags</span></span>           | <span data-ttu-id="0b6d2-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b6d2-153">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-154">System-Flags</span></span>           | <span data-ttu-id="0b6d2-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b6d2-155">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b6d2-156">Classes used in</span></span>        | [<span data-ttu-id="0b6d2-157">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-157">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0b6d2-158">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-158">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0b6d2-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b6d2-159">Windows Server 2003</span></span>



| <span data-ttu-id="0b6d2-160">進入</span><span class="sxs-lookup"><span data-stu-id="0b6d2-160">Entry</span></span> | <span data-ttu-id="0b6d2-161">值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6d2-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b6d2-162">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b6d2-163">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b6d2-164">System-Only</span></span>            | <span data-ttu-id="0b6d2-165">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-165">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-166">Is-Single-Valued</span></span>       | <span data-ttu-id="0b6d2-167">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-167">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b6d2-168">Is Indexed</span></span>             | <span data-ttu-id="0b6d2-169">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-169">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b6d2-170">In Global Catalog</span></span>      | <span data-ttu-id="0b6d2-171">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-171">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b6d2-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b6d2-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b6d2-173">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0b6d2-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b6d2-174">Range-Lower</span></span>            | <span data-ttu-id="0b6d2-175">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-175">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b6d2-176">Range-Upper</span></span>            | <span data-ttu-id="0b6d2-177">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-177">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-178">Search-Flags</span></span>           | <span data-ttu-id="0b6d2-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b6d2-179">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-180">System-Flags</span></span>           | <span data-ttu-id="0b6d2-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b6d2-181">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b6d2-182">Classes used in</span></span>        | [<span data-ttu-id="0b6d2-183">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-183">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0b6d2-184">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-184">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0b6d2-185">亞當</span><span class="sxs-lookup"><span data-stu-id="0b6d2-185">ADAM</span></span>



| <span data-ttu-id="0b6d2-186">進入</span><span class="sxs-lookup"><span data-stu-id="0b6d2-186">Entry</span></span> | <span data-ttu-id="0b6d2-187">值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-187">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6d2-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b6d2-188">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b6d2-189">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b6d2-190">System-Only</span></span>            | <span data-ttu-id="0b6d2-191">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-191">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-192">Is-Single-Valued</span></span>       | <span data-ttu-id="0b6d2-193">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-193">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b6d2-194">Is Indexed</span></span>             | <span data-ttu-id="0b6d2-195">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-195">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b6d2-196">In Global Catalog</span></span>      | <span data-ttu-id="0b6d2-197">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-197">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b6d2-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b6d2-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b6d2-199">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0b6d2-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b6d2-200">Range-Lower</span></span>            | <span data-ttu-id="0b6d2-201">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-201">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b6d2-202">Range-Upper</span></span>            | <span data-ttu-id="0b6d2-203">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-203">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-204">Search-Flags</span></span>           | <span data-ttu-id="0b6d2-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b6d2-205">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-206">System-Flags</span></span>           | <span data-ttu-id="0b6d2-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b6d2-207">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b6d2-208">Classes used in</span></span>        | [<span data-ttu-id="0b6d2-209">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-209">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0b6d2-210">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-210">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b6d2-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b6d2-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b6d2-212">進入</span><span class="sxs-lookup"><span data-stu-id="0b6d2-212">Entry</span></span> | <span data-ttu-id="0b6d2-213">值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-213">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6d2-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b6d2-214">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b6d2-215">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b6d2-216">System-Only</span></span>            | <span data-ttu-id="0b6d2-217">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-217">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-218">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-218">Is-Single-Valued</span></span>       | <span data-ttu-id="0b6d2-219">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-219">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-220">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b6d2-220">Is Indexed</span></span>             | <span data-ttu-id="0b6d2-221">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-221">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-222">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b6d2-222">In Global Catalog</span></span>      | <span data-ttu-id="0b6d2-223">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-223">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-224">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b6d2-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b6d2-225">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b6d2-225">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0b6d2-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b6d2-226">Range-Lower</span></span>            | <span data-ttu-id="0b6d2-227">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-227">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b6d2-228">Range-Upper</span></span>            | <span data-ttu-id="0b6d2-229">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-229">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-230">Search-Flags</span></span>           | <span data-ttu-id="0b6d2-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b6d2-231">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-232">System-Flags</span></span>           | <span data-ttu-id="0b6d2-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b6d2-233">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-234">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b6d2-234">Classes used in</span></span>        | [<span data-ttu-id="0b6d2-235">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-235">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0b6d2-236">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-236">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b6d2-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b6d2-237">Windows Server 2008</span></span>



| <span data-ttu-id="0b6d2-238">進入</span><span class="sxs-lookup"><span data-stu-id="0b6d2-238">Entry</span></span> | <span data-ttu-id="0b6d2-239">值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-239">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6d2-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b6d2-240">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b6d2-241">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b6d2-242">System-Only</span></span>            | <span data-ttu-id="0b6d2-243">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-243">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-244">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-244">Is-Single-Valued</span></span>       | <span data-ttu-id="0b6d2-245">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-245">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-246">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b6d2-246">Is Indexed</span></span>             | <span data-ttu-id="0b6d2-247">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-247">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-248">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b6d2-248">In Global Catalog</span></span>      | <span data-ttu-id="0b6d2-249">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-249">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-250">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b6d2-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b6d2-251">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b6d2-251">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0b6d2-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b6d2-252">Range-Lower</span></span>            | <span data-ttu-id="0b6d2-253">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-253">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b6d2-254">Range-Upper</span></span>            | <span data-ttu-id="0b6d2-255">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-255">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-256">Search-Flags</span></span>           | <span data-ttu-id="0b6d2-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b6d2-257">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-258">System-Flags</span></span>           | <span data-ttu-id="0b6d2-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b6d2-259">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-260">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b6d2-260">Classes used in</span></span>        | [<span data-ttu-id="0b6d2-261">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-261">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0b6d2-262">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-262">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b6d2-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b6d2-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b6d2-264">進入</span><span class="sxs-lookup"><span data-stu-id="0b6d2-264">Entry</span></span> | <span data-ttu-id="0b6d2-265">值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-265">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6d2-266">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b6d2-266">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b6d2-267">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b6d2-268">System-Only</span></span>            | <span data-ttu-id="0b6d2-269">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-269">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-270">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-270">Is-Single-Valued</span></span>       | <span data-ttu-id="0b6d2-271">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-271">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-272">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b6d2-272">Is Indexed</span></span>             | <span data-ttu-id="0b6d2-273">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-273">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-274">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b6d2-274">In Global Catalog</span></span>      | <span data-ttu-id="0b6d2-275">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-275">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-276">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b6d2-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b6d2-277">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b6d2-277">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0b6d2-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b6d2-278">Range-Lower</span></span>            | <span data-ttu-id="0b6d2-279">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-279">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b6d2-280">Range-Upper</span></span>            | <span data-ttu-id="0b6d2-281">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-281">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-282">Search-Flags</span></span>           | <span data-ttu-id="0b6d2-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b6d2-283">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-284">System-Flags</span></span>           | <span data-ttu-id="0b6d2-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b6d2-285">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-286">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b6d2-286">Classes used in</span></span>        | [<span data-ttu-id="0b6d2-287">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-287">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0b6d2-288">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-288">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b6d2-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b6d2-289">Windows Server 2012</span></span>



| <span data-ttu-id="0b6d2-290">進入</span><span class="sxs-lookup"><span data-stu-id="0b6d2-290">Entry</span></span> | <span data-ttu-id="0b6d2-291">值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-291">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6d2-292">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b6d2-292">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b6d2-293">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="0b6d2-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b6d2-294">System-Only</span></span>            | <span data-ttu-id="0b6d2-295">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-295">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-296">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b6d2-296">Is-Single-Valued</span></span>       | <span data-ttu-id="0b6d2-297">對</span><span class="sxs-lookup"><span data-stu-id="0b6d2-297">True</span></span>                                                                                                      |
| <span data-ttu-id="0b6d2-298">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b6d2-298">Is Indexed</span></span>             | <span data-ttu-id="0b6d2-299">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-299">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-300">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b6d2-300">In Global Catalog</span></span>      | <span data-ttu-id="0b6d2-301">否</span><span class="sxs-lookup"><span data-stu-id="0b6d2-301">False</span></span>                                                                                                     |
| <span data-ttu-id="0b6d2-302">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b6d2-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b6d2-303">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b6d2-303">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="0b6d2-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b6d2-304">Range-Lower</span></span>            | <span data-ttu-id="0b6d2-305">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-305">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b6d2-306">Range-Upper</span></span>            | <span data-ttu-id="0b6d2-307">16</span><span class="sxs-lookup"><span data-stu-id="0b6d2-307">16</span></span>                                                                                                        |
| <span data-ttu-id="0b6d2-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-308">Search-Flags</span></span>           | <span data-ttu-id="0b6d2-309">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b6d2-309">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b6d2-310">System-Flags</span></span>           | <span data-ttu-id="0b6d2-311">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b6d2-311">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="0b6d2-312">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b6d2-312">Classes used in</span></span>        | [<span data-ttu-id="0b6d2-313">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-313">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="0b6d2-314">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-314">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 






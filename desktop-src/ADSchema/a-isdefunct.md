---
title: Is-Defunct 屬性
description: 若為 TRUE，則表示類別或屬性無法再使用。 此物件的舊版可能存在，但無法建立新的版本。
ms.assetid: ca1b7701-e501-424d-9c07-20835b23dcd3
ms.tgt_platform: multiple
keywords:
- Is-Defunct 屬性 AD 架構
- isDefunct 屬性 AD 架構
topic_type:
- apiref
api_name:
- Is-Defunct
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895a4af5d02c76a709607753065b6e965966bb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970479"
---
# <a name="is-defunct-attribute"></a><span data-ttu-id="7ccc8-106">Is-Defunct 屬性</span><span class="sxs-lookup"><span data-stu-id="7ccc8-106">Is-Defunct attribute</span></span>

<span data-ttu-id="7ccc8-107">若 **為 TRUE**，則表示類別或屬性無法再使用。</span><span class="sxs-lookup"><span data-stu-id="7ccc8-107">If **TRUE**, the class or attribute is no longer usable.</span></span> <span data-ttu-id="7ccc8-108">此物件的舊版可能存在，但無法建立新的版本。</span><span class="sxs-lookup"><span data-stu-id="7ccc8-108">Old versions of this object may exist, but new ones cannot be created.</span></span>



| <span data-ttu-id="7ccc8-109">進入</span><span class="sxs-lookup"><span data-stu-id="7ccc8-109">Entry</span></span> | <span data-ttu-id="7ccc8-110">值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7ccc8-111">CN</span><span class="sxs-lookup"><span data-stu-id="7ccc8-111">CN</span></span>                | <span data-ttu-id="7ccc8-112">Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="7ccc8-112">Is-Defunct</span></span>                           |
| <span data-ttu-id="7ccc8-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7ccc8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7ccc8-114">isDefunct</span><span class="sxs-lookup"><span data-stu-id="7ccc8-114">isDefunct</span></span>                            |
| <span data-ttu-id="7ccc8-115">大小</span><span class="sxs-lookup"><span data-stu-id="7ccc8-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="7ccc8-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7ccc8-116">Update Privilege</span></span>  | <span data-ttu-id="7ccc8-117">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="7ccc8-117">Schema administrator</span></span>                 |
| <span data-ttu-id="7ccc8-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7ccc8-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7ccc8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ccc8-119">Attribute-Id</span></span>      | <span data-ttu-id="7ccc8-120">1.2.840.113556.1.4.661</span><span class="sxs-lookup"><span data-stu-id="7ccc8-120">1.2.840.113556.1.4.661</span></span>               |
| <span data-ttu-id="7ccc8-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7ccc8-121">System-Id-Guid</span></span>    | <span data-ttu-id="7ccc8-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7ccc8-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span></span> |
| <span data-ttu-id="7ccc8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ccc8-123">Syntax</span></span>            | [<span data-ttu-id="7ccc8-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="7ccc8-125">實作</span><span class="sxs-lookup"><span data-stu-id="7ccc8-125">Implementations</span></span>

-   [<span data-ttu-id="7ccc8-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7ccc8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ccc8-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7ccc8-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ccc8-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ccc8-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ccc8-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7ccc8-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ccc8-133">Windows 2000 Server</span></span>



| <span data-ttu-id="7ccc8-134">進入</span><span class="sxs-lookup"><span data-stu-id="7ccc8-134">Entry</span></span> | <span data-ttu-id="7ccc8-135">值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccc8-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ccc8-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccc8-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccc8-138">System-Only</span></span>            | <span data-ttu-id="7ccc8-139">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-139">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-140">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccc8-141">對</span><span class="sxs-lookup"><span data-stu-id="7ccc8-141">True</span></span>                                                                                                      |
| <span data-ttu-id="7ccc8-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ccc8-142">Is Indexed</span></span>             | <span data-ttu-id="7ccc8-143">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-143">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ccc8-144">In Global Catalog</span></span>      | <span data-ttu-id="7ccc8-145">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-145">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ccc8-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccc8-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ccc8-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="7ccc8-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccc8-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccc8-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-150">Search-Flags</span></span>           | <span data-ttu-id="7ccc8-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccc8-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-152">System-Flags</span></span>           | <span data-ttu-id="7ccc8-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccc8-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ccc8-154">Classes used in</span></span>        | [<span data-ttu-id="7ccc8-155">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="7ccc8-156">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7ccc8-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ccc8-157">Windows Server 2003</span></span>



| <span data-ttu-id="7ccc8-158">進入</span><span class="sxs-lookup"><span data-stu-id="7ccc8-158">Entry</span></span> | <span data-ttu-id="7ccc8-159">值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccc8-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ccc8-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccc8-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccc8-162">System-Only</span></span>            | <span data-ttu-id="7ccc8-163">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-163">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccc8-165">對</span><span class="sxs-lookup"><span data-stu-id="7ccc8-165">True</span></span>                                                                                                      |
| <span data-ttu-id="7ccc8-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ccc8-166">Is Indexed</span></span>             | <span data-ttu-id="7ccc8-167">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-167">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ccc8-168">In Global Catalog</span></span>      | <span data-ttu-id="7ccc8-169">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-169">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ccc8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccc8-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ccc8-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="7ccc8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccc8-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccc8-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-174">Search-Flags</span></span>           | <span data-ttu-id="7ccc8-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccc8-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-176">System-Flags</span></span>           | <span data-ttu-id="7ccc8-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccc8-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ccc8-178">Classes used in</span></span>        | [<span data-ttu-id="7ccc8-179">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="7ccc8-180">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7ccc8-181">亞當</span><span class="sxs-lookup"><span data-stu-id="7ccc8-181">ADAM</span></span>



| <span data-ttu-id="7ccc8-182">進入</span><span class="sxs-lookup"><span data-stu-id="7ccc8-182">Entry</span></span> | <span data-ttu-id="7ccc8-183">值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccc8-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ccc8-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccc8-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccc8-186">System-Only</span></span>            | <span data-ttu-id="7ccc8-187">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-187">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-188">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccc8-189">對</span><span class="sxs-lookup"><span data-stu-id="7ccc8-189">True</span></span>                                                                                                      |
| <span data-ttu-id="7ccc8-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ccc8-190">Is Indexed</span></span>             | <span data-ttu-id="7ccc8-191">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-191">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ccc8-192">In Global Catalog</span></span>      | <span data-ttu-id="7ccc8-193">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-193">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ccc8-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccc8-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ccc8-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="7ccc8-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccc8-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccc8-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-198">Search-Flags</span></span>           | <span data-ttu-id="7ccc8-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccc8-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-200">System-Flags</span></span>           | <span data-ttu-id="7ccc8-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccc8-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ccc8-202">Classes used in</span></span>        | [<span data-ttu-id="7ccc8-203">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="7ccc8-204">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ccc8-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ccc8-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ccc8-206">進入</span><span class="sxs-lookup"><span data-stu-id="7ccc8-206">Entry</span></span> | <span data-ttu-id="7ccc8-207">值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccc8-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ccc8-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccc8-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccc8-210">System-Only</span></span>            | <span data-ttu-id="7ccc8-211">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-211">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccc8-213">對</span><span class="sxs-lookup"><span data-stu-id="7ccc8-213">True</span></span>                                                                                                      |
| <span data-ttu-id="7ccc8-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ccc8-214">Is Indexed</span></span>             | <span data-ttu-id="7ccc8-215">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-215">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ccc8-216">In Global Catalog</span></span>      | <span data-ttu-id="7ccc8-217">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-217">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ccc8-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccc8-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ccc8-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="7ccc8-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccc8-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccc8-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-222">Search-Flags</span></span>           | <span data-ttu-id="7ccc8-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccc8-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-224">System-Flags</span></span>           | <span data-ttu-id="7ccc8-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccc8-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ccc8-226">Classes used in</span></span>        | [<span data-ttu-id="7ccc8-227">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="7ccc8-228">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ccc8-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ccc8-229">Windows Server 2008</span></span>



| <span data-ttu-id="7ccc8-230">進入</span><span class="sxs-lookup"><span data-stu-id="7ccc8-230">Entry</span></span> | <span data-ttu-id="7ccc8-231">值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccc8-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ccc8-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccc8-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccc8-234">System-Only</span></span>            | <span data-ttu-id="7ccc8-235">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-235">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-236">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccc8-237">對</span><span class="sxs-lookup"><span data-stu-id="7ccc8-237">True</span></span>                                                                                                      |
| <span data-ttu-id="7ccc8-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ccc8-238">Is Indexed</span></span>             | <span data-ttu-id="7ccc8-239">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-239">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ccc8-240">In Global Catalog</span></span>      | <span data-ttu-id="7ccc8-241">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-241">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ccc8-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccc8-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ccc8-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="7ccc8-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccc8-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccc8-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-246">Search-Flags</span></span>           | <span data-ttu-id="7ccc8-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccc8-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-248">System-Flags</span></span>           | <span data-ttu-id="7ccc8-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccc8-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ccc8-250">Classes used in</span></span>        | [<span data-ttu-id="7ccc8-251">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="7ccc8-252">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ccc8-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ccc8-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ccc8-254">進入</span><span class="sxs-lookup"><span data-stu-id="7ccc8-254">Entry</span></span> | <span data-ttu-id="7ccc8-255">值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccc8-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ccc8-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccc8-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccc8-258">System-Only</span></span>            | <span data-ttu-id="7ccc8-259">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-259">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-260">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccc8-261">對</span><span class="sxs-lookup"><span data-stu-id="7ccc8-261">True</span></span>                                                                                                      |
| <span data-ttu-id="7ccc8-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ccc8-262">Is Indexed</span></span>             | <span data-ttu-id="7ccc8-263">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-263">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ccc8-264">In Global Catalog</span></span>      | <span data-ttu-id="7ccc8-265">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-265">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ccc8-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccc8-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ccc8-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="7ccc8-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccc8-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccc8-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-270">Search-Flags</span></span>           | <span data-ttu-id="7ccc8-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccc8-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-272">System-Flags</span></span>           | <span data-ttu-id="7ccc8-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccc8-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ccc8-274">Classes used in</span></span>        | [<span data-ttu-id="7ccc8-275">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="7ccc8-276">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ccc8-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ccc8-277">Windows Server 2012</span></span>



| <span data-ttu-id="7ccc8-278">進入</span><span class="sxs-lookup"><span data-stu-id="7ccc8-278">Entry</span></span> | <span data-ttu-id="7ccc8-279">值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccc8-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ccc8-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ccc8-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="7ccc8-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ccc8-282">System-Only</span></span>            | <span data-ttu-id="7ccc8-283">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-283">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ccc8-284">Is-Single-Valued</span></span>       | <span data-ttu-id="7ccc8-285">對</span><span class="sxs-lookup"><span data-stu-id="7ccc8-285">True</span></span>                                                                                                      |
| <span data-ttu-id="7ccc8-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ccc8-286">Is Indexed</span></span>             | <span data-ttu-id="7ccc8-287">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-287">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ccc8-288">In Global Catalog</span></span>      | <span data-ttu-id="7ccc8-289">否</span><span class="sxs-lookup"><span data-stu-id="7ccc8-289">False</span></span>                                                                                                     |
| <span data-ttu-id="7ccc8-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ccc8-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ccc8-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ccc8-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="7ccc8-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ccc8-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ccc8-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="7ccc8-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-294">Search-Flags</span></span>           | <span data-ttu-id="7ccc8-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ccc8-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ccc8-296">System-Flags</span></span>           | <span data-ttu-id="7ccc8-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ccc8-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="7ccc8-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ccc8-298">Classes used in</span></span>        | [<span data-ttu-id="7ccc8-299">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="7ccc8-300">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="7ccc8-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 






---
title: 預設值-安全描述項屬性
description: 第一次建立物件時，要指派給該物件的安全描述項。
ms.assetid: 22575883-2ef3-492b-9868-1eb350c4f547
ms.tgt_platform: multiple
keywords:
- 預設-安全性-描述元屬性 AD 架構
- defaultSecurityDescriptor 屬性 AD 架構
topic_type:
- apiref
api_name:
- Default-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0b4a8dbe0c633a15b6a5167cb1171a14d1769
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467194"
---
# <a name="default-security-descriptor-attribute"></a><span data-ttu-id="cb398-105">預設值-安全描述項屬性</span><span class="sxs-lookup"><span data-stu-id="cb398-105">Default-Security-Descriptor attribute</span></span>

<span data-ttu-id="cb398-106">第一次建立物件時，要指派給該物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="cb398-106">The security descriptor to be assigned to the object when it is first created.</span></span>



| <span data-ttu-id="cb398-107">進入</span><span class="sxs-lookup"><span data-stu-id="cb398-107">Entry</span></span> | <span data-ttu-id="cb398-108">值</span><span class="sxs-lookup"><span data-stu-id="cb398-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cb398-109">CN</span><span class="sxs-lookup"><span data-stu-id="cb398-109">CN</span></span>                | <span data-ttu-id="cb398-110">預設-安全性-描述元</span><span class="sxs-lookup"><span data-stu-id="cb398-110">Default-Security-Descriptor</span></span>                 |
| <span data-ttu-id="cb398-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="cb398-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cb398-112">defaultSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="cb398-112">defaultSecurityDescriptor</span></span>                   |
| <span data-ttu-id="cb398-113">大小</span><span class="sxs-lookup"><span data-stu-id="cb398-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="cb398-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="cb398-114">Update Privilege</span></span>  | <span data-ttu-id="cb398-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="cb398-115">Schema administrator</span></span>                        |
| <span data-ttu-id="cb398-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="cb398-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="cb398-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cb398-117">Attribute-Id</span></span>      | <span data-ttu-id="cb398-118">1.2.840.113556.1.4.224</span><span class="sxs-lookup"><span data-stu-id="cb398-118">1.2.840.113556.1.4.224</span></span>                      |
| <span data-ttu-id="cb398-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="cb398-119">System-Id-Guid</span></span>    | <span data-ttu-id="cb398-120">807a6d30-1669-11d0-a064-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="cb398-120">807a6d30-1669-11d0-a064-00aa006c33ed</span></span>        |
| <span data-ttu-id="cb398-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb398-121">Syntax</span></span>            | [<span data-ttu-id="cb398-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cb398-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cb398-123">實作</span><span class="sxs-lookup"><span data-stu-id="cb398-123">Implementations</span></span>

-   [<span data-ttu-id="cb398-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cb398-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cb398-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cb398-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cb398-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="cb398-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cb398-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cb398-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cb398-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cb398-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cb398-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cb398-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cb398-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cb398-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cb398-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cb398-131">Windows 2000 Server</span></span>



| <span data-ttu-id="cb398-132">進入</span><span class="sxs-lookup"><span data-stu-id="cb398-132">Entry</span></span> | <span data-ttu-id="cb398-133">值</span><span class="sxs-lookup"><span data-stu-id="cb398-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb398-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cb398-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb398-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb398-136">System-Only</span></span>            | <span data-ttu-id="cb398-137">否</span><span class="sxs-lookup"><span data-stu-id="cb398-137">False</span></span>                                            |
| <span data-ttu-id="cb398-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cb398-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cb398-139">對</span><span class="sxs-lookup"><span data-stu-id="cb398-139">True</span></span>                                             |
| <span data-ttu-id="cb398-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cb398-140">Is Indexed</span></span>             | <span data-ttu-id="cb398-141">否</span><span class="sxs-lookup"><span data-stu-id="cb398-141">False</span></span>                                            |
| <span data-ttu-id="cb398-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cb398-142">In Global Catalog</span></span>      | <span data-ttu-id="cb398-143">否</span><span class="sxs-lookup"><span data-stu-id="cb398-143">False</span></span>                                            |
| <span data-ttu-id="cb398-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cb398-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb398-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cb398-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb398-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb398-146">Range-Lower</span></span>            | <span data-ttu-id="cb398-147">0</span><span class="sxs-lookup"><span data-stu-id="cb398-147">0</span></span>                                                |
| <span data-ttu-id="cb398-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb398-148">Range-Upper</span></span>            | <span data-ttu-id="cb398-149">32767</span><span class="sxs-lookup"><span data-stu-id="cb398-149">32767</span></span>                                            |
| <span data-ttu-id="cb398-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-150">Search-Flags</span></span>           | <span data-ttu-id="cb398-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb398-151">0x00000000</span></span>                                       |
| <span data-ttu-id="cb398-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-152">System-Flags</span></span>           | <span data-ttu-id="cb398-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb398-153">0x00000010</span></span>                                       |
| <span data-ttu-id="cb398-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cb398-154">Classes used in</span></span>        | [<span data-ttu-id="cb398-155">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="cb398-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cb398-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb398-156">Windows Server 2003</span></span>



| <span data-ttu-id="cb398-157">進入</span><span class="sxs-lookup"><span data-stu-id="cb398-157">Entry</span></span> | <span data-ttu-id="cb398-158">值</span><span class="sxs-lookup"><span data-stu-id="cb398-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb398-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cb398-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb398-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb398-161">System-Only</span></span>            | <span data-ttu-id="cb398-162">否</span><span class="sxs-lookup"><span data-stu-id="cb398-162">False</span></span>                                            |
| <span data-ttu-id="cb398-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cb398-163">Is-Single-Valued</span></span>       | <span data-ttu-id="cb398-164">對</span><span class="sxs-lookup"><span data-stu-id="cb398-164">True</span></span>                                             |
| <span data-ttu-id="cb398-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cb398-165">Is Indexed</span></span>             | <span data-ttu-id="cb398-166">否</span><span class="sxs-lookup"><span data-stu-id="cb398-166">False</span></span>                                            |
| <span data-ttu-id="cb398-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cb398-167">In Global Catalog</span></span>      | <span data-ttu-id="cb398-168">否</span><span class="sxs-lookup"><span data-stu-id="cb398-168">False</span></span>                                            |
| <span data-ttu-id="cb398-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cb398-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb398-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cb398-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb398-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb398-171">Range-Lower</span></span>            | <span data-ttu-id="cb398-172">0</span><span class="sxs-lookup"><span data-stu-id="cb398-172">0</span></span>                                                |
| <span data-ttu-id="cb398-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb398-173">Range-Upper</span></span>            | <span data-ttu-id="cb398-174">32767</span><span class="sxs-lookup"><span data-stu-id="cb398-174">32767</span></span>                                            |
| <span data-ttu-id="cb398-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-175">Search-Flags</span></span>           | <span data-ttu-id="cb398-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb398-176">0x00000000</span></span>                                       |
| <span data-ttu-id="cb398-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-177">System-Flags</span></span>           | <span data-ttu-id="cb398-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb398-178">0x00000010</span></span>                                       |
| <span data-ttu-id="cb398-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cb398-179">Classes used in</span></span>        | [<span data-ttu-id="cb398-180">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="cb398-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cb398-181">亞當</span><span class="sxs-lookup"><span data-stu-id="cb398-181">ADAM</span></span>



| <span data-ttu-id="cb398-182">進入</span><span class="sxs-lookup"><span data-stu-id="cb398-182">Entry</span></span> | <span data-ttu-id="cb398-183">值</span><span class="sxs-lookup"><span data-stu-id="cb398-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb398-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cb398-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb398-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb398-186">System-Only</span></span>            | <span data-ttu-id="cb398-187">否</span><span class="sxs-lookup"><span data-stu-id="cb398-187">False</span></span>                                            |
| <span data-ttu-id="cb398-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cb398-188">Is-Single-Valued</span></span>       | <span data-ttu-id="cb398-189">對</span><span class="sxs-lookup"><span data-stu-id="cb398-189">True</span></span>                                             |
| <span data-ttu-id="cb398-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cb398-190">Is Indexed</span></span>             | <span data-ttu-id="cb398-191">否</span><span class="sxs-lookup"><span data-stu-id="cb398-191">False</span></span>                                            |
| <span data-ttu-id="cb398-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cb398-192">In Global Catalog</span></span>      | <span data-ttu-id="cb398-193">否</span><span class="sxs-lookup"><span data-stu-id="cb398-193">False</span></span>                                            |
| <span data-ttu-id="cb398-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cb398-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb398-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cb398-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb398-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb398-196">Range-Lower</span></span>            | <span data-ttu-id="cb398-197">0</span><span class="sxs-lookup"><span data-stu-id="cb398-197">0</span></span>                                                |
| <span data-ttu-id="cb398-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb398-198">Range-Upper</span></span>            | <span data-ttu-id="cb398-199">32767</span><span class="sxs-lookup"><span data-stu-id="cb398-199">32767</span></span>                                            |
| <span data-ttu-id="cb398-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-200">Search-Flags</span></span>           | <span data-ttu-id="cb398-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb398-201">0x00000000</span></span>                                       |
| <span data-ttu-id="cb398-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-202">System-Flags</span></span>           | <span data-ttu-id="cb398-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb398-203">0x00000010</span></span>                                       |
| <span data-ttu-id="cb398-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cb398-204">Classes used in</span></span>        | [<span data-ttu-id="cb398-205">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="cb398-205">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cb398-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cb398-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cb398-207">進入</span><span class="sxs-lookup"><span data-stu-id="cb398-207">Entry</span></span> | <span data-ttu-id="cb398-208">值</span><span class="sxs-lookup"><span data-stu-id="cb398-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb398-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cb398-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb398-210">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb398-211">System-Only</span></span>            | <span data-ttu-id="cb398-212">否</span><span class="sxs-lookup"><span data-stu-id="cb398-212">False</span></span>                                            |
| <span data-ttu-id="cb398-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cb398-213">Is-Single-Valued</span></span>       | <span data-ttu-id="cb398-214">對</span><span class="sxs-lookup"><span data-stu-id="cb398-214">True</span></span>                                             |
| <span data-ttu-id="cb398-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cb398-215">Is Indexed</span></span>             | <span data-ttu-id="cb398-216">否</span><span class="sxs-lookup"><span data-stu-id="cb398-216">False</span></span>                                            |
| <span data-ttu-id="cb398-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cb398-217">In Global Catalog</span></span>      | <span data-ttu-id="cb398-218">否</span><span class="sxs-lookup"><span data-stu-id="cb398-218">False</span></span>                                            |
| <span data-ttu-id="cb398-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cb398-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb398-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cb398-220">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb398-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb398-221">Range-Lower</span></span>            | <span data-ttu-id="cb398-222">0</span><span class="sxs-lookup"><span data-stu-id="cb398-222">0</span></span>                                                |
| <span data-ttu-id="cb398-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb398-223">Range-Upper</span></span>            | <span data-ttu-id="cb398-224">32767</span><span class="sxs-lookup"><span data-stu-id="cb398-224">32767</span></span>                                            |
| <span data-ttu-id="cb398-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-225">Search-Flags</span></span>           | <span data-ttu-id="cb398-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb398-226">0x00000000</span></span>                                       |
| <span data-ttu-id="cb398-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-227">System-Flags</span></span>           | <span data-ttu-id="cb398-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb398-228">0x00000010</span></span>                                       |
| <span data-ttu-id="cb398-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cb398-229">Classes used in</span></span>        | [<span data-ttu-id="cb398-230">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="cb398-230">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cb398-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb398-231">Windows Server 2008</span></span>



| <span data-ttu-id="cb398-232">進入</span><span class="sxs-lookup"><span data-stu-id="cb398-232">Entry</span></span> | <span data-ttu-id="cb398-233">值</span><span class="sxs-lookup"><span data-stu-id="cb398-233">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb398-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cb398-234">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb398-235">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb398-236">System-Only</span></span>            | <span data-ttu-id="cb398-237">否</span><span class="sxs-lookup"><span data-stu-id="cb398-237">False</span></span>                                            |
| <span data-ttu-id="cb398-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cb398-238">Is-Single-Valued</span></span>       | <span data-ttu-id="cb398-239">對</span><span class="sxs-lookup"><span data-stu-id="cb398-239">True</span></span>                                             |
| <span data-ttu-id="cb398-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cb398-240">Is Indexed</span></span>             | <span data-ttu-id="cb398-241">否</span><span class="sxs-lookup"><span data-stu-id="cb398-241">False</span></span>                                            |
| <span data-ttu-id="cb398-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cb398-242">In Global Catalog</span></span>      | <span data-ttu-id="cb398-243">否</span><span class="sxs-lookup"><span data-stu-id="cb398-243">False</span></span>                                            |
| <span data-ttu-id="cb398-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cb398-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb398-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cb398-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb398-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb398-246">Range-Lower</span></span>            | <span data-ttu-id="cb398-247">0</span><span class="sxs-lookup"><span data-stu-id="cb398-247">0</span></span>                                                |
| <span data-ttu-id="cb398-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb398-248">Range-Upper</span></span>            | <span data-ttu-id="cb398-249">32767</span><span class="sxs-lookup"><span data-stu-id="cb398-249">32767</span></span>                                            |
| <span data-ttu-id="cb398-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-250">Search-Flags</span></span>           | <span data-ttu-id="cb398-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb398-251">0x00000000</span></span>                                       |
| <span data-ttu-id="cb398-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-252">System-Flags</span></span>           | <span data-ttu-id="cb398-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb398-253">0x00000010</span></span>                                       |
| <span data-ttu-id="cb398-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cb398-254">Classes used in</span></span>        | [<span data-ttu-id="cb398-255">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="cb398-255">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cb398-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cb398-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cb398-257">進入</span><span class="sxs-lookup"><span data-stu-id="cb398-257">Entry</span></span> | <span data-ttu-id="cb398-258">值</span><span class="sxs-lookup"><span data-stu-id="cb398-258">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb398-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cb398-259">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb398-260">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb398-261">System-Only</span></span>            | <span data-ttu-id="cb398-262">否</span><span class="sxs-lookup"><span data-stu-id="cb398-262">False</span></span>                                            |
| <span data-ttu-id="cb398-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cb398-263">Is-Single-Valued</span></span>       | <span data-ttu-id="cb398-264">對</span><span class="sxs-lookup"><span data-stu-id="cb398-264">True</span></span>                                             |
| <span data-ttu-id="cb398-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cb398-265">Is Indexed</span></span>             | <span data-ttu-id="cb398-266">否</span><span class="sxs-lookup"><span data-stu-id="cb398-266">False</span></span>                                            |
| <span data-ttu-id="cb398-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cb398-267">In Global Catalog</span></span>      | <span data-ttu-id="cb398-268">否</span><span class="sxs-lookup"><span data-stu-id="cb398-268">False</span></span>                                            |
| <span data-ttu-id="cb398-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cb398-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb398-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cb398-270">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb398-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb398-271">Range-Lower</span></span>            | <span data-ttu-id="cb398-272">0</span><span class="sxs-lookup"><span data-stu-id="cb398-272">0</span></span>                                                |
| <span data-ttu-id="cb398-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb398-273">Range-Upper</span></span>            | <span data-ttu-id="cb398-274">32767</span><span class="sxs-lookup"><span data-stu-id="cb398-274">32767</span></span>                                            |
| <span data-ttu-id="cb398-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-275">Search-Flags</span></span>           | <span data-ttu-id="cb398-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb398-276">0x00000000</span></span>                                       |
| <span data-ttu-id="cb398-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-277">System-Flags</span></span>           | <span data-ttu-id="cb398-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb398-278">0x00000010</span></span>                                       |
| <span data-ttu-id="cb398-279">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cb398-279">Classes used in</span></span>        | [<span data-ttu-id="cb398-280">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="cb398-280">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cb398-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb398-281">Windows Server 2012</span></span>



| <span data-ttu-id="cb398-282">進入</span><span class="sxs-lookup"><span data-stu-id="cb398-282">Entry</span></span> | <span data-ttu-id="cb398-283">值</span><span class="sxs-lookup"><span data-stu-id="cb398-283">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb398-284">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cb398-284">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb398-285">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb398-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb398-286">System-Only</span></span>            | <span data-ttu-id="cb398-287">否</span><span class="sxs-lookup"><span data-stu-id="cb398-287">False</span></span>                                            |
| <span data-ttu-id="cb398-288">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cb398-288">Is-Single-Valued</span></span>       | <span data-ttu-id="cb398-289">對</span><span class="sxs-lookup"><span data-stu-id="cb398-289">True</span></span>                                             |
| <span data-ttu-id="cb398-290">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cb398-290">Is Indexed</span></span>             | <span data-ttu-id="cb398-291">否</span><span class="sxs-lookup"><span data-stu-id="cb398-291">False</span></span>                                            |
| <span data-ttu-id="cb398-292">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cb398-292">In Global Catalog</span></span>      | <span data-ttu-id="cb398-293">否</span><span class="sxs-lookup"><span data-stu-id="cb398-293">False</span></span>                                            |
| <span data-ttu-id="cb398-294">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cb398-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb398-295">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cb398-295">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb398-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb398-296">Range-Lower</span></span>            | <span data-ttu-id="cb398-297">0</span><span class="sxs-lookup"><span data-stu-id="cb398-297">0</span></span>                                                |
| <span data-ttu-id="cb398-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb398-298">Range-Upper</span></span>            | <span data-ttu-id="cb398-299">32767</span><span class="sxs-lookup"><span data-stu-id="cb398-299">32767</span></span>                                            |
| <span data-ttu-id="cb398-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-300">Search-Flags</span></span>           | <span data-ttu-id="cb398-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb398-301">0x00000000</span></span>                                       |
| <span data-ttu-id="cb398-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb398-302">System-Flags</span></span>           | <span data-ttu-id="cb398-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb398-303">0x00000010</span></span>                                       |
| <span data-ttu-id="cb398-304">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cb398-304">Classes used in</span></span>        | [<span data-ttu-id="cb398-305">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="cb398-305">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 






---
title: Default-Group 屬性
description: 此物件建立時所指派的群組。
ms.assetid: 47fc8548-377b-4299-9c12-8f41e350eec9
ms.tgt_platform: multiple
keywords:
- Default-Group 屬性 AD 架構
- defaultGroup 屬性 AD 架構
topic_type:
- apiref
api_name:
- Default-Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dfd6a9d54fb4d16212d5b05fe73f392aa1ddf25
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935270"
---
# <a name="default-group-attribute"></a><span data-ttu-id="7e79d-105">Default-Group 屬性</span><span class="sxs-lookup"><span data-stu-id="7e79d-105">Default-Group attribute</span></span>

<span data-ttu-id="7e79d-106">此物件建立時所指派的群組。</span><span class="sxs-lookup"><span data-stu-id="7e79d-106">The group to which this object is assigned when it is created.</span></span>



| <span data-ttu-id="7e79d-107">進入</span><span class="sxs-lookup"><span data-stu-id="7e79d-107">Entry</span></span> | <span data-ttu-id="7e79d-108">值</span><span class="sxs-lookup"><span data-stu-id="7e79d-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7e79d-109">CN</span><span class="sxs-lookup"><span data-stu-id="7e79d-109">CN</span></span>                | <span data-ttu-id="7e79d-110">Default-Group</span><span class="sxs-lookup"><span data-stu-id="7e79d-110">Default-Group</span></span>                           |
| <span data-ttu-id="7e79d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7e79d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7e79d-112">defaultGroup</span><span class="sxs-lookup"><span data-stu-id="7e79d-112">defaultGroup</span></span>                            |
| <span data-ttu-id="7e79d-113">大小</span><span class="sxs-lookup"><span data-stu-id="7e79d-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7e79d-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7e79d-114">Update Privilege</span></span>  | <span data-ttu-id="7e79d-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7e79d-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="7e79d-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7e79d-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7e79d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e79d-117">Attribute-Id</span></span>      | <span data-ttu-id="7e79d-118">1.2.840.113556.1.4.480</span><span class="sxs-lookup"><span data-stu-id="7e79d-118">1.2.840.113556.1.4.480</span></span>                  |
| <span data-ttu-id="7e79d-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7e79d-119">System-Id-Guid</span></span>    | <span data-ttu-id="7e79d-120">720bc4e2-a54a-11d0-afdf-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="7e79d-120">720bc4e2-a54a-11d0-afdf-00c04fd930c9</span></span>    |
| <span data-ttu-id="7e79d-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e79d-121">Syntax</span></span>            | [<span data-ttu-id="7e79d-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7e79d-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7e79d-123">實作</span><span class="sxs-lookup"><span data-stu-id="7e79d-123">Implementations</span></span>

-   [<span data-ttu-id="7e79d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7e79d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7e79d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e79d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e79d-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7e79d-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7e79d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e79d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e79d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e79d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e79d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e79d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e79d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e79d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7e79d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e79d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7e79d-132">進入</span><span class="sxs-lookup"><span data-stu-id="7e79d-132">Entry</span></span> | <span data-ttu-id="7e79d-133">值</span><span class="sxs-lookup"><span data-stu-id="7e79d-133">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e79d-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e79d-134">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e79d-135">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e79d-136">System-Only</span></span>            | <span data-ttu-id="7e79d-137">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-137">False</span></span>                                                          |
| <span data-ttu-id="7e79d-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e79d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7e79d-139">對</span><span class="sxs-lookup"><span data-stu-id="7e79d-139">True</span></span>                                                           |
| <span data-ttu-id="7e79d-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e79d-140">Is Indexed</span></span>             | <span data-ttu-id="7e79d-141">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-141">False</span></span>                                                          |
| <span data-ttu-id="7e79d-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e79d-142">In Global Catalog</span></span>      | <span data-ttu-id="7e79d-143">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-143">False</span></span>                                                          |
| <span data-ttu-id="7e79d-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e79d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e79d-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e79d-145">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e79d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e79d-146">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e79d-147">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-148">Search-Flags</span></span>           | <span data-ttu-id="7e79d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e79d-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e79d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-150">System-Flags</span></span>           | <span data-ttu-id="7e79d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e79d-151">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e79d-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e79d-152">Classes used in</span></span>        | [<span data-ttu-id="7e79d-153">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="7e79d-153">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7e79d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e79d-154">Windows Server 2003</span></span>



| <span data-ttu-id="7e79d-155">進入</span><span class="sxs-lookup"><span data-stu-id="7e79d-155">Entry</span></span> | <span data-ttu-id="7e79d-156">值</span><span class="sxs-lookup"><span data-stu-id="7e79d-156">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e79d-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e79d-157">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e79d-158">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e79d-159">System-Only</span></span>            | <span data-ttu-id="7e79d-160">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-160">False</span></span>                                                          |
| <span data-ttu-id="7e79d-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e79d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7e79d-162">對</span><span class="sxs-lookup"><span data-stu-id="7e79d-162">True</span></span>                                                           |
| <span data-ttu-id="7e79d-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e79d-163">Is Indexed</span></span>             | <span data-ttu-id="7e79d-164">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-164">False</span></span>                                                          |
| <span data-ttu-id="7e79d-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e79d-165">In Global Catalog</span></span>      | <span data-ttu-id="7e79d-166">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-166">False</span></span>                                                          |
| <span data-ttu-id="7e79d-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e79d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e79d-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e79d-168">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e79d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e79d-169">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e79d-170">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-171">Search-Flags</span></span>           | <span data-ttu-id="7e79d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e79d-172">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e79d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-173">System-Flags</span></span>           | <span data-ttu-id="7e79d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e79d-174">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e79d-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e79d-175">Classes used in</span></span>        | [<span data-ttu-id="7e79d-176">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="7e79d-176">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7e79d-177">亞當</span><span class="sxs-lookup"><span data-stu-id="7e79d-177">ADAM</span></span>



| <span data-ttu-id="7e79d-178">進入</span><span class="sxs-lookup"><span data-stu-id="7e79d-178">Entry</span></span> | <span data-ttu-id="7e79d-179">值</span><span class="sxs-lookup"><span data-stu-id="7e79d-179">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e79d-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e79d-180">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e79d-181">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e79d-182">System-Only</span></span>            | <span data-ttu-id="7e79d-183">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-183">False</span></span>                                                          |
| <span data-ttu-id="7e79d-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e79d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7e79d-185">對</span><span class="sxs-lookup"><span data-stu-id="7e79d-185">True</span></span>                                                           |
| <span data-ttu-id="7e79d-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e79d-186">Is Indexed</span></span>             | <span data-ttu-id="7e79d-187">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-187">False</span></span>                                                          |
| <span data-ttu-id="7e79d-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e79d-188">In Global Catalog</span></span>      | <span data-ttu-id="7e79d-189">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-189">False</span></span>                                                          |
| <span data-ttu-id="7e79d-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e79d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e79d-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e79d-191">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e79d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e79d-192">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e79d-193">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-194">Search-Flags</span></span>           | <span data-ttu-id="7e79d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e79d-195">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e79d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-196">System-Flags</span></span>           | <span data-ttu-id="7e79d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e79d-197">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e79d-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e79d-198">Classes used in</span></span>        | [<span data-ttu-id="7e79d-199">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="7e79d-199">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e79d-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e79d-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e79d-201">進入</span><span class="sxs-lookup"><span data-stu-id="7e79d-201">Entry</span></span> | <span data-ttu-id="7e79d-202">值</span><span class="sxs-lookup"><span data-stu-id="7e79d-202">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e79d-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e79d-203">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e79d-204">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e79d-205">System-Only</span></span>            | <span data-ttu-id="7e79d-206">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-206">False</span></span>                                                          |
| <span data-ttu-id="7e79d-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e79d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7e79d-208">對</span><span class="sxs-lookup"><span data-stu-id="7e79d-208">True</span></span>                                                           |
| <span data-ttu-id="7e79d-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e79d-209">Is Indexed</span></span>             | <span data-ttu-id="7e79d-210">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-210">False</span></span>                                                          |
| <span data-ttu-id="7e79d-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e79d-211">In Global Catalog</span></span>      | <span data-ttu-id="7e79d-212">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-212">False</span></span>                                                          |
| <span data-ttu-id="7e79d-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e79d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e79d-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e79d-214">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e79d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e79d-215">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e79d-216">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-217">Search-Flags</span></span>           | <span data-ttu-id="7e79d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e79d-218">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e79d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-219">System-Flags</span></span>           | <span data-ttu-id="7e79d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e79d-220">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e79d-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e79d-221">Classes used in</span></span>        | [<span data-ttu-id="7e79d-222">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="7e79d-222">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e79d-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e79d-223">Windows Server 2008</span></span>



| <span data-ttu-id="7e79d-224">進入</span><span class="sxs-lookup"><span data-stu-id="7e79d-224">Entry</span></span> | <span data-ttu-id="7e79d-225">值</span><span class="sxs-lookup"><span data-stu-id="7e79d-225">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e79d-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e79d-226">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e79d-227">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e79d-228">System-Only</span></span>            | <span data-ttu-id="7e79d-229">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-229">False</span></span>                                                          |
| <span data-ttu-id="7e79d-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e79d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7e79d-231">對</span><span class="sxs-lookup"><span data-stu-id="7e79d-231">True</span></span>                                                           |
| <span data-ttu-id="7e79d-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e79d-232">Is Indexed</span></span>             | <span data-ttu-id="7e79d-233">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-233">False</span></span>                                                          |
| <span data-ttu-id="7e79d-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e79d-234">In Global Catalog</span></span>      | <span data-ttu-id="7e79d-235">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-235">False</span></span>                                                          |
| <span data-ttu-id="7e79d-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e79d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e79d-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e79d-237">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e79d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e79d-238">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e79d-239">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-240">Search-Flags</span></span>           | <span data-ttu-id="7e79d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e79d-241">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e79d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-242">System-Flags</span></span>           | <span data-ttu-id="7e79d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e79d-243">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e79d-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e79d-244">Classes used in</span></span>        | [<span data-ttu-id="7e79d-245">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="7e79d-245">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e79d-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e79d-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e79d-247">進入</span><span class="sxs-lookup"><span data-stu-id="7e79d-247">Entry</span></span> | <span data-ttu-id="7e79d-248">值</span><span class="sxs-lookup"><span data-stu-id="7e79d-248">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e79d-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e79d-249">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e79d-250">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e79d-251">System-Only</span></span>            | <span data-ttu-id="7e79d-252">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-252">False</span></span>                                                          |
| <span data-ttu-id="7e79d-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e79d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7e79d-254">對</span><span class="sxs-lookup"><span data-stu-id="7e79d-254">True</span></span>                                                           |
| <span data-ttu-id="7e79d-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e79d-255">Is Indexed</span></span>             | <span data-ttu-id="7e79d-256">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-256">False</span></span>                                                          |
| <span data-ttu-id="7e79d-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e79d-257">In Global Catalog</span></span>      | <span data-ttu-id="7e79d-258">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-258">False</span></span>                                                          |
| <span data-ttu-id="7e79d-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e79d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e79d-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e79d-260">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e79d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e79d-261">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e79d-262">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-263">Search-Flags</span></span>           | <span data-ttu-id="7e79d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e79d-264">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e79d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-265">System-Flags</span></span>           | <span data-ttu-id="7e79d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e79d-266">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e79d-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e79d-267">Classes used in</span></span>        | [<span data-ttu-id="7e79d-268">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="7e79d-268">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e79d-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e79d-269">Windows Server 2012</span></span>



| <span data-ttu-id="7e79d-270">進入</span><span class="sxs-lookup"><span data-stu-id="7e79d-270">Entry</span></span> | <span data-ttu-id="7e79d-271">值</span><span class="sxs-lookup"><span data-stu-id="7e79d-271">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e79d-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e79d-272">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e79d-273">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e79d-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e79d-274">System-Only</span></span>            | <span data-ttu-id="7e79d-275">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-275">False</span></span>                                                          |
| <span data-ttu-id="7e79d-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e79d-276">Is-Single-Valued</span></span>       | <span data-ttu-id="7e79d-277">對</span><span class="sxs-lookup"><span data-stu-id="7e79d-277">True</span></span>                                                           |
| <span data-ttu-id="7e79d-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e79d-278">Is Indexed</span></span>             | <span data-ttu-id="7e79d-279">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-279">False</span></span>                                                          |
| <span data-ttu-id="7e79d-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e79d-280">In Global Catalog</span></span>      | <span data-ttu-id="7e79d-281">否</span><span class="sxs-lookup"><span data-stu-id="7e79d-281">False</span></span>                                                          |
| <span data-ttu-id="7e79d-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e79d-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e79d-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e79d-283">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e79d-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e79d-284">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e79d-285">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e79d-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-286">Search-Flags</span></span>           | <span data-ttu-id="7e79d-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e79d-287">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e79d-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e79d-288">System-Flags</span></span>           | <span data-ttu-id="7e79d-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e79d-289">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e79d-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e79d-290">Classes used in</span></span>        | [<span data-ttu-id="7e79d-291">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="7e79d-291">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 






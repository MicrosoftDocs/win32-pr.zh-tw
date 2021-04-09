---
title: netboot-新增-電腦-OU 屬性
description: 指出將建立新用戶端電腦帳戶的位置。
ms.assetid: 0e1a9145-65cc-499f-a264-c56f9028341b
ms.tgt_platform: multiple
keywords:
- netboot-新增-電腦-OU 屬性 AD 架構
- netbootNewMachineOU 屬性 AD 架構
topic_type:
- apiref
api_name:
- netboot-New-Machine-OU
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a3f4a8169d91dc206f6b57cba96374903077b7f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844995"
---
# <a name="netboot-new-machine-ou-attribute"></a><span data-ttu-id="06078-105">netboot-新增-電腦-OU 屬性</span><span class="sxs-lookup"><span data-stu-id="06078-105">netboot-New-Machine-OU attribute</span></span>

<span data-ttu-id="06078-106">指出將建立新用戶端電腦帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="06078-106">Indicates where the new client computer account will be created.</span></span>



| <span data-ttu-id="06078-107">進入</span><span class="sxs-lookup"><span data-stu-id="06078-107">Entry</span></span> | <span data-ttu-id="06078-108">值</span><span class="sxs-lookup"><span data-stu-id="06078-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="06078-109">CN</span><span class="sxs-lookup"><span data-stu-id="06078-109">CN</span></span>                | <span data-ttu-id="06078-110">netboot-新增-電腦-OU</span><span class="sxs-lookup"><span data-stu-id="06078-110">netboot-New-Machine-OU</span></span>                  |
| <span data-ttu-id="06078-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="06078-111">Ldap-Display-Name</span></span> | <span data-ttu-id="06078-112">netbootNewMachineOU</span><span class="sxs-lookup"><span data-stu-id="06078-112">netbootNewMachineOU</span></span>                     |
| <span data-ttu-id="06078-113">大小</span><span class="sxs-lookup"><span data-stu-id="06078-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="06078-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="06078-114">Update Privilege</span></span>  | <span data-ttu-id="06078-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="06078-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="06078-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="06078-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="06078-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="06078-117">Attribute-Id</span></span>      | <span data-ttu-id="06078-118">1.2.840.113556.1.4.856</span><span class="sxs-lookup"><span data-stu-id="06078-118">1.2.840.113556.1.4.856</span></span>                  |
| <span data-ttu-id="06078-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="06078-119">System-Id-Guid</span></span>    | <span data-ttu-id="06078-120">0738307d-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="06078-120">0738307d-91df-11d1-aebc-0000f80367c1</span></span>    |
| <span data-ttu-id="06078-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="06078-121">Syntax</span></span>            | [<span data-ttu-id="06078-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="06078-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="06078-123">實作</span><span class="sxs-lookup"><span data-stu-id="06078-123">Implementations</span></span>

-   [<span data-ttu-id="06078-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="06078-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="06078-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="06078-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="06078-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="06078-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="06078-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="06078-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="06078-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="06078-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="06078-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="06078-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="06078-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="06078-130">Windows 2000 Server</span></span>



| <span data-ttu-id="06078-131">進入</span><span class="sxs-lookup"><span data-stu-id="06078-131">Entry</span></span> | <span data-ttu-id="06078-132">值</span><span class="sxs-lookup"><span data-stu-id="06078-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="06078-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06078-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-135">System-Only</span></span>            | <span data-ttu-id="06078-136">否</span><span class="sxs-lookup"><span data-stu-id="06078-136">False</span></span>                                                      |
| <span data-ttu-id="06078-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06078-137">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-138">對</span><span class="sxs-lookup"><span data-stu-id="06078-138">True</span></span>                                                       |
| <span data-ttu-id="06078-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06078-139">Is Indexed</span></span>             | <span data-ttu-id="06078-140">否</span><span class="sxs-lookup"><span data-stu-id="06078-140">False</span></span>                                                      |
| <span data-ttu-id="06078-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06078-141">In Global Catalog</span></span>      | <span data-ttu-id="06078-142">否</span><span class="sxs-lookup"><span data-stu-id="06078-142">False</span></span>                                                      |
| <span data-ttu-id="06078-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06078-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06078-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="06078-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="06078-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="06078-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-147">Search-Flags</span></span>           | <span data-ttu-id="06078-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="06078-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-149">System-Flags</span></span>           | <span data-ttu-id="06078-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="06078-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06078-151">Classes used in</span></span>        | [<span data-ttu-id="06078-152">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="06078-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="06078-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06078-153">Windows Server 2003</span></span>



| <span data-ttu-id="06078-154">進入</span><span class="sxs-lookup"><span data-stu-id="06078-154">Entry</span></span> | <span data-ttu-id="06078-155">值</span><span class="sxs-lookup"><span data-stu-id="06078-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="06078-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06078-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-158">System-Only</span></span>            | <span data-ttu-id="06078-159">否</span><span class="sxs-lookup"><span data-stu-id="06078-159">False</span></span>                                                      |
| <span data-ttu-id="06078-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06078-160">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-161">對</span><span class="sxs-lookup"><span data-stu-id="06078-161">True</span></span>                                                       |
| <span data-ttu-id="06078-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06078-162">Is Indexed</span></span>             | <span data-ttu-id="06078-163">否</span><span class="sxs-lookup"><span data-stu-id="06078-163">False</span></span>                                                      |
| <span data-ttu-id="06078-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06078-164">In Global Catalog</span></span>      | <span data-ttu-id="06078-165">否</span><span class="sxs-lookup"><span data-stu-id="06078-165">False</span></span>                                                      |
| <span data-ttu-id="06078-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06078-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06078-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="06078-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="06078-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="06078-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-170">Search-Flags</span></span>           | <span data-ttu-id="06078-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="06078-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-172">System-Flags</span></span>           | <span data-ttu-id="06078-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="06078-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06078-174">Classes used in</span></span>        | [<span data-ttu-id="06078-175">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="06078-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="06078-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="06078-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="06078-177">進入</span><span class="sxs-lookup"><span data-stu-id="06078-177">Entry</span></span> | <span data-ttu-id="06078-178">值</span><span class="sxs-lookup"><span data-stu-id="06078-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="06078-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06078-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-181">System-Only</span></span>            | <span data-ttu-id="06078-182">否</span><span class="sxs-lookup"><span data-stu-id="06078-182">False</span></span>                                                      |
| <span data-ttu-id="06078-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06078-183">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-184">對</span><span class="sxs-lookup"><span data-stu-id="06078-184">True</span></span>                                                       |
| <span data-ttu-id="06078-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06078-185">Is Indexed</span></span>             | <span data-ttu-id="06078-186">否</span><span class="sxs-lookup"><span data-stu-id="06078-186">False</span></span>                                                      |
| <span data-ttu-id="06078-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06078-187">In Global Catalog</span></span>      | <span data-ttu-id="06078-188">否</span><span class="sxs-lookup"><span data-stu-id="06078-188">False</span></span>                                                      |
| <span data-ttu-id="06078-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06078-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06078-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="06078-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="06078-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="06078-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-193">Search-Flags</span></span>           | <span data-ttu-id="06078-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="06078-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-195">System-Flags</span></span>           | <span data-ttu-id="06078-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="06078-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06078-197">Classes used in</span></span>        | [<span data-ttu-id="06078-198">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="06078-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="06078-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06078-199">Windows Server 2008</span></span>



| <span data-ttu-id="06078-200">進入</span><span class="sxs-lookup"><span data-stu-id="06078-200">Entry</span></span> | <span data-ttu-id="06078-201">值</span><span class="sxs-lookup"><span data-stu-id="06078-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="06078-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06078-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-204">System-Only</span></span>            | <span data-ttu-id="06078-205">否</span><span class="sxs-lookup"><span data-stu-id="06078-205">False</span></span>                                                      |
| <span data-ttu-id="06078-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06078-206">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-207">對</span><span class="sxs-lookup"><span data-stu-id="06078-207">True</span></span>                                                       |
| <span data-ttu-id="06078-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06078-208">Is Indexed</span></span>             | <span data-ttu-id="06078-209">否</span><span class="sxs-lookup"><span data-stu-id="06078-209">False</span></span>                                                      |
| <span data-ttu-id="06078-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06078-210">In Global Catalog</span></span>      | <span data-ttu-id="06078-211">否</span><span class="sxs-lookup"><span data-stu-id="06078-211">False</span></span>                                                      |
| <span data-ttu-id="06078-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06078-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06078-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="06078-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="06078-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="06078-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-216">Search-Flags</span></span>           | <span data-ttu-id="06078-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="06078-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-218">System-Flags</span></span>           | <span data-ttu-id="06078-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="06078-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06078-220">Classes used in</span></span>        | [<span data-ttu-id="06078-221">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="06078-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="06078-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06078-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="06078-223">進入</span><span class="sxs-lookup"><span data-stu-id="06078-223">Entry</span></span> | <span data-ttu-id="06078-224">值</span><span class="sxs-lookup"><span data-stu-id="06078-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="06078-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06078-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-227">System-Only</span></span>            | <span data-ttu-id="06078-228">否</span><span class="sxs-lookup"><span data-stu-id="06078-228">False</span></span>                                                      |
| <span data-ttu-id="06078-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06078-229">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-230">對</span><span class="sxs-lookup"><span data-stu-id="06078-230">True</span></span>                                                       |
| <span data-ttu-id="06078-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06078-231">Is Indexed</span></span>             | <span data-ttu-id="06078-232">否</span><span class="sxs-lookup"><span data-stu-id="06078-232">False</span></span>                                                      |
| <span data-ttu-id="06078-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06078-233">In Global Catalog</span></span>      | <span data-ttu-id="06078-234">否</span><span class="sxs-lookup"><span data-stu-id="06078-234">False</span></span>                                                      |
| <span data-ttu-id="06078-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06078-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06078-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="06078-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="06078-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="06078-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-239">Search-Flags</span></span>           | <span data-ttu-id="06078-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="06078-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-241">System-Flags</span></span>           | <span data-ttu-id="06078-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="06078-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06078-243">Classes used in</span></span>        | [<span data-ttu-id="06078-244">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="06078-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="06078-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06078-245">Windows Server 2012</span></span>



| <span data-ttu-id="06078-246">進入</span><span class="sxs-lookup"><span data-stu-id="06078-246">Entry</span></span> | <span data-ttu-id="06078-247">值</span><span class="sxs-lookup"><span data-stu-id="06078-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="06078-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06078-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06078-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="06078-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="06078-250">System-Only</span></span>            | <span data-ttu-id="06078-251">否</span><span class="sxs-lookup"><span data-stu-id="06078-251">False</span></span>                                                      |
| <span data-ttu-id="06078-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06078-252">Is-Single-Valued</span></span>       | <span data-ttu-id="06078-253">對</span><span class="sxs-lookup"><span data-stu-id="06078-253">True</span></span>                                                       |
| <span data-ttu-id="06078-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06078-254">Is Indexed</span></span>             | <span data-ttu-id="06078-255">否</span><span class="sxs-lookup"><span data-stu-id="06078-255">False</span></span>                                                      |
| <span data-ttu-id="06078-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06078-256">In Global Catalog</span></span>      | <span data-ttu-id="06078-257">否</span><span class="sxs-lookup"><span data-stu-id="06078-257">False</span></span>                                                      |
| <span data-ttu-id="06078-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06078-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="06078-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06078-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="06078-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06078-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="06078-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06078-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="06078-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-262">Search-Flags</span></span>           | <span data-ttu-id="06078-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06078-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="06078-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06078-264">System-Flags</span></span>           | <span data-ttu-id="06078-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06078-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="06078-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06078-266">Classes used in</span></span>        | [<span data-ttu-id="06078-267">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="06078-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 






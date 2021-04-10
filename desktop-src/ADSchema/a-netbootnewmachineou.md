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
# <a name="netboot-new-machine-ou-attribute"></a><span data-ttu-id="c9d05-105">netboot-新增-電腦-OU 屬性</span><span class="sxs-lookup"><span data-stu-id="c9d05-105">netboot-New-Machine-OU attribute</span></span>

<span data-ttu-id="c9d05-106">指出將建立新用戶端電腦帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="c9d05-106">Indicates where the new client computer account will be created.</span></span>



| <span data-ttu-id="c9d05-107">進入</span><span class="sxs-lookup"><span data-stu-id="c9d05-107">Entry</span></span> | <span data-ttu-id="c9d05-108">值</span><span class="sxs-lookup"><span data-stu-id="c9d05-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c9d05-109">CN</span><span class="sxs-lookup"><span data-stu-id="c9d05-109">CN</span></span>                | <span data-ttu-id="c9d05-110">netboot-新增-電腦-OU</span><span class="sxs-lookup"><span data-stu-id="c9d05-110">netboot-New-Machine-OU</span></span>                  |
| <span data-ttu-id="c9d05-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c9d05-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c9d05-112">netbootNewMachineOU</span><span class="sxs-lookup"><span data-stu-id="c9d05-112">netbootNewMachineOU</span></span>                     |
| <span data-ttu-id="c9d05-113">大小</span><span class="sxs-lookup"><span data-stu-id="c9d05-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c9d05-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c9d05-114">Update Privilege</span></span>  | <span data-ttu-id="c9d05-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="c9d05-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="c9d05-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c9d05-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c9d05-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9d05-117">Attribute-Id</span></span>      | <span data-ttu-id="c9d05-118">1.2.840.113556.1.4.856</span><span class="sxs-lookup"><span data-stu-id="c9d05-118">1.2.840.113556.1.4.856</span></span>                  |
| <span data-ttu-id="c9d05-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c9d05-119">System-Id-Guid</span></span>    | <span data-ttu-id="c9d05-120">0738307d-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c9d05-120">0738307d-91df-11d1-aebc-0000f80367c1</span></span>    |
| <span data-ttu-id="c9d05-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9d05-121">Syntax</span></span>            | [<span data-ttu-id="c9d05-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c9d05-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c9d05-123">實作</span><span class="sxs-lookup"><span data-stu-id="c9d05-123">Implementations</span></span>

-   [<span data-ttu-id="c9d05-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9d05-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9d05-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9d05-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9d05-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9d05-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9d05-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9d05-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9d05-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9d05-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9d05-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9d05-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9d05-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9d05-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c9d05-131">進入</span><span class="sxs-lookup"><span data-stu-id="c9d05-131">Entry</span></span> | <span data-ttu-id="c9d05-132">值</span><span class="sxs-lookup"><span data-stu-id="c9d05-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="c9d05-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9d05-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9d05-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9d05-135">System-Only</span></span>            | <span data-ttu-id="c9d05-136">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-136">False</span></span>                                                      |
| <span data-ttu-id="c9d05-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9d05-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c9d05-138">對</span><span class="sxs-lookup"><span data-stu-id="c9d05-138">True</span></span>                                                       |
| <span data-ttu-id="c9d05-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9d05-139">Is Indexed</span></span>             | <span data-ttu-id="c9d05-140">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-140">False</span></span>                                                      |
| <span data-ttu-id="c9d05-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9d05-141">In Global Catalog</span></span>      | <span data-ttu-id="c9d05-142">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-142">False</span></span>                                                      |
| <span data-ttu-id="c9d05-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9d05-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9d05-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9d05-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="c9d05-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9d05-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9d05-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-147">Search-Flags</span></span>           | <span data-ttu-id="c9d05-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9d05-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="c9d05-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-149">System-Flags</span></span>           | <span data-ttu-id="c9d05-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9d05-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="c9d05-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9d05-151">Classes used in</span></span>        | [<span data-ttu-id="c9d05-152">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="c9d05-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9d05-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9d05-153">Windows Server 2003</span></span>



| <span data-ttu-id="c9d05-154">進入</span><span class="sxs-lookup"><span data-stu-id="c9d05-154">Entry</span></span> | <span data-ttu-id="c9d05-155">值</span><span class="sxs-lookup"><span data-stu-id="c9d05-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="c9d05-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9d05-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9d05-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9d05-158">System-Only</span></span>            | <span data-ttu-id="c9d05-159">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-159">False</span></span>                                                      |
| <span data-ttu-id="c9d05-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9d05-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c9d05-161">對</span><span class="sxs-lookup"><span data-stu-id="c9d05-161">True</span></span>                                                       |
| <span data-ttu-id="c9d05-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9d05-162">Is Indexed</span></span>             | <span data-ttu-id="c9d05-163">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-163">False</span></span>                                                      |
| <span data-ttu-id="c9d05-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9d05-164">In Global Catalog</span></span>      | <span data-ttu-id="c9d05-165">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-165">False</span></span>                                                      |
| <span data-ttu-id="c9d05-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9d05-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9d05-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9d05-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="c9d05-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9d05-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9d05-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-170">Search-Flags</span></span>           | <span data-ttu-id="c9d05-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9d05-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="c9d05-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-172">System-Flags</span></span>           | <span data-ttu-id="c9d05-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9d05-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="c9d05-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9d05-174">Classes used in</span></span>        | [<span data-ttu-id="c9d05-175">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="c9d05-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9d05-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9d05-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9d05-177">進入</span><span class="sxs-lookup"><span data-stu-id="c9d05-177">Entry</span></span> | <span data-ttu-id="c9d05-178">值</span><span class="sxs-lookup"><span data-stu-id="c9d05-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="c9d05-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9d05-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9d05-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9d05-181">System-Only</span></span>            | <span data-ttu-id="c9d05-182">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-182">False</span></span>                                                      |
| <span data-ttu-id="c9d05-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9d05-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c9d05-184">對</span><span class="sxs-lookup"><span data-stu-id="c9d05-184">True</span></span>                                                       |
| <span data-ttu-id="c9d05-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9d05-185">Is Indexed</span></span>             | <span data-ttu-id="c9d05-186">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-186">False</span></span>                                                      |
| <span data-ttu-id="c9d05-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9d05-187">In Global Catalog</span></span>      | <span data-ttu-id="c9d05-188">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-188">False</span></span>                                                      |
| <span data-ttu-id="c9d05-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9d05-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9d05-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9d05-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="c9d05-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9d05-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9d05-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-193">Search-Flags</span></span>           | <span data-ttu-id="c9d05-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9d05-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="c9d05-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-195">System-Flags</span></span>           | <span data-ttu-id="c9d05-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9d05-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="c9d05-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9d05-197">Classes used in</span></span>        | [<span data-ttu-id="c9d05-198">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="c9d05-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9d05-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9d05-199">Windows Server 2008</span></span>



| <span data-ttu-id="c9d05-200">進入</span><span class="sxs-lookup"><span data-stu-id="c9d05-200">Entry</span></span> | <span data-ttu-id="c9d05-201">值</span><span class="sxs-lookup"><span data-stu-id="c9d05-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="c9d05-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9d05-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9d05-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9d05-204">System-Only</span></span>            | <span data-ttu-id="c9d05-205">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-205">False</span></span>                                                      |
| <span data-ttu-id="c9d05-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9d05-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c9d05-207">對</span><span class="sxs-lookup"><span data-stu-id="c9d05-207">True</span></span>                                                       |
| <span data-ttu-id="c9d05-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9d05-208">Is Indexed</span></span>             | <span data-ttu-id="c9d05-209">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-209">False</span></span>                                                      |
| <span data-ttu-id="c9d05-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9d05-210">In Global Catalog</span></span>      | <span data-ttu-id="c9d05-211">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-211">False</span></span>                                                      |
| <span data-ttu-id="c9d05-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9d05-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9d05-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9d05-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="c9d05-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9d05-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9d05-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-216">Search-Flags</span></span>           | <span data-ttu-id="c9d05-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9d05-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="c9d05-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-218">System-Flags</span></span>           | <span data-ttu-id="c9d05-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9d05-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="c9d05-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9d05-220">Classes used in</span></span>        | [<span data-ttu-id="c9d05-221">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="c9d05-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9d05-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9d05-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9d05-223">進入</span><span class="sxs-lookup"><span data-stu-id="c9d05-223">Entry</span></span> | <span data-ttu-id="c9d05-224">值</span><span class="sxs-lookup"><span data-stu-id="c9d05-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="c9d05-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9d05-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9d05-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9d05-227">System-Only</span></span>            | <span data-ttu-id="c9d05-228">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-228">False</span></span>                                                      |
| <span data-ttu-id="c9d05-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9d05-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c9d05-230">對</span><span class="sxs-lookup"><span data-stu-id="c9d05-230">True</span></span>                                                       |
| <span data-ttu-id="c9d05-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9d05-231">Is Indexed</span></span>             | <span data-ttu-id="c9d05-232">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-232">False</span></span>                                                      |
| <span data-ttu-id="c9d05-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9d05-233">In Global Catalog</span></span>      | <span data-ttu-id="c9d05-234">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-234">False</span></span>                                                      |
| <span data-ttu-id="c9d05-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9d05-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9d05-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9d05-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="c9d05-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9d05-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9d05-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-239">Search-Flags</span></span>           | <span data-ttu-id="c9d05-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9d05-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="c9d05-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-241">System-Flags</span></span>           | <span data-ttu-id="c9d05-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9d05-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="c9d05-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9d05-243">Classes used in</span></span>        | [<span data-ttu-id="c9d05-244">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="c9d05-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9d05-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9d05-245">Windows Server 2012</span></span>



| <span data-ttu-id="c9d05-246">進入</span><span class="sxs-lookup"><span data-stu-id="c9d05-246">Entry</span></span> | <span data-ttu-id="c9d05-247">值</span><span class="sxs-lookup"><span data-stu-id="c9d05-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="c9d05-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9d05-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9d05-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="c9d05-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9d05-250">System-Only</span></span>            | <span data-ttu-id="c9d05-251">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-251">False</span></span>                                                      |
| <span data-ttu-id="c9d05-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9d05-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c9d05-253">對</span><span class="sxs-lookup"><span data-stu-id="c9d05-253">True</span></span>                                                       |
| <span data-ttu-id="c9d05-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9d05-254">Is Indexed</span></span>             | <span data-ttu-id="c9d05-255">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-255">False</span></span>                                                      |
| <span data-ttu-id="c9d05-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9d05-256">In Global Catalog</span></span>      | <span data-ttu-id="c9d05-257">否</span><span class="sxs-lookup"><span data-stu-id="c9d05-257">False</span></span>                                                      |
| <span data-ttu-id="c9d05-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9d05-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9d05-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9d05-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="c9d05-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9d05-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9d05-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="c9d05-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-262">Search-Flags</span></span>           | <span data-ttu-id="c9d05-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9d05-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="c9d05-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9d05-264">System-Flags</span></span>           | <span data-ttu-id="c9d05-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9d05-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="c9d05-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9d05-266">Classes used in</span></span>        | [<span data-ttu-id="c9d05-267">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="c9d05-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 






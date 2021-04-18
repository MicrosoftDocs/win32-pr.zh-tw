---
title: FRS-根目錄安全性屬性
description: 檔案複寫的複本集根目錄的安全描述項。
ms.assetid: 1db92f68-465a-4d93-ad4d-706ef4761ddc
ms.tgt_platform: multiple
keywords:
- FRS-根目錄安全性屬性 AD 架構
- fRSRootSecurity 屬性 AD 架構
topic_type:
- apiref
api_name:
- FRS-Root-Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a84059902998b120ad38215257fdddcb1c21ea6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106968602"
---
# <a name="frs-root-security-attribute"></a><span data-ttu-id="c9bee-105">FRS-根目錄安全性屬性</span><span class="sxs-lookup"><span data-stu-id="c9bee-105">FRS-Root-Security attribute</span></span>

<span data-ttu-id="c9bee-106">檔案複寫的複本集根目錄的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="c9bee-106">The security descriptor of replica set root for file replication.</span></span>



| <span data-ttu-id="c9bee-107">進入</span><span class="sxs-lookup"><span data-stu-id="c9bee-107">Entry</span></span> | <span data-ttu-id="c9bee-108">值</span><span class="sxs-lookup"><span data-stu-id="c9bee-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="c9bee-109">CN</span><span class="sxs-lookup"><span data-stu-id="c9bee-109">CN</span></span>                | <span data-ttu-id="c9bee-110">FRS-根目錄-安全性</span><span class="sxs-lookup"><span data-stu-id="c9bee-110">FRS-Root-Security</span></span>                                   |
| <span data-ttu-id="c9bee-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c9bee-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c9bee-112">fRSRootSecurity</span><span class="sxs-lookup"><span data-stu-id="c9bee-112">fRSRootSecurity</span></span>                                     |
| <span data-ttu-id="c9bee-113">大小</span><span class="sxs-lookup"><span data-stu-id="c9bee-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="c9bee-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c9bee-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="c9bee-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c9bee-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="c9bee-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9bee-116">Attribute-Id</span></span>      | <span data-ttu-id="c9bee-117">1.2.840.113556.1.4.535</span><span class="sxs-lookup"><span data-stu-id="c9bee-117">1.2.840.113556.1.4.535</span></span>                              |
| <span data-ttu-id="c9bee-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c9bee-118">System-Id-Guid</span></span>    | <span data-ttu-id="c9bee-119">5245801f-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c9bee-119">5245801f-ca6a-11d0-afff-0000f80367c1</span></span>                |
| <span data-ttu-id="c9bee-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9bee-120">Syntax</span></span>            | [<span data-ttu-id="c9bee-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="c9bee-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="c9bee-122">實作</span><span class="sxs-lookup"><span data-stu-id="c9bee-122">Implementations</span></span>

-   [<span data-ttu-id="c9bee-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9bee-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9bee-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9bee-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9bee-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9bee-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9bee-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9bee-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9bee-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9bee-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9bee-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9bee-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9bee-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9bee-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c9bee-130">進入</span><span class="sxs-lookup"><span data-stu-id="c9bee-130">Entry</span></span> | <span data-ttu-id="c9bee-131">值</span><span class="sxs-lookup"><span data-stu-id="c9bee-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bee-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9bee-132">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9bee-133">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9bee-134">System-Only</span></span>            | <span data-ttu-id="c9bee-135">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-135">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9bee-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c9bee-137">對</span><span class="sxs-lookup"><span data-stu-id="c9bee-137">True</span></span>                                                                                                       |
| <span data-ttu-id="c9bee-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9bee-138">Is Indexed</span></span>             | <span data-ttu-id="c9bee-139">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-139">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9bee-140">In Global Catalog</span></span>      | <span data-ttu-id="c9bee-141">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-141">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9bee-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9bee-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9bee-143">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c9bee-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9bee-144">Range-Lower</span></span>            | <span data-ttu-id="c9bee-145">0</span><span class="sxs-lookup"><span data-stu-id="c9bee-145">0</span></span>                                                                                                          |
| <span data-ttu-id="c9bee-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9bee-146">Range-Upper</span></span>            | <span data-ttu-id="c9bee-147">65535</span><span class="sxs-lookup"><span data-stu-id="c9bee-147">65535</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-148">Search-Flags</span></span>           | <span data-ttu-id="c9bee-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9bee-149">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-150">System-Flags</span></span>           | <span data-ttu-id="c9bee-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9bee-151">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9bee-152">Classes used in</span></span>        | [<span data-ttu-id="c9bee-153">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="c9bee-153">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="c9bee-154">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9bee-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9bee-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9bee-155">Windows Server 2003</span></span>



| <span data-ttu-id="c9bee-156">進入</span><span class="sxs-lookup"><span data-stu-id="c9bee-156">Entry</span></span> | <span data-ttu-id="c9bee-157">值</span><span class="sxs-lookup"><span data-stu-id="c9bee-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bee-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9bee-158">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9bee-159">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9bee-160">System-Only</span></span>            | <span data-ttu-id="c9bee-161">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-161">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9bee-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c9bee-163">對</span><span class="sxs-lookup"><span data-stu-id="c9bee-163">True</span></span>                                                                                                       |
| <span data-ttu-id="c9bee-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9bee-164">Is Indexed</span></span>             | <span data-ttu-id="c9bee-165">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-165">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9bee-166">In Global Catalog</span></span>      | <span data-ttu-id="c9bee-167">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-167">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9bee-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9bee-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9bee-169">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c9bee-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9bee-170">Range-Lower</span></span>            | <span data-ttu-id="c9bee-171">0</span><span class="sxs-lookup"><span data-stu-id="c9bee-171">0</span></span>                                                                                                          |
| <span data-ttu-id="c9bee-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9bee-172">Range-Upper</span></span>            | <span data-ttu-id="c9bee-173">65535</span><span class="sxs-lookup"><span data-stu-id="c9bee-173">65535</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-174">Search-Flags</span></span>           | <span data-ttu-id="c9bee-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9bee-175">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-176">System-Flags</span></span>           | <span data-ttu-id="c9bee-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9bee-177">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9bee-178">Classes used in</span></span>        | [<span data-ttu-id="c9bee-179">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="c9bee-179">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="c9bee-180">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9bee-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9bee-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9bee-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9bee-182">進入</span><span class="sxs-lookup"><span data-stu-id="c9bee-182">Entry</span></span> | <span data-ttu-id="c9bee-183">值</span><span class="sxs-lookup"><span data-stu-id="c9bee-183">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bee-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9bee-184">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9bee-185">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9bee-186">System-Only</span></span>            | <span data-ttu-id="c9bee-187">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-187">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9bee-188">Is-Single-Valued</span></span>       | <span data-ttu-id="c9bee-189">對</span><span class="sxs-lookup"><span data-stu-id="c9bee-189">True</span></span>                                                                                                       |
| <span data-ttu-id="c9bee-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9bee-190">Is Indexed</span></span>             | <span data-ttu-id="c9bee-191">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-191">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9bee-192">In Global Catalog</span></span>      | <span data-ttu-id="c9bee-193">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-193">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9bee-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9bee-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9bee-195">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c9bee-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9bee-196">Range-Lower</span></span>            | <span data-ttu-id="c9bee-197">0</span><span class="sxs-lookup"><span data-stu-id="c9bee-197">0</span></span>                                                                                                          |
| <span data-ttu-id="c9bee-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9bee-198">Range-Upper</span></span>            | <span data-ttu-id="c9bee-199">65535</span><span class="sxs-lookup"><span data-stu-id="c9bee-199">65535</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-200">Search-Flags</span></span>           | <span data-ttu-id="c9bee-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9bee-201">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-202">System-Flags</span></span>           | <span data-ttu-id="c9bee-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9bee-203">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9bee-204">Classes used in</span></span>        | [<span data-ttu-id="c9bee-205">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="c9bee-205">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="c9bee-206">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9bee-206">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9bee-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9bee-207">Windows Server 2008</span></span>



| <span data-ttu-id="c9bee-208">進入</span><span class="sxs-lookup"><span data-stu-id="c9bee-208">Entry</span></span> | <span data-ttu-id="c9bee-209">值</span><span class="sxs-lookup"><span data-stu-id="c9bee-209">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bee-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9bee-210">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9bee-211">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9bee-212">System-Only</span></span>            | <span data-ttu-id="c9bee-213">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-213">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9bee-214">Is-Single-Valued</span></span>       | <span data-ttu-id="c9bee-215">對</span><span class="sxs-lookup"><span data-stu-id="c9bee-215">True</span></span>                                                                                                       |
| <span data-ttu-id="c9bee-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9bee-216">Is Indexed</span></span>             | <span data-ttu-id="c9bee-217">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-217">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9bee-218">In Global Catalog</span></span>      | <span data-ttu-id="c9bee-219">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-219">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9bee-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9bee-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9bee-221">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c9bee-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9bee-222">Range-Lower</span></span>            | <span data-ttu-id="c9bee-223">0</span><span class="sxs-lookup"><span data-stu-id="c9bee-223">0</span></span>                                                                                                          |
| <span data-ttu-id="c9bee-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9bee-224">Range-Upper</span></span>            | <span data-ttu-id="c9bee-225">65535</span><span class="sxs-lookup"><span data-stu-id="c9bee-225">65535</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-226">Search-Flags</span></span>           | <span data-ttu-id="c9bee-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9bee-227">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-228">System-Flags</span></span>           | <span data-ttu-id="c9bee-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9bee-229">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9bee-230">Classes used in</span></span>        | [<span data-ttu-id="c9bee-231">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="c9bee-231">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="c9bee-232">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9bee-232">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9bee-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9bee-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9bee-234">進入</span><span class="sxs-lookup"><span data-stu-id="c9bee-234">Entry</span></span> | <span data-ttu-id="c9bee-235">值</span><span class="sxs-lookup"><span data-stu-id="c9bee-235">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bee-236">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9bee-236">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9bee-237">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9bee-238">System-Only</span></span>            | <span data-ttu-id="c9bee-239">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-239">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-240">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9bee-240">Is-Single-Valued</span></span>       | <span data-ttu-id="c9bee-241">對</span><span class="sxs-lookup"><span data-stu-id="c9bee-241">True</span></span>                                                                                                       |
| <span data-ttu-id="c9bee-242">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9bee-242">Is Indexed</span></span>             | <span data-ttu-id="c9bee-243">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-243">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-244">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9bee-244">In Global Catalog</span></span>      | <span data-ttu-id="c9bee-245">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-245">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-246">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9bee-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9bee-247">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9bee-247">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c9bee-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9bee-248">Range-Lower</span></span>            | <span data-ttu-id="c9bee-249">0</span><span class="sxs-lookup"><span data-stu-id="c9bee-249">0</span></span>                                                                                                          |
| <span data-ttu-id="c9bee-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9bee-250">Range-Upper</span></span>            | <span data-ttu-id="c9bee-251">65535</span><span class="sxs-lookup"><span data-stu-id="c9bee-251">65535</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-252">Search-Flags</span></span>           | <span data-ttu-id="c9bee-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9bee-253">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-254">System-Flags</span></span>           | <span data-ttu-id="c9bee-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9bee-255">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-256">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9bee-256">Classes used in</span></span>        | [<span data-ttu-id="c9bee-257">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="c9bee-257">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="c9bee-258">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9bee-258">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9bee-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9bee-259">Windows Server 2012</span></span>



| <span data-ttu-id="c9bee-260">進入</span><span class="sxs-lookup"><span data-stu-id="c9bee-260">Entry</span></span> | <span data-ttu-id="c9bee-261">值</span><span class="sxs-lookup"><span data-stu-id="c9bee-261">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bee-262">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9bee-262">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9bee-263">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c9bee-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9bee-264">System-Only</span></span>            | <span data-ttu-id="c9bee-265">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-265">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-266">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9bee-266">Is-Single-Valued</span></span>       | <span data-ttu-id="c9bee-267">對</span><span class="sxs-lookup"><span data-stu-id="c9bee-267">True</span></span>                                                                                                       |
| <span data-ttu-id="c9bee-268">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9bee-268">Is Indexed</span></span>             | <span data-ttu-id="c9bee-269">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-269">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-270">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9bee-270">In Global Catalog</span></span>      | <span data-ttu-id="c9bee-271">否</span><span class="sxs-lookup"><span data-stu-id="c9bee-271">False</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-272">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9bee-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9bee-273">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9bee-273">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c9bee-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9bee-274">Range-Lower</span></span>            | <span data-ttu-id="c9bee-275">0</span><span class="sxs-lookup"><span data-stu-id="c9bee-275">0</span></span>                                                                                                          |
| <span data-ttu-id="c9bee-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9bee-276">Range-Upper</span></span>            | <span data-ttu-id="c9bee-277">65535</span><span class="sxs-lookup"><span data-stu-id="c9bee-277">65535</span></span>                                                                                                      |
| <span data-ttu-id="c9bee-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-278">Search-Flags</span></span>           | <span data-ttu-id="c9bee-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9bee-279">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9bee-280">System-Flags</span></span>           | <span data-ttu-id="c9bee-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9bee-281">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c9bee-282">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9bee-282">Classes used in</span></span>        | [<span data-ttu-id="c9bee-283">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="c9bee-283">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="c9bee-284">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9bee-284">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 






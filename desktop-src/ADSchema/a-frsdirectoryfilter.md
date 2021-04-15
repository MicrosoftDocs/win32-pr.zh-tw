---
title: FRS-目錄-篩選屬性
description: 從檔案複寫排除的目錄清單，例如 temp 或 obj。
ms.assetid: 3ce37a96-0cb2-46bf-aad1-80fc1304855d
ms.tgt_platform: multiple
keywords:
- FRS-目錄-篩選屬性 AD 架構
- fRSDirectoryFilter 屬性 AD 架構
topic_type:
- apiref
api_name:
- FRS-Directory-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b547cd431d7f51af698a137b7edd7dd299a3ec2f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467185"
---
# <a name="frs-directory-filter-attribute"></a><span data-ttu-id="3d43f-105">FRS-目錄-篩選屬性</span><span class="sxs-lookup"><span data-stu-id="3d43f-105">FRS-Directory-Filter attribute</span></span>

<span data-ttu-id="3d43f-106">從檔案複寫排除的目錄清單，例如 temp 或 obj。</span><span class="sxs-lookup"><span data-stu-id="3d43f-106">The list of directories excluded from file replication, for example, temp, or obj.</span></span>



| <span data-ttu-id="3d43f-107">進入</span><span class="sxs-lookup"><span data-stu-id="3d43f-107">Entry</span></span> | <span data-ttu-id="3d43f-108">值</span><span class="sxs-lookup"><span data-stu-id="3d43f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3d43f-109">CN</span><span class="sxs-lookup"><span data-stu-id="3d43f-109">CN</span></span>                | <span data-ttu-id="3d43f-110">FRS-目錄-篩選</span><span class="sxs-lookup"><span data-stu-id="3d43f-110">FRS-Directory-Filter</span></span>                        |
| <span data-ttu-id="3d43f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3d43f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3d43f-112">fRSDirectoryFilter</span><span class="sxs-lookup"><span data-stu-id="3d43f-112">fRSDirectoryFilter</span></span>                          |
| <span data-ttu-id="3d43f-113">大小</span><span class="sxs-lookup"><span data-stu-id="3d43f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="3d43f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3d43f-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="3d43f-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3d43f-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3d43f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d43f-116">Attribute-Id</span></span>      | <span data-ttu-id="3d43f-117">1.2.840.113556.1.4.484</span><span class="sxs-lookup"><span data-stu-id="3d43f-117">1.2.840.113556.1.4.484</span></span>                      |
| <span data-ttu-id="3d43f-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3d43f-118">System-Id-Guid</span></span>    | <span data-ttu-id="3d43f-119">1be8f171-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="3d43f-119">1be8f171-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="3d43f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d43f-120">Syntax</span></span>            | [<span data-ttu-id="3d43f-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3d43f-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3d43f-122">實作</span><span class="sxs-lookup"><span data-stu-id="3d43f-122">Implementations</span></span>

-   [<span data-ttu-id="3d43f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3d43f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3d43f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d43f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d43f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d43f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d43f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d43f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d43f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d43f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d43f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d43f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3d43f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d43f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="3d43f-130">進入</span><span class="sxs-lookup"><span data-stu-id="3d43f-130">Entry</span></span> | <span data-ttu-id="3d43f-131">值</span><span class="sxs-lookup"><span data-stu-id="3d43f-131">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3d43f-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d43f-132">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d43f-133">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d43f-134">System-Only</span></span>            | <span data-ttu-id="3d43f-135">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-135">False</span></span>                                                     |
| <span data-ttu-id="3d43f-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d43f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="3d43f-137">對</span><span class="sxs-lookup"><span data-stu-id="3d43f-137">True</span></span>                                                      |
| <span data-ttu-id="3d43f-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d43f-138">Is Indexed</span></span>             | <span data-ttu-id="3d43f-139">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-139">False</span></span>                                                     |
| <span data-ttu-id="3d43f-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d43f-140">In Global Catalog</span></span>      | <span data-ttu-id="3d43f-141">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-141">False</span></span>                                                     |
| <span data-ttu-id="3d43f-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d43f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d43f-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d43f-143">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3d43f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d43f-144">Range-Lower</span></span>            | <span data-ttu-id="3d43f-145">0</span><span class="sxs-lookup"><span data-stu-id="3d43f-145">0</span></span>                                                         |
| <span data-ttu-id="3d43f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d43f-146">Range-Upper</span></span>            | <span data-ttu-id="3d43f-147">2048</span><span class="sxs-lookup"><span data-stu-id="3d43f-147">2048</span></span>                                                      |
| <span data-ttu-id="3d43f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-148">Search-Flags</span></span>           | <span data-ttu-id="3d43f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d43f-149">0x00000000</span></span>                                                |
| <span data-ttu-id="3d43f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-150">System-Flags</span></span>           | <span data-ttu-id="3d43f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d43f-151">0x00000010</span></span>                                                |
| <span data-ttu-id="3d43f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d43f-152">Classes used in</span></span>        | [<span data-ttu-id="3d43f-153">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3d43f-153">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3d43f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d43f-154">Windows Server 2003</span></span>



| <span data-ttu-id="3d43f-155">進入</span><span class="sxs-lookup"><span data-stu-id="3d43f-155">Entry</span></span> | <span data-ttu-id="3d43f-156">值</span><span class="sxs-lookup"><span data-stu-id="3d43f-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3d43f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d43f-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d43f-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d43f-159">System-Only</span></span>            | <span data-ttu-id="3d43f-160">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-160">False</span></span>                                                     |
| <span data-ttu-id="3d43f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d43f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3d43f-162">對</span><span class="sxs-lookup"><span data-stu-id="3d43f-162">True</span></span>                                                      |
| <span data-ttu-id="3d43f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d43f-163">Is Indexed</span></span>             | <span data-ttu-id="3d43f-164">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-164">False</span></span>                                                     |
| <span data-ttu-id="3d43f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d43f-165">In Global Catalog</span></span>      | <span data-ttu-id="3d43f-166">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-166">False</span></span>                                                     |
| <span data-ttu-id="3d43f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d43f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d43f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d43f-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3d43f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d43f-169">Range-Lower</span></span>            | <span data-ttu-id="3d43f-170">0</span><span class="sxs-lookup"><span data-stu-id="3d43f-170">0</span></span>                                                         |
| <span data-ttu-id="3d43f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d43f-171">Range-Upper</span></span>            | <span data-ttu-id="3d43f-172">2048</span><span class="sxs-lookup"><span data-stu-id="3d43f-172">2048</span></span>                                                      |
| <span data-ttu-id="3d43f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-173">Search-Flags</span></span>           | <span data-ttu-id="3d43f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d43f-174">0x00000000</span></span>                                                |
| <span data-ttu-id="3d43f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-175">System-Flags</span></span>           | <span data-ttu-id="3d43f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d43f-176">0x00000010</span></span>                                                |
| <span data-ttu-id="3d43f-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d43f-177">Classes used in</span></span>        | [<span data-ttu-id="3d43f-178">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3d43f-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d43f-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d43f-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d43f-180">進入</span><span class="sxs-lookup"><span data-stu-id="3d43f-180">Entry</span></span> | <span data-ttu-id="3d43f-181">值</span><span class="sxs-lookup"><span data-stu-id="3d43f-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3d43f-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d43f-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d43f-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d43f-184">System-Only</span></span>            | <span data-ttu-id="3d43f-185">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-185">False</span></span>                                                     |
| <span data-ttu-id="3d43f-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d43f-186">Is-Single-Valued</span></span>       | <span data-ttu-id="3d43f-187">對</span><span class="sxs-lookup"><span data-stu-id="3d43f-187">True</span></span>                                                      |
| <span data-ttu-id="3d43f-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d43f-188">Is Indexed</span></span>             | <span data-ttu-id="3d43f-189">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-189">False</span></span>                                                     |
| <span data-ttu-id="3d43f-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d43f-190">In Global Catalog</span></span>      | <span data-ttu-id="3d43f-191">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-191">False</span></span>                                                     |
| <span data-ttu-id="3d43f-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d43f-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d43f-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d43f-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3d43f-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d43f-194">Range-Lower</span></span>            | <span data-ttu-id="3d43f-195">0</span><span class="sxs-lookup"><span data-stu-id="3d43f-195">0</span></span>                                                         |
| <span data-ttu-id="3d43f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d43f-196">Range-Upper</span></span>            | <span data-ttu-id="3d43f-197">2048</span><span class="sxs-lookup"><span data-stu-id="3d43f-197">2048</span></span>                                                      |
| <span data-ttu-id="3d43f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-198">Search-Flags</span></span>           | <span data-ttu-id="3d43f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d43f-199">0x00000000</span></span>                                                |
| <span data-ttu-id="3d43f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-200">System-Flags</span></span>           | <span data-ttu-id="3d43f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d43f-201">0x00000010</span></span>                                                |
| <span data-ttu-id="3d43f-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d43f-202">Classes used in</span></span>        | [<span data-ttu-id="3d43f-203">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3d43f-203">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d43f-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d43f-204">Windows Server 2008</span></span>



| <span data-ttu-id="3d43f-205">進入</span><span class="sxs-lookup"><span data-stu-id="3d43f-205">Entry</span></span> | <span data-ttu-id="3d43f-206">值</span><span class="sxs-lookup"><span data-stu-id="3d43f-206">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3d43f-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d43f-207">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d43f-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d43f-209">System-Only</span></span>            | <span data-ttu-id="3d43f-210">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-210">False</span></span>                                                     |
| <span data-ttu-id="3d43f-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d43f-211">Is-Single-Valued</span></span>       | <span data-ttu-id="3d43f-212">對</span><span class="sxs-lookup"><span data-stu-id="3d43f-212">True</span></span>                                                      |
| <span data-ttu-id="3d43f-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d43f-213">Is Indexed</span></span>             | <span data-ttu-id="3d43f-214">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-214">False</span></span>                                                     |
| <span data-ttu-id="3d43f-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d43f-215">In Global Catalog</span></span>      | <span data-ttu-id="3d43f-216">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-216">False</span></span>                                                     |
| <span data-ttu-id="3d43f-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d43f-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d43f-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d43f-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3d43f-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d43f-219">Range-Lower</span></span>            | <span data-ttu-id="3d43f-220">0</span><span class="sxs-lookup"><span data-stu-id="3d43f-220">0</span></span>                                                         |
| <span data-ttu-id="3d43f-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d43f-221">Range-Upper</span></span>            | <span data-ttu-id="3d43f-222">2048</span><span class="sxs-lookup"><span data-stu-id="3d43f-222">2048</span></span>                                                      |
| <span data-ttu-id="3d43f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-223">Search-Flags</span></span>           | <span data-ttu-id="3d43f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d43f-224">0x00000000</span></span>                                                |
| <span data-ttu-id="3d43f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-225">System-Flags</span></span>           | <span data-ttu-id="3d43f-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d43f-226">0x00000010</span></span>                                                |
| <span data-ttu-id="3d43f-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d43f-227">Classes used in</span></span>        | [<span data-ttu-id="3d43f-228">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3d43f-228">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d43f-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d43f-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d43f-230">進入</span><span class="sxs-lookup"><span data-stu-id="3d43f-230">Entry</span></span> | <span data-ttu-id="3d43f-231">值</span><span class="sxs-lookup"><span data-stu-id="3d43f-231">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3d43f-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d43f-232">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d43f-233">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d43f-234">System-Only</span></span>            | <span data-ttu-id="3d43f-235">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-235">False</span></span>                                                     |
| <span data-ttu-id="3d43f-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d43f-236">Is-Single-Valued</span></span>       | <span data-ttu-id="3d43f-237">對</span><span class="sxs-lookup"><span data-stu-id="3d43f-237">True</span></span>                                                      |
| <span data-ttu-id="3d43f-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d43f-238">Is Indexed</span></span>             | <span data-ttu-id="3d43f-239">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-239">False</span></span>                                                     |
| <span data-ttu-id="3d43f-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d43f-240">In Global Catalog</span></span>      | <span data-ttu-id="3d43f-241">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-241">False</span></span>                                                     |
| <span data-ttu-id="3d43f-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d43f-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d43f-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d43f-243">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3d43f-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d43f-244">Range-Lower</span></span>            | <span data-ttu-id="3d43f-245">0</span><span class="sxs-lookup"><span data-stu-id="3d43f-245">0</span></span>                                                         |
| <span data-ttu-id="3d43f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d43f-246">Range-Upper</span></span>            | <span data-ttu-id="3d43f-247">2048</span><span class="sxs-lookup"><span data-stu-id="3d43f-247">2048</span></span>                                                      |
| <span data-ttu-id="3d43f-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-248">Search-Flags</span></span>           | <span data-ttu-id="3d43f-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d43f-249">0x00000000</span></span>                                                |
| <span data-ttu-id="3d43f-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-250">System-Flags</span></span>           | <span data-ttu-id="3d43f-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d43f-251">0x00000010</span></span>                                                |
| <span data-ttu-id="3d43f-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d43f-252">Classes used in</span></span>        | [<span data-ttu-id="3d43f-253">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3d43f-253">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d43f-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d43f-254">Windows Server 2012</span></span>



| <span data-ttu-id="3d43f-255">進入</span><span class="sxs-lookup"><span data-stu-id="3d43f-255">Entry</span></span> | <span data-ttu-id="3d43f-256">值</span><span class="sxs-lookup"><span data-stu-id="3d43f-256">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3d43f-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d43f-257">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d43f-258">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3d43f-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d43f-259">System-Only</span></span>            | <span data-ttu-id="3d43f-260">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-260">False</span></span>                                                     |
| <span data-ttu-id="3d43f-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d43f-261">Is-Single-Valued</span></span>       | <span data-ttu-id="3d43f-262">對</span><span class="sxs-lookup"><span data-stu-id="3d43f-262">True</span></span>                                                      |
| <span data-ttu-id="3d43f-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d43f-263">Is Indexed</span></span>             | <span data-ttu-id="3d43f-264">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-264">False</span></span>                                                     |
| <span data-ttu-id="3d43f-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d43f-265">In Global Catalog</span></span>      | <span data-ttu-id="3d43f-266">否</span><span class="sxs-lookup"><span data-stu-id="3d43f-266">False</span></span>                                                     |
| <span data-ttu-id="3d43f-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d43f-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d43f-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d43f-268">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3d43f-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d43f-269">Range-Lower</span></span>            | <span data-ttu-id="3d43f-270">0</span><span class="sxs-lookup"><span data-stu-id="3d43f-270">0</span></span>                                                         |
| <span data-ttu-id="3d43f-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d43f-271">Range-Upper</span></span>            | <span data-ttu-id="3d43f-272">2048</span><span class="sxs-lookup"><span data-stu-id="3d43f-272">2048</span></span>                                                      |
| <span data-ttu-id="3d43f-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-273">Search-Flags</span></span>           | <span data-ttu-id="3d43f-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d43f-274">0x00000000</span></span>                                                |
| <span data-ttu-id="3d43f-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d43f-275">System-Flags</span></span>           | <span data-ttu-id="3d43f-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d43f-276">0x00000010</span></span>                                                |
| <span data-ttu-id="3d43f-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d43f-277">Classes used in</span></span>        | [<span data-ttu-id="3d43f-278">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3d43f-278">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 






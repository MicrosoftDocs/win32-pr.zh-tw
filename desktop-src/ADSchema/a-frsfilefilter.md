---
title: FRS-檔案篩選器屬性
description: 從檔案複寫中排除的副檔名清單。
ms.assetid: 094a393a-9e1a-4da8-a38a-161102f164fd
ms.tgt_platform: multiple
keywords:
- FRS-檔案-篩選屬性 AD 架構
- fRSFileFilter 屬性 AD 架構
topic_type:
- apiref
api_name:
- FRS-File-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234cf7d6e56e84c2ed9578fc56036e581a2f0ad2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971883"
---
# <a name="frs-file-filter-attribute"></a><span data-ttu-id="116b8-105">FRS-檔案篩選器屬性</span><span class="sxs-lookup"><span data-stu-id="116b8-105">FRS-File-Filter attribute</span></span>

<span data-ttu-id="116b8-106">從檔案複寫中排除的副檔名清單。</span><span class="sxs-lookup"><span data-stu-id="116b8-106">A list of file name extensions excluded from file replication.</span></span>



| <span data-ttu-id="116b8-107">進入</span><span class="sxs-lookup"><span data-stu-id="116b8-107">Entry</span></span> | <span data-ttu-id="116b8-108">值</span><span class="sxs-lookup"><span data-stu-id="116b8-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="116b8-109">CN</span><span class="sxs-lookup"><span data-stu-id="116b8-109">CN</span></span>                | <span data-ttu-id="116b8-110">FRS-檔案-篩選</span><span class="sxs-lookup"><span data-stu-id="116b8-110">FRS-File-Filter</span></span>                             |
| <span data-ttu-id="116b8-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="116b8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="116b8-112">fRSFileFilter</span><span class="sxs-lookup"><span data-stu-id="116b8-112">fRSFileFilter</span></span>                               |
| <span data-ttu-id="116b8-113">大小</span><span class="sxs-lookup"><span data-stu-id="116b8-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="116b8-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="116b8-114">Update Privilege</span></span>  | <span data-ttu-id="116b8-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="116b8-115">Domain administrator</span></span>                        |
| <span data-ttu-id="116b8-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="116b8-116">Update Frequency</span></span>  | <span data-ttu-id="116b8-117">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="116b8-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="116b8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="116b8-118">Attribute-Id</span></span>      | <span data-ttu-id="116b8-119">1.2.840.113556.1.4.483</span><span class="sxs-lookup"><span data-stu-id="116b8-119">1.2.840.113556.1.4.483</span></span>                      |
| <span data-ttu-id="116b8-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="116b8-120">System-Id-Guid</span></span>    | <span data-ttu-id="116b8-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="116b8-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="116b8-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="116b8-122">Syntax</span></span>            | [<span data-ttu-id="116b8-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="116b8-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="116b8-124">實作</span><span class="sxs-lookup"><span data-stu-id="116b8-124">Implementations</span></span>

-   [<span data-ttu-id="116b8-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="116b8-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="116b8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="116b8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="116b8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="116b8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="116b8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="116b8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="116b8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="116b8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="116b8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="116b8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="116b8-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="116b8-131">Windows 2000 Server</span></span>



| <span data-ttu-id="116b8-132">進入</span><span class="sxs-lookup"><span data-stu-id="116b8-132">Entry</span></span> | <span data-ttu-id="116b8-133">值</span><span class="sxs-lookup"><span data-stu-id="116b8-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="116b8-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="116b8-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="116b8-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="116b8-136">System-Only</span></span>            | <span data-ttu-id="116b8-137">否</span><span class="sxs-lookup"><span data-stu-id="116b8-137">False</span></span>                                                     |
| <span data-ttu-id="116b8-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="116b8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="116b8-139">對</span><span class="sxs-lookup"><span data-stu-id="116b8-139">True</span></span>                                                      |
| <span data-ttu-id="116b8-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="116b8-140">Is Indexed</span></span>             | <span data-ttu-id="116b8-141">否</span><span class="sxs-lookup"><span data-stu-id="116b8-141">False</span></span>                                                     |
| <span data-ttu-id="116b8-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="116b8-142">In Global Catalog</span></span>      | <span data-ttu-id="116b8-143">否</span><span class="sxs-lookup"><span data-stu-id="116b8-143">False</span></span>                                                     |
| <span data-ttu-id="116b8-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="116b8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="116b8-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="116b8-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="116b8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="116b8-146">Range-Lower</span></span>            | <span data-ttu-id="116b8-147">0</span><span class="sxs-lookup"><span data-stu-id="116b8-147">0</span></span>                                                         |
| <span data-ttu-id="116b8-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="116b8-148">Range-Upper</span></span>            | <span data-ttu-id="116b8-149">2048</span><span class="sxs-lookup"><span data-stu-id="116b8-149">2048</span></span>                                                      |
| <span data-ttu-id="116b8-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-150">Search-Flags</span></span>           | <span data-ttu-id="116b8-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="116b8-151">0x00000000</span></span>                                                |
| <span data-ttu-id="116b8-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-152">System-Flags</span></span>           | <span data-ttu-id="116b8-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="116b8-153">0x00000010</span></span>                                                |
| <span data-ttu-id="116b8-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="116b8-154">Classes used in</span></span>        | [<span data-ttu-id="116b8-155">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="116b8-155">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="116b8-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="116b8-156">Windows Server 2003</span></span>



| <span data-ttu-id="116b8-157">進入</span><span class="sxs-lookup"><span data-stu-id="116b8-157">Entry</span></span> | <span data-ttu-id="116b8-158">值</span><span class="sxs-lookup"><span data-stu-id="116b8-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="116b8-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="116b8-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="116b8-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="116b8-161">System-Only</span></span>            | <span data-ttu-id="116b8-162">否</span><span class="sxs-lookup"><span data-stu-id="116b8-162">False</span></span>                                                     |
| <span data-ttu-id="116b8-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="116b8-163">Is-Single-Valued</span></span>       | <span data-ttu-id="116b8-164">對</span><span class="sxs-lookup"><span data-stu-id="116b8-164">True</span></span>                                                      |
| <span data-ttu-id="116b8-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="116b8-165">Is Indexed</span></span>             | <span data-ttu-id="116b8-166">否</span><span class="sxs-lookup"><span data-stu-id="116b8-166">False</span></span>                                                     |
| <span data-ttu-id="116b8-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="116b8-167">In Global Catalog</span></span>      | <span data-ttu-id="116b8-168">否</span><span class="sxs-lookup"><span data-stu-id="116b8-168">False</span></span>                                                     |
| <span data-ttu-id="116b8-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="116b8-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="116b8-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="116b8-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="116b8-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="116b8-171">Range-Lower</span></span>            | <span data-ttu-id="116b8-172">0</span><span class="sxs-lookup"><span data-stu-id="116b8-172">0</span></span>                                                         |
| <span data-ttu-id="116b8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="116b8-173">Range-Upper</span></span>            | <span data-ttu-id="116b8-174">2048</span><span class="sxs-lookup"><span data-stu-id="116b8-174">2048</span></span>                                                      |
| <span data-ttu-id="116b8-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-175">Search-Flags</span></span>           | <span data-ttu-id="116b8-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="116b8-176">0x00000000</span></span>                                                |
| <span data-ttu-id="116b8-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-177">System-Flags</span></span>           | <span data-ttu-id="116b8-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="116b8-178">0x00000010</span></span>                                                |
| <span data-ttu-id="116b8-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="116b8-179">Classes used in</span></span>        | [<span data-ttu-id="116b8-180">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="116b8-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="116b8-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="116b8-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="116b8-182">進入</span><span class="sxs-lookup"><span data-stu-id="116b8-182">Entry</span></span> | <span data-ttu-id="116b8-183">值</span><span class="sxs-lookup"><span data-stu-id="116b8-183">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="116b8-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="116b8-184">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="116b8-185">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="116b8-186">System-Only</span></span>            | <span data-ttu-id="116b8-187">否</span><span class="sxs-lookup"><span data-stu-id="116b8-187">False</span></span>                                                     |
| <span data-ttu-id="116b8-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="116b8-188">Is-Single-Valued</span></span>       | <span data-ttu-id="116b8-189">對</span><span class="sxs-lookup"><span data-stu-id="116b8-189">True</span></span>                                                      |
| <span data-ttu-id="116b8-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="116b8-190">Is Indexed</span></span>             | <span data-ttu-id="116b8-191">否</span><span class="sxs-lookup"><span data-stu-id="116b8-191">False</span></span>                                                     |
| <span data-ttu-id="116b8-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="116b8-192">In Global Catalog</span></span>      | <span data-ttu-id="116b8-193">否</span><span class="sxs-lookup"><span data-stu-id="116b8-193">False</span></span>                                                     |
| <span data-ttu-id="116b8-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="116b8-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="116b8-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="116b8-195">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="116b8-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="116b8-196">Range-Lower</span></span>            | <span data-ttu-id="116b8-197">0</span><span class="sxs-lookup"><span data-stu-id="116b8-197">0</span></span>                                                         |
| <span data-ttu-id="116b8-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="116b8-198">Range-Upper</span></span>            | <span data-ttu-id="116b8-199">2048</span><span class="sxs-lookup"><span data-stu-id="116b8-199">2048</span></span>                                                      |
| <span data-ttu-id="116b8-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-200">Search-Flags</span></span>           | <span data-ttu-id="116b8-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="116b8-201">0x00000000</span></span>                                                |
| <span data-ttu-id="116b8-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-202">System-Flags</span></span>           | <span data-ttu-id="116b8-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="116b8-203">0x00000010</span></span>                                                |
| <span data-ttu-id="116b8-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="116b8-204">Classes used in</span></span>        | [<span data-ttu-id="116b8-205">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="116b8-205">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="116b8-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="116b8-206">Windows Server 2008</span></span>



| <span data-ttu-id="116b8-207">進入</span><span class="sxs-lookup"><span data-stu-id="116b8-207">Entry</span></span> | <span data-ttu-id="116b8-208">值</span><span class="sxs-lookup"><span data-stu-id="116b8-208">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="116b8-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="116b8-209">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="116b8-210">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="116b8-211">System-Only</span></span>            | <span data-ttu-id="116b8-212">否</span><span class="sxs-lookup"><span data-stu-id="116b8-212">False</span></span>                                                     |
| <span data-ttu-id="116b8-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="116b8-213">Is-Single-Valued</span></span>       | <span data-ttu-id="116b8-214">對</span><span class="sxs-lookup"><span data-stu-id="116b8-214">True</span></span>                                                      |
| <span data-ttu-id="116b8-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="116b8-215">Is Indexed</span></span>             | <span data-ttu-id="116b8-216">否</span><span class="sxs-lookup"><span data-stu-id="116b8-216">False</span></span>                                                     |
| <span data-ttu-id="116b8-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="116b8-217">In Global Catalog</span></span>      | <span data-ttu-id="116b8-218">否</span><span class="sxs-lookup"><span data-stu-id="116b8-218">False</span></span>                                                     |
| <span data-ttu-id="116b8-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="116b8-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="116b8-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="116b8-220">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="116b8-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="116b8-221">Range-Lower</span></span>            | <span data-ttu-id="116b8-222">0</span><span class="sxs-lookup"><span data-stu-id="116b8-222">0</span></span>                                                         |
| <span data-ttu-id="116b8-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="116b8-223">Range-Upper</span></span>            | <span data-ttu-id="116b8-224">2048</span><span class="sxs-lookup"><span data-stu-id="116b8-224">2048</span></span>                                                      |
| <span data-ttu-id="116b8-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-225">Search-Flags</span></span>           | <span data-ttu-id="116b8-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="116b8-226">0x00000000</span></span>                                                |
| <span data-ttu-id="116b8-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-227">System-Flags</span></span>           | <span data-ttu-id="116b8-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="116b8-228">0x00000010</span></span>                                                |
| <span data-ttu-id="116b8-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="116b8-229">Classes used in</span></span>        | [<span data-ttu-id="116b8-230">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="116b8-230">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="116b8-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="116b8-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="116b8-232">進入</span><span class="sxs-lookup"><span data-stu-id="116b8-232">Entry</span></span> | <span data-ttu-id="116b8-233">值</span><span class="sxs-lookup"><span data-stu-id="116b8-233">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="116b8-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="116b8-234">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="116b8-235">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="116b8-236">System-Only</span></span>            | <span data-ttu-id="116b8-237">否</span><span class="sxs-lookup"><span data-stu-id="116b8-237">False</span></span>                                                     |
| <span data-ttu-id="116b8-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="116b8-238">Is-Single-Valued</span></span>       | <span data-ttu-id="116b8-239">對</span><span class="sxs-lookup"><span data-stu-id="116b8-239">True</span></span>                                                      |
| <span data-ttu-id="116b8-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="116b8-240">Is Indexed</span></span>             | <span data-ttu-id="116b8-241">否</span><span class="sxs-lookup"><span data-stu-id="116b8-241">False</span></span>                                                     |
| <span data-ttu-id="116b8-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="116b8-242">In Global Catalog</span></span>      | <span data-ttu-id="116b8-243">否</span><span class="sxs-lookup"><span data-stu-id="116b8-243">False</span></span>                                                     |
| <span data-ttu-id="116b8-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="116b8-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="116b8-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="116b8-245">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="116b8-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="116b8-246">Range-Lower</span></span>            | <span data-ttu-id="116b8-247">0</span><span class="sxs-lookup"><span data-stu-id="116b8-247">0</span></span>                                                         |
| <span data-ttu-id="116b8-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="116b8-248">Range-Upper</span></span>            | <span data-ttu-id="116b8-249">2048</span><span class="sxs-lookup"><span data-stu-id="116b8-249">2048</span></span>                                                      |
| <span data-ttu-id="116b8-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-250">Search-Flags</span></span>           | <span data-ttu-id="116b8-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="116b8-251">0x00000000</span></span>                                                |
| <span data-ttu-id="116b8-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-252">System-Flags</span></span>           | <span data-ttu-id="116b8-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="116b8-253">0x00000010</span></span>                                                |
| <span data-ttu-id="116b8-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="116b8-254">Classes used in</span></span>        | [<span data-ttu-id="116b8-255">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="116b8-255">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="116b8-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="116b8-256">Windows Server 2012</span></span>



| <span data-ttu-id="116b8-257">進入</span><span class="sxs-lookup"><span data-stu-id="116b8-257">Entry</span></span> | <span data-ttu-id="116b8-258">值</span><span class="sxs-lookup"><span data-stu-id="116b8-258">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="116b8-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="116b8-259">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="116b8-260">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="116b8-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="116b8-261">System-Only</span></span>            | <span data-ttu-id="116b8-262">否</span><span class="sxs-lookup"><span data-stu-id="116b8-262">False</span></span>                                                     |
| <span data-ttu-id="116b8-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="116b8-263">Is-Single-Valued</span></span>       | <span data-ttu-id="116b8-264">對</span><span class="sxs-lookup"><span data-stu-id="116b8-264">True</span></span>                                                      |
| <span data-ttu-id="116b8-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="116b8-265">Is Indexed</span></span>             | <span data-ttu-id="116b8-266">否</span><span class="sxs-lookup"><span data-stu-id="116b8-266">False</span></span>                                                     |
| <span data-ttu-id="116b8-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="116b8-267">In Global Catalog</span></span>      | <span data-ttu-id="116b8-268">否</span><span class="sxs-lookup"><span data-stu-id="116b8-268">False</span></span>                                                     |
| <span data-ttu-id="116b8-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="116b8-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="116b8-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="116b8-270">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="116b8-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="116b8-271">Range-Lower</span></span>            | <span data-ttu-id="116b8-272">0</span><span class="sxs-lookup"><span data-stu-id="116b8-272">0</span></span>                                                         |
| <span data-ttu-id="116b8-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="116b8-273">Range-Upper</span></span>            | <span data-ttu-id="116b8-274">2048</span><span class="sxs-lookup"><span data-stu-id="116b8-274">2048</span></span>                                                      |
| <span data-ttu-id="116b8-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-275">Search-Flags</span></span>           | <span data-ttu-id="116b8-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="116b8-276">0x00000000</span></span>                                                |
| <span data-ttu-id="116b8-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="116b8-277">System-Flags</span></span>           | <span data-ttu-id="116b8-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="116b8-278">0x00000010</span></span>                                                |
| <span data-ttu-id="116b8-279">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="116b8-279">Classes used in</span></span>        | [<span data-ttu-id="116b8-280">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="116b8-280">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 






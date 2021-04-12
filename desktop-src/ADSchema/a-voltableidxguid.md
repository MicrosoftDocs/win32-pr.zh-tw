---
title: Vol-資料表-Idx-GUID 屬性
description: 連結追蹤磁片區資料表專案的索引識別碼。
ms.assetid: f6df4ff1-87aa-480e-90f5-0a47822cd461
ms.tgt_platform: multiple
keywords:
- Vol-資料表-Idx-GUID 屬性 AD 架構
- volTableIdxGUID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Vol-Table-Idx-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a760d99b6883ea070e2f06daf11227056ea74a08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509648"
---
# <a name="vol-table-idx-guid-attribute"></a><span data-ttu-id="38dcd-105">Vol-資料表-Idx-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="38dcd-105">Vol-Table-Idx-GUID attribute</span></span>

<span data-ttu-id="38dcd-106">連結追蹤磁片區資料表專案的索引識別碼。</span><span class="sxs-lookup"><span data-stu-id="38dcd-106">The index identifier for a Link-Track-Volume table entry.</span></span>



| <span data-ttu-id="38dcd-107">進入</span><span class="sxs-lookup"><span data-stu-id="38dcd-107">Entry</span></span> | <span data-ttu-id="38dcd-108">值</span><span class="sxs-lookup"><span data-stu-id="38dcd-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="38dcd-109">CN</span><span class="sxs-lookup"><span data-stu-id="38dcd-109">CN</span></span>                | <span data-ttu-id="38dcd-110">Vol-資料表-Idx-GUID</span><span class="sxs-lookup"><span data-stu-id="38dcd-110">Vol-Table-Idx-GUID</span></span>                                    |
| <span data-ttu-id="38dcd-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="38dcd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="38dcd-112">volTableIdxGUID</span><span class="sxs-lookup"><span data-stu-id="38dcd-112">volTableIdxGUID</span></span>                                       |
| <span data-ttu-id="38dcd-113">大小</span><span class="sxs-lookup"><span data-stu-id="38dcd-113">Size</span></span>              | <span data-ttu-id="38dcd-114">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="38dcd-114">16 bytes</span></span>                                              |
| <span data-ttu-id="38dcd-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="38dcd-115">Update Privilege</span></span>  | <span data-ttu-id="38dcd-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="38dcd-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="38dcd-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="38dcd-117">Update Frequency</span></span>  | <span data-ttu-id="38dcd-118">只要建立新的檔案連結。</span><span class="sxs-lookup"><span data-stu-id="38dcd-118">Whenever a new link to a file is created.</span></span>             |
| <span data-ttu-id="38dcd-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38dcd-119">Attribute-Id</span></span>      | <span data-ttu-id="38dcd-120">1.2.840.113556.1.4.334</span><span class="sxs-lookup"><span data-stu-id="38dcd-120">1.2.840.113556.1.4.334</span></span>                                |
| <span data-ttu-id="38dcd-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="38dcd-121">System-Id-Guid</span></span>    | <span data-ttu-id="38dcd-122">1f0075fb-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="38dcd-122">1f0075fb-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="38dcd-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="38dcd-123">Syntax</span></span>            | [<span data-ttu-id="38dcd-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="38dcd-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="38dcd-125">實作</span><span class="sxs-lookup"><span data-stu-id="38dcd-125">Implementations</span></span>

-   [<span data-ttu-id="38dcd-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="38dcd-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="38dcd-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38dcd-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38dcd-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38dcd-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38dcd-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38dcd-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38dcd-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38dcd-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38dcd-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38dcd-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="38dcd-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38dcd-132">Windows 2000 Server</span></span>



| <span data-ttu-id="38dcd-133">進入</span><span class="sxs-lookup"><span data-stu-id="38dcd-133">Entry</span></span> | <span data-ttu-id="38dcd-134">值</span><span class="sxs-lookup"><span data-stu-id="38dcd-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="38dcd-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38dcd-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38dcd-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="38dcd-137">System-Only</span></span>            | <span data-ttu-id="38dcd-138">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-138">False</span></span>                                                          |
| <span data-ttu-id="38dcd-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38dcd-139">Is-Single-Valued</span></span>       | <span data-ttu-id="38dcd-140">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-140">True</span></span>                                                           |
| <span data-ttu-id="38dcd-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38dcd-141">Is Indexed</span></span>             | <span data-ttu-id="38dcd-142">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-142">True</span></span>                                                           |
| <span data-ttu-id="38dcd-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38dcd-143">In Global Catalog</span></span>      | <span data-ttu-id="38dcd-144">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-144">False</span></span>                                                          |
| <span data-ttu-id="38dcd-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38dcd-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="38dcd-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38dcd-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="38dcd-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38dcd-147">Range-Lower</span></span>            | <span data-ttu-id="38dcd-148">0</span><span class="sxs-lookup"><span data-stu-id="38dcd-148">0</span></span>                                                              |
| <span data-ttu-id="38dcd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38dcd-149">Range-Upper</span></span>            | <span data-ttu-id="38dcd-150">16</span><span class="sxs-lookup"><span data-stu-id="38dcd-150">16</span></span>                                                             |
| <span data-ttu-id="38dcd-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-151">Search-Flags</span></span>           | <span data-ttu-id="38dcd-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38dcd-152">0x00000001</span></span>                                                     |
| <span data-ttu-id="38dcd-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-153">System-Flags</span></span>           | <span data-ttu-id="38dcd-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38dcd-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="38dcd-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38dcd-155">Classes used in</span></span>        | [<span data-ttu-id="38dcd-156">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="38dcd-156">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="38dcd-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38dcd-157">Windows Server 2003</span></span>



| <span data-ttu-id="38dcd-158">進入</span><span class="sxs-lookup"><span data-stu-id="38dcd-158">Entry</span></span> | <span data-ttu-id="38dcd-159">值</span><span class="sxs-lookup"><span data-stu-id="38dcd-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="38dcd-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38dcd-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38dcd-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="38dcd-162">System-Only</span></span>            | <span data-ttu-id="38dcd-163">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-163">False</span></span>                                                          |
| <span data-ttu-id="38dcd-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38dcd-164">Is-Single-Valued</span></span>       | <span data-ttu-id="38dcd-165">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-165">True</span></span>                                                           |
| <span data-ttu-id="38dcd-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38dcd-166">Is Indexed</span></span>             | <span data-ttu-id="38dcd-167">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-167">True</span></span>                                                           |
| <span data-ttu-id="38dcd-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38dcd-168">In Global Catalog</span></span>      | <span data-ttu-id="38dcd-169">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-169">False</span></span>                                                          |
| <span data-ttu-id="38dcd-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38dcd-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="38dcd-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38dcd-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="38dcd-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38dcd-172">Range-Lower</span></span>            | <span data-ttu-id="38dcd-173">0</span><span class="sxs-lookup"><span data-stu-id="38dcd-173">0</span></span>                                                              |
| <span data-ttu-id="38dcd-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38dcd-174">Range-Upper</span></span>            | <span data-ttu-id="38dcd-175">16</span><span class="sxs-lookup"><span data-stu-id="38dcd-175">16</span></span>                                                             |
| <span data-ttu-id="38dcd-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-176">Search-Flags</span></span>           | <span data-ttu-id="38dcd-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38dcd-177">0x00000001</span></span>                                                     |
| <span data-ttu-id="38dcd-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-178">System-Flags</span></span>           | <span data-ttu-id="38dcd-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38dcd-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="38dcd-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38dcd-180">Classes used in</span></span>        | [<span data-ttu-id="38dcd-181">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="38dcd-181">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38dcd-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38dcd-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38dcd-183">進入</span><span class="sxs-lookup"><span data-stu-id="38dcd-183">Entry</span></span> | <span data-ttu-id="38dcd-184">值</span><span class="sxs-lookup"><span data-stu-id="38dcd-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="38dcd-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38dcd-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38dcd-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="38dcd-187">System-Only</span></span>            | <span data-ttu-id="38dcd-188">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-188">False</span></span>                                                          |
| <span data-ttu-id="38dcd-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38dcd-189">Is-Single-Valued</span></span>       | <span data-ttu-id="38dcd-190">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-190">True</span></span>                                                           |
| <span data-ttu-id="38dcd-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38dcd-191">Is Indexed</span></span>             | <span data-ttu-id="38dcd-192">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-192">True</span></span>                                                           |
| <span data-ttu-id="38dcd-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38dcd-193">In Global Catalog</span></span>      | <span data-ttu-id="38dcd-194">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-194">False</span></span>                                                          |
| <span data-ttu-id="38dcd-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38dcd-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="38dcd-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38dcd-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="38dcd-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38dcd-197">Range-Lower</span></span>            | <span data-ttu-id="38dcd-198">0</span><span class="sxs-lookup"><span data-stu-id="38dcd-198">0</span></span>                                                              |
| <span data-ttu-id="38dcd-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38dcd-199">Range-Upper</span></span>            | <span data-ttu-id="38dcd-200">16</span><span class="sxs-lookup"><span data-stu-id="38dcd-200">16</span></span>                                                             |
| <span data-ttu-id="38dcd-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-201">Search-Flags</span></span>           | <span data-ttu-id="38dcd-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38dcd-202">0x00000001</span></span>                                                     |
| <span data-ttu-id="38dcd-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-203">System-Flags</span></span>           | <span data-ttu-id="38dcd-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38dcd-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="38dcd-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38dcd-205">Classes used in</span></span>        | [<span data-ttu-id="38dcd-206">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="38dcd-206">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38dcd-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38dcd-207">Windows Server 2008</span></span>



| <span data-ttu-id="38dcd-208">進入</span><span class="sxs-lookup"><span data-stu-id="38dcd-208">Entry</span></span> | <span data-ttu-id="38dcd-209">值</span><span class="sxs-lookup"><span data-stu-id="38dcd-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="38dcd-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38dcd-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38dcd-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="38dcd-212">System-Only</span></span>            | <span data-ttu-id="38dcd-213">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-213">False</span></span>                                                          |
| <span data-ttu-id="38dcd-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38dcd-214">Is-Single-Valued</span></span>       | <span data-ttu-id="38dcd-215">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-215">True</span></span>                                                           |
| <span data-ttu-id="38dcd-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38dcd-216">Is Indexed</span></span>             | <span data-ttu-id="38dcd-217">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-217">True</span></span>                                                           |
| <span data-ttu-id="38dcd-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38dcd-218">In Global Catalog</span></span>      | <span data-ttu-id="38dcd-219">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-219">False</span></span>                                                          |
| <span data-ttu-id="38dcd-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38dcd-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="38dcd-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38dcd-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="38dcd-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38dcd-222">Range-Lower</span></span>            | <span data-ttu-id="38dcd-223">0</span><span class="sxs-lookup"><span data-stu-id="38dcd-223">0</span></span>                                                              |
| <span data-ttu-id="38dcd-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38dcd-224">Range-Upper</span></span>            | <span data-ttu-id="38dcd-225">16</span><span class="sxs-lookup"><span data-stu-id="38dcd-225">16</span></span>                                                             |
| <span data-ttu-id="38dcd-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-226">Search-Flags</span></span>           | <span data-ttu-id="38dcd-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38dcd-227">0x00000001</span></span>                                                     |
| <span data-ttu-id="38dcd-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-228">System-Flags</span></span>           | <span data-ttu-id="38dcd-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38dcd-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="38dcd-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38dcd-230">Classes used in</span></span>        | [<span data-ttu-id="38dcd-231">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="38dcd-231">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38dcd-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38dcd-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38dcd-233">進入</span><span class="sxs-lookup"><span data-stu-id="38dcd-233">Entry</span></span> | <span data-ttu-id="38dcd-234">值</span><span class="sxs-lookup"><span data-stu-id="38dcd-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="38dcd-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38dcd-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38dcd-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="38dcd-237">System-Only</span></span>            | <span data-ttu-id="38dcd-238">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-238">False</span></span>                                                          |
| <span data-ttu-id="38dcd-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38dcd-239">Is-Single-Valued</span></span>       | <span data-ttu-id="38dcd-240">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-240">True</span></span>                                                           |
| <span data-ttu-id="38dcd-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38dcd-241">Is Indexed</span></span>             | <span data-ttu-id="38dcd-242">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-242">True</span></span>                                                           |
| <span data-ttu-id="38dcd-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38dcd-243">In Global Catalog</span></span>      | <span data-ttu-id="38dcd-244">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-244">False</span></span>                                                          |
| <span data-ttu-id="38dcd-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38dcd-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="38dcd-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38dcd-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="38dcd-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38dcd-247">Range-Lower</span></span>            | <span data-ttu-id="38dcd-248">0</span><span class="sxs-lookup"><span data-stu-id="38dcd-248">0</span></span>                                                              |
| <span data-ttu-id="38dcd-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38dcd-249">Range-Upper</span></span>            | <span data-ttu-id="38dcd-250">16</span><span class="sxs-lookup"><span data-stu-id="38dcd-250">16</span></span>                                                             |
| <span data-ttu-id="38dcd-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-251">Search-Flags</span></span>           | <span data-ttu-id="38dcd-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38dcd-252">0x00000001</span></span>                                                     |
| <span data-ttu-id="38dcd-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-253">System-Flags</span></span>           | <span data-ttu-id="38dcd-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38dcd-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="38dcd-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38dcd-255">Classes used in</span></span>        | [<span data-ttu-id="38dcd-256">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="38dcd-256">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38dcd-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38dcd-257">Windows Server 2012</span></span>



| <span data-ttu-id="38dcd-258">進入</span><span class="sxs-lookup"><span data-stu-id="38dcd-258">Entry</span></span> | <span data-ttu-id="38dcd-259">值</span><span class="sxs-lookup"><span data-stu-id="38dcd-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="38dcd-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38dcd-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38dcd-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="38dcd-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="38dcd-262">System-Only</span></span>            | <span data-ttu-id="38dcd-263">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-263">False</span></span>                                                          |
| <span data-ttu-id="38dcd-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38dcd-264">Is-Single-Valued</span></span>       | <span data-ttu-id="38dcd-265">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-265">True</span></span>                                                           |
| <span data-ttu-id="38dcd-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38dcd-266">Is Indexed</span></span>             | <span data-ttu-id="38dcd-267">對</span><span class="sxs-lookup"><span data-stu-id="38dcd-267">True</span></span>                                                           |
| <span data-ttu-id="38dcd-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38dcd-268">In Global Catalog</span></span>      | <span data-ttu-id="38dcd-269">否</span><span class="sxs-lookup"><span data-stu-id="38dcd-269">False</span></span>                                                          |
| <span data-ttu-id="38dcd-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38dcd-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="38dcd-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38dcd-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="38dcd-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38dcd-272">Range-Lower</span></span>            | <span data-ttu-id="38dcd-273">0</span><span class="sxs-lookup"><span data-stu-id="38dcd-273">0</span></span>                                                              |
| <span data-ttu-id="38dcd-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38dcd-274">Range-Upper</span></span>            | <span data-ttu-id="38dcd-275">16</span><span class="sxs-lookup"><span data-stu-id="38dcd-275">16</span></span>                                                             |
| <span data-ttu-id="38dcd-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-276">Search-Flags</span></span>           | <span data-ttu-id="38dcd-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38dcd-277">0x00000001</span></span>                                                     |
| <span data-ttu-id="38dcd-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38dcd-278">System-Flags</span></span>           | <span data-ttu-id="38dcd-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38dcd-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="38dcd-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38dcd-280">Classes used in</span></span>        | [<span data-ttu-id="38dcd-281">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="38dcd-281">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 






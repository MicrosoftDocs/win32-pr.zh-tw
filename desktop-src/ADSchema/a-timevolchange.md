---
title: 時間-音量-變更屬性
description: 這個屬性工作表示上次變更遠端存放裝置磁片區中檔案的時間。
ms.assetid: e0a985fb-1b50-457e-80db-e71ab5570c51
ms.tgt_platform: multiple
keywords:
- 時間-音量-變更屬性 AD 架構
- timeVolChange 屬性 AD 架構
topic_type:
- apiref
api_name:
- Time-Vol-Change
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315715996e685949f35f7088fff5368b95c5ba54
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844904"
---
# <a name="time-vol-change-attribute"></a><span data-ttu-id="84452-105">時間-音量-變更屬性</span><span class="sxs-lookup"><span data-stu-id="84452-105">Time-Vol-Change attribute</span></span>

<span data-ttu-id="84452-106">這個屬性工作表示上次變更遠端存放裝置磁片區中檔案的時間。</span><span class="sxs-lookup"><span data-stu-id="84452-106">This attribute indicates the last time that a file in the remote storage volume was changed.</span></span>



| <span data-ttu-id="84452-107">進入</span><span class="sxs-lookup"><span data-stu-id="84452-107">Entry</span></span> | <span data-ttu-id="84452-108">值</span><span class="sxs-lookup"><span data-stu-id="84452-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="84452-109">CN</span><span class="sxs-lookup"><span data-stu-id="84452-109">CN</span></span>                | <span data-ttu-id="84452-110">時間-音量-變更</span><span class="sxs-lookup"><span data-stu-id="84452-110">Time-Vol-Change</span></span>                      |
| <span data-ttu-id="84452-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="84452-111">Ldap-Display-Name</span></span> | <span data-ttu-id="84452-112">timeVolChange</span><span class="sxs-lookup"><span data-stu-id="84452-112">timeVolChange</span></span>                        |
| <span data-ttu-id="84452-113">大小</span><span class="sxs-lookup"><span data-stu-id="84452-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="84452-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="84452-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="84452-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="84452-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="84452-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="84452-116">Attribute-Id</span></span>      | <span data-ttu-id="84452-117">1.2.840.113556.1.4.502</span><span class="sxs-lookup"><span data-stu-id="84452-117">1.2.840.113556.1.4.502</span></span>               |
| <span data-ttu-id="84452-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="84452-118">System-Id-Guid</span></span>    | <span data-ttu-id="84452-119">ddac0cf0-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="84452-119">ddac0cf0-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="84452-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="84452-120">Syntax</span></span>            | [<span data-ttu-id="84452-121">**間隔**</span><span class="sxs-lookup"><span data-stu-id="84452-121">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="84452-122">實作</span><span class="sxs-lookup"><span data-stu-id="84452-122">Implementations</span></span>

-   [<span data-ttu-id="84452-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="84452-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="84452-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="84452-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="84452-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="84452-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="84452-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="84452-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="84452-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="84452-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="84452-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="84452-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="84452-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="84452-129">Windows 2000 Server</span></span>



| <span data-ttu-id="84452-130">進入</span><span class="sxs-lookup"><span data-stu-id="84452-130">Entry</span></span> | <span data-ttu-id="84452-131">值</span><span class="sxs-lookup"><span data-stu-id="84452-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="84452-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84452-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84452-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="84452-134">System-Only</span></span>            | <span data-ttu-id="84452-135">否</span><span class="sxs-lookup"><span data-stu-id="84452-135">False</span></span>                                                          |
| <span data-ttu-id="84452-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84452-136">Is-Single-Valued</span></span>       | <span data-ttu-id="84452-137">對</span><span class="sxs-lookup"><span data-stu-id="84452-137">True</span></span>                                                           |
| <span data-ttu-id="84452-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84452-138">Is Indexed</span></span>             | <span data-ttu-id="84452-139">對</span><span class="sxs-lookup"><span data-stu-id="84452-139">True</span></span>                                                           |
| <span data-ttu-id="84452-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84452-140">In Global Catalog</span></span>      | <span data-ttu-id="84452-141">否</span><span class="sxs-lookup"><span data-stu-id="84452-141">False</span></span>                                                          |
| <span data-ttu-id="84452-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84452-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="84452-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84452-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="84452-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84452-144">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="84452-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84452-145">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="84452-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-146">Search-Flags</span></span>           | <span data-ttu-id="84452-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="84452-147">0x00000001</span></span>                                                     |
| <span data-ttu-id="84452-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-148">System-Flags</span></span>           | <span data-ttu-id="84452-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84452-149">0x00000010</span></span>                                                     |
| <span data-ttu-id="84452-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84452-150">Classes used in</span></span>        | [<span data-ttu-id="84452-151">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="84452-151">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="84452-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="84452-152">Windows Server 2003</span></span>



| <span data-ttu-id="84452-153">進入</span><span class="sxs-lookup"><span data-stu-id="84452-153">Entry</span></span> | <span data-ttu-id="84452-154">值</span><span class="sxs-lookup"><span data-stu-id="84452-154">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="84452-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84452-155">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84452-156">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="84452-157">System-Only</span></span>            | <span data-ttu-id="84452-158">否</span><span class="sxs-lookup"><span data-stu-id="84452-158">False</span></span>                                                          |
| <span data-ttu-id="84452-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84452-159">Is-Single-Valued</span></span>       | <span data-ttu-id="84452-160">對</span><span class="sxs-lookup"><span data-stu-id="84452-160">True</span></span>                                                           |
| <span data-ttu-id="84452-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84452-161">Is Indexed</span></span>             | <span data-ttu-id="84452-162">對</span><span class="sxs-lookup"><span data-stu-id="84452-162">True</span></span>                                                           |
| <span data-ttu-id="84452-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84452-163">In Global Catalog</span></span>      | <span data-ttu-id="84452-164">否</span><span class="sxs-lookup"><span data-stu-id="84452-164">False</span></span>                                                          |
| <span data-ttu-id="84452-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84452-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="84452-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84452-166">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="84452-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84452-167">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="84452-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84452-168">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="84452-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-169">Search-Flags</span></span>           | <span data-ttu-id="84452-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="84452-170">0x00000001</span></span>                                                     |
| <span data-ttu-id="84452-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-171">System-Flags</span></span>           | <span data-ttu-id="84452-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84452-172">0x00000010</span></span>                                                     |
| <span data-ttu-id="84452-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84452-173">Classes used in</span></span>        | [<span data-ttu-id="84452-174">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="84452-174">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="84452-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="84452-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="84452-176">進入</span><span class="sxs-lookup"><span data-stu-id="84452-176">Entry</span></span> | <span data-ttu-id="84452-177">值</span><span class="sxs-lookup"><span data-stu-id="84452-177">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="84452-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84452-178">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84452-179">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="84452-180">System-Only</span></span>            | <span data-ttu-id="84452-181">否</span><span class="sxs-lookup"><span data-stu-id="84452-181">False</span></span>                                                          |
| <span data-ttu-id="84452-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84452-182">Is-Single-Valued</span></span>       | <span data-ttu-id="84452-183">對</span><span class="sxs-lookup"><span data-stu-id="84452-183">True</span></span>                                                           |
| <span data-ttu-id="84452-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84452-184">Is Indexed</span></span>             | <span data-ttu-id="84452-185">對</span><span class="sxs-lookup"><span data-stu-id="84452-185">True</span></span>                                                           |
| <span data-ttu-id="84452-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84452-186">In Global Catalog</span></span>      | <span data-ttu-id="84452-187">否</span><span class="sxs-lookup"><span data-stu-id="84452-187">False</span></span>                                                          |
| <span data-ttu-id="84452-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84452-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="84452-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84452-189">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="84452-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84452-190">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="84452-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84452-191">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="84452-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-192">Search-Flags</span></span>           | <span data-ttu-id="84452-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="84452-193">0x00000001</span></span>                                                     |
| <span data-ttu-id="84452-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-194">System-Flags</span></span>           | <span data-ttu-id="84452-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84452-195">0x00000010</span></span>                                                     |
| <span data-ttu-id="84452-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84452-196">Classes used in</span></span>        | [<span data-ttu-id="84452-197">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="84452-197">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="84452-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84452-198">Windows Server 2008</span></span>



| <span data-ttu-id="84452-199">進入</span><span class="sxs-lookup"><span data-stu-id="84452-199">Entry</span></span> | <span data-ttu-id="84452-200">值</span><span class="sxs-lookup"><span data-stu-id="84452-200">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="84452-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84452-201">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84452-202">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="84452-203">System-Only</span></span>            | <span data-ttu-id="84452-204">否</span><span class="sxs-lookup"><span data-stu-id="84452-204">False</span></span>                                                          |
| <span data-ttu-id="84452-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84452-205">Is-Single-Valued</span></span>       | <span data-ttu-id="84452-206">對</span><span class="sxs-lookup"><span data-stu-id="84452-206">True</span></span>                                                           |
| <span data-ttu-id="84452-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84452-207">Is Indexed</span></span>             | <span data-ttu-id="84452-208">對</span><span class="sxs-lookup"><span data-stu-id="84452-208">True</span></span>                                                           |
| <span data-ttu-id="84452-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84452-209">In Global Catalog</span></span>      | <span data-ttu-id="84452-210">否</span><span class="sxs-lookup"><span data-stu-id="84452-210">False</span></span>                                                          |
| <span data-ttu-id="84452-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84452-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="84452-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84452-212">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="84452-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84452-213">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="84452-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84452-214">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="84452-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-215">Search-Flags</span></span>           | <span data-ttu-id="84452-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="84452-216">0x00000001</span></span>                                                     |
| <span data-ttu-id="84452-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-217">System-Flags</span></span>           | <span data-ttu-id="84452-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84452-218">0x00000010</span></span>                                                     |
| <span data-ttu-id="84452-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84452-219">Classes used in</span></span>        | [<span data-ttu-id="84452-220">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="84452-220">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="84452-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84452-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="84452-222">進入</span><span class="sxs-lookup"><span data-stu-id="84452-222">Entry</span></span> | <span data-ttu-id="84452-223">值</span><span class="sxs-lookup"><span data-stu-id="84452-223">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="84452-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84452-224">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84452-225">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="84452-226">System-Only</span></span>            | <span data-ttu-id="84452-227">否</span><span class="sxs-lookup"><span data-stu-id="84452-227">False</span></span>                                                          |
| <span data-ttu-id="84452-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84452-228">Is-Single-Valued</span></span>       | <span data-ttu-id="84452-229">對</span><span class="sxs-lookup"><span data-stu-id="84452-229">True</span></span>                                                           |
| <span data-ttu-id="84452-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84452-230">Is Indexed</span></span>             | <span data-ttu-id="84452-231">對</span><span class="sxs-lookup"><span data-stu-id="84452-231">True</span></span>                                                           |
| <span data-ttu-id="84452-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84452-232">In Global Catalog</span></span>      | <span data-ttu-id="84452-233">否</span><span class="sxs-lookup"><span data-stu-id="84452-233">False</span></span>                                                          |
| <span data-ttu-id="84452-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84452-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="84452-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84452-235">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="84452-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84452-236">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="84452-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84452-237">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="84452-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-238">Search-Flags</span></span>           | <span data-ttu-id="84452-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="84452-239">0x00000001</span></span>                                                     |
| <span data-ttu-id="84452-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-240">System-Flags</span></span>           | <span data-ttu-id="84452-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84452-241">0x00000010</span></span>                                                     |
| <span data-ttu-id="84452-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84452-242">Classes used in</span></span>        | [<span data-ttu-id="84452-243">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="84452-243">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="84452-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84452-244">Windows Server 2012</span></span>



| <span data-ttu-id="84452-245">進入</span><span class="sxs-lookup"><span data-stu-id="84452-245">Entry</span></span> | <span data-ttu-id="84452-246">值</span><span class="sxs-lookup"><span data-stu-id="84452-246">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="84452-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84452-247">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84452-248">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="84452-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="84452-249">System-Only</span></span>            | <span data-ttu-id="84452-250">否</span><span class="sxs-lookup"><span data-stu-id="84452-250">False</span></span>                                                          |
| <span data-ttu-id="84452-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84452-251">Is-Single-Valued</span></span>       | <span data-ttu-id="84452-252">對</span><span class="sxs-lookup"><span data-stu-id="84452-252">True</span></span>                                                           |
| <span data-ttu-id="84452-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84452-253">Is Indexed</span></span>             | <span data-ttu-id="84452-254">對</span><span class="sxs-lookup"><span data-stu-id="84452-254">True</span></span>                                                           |
| <span data-ttu-id="84452-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84452-255">In Global Catalog</span></span>      | <span data-ttu-id="84452-256">否</span><span class="sxs-lookup"><span data-stu-id="84452-256">False</span></span>                                                          |
| <span data-ttu-id="84452-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84452-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="84452-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84452-258">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="84452-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84452-259">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="84452-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84452-260">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="84452-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-261">Search-Flags</span></span>           | <span data-ttu-id="84452-262">0x00000001</span><span class="sxs-lookup"><span data-stu-id="84452-262">0x00000001</span></span>                                                     |
| <span data-ttu-id="84452-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84452-263">System-Flags</span></span>           | <span data-ttu-id="84452-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84452-264">0x00000010</span></span>                                                     |
| <span data-ttu-id="84452-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84452-265">Classes used in</span></span>        | [<span data-ttu-id="84452-266">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="84452-266">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 






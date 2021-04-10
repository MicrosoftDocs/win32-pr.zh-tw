---
title: 上次備份-還原時間屬性
description: 上次發生系統還原的時間。
ms.assetid: 44850c16-3f17-4883-9a54-3e82ca7d63da
ms.tgt_platform: multiple
keywords:
- 上次備份-還原時間屬性 AD 架構
- lastBackupRestorationTime 屬性 AD 架構
topic_type:
- apiref
api_name:
- Last-Backup-Restoration-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9220d06a4cdd562599611d2ad19cf09fa279ef3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104025524"
---
# <a name="last-backup-restoration-time-attribute"></a><span data-ttu-id="2dc7a-105">上次備份-還原時間屬性</span><span class="sxs-lookup"><span data-stu-id="2dc7a-105">Last-Backup-Restoration-Time attribute</span></span>

<span data-ttu-id="2dc7a-106">上次發生系統還原的時間。</span><span class="sxs-lookup"><span data-stu-id="2dc7a-106">When the last system restore occurred.</span></span>



| <span data-ttu-id="2dc7a-107">進入</span><span class="sxs-lookup"><span data-stu-id="2dc7a-107">Entry</span></span> | <span data-ttu-id="2dc7a-108">值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2dc7a-109">CN</span><span class="sxs-lookup"><span data-stu-id="2dc7a-109">CN</span></span>                | <span data-ttu-id="2dc7a-110">上次備份-還原時間</span><span class="sxs-lookup"><span data-stu-id="2dc7a-110">Last-Backup-Restoration-Time</span></span>         |
| <span data-ttu-id="2dc7a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2dc7a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2dc7a-112">lastBackupRestorationTime</span><span class="sxs-lookup"><span data-stu-id="2dc7a-112">lastBackupRestorationTime</span></span>            |
| <span data-ttu-id="2dc7a-113">大小</span><span class="sxs-lookup"><span data-stu-id="2dc7a-113">Size</span></span>              | <span data-ttu-id="2dc7a-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="2dc7a-114">8 bytes</span></span>                              |
| <span data-ttu-id="2dc7a-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2dc7a-115">Update Privilege</span></span>  | <span data-ttu-id="2dc7a-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="2dc7a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="2dc7a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2dc7a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2dc7a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2dc7a-118">Attribute-Id</span></span>      | <span data-ttu-id="2dc7a-119">1.2.840.113556.1.4.519</span><span class="sxs-lookup"><span data-stu-id="2dc7a-119">1.2.840.113556.1.4.519</span></span>               |
| <span data-ttu-id="2dc7a-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2dc7a-120">System-Id-Guid</span></span>    | <span data-ttu-id="2dc7a-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2dc7a-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span></span> |
| <span data-ttu-id="2dc7a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dc7a-122">Syntax</span></span>            | [<span data-ttu-id="2dc7a-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2dc7a-124">實作</span><span class="sxs-lookup"><span data-stu-id="2dc7a-124">Implementations</span></span>

-   [<span data-ttu-id="2dc7a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2dc7a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2dc7a-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2dc7a-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2dc7a-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2dc7a-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2dc7a-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2dc7a-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2dc7a-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2dc7a-133">進入</span><span class="sxs-lookup"><span data-stu-id="2dc7a-133">Entry</span></span> | <span data-ttu-id="2dc7a-134">值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2dc7a-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2dc7a-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2dc7a-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="2dc7a-137">System-Only</span></span>            | <span data-ttu-id="2dc7a-138">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-138">False</span></span>                                    |
| <span data-ttu-id="2dc7a-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="2dc7a-140">對</span><span class="sxs-lookup"><span data-stu-id="2dc7a-140">True</span></span>                                     |
| <span data-ttu-id="2dc7a-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2dc7a-141">Is Indexed</span></span>             | <span data-ttu-id="2dc7a-142">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-142">False</span></span>                                    |
| <span data-ttu-id="2dc7a-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2dc7a-143">In Global Catalog</span></span>      | <span data-ttu-id="2dc7a-144">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-144">False</span></span>                                    |
| <span data-ttu-id="2dc7a-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2dc7a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="2dc7a-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2dc7a-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2dc7a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2dc7a-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2dc7a-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-149">Search-Flags</span></span>           | <span data-ttu-id="2dc7a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2dc7a-150">0x00000000</span></span>                               |
| <span data-ttu-id="2dc7a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-151">System-Flags</span></span>           | <span data-ttu-id="2dc7a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2dc7a-152">0x00000010</span></span>                               |
| <span data-ttu-id="2dc7a-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2dc7a-153">Classes used in</span></span>        | [<span data-ttu-id="2dc7a-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2dc7a-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2dc7a-155">Windows Server 2003</span></span>



| <span data-ttu-id="2dc7a-156">進入</span><span class="sxs-lookup"><span data-stu-id="2dc7a-156">Entry</span></span> | <span data-ttu-id="2dc7a-157">值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2dc7a-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2dc7a-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2dc7a-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="2dc7a-160">System-Only</span></span>            | <span data-ttu-id="2dc7a-161">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-161">False</span></span>                                    |
| <span data-ttu-id="2dc7a-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="2dc7a-163">對</span><span class="sxs-lookup"><span data-stu-id="2dc7a-163">True</span></span>                                     |
| <span data-ttu-id="2dc7a-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2dc7a-164">Is Indexed</span></span>             | <span data-ttu-id="2dc7a-165">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-165">False</span></span>                                    |
| <span data-ttu-id="2dc7a-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2dc7a-166">In Global Catalog</span></span>      | <span data-ttu-id="2dc7a-167">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-167">False</span></span>                                    |
| <span data-ttu-id="2dc7a-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2dc7a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="2dc7a-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2dc7a-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2dc7a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2dc7a-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2dc7a-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-172">Search-Flags</span></span>           | <span data-ttu-id="2dc7a-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2dc7a-173">0x00000000</span></span>                               |
| <span data-ttu-id="2dc7a-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-174">System-Flags</span></span>           | <span data-ttu-id="2dc7a-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2dc7a-175">0x00000010</span></span>                               |
| <span data-ttu-id="2dc7a-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2dc7a-176">Classes used in</span></span>        | [<span data-ttu-id="2dc7a-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2dc7a-178">亞當</span><span class="sxs-lookup"><span data-stu-id="2dc7a-178">ADAM</span></span>



| <span data-ttu-id="2dc7a-179">進入</span><span class="sxs-lookup"><span data-stu-id="2dc7a-179">Entry</span></span> | <span data-ttu-id="2dc7a-180">值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2dc7a-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2dc7a-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2dc7a-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="2dc7a-183">System-Only</span></span>            | <span data-ttu-id="2dc7a-184">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-184">False</span></span>                                    |
| <span data-ttu-id="2dc7a-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-185">Is-Single-Valued</span></span>       | <span data-ttu-id="2dc7a-186">對</span><span class="sxs-lookup"><span data-stu-id="2dc7a-186">True</span></span>                                     |
| <span data-ttu-id="2dc7a-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2dc7a-187">Is Indexed</span></span>             | <span data-ttu-id="2dc7a-188">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-188">False</span></span>                                    |
| <span data-ttu-id="2dc7a-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2dc7a-189">In Global Catalog</span></span>      | <span data-ttu-id="2dc7a-190">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-190">False</span></span>                                    |
| <span data-ttu-id="2dc7a-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2dc7a-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="2dc7a-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2dc7a-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2dc7a-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2dc7a-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2dc7a-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-195">Search-Flags</span></span>           | <span data-ttu-id="2dc7a-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2dc7a-196">0x00000000</span></span>                               |
| <span data-ttu-id="2dc7a-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-197">System-Flags</span></span>           | <span data-ttu-id="2dc7a-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2dc7a-198">0x00000010</span></span>                               |
| <span data-ttu-id="2dc7a-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2dc7a-199">Classes used in</span></span>        | [<span data-ttu-id="2dc7a-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2dc7a-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2dc7a-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2dc7a-202">進入</span><span class="sxs-lookup"><span data-stu-id="2dc7a-202">Entry</span></span> | <span data-ttu-id="2dc7a-203">值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2dc7a-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2dc7a-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2dc7a-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="2dc7a-206">System-Only</span></span>            | <span data-ttu-id="2dc7a-207">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-207">False</span></span>                                    |
| <span data-ttu-id="2dc7a-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-208">Is-Single-Valued</span></span>       | <span data-ttu-id="2dc7a-209">對</span><span class="sxs-lookup"><span data-stu-id="2dc7a-209">True</span></span>                                     |
| <span data-ttu-id="2dc7a-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2dc7a-210">Is Indexed</span></span>             | <span data-ttu-id="2dc7a-211">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-211">False</span></span>                                    |
| <span data-ttu-id="2dc7a-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2dc7a-212">In Global Catalog</span></span>      | <span data-ttu-id="2dc7a-213">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-213">False</span></span>                                    |
| <span data-ttu-id="2dc7a-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2dc7a-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="2dc7a-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2dc7a-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2dc7a-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2dc7a-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2dc7a-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-218">Search-Flags</span></span>           | <span data-ttu-id="2dc7a-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2dc7a-219">0x00000000</span></span>                               |
| <span data-ttu-id="2dc7a-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-220">System-Flags</span></span>           | <span data-ttu-id="2dc7a-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2dc7a-221">0x00000010</span></span>                               |
| <span data-ttu-id="2dc7a-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2dc7a-222">Classes used in</span></span>        | [<span data-ttu-id="2dc7a-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2dc7a-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2dc7a-224">Windows Server 2008</span></span>



| <span data-ttu-id="2dc7a-225">進入</span><span class="sxs-lookup"><span data-stu-id="2dc7a-225">Entry</span></span> | <span data-ttu-id="2dc7a-226">值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2dc7a-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2dc7a-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2dc7a-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="2dc7a-229">System-Only</span></span>            | <span data-ttu-id="2dc7a-230">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-230">False</span></span>                                    |
| <span data-ttu-id="2dc7a-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-231">Is-Single-Valued</span></span>       | <span data-ttu-id="2dc7a-232">對</span><span class="sxs-lookup"><span data-stu-id="2dc7a-232">True</span></span>                                     |
| <span data-ttu-id="2dc7a-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2dc7a-233">Is Indexed</span></span>             | <span data-ttu-id="2dc7a-234">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-234">False</span></span>                                    |
| <span data-ttu-id="2dc7a-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2dc7a-235">In Global Catalog</span></span>      | <span data-ttu-id="2dc7a-236">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-236">False</span></span>                                    |
| <span data-ttu-id="2dc7a-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2dc7a-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="2dc7a-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2dc7a-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2dc7a-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2dc7a-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2dc7a-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-241">Search-Flags</span></span>           | <span data-ttu-id="2dc7a-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2dc7a-242">0x00000000</span></span>                               |
| <span data-ttu-id="2dc7a-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-243">System-Flags</span></span>           | <span data-ttu-id="2dc7a-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2dc7a-244">0x00000010</span></span>                               |
| <span data-ttu-id="2dc7a-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2dc7a-245">Classes used in</span></span>        | [<span data-ttu-id="2dc7a-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2dc7a-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2dc7a-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2dc7a-248">進入</span><span class="sxs-lookup"><span data-stu-id="2dc7a-248">Entry</span></span> | <span data-ttu-id="2dc7a-249">值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2dc7a-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2dc7a-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2dc7a-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="2dc7a-252">System-Only</span></span>            | <span data-ttu-id="2dc7a-253">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-253">False</span></span>                                    |
| <span data-ttu-id="2dc7a-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-254">Is-Single-Valued</span></span>       | <span data-ttu-id="2dc7a-255">對</span><span class="sxs-lookup"><span data-stu-id="2dc7a-255">True</span></span>                                     |
| <span data-ttu-id="2dc7a-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2dc7a-256">Is Indexed</span></span>             | <span data-ttu-id="2dc7a-257">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-257">False</span></span>                                    |
| <span data-ttu-id="2dc7a-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2dc7a-258">In Global Catalog</span></span>      | <span data-ttu-id="2dc7a-259">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-259">False</span></span>                                    |
| <span data-ttu-id="2dc7a-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2dc7a-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="2dc7a-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2dc7a-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2dc7a-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2dc7a-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2dc7a-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-264">Search-Flags</span></span>           | <span data-ttu-id="2dc7a-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2dc7a-265">0x00000000</span></span>                               |
| <span data-ttu-id="2dc7a-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-266">System-Flags</span></span>           | <span data-ttu-id="2dc7a-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2dc7a-267">0x00000010</span></span>                               |
| <span data-ttu-id="2dc7a-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2dc7a-268">Classes used in</span></span>        | [<span data-ttu-id="2dc7a-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2dc7a-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2dc7a-270">Windows Server 2012</span></span>



| <span data-ttu-id="2dc7a-271">進入</span><span class="sxs-lookup"><span data-stu-id="2dc7a-271">Entry</span></span> | <span data-ttu-id="2dc7a-272">值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2dc7a-273">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2dc7a-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2dc7a-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2dc7a-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="2dc7a-275">System-Only</span></span>            | <span data-ttu-id="2dc7a-276">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-276">False</span></span>                                    |
| <span data-ttu-id="2dc7a-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2dc7a-277">Is-Single-Valued</span></span>       | <span data-ttu-id="2dc7a-278">對</span><span class="sxs-lookup"><span data-stu-id="2dc7a-278">True</span></span>                                     |
| <span data-ttu-id="2dc7a-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2dc7a-279">Is Indexed</span></span>             | <span data-ttu-id="2dc7a-280">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-280">False</span></span>                                    |
| <span data-ttu-id="2dc7a-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2dc7a-281">In Global Catalog</span></span>      | <span data-ttu-id="2dc7a-282">否</span><span class="sxs-lookup"><span data-stu-id="2dc7a-282">False</span></span>                                    |
| <span data-ttu-id="2dc7a-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2dc7a-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="2dc7a-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2dc7a-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2dc7a-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2dc7a-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2dc7a-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2dc7a-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-287">Search-Flags</span></span>           | <span data-ttu-id="2dc7a-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2dc7a-288">0x00000000</span></span>                               |
| <span data-ttu-id="2dc7a-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2dc7a-289">System-Flags</span></span>           | <span data-ttu-id="2dc7a-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2dc7a-290">0x00000010</span></span>                               |
| <span data-ttu-id="2dc7a-291">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2dc7a-291">Classes used in</span></span>        | [<span data-ttu-id="2dc7a-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2dc7a-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 






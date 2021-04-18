---
title: ms DS-登入時間同步處理間隔屬性
description: 這個屬性會控制使用者或電腦上次登入時間（記錄在 lastLogonTimestamp 屬性中）複寫到網域中所有 Dc 的資料細微性（以天為單位）。
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- ms DS-登入時間-同步處理間隔屬性 AD 架構
- LogonTimeSyncInterval 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbf23ca77bda9dac76f02986be1c05c80559199
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509704"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a><span data-ttu-id="8b77b-105">ms DS-登入時間同步處理間隔屬性</span><span class="sxs-lookup"><span data-stu-id="8b77b-105">ms-DS-Logon-Time-Sync-Interval attribute</span></span>

<span data-ttu-id="8b77b-106">這個屬性會控制使用者或電腦上次登入時間（記錄在 lastLogonTimestamp 屬性中）複寫到網域中所有 Dc 的資料細微性（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="8b77b-106">This attribute controls the granularity, in days, with which the last logon time for a user or computer, recorded in the lastLogonTimestamp attribute, is replicated to all DCs in a domain.</span></span>



| <span data-ttu-id="8b77b-107">進入</span><span class="sxs-lookup"><span data-stu-id="8b77b-107">Entry</span></span> | <span data-ttu-id="8b77b-108">值</span><span class="sxs-lookup"><span data-stu-id="8b77b-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b77b-109">CN</span><span class="sxs-lookup"><span data-stu-id="8b77b-109">CN</span></span>                | <span data-ttu-id="8b77b-110">ms DS-登入時間-同步處理間隔</span><span class="sxs-lookup"><span data-stu-id="8b77b-110">ms-DS-Logon-Time-Sync-Interval</span></span>                                                                             |
| <span data-ttu-id="8b77b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8b77b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8b77b-112">LogonTimeSyncInterval</span><span class="sxs-lookup"><span data-stu-id="8b77b-112">msDS-LogonTimeSyncInterval</span></span>                                                                                 |
| <span data-ttu-id="8b77b-113">大小</span><span class="sxs-lookup"><span data-stu-id="8b77b-113">Size</span></span>              | <span data-ttu-id="8b77b-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="8b77b-114">4 bytes</span></span>                                                                                                    |
| <span data-ttu-id="8b77b-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8b77b-115">Update Privilege</span></span>  | <span data-ttu-id="8b77b-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="8b77b-116">Domain administrator</span></span>                                                                                       |
| <span data-ttu-id="8b77b-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8b77b-117">Update Frequency</span></span>  | <span data-ttu-id="8b77b-118">這很少是因為這是一項原則設定，只有在需要全網域原則的變更時才會更新。</span><span class="sxs-lookup"><span data-stu-id="8b77b-118">Rarely, since this is a policy setting, it is updated only when a change in domain-wide policy is desired.</span></span> |
| <span data-ttu-id="8b77b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b77b-119">Attribute-Id</span></span>      | <span data-ttu-id="8b77b-120">1.2.840.113556.1.4.1784</span><span class="sxs-lookup"><span data-stu-id="8b77b-120">1.2.840.113556.1.4.1784</span></span>                                                                                    |
| <span data-ttu-id="8b77b-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8b77b-121">System-Id-Guid</span></span>    | <span data-ttu-id="8b77b-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span><span class="sxs-lookup"><span data-stu-id="8b77b-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span></span>                                                                       |
| <span data-ttu-id="8b77b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b77b-123">Syntax</span></span>            | [<span data-ttu-id="8b77b-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="8b77b-124">**Enumeration**</span></span>](s-enumeration.md)                                                                       |



## <a name="implementations"></a><span data-ttu-id="8b77b-125">實作</span><span class="sxs-lookup"><span data-stu-id="8b77b-125">Implementations</span></span>

-   [<span data-ttu-id="8b77b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b77b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b77b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b77b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b77b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b77b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b77b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b77b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b77b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b77b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8b77b-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b77b-131">Windows Server 2003</span></span>



| <span data-ttu-id="8b77b-132">進入</span><span class="sxs-lookup"><span data-stu-id="8b77b-132">Entry</span></span> | <span data-ttu-id="8b77b-133">值</span><span class="sxs-lookup"><span data-stu-id="8b77b-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b77b-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b77b-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b77b-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b77b-136">System-Only</span></span>            | <span data-ttu-id="8b77b-137">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-137">False</span></span>                                        |
| <span data-ttu-id="8b77b-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b77b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8b77b-139">對</span><span class="sxs-lookup"><span data-stu-id="8b77b-139">True</span></span>                                         |
| <span data-ttu-id="8b77b-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b77b-140">Is Indexed</span></span>             | <span data-ttu-id="8b77b-141">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-141">False</span></span>                                        |
| <span data-ttu-id="8b77b-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b77b-142">In Global Catalog</span></span>      | <span data-ttu-id="8b77b-143">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-143">False</span></span>                                        |
| <span data-ttu-id="8b77b-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b77b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b77b-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b77b-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b77b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b77b-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b77b-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-148">Search-Flags</span></span>           | <span data-ttu-id="8b77b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b77b-149">0x00000000</span></span>                                   |
| <span data-ttu-id="8b77b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-150">System-Flags</span></span>           | <span data-ttu-id="8b77b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b77b-151">0x00000010</span></span>                                   |
| <span data-ttu-id="8b77b-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b77b-152">Classes used in</span></span>        | [<span data-ttu-id="8b77b-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8b77b-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b77b-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b77b-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b77b-155">進入</span><span class="sxs-lookup"><span data-stu-id="8b77b-155">Entry</span></span> | <span data-ttu-id="8b77b-156">值</span><span class="sxs-lookup"><span data-stu-id="8b77b-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b77b-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b77b-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b77b-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b77b-159">System-Only</span></span>            | <span data-ttu-id="8b77b-160">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-160">False</span></span>                                        |
| <span data-ttu-id="8b77b-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b77b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8b77b-162">對</span><span class="sxs-lookup"><span data-stu-id="8b77b-162">True</span></span>                                         |
| <span data-ttu-id="8b77b-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b77b-163">Is Indexed</span></span>             | <span data-ttu-id="8b77b-164">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-164">False</span></span>                                        |
| <span data-ttu-id="8b77b-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b77b-165">In Global Catalog</span></span>      | <span data-ttu-id="8b77b-166">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-166">False</span></span>                                        |
| <span data-ttu-id="8b77b-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b77b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b77b-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b77b-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b77b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b77b-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b77b-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-171">Search-Flags</span></span>           | <span data-ttu-id="8b77b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b77b-172">0x00000000</span></span>                                   |
| <span data-ttu-id="8b77b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-173">System-Flags</span></span>           | <span data-ttu-id="8b77b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b77b-174">0x00000010</span></span>                                   |
| <span data-ttu-id="8b77b-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b77b-175">Classes used in</span></span>        | [<span data-ttu-id="8b77b-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8b77b-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b77b-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b77b-177">Windows Server 2008</span></span>



| <span data-ttu-id="8b77b-178">進入</span><span class="sxs-lookup"><span data-stu-id="8b77b-178">Entry</span></span> | <span data-ttu-id="8b77b-179">值</span><span class="sxs-lookup"><span data-stu-id="8b77b-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b77b-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b77b-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b77b-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b77b-182">System-Only</span></span>            | <span data-ttu-id="8b77b-183">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-183">False</span></span>                                        |
| <span data-ttu-id="8b77b-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b77b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8b77b-185">對</span><span class="sxs-lookup"><span data-stu-id="8b77b-185">True</span></span>                                         |
| <span data-ttu-id="8b77b-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b77b-186">Is Indexed</span></span>             | <span data-ttu-id="8b77b-187">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-187">False</span></span>                                        |
| <span data-ttu-id="8b77b-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b77b-188">In Global Catalog</span></span>      | <span data-ttu-id="8b77b-189">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-189">False</span></span>                                        |
| <span data-ttu-id="8b77b-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b77b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b77b-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b77b-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b77b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b77b-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b77b-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-194">Search-Flags</span></span>           | <span data-ttu-id="8b77b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b77b-195">0x00000000</span></span>                                   |
| <span data-ttu-id="8b77b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-196">System-Flags</span></span>           | <span data-ttu-id="8b77b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b77b-197">0x00000010</span></span>                                   |
| <span data-ttu-id="8b77b-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b77b-198">Classes used in</span></span>        | [<span data-ttu-id="8b77b-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8b77b-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b77b-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b77b-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b77b-201">進入</span><span class="sxs-lookup"><span data-stu-id="8b77b-201">Entry</span></span> | <span data-ttu-id="8b77b-202">值</span><span class="sxs-lookup"><span data-stu-id="8b77b-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b77b-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b77b-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b77b-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b77b-205">System-Only</span></span>            | <span data-ttu-id="8b77b-206">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-206">False</span></span>                                        |
| <span data-ttu-id="8b77b-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b77b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8b77b-208">對</span><span class="sxs-lookup"><span data-stu-id="8b77b-208">True</span></span>                                         |
| <span data-ttu-id="8b77b-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b77b-209">Is Indexed</span></span>             | <span data-ttu-id="8b77b-210">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-210">False</span></span>                                        |
| <span data-ttu-id="8b77b-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b77b-211">In Global Catalog</span></span>      | <span data-ttu-id="8b77b-212">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-212">False</span></span>                                        |
| <span data-ttu-id="8b77b-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b77b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b77b-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b77b-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b77b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b77b-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b77b-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-217">Search-Flags</span></span>           | <span data-ttu-id="8b77b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b77b-218">0x00000000</span></span>                                   |
| <span data-ttu-id="8b77b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-219">System-Flags</span></span>           | <span data-ttu-id="8b77b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b77b-220">0x00000010</span></span>                                   |
| <span data-ttu-id="8b77b-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b77b-221">Classes used in</span></span>        | [<span data-ttu-id="8b77b-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8b77b-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b77b-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b77b-223">Windows Server 2012</span></span>



| <span data-ttu-id="8b77b-224">進入</span><span class="sxs-lookup"><span data-stu-id="8b77b-224">Entry</span></span> | <span data-ttu-id="8b77b-225">值</span><span class="sxs-lookup"><span data-stu-id="8b77b-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b77b-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b77b-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b77b-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b77b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b77b-228">System-Only</span></span>            | <span data-ttu-id="8b77b-229">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-229">False</span></span>                                        |
| <span data-ttu-id="8b77b-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b77b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8b77b-231">對</span><span class="sxs-lookup"><span data-stu-id="8b77b-231">True</span></span>                                         |
| <span data-ttu-id="8b77b-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b77b-232">Is Indexed</span></span>             | <span data-ttu-id="8b77b-233">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-233">False</span></span>                                        |
| <span data-ttu-id="8b77b-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b77b-234">In Global Catalog</span></span>      | <span data-ttu-id="8b77b-235">否</span><span class="sxs-lookup"><span data-stu-id="8b77b-235">False</span></span>                                        |
| <span data-ttu-id="8b77b-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b77b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b77b-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b77b-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b77b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b77b-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b77b-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b77b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-240">Search-Flags</span></span>           | <span data-ttu-id="8b77b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b77b-241">0x00000000</span></span>                                   |
| <span data-ttu-id="8b77b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b77b-242">System-Flags</span></span>           | <span data-ttu-id="8b77b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b77b-243">0x00000010</span></span>                                   |
| <span data-ttu-id="8b77b-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b77b-244">Classes used in</span></span>        | [<span data-ttu-id="8b77b-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8b77b-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






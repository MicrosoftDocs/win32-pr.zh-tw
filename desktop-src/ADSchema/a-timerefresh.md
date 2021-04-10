---
title: Time-Refresh 屬性
description: 此屬性具有時間間隔，在這段期間內應針對 DNS 伺服器重新整理 Active Directory 整合區域中包含的資源記錄。 預設間隔為7天。
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- Time-Refresh 屬性 AD 架構
- timeRefresh 屬性 AD 架構
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bc360686b1692d2dbda1ee23ad6351e69d3afe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935479"
---
# <a name="time-refresh-attribute"></a><span data-ttu-id="58617-106">Time-Refresh 屬性</span><span class="sxs-lookup"><span data-stu-id="58617-106">Time-Refresh attribute</span></span>

<span data-ttu-id="58617-107">此屬性具有時間間隔，在這段期間內應針對 DNS 伺服器重新整理 Active Directory 整合區域中包含的資源記錄。</span><span class="sxs-lookup"><span data-stu-id="58617-107">This attribute has the interval during which a resource record that is contained in an Active Directory integrated zone should be refreshed for the DNS server.</span></span> <span data-ttu-id="58617-108">預設間隔為7天。</span><span class="sxs-lookup"><span data-stu-id="58617-108">The default interval is 7 days.</span></span>



| <span data-ttu-id="58617-109">進入</span><span class="sxs-lookup"><span data-stu-id="58617-109">Entry</span></span> | <span data-ttu-id="58617-110">值</span><span class="sxs-lookup"><span data-stu-id="58617-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="58617-111">CN</span><span class="sxs-lookup"><span data-stu-id="58617-111">CN</span></span>                | <span data-ttu-id="58617-112">Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="58617-112">Time-Refresh</span></span>                         |
| <span data-ttu-id="58617-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="58617-113">Ldap-Display-Name</span></span> | <span data-ttu-id="58617-114">timeRefresh</span><span class="sxs-lookup"><span data-stu-id="58617-114">timeRefresh</span></span>                          |
| <span data-ttu-id="58617-115">大小</span><span class="sxs-lookup"><span data-stu-id="58617-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="58617-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="58617-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="58617-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="58617-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="58617-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="58617-118">Attribute-Id</span></span>      | <span data-ttu-id="58617-119">1.2.840.113556.1.4.503</span><span class="sxs-lookup"><span data-stu-id="58617-119">1.2.840.113556.1.4.503</span></span>               |
| <span data-ttu-id="58617-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="58617-120">System-Id-Guid</span></span>    | <span data-ttu-id="58617-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="58617-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="58617-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="58617-122">Syntax</span></span>            | [<span data-ttu-id="58617-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="58617-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="58617-124">實作</span><span class="sxs-lookup"><span data-stu-id="58617-124">Implementations</span></span>

-   [<span data-ttu-id="58617-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="58617-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="58617-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="58617-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="58617-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="58617-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="58617-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="58617-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="58617-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="58617-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="58617-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="58617-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="58617-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="58617-131">Windows 2000 Server</span></span>



| <span data-ttu-id="58617-132">進入</span><span class="sxs-lookup"><span data-stu-id="58617-132">Entry</span></span> | <span data-ttu-id="58617-133">值</span><span class="sxs-lookup"><span data-stu-id="58617-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58617-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="58617-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58617-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="58617-136">System-Only</span></span>            | <span data-ttu-id="58617-137">否</span><span class="sxs-lookup"><span data-stu-id="58617-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="58617-138">Is-Single-Valued</span></span>       | <span data-ttu-id="58617-139">對</span><span class="sxs-lookup"><span data-stu-id="58617-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="58617-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="58617-140">Is Indexed</span></span>             | <span data-ttu-id="58617-141">否</span><span class="sxs-lookup"><span data-stu-id="58617-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="58617-142">In Global Catalog</span></span>      | <span data-ttu-id="58617-143">否</span><span class="sxs-lookup"><span data-stu-id="58617-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="58617-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="58617-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="58617-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="58617-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58617-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58617-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-148">Search-Flags</span></span>           | <span data-ttu-id="58617-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58617-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="58617-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-150">System-Flags</span></span>           | <span data-ttu-id="58617-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58617-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="58617-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="58617-152">Classes used in</span></span>        | [<span data-ttu-id="58617-153">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="58617-153">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="58617-154">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="58617-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="58617-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58617-155">Windows Server 2003</span></span>



| <span data-ttu-id="58617-156">進入</span><span class="sxs-lookup"><span data-stu-id="58617-156">Entry</span></span> | <span data-ttu-id="58617-157">值</span><span class="sxs-lookup"><span data-stu-id="58617-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58617-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="58617-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58617-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="58617-160">System-Only</span></span>            | <span data-ttu-id="58617-161">否</span><span class="sxs-lookup"><span data-stu-id="58617-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="58617-162">Is-Single-Valued</span></span>       | <span data-ttu-id="58617-163">對</span><span class="sxs-lookup"><span data-stu-id="58617-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="58617-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="58617-164">Is Indexed</span></span>             | <span data-ttu-id="58617-165">否</span><span class="sxs-lookup"><span data-stu-id="58617-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="58617-166">In Global Catalog</span></span>      | <span data-ttu-id="58617-167">否</span><span class="sxs-lookup"><span data-stu-id="58617-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="58617-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="58617-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="58617-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="58617-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58617-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58617-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-172">Search-Flags</span></span>           | <span data-ttu-id="58617-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58617-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="58617-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-174">System-Flags</span></span>           | <span data-ttu-id="58617-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58617-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="58617-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="58617-176">Classes used in</span></span>        | [<span data-ttu-id="58617-177">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="58617-177">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="58617-178">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="58617-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="58617-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="58617-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="58617-180">進入</span><span class="sxs-lookup"><span data-stu-id="58617-180">Entry</span></span> | <span data-ttu-id="58617-181">值</span><span class="sxs-lookup"><span data-stu-id="58617-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58617-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="58617-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58617-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="58617-184">System-Only</span></span>            | <span data-ttu-id="58617-185">否</span><span class="sxs-lookup"><span data-stu-id="58617-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="58617-186">Is-Single-Valued</span></span>       | <span data-ttu-id="58617-187">對</span><span class="sxs-lookup"><span data-stu-id="58617-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="58617-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="58617-188">Is Indexed</span></span>             | <span data-ttu-id="58617-189">否</span><span class="sxs-lookup"><span data-stu-id="58617-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="58617-190">In Global Catalog</span></span>      | <span data-ttu-id="58617-191">否</span><span class="sxs-lookup"><span data-stu-id="58617-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="58617-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="58617-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="58617-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="58617-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58617-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58617-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-196">Search-Flags</span></span>           | <span data-ttu-id="58617-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58617-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="58617-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-198">System-Flags</span></span>           | <span data-ttu-id="58617-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58617-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="58617-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="58617-200">Classes used in</span></span>        | [<span data-ttu-id="58617-201">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="58617-201">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="58617-202">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="58617-202">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="58617-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58617-203">Windows Server 2008</span></span>



| <span data-ttu-id="58617-204">進入</span><span class="sxs-lookup"><span data-stu-id="58617-204">Entry</span></span> | <span data-ttu-id="58617-205">值</span><span class="sxs-lookup"><span data-stu-id="58617-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58617-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="58617-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58617-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="58617-208">System-Only</span></span>            | <span data-ttu-id="58617-209">否</span><span class="sxs-lookup"><span data-stu-id="58617-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="58617-210">Is-Single-Valued</span></span>       | <span data-ttu-id="58617-211">對</span><span class="sxs-lookup"><span data-stu-id="58617-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="58617-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="58617-212">Is Indexed</span></span>             | <span data-ttu-id="58617-213">否</span><span class="sxs-lookup"><span data-stu-id="58617-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="58617-214">In Global Catalog</span></span>      | <span data-ttu-id="58617-215">否</span><span class="sxs-lookup"><span data-stu-id="58617-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="58617-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="58617-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="58617-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="58617-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58617-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58617-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-220">Search-Flags</span></span>           | <span data-ttu-id="58617-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58617-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="58617-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-222">System-Flags</span></span>           | <span data-ttu-id="58617-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58617-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="58617-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="58617-224">Classes used in</span></span>        | [<span data-ttu-id="58617-225">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="58617-225">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="58617-226">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="58617-226">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="58617-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58617-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="58617-228">進入</span><span class="sxs-lookup"><span data-stu-id="58617-228">Entry</span></span> | <span data-ttu-id="58617-229">值</span><span class="sxs-lookup"><span data-stu-id="58617-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58617-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="58617-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58617-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="58617-232">System-Only</span></span>            | <span data-ttu-id="58617-233">否</span><span class="sxs-lookup"><span data-stu-id="58617-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="58617-234">Is-Single-Valued</span></span>       | <span data-ttu-id="58617-235">對</span><span class="sxs-lookup"><span data-stu-id="58617-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="58617-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="58617-236">Is Indexed</span></span>             | <span data-ttu-id="58617-237">否</span><span class="sxs-lookup"><span data-stu-id="58617-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="58617-238">In Global Catalog</span></span>      | <span data-ttu-id="58617-239">否</span><span class="sxs-lookup"><span data-stu-id="58617-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="58617-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="58617-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="58617-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="58617-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58617-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58617-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-244">Search-Flags</span></span>           | <span data-ttu-id="58617-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58617-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="58617-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-246">System-Flags</span></span>           | <span data-ttu-id="58617-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58617-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="58617-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="58617-248">Classes used in</span></span>        | [<span data-ttu-id="58617-249">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="58617-249">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="58617-250">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="58617-250">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="58617-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58617-251">Windows Server 2012</span></span>



| <span data-ttu-id="58617-252">進入</span><span class="sxs-lookup"><span data-stu-id="58617-252">Entry</span></span> | <span data-ttu-id="58617-253">值</span><span class="sxs-lookup"><span data-stu-id="58617-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58617-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="58617-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58617-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="58617-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="58617-256">System-Only</span></span>            | <span data-ttu-id="58617-257">否</span><span class="sxs-lookup"><span data-stu-id="58617-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="58617-258">Is-Single-Valued</span></span>       | <span data-ttu-id="58617-259">對</span><span class="sxs-lookup"><span data-stu-id="58617-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="58617-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="58617-260">Is Indexed</span></span>             | <span data-ttu-id="58617-261">否</span><span class="sxs-lookup"><span data-stu-id="58617-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="58617-262">In Global Catalog</span></span>      | <span data-ttu-id="58617-263">否</span><span class="sxs-lookup"><span data-stu-id="58617-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="58617-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="58617-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="58617-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="58617-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="58617-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58617-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58617-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="58617-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-268">Search-Flags</span></span>           | <span data-ttu-id="58617-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58617-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="58617-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58617-270">System-Flags</span></span>           | <span data-ttu-id="58617-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58617-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="58617-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="58617-272">Classes used in</span></span>        | [<span data-ttu-id="58617-273">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="58617-273">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="58617-274">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="58617-274">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 






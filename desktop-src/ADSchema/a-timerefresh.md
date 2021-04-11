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
# <a name="time-refresh-attribute"></a><span data-ttu-id="6b607-106">Time-Refresh 屬性</span><span class="sxs-lookup"><span data-stu-id="6b607-106">Time-Refresh attribute</span></span>

<span data-ttu-id="6b607-107">此屬性具有時間間隔，在這段期間內應針對 DNS 伺服器重新整理 Active Directory 整合區域中包含的資源記錄。</span><span class="sxs-lookup"><span data-stu-id="6b607-107">This attribute has the interval during which a resource record that is contained in an Active Directory integrated zone should be refreshed for the DNS server.</span></span> <span data-ttu-id="6b607-108">預設間隔為7天。</span><span class="sxs-lookup"><span data-stu-id="6b607-108">The default interval is 7 days.</span></span>



| <span data-ttu-id="6b607-109">進入</span><span class="sxs-lookup"><span data-stu-id="6b607-109">Entry</span></span> | <span data-ttu-id="6b607-110">值</span><span class="sxs-lookup"><span data-stu-id="6b607-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6b607-111">CN</span><span class="sxs-lookup"><span data-stu-id="6b607-111">CN</span></span>                | <span data-ttu-id="6b607-112">Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="6b607-112">Time-Refresh</span></span>                         |
| <span data-ttu-id="6b607-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6b607-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6b607-114">timeRefresh</span><span class="sxs-lookup"><span data-stu-id="6b607-114">timeRefresh</span></span>                          |
| <span data-ttu-id="6b607-115">大小</span><span class="sxs-lookup"><span data-stu-id="6b607-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="6b607-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6b607-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="6b607-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6b607-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6b607-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6b607-118">Attribute-Id</span></span>      | <span data-ttu-id="6b607-119">1.2.840.113556.1.4.503</span><span class="sxs-lookup"><span data-stu-id="6b607-119">1.2.840.113556.1.4.503</span></span>               |
| <span data-ttu-id="6b607-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6b607-120">System-Id-Guid</span></span>    | <span data-ttu-id="6b607-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="6b607-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="6b607-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b607-122">Syntax</span></span>            | [<span data-ttu-id="6b607-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="6b607-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="6b607-124">實作</span><span class="sxs-lookup"><span data-stu-id="6b607-124">Implementations</span></span>

-   [<span data-ttu-id="6b607-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6b607-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6b607-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6b607-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6b607-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6b607-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6b607-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6b607-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6b607-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6b607-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6b607-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6b607-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6b607-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6b607-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6b607-132">進入</span><span class="sxs-lookup"><span data-stu-id="6b607-132">Entry</span></span> | <span data-ttu-id="6b607-133">值</span><span class="sxs-lookup"><span data-stu-id="6b607-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b607-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6b607-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b607-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b607-136">System-Only</span></span>            | <span data-ttu-id="6b607-137">否</span><span class="sxs-lookup"><span data-stu-id="6b607-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6b607-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6b607-139">對</span><span class="sxs-lookup"><span data-stu-id="6b607-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="6b607-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6b607-140">Is Indexed</span></span>             | <span data-ttu-id="6b607-141">否</span><span class="sxs-lookup"><span data-stu-id="6b607-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6b607-142">In Global Catalog</span></span>      | <span data-ttu-id="6b607-143">否</span><span class="sxs-lookup"><span data-stu-id="6b607-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6b607-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b607-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6b607-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6b607-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b607-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b607-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-148">Search-Flags</span></span>           | <span data-ttu-id="6b607-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b607-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-150">System-Flags</span></span>           | <span data-ttu-id="6b607-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b607-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6b607-152">Classes used in</span></span>        | [<span data-ttu-id="6b607-153">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="6b607-153">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="6b607-154">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="6b607-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6b607-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b607-155">Windows Server 2003</span></span>



| <span data-ttu-id="6b607-156">進入</span><span class="sxs-lookup"><span data-stu-id="6b607-156">Entry</span></span> | <span data-ttu-id="6b607-157">值</span><span class="sxs-lookup"><span data-stu-id="6b607-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b607-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6b607-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b607-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b607-160">System-Only</span></span>            | <span data-ttu-id="6b607-161">否</span><span class="sxs-lookup"><span data-stu-id="6b607-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6b607-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6b607-163">對</span><span class="sxs-lookup"><span data-stu-id="6b607-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="6b607-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6b607-164">Is Indexed</span></span>             | <span data-ttu-id="6b607-165">否</span><span class="sxs-lookup"><span data-stu-id="6b607-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6b607-166">In Global Catalog</span></span>      | <span data-ttu-id="6b607-167">否</span><span class="sxs-lookup"><span data-stu-id="6b607-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6b607-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b607-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6b607-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6b607-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b607-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b607-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-172">Search-Flags</span></span>           | <span data-ttu-id="6b607-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b607-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-174">System-Flags</span></span>           | <span data-ttu-id="6b607-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b607-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6b607-176">Classes used in</span></span>        | [<span data-ttu-id="6b607-177">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="6b607-177">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="6b607-178">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="6b607-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6b607-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6b607-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6b607-180">進入</span><span class="sxs-lookup"><span data-stu-id="6b607-180">Entry</span></span> | <span data-ttu-id="6b607-181">值</span><span class="sxs-lookup"><span data-stu-id="6b607-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b607-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6b607-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b607-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b607-184">System-Only</span></span>            | <span data-ttu-id="6b607-185">否</span><span class="sxs-lookup"><span data-stu-id="6b607-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6b607-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6b607-187">對</span><span class="sxs-lookup"><span data-stu-id="6b607-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="6b607-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6b607-188">Is Indexed</span></span>             | <span data-ttu-id="6b607-189">否</span><span class="sxs-lookup"><span data-stu-id="6b607-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6b607-190">In Global Catalog</span></span>      | <span data-ttu-id="6b607-191">否</span><span class="sxs-lookup"><span data-stu-id="6b607-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6b607-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b607-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6b607-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6b607-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b607-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b607-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-196">Search-Flags</span></span>           | <span data-ttu-id="6b607-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b607-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-198">System-Flags</span></span>           | <span data-ttu-id="6b607-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b607-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6b607-200">Classes used in</span></span>        | [<span data-ttu-id="6b607-201">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="6b607-201">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="6b607-202">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="6b607-202">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6b607-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b607-203">Windows Server 2008</span></span>



| <span data-ttu-id="6b607-204">進入</span><span class="sxs-lookup"><span data-stu-id="6b607-204">Entry</span></span> | <span data-ttu-id="6b607-205">值</span><span class="sxs-lookup"><span data-stu-id="6b607-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b607-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6b607-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b607-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b607-208">System-Only</span></span>            | <span data-ttu-id="6b607-209">否</span><span class="sxs-lookup"><span data-stu-id="6b607-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6b607-210">Is-Single-Valued</span></span>       | <span data-ttu-id="6b607-211">對</span><span class="sxs-lookup"><span data-stu-id="6b607-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="6b607-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6b607-212">Is Indexed</span></span>             | <span data-ttu-id="6b607-213">否</span><span class="sxs-lookup"><span data-stu-id="6b607-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6b607-214">In Global Catalog</span></span>      | <span data-ttu-id="6b607-215">否</span><span class="sxs-lookup"><span data-stu-id="6b607-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6b607-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b607-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6b607-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6b607-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b607-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b607-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-220">Search-Flags</span></span>           | <span data-ttu-id="6b607-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b607-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-222">System-Flags</span></span>           | <span data-ttu-id="6b607-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b607-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6b607-224">Classes used in</span></span>        | [<span data-ttu-id="6b607-225">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="6b607-225">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="6b607-226">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="6b607-226">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6b607-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6b607-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6b607-228">進入</span><span class="sxs-lookup"><span data-stu-id="6b607-228">Entry</span></span> | <span data-ttu-id="6b607-229">值</span><span class="sxs-lookup"><span data-stu-id="6b607-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b607-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6b607-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b607-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b607-232">System-Only</span></span>            | <span data-ttu-id="6b607-233">否</span><span class="sxs-lookup"><span data-stu-id="6b607-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6b607-234">Is-Single-Valued</span></span>       | <span data-ttu-id="6b607-235">對</span><span class="sxs-lookup"><span data-stu-id="6b607-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="6b607-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6b607-236">Is Indexed</span></span>             | <span data-ttu-id="6b607-237">否</span><span class="sxs-lookup"><span data-stu-id="6b607-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6b607-238">In Global Catalog</span></span>      | <span data-ttu-id="6b607-239">否</span><span class="sxs-lookup"><span data-stu-id="6b607-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6b607-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b607-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6b607-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6b607-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b607-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b607-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-244">Search-Flags</span></span>           | <span data-ttu-id="6b607-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b607-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-246">System-Flags</span></span>           | <span data-ttu-id="6b607-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b607-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6b607-248">Classes used in</span></span>        | [<span data-ttu-id="6b607-249">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="6b607-249">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="6b607-250">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="6b607-250">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6b607-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6b607-251">Windows Server 2012</span></span>



| <span data-ttu-id="6b607-252">進入</span><span class="sxs-lookup"><span data-stu-id="6b607-252">Entry</span></span> | <span data-ttu-id="6b607-253">值</span><span class="sxs-lookup"><span data-stu-id="6b607-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b607-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6b607-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b607-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="6b607-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b607-256">System-Only</span></span>            | <span data-ttu-id="6b607-257">否</span><span class="sxs-lookup"><span data-stu-id="6b607-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6b607-258">Is-Single-Valued</span></span>       | <span data-ttu-id="6b607-259">對</span><span class="sxs-lookup"><span data-stu-id="6b607-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="6b607-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6b607-260">Is Indexed</span></span>             | <span data-ttu-id="6b607-261">否</span><span class="sxs-lookup"><span data-stu-id="6b607-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6b607-262">In Global Catalog</span></span>      | <span data-ttu-id="6b607-263">否</span><span class="sxs-lookup"><span data-stu-id="6b607-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="6b607-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6b607-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b607-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6b607-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="6b607-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b607-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b607-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="6b607-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-268">Search-Flags</span></span>           | <span data-ttu-id="6b607-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b607-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b607-270">System-Flags</span></span>           | <span data-ttu-id="6b607-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b607-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="6b607-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6b607-272">Classes used in</span></span>        | [<span data-ttu-id="6b607-273">**連結-追蹤-OMT-Entry**</span><span class="sxs-lookup"><span data-stu-id="6b607-273">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="6b607-274">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="6b607-274">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 






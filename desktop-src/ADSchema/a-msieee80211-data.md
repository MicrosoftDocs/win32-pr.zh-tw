---
title: ms-ieee-80211-Data 屬性
description: 在無線網路的群組原則中儲存慣用網路設定的清單。
ms.assetid: 8e5ae2c6-c048-419d-a684-e450a2445a0e
ms.tgt_platform: multiple
keywords:
- ms-ieee-80211-Data attribute AD 架構
- msieee80211-Data 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-ieee-80211-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a53138e15a15e4fafecb998b87ef8b4df71fb2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509609"
---
# <a name="ms-ieee-80211-data-attribute"></a><span data-ttu-id="988f9-105">ms-ieee-80211-Data 屬性</span><span class="sxs-lookup"><span data-stu-id="988f9-105">ms-ieee-80211-Data attribute</span></span>

<span data-ttu-id="988f9-106">在無線網路的群組原則中儲存慣用網路設定的清單。</span><span class="sxs-lookup"><span data-stu-id="988f9-106">Stores a list of preferred network configurations in Group Policy for wireless networks.</span></span>



| <span data-ttu-id="988f9-107">進入</span><span class="sxs-lookup"><span data-stu-id="988f9-107">Entry</span></span> | <span data-ttu-id="988f9-108">值</span><span class="sxs-lookup"><span data-stu-id="988f9-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="988f9-109">CN</span><span class="sxs-lookup"><span data-stu-id="988f9-109">CN</span></span>                | <span data-ttu-id="988f9-110">ms-ieee-80211-資料</span><span class="sxs-lookup"><span data-stu-id="988f9-110">ms-ieee-80211-Data</span></span>                                                               |
| <span data-ttu-id="988f9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="988f9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="988f9-112">msieee80211-資料</span><span class="sxs-lookup"><span data-stu-id="988f9-112">msieee80211-Data</span></span>                                                                 |
| <span data-ttu-id="988f9-113">大小</span><span class="sxs-lookup"><span data-stu-id="988f9-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="988f9-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="988f9-114">Update Privilege</span></span>  | <span data-ttu-id="988f9-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="988f9-115">Domain administrator</span></span>                                                             |
| <span data-ttu-id="988f9-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="988f9-116">Update Frequency</span></span>  | <span data-ttu-id="988f9-117">每次網域管理員變更網域或 OU 的無線網路原則時。</span><span class="sxs-lookup"><span data-stu-id="988f9-117">Each time a Domain Admin changes the wireless network policy for a domain or OU.</span></span> |
| <span data-ttu-id="988f9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="988f9-118">Attribute-Id</span></span>      | <span data-ttu-id="988f9-119">1.2.840.113556.1.4.1821</span><span class="sxs-lookup"><span data-stu-id="988f9-119">1.2.840.113556.1.4.1821</span></span>                                                          |
| <span data-ttu-id="988f9-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="988f9-120">System-Id-Guid</span></span>    | <span data-ttu-id="988f9-121">0e0d0938-2658-4580-a9f6-7a0ac7b566cb</span><span class="sxs-lookup"><span data-stu-id="988f9-121">0e0d0938-2658-4580-a9f6-7a0ac7b566cb</span></span>                                             |
| <span data-ttu-id="988f9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="988f9-122">Syntax</span></span>            | [<span data-ttu-id="988f9-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="988f9-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                            |



## <a name="implementations"></a><span data-ttu-id="988f9-124">實作</span><span class="sxs-lookup"><span data-stu-id="988f9-124">Implementations</span></span>

-   [<span data-ttu-id="988f9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="988f9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="988f9-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="988f9-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="988f9-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="988f9-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="988f9-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="988f9-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="988f9-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="988f9-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="988f9-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="988f9-130">Windows Server 2003</span></span>



| <span data-ttu-id="988f9-131">進入</span><span class="sxs-lookup"><span data-stu-id="988f9-131">Entry</span></span> | <span data-ttu-id="988f9-132">值</span><span class="sxs-lookup"><span data-stu-id="988f9-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="988f9-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="988f9-133">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="988f9-134">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="988f9-135">System-Only</span></span>            | <span data-ttu-id="988f9-136">否</span><span class="sxs-lookup"><span data-stu-id="988f9-136">False</span></span>                                                           |
| <span data-ttu-id="988f9-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="988f9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="988f9-138">對</span><span class="sxs-lookup"><span data-stu-id="988f9-138">True</span></span>                                                            |
| <span data-ttu-id="988f9-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="988f9-139">Is Indexed</span></span>             | <span data-ttu-id="988f9-140">否</span><span class="sxs-lookup"><span data-stu-id="988f9-140">False</span></span>                                                           |
| <span data-ttu-id="988f9-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="988f9-141">In Global Catalog</span></span>      | <span data-ttu-id="988f9-142">否</span><span class="sxs-lookup"><span data-stu-id="988f9-142">False</span></span>                                                           |
| <span data-ttu-id="988f9-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="988f9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="988f9-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="988f9-144">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="988f9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="988f9-145">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="988f9-146">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-147">Search-Flags</span></span>           | <span data-ttu-id="988f9-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="988f9-148">0x00000000</span></span>                                                      |
| <span data-ttu-id="988f9-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-149">System-Flags</span></span>           | <span data-ttu-id="988f9-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="988f9-150">0x00000010</span></span>                                                      |
| <span data-ttu-id="988f9-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="988f9-151">Classes used in</span></span>        | [<span data-ttu-id="988f9-152">**ms-ieee-80211-原則**</span><span class="sxs-lookup"><span data-stu-id="988f9-152">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="988f9-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="988f9-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="988f9-154">進入</span><span class="sxs-lookup"><span data-stu-id="988f9-154">Entry</span></span> | <span data-ttu-id="988f9-155">值</span><span class="sxs-lookup"><span data-stu-id="988f9-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="988f9-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="988f9-156">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="988f9-157">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="988f9-158">System-Only</span></span>            | <span data-ttu-id="988f9-159">否</span><span class="sxs-lookup"><span data-stu-id="988f9-159">False</span></span>                                                           |
| <span data-ttu-id="988f9-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="988f9-160">Is-Single-Valued</span></span>       | <span data-ttu-id="988f9-161">對</span><span class="sxs-lookup"><span data-stu-id="988f9-161">True</span></span>                                                            |
| <span data-ttu-id="988f9-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="988f9-162">Is Indexed</span></span>             | <span data-ttu-id="988f9-163">否</span><span class="sxs-lookup"><span data-stu-id="988f9-163">False</span></span>                                                           |
| <span data-ttu-id="988f9-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="988f9-164">In Global Catalog</span></span>      | <span data-ttu-id="988f9-165">否</span><span class="sxs-lookup"><span data-stu-id="988f9-165">False</span></span>                                                           |
| <span data-ttu-id="988f9-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="988f9-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="988f9-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="988f9-167">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="988f9-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="988f9-168">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="988f9-169">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-170">Search-Flags</span></span>           | <span data-ttu-id="988f9-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="988f9-171">0x00000000</span></span>                                                      |
| <span data-ttu-id="988f9-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-172">System-Flags</span></span>           | <span data-ttu-id="988f9-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="988f9-173">0x00000010</span></span>                                                      |
| <span data-ttu-id="988f9-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="988f9-174">Classes used in</span></span>        | [<span data-ttu-id="988f9-175">**ms-ieee-80211-原則**</span><span class="sxs-lookup"><span data-stu-id="988f9-175">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="988f9-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="988f9-176">Windows Server 2008</span></span>



| <span data-ttu-id="988f9-177">進入</span><span class="sxs-lookup"><span data-stu-id="988f9-177">Entry</span></span> | <span data-ttu-id="988f9-178">值</span><span class="sxs-lookup"><span data-stu-id="988f9-178">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="988f9-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="988f9-179">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="988f9-180">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="988f9-181">System-Only</span></span>            | <span data-ttu-id="988f9-182">否</span><span class="sxs-lookup"><span data-stu-id="988f9-182">False</span></span>                                                           |
| <span data-ttu-id="988f9-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="988f9-183">Is-Single-Valued</span></span>       | <span data-ttu-id="988f9-184">對</span><span class="sxs-lookup"><span data-stu-id="988f9-184">True</span></span>                                                            |
| <span data-ttu-id="988f9-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="988f9-185">Is Indexed</span></span>             | <span data-ttu-id="988f9-186">否</span><span class="sxs-lookup"><span data-stu-id="988f9-186">False</span></span>                                                           |
| <span data-ttu-id="988f9-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="988f9-187">In Global Catalog</span></span>      | <span data-ttu-id="988f9-188">否</span><span class="sxs-lookup"><span data-stu-id="988f9-188">False</span></span>                                                           |
| <span data-ttu-id="988f9-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="988f9-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="988f9-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="988f9-190">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="988f9-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="988f9-191">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="988f9-192">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-193">Search-Flags</span></span>           | <span data-ttu-id="988f9-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="988f9-194">0x00000000</span></span>                                                      |
| <span data-ttu-id="988f9-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-195">System-Flags</span></span>           | <span data-ttu-id="988f9-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="988f9-196">0x00000010</span></span>                                                      |
| <span data-ttu-id="988f9-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="988f9-197">Classes used in</span></span>        | [<span data-ttu-id="988f9-198">**ms-ieee-80211-原則**</span><span class="sxs-lookup"><span data-stu-id="988f9-198">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="988f9-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="988f9-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="988f9-200">進入</span><span class="sxs-lookup"><span data-stu-id="988f9-200">Entry</span></span> | <span data-ttu-id="988f9-201">值</span><span class="sxs-lookup"><span data-stu-id="988f9-201">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="988f9-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="988f9-202">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="988f9-203">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="988f9-204">System-Only</span></span>            | <span data-ttu-id="988f9-205">否</span><span class="sxs-lookup"><span data-stu-id="988f9-205">False</span></span>                                                           |
| <span data-ttu-id="988f9-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="988f9-206">Is-Single-Valued</span></span>       | <span data-ttu-id="988f9-207">對</span><span class="sxs-lookup"><span data-stu-id="988f9-207">True</span></span>                                                            |
| <span data-ttu-id="988f9-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="988f9-208">Is Indexed</span></span>             | <span data-ttu-id="988f9-209">否</span><span class="sxs-lookup"><span data-stu-id="988f9-209">False</span></span>                                                           |
| <span data-ttu-id="988f9-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="988f9-210">In Global Catalog</span></span>      | <span data-ttu-id="988f9-211">否</span><span class="sxs-lookup"><span data-stu-id="988f9-211">False</span></span>                                                           |
| <span data-ttu-id="988f9-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="988f9-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="988f9-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="988f9-213">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="988f9-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="988f9-214">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="988f9-215">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-216">Search-Flags</span></span>           | <span data-ttu-id="988f9-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="988f9-217">0x00000000</span></span>                                                      |
| <span data-ttu-id="988f9-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-218">System-Flags</span></span>           | <span data-ttu-id="988f9-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="988f9-219">0x00000010</span></span>                                                      |
| <span data-ttu-id="988f9-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="988f9-220">Classes used in</span></span>        | [<span data-ttu-id="988f9-221">**ms-ieee-80211-原則**</span><span class="sxs-lookup"><span data-stu-id="988f9-221">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="988f9-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="988f9-222">Windows Server 2012</span></span>



| <span data-ttu-id="988f9-223">進入</span><span class="sxs-lookup"><span data-stu-id="988f9-223">Entry</span></span> | <span data-ttu-id="988f9-224">值</span><span class="sxs-lookup"><span data-stu-id="988f9-224">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="988f9-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="988f9-225">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="988f9-226">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="988f9-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="988f9-227">System-Only</span></span>            | <span data-ttu-id="988f9-228">否</span><span class="sxs-lookup"><span data-stu-id="988f9-228">False</span></span>                                                           |
| <span data-ttu-id="988f9-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="988f9-229">Is-Single-Valued</span></span>       | <span data-ttu-id="988f9-230">對</span><span class="sxs-lookup"><span data-stu-id="988f9-230">True</span></span>                                                            |
| <span data-ttu-id="988f9-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="988f9-231">Is Indexed</span></span>             | <span data-ttu-id="988f9-232">否</span><span class="sxs-lookup"><span data-stu-id="988f9-232">False</span></span>                                                           |
| <span data-ttu-id="988f9-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="988f9-233">In Global Catalog</span></span>      | <span data-ttu-id="988f9-234">否</span><span class="sxs-lookup"><span data-stu-id="988f9-234">False</span></span>                                                           |
| <span data-ttu-id="988f9-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="988f9-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="988f9-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="988f9-236">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="988f9-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="988f9-237">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="988f9-238">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="988f9-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-239">Search-Flags</span></span>           | <span data-ttu-id="988f9-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="988f9-240">0x00000000</span></span>                                                      |
| <span data-ttu-id="988f9-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="988f9-241">System-Flags</span></span>           | <span data-ttu-id="988f9-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="988f9-242">0x00000010</span></span>                                                      |
| <span data-ttu-id="988f9-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="988f9-243">Classes used in</span></span>        | [<span data-ttu-id="988f9-244">**ms-ieee-80211-原則**</span><span class="sxs-lookup"><span data-stu-id="988f9-244">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



 

 






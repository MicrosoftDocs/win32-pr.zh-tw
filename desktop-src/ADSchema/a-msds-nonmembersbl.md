---
title: ms DS-非成員-BL 屬性
description: 從非成員群組或使用者到 Az 群組的反向連結（連結至該群組） (與非安全性成員 BL) 相同的功能。
ms.assetid: 51725a95-a9c0-4c88-a390-b8e35b8fd3e1
ms.tgt_platform: multiple
keywords:
- ms DS-非成員-BL 屬性 AD 架構
- NonMembersBL 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Non-Members-BL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88483757e5c9f87771ce8d71f21d26ea3154f975
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970868"
---
# <a name="ms-ds-non-members-bl-attribute"></a><span data-ttu-id="0d7be-105">ms DS-非成員-BL 屬性</span><span class="sxs-lookup"><span data-stu-id="0d7be-105">ms-DS-Non-Members-BL attribute</span></span>

<span data-ttu-id="0d7be-106">從非成員群組或使用者到 Az 群組的反向連結（連結至該群組） (與非安全性成員 BL) 相同的功能。</span><span class="sxs-lookup"><span data-stu-id="0d7be-106">Backward link from non-member group or user to Az groups that link to it (same functionality as Non-Security-Member-BL).</span></span>



| <span data-ttu-id="0d7be-107">進入</span><span class="sxs-lookup"><span data-stu-id="0d7be-107">Entry</span></span> | <span data-ttu-id="0d7be-108">值</span><span class="sxs-lookup"><span data-stu-id="0d7be-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="0d7be-109">CN</span><span class="sxs-lookup"><span data-stu-id="0d7be-109">CN</span></span>                | <span data-ttu-id="0d7be-110">ms DS-非成員-BL</span><span class="sxs-lookup"><span data-stu-id="0d7be-110">ms-DS-Non-Members-BL</span></span>                    |
| <span data-ttu-id="0d7be-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0d7be-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0d7be-112">NonMembersBL</span><span class="sxs-lookup"><span data-stu-id="0d7be-112">msDS-NonMembersBL</span></span>                       |
| <span data-ttu-id="0d7be-113">大小</span><span class="sxs-lookup"><span data-stu-id="0d7be-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="0d7be-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0d7be-114">Update Privilege</span></span>  | <span data-ttu-id="0d7be-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="0d7be-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="0d7be-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0d7be-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="0d7be-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0d7be-117">Attribute-Id</span></span>      | <span data-ttu-id="0d7be-118">1.2.840.113556.1.4.1794</span><span class="sxs-lookup"><span data-stu-id="0d7be-118">1.2.840.113556.1.4.1794</span></span>                 |
| <span data-ttu-id="0d7be-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0d7be-119">System-Id-Guid</span></span>    | <span data-ttu-id="0d7be-120">2a8c68fc-3a7a-4e87-8720-fe77c51cbe74</span><span class="sxs-lookup"><span data-stu-id="0d7be-120">2a8c68fc-3a7a-4e87-8720-fe77c51cbe74</span></span>    |
| <span data-ttu-id="0d7be-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d7be-121">Syntax</span></span>            | [<span data-ttu-id="0d7be-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="0d7be-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="0d7be-123">實作</span><span class="sxs-lookup"><span data-stu-id="0d7be-123">Implementations</span></span>

-   [<span data-ttu-id="0d7be-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0d7be-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0d7be-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0d7be-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0d7be-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0d7be-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0d7be-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0d7be-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0d7be-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0d7be-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0d7be-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d7be-129">Windows Server 2003</span></span>



| <span data-ttu-id="0d7be-130">進入</span><span class="sxs-lookup"><span data-stu-id="0d7be-130">Entry</span></span> | <span data-ttu-id="0d7be-131">值</span><span class="sxs-lookup"><span data-stu-id="0d7be-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d7be-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d7be-132">Link-Id</span></span>                | <span data-ttu-id="0d7be-133">2015</span><span class="sxs-lookup"><span data-stu-id="0d7be-133">2015</span></span>                            |
| <span data-ttu-id="0d7be-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d7be-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d7be-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d7be-135">System-Only</span></span>            | <span data-ttu-id="0d7be-136">對</span><span class="sxs-lookup"><span data-stu-id="0d7be-136">True</span></span>                            |
| <span data-ttu-id="0d7be-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d7be-137">Is-Single-Valued</span></span>       | <span data-ttu-id="0d7be-138">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-138">False</span></span>                           |
| <span data-ttu-id="0d7be-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d7be-139">Is Indexed</span></span>             | <span data-ttu-id="0d7be-140">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-140">False</span></span>                           |
| <span data-ttu-id="0d7be-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d7be-141">In Global Catalog</span></span>      | <span data-ttu-id="0d7be-142">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-142">False</span></span>                           |
| <span data-ttu-id="0d7be-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d7be-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d7be-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d7be-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d7be-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d7be-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0d7be-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d7be-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0d7be-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-147">Search-Flags</span></span>           | <span data-ttu-id="0d7be-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d7be-148">0x00000000</span></span>                      |
| <span data-ttu-id="0d7be-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-149">System-Flags</span></span>           | <span data-ttu-id="0d7be-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d7be-150">0x00000010</span></span>                      |
| <span data-ttu-id="0d7be-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d7be-151">Classes used in</span></span>        | [<span data-ttu-id="0d7be-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0d7be-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0d7be-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0d7be-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0d7be-154">進入</span><span class="sxs-lookup"><span data-stu-id="0d7be-154">Entry</span></span> | <span data-ttu-id="0d7be-155">值</span><span class="sxs-lookup"><span data-stu-id="0d7be-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d7be-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d7be-156">Link-Id</span></span>                | <span data-ttu-id="0d7be-157">2015</span><span class="sxs-lookup"><span data-stu-id="0d7be-157">2015</span></span>                            |
| <span data-ttu-id="0d7be-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d7be-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d7be-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d7be-159">System-Only</span></span>            | <span data-ttu-id="0d7be-160">對</span><span class="sxs-lookup"><span data-stu-id="0d7be-160">True</span></span>                            |
| <span data-ttu-id="0d7be-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d7be-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0d7be-162">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-162">False</span></span>                           |
| <span data-ttu-id="0d7be-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d7be-163">Is Indexed</span></span>             | <span data-ttu-id="0d7be-164">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-164">False</span></span>                           |
| <span data-ttu-id="0d7be-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d7be-165">In Global Catalog</span></span>      | <span data-ttu-id="0d7be-166">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-166">False</span></span>                           |
| <span data-ttu-id="0d7be-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d7be-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d7be-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d7be-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d7be-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d7be-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0d7be-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d7be-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0d7be-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-171">Search-Flags</span></span>           | <span data-ttu-id="0d7be-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d7be-172">0x00000000</span></span>                      |
| <span data-ttu-id="0d7be-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-173">System-Flags</span></span>           | <span data-ttu-id="0d7be-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d7be-174">0x00000010</span></span>                      |
| <span data-ttu-id="0d7be-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d7be-175">Classes used in</span></span>        | [<span data-ttu-id="0d7be-176">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0d7be-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0d7be-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d7be-177">Windows Server 2008</span></span>



| <span data-ttu-id="0d7be-178">進入</span><span class="sxs-lookup"><span data-stu-id="0d7be-178">Entry</span></span> | <span data-ttu-id="0d7be-179">值</span><span class="sxs-lookup"><span data-stu-id="0d7be-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d7be-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d7be-180">Link-Id</span></span>                | <span data-ttu-id="0d7be-181">2015</span><span class="sxs-lookup"><span data-stu-id="0d7be-181">2015</span></span>                            |
| <span data-ttu-id="0d7be-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d7be-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d7be-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d7be-183">System-Only</span></span>            | <span data-ttu-id="0d7be-184">對</span><span class="sxs-lookup"><span data-stu-id="0d7be-184">True</span></span>                            |
| <span data-ttu-id="0d7be-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d7be-185">Is-Single-Valued</span></span>       | <span data-ttu-id="0d7be-186">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-186">False</span></span>                           |
| <span data-ttu-id="0d7be-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d7be-187">Is Indexed</span></span>             | <span data-ttu-id="0d7be-188">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-188">False</span></span>                           |
| <span data-ttu-id="0d7be-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d7be-189">In Global Catalog</span></span>      | <span data-ttu-id="0d7be-190">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-190">False</span></span>                           |
| <span data-ttu-id="0d7be-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d7be-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d7be-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d7be-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d7be-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d7be-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0d7be-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d7be-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0d7be-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-195">Search-Flags</span></span>           | <span data-ttu-id="0d7be-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d7be-196">0x00000000</span></span>                      |
| <span data-ttu-id="0d7be-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-197">System-Flags</span></span>           | <span data-ttu-id="0d7be-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d7be-198">0x00000010</span></span>                      |
| <span data-ttu-id="0d7be-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d7be-199">Classes used in</span></span>        | [<span data-ttu-id="0d7be-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0d7be-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0d7be-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0d7be-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0d7be-202">進入</span><span class="sxs-lookup"><span data-stu-id="0d7be-202">Entry</span></span> | <span data-ttu-id="0d7be-203">值</span><span class="sxs-lookup"><span data-stu-id="0d7be-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d7be-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d7be-204">Link-Id</span></span>                | <span data-ttu-id="0d7be-205">2015</span><span class="sxs-lookup"><span data-stu-id="0d7be-205">2015</span></span>                            |
| <span data-ttu-id="0d7be-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d7be-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d7be-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d7be-207">System-Only</span></span>            | <span data-ttu-id="0d7be-208">對</span><span class="sxs-lookup"><span data-stu-id="0d7be-208">True</span></span>                            |
| <span data-ttu-id="0d7be-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d7be-209">Is-Single-Valued</span></span>       | <span data-ttu-id="0d7be-210">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-210">False</span></span>                           |
| <span data-ttu-id="0d7be-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d7be-211">Is Indexed</span></span>             | <span data-ttu-id="0d7be-212">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-212">False</span></span>                           |
| <span data-ttu-id="0d7be-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d7be-213">In Global Catalog</span></span>      | <span data-ttu-id="0d7be-214">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-214">False</span></span>                           |
| <span data-ttu-id="0d7be-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d7be-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d7be-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d7be-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d7be-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d7be-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0d7be-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d7be-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0d7be-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-219">Search-Flags</span></span>           | <span data-ttu-id="0d7be-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d7be-220">0x00000000</span></span>                      |
| <span data-ttu-id="0d7be-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-221">System-Flags</span></span>           | <span data-ttu-id="0d7be-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d7be-222">0x00000010</span></span>                      |
| <span data-ttu-id="0d7be-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d7be-223">Classes used in</span></span>        | [<span data-ttu-id="0d7be-224">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0d7be-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0d7be-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d7be-225">Windows Server 2012</span></span>



| <span data-ttu-id="0d7be-226">進入</span><span class="sxs-lookup"><span data-stu-id="0d7be-226">Entry</span></span> | <span data-ttu-id="0d7be-227">值</span><span class="sxs-lookup"><span data-stu-id="0d7be-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d7be-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0d7be-228">Link-Id</span></span>                | <span data-ttu-id="0d7be-229">2015</span><span class="sxs-lookup"><span data-stu-id="0d7be-229">2015</span></span>                            |
| <span data-ttu-id="0d7be-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d7be-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d7be-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d7be-231">System-Only</span></span>            | <span data-ttu-id="0d7be-232">對</span><span class="sxs-lookup"><span data-stu-id="0d7be-232">True</span></span>                            |
| <span data-ttu-id="0d7be-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0d7be-233">Is-Single-Valued</span></span>       | <span data-ttu-id="0d7be-234">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-234">False</span></span>                           |
| <span data-ttu-id="0d7be-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0d7be-235">Is Indexed</span></span>             | <span data-ttu-id="0d7be-236">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-236">False</span></span>                           |
| <span data-ttu-id="0d7be-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0d7be-237">In Global Catalog</span></span>      | <span data-ttu-id="0d7be-238">否</span><span class="sxs-lookup"><span data-stu-id="0d7be-238">False</span></span>                           |
| <span data-ttu-id="0d7be-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0d7be-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d7be-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0d7be-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d7be-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d7be-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0d7be-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d7be-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0d7be-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-243">Search-Flags</span></span>           | <span data-ttu-id="0d7be-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d7be-244">0x00000000</span></span>                      |
| <span data-ttu-id="0d7be-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d7be-245">System-Flags</span></span>           | <span data-ttu-id="0d7be-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d7be-246">0x00000010</span></span>                      |
| <span data-ttu-id="0d7be-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0d7be-247">Classes used in</span></span>        | [<span data-ttu-id="0d7be-248">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0d7be-248">**Top**</span></span>](c-top.md)<br/> |



 

 






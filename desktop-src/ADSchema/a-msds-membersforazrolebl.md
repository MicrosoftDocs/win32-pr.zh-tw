---
title: BL 屬性的 ms DS-成員
description: 從成員應用程式群組或使用者到連結的 Az-Role 物件的反向連結。
ms.assetid: dcee8af0-6055-4569-a25e-d49e5ec02fee
ms.tgt_platform: multiple
keywords:
- BL 屬性 AD 架構的 ms DS-成員
- MembersForAzRoleBL 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Members-For-Az-Role-BL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258d198ca4931aa6fdc19fffda0e4dd234013a59
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467282"
---
# <a name="ms-ds-members-for-az-role-bl-attribute"></a><span data-ttu-id="8d099-105">BL 屬性的 ms DS-成員</span><span class="sxs-lookup"><span data-stu-id="8d099-105">ms-DS-Members-For-Az-Role-BL attribute</span></span>

<span data-ttu-id="8d099-106">從成員應用程式群組或使用者到連結的 Az-Role 物件的反向連結。</span><span class="sxs-lookup"><span data-stu-id="8d099-106">Backward link from member application group or user to Az-Role objects linking to it.</span></span>



| <span data-ttu-id="8d099-107">進入</span><span class="sxs-lookup"><span data-stu-id="8d099-107">Entry</span></span> | <span data-ttu-id="8d099-108">值</span><span class="sxs-lookup"><span data-stu-id="8d099-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="8d099-109">CN</span><span class="sxs-lookup"><span data-stu-id="8d099-109">CN</span></span>                | <span data-ttu-id="8d099-110">ms DS-成員--Az-Role-BL</span><span class="sxs-lookup"><span data-stu-id="8d099-110">ms-DS-Members-For-Az-Role-BL</span></span>            |
| <span data-ttu-id="8d099-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8d099-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8d099-112">MembersForAzRoleBL</span><span class="sxs-lookup"><span data-stu-id="8d099-112">msDS-MembersForAzRoleBL</span></span>                 |
| <span data-ttu-id="8d099-113">大小</span><span class="sxs-lookup"><span data-stu-id="8d099-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="8d099-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8d099-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="8d099-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8d099-115">Update Frequency</span></span>  | <span data-ttu-id="8d099-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="8d099-116">This value is set by the system.</span></span>        |
| <span data-ttu-id="8d099-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8d099-117">Attribute-Id</span></span>      | <span data-ttu-id="8d099-118">1.2.840.113556.1.4.1807</span><span class="sxs-lookup"><span data-stu-id="8d099-118">1.2.840.113556.1.4.1807</span></span>                 |
| <span data-ttu-id="8d099-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8d099-119">System-Id-Guid</span></span>    | <span data-ttu-id="8d099-120">ececcd20-a7e0-4688-9ccf-02ece5e287f5</span><span class="sxs-lookup"><span data-stu-id="8d099-120">ececcd20-a7e0-4688-9ccf-02ece5e287f5</span></span>    |
| <span data-ttu-id="8d099-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d099-121">Syntax</span></span>            | [<span data-ttu-id="8d099-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8d099-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="8d099-123">實作</span><span class="sxs-lookup"><span data-stu-id="8d099-123">Implementations</span></span>

-   [<span data-ttu-id="8d099-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8d099-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8d099-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8d099-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8d099-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8d099-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8d099-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8d099-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8d099-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8d099-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8d099-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8d099-129">Windows Server 2003</span></span>



| <span data-ttu-id="8d099-130">進入</span><span class="sxs-lookup"><span data-stu-id="8d099-130">Entry</span></span> | <span data-ttu-id="8d099-131">值</span><span class="sxs-lookup"><span data-stu-id="8d099-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8d099-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d099-132">Link-Id</span></span>                | <span data-ttu-id="8d099-133">2017</span><span class="sxs-lookup"><span data-stu-id="8d099-133">2017</span></span>                            |
| <span data-ttu-id="8d099-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d099-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8d099-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d099-135">System-Only</span></span>            | <span data-ttu-id="8d099-136">對</span><span class="sxs-lookup"><span data-stu-id="8d099-136">True</span></span>                            |
| <span data-ttu-id="8d099-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d099-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8d099-138">否</span><span class="sxs-lookup"><span data-stu-id="8d099-138">False</span></span>                           |
| <span data-ttu-id="8d099-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d099-139">Is Indexed</span></span>             | <span data-ttu-id="8d099-140">否</span><span class="sxs-lookup"><span data-stu-id="8d099-140">False</span></span>                           |
| <span data-ttu-id="8d099-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d099-141">In Global Catalog</span></span>      | <span data-ttu-id="8d099-142">否</span><span class="sxs-lookup"><span data-stu-id="8d099-142">False</span></span>                           |
| <span data-ttu-id="8d099-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d099-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d099-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d099-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8d099-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d099-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8d099-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d099-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8d099-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-147">Search-Flags</span></span>           | <span data-ttu-id="8d099-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d099-148">0x00000000</span></span>                      |
| <span data-ttu-id="8d099-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-149">System-Flags</span></span>           | <span data-ttu-id="8d099-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d099-150">0x00000010</span></span>                      |
| <span data-ttu-id="8d099-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d099-151">Classes used in</span></span>        | [<span data-ttu-id="8d099-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8d099-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8d099-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8d099-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8d099-154">進入</span><span class="sxs-lookup"><span data-stu-id="8d099-154">Entry</span></span> | <span data-ttu-id="8d099-155">值</span><span class="sxs-lookup"><span data-stu-id="8d099-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8d099-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d099-156">Link-Id</span></span>                | <span data-ttu-id="8d099-157">2017</span><span class="sxs-lookup"><span data-stu-id="8d099-157">2017</span></span>                            |
| <span data-ttu-id="8d099-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d099-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8d099-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d099-159">System-Only</span></span>            | <span data-ttu-id="8d099-160">對</span><span class="sxs-lookup"><span data-stu-id="8d099-160">True</span></span>                            |
| <span data-ttu-id="8d099-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d099-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8d099-162">否</span><span class="sxs-lookup"><span data-stu-id="8d099-162">False</span></span>                           |
| <span data-ttu-id="8d099-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d099-163">Is Indexed</span></span>             | <span data-ttu-id="8d099-164">否</span><span class="sxs-lookup"><span data-stu-id="8d099-164">False</span></span>                           |
| <span data-ttu-id="8d099-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d099-165">In Global Catalog</span></span>      | <span data-ttu-id="8d099-166">否</span><span class="sxs-lookup"><span data-stu-id="8d099-166">False</span></span>                           |
| <span data-ttu-id="8d099-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d099-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d099-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d099-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8d099-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d099-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8d099-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d099-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8d099-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-171">Search-Flags</span></span>           | <span data-ttu-id="8d099-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d099-172">0x00000000</span></span>                      |
| <span data-ttu-id="8d099-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-173">System-Flags</span></span>           | <span data-ttu-id="8d099-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d099-174">0x00000010</span></span>                      |
| <span data-ttu-id="8d099-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d099-175">Classes used in</span></span>        | [<span data-ttu-id="8d099-176">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8d099-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8d099-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d099-177">Windows Server 2008</span></span>



| <span data-ttu-id="8d099-178">進入</span><span class="sxs-lookup"><span data-stu-id="8d099-178">Entry</span></span> | <span data-ttu-id="8d099-179">值</span><span class="sxs-lookup"><span data-stu-id="8d099-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8d099-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d099-180">Link-Id</span></span>                | <span data-ttu-id="8d099-181">2017</span><span class="sxs-lookup"><span data-stu-id="8d099-181">2017</span></span>                            |
| <span data-ttu-id="8d099-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d099-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8d099-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d099-183">System-Only</span></span>            | <span data-ttu-id="8d099-184">對</span><span class="sxs-lookup"><span data-stu-id="8d099-184">True</span></span>                            |
| <span data-ttu-id="8d099-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d099-185">Is-Single-Valued</span></span>       | <span data-ttu-id="8d099-186">否</span><span class="sxs-lookup"><span data-stu-id="8d099-186">False</span></span>                           |
| <span data-ttu-id="8d099-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d099-187">Is Indexed</span></span>             | <span data-ttu-id="8d099-188">否</span><span class="sxs-lookup"><span data-stu-id="8d099-188">False</span></span>                           |
| <span data-ttu-id="8d099-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d099-189">In Global Catalog</span></span>      | <span data-ttu-id="8d099-190">否</span><span class="sxs-lookup"><span data-stu-id="8d099-190">False</span></span>                           |
| <span data-ttu-id="8d099-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d099-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d099-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d099-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8d099-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d099-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8d099-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d099-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8d099-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-195">Search-Flags</span></span>           | <span data-ttu-id="8d099-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d099-196">0x00000000</span></span>                      |
| <span data-ttu-id="8d099-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-197">System-Flags</span></span>           | <span data-ttu-id="8d099-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d099-198">0x00000010</span></span>                      |
| <span data-ttu-id="8d099-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d099-199">Classes used in</span></span>        | [<span data-ttu-id="8d099-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8d099-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8d099-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d099-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8d099-202">進入</span><span class="sxs-lookup"><span data-stu-id="8d099-202">Entry</span></span> | <span data-ttu-id="8d099-203">值</span><span class="sxs-lookup"><span data-stu-id="8d099-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8d099-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d099-204">Link-Id</span></span>                | <span data-ttu-id="8d099-205">2017</span><span class="sxs-lookup"><span data-stu-id="8d099-205">2017</span></span>                            |
| <span data-ttu-id="8d099-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d099-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8d099-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d099-207">System-Only</span></span>            | <span data-ttu-id="8d099-208">對</span><span class="sxs-lookup"><span data-stu-id="8d099-208">True</span></span>                            |
| <span data-ttu-id="8d099-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d099-209">Is-Single-Valued</span></span>       | <span data-ttu-id="8d099-210">否</span><span class="sxs-lookup"><span data-stu-id="8d099-210">False</span></span>                           |
| <span data-ttu-id="8d099-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d099-211">Is Indexed</span></span>             | <span data-ttu-id="8d099-212">否</span><span class="sxs-lookup"><span data-stu-id="8d099-212">False</span></span>                           |
| <span data-ttu-id="8d099-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d099-213">In Global Catalog</span></span>      | <span data-ttu-id="8d099-214">否</span><span class="sxs-lookup"><span data-stu-id="8d099-214">False</span></span>                           |
| <span data-ttu-id="8d099-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d099-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d099-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d099-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8d099-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d099-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8d099-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d099-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8d099-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-219">Search-Flags</span></span>           | <span data-ttu-id="8d099-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d099-220">0x00000000</span></span>                      |
| <span data-ttu-id="8d099-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-221">System-Flags</span></span>           | <span data-ttu-id="8d099-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d099-222">0x00000010</span></span>                      |
| <span data-ttu-id="8d099-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d099-223">Classes used in</span></span>        | [<span data-ttu-id="8d099-224">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8d099-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8d099-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d099-225">Windows Server 2012</span></span>



| <span data-ttu-id="8d099-226">進入</span><span class="sxs-lookup"><span data-stu-id="8d099-226">Entry</span></span> | <span data-ttu-id="8d099-227">值</span><span class="sxs-lookup"><span data-stu-id="8d099-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8d099-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d099-228">Link-Id</span></span>                | <span data-ttu-id="8d099-229">2017</span><span class="sxs-lookup"><span data-stu-id="8d099-229">2017</span></span>                            |
| <span data-ttu-id="8d099-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d099-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8d099-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d099-231">System-Only</span></span>            | <span data-ttu-id="8d099-232">對</span><span class="sxs-lookup"><span data-stu-id="8d099-232">True</span></span>                            |
| <span data-ttu-id="8d099-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d099-233">Is-Single-Valued</span></span>       | <span data-ttu-id="8d099-234">否</span><span class="sxs-lookup"><span data-stu-id="8d099-234">False</span></span>                           |
| <span data-ttu-id="8d099-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d099-235">Is Indexed</span></span>             | <span data-ttu-id="8d099-236">否</span><span class="sxs-lookup"><span data-stu-id="8d099-236">False</span></span>                           |
| <span data-ttu-id="8d099-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d099-237">In Global Catalog</span></span>      | <span data-ttu-id="8d099-238">否</span><span class="sxs-lookup"><span data-stu-id="8d099-238">False</span></span>                           |
| <span data-ttu-id="8d099-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d099-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d099-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d099-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8d099-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d099-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8d099-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d099-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8d099-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-243">Search-Flags</span></span>           | <span data-ttu-id="8d099-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d099-244">0x00000000</span></span>                      |
| <span data-ttu-id="8d099-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d099-245">System-Flags</span></span>           | <span data-ttu-id="8d099-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d099-246">0x00000010</span></span>                      |
| <span data-ttu-id="8d099-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d099-247">Classes used in</span></span>        | [<span data-ttu-id="8d099-248">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8d099-248">**Top**</span></span>](c-top.md)<br/> |



 

 






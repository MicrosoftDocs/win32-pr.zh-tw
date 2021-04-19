---
title: Managed-Objects 屬性
description: 包含由使用者管理的物件清單。 列出的物件是屬性 managedBy 屬性設定為此使用者的物件。 清單中的每個專案都是 managed 物件的連結參考。
ms.assetid: 59b76431-03a5-4839-8800-ef03d26b66cc
ms.tgt_platform: multiple
keywords:
- Managed-Objects 屬性 AD 架構
- Managedobjects 之下屬性 AD 架構
topic_type:
- apiref
api_name:
- Managed-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c7bc489d11c99f8790426a531e09a20f133476
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971062"
---
# <a name="managed-objects-attribute"></a><span data-ttu-id="02175-107">Managed-Objects 屬性</span><span class="sxs-lookup"><span data-stu-id="02175-107">Managed-Objects attribute</span></span>

<span data-ttu-id="02175-108">包含由使用者管理的物件清單。</span><span class="sxs-lookup"><span data-stu-id="02175-108">Contains the list of objects that are managed by the user.</span></span> <span data-ttu-id="02175-109">列出的物件是屬性 managedBy 屬性設定為此使用者的物件。</span><span class="sxs-lookup"><span data-stu-id="02175-109">The objects listed are those that have the property managedBy property set to this user.</span></span> <span data-ttu-id="02175-110">清單中的每個專案都是 managed 物件的連結參考。</span><span class="sxs-lookup"><span data-stu-id="02175-110">Each item in the list is a linked reference to the managed object.</span></span>



| <span data-ttu-id="02175-111">進入</span><span class="sxs-lookup"><span data-stu-id="02175-111">Entry</span></span> | <span data-ttu-id="02175-112">值</span><span class="sxs-lookup"><span data-stu-id="02175-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02175-113">CN</span><span class="sxs-lookup"><span data-stu-id="02175-113">CN</span></span>                | <span data-ttu-id="02175-114">Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="02175-114">Managed-Objects</span></span>                                                                    |
| <span data-ttu-id="02175-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="02175-115">Ldap-Display-Name</span></span> | <span data-ttu-id="02175-116">Managedobjects 之下</span><span class="sxs-lookup"><span data-stu-id="02175-116">managedObjects</span></span>                                                                     |
| <span data-ttu-id="02175-117">大小</span><span class="sxs-lookup"><span data-stu-id="02175-117">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="02175-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="02175-118">Update Privilege</span></span>  | <span data-ttu-id="02175-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="02175-119">This value is set by the system.</span></span>                                                   |
| <span data-ttu-id="02175-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="02175-120">Update Frequency</span></span>  | <span data-ttu-id="02175-121">當使用者記錄建立時，以及每當受管理物件需要變更時。</span><span class="sxs-lookup"><span data-stu-id="02175-121">When the users record is created and whenever the managed objects needs to change.</span></span> |
| <span data-ttu-id="02175-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="02175-122">Attribute-Id</span></span>      | <span data-ttu-id="02175-123">1.2.840.113556.1.4.654</span><span class="sxs-lookup"><span data-stu-id="02175-123">1.2.840.113556.1.4.654</span></span>                                                             |
| <span data-ttu-id="02175-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="02175-124">System-Id-Guid</span></span>    | <span data-ttu-id="02175-125">0296c124-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="02175-125">0296c124-40da-11d1-a9c0-0000f80367c1</span></span>                                               |
| <span data-ttu-id="02175-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="02175-126">Syntax</span></span>            | [<span data-ttu-id="02175-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="02175-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                            |



## <a name="implementations"></a><span data-ttu-id="02175-128">實作</span><span class="sxs-lookup"><span data-stu-id="02175-128">Implementations</span></span>

-   [<span data-ttu-id="02175-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="02175-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="02175-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="02175-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="02175-131">**亞當**</span><span class="sxs-lookup"><span data-stu-id="02175-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="02175-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="02175-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="02175-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="02175-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="02175-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="02175-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="02175-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="02175-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="02175-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="02175-136">Windows 2000 Server</span></span>



| <span data-ttu-id="02175-137">進入</span><span class="sxs-lookup"><span data-stu-id="02175-137">Entry</span></span> | <span data-ttu-id="02175-138">值</span><span class="sxs-lookup"><span data-stu-id="02175-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02175-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="02175-139">Link-Id</span></span>                | <span data-ttu-id="02175-140">73</span><span class="sxs-lookup"><span data-stu-id="02175-140">73</span></span>                              |
| <span data-ttu-id="02175-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02175-141">MAPI-Id</span></span>                | <span data-ttu-id="02175-142">0x8024</span><span class="sxs-lookup"><span data-stu-id="02175-142">0x8024</span></span>                          |
| <span data-ttu-id="02175-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="02175-143">System-Only</span></span>            | <span data-ttu-id="02175-144">對</span><span class="sxs-lookup"><span data-stu-id="02175-144">True</span></span>                            |
| <span data-ttu-id="02175-145">是-單一值</span><span class="sxs-lookup"><span data-stu-id="02175-145">Is-Single-Valued</span></span>       | <span data-ttu-id="02175-146">否</span><span class="sxs-lookup"><span data-stu-id="02175-146">False</span></span>                           |
| <span data-ttu-id="02175-147">已編制索引</span><span class="sxs-lookup"><span data-stu-id="02175-147">Is Indexed</span></span>             | <span data-ttu-id="02175-148">否</span><span class="sxs-lookup"><span data-stu-id="02175-148">False</span></span>                           |
| <span data-ttu-id="02175-149">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="02175-149">In Global Catalog</span></span>      | <span data-ttu-id="02175-150">否</span><span class="sxs-lookup"><span data-stu-id="02175-150">False</span></span>                           |
| <span data-ttu-id="02175-151">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="02175-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="02175-152">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="02175-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02175-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02175-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02175-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02175-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02175-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-155">Search-Flags</span></span>           | <span data-ttu-id="02175-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02175-156">0x00000000</span></span>                      |
| <span data-ttu-id="02175-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-157">System-Flags</span></span>           | <span data-ttu-id="02175-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02175-158">0x00000010</span></span>                      |
| <span data-ttu-id="02175-159">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="02175-159">Classes used in</span></span>        | [<span data-ttu-id="02175-160">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="02175-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="02175-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="02175-161">Windows Server 2003</span></span>



| <span data-ttu-id="02175-162">進入</span><span class="sxs-lookup"><span data-stu-id="02175-162">Entry</span></span> | <span data-ttu-id="02175-163">值</span><span class="sxs-lookup"><span data-stu-id="02175-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02175-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="02175-164">Link-Id</span></span>                | <span data-ttu-id="02175-165">73</span><span class="sxs-lookup"><span data-stu-id="02175-165">73</span></span>                              |
| <span data-ttu-id="02175-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02175-166">MAPI-Id</span></span>                | <span data-ttu-id="02175-167">0x8024</span><span class="sxs-lookup"><span data-stu-id="02175-167">0x8024</span></span>                          |
| <span data-ttu-id="02175-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="02175-168">System-Only</span></span>            | <span data-ttu-id="02175-169">對</span><span class="sxs-lookup"><span data-stu-id="02175-169">True</span></span>                            |
| <span data-ttu-id="02175-170">是-單一值</span><span class="sxs-lookup"><span data-stu-id="02175-170">Is-Single-Valued</span></span>       | <span data-ttu-id="02175-171">否</span><span class="sxs-lookup"><span data-stu-id="02175-171">False</span></span>                           |
| <span data-ttu-id="02175-172">已編制索引</span><span class="sxs-lookup"><span data-stu-id="02175-172">Is Indexed</span></span>             | <span data-ttu-id="02175-173">否</span><span class="sxs-lookup"><span data-stu-id="02175-173">False</span></span>                           |
| <span data-ttu-id="02175-174">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="02175-174">In Global Catalog</span></span>      | <span data-ttu-id="02175-175">否</span><span class="sxs-lookup"><span data-stu-id="02175-175">False</span></span>                           |
| <span data-ttu-id="02175-176">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="02175-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="02175-177">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="02175-177">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02175-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02175-178">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02175-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02175-179">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02175-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-180">Search-Flags</span></span>           | <span data-ttu-id="02175-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02175-181">0x00000000</span></span>                      |
| <span data-ttu-id="02175-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-182">System-Flags</span></span>           | <span data-ttu-id="02175-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02175-183">0x00000010</span></span>                      |
| <span data-ttu-id="02175-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="02175-184">Classes used in</span></span>        | [<span data-ttu-id="02175-185">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="02175-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="02175-186">亞當</span><span class="sxs-lookup"><span data-stu-id="02175-186">ADAM</span></span>



| <span data-ttu-id="02175-187">進入</span><span class="sxs-lookup"><span data-stu-id="02175-187">Entry</span></span> | <span data-ttu-id="02175-188">值</span><span class="sxs-lookup"><span data-stu-id="02175-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02175-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="02175-189">Link-Id</span></span>                | <span data-ttu-id="02175-190">73</span><span class="sxs-lookup"><span data-stu-id="02175-190">73</span></span>                              |
| <span data-ttu-id="02175-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02175-191">MAPI-Id</span></span>                | <span data-ttu-id="02175-192">0x8024</span><span class="sxs-lookup"><span data-stu-id="02175-192">0x8024</span></span>                          |
| <span data-ttu-id="02175-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="02175-193">System-Only</span></span>            | <span data-ttu-id="02175-194">對</span><span class="sxs-lookup"><span data-stu-id="02175-194">True</span></span>                            |
| <span data-ttu-id="02175-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="02175-195">Is-Single-Valued</span></span>       | <span data-ttu-id="02175-196">否</span><span class="sxs-lookup"><span data-stu-id="02175-196">False</span></span>                           |
| <span data-ttu-id="02175-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="02175-197">Is Indexed</span></span>             | <span data-ttu-id="02175-198">否</span><span class="sxs-lookup"><span data-stu-id="02175-198">False</span></span>                           |
| <span data-ttu-id="02175-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="02175-199">In Global Catalog</span></span>      | <span data-ttu-id="02175-200">否</span><span class="sxs-lookup"><span data-stu-id="02175-200">False</span></span>                           |
| <span data-ttu-id="02175-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="02175-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="02175-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="02175-202">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02175-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02175-203">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02175-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02175-204">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02175-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-205">Search-Flags</span></span>           | <span data-ttu-id="02175-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02175-206">0x00000000</span></span>                      |
| <span data-ttu-id="02175-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-207">System-Flags</span></span>           | <span data-ttu-id="02175-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02175-208">0x00000010</span></span>                      |
| <span data-ttu-id="02175-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="02175-209">Classes used in</span></span>        | [<span data-ttu-id="02175-210">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="02175-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="02175-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="02175-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="02175-212">進入</span><span class="sxs-lookup"><span data-stu-id="02175-212">Entry</span></span> | <span data-ttu-id="02175-213">值</span><span class="sxs-lookup"><span data-stu-id="02175-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02175-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="02175-214">Link-Id</span></span>                | <span data-ttu-id="02175-215">73</span><span class="sxs-lookup"><span data-stu-id="02175-215">73</span></span>                              |
| <span data-ttu-id="02175-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02175-216">MAPI-Id</span></span>                | <span data-ttu-id="02175-217">0x8024</span><span class="sxs-lookup"><span data-stu-id="02175-217">0x8024</span></span>                          |
| <span data-ttu-id="02175-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="02175-218">System-Only</span></span>            | <span data-ttu-id="02175-219">對</span><span class="sxs-lookup"><span data-stu-id="02175-219">True</span></span>                            |
| <span data-ttu-id="02175-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="02175-220">Is-Single-Valued</span></span>       | <span data-ttu-id="02175-221">否</span><span class="sxs-lookup"><span data-stu-id="02175-221">False</span></span>                           |
| <span data-ttu-id="02175-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="02175-222">Is Indexed</span></span>             | <span data-ttu-id="02175-223">否</span><span class="sxs-lookup"><span data-stu-id="02175-223">False</span></span>                           |
| <span data-ttu-id="02175-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="02175-224">In Global Catalog</span></span>      | <span data-ttu-id="02175-225">否</span><span class="sxs-lookup"><span data-stu-id="02175-225">False</span></span>                           |
| <span data-ttu-id="02175-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="02175-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="02175-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="02175-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02175-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02175-228">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02175-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02175-229">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02175-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-230">Search-Flags</span></span>           | <span data-ttu-id="02175-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02175-231">0x00000000</span></span>                      |
| <span data-ttu-id="02175-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-232">System-Flags</span></span>           | <span data-ttu-id="02175-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02175-233">0x00000010</span></span>                      |
| <span data-ttu-id="02175-234">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="02175-234">Classes used in</span></span>        | [<span data-ttu-id="02175-235">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="02175-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="02175-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02175-236">Windows Server 2008</span></span>



| <span data-ttu-id="02175-237">進入</span><span class="sxs-lookup"><span data-stu-id="02175-237">Entry</span></span> | <span data-ttu-id="02175-238">值</span><span class="sxs-lookup"><span data-stu-id="02175-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02175-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="02175-239">Link-Id</span></span>                | <span data-ttu-id="02175-240">73</span><span class="sxs-lookup"><span data-stu-id="02175-240">73</span></span>                              |
| <span data-ttu-id="02175-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02175-241">MAPI-Id</span></span>                | <span data-ttu-id="02175-242">0x8024</span><span class="sxs-lookup"><span data-stu-id="02175-242">0x8024</span></span>                          |
| <span data-ttu-id="02175-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="02175-243">System-Only</span></span>            | <span data-ttu-id="02175-244">對</span><span class="sxs-lookup"><span data-stu-id="02175-244">True</span></span>                            |
| <span data-ttu-id="02175-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="02175-245">Is-Single-Valued</span></span>       | <span data-ttu-id="02175-246">否</span><span class="sxs-lookup"><span data-stu-id="02175-246">False</span></span>                           |
| <span data-ttu-id="02175-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="02175-247">Is Indexed</span></span>             | <span data-ttu-id="02175-248">否</span><span class="sxs-lookup"><span data-stu-id="02175-248">False</span></span>                           |
| <span data-ttu-id="02175-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="02175-249">In Global Catalog</span></span>      | <span data-ttu-id="02175-250">否</span><span class="sxs-lookup"><span data-stu-id="02175-250">False</span></span>                           |
| <span data-ttu-id="02175-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="02175-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="02175-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="02175-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02175-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02175-253">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02175-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02175-254">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02175-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-255">Search-Flags</span></span>           | <span data-ttu-id="02175-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02175-256">0x00000000</span></span>                      |
| <span data-ttu-id="02175-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-257">System-Flags</span></span>           | <span data-ttu-id="02175-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02175-258">0x00000010</span></span>                      |
| <span data-ttu-id="02175-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="02175-259">Classes used in</span></span>        | [<span data-ttu-id="02175-260">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="02175-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="02175-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="02175-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="02175-262">進入</span><span class="sxs-lookup"><span data-stu-id="02175-262">Entry</span></span> | <span data-ttu-id="02175-263">值</span><span class="sxs-lookup"><span data-stu-id="02175-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02175-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="02175-264">Link-Id</span></span>                | <span data-ttu-id="02175-265">73</span><span class="sxs-lookup"><span data-stu-id="02175-265">73</span></span>                              |
| <span data-ttu-id="02175-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02175-266">MAPI-Id</span></span>                | <span data-ttu-id="02175-267">0x8024</span><span class="sxs-lookup"><span data-stu-id="02175-267">0x8024</span></span>                          |
| <span data-ttu-id="02175-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="02175-268">System-Only</span></span>            | <span data-ttu-id="02175-269">對</span><span class="sxs-lookup"><span data-stu-id="02175-269">True</span></span>                            |
| <span data-ttu-id="02175-270">是-單一值</span><span class="sxs-lookup"><span data-stu-id="02175-270">Is-Single-Valued</span></span>       | <span data-ttu-id="02175-271">否</span><span class="sxs-lookup"><span data-stu-id="02175-271">False</span></span>                           |
| <span data-ttu-id="02175-272">已編制索引</span><span class="sxs-lookup"><span data-stu-id="02175-272">Is Indexed</span></span>             | <span data-ttu-id="02175-273">否</span><span class="sxs-lookup"><span data-stu-id="02175-273">False</span></span>                           |
| <span data-ttu-id="02175-274">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="02175-274">In Global Catalog</span></span>      | <span data-ttu-id="02175-275">否</span><span class="sxs-lookup"><span data-stu-id="02175-275">False</span></span>                           |
| <span data-ttu-id="02175-276">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="02175-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="02175-277">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="02175-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02175-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02175-278">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02175-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02175-279">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02175-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-280">Search-Flags</span></span>           | <span data-ttu-id="02175-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02175-281">0x00000000</span></span>                      |
| <span data-ttu-id="02175-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-282">System-Flags</span></span>           | <span data-ttu-id="02175-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02175-283">0x00000010</span></span>                      |
| <span data-ttu-id="02175-284">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="02175-284">Classes used in</span></span>        | [<span data-ttu-id="02175-285">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="02175-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="02175-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="02175-286">Windows Server 2012</span></span>



| <span data-ttu-id="02175-287">進入</span><span class="sxs-lookup"><span data-stu-id="02175-287">Entry</span></span> | <span data-ttu-id="02175-288">值</span><span class="sxs-lookup"><span data-stu-id="02175-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="02175-289">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="02175-289">Link-Id</span></span>                | <span data-ttu-id="02175-290">73</span><span class="sxs-lookup"><span data-stu-id="02175-290">73</span></span>                              |
| <span data-ttu-id="02175-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02175-291">MAPI-Id</span></span>                | <span data-ttu-id="02175-292">0x8024</span><span class="sxs-lookup"><span data-stu-id="02175-292">0x8024</span></span>                          |
| <span data-ttu-id="02175-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="02175-293">System-Only</span></span>            | <span data-ttu-id="02175-294">對</span><span class="sxs-lookup"><span data-stu-id="02175-294">True</span></span>                            |
| <span data-ttu-id="02175-295">是-單一值</span><span class="sxs-lookup"><span data-stu-id="02175-295">Is-Single-Valued</span></span>       | <span data-ttu-id="02175-296">否</span><span class="sxs-lookup"><span data-stu-id="02175-296">False</span></span>                           |
| <span data-ttu-id="02175-297">已編制索引</span><span class="sxs-lookup"><span data-stu-id="02175-297">Is Indexed</span></span>             | <span data-ttu-id="02175-298">否</span><span class="sxs-lookup"><span data-stu-id="02175-298">False</span></span>                           |
| <span data-ttu-id="02175-299">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="02175-299">In Global Catalog</span></span>      | <span data-ttu-id="02175-300">否</span><span class="sxs-lookup"><span data-stu-id="02175-300">False</span></span>                           |
| <span data-ttu-id="02175-301">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="02175-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="02175-302">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="02175-302">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="02175-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02175-303">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="02175-304">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02175-304">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="02175-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-305">Search-Flags</span></span>           | <span data-ttu-id="02175-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="02175-306">0x00000000</span></span>                      |
| <span data-ttu-id="02175-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02175-307">System-Flags</span></span>           | <span data-ttu-id="02175-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02175-308">0x00000010</span></span>                      |
| <span data-ttu-id="02175-309">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="02175-309">Classes used in</span></span>        | [<span data-ttu-id="02175-310">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="02175-310">**Top**</span></span>](c-top.md)<br/> |



 

 






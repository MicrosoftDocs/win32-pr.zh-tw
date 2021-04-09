---
title: FSMO 角色-擁有者屬性
description: 彈性的 Single-Master 操作可修改架構之 DC 的分辨名稱。
ms.assetid: 8eb28524-4bbf-453c-89ab-864ef94b0781
ms.tgt_platform: multiple
keywords:
- FSMO 角色-擁有者屬性 AD 架構
- fSMORoleOwner 屬性 AD 架構
topic_type:
- apiref
api_name:
- FSMO-Role-Owner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4439e5ee10fba11db831024d6b1958b75cd81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845256"
---
# <a name="fsmo-role-owner-attribute"></a><span data-ttu-id="21528-105">FSMO 角色-擁有者屬性</span><span class="sxs-lookup"><span data-stu-id="21528-105">FSMO-Role-Owner attribute</span></span>

<span data-ttu-id="21528-106">彈性的 Single-Master 作業：可以修改架構之 DC 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="21528-106">Flexible Single-Master Operation: The distinguished name of the DC where the schema can be modified.</span></span>



| <span data-ttu-id="21528-107">進入</span><span class="sxs-lookup"><span data-stu-id="21528-107">Entry</span></span> | <span data-ttu-id="21528-108">值</span><span class="sxs-lookup"><span data-stu-id="21528-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="21528-109">CN</span><span class="sxs-lookup"><span data-stu-id="21528-109">CN</span></span>                | <span data-ttu-id="21528-110">FSMO 角色-擁有者</span><span class="sxs-lookup"><span data-stu-id="21528-110">FSMO-Role-Owner</span></span>                         |
| <span data-ttu-id="21528-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="21528-111">Ldap-Display-Name</span></span> | <span data-ttu-id="21528-112">fSMORoleOwner</span><span class="sxs-lookup"><span data-stu-id="21528-112">fSMORoleOwner</span></span>                           |
| <span data-ttu-id="21528-113">大小</span><span class="sxs-lookup"><span data-stu-id="21528-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="21528-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="21528-114">Update Privilege</span></span>  | <span data-ttu-id="21528-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="21528-115">Schema administrator</span></span>                    |
| <span data-ttu-id="21528-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="21528-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="21528-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21528-117">Attribute-Id</span></span>      | <span data-ttu-id="21528-118">1.2.840.113556.1.4.369</span><span class="sxs-lookup"><span data-stu-id="21528-118">1.2.840.113556.1.4.369</span></span>                  |
| <span data-ttu-id="21528-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="21528-119">System-Id-Guid</span></span>    | <span data-ttu-id="21528-120">66171887-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="21528-120">66171887-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="21528-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="21528-121">Syntax</span></span>            | [<span data-ttu-id="21528-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="21528-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="21528-123">實作</span><span class="sxs-lookup"><span data-stu-id="21528-123">Implementations</span></span>

-   [<span data-ttu-id="21528-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="21528-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="21528-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="21528-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="21528-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="21528-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="21528-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="21528-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="21528-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21528-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21528-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21528-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21528-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21528-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="21528-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21528-131">Windows 2000 Server</span></span>



| <span data-ttu-id="21528-132">進入</span><span class="sxs-lookup"><span data-stu-id="21528-132">Entry</span></span> | <span data-ttu-id="21528-133">值</span><span class="sxs-lookup"><span data-stu-id="21528-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21528-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21528-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21528-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="21528-136">System-Only</span></span>            | <span data-ttu-id="21528-137">否</span><span class="sxs-lookup"><span data-stu-id="21528-137">False</span></span>                           |
| <span data-ttu-id="21528-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21528-138">Is-Single-Valued</span></span>       | <span data-ttu-id="21528-139">對</span><span class="sxs-lookup"><span data-stu-id="21528-139">True</span></span>                            |
| <span data-ttu-id="21528-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21528-140">Is Indexed</span></span>             | <span data-ttu-id="21528-141">對</span><span class="sxs-lookup"><span data-stu-id="21528-141">True</span></span>                            |
| <span data-ttu-id="21528-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21528-142">In Global Catalog</span></span>      | <span data-ttu-id="21528-143">否</span><span class="sxs-lookup"><span data-stu-id="21528-143">False</span></span>                           |
| <span data-ttu-id="21528-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21528-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="21528-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21528-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21528-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21528-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21528-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21528-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21528-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-148">Search-Flags</span></span>           | <span data-ttu-id="21528-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21528-149">0x00000001</span></span>                      |
| <span data-ttu-id="21528-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-150">System-Flags</span></span>           | <span data-ttu-id="21528-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21528-151">0x00000010</span></span>                      |
| <span data-ttu-id="21528-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21528-152">Classes used in</span></span>        | [<span data-ttu-id="21528-153">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="21528-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="21528-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21528-154">Windows Server 2003</span></span>



| <span data-ttu-id="21528-155">進入</span><span class="sxs-lookup"><span data-stu-id="21528-155">Entry</span></span> | <span data-ttu-id="21528-156">值</span><span class="sxs-lookup"><span data-stu-id="21528-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21528-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21528-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21528-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="21528-159">System-Only</span></span>            | <span data-ttu-id="21528-160">否</span><span class="sxs-lookup"><span data-stu-id="21528-160">False</span></span>                           |
| <span data-ttu-id="21528-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21528-161">Is-Single-Valued</span></span>       | <span data-ttu-id="21528-162">對</span><span class="sxs-lookup"><span data-stu-id="21528-162">True</span></span>                            |
| <span data-ttu-id="21528-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21528-163">Is Indexed</span></span>             | <span data-ttu-id="21528-164">對</span><span class="sxs-lookup"><span data-stu-id="21528-164">True</span></span>                            |
| <span data-ttu-id="21528-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21528-165">In Global Catalog</span></span>      | <span data-ttu-id="21528-166">否</span><span class="sxs-lookup"><span data-stu-id="21528-166">False</span></span>                           |
| <span data-ttu-id="21528-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21528-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="21528-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21528-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21528-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21528-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21528-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21528-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21528-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-171">Search-Flags</span></span>           | <span data-ttu-id="21528-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21528-172">0x00000001</span></span>                      |
| <span data-ttu-id="21528-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-173">System-Flags</span></span>           | <span data-ttu-id="21528-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21528-174">0x00000010</span></span>                      |
| <span data-ttu-id="21528-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21528-175">Classes used in</span></span>        | [<span data-ttu-id="21528-176">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="21528-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="21528-177">亞當</span><span class="sxs-lookup"><span data-stu-id="21528-177">ADAM</span></span>



| <span data-ttu-id="21528-178">進入</span><span class="sxs-lookup"><span data-stu-id="21528-178">Entry</span></span> | <span data-ttu-id="21528-179">值</span><span class="sxs-lookup"><span data-stu-id="21528-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21528-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21528-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21528-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="21528-182">System-Only</span></span>            | <span data-ttu-id="21528-183">否</span><span class="sxs-lookup"><span data-stu-id="21528-183">False</span></span>                           |
| <span data-ttu-id="21528-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21528-184">Is-Single-Valued</span></span>       | <span data-ttu-id="21528-185">對</span><span class="sxs-lookup"><span data-stu-id="21528-185">True</span></span>                            |
| <span data-ttu-id="21528-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21528-186">Is Indexed</span></span>             | <span data-ttu-id="21528-187">對</span><span class="sxs-lookup"><span data-stu-id="21528-187">True</span></span>                            |
| <span data-ttu-id="21528-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21528-188">In Global Catalog</span></span>      | <span data-ttu-id="21528-189">否</span><span class="sxs-lookup"><span data-stu-id="21528-189">False</span></span>                           |
| <span data-ttu-id="21528-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21528-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="21528-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21528-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21528-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21528-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21528-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21528-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21528-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-194">Search-Flags</span></span>           | <span data-ttu-id="21528-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21528-195">0x00000001</span></span>                      |
| <span data-ttu-id="21528-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-196">System-Flags</span></span>           | <span data-ttu-id="21528-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21528-197">0x00000010</span></span>                      |
| <span data-ttu-id="21528-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21528-198">Classes used in</span></span>        | [<span data-ttu-id="21528-199">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="21528-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="21528-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21528-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="21528-201">進入</span><span class="sxs-lookup"><span data-stu-id="21528-201">Entry</span></span> | <span data-ttu-id="21528-202">值</span><span class="sxs-lookup"><span data-stu-id="21528-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21528-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21528-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21528-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="21528-205">System-Only</span></span>            | <span data-ttu-id="21528-206">否</span><span class="sxs-lookup"><span data-stu-id="21528-206">False</span></span>                           |
| <span data-ttu-id="21528-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21528-207">Is-Single-Valued</span></span>       | <span data-ttu-id="21528-208">對</span><span class="sxs-lookup"><span data-stu-id="21528-208">True</span></span>                            |
| <span data-ttu-id="21528-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21528-209">Is Indexed</span></span>             | <span data-ttu-id="21528-210">對</span><span class="sxs-lookup"><span data-stu-id="21528-210">True</span></span>                            |
| <span data-ttu-id="21528-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21528-211">In Global Catalog</span></span>      | <span data-ttu-id="21528-212">否</span><span class="sxs-lookup"><span data-stu-id="21528-212">False</span></span>                           |
| <span data-ttu-id="21528-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21528-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="21528-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21528-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21528-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21528-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21528-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21528-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21528-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-217">Search-Flags</span></span>           | <span data-ttu-id="21528-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21528-218">0x00000001</span></span>                      |
| <span data-ttu-id="21528-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-219">System-Flags</span></span>           | <span data-ttu-id="21528-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21528-220">0x00000010</span></span>                      |
| <span data-ttu-id="21528-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21528-221">Classes used in</span></span>        | [<span data-ttu-id="21528-222">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="21528-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="21528-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21528-223">Windows Server 2008</span></span>



| <span data-ttu-id="21528-224">進入</span><span class="sxs-lookup"><span data-stu-id="21528-224">Entry</span></span> | <span data-ttu-id="21528-225">值</span><span class="sxs-lookup"><span data-stu-id="21528-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21528-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21528-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21528-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="21528-228">System-Only</span></span>            | <span data-ttu-id="21528-229">否</span><span class="sxs-lookup"><span data-stu-id="21528-229">False</span></span>                           |
| <span data-ttu-id="21528-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21528-230">Is-Single-Valued</span></span>       | <span data-ttu-id="21528-231">對</span><span class="sxs-lookup"><span data-stu-id="21528-231">True</span></span>                            |
| <span data-ttu-id="21528-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21528-232">Is Indexed</span></span>             | <span data-ttu-id="21528-233">對</span><span class="sxs-lookup"><span data-stu-id="21528-233">True</span></span>                            |
| <span data-ttu-id="21528-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21528-234">In Global Catalog</span></span>      | <span data-ttu-id="21528-235">否</span><span class="sxs-lookup"><span data-stu-id="21528-235">False</span></span>                           |
| <span data-ttu-id="21528-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21528-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="21528-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21528-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21528-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21528-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21528-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21528-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21528-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-240">Search-Flags</span></span>           | <span data-ttu-id="21528-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21528-241">0x00000001</span></span>                      |
| <span data-ttu-id="21528-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-242">System-Flags</span></span>           | <span data-ttu-id="21528-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21528-243">0x00000010</span></span>                      |
| <span data-ttu-id="21528-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21528-244">Classes used in</span></span>        | [<span data-ttu-id="21528-245">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="21528-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21528-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21528-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21528-247">進入</span><span class="sxs-lookup"><span data-stu-id="21528-247">Entry</span></span> | <span data-ttu-id="21528-248">值</span><span class="sxs-lookup"><span data-stu-id="21528-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21528-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21528-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21528-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="21528-251">System-Only</span></span>            | <span data-ttu-id="21528-252">否</span><span class="sxs-lookup"><span data-stu-id="21528-252">False</span></span>                           |
| <span data-ttu-id="21528-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21528-253">Is-Single-Valued</span></span>       | <span data-ttu-id="21528-254">對</span><span class="sxs-lookup"><span data-stu-id="21528-254">True</span></span>                            |
| <span data-ttu-id="21528-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21528-255">Is Indexed</span></span>             | <span data-ttu-id="21528-256">對</span><span class="sxs-lookup"><span data-stu-id="21528-256">True</span></span>                            |
| <span data-ttu-id="21528-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21528-257">In Global Catalog</span></span>      | <span data-ttu-id="21528-258">否</span><span class="sxs-lookup"><span data-stu-id="21528-258">False</span></span>                           |
| <span data-ttu-id="21528-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21528-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="21528-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21528-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21528-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21528-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21528-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21528-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21528-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-263">Search-Flags</span></span>           | <span data-ttu-id="21528-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21528-264">0x00000001</span></span>                      |
| <span data-ttu-id="21528-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-265">System-Flags</span></span>           | <span data-ttu-id="21528-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21528-266">0x00000010</span></span>                      |
| <span data-ttu-id="21528-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21528-267">Classes used in</span></span>        | [<span data-ttu-id="21528-268">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="21528-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="21528-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21528-269">Windows Server 2012</span></span>



| <span data-ttu-id="21528-270">進入</span><span class="sxs-lookup"><span data-stu-id="21528-270">Entry</span></span> | <span data-ttu-id="21528-271">值</span><span class="sxs-lookup"><span data-stu-id="21528-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="21528-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21528-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21528-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="21528-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="21528-274">System-Only</span></span>            | <span data-ttu-id="21528-275">否</span><span class="sxs-lookup"><span data-stu-id="21528-275">False</span></span>                           |
| <span data-ttu-id="21528-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21528-276">Is-Single-Valued</span></span>       | <span data-ttu-id="21528-277">對</span><span class="sxs-lookup"><span data-stu-id="21528-277">True</span></span>                            |
| <span data-ttu-id="21528-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21528-278">Is Indexed</span></span>             | <span data-ttu-id="21528-279">對</span><span class="sxs-lookup"><span data-stu-id="21528-279">True</span></span>                            |
| <span data-ttu-id="21528-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21528-280">In Global Catalog</span></span>      | <span data-ttu-id="21528-281">否</span><span class="sxs-lookup"><span data-stu-id="21528-281">False</span></span>                           |
| <span data-ttu-id="21528-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21528-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="21528-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21528-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="21528-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21528-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="21528-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21528-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="21528-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-286">Search-Flags</span></span>           | <span data-ttu-id="21528-287">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21528-287">0x00000001</span></span>                      |
| <span data-ttu-id="21528-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21528-288">System-Flags</span></span>           | <span data-ttu-id="21528-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21528-289">0x00000010</span></span>                      |
| <span data-ttu-id="21528-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21528-290">Classes used in</span></span>        | [<span data-ttu-id="21528-291">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="21528-291">**Top**</span></span>](c-top.md)<br/> |



 

 






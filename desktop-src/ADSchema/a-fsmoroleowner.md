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
# <a name="fsmo-role-owner-attribute"></a><span data-ttu-id="889d7-105">FSMO 角色-擁有者屬性</span><span class="sxs-lookup"><span data-stu-id="889d7-105">FSMO-Role-Owner attribute</span></span>

<span data-ttu-id="889d7-106">彈性的 Single-Master 作業：可以修改架構之 DC 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="889d7-106">Flexible Single-Master Operation: The distinguished name of the DC where the schema can be modified.</span></span>



| <span data-ttu-id="889d7-107">進入</span><span class="sxs-lookup"><span data-stu-id="889d7-107">Entry</span></span> | <span data-ttu-id="889d7-108">值</span><span class="sxs-lookup"><span data-stu-id="889d7-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="889d7-109">CN</span><span class="sxs-lookup"><span data-stu-id="889d7-109">CN</span></span>                | <span data-ttu-id="889d7-110">FSMO 角色-擁有者</span><span class="sxs-lookup"><span data-stu-id="889d7-110">FSMO-Role-Owner</span></span>                         |
| <span data-ttu-id="889d7-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="889d7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="889d7-112">fSMORoleOwner</span><span class="sxs-lookup"><span data-stu-id="889d7-112">fSMORoleOwner</span></span>                           |
| <span data-ttu-id="889d7-113">大小</span><span class="sxs-lookup"><span data-stu-id="889d7-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="889d7-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="889d7-114">Update Privilege</span></span>  | <span data-ttu-id="889d7-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="889d7-115">Schema administrator</span></span>                    |
| <span data-ttu-id="889d7-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="889d7-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="889d7-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="889d7-117">Attribute-Id</span></span>      | <span data-ttu-id="889d7-118">1.2.840.113556.1.4.369</span><span class="sxs-lookup"><span data-stu-id="889d7-118">1.2.840.113556.1.4.369</span></span>                  |
| <span data-ttu-id="889d7-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="889d7-119">System-Id-Guid</span></span>    | <span data-ttu-id="889d7-120">66171887-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="889d7-120">66171887-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="889d7-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="889d7-121">Syntax</span></span>            | [<span data-ttu-id="889d7-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="889d7-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="889d7-123">實作</span><span class="sxs-lookup"><span data-stu-id="889d7-123">Implementations</span></span>

-   [<span data-ttu-id="889d7-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="889d7-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="889d7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="889d7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="889d7-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="889d7-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="889d7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="889d7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="889d7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="889d7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="889d7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="889d7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="889d7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="889d7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="889d7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="889d7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="889d7-132">進入</span><span class="sxs-lookup"><span data-stu-id="889d7-132">Entry</span></span> | <span data-ttu-id="889d7-133">值</span><span class="sxs-lookup"><span data-stu-id="889d7-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="889d7-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889d7-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889d7-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="889d7-136">System-Only</span></span>            | <span data-ttu-id="889d7-137">否</span><span class="sxs-lookup"><span data-stu-id="889d7-137">False</span></span>                           |
| <span data-ttu-id="889d7-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889d7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="889d7-139">對</span><span class="sxs-lookup"><span data-stu-id="889d7-139">True</span></span>                            |
| <span data-ttu-id="889d7-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889d7-140">Is Indexed</span></span>             | <span data-ttu-id="889d7-141">對</span><span class="sxs-lookup"><span data-stu-id="889d7-141">True</span></span>                            |
| <span data-ttu-id="889d7-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889d7-142">In Global Catalog</span></span>      | <span data-ttu-id="889d7-143">否</span><span class="sxs-lookup"><span data-stu-id="889d7-143">False</span></span>                           |
| <span data-ttu-id="889d7-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889d7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="889d7-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889d7-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="889d7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889d7-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="889d7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889d7-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="889d7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-148">Search-Flags</span></span>           | <span data-ttu-id="889d7-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="889d7-149">0x00000001</span></span>                      |
| <span data-ttu-id="889d7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-150">System-Flags</span></span>           | <span data-ttu-id="889d7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889d7-151">0x00000010</span></span>                      |
| <span data-ttu-id="889d7-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889d7-152">Classes used in</span></span>        | [<span data-ttu-id="889d7-153">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="889d7-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="889d7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="889d7-154">Windows Server 2003</span></span>



| <span data-ttu-id="889d7-155">進入</span><span class="sxs-lookup"><span data-stu-id="889d7-155">Entry</span></span> | <span data-ttu-id="889d7-156">值</span><span class="sxs-lookup"><span data-stu-id="889d7-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="889d7-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889d7-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889d7-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="889d7-159">System-Only</span></span>            | <span data-ttu-id="889d7-160">否</span><span class="sxs-lookup"><span data-stu-id="889d7-160">False</span></span>                           |
| <span data-ttu-id="889d7-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889d7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="889d7-162">對</span><span class="sxs-lookup"><span data-stu-id="889d7-162">True</span></span>                            |
| <span data-ttu-id="889d7-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889d7-163">Is Indexed</span></span>             | <span data-ttu-id="889d7-164">對</span><span class="sxs-lookup"><span data-stu-id="889d7-164">True</span></span>                            |
| <span data-ttu-id="889d7-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889d7-165">In Global Catalog</span></span>      | <span data-ttu-id="889d7-166">否</span><span class="sxs-lookup"><span data-stu-id="889d7-166">False</span></span>                           |
| <span data-ttu-id="889d7-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889d7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="889d7-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889d7-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="889d7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889d7-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="889d7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889d7-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="889d7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-171">Search-Flags</span></span>           | <span data-ttu-id="889d7-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="889d7-172">0x00000001</span></span>                      |
| <span data-ttu-id="889d7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-173">System-Flags</span></span>           | <span data-ttu-id="889d7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889d7-174">0x00000010</span></span>                      |
| <span data-ttu-id="889d7-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889d7-175">Classes used in</span></span>        | [<span data-ttu-id="889d7-176">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="889d7-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="889d7-177">亞當</span><span class="sxs-lookup"><span data-stu-id="889d7-177">ADAM</span></span>



| <span data-ttu-id="889d7-178">進入</span><span class="sxs-lookup"><span data-stu-id="889d7-178">Entry</span></span> | <span data-ttu-id="889d7-179">值</span><span class="sxs-lookup"><span data-stu-id="889d7-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="889d7-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889d7-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889d7-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="889d7-182">System-Only</span></span>            | <span data-ttu-id="889d7-183">否</span><span class="sxs-lookup"><span data-stu-id="889d7-183">False</span></span>                           |
| <span data-ttu-id="889d7-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889d7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="889d7-185">對</span><span class="sxs-lookup"><span data-stu-id="889d7-185">True</span></span>                            |
| <span data-ttu-id="889d7-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889d7-186">Is Indexed</span></span>             | <span data-ttu-id="889d7-187">對</span><span class="sxs-lookup"><span data-stu-id="889d7-187">True</span></span>                            |
| <span data-ttu-id="889d7-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889d7-188">In Global Catalog</span></span>      | <span data-ttu-id="889d7-189">否</span><span class="sxs-lookup"><span data-stu-id="889d7-189">False</span></span>                           |
| <span data-ttu-id="889d7-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889d7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="889d7-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889d7-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="889d7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889d7-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="889d7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889d7-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="889d7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-194">Search-Flags</span></span>           | <span data-ttu-id="889d7-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="889d7-195">0x00000001</span></span>                      |
| <span data-ttu-id="889d7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-196">System-Flags</span></span>           | <span data-ttu-id="889d7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889d7-197">0x00000010</span></span>                      |
| <span data-ttu-id="889d7-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889d7-198">Classes used in</span></span>        | [<span data-ttu-id="889d7-199">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="889d7-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="889d7-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="889d7-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="889d7-201">進入</span><span class="sxs-lookup"><span data-stu-id="889d7-201">Entry</span></span> | <span data-ttu-id="889d7-202">值</span><span class="sxs-lookup"><span data-stu-id="889d7-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="889d7-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889d7-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889d7-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="889d7-205">System-Only</span></span>            | <span data-ttu-id="889d7-206">否</span><span class="sxs-lookup"><span data-stu-id="889d7-206">False</span></span>                           |
| <span data-ttu-id="889d7-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889d7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="889d7-208">對</span><span class="sxs-lookup"><span data-stu-id="889d7-208">True</span></span>                            |
| <span data-ttu-id="889d7-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889d7-209">Is Indexed</span></span>             | <span data-ttu-id="889d7-210">對</span><span class="sxs-lookup"><span data-stu-id="889d7-210">True</span></span>                            |
| <span data-ttu-id="889d7-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889d7-211">In Global Catalog</span></span>      | <span data-ttu-id="889d7-212">否</span><span class="sxs-lookup"><span data-stu-id="889d7-212">False</span></span>                           |
| <span data-ttu-id="889d7-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889d7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="889d7-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889d7-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="889d7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889d7-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="889d7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889d7-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="889d7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-217">Search-Flags</span></span>           | <span data-ttu-id="889d7-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="889d7-218">0x00000001</span></span>                      |
| <span data-ttu-id="889d7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-219">System-Flags</span></span>           | <span data-ttu-id="889d7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889d7-220">0x00000010</span></span>                      |
| <span data-ttu-id="889d7-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889d7-221">Classes used in</span></span>        | [<span data-ttu-id="889d7-222">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="889d7-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="889d7-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="889d7-223">Windows Server 2008</span></span>



| <span data-ttu-id="889d7-224">進入</span><span class="sxs-lookup"><span data-stu-id="889d7-224">Entry</span></span> | <span data-ttu-id="889d7-225">值</span><span class="sxs-lookup"><span data-stu-id="889d7-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="889d7-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889d7-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889d7-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="889d7-228">System-Only</span></span>            | <span data-ttu-id="889d7-229">否</span><span class="sxs-lookup"><span data-stu-id="889d7-229">False</span></span>                           |
| <span data-ttu-id="889d7-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889d7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="889d7-231">對</span><span class="sxs-lookup"><span data-stu-id="889d7-231">True</span></span>                            |
| <span data-ttu-id="889d7-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889d7-232">Is Indexed</span></span>             | <span data-ttu-id="889d7-233">對</span><span class="sxs-lookup"><span data-stu-id="889d7-233">True</span></span>                            |
| <span data-ttu-id="889d7-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889d7-234">In Global Catalog</span></span>      | <span data-ttu-id="889d7-235">否</span><span class="sxs-lookup"><span data-stu-id="889d7-235">False</span></span>                           |
| <span data-ttu-id="889d7-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889d7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="889d7-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889d7-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="889d7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889d7-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="889d7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889d7-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="889d7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-240">Search-Flags</span></span>           | <span data-ttu-id="889d7-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="889d7-241">0x00000001</span></span>                      |
| <span data-ttu-id="889d7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-242">System-Flags</span></span>           | <span data-ttu-id="889d7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889d7-243">0x00000010</span></span>                      |
| <span data-ttu-id="889d7-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889d7-244">Classes used in</span></span>        | [<span data-ttu-id="889d7-245">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="889d7-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="889d7-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="889d7-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="889d7-247">進入</span><span class="sxs-lookup"><span data-stu-id="889d7-247">Entry</span></span> | <span data-ttu-id="889d7-248">值</span><span class="sxs-lookup"><span data-stu-id="889d7-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="889d7-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889d7-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889d7-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="889d7-251">System-Only</span></span>            | <span data-ttu-id="889d7-252">否</span><span class="sxs-lookup"><span data-stu-id="889d7-252">False</span></span>                           |
| <span data-ttu-id="889d7-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889d7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="889d7-254">對</span><span class="sxs-lookup"><span data-stu-id="889d7-254">True</span></span>                            |
| <span data-ttu-id="889d7-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889d7-255">Is Indexed</span></span>             | <span data-ttu-id="889d7-256">對</span><span class="sxs-lookup"><span data-stu-id="889d7-256">True</span></span>                            |
| <span data-ttu-id="889d7-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889d7-257">In Global Catalog</span></span>      | <span data-ttu-id="889d7-258">否</span><span class="sxs-lookup"><span data-stu-id="889d7-258">False</span></span>                           |
| <span data-ttu-id="889d7-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889d7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="889d7-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889d7-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="889d7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889d7-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="889d7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889d7-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="889d7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-263">Search-Flags</span></span>           | <span data-ttu-id="889d7-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="889d7-264">0x00000001</span></span>                      |
| <span data-ttu-id="889d7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-265">System-Flags</span></span>           | <span data-ttu-id="889d7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889d7-266">0x00000010</span></span>                      |
| <span data-ttu-id="889d7-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889d7-267">Classes used in</span></span>        | [<span data-ttu-id="889d7-268">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="889d7-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="889d7-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="889d7-269">Windows Server 2012</span></span>



| <span data-ttu-id="889d7-270">進入</span><span class="sxs-lookup"><span data-stu-id="889d7-270">Entry</span></span> | <span data-ttu-id="889d7-271">值</span><span class="sxs-lookup"><span data-stu-id="889d7-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="889d7-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889d7-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889d7-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="889d7-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="889d7-274">System-Only</span></span>            | <span data-ttu-id="889d7-275">否</span><span class="sxs-lookup"><span data-stu-id="889d7-275">False</span></span>                           |
| <span data-ttu-id="889d7-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889d7-276">Is-Single-Valued</span></span>       | <span data-ttu-id="889d7-277">對</span><span class="sxs-lookup"><span data-stu-id="889d7-277">True</span></span>                            |
| <span data-ttu-id="889d7-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889d7-278">Is Indexed</span></span>             | <span data-ttu-id="889d7-279">對</span><span class="sxs-lookup"><span data-stu-id="889d7-279">True</span></span>                            |
| <span data-ttu-id="889d7-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889d7-280">In Global Catalog</span></span>      | <span data-ttu-id="889d7-281">否</span><span class="sxs-lookup"><span data-stu-id="889d7-281">False</span></span>                           |
| <span data-ttu-id="889d7-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889d7-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="889d7-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889d7-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="889d7-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889d7-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="889d7-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889d7-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="889d7-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-286">Search-Flags</span></span>           | <span data-ttu-id="889d7-287">0x00000001</span><span class="sxs-lookup"><span data-stu-id="889d7-287">0x00000001</span></span>                      |
| <span data-ttu-id="889d7-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889d7-288">System-Flags</span></span>           | <span data-ttu-id="889d7-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889d7-289">0x00000010</span></span>                      |
| <span data-ttu-id="889d7-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889d7-290">Classes used in</span></span>        | [<span data-ttu-id="889d7-291">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="889d7-291">**Top**</span></span>](c-top.md)<br/> |



 

 






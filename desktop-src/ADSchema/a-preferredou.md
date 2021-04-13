---
title: 慣用-OU 屬性
description: 使用者桌面上預設顯示的組織單位。
ms.assetid: e6f0d6df-0353-4626-8b1b-fa5f99f5ef58
ms.tgt_platform: multiple
keywords:
- 慣用-OU 屬性 AD 架構
- preferredOU 屬性 AD 架構
topic_type:
- apiref
api_name:
- Preferred-OU
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b4e2bc2d125524934fa629c0a42121875d14c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509530"
---
# <a name="preferred-ou-attribute"></a><span data-ttu-id="f7850-105">慣用-OU 屬性</span><span class="sxs-lookup"><span data-stu-id="f7850-105">Preferred-OU attribute</span></span>

<span data-ttu-id="f7850-106">使用者桌面上預設顯示的組織單位。</span><span class="sxs-lookup"><span data-stu-id="f7850-106">The Organizational Unit to show by default on user' s desktop.</span></span>



| <span data-ttu-id="f7850-107">進入</span><span class="sxs-lookup"><span data-stu-id="f7850-107">Entry</span></span> | <span data-ttu-id="f7850-108">值</span><span class="sxs-lookup"><span data-stu-id="f7850-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f7850-109">CN</span><span class="sxs-lookup"><span data-stu-id="f7850-109">CN</span></span>                | <span data-ttu-id="f7850-110">慣用-OU</span><span class="sxs-lookup"><span data-stu-id="f7850-110">Preferred-OU</span></span>                            |
| <span data-ttu-id="f7850-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f7850-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f7850-112">preferredOU</span><span class="sxs-lookup"><span data-stu-id="f7850-112">preferredOU</span></span>                             |
| <span data-ttu-id="f7850-113">大小</span><span class="sxs-lookup"><span data-stu-id="f7850-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f7850-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f7850-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="f7850-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f7850-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f7850-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7850-116">Attribute-Id</span></span>      | <span data-ttu-id="f7850-117">1.2.840.113556.1.4.97</span><span class="sxs-lookup"><span data-stu-id="f7850-117">1.2.840.113556.1.4.97</span></span>                   |
| <span data-ttu-id="f7850-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f7850-118">System-Id-Guid</span></span>    | <span data-ttu-id="f7850-119">bf9679ff-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f7850-119">bf9679ff-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="f7850-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7850-120">Syntax</span></span>            | [<span data-ttu-id="f7850-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f7850-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f7850-122">實作</span><span class="sxs-lookup"><span data-stu-id="f7850-122">Implementations</span></span>

-   [<span data-ttu-id="f7850-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f7850-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f7850-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7850-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7850-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7850-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7850-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7850-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7850-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7850-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7850-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7850-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f7850-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7850-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f7850-130">進入</span><span class="sxs-lookup"><span data-stu-id="f7850-130">Entry</span></span> | <span data-ttu-id="f7850-131">值</span><span class="sxs-lookup"><span data-stu-id="f7850-131">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7850-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7850-132">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7850-133">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7850-134">System-Only</span></span>            | <span data-ttu-id="f7850-135">否</span><span class="sxs-lookup"><span data-stu-id="f7850-135">False</span></span>                             |
| <span data-ttu-id="f7850-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7850-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f7850-137">對</span><span class="sxs-lookup"><span data-stu-id="f7850-137">True</span></span>                              |
| <span data-ttu-id="f7850-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7850-138">Is Indexed</span></span>             | <span data-ttu-id="f7850-139">否</span><span class="sxs-lookup"><span data-stu-id="f7850-139">False</span></span>                             |
| <span data-ttu-id="f7850-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7850-140">In Global Catalog</span></span>      | <span data-ttu-id="f7850-141">否</span><span class="sxs-lookup"><span data-stu-id="f7850-141">False</span></span>                             |
| <span data-ttu-id="f7850-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7850-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7850-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7850-143">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7850-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7850-144">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7850-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7850-145">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7850-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-146">Search-Flags</span></span>           | <span data-ttu-id="f7850-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-147">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-148">System-Flags</span></span>           | <span data-ttu-id="f7850-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-149">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7850-150">Classes used in</span></span>        | [<span data-ttu-id="f7850-151">**User**</span><span class="sxs-lookup"><span data-stu-id="f7850-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f7850-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7850-152">Windows Server 2003</span></span>



| <span data-ttu-id="f7850-153">進入</span><span class="sxs-lookup"><span data-stu-id="f7850-153">Entry</span></span> | <span data-ttu-id="f7850-154">值</span><span class="sxs-lookup"><span data-stu-id="f7850-154">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7850-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7850-155">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7850-156">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7850-157">System-Only</span></span>            | <span data-ttu-id="f7850-158">否</span><span class="sxs-lookup"><span data-stu-id="f7850-158">False</span></span>                             |
| <span data-ttu-id="f7850-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7850-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f7850-160">對</span><span class="sxs-lookup"><span data-stu-id="f7850-160">True</span></span>                              |
| <span data-ttu-id="f7850-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7850-161">Is Indexed</span></span>             | <span data-ttu-id="f7850-162">否</span><span class="sxs-lookup"><span data-stu-id="f7850-162">False</span></span>                             |
| <span data-ttu-id="f7850-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7850-163">In Global Catalog</span></span>      | <span data-ttu-id="f7850-164">否</span><span class="sxs-lookup"><span data-stu-id="f7850-164">False</span></span>                             |
| <span data-ttu-id="f7850-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7850-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7850-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7850-166">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7850-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7850-167">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7850-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7850-168">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7850-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-169">Search-Flags</span></span>           | <span data-ttu-id="f7850-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-170">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-171">System-Flags</span></span>           | <span data-ttu-id="f7850-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-172">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7850-173">Classes used in</span></span>        | [<span data-ttu-id="f7850-174">**User**</span><span class="sxs-lookup"><span data-stu-id="f7850-174">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7850-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7850-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7850-176">進入</span><span class="sxs-lookup"><span data-stu-id="f7850-176">Entry</span></span> | <span data-ttu-id="f7850-177">值</span><span class="sxs-lookup"><span data-stu-id="f7850-177">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7850-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7850-178">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7850-179">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7850-180">System-Only</span></span>            | <span data-ttu-id="f7850-181">否</span><span class="sxs-lookup"><span data-stu-id="f7850-181">False</span></span>                             |
| <span data-ttu-id="f7850-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7850-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f7850-183">對</span><span class="sxs-lookup"><span data-stu-id="f7850-183">True</span></span>                              |
| <span data-ttu-id="f7850-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7850-184">Is Indexed</span></span>             | <span data-ttu-id="f7850-185">否</span><span class="sxs-lookup"><span data-stu-id="f7850-185">False</span></span>                             |
| <span data-ttu-id="f7850-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7850-186">In Global Catalog</span></span>      | <span data-ttu-id="f7850-187">否</span><span class="sxs-lookup"><span data-stu-id="f7850-187">False</span></span>                             |
| <span data-ttu-id="f7850-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7850-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7850-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7850-189">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7850-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7850-190">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7850-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7850-191">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7850-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-192">Search-Flags</span></span>           | <span data-ttu-id="f7850-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-193">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-194">System-Flags</span></span>           | <span data-ttu-id="f7850-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-195">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7850-196">Classes used in</span></span>        | [<span data-ttu-id="f7850-197">**User**</span><span class="sxs-lookup"><span data-stu-id="f7850-197">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7850-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7850-198">Windows Server 2008</span></span>



| <span data-ttu-id="f7850-199">進入</span><span class="sxs-lookup"><span data-stu-id="f7850-199">Entry</span></span> | <span data-ttu-id="f7850-200">值</span><span class="sxs-lookup"><span data-stu-id="f7850-200">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7850-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7850-201">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7850-202">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7850-203">System-Only</span></span>            | <span data-ttu-id="f7850-204">否</span><span class="sxs-lookup"><span data-stu-id="f7850-204">False</span></span>                             |
| <span data-ttu-id="f7850-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7850-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f7850-206">對</span><span class="sxs-lookup"><span data-stu-id="f7850-206">True</span></span>                              |
| <span data-ttu-id="f7850-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7850-207">Is Indexed</span></span>             | <span data-ttu-id="f7850-208">否</span><span class="sxs-lookup"><span data-stu-id="f7850-208">False</span></span>                             |
| <span data-ttu-id="f7850-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7850-209">In Global Catalog</span></span>      | <span data-ttu-id="f7850-210">否</span><span class="sxs-lookup"><span data-stu-id="f7850-210">False</span></span>                             |
| <span data-ttu-id="f7850-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7850-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7850-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7850-212">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7850-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7850-213">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7850-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7850-214">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7850-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-215">Search-Flags</span></span>           | <span data-ttu-id="f7850-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-216">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-217">System-Flags</span></span>           | <span data-ttu-id="f7850-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-218">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7850-219">Classes used in</span></span>        | [<span data-ttu-id="f7850-220">**User**</span><span class="sxs-lookup"><span data-stu-id="f7850-220">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7850-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7850-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7850-222">進入</span><span class="sxs-lookup"><span data-stu-id="f7850-222">Entry</span></span> | <span data-ttu-id="f7850-223">值</span><span class="sxs-lookup"><span data-stu-id="f7850-223">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7850-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7850-224">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7850-225">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7850-226">System-Only</span></span>            | <span data-ttu-id="f7850-227">否</span><span class="sxs-lookup"><span data-stu-id="f7850-227">False</span></span>                             |
| <span data-ttu-id="f7850-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7850-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f7850-229">對</span><span class="sxs-lookup"><span data-stu-id="f7850-229">True</span></span>                              |
| <span data-ttu-id="f7850-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7850-230">Is Indexed</span></span>             | <span data-ttu-id="f7850-231">否</span><span class="sxs-lookup"><span data-stu-id="f7850-231">False</span></span>                             |
| <span data-ttu-id="f7850-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7850-232">In Global Catalog</span></span>      | <span data-ttu-id="f7850-233">否</span><span class="sxs-lookup"><span data-stu-id="f7850-233">False</span></span>                             |
| <span data-ttu-id="f7850-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7850-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7850-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7850-235">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7850-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7850-236">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7850-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7850-237">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7850-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-238">Search-Flags</span></span>           | <span data-ttu-id="f7850-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-239">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-240">System-Flags</span></span>           | <span data-ttu-id="f7850-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-241">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7850-242">Classes used in</span></span>        | [<span data-ttu-id="f7850-243">**User**</span><span class="sxs-lookup"><span data-stu-id="f7850-243">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7850-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7850-244">Windows Server 2012</span></span>



| <span data-ttu-id="f7850-245">進入</span><span class="sxs-lookup"><span data-stu-id="f7850-245">Entry</span></span> | <span data-ttu-id="f7850-246">值</span><span class="sxs-lookup"><span data-stu-id="f7850-246">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7850-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7850-247">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7850-248">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7850-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7850-249">System-Only</span></span>            | <span data-ttu-id="f7850-250">否</span><span class="sxs-lookup"><span data-stu-id="f7850-250">False</span></span>                             |
| <span data-ttu-id="f7850-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7850-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f7850-252">對</span><span class="sxs-lookup"><span data-stu-id="f7850-252">True</span></span>                              |
| <span data-ttu-id="f7850-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7850-253">Is Indexed</span></span>             | <span data-ttu-id="f7850-254">否</span><span class="sxs-lookup"><span data-stu-id="f7850-254">False</span></span>                             |
| <span data-ttu-id="f7850-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7850-255">In Global Catalog</span></span>      | <span data-ttu-id="f7850-256">否</span><span class="sxs-lookup"><span data-stu-id="f7850-256">False</span></span>                             |
| <span data-ttu-id="f7850-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7850-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7850-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7850-258">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7850-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7850-259">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7850-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7850-260">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7850-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-261">Search-Flags</span></span>           | <span data-ttu-id="f7850-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-262">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7850-263">System-Flags</span></span>           | <span data-ttu-id="f7850-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7850-264">0x00000010</span></span>                        |
| <span data-ttu-id="f7850-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7850-265">Classes used in</span></span>        | [<span data-ttu-id="f7850-266">**User**</span><span class="sxs-lookup"><span data-stu-id="f7850-266">**User**</span></span>](c-user.md)<br/> |



 

 






---
title: Admin-顯示名稱屬性
description: 要在系統管理員畫面上顯示的名稱。
ms.assetid: a4395f7f-3665-48c8-ac1a-68ab9a03d762
ms.tgt_platform: multiple
keywords:
- 系統管理員-顯示名稱屬性 AD 架構
- adminDisplayName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Admin-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f8e84e0c6779e8a1a7dc25eff285cd4b13b5d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467383"
---
# <a name="admin-display-name-attribute"></a><span data-ttu-id="6ba32-105">Admin-顯示名稱屬性</span><span class="sxs-lookup"><span data-stu-id="6ba32-105">Admin-Display-Name attribute</span></span>

<span data-ttu-id="6ba32-106">要在系統管理員畫面上顯示的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ba32-106">The name to be displayed on admin screens.</span></span>



| <span data-ttu-id="6ba32-107">進入</span><span class="sxs-lookup"><span data-stu-id="6ba32-107">Entry</span></span> | <span data-ttu-id="6ba32-108">值</span><span class="sxs-lookup"><span data-stu-id="6ba32-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6ba32-109">CN</span><span class="sxs-lookup"><span data-stu-id="6ba32-109">CN</span></span>                | <span data-ttu-id="6ba32-110">系統管理員-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6ba32-110">Admin-Display-Name</span></span>                          |
| <span data-ttu-id="6ba32-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6ba32-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6ba32-112">adminDisplayName</span><span class="sxs-lookup"><span data-stu-id="6ba32-112">adminDisplayName</span></span>                            |
| <span data-ttu-id="6ba32-113">大小</span><span class="sxs-lookup"><span data-stu-id="6ba32-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="6ba32-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6ba32-114">Update Privilege</span></span>  | <span data-ttu-id="6ba32-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="6ba32-115">Domain administrator</span></span>                        |
| <span data-ttu-id="6ba32-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6ba32-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6ba32-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6ba32-117">Attribute-Id</span></span>      | <span data-ttu-id="6ba32-118">1.2.840.113556.1.2.194</span><span class="sxs-lookup"><span data-stu-id="6ba32-118">1.2.840.113556.1.2.194</span></span>                      |
| <span data-ttu-id="6ba32-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6ba32-119">System-Id-Guid</span></span>    | <span data-ttu-id="6ba32-120">bf96791a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6ba32-120">bf96791a-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="6ba32-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ba32-121">Syntax</span></span>            | [<span data-ttu-id="6ba32-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6ba32-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6ba32-123">實作</span><span class="sxs-lookup"><span data-stu-id="6ba32-123">Implementations</span></span>

-   [<span data-ttu-id="6ba32-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6ba32-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6ba32-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6ba32-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6ba32-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="6ba32-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6ba32-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6ba32-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6ba32-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6ba32-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6ba32-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6ba32-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6ba32-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6ba32-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6ba32-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ba32-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6ba32-132">進入</span><span class="sxs-lookup"><span data-stu-id="6ba32-132">Entry</span></span> | <span data-ttu-id="6ba32-133">值</span><span class="sxs-lookup"><span data-stu-id="6ba32-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6ba32-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ba32-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6ba32-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ba32-135">MAPI-Id</span></span>                | <span data-ttu-id="6ba32-136">0x804B</span><span class="sxs-lookup"><span data-stu-id="6ba32-136">0x804B</span></span>                          |
| <span data-ttu-id="6ba32-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ba32-137">System-Only</span></span>            | <span data-ttu-id="6ba32-138">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-138">False</span></span>                           |
| <span data-ttu-id="6ba32-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ba32-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6ba32-140">對</span><span class="sxs-lookup"><span data-stu-id="6ba32-140">True</span></span>                            |
| <span data-ttu-id="6ba32-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ba32-141">Is Indexed</span></span>             | <span data-ttu-id="6ba32-142">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-142">False</span></span>                           |
| <span data-ttu-id="6ba32-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ba32-143">In Global Catalog</span></span>      | <span data-ttu-id="6ba32-144">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-144">False</span></span>                           |
| <span data-ttu-id="6ba32-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ba32-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ba32-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ba32-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6ba32-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ba32-147">Range-Lower</span></span>            | <span data-ttu-id="6ba32-148">1</span><span class="sxs-lookup"><span data-stu-id="6ba32-148">1</span></span>                               |
| <span data-ttu-id="6ba32-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ba32-149">Range-Upper</span></span>            | <span data-ttu-id="6ba32-150">256</span><span class="sxs-lookup"><span data-stu-id="6ba32-150">256</span></span>                             |
| <span data-ttu-id="6ba32-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-151">Search-Flags</span></span>           | <span data-ttu-id="6ba32-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ba32-152">0x00000000</span></span>                      |
| <span data-ttu-id="6ba32-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-153">System-Flags</span></span>           | <span data-ttu-id="6ba32-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ba32-154">0x00000010</span></span>                      |
| <span data-ttu-id="6ba32-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ba32-155">Classes used in</span></span>        | [<span data-ttu-id="6ba32-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6ba32-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6ba32-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ba32-157">Windows Server 2003</span></span>



| <span data-ttu-id="6ba32-158">進入</span><span class="sxs-lookup"><span data-stu-id="6ba32-158">Entry</span></span> | <span data-ttu-id="6ba32-159">值</span><span class="sxs-lookup"><span data-stu-id="6ba32-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6ba32-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ba32-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6ba32-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ba32-161">MAPI-Id</span></span>                | <span data-ttu-id="6ba32-162">0x804B</span><span class="sxs-lookup"><span data-stu-id="6ba32-162">0x804B</span></span>                          |
| <span data-ttu-id="6ba32-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ba32-163">System-Only</span></span>            | <span data-ttu-id="6ba32-164">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-164">False</span></span>                           |
| <span data-ttu-id="6ba32-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ba32-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6ba32-166">對</span><span class="sxs-lookup"><span data-stu-id="6ba32-166">True</span></span>                            |
| <span data-ttu-id="6ba32-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ba32-167">Is Indexed</span></span>             | <span data-ttu-id="6ba32-168">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-168">False</span></span>                           |
| <span data-ttu-id="6ba32-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ba32-169">In Global Catalog</span></span>      | <span data-ttu-id="6ba32-170">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-170">False</span></span>                           |
| <span data-ttu-id="6ba32-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ba32-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ba32-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ba32-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6ba32-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ba32-173">Range-Lower</span></span>            | <span data-ttu-id="6ba32-174">1</span><span class="sxs-lookup"><span data-stu-id="6ba32-174">1</span></span>                               |
| <span data-ttu-id="6ba32-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ba32-175">Range-Upper</span></span>            | <span data-ttu-id="6ba32-176">256</span><span class="sxs-lookup"><span data-stu-id="6ba32-176">256</span></span>                             |
| <span data-ttu-id="6ba32-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-177">Search-Flags</span></span>           | <span data-ttu-id="6ba32-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ba32-178">0x00000000</span></span>                      |
| <span data-ttu-id="6ba32-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-179">System-Flags</span></span>           | <span data-ttu-id="6ba32-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ba32-180">0x00000010</span></span>                      |
| <span data-ttu-id="6ba32-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ba32-181">Classes used in</span></span>        | [<span data-ttu-id="6ba32-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6ba32-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6ba32-183">亞當</span><span class="sxs-lookup"><span data-stu-id="6ba32-183">ADAM</span></span>



| <span data-ttu-id="6ba32-184">進入</span><span class="sxs-lookup"><span data-stu-id="6ba32-184">Entry</span></span> | <span data-ttu-id="6ba32-185">值</span><span class="sxs-lookup"><span data-stu-id="6ba32-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6ba32-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ba32-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6ba32-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ba32-187">MAPI-Id</span></span>                | <span data-ttu-id="6ba32-188">0x804B</span><span class="sxs-lookup"><span data-stu-id="6ba32-188">0x804B</span></span>                          |
| <span data-ttu-id="6ba32-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ba32-189">System-Only</span></span>            | <span data-ttu-id="6ba32-190">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-190">False</span></span>                           |
| <span data-ttu-id="6ba32-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ba32-191">Is-Single-Valued</span></span>       | <span data-ttu-id="6ba32-192">對</span><span class="sxs-lookup"><span data-stu-id="6ba32-192">True</span></span>                            |
| <span data-ttu-id="6ba32-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ba32-193">Is Indexed</span></span>             | <span data-ttu-id="6ba32-194">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-194">False</span></span>                           |
| <span data-ttu-id="6ba32-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ba32-195">In Global Catalog</span></span>      | <span data-ttu-id="6ba32-196">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-196">False</span></span>                           |
| <span data-ttu-id="6ba32-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ba32-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ba32-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ba32-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6ba32-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ba32-199">Range-Lower</span></span>            | <span data-ttu-id="6ba32-200">1</span><span class="sxs-lookup"><span data-stu-id="6ba32-200">1</span></span>                               |
| <span data-ttu-id="6ba32-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ba32-201">Range-Upper</span></span>            | <span data-ttu-id="6ba32-202">256</span><span class="sxs-lookup"><span data-stu-id="6ba32-202">256</span></span>                             |
| <span data-ttu-id="6ba32-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-203">Search-Flags</span></span>           | <span data-ttu-id="6ba32-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ba32-204">0x00000000</span></span>                      |
| <span data-ttu-id="6ba32-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-205">System-Flags</span></span>           | <span data-ttu-id="6ba32-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ba32-206">0x00000010</span></span>                      |
| <span data-ttu-id="6ba32-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ba32-207">Classes used in</span></span>        | [<span data-ttu-id="6ba32-208">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6ba32-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6ba32-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6ba32-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6ba32-210">進入</span><span class="sxs-lookup"><span data-stu-id="6ba32-210">Entry</span></span> | <span data-ttu-id="6ba32-211">值</span><span class="sxs-lookup"><span data-stu-id="6ba32-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6ba32-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ba32-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6ba32-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ba32-213">MAPI-Id</span></span>                | <span data-ttu-id="6ba32-214">0x804B</span><span class="sxs-lookup"><span data-stu-id="6ba32-214">0x804B</span></span>                          |
| <span data-ttu-id="6ba32-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ba32-215">System-Only</span></span>            | <span data-ttu-id="6ba32-216">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-216">False</span></span>                           |
| <span data-ttu-id="6ba32-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ba32-217">Is-Single-Valued</span></span>       | <span data-ttu-id="6ba32-218">對</span><span class="sxs-lookup"><span data-stu-id="6ba32-218">True</span></span>                            |
| <span data-ttu-id="6ba32-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ba32-219">Is Indexed</span></span>             | <span data-ttu-id="6ba32-220">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-220">False</span></span>                           |
| <span data-ttu-id="6ba32-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ba32-221">In Global Catalog</span></span>      | <span data-ttu-id="6ba32-222">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-222">False</span></span>                           |
| <span data-ttu-id="6ba32-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ba32-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ba32-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ba32-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6ba32-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ba32-225">Range-Lower</span></span>            | <span data-ttu-id="6ba32-226">1</span><span class="sxs-lookup"><span data-stu-id="6ba32-226">1</span></span>                               |
| <span data-ttu-id="6ba32-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ba32-227">Range-Upper</span></span>            | <span data-ttu-id="6ba32-228">256</span><span class="sxs-lookup"><span data-stu-id="6ba32-228">256</span></span>                             |
| <span data-ttu-id="6ba32-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-229">Search-Flags</span></span>           | <span data-ttu-id="6ba32-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ba32-230">0x00000000</span></span>                      |
| <span data-ttu-id="6ba32-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-231">System-Flags</span></span>           | <span data-ttu-id="6ba32-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ba32-232">0x00000010</span></span>                      |
| <span data-ttu-id="6ba32-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ba32-233">Classes used in</span></span>        | [<span data-ttu-id="6ba32-234">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6ba32-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6ba32-235">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ba32-235">Windows Server 2008</span></span>



| <span data-ttu-id="6ba32-236">進入</span><span class="sxs-lookup"><span data-stu-id="6ba32-236">Entry</span></span> | <span data-ttu-id="6ba32-237">值</span><span class="sxs-lookup"><span data-stu-id="6ba32-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6ba32-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ba32-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6ba32-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ba32-239">MAPI-Id</span></span>                | <span data-ttu-id="6ba32-240">0x804B</span><span class="sxs-lookup"><span data-stu-id="6ba32-240">0x804B</span></span>                          |
| <span data-ttu-id="6ba32-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ba32-241">System-Only</span></span>            | <span data-ttu-id="6ba32-242">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-242">False</span></span>                           |
| <span data-ttu-id="6ba32-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ba32-243">Is-Single-Valued</span></span>       | <span data-ttu-id="6ba32-244">對</span><span class="sxs-lookup"><span data-stu-id="6ba32-244">True</span></span>                            |
| <span data-ttu-id="6ba32-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ba32-245">Is Indexed</span></span>             | <span data-ttu-id="6ba32-246">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-246">False</span></span>                           |
| <span data-ttu-id="6ba32-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ba32-247">In Global Catalog</span></span>      | <span data-ttu-id="6ba32-248">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-248">False</span></span>                           |
| <span data-ttu-id="6ba32-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ba32-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ba32-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ba32-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6ba32-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ba32-251">Range-Lower</span></span>            | <span data-ttu-id="6ba32-252">1</span><span class="sxs-lookup"><span data-stu-id="6ba32-252">1</span></span>                               |
| <span data-ttu-id="6ba32-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ba32-253">Range-Upper</span></span>            | <span data-ttu-id="6ba32-254">256</span><span class="sxs-lookup"><span data-stu-id="6ba32-254">256</span></span>                             |
| <span data-ttu-id="6ba32-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-255">Search-Flags</span></span>           | <span data-ttu-id="6ba32-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ba32-256">0x00000000</span></span>                      |
| <span data-ttu-id="6ba32-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-257">System-Flags</span></span>           | <span data-ttu-id="6ba32-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ba32-258">0x00000010</span></span>                      |
| <span data-ttu-id="6ba32-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ba32-259">Classes used in</span></span>        | [<span data-ttu-id="6ba32-260">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6ba32-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6ba32-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6ba32-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6ba32-262">進入</span><span class="sxs-lookup"><span data-stu-id="6ba32-262">Entry</span></span> | <span data-ttu-id="6ba32-263">值</span><span class="sxs-lookup"><span data-stu-id="6ba32-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6ba32-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ba32-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6ba32-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ba32-265">MAPI-Id</span></span>                | <span data-ttu-id="6ba32-266">0x804B</span><span class="sxs-lookup"><span data-stu-id="6ba32-266">0x804B</span></span>                          |
| <span data-ttu-id="6ba32-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ba32-267">System-Only</span></span>            | <span data-ttu-id="6ba32-268">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-268">False</span></span>                           |
| <span data-ttu-id="6ba32-269">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ba32-269">Is-Single-Valued</span></span>       | <span data-ttu-id="6ba32-270">對</span><span class="sxs-lookup"><span data-stu-id="6ba32-270">True</span></span>                            |
| <span data-ttu-id="6ba32-271">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ba32-271">Is Indexed</span></span>             | <span data-ttu-id="6ba32-272">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-272">False</span></span>                           |
| <span data-ttu-id="6ba32-273">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ba32-273">In Global Catalog</span></span>      | <span data-ttu-id="6ba32-274">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-274">False</span></span>                           |
| <span data-ttu-id="6ba32-275">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ba32-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ba32-276">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ba32-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6ba32-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ba32-277">Range-Lower</span></span>            | <span data-ttu-id="6ba32-278">1</span><span class="sxs-lookup"><span data-stu-id="6ba32-278">1</span></span>                               |
| <span data-ttu-id="6ba32-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ba32-279">Range-Upper</span></span>            | <span data-ttu-id="6ba32-280">256</span><span class="sxs-lookup"><span data-stu-id="6ba32-280">256</span></span>                             |
| <span data-ttu-id="6ba32-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-281">Search-Flags</span></span>           | <span data-ttu-id="6ba32-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ba32-282">0x00000000</span></span>                      |
| <span data-ttu-id="6ba32-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-283">System-Flags</span></span>           | <span data-ttu-id="6ba32-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ba32-284">0x00000010</span></span>                      |
| <span data-ttu-id="6ba32-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ba32-285">Classes used in</span></span>        | [<span data-ttu-id="6ba32-286">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6ba32-286">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6ba32-287">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ba32-287">Windows Server 2012</span></span>



| <span data-ttu-id="6ba32-288">進入</span><span class="sxs-lookup"><span data-stu-id="6ba32-288">Entry</span></span> | <span data-ttu-id="6ba32-289">值</span><span class="sxs-lookup"><span data-stu-id="6ba32-289">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6ba32-290">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ba32-290">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6ba32-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ba32-291">MAPI-Id</span></span>                | <span data-ttu-id="6ba32-292">0x804B</span><span class="sxs-lookup"><span data-stu-id="6ba32-292">0x804B</span></span>                          |
| <span data-ttu-id="6ba32-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ba32-293">System-Only</span></span>            | <span data-ttu-id="6ba32-294">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-294">False</span></span>                           |
| <span data-ttu-id="6ba32-295">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ba32-295">Is-Single-Valued</span></span>       | <span data-ttu-id="6ba32-296">對</span><span class="sxs-lookup"><span data-stu-id="6ba32-296">True</span></span>                            |
| <span data-ttu-id="6ba32-297">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ba32-297">Is Indexed</span></span>             | <span data-ttu-id="6ba32-298">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-298">False</span></span>                           |
| <span data-ttu-id="6ba32-299">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ba32-299">In Global Catalog</span></span>      | <span data-ttu-id="6ba32-300">否</span><span class="sxs-lookup"><span data-stu-id="6ba32-300">False</span></span>                           |
| <span data-ttu-id="6ba32-301">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ba32-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ba32-302">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ba32-302">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6ba32-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ba32-303">Range-Lower</span></span>            | <span data-ttu-id="6ba32-304">1</span><span class="sxs-lookup"><span data-stu-id="6ba32-304">1</span></span>                               |
| <span data-ttu-id="6ba32-305">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ba32-305">Range-Upper</span></span>            | <span data-ttu-id="6ba32-306">256</span><span class="sxs-lookup"><span data-stu-id="6ba32-306">256</span></span>                             |
| <span data-ttu-id="6ba32-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-307">Search-Flags</span></span>           | <span data-ttu-id="6ba32-308">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ba32-308">0x00000000</span></span>                      |
| <span data-ttu-id="6ba32-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ba32-309">System-Flags</span></span>           | <span data-ttu-id="6ba32-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ba32-310">0x00000010</span></span>                      |
| <span data-ttu-id="6ba32-311">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ba32-311">Classes used in</span></span>        | [<span data-ttu-id="6ba32-312">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6ba32-312">**Top**</span></span>](c-top.md)<br/> |



 

 






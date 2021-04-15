---
title: Logon-Hours 屬性
description: 允許使用者登入網域的時數。
ms.assetid: b97cc8b0-7f26-45c1-b1c9-bae6467bdfb6
ms.tgt_platform: multiple
keywords:
- Logon-Hours 屬性 AD 架構
- logonHours 屬性 AD 架構
topic_type:
- apiref
api_name:
- Logon-Hours
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f764192ac57efdb1f14d55f691183240f0eddfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467203"
---
# <a name="logon-hours-attribute"></a><span data-ttu-id="f2c80-105">Logon-Hours 屬性</span><span class="sxs-lookup"><span data-stu-id="f2c80-105">Logon-Hours attribute</span></span>

<span data-ttu-id="f2c80-106">允許使用者登入網域的時數。</span><span class="sxs-lookup"><span data-stu-id="f2c80-106">The hours that the user is allowed to logon to the domain.</span></span>



| <span data-ttu-id="f2c80-107">進入</span><span class="sxs-lookup"><span data-stu-id="f2c80-107">Entry</span></span> | <span data-ttu-id="f2c80-108">值</span><span class="sxs-lookup"><span data-stu-id="f2c80-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f2c80-109">CN</span><span class="sxs-lookup"><span data-stu-id="f2c80-109">CN</span></span>                | <span data-ttu-id="f2c80-110">Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="f2c80-110">Logon-Hours</span></span>                                           |
| <span data-ttu-id="f2c80-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f2c80-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f2c80-112">logonHours</span><span class="sxs-lookup"><span data-stu-id="f2c80-112">logonHours</span></span>                                            |
| <span data-ttu-id="f2c80-113">大小</span><span class="sxs-lookup"><span data-stu-id="f2c80-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f2c80-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f2c80-114">Update Privilege</span></span>  | <span data-ttu-id="f2c80-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="f2c80-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="f2c80-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f2c80-116">Update Frequency</span></span>  | <span data-ttu-id="f2c80-117">只要帳戶的登入時數需要變更。</span><span class="sxs-lookup"><span data-stu-id="f2c80-117">Whenever the account's logon hours needs to change.</span></span>   |
| <span data-ttu-id="f2c80-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f2c80-118">Attribute-Id</span></span>      | <span data-ttu-id="f2c80-119">1.2.840.113556.1.4.64</span><span class="sxs-lookup"><span data-stu-id="f2c80-119">1.2.840.113556.1.4.64</span></span>                                 |
| <span data-ttu-id="f2c80-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f2c80-120">System-Id-Guid</span></span>    | <span data-ttu-id="f2c80-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f2c80-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="f2c80-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2c80-122">Syntax</span></span>            | [<span data-ttu-id="f2c80-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f2c80-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f2c80-124">實作</span><span class="sxs-lookup"><span data-stu-id="f2c80-124">Implementations</span></span>

-   [<span data-ttu-id="f2c80-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f2c80-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f2c80-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f2c80-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f2c80-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f2c80-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f2c80-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f2c80-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f2c80-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f2c80-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f2c80-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f2c80-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f2c80-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2c80-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f2c80-132">進入</span><span class="sxs-lookup"><span data-stu-id="f2c80-132">Entry</span></span> | <span data-ttu-id="f2c80-133">值</span><span class="sxs-lookup"><span data-stu-id="f2c80-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2c80-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f2c80-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2c80-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2c80-136">System-Only</span></span>            | <span data-ttu-id="f2c80-137">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-137">False</span></span>                             |
| <span data-ttu-id="f2c80-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f2c80-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f2c80-139">對</span><span class="sxs-lookup"><span data-stu-id="f2c80-139">True</span></span>                              |
| <span data-ttu-id="f2c80-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f2c80-140">Is Indexed</span></span>             | <span data-ttu-id="f2c80-141">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-141">False</span></span>                             |
| <span data-ttu-id="f2c80-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f2c80-142">In Global Catalog</span></span>      | <span data-ttu-id="f2c80-143">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-143">False</span></span>                             |
| <span data-ttu-id="f2c80-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f2c80-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2c80-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f2c80-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2c80-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2c80-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2c80-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2c80-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2c80-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-148">Search-Flags</span></span>           | <span data-ttu-id="f2c80-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-149">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-150">System-Flags</span></span>           | <span data-ttu-id="f2c80-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-151">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f2c80-152">Classes used in</span></span>        | [<span data-ttu-id="f2c80-153">**User**</span><span class="sxs-lookup"><span data-stu-id="f2c80-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f2c80-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2c80-154">Windows Server 2003</span></span>



| <span data-ttu-id="f2c80-155">進入</span><span class="sxs-lookup"><span data-stu-id="f2c80-155">Entry</span></span> | <span data-ttu-id="f2c80-156">值</span><span class="sxs-lookup"><span data-stu-id="f2c80-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2c80-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f2c80-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2c80-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2c80-159">System-Only</span></span>            | <span data-ttu-id="f2c80-160">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-160">False</span></span>                             |
| <span data-ttu-id="f2c80-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f2c80-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f2c80-162">對</span><span class="sxs-lookup"><span data-stu-id="f2c80-162">True</span></span>                              |
| <span data-ttu-id="f2c80-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f2c80-163">Is Indexed</span></span>             | <span data-ttu-id="f2c80-164">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-164">False</span></span>                             |
| <span data-ttu-id="f2c80-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f2c80-165">In Global Catalog</span></span>      | <span data-ttu-id="f2c80-166">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-166">False</span></span>                             |
| <span data-ttu-id="f2c80-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f2c80-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2c80-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f2c80-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2c80-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2c80-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2c80-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2c80-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2c80-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-171">Search-Flags</span></span>           | <span data-ttu-id="f2c80-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-172">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-173">System-Flags</span></span>           | <span data-ttu-id="f2c80-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-174">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f2c80-175">Classes used in</span></span>        | [<span data-ttu-id="f2c80-176">**User**</span><span class="sxs-lookup"><span data-stu-id="f2c80-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f2c80-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f2c80-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f2c80-178">進入</span><span class="sxs-lookup"><span data-stu-id="f2c80-178">Entry</span></span> | <span data-ttu-id="f2c80-179">值</span><span class="sxs-lookup"><span data-stu-id="f2c80-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2c80-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f2c80-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2c80-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2c80-182">System-Only</span></span>            | <span data-ttu-id="f2c80-183">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-183">False</span></span>                             |
| <span data-ttu-id="f2c80-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f2c80-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f2c80-185">對</span><span class="sxs-lookup"><span data-stu-id="f2c80-185">True</span></span>                              |
| <span data-ttu-id="f2c80-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f2c80-186">Is Indexed</span></span>             | <span data-ttu-id="f2c80-187">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-187">False</span></span>                             |
| <span data-ttu-id="f2c80-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f2c80-188">In Global Catalog</span></span>      | <span data-ttu-id="f2c80-189">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-189">False</span></span>                             |
| <span data-ttu-id="f2c80-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f2c80-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2c80-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f2c80-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2c80-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2c80-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2c80-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2c80-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2c80-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-194">Search-Flags</span></span>           | <span data-ttu-id="f2c80-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-195">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-196">System-Flags</span></span>           | <span data-ttu-id="f2c80-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-197">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f2c80-198">Classes used in</span></span>        | [<span data-ttu-id="f2c80-199">**User**</span><span class="sxs-lookup"><span data-stu-id="f2c80-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f2c80-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2c80-200">Windows Server 2008</span></span>



| <span data-ttu-id="f2c80-201">進入</span><span class="sxs-lookup"><span data-stu-id="f2c80-201">Entry</span></span> | <span data-ttu-id="f2c80-202">值</span><span class="sxs-lookup"><span data-stu-id="f2c80-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2c80-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f2c80-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2c80-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2c80-205">System-Only</span></span>            | <span data-ttu-id="f2c80-206">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-206">False</span></span>                             |
| <span data-ttu-id="f2c80-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f2c80-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f2c80-208">對</span><span class="sxs-lookup"><span data-stu-id="f2c80-208">True</span></span>                              |
| <span data-ttu-id="f2c80-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f2c80-209">Is Indexed</span></span>             | <span data-ttu-id="f2c80-210">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-210">False</span></span>                             |
| <span data-ttu-id="f2c80-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f2c80-211">In Global Catalog</span></span>      | <span data-ttu-id="f2c80-212">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-212">False</span></span>                             |
| <span data-ttu-id="f2c80-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f2c80-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2c80-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f2c80-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2c80-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2c80-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2c80-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2c80-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2c80-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-217">Search-Flags</span></span>           | <span data-ttu-id="f2c80-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-218">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-219">System-Flags</span></span>           | <span data-ttu-id="f2c80-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-220">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f2c80-221">Classes used in</span></span>        | [<span data-ttu-id="f2c80-222">**User**</span><span class="sxs-lookup"><span data-stu-id="f2c80-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f2c80-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2c80-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f2c80-224">進入</span><span class="sxs-lookup"><span data-stu-id="f2c80-224">Entry</span></span> | <span data-ttu-id="f2c80-225">值</span><span class="sxs-lookup"><span data-stu-id="f2c80-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2c80-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f2c80-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2c80-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2c80-228">System-Only</span></span>            | <span data-ttu-id="f2c80-229">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-229">False</span></span>                             |
| <span data-ttu-id="f2c80-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f2c80-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f2c80-231">對</span><span class="sxs-lookup"><span data-stu-id="f2c80-231">True</span></span>                              |
| <span data-ttu-id="f2c80-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f2c80-232">Is Indexed</span></span>             | <span data-ttu-id="f2c80-233">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-233">False</span></span>                             |
| <span data-ttu-id="f2c80-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f2c80-234">In Global Catalog</span></span>      | <span data-ttu-id="f2c80-235">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-235">False</span></span>                             |
| <span data-ttu-id="f2c80-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f2c80-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2c80-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f2c80-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2c80-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2c80-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2c80-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2c80-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2c80-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-240">Search-Flags</span></span>           | <span data-ttu-id="f2c80-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-241">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-242">System-Flags</span></span>           | <span data-ttu-id="f2c80-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-243">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f2c80-244">Classes used in</span></span>        | [<span data-ttu-id="f2c80-245">**User**</span><span class="sxs-lookup"><span data-stu-id="f2c80-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f2c80-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2c80-246">Windows Server 2012</span></span>



| <span data-ttu-id="f2c80-247">進入</span><span class="sxs-lookup"><span data-stu-id="f2c80-247">Entry</span></span> | <span data-ttu-id="f2c80-248">值</span><span class="sxs-lookup"><span data-stu-id="f2c80-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2c80-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f2c80-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2c80-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2c80-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2c80-251">System-Only</span></span>            | <span data-ttu-id="f2c80-252">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-252">False</span></span>                             |
| <span data-ttu-id="f2c80-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f2c80-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f2c80-254">對</span><span class="sxs-lookup"><span data-stu-id="f2c80-254">True</span></span>                              |
| <span data-ttu-id="f2c80-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f2c80-255">Is Indexed</span></span>             | <span data-ttu-id="f2c80-256">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-256">False</span></span>                             |
| <span data-ttu-id="f2c80-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f2c80-257">In Global Catalog</span></span>      | <span data-ttu-id="f2c80-258">否</span><span class="sxs-lookup"><span data-stu-id="f2c80-258">False</span></span>                             |
| <span data-ttu-id="f2c80-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f2c80-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2c80-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f2c80-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2c80-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2c80-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2c80-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2c80-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2c80-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-263">Search-Flags</span></span>           | <span data-ttu-id="f2c80-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-264">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2c80-265">System-Flags</span></span>           | <span data-ttu-id="f2c80-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2c80-266">0x00000010</span></span>                        |
| <span data-ttu-id="f2c80-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f2c80-267">Classes used in</span></span>        | [<span data-ttu-id="f2c80-268">**User**</span><span class="sxs-lookup"><span data-stu-id="f2c80-268">**User**</span></span>](c-user.md)<br/> |



 

 






---
title: Server-Role 屬性
description: 相容于 Windows 2000 之前的伺服器伺服器。 執行 Windows NT Server 的電腦可以是獨立伺服器、主域控制站 (PDC) ，或 (BDC) 的備份網域控制站。
ms.assetid: 0c2e5b18-14ad-4f77-a62c-eeb95aabbb99
ms.tgt_platform: multiple
keywords:
- Server-Role 屬性 AD 架構
- serverRole 屬性 AD 架構
topic_type:
- apiref
api_name:
- Server-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a127a94cd1ecc2bfce3701c11ee2a5e0c2376c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106976989"
---
# <a name="server-role-attribute"></a><span data-ttu-id="98c29-106">Server-Role 屬性</span><span class="sxs-lookup"><span data-stu-id="98c29-106">Server-Role attribute</span></span>

<span data-ttu-id="98c29-107">相容于 Windows 2000 之前的伺服器伺服器。</span><span class="sxs-lookup"><span data-stu-id="98c29-107">For compatibility with pre-Windows 2000 Server servers.</span></span> <span data-ttu-id="98c29-108">執行 Windows NT Server 的電腦可以是獨立伺服器、主域控制站 (PDC) ，或 (BDC) 的備份網域控制站。</span><span class="sxs-lookup"><span data-stu-id="98c29-108">A computer running Windows NT Server can be a standalone server, a primary domain controller (PDC), or a backup domain controller (BDC).</span></span>



| <span data-ttu-id="98c29-109">進入</span><span class="sxs-lookup"><span data-stu-id="98c29-109">Entry</span></span> | <span data-ttu-id="98c29-110">值</span><span class="sxs-lookup"><span data-stu-id="98c29-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="98c29-111">CN</span><span class="sxs-lookup"><span data-stu-id="98c29-111">CN</span></span>                | <span data-ttu-id="98c29-112">Server-Role</span><span class="sxs-lookup"><span data-stu-id="98c29-112">Server-Role</span></span>                          |
| <span data-ttu-id="98c29-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="98c29-113">Ldap-Display-Name</span></span> | <span data-ttu-id="98c29-114">serverRole</span><span class="sxs-lookup"><span data-stu-id="98c29-114">serverRole</span></span>                           |
| <span data-ttu-id="98c29-115">大小</span><span class="sxs-lookup"><span data-stu-id="98c29-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="98c29-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="98c29-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="98c29-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="98c29-117">Update Frequency</span></span>  | <span data-ttu-id="98c29-118">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="98c29-118">4 bytes</span></span>                              |
| <span data-ttu-id="98c29-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="98c29-119">Attribute-Id</span></span>      | <span data-ttu-id="98c29-120">1.2.840.113556.1.4.157</span><span class="sxs-lookup"><span data-stu-id="98c29-120">1.2.840.113556.1.4.157</span></span>               |
| <span data-ttu-id="98c29-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="98c29-121">System-Id-Guid</span></span>    | <span data-ttu-id="98c29-122">bf967a33-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="98c29-122">bf967a33-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="98c29-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="98c29-123">Syntax</span></span>            | [<span data-ttu-id="98c29-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="98c29-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="98c29-125">實作</span><span class="sxs-lookup"><span data-stu-id="98c29-125">Implementations</span></span>

-   [<span data-ttu-id="98c29-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="98c29-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="98c29-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="98c29-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="98c29-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="98c29-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="98c29-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="98c29-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="98c29-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="98c29-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="98c29-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="98c29-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="98c29-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98c29-132">Windows 2000 Server</span></span>



| <span data-ttu-id="98c29-133">進入</span><span class="sxs-lookup"><span data-stu-id="98c29-133">Entry</span></span> | <span data-ttu-id="98c29-134">值</span><span class="sxs-lookup"><span data-stu-id="98c29-134">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="98c29-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98c29-135">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98c29-136">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="98c29-137">System-Only</span></span>            | <span data-ttu-id="98c29-138">否</span><span class="sxs-lookup"><span data-stu-id="98c29-138">False</span></span>                                                 |
| <span data-ttu-id="98c29-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98c29-139">Is-Single-Valued</span></span>       | <span data-ttu-id="98c29-140">對</span><span class="sxs-lookup"><span data-stu-id="98c29-140">True</span></span>                                                  |
| <span data-ttu-id="98c29-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98c29-141">Is Indexed</span></span>             | <span data-ttu-id="98c29-142">否</span><span class="sxs-lookup"><span data-stu-id="98c29-142">False</span></span>                                                 |
| <span data-ttu-id="98c29-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98c29-143">In Global Catalog</span></span>      | <span data-ttu-id="98c29-144">否</span><span class="sxs-lookup"><span data-stu-id="98c29-144">False</span></span>                                                 |
| <span data-ttu-id="98c29-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98c29-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="98c29-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98c29-146">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="98c29-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98c29-147">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98c29-148">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-149">Search-Flags</span></span>           | <span data-ttu-id="98c29-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98c29-150">0x00000000</span></span>                                            |
| <span data-ttu-id="98c29-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-151">System-Flags</span></span>           | <span data-ttu-id="98c29-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98c29-152">0x00000010</span></span>                                            |
| <span data-ttu-id="98c29-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98c29-153">Classes used in</span></span>        | [<span data-ttu-id="98c29-154">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="98c29-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="98c29-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="98c29-155">Windows Server 2003</span></span>



| <span data-ttu-id="98c29-156">進入</span><span class="sxs-lookup"><span data-stu-id="98c29-156">Entry</span></span> | <span data-ttu-id="98c29-157">值</span><span class="sxs-lookup"><span data-stu-id="98c29-157">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="98c29-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98c29-158">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98c29-159">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="98c29-160">System-Only</span></span>            | <span data-ttu-id="98c29-161">否</span><span class="sxs-lookup"><span data-stu-id="98c29-161">False</span></span>                                                 |
| <span data-ttu-id="98c29-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98c29-162">Is-Single-Valued</span></span>       | <span data-ttu-id="98c29-163">對</span><span class="sxs-lookup"><span data-stu-id="98c29-163">True</span></span>                                                  |
| <span data-ttu-id="98c29-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98c29-164">Is Indexed</span></span>             | <span data-ttu-id="98c29-165">否</span><span class="sxs-lookup"><span data-stu-id="98c29-165">False</span></span>                                                 |
| <span data-ttu-id="98c29-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98c29-166">In Global Catalog</span></span>      | <span data-ttu-id="98c29-167">否</span><span class="sxs-lookup"><span data-stu-id="98c29-167">False</span></span>                                                 |
| <span data-ttu-id="98c29-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98c29-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="98c29-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98c29-169">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="98c29-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98c29-170">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98c29-171">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-172">Search-Flags</span></span>           | <span data-ttu-id="98c29-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98c29-173">0x00000000</span></span>                                            |
| <span data-ttu-id="98c29-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-174">System-Flags</span></span>           | <span data-ttu-id="98c29-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98c29-175">0x00000010</span></span>                                            |
| <span data-ttu-id="98c29-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98c29-176">Classes used in</span></span>        | [<span data-ttu-id="98c29-177">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="98c29-177">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="98c29-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="98c29-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="98c29-179">進入</span><span class="sxs-lookup"><span data-stu-id="98c29-179">Entry</span></span> | <span data-ttu-id="98c29-180">值</span><span class="sxs-lookup"><span data-stu-id="98c29-180">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="98c29-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98c29-181">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98c29-182">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="98c29-183">System-Only</span></span>            | <span data-ttu-id="98c29-184">否</span><span class="sxs-lookup"><span data-stu-id="98c29-184">False</span></span>                                                 |
| <span data-ttu-id="98c29-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98c29-185">Is-Single-Valued</span></span>       | <span data-ttu-id="98c29-186">對</span><span class="sxs-lookup"><span data-stu-id="98c29-186">True</span></span>                                                  |
| <span data-ttu-id="98c29-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98c29-187">Is Indexed</span></span>             | <span data-ttu-id="98c29-188">否</span><span class="sxs-lookup"><span data-stu-id="98c29-188">False</span></span>                                                 |
| <span data-ttu-id="98c29-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98c29-189">In Global Catalog</span></span>      | <span data-ttu-id="98c29-190">否</span><span class="sxs-lookup"><span data-stu-id="98c29-190">False</span></span>                                                 |
| <span data-ttu-id="98c29-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98c29-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="98c29-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98c29-192">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="98c29-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98c29-193">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98c29-194">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-195">Search-Flags</span></span>           | <span data-ttu-id="98c29-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98c29-196">0x00000000</span></span>                                            |
| <span data-ttu-id="98c29-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-197">System-Flags</span></span>           | <span data-ttu-id="98c29-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98c29-198">0x00000010</span></span>                                            |
| <span data-ttu-id="98c29-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98c29-199">Classes used in</span></span>        | [<span data-ttu-id="98c29-200">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="98c29-200">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="98c29-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98c29-201">Windows Server 2008</span></span>



| <span data-ttu-id="98c29-202">進入</span><span class="sxs-lookup"><span data-stu-id="98c29-202">Entry</span></span> | <span data-ttu-id="98c29-203">值</span><span class="sxs-lookup"><span data-stu-id="98c29-203">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="98c29-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98c29-204">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98c29-205">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="98c29-206">System-Only</span></span>            | <span data-ttu-id="98c29-207">否</span><span class="sxs-lookup"><span data-stu-id="98c29-207">False</span></span>                                                 |
| <span data-ttu-id="98c29-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98c29-208">Is-Single-Valued</span></span>       | <span data-ttu-id="98c29-209">對</span><span class="sxs-lookup"><span data-stu-id="98c29-209">True</span></span>                                                  |
| <span data-ttu-id="98c29-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98c29-210">Is Indexed</span></span>             | <span data-ttu-id="98c29-211">否</span><span class="sxs-lookup"><span data-stu-id="98c29-211">False</span></span>                                                 |
| <span data-ttu-id="98c29-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98c29-212">In Global Catalog</span></span>      | <span data-ttu-id="98c29-213">否</span><span class="sxs-lookup"><span data-stu-id="98c29-213">False</span></span>                                                 |
| <span data-ttu-id="98c29-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98c29-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="98c29-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98c29-215">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="98c29-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98c29-216">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98c29-217">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-218">Search-Flags</span></span>           | <span data-ttu-id="98c29-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98c29-219">0x00000000</span></span>                                            |
| <span data-ttu-id="98c29-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-220">System-Flags</span></span>           | <span data-ttu-id="98c29-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98c29-221">0x00000010</span></span>                                            |
| <span data-ttu-id="98c29-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98c29-222">Classes used in</span></span>        | [<span data-ttu-id="98c29-223">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="98c29-223">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="98c29-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="98c29-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="98c29-225">進入</span><span class="sxs-lookup"><span data-stu-id="98c29-225">Entry</span></span> | <span data-ttu-id="98c29-226">值</span><span class="sxs-lookup"><span data-stu-id="98c29-226">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="98c29-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98c29-227">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98c29-228">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="98c29-229">System-Only</span></span>            | <span data-ttu-id="98c29-230">否</span><span class="sxs-lookup"><span data-stu-id="98c29-230">False</span></span>                                                 |
| <span data-ttu-id="98c29-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98c29-231">Is-Single-Valued</span></span>       | <span data-ttu-id="98c29-232">對</span><span class="sxs-lookup"><span data-stu-id="98c29-232">True</span></span>                                                  |
| <span data-ttu-id="98c29-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98c29-233">Is Indexed</span></span>             | <span data-ttu-id="98c29-234">否</span><span class="sxs-lookup"><span data-stu-id="98c29-234">False</span></span>                                                 |
| <span data-ttu-id="98c29-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98c29-235">In Global Catalog</span></span>      | <span data-ttu-id="98c29-236">否</span><span class="sxs-lookup"><span data-stu-id="98c29-236">False</span></span>                                                 |
| <span data-ttu-id="98c29-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98c29-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="98c29-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98c29-238">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="98c29-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98c29-239">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98c29-240">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-241">Search-Flags</span></span>           | <span data-ttu-id="98c29-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98c29-242">0x00000000</span></span>                                            |
| <span data-ttu-id="98c29-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-243">System-Flags</span></span>           | <span data-ttu-id="98c29-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98c29-244">0x00000010</span></span>                                            |
| <span data-ttu-id="98c29-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98c29-245">Classes used in</span></span>        | [<span data-ttu-id="98c29-246">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="98c29-246">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="98c29-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="98c29-247">Windows Server 2012</span></span>



| <span data-ttu-id="98c29-248">進入</span><span class="sxs-lookup"><span data-stu-id="98c29-248">Entry</span></span> | <span data-ttu-id="98c29-249">值</span><span class="sxs-lookup"><span data-stu-id="98c29-249">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="98c29-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98c29-250">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98c29-251">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="98c29-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="98c29-252">System-Only</span></span>            | <span data-ttu-id="98c29-253">否</span><span class="sxs-lookup"><span data-stu-id="98c29-253">False</span></span>                                                 |
| <span data-ttu-id="98c29-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98c29-254">Is-Single-Valued</span></span>       | <span data-ttu-id="98c29-255">對</span><span class="sxs-lookup"><span data-stu-id="98c29-255">True</span></span>                                                  |
| <span data-ttu-id="98c29-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98c29-256">Is Indexed</span></span>             | <span data-ttu-id="98c29-257">否</span><span class="sxs-lookup"><span data-stu-id="98c29-257">False</span></span>                                                 |
| <span data-ttu-id="98c29-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98c29-258">In Global Catalog</span></span>      | <span data-ttu-id="98c29-259">否</span><span class="sxs-lookup"><span data-stu-id="98c29-259">False</span></span>                                                 |
| <span data-ttu-id="98c29-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98c29-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="98c29-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98c29-261">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="98c29-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98c29-262">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98c29-263">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="98c29-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-264">Search-Flags</span></span>           | <span data-ttu-id="98c29-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98c29-265">0x00000000</span></span>                                            |
| <span data-ttu-id="98c29-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98c29-266">System-Flags</span></span>           | <span data-ttu-id="98c29-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98c29-267">0x00000010</span></span>                                            |
| <span data-ttu-id="98c29-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98c29-268">Classes used in</span></span>        | [<span data-ttu-id="98c29-269">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="98c29-269">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 






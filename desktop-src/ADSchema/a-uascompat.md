---
title: UAS-Compat 屬性
description: 指出安全性帳戶管理員是否會強制執行資料大小，使 Active Directory 與 LanManager 使用者帳戶系統相容 (的) 。
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- UAS-Compat 屬性 AD 架構
- uASCompat 屬性 AD 架構
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970661"
---
# <a name="uas-compat-attribute"></a><span data-ttu-id="65276-105">UAS-Compat 屬性</span><span class="sxs-lookup"><span data-stu-id="65276-105">UAS-Compat attribute</span></span>

<span data-ttu-id="65276-106">指出安全性帳戶管理員是否會強制執行資料大小，使 Active Directory 與 LanManager 使用者帳戶系統相容 (的) 。</span><span class="sxs-lookup"><span data-stu-id="65276-106">Indicates if the security account manager will enforce data sizes to make Active Directory compatible with the LanManager User Account System (UAS).</span></span> <span data-ttu-id="65276-107">如果這個值為0，則不會強制執行任何限制。</span><span class="sxs-lookup"><span data-stu-id="65276-107">If this value is 0, no limits are enforced.</span></span> <span data-ttu-id="65276-108">如果這個值是1，則會強制執行下列限制。</span><span class="sxs-lookup"><span data-stu-id="65276-108">If this value is 1, the following limits are enforced.</span></span>



| <span data-ttu-id="65276-109">值</span><span class="sxs-lookup"><span data-stu-id="65276-109">Value</span></span>                          | <span data-ttu-id="65276-110">長度</span><span class="sxs-lookup"><span data-stu-id="65276-110">Length</span></span>                         |
|--------------------------------|--------------------------------|
| <span data-ttu-id="65276-111">密碼</span><span class="sxs-lookup"><span data-stu-id="65276-111">Password</span></span><br/>            | <span data-ttu-id="65276-112">0到14個字元</span><span class="sxs-lookup"><span data-stu-id="65276-112">0 to 14 characters</span></span><br/>  |
| <span data-ttu-id="65276-113">帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="65276-113">Account Name</span></span><br/>        | <span data-ttu-id="65276-114">0到20個字元</span><span class="sxs-lookup"><span data-stu-id="65276-114">0 to 20 characters</span></span><br/>  |
| <span data-ttu-id="65276-115">網域名稱</span><span class="sxs-lookup"><span data-stu-id="65276-115">Domain Name</span></span><br/>         | <span data-ttu-id="65276-116">0到15個字元</span><span class="sxs-lookup"><span data-stu-id="65276-116">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="65276-117">電腦名稱</span><span class="sxs-lookup"><span data-stu-id="65276-117">Computer Name</span></span><br/>       | <span data-ttu-id="65276-118">0到15個字元</span><span class="sxs-lookup"><span data-stu-id="65276-118">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="65276-119">註解</span><span class="sxs-lookup"><span data-stu-id="65276-119">Comments</span></span><br/>            | <span data-ttu-id="65276-120">0到48個字元</span><span class="sxs-lookup"><span data-stu-id="65276-120">0 to 48 characters</span></span><br/>  |
| <span data-ttu-id="65276-121">主目錄</span><span class="sxs-lookup"><span data-stu-id="65276-121">Home Directory</span></span><br/>      | <span data-ttu-id="65276-122">0到256個字元</span><span class="sxs-lookup"><span data-stu-id="65276-122">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="65276-123">腳本路徑</span><span class="sxs-lookup"><span data-stu-id="65276-123">Script Path</span></span><br/>         | <span data-ttu-id="65276-124">0到256個字元</span><span class="sxs-lookup"><span data-stu-id="65276-124">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="65276-125">每週的時間單位</span><span class="sxs-lookup"><span data-stu-id="65276-125">Time Units Per Week</span></span><br/> | <span data-ttu-id="65276-126">168個位 (21 個位元組) </span><span class="sxs-lookup"><span data-stu-id="65276-126">168 bits (21 bytes)</span></span><br/> |



 



| <span data-ttu-id="65276-127">進入</span><span class="sxs-lookup"><span data-stu-id="65276-127">Entry</span></span> | <span data-ttu-id="65276-128">值</span><span class="sxs-lookup"><span data-stu-id="65276-128">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="65276-129">CN</span><span class="sxs-lookup"><span data-stu-id="65276-129">CN</span></span>                | <span data-ttu-id="65276-130">UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="65276-130">UAS-Compat</span></span>                           |
| <span data-ttu-id="65276-131">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="65276-131">Ldap-Display-Name</span></span> | <span data-ttu-id="65276-132">uASCompat</span><span class="sxs-lookup"><span data-stu-id="65276-132">uASCompat</span></span>                            |
| <span data-ttu-id="65276-133">大小</span><span class="sxs-lookup"><span data-stu-id="65276-133">Size</span></span>              | \-                                   |
| <span data-ttu-id="65276-134">更新許可權</span><span class="sxs-lookup"><span data-stu-id="65276-134">Update Privilege</span></span>  | <span data-ttu-id="65276-135">由系統管理員執行。</span><span class="sxs-lookup"><span data-stu-id="65276-135">Performed by an administrator.</span></span>       |
| <span data-ttu-id="65276-136">更新頻率</span><span class="sxs-lookup"><span data-stu-id="65276-136">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="65276-137">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="65276-137">Attribute-Id</span></span>      | <span data-ttu-id="65276-138">1.2.840.113556.1.4.155</span><span class="sxs-lookup"><span data-stu-id="65276-138">1.2.840.113556.1.4.155</span></span>               |
| <span data-ttu-id="65276-139">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="65276-139">System-Id-Guid</span></span>    | <span data-ttu-id="65276-140">bf967a61-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="65276-140">bf967a61-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="65276-141">Syntax</span><span class="sxs-lookup"><span data-stu-id="65276-141">Syntax</span></span>            | [<span data-ttu-id="65276-142">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="65276-142">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="65276-143">實作</span><span class="sxs-lookup"><span data-stu-id="65276-143">Implementations</span></span>

-   [<span data-ttu-id="65276-144">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="65276-144">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="65276-145">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="65276-145">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="65276-146">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="65276-146">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="65276-147">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="65276-147">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="65276-148">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="65276-148">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="65276-149">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="65276-149">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="65276-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="65276-150">Windows 2000 Server</span></span>



| <span data-ttu-id="65276-151">進入</span><span class="sxs-lookup"><span data-stu-id="65276-151">Entry</span></span> | <span data-ttu-id="65276-152">值</span><span class="sxs-lookup"><span data-stu-id="65276-152">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="65276-153">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65276-153">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65276-154">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="65276-155">System-Only</span></span>            | <span data-ttu-id="65276-156">否</span><span class="sxs-lookup"><span data-stu-id="65276-156">False</span></span>                                                 |
| <span data-ttu-id="65276-157">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65276-157">Is-Single-Valued</span></span>       | <span data-ttu-id="65276-158">對</span><span class="sxs-lookup"><span data-stu-id="65276-158">True</span></span>                                                  |
| <span data-ttu-id="65276-159">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65276-159">Is Indexed</span></span>             | <span data-ttu-id="65276-160">否</span><span class="sxs-lookup"><span data-stu-id="65276-160">False</span></span>                                                 |
| <span data-ttu-id="65276-161">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65276-161">In Global Catalog</span></span>      | <span data-ttu-id="65276-162">否</span><span class="sxs-lookup"><span data-stu-id="65276-162">False</span></span>                                                 |
| <span data-ttu-id="65276-163">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65276-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="65276-164">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65276-164">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="65276-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65276-165">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="65276-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65276-166">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="65276-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-167">Search-Flags</span></span>           | <span data-ttu-id="65276-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65276-168">0x00000000</span></span>                                            |
| <span data-ttu-id="65276-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-169">System-Flags</span></span>           | <span data-ttu-id="65276-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65276-170">0x00000010</span></span>                                            |
| <span data-ttu-id="65276-171">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65276-171">Classes used in</span></span>        | [<span data-ttu-id="65276-172">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="65276-172">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="65276-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65276-173">Windows Server 2003</span></span>



| <span data-ttu-id="65276-174">進入</span><span class="sxs-lookup"><span data-stu-id="65276-174">Entry</span></span> | <span data-ttu-id="65276-175">值</span><span class="sxs-lookup"><span data-stu-id="65276-175">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="65276-176">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65276-176">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65276-177">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="65276-178">System-Only</span></span>            | <span data-ttu-id="65276-179">否</span><span class="sxs-lookup"><span data-stu-id="65276-179">False</span></span>                                                 |
| <span data-ttu-id="65276-180">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65276-180">Is-Single-Valued</span></span>       | <span data-ttu-id="65276-181">對</span><span class="sxs-lookup"><span data-stu-id="65276-181">True</span></span>                                                  |
| <span data-ttu-id="65276-182">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65276-182">Is Indexed</span></span>             | <span data-ttu-id="65276-183">否</span><span class="sxs-lookup"><span data-stu-id="65276-183">False</span></span>                                                 |
| <span data-ttu-id="65276-184">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65276-184">In Global Catalog</span></span>      | <span data-ttu-id="65276-185">否</span><span class="sxs-lookup"><span data-stu-id="65276-185">False</span></span>                                                 |
| <span data-ttu-id="65276-186">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65276-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="65276-187">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65276-187">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="65276-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65276-188">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="65276-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65276-189">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="65276-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-190">Search-Flags</span></span>           | <span data-ttu-id="65276-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65276-191">0x00000000</span></span>                                            |
| <span data-ttu-id="65276-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-192">System-Flags</span></span>           | <span data-ttu-id="65276-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65276-193">0x00000010</span></span>                                            |
| <span data-ttu-id="65276-194">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65276-194">Classes used in</span></span>        | [<span data-ttu-id="65276-195">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="65276-195">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="65276-196">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="65276-196">Windows Server 2003 R2</span></span>



| <span data-ttu-id="65276-197">進入</span><span class="sxs-lookup"><span data-stu-id="65276-197">Entry</span></span> | <span data-ttu-id="65276-198">值</span><span class="sxs-lookup"><span data-stu-id="65276-198">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="65276-199">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65276-199">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65276-200">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="65276-201">System-Only</span></span>            | <span data-ttu-id="65276-202">否</span><span class="sxs-lookup"><span data-stu-id="65276-202">False</span></span>                                                 |
| <span data-ttu-id="65276-203">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65276-203">Is-Single-Valued</span></span>       | <span data-ttu-id="65276-204">對</span><span class="sxs-lookup"><span data-stu-id="65276-204">True</span></span>                                                  |
| <span data-ttu-id="65276-205">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65276-205">Is Indexed</span></span>             | <span data-ttu-id="65276-206">否</span><span class="sxs-lookup"><span data-stu-id="65276-206">False</span></span>                                                 |
| <span data-ttu-id="65276-207">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65276-207">In Global Catalog</span></span>      | <span data-ttu-id="65276-208">否</span><span class="sxs-lookup"><span data-stu-id="65276-208">False</span></span>                                                 |
| <span data-ttu-id="65276-209">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65276-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="65276-210">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65276-210">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="65276-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65276-211">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="65276-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65276-212">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="65276-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-213">Search-Flags</span></span>           | <span data-ttu-id="65276-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65276-214">0x00000000</span></span>                                            |
| <span data-ttu-id="65276-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-215">System-Flags</span></span>           | <span data-ttu-id="65276-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65276-216">0x00000010</span></span>                                            |
| <span data-ttu-id="65276-217">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65276-217">Classes used in</span></span>        | [<span data-ttu-id="65276-218">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="65276-218">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="65276-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65276-219">Windows Server 2008</span></span>



| <span data-ttu-id="65276-220">進入</span><span class="sxs-lookup"><span data-stu-id="65276-220">Entry</span></span> | <span data-ttu-id="65276-221">值</span><span class="sxs-lookup"><span data-stu-id="65276-221">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="65276-222">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65276-222">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-223">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65276-223">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="65276-224">System-Only</span></span>            | <span data-ttu-id="65276-225">否</span><span class="sxs-lookup"><span data-stu-id="65276-225">False</span></span>                                                 |
| <span data-ttu-id="65276-226">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65276-226">Is-Single-Valued</span></span>       | <span data-ttu-id="65276-227">對</span><span class="sxs-lookup"><span data-stu-id="65276-227">True</span></span>                                                  |
| <span data-ttu-id="65276-228">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65276-228">Is Indexed</span></span>             | <span data-ttu-id="65276-229">否</span><span class="sxs-lookup"><span data-stu-id="65276-229">False</span></span>                                                 |
| <span data-ttu-id="65276-230">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65276-230">In Global Catalog</span></span>      | <span data-ttu-id="65276-231">否</span><span class="sxs-lookup"><span data-stu-id="65276-231">False</span></span>                                                 |
| <span data-ttu-id="65276-232">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65276-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="65276-233">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65276-233">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="65276-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65276-234">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="65276-235">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65276-235">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="65276-236">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-236">Search-Flags</span></span>           | <span data-ttu-id="65276-237">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65276-237">0x00000000</span></span>                                            |
| <span data-ttu-id="65276-238">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-238">System-Flags</span></span>           | <span data-ttu-id="65276-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65276-239">0x00000010</span></span>                                            |
| <span data-ttu-id="65276-240">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65276-240">Classes used in</span></span>        | [<span data-ttu-id="65276-241">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="65276-241">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="65276-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65276-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="65276-243">進入</span><span class="sxs-lookup"><span data-stu-id="65276-243">Entry</span></span> | <span data-ttu-id="65276-244">值</span><span class="sxs-lookup"><span data-stu-id="65276-244">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="65276-245">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65276-245">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65276-246">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="65276-247">System-Only</span></span>            | <span data-ttu-id="65276-248">否</span><span class="sxs-lookup"><span data-stu-id="65276-248">False</span></span>                                                 |
| <span data-ttu-id="65276-249">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65276-249">Is-Single-Valued</span></span>       | <span data-ttu-id="65276-250">對</span><span class="sxs-lookup"><span data-stu-id="65276-250">True</span></span>                                                  |
| <span data-ttu-id="65276-251">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65276-251">Is Indexed</span></span>             | <span data-ttu-id="65276-252">否</span><span class="sxs-lookup"><span data-stu-id="65276-252">False</span></span>                                                 |
| <span data-ttu-id="65276-253">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65276-253">In Global Catalog</span></span>      | <span data-ttu-id="65276-254">否</span><span class="sxs-lookup"><span data-stu-id="65276-254">False</span></span>                                                 |
| <span data-ttu-id="65276-255">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65276-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="65276-256">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65276-256">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="65276-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65276-257">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="65276-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65276-258">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="65276-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-259">Search-Flags</span></span>           | <span data-ttu-id="65276-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65276-260">0x00000000</span></span>                                            |
| <span data-ttu-id="65276-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-261">System-Flags</span></span>           | <span data-ttu-id="65276-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65276-262">0x00000010</span></span>                                            |
| <span data-ttu-id="65276-263">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65276-263">Classes used in</span></span>        | [<span data-ttu-id="65276-264">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="65276-264">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="65276-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65276-265">Windows Server 2012</span></span>



| <span data-ttu-id="65276-266">進入</span><span class="sxs-lookup"><span data-stu-id="65276-266">Entry</span></span> | <span data-ttu-id="65276-267">值</span><span class="sxs-lookup"><span data-stu-id="65276-267">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="65276-268">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65276-268">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65276-269">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="65276-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="65276-270">System-Only</span></span>            | <span data-ttu-id="65276-271">否</span><span class="sxs-lookup"><span data-stu-id="65276-271">False</span></span>                                                 |
| <span data-ttu-id="65276-272">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65276-272">Is-Single-Valued</span></span>       | <span data-ttu-id="65276-273">對</span><span class="sxs-lookup"><span data-stu-id="65276-273">True</span></span>                                                  |
| <span data-ttu-id="65276-274">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65276-274">Is Indexed</span></span>             | <span data-ttu-id="65276-275">否</span><span class="sxs-lookup"><span data-stu-id="65276-275">False</span></span>                                                 |
| <span data-ttu-id="65276-276">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65276-276">In Global Catalog</span></span>      | <span data-ttu-id="65276-277">否</span><span class="sxs-lookup"><span data-stu-id="65276-277">False</span></span>                                                 |
| <span data-ttu-id="65276-278">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65276-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="65276-279">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65276-279">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="65276-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65276-280">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="65276-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65276-281">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="65276-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-282">Search-Flags</span></span>           | <span data-ttu-id="65276-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65276-283">0x00000000</span></span>                                            |
| <span data-ttu-id="65276-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65276-284">System-Flags</span></span>           | <span data-ttu-id="65276-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65276-285">0x00000010</span></span>                                            |
| <span data-ttu-id="65276-286">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65276-286">Classes used in</span></span>        | [<span data-ttu-id="65276-287">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="65276-287">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 






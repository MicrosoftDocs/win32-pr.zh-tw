---
title: 錯誤-Pwd-Count 屬性
description: 使用者嘗試使用不正確的密碼登入帳戶的次數。
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- 錯誤-Pwd-Count 屬性 AD 架構
- badPwdCount 屬性 AD 架構
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3a406058737773781874a81e9968786e1523d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107285"
---
# <a name="bad-pwd-count-attribute"></a><span data-ttu-id="1d45a-105">錯誤-Pwd-Count 屬性</span><span class="sxs-lookup"><span data-stu-id="1d45a-105">Bad-Pwd-Count attribute</span></span>

<span data-ttu-id="1d45a-106">使用者嘗試使用不正確的密碼登入帳戶的次數。</span><span class="sxs-lookup"><span data-stu-id="1d45a-106">The number of times the user tried to log on to the account using an incorrect password.</span></span> <span data-ttu-id="1d45a-107">值為0表示值不明。</span><span class="sxs-lookup"><span data-stu-id="1d45a-107">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="1d45a-108">進入</span><span class="sxs-lookup"><span data-stu-id="1d45a-108">Entry</span></span> | <span data-ttu-id="1d45a-109">值</span><span class="sxs-lookup"><span data-stu-id="1d45a-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="1d45a-110">CN</span><span class="sxs-lookup"><span data-stu-id="1d45a-110">CN</span></span>                | <span data-ttu-id="1d45a-111">錯誤-Pwd-計數</span><span class="sxs-lookup"><span data-stu-id="1d45a-111">Bad-Pwd-Count</span></span>                             |
| <span data-ttu-id="1d45a-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1d45a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="1d45a-113">badPwdCount</span><span class="sxs-lookup"><span data-stu-id="1d45a-113">badPwdCount</span></span>                               |
| <span data-ttu-id="1d45a-114">大小</span><span class="sxs-lookup"><span data-stu-id="1d45a-114">Size</span></span>              | <span data-ttu-id="1d45a-115">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="1d45a-115">4 bytes</span></span>                                   |
| <span data-ttu-id="1d45a-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1d45a-116">Update Privilege</span></span>  | <span data-ttu-id="1d45a-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="1d45a-117">This value is set by the system.</span></span>          |
| <span data-ttu-id="1d45a-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1d45a-118">Update Frequency</span></span>  | <span data-ttu-id="1d45a-119">每次使用者輸入錯誤密碼時。</span><span class="sxs-lookup"><span data-stu-id="1d45a-119">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="1d45a-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1d45a-120">Attribute-Id</span></span>      | <span data-ttu-id="1d45a-121">1.2.840.113556.1.4.12</span><span class="sxs-lookup"><span data-stu-id="1d45a-121">1.2.840.113556.1.4.12</span></span>                     |
| <span data-ttu-id="1d45a-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1d45a-122">System-Id-Guid</span></span>    | <span data-ttu-id="1d45a-123">bf96792e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1d45a-123">bf96792e-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="1d45a-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d45a-124">Syntax</span></span>            | [<span data-ttu-id="1d45a-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="1d45a-125">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="1d45a-126">實作</span><span class="sxs-lookup"><span data-stu-id="1d45a-126">Implementations</span></span>

-   [<span data-ttu-id="1d45a-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1d45a-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1d45a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1d45a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1d45a-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="1d45a-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1d45a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1d45a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1d45a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1d45a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1d45a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1d45a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1d45a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1d45a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1d45a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d45a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="1d45a-135">進入</span><span class="sxs-lookup"><span data-stu-id="1d45a-135">Entry</span></span> | <span data-ttu-id="1d45a-136">值</span><span class="sxs-lookup"><span data-stu-id="1d45a-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1d45a-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d45a-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45a-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45a-139">System-Only</span></span>            | <span data-ttu-id="1d45a-140">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-140">False</span></span>                             |
| <span data-ttu-id="1d45a-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d45a-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45a-142">對</span><span class="sxs-lookup"><span data-stu-id="1d45a-142">True</span></span>                              |
| <span data-ttu-id="1d45a-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d45a-143">Is Indexed</span></span>             | <span data-ttu-id="1d45a-144">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-144">False</span></span>                             |
| <span data-ttu-id="1d45a-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d45a-145">In Global Catalog</span></span>      | <span data-ttu-id="1d45a-146">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-146">False</span></span>                             |
| <span data-ttu-id="1d45a-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d45a-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45a-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d45a-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1d45a-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45a-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1d45a-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45a-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1d45a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-151">Search-Flags</span></span>           | <span data-ttu-id="1d45a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45a-152">0x00000000</span></span>                        |
| <span data-ttu-id="1d45a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-153">System-Flags</span></span>           | <span data-ttu-id="1d45a-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1d45a-154">0x00000011</span></span>                        |
| <span data-ttu-id="1d45a-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d45a-155">Classes used in</span></span>        | [<span data-ttu-id="1d45a-156">**User**</span><span class="sxs-lookup"><span data-stu-id="1d45a-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1d45a-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d45a-157">Windows Server 2003</span></span>



| <span data-ttu-id="1d45a-158">進入</span><span class="sxs-lookup"><span data-stu-id="1d45a-158">Entry</span></span> | <span data-ttu-id="1d45a-159">值</span><span class="sxs-lookup"><span data-stu-id="1d45a-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1d45a-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d45a-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45a-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45a-162">System-Only</span></span>            | <span data-ttu-id="1d45a-163">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-163">False</span></span>                             |
| <span data-ttu-id="1d45a-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d45a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45a-165">對</span><span class="sxs-lookup"><span data-stu-id="1d45a-165">True</span></span>                              |
| <span data-ttu-id="1d45a-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d45a-166">Is Indexed</span></span>             | <span data-ttu-id="1d45a-167">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-167">False</span></span>                             |
| <span data-ttu-id="1d45a-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d45a-168">In Global Catalog</span></span>      | <span data-ttu-id="1d45a-169">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-169">False</span></span>                             |
| <span data-ttu-id="1d45a-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d45a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45a-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d45a-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1d45a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45a-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1d45a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45a-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1d45a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-174">Search-Flags</span></span>           | <span data-ttu-id="1d45a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45a-175">0x00000000</span></span>                        |
| <span data-ttu-id="1d45a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-176">System-Flags</span></span>           | <span data-ttu-id="1d45a-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1d45a-177">0x00000011</span></span>                        |
| <span data-ttu-id="1d45a-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d45a-178">Classes used in</span></span>        | [<span data-ttu-id="1d45a-179">**User**</span><span class="sxs-lookup"><span data-stu-id="1d45a-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1d45a-180">亞當</span><span class="sxs-lookup"><span data-stu-id="1d45a-180">ADAM</span></span>



| <span data-ttu-id="1d45a-181">進入</span><span class="sxs-lookup"><span data-stu-id="1d45a-181">Entry</span></span> | <span data-ttu-id="1d45a-182">值</span><span class="sxs-lookup"><span data-stu-id="1d45a-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1d45a-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d45a-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45a-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="1d45a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45a-185">System-Only</span></span>            | <span data-ttu-id="1d45a-186">對</span><span class="sxs-lookup"><span data-stu-id="1d45a-186">True</span></span>                                                              |
| <span data-ttu-id="1d45a-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d45a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45a-188">對</span><span class="sxs-lookup"><span data-stu-id="1d45a-188">True</span></span>                                                              |
| <span data-ttu-id="1d45a-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d45a-189">Is Indexed</span></span>             | <span data-ttu-id="1d45a-190">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-190">False</span></span>                                                             |
| <span data-ttu-id="1d45a-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d45a-191">In Global Catalog</span></span>      | <span data-ttu-id="1d45a-192">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-192">False</span></span>                                                             |
| <span data-ttu-id="1d45a-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d45a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45a-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d45a-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="1d45a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45a-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="1d45a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45a-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="1d45a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-197">Search-Flags</span></span>           | <span data-ttu-id="1d45a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45a-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="1d45a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-199">System-Flags</span></span>           | <span data-ttu-id="1d45a-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1d45a-200">0x00000011</span></span>                                                        |
| <span data-ttu-id="1d45a-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d45a-201">Classes used in</span></span>        | [<span data-ttu-id="1d45a-202">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="1d45a-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1d45a-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1d45a-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1d45a-204">進入</span><span class="sxs-lookup"><span data-stu-id="1d45a-204">Entry</span></span> | <span data-ttu-id="1d45a-205">值</span><span class="sxs-lookup"><span data-stu-id="1d45a-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1d45a-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d45a-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45a-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45a-208">System-Only</span></span>            | <span data-ttu-id="1d45a-209">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-209">False</span></span>                             |
| <span data-ttu-id="1d45a-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d45a-210">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45a-211">對</span><span class="sxs-lookup"><span data-stu-id="1d45a-211">True</span></span>                              |
| <span data-ttu-id="1d45a-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d45a-212">Is Indexed</span></span>             | <span data-ttu-id="1d45a-213">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-213">False</span></span>                             |
| <span data-ttu-id="1d45a-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d45a-214">In Global Catalog</span></span>      | <span data-ttu-id="1d45a-215">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-215">False</span></span>                             |
| <span data-ttu-id="1d45a-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d45a-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45a-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d45a-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1d45a-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45a-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1d45a-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45a-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1d45a-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-220">Search-Flags</span></span>           | <span data-ttu-id="1d45a-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45a-221">0x00000000</span></span>                        |
| <span data-ttu-id="1d45a-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-222">System-Flags</span></span>           | <span data-ttu-id="1d45a-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1d45a-223">0x00000011</span></span>                        |
| <span data-ttu-id="1d45a-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d45a-224">Classes used in</span></span>        | [<span data-ttu-id="1d45a-225">**User**</span><span class="sxs-lookup"><span data-stu-id="1d45a-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1d45a-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d45a-226">Windows Server 2008</span></span>



| <span data-ttu-id="1d45a-227">進入</span><span class="sxs-lookup"><span data-stu-id="1d45a-227">Entry</span></span> | <span data-ttu-id="1d45a-228">值</span><span class="sxs-lookup"><span data-stu-id="1d45a-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1d45a-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d45a-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45a-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45a-231">System-Only</span></span>            | <span data-ttu-id="1d45a-232">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-232">False</span></span>                             |
| <span data-ttu-id="1d45a-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d45a-233">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45a-234">對</span><span class="sxs-lookup"><span data-stu-id="1d45a-234">True</span></span>                              |
| <span data-ttu-id="1d45a-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d45a-235">Is Indexed</span></span>             | <span data-ttu-id="1d45a-236">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-236">False</span></span>                             |
| <span data-ttu-id="1d45a-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d45a-237">In Global Catalog</span></span>      | <span data-ttu-id="1d45a-238">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-238">False</span></span>                             |
| <span data-ttu-id="1d45a-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d45a-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45a-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d45a-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1d45a-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45a-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1d45a-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45a-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1d45a-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-243">Search-Flags</span></span>           | <span data-ttu-id="1d45a-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45a-244">0x00000000</span></span>                        |
| <span data-ttu-id="1d45a-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-245">System-Flags</span></span>           | <span data-ttu-id="1d45a-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1d45a-246">0x00000011</span></span>                        |
| <span data-ttu-id="1d45a-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d45a-247">Classes used in</span></span>        | [<span data-ttu-id="1d45a-248">**User**</span><span class="sxs-lookup"><span data-stu-id="1d45a-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1d45a-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d45a-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1d45a-250">進入</span><span class="sxs-lookup"><span data-stu-id="1d45a-250">Entry</span></span> | <span data-ttu-id="1d45a-251">值</span><span class="sxs-lookup"><span data-stu-id="1d45a-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1d45a-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d45a-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45a-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45a-254">System-Only</span></span>            | <span data-ttu-id="1d45a-255">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-255">False</span></span>                             |
| <span data-ttu-id="1d45a-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d45a-256">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45a-257">對</span><span class="sxs-lookup"><span data-stu-id="1d45a-257">True</span></span>                              |
| <span data-ttu-id="1d45a-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d45a-258">Is Indexed</span></span>             | <span data-ttu-id="1d45a-259">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-259">False</span></span>                             |
| <span data-ttu-id="1d45a-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d45a-260">In Global Catalog</span></span>      | <span data-ttu-id="1d45a-261">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-261">False</span></span>                             |
| <span data-ttu-id="1d45a-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d45a-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45a-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d45a-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1d45a-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45a-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1d45a-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45a-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1d45a-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-266">Search-Flags</span></span>           | <span data-ttu-id="1d45a-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45a-267">0x00000000</span></span>                        |
| <span data-ttu-id="1d45a-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-268">System-Flags</span></span>           | <span data-ttu-id="1d45a-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1d45a-269">0x00000011</span></span>                        |
| <span data-ttu-id="1d45a-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d45a-270">Classes used in</span></span>        | [<span data-ttu-id="1d45a-271">**User**</span><span class="sxs-lookup"><span data-stu-id="1d45a-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1d45a-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d45a-272">Windows Server 2012</span></span>



| <span data-ttu-id="1d45a-273">進入</span><span class="sxs-lookup"><span data-stu-id="1d45a-273">Entry</span></span> | <span data-ttu-id="1d45a-274">值</span><span class="sxs-lookup"><span data-stu-id="1d45a-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1d45a-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d45a-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d45a-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1d45a-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d45a-277">System-Only</span></span>            | <span data-ttu-id="1d45a-278">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-278">False</span></span>                             |
| <span data-ttu-id="1d45a-279">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d45a-279">Is-Single-Valued</span></span>       | <span data-ttu-id="1d45a-280">對</span><span class="sxs-lookup"><span data-stu-id="1d45a-280">True</span></span>                              |
| <span data-ttu-id="1d45a-281">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d45a-281">Is Indexed</span></span>             | <span data-ttu-id="1d45a-282">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-282">False</span></span>                             |
| <span data-ttu-id="1d45a-283">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d45a-283">In Global Catalog</span></span>      | <span data-ttu-id="1d45a-284">否</span><span class="sxs-lookup"><span data-stu-id="1d45a-284">False</span></span>                             |
| <span data-ttu-id="1d45a-285">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d45a-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d45a-286">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d45a-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1d45a-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d45a-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1d45a-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d45a-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1d45a-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-289">Search-Flags</span></span>           | <span data-ttu-id="1d45a-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d45a-290">0x00000000</span></span>                        |
| <span data-ttu-id="1d45a-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d45a-291">System-Flags</span></span>           | <span data-ttu-id="1d45a-292">0x00000011</span><span class="sxs-lookup"><span data-stu-id="1d45a-292">0x00000011</span></span>                        |
| <span data-ttu-id="1d45a-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d45a-293">Classes used in</span></span>        | [<span data-ttu-id="1d45a-294">**User**</span><span class="sxs-lookup"><span data-stu-id="1d45a-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1d45a-295">備註</span><span class="sxs-lookup"><span data-stu-id="1d45a-295">Remarks</span></span>

<span data-ttu-id="1d45a-296">這個屬性不會複寫，並且會在網域中的每個網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="1d45a-296">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span>

<span data-ttu-id="1d45a-297">當使用者成功登入網域控制站時，會在特定網域控制站上重設此屬性。</span><span class="sxs-lookup"><span data-stu-id="1d45a-297">This attribute is reset on a specific domain controller when the user successfully logs onto that domain controller.</span></span>

 

 






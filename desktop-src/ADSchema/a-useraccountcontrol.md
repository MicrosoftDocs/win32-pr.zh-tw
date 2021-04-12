---
title: 使用者帳戶控制屬性
description: 控制使用者帳戶行為的旗標。
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- 使用者-帳戶控制屬性 AD 架構
- userAccountControl 屬性 AD 架構
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107924"
---
# <a name="user-account-control-attribute"></a><span data-ttu-id="a29c1-105">使用者帳戶控制屬性</span><span class="sxs-lookup"><span data-stu-id="a29c1-105">User-Account-Control attribute</span></span>

<span data-ttu-id="a29c1-106">控制使用者帳戶行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="a29c1-106">Flags that control the behavior of the user account.</span></span>



| <span data-ttu-id="a29c1-107">進入</span><span class="sxs-lookup"><span data-stu-id="a29c1-107">Entry</span></span> | <span data-ttu-id="a29c1-108">值</span><span class="sxs-lookup"><span data-stu-id="a29c1-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="a29c1-109">CN</span><span class="sxs-lookup"><span data-stu-id="a29c1-109">CN</span></span>                | <span data-ttu-id="a29c1-110">使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="a29c1-110">User-Account-Control</span></span>                  |
| <span data-ttu-id="a29c1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a29c1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a29c1-112">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="a29c1-112">userAccountControl</span></span>                    |
| <span data-ttu-id="a29c1-113">大小</span><span class="sxs-lookup"><span data-stu-id="a29c1-113">Size</span></span>              | <span data-ttu-id="a29c1-114">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="a29c1-114">4 bytes.</span></span>                              |
| <span data-ttu-id="a29c1-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a29c1-115">Update Privilege</span></span>  | <span data-ttu-id="a29c1-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="a29c1-116">This value is set by the system.</span></span>      |
| <span data-ttu-id="a29c1-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a29c1-117">Update Frequency</span></span>  | <span data-ttu-id="a29c1-118">每次帳戶原則變更時。</span><span class="sxs-lookup"><span data-stu-id="a29c1-118">Each time the account policy changes.</span></span> |
| <span data-ttu-id="a29c1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a29c1-119">Attribute-Id</span></span>      | <span data-ttu-id="a29c1-120">1.2.840.113556.1.4.8</span><span class="sxs-lookup"><span data-stu-id="a29c1-120">1.2.840.113556.1.4.8</span></span>                  |
| <span data-ttu-id="a29c1-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a29c1-121">System-Id-Guid</span></span>    | <span data-ttu-id="a29c1-122">bf967a68-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a29c1-122">bf967a68-0de6-11d0-a285-00aa003049e2</span></span>  |
| <span data-ttu-id="a29c1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a29c1-123">Syntax</span></span>            | [<span data-ttu-id="a29c1-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="a29c1-124">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="a29c1-125">實作</span><span class="sxs-lookup"><span data-stu-id="a29c1-125">Implementations</span></span>

-   [<span data-ttu-id="a29c1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a29c1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a29c1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a29c1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a29c1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a29c1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a29c1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a29c1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a29c1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a29c1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a29c1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a29c1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a29c1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a29c1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a29c1-133">進入</span><span class="sxs-lookup"><span data-stu-id="a29c1-133">Entry</span></span> | <span data-ttu-id="a29c1-134">值</span><span class="sxs-lookup"><span data-stu-id="a29c1-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a29c1-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a29c1-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a29c1-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a29c1-137">System-Only</span></span>            | <span data-ttu-id="a29c1-138">否</span><span class="sxs-lookup"><span data-stu-id="a29c1-138">False</span></span>                             |
| <span data-ttu-id="a29c1-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a29c1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a29c1-140">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-140">True</span></span>                              |
| <span data-ttu-id="a29c1-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a29c1-141">Is Indexed</span></span>             | <span data-ttu-id="a29c1-142">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-142">True</span></span>                              |
| <span data-ttu-id="a29c1-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a29c1-143">In Global Catalog</span></span>      | <span data-ttu-id="a29c1-144">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-144">True</span></span>                              |
| <span data-ttu-id="a29c1-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a29c1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a29c1-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a29c1-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a29c1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a29c1-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a29c1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a29c1-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a29c1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-149">Search-Flags</span></span>           | <span data-ttu-id="a29c1-150">0x00000019</span><span class="sxs-lookup"><span data-stu-id="a29c1-150">0x00000019</span></span>                        |
| <span data-ttu-id="a29c1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-151">System-Flags</span></span>           | <span data-ttu-id="a29c1-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a29c1-152">0x00000012</span></span>                        |
| <span data-ttu-id="a29c1-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a29c1-153">Classes used in</span></span>        | [<span data-ttu-id="a29c1-154">**User**</span><span class="sxs-lookup"><span data-stu-id="a29c1-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a29c1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a29c1-155">Windows Server 2003</span></span>



| <span data-ttu-id="a29c1-156">進入</span><span class="sxs-lookup"><span data-stu-id="a29c1-156">Entry</span></span> | <span data-ttu-id="a29c1-157">值</span><span class="sxs-lookup"><span data-stu-id="a29c1-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a29c1-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a29c1-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a29c1-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a29c1-160">System-Only</span></span>            | <span data-ttu-id="a29c1-161">否</span><span class="sxs-lookup"><span data-stu-id="a29c1-161">False</span></span>                             |
| <span data-ttu-id="a29c1-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a29c1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a29c1-163">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-163">True</span></span>                              |
| <span data-ttu-id="a29c1-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a29c1-164">Is Indexed</span></span>             | <span data-ttu-id="a29c1-165">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-165">True</span></span>                              |
| <span data-ttu-id="a29c1-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a29c1-166">In Global Catalog</span></span>      | <span data-ttu-id="a29c1-167">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-167">True</span></span>                              |
| <span data-ttu-id="a29c1-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a29c1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a29c1-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a29c1-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a29c1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a29c1-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a29c1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a29c1-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a29c1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-172">Search-Flags</span></span>           | <span data-ttu-id="a29c1-173">0x00000019</span><span class="sxs-lookup"><span data-stu-id="a29c1-173">0x00000019</span></span>                        |
| <span data-ttu-id="a29c1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-174">System-Flags</span></span>           | <span data-ttu-id="a29c1-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a29c1-175">0x00000012</span></span>                        |
| <span data-ttu-id="a29c1-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a29c1-176">Classes used in</span></span>        | [<span data-ttu-id="a29c1-177">**User**</span><span class="sxs-lookup"><span data-stu-id="a29c1-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a29c1-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a29c1-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a29c1-179">進入</span><span class="sxs-lookup"><span data-stu-id="a29c1-179">Entry</span></span> | <span data-ttu-id="a29c1-180">值</span><span class="sxs-lookup"><span data-stu-id="a29c1-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a29c1-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a29c1-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a29c1-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a29c1-183">System-Only</span></span>            | <span data-ttu-id="a29c1-184">否</span><span class="sxs-lookup"><span data-stu-id="a29c1-184">False</span></span>                             |
| <span data-ttu-id="a29c1-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a29c1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a29c1-186">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-186">True</span></span>                              |
| <span data-ttu-id="a29c1-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a29c1-187">Is Indexed</span></span>             | <span data-ttu-id="a29c1-188">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-188">True</span></span>                              |
| <span data-ttu-id="a29c1-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a29c1-189">In Global Catalog</span></span>      | <span data-ttu-id="a29c1-190">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-190">True</span></span>                              |
| <span data-ttu-id="a29c1-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a29c1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a29c1-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a29c1-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a29c1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a29c1-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a29c1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a29c1-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a29c1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-195">Search-Flags</span></span>           | <span data-ttu-id="a29c1-196">0x00000019</span><span class="sxs-lookup"><span data-stu-id="a29c1-196">0x00000019</span></span>                        |
| <span data-ttu-id="a29c1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-197">System-Flags</span></span>           | <span data-ttu-id="a29c1-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a29c1-198">0x00000012</span></span>                        |
| <span data-ttu-id="a29c1-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a29c1-199">Classes used in</span></span>        | [<span data-ttu-id="a29c1-200">**User**</span><span class="sxs-lookup"><span data-stu-id="a29c1-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a29c1-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a29c1-201">Windows Server 2008</span></span>



| <span data-ttu-id="a29c1-202">進入</span><span class="sxs-lookup"><span data-stu-id="a29c1-202">Entry</span></span> | <span data-ttu-id="a29c1-203">值</span><span class="sxs-lookup"><span data-stu-id="a29c1-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a29c1-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a29c1-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a29c1-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a29c1-206">System-Only</span></span>            | <span data-ttu-id="a29c1-207">否</span><span class="sxs-lookup"><span data-stu-id="a29c1-207">False</span></span>                             |
| <span data-ttu-id="a29c1-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a29c1-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a29c1-209">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-209">True</span></span>                              |
| <span data-ttu-id="a29c1-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a29c1-210">Is Indexed</span></span>             | <span data-ttu-id="a29c1-211">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-211">True</span></span>                              |
| <span data-ttu-id="a29c1-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a29c1-212">In Global Catalog</span></span>      | <span data-ttu-id="a29c1-213">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-213">True</span></span>                              |
| <span data-ttu-id="a29c1-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a29c1-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a29c1-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a29c1-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a29c1-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a29c1-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a29c1-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a29c1-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a29c1-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-218">Search-Flags</span></span>           | <span data-ttu-id="a29c1-219">0x00000019</span><span class="sxs-lookup"><span data-stu-id="a29c1-219">0x00000019</span></span>                        |
| <span data-ttu-id="a29c1-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-220">System-Flags</span></span>           | <span data-ttu-id="a29c1-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a29c1-221">0x00000012</span></span>                        |
| <span data-ttu-id="a29c1-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a29c1-222">Classes used in</span></span>        | [<span data-ttu-id="a29c1-223">**User**</span><span class="sxs-lookup"><span data-stu-id="a29c1-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a29c1-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a29c1-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a29c1-225">進入</span><span class="sxs-lookup"><span data-stu-id="a29c1-225">Entry</span></span> | <span data-ttu-id="a29c1-226">值</span><span class="sxs-lookup"><span data-stu-id="a29c1-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a29c1-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a29c1-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a29c1-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a29c1-229">System-Only</span></span>            | <span data-ttu-id="a29c1-230">否</span><span class="sxs-lookup"><span data-stu-id="a29c1-230">False</span></span>                             |
| <span data-ttu-id="a29c1-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a29c1-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a29c1-232">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-232">True</span></span>                              |
| <span data-ttu-id="a29c1-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a29c1-233">Is Indexed</span></span>             | <span data-ttu-id="a29c1-234">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-234">True</span></span>                              |
| <span data-ttu-id="a29c1-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a29c1-235">In Global Catalog</span></span>      | <span data-ttu-id="a29c1-236">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-236">True</span></span>                              |
| <span data-ttu-id="a29c1-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a29c1-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a29c1-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a29c1-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a29c1-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a29c1-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a29c1-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a29c1-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a29c1-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-241">Search-Flags</span></span>           | <span data-ttu-id="a29c1-242">0x00000019</span><span class="sxs-lookup"><span data-stu-id="a29c1-242">0x00000019</span></span>                        |
| <span data-ttu-id="a29c1-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-243">System-Flags</span></span>           | <span data-ttu-id="a29c1-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a29c1-244">0x00000012</span></span>                        |
| <span data-ttu-id="a29c1-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a29c1-245">Classes used in</span></span>        | [<span data-ttu-id="a29c1-246">**User**</span><span class="sxs-lookup"><span data-stu-id="a29c1-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a29c1-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a29c1-247">Windows Server 2012</span></span>



| <span data-ttu-id="a29c1-248">進入</span><span class="sxs-lookup"><span data-stu-id="a29c1-248">Entry</span></span> | <span data-ttu-id="a29c1-249">值</span><span class="sxs-lookup"><span data-stu-id="a29c1-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a29c1-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a29c1-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a29c1-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a29c1-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="a29c1-252">System-Only</span></span>            | <span data-ttu-id="a29c1-253">否</span><span class="sxs-lookup"><span data-stu-id="a29c1-253">False</span></span>                             |
| <span data-ttu-id="a29c1-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a29c1-254">Is-Single-Valued</span></span>       | <span data-ttu-id="a29c1-255">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-255">True</span></span>                              |
| <span data-ttu-id="a29c1-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a29c1-256">Is Indexed</span></span>             | <span data-ttu-id="a29c1-257">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-257">True</span></span>                              |
| <span data-ttu-id="a29c1-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a29c1-258">In Global Catalog</span></span>      | <span data-ttu-id="a29c1-259">對</span><span class="sxs-lookup"><span data-stu-id="a29c1-259">True</span></span>                              |
| <span data-ttu-id="a29c1-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a29c1-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="a29c1-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a29c1-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a29c1-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a29c1-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a29c1-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a29c1-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a29c1-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-264">Search-Flags</span></span>           | <span data-ttu-id="a29c1-265">0x00000019</span><span class="sxs-lookup"><span data-stu-id="a29c1-265">0x00000019</span></span>                        |
| <span data-ttu-id="a29c1-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a29c1-266">System-Flags</span></span>           | <span data-ttu-id="a29c1-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a29c1-267">0x00000012</span></span>                        |
| <span data-ttu-id="a29c1-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a29c1-268">Classes used in</span></span>        | [<span data-ttu-id="a29c1-269">**User**</span><span class="sxs-lookup"><span data-stu-id="a29c1-269">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a29c1-270">備註</span><span class="sxs-lookup"><span data-stu-id="a29c1-270">Remarks</span></span>

<span data-ttu-id="a29c1-271">這個屬性值可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="a29c1-271">This attribute value can be zero or a combination of one or more of the following values.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a29c1-272">十六進位值</span><span class="sxs-lookup"><span data-stu-id="a29c1-272">Hexadecimal value</span></span></th>
<th><span data-ttu-id="a29c1-273">Iads 中定義的識別碼 () </span><span class="sxs-lookup"><span data-stu-id="a29c1-273">Identifier (defined in iads.h)</span></span></th>
<th><span data-ttu-id="a29c1-274">Description</span><span class="sxs-lookup"><span data-stu-id="a29c1-274">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a29c1-275">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a29c1-275">0x00000001</span></span></td>
<td><span data-ttu-id="a29c1-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-277">執行登入腳本。</span><span class="sxs-lookup"><span data-stu-id="a29c1-277">The logon script is executed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-278">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a29c1-278">0x00000002</span></span></td>
<td><span data-ttu-id="a29c1-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-280">使用者帳戶已停用。</span><span class="sxs-lookup"><span data-stu-id="a29c1-280">The user account is disabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-281">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a29c1-281">0x00000008</span></span></td>
<td><span data-ttu-id="a29c1-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-283">需要主目錄。</span><span class="sxs-lookup"><span data-stu-id="a29c1-283">The home directory is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a29c1-284">0x00000010</span></span></td>
<td><span data-ttu-id="a29c1-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-286">帳戶目前已鎖定。</span><span class="sxs-lookup"><span data-stu-id="a29c1-286">The account is currently locked out.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-287">0x00000020</span><span class="sxs-lookup"><span data-stu-id="a29c1-287">0x00000020</span></span></td>
<td><span data-ttu-id="a29c1-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-289">不需要密碼。</span><span class="sxs-lookup"><span data-stu-id="a29c1-289">No password is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-290">0x00000040</span><span class="sxs-lookup"><span data-stu-id="a29c1-290">0x00000040</span></span></td>
<td><span data-ttu-id="a29c1-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-292">使用者無法變更密碼。</span><span class="sxs-lookup"><span data-stu-id="a29c1-292">The user cannot change the password.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a29c1-293">您無法直接修改 UserAccountControl 屬性來指派 PASSWD_CANT_CHANGE 的許可權設定。</span><span class="sxs-lookup"><span data-stu-id="a29c1-293">You cannot assign the permission settings of PASSWD_CANT_CHANGE by directly modifying the UserAccountControl attribute.</span></span> <span data-ttu-id="a29c1-294">如需詳細資訊和顯示如何防止使用者變更密碼的程式碼範例，請參閱 <a href="/windows/desktop/ADSI/user-cannot-change-password">使用者無法變更密碼</a>。</span><span class="sxs-lookup"><span data-stu-id="a29c1-294">For more information and a code example that shows how to prevent a user from changing the password, see <a href="/windows/desktop/ADSI/user-cannot-change-password">User Cannot Change Password</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="a29c1-295">:</span><span class="sxs-lookup"><span data-stu-id="a29c1-295">:</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-296">0x00000080</span><span class="sxs-lookup"><span data-stu-id="a29c1-296">0x00000080</span></span></td>
<td><span data-ttu-id="a29c1-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-298">使用者可以傳送加密密碼。</span><span class="sxs-lookup"><span data-stu-id="a29c1-298">The user can send an encrypted password.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-299">0x00000100</span><span class="sxs-lookup"><span data-stu-id="a29c1-299">0x00000100</span></span></td>
<td><span data-ttu-id="a29c1-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-301">這是主要帳戶位於另一個網域的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="a29c1-301">This is an account for users whose primary account is in another domain.</span></span> <span data-ttu-id="a29c1-302">此帳戶可讓使用者存取此網域，但不提供任何信任此網域的網域。</span><span class="sxs-lookup"><span data-stu-id="a29c1-302">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="a29c1-303">也稱為本機使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="a29c1-303">Also known as a local user account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-304">0x00000200</span><span class="sxs-lookup"><span data-stu-id="a29c1-304">0x00000200</span></span></td>
<td><span data-ttu-id="a29c1-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-306">這是代表一般使用者的預設帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="a29c1-306">This is a default account type that represents a typical user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-307">0x00000800</span><span class="sxs-lookup"><span data-stu-id="a29c1-307">0x00000800</span></span></td>
<td><span data-ttu-id="a29c1-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-309">這是允許信任其他網域之系統網域的帳戶。</span><span class="sxs-lookup"><span data-stu-id="a29c1-309">This is a permit to trust account for a system domain that trusts other domains.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-310">0x00001000</span><span class="sxs-lookup"><span data-stu-id="a29c1-310">0x00001000</span></span></td>
<td><span data-ttu-id="a29c1-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-312">這是屬於此網域成員之電腦的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="a29c1-312">This is a computer account for a computer that is a member of this domain.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-313">0x00002000</span><span class="sxs-lookup"><span data-stu-id="a29c1-313">0x00002000</span></span></td>
<td><span data-ttu-id="a29c1-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-315">這是屬於此網域成員之系統備份網域控制站的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="a29c1-315">This is a computer account for a system backup domain controller that is a member of this domain.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-316">0x00004000</span><span class="sxs-lookup"><span data-stu-id="a29c1-316">0x00004000</span></span></td>
<td><span data-ttu-id="a29c1-317">N/A</span><span class="sxs-lookup"><span data-stu-id="a29c1-317">N/A</span></span></td>
<td><span data-ttu-id="a29c1-318">未使用。</span><span class="sxs-lookup"><span data-stu-id="a29c1-318">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-319">0x00008000</span><span class="sxs-lookup"><span data-stu-id="a29c1-319">0x00008000</span></span></td>
<td><span data-ttu-id="a29c1-320">N/A</span><span class="sxs-lookup"><span data-stu-id="a29c1-320">N/A</span></span></td>
<td><span data-ttu-id="a29c1-321">未使用。</span><span class="sxs-lookup"><span data-stu-id="a29c1-321">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-322">0x00010000</span><span class="sxs-lookup"><span data-stu-id="a29c1-322">0x00010000</span></span></td>
<td><span data-ttu-id="a29c1-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-324">此帳戶的密碼永遠不會過期。</span><span class="sxs-lookup"><span data-stu-id="a29c1-324">The password for this account will never expire.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-325">0x00020000</span><span class="sxs-lookup"><span data-stu-id="a29c1-325">0x00020000</span></span></td>
<td><span data-ttu-id="a29c1-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-327">這是 MNS 登入帳戶。</span><span class="sxs-lookup"><span data-stu-id="a29c1-327">This is an MNS logon account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-328">0x00040000</span><span class="sxs-lookup"><span data-stu-id="a29c1-328">0x00040000</span></span></td>
<td><span data-ttu-id="a29c1-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-330">使用者必須使用智慧卡登入。</span><span class="sxs-lookup"><span data-stu-id="a29c1-330">The user must log on using a smart card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-331">0x00080000</span><span class="sxs-lookup"><span data-stu-id="a29c1-331">0x00080000</span></span></td>
<td><span data-ttu-id="a29c1-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-333">服務帳戶 (用來執行服務的使用者或電腦帳戶) ，受 Kerberos 委派的信任。</span><span class="sxs-lookup"><span data-stu-id="a29c1-333">The service account (user or computer account), under which a service runs, is trusted for Kerberos delegation.</span></span> <span data-ttu-id="a29c1-334">任何這類服務都可以模擬要求服務的用戶端。</span><span class="sxs-lookup"><span data-stu-id="a29c1-334">Any such service can impersonate a client requesting the service.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-335">0x00100000</span><span class="sxs-lookup"><span data-stu-id="a29c1-335">0x00100000</span></span></td>
<td><span data-ttu-id="a29c1-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-337">即使服務帳戶設定為受信任的 Kerberos 委派，也不會將使用者的安全性內容委派給服務。</span><span class="sxs-lookup"><span data-stu-id="a29c1-337">The security context of the user will not be delegated to a service even if the service account is set as trusted for Kerberos delegation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-338">0x00200000</span><span class="sxs-lookup"><span data-stu-id="a29c1-338">0x00200000</span></span></td>
<td><span data-ttu-id="a29c1-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-340">限制此主體僅使用資料加密標準 (DES) 金鑰加密類型。</span><span class="sxs-lookup"><span data-stu-id="a29c1-340">Restrict this principal to use only Data Encryption Standard (DES) encryption types for keys.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-341">0x00400000</span><span class="sxs-lookup"><span data-stu-id="a29c1-341">0x00400000</span></span></td>
<td><span data-ttu-id="a29c1-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-343">此帳戶不需要 Kerberos 預先驗證即可登入。</span><span class="sxs-lookup"><span data-stu-id="a29c1-343">This account does not require Kerberos pre-authentication for logon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a29c1-344">0x00800000</span><span class="sxs-lookup"><span data-stu-id="a29c1-344">0x00800000</span></span></td>
<td><span data-ttu-id="a29c1-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-346">使用者密碼已過期。</span><span class="sxs-lookup"><span data-stu-id="a29c1-346">The user password has expired.</span></span> <span data-ttu-id="a29c1-347">此旗標是由系統使用來自 <a href="a-pwdlastset.md"><strong>Pwd 的 Last 設定</strong></a> 屬性和網域原則的資料所建立。</span><span class="sxs-lookup"><span data-stu-id="a29c1-347">This flag is created by the system using data from the <a href="a-pwdlastset.md"><strong>Pwd-Last-Set</strong></a> attribute and the domain policy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a29c1-348">0x01000000</span><span class="sxs-lookup"><span data-stu-id="a29c1-348">0x01000000</span></span></td>
<td><span data-ttu-id="a29c1-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29c1-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="a29c1-350">帳戶已啟用委派。</span><span class="sxs-lookup"><span data-stu-id="a29c1-350">The account is enabled for delegation.</span></span> <span data-ttu-id="a29c1-351">這是安全性相關設定;啟用此選項的帳戶應受到嚴格的控制。</span><span class="sxs-lookup"><span data-stu-id="a29c1-351">This is a security-sensitive setting; accounts with this option enabled should be strictly controlled.</span></span> <span data-ttu-id="a29c1-352">此設定可讓在此帳戶下執行的服務採用用戶端身分識別，並以該使用者身分向網路上的其他遠端伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="a29c1-352">This setting enables a service running under the account to assume a client identity and authenticate as that user to other remote servers on the network.</span></span></td>
</tr>
</tbody>
</table>



 


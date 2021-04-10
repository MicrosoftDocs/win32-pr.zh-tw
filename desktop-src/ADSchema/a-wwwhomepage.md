---
title: WWW-首頁屬性
description: 網站主要登陸頁面的網頁。
ms.assetid: 5dbc571d-3032-4eee-ab2d-9f6f0273a472
ms.tgt_platform: multiple
keywords:
- WWW-首頁屬性 AD 架構
- wWWHomePage 屬性 AD 架構
topic_type:
- apiref
api_name:
- WWW-Home-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 360240cebe5c8d02054307718de0bcaee47cec4e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935466"
---
# <a name="www-home-page-attribute"></a><span data-ttu-id="f774c-105">WWW-首頁屬性</span><span class="sxs-lookup"><span data-stu-id="f774c-105">WWW-Home-Page attribute</span></span>

<span data-ttu-id="f774c-106">網站主要登陸頁面的網頁。</span><span class="sxs-lookup"><span data-stu-id="f774c-106">A web page that is the primary landing page of a website.</span></span>



| <span data-ttu-id="f774c-107">進入</span><span class="sxs-lookup"><span data-stu-id="f774c-107">Entry</span></span> | <span data-ttu-id="f774c-108">值</span><span class="sxs-lookup"><span data-stu-id="f774c-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="f774c-109">CN</span><span class="sxs-lookup"><span data-stu-id="f774c-109">CN</span></span>                | <span data-ttu-id="f774c-110">WWW-首頁</span><span class="sxs-lookup"><span data-stu-id="f774c-110">WWW-Home-Page</span></span>                                                               |
| <span data-ttu-id="f774c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f774c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f774c-112">wWWHomePage</span><span class="sxs-lookup"><span data-stu-id="f774c-112">wWWHomePage</span></span>                                                                 |
| <span data-ttu-id="f774c-113">大小</span><span class="sxs-lookup"><span data-stu-id="f774c-113">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="f774c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f774c-114">Update Privilege</span></span>  | <span data-ttu-id="f774c-115">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="f774c-115">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="f774c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f774c-116">Update Frequency</span></span>  | <span data-ttu-id="f774c-117">當使用者的記錄建立時，以及每當網頁需要變更時。</span><span class="sxs-lookup"><span data-stu-id="f774c-117">When the user's record is created and whenever the webpage needs to change.</span></span> |
| <span data-ttu-id="f774c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f774c-118">Attribute-Id</span></span>      | <span data-ttu-id="f774c-119">1.2.840.113556.1.2.464</span><span class="sxs-lookup"><span data-stu-id="f774c-119">1.2.840.113556.1.2.464</span></span>                                                      |
| <span data-ttu-id="f774c-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f774c-120">System-Id-Guid</span></span>    | <span data-ttu-id="f774c-121">bf967a7a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f774c-121">bf967a7a-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="f774c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f774c-122">Syntax</span></span>            | [<span data-ttu-id="f774c-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f774c-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="f774c-124">實作</span><span class="sxs-lookup"><span data-stu-id="f774c-124">Implementations</span></span>

-   [<span data-ttu-id="f774c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f774c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f774c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f774c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f774c-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f774c-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f774c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f774c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f774c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f774c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f774c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f774c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f774c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f774c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f774c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f774c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f774c-133">進入</span><span class="sxs-lookup"><span data-stu-id="f774c-133">Entry</span></span> | <span data-ttu-id="f774c-134">值</span><span class="sxs-lookup"><span data-stu-id="f774c-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f774c-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f774c-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f774c-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f774c-137">System-Only</span></span>            | <span data-ttu-id="f774c-138">否</span><span class="sxs-lookup"><span data-stu-id="f774c-138">False</span></span>                           |
| <span data-ttu-id="f774c-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f774c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f774c-140">對</span><span class="sxs-lookup"><span data-stu-id="f774c-140">True</span></span>                            |
| <span data-ttu-id="f774c-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f774c-141">Is Indexed</span></span>             | <span data-ttu-id="f774c-142">否</span><span class="sxs-lookup"><span data-stu-id="f774c-142">False</span></span>                           |
| <span data-ttu-id="f774c-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f774c-143">In Global Catalog</span></span>      | <span data-ttu-id="f774c-144">否</span><span class="sxs-lookup"><span data-stu-id="f774c-144">False</span></span>                           |
| <span data-ttu-id="f774c-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f774c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f774c-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f774c-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f774c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f774c-147">Range-Lower</span></span>            | <span data-ttu-id="f774c-148">1</span><span class="sxs-lookup"><span data-stu-id="f774c-148">1</span></span>                               |
| <span data-ttu-id="f774c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f774c-149">Range-Upper</span></span>            | <span data-ttu-id="f774c-150">2048</span><span class="sxs-lookup"><span data-stu-id="f774c-150">2048</span></span>                            |
| <span data-ttu-id="f774c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-151">Search-Flags</span></span>           | <span data-ttu-id="f774c-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f774c-152">0x00000000</span></span>                      |
| <span data-ttu-id="f774c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-153">System-Flags</span></span>           | <span data-ttu-id="f774c-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f774c-154">0x00000010</span></span>                      |
| <span data-ttu-id="f774c-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f774c-155">Classes used in</span></span>        | [<span data-ttu-id="f774c-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f774c-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f774c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f774c-157">Windows Server 2003</span></span>



| <span data-ttu-id="f774c-158">進入</span><span class="sxs-lookup"><span data-stu-id="f774c-158">Entry</span></span> | <span data-ttu-id="f774c-159">值</span><span class="sxs-lookup"><span data-stu-id="f774c-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f774c-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f774c-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f774c-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f774c-162">System-Only</span></span>            | <span data-ttu-id="f774c-163">否</span><span class="sxs-lookup"><span data-stu-id="f774c-163">False</span></span>                           |
| <span data-ttu-id="f774c-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f774c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f774c-165">對</span><span class="sxs-lookup"><span data-stu-id="f774c-165">True</span></span>                            |
| <span data-ttu-id="f774c-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f774c-166">Is Indexed</span></span>             | <span data-ttu-id="f774c-167">否</span><span class="sxs-lookup"><span data-stu-id="f774c-167">False</span></span>                           |
| <span data-ttu-id="f774c-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f774c-168">In Global Catalog</span></span>      | <span data-ttu-id="f774c-169">否</span><span class="sxs-lookup"><span data-stu-id="f774c-169">False</span></span>                           |
| <span data-ttu-id="f774c-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f774c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f774c-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f774c-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f774c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f774c-172">Range-Lower</span></span>            | <span data-ttu-id="f774c-173">1</span><span class="sxs-lookup"><span data-stu-id="f774c-173">1</span></span>                               |
| <span data-ttu-id="f774c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f774c-174">Range-Upper</span></span>            | <span data-ttu-id="f774c-175">2048</span><span class="sxs-lookup"><span data-stu-id="f774c-175">2048</span></span>                            |
| <span data-ttu-id="f774c-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-176">Search-Flags</span></span>           | <span data-ttu-id="f774c-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f774c-177">0x00000000</span></span>                      |
| <span data-ttu-id="f774c-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-178">System-Flags</span></span>           | <span data-ttu-id="f774c-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f774c-179">0x00000010</span></span>                      |
| <span data-ttu-id="f774c-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f774c-180">Classes used in</span></span>        | [<span data-ttu-id="f774c-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f774c-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f774c-182">亞當</span><span class="sxs-lookup"><span data-stu-id="f774c-182">ADAM</span></span>



| <span data-ttu-id="f774c-183">進入</span><span class="sxs-lookup"><span data-stu-id="f774c-183">Entry</span></span> | <span data-ttu-id="f774c-184">值</span><span class="sxs-lookup"><span data-stu-id="f774c-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f774c-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f774c-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f774c-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="f774c-187">System-Only</span></span>            | <span data-ttu-id="f774c-188">否</span><span class="sxs-lookup"><span data-stu-id="f774c-188">False</span></span>                           |
| <span data-ttu-id="f774c-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f774c-189">Is-Single-Valued</span></span>       | <span data-ttu-id="f774c-190">對</span><span class="sxs-lookup"><span data-stu-id="f774c-190">True</span></span>                            |
| <span data-ttu-id="f774c-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f774c-191">Is Indexed</span></span>             | <span data-ttu-id="f774c-192">否</span><span class="sxs-lookup"><span data-stu-id="f774c-192">False</span></span>                           |
| <span data-ttu-id="f774c-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f774c-193">In Global Catalog</span></span>      | <span data-ttu-id="f774c-194">否</span><span class="sxs-lookup"><span data-stu-id="f774c-194">False</span></span>                           |
| <span data-ttu-id="f774c-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f774c-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="f774c-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f774c-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f774c-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f774c-197">Range-Lower</span></span>            | <span data-ttu-id="f774c-198">1</span><span class="sxs-lookup"><span data-stu-id="f774c-198">1</span></span>                               |
| <span data-ttu-id="f774c-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f774c-199">Range-Upper</span></span>            | <span data-ttu-id="f774c-200">2048</span><span class="sxs-lookup"><span data-stu-id="f774c-200">2048</span></span>                            |
| <span data-ttu-id="f774c-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-201">Search-Flags</span></span>           | <span data-ttu-id="f774c-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f774c-202">0x00000000</span></span>                      |
| <span data-ttu-id="f774c-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-203">System-Flags</span></span>           | <span data-ttu-id="f774c-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f774c-204">0x00000010</span></span>                      |
| <span data-ttu-id="f774c-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f774c-205">Classes used in</span></span>        | [<span data-ttu-id="f774c-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f774c-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f774c-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f774c-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f774c-208">進入</span><span class="sxs-lookup"><span data-stu-id="f774c-208">Entry</span></span> | <span data-ttu-id="f774c-209">值</span><span class="sxs-lookup"><span data-stu-id="f774c-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f774c-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f774c-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f774c-211">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="f774c-212">System-Only</span></span>            | <span data-ttu-id="f774c-213">否</span><span class="sxs-lookup"><span data-stu-id="f774c-213">False</span></span>                           |
| <span data-ttu-id="f774c-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f774c-214">Is-Single-Valued</span></span>       | <span data-ttu-id="f774c-215">對</span><span class="sxs-lookup"><span data-stu-id="f774c-215">True</span></span>                            |
| <span data-ttu-id="f774c-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f774c-216">Is Indexed</span></span>             | <span data-ttu-id="f774c-217">否</span><span class="sxs-lookup"><span data-stu-id="f774c-217">False</span></span>                           |
| <span data-ttu-id="f774c-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f774c-218">In Global Catalog</span></span>      | <span data-ttu-id="f774c-219">否</span><span class="sxs-lookup"><span data-stu-id="f774c-219">False</span></span>                           |
| <span data-ttu-id="f774c-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f774c-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="f774c-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f774c-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f774c-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f774c-222">Range-Lower</span></span>            | <span data-ttu-id="f774c-223">1</span><span class="sxs-lookup"><span data-stu-id="f774c-223">1</span></span>                               |
| <span data-ttu-id="f774c-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f774c-224">Range-Upper</span></span>            | <span data-ttu-id="f774c-225">2048</span><span class="sxs-lookup"><span data-stu-id="f774c-225">2048</span></span>                            |
| <span data-ttu-id="f774c-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-226">Search-Flags</span></span>           | <span data-ttu-id="f774c-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f774c-227">0x00000000</span></span>                      |
| <span data-ttu-id="f774c-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-228">System-Flags</span></span>           | <span data-ttu-id="f774c-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f774c-229">0x00000010</span></span>                      |
| <span data-ttu-id="f774c-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f774c-230">Classes used in</span></span>        | [<span data-ttu-id="f774c-231">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f774c-231">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f774c-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f774c-232">Windows Server 2008</span></span>



| <span data-ttu-id="f774c-233">進入</span><span class="sxs-lookup"><span data-stu-id="f774c-233">Entry</span></span> | <span data-ttu-id="f774c-234">值</span><span class="sxs-lookup"><span data-stu-id="f774c-234">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f774c-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f774c-235">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f774c-236">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="f774c-237">System-Only</span></span>            | <span data-ttu-id="f774c-238">否</span><span class="sxs-lookup"><span data-stu-id="f774c-238">False</span></span>                           |
| <span data-ttu-id="f774c-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f774c-239">Is-Single-Valued</span></span>       | <span data-ttu-id="f774c-240">對</span><span class="sxs-lookup"><span data-stu-id="f774c-240">True</span></span>                            |
| <span data-ttu-id="f774c-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f774c-241">Is Indexed</span></span>             | <span data-ttu-id="f774c-242">否</span><span class="sxs-lookup"><span data-stu-id="f774c-242">False</span></span>                           |
| <span data-ttu-id="f774c-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f774c-243">In Global Catalog</span></span>      | <span data-ttu-id="f774c-244">否</span><span class="sxs-lookup"><span data-stu-id="f774c-244">False</span></span>                           |
| <span data-ttu-id="f774c-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f774c-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="f774c-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f774c-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f774c-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f774c-247">Range-Lower</span></span>            | <span data-ttu-id="f774c-248">1</span><span class="sxs-lookup"><span data-stu-id="f774c-248">1</span></span>                               |
| <span data-ttu-id="f774c-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f774c-249">Range-Upper</span></span>            | <span data-ttu-id="f774c-250">2048</span><span class="sxs-lookup"><span data-stu-id="f774c-250">2048</span></span>                            |
| <span data-ttu-id="f774c-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-251">Search-Flags</span></span>           | <span data-ttu-id="f774c-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f774c-252">0x00000000</span></span>                      |
| <span data-ttu-id="f774c-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-253">System-Flags</span></span>           | <span data-ttu-id="f774c-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f774c-254">0x00000010</span></span>                      |
| <span data-ttu-id="f774c-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f774c-255">Classes used in</span></span>        | [<span data-ttu-id="f774c-256">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f774c-256">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f774c-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f774c-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f774c-258">進入</span><span class="sxs-lookup"><span data-stu-id="f774c-258">Entry</span></span> | <span data-ttu-id="f774c-259">值</span><span class="sxs-lookup"><span data-stu-id="f774c-259">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f774c-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f774c-260">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f774c-261">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="f774c-262">System-Only</span></span>            | <span data-ttu-id="f774c-263">否</span><span class="sxs-lookup"><span data-stu-id="f774c-263">False</span></span>                           |
| <span data-ttu-id="f774c-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f774c-264">Is-Single-Valued</span></span>       | <span data-ttu-id="f774c-265">對</span><span class="sxs-lookup"><span data-stu-id="f774c-265">True</span></span>                            |
| <span data-ttu-id="f774c-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f774c-266">Is Indexed</span></span>             | <span data-ttu-id="f774c-267">否</span><span class="sxs-lookup"><span data-stu-id="f774c-267">False</span></span>                           |
| <span data-ttu-id="f774c-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f774c-268">In Global Catalog</span></span>      | <span data-ttu-id="f774c-269">否</span><span class="sxs-lookup"><span data-stu-id="f774c-269">False</span></span>                           |
| <span data-ttu-id="f774c-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f774c-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="f774c-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f774c-271">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f774c-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f774c-272">Range-Lower</span></span>            | <span data-ttu-id="f774c-273">1</span><span class="sxs-lookup"><span data-stu-id="f774c-273">1</span></span>                               |
| <span data-ttu-id="f774c-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f774c-274">Range-Upper</span></span>            | <span data-ttu-id="f774c-275">2048</span><span class="sxs-lookup"><span data-stu-id="f774c-275">2048</span></span>                            |
| <span data-ttu-id="f774c-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-276">Search-Flags</span></span>           | <span data-ttu-id="f774c-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f774c-277">0x00000000</span></span>                      |
| <span data-ttu-id="f774c-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-278">System-Flags</span></span>           | <span data-ttu-id="f774c-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f774c-279">0x00000010</span></span>                      |
| <span data-ttu-id="f774c-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f774c-280">Classes used in</span></span>        | [<span data-ttu-id="f774c-281">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f774c-281">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f774c-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f774c-282">Windows Server 2012</span></span>



| <span data-ttu-id="f774c-283">進入</span><span class="sxs-lookup"><span data-stu-id="f774c-283">Entry</span></span> | <span data-ttu-id="f774c-284">值</span><span class="sxs-lookup"><span data-stu-id="f774c-284">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f774c-285">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f774c-285">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f774c-286">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f774c-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="f774c-287">System-Only</span></span>            | <span data-ttu-id="f774c-288">否</span><span class="sxs-lookup"><span data-stu-id="f774c-288">False</span></span>                           |
| <span data-ttu-id="f774c-289">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f774c-289">Is-Single-Valued</span></span>       | <span data-ttu-id="f774c-290">對</span><span class="sxs-lookup"><span data-stu-id="f774c-290">True</span></span>                            |
| <span data-ttu-id="f774c-291">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f774c-291">Is Indexed</span></span>             | <span data-ttu-id="f774c-292">否</span><span class="sxs-lookup"><span data-stu-id="f774c-292">False</span></span>                           |
| <span data-ttu-id="f774c-293">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f774c-293">In Global Catalog</span></span>      | <span data-ttu-id="f774c-294">否</span><span class="sxs-lookup"><span data-stu-id="f774c-294">False</span></span>                           |
| <span data-ttu-id="f774c-295">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f774c-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="f774c-296">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f774c-296">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f774c-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f774c-297">Range-Lower</span></span>            | <span data-ttu-id="f774c-298">1</span><span class="sxs-lookup"><span data-stu-id="f774c-298">1</span></span>                               |
| <span data-ttu-id="f774c-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f774c-299">Range-Upper</span></span>            | <span data-ttu-id="f774c-300">2048</span><span class="sxs-lookup"><span data-stu-id="f774c-300">2048</span></span>                            |
| <span data-ttu-id="f774c-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-301">Search-Flags</span></span>           | <span data-ttu-id="f774c-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f774c-302">0x00000000</span></span>                      |
| <span data-ttu-id="f774c-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f774c-303">System-Flags</span></span>           | <span data-ttu-id="f774c-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f774c-304">0x00000010</span></span>                      |
| <span data-ttu-id="f774c-305">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f774c-305">Classes used in</span></span>        | [<span data-ttu-id="f774c-306">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f774c-306">**Top**</span></span>](c-top.md)<br/> |



 

 






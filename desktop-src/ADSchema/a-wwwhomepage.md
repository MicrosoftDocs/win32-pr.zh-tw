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
# <a name="www-home-page-attribute"></a><span data-ttu-id="642a6-105">WWW-首頁屬性</span><span class="sxs-lookup"><span data-stu-id="642a6-105">WWW-Home-Page attribute</span></span>

<span data-ttu-id="642a6-106">網站主要登陸頁面的網頁。</span><span class="sxs-lookup"><span data-stu-id="642a6-106">A web page that is the primary landing page of a website.</span></span>



| <span data-ttu-id="642a6-107">進入</span><span class="sxs-lookup"><span data-stu-id="642a6-107">Entry</span></span> | <span data-ttu-id="642a6-108">值</span><span class="sxs-lookup"><span data-stu-id="642a6-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="642a6-109">CN</span><span class="sxs-lookup"><span data-stu-id="642a6-109">CN</span></span>                | <span data-ttu-id="642a6-110">WWW-首頁</span><span class="sxs-lookup"><span data-stu-id="642a6-110">WWW-Home-Page</span></span>                                                               |
| <span data-ttu-id="642a6-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="642a6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="642a6-112">wWWHomePage</span><span class="sxs-lookup"><span data-stu-id="642a6-112">wWWHomePage</span></span>                                                                 |
| <span data-ttu-id="642a6-113">大小</span><span class="sxs-lookup"><span data-stu-id="642a6-113">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="642a6-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="642a6-114">Update Privilege</span></span>  | <span data-ttu-id="642a6-115">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="642a6-115">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="642a6-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="642a6-116">Update Frequency</span></span>  | <span data-ttu-id="642a6-117">當使用者的記錄建立時，以及每當網頁需要變更時。</span><span class="sxs-lookup"><span data-stu-id="642a6-117">When the user's record is created and whenever the webpage needs to change.</span></span> |
| <span data-ttu-id="642a6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="642a6-118">Attribute-Id</span></span>      | <span data-ttu-id="642a6-119">1.2.840.113556.1.2.464</span><span class="sxs-lookup"><span data-stu-id="642a6-119">1.2.840.113556.1.2.464</span></span>                                                      |
| <span data-ttu-id="642a6-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="642a6-120">System-Id-Guid</span></span>    | <span data-ttu-id="642a6-121">bf967a7a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="642a6-121">bf967a7a-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="642a6-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="642a6-122">Syntax</span></span>            | [<span data-ttu-id="642a6-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="642a6-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="642a6-124">實作</span><span class="sxs-lookup"><span data-stu-id="642a6-124">Implementations</span></span>

-   [<span data-ttu-id="642a6-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="642a6-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="642a6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="642a6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="642a6-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="642a6-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="642a6-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="642a6-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="642a6-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="642a6-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="642a6-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="642a6-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="642a6-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="642a6-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="642a6-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="642a6-132">Windows 2000 Server</span></span>



| <span data-ttu-id="642a6-133">進入</span><span class="sxs-lookup"><span data-stu-id="642a6-133">Entry</span></span> | <span data-ttu-id="642a6-134">值</span><span class="sxs-lookup"><span data-stu-id="642a6-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="642a6-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="642a6-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="642a6-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="642a6-137">System-Only</span></span>            | <span data-ttu-id="642a6-138">否</span><span class="sxs-lookup"><span data-stu-id="642a6-138">False</span></span>                           |
| <span data-ttu-id="642a6-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="642a6-139">Is-Single-Valued</span></span>       | <span data-ttu-id="642a6-140">對</span><span class="sxs-lookup"><span data-stu-id="642a6-140">True</span></span>                            |
| <span data-ttu-id="642a6-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="642a6-141">Is Indexed</span></span>             | <span data-ttu-id="642a6-142">否</span><span class="sxs-lookup"><span data-stu-id="642a6-142">False</span></span>                           |
| <span data-ttu-id="642a6-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="642a6-143">In Global Catalog</span></span>      | <span data-ttu-id="642a6-144">否</span><span class="sxs-lookup"><span data-stu-id="642a6-144">False</span></span>                           |
| <span data-ttu-id="642a6-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="642a6-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="642a6-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="642a6-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="642a6-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="642a6-147">Range-Lower</span></span>            | <span data-ttu-id="642a6-148">1</span><span class="sxs-lookup"><span data-stu-id="642a6-148">1</span></span>                               |
| <span data-ttu-id="642a6-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="642a6-149">Range-Upper</span></span>            | <span data-ttu-id="642a6-150">2048</span><span class="sxs-lookup"><span data-stu-id="642a6-150">2048</span></span>                            |
| <span data-ttu-id="642a6-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-151">Search-Flags</span></span>           | <span data-ttu-id="642a6-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="642a6-152">0x00000000</span></span>                      |
| <span data-ttu-id="642a6-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-153">System-Flags</span></span>           | <span data-ttu-id="642a6-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="642a6-154">0x00000010</span></span>                      |
| <span data-ttu-id="642a6-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="642a6-155">Classes used in</span></span>        | [<span data-ttu-id="642a6-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="642a6-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="642a6-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="642a6-157">Windows Server 2003</span></span>



| <span data-ttu-id="642a6-158">進入</span><span class="sxs-lookup"><span data-stu-id="642a6-158">Entry</span></span> | <span data-ttu-id="642a6-159">值</span><span class="sxs-lookup"><span data-stu-id="642a6-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="642a6-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="642a6-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="642a6-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="642a6-162">System-Only</span></span>            | <span data-ttu-id="642a6-163">否</span><span class="sxs-lookup"><span data-stu-id="642a6-163">False</span></span>                           |
| <span data-ttu-id="642a6-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="642a6-164">Is-Single-Valued</span></span>       | <span data-ttu-id="642a6-165">對</span><span class="sxs-lookup"><span data-stu-id="642a6-165">True</span></span>                            |
| <span data-ttu-id="642a6-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="642a6-166">Is Indexed</span></span>             | <span data-ttu-id="642a6-167">否</span><span class="sxs-lookup"><span data-stu-id="642a6-167">False</span></span>                           |
| <span data-ttu-id="642a6-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="642a6-168">In Global Catalog</span></span>      | <span data-ttu-id="642a6-169">否</span><span class="sxs-lookup"><span data-stu-id="642a6-169">False</span></span>                           |
| <span data-ttu-id="642a6-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="642a6-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="642a6-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="642a6-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="642a6-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="642a6-172">Range-Lower</span></span>            | <span data-ttu-id="642a6-173">1</span><span class="sxs-lookup"><span data-stu-id="642a6-173">1</span></span>                               |
| <span data-ttu-id="642a6-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="642a6-174">Range-Upper</span></span>            | <span data-ttu-id="642a6-175">2048</span><span class="sxs-lookup"><span data-stu-id="642a6-175">2048</span></span>                            |
| <span data-ttu-id="642a6-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-176">Search-Flags</span></span>           | <span data-ttu-id="642a6-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="642a6-177">0x00000000</span></span>                      |
| <span data-ttu-id="642a6-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-178">System-Flags</span></span>           | <span data-ttu-id="642a6-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="642a6-179">0x00000010</span></span>                      |
| <span data-ttu-id="642a6-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="642a6-180">Classes used in</span></span>        | [<span data-ttu-id="642a6-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="642a6-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="642a6-182">亞當</span><span class="sxs-lookup"><span data-stu-id="642a6-182">ADAM</span></span>



| <span data-ttu-id="642a6-183">進入</span><span class="sxs-lookup"><span data-stu-id="642a6-183">Entry</span></span> | <span data-ttu-id="642a6-184">值</span><span class="sxs-lookup"><span data-stu-id="642a6-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="642a6-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="642a6-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="642a6-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="642a6-187">System-Only</span></span>            | <span data-ttu-id="642a6-188">否</span><span class="sxs-lookup"><span data-stu-id="642a6-188">False</span></span>                           |
| <span data-ttu-id="642a6-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="642a6-189">Is-Single-Valued</span></span>       | <span data-ttu-id="642a6-190">對</span><span class="sxs-lookup"><span data-stu-id="642a6-190">True</span></span>                            |
| <span data-ttu-id="642a6-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="642a6-191">Is Indexed</span></span>             | <span data-ttu-id="642a6-192">否</span><span class="sxs-lookup"><span data-stu-id="642a6-192">False</span></span>                           |
| <span data-ttu-id="642a6-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="642a6-193">In Global Catalog</span></span>      | <span data-ttu-id="642a6-194">否</span><span class="sxs-lookup"><span data-stu-id="642a6-194">False</span></span>                           |
| <span data-ttu-id="642a6-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="642a6-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="642a6-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="642a6-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="642a6-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="642a6-197">Range-Lower</span></span>            | <span data-ttu-id="642a6-198">1</span><span class="sxs-lookup"><span data-stu-id="642a6-198">1</span></span>                               |
| <span data-ttu-id="642a6-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="642a6-199">Range-Upper</span></span>            | <span data-ttu-id="642a6-200">2048</span><span class="sxs-lookup"><span data-stu-id="642a6-200">2048</span></span>                            |
| <span data-ttu-id="642a6-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-201">Search-Flags</span></span>           | <span data-ttu-id="642a6-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="642a6-202">0x00000000</span></span>                      |
| <span data-ttu-id="642a6-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-203">System-Flags</span></span>           | <span data-ttu-id="642a6-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="642a6-204">0x00000010</span></span>                      |
| <span data-ttu-id="642a6-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="642a6-205">Classes used in</span></span>        | [<span data-ttu-id="642a6-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="642a6-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="642a6-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="642a6-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="642a6-208">進入</span><span class="sxs-lookup"><span data-stu-id="642a6-208">Entry</span></span> | <span data-ttu-id="642a6-209">值</span><span class="sxs-lookup"><span data-stu-id="642a6-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="642a6-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="642a6-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="642a6-211">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="642a6-212">System-Only</span></span>            | <span data-ttu-id="642a6-213">否</span><span class="sxs-lookup"><span data-stu-id="642a6-213">False</span></span>                           |
| <span data-ttu-id="642a6-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="642a6-214">Is-Single-Valued</span></span>       | <span data-ttu-id="642a6-215">對</span><span class="sxs-lookup"><span data-stu-id="642a6-215">True</span></span>                            |
| <span data-ttu-id="642a6-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="642a6-216">Is Indexed</span></span>             | <span data-ttu-id="642a6-217">否</span><span class="sxs-lookup"><span data-stu-id="642a6-217">False</span></span>                           |
| <span data-ttu-id="642a6-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="642a6-218">In Global Catalog</span></span>      | <span data-ttu-id="642a6-219">否</span><span class="sxs-lookup"><span data-stu-id="642a6-219">False</span></span>                           |
| <span data-ttu-id="642a6-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="642a6-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="642a6-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="642a6-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="642a6-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="642a6-222">Range-Lower</span></span>            | <span data-ttu-id="642a6-223">1</span><span class="sxs-lookup"><span data-stu-id="642a6-223">1</span></span>                               |
| <span data-ttu-id="642a6-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="642a6-224">Range-Upper</span></span>            | <span data-ttu-id="642a6-225">2048</span><span class="sxs-lookup"><span data-stu-id="642a6-225">2048</span></span>                            |
| <span data-ttu-id="642a6-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-226">Search-Flags</span></span>           | <span data-ttu-id="642a6-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="642a6-227">0x00000000</span></span>                      |
| <span data-ttu-id="642a6-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-228">System-Flags</span></span>           | <span data-ttu-id="642a6-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="642a6-229">0x00000010</span></span>                      |
| <span data-ttu-id="642a6-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="642a6-230">Classes used in</span></span>        | [<span data-ttu-id="642a6-231">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="642a6-231">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="642a6-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="642a6-232">Windows Server 2008</span></span>



| <span data-ttu-id="642a6-233">進入</span><span class="sxs-lookup"><span data-stu-id="642a6-233">Entry</span></span> | <span data-ttu-id="642a6-234">值</span><span class="sxs-lookup"><span data-stu-id="642a6-234">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="642a6-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="642a6-235">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="642a6-236">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="642a6-237">System-Only</span></span>            | <span data-ttu-id="642a6-238">否</span><span class="sxs-lookup"><span data-stu-id="642a6-238">False</span></span>                           |
| <span data-ttu-id="642a6-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="642a6-239">Is-Single-Valued</span></span>       | <span data-ttu-id="642a6-240">對</span><span class="sxs-lookup"><span data-stu-id="642a6-240">True</span></span>                            |
| <span data-ttu-id="642a6-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="642a6-241">Is Indexed</span></span>             | <span data-ttu-id="642a6-242">否</span><span class="sxs-lookup"><span data-stu-id="642a6-242">False</span></span>                           |
| <span data-ttu-id="642a6-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="642a6-243">In Global Catalog</span></span>      | <span data-ttu-id="642a6-244">否</span><span class="sxs-lookup"><span data-stu-id="642a6-244">False</span></span>                           |
| <span data-ttu-id="642a6-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="642a6-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="642a6-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="642a6-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="642a6-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="642a6-247">Range-Lower</span></span>            | <span data-ttu-id="642a6-248">1</span><span class="sxs-lookup"><span data-stu-id="642a6-248">1</span></span>                               |
| <span data-ttu-id="642a6-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="642a6-249">Range-Upper</span></span>            | <span data-ttu-id="642a6-250">2048</span><span class="sxs-lookup"><span data-stu-id="642a6-250">2048</span></span>                            |
| <span data-ttu-id="642a6-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-251">Search-Flags</span></span>           | <span data-ttu-id="642a6-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="642a6-252">0x00000000</span></span>                      |
| <span data-ttu-id="642a6-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-253">System-Flags</span></span>           | <span data-ttu-id="642a6-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="642a6-254">0x00000010</span></span>                      |
| <span data-ttu-id="642a6-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="642a6-255">Classes used in</span></span>        | [<span data-ttu-id="642a6-256">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="642a6-256">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="642a6-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="642a6-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="642a6-258">進入</span><span class="sxs-lookup"><span data-stu-id="642a6-258">Entry</span></span> | <span data-ttu-id="642a6-259">值</span><span class="sxs-lookup"><span data-stu-id="642a6-259">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="642a6-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="642a6-260">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="642a6-261">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="642a6-262">System-Only</span></span>            | <span data-ttu-id="642a6-263">否</span><span class="sxs-lookup"><span data-stu-id="642a6-263">False</span></span>                           |
| <span data-ttu-id="642a6-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="642a6-264">Is-Single-Valued</span></span>       | <span data-ttu-id="642a6-265">對</span><span class="sxs-lookup"><span data-stu-id="642a6-265">True</span></span>                            |
| <span data-ttu-id="642a6-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="642a6-266">Is Indexed</span></span>             | <span data-ttu-id="642a6-267">否</span><span class="sxs-lookup"><span data-stu-id="642a6-267">False</span></span>                           |
| <span data-ttu-id="642a6-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="642a6-268">In Global Catalog</span></span>      | <span data-ttu-id="642a6-269">否</span><span class="sxs-lookup"><span data-stu-id="642a6-269">False</span></span>                           |
| <span data-ttu-id="642a6-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="642a6-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="642a6-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="642a6-271">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="642a6-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="642a6-272">Range-Lower</span></span>            | <span data-ttu-id="642a6-273">1</span><span class="sxs-lookup"><span data-stu-id="642a6-273">1</span></span>                               |
| <span data-ttu-id="642a6-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="642a6-274">Range-Upper</span></span>            | <span data-ttu-id="642a6-275">2048</span><span class="sxs-lookup"><span data-stu-id="642a6-275">2048</span></span>                            |
| <span data-ttu-id="642a6-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-276">Search-Flags</span></span>           | <span data-ttu-id="642a6-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="642a6-277">0x00000000</span></span>                      |
| <span data-ttu-id="642a6-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-278">System-Flags</span></span>           | <span data-ttu-id="642a6-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="642a6-279">0x00000010</span></span>                      |
| <span data-ttu-id="642a6-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="642a6-280">Classes used in</span></span>        | [<span data-ttu-id="642a6-281">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="642a6-281">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="642a6-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="642a6-282">Windows Server 2012</span></span>



| <span data-ttu-id="642a6-283">進入</span><span class="sxs-lookup"><span data-stu-id="642a6-283">Entry</span></span> | <span data-ttu-id="642a6-284">值</span><span class="sxs-lookup"><span data-stu-id="642a6-284">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="642a6-285">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="642a6-285">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="642a6-286">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="642a6-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="642a6-287">System-Only</span></span>            | <span data-ttu-id="642a6-288">否</span><span class="sxs-lookup"><span data-stu-id="642a6-288">False</span></span>                           |
| <span data-ttu-id="642a6-289">是-單一值</span><span class="sxs-lookup"><span data-stu-id="642a6-289">Is-Single-Valued</span></span>       | <span data-ttu-id="642a6-290">對</span><span class="sxs-lookup"><span data-stu-id="642a6-290">True</span></span>                            |
| <span data-ttu-id="642a6-291">已編制索引</span><span class="sxs-lookup"><span data-stu-id="642a6-291">Is Indexed</span></span>             | <span data-ttu-id="642a6-292">否</span><span class="sxs-lookup"><span data-stu-id="642a6-292">False</span></span>                           |
| <span data-ttu-id="642a6-293">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="642a6-293">In Global Catalog</span></span>      | <span data-ttu-id="642a6-294">否</span><span class="sxs-lookup"><span data-stu-id="642a6-294">False</span></span>                           |
| <span data-ttu-id="642a6-295">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="642a6-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="642a6-296">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="642a6-296">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="642a6-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="642a6-297">Range-Lower</span></span>            | <span data-ttu-id="642a6-298">1</span><span class="sxs-lookup"><span data-stu-id="642a6-298">1</span></span>                               |
| <span data-ttu-id="642a6-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="642a6-299">Range-Upper</span></span>            | <span data-ttu-id="642a6-300">2048</span><span class="sxs-lookup"><span data-stu-id="642a6-300">2048</span></span>                            |
| <span data-ttu-id="642a6-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-301">Search-Flags</span></span>           | <span data-ttu-id="642a6-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="642a6-302">0x00000000</span></span>                      |
| <span data-ttu-id="642a6-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="642a6-303">System-Flags</span></span>           | <span data-ttu-id="642a6-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="642a6-304">0x00000010</span></span>                      |
| <span data-ttu-id="642a6-305">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="642a6-305">Classes used in</span></span>        | [<span data-ttu-id="642a6-306">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="642a6-306">**Top**</span></span>](c-top.md)<br/> |



 

 






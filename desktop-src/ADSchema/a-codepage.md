---
title: Code-Page 屬性
description: 指定使用者所選擇語言的字碼頁。 Windows 2000 不會使用這個值。
ms.assetid: f98e6fbe-0c9a-4ee0-8158-3eaaca359675
ms.tgt_platform: multiple
keywords:
- Code-Page 屬性 AD 架構
- 字碼頁屬性 AD 架構
topic_type:
- apiref
api_name:
- Code-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c3e9858ba387b98d5556c6010490c024be836b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686879"
---
# <a name="code-page-attribute"></a><span data-ttu-id="68216-106">Code-Page 屬性</span><span class="sxs-lookup"><span data-stu-id="68216-106">Code-Page attribute</span></span>

<span data-ttu-id="68216-107">指定使用者所選擇語言的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="68216-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="68216-108">Windows 2000 不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="68216-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="68216-109">進入</span><span class="sxs-lookup"><span data-stu-id="68216-109">Entry</span></span> | <span data-ttu-id="68216-110">值</span><span class="sxs-lookup"><span data-stu-id="68216-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="68216-111">CN</span><span class="sxs-lookup"><span data-stu-id="68216-111">CN</span></span>                | <span data-ttu-id="68216-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="68216-112">Code-Page</span></span>                                             |
| <span data-ttu-id="68216-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="68216-113">Ldap-Display-Name</span></span> | <span data-ttu-id="68216-114">字碼頁</span><span class="sxs-lookup"><span data-stu-id="68216-114">codePage</span></span>                                              |
| <span data-ttu-id="68216-115">大小</span><span class="sxs-lookup"><span data-stu-id="68216-115">Size</span></span>              | <span data-ttu-id="68216-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="68216-116">4 bytes</span></span>                                               |
| <span data-ttu-id="68216-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="68216-117">Update Privilege</span></span>  | <span data-ttu-id="68216-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="68216-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="68216-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="68216-119">Update Frequency</span></span>  | <span data-ttu-id="68216-120">當使用者想要變更預設語言時。</span><span class="sxs-lookup"><span data-stu-id="68216-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="68216-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="68216-121">Attribute-Id</span></span>      | <span data-ttu-id="68216-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="68216-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="68216-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="68216-123">System-Id-Guid</span></span>    | <span data-ttu-id="68216-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="68216-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="68216-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="68216-125">Syntax</span></span>            | [<span data-ttu-id="68216-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="68216-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="68216-127">實作</span><span class="sxs-lookup"><span data-stu-id="68216-127">Implementations</span></span>

-   [<span data-ttu-id="68216-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="68216-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="68216-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="68216-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="68216-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="68216-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="68216-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="68216-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="68216-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="68216-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="68216-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="68216-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="68216-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68216-134">Windows 2000 Server</span></span>



| <span data-ttu-id="68216-135">進入</span><span class="sxs-lookup"><span data-stu-id="68216-135">Entry</span></span> | <span data-ttu-id="68216-136">值</span><span class="sxs-lookup"><span data-stu-id="68216-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="68216-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="68216-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68216-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="68216-139">System-Only</span></span>            | <span data-ttu-id="68216-140">否</span><span class="sxs-lookup"><span data-stu-id="68216-140">False</span></span>                             |
| <span data-ttu-id="68216-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="68216-141">Is-Single-Valued</span></span>       | <span data-ttu-id="68216-142">對</span><span class="sxs-lookup"><span data-stu-id="68216-142">True</span></span>                              |
| <span data-ttu-id="68216-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="68216-143">Is Indexed</span></span>             | <span data-ttu-id="68216-144">否</span><span class="sxs-lookup"><span data-stu-id="68216-144">False</span></span>                             |
| <span data-ttu-id="68216-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="68216-145">In Global Catalog</span></span>      | <span data-ttu-id="68216-146">否</span><span class="sxs-lookup"><span data-stu-id="68216-146">False</span></span>                             |
| <span data-ttu-id="68216-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="68216-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="68216-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="68216-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="68216-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68216-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="68216-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68216-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="68216-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-151">Search-Flags</span></span>           | <span data-ttu-id="68216-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-152">0x00000010</span></span>                        |
| <span data-ttu-id="68216-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-153">System-Flags</span></span>           | <span data-ttu-id="68216-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-154">0x00000010</span></span>                        |
| <span data-ttu-id="68216-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="68216-155">Classes used in</span></span>        | [<span data-ttu-id="68216-156">**User**</span><span class="sxs-lookup"><span data-stu-id="68216-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="68216-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68216-157">Windows Server 2003</span></span>



| <span data-ttu-id="68216-158">進入</span><span class="sxs-lookup"><span data-stu-id="68216-158">Entry</span></span> | <span data-ttu-id="68216-159">值</span><span class="sxs-lookup"><span data-stu-id="68216-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="68216-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="68216-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68216-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="68216-162">System-Only</span></span>            | <span data-ttu-id="68216-163">否</span><span class="sxs-lookup"><span data-stu-id="68216-163">False</span></span>                             |
| <span data-ttu-id="68216-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="68216-164">Is-Single-Valued</span></span>       | <span data-ttu-id="68216-165">對</span><span class="sxs-lookup"><span data-stu-id="68216-165">True</span></span>                              |
| <span data-ttu-id="68216-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="68216-166">Is Indexed</span></span>             | <span data-ttu-id="68216-167">否</span><span class="sxs-lookup"><span data-stu-id="68216-167">False</span></span>                             |
| <span data-ttu-id="68216-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="68216-168">In Global Catalog</span></span>      | <span data-ttu-id="68216-169">否</span><span class="sxs-lookup"><span data-stu-id="68216-169">False</span></span>                             |
| <span data-ttu-id="68216-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="68216-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="68216-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="68216-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="68216-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68216-172">Range-Lower</span></span>            | <span data-ttu-id="68216-173">0</span><span class="sxs-lookup"><span data-stu-id="68216-173">0</span></span>                                 |
| <span data-ttu-id="68216-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68216-174">Range-Upper</span></span>            | <span data-ttu-id="68216-175">65535</span><span class="sxs-lookup"><span data-stu-id="68216-175">65535</span></span>                             |
| <span data-ttu-id="68216-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-176">Search-Flags</span></span>           | <span data-ttu-id="68216-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-177">0x00000010</span></span>                        |
| <span data-ttu-id="68216-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-178">System-Flags</span></span>           | <span data-ttu-id="68216-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-179">0x00000010</span></span>                        |
| <span data-ttu-id="68216-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="68216-180">Classes used in</span></span>        | [<span data-ttu-id="68216-181">**User**</span><span class="sxs-lookup"><span data-stu-id="68216-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="68216-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="68216-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="68216-183">進入</span><span class="sxs-lookup"><span data-stu-id="68216-183">Entry</span></span> | <span data-ttu-id="68216-184">值</span><span class="sxs-lookup"><span data-stu-id="68216-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="68216-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="68216-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68216-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="68216-187">System-Only</span></span>            | <span data-ttu-id="68216-188">否</span><span class="sxs-lookup"><span data-stu-id="68216-188">False</span></span>                             |
| <span data-ttu-id="68216-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="68216-189">Is-Single-Valued</span></span>       | <span data-ttu-id="68216-190">對</span><span class="sxs-lookup"><span data-stu-id="68216-190">True</span></span>                              |
| <span data-ttu-id="68216-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="68216-191">Is Indexed</span></span>             | <span data-ttu-id="68216-192">否</span><span class="sxs-lookup"><span data-stu-id="68216-192">False</span></span>                             |
| <span data-ttu-id="68216-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="68216-193">In Global Catalog</span></span>      | <span data-ttu-id="68216-194">否</span><span class="sxs-lookup"><span data-stu-id="68216-194">False</span></span>                             |
| <span data-ttu-id="68216-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="68216-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="68216-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="68216-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="68216-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68216-197">Range-Lower</span></span>            | <span data-ttu-id="68216-198">0</span><span class="sxs-lookup"><span data-stu-id="68216-198">0</span></span>                                 |
| <span data-ttu-id="68216-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68216-199">Range-Upper</span></span>            | <span data-ttu-id="68216-200">65535</span><span class="sxs-lookup"><span data-stu-id="68216-200">65535</span></span>                             |
| <span data-ttu-id="68216-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-201">Search-Flags</span></span>           | <span data-ttu-id="68216-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-202">0x00000010</span></span>                        |
| <span data-ttu-id="68216-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-203">System-Flags</span></span>           | <span data-ttu-id="68216-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-204">0x00000010</span></span>                        |
| <span data-ttu-id="68216-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="68216-205">Classes used in</span></span>        | [<span data-ttu-id="68216-206">**User**</span><span class="sxs-lookup"><span data-stu-id="68216-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="68216-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68216-207">Windows Server 2008</span></span>



| <span data-ttu-id="68216-208">進入</span><span class="sxs-lookup"><span data-stu-id="68216-208">Entry</span></span> | <span data-ttu-id="68216-209">值</span><span class="sxs-lookup"><span data-stu-id="68216-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="68216-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="68216-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68216-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="68216-212">System-Only</span></span>            | <span data-ttu-id="68216-213">否</span><span class="sxs-lookup"><span data-stu-id="68216-213">False</span></span>                             |
| <span data-ttu-id="68216-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="68216-214">Is-Single-Valued</span></span>       | <span data-ttu-id="68216-215">對</span><span class="sxs-lookup"><span data-stu-id="68216-215">True</span></span>                              |
| <span data-ttu-id="68216-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="68216-216">Is Indexed</span></span>             | <span data-ttu-id="68216-217">否</span><span class="sxs-lookup"><span data-stu-id="68216-217">False</span></span>                             |
| <span data-ttu-id="68216-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="68216-218">In Global Catalog</span></span>      | <span data-ttu-id="68216-219">否</span><span class="sxs-lookup"><span data-stu-id="68216-219">False</span></span>                             |
| <span data-ttu-id="68216-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="68216-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="68216-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="68216-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="68216-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68216-222">Range-Lower</span></span>            | <span data-ttu-id="68216-223">0</span><span class="sxs-lookup"><span data-stu-id="68216-223">0</span></span>                                 |
| <span data-ttu-id="68216-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68216-224">Range-Upper</span></span>            | <span data-ttu-id="68216-225">65535</span><span class="sxs-lookup"><span data-stu-id="68216-225">65535</span></span>                             |
| <span data-ttu-id="68216-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-226">Search-Flags</span></span>           | <span data-ttu-id="68216-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-227">0x00000010</span></span>                        |
| <span data-ttu-id="68216-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-228">System-Flags</span></span>           | <span data-ttu-id="68216-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-229">0x00000010</span></span>                        |
| <span data-ttu-id="68216-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="68216-230">Classes used in</span></span>        | [<span data-ttu-id="68216-231">**User**</span><span class="sxs-lookup"><span data-stu-id="68216-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="68216-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="68216-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="68216-233">進入</span><span class="sxs-lookup"><span data-stu-id="68216-233">Entry</span></span> | <span data-ttu-id="68216-234">值</span><span class="sxs-lookup"><span data-stu-id="68216-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="68216-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="68216-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68216-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="68216-237">System-Only</span></span>            | <span data-ttu-id="68216-238">否</span><span class="sxs-lookup"><span data-stu-id="68216-238">False</span></span>                             |
| <span data-ttu-id="68216-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="68216-239">Is-Single-Valued</span></span>       | <span data-ttu-id="68216-240">對</span><span class="sxs-lookup"><span data-stu-id="68216-240">True</span></span>                              |
| <span data-ttu-id="68216-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="68216-241">Is Indexed</span></span>             | <span data-ttu-id="68216-242">否</span><span class="sxs-lookup"><span data-stu-id="68216-242">False</span></span>                             |
| <span data-ttu-id="68216-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="68216-243">In Global Catalog</span></span>      | <span data-ttu-id="68216-244">否</span><span class="sxs-lookup"><span data-stu-id="68216-244">False</span></span>                             |
| <span data-ttu-id="68216-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="68216-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="68216-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="68216-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="68216-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68216-247">Range-Lower</span></span>            | <span data-ttu-id="68216-248">0</span><span class="sxs-lookup"><span data-stu-id="68216-248">0</span></span>                                 |
| <span data-ttu-id="68216-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68216-249">Range-Upper</span></span>            | <span data-ttu-id="68216-250">65535</span><span class="sxs-lookup"><span data-stu-id="68216-250">65535</span></span>                             |
| <span data-ttu-id="68216-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-251">Search-Flags</span></span>           | <span data-ttu-id="68216-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-252">0x00000010</span></span>                        |
| <span data-ttu-id="68216-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-253">System-Flags</span></span>           | <span data-ttu-id="68216-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-254">0x00000010</span></span>                        |
| <span data-ttu-id="68216-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="68216-255">Classes used in</span></span>        | [<span data-ttu-id="68216-256">**User**</span><span class="sxs-lookup"><span data-stu-id="68216-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="68216-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68216-257">Windows Server 2012</span></span>



| <span data-ttu-id="68216-258">進入</span><span class="sxs-lookup"><span data-stu-id="68216-258">Entry</span></span> | <span data-ttu-id="68216-259">值</span><span class="sxs-lookup"><span data-stu-id="68216-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="68216-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="68216-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68216-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="68216-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="68216-262">System-Only</span></span>            | <span data-ttu-id="68216-263">否</span><span class="sxs-lookup"><span data-stu-id="68216-263">False</span></span>                             |
| <span data-ttu-id="68216-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="68216-264">Is-Single-Valued</span></span>       | <span data-ttu-id="68216-265">對</span><span class="sxs-lookup"><span data-stu-id="68216-265">True</span></span>                              |
| <span data-ttu-id="68216-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="68216-266">Is Indexed</span></span>             | <span data-ttu-id="68216-267">否</span><span class="sxs-lookup"><span data-stu-id="68216-267">False</span></span>                             |
| <span data-ttu-id="68216-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="68216-268">In Global Catalog</span></span>      | <span data-ttu-id="68216-269">否</span><span class="sxs-lookup"><span data-stu-id="68216-269">False</span></span>                             |
| <span data-ttu-id="68216-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="68216-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="68216-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="68216-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="68216-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68216-272">Range-Lower</span></span>            | <span data-ttu-id="68216-273">0</span><span class="sxs-lookup"><span data-stu-id="68216-273">0</span></span>                                 |
| <span data-ttu-id="68216-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68216-274">Range-Upper</span></span>            | <span data-ttu-id="68216-275">65535</span><span class="sxs-lookup"><span data-stu-id="68216-275">65535</span></span>                             |
| <span data-ttu-id="68216-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-276">Search-Flags</span></span>           | <span data-ttu-id="68216-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-277">0x00000010</span></span>                        |
| <span data-ttu-id="68216-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68216-278">System-Flags</span></span>           | <span data-ttu-id="68216-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68216-279">0x00000010</span></span>                        |
| <span data-ttu-id="68216-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="68216-280">Classes used in</span></span>        | [<span data-ttu-id="68216-281">**User**</span><span class="sxs-lookup"><span data-stu-id="68216-281">**User**</span></span>](c-user.md)<br/> |



 

 






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
# <a name="code-page-attribute"></a><span data-ttu-id="ee060-106">Code-Page 屬性</span><span class="sxs-lookup"><span data-stu-id="ee060-106">Code-Page attribute</span></span>

<span data-ttu-id="ee060-107">指定使用者所選擇語言的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="ee060-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="ee060-108">Windows 2000 不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="ee060-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="ee060-109">進入</span><span class="sxs-lookup"><span data-stu-id="ee060-109">Entry</span></span> | <span data-ttu-id="ee060-110">值</span><span class="sxs-lookup"><span data-stu-id="ee060-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ee060-111">CN</span><span class="sxs-lookup"><span data-stu-id="ee060-111">CN</span></span>                | <span data-ttu-id="ee060-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="ee060-112">Code-Page</span></span>                                             |
| <span data-ttu-id="ee060-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ee060-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ee060-114">字碼頁</span><span class="sxs-lookup"><span data-stu-id="ee060-114">codePage</span></span>                                              |
| <span data-ttu-id="ee060-115">大小</span><span class="sxs-lookup"><span data-stu-id="ee060-115">Size</span></span>              | <span data-ttu-id="ee060-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ee060-116">4 bytes</span></span>                                               |
| <span data-ttu-id="ee060-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ee060-117">Update Privilege</span></span>  | <span data-ttu-id="ee060-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="ee060-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="ee060-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ee060-119">Update Frequency</span></span>  | <span data-ttu-id="ee060-120">當使用者想要變更預設語言時。</span><span class="sxs-lookup"><span data-stu-id="ee060-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="ee060-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ee060-121">Attribute-Id</span></span>      | <span data-ttu-id="ee060-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="ee060-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="ee060-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ee060-123">System-Id-Guid</span></span>    | <span data-ttu-id="ee060-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ee060-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="ee060-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee060-125">Syntax</span></span>            | [<span data-ttu-id="ee060-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ee060-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="ee060-127">實作</span><span class="sxs-lookup"><span data-stu-id="ee060-127">Implementations</span></span>

-   [<span data-ttu-id="ee060-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ee060-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ee060-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ee060-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ee060-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ee060-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ee060-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ee060-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ee060-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ee060-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ee060-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ee060-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ee060-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee060-134">Windows 2000 Server</span></span>



| <span data-ttu-id="ee060-135">進入</span><span class="sxs-lookup"><span data-stu-id="ee060-135">Entry</span></span> | <span data-ttu-id="ee060-136">值</span><span class="sxs-lookup"><span data-stu-id="ee060-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee060-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ee060-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee060-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee060-139">System-Only</span></span>            | <span data-ttu-id="ee060-140">否</span><span class="sxs-lookup"><span data-stu-id="ee060-140">False</span></span>                             |
| <span data-ttu-id="ee060-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ee060-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ee060-142">對</span><span class="sxs-lookup"><span data-stu-id="ee060-142">True</span></span>                              |
| <span data-ttu-id="ee060-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ee060-143">Is Indexed</span></span>             | <span data-ttu-id="ee060-144">否</span><span class="sxs-lookup"><span data-stu-id="ee060-144">False</span></span>                             |
| <span data-ttu-id="ee060-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ee060-145">In Global Catalog</span></span>      | <span data-ttu-id="ee060-146">否</span><span class="sxs-lookup"><span data-stu-id="ee060-146">False</span></span>                             |
| <span data-ttu-id="ee060-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ee060-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee060-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ee060-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee060-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee060-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ee060-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee060-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ee060-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-151">Search-Flags</span></span>           | <span data-ttu-id="ee060-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-152">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-153">System-Flags</span></span>           | <span data-ttu-id="ee060-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-154">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ee060-155">Classes used in</span></span>        | [<span data-ttu-id="ee060-156">**User**</span><span class="sxs-lookup"><span data-stu-id="ee060-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ee060-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee060-157">Windows Server 2003</span></span>



| <span data-ttu-id="ee060-158">進入</span><span class="sxs-lookup"><span data-stu-id="ee060-158">Entry</span></span> | <span data-ttu-id="ee060-159">值</span><span class="sxs-lookup"><span data-stu-id="ee060-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee060-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ee060-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee060-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee060-162">System-Only</span></span>            | <span data-ttu-id="ee060-163">否</span><span class="sxs-lookup"><span data-stu-id="ee060-163">False</span></span>                             |
| <span data-ttu-id="ee060-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ee060-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ee060-165">對</span><span class="sxs-lookup"><span data-stu-id="ee060-165">True</span></span>                              |
| <span data-ttu-id="ee060-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ee060-166">Is Indexed</span></span>             | <span data-ttu-id="ee060-167">否</span><span class="sxs-lookup"><span data-stu-id="ee060-167">False</span></span>                             |
| <span data-ttu-id="ee060-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ee060-168">In Global Catalog</span></span>      | <span data-ttu-id="ee060-169">否</span><span class="sxs-lookup"><span data-stu-id="ee060-169">False</span></span>                             |
| <span data-ttu-id="ee060-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ee060-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee060-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ee060-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee060-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee060-172">Range-Lower</span></span>            | <span data-ttu-id="ee060-173">0</span><span class="sxs-lookup"><span data-stu-id="ee060-173">0</span></span>                                 |
| <span data-ttu-id="ee060-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee060-174">Range-Upper</span></span>            | <span data-ttu-id="ee060-175">65535</span><span class="sxs-lookup"><span data-stu-id="ee060-175">65535</span></span>                             |
| <span data-ttu-id="ee060-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-176">Search-Flags</span></span>           | <span data-ttu-id="ee060-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-177">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-178">System-Flags</span></span>           | <span data-ttu-id="ee060-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-179">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ee060-180">Classes used in</span></span>        | [<span data-ttu-id="ee060-181">**User**</span><span class="sxs-lookup"><span data-stu-id="ee060-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ee060-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ee060-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ee060-183">進入</span><span class="sxs-lookup"><span data-stu-id="ee060-183">Entry</span></span> | <span data-ttu-id="ee060-184">值</span><span class="sxs-lookup"><span data-stu-id="ee060-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee060-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ee060-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee060-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee060-187">System-Only</span></span>            | <span data-ttu-id="ee060-188">否</span><span class="sxs-lookup"><span data-stu-id="ee060-188">False</span></span>                             |
| <span data-ttu-id="ee060-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ee060-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ee060-190">對</span><span class="sxs-lookup"><span data-stu-id="ee060-190">True</span></span>                              |
| <span data-ttu-id="ee060-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ee060-191">Is Indexed</span></span>             | <span data-ttu-id="ee060-192">否</span><span class="sxs-lookup"><span data-stu-id="ee060-192">False</span></span>                             |
| <span data-ttu-id="ee060-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ee060-193">In Global Catalog</span></span>      | <span data-ttu-id="ee060-194">否</span><span class="sxs-lookup"><span data-stu-id="ee060-194">False</span></span>                             |
| <span data-ttu-id="ee060-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ee060-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee060-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ee060-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee060-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee060-197">Range-Lower</span></span>            | <span data-ttu-id="ee060-198">0</span><span class="sxs-lookup"><span data-stu-id="ee060-198">0</span></span>                                 |
| <span data-ttu-id="ee060-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee060-199">Range-Upper</span></span>            | <span data-ttu-id="ee060-200">65535</span><span class="sxs-lookup"><span data-stu-id="ee060-200">65535</span></span>                             |
| <span data-ttu-id="ee060-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-201">Search-Flags</span></span>           | <span data-ttu-id="ee060-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-202">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-203">System-Flags</span></span>           | <span data-ttu-id="ee060-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-204">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ee060-205">Classes used in</span></span>        | [<span data-ttu-id="ee060-206">**User**</span><span class="sxs-lookup"><span data-stu-id="ee060-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ee060-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee060-207">Windows Server 2008</span></span>



| <span data-ttu-id="ee060-208">進入</span><span class="sxs-lookup"><span data-stu-id="ee060-208">Entry</span></span> | <span data-ttu-id="ee060-209">值</span><span class="sxs-lookup"><span data-stu-id="ee060-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee060-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ee060-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee060-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee060-212">System-Only</span></span>            | <span data-ttu-id="ee060-213">否</span><span class="sxs-lookup"><span data-stu-id="ee060-213">False</span></span>                             |
| <span data-ttu-id="ee060-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ee060-214">Is-Single-Valued</span></span>       | <span data-ttu-id="ee060-215">對</span><span class="sxs-lookup"><span data-stu-id="ee060-215">True</span></span>                              |
| <span data-ttu-id="ee060-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ee060-216">Is Indexed</span></span>             | <span data-ttu-id="ee060-217">否</span><span class="sxs-lookup"><span data-stu-id="ee060-217">False</span></span>                             |
| <span data-ttu-id="ee060-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ee060-218">In Global Catalog</span></span>      | <span data-ttu-id="ee060-219">否</span><span class="sxs-lookup"><span data-stu-id="ee060-219">False</span></span>                             |
| <span data-ttu-id="ee060-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ee060-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee060-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ee060-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee060-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee060-222">Range-Lower</span></span>            | <span data-ttu-id="ee060-223">0</span><span class="sxs-lookup"><span data-stu-id="ee060-223">0</span></span>                                 |
| <span data-ttu-id="ee060-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee060-224">Range-Upper</span></span>            | <span data-ttu-id="ee060-225">65535</span><span class="sxs-lookup"><span data-stu-id="ee060-225">65535</span></span>                             |
| <span data-ttu-id="ee060-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-226">Search-Flags</span></span>           | <span data-ttu-id="ee060-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-227">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-228">System-Flags</span></span>           | <span data-ttu-id="ee060-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-229">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ee060-230">Classes used in</span></span>        | [<span data-ttu-id="ee060-231">**User**</span><span class="sxs-lookup"><span data-stu-id="ee060-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ee060-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee060-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ee060-233">進入</span><span class="sxs-lookup"><span data-stu-id="ee060-233">Entry</span></span> | <span data-ttu-id="ee060-234">值</span><span class="sxs-lookup"><span data-stu-id="ee060-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee060-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ee060-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee060-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee060-237">System-Only</span></span>            | <span data-ttu-id="ee060-238">否</span><span class="sxs-lookup"><span data-stu-id="ee060-238">False</span></span>                             |
| <span data-ttu-id="ee060-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ee060-239">Is-Single-Valued</span></span>       | <span data-ttu-id="ee060-240">對</span><span class="sxs-lookup"><span data-stu-id="ee060-240">True</span></span>                              |
| <span data-ttu-id="ee060-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ee060-241">Is Indexed</span></span>             | <span data-ttu-id="ee060-242">否</span><span class="sxs-lookup"><span data-stu-id="ee060-242">False</span></span>                             |
| <span data-ttu-id="ee060-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ee060-243">In Global Catalog</span></span>      | <span data-ttu-id="ee060-244">否</span><span class="sxs-lookup"><span data-stu-id="ee060-244">False</span></span>                             |
| <span data-ttu-id="ee060-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ee060-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee060-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ee060-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee060-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee060-247">Range-Lower</span></span>            | <span data-ttu-id="ee060-248">0</span><span class="sxs-lookup"><span data-stu-id="ee060-248">0</span></span>                                 |
| <span data-ttu-id="ee060-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee060-249">Range-Upper</span></span>            | <span data-ttu-id="ee060-250">65535</span><span class="sxs-lookup"><span data-stu-id="ee060-250">65535</span></span>                             |
| <span data-ttu-id="ee060-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-251">Search-Flags</span></span>           | <span data-ttu-id="ee060-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-252">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-253">System-Flags</span></span>           | <span data-ttu-id="ee060-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-254">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ee060-255">Classes used in</span></span>        | [<span data-ttu-id="ee060-256">**User**</span><span class="sxs-lookup"><span data-stu-id="ee060-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ee060-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee060-257">Windows Server 2012</span></span>



| <span data-ttu-id="ee060-258">進入</span><span class="sxs-lookup"><span data-stu-id="ee060-258">Entry</span></span> | <span data-ttu-id="ee060-259">值</span><span class="sxs-lookup"><span data-stu-id="ee060-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ee060-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ee060-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee060-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ee060-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee060-262">System-Only</span></span>            | <span data-ttu-id="ee060-263">否</span><span class="sxs-lookup"><span data-stu-id="ee060-263">False</span></span>                             |
| <span data-ttu-id="ee060-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ee060-264">Is-Single-Valued</span></span>       | <span data-ttu-id="ee060-265">對</span><span class="sxs-lookup"><span data-stu-id="ee060-265">True</span></span>                              |
| <span data-ttu-id="ee060-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ee060-266">Is Indexed</span></span>             | <span data-ttu-id="ee060-267">否</span><span class="sxs-lookup"><span data-stu-id="ee060-267">False</span></span>                             |
| <span data-ttu-id="ee060-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ee060-268">In Global Catalog</span></span>      | <span data-ttu-id="ee060-269">否</span><span class="sxs-lookup"><span data-stu-id="ee060-269">False</span></span>                             |
| <span data-ttu-id="ee060-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ee060-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee060-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ee060-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ee060-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee060-272">Range-Lower</span></span>            | <span data-ttu-id="ee060-273">0</span><span class="sxs-lookup"><span data-stu-id="ee060-273">0</span></span>                                 |
| <span data-ttu-id="ee060-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee060-274">Range-Upper</span></span>            | <span data-ttu-id="ee060-275">65535</span><span class="sxs-lookup"><span data-stu-id="ee060-275">65535</span></span>                             |
| <span data-ttu-id="ee060-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-276">Search-Flags</span></span>           | <span data-ttu-id="ee060-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-277">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee060-278">System-Flags</span></span>           | <span data-ttu-id="ee060-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee060-279">0x00000010</span></span>                        |
| <span data-ttu-id="ee060-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ee060-280">Classes used in</span></span>        | [<span data-ttu-id="ee060-281">**User**</span><span class="sxs-lookup"><span data-stu-id="ee060-281">**User**</span></span>](c-user.md)<br/> |



 

 






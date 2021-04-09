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
# <a name="code-page-attribute"></a><span data-ttu-id="2b2be-106">Code-Page 屬性</span><span class="sxs-lookup"><span data-stu-id="2b2be-106">Code-Page attribute</span></span>

<span data-ttu-id="2b2be-107">指定使用者所選擇語言的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="2b2be-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="2b2be-108">Windows 2000 不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="2b2be-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="2b2be-109">進入</span><span class="sxs-lookup"><span data-stu-id="2b2be-109">Entry</span></span> | <span data-ttu-id="2b2be-110">值</span><span class="sxs-lookup"><span data-stu-id="2b2be-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2b2be-111">CN</span><span class="sxs-lookup"><span data-stu-id="2b2be-111">CN</span></span>                | <span data-ttu-id="2b2be-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="2b2be-112">Code-Page</span></span>                                             |
| <span data-ttu-id="2b2be-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2b2be-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2b2be-114">字碼頁</span><span class="sxs-lookup"><span data-stu-id="2b2be-114">codePage</span></span>                                              |
| <span data-ttu-id="2b2be-115">大小</span><span class="sxs-lookup"><span data-stu-id="2b2be-115">Size</span></span>              | <span data-ttu-id="2b2be-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="2b2be-116">4 bytes</span></span>                                               |
| <span data-ttu-id="2b2be-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2b2be-117">Update Privilege</span></span>  | <span data-ttu-id="2b2be-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="2b2be-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="2b2be-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2b2be-119">Update Frequency</span></span>  | <span data-ttu-id="2b2be-120">當使用者想要變更預設語言時。</span><span class="sxs-lookup"><span data-stu-id="2b2be-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="2b2be-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2b2be-121">Attribute-Id</span></span>      | <span data-ttu-id="2b2be-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="2b2be-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="2b2be-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2b2be-123">System-Id-Guid</span></span>    | <span data-ttu-id="2b2be-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2b2be-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="2b2be-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b2be-125">Syntax</span></span>            | [<span data-ttu-id="2b2be-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="2b2be-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="2b2be-127">實作</span><span class="sxs-lookup"><span data-stu-id="2b2be-127">Implementations</span></span>

-   [<span data-ttu-id="2b2be-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2b2be-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2b2be-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2b2be-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2b2be-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2b2be-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2b2be-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2b2be-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2b2be-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2b2be-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2b2be-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2b2be-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2b2be-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b2be-134">Windows 2000 Server</span></span>



| <span data-ttu-id="2b2be-135">進入</span><span class="sxs-lookup"><span data-stu-id="2b2be-135">Entry</span></span> | <span data-ttu-id="2b2be-136">值</span><span class="sxs-lookup"><span data-stu-id="2b2be-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b2be-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b2be-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2be-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2be-139">System-Only</span></span>            | <span data-ttu-id="2b2be-140">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-140">False</span></span>                             |
| <span data-ttu-id="2b2be-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b2be-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2be-142">對</span><span class="sxs-lookup"><span data-stu-id="2b2be-142">True</span></span>                              |
| <span data-ttu-id="2b2be-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b2be-143">Is Indexed</span></span>             | <span data-ttu-id="2b2be-144">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-144">False</span></span>                             |
| <span data-ttu-id="2b2be-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b2be-145">In Global Catalog</span></span>      | <span data-ttu-id="2b2be-146">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-146">False</span></span>                             |
| <span data-ttu-id="2b2be-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b2be-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2be-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b2be-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b2be-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2be-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2b2be-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2be-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2b2be-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-151">Search-Flags</span></span>           | <span data-ttu-id="2b2be-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-152">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-153">System-Flags</span></span>           | <span data-ttu-id="2b2be-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-154">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b2be-155">Classes used in</span></span>        | [<span data-ttu-id="2b2be-156">**User**</span><span class="sxs-lookup"><span data-stu-id="2b2be-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2b2be-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b2be-157">Windows Server 2003</span></span>



| <span data-ttu-id="2b2be-158">進入</span><span class="sxs-lookup"><span data-stu-id="2b2be-158">Entry</span></span> | <span data-ttu-id="2b2be-159">值</span><span class="sxs-lookup"><span data-stu-id="2b2be-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b2be-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b2be-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2be-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2be-162">System-Only</span></span>            | <span data-ttu-id="2b2be-163">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-163">False</span></span>                             |
| <span data-ttu-id="2b2be-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b2be-164">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2be-165">對</span><span class="sxs-lookup"><span data-stu-id="2b2be-165">True</span></span>                              |
| <span data-ttu-id="2b2be-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b2be-166">Is Indexed</span></span>             | <span data-ttu-id="2b2be-167">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-167">False</span></span>                             |
| <span data-ttu-id="2b2be-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b2be-168">In Global Catalog</span></span>      | <span data-ttu-id="2b2be-169">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-169">False</span></span>                             |
| <span data-ttu-id="2b2be-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b2be-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2be-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b2be-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b2be-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2be-172">Range-Lower</span></span>            | <span data-ttu-id="2b2be-173">0</span><span class="sxs-lookup"><span data-stu-id="2b2be-173">0</span></span>                                 |
| <span data-ttu-id="2b2be-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2be-174">Range-Upper</span></span>            | <span data-ttu-id="2b2be-175">65535</span><span class="sxs-lookup"><span data-stu-id="2b2be-175">65535</span></span>                             |
| <span data-ttu-id="2b2be-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-176">Search-Flags</span></span>           | <span data-ttu-id="2b2be-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-177">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-178">System-Flags</span></span>           | <span data-ttu-id="2b2be-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-179">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b2be-180">Classes used in</span></span>        | [<span data-ttu-id="2b2be-181">**User**</span><span class="sxs-lookup"><span data-stu-id="2b2be-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2b2be-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2b2be-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2b2be-183">進入</span><span class="sxs-lookup"><span data-stu-id="2b2be-183">Entry</span></span> | <span data-ttu-id="2b2be-184">值</span><span class="sxs-lookup"><span data-stu-id="2b2be-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b2be-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b2be-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2be-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2be-187">System-Only</span></span>            | <span data-ttu-id="2b2be-188">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-188">False</span></span>                             |
| <span data-ttu-id="2b2be-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b2be-189">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2be-190">對</span><span class="sxs-lookup"><span data-stu-id="2b2be-190">True</span></span>                              |
| <span data-ttu-id="2b2be-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b2be-191">Is Indexed</span></span>             | <span data-ttu-id="2b2be-192">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-192">False</span></span>                             |
| <span data-ttu-id="2b2be-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b2be-193">In Global Catalog</span></span>      | <span data-ttu-id="2b2be-194">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-194">False</span></span>                             |
| <span data-ttu-id="2b2be-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b2be-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2be-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b2be-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b2be-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2be-197">Range-Lower</span></span>            | <span data-ttu-id="2b2be-198">0</span><span class="sxs-lookup"><span data-stu-id="2b2be-198">0</span></span>                                 |
| <span data-ttu-id="2b2be-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2be-199">Range-Upper</span></span>            | <span data-ttu-id="2b2be-200">65535</span><span class="sxs-lookup"><span data-stu-id="2b2be-200">65535</span></span>                             |
| <span data-ttu-id="2b2be-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-201">Search-Flags</span></span>           | <span data-ttu-id="2b2be-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-202">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-203">System-Flags</span></span>           | <span data-ttu-id="2b2be-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-204">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b2be-205">Classes used in</span></span>        | [<span data-ttu-id="2b2be-206">**User**</span><span class="sxs-lookup"><span data-stu-id="2b2be-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2b2be-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b2be-207">Windows Server 2008</span></span>



| <span data-ttu-id="2b2be-208">進入</span><span class="sxs-lookup"><span data-stu-id="2b2be-208">Entry</span></span> | <span data-ttu-id="2b2be-209">值</span><span class="sxs-lookup"><span data-stu-id="2b2be-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b2be-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b2be-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2be-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2be-212">System-Only</span></span>            | <span data-ttu-id="2b2be-213">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-213">False</span></span>                             |
| <span data-ttu-id="2b2be-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b2be-214">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2be-215">對</span><span class="sxs-lookup"><span data-stu-id="2b2be-215">True</span></span>                              |
| <span data-ttu-id="2b2be-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b2be-216">Is Indexed</span></span>             | <span data-ttu-id="2b2be-217">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-217">False</span></span>                             |
| <span data-ttu-id="2b2be-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b2be-218">In Global Catalog</span></span>      | <span data-ttu-id="2b2be-219">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-219">False</span></span>                             |
| <span data-ttu-id="2b2be-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b2be-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2be-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b2be-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b2be-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2be-222">Range-Lower</span></span>            | <span data-ttu-id="2b2be-223">0</span><span class="sxs-lookup"><span data-stu-id="2b2be-223">0</span></span>                                 |
| <span data-ttu-id="2b2be-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2be-224">Range-Upper</span></span>            | <span data-ttu-id="2b2be-225">65535</span><span class="sxs-lookup"><span data-stu-id="2b2be-225">65535</span></span>                             |
| <span data-ttu-id="2b2be-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-226">Search-Flags</span></span>           | <span data-ttu-id="2b2be-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-227">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-228">System-Flags</span></span>           | <span data-ttu-id="2b2be-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-229">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b2be-230">Classes used in</span></span>        | [<span data-ttu-id="2b2be-231">**User**</span><span class="sxs-lookup"><span data-stu-id="2b2be-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2b2be-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b2be-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2b2be-233">進入</span><span class="sxs-lookup"><span data-stu-id="2b2be-233">Entry</span></span> | <span data-ttu-id="2b2be-234">值</span><span class="sxs-lookup"><span data-stu-id="2b2be-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b2be-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b2be-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2be-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2be-237">System-Only</span></span>            | <span data-ttu-id="2b2be-238">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-238">False</span></span>                             |
| <span data-ttu-id="2b2be-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b2be-239">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2be-240">對</span><span class="sxs-lookup"><span data-stu-id="2b2be-240">True</span></span>                              |
| <span data-ttu-id="2b2be-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b2be-241">Is Indexed</span></span>             | <span data-ttu-id="2b2be-242">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-242">False</span></span>                             |
| <span data-ttu-id="2b2be-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b2be-243">In Global Catalog</span></span>      | <span data-ttu-id="2b2be-244">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-244">False</span></span>                             |
| <span data-ttu-id="2b2be-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b2be-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2be-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b2be-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b2be-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2be-247">Range-Lower</span></span>            | <span data-ttu-id="2b2be-248">0</span><span class="sxs-lookup"><span data-stu-id="2b2be-248">0</span></span>                                 |
| <span data-ttu-id="2b2be-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2be-249">Range-Upper</span></span>            | <span data-ttu-id="2b2be-250">65535</span><span class="sxs-lookup"><span data-stu-id="2b2be-250">65535</span></span>                             |
| <span data-ttu-id="2b2be-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-251">Search-Flags</span></span>           | <span data-ttu-id="2b2be-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-252">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-253">System-Flags</span></span>           | <span data-ttu-id="2b2be-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-254">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b2be-255">Classes used in</span></span>        | [<span data-ttu-id="2b2be-256">**User**</span><span class="sxs-lookup"><span data-stu-id="2b2be-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2b2be-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b2be-257">Windows Server 2012</span></span>



| <span data-ttu-id="2b2be-258">進入</span><span class="sxs-lookup"><span data-stu-id="2b2be-258">Entry</span></span> | <span data-ttu-id="2b2be-259">值</span><span class="sxs-lookup"><span data-stu-id="2b2be-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2b2be-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b2be-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2be-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2b2be-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2be-262">System-Only</span></span>            | <span data-ttu-id="2b2be-263">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-263">False</span></span>                             |
| <span data-ttu-id="2b2be-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b2be-264">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2be-265">對</span><span class="sxs-lookup"><span data-stu-id="2b2be-265">True</span></span>                              |
| <span data-ttu-id="2b2be-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b2be-266">Is Indexed</span></span>             | <span data-ttu-id="2b2be-267">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-267">False</span></span>                             |
| <span data-ttu-id="2b2be-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b2be-268">In Global Catalog</span></span>      | <span data-ttu-id="2b2be-269">否</span><span class="sxs-lookup"><span data-stu-id="2b2be-269">False</span></span>                             |
| <span data-ttu-id="2b2be-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b2be-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2be-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b2be-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2b2be-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2be-272">Range-Lower</span></span>            | <span data-ttu-id="2b2be-273">0</span><span class="sxs-lookup"><span data-stu-id="2b2be-273">0</span></span>                                 |
| <span data-ttu-id="2b2be-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2be-274">Range-Upper</span></span>            | <span data-ttu-id="2b2be-275">65535</span><span class="sxs-lookup"><span data-stu-id="2b2be-275">65535</span></span>                             |
| <span data-ttu-id="2b2be-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-276">Search-Flags</span></span>           | <span data-ttu-id="2b2be-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-277">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2be-278">System-Flags</span></span>           | <span data-ttu-id="2b2be-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b2be-279">0x00000010</span></span>                        |
| <span data-ttu-id="2b2be-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b2be-280">Classes used in</span></span>        | [<span data-ttu-id="2b2be-281">**User**</span><span class="sxs-lookup"><span data-stu-id="2b2be-281">**User**</span></span>](c-user.md)<br/> |



 

 






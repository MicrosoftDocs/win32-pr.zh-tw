---
title: Comment 屬性
description: 使用者的批註。 這個字串可以是 null 字串。
ms.assetid: c57493b3-a42a-49ad-8f8c-0afadbb3ba09
ms.tgt_platform: multiple
keywords:
- Comment 屬性 AD 架構
- info 屬性 AD 架構
topic_type:
- apiref
api_name:
- Comment
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd84674fce08f75c3162628b32f67a75fb8c026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686783"
---
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="527df-106"> (AD 架構) 的批註屬性</span><span class="sxs-lookup"><span data-stu-id="527df-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="527df-107">使用者的批註。</span><span class="sxs-lookup"><span data-stu-id="527df-107">The user's comments.</span></span> <span data-ttu-id="527df-108">這個字串可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="527df-108">This string can be a null string.</span></span>



| <span data-ttu-id="527df-109">進入</span><span class="sxs-lookup"><span data-stu-id="527df-109">Entry</span></span> | <span data-ttu-id="527df-110">值</span><span class="sxs-lookup"><span data-stu-id="527df-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="527df-111">CN</span><span class="sxs-lookup"><span data-stu-id="527df-111">CN</span></span>                | <span data-ttu-id="527df-112">註解</span><span class="sxs-lookup"><span data-stu-id="527df-112">Comment</span></span>                                                                  |
| <span data-ttu-id="527df-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="527df-113">Ldap-Display-Name</span></span> | <span data-ttu-id="527df-114">info</span><span class="sxs-lookup"><span data-stu-id="527df-114">info</span></span>                                                                     |
| <span data-ttu-id="527df-115">大小</span><span class="sxs-lookup"><span data-stu-id="527df-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="527df-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="527df-116">Update Privilege</span></span>  | <span data-ttu-id="527df-117">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="527df-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="527df-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="527df-118">Update Frequency</span></span>  | <span data-ttu-id="527df-119">每次使用者或系統管理員需要在帳戶上新增留言。</span><span class="sxs-lookup"><span data-stu-id="527df-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="527df-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="527df-120">Attribute-Id</span></span>      | <span data-ttu-id="527df-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="527df-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="527df-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="527df-122">System-Id-Guid</span></span>    | <span data-ttu-id="527df-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="527df-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="527df-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="527df-124">Syntax</span></span>            | [<span data-ttu-id="527df-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="527df-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="527df-126">實作</span><span class="sxs-lookup"><span data-stu-id="527df-126">Implementations</span></span>

-   [<span data-ttu-id="527df-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="527df-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="527df-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="527df-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="527df-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="527df-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="527df-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="527df-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="527df-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="527df-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="527df-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="527df-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="527df-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="527df-133">Windows 2000 Server</span></span>



| <span data-ttu-id="527df-134">進入</span><span class="sxs-lookup"><span data-stu-id="527df-134">Entry</span></span> | <span data-ttu-id="527df-135">值</span><span class="sxs-lookup"><span data-stu-id="527df-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="527df-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="527df-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="527df-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="527df-137">MAPI-Id</span></span>                | <span data-ttu-id="527df-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="527df-138">0x3004</span></span>                                               |
| <span data-ttu-id="527df-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="527df-139">System-Only</span></span>            | <span data-ttu-id="527df-140">否</span><span class="sxs-lookup"><span data-stu-id="527df-140">False</span></span>                                                |
| <span data-ttu-id="527df-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="527df-141">Is-Single-Valued</span></span>       | <span data-ttu-id="527df-142">對</span><span class="sxs-lookup"><span data-stu-id="527df-142">True</span></span>                                                 |
| <span data-ttu-id="527df-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="527df-143">Is Indexed</span></span>             | <span data-ttu-id="527df-144">否</span><span class="sxs-lookup"><span data-stu-id="527df-144">False</span></span>                                                |
| <span data-ttu-id="527df-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="527df-145">In Global Catalog</span></span>      | <span data-ttu-id="527df-146">否</span><span class="sxs-lookup"><span data-stu-id="527df-146">False</span></span>                                                |
| <span data-ttu-id="527df-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="527df-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="527df-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="527df-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="527df-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="527df-149">Range-Lower</span></span>            | <span data-ttu-id="527df-150">1</span><span class="sxs-lookup"><span data-stu-id="527df-150">1</span></span>                                                    |
| <span data-ttu-id="527df-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="527df-151">Range-Upper</span></span>            | <span data-ttu-id="527df-152">1024</span><span class="sxs-lookup"><span data-stu-id="527df-152">1024</span></span>                                                 |
| <span data-ttu-id="527df-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-153">Search-Flags</span></span>           | <span data-ttu-id="527df-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="527df-154">0x00000000</span></span>                                           |
| <span data-ttu-id="527df-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-155">System-Flags</span></span>           | <span data-ttu-id="527df-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="527df-156">0x00000010</span></span>                                           |
| <span data-ttu-id="527df-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="527df-157">Classes used in</span></span>        | [<span data-ttu-id="527df-158">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="527df-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="527df-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="527df-159">Windows Server 2003</span></span>



| <span data-ttu-id="527df-160">進入</span><span class="sxs-lookup"><span data-stu-id="527df-160">Entry</span></span> | <span data-ttu-id="527df-161">值</span><span class="sxs-lookup"><span data-stu-id="527df-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="527df-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="527df-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="527df-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="527df-163">MAPI-Id</span></span>                | <span data-ttu-id="527df-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="527df-164">0x3004</span></span>                                               |
| <span data-ttu-id="527df-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="527df-165">System-Only</span></span>            | <span data-ttu-id="527df-166">否</span><span class="sxs-lookup"><span data-stu-id="527df-166">False</span></span>                                                |
| <span data-ttu-id="527df-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="527df-167">Is-Single-Valued</span></span>       | <span data-ttu-id="527df-168">對</span><span class="sxs-lookup"><span data-stu-id="527df-168">True</span></span>                                                 |
| <span data-ttu-id="527df-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="527df-169">Is Indexed</span></span>             | <span data-ttu-id="527df-170">否</span><span class="sxs-lookup"><span data-stu-id="527df-170">False</span></span>                                                |
| <span data-ttu-id="527df-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="527df-171">In Global Catalog</span></span>      | <span data-ttu-id="527df-172">否</span><span class="sxs-lookup"><span data-stu-id="527df-172">False</span></span>                                                |
| <span data-ttu-id="527df-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="527df-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="527df-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="527df-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="527df-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="527df-175">Range-Lower</span></span>            | <span data-ttu-id="527df-176">1</span><span class="sxs-lookup"><span data-stu-id="527df-176">1</span></span>                                                    |
| <span data-ttu-id="527df-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="527df-177">Range-Upper</span></span>            | <span data-ttu-id="527df-178">1024</span><span class="sxs-lookup"><span data-stu-id="527df-178">1024</span></span>                                                 |
| <span data-ttu-id="527df-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-179">Search-Flags</span></span>           | <span data-ttu-id="527df-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="527df-180">0x00000000</span></span>                                           |
| <span data-ttu-id="527df-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-181">System-Flags</span></span>           | <span data-ttu-id="527df-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="527df-182">0x00000010</span></span>                                           |
| <span data-ttu-id="527df-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="527df-183">Classes used in</span></span>        | [<span data-ttu-id="527df-184">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="527df-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="527df-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="527df-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="527df-186">進入</span><span class="sxs-lookup"><span data-stu-id="527df-186">Entry</span></span> | <span data-ttu-id="527df-187">值</span><span class="sxs-lookup"><span data-stu-id="527df-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="527df-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="527df-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="527df-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="527df-189">MAPI-Id</span></span>                | <span data-ttu-id="527df-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="527df-190">0x3004</span></span>                                               |
| <span data-ttu-id="527df-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="527df-191">System-Only</span></span>            | <span data-ttu-id="527df-192">否</span><span class="sxs-lookup"><span data-stu-id="527df-192">False</span></span>                                                |
| <span data-ttu-id="527df-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="527df-193">Is-Single-Valued</span></span>       | <span data-ttu-id="527df-194">對</span><span class="sxs-lookup"><span data-stu-id="527df-194">True</span></span>                                                 |
| <span data-ttu-id="527df-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="527df-195">Is Indexed</span></span>             | <span data-ttu-id="527df-196">否</span><span class="sxs-lookup"><span data-stu-id="527df-196">False</span></span>                                                |
| <span data-ttu-id="527df-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="527df-197">In Global Catalog</span></span>      | <span data-ttu-id="527df-198">否</span><span class="sxs-lookup"><span data-stu-id="527df-198">False</span></span>                                                |
| <span data-ttu-id="527df-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="527df-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="527df-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="527df-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="527df-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="527df-201">Range-Lower</span></span>            | <span data-ttu-id="527df-202">1</span><span class="sxs-lookup"><span data-stu-id="527df-202">1</span></span>                                                    |
| <span data-ttu-id="527df-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="527df-203">Range-Upper</span></span>            | <span data-ttu-id="527df-204">1024</span><span class="sxs-lookup"><span data-stu-id="527df-204">1024</span></span>                                                 |
| <span data-ttu-id="527df-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-205">Search-Flags</span></span>           | <span data-ttu-id="527df-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="527df-206">0x00000000</span></span>                                           |
| <span data-ttu-id="527df-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-207">System-Flags</span></span>           | <span data-ttu-id="527df-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="527df-208">0x00000010</span></span>                                           |
| <span data-ttu-id="527df-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="527df-209">Classes used in</span></span>        | [<span data-ttu-id="527df-210">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="527df-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="527df-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="527df-211">Windows Server 2008</span></span>



| <span data-ttu-id="527df-212">進入</span><span class="sxs-lookup"><span data-stu-id="527df-212">Entry</span></span> | <span data-ttu-id="527df-213">值</span><span class="sxs-lookup"><span data-stu-id="527df-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="527df-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="527df-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="527df-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="527df-215">MAPI-Id</span></span>                | <span data-ttu-id="527df-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="527df-216">0x3004</span></span>                                               |
| <span data-ttu-id="527df-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="527df-217">System-Only</span></span>            | <span data-ttu-id="527df-218">否</span><span class="sxs-lookup"><span data-stu-id="527df-218">False</span></span>                                                |
| <span data-ttu-id="527df-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="527df-219">Is-Single-Valued</span></span>       | <span data-ttu-id="527df-220">對</span><span class="sxs-lookup"><span data-stu-id="527df-220">True</span></span>                                                 |
| <span data-ttu-id="527df-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="527df-221">Is Indexed</span></span>             | <span data-ttu-id="527df-222">否</span><span class="sxs-lookup"><span data-stu-id="527df-222">False</span></span>                                                |
| <span data-ttu-id="527df-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="527df-223">In Global Catalog</span></span>      | <span data-ttu-id="527df-224">否</span><span class="sxs-lookup"><span data-stu-id="527df-224">False</span></span>                                                |
| <span data-ttu-id="527df-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="527df-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="527df-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="527df-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="527df-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="527df-227">Range-Lower</span></span>            | <span data-ttu-id="527df-228">1</span><span class="sxs-lookup"><span data-stu-id="527df-228">1</span></span>                                                    |
| <span data-ttu-id="527df-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="527df-229">Range-Upper</span></span>            | <span data-ttu-id="527df-230">1024</span><span class="sxs-lookup"><span data-stu-id="527df-230">1024</span></span>                                                 |
| <span data-ttu-id="527df-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-231">Search-Flags</span></span>           | <span data-ttu-id="527df-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="527df-232">0x00000000</span></span>                                           |
| <span data-ttu-id="527df-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-233">System-Flags</span></span>           | <span data-ttu-id="527df-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="527df-234">0x00000010</span></span>                                           |
| <span data-ttu-id="527df-235">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="527df-235">Classes used in</span></span>        | [<span data-ttu-id="527df-236">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="527df-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="527df-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="527df-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="527df-238">進入</span><span class="sxs-lookup"><span data-stu-id="527df-238">Entry</span></span> | <span data-ttu-id="527df-239">值</span><span class="sxs-lookup"><span data-stu-id="527df-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="527df-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="527df-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="527df-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="527df-241">MAPI-Id</span></span>                | <span data-ttu-id="527df-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="527df-242">0x3004</span></span>                                               |
| <span data-ttu-id="527df-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="527df-243">System-Only</span></span>            | <span data-ttu-id="527df-244">否</span><span class="sxs-lookup"><span data-stu-id="527df-244">False</span></span>                                                |
| <span data-ttu-id="527df-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="527df-245">Is-Single-Valued</span></span>       | <span data-ttu-id="527df-246">對</span><span class="sxs-lookup"><span data-stu-id="527df-246">True</span></span>                                                 |
| <span data-ttu-id="527df-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="527df-247">Is Indexed</span></span>             | <span data-ttu-id="527df-248">否</span><span class="sxs-lookup"><span data-stu-id="527df-248">False</span></span>                                                |
| <span data-ttu-id="527df-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="527df-249">In Global Catalog</span></span>      | <span data-ttu-id="527df-250">否</span><span class="sxs-lookup"><span data-stu-id="527df-250">False</span></span>                                                |
| <span data-ttu-id="527df-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="527df-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="527df-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="527df-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="527df-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="527df-253">Range-Lower</span></span>            | <span data-ttu-id="527df-254">1</span><span class="sxs-lookup"><span data-stu-id="527df-254">1</span></span>                                                    |
| <span data-ttu-id="527df-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="527df-255">Range-Upper</span></span>            | <span data-ttu-id="527df-256">1024</span><span class="sxs-lookup"><span data-stu-id="527df-256">1024</span></span>                                                 |
| <span data-ttu-id="527df-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-257">Search-Flags</span></span>           | <span data-ttu-id="527df-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="527df-258">0x00000000</span></span>                                           |
| <span data-ttu-id="527df-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-259">System-Flags</span></span>           | <span data-ttu-id="527df-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="527df-260">0x00000010</span></span>                                           |
| <span data-ttu-id="527df-261">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="527df-261">Classes used in</span></span>        | [<span data-ttu-id="527df-262">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="527df-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="527df-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="527df-263">Windows Server 2012</span></span>



| <span data-ttu-id="527df-264">進入</span><span class="sxs-lookup"><span data-stu-id="527df-264">Entry</span></span> | <span data-ttu-id="527df-265">值</span><span class="sxs-lookup"><span data-stu-id="527df-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="527df-266">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="527df-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="527df-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="527df-267">MAPI-Id</span></span>                | <span data-ttu-id="527df-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="527df-268">0x3004</span></span>                                               |
| <span data-ttu-id="527df-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="527df-269">System-Only</span></span>            | <span data-ttu-id="527df-270">否</span><span class="sxs-lookup"><span data-stu-id="527df-270">False</span></span>                                                |
| <span data-ttu-id="527df-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="527df-271">Is-Single-Valued</span></span>       | <span data-ttu-id="527df-272">對</span><span class="sxs-lookup"><span data-stu-id="527df-272">True</span></span>                                                 |
| <span data-ttu-id="527df-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="527df-273">Is Indexed</span></span>             | <span data-ttu-id="527df-274">否</span><span class="sxs-lookup"><span data-stu-id="527df-274">False</span></span>                                                |
| <span data-ttu-id="527df-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="527df-275">In Global Catalog</span></span>      | <span data-ttu-id="527df-276">否</span><span class="sxs-lookup"><span data-stu-id="527df-276">False</span></span>                                                |
| <span data-ttu-id="527df-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="527df-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="527df-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="527df-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="527df-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="527df-279">Range-Lower</span></span>            | <span data-ttu-id="527df-280">1</span><span class="sxs-lookup"><span data-stu-id="527df-280">1</span></span>                                                    |
| <span data-ttu-id="527df-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="527df-281">Range-Upper</span></span>            | <span data-ttu-id="527df-282">1024</span><span class="sxs-lookup"><span data-stu-id="527df-282">1024</span></span>                                                 |
| <span data-ttu-id="527df-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-283">Search-Flags</span></span>           | <span data-ttu-id="527df-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="527df-284">0x00000000</span></span>                                           |
| <span data-ttu-id="527df-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="527df-285">System-Flags</span></span>           | <span data-ttu-id="527df-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="527df-286">0x00000010</span></span>                                           |
| <span data-ttu-id="527df-287">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="527df-287">Classes used in</span></span>        | [<span data-ttu-id="527df-288">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="527df-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 






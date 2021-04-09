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
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="037b1-106"> (AD 架構) 的批註屬性</span><span class="sxs-lookup"><span data-stu-id="037b1-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="037b1-107">使用者的批註。</span><span class="sxs-lookup"><span data-stu-id="037b1-107">The user's comments.</span></span> <span data-ttu-id="037b1-108">這個字串可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="037b1-108">This string can be a null string.</span></span>



| <span data-ttu-id="037b1-109">進入</span><span class="sxs-lookup"><span data-stu-id="037b1-109">Entry</span></span> | <span data-ttu-id="037b1-110">值</span><span class="sxs-lookup"><span data-stu-id="037b1-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="037b1-111">CN</span><span class="sxs-lookup"><span data-stu-id="037b1-111">CN</span></span>                | <span data-ttu-id="037b1-112">註解</span><span class="sxs-lookup"><span data-stu-id="037b1-112">Comment</span></span>                                                                  |
| <span data-ttu-id="037b1-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="037b1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="037b1-114">info</span><span class="sxs-lookup"><span data-stu-id="037b1-114">info</span></span>                                                                     |
| <span data-ttu-id="037b1-115">大小</span><span class="sxs-lookup"><span data-stu-id="037b1-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="037b1-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="037b1-116">Update Privilege</span></span>  | <span data-ttu-id="037b1-117">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="037b1-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="037b1-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="037b1-118">Update Frequency</span></span>  | <span data-ttu-id="037b1-119">每次使用者或系統管理員需要在帳戶上新增留言。</span><span class="sxs-lookup"><span data-stu-id="037b1-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="037b1-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="037b1-120">Attribute-Id</span></span>      | <span data-ttu-id="037b1-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="037b1-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="037b1-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="037b1-122">System-Id-Guid</span></span>    | <span data-ttu-id="037b1-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="037b1-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="037b1-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="037b1-124">Syntax</span></span>            | [<span data-ttu-id="037b1-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="037b1-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="037b1-126">實作</span><span class="sxs-lookup"><span data-stu-id="037b1-126">Implementations</span></span>

-   [<span data-ttu-id="037b1-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="037b1-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="037b1-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="037b1-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="037b1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="037b1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="037b1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="037b1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="037b1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="037b1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="037b1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="037b1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="037b1-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="037b1-133">Windows 2000 Server</span></span>



| <span data-ttu-id="037b1-134">進入</span><span class="sxs-lookup"><span data-stu-id="037b1-134">Entry</span></span> | <span data-ttu-id="037b1-135">值</span><span class="sxs-lookup"><span data-stu-id="037b1-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="037b1-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="037b1-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="037b1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="037b1-137">MAPI-Id</span></span>                | <span data-ttu-id="037b1-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="037b1-138">0x3004</span></span>                                               |
| <span data-ttu-id="037b1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="037b1-139">System-Only</span></span>            | <span data-ttu-id="037b1-140">否</span><span class="sxs-lookup"><span data-stu-id="037b1-140">False</span></span>                                                |
| <span data-ttu-id="037b1-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="037b1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="037b1-142">對</span><span class="sxs-lookup"><span data-stu-id="037b1-142">True</span></span>                                                 |
| <span data-ttu-id="037b1-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="037b1-143">Is Indexed</span></span>             | <span data-ttu-id="037b1-144">否</span><span class="sxs-lookup"><span data-stu-id="037b1-144">False</span></span>                                                |
| <span data-ttu-id="037b1-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="037b1-145">In Global Catalog</span></span>      | <span data-ttu-id="037b1-146">否</span><span class="sxs-lookup"><span data-stu-id="037b1-146">False</span></span>                                                |
| <span data-ttu-id="037b1-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="037b1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="037b1-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="037b1-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="037b1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="037b1-149">Range-Lower</span></span>            | <span data-ttu-id="037b1-150">1</span><span class="sxs-lookup"><span data-stu-id="037b1-150">1</span></span>                                                    |
| <span data-ttu-id="037b1-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="037b1-151">Range-Upper</span></span>            | <span data-ttu-id="037b1-152">1024</span><span class="sxs-lookup"><span data-stu-id="037b1-152">1024</span></span>                                                 |
| <span data-ttu-id="037b1-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-153">Search-Flags</span></span>           | <span data-ttu-id="037b1-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="037b1-154">0x00000000</span></span>                                           |
| <span data-ttu-id="037b1-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-155">System-Flags</span></span>           | <span data-ttu-id="037b1-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="037b1-156">0x00000010</span></span>                                           |
| <span data-ttu-id="037b1-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="037b1-157">Classes used in</span></span>        | [<span data-ttu-id="037b1-158">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="037b1-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="037b1-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="037b1-159">Windows Server 2003</span></span>



| <span data-ttu-id="037b1-160">進入</span><span class="sxs-lookup"><span data-stu-id="037b1-160">Entry</span></span> | <span data-ttu-id="037b1-161">值</span><span class="sxs-lookup"><span data-stu-id="037b1-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="037b1-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="037b1-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="037b1-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="037b1-163">MAPI-Id</span></span>                | <span data-ttu-id="037b1-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="037b1-164">0x3004</span></span>                                               |
| <span data-ttu-id="037b1-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="037b1-165">System-Only</span></span>            | <span data-ttu-id="037b1-166">否</span><span class="sxs-lookup"><span data-stu-id="037b1-166">False</span></span>                                                |
| <span data-ttu-id="037b1-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="037b1-167">Is-Single-Valued</span></span>       | <span data-ttu-id="037b1-168">對</span><span class="sxs-lookup"><span data-stu-id="037b1-168">True</span></span>                                                 |
| <span data-ttu-id="037b1-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="037b1-169">Is Indexed</span></span>             | <span data-ttu-id="037b1-170">否</span><span class="sxs-lookup"><span data-stu-id="037b1-170">False</span></span>                                                |
| <span data-ttu-id="037b1-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="037b1-171">In Global Catalog</span></span>      | <span data-ttu-id="037b1-172">否</span><span class="sxs-lookup"><span data-stu-id="037b1-172">False</span></span>                                                |
| <span data-ttu-id="037b1-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="037b1-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="037b1-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="037b1-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="037b1-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="037b1-175">Range-Lower</span></span>            | <span data-ttu-id="037b1-176">1</span><span class="sxs-lookup"><span data-stu-id="037b1-176">1</span></span>                                                    |
| <span data-ttu-id="037b1-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="037b1-177">Range-Upper</span></span>            | <span data-ttu-id="037b1-178">1024</span><span class="sxs-lookup"><span data-stu-id="037b1-178">1024</span></span>                                                 |
| <span data-ttu-id="037b1-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-179">Search-Flags</span></span>           | <span data-ttu-id="037b1-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="037b1-180">0x00000000</span></span>                                           |
| <span data-ttu-id="037b1-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-181">System-Flags</span></span>           | <span data-ttu-id="037b1-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="037b1-182">0x00000010</span></span>                                           |
| <span data-ttu-id="037b1-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="037b1-183">Classes used in</span></span>        | [<span data-ttu-id="037b1-184">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="037b1-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="037b1-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="037b1-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="037b1-186">進入</span><span class="sxs-lookup"><span data-stu-id="037b1-186">Entry</span></span> | <span data-ttu-id="037b1-187">值</span><span class="sxs-lookup"><span data-stu-id="037b1-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="037b1-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="037b1-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="037b1-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="037b1-189">MAPI-Id</span></span>                | <span data-ttu-id="037b1-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="037b1-190">0x3004</span></span>                                               |
| <span data-ttu-id="037b1-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="037b1-191">System-Only</span></span>            | <span data-ttu-id="037b1-192">否</span><span class="sxs-lookup"><span data-stu-id="037b1-192">False</span></span>                                                |
| <span data-ttu-id="037b1-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="037b1-193">Is-Single-Valued</span></span>       | <span data-ttu-id="037b1-194">對</span><span class="sxs-lookup"><span data-stu-id="037b1-194">True</span></span>                                                 |
| <span data-ttu-id="037b1-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="037b1-195">Is Indexed</span></span>             | <span data-ttu-id="037b1-196">否</span><span class="sxs-lookup"><span data-stu-id="037b1-196">False</span></span>                                                |
| <span data-ttu-id="037b1-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="037b1-197">In Global Catalog</span></span>      | <span data-ttu-id="037b1-198">否</span><span class="sxs-lookup"><span data-stu-id="037b1-198">False</span></span>                                                |
| <span data-ttu-id="037b1-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="037b1-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="037b1-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="037b1-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="037b1-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="037b1-201">Range-Lower</span></span>            | <span data-ttu-id="037b1-202">1</span><span class="sxs-lookup"><span data-stu-id="037b1-202">1</span></span>                                                    |
| <span data-ttu-id="037b1-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="037b1-203">Range-Upper</span></span>            | <span data-ttu-id="037b1-204">1024</span><span class="sxs-lookup"><span data-stu-id="037b1-204">1024</span></span>                                                 |
| <span data-ttu-id="037b1-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-205">Search-Flags</span></span>           | <span data-ttu-id="037b1-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="037b1-206">0x00000000</span></span>                                           |
| <span data-ttu-id="037b1-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-207">System-Flags</span></span>           | <span data-ttu-id="037b1-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="037b1-208">0x00000010</span></span>                                           |
| <span data-ttu-id="037b1-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="037b1-209">Classes used in</span></span>        | [<span data-ttu-id="037b1-210">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="037b1-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="037b1-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="037b1-211">Windows Server 2008</span></span>



| <span data-ttu-id="037b1-212">進入</span><span class="sxs-lookup"><span data-stu-id="037b1-212">Entry</span></span> | <span data-ttu-id="037b1-213">值</span><span class="sxs-lookup"><span data-stu-id="037b1-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="037b1-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="037b1-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="037b1-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="037b1-215">MAPI-Id</span></span>                | <span data-ttu-id="037b1-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="037b1-216">0x3004</span></span>                                               |
| <span data-ttu-id="037b1-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="037b1-217">System-Only</span></span>            | <span data-ttu-id="037b1-218">否</span><span class="sxs-lookup"><span data-stu-id="037b1-218">False</span></span>                                                |
| <span data-ttu-id="037b1-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="037b1-219">Is-Single-Valued</span></span>       | <span data-ttu-id="037b1-220">對</span><span class="sxs-lookup"><span data-stu-id="037b1-220">True</span></span>                                                 |
| <span data-ttu-id="037b1-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="037b1-221">Is Indexed</span></span>             | <span data-ttu-id="037b1-222">否</span><span class="sxs-lookup"><span data-stu-id="037b1-222">False</span></span>                                                |
| <span data-ttu-id="037b1-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="037b1-223">In Global Catalog</span></span>      | <span data-ttu-id="037b1-224">否</span><span class="sxs-lookup"><span data-stu-id="037b1-224">False</span></span>                                                |
| <span data-ttu-id="037b1-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="037b1-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="037b1-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="037b1-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="037b1-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="037b1-227">Range-Lower</span></span>            | <span data-ttu-id="037b1-228">1</span><span class="sxs-lookup"><span data-stu-id="037b1-228">1</span></span>                                                    |
| <span data-ttu-id="037b1-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="037b1-229">Range-Upper</span></span>            | <span data-ttu-id="037b1-230">1024</span><span class="sxs-lookup"><span data-stu-id="037b1-230">1024</span></span>                                                 |
| <span data-ttu-id="037b1-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-231">Search-Flags</span></span>           | <span data-ttu-id="037b1-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="037b1-232">0x00000000</span></span>                                           |
| <span data-ttu-id="037b1-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-233">System-Flags</span></span>           | <span data-ttu-id="037b1-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="037b1-234">0x00000010</span></span>                                           |
| <span data-ttu-id="037b1-235">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="037b1-235">Classes used in</span></span>        | [<span data-ttu-id="037b1-236">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="037b1-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="037b1-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="037b1-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="037b1-238">進入</span><span class="sxs-lookup"><span data-stu-id="037b1-238">Entry</span></span> | <span data-ttu-id="037b1-239">值</span><span class="sxs-lookup"><span data-stu-id="037b1-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="037b1-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="037b1-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="037b1-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="037b1-241">MAPI-Id</span></span>                | <span data-ttu-id="037b1-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="037b1-242">0x3004</span></span>                                               |
| <span data-ttu-id="037b1-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="037b1-243">System-Only</span></span>            | <span data-ttu-id="037b1-244">否</span><span class="sxs-lookup"><span data-stu-id="037b1-244">False</span></span>                                                |
| <span data-ttu-id="037b1-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="037b1-245">Is-Single-Valued</span></span>       | <span data-ttu-id="037b1-246">對</span><span class="sxs-lookup"><span data-stu-id="037b1-246">True</span></span>                                                 |
| <span data-ttu-id="037b1-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="037b1-247">Is Indexed</span></span>             | <span data-ttu-id="037b1-248">否</span><span class="sxs-lookup"><span data-stu-id="037b1-248">False</span></span>                                                |
| <span data-ttu-id="037b1-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="037b1-249">In Global Catalog</span></span>      | <span data-ttu-id="037b1-250">否</span><span class="sxs-lookup"><span data-stu-id="037b1-250">False</span></span>                                                |
| <span data-ttu-id="037b1-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="037b1-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="037b1-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="037b1-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="037b1-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="037b1-253">Range-Lower</span></span>            | <span data-ttu-id="037b1-254">1</span><span class="sxs-lookup"><span data-stu-id="037b1-254">1</span></span>                                                    |
| <span data-ttu-id="037b1-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="037b1-255">Range-Upper</span></span>            | <span data-ttu-id="037b1-256">1024</span><span class="sxs-lookup"><span data-stu-id="037b1-256">1024</span></span>                                                 |
| <span data-ttu-id="037b1-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-257">Search-Flags</span></span>           | <span data-ttu-id="037b1-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="037b1-258">0x00000000</span></span>                                           |
| <span data-ttu-id="037b1-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-259">System-Flags</span></span>           | <span data-ttu-id="037b1-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="037b1-260">0x00000010</span></span>                                           |
| <span data-ttu-id="037b1-261">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="037b1-261">Classes used in</span></span>        | [<span data-ttu-id="037b1-262">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="037b1-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="037b1-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="037b1-263">Windows Server 2012</span></span>



| <span data-ttu-id="037b1-264">進入</span><span class="sxs-lookup"><span data-stu-id="037b1-264">Entry</span></span> | <span data-ttu-id="037b1-265">值</span><span class="sxs-lookup"><span data-stu-id="037b1-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="037b1-266">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="037b1-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="037b1-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="037b1-267">MAPI-Id</span></span>                | <span data-ttu-id="037b1-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="037b1-268">0x3004</span></span>                                               |
| <span data-ttu-id="037b1-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="037b1-269">System-Only</span></span>            | <span data-ttu-id="037b1-270">否</span><span class="sxs-lookup"><span data-stu-id="037b1-270">False</span></span>                                                |
| <span data-ttu-id="037b1-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="037b1-271">Is-Single-Valued</span></span>       | <span data-ttu-id="037b1-272">對</span><span class="sxs-lookup"><span data-stu-id="037b1-272">True</span></span>                                                 |
| <span data-ttu-id="037b1-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="037b1-273">Is Indexed</span></span>             | <span data-ttu-id="037b1-274">否</span><span class="sxs-lookup"><span data-stu-id="037b1-274">False</span></span>                                                |
| <span data-ttu-id="037b1-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="037b1-275">In Global Catalog</span></span>      | <span data-ttu-id="037b1-276">否</span><span class="sxs-lookup"><span data-stu-id="037b1-276">False</span></span>                                                |
| <span data-ttu-id="037b1-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="037b1-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="037b1-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="037b1-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="037b1-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="037b1-279">Range-Lower</span></span>            | <span data-ttu-id="037b1-280">1</span><span class="sxs-lookup"><span data-stu-id="037b1-280">1</span></span>                                                    |
| <span data-ttu-id="037b1-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="037b1-281">Range-Upper</span></span>            | <span data-ttu-id="037b1-282">1024</span><span class="sxs-lookup"><span data-stu-id="037b1-282">1024</span></span>                                                 |
| <span data-ttu-id="037b1-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-283">Search-Flags</span></span>           | <span data-ttu-id="037b1-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="037b1-284">0x00000000</span></span>                                           |
| <span data-ttu-id="037b1-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="037b1-285">System-Flags</span></span>           | <span data-ttu-id="037b1-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="037b1-286">0x00000010</span></span>                                           |
| <span data-ttu-id="037b1-287">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="037b1-287">Classes used in</span></span>        | [<span data-ttu-id="037b1-288">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="037b1-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 






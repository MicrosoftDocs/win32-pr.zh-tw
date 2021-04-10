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
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="b2580-106"> (AD 架構) 的批註屬性</span><span class="sxs-lookup"><span data-stu-id="b2580-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="b2580-107">使用者的批註。</span><span class="sxs-lookup"><span data-stu-id="b2580-107">The user's comments.</span></span> <span data-ttu-id="b2580-108">這個字串可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="b2580-108">This string can be a null string.</span></span>



| <span data-ttu-id="b2580-109">進入</span><span class="sxs-lookup"><span data-stu-id="b2580-109">Entry</span></span> | <span data-ttu-id="b2580-110">值</span><span class="sxs-lookup"><span data-stu-id="b2580-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="b2580-111">CN</span><span class="sxs-lookup"><span data-stu-id="b2580-111">CN</span></span>                | <span data-ttu-id="b2580-112">註解</span><span class="sxs-lookup"><span data-stu-id="b2580-112">Comment</span></span>                                                                  |
| <span data-ttu-id="b2580-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b2580-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b2580-114">info</span><span class="sxs-lookup"><span data-stu-id="b2580-114">info</span></span>                                                                     |
| <span data-ttu-id="b2580-115">大小</span><span class="sxs-lookup"><span data-stu-id="b2580-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="b2580-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b2580-116">Update Privilege</span></span>  | <span data-ttu-id="b2580-117">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="b2580-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="b2580-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b2580-118">Update Frequency</span></span>  | <span data-ttu-id="b2580-119">每次使用者或系統管理員需要在帳戶上新增留言。</span><span class="sxs-lookup"><span data-stu-id="b2580-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="b2580-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b2580-120">Attribute-Id</span></span>      | <span data-ttu-id="b2580-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="b2580-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="b2580-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b2580-122">System-Id-Guid</span></span>    | <span data-ttu-id="b2580-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b2580-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="b2580-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2580-124">Syntax</span></span>            | [<span data-ttu-id="b2580-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b2580-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="b2580-126">實作</span><span class="sxs-lookup"><span data-stu-id="b2580-126">Implementations</span></span>

-   [<span data-ttu-id="b2580-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b2580-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b2580-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b2580-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b2580-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b2580-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b2580-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b2580-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b2580-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b2580-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b2580-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b2580-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b2580-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b2580-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b2580-134">進入</span><span class="sxs-lookup"><span data-stu-id="b2580-134">Entry</span></span> | <span data-ttu-id="b2580-135">值</span><span class="sxs-lookup"><span data-stu-id="b2580-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b2580-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2580-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b2580-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2580-137">MAPI-Id</span></span>                | <span data-ttu-id="b2580-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="b2580-138">0x3004</span></span>                                               |
| <span data-ttu-id="b2580-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2580-139">System-Only</span></span>            | <span data-ttu-id="b2580-140">否</span><span class="sxs-lookup"><span data-stu-id="b2580-140">False</span></span>                                                |
| <span data-ttu-id="b2580-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2580-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b2580-142">對</span><span class="sxs-lookup"><span data-stu-id="b2580-142">True</span></span>                                                 |
| <span data-ttu-id="b2580-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2580-143">Is Indexed</span></span>             | <span data-ttu-id="b2580-144">否</span><span class="sxs-lookup"><span data-stu-id="b2580-144">False</span></span>                                                |
| <span data-ttu-id="b2580-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2580-145">In Global Catalog</span></span>      | <span data-ttu-id="b2580-146">否</span><span class="sxs-lookup"><span data-stu-id="b2580-146">False</span></span>                                                |
| <span data-ttu-id="b2580-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2580-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2580-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2580-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b2580-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2580-149">Range-Lower</span></span>            | <span data-ttu-id="b2580-150">1</span><span class="sxs-lookup"><span data-stu-id="b2580-150">1</span></span>                                                    |
| <span data-ttu-id="b2580-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2580-151">Range-Upper</span></span>            | <span data-ttu-id="b2580-152">1024</span><span class="sxs-lookup"><span data-stu-id="b2580-152">1024</span></span>                                                 |
| <span data-ttu-id="b2580-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-153">Search-Flags</span></span>           | <span data-ttu-id="b2580-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2580-154">0x00000000</span></span>                                           |
| <span data-ttu-id="b2580-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-155">System-Flags</span></span>           | <span data-ttu-id="b2580-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2580-156">0x00000010</span></span>                                           |
| <span data-ttu-id="b2580-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2580-157">Classes used in</span></span>        | [<span data-ttu-id="b2580-158">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="b2580-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b2580-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2580-159">Windows Server 2003</span></span>



| <span data-ttu-id="b2580-160">進入</span><span class="sxs-lookup"><span data-stu-id="b2580-160">Entry</span></span> | <span data-ttu-id="b2580-161">值</span><span class="sxs-lookup"><span data-stu-id="b2580-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b2580-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2580-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b2580-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2580-163">MAPI-Id</span></span>                | <span data-ttu-id="b2580-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="b2580-164">0x3004</span></span>                                               |
| <span data-ttu-id="b2580-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2580-165">System-Only</span></span>            | <span data-ttu-id="b2580-166">否</span><span class="sxs-lookup"><span data-stu-id="b2580-166">False</span></span>                                                |
| <span data-ttu-id="b2580-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2580-167">Is-Single-Valued</span></span>       | <span data-ttu-id="b2580-168">對</span><span class="sxs-lookup"><span data-stu-id="b2580-168">True</span></span>                                                 |
| <span data-ttu-id="b2580-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2580-169">Is Indexed</span></span>             | <span data-ttu-id="b2580-170">否</span><span class="sxs-lookup"><span data-stu-id="b2580-170">False</span></span>                                                |
| <span data-ttu-id="b2580-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2580-171">In Global Catalog</span></span>      | <span data-ttu-id="b2580-172">否</span><span class="sxs-lookup"><span data-stu-id="b2580-172">False</span></span>                                                |
| <span data-ttu-id="b2580-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2580-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2580-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2580-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b2580-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2580-175">Range-Lower</span></span>            | <span data-ttu-id="b2580-176">1</span><span class="sxs-lookup"><span data-stu-id="b2580-176">1</span></span>                                                    |
| <span data-ttu-id="b2580-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2580-177">Range-Upper</span></span>            | <span data-ttu-id="b2580-178">1024</span><span class="sxs-lookup"><span data-stu-id="b2580-178">1024</span></span>                                                 |
| <span data-ttu-id="b2580-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-179">Search-Flags</span></span>           | <span data-ttu-id="b2580-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2580-180">0x00000000</span></span>                                           |
| <span data-ttu-id="b2580-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-181">System-Flags</span></span>           | <span data-ttu-id="b2580-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2580-182">0x00000010</span></span>                                           |
| <span data-ttu-id="b2580-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2580-183">Classes used in</span></span>        | [<span data-ttu-id="b2580-184">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="b2580-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b2580-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b2580-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b2580-186">進入</span><span class="sxs-lookup"><span data-stu-id="b2580-186">Entry</span></span> | <span data-ttu-id="b2580-187">值</span><span class="sxs-lookup"><span data-stu-id="b2580-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b2580-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2580-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b2580-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2580-189">MAPI-Id</span></span>                | <span data-ttu-id="b2580-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="b2580-190">0x3004</span></span>                                               |
| <span data-ttu-id="b2580-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2580-191">System-Only</span></span>            | <span data-ttu-id="b2580-192">否</span><span class="sxs-lookup"><span data-stu-id="b2580-192">False</span></span>                                                |
| <span data-ttu-id="b2580-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2580-193">Is-Single-Valued</span></span>       | <span data-ttu-id="b2580-194">對</span><span class="sxs-lookup"><span data-stu-id="b2580-194">True</span></span>                                                 |
| <span data-ttu-id="b2580-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2580-195">Is Indexed</span></span>             | <span data-ttu-id="b2580-196">否</span><span class="sxs-lookup"><span data-stu-id="b2580-196">False</span></span>                                                |
| <span data-ttu-id="b2580-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2580-197">In Global Catalog</span></span>      | <span data-ttu-id="b2580-198">否</span><span class="sxs-lookup"><span data-stu-id="b2580-198">False</span></span>                                                |
| <span data-ttu-id="b2580-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2580-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2580-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2580-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b2580-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2580-201">Range-Lower</span></span>            | <span data-ttu-id="b2580-202">1</span><span class="sxs-lookup"><span data-stu-id="b2580-202">1</span></span>                                                    |
| <span data-ttu-id="b2580-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2580-203">Range-Upper</span></span>            | <span data-ttu-id="b2580-204">1024</span><span class="sxs-lookup"><span data-stu-id="b2580-204">1024</span></span>                                                 |
| <span data-ttu-id="b2580-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-205">Search-Flags</span></span>           | <span data-ttu-id="b2580-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2580-206">0x00000000</span></span>                                           |
| <span data-ttu-id="b2580-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-207">System-Flags</span></span>           | <span data-ttu-id="b2580-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2580-208">0x00000010</span></span>                                           |
| <span data-ttu-id="b2580-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2580-209">Classes used in</span></span>        | [<span data-ttu-id="b2580-210">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="b2580-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b2580-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2580-211">Windows Server 2008</span></span>



| <span data-ttu-id="b2580-212">進入</span><span class="sxs-lookup"><span data-stu-id="b2580-212">Entry</span></span> | <span data-ttu-id="b2580-213">值</span><span class="sxs-lookup"><span data-stu-id="b2580-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b2580-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2580-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b2580-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2580-215">MAPI-Id</span></span>                | <span data-ttu-id="b2580-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="b2580-216">0x3004</span></span>                                               |
| <span data-ttu-id="b2580-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2580-217">System-Only</span></span>            | <span data-ttu-id="b2580-218">否</span><span class="sxs-lookup"><span data-stu-id="b2580-218">False</span></span>                                                |
| <span data-ttu-id="b2580-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2580-219">Is-Single-Valued</span></span>       | <span data-ttu-id="b2580-220">對</span><span class="sxs-lookup"><span data-stu-id="b2580-220">True</span></span>                                                 |
| <span data-ttu-id="b2580-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2580-221">Is Indexed</span></span>             | <span data-ttu-id="b2580-222">否</span><span class="sxs-lookup"><span data-stu-id="b2580-222">False</span></span>                                                |
| <span data-ttu-id="b2580-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2580-223">In Global Catalog</span></span>      | <span data-ttu-id="b2580-224">否</span><span class="sxs-lookup"><span data-stu-id="b2580-224">False</span></span>                                                |
| <span data-ttu-id="b2580-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2580-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2580-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2580-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b2580-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2580-227">Range-Lower</span></span>            | <span data-ttu-id="b2580-228">1</span><span class="sxs-lookup"><span data-stu-id="b2580-228">1</span></span>                                                    |
| <span data-ttu-id="b2580-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2580-229">Range-Upper</span></span>            | <span data-ttu-id="b2580-230">1024</span><span class="sxs-lookup"><span data-stu-id="b2580-230">1024</span></span>                                                 |
| <span data-ttu-id="b2580-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-231">Search-Flags</span></span>           | <span data-ttu-id="b2580-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2580-232">0x00000000</span></span>                                           |
| <span data-ttu-id="b2580-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-233">System-Flags</span></span>           | <span data-ttu-id="b2580-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2580-234">0x00000010</span></span>                                           |
| <span data-ttu-id="b2580-235">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2580-235">Classes used in</span></span>        | [<span data-ttu-id="b2580-236">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="b2580-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b2580-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2580-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b2580-238">進入</span><span class="sxs-lookup"><span data-stu-id="b2580-238">Entry</span></span> | <span data-ttu-id="b2580-239">值</span><span class="sxs-lookup"><span data-stu-id="b2580-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b2580-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2580-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b2580-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2580-241">MAPI-Id</span></span>                | <span data-ttu-id="b2580-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="b2580-242">0x3004</span></span>                                               |
| <span data-ttu-id="b2580-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2580-243">System-Only</span></span>            | <span data-ttu-id="b2580-244">否</span><span class="sxs-lookup"><span data-stu-id="b2580-244">False</span></span>                                                |
| <span data-ttu-id="b2580-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2580-245">Is-Single-Valued</span></span>       | <span data-ttu-id="b2580-246">對</span><span class="sxs-lookup"><span data-stu-id="b2580-246">True</span></span>                                                 |
| <span data-ttu-id="b2580-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2580-247">Is Indexed</span></span>             | <span data-ttu-id="b2580-248">否</span><span class="sxs-lookup"><span data-stu-id="b2580-248">False</span></span>                                                |
| <span data-ttu-id="b2580-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2580-249">In Global Catalog</span></span>      | <span data-ttu-id="b2580-250">否</span><span class="sxs-lookup"><span data-stu-id="b2580-250">False</span></span>                                                |
| <span data-ttu-id="b2580-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2580-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2580-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2580-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b2580-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2580-253">Range-Lower</span></span>            | <span data-ttu-id="b2580-254">1</span><span class="sxs-lookup"><span data-stu-id="b2580-254">1</span></span>                                                    |
| <span data-ttu-id="b2580-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2580-255">Range-Upper</span></span>            | <span data-ttu-id="b2580-256">1024</span><span class="sxs-lookup"><span data-stu-id="b2580-256">1024</span></span>                                                 |
| <span data-ttu-id="b2580-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-257">Search-Flags</span></span>           | <span data-ttu-id="b2580-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2580-258">0x00000000</span></span>                                           |
| <span data-ttu-id="b2580-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-259">System-Flags</span></span>           | <span data-ttu-id="b2580-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2580-260">0x00000010</span></span>                                           |
| <span data-ttu-id="b2580-261">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2580-261">Classes used in</span></span>        | [<span data-ttu-id="b2580-262">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="b2580-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b2580-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2580-263">Windows Server 2012</span></span>



| <span data-ttu-id="b2580-264">進入</span><span class="sxs-lookup"><span data-stu-id="b2580-264">Entry</span></span> | <span data-ttu-id="b2580-265">值</span><span class="sxs-lookup"><span data-stu-id="b2580-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b2580-266">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2580-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b2580-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2580-267">MAPI-Id</span></span>                | <span data-ttu-id="b2580-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="b2580-268">0x3004</span></span>                                               |
| <span data-ttu-id="b2580-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2580-269">System-Only</span></span>            | <span data-ttu-id="b2580-270">否</span><span class="sxs-lookup"><span data-stu-id="b2580-270">False</span></span>                                                |
| <span data-ttu-id="b2580-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2580-271">Is-Single-Valued</span></span>       | <span data-ttu-id="b2580-272">對</span><span class="sxs-lookup"><span data-stu-id="b2580-272">True</span></span>                                                 |
| <span data-ttu-id="b2580-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2580-273">Is Indexed</span></span>             | <span data-ttu-id="b2580-274">否</span><span class="sxs-lookup"><span data-stu-id="b2580-274">False</span></span>                                                |
| <span data-ttu-id="b2580-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2580-275">In Global Catalog</span></span>      | <span data-ttu-id="b2580-276">否</span><span class="sxs-lookup"><span data-stu-id="b2580-276">False</span></span>                                                |
| <span data-ttu-id="b2580-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2580-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2580-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2580-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b2580-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2580-279">Range-Lower</span></span>            | <span data-ttu-id="b2580-280">1</span><span class="sxs-lookup"><span data-stu-id="b2580-280">1</span></span>                                                    |
| <span data-ttu-id="b2580-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2580-281">Range-Upper</span></span>            | <span data-ttu-id="b2580-282">1024</span><span class="sxs-lookup"><span data-stu-id="b2580-282">1024</span></span>                                                 |
| <span data-ttu-id="b2580-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-283">Search-Flags</span></span>           | <span data-ttu-id="b2580-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2580-284">0x00000000</span></span>                                           |
| <span data-ttu-id="b2580-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2580-285">System-Flags</span></span>           | <span data-ttu-id="b2580-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2580-286">0x00000010</span></span>                                           |
| <span data-ttu-id="b2580-287">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2580-287">Classes used in</span></span>        | [<span data-ttu-id="b2580-288">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="b2580-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 






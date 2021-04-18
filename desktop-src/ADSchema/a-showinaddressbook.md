---
title: 顯示通訊錄屬性
description: 這個屬性是用來指出物件將出現在哪些 MAPI 通訊錄中。
ms.assetid: de00da4d-7c04-4d1d-b375-ce3b5eb2f50f
ms.tgt_platform: multiple
keywords:
- 顯示位址-書籍屬性 AD 架構
- showInAddressBook 屬性 AD 架構
topic_type:
- apiref
api_name:
- Show-In-Address-Book
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44632604c539278c67e9dd46537d8e797e2d70d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467242"
---
# <a name="show-in-address-book-attribute"></a><span data-ttu-id="34004-105">顯示通訊錄屬性</span><span class="sxs-lookup"><span data-stu-id="34004-105">Show-In-Address-Book attribute</span></span>

<span data-ttu-id="34004-106">這個屬性是用來指出物件將出現在哪些 MAPI 通訊錄中。</span><span class="sxs-lookup"><span data-stu-id="34004-106">This attribute is used to indicate in which MAPI address books an object will appear.</span></span> <span data-ttu-id="34004-107">它通常是由 Exchange 收件者更新服務維護。</span><span class="sxs-lookup"><span data-stu-id="34004-107">It is usually maintained by the Exchange Recipient Update Service.</span></span>



| <span data-ttu-id="34004-108">進入</span><span class="sxs-lookup"><span data-stu-id="34004-108">Entry</span></span> | <span data-ttu-id="34004-109">值</span><span class="sxs-lookup"><span data-stu-id="34004-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="34004-110">CN</span><span class="sxs-lookup"><span data-stu-id="34004-110">CN</span></span>                | <span data-ttu-id="34004-111">顯示位址-書籍</span><span class="sxs-lookup"><span data-stu-id="34004-111">Show-In-Address-Book</span></span>                    |
| <span data-ttu-id="34004-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="34004-112">Ldap-Display-Name</span></span> | <span data-ttu-id="34004-113">showInAddressBook</span><span class="sxs-lookup"><span data-stu-id="34004-113">showInAddressBook</span></span>                       |
| <span data-ttu-id="34004-114">大小</span><span class="sxs-lookup"><span data-stu-id="34004-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="34004-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="34004-115">Update Privilege</span></span>  | <span data-ttu-id="34004-116">系統會使用此方法。</span><span class="sxs-lookup"><span data-stu-id="34004-116">This is used by the system.</span></span>             |
| <span data-ttu-id="34004-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="34004-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="34004-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="34004-118">Attribute-Id</span></span>      | <span data-ttu-id="34004-119">1.2.840.113556.1.4.644</span><span class="sxs-lookup"><span data-stu-id="34004-119">1.2.840.113556.1.4.644</span></span>                  |
| <span data-ttu-id="34004-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="34004-120">System-Id-Guid</span></span>    | <span data-ttu-id="34004-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="34004-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="34004-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="34004-122">Syntax</span></span>            | [<span data-ttu-id="34004-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="34004-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="34004-124">實作</span><span class="sxs-lookup"><span data-stu-id="34004-124">Implementations</span></span>

-   [<span data-ttu-id="34004-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="34004-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="34004-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="34004-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="34004-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="34004-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="34004-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="34004-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="34004-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="34004-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="34004-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="34004-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="34004-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="34004-131">Windows 2000 Server</span></span>



| <span data-ttu-id="34004-132">進入</span><span class="sxs-lookup"><span data-stu-id="34004-132">Entry</span></span> | <span data-ttu-id="34004-133">值</span><span class="sxs-lookup"><span data-stu-id="34004-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="34004-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34004-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34004-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="34004-136">System-Only</span></span>            | <span data-ttu-id="34004-137">否</span><span class="sxs-lookup"><span data-stu-id="34004-137">False</span></span>                                                |
| <span data-ttu-id="34004-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34004-138">Is-Single-Valued</span></span>       | <span data-ttu-id="34004-139">否</span><span class="sxs-lookup"><span data-stu-id="34004-139">False</span></span>                                                |
| <span data-ttu-id="34004-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34004-140">Is Indexed</span></span>             | <span data-ttu-id="34004-141">否</span><span class="sxs-lookup"><span data-stu-id="34004-141">False</span></span>                                                |
| <span data-ttu-id="34004-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34004-142">In Global Catalog</span></span>      | <span data-ttu-id="34004-143">否</span><span class="sxs-lookup"><span data-stu-id="34004-143">False</span></span>                                                |
| <span data-ttu-id="34004-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34004-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="34004-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34004-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="34004-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34004-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="34004-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34004-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="34004-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-148">Search-Flags</span></span>           | <span data-ttu-id="34004-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-149">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-150">System-Flags</span></span>           | <span data-ttu-id="34004-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-151">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34004-152">Classes used in</span></span>        | [<span data-ttu-id="34004-153">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="34004-153">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="34004-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34004-154">Windows Server 2003</span></span>



| <span data-ttu-id="34004-155">進入</span><span class="sxs-lookup"><span data-stu-id="34004-155">Entry</span></span> | <span data-ttu-id="34004-156">值</span><span class="sxs-lookup"><span data-stu-id="34004-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="34004-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34004-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34004-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="34004-159">System-Only</span></span>            | <span data-ttu-id="34004-160">否</span><span class="sxs-lookup"><span data-stu-id="34004-160">False</span></span>                                                |
| <span data-ttu-id="34004-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34004-161">Is-Single-Valued</span></span>       | <span data-ttu-id="34004-162">否</span><span class="sxs-lookup"><span data-stu-id="34004-162">False</span></span>                                                |
| <span data-ttu-id="34004-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34004-163">Is Indexed</span></span>             | <span data-ttu-id="34004-164">否</span><span class="sxs-lookup"><span data-stu-id="34004-164">False</span></span>                                                |
| <span data-ttu-id="34004-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34004-165">In Global Catalog</span></span>      | <span data-ttu-id="34004-166">否</span><span class="sxs-lookup"><span data-stu-id="34004-166">False</span></span>                                                |
| <span data-ttu-id="34004-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34004-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="34004-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34004-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="34004-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34004-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="34004-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34004-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="34004-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-171">Search-Flags</span></span>           | <span data-ttu-id="34004-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-172">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-173">System-Flags</span></span>           | <span data-ttu-id="34004-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-174">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34004-175">Classes used in</span></span>        | [<span data-ttu-id="34004-176">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="34004-176">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="34004-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="34004-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="34004-178">進入</span><span class="sxs-lookup"><span data-stu-id="34004-178">Entry</span></span> | <span data-ttu-id="34004-179">值</span><span class="sxs-lookup"><span data-stu-id="34004-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="34004-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34004-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34004-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="34004-182">System-Only</span></span>            | <span data-ttu-id="34004-183">否</span><span class="sxs-lookup"><span data-stu-id="34004-183">False</span></span>                                                |
| <span data-ttu-id="34004-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34004-184">Is-Single-Valued</span></span>       | <span data-ttu-id="34004-185">否</span><span class="sxs-lookup"><span data-stu-id="34004-185">False</span></span>                                                |
| <span data-ttu-id="34004-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34004-186">Is Indexed</span></span>             | <span data-ttu-id="34004-187">否</span><span class="sxs-lookup"><span data-stu-id="34004-187">False</span></span>                                                |
| <span data-ttu-id="34004-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34004-188">In Global Catalog</span></span>      | <span data-ttu-id="34004-189">否</span><span class="sxs-lookup"><span data-stu-id="34004-189">False</span></span>                                                |
| <span data-ttu-id="34004-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34004-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="34004-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34004-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="34004-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34004-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="34004-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34004-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="34004-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-194">Search-Flags</span></span>           | <span data-ttu-id="34004-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-195">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-196">System-Flags</span></span>           | <span data-ttu-id="34004-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-197">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34004-198">Classes used in</span></span>        | [<span data-ttu-id="34004-199">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="34004-199">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="34004-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34004-200">Windows Server 2008</span></span>



| <span data-ttu-id="34004-201">進入</span><span class="sxs-lookup"><span data-stu-id="34004-201">Entry</span></span> | <span data-ttu-id="34004-202">值</span><span class="sxs-lookup"><span data-stu-id="34004-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="34004-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34004-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34004-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="34004-205">System-Only</span></span>            | <span data-ttu-id="34004-206">否</span><span class="sxs-lookup"><span data-stu-id="34004-206">False</span></span>                                                |
| <span data-ttu-id="34004-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34004-207">Is-Single-Valued</span></span>       | <span data-ttu-id="34004-208">否</span><span class="sxs-lookup"><span data-stu-id="34004-208">False</span></span>                                                |
| <span data-ttu-id="34004-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34004-209">Is Indexed</span></span>             | <span data-ttu-id="34004-210">否</span><span class="sxs-lookup"><span data-stu-id="34004-210">False</span></span>                                                |
| <span data-ttu-id="34004-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34004-211">In Global Catalog</span></span>      | <span data-ttu-id="34004-212">否</span><span class="sxs-lookup"><span data-stu-id="34004-212">False</span></span>                                                |
| <span data-ttu-id="34004-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34004-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="34004-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34004-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="34004-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34004-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="34004-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34004-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="34004-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-217">Search-Flags</span></span>           | <span data-ttu-id="34004-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-218">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-219">System-Flags</span></span>           | <span data-ttu-id="34004-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-220">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34004-221">Classes used in</span></span>        | [<span data-ttu-id="34004-222">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="34004-222">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="34004-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="34004-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="34004-224">進入</span><span class="sxs-lookup"><span data-stu-id="34004-224">Entry</span></span> | <span data-ttu-id="34004-225">值</span><span class="sxs-lookup"><span data-stu-id="34004-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="34004-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34004-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34004-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="34004-228">System-Only</span></span>            | <span data-ttu-id="34004-229">否</span><span class="sxs-lookup"><span data-stu-id="34004-229">False</span></span>                                                |
| <span data-ttu-id="34004-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34004-230">Is-Single-Valued</span></span>       | <span data-ttu-id="34004-231">否</span><span class="sxs-lookup"><span data-stu-id="34004-231">False</span></span>                                                |
| <span data-ttu-id="34004-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34004-232">Is Indexed</span></span>             | <span data-ttu-id="34004-233">否</span><span class="sxs-lookup"><span data-stu-id="34004-233">False</span></span>                                                |
| <span data-ttu-id="34004-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34004-234">In Global Catalog</span></span>      | <span data-ttu-id="34004-235">否</span><span class="sxs-lookup"><span data-stu-id="34004-235">False</span></span>                                                |
| <span data-ttu-id="34004-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34004-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="34004-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34004-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="34004-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34004-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="34004-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34004-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="34004-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-240">Search-Flags</span></span>           | <span data-ttu-id="34004-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-241">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-242">System-Flags</span></span>           | <span data-ttu-id="34004-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-243">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34004-244">Classes used in</span></span>        | [<span data-ttu-id="34004-245">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="34004-245">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="34004-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="34004-246">Windows Server 2012</span></span>



| <span data-ttu-id="34004-247">進入</span><span class="sxs-lookup"><span data-stu-id="34004-247">Entry</span></span> | <span data-ttu-id="34004-248">值</span><span class="sxs-lookup"><span data-stu-id="34004-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="34004-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34004-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34004-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="34004-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="34004-251">System-Only</span></span>            | <span data-ttu-id="34004-252">否</span><span class="sxs-lookup"><span data-stu-id="34004-252">False</span></span>                                                |
| <span data-ttu-id="34004-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34004-253">Is-Single-Valued</span></span>       | <span data-ttu-id="34004-254">否</span><span class="sxs-lookup"><span data-stu-id="34004-254">False</span></span>                                                |
| <span data-ttu-id="34004-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34004-255">Is Indexed</span></span>             | <span data-ttu-id="34004-256">否</span><span class="sxs-lookup"><span data-stu-id="34004-256">False</span></span>                                                |
| <span data-ttu-id="34004-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34004-257">In Global Catalog</span></span>      | <span data-ttu-id="34004-258">否</span><span class="sxs-lookup"><span data-stu-id="34004-258">False</span></span>                                                |
| <span data-ttu-id="34004-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34004-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="34004-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34004-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="34004-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34004-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="34004-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34004-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="34004-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-263">Search-Flags</span></span>           | <span data-ttu-id="34004-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-264">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34004-265">System-Flags</span></span>           | <span data-ttu-id="34004-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34004-266">0x00000010</span></span>                                           |
| <span data-ttu-id="34004-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34004-267">Classes used in</span></span>        | [<span data-ttu-id="34004-268">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="34004-268">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 






---
title: MSMQ-收件者-Msmq.formatname 屬性
description: 當做 MSMQ 自訂收件者類別中的收件者格式名稱使用。
ms.assetid: 26ee4cec-4e69-412e-914b-437f2f4cd88e
ms.tgt_platform: multiple
keywords:
- MSMQ-收件者-Msmq.formatname 屬性 AD 架構
- msMQ-收件者-Msmq.formatname 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Recipient-FormatName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57fbeee49ddf0c734212bc91926e5c848a9e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108100"
---
# <a name="msmq-recipient-formatname-attribute"></a><span data-ttu-id="88a08-105">MSMQ-收件者-Msmq.formatname 屬性</span><span class="sxs-lookup"><span data-stu-id="88a08-105">MSMQ-Recipient-FormatName attribute</span></span>

<span data-ttu-id="88a08-106">當做 MSMQ 自訂收件者類別中的收件者格式名稱使用。</span><span class="sxs-lookup"><span data-stu-id="88a08-106">Used as the recipient format name in the MSMQ-Custom-Recipient class.</span></span>



| <span data-ttu-id="88a08-107">進入</span><span class="sxs-lookup"><span data-stu-id="88a08-107">Entry</span></span> | <span data-ttu-id="88a08-108">值</span><span class="sxs-lookup"><span data-stu-id="88a08-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="88a08-109">CN</span><span class="sxs-lookup"><span data-stu-id="88a08-109">CN</span></span>                | <span data-ttu-id="88a08-110">MSMQ-收件者-Msmq.formatname</span><span class="sxs-lookup"><span data-stu-id="88a08-110">MSMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="88a08-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="88a08-111">Ldap-Display-Name</span></span> | <span data-ttu-id="88a08-112">msMQ-收件者-Msmq.formatname</span><span class="sxs-lookup"><span data-stu-id="88a08-112">msMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="88a08-113">大小</span><span class="sxs-lookup"><span data-stu-id="88a08-113">Size</span></span>              | <span data-ttu-id="88a08-114">1到255個字元。</span><span class="sxs-lookup"><span data-stu-id="88a08-114">1 to 255 characters.</span></span>                        |
| <span data-ttu-id="88a08-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="88a08-115">Update Privilege</span></span>  | <span data-ttu-id="88a08-116">佇列擁有者。</span><span class="sxs-lookup"><span data-stu-id="88a08-116">The queue owner.</span></span>                            |
| <span data-ttu-id="88a08-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="88a08-117">Update Frequency</span></span>  | <span data-ttu-id="88a08-118">只有在移動外部佇列之後。</span><span class="sxs-lookup"><span data-stu-id="88a08-118">Only after the external queue was moved.</span></span>    |
| <span data-ttu-id="88a08-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88a08-119">Attribute-Id</span></span>      | <span data-ttu-id="88a08-120">1.2.840.113556.1.4.1695</span><span class="sxs-lookup"><span data-stu-id="88a08-120">1.2.840.113556.1.4.1695</span></span>                     |
| <span data-ttu-id="88a08-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="88a08-121">System-Id-Guid</span></span>    | <span data-ttu-id="88a08-122">3bfe6748-b544-485a-b067-1b310c4334bf</span><span class="sxs-lookup"><span data-stu-id="88a08-122">3bfe6748-b544-485a-b067-1b310c4334bf</span></span>        |
| <span data-ttu-id="88a08-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="88a08-123">Syntax</span></span>            | [<span data-ttu-id="88a08-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="88a08-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="88a08-125">實作</span><span class="sxs-lookup"><span data-stu-id="88a08-125">Implementations</span></span>

-   [<span data-ttu-id="88a08-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="88a08-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="88a08-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="88a08-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="88a08-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88a08-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88a08-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88a08-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88a08-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88a08-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="88a08-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88a08-131">Windows Server 2003</span></span>



| <span data-ttu-id="88a08-132">進入</span><span class="sxs-lookup"><span data-stu-id="88a08-132">Entry</span></span> | <span data-ttu-id="88a08-133">值</span><span class="sxs-lookup"><span data-stu-id="88a08-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88a08-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88a08-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a08-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a08-136">System-Only</span></span>            | <span data-ttu-id="88a08-137">否</span><span class="sxs-lookup"><span data-stu-id="88a08-137">False</span></span>                                                               |
| <span data-ttu-id="88a08-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88a08-138">Is-Single-Valued</span></span>       | <span data-ttu-id="88a08-139">對</span><span class="sxs-lookup"><span data-stu-id="88a08-139">True</span></span>                                                                |
| <span data-ttu-id="88a08-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88a08-140">Is Indexed</span></span>             | <span data-ttu-id="88a08-141">否</span><span class="sxs-lookup"><span data-stu-id="88a08-141">False</span></span>                                                               |
| <span data-ttu-id="88a08-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88a08-142">In Global Catalog</span></span>      | <span data-ttu-id="88a08-143">否</span><span class="sxs-lookup"><span data-stu-id="88a08-143">False</span></span>                                                               |
| <span data-ttu-id="88a08-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88a08-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a08-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88a08-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88a08-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a08-146">Range-Lower</span></span>            | <span data-ttu-id="88a08-147">1</span><span class="sxs-lookup"><span data-stu-id="88a08-147">1</span></span>                                                                   |
| <span data-ttu-id="88a08-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a08-148">Range-Upper</span></span>            | <span data-ttu-id="88a08-149">255</span><span class="sxs-lookup"><span data-stu-id="88a08-149">255</span></span>                                                                 |
| <span data-ttu-id="88a08-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-150">Search-Flags</span></span>           | <span data-ttu-id="88a08-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a08-151">0x00000000</span></span>                                                          |
| <span data-ttu-id="88a08-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-152">System-Flags</span></span>           | <span data-ttu-id="88a08-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a08-153">0x00000010</span></span>                                                          |
| <span data-ttu-id="88a08-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88a08-154">Classes used in</span></span>        | [<span data-ttu-id="88a08-155">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="88a08-155">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="88a08-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="88a08-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="88a08-157">進入</span><span class="sxs-lookup"><span data-stu-id="88a08-157">Entry</span></span> | <span data-ttu-id="88a08-158">值</span><span class="sxs-lookup"><span data-stu-id="88a08-158">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88a08-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88a08-159">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a08-160">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a08-161">System-Only</span></span>            | <span data-ttu-id="88a08-162">否</span><span class="sxs-lookup"><span data-stu-id="88a08-162">False</span></span>                                                               |
| <span data-ttu-id="88a08-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88a08-163">Is-Single-Valued</span></span>       | <span data-ttu-id="88a08-164">對</span><span class="sxs-lookup"><span data-stu-id="88a08-164">True</span></span>                                                                |
| <span data-ttu-id="88a08-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88a08-165">Is Indexed</span></span>             | <span data-ttu-id="88a08-166">否</span><span class="sxs-lookup"><span data-stu-id="88a08-166">False</span></span>                                                               |
| <span data-ttu-id="88a08-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88a08-167">In Global Catalog</span></span>      | <span data-ttu-id="88a08-168">否</span><span class="sxs-lookup"><span data-stu-id="88a08-168">False</span></span>                                                               |
| <span data-ttu-id="88a08-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88a08-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a08-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88a08-170">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88a08-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a08-171">Range-Lower</span></span>            | <span data-ttu-id="88a08-172">1</span><span class="sxs-lookup"><span data-stu-id="88a08-172">1</span></span>                                                                   |
| <span data-ttu-id="88a08-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a08-173">Range-Upper</span></span>            | <span data-ttu-id="88a08-174">255</span><span class="sxs-lookup"><span data-stu-id="88a08-174">255</span></span>                                                                 |
| <span data-ttu-id="88a08-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-175">Search-Flags</span></span>           | <span data-ttu-id="88a08-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a08-176">0x00000000</span></span>                                                          |
| <span data-ttu-id="88a08-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-177">System-Flags</span></span>           | <span data-ttu-id="88a08-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a08-178">0x00000010</span></span>                                                          |
| <span data-ttu-id="88a08-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88a08-179">Classes used in</span></span>        | [<span data-ttu-id="88a08-180">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="88a08-180">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="88a08-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88a08-181">Windows Server 2008</span></span>



| <span data-ttu-id="88a08-182">進入</span><span class="sxs-lookup"><span data-stu-id="88a08-182">Entry</span></span> | <span data-ttu-id="88a08-183">值</span><span class="sxs-lookup"><span data-stu-id="88a08-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88a08-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88a08-184">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a08-185">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a08-186">System-Only</span></span>            | <span data-ttu-id="88a08-187">否</span><span class="sxs-lookup"><span data-stu-id="88a08-187">False</span></span>                                                               |
| <span data-ttu-id="88a08-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88a08-188">Is-Single-Valued</span></span>       | <span data-ttu-id="88a08-189">對</span><span class="sxs-lookup"><span data-stu-id="88a08-189">True</span></span>                                                                |
| <span data-ttu-id="88a08-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88a08-190">Is Indexed</span></span>             | <span data-ttu-id="88a08-191">否</span><span class="sxs-lookup"><span data-stu-id="88a08-191">False</span></span>                                                               |
| <span data-ttu-id="88a08-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88a08-192">In Global Catalog</span></span>      | <span data-ttu-id="88a08-193">否</span><span class="sxs-lookup"><span data-stu-id="88a08-193">False</span></span>                                                               |
| <span data-ttu-id="88a08-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88a08-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a08-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88a08-195">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88a08-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a08-196">Range-Lower</span></span>            | <span data-ttu-id="88a08-197">1</span><span class="sxs-lookup"><span data-stu-id="88a08-197">1</span></span>                                                                   |
| <span data-ttu-id="88a08-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a08-198">Range-Upper</span></span>            | <span data-ttu-id="88a08-199">255</span><span class="sxs-lookup"><span data-stu-id="88a08-199">255</span></span>                                                                 |
| <span data-ttu-id="88a08-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-200">Search-Flags</span></span>           | <span data-ttu-id="88a08-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a08-201">0x00000000</span></span>                                                          |
| <span data-ttu-id="88a08-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-202">System-Flags</span></span>           | <span data-ttu-id="88a08-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a08-203">0x00000010</span></span>                                                          |
| <span data-ttu-id="88a08-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88a08-204">Classes used in</span></span>        | [<span data-ttu-id="88a08-205">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="88a08-205">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88a08-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88a08-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88a08-207">進入</span><span class="sxs-lookup"><span data-stu-id="88a08-207">Entry</span></span> | <span data-ttu-id="88a08-208">值</span><span class="sxs-lookup"><span data-stu-id="88a08-208">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88a08-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88a08-209">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a08-210">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a08-211">System-Only</span></span>            | <span data-ttu-id="88a08-212">否</span><span class="sxs-lookup"><span data-stu-id="88a08-212">False</span></span>                                                               |
| <span data-ttu-id="88a08-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88a08-213">Is-Single-Valued</span></span>       | <span data-ttu-id="88a08-214">對</span><span class="sxs-lookup"><span data-stu-id="88a08-214">True</span></span>                                                                |
| <span data-ttu-id="88a08-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88a08-215">Is Indexed</span></span>             | <span data-ttu-id="88a08-216">否</span><span class="sxs-lookup"><span data-stu-id="88a08-216">False</span></span>                                                               |
| <span data-ttu-id="88a08-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88a08-217">In Global Catalog</span></span>      | <span data-ttu-id="88a08-218">否</span><span class="sxs-lookup"><span data-stu-id="88a08-218">False</span></span>                                                               |
| <span data-ttu-id="88a08-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88a08-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a08-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88a08-220">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88a08-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a08-221">Range-Lower</span></span>            | <span data-ttu-id="88a08-222">1</span><span class="sxs-lookup"><span data-stu-id="88a08-222">1</span></span>                                                                   |
| <span data-ttu-id="88a08-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a08-223">Range-Upper</span></span>            | <span data-ttu-id="88a08-224">255</span><span class="sxs-lookup"><span data-stu-id="88a08-224">255</span></span>                                                                 |
| <span data-ttu-id="88a08-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-225">Search-Flags</span></span>           | <span data-ttu-id="88a08-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a08-226">0x00000000</span></span>                                                          |
| <span data-ttu-id="88a08-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-227">System-Flags</span></span>           | <span data-ttu-id="88a08-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a08-228">0x00000010</span></span>                                                          |
| <span data-ttu-id="88a08-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88a08-229">Classes used in</span></span>        | [<span data-ttu-id="88a08-230">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="88a08-230">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88a08-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88a08-231">Windows Server 2012</span></span>



| <span data-ttu-id="88a08-232">進入</span><span class="sxs-lookup"><span data-stu-id="88a08-232">Entry</span></span> | <span data-ttu-id="88a08-233">值</span><span class="sxs-lookup"><span data-stu-id="88a08-233">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="88a08-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88a08-234">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a08-235">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="88a08-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a08-236">System-Only</span></span>            | <span data-ttu-id="88a08-237">否</span><span class="sxs-lookup"><span data-stu-id="88a08-237">False</span></span>                                                               |
| <span data-ttu-id="88a08-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88a08-238">Is-Single-Valued</span></span>       | <span data-ttu-id="88a08-239">對</span><span class="sxs-lookup"><span data-stu-id="88a08-239">True</span></span>                                                                |
| <span data-ttu-id="88a08-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88a08-240">Is Indexed</span></span>             | <span data-ttu-id="88a08-241">否</span><span class="sxs-lookup"><span data-stu-id="88a08-241">False</span></span>                                                               |
| <span data-ttu-id="88a08-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88a08-242">In Global Catalog</span></span>      | <span data-ttu-id="88a08-243">否</span><span class="sxs-lookup"><span data-stu-id="88a08-243">False</span></span>                                                               |
| <span data-ttu-id="88a08-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88a08-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a08-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88a08-245">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="88a08-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a08-246">Range-Lower</span></span>            | <span data-ttu-id="88a08-247">1</span><span class="sxs-lookup"><span data-stu-id="88a08-247">1</span></span>                                                                   |
| <span data-ttu-id="88a08-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a08-248">Range-Upper</span></span>            | <span data-ttu-id="88a08-249">255</span><span class="sxs-lookup"><span data-stu-id="88a08-249">255</span></span>                                                                 |
| <span data-ttu-id="88a08-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-250">Search-Flags</span></span>           | <span data-ttu-id="88a08-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a08-251">0x00000000</span></span>                                                          |
| <span data-ttu-id="88a08-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a08-252">System-Flags</span></span>           | <span data-ttu-id="88a08-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a08-253">0x00000010</span></span>                                                          |
| <span data-ttu-id="88a08-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88a08-254">Classes used in</span></span>        | [<span data-ttu-id="88a08-255">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="88a08-255">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



 

 






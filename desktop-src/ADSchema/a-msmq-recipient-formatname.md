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
# <a name="msmq-recipient-formatname-attribute"></a><span data-ttu-id="10a3c-105">MSMQ-收件者-Msmq.formatname 屬性</span><span class="sxs-lookup"><span data-stu-id="10a3c-105">MSMQ-Recipient-FormatName attribute</span></span>

<span data-ttu-id="10a3c-106">當做 MSMQ 自訂收件者類別中的收件者格式名稱使用。</span><span class="sxs-lookup"><span data-stu-id="10a3c-106">Used as the recipient format name in the MSMQ-Custom-Recipient class.</span></span>



| <span data-ttu-id="10a3c-107">進入</span><span class="sxs-lookup"><span data-stu-id="10a3c-107">Entry</span></span> | <span data-ttu-id="10a3c-108">值</span><span class="sxs-lookup"><span data-stu-id="10a3c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="10a3c-109">CN</span><span class="sxs-lookup"><span data-stu-id="10a3c-109">CN</span></span>                | <span data-ttu-id="10a3c-110">MSMQ-收件者-Msmq.formatname</span><span class="sxs-lookup"><span data-stu-id="10a3c-110">MSMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="10a3c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="10a3c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="10a3c-112">msMQ-收件者-Msmq.formatname</span><span class="sxs-lookup"><span data-stu-id="10a3c-112">msMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="10a3c-113">大小</span><span class="sxs-lookup"><span data-stu-id="10a3c-113">Size</span></span>              | <span data-ttu-id="10a3c-114">1到255個字元。</span><span class="sxs-lookup"><span data-stu-id="10a3c-114">1 to 255 characters.</span></span>                        |
| <span data-ttu-id="10a3c-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="10a3c-115">Update Privilege</span></span>  | <span data-ttu-id="10a3c-116">佇列擁有者。</span><span class="sxs-lookup"><span data-stu-id="10a3c-116">The queue owner.</span></span>                            |
| <span data-ttu-id="10a3c-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="10a3c-117">Update Frequency</span></span>  | <span data-ttu-id="10a3c-118">只有在移動外部佇列之後。</span><span class="sxs-lookup"><span data-stu-id="10a3c-118">Only after the external queue was moved.</span></span>    |
| <span data-ttu-id="10a3c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="10a3c-119">Attribute-Id</span></span>      | <span data-ttu-id="10a3c-120">1.2.840.113556.1.4.1695</span><span class="sxs-lookup"><span data-stu-id="10a3c-120">1.2.840.113556.1.4.1695</span></span>                     |
| <span data-ttu-id="10a3c-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="10a3c-121">System-Id-Guid</span></span>    | <span data-ttu-id="10a3c-122">3bfe6748-b544-485a-b067-1b310c4334bf</span><span class="sxs-lookup"><span data-stu-id="10a3c-122">3bfe6748-b544-485a-b067-1b310c4334bf</span></span>        |
| <span data-ttu-id="10a3c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="10a3c-123">Syntax</span></span>            | [<span data-ttu-id="10a3c-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="10a3c-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="10a3c-125">實作</span><span class="sxs-lookup"><span data-stu-id="10a3c-125">Implementations</span></span>

-   [<span data-ttu-id="10a3c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="10a3c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="10a3c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="10a3c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="10a3c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="10a3c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="10a3c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="10a3c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="10a3c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="10a3c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="10a3c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="10a3c-131">Windows Server 2003</span></span>



| <span data-ttu-id="10a3c-132">進入</span><span class="sxs-lookup"><span data-stu-id="10a3c-132">Entry</span></span> | <span data-ttu-id="10a3c-133">值</span><span class="sxs-lookup"><span data-stu-id="10a3c-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="10a3c-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10a3c-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10a3c-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="10a3c-136">System-Only</span></span>            | <span data-ttu-id="10a3c-137">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-137">False</span></span>                                                               |
| <span data-ttu-id="10a3c-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10a3c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="10a3c-139">對</span><span class="sxs-lookup"><span data-stu-id="10a3c-139">True</span></span>                                                                |
| <span data-ttu-id="10a3c-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10a3c-140">Is Indexed</span></span>             | <span data-ttu-id="10a3c-141">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-141">False</span></span>                                                               |
| <span data-ttu-id="10a3c-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10a3c-142">In Global Catalog</span></span>      | <span data-ttu-id="10a3c-143">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-143">False</span></span>                                                               |
| <span data-ttu-id="10a3c-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10a3c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="10a3c-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10a3c-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="10a3c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10a3c-146">Range-Lower</span></span>            | <span data-ttu-id="10a3c-147">1</span><span class="sxs-lookup"><span data-stu-id="10a3c-147">1</span></span>                                                                   |
| <span data-ttu-id="10a3c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10a3c-148">Range-Upper</span></span>            | <span data-ttu-id="10a3c-149">255</span><span class="sxs-lookup"><span data-stu-id="10a3c-149">255</span></span>                                                                 |
| <span data-ttu-id="10a3c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-150">Search-Flags</span></span>           | <span data-ttu-id="10a3c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10a3c-151">0x00000000</span></span>                                                          |
| <span data-ttu-id="10a3c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-152">System-Flags</span></span>           | <span data-ttu-id="10a3c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10a3c-153">0x00000010</span></span>                                                          |
| <span data-ttu-id="10a3c-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10a3c-154">Classes used in</span></span>        | [<span data-ttu-id="10a3c-155">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="10a3c-155">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="10a3c-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="10a3c-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="10a3c-157">進入</span><span class="sxs-lookup"><span data-stu-id="10a3c-157">Entry</span></span> | <span data-ttu-id="10a3c-158">值</span><span class="sxs-lookup"><span data-stu-id="10a3c-158">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="10a3c-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10a3c-159">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10a3c-160">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="10a3c-161">System-Only</span></span>            | <span data-ttu-id="10a3c-162">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-162">False</span></span>                                                               |
| <span data-ttu-id="10a3c-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10a3c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="10a3c-164">對</span><span class="sxs-lookup"><span data-stu-id="10a3c-164">True</span></span>                                                                |
| <span data-ttu-id="10a3c-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10a3c-165">Is Indexed</span></span>             | <span data-ttu-id="10a3c-166">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-166">False</span></span>                                                               |
| <span data-ttu-id="10a3c-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10a3c-167">In Global Catalog</span></span>      | <span data-ttu-id="10a3c-168">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-168">False</span></span>                                                               |
| <span data-ttu-id="10a3c-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10a3c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="10a3c-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10a3c-170">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="10a3c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10a3c-171">Range-Lower</span></span>            | <span data-ttu-id="10a3c-172">1</span><span class="sxs-lookup"><span data-stu-id="10a3c-172">1</span></span>                                                                   |
| <span data-ttu-id="10a3c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10a3c-173">Range-Upper</span></span>            | <span data-ttu-id="10a3c-174">255</span><span class="sxs-lookup"><span data-stu-id="10a3c-174">255</span></span>                                                                 |
| <span data-ttu-id="10a3c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-175">Search-Flags</span></span>           | <span data-ttu-id="10a3c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10a3c-176">0x00000000</span></span>                                                          |
| <span data-ttu-id="10a3c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-177">System-Flags</span></span>           | <span data-ttu-id="10a3c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10a3c-178">0x00000010</span></span>                                                          |
| <span data-ttu-id="10a3c-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10a3c-179">Classes used in</span></span>        | [<span data-ttu-id="10a3c-180">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="10a3c-180">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="10a3c-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10a3c-181">Windows Server 2008</span></span>



| <span data-ttu-id="10a3c-182">進入</span><span class="sxs-lookup"><span data-stu-id="10a3c-182">Entry</span></span> | <span data-ttu-id="10a3c-183">值</span><span class="sxs-lookup"><span data-stu-id="10a3c-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="10a3c-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10a3c-184">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10a3c-185">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="10a3c-186">System-Only</span></span>            | <span data-ttu-id="10a3c-187">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-187">False</span></span>                                                               |
| <span data-ttu-id="10a3c-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10a3c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="10a3c-189">對</span><span class="sxs-lookup"><span data-stu-id="10a3c-189">True</span></span>                                                                |
| <span data-ttu-id="10a3c-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10a3c-190">Is Indexed</span></span>             | <span data-ttu-id="10a3c-191">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-191">False</span></span>                                                               |
| <span data-ttu-id="10a3c-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10a3c-192">In Global Catalog</span></span>      | <span data-ttu-id="10a3c-193">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-193">False</span></span>                                                               |
| <span data-ttu-id="10a3c-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10a3c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="10a3c-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10a3c-195">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="10a3c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10a3c-196">Range-Lower</span></span>            | <span data-ttu-id="10a3c-197">1</span><span class="sxs-lookup"><span data-stu-id="10a3c-197">1</span></span>                                                                   |
| <span data-ttu-id="10a3c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10a3c-198">Range-Upper</span></span>            | <span data-ttu-id="10a3c-199">255</span><span class="sxs-lookup"><span data-stu-id="10a3c-199">255</span></span>                                                                 |
| <span data-ttu-id="10a3c-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-200">Search-Flags</span></span>           | <span data-ttu-id="10a3c-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10a3c-201">0x00000000</span></span>                                                          |
| <span data-ttu-id="10a3c-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-202">System-Flags</span></span>           | <span data-ttu-id="10a3c-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10a3c-203">0x00000010</span></span>                                                          |
| <span data-ttu-id="10a3c-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10a3c-204">Classes used in</span></span>        | [<span data-ttu-id="10a3c-205">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="10a3c-205">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="10a3c-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10a3c-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="10a3c-207">進入</span><span class="sxs-lookup"><span data-stu-id="10a3c-207">Entry</span></span> | <span data-ttu-id="10a3c-208">值</span><span class="sxs-lookup"><span data-stu-id="10a3c-208">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="10a3c-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10a3c-209">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10a3c-210">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="10a3c-211">System-Only</span></span>            | <span data-ttu-id="10a3c-212">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-212">False</span></span>                                                               |
| <span data-ttu-id="10a3c-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10a3c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="10a3c-214">對</span><span class="sxs-lookup"><span data-stu-id="10a3c-214">True</span></span>                                                                |
| <span data-ttu-id="10a3c-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10a3c-215">Is Indexed</span></span>             | <span data-ttu-id="10a3c-216">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-216">False</span></span>                                                               |
| <span data-ttu-id="10a3c-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10a3c-217">In Global Catalog</span></span>      | <span data-ttu-id="10a3c-218">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-218">False</span></span>                                                               |
| <span data-ttu-id="10a3c-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10a3c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="10a3c-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10a3c-220">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="10a3c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10a3c-221">Range-Lower</span></span>            | <span data-ttu-id="10a3c-222">1</span><span class="sxs-lookup"><span data-stu-id="10a3c-222">1</span></span>                                                                   |
| <span data-ttu-id="10a3c-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10a3c-223">Range-Upper</span></span>            | <span data-ttu-id="10a3c-224">255</span><span class="sxs-lookup"><span data-stu-id="10a3c-224">255</span></span>                                                                 |
| <span data-ttu-id="10a3c-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-225">Search-Flags</span></span>           | <span data-ttu-id="10a3c-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10a3c-226">0x00000000</span></span>                                                          |
| <span data-ttu-id="10a3c-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-227">System-Flags</span></span>           | <span data-ttu-id="10a3c-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10a3c-228">0x00000010</span></span>                                                          |
| <span data-ttu-id="10a3c-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10a3c-229">Classes used in</span></span>        | [<span data-ttu-id="10a3c-230">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="10a3c-230">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="10a3c-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10a3c-231">Windows Server 2012</span></span>



| <span data-ttu-id="10a3c-232">進入</span><span class="sxs-lookup"><span data-stu-id="10a3c-232">Entry</span></span> | <span data-ttu-id="10a3c-233">值</span><span class="sxs-lookup"><span data-stu-id="10a3c-233">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="10a3c-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10a3c-234">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10a3c-235">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="10a3c-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="10a3c-236">System-Only</span></span>            | <span data-ttu-id="10a3c-237">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-237">False</span></span>                                                               |
| <span data-ttu-id="10a3c-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10a3c-238">Is-Single-Valued</span></span>       | <span data-ttu-id="10a3c-239">對</span><span class="sxs-lookup"><span data-stu-id="10a3c-239">True</span></span>                                                                |
| <span data-ttu-id="10a3c-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10a3c-240">Is Indexed</span></span>             | <span data-ttu-id="10a3c-241">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-241">False</span></span>                                                               |
| <span data-ttu-id="10a3c-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10a3c-242">In Global Catalog</span></span>      | <span data-ttu-id="10a3c-243">否</span><span class="sxs-lookup"><span data-stu-id="10a3c-243">False</span></span>                                                               |
| <span data-ttu-id="10a3c-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10a3c-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="10a3c-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10a3c-245">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="10a3c-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10a3c-246">Range-Lower</span></span>            | <span data-ttu-id="10a3c-247">1</span><span class="sxs-lookup"><span data-stu-id="10a3c-247">1</span></span>                                                                   |
| <span data-ttu-id="10a3c-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10a3c-248">Range-Upper</span></span>            | <span data-ttu-id="10a3c-249">255</span><span class="sxs-lookup"><span data-stu-id="10a3c-249">255</span></span>                                                                 |
| <span data-ttu-id="10a3c-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-250">Search-Flags</span></span>           | <span data-ttu-id="10a3c-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10a3c-251">0x00000000</span></span>                                                          |
| <span data-ttu-id="10a3c-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10a3c-252">System-Flags</span></span>           | <span data-ttu-id="10a3c-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10a3c-253">0x00000010</span></span>                                                          |
| <span data-ttu-id="10a3c-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10a3c-254">Classes used in</span></span>        | [<span data-ttu-id="10a3c-255">**MSMQ-自訂-收件者**</span><span class="sxs-lookup"><span data-stu-id="10a3c-255">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



 

 






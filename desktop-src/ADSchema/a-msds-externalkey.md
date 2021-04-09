---
title: ms DS-External-Key 屬性
description: 識別外部存放區中之物件的字串，例如資料庫中的記錄。
ms.assetid: aa5b02eb-f872-4184-9508-fe3d4180c680
ms.tgt_platform: multiple
keywords:
- ms DS-External-Key 屬性 AD 架構
- ExternalKey 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-External-Key
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aeaaf506495dd2feffe7bdb6d76ea702b84ff00
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687259"
---
# <a name="ms-ds-external-key-attribute"></a><span data-ttu-id="c69e4-105">ms DS-External-Key 屬性</span><span class="sxs-lookup"><span data-stu-id="c69e4-105">ms-DS-External-Key attribute</span></span>

<span data-ttu-id="c69e4-106">識別外部存放區中之物件的字串，例如資料庫中的記錄。</span><span class="sxs-lookup"><span data-stu-id="c69e4-106">A string that identifies an object in an external store, such as a record in a database.</span></span>



| <span data-ttu-id="c69e4-107">進入</span><span class="sxs-lookup"><span data-stu-id="c69e4-107">Entry</span></span> | <span data-ttu-id="c69e4-108">值</span><span class="sxs-lookup"><span data-stu-id="c69e4-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c69e4-109">CN</span><span class="sxs-lookup"><span data-stu-id="c69e4-109">CN</span></span>                | <span data-ttu-id="c69e4-110">ms DS-External-Key</span><span class="sxs-lookup"><span data-stu-id="c69e4-110">ms-DS-External-Key</span></span>                          |
| <span data-ttu-id="c69e4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c69e4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c69e4-112">ExternalKey</span><span class="sxs-lookup"><span data-stu-id="c69e4-112">msDS-ExternalKey</span></span>                            |
| <span data-ttu-id="c69e4-113">大小</span><span class="sxs-lookup"><span data-stu-id="c69e4-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c69e4-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c69e4-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="c69e4-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c69e4-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c69e4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c69e4-116">Attribute-Id</span></span>      | <span data-ttu-id="c69e4-117">1.2.840.113556.1.4.1833</span><span class="sxs-lookup"><span data-stu-id="c69e4-117">1.2.840.113556.1.4.1833</span></span>                     |
| <span data-ttu-id="c69e4-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c69e4-118">System-Id-Guid</span></span>    | <span data-ttu-id="c69e4-119">b92fd528-38ac-40d4-818d-0433380837c1</span><span class="sxs-lookup"><span data-stu-id="c69e4-119">b92fd528-38ac-40d4-818d-0433380837c1</span></span>        |
| <span data-ttu-id="c69e4-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c69e4-120">Syntax</span></span>            | [<span data-ttu-id="c69e4-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c69e4-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c69e4-122">實作</span><span class="sxs-lookup"><span data-stu-id="c69e4-122">Implementations</span></span>

-   [<span data-ttu-id="c69e4-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c69e4-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c69e4-124">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c69e4-124">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c69e4-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c69e4-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c69e4-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c69e4-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c69e4-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c69e4-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c69e4-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c69e4-128">Windows Server 2003</span></span>



| <span data-ttu-id="c69e4-129">進入</span><span class="sxs-lookup"><span data-stu-id="c69e4-129">Entry</span></span> | <span data-ttu-id="c69e4-130">值</span><span class="sxs-lookup"><span data-stu-id="c69e4-130">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c69e4-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c69e4-131">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69e4-132">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69e4-133">System-Only</span></span>            | <span data-ttu-id="c69e4-134">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-134">False</span></span>        |
| <span data-ttu-id="c69e4-135">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c69e4-135">Is-Single-Valued</span></span>       | <span data-ttu-id="c69e4-136">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-136">False</span></span>        |
| <span data-ttu-id="c69e4-137">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c69e4-137">Is Indexed</span></span>             | <span data-ttu-id="c69e4-138">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-138">False</span></span>        |
| <span data-ttu-id="c69e4-139">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c69e4-139">In Global Catalog</span></span>      | <span data-ttu-id="c69e4-140">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-140">False</span></span>        |
| <span data-ttu-id="c69e4-141">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c69e4-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69e4-142">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c69e4-142">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c69e4-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69e4-143">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c69e4-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69e4-144">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c69e4-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-145">Search-Flags</span></span>           | <span data-ttu-id="c69e4-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-146">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-147">System-Flags</span></span>           | <span data-ttu-id="c69e4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-148">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-149">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c69e4-149">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c69e4-150">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c69e4-150">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c69e4-151">進入</span><span class="sxs-lookup"><span data-stu-id="c69e4-151">Entry</span></span> | <span data-ttu-id="c69e4-152">值</span><span class="sxs-lookup"><span data-stu-id="c69e4-152">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c69e4-153">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c69e4-153">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69e4-154">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69e4-155">System-Only</span></span>            | <span data-ttu-id="c69e4-156">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-156">False</span></span>        |
| <span data-ttu-id="c69e4-157">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c69e4-157">Is-Single-Valued</span></span>       | <span data-ttu-id="c69e4-158">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-158">False</span></span>        |
| <span data-ttu-id="c69e4-159">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c69e4-159">Is Indexed</span></span>             | <span data-ttu-id="c69e4-160">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-160">False</span></span>        |
| <span data-ttu-id="c69e4-161">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c69e4-161">In Global Catalog</span></span>      | <span data-ttu-id="c69e4-162">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-162">False</span></span>        |
| <span data-ttu-id="c69e4-163">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c69e4-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69e4-164">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c69e4-164">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c69e4-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69e4-165">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c69e4-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69e4-166">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c69e4-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-167">Search-Flags</span></span>           | <span data-ttu-id="c69e4-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-168">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-169">System-Flags</span></span>           | <span data-ttu-id="c69e4-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-170">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-171">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c69e4-171">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="c69e4-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c69e4-172">Windows Server 2008</span></span>



| <span data-ttu-id="c69e4-173">進入</span><span class="sxs-lookup"><span data-stu-id="c69e4-173">Entry</span></span> | <span data-ttu-id="c69e4-174">值</span><span class="sxs-lookup"><span data-stu-id="c69e4-174">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c69e4-175">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c69e4-175">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-176">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69e4-176">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-177">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69e4-177">System-Only</span></span>            | <span data-ttu-id="c69e4-178">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-178">False</span></span>        |
| <span data-ttu-id="c69e4-179">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c69e4-179">Is-Single-Valued</span></span>       | <span data-ttu-id="c69e4-180">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-180">False</span></span>        |
| <span data-ttu-id="c69e4-181">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c69e4-181">Is Indexed</span></span>             | <span data-ttu-id="c69e4-182">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-182">False</span></span>        |
| <span data-ttu-id="c69e4-183">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c69e4-183">In Global Catalog</span></span>      | <span data-ttu-id="c69e4-184">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-184">False</span></span>        |
| <span data-ttu-id="c69e4-185">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c69e4-185">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69e4-186">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c69e4-186">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c69e4-187">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69e4-187">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c69e4-188">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69e4-188">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c69e4-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-189">Search-Flags</span></span>           | <span data-ttu-id="c69e4-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-190">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-191">System-Flags</span></span>           | <span data-ttu-id="c69e4-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-192">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-193">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c69e4-193">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c69e4-194">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c69e4-194">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c69e4-195">進入</span><span class="sxs-lookup"><span data-stu-id="c69e4-195">Entry</span></span> | <span data-ttu-id="c69e4-196">值</span><span class="sxs-lookup"><span data-stu-id="c69e4-196">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c69e4-197">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c69e4-197">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-198">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69e4-198">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-199">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69e4-199">System-Only</span></span>            | <span data-ttu-id="c69e4-200">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-200">False</span></span>        |
| <span data-ttu-id="c69e4-201">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c69e4-201">Is-Single-Valued</span></span>       | <span data-ttu-id="c69e4-202">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-202">False</span></span>        |
| <span data-ttu-id="c69e4-203">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c69e4-203">Is Indexed</span></span>             | <span data-ttu-id="c69e4-204">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-204">False</span></span>        |
| <span data-ttu-id="c69e4-205">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c69e4-205">In Global Catalog</span></span>      | <span data-ttu-id="c69e4-206">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-206">False</span></span>        |
| <span data-ttu-id="c69e4-207">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c69e4-207">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69e4-208">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c69e4-208">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c69e4-209">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69e4-209">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c69e4-210">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69e4-210">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c69e4-211">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-211">Search-Flags</span></span>           | <span data-ttu-id="c69e4-212">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-212">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-213">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-213">System-Flags</span></span>           | <span data-ttu-id="c69e4-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-214">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-215">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c69e4-215">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="c69e4-216">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c69e4-216">Windows Server 2012</span></span>



| <span data-ttu-id="c69e4-217">進入</span><span class="sxs-lookup"><span data-stu-id="c69e4-217">Entry</span></span> | <span data-ttu-id="c69e4-218">值</span><span class="sxs-lookup"><span data-stu-id="c69e4-218">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c69e4-219">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c69e4-219">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-220">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69e4-220">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c69e4-221">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69e4-221">System-Only</span></span>            | <span data-ttu-id="c69e4-222">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-222">False</span></span>        |
| <span data-ttu-id="c69e4-223">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c69e4-223">Is-Single-Valued</span></span>       | <span data-ttu-id="c69e4-224">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-224">False</span></span>        |
| <span data-ttu-id="c69e4-225">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c69e4-225">Is Indexed</span></span>             | <span data-ttu-id="c69e4-226">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-226">False</span></span>        |
| <span data-ttu-id="c69e4-227">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c69e4-227">In Global Catalog</span></span>      | <span data-ttu-id="c69e4-228">否</span><span class="sxs-lookup"><span data-stu-id="c69e4-228">False</span></span>        |
| <span data-ttu-id="c69e4-229">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c69e4-229">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69e4-230">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c69e4-230">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c69e4-231">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69e4-231">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c69e4-232">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69e4-232">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c69e4-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-233">Search-Flags</span></span>           | <span data-ttu-id="c69e4-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-234">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69e4-235">System-Flags</span></span>           | <span data-ttu-id="c69e4-236">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69e4-236">0x00000000</span></span>   |
| <span data-ttu-id="c69e4-237">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c69e4-237">Classes used in</span></span>        | \-           |



 

 





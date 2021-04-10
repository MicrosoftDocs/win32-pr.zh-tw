---
title: Extra-Columns 屬性
description: 這是一個多重值屬性，其值包含5個元組 (屬性名稱) 、 (資料行標題) 、 (預設可見度 (0、1) ) 、 (資料行寬度 ( \ 8211; 1 代表自動寬度) ) ，0 (保留供日後使用，則必須為零) 。
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Extra-Columns 屬性 AD 架構
- extraColumns 屬性 AD 架構
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686867"
---
# <a name="extra-columns-attribute"></a><span data-ttu-id="ff0db-105">Extra-Columns 屬性</span><span class="sxs-lookup"><span data-stu-id="ff0db-105">Extra-Columns attribute</span></span>

<span data-ttu-id="ff0db-106">這是一個多重值屬性，其值包含5個元組： (的屬性名稱) 、 (的資料行標題) 、 (預設可見度 (0、1) ) 、 (資料行寬度 ( 1 表示自動寬度) ) 、0 (保留供日後使用，則必須為零) 。</span><span class="sxs-lookup"><span data-stu-id="ff0db-106">This is a multivalued attribute whose values consist of a 5 tuple: (attribute name), (column title), (default visibility (0,1)), (column width ( 1 for auto width)), 0 (reserved for future use must be zero).</span></span> <span data-ttu-id="ff0db-107">[AD 使用者和電腦] 主控台會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="ff0db-107">This value is used by the AD Users and Computers console.</span></span>



| <span data-ttu-id="ff0db-108">進入</span><span class="sxs-lookup"><span data-stu-id="ff0db-108">Entry</span></span> | <span data-ttu-id="ff0db-109">值</span><span class="sxs-lookup"><span data-stu-id="ff0db-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0db-110">CN</span><span class="sxs-lookup"><span data-stu-id="ff0db-110">CN</span></span>                | <span data-ttu-id="ff0db-111">Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="ff0db-111">Extra-Columns</span></span>                                                                                                                                                        |
| <span data-ttu-id="ff0db-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ff0db-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ff0db-113">extraColumns</span><span class="sxs-lookup"><span data-stu-id="ff0db-113">extraColumns</span></span>                                                                                                                                                         |
| <span data-ttu-id="ff0db-114">大小</span><span class="sxs-lookup"><span data-stu-id="ff0db-114">Size</span></span>              | <span data-ttu-id="ff0db-115">每個值都是上述5個元組的字串大小。</span><span class="sxs-lookup"><span data-stu-id="ff0db-115">Each value would be the size of the string of the 5 tuple above.</span></span> <span data-ttu-id="ff0db-116">根據預設，DisplaySpecifier 容器中的預設顯示物件上會有22個值。</span><span class="sxs-lookup"><span data-stu-id="ff0db-116">By default there will be 22 values on the default-Display object in the DisplaySpecifier container.</span></span> |
| <span data-ttu-id="ff0db-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ff0db-117">Update Privilege</span></span>  | <span data-ttu-id="ff0db-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="ff0db-118">Domain administrator</span></span>                                                                                                                                                 |
| <span data-ttu-id="ff0db-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ff0db-119">Update Frequency</span></span>  | <span data-ttu-id="ff0db-120">只有在已安裝 Exchange 之類的服務時，才會更新此項。</span><span class="sxs-lookup"><span data-stu-id="ff0db-120">This will only be updated if a service like Exchange is installed.</span></span>                                                                                                   |
| <span data-ttu-id="ff0db-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ff0db-121">Attribute-Id</span></span>      | <span data-ttu-id="ff0db-122">1.2.840.113556.1.4.1687</span><span class="sxs-lookup"><span data-stu-id="ff0db-122">1.2.840.113556.1.4.1687</span></span>                                                                                                                                              |
| <span data-ttu-id="ff0db-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ff0db-123">System-Id-Guid</span></span>    | <span data-ttu-id="ff0db-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span><span class="sxs-lookup"><span data-stu-id="ff0db-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span></span>                                                                                                                                 |
| <span data-ttu-id="ff0db-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff0db-125">Syntax</span></span>            | [<span data-ttu-id="ff0db-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ff0db-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a><span data-ttu-id="ff0db-127">實作</span><span class="sxs-lookup"><span data-stu-id="ff0db-127">Implementations</span></span>

-   [<span data-ttu-id="ff0db-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ff0db-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ff0db-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ff0db-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ff0db-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ff0db-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ff0db-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ff0db-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ff0db-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ff0db-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ff0db-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff0db-133">Windows Server 2003</span></span>



| <span data-ttu-id="ff0db-134">進入</span><span class="sxs-lookup"><span data-stu-id="ff0db-134">Entry</span></span> | <span data-ttu-id="ff0db-135">值</span><span class="sxs-lookup"><span data-stu-id="ff0db-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ff0db-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ff0db-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff0db-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff0db-138">System-Only</span></span>            | <span data-ttu-id="ff0db-139">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-139">False</span></span>                                                      |
| <span data-ttu-id="ff0db-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ff0db-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ff0db-141">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-141">False</span></span>                                                      |
| <span data-ttu-id="ff0db-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ff0db-142">Is Indexed</span></span>             | <span data-ttu-id="ff0db-143">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-143">False</span></span>                                                      |
| <span data-ttu-id="ff0db-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ff0db-144">In Global Catalog</span></span>      | <span data-ttu-id="ff0db-145">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-145">False</span></span>                                                      |
| <span data-ttu-id="ff0db-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ff0db-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff0db-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ff0db-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ff0db-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff0db-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff0db-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-150">Search-Flags</span></span>           | <span data-ttu-id="ff0db-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff0db-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="ff0db-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-152">System-Flags</span></span>           | <span data-ttu-id="ff0db-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff0db-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="ff0db-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ff0db-154">Classes used in</span></span>        | [<span data-ttu-id="ff0db-155">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="ff0db-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ff0db-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ff0db-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ff0db-157">進入</span><span class="sxs-lookup"><span data-stu-id="ff0db-157">Entry</span></span> | <span data-ttu-id="ff0db-158">值</span><span class="sxs-lookup"><span data-stu-id="ff0db-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ff0db-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ff0db-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff0db-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff0db-161">System-Only</span></span>            | <span data-ttu-id="ff0db-162">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-162">False</span></span>                                                      |
| <span data-ttu-id="ff0db-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ff0db-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ff0db-164">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-164">False</span></span>                                                      |
| <span data-ttu-id="ff0db-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ff0db-165">Is Indexed</span></span>             | <span data-ttu-id="ff0db-166">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-166">False</span></span>                                                      |
| <span data-ttu-id="ff0db-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ff0db-167">In Global Catalog</span></span>      | <span data-ttu-id="ff0db-168">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-168">False</span></span>                                                      |
| <span data-ttu-id="ff0db-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ff0db-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff0db-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ff0db-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ff0db-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff0db-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff0db-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-173">Search-Flags</span></span>           | <span data-ttu-id="ff0db-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff0db-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="ff0db-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-175">System-Flags</span></span>           | <span data-ttu-id="ff0db-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff0db-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="ff0db-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ff0db-177">Classes used in</span></span>        | [<span data-ttu-id="ff0db-178">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="ff0db-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ff0db-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff0db-179">Windows Server 2008</span></span>



| <span data-ttu-id="ff0db-180">進入</span><span class="sxs-lookup"><span data-stu-id="ff0db-180">Entry</span></span> | <span data-ttu-id="ff0db-181">值</span><span class="sxs-lookup"><span data-stu-id="ff0db-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ff0db-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ff0db-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff0db-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff0db-184">System-Only</span></span>            | <span data-ttu-id="ff0db-185">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-185">False</span></span>                                                      |
| <span data-ttu-id="ff0db-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ff0db-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ff0db-187">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-187">False</span></span>                                                      |
| <span data-ttu-id="ff0db-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ff0db-188">Is Indexed</span></span>             | <span data-ttu-id="ff0db-189">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-189">False</span></span>                                                      |
| <span data-ttu-id="ff0db-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ff0db-190">In Global Catalog</span></span>      | <span data-ttu-id="ff0db-191">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-191">False</span></span>                                                      |
| <span data-ttu-id="ff0db-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ff0db-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff0db-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ff0db-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ff0db-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff0db-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff0db-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-196">Search-Flags</span></span>           | <span data-ttu-id="ff0db-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff0db-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="ff0db-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-198">System-Flags</span></span>           | <span data-ttu-id="ff0db-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff0db-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="ff0db-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ff0db-200">Classes used in</span></span>        | [<span data-ttu-id="ff0db-201">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="ff0db-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ff0db-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff0db-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ff0db-203">進入</span><span class="sxs-lookup"><span data-stu-id="ff0db-203">Entry</span></span> | <span data-ttu-id="ff0db-204">值</span><span class="sxs-lookup"><span data-stu-id="ff0db-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ff0db-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ff0db-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff0db-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff0db-207">System-Only</span></span>            | <span data-ttu-id="ff0db-208">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-208">False</span></span>                                                      |
| <span data-ttu-id="ff0db-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ff0db-209">Is-Single-Valued</span></span>       | <span data-ttu-id="ff0db-210">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-210">False</span></span>                                                      |
| <span data-ttu-id="ff0db-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ff0db-211">Is Indexed</span></span>             | <span data-ttu-id="ff0db-212">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-212">False</span></span>                                                      |
| <span data-ttu-id="ff0db-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ff0db-213">In Global Catalog</span></span>      | <span data-ttu-id="ff0db-214">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-214">False</span></span>                                                      |
| <span data-ttu-id="ff0db-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ff0db-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff0db-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ff0db-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ff0db-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff0db-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff0db-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-219">Search-Flags</span></span>           | <span data-ttu-id="ff0db-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff0db-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="ff0db-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-221">System-Flags</span></span>           | <span data-ttu-id="ff0db-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff0db-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="ff0db-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ff0db-223">Classes used in</span></span>        | [<span data-ttu-id="ff0db-224">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="ff0db-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ff0db-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff0db-225">Windows Server 2012</span></span>



| <span data-ttu-id="ff0db-226">進入</span><span class="sxs-lookup"><span data-stu-id="ff0db-226">Entry</span></span> | <span data-ttu-id="ff0db-227">值</span><span class="sxs-lookup"><span data-stu-id="ff0db-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ff0db-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ff0db-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff0db-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ff0db-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff0db-230">System-Only</span></span>            | <span data-ttu-id="ff0db-231">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-231">False</span></span>                                                      |
| <span data-ttu-id="ff0db-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ff0db-232">Is-Single-Valued</span></span>       | <span data-ttu-id="ff0db-233">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-233">False</span></span>                                                      |
| <span data-ttu-id="ff0db-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ff0db-234">Is Indexed</span></span>             | <span data-ttu-id="ff0db-235">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-235">False</span></span>                                                      |
| <span data-ttu-id="ff0db-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ff0db-236">In Global Catalog</span></span>      | <span data-ttu-id="ff0db-237">否</span><span class="sxs-lookup"><span data-stu-id="ff0db-237">False</span></span>                                                      |
| <span data-ttu-id="ff0db-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ff0db-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff0db-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ff0db-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ff0db-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff0db-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff0db-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ff0db-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-242">Search-Flags</span></span>           | <span data-ttu-id="ff0db-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff0db-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="ff0db-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff0db-244">System-Flags</span></span>           | <span data-ttu-id="ff0db-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff0db-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="ff0db-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ff0db-246">Classes used in</span></span>        | [<span data-ttu-id="ff0db-247">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="ff0db-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 






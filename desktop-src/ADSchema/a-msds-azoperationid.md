---
title: ms-DS-Az-Operation-ID 屬性
description: 讓應用程式成為唯一作業的應用程式特定識別碼。
ms.assetid: 0d0fc8ce-7044-481a-8df2-489e33264412
ms.tgt_platform: multiple
keywords:
- ms-DS-Az-Operation-ID attribute AD Schema
- AzOperationID 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Az-Operation-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58cc05338fa3960185a795422c62256a63e6f1ca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104187344"
---
# <a name="ms-ds-az-operation-id-attribute"></a><span data-ttu-id="824d4-105">ms-DS-Az-Operation-ID 屬性</span><span class="sxs-lookup"><span data-stu-id="824d4-105">ms-DS-Az-Operation-ID attribute</span></span>

<span data-ttu-id="824d4-106">讓應用程式成為唯一作業的應用程式特定識別碼。</span><span class="sxs-lookup"><span data-stu-id="824d4-106">An application specific ID that makes the operation unique to the application.</span></span>



| <span data-ttu-id="824d4-107">進入</span><span class="sxs-lookup"><span data-stu-id="824d4-107">Entry</span></span> | <span data-ttu-id="824d4-108">值</span><span class="sxs-lookup"><span data-stu-id="824d4-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="824d4-109">CN</span><span class="sxs-lookup"><span data-stu-id="824d4-109">CN</span></span>                | <span data-ttu-id="824d4-110">ms-DS-Az-Operation-ID</span><span class="sxs-lookup"><span data-stu-id="824d4-110">ms-DS-Az-Operation-ID</span></span>                   |
| <span data-ttu-id="824d4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="824d4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="824d4-112">AzOperationID</span><span class="sxs-lookup"><span data-stu-id="824d4-112">msDS-AzOperationID</span></span>                      |
| <span data-ttu-id="824d4-113">大小</span><span class="sxs-lookup"><span data-stu-id="824d4-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="824d4-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="824d4-114">Update Privilege</span></span>  | <span data-ttu-id="824d4-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="824d4-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="824d4-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="824d4-116">Update Frequency</span></span>  | <span data-ttu-id="824d4-117">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="824d4-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="824d4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="824d4-118">Attribute-Id</span></span>      | <span data-ttu-id="824d4-119">1.2.840.113556.1.4.1800</span><span class="sxs-lookup"><span data-stu-id="824d4-119">1.2.840.113556.1.4.1800</span></span>                 |
| <span data-ttu-id="824d4-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="824d4-120">System-Id-Guid</span></span>    | <span data-ttu-id="824d4-121">a5f3b553-5d76-4cbe-ba3f-4312152cab18</span><span class="sxs-lookup"><span data-stu-id="824d4-121">a5f3b553-5d76-4cbe-ba3f-4312152cab18</span></span>    |
| <span data-ttu-id="824d4-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="824d4-122">Syntax</span></span>            | [<span data-ttu-id="824d4-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="824d4-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="824d4-124">實作</span><span class="sxs-lookup"><span data-stu-id="824d4-124">Implementations</span></span>

-   [<span data-ttu-id="824d4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="824d4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="824d4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="824d4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="824d4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="824d4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="824d4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="824d4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="824d4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="824d4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="824d4-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="824d4-130">Windows Server 2003</span></span>



| <span data-ttu-id="824d4-131">進入</span><span class="sxs-lookup"><span data-stu-id="824d4-131">Entry</span></span> | <span data-ttu-id="824d4-132">值</span><span class="sxs-lookup"><span data-stu-id="824d4-132">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="824d4-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="824d4-133">Link-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d4-134">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d4-135">System-Only</span></span>            | <span data-ttu-id="824d4-136">否</span><span class="sxs-lookup"><span data-stu-id="824d4-136">False</span></span>        |
| <span data-ttu-id="824d4-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="824d4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="824d4-138">對</span><span class="sxs-lookup"><span data-stu-id="824d4-138">True</span></span>         |
| <span data-ttu-id="824d4-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="824d4-139">Is Indexed</span></span>             | <span data-ttu-id="824d4-140">否</span><span class="sxs-lookup"><span data-stu-id="824d4-140">False</span></span>        |
| <span data-ttu-id="824d4-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="824d4-141">In Global Catalog</span></span>      | <span data-ttu-id="824d4-142">否</span><span class="sxs-lookup"><span data-stu-id="824d4-142">False</span></span>        |
| <span data-ttu-id="824d4-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="824d4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d4-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="824d4-144">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="824d4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d4-145">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="824d4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d4-146">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="824d4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-147">Search-Flags</span></span>           | <span data-ttu-id="824d4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d4-148">0x00000000</span></span>   |
| <span data-ttu-id="824d4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-149">System-Flags</span></span>           | <span data-ttu-id="824d4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d4-150">0x00000010</span></span>   |
| <span data-ttu-id="824d4-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="824d4-151">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="824d4-152">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="824d4-152">Windows Server 2003 R2</span></span>



| <span data-ttu-id="824d4-153">進入</span><span class="sxs-lookup"><span data-stu-id="824d4-153">Entry</span></span> | <span data-ttu-id="824d4-154">值</span><span class="sxs-lookup"><span data-stu-id="824d4-154">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="824d4-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="824d4-155">Link-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d4-156">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d4-157">System-Only</span></span>            | <span data-ttu-id="824d4-158">否</span><span class="sxs-lookup"><span data-stu-id="824d4-158">False</span></span>        |
| <span data-ttu-id="824d4-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="824d4-159">Is-Single-Valued</span></span>       | <span data-ttu-id="824d4-160">對</span><span class="sxs-lookup"><span data-stu-id="824d4-160">True</span></span>         |
| <span data-ttu-id="824d4-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="824d4-161">Is Indexed</span></span>             | <span data-ttu-id="824d4-162">否</span><span class="sxs-lookup"><span data-stu-id="824d4-162">False</span></span>        |
| <span data-ttu-id="824d4-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="824d4-163">In Global Catalog</span></span>      | <span data-ttu-id="824d4-164">否</span><span class="sxs-lookup"><span data-stu-id="824d4-164">False</span></span>        |
| <span data-ttu-id="824d4-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="824d4-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d4-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="824d4-166">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="824d4-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d4-167">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="824d4-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d4-168">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="824d4-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-169">Search-Flags</span></span>           | <span data-ttu-id="824d4-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d4-170">0x00000000</span></span>   |
| <span data-ttu-id="824d4-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-171">System-Flags</span></span>           | <span data-ttu-id="824d4-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d4-172">0x00000010</span></span>   |
| <span data-ttu-id="824d4-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="824d4-173">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="824d4-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="824d4-174">Windows Server 2008</span></span>



| <span data-ttu-id="824d4-175">進入</span><span class="sxs-lookup"><span data-stu-id="824d4-175">Entry</span></span> | <span data-ttu-id="824d4-176">值</span><span class="sxs-lookup"><span data-stu-id="824d4-176">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="824d4-177">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="824d4-177">Link-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-178">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d4-178">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d4-179">System-Only</span></span>            | <span data-ttu-id="824d4-180">否</span><span class="sxs-lookup"><span data-stu-id="824d4-180">False</span></span>        |
| <span data-ttu-id="824d4-181">是-單一值</span><span class="sxs-lookup"><span data-stu-id="824d4-181">Is-Single-Valued</span></span>       | <span data-ttu-id="824d4-182">對</span><span class="sxs-lookup"><span data-stu-id="824d4-182">True</span></span>         |
| <span data-ttu-id="824d4-183">已編制索引</span><span class="sxs-lookup"><span data-stu-id="824d4-183">Is Indexed</span></span>             | <span data-ttu-id="824d4-184">否</span><span class="sxs-lookup"><span data-stu-id="824d4-184">False</span></span>        |
| <span data-ttu-id="824d4-185">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="824d4-185">In Global Catalog</span></span>      | <span data-ttu-id="824d4-186">否</span><span class="sxs-lookup"><span data-stu-id="824d4-186">False</span></span>        |
| <span data-ttu-id="824d4-187">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="824d4-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d4-188">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="824d4-188">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="824d4-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d4-189">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="824d4-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d4-190">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="824d4-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-191">Search-Flags</span></span>           | <span data-ttu-id="824d4-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d4-192">0x00000000</span></span>   |
| <span data-ttu-id="824d4-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-193">System-Flags</span></span>           | <span data-ttu-id="824d4-194">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d4-194">0x00000010</span></span>   |
| <span data-ttu-id="824d4-195">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="824d4-195">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="824d4-196">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="824d4-196">Windows Server 2008 R2</span></span>



| <span data-ttu-id="824d4-197">進入</span><span class="sxs-lookup"><span data-stu-id="824d4-197">Entry</span></span> | <span data-ttu-id="824d4-198">值</span><span class="sxs-lookup"><span data-stu-id="824d4-198">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="824d4-199">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="824d4-199">Link-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d4-200">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d4-201">System-Only</span></span>            | <span data-ttu-id="824d4-202">否</span><span class="sxs-lookup"><span data-stu-id="824d4-202">False</span></span>        |
| <span data-ttu-id="824d4-203">是-單一值</span><span class="sxs-lookup"><span data-stu-id="824d4-203">Is-Single-Valued</span></span>       | <span data-ttu-id="824d4-204">對</span><span class="sxs-lookup"><span data-stu-id="824d4-204">True</span></span>         |
| <span data-ttu-id="824d4-205">已編制索引</span><span class="sxs-lookup"><span data-stu-id="824d4-205">Is Indexed</span></span>             | <span data-ttu-id="824d4-206">否</span><span class="sxs-lookup"><span data-stu-id="824d4-206">False</span></span>        |
| <span data-ttu-id="824d4-207">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="824d4-207">In Global Catalog</span></span>      | <span data-ttu-id="824d4-208">否</span><span class="sxs-lookup"><span data-stu-id="824d4-208">False</span></span>        |
| <span data-ttu-id="824d4-209">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="824d4-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d4-210">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="824d4-210">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="824d4-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d4-211">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="824d4-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d4-212">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="824d4-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-213">Search-Flags</span></span>           | <span data-ttu-id="824d4-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d4-214">0x00000000</span></span>   |
| <span data-ttu-id="824d4-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-215">System-Flags</span></span>           | <span data-ttu-id="824d4-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d4-216">0x00000010</span></span>   |
| <span data-ttu-id="824d4-217">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="824d4-217">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="824d4-218">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="824d4-218">Windows Server 2012</span></span>



| <span data-ttu-id="824d4-219">進入</span><span class="sxs-lookup"><span data-stu-id="824d4-219">Entry</span></span> | <span data-ttu-id="824d4-220">值</span><span class="sxs-lookup"><span data-stu-id="824d4-220">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="824d4-221">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="824d4-221">Link-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-222">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d4-222">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="824d4-223">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d4-223">System-Only</span></span>            | <span data-ttu-id="824d4-224">否</span><span class="sxs-lookup"><span data-stu-id="824d4-224">False</span></span>        |
| <span data-ttu-id="824d4-225">是-單一值</span><span class="sxs-lookup"><span data-stu-id="824d4-225">Is-Single-Valued</span></span>       | <span data-ttu-id="824d4-226">對</span><span class="sxs-lookup"><span data-stu-id="824d4-226">True</span></span>         |
| <span data-ttu-id="824d4-227">已編制索引</span><span class="sxs-lookup"><span data-stu-id="824d4-227">Is Indexed</span></span>             | <span data-ttu-id="824d4-228">否</span><span class="sxs-lookup"><span data-stu-id="824d4-228">False</span></span>        |
| <span data-ttu-id="824d4-229">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="824d4-229">In Global Catalog</span></span>      | <span data-ttu-id="824d4-230">否</span><span class="sxs-lookup"><span data-stu-id="824d4-230">False</span></span>        |
| <span data-ttu-id="824d4-231">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="824d4-231">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d4-232">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="824d4-232">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="824d4-233">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d4-233">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="824d4-234">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d4-234">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="824d4-235">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-235">Search-Flags</span></span>           | <span data-ttu-id="824d4-236">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d4-236">0x00000000</span></span>   |
| <span data-ttu-id="824d4-237">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d4-237">System-Flags</span></span>           | <span data-ttu-id="824d4-238">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d4-238">0x00000010</span></span>   |
| <span data-ttu-id="824d4-239">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="824d4-239">Classes used in</span></span>        | \-           |



 

 





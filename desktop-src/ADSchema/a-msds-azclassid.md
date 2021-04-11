---
title: ms-chap-Az-Class ID 屬性
description: AzApplication 物件上 AzRoles UI 所需的類別識別碼。
ms.assetid: cbbdc898-82b2-410e-8c9d-ae4f9641ac1a
ms.tgt_platform: multiple
keywords:
- ms-chap-Az-Class ID attribute AD Schema
- AzClassId 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Az-Class-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77d7ae6376deceaf23a9b7fa3c85ee8cb2b9748
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108153"
---
# <a name="ms-ds-az-class-id-attribute"></a><span data-ttu-id="a148a-105">ms-chap-Az-Class ID 屬性</span><span class="sxs-lookup"><span data-stu-id="a148a-105">ms-DS-Az-Class-ID attribute</span></span>

<span data-ttu-id="a148a-106">AzApplication 物件上 AzRoles UI 所需的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="a148a-106">A class ID required by the AzRoles UI on the AzApplication object.</span></span>



| <span data-ttu-id="a148a-107">進入</span><span class="sxs-lookup"><span data-stu-id="a148a-107">Entry</span></span> | <span data-ttu-id="a148a-108">值</span><span class="sxs-lookup"><span data-stu-id="a148a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a148a-109">CN</span><span class="sxs-lookup"><span data-stu-id="a148a-109">CN</span></span>                | <span data-ttu-id="a148a-110">ms-chap-Az-Class-ID</span><span class="sxs-lookup"><span data-stu-id="a148a-110">ms-DS-Az-Class-ID</span></span>                           |
| <span data-ttu-id="a148a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a148a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a148a-112">AzClassId</span><span class="sxs-lookup"><span data-stu-id="a148a-112">msDS-AzClassId</span></span>                              |
| <span data-ttu-id="a148a-113">大小</span><span class="sxs-lookup"><span data-stu-id="a148a-113">Size</span></span>              | <span data-ttu-id="a148a-114">36個字元</span><span class="sxs-lookup"><span data-stu-id="a148a-114">36 characters</span></span>                               |
| <span data-ttu-id="a148a-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a148a-115">Update Privilege</span></span>  | <span data-ttu-id="a148a-116">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="a148a-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="a148a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a148a-117">Update Frequency</span></span>  | <span data-ttu-id="a148a-118">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="a148a-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="a148a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a148a-119">Attribute-Id</span></span>      | <span data-ttu-id="a148a-120">1.2.840.113556.1.4.1816</span><span class="sxs-lookup"><span data-stu-id="a148a-120">1.2.840.113556.1.4.1816</span></span>                     |
| <span data-ttu-id="a148a-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a148a-121">System-Id-Guid</span></span>    | <span data-ttu-id="a148a-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span><span class="sxs-lookup"><span data-stu-id="a148a-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span></span>        |
| <span data-ttu-id="a148a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a148a-123">Syntax</span></span>            | [<span data-ttu-id="a148a-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a148a-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a148a-125">實作</span><span class="sxs-lookup"><span data-stu-id="a148a-125">Implementations</span></span>

-   [<span data-ttu-id="a148a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a148a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a148a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a148a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a148a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a148a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a148a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a148a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a148a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a148a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a148a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a148a-131">Windows Server 2003</span></span>



| <span data-ttu-id="a148a-132">進入</span><span class="sxs-lookup"><span data-stu-id="a148a-132">Entry</span></span> | <span data-ttu-id="a148a-133">值</span><span class="sxs-lookup"><span data-stu-id="a148a-133">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a148a-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a148a-134">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a148a-135">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a148a-136">System-Only</span></span>            | <span data-ttu-id="a148a-137">否</span><span class="sxs-lookup"><span data-stu-id="a148a-137">False</span></span>        |
| <span data-ttu-id="a148a-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a148a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a148a-139">對</span><span class="sxs-lookup"><span data-stu-id="a148a-139">True</span></span>         |
| <span data-ttu-id="a148a-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a148a-140">Is Indexed</span></span>             | <span data-ttu-id="a148a-141">否</span><span class="sxs-lookup"><span data-stu-id="a148a-141">False</span></span>        |
| <span data-ttu-id="a148a-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a148a-142">In Global Catalog</span></span>      | <span data-ttu-id="a148a-143">否</span><span class="sxs-lookup"><span data-stu-id="a148a-143">False</span></span>        |
| <span data-ttu-id="a148a-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a148a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a148a-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a148a-145">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a148a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a148a-146">Range-Lower</span></span>            | <span data-ttu-id="a148a-147">0</span><span class="sxs-lookup"><span data-stu-id="a148a-147">0</span></span>            |
| <span data-ttu-id="a148a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a148a-148">Range-Upper</span></span>            | <span data-ttu-id="a148a-149">40</span><span class="sxs-lookup"><span data-stu-id="a148a-149">40</span></span>           |
| <span data-ttu-id="a148a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-150">Search-Flags</span></span>           | <span data-ttu-id="a148a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a148a-151">0x00000000</span></span>   |
| <span data-ttu-id="a148a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-152">System-Flags</span></span>           | <span data-ttu-id="a148a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a148a-153">0x00000010</span></span>   |
| <span data-ttu-id="a148a-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a148a-154">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a148a-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a148a-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a148a-156">進入</span><span class="sxs-lookup"><span data-stu-id="a148a-156">Entry</span></span> | <span data-ttu-id="a148a-157">值</span><span class="sxs-lookup"><span data-stu-id="a148a-157">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a148a-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a148a-158">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a148a-159">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a148a-160">System-Only</span></span>            | <span data-ttu-id="a148a-161">否</span><span class="sxs-lookup"><span data-stu-id="a148a-161">False</span></span>        |
| <span data-ttu-id="a148a-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a148a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a148a-163">對</span><span class="sxs-lookup"><span data-stu-id="a148a-163">True</span></span>         |
| <span data-ttu-id="a148a-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a148a-164">Is Indexed</span></span>             | <span data-ttu-id="a148a-165">否</span><span class="sxs-lookup"><span data-stu-id="a148a-165">False</span></span>        |
| <span data-ttu-id="a148a-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a148a-166">In Global Catalog</span></span>      | <span data-ttu-id="a148a-167">否</span><span class="sxs-lookup"><span data-stu-id="a148a-167">False</span></span>        |
| <span data-ttu-id="a148a-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a148a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a148a-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a148a-169">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a148a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a148a-170">Range-Lower</span></span>            | <span data-ttu-id="a148a-171">0</span><span class="sxs-lookup"><span data-stu-id="a148a-171">0</span></span>            |
| <span data-ttu-id="a148a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a148a-172">Range-Upper</span></span>            | <span data-ttu-id="a148a-173">40</span><span class="sxs-lookup"><span data-stu-id="a148a-173">40</span></span>           |
| <span data-ttu-id="a148a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-174">Search-Flags</span></span>           | <span data-ttu-id="a148a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a148a-175">0x00000000</span></span>   |
| <span data-ttu-id="a148a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-176">System-Flags</span></span>           | <span data-ttu-id="a148a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a148a-177">0x00000010</span></span>   |
| <span data-ttu-id="a148a-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a148a-178">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="a148a-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a148a-179">Windows Server 2008</span></span>



| <span data-ttu-id="a148a-180">進入</span><span class="sxs-lookup"><span data-stu-id="a148a-180">Entry</span></span> | <span data-ttu-id="a148a-181">值</span><span class="sxs-lookup"><span data-stu-id="a148a-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a148a-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a148a-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a148a-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a148a-184">System-Only</span></span>            | <span data-ttu-id="a148a-185">否</span><span class="sxs-lookup"><span data-stu-id="a148a-185">False</span></span>        |
| <span data-ttu-id="a148a-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a148a-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a148a-187">對</span><span class="sxs-lookup"><span data-stu-id="a148a-187">True</span></span>         |
| <span data-ttu-id="a148a-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a148a-188">Is Indexed</span></span>             | <span data-ttu-id="a148a-189">否</span><span class="sxs-lookup"><span data-stu-id="a148a-189">False</span></span>        |
| <span data-ttu-id="a148a-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a148a-190">In Global Catalog</span></span>      | <span data-ttu-id="a148a-191">否</span><span class="sxs-lookup"><span data-stu-id="a148a-191">False</span></span>        |
| <span data-ttu-id="a148a-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a148a-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a148a-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a148a-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a148a-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a148a-194">Range-Lower</span></span>            | <span data-ttu-id="a148a-195">0</span><span class="sxs-lookup"><span data-stu-id="a148a-195">0</span></span>            |
| <span data-ttu-id="a148a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a148a-196">Range-Upper</span></span>            | <span data-ttu-id="a148a-197">40</span><span class="sxs-lookup"><span data-stu-id="a148a-197">40</span></span>           |
| <span data-ttu-id="a148a-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-198">Search-Flags</span></span>           | <span data-ttu-id="a148a-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a148a-199">0x00000000</span></span>   |
| <span data-ttu-id="a148a-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-200">System-Flags</span></span>           | <span data-ttu-id="a148a-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a148a-201">0x00000010</span></span>   |
| <span data-ttu-id="a148a-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a148a-202">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a148a-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a148a-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a148a-204">進入</span><span class="sxs-lookup"><span data-stu-id="a148a-204">Entry</span></span> | <span data-ttu-id="a148a-205">值</span><span class="sxs-lookup"><span data-stu-id="a148a-205">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a148a-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a148a-206">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a148a-207">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="a148a-208">System-Only</span></span>            | <span data-ttu-id="a148a-209">否</span><span class="sxs-lookup"><span data-stu-id="a148a-209">False</span></span>        |
| <span data-ttu-id="a148a-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a148a-210">Is-Single-Valued</span></span>       | <span data-ttu-id="a148a-211">對</span><span class="sxs-lookup"><span data-stu-id="a148a-211">True</span></span>         |
| <span data-ttu-id="a148a-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a148a-212">Is Indexed</span></span>             | <span data-ttu-id="a148a-213">否</span><span class="sxs-lookup"><span data-stu-id="a148a-213">False</span></span>        |
| <span data-ttu-id="a148a-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a148a-214">In Global Catalog</span></span>      | <span data-ttu-id="a148a-215">否</span><span class="sxs-lookup"><span data-stu-id="a148a-215">False</span></span>        |
| <span data-ttu-id="a148a-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a148a-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="a148a-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a148a-217">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a148a-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a148a-218">Range-Lower</span></span>            | <span data-ttu-id="a148a-219">0</span><span class="sxs-lookup"><span data-stu-id="a148a-219">0</span></span>            |
| <span data-ttu-id="a148a-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a148a-220">Range-Upper</span></span>            | <span data-ttu-id="a148a-221">40</span><span class="sxs-lookup"><span data-stu-id="a148a-221">40</span></span>           |
| <span data-ttu-id="a148a-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-222">Search-Flags</span></span>           | <span data-ttu-id="a148a-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a148a-223">0x00000000</span></span>   |
| <span data-ttu-id="a148a-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-224">System-Flags</span></span>           | <span data-ttu-id="a148a-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a148a-225">0x00000010</span></span>   |
| <span data-ttu-id="a148a-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a148a-226">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="a148a-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a148a-227">Windows Server 2012</span></span>



| <span data-ttu-id="a148a-228">進入</span><span class="sxs-lookup"><span data-stu-id="a148a-228">Entry</span></span> | <span data-ttu-id="a148a-229">值</span><span class="sxs-lookup"><span data-stu-id="a148a-229">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a148a-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a148a-230">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a148a-231">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a148a-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="a148a-232">System-Only</span></span>            | <span data-ttu-id="a148a-233">否</span><span class="sxs-lookup"><span data-stu-id="a148a-233">False</span></span>        |
| <span data-ttu-id="a148a-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a148a-234">Is-Single-Valued</span></span>       | <span data-ttu-id="a148a-235">對</span><span class="sxs-lookup"><span data-stu-id="a148a-235">True</span></span>         |
| <span data-ttu-id="a148a-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a148a-236">Is Indexed</span></span>             | <span data-ttu-id="a148a-237">否</span><span class="sxs-lookup"><span data-stu-id="a148a-237">False</span></span>        |
| <span data-ttu-id="a148a-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a148a-238">In Global Catalog</span></span>      | <span data-ttu-id="a148a-239">否</span><span class="sxs-lookup"><span data-stu-id="a148a-239">False</span></span>        |
| <span data-ttu-id="a148a-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a148a-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="a148a-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a148a-241">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a148a-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a148a-242">Range-Lower</span></span>            | <span data-ttu-id="a148a-243">0</span><span class="sxs-lookup"><span data-stu-id="a148a-243">0</span></span>            |
| <span data-ttu-id="a148a-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a148a-244">Range-Upper</span></span>            | <span data-ttu-id="a148a-245">40</span><span class="sxs-lookup"><span data-stu-id="a148a-245">40</span></span>           |
| <span data-ttu-id="a148a-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-246">Search-Flags</span></span>           | <span data-ttu-id="a148a-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a148a-247">0x00000000</span></span>   |
| <span data-ttu-id="a148a-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a148a-248">System-Flags</span></span>           | <span data-ttu-id="a148a-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a148a-249">0x00000010</span></span>   |
| <span data-ttu-id="a148a-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a148a-250">Classes used in</span></span>        | \-           |



 

 





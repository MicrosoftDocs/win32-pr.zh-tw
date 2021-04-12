---
title: ms-chap-Az-Scope-Name 屬性
description: 可唯一識別範圍物件的字串。
ms.assetid: f5a15040-c4d0-4eab-bf3f-34585768c5a3
ms.tgt_platform: multiple
keywords:
- ms DS-Az-Scope-Name 屬性 AD 架構
- AzScopeName 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Az-Scope-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b59e2989a5054253159d9f8991ef25c72688b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509708"
---
# <a name="ms-ds-az-scope-name-attribute"></a><span data-ttu-id="b2c9a-105">ms-chap-Az-Scope-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="b2c9a-105">ms-DS-Az-Scope-Name attribute</span></span>

<span data-ttu-id="b2c9a-106">可唯一識別範圍物件的字串。</span><span class="sxs-lookup"><span data-stu-id="b2c9a-106">A string that uniquely identifies a scope object.</span></span>



| <span data-ttu-id="b2c9a-107">進入</span><span class="sxs-lookup"><span data-stu-id="b2c9a-107">Entry</span></span> | <span data-ttu-id="b2c9a-108">值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b2c9a-109">CN</span><span class="sxs-lookup"><span data-stu-id="b2c9a-109">CN</span></span>                | <span data-ttu-id="b2c9a-110">ms-chap-Az-範圍名稱</span><span class="sxs-lookup"><span data-stu-id="b2c9a-110">ms-DS-Az-Scope-Name</span></span>                         |
| <span data-ttu-id="b2c9a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b2c9a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b2c9a-112">AzScopeName</span><span class="sxs-lookup"><span data-stu-id="b2c9a-112">msDS-AzScopeName</span></span>                            |
| <span data-ttu-id="b2c9a-113">大小</span><span class="sxs-lookup"><span data-stu-id="b2c9a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b2c9a-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b2c9a-114">Update Privilege</span></span>  | <span data-ttu-id="b2c9a-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="b2c9a-115">AzRoles admin</span></span>                               |
| <span data-ttu-id="b2c9a-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b2c9a-116">Update Frequency</span></span>  | <span data-ttu-id="b2c9a-117">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="b2c9a-117">During initialization or policy change.</span></span>     |
| <span data-ttu-id="b2c9a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b2c9a-118">Attribute-Id</span></span>      | <span data-ttu-id="b2c9a-119">1.2.840.113556.1.4.1799</span><span class="sxs-lookup"><span data-stu-id="b2c9a-119">1.2.840.113556.1.4.1799</span></span>                     |
| <span data-ttu-id="b2c9a-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b2c9a-120">System-Id-Guid</span></span>    | <span data-ttu-id="b2c9a-121">515a6b06-2617-4173-8099-d5605df043c6</span><span class="sxs-lookup"><span data-stu-id="b2c9a-121">515a6b06-2617-4173-8099-d5605df043c6</span></span>        |
| <span data-ttu-id="b2c9a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2c9a-122">Syntax</span></span>            | [<span data-ttu-id="b2c9a-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b2c9a-124">實作</span><span class="sxs-lookup"><span data-stu-id="b2c9a-124">Implementations</span></span>

-   [<span data-ttu-id="b2c9a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b2c9a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b2c9a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b2c9a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b2c9a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b2c9a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2c9a-130">Windows Server 2003</span></span>



| <span data-ttu-id="b2c9a-131">進入</span><span class="sxs-lookup"><span data-stu-id="b2c9a-131">Entry</span></span> | <span data-ttu-id="b2c9a-132">值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="b2c9a-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2c9a-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2c9a-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2c9a-135">System-Only</span></span>            | <span data-ttu-id="b2c9a-136">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-136">False</span></span>                                               |
| <span data-ttu-id="b2c9a-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b2c9a-138">對</span><span class="sxs-lookup"><span data-stu-id="b2c9a-138">True</span></span>                                                |
| <span data-ttu-id="b2c9a-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2c9a-139">Is Indexed</span></span>             | <span data-ttu-id="b2c9a-140">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-140">False</span></span>                                               |
| <span data-ttu-id="b2c9a-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2c9a-141">In Global Catalog</span></span>      | <span data-ttu-id="b2c9a-142">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-142">False</span></span>                                               |
| <span data-ttu-id="b2c9a-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2c9a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2c9a-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2c9a-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="b2c9a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2c9a-145">Range-Lower</span></span>            | <span data-ttu-id="b2c9a-146">0</span><span class="sxs-lookup"><span data-stu-id="b2c9a-146">0</span></span>                                                   |
| <span data-ttu-id="b2c9a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2c9a-147">Range-Upper</span></span>            | <span data-ttu-id="b2c9a-148">65536</span><span class="sxs-lookup"><span data-stu-id="b2c9a-148">65536</span></span>                                               |
| <span data-ttu-id="b2c9a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-149">Search-Flags</span></span>           | <span data-ttu-id="b2c9a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2c9a-150">0x00000000</span></span>                                          |
| <span data-ttu-id="b2c9a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-151">System-Flags</span></span>           | <span data-ttu-id="b2c9a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2c9a-152">0x00000010</span></span>                                          |
| <span data-ttu-id="b2c9a-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2c9a-153">Classes used in</span></span>        | [<span data-ttu-id="b2c9a-154">**ms DS-Az-範圍**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-154">**ms-DS-Az-Scope**</span></span>](c-msds-azscope.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b2c9a-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b2c9a-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b2c9a-156">進入</span><span class="sxs-lookup"><span data-stu-id="b2c9a-156">Entry</span></span> | <span data-ttu-id="b2c9a-157">值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-157">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="b2c9a-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2c9a-158">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2c9a-159">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2c9a-160">System-Only</span></span>            | <span data-ttu-id="b2c9a-161">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-161">False</span></span>                                               |
| <span data-ttu-id="b2c9a-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b2c9a-163">對</span><span class="sxs-lookup"><span data-stu-id="b2c9a-163">True</span></span>                                                |
| <span data-ttu-id="b2c9a-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2c9a-164">Is Indexed</span></span>             | <span data-ttu-id="b2c9a-165">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-165">False</span></span>                                               |
| <span data-ttu-id="b2c9a-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2c9a-166">In Global Catalog</span></span>      | <span data-ttu-id="b2c9a-167">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-167">False</span></span>                                               |
| <span data-ttu-id="b2c9a-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2c9a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2c9a-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2c9a-169">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="b2c9a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2c9a-170">Range-Lower</span></span>            | <span data-ttu-id="b2c9a-171">0</span><span class="sxs-lookup"><span data-stu-id="b2c9a-171">0</span></span>                                                   |
| <span data-ttu-id="b2c9a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2c9a-172">Range-Upper</span></span>            | <span data-ttu-id="b2c9a-173">65536</span><span class="sxs-lookup"><span data-stu-id="b2c9a-173">65536</span></span>                                               |
| <span data-ttu-id="b2c9a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-174">Search-Flags</span></span>           | <span data-ttu-id="b2c9a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2c9a-175">0x00000000</span></span>                                          |
| <span data-ttu-id="b2c9a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-176">System-Flags</span></span>           | <span data-ttu-id="b2c9a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2c9a-177">0x00000010</span></span>                                          |
| <span data-ttu-id="b2c9a-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2c9a-178">Classes used in</span></span>        | [<span data-ttu-id="b2c9a-179">**ms DS-Az-範圍**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-179">**ms-DS-Az-Scope**</span></span>](c-msds-azscope.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b2c9a-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2c9a-180">Windows Server 2008</span></span>



| <span data-ttu-id="b2c9a-181">進入</span><span class="sxs-lookup"><span data-stu-id="b2c9a-181">Entry</span></span> | <span data-ttu-id="b2c9a-182">值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-182">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="b2c9a-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2c9a-183">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2c9a-184">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2c9a-185">System-Only</span></span>            | <span data-ttu-id="b2c9a-186">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-186">False</span></span>                                               |
| <span data-ttu-id="b2c9a-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b2c9a-188">對</span><span class="sxs-lookup"><span data-stu-id="b2c9a-188">True</span></span>                                                |
| <span data-ttu-id="b2c9a-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2c9a-189">Is Indexed</span></span>             | <span data-ttu-id="b2c9a-190">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-190">False</span></span>                                               |
| <span data-ttu-id="b2c9a-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2c9a-191">In Global Catalog</span></span>      | <span data-ttu-id="b2c9a-192">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-192">False</span></span>                                               |
| <span data-ttu-id="b2c9a-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2c9a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2c9a-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2c9a-194">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="b2c9a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2c9a-195">Range-Lower</span></span>            | <span data-ttu-id="b2c9a-196">0</span><span class="sxs-lookup"><span data-stu-id="b2c9a-196">0</span></span>                                                   |
| <span data-ttu-id="b2c9a-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2c9a-197">Range-Upper</span></span>            | <span data-ttu-id="b2c9a-198">65536</span><span class="sxs-lookup"><span data-stu-id="b2c9a-198">65536</span></span>                                               |
| <span data-ttu-id="b2c9a-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-199">Search-Flags</span></span>           | <span data-ttu-id="b2c9a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2c9a-200">0x00000000</span></span>                                          |
| <span data-ttu-id="b2c9a-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-201">System-Flags</span></span>           | <span data-ttu-id="b2c9a-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2c9a-202">0x00000010</span></span>                                          |
| <span data-ttu-id="b2c9a-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2c9a-203">Classes used in</span></span>        | [<span data-ttu-id="b2c9a-204">**ms DS-Az-範圍**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-204">**ms-DS-Az-Scope**</span></span>](c-msds-azscope.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b2c9a-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2c9a-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b2c9a-206">進入</span><span class="sxs-lookup"><span data-stu-id="b2c9a-206">Entry</span></span> | <span data-ttu-id="b2c9a-207">值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-207">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="b2c9a-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2c9a-208">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2c9a-209">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2c9a-210">System-Only</span></span>            | <span data-ttu-id="b2c9a-211">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-211">False</span></span>                                               |
| <span data-ttu-id="b2c9a-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-212">Is-Single-Valued</span></span>       | <span data-ttu-id="b2c9a-213">對</span><span class="sxs-lookup"><span data-stu-id="b2c9a-213">True</span></span>                                                |
| <span data-ttu-id="b2c9a-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2c9a-214">Is Indexed</span></span>             | <span data-ttu-id="b2c9a-215">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-215">False</span></span>                                               |
| <span data-ttu-id="b2c9a-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2c9a-216">In Global Catalog</span></span>      | <span data-ttu-id="b2c9a-217">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-217">False</span></span>                                               |
| <span data-ttu-id="b2c9a-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2c9a-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2c9a-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2c9a-219">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="b2c9a-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2c9a-220">Range-Lower</span></span>            | <span data-ttu-id="b2c9a-221">0</span><span class="sxs-lookup"><span data-stu-id="b2c9a-221">0</span></span>                                                   |
| <span data-ttu-id="b2c9a-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2c9a-222">Range-Upper</span></span>            | <span data-ttu-id="b2c9a-223">65536</span><span class="sxs-lookup"><span data-stu-id="b2c9a-223">65536</span></span>                                               |
| <span data-ttu-id="b2c9a-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-224">Search-Flags</span></span>           | <span data-ttu-id="b2c9a-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2c9a-225">0x00000000</span></span>                                          |
| <span data-ttu-id="b2c9a-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-226">System-Flags</span></span>           | <span data-ttu-id="b2c9a-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2c9a-227">0x00000010</span></span>                                          |
| <span data-ttu-id="b2c9a-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2c9a-228">Classes used in</span></span>        | [<span data-ttu-id="b2c9a-229">**ms DS-Az-範圍**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-229">**ms-DS-Az-Scope**</span></span>](c-msds-azscope.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b2c9a-230">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2c9a-230">Windows Server 2012</span></span>



| <span data-ttu-id="b2c9a-231">進入</span><span class="sxs-lookup"><span data-stu-id="b2c9a-231">Entry</span></span> | <span data-ttu-id="b2c9a-232">值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-232">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="b2c9a-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2c9a-233">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2c9a-234">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="b2c9a-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2c9a-235">System-Only</span></span>            | <span data-ttu-id="b2c9a-236">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-236">False</span></span>                                               |
| <span data-ttu-id="b2c9a-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2c9a-237">Is-Single-Valued</span></span>       | <span data-ttu-id="b2c9a-238">對</span><span class="sxs-lookup"><span data-stu-id="b2c9a-238">True</span></span>                                                |
| <span data-ttu-id="b2c9a-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2c9a-239">Is Indexed</span></span>             | <span data-ttu-id="b2c9a-240">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-240">False</span></span>                                               |
| <span data-ttu-id="b2c9a-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2c9a-241">In Global Catalog</span></span>      | <span data-ttu-id="b2c9a-242">否</span><span class="sxs-lookup"><span data-stu-id="b2c9a-242">False</span></span>                                               |
| <span data-ttu-id="b2c9a-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2c9a-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2c9a-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2c9a-244">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="b2c9a-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2c9a-245">Range-Lower</span></span>            | <span data-ttu-id="b2c9a-246">0</span><span class="sxs-lookup"><span data-stu-id="b2c9a-246">0</span></span>                                                   |
| <span data-ttu-id="b2c9a-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2c9a-247">Range-Upper</span></span>            | <span data-ttu-id="b2c9a-248">65536</span><span class="sxs-lookup"><span data-stu-id="b2c9a-248">65536</span></span>                                               |
| <span data-ttu-id="b2c9a-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-249">Search-Flags</span></span>           | <span data-ttu-id="b2c9a-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2c9a-250">0x00000000</span></span>                                          |
| <span data-ttu-id="b2c9a-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2c9a-251">System-Flags</span></span>           | <span data-ttu-id="b2c9a-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2c9a-252">0x00000010</span></span>                                          |
| <span data-ttu-id="b2c9a-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2c9a-253">Classes used in</span></span>        | [<span data-ttu-id="b2c9a-254">**ms DS-Az-範圍**</span><span class="sxs-lookup"><span data-stu-id="b2c9a-254">**ms-DS-Az-Scope**</span></span>](c-msds-azscope.md)<br/> |



 

 






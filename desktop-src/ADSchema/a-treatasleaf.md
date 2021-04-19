---
title: 視為分葉屬性
description: 此旗標設為 TRUE 的顯示規範會強制將相關類別顯示為分葉類別，即使它有子系也一樣。
ms.assetid: 7b19fc04-69ac-4e4b-8b9b-bd1ec74fcea7
ms.tgt_platform: multiple
keywords:
- 視為分葉屬性的 AD 架構
- treatAsLeaf 屬性 AD 架構
topic_type:
- apiref
api_name:
- Treat-As-Leaf
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d357fa368818a9b216fe18a394b806e390b46b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972902"
---
# <a name="treat-as-leaf-attribute"></a><span data-ttu-id="efa9d-105">視為分葉屬性</span><span class="sxs-lookup"><span data-stu-id="efa9d-105">Treat-As-Leaf attribute</span></span>

<span data-ttu-id="efa9d-106">此旗標設為 **TRUE** 的顯示規範會強制將相關類別顯示為分葉類別，即使它有子系也一樣。</span><span class="sxs-lookup"><span data-stu-id="efa9d-106">Display-specifiers with this flag set to **TRUE** force the related class to be displayed as a leaf class even if it has children.</span></span>



| <span data-ttu-id="efa9d-107">進入</span><span class="sxs-lookup"><span data-stu-id="efa9d-107">Entry</span></span> | <span data-ttu-id="efa9d-108">值</span><span class="sxs-lookup"><span data-stu-id="efa9d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="efa9d-109">CN</span><span class="sxs-lookup"><span data-stu-id="efa9d-109">CN</span></span>                | <span data-ttu-id="efa9d-110">視為分葉</span><span class="sxs-lookup"><span data-stu-id="efa9d-110">Treat-As-Leaf</span></span>                        |
| <span data-ttu-id="efa9d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="efa9d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="efa9d-112">treatAsLeaf</span><span class="sxs-lookup"><span data-stu-id="efa9d-112">treatAsLeaf</span></span>                          |
| <span data-ttu-id="efa9d-113">大小</span><span class="sxs-lookup"><span data-stu-id="efa9d-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="efa9d-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="efa9d-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="efa9d-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="efa9d-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="efa9d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="efa9d-116">Attribute-Id</span></span>      | <span data-ttu-id="efa9d-117">1.2.840.113556.1.4.806</span><span class="sxs-lookup"><span data-stu-id="efa9d-117">1.2.840.113556.1.4.806</span></span>               |
| <span data-ttu-id="efa9d-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="efa9d-118">System-Id-Guid</span></span>    | <span data-ttu-id="efa9d-119">8fd044e3-771f-11d1-aeae-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="efa9d-119">8fd044e3-771f-11d1-aeae-0000f80367c1</span></span> |
| <span data-ttu-id="efa9d-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="efa9d-120">Syntax</span></span>            | [<span data-ttu-id="efa9d-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="efa9d-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="efa9d-122">實作</span><span class="sxs-lookup"><span data-stu-id="efa9d-122">Implementations</span></span>

-   [<span data-ttu-id="efa9d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="efa9d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="efa9d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="efa9d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="efa9d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="efa9d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="efa9d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="efa9d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="efa9d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="efa9d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="efa9d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="efa9d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="efa9d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="efa9d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="efa9d-130">進入</span><span class="sxs-lookup"><span data-stu-id="efa9d-130">Entry</span></span> | <span data-ttu-id="efa9d-131">值</span><span class="sxs-lookup"><span data-stu-id="efa9d-131">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efa9d-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="efa9d-132">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efa9d-133">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="efa9d-134">System-Only</span></span>            | <span data-ttu-id="efa9d-135">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-135">False</span></span>                                                      |
| <span data-ttu-id="efa9d-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="efa9d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="efa9d-137">對</span><span class="sxs-lookup"><span data-stu-id="efa9d-137">True</span></span>                                                       |
| <span data-ttu-id="efa9d-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="efa9d-138">Is Indexed</span></span>             | <span data-ttu-id="efa9d-139">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-139">False</span></span>                                                      |
| <span data-ttu-id="efa9d-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="efa9d-140">In Global Catalog</span></span>      | <span data-ttu-id="efa9d-141">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-141">False</span></span>                                                      |
| <span data-ttu-id="efa9d-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="efa9d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="efa9d-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="efa9d-143">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efa9d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efa9d-144">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efa9d-145">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-146">Search-Flags</span></span>           | <span data-ttu-id="efa9d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efa9d-147">0x00000000</span></span>                                                 |
| <span data-ttu-id="efa9d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-148">System-Flags</span></span>           | <span data-ttu-id="efa9d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efa9d-149">0x00000010</span></span>                                                 |
| <span data-ttu-id="efa9d-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="efa9d-150">Classes used in</span></span>        | [<span data-ttu-id="efa9d-151">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="efa9d-151">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="efa9d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="efa9d-152">Windows Server 2003</span></span>



| <span data-ttu-id="efa9d-153">進入</span><span class="sxs-lookup"><span data-stu-id="efa9d-153">Entry</span></span> | <span data-ttu-id="efa9d-154">值</span><span class="sxs-lookup"><span data-stu-id="efa9d-154">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efa9d-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="efa9d-155">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efa9d-156">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="efa9d-157">System-Only</span></span>            | <span data-ttu-id="efa9d-158">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-158">False</span></span>                                                      |
| <span data-ttu-id="efa9d-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="efa9d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="efa9d-160">對</span><span class="sxs-lookup"><span data-stu-id="efa9d-160">True</span></span>                                                       |
| <span data-ttu-id="efa9d-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="efa9d-161">Is Indexed</span></span>             | <span data-ttu-id="efa9d-162">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-162">False</span></span>                                                      |
| <span data-ttu-id="efa9d-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="efa9d-163">In Global Catalog</span></span>      | <span data-ttu-id="efa9d-164">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-164">False</span></span>                                                      |
| <span data-ttu-id="efa9d-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="efa9d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="efa9d-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="efa9d-166">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efa9d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efa9d-167">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efa9d-168">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-169">Search-Flags</span></span>           | <span data-ttu-id="efa9d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efa9d-170">0x00000000</span></span>                                                 |
| <span data-ttu-id="efa9d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-171">System-Flags</span></span>           | <span data-ttu-id="efa9d-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efa9d-172">0x00000010</span></span>                                                 |
| <span data-ttu-id="efa9d-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="efa9d-173">Classes used in</span></span>        | [<span data-ttu-id="efa9d-174">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="efa9d-174">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="efa9d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="efa9d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="efa9d-176">進入</span><span class="sxs-lookup"><span data-stu-id="efa9d-176">Entry</span></span> | <span data-ttu-id="efa9d-177">值</span><span class="sxs-lookup"><span data-stu-id="efa9d-177">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efa9d-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="efa9d-178">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efa9d-179">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="efa9d-180">System-Only</span></span>            | <span data-ttu-id="efa9d-181">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-181">False</span></span>                                                      |
| <span data-ttu-id="efa9d-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="efa9d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="efa9d-183">對</span><span class="sxs-lookup"><span data-stu-id="efa9d-183">True</span></span>                                                       |
| <span data-ttu-id="efa9d-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="efa9d-184">Is Indexed</span></span>             | <span data-ttu-id="efa9d-185">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-185">False</span></span>                                                      |
| <span data-ttu-id="efa9d-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="efa9d-186">In Global Catalog</span></span>      | <span data-ttu-id="efa9d-187">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-187">False</span></span>                                                      |
| <span data-ttu-id="efa9d-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="efa9d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="efa9d-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="efa9d-189">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efa9d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efa9d-190">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efa9d-191">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-192">Search-Flags</span></span>           | <span data-ttu-id="efa9d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efa9d-193">0x00000000</span></span>                                                 |
| <span data-ttu-id="efa9d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-194">System-Flags</span></span>           | <span data-ttu-id="efa9d-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efa9d-195">0x00000010</span></span>                                                 |
| <span data-ttu-id="efa9d-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="efa9d-196">Classes used in</span></span>        | [<span data-ttu-id="efa9d-197">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="efa9d-197">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="efa9d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efa9d-198">Windows Server 2008</span></span>



| <span data-ttu-id="efa9d-199">進入</span><span class="sxs-lookup"><span data-stu-id="efa9d-199">Entry</span></span> | <span data-ttu-id="efa9d-200">值</span><span class="sxs-lookup"><span data-stu-id="efa9d-200">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efa9d-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="efa9d-201">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efa9d-202">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="efa9d-203">System-Only</span></span>            | <span data-ttu-id="efa9d-204">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-204">False</span></span>                                                      |
| <span data-ttu-id="efa9d-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="efa9d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="efa9d-206">對</span><span class="sxs-lookup"><span data-stu-id="efa9d-206">True</span></span>                                                       |
| <span data-ttu-id="efa9d-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="efa9d-207">Is Indexed</span></span>             | <span data-ttu-id="efa9d-208">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-208">False</span></span>                                                      |
| <span data-ttu-id="efa9d-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="efa9d-209">In Global Catalog</span></span>      | <span data-ttu-id="efa9d-210">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-210">False</span></span>                                                      |
| <span data-ttu-id="efa9d-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="efa9d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="efa9d-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="efa9d-212">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efa9d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efa9d-213">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efa9d-214">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-215">Search-Flags</span></span>           | <span data-ttu-id="efa9d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efa9d-216">0x00000000</span></span>                                                 |
| <span data-ttu-id="efa9d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-217">System-Flags</span></span>           | <span data-ttu-id="efa9d-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efa9d-218">0x00000010</span></span>                                                 |
| <span data-ttu-id="efa9d-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="efa9d-219">Classes used in</span></span>        | [<span data-ttu-id="efa9d-220">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="efa9d-220">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="efa9d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="efa9d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="efa9d-222">進入</span><span class="sxs-lookup"><span data-stu-id="efa9d-222">Entry</span></span> | <span data-ttu-id="efa9d-223">值</span><span class="sxs-lookup"><span data-stu-id="efa9d-223">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efa9d-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="efa9d-224">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efa9d-225">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="efa9d-226">System-Only</span></span>            | <span data-ttu-id="efa9d-227">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-227">False</span></span>                                                      |
| <span data-ttu-id="efa9d-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="efa9d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="efa9d-229">對</span><span class="sxs-lookup"><span data-stu-id="efa9d-229">True</span></span>                                                       |
| <span data-ttu-id="efa9d-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="efa9d-230">Is Indexed</span></span>             | <span data-ttu-id="efa9d-231">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-231">False</span></span>                                                      |
| <span data-ttu-id="efa9d-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="efa9d-232">In Global Catalog</span></span>      | <span data-ttu-id="efa9d-233">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-233">False</span></span>                                                      |
| <span data-ttu-id="efa9d-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="efa9d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="efa9d-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="efa9d-235">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efa9d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efa9d-236">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efa9d-237">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-238">Search-Flags</span></span>           | <span data-ttu-id="efa9d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efa9d-239">0x00000000</span></span>                                                 |
| <span data-ttu-id="efa9d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-240">System-Flags</span></span>           | <span data-ttu-id="efa9d-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efa9d-241">0x00000010</span></span>                                                 |
| <span data-ttu-id="efa9d-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="efa9d-242">Classes used in</span></span>        | [<span data-ttu-id="efa9d-243">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="efa9d-243">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="efa9d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="efa9d-244">Windows Server 2012</span></span>



| <span data-ttu-id="efa9d-245">進入</span><span class="sxs-lookup"><span data-stu-id="efa9d-245">Entry</span></span> | <span data-ttu-id="efa9d-246">值</span><span class="sxs-lookup"><span data-stu-id="efa9d-246">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efa9d-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="efa9d-247">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efa9d-248">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efa9d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="efa9d-249">System-Only</span></span>            | <span data-ttu-id="efa9d-250">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-250">False</span></span>                                                      |
| <span data-ttu-id="efa9d-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="efa9d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="efa9d-252">對</span><span class="sxs-lookup"><span data-stu-id="efa9d-252">True</span></span>                                                       |
| <span data-ttu-id="efa9d-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="efa9d-253">Is Indexed</span></span>             | <span data-ttu-id="efa9d-254">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-254">False</span></span>                                                      |
| <span data-ttu-id="efa9d-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="efa9d-255">In Global Catalog</span></span>      | <span data-ttu-id="efa9d-256">否</span><span class="sxs-lookup"><span data-stu-id="efa9d-256">False</span></span>                                                      |
| <span data-ttu-id="efa9d-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="efa9d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="efa9d-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="efa9d-258">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efa9d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efa9d-259">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efa9d-260">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efa9d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-261">Search-Flags</span></span>           | <span data-ttu-id="efa9d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efa9d-262">0x00000000</span></span>                                                 |
| <span data-ttu-id="efa9d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efa9d-263">System-Flags</span></span>           | <span data-ttu-id="efa9d-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efa9d-264">0x00000010</span></span>                                                 |
| <span data-ttu-id="efa9d-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="efa9d-265">Classes used in</span></span>        | [<span data-ttu-id="efa9d-266">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="efa9d-266">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 






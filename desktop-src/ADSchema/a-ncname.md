---
title: NC-Name 屬性
description: 物件之命名內容的分辨名稱。
ms.assetid: c60294b6-b803-49b4-9c94-6c0b82a45a9c
ms.tgt_platform: multiple
keywords:
- NC-Name 屬性 AD 架構
- nCName 屬性 AD 架構
topic_type:
- apiref
api_name:
- NC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152083e53950be81f2942ac217691989d5eb07b7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970263"
---
# <a name="nc-name-attribute"></a><span data-ttu-id="874b6-105">NC-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="874b6-105">NC-Name attribute</span></span>

<span data-ttu-id="874b6-106">物件之命名內容的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="874b6-106">The distinguished name of the Naming Context for the object.</span></span>



| <span data-ttu-id="874b6-107">進入</span><span class="sxs-lookup"><span data-stu-id="874b6-107">Entry</span></span> | <span data-ttu-id="874b6-108">值</span><span class="sxs-lookup"><span data-stu-id="874b6-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="874b6-109">CN</span><span class="sxs-lookup"><span data-stu-id="874b6-109">CN</span></span>                | <span data-ttu-id="874b6-110">NC-Name</span><span class="sxs-lookup"><span data-stu-id="874b6-110">NC-Name</span></span>                                 |
| <span data-ttu-id="874b6-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="874b6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="874b6-112">nCName</span><span class="sxs-lookup"><span data-stu-id="874b6-112">nCName</span></span>                                  |
| <span data-ttu-id="874b6-113">大小</span><span class="sxs-lookup"><span data-stu-id="874b6-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="874b6-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="874b6-114">Update Privilege</span></span>  | <span data-ttu-id="874b6-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="874b6-115">Domain administrator</span></span>                    |
| <span data-ttu-id="874b6-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="874b6-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="874b6-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="874b6-117">Attribute-Id</span></span>      | <span data-ttu-id="874b6-118">1.2.840.113556.1.2.16</span><span class="sxs-lookup"><span data-stu-id="874b6-118">1.2.840.113556.1.2.16</span></span>                   |
| <span data-ttu-id="874b6-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="874b6-119">System-Id-Guid</span></span>    | <span data-ttu-id="874b6-120">bf9679d6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="874b6-120">bf9679d6-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="874b6-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="874b6-121">Syntax</span></span>            | [<span data-ttu-id="874b6-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="874b6-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="874b6-123">實作</span><span class="sxs-lookup"><span data-stu-id="874b6-123">Implementations</span></span>

-   [<span data-ttu-id="874b6-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="874b6-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="874b6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="874b6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="874b6-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="874b6-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="874b6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="874b6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="874b6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="874b6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="874b6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="874b6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="874b6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="874b6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="874b6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="874b6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="874b6-132">進入</span><span class="sxs-lookup"><span data-stu-id="874b6-132">Entry</span></span> | <span data-ttu-id="874b6-133">值</span><span class="sxs-lookup"><span data-stu-id="874b6-133">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="874b6-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="874b6-134">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="874b6-135">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="874b6-136">System-Only</span></span>            | <span data-ttu-id="874b6-137">對</span><span class="sxs-lookup"><span data-stu-id="874b6-137">True</span></span>                                       |
| <span data-ttu-id="874b6-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="874b6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="874b6-139">對</span><span class="sxs-lookup"><span data-stu-id="874b6-139">True</span></span>                                       |
| <span data-ttu-id="874b6-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="874b6-140">Is Indexed</span></span>             | <span data-ttu-id="874b6-141">否</span><span class="sxs-lookup"><span data-stu-id="874b6-141">False</span></span>                                      |
| <span data-ttu-id="874b6-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="874b6-142">In Global Catalog</span></span>      | <span data-ttu-id="874b6-143">否</span><span class="sxs-lookup"><span data-stu-id="874b6-143">False</span></span>                                      |
| <span data-ttu-id="874b6-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="874b6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="874b6-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="874b6-145">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="874b6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="874b6-146">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="874b6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="874b6-147">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="874b6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-148">Search-Flags</span></span>           | <span data-ttu-id="874b6-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="874b6-149">0x00000008</span></span>                                 |
| <span data-ttu-id="874b6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-150">System-Flags</span></span>           | <span data-ttu-id="874b6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="874b6-151">0x00000010</span></span>                                 |
| <span data-ttu-id="874b6-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="874b6-152">Classes used in</span></span>        | [<span data-ttu-id="874b6-153">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="874b6-153">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="874b6-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="874b6-154">Windows Server 2003</span></span>



| <span data-ttu-id="874b6-155">進入</span><span class="sxs-lookup"><span data-stu-id="874b6-155">Entry</span></span> | <span data-ttu-id="874b6-156">值</span><span class="sxs-lookup"><span data-stu-id="874b6-156">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="874b6-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="874b6-157">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="874b6-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="874b6-159">System-Only</span></span>            | <span data-ttu-id="874b6-160">對</span><span class="sxs-lookup"><span data-stu-id="874b6-160">True</span></span>                                       |
| <span data-ttu-id="874b6-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="874b6-161">Is-Single-Valued</span></span>       | <span data-ttu-id="874b6-162">對</span><span class="sxs-lookup"><span data-stu-id="874b6-162">True</span></span>                                       |
| <span data-ttu-id="874b6-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="874b6-163">Is Indexed</span></span>             | <span data-ttu-id="874b6-164">否</span><span class="sxs-lookup"><span data-stu-id="874b6-164">False</span></span>                                      |
| <span data-ttu-id="874b6-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="874b6-165">In Global Catalog</span></span>      | <span data-ttu-id="874b6-166">否</span><span class="sxs-lookup"><span data-stu-id="874b6-166">False</span></span>                                      |
| <span data-ttu-id="874b6-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="874b6-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="874b6-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="874b6-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="874b6-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="874b6-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="874b6-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="874b6-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="874b6-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-171">Search-Flags</span></span>           | <span data-ttu-id="874b6-172">0x00000008</span><span class="sxs-lookup"><span data-stu-id="874b6-172">0x00000008</span></span>                                 |
| <span data-ttu-id="874b6-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-173">System-Flags</span></span>           | <span data-ttu-id="874b6-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="874b6-174">0x00000010</span></span>                                 |
| <span data-ttu-id="874b6-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="874b6-175">Classes used in</span></span>        | [<span data-ttu-id="874b6-176">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="874b6-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="874b6-177">亞當</span><span class="sxs-lookup"><span data-stu-id="874b6-177">ADAM</span></span>



| <span data-ttu-id="874b6-178">進入</span><span class="sxs-lookup"><span data-stu-id="874b6-178">Entry</span></span> | <span data-ttu-id="874b6-179">值</span><span class="sxs-lookup"><span data-stu-id="874b6-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="874b6-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="874b6-180">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="874b6-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="874b6-182">System-Only</span></span>            | <span data-ttu-id="874b6-183">對</span><span class="sxs-lookup"><span data-stu-id="874b6-183">True</span></span>                                       |
| <span data-ttu-id="874b6-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="874b6-184">Is-Single-Valued</span></span>       | <span data-ttu-id="874b6-185">對</span><span class="sxs-lookup"><span data-stu-id="874b6-185">True</span></span>                                       |
| <span data-ttu-id="874b6-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="874b6-186">Is Indexed</span></span>             | <span data-ttu-id="874b6-187">否</span><span class="sxs-lookup"><span data-stu-id="874b6-187">False</span></span>                                      |
| <span data-ttu-id="874b6-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="874b6-188">In Global Catalog</span></span>      | <span data-ttu-id="874b6-189">否</span><span class="sxs-lookup"><span data-stu-id="874b6-189">False</span></span>                                      |
| <span data-ttu-id="874b6-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="874b6-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="874b6-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="874b6-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="874b6-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="874b6-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="874b6-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="874b6-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="874b6-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-194">Search-Flags</span></span>           | <span data-ttu-id="874b6-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="874b6-195">0x00000008</span></span>                                 |
| <span data-ttu-id="874b6-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-196">System-Flags</span></span>           | <span data-ttu-id="874b6-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="874b6-197">0x00000010</span></span>                                 |
| <span data-ttu-id="874b6-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="874b6-198">Classes used in</span></span>        | [<span data-ttu-id="874b6-199">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="874b6-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="874b6-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="874b6-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="874b6-201">進入</span><span class="sxs-lookup"><span data-stu-id="874b6-201">Entry</span></span> | <span data-ttu-id="874b6-202">值</span><span class="sxs-lookup"><span data-stu-id="874b6-202">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="874b6-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="874b6-203">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="874b6-204">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="874b6-205">System-Only</span></span>            | <span data-ttu-id="874b6-206">對</span><span class="sxs-lookup"><span data-stu-id="874b6-206">True</span></span>                                       |
| <span data-ttu-id="874b6-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="874b6-207">Is-Single-Valued</span></span>       | <span data-ttu-id="874b6-208">對</span><span class="sxs-lookup"><span data-stu-id="874b6-208">True</span></span>                                       |
| <span data-ttu-id="874b6-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="874b6-209">Is Indexed</span></span>             | <span data-ttu-id="874b6-210">否</span><span class="sxs-lookup"><span data-stu-id="874b6-210">False</span></span>                                      |
| <span data-ttu-id="874b6-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="874b6-211">In Global Catalog</span></span>      | <span data-ttu-id="874b6-212">否</span><span class="sxs-lookup"><span data-stu-id="874b6-212">False</span></span>                                      |
| <span data-ttu-id="874b6-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="874b6-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="874b6-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="874b6-214">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="874b6-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="874b6-215">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="874b6-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="874b6-216">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="874b6-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-217">Search-Flags</span></span>           | <span data-ttu-id="874b6-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="874b6-218">0x00000008</span></span>                                 |
| <span data-ttu-id="874b6-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-219">System-Flags</span></span>           | <span data-ttu-id="874b6-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="874b6-220">0x00000010</span></span>                                 |
| <span data-ttu-id="874b6-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="874b6-221">Classes used in</span></span>        | [<span data-ttu-id="874b6-222">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="874b6-222">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="874b6-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="874b6-223">Windows Server 2008</span></span>



| <span data-ttu-id="874b6-224">進入</span><span class="sxs-lookup"><span data-stu-id="874b6-224">Entry</span></span> | <span data-ttu-id="874b6-225">值</span><span class="sxs-lookup"><span data-stu-id="874b6-225">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="874b6-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="874b6-226">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="874b6-227">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="874b6-228">System-Only</span></span>            | <span data-ttu-id="874b6-229">對</span><span class="sxs-lookup"><span data-stu-id="874b6-229">True</span></span>                                       |
| <span data-ttu-id="874b6-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="874b6-230">Is-Single-Valued</span></span>       | <span data-ttu-id="874b6-231">對</span><span class="sxs-lookup"><span data-stu-id="874b6-231">True</span></span>                                       |
| <span data-ttu-id="874b6-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="874b6-232">Is Indexed</span></span>             | <span data-ttu-id="874b6-233">否</span><span class="sxs-lookup"><span data-stu-id="874b6-233">False</span></span>                                      |
| <span data-ttu-id="874b6-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="874b6-234">In Global Catalog</span></span>      | <span data-ttu-id="874b6-235">否</span><span class="sxs-lookup"><span data-stu-id="874b6-235">False</span></span>                                      |
| <span data-ttu-id="874b6-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="874b6-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="874b6-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="874b6-237">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="874b6-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="874b6-238">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="874b6-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="874b6-239">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="874b6-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-240">Search-Flags</span></span>           | <span data-ttu-id="874b6-241">0x00000008</span><span class="sxs-lookup"><span data-stu-id="874b6-241">0x00000008</span></span>                                 |
| <span data-ttu-id="874b6-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-242">System-Flags</span></span>           | <span data-ttu-id="874b6-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="874b6-243">0x00000010</span></span>                                 |
| <span data-ttu-id="874b6-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="874b6-244">Classes used in</span></span>        | [<span data-ttu-id="874b6-245">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="874b6-245">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="874b6-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="874b6-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="874b6-247">進入</span><span class="sxs-lookup"><span data-stu-id="874b6-247">Entry</span></span> | <span data-ttu-id="874b6-248">值</span><span class="sxs-lookup"><span data-stu-id="874b6-248">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="874b6-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="874b6-249">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="874b6-250">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="874b6-251">System-Only</span></span>            | <span data-ttu-id="874b6-252">對</span><span class="sxs-lookup"><span data-stu-id="874b6-252">True</span></span>                                       |
| <span data-ttu-id="874b6-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="874b6-253">Is-Single-Valued</span></span>       | <span data-ttu-id="874b6-254">對</span><span class="sxs-lookup"><span data-stu-id="874b6-254">True</span></span>                                       |
| <span data-ttu-id="874b6-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="874b6-255">Is Indexed</span></span>             | <span data-ttu-id="874b6-256">否</span><span class="sxs-lookup"><span data-stu-id="874b6-256">False</span></span>                                      |
| <span data-ttu-id="874b6-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="874b6-257">In Global Catalog</span></span>      | <span data-ttu-id="874b6-258">否</span><span class="sxs-lookup"><span data-stu-id="874b6-258">False</span></span>                                      |
| <span data-ttu-id="874b6-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="874b6-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="874b6-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="874b6-260">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="874b6-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="874b6-261">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="874b6-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="874b6-262">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="874b6-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-263">Search-Flags</span></span>           | <span data-ttu-id="874b6-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="874b6-264">0x00000008</span></span>                                 |
| <span data-ttu-id="874b6-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-265">System-Flags</span></span>           | <span data-ttu-id="874b6-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="874b6-266">0x00000010</span></span>                                 |
| <span data-ttu-id="874b6-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="874b6-267">Classes used in</span></span>        | [<span data-ttu-id="874b6-268">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="874b6-268">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="874b6-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="874b6-269">Windows Server 2012</span></span>



| <span data-ttu-id="874b6-270">進入</span><span class="sxs-lookup"><span data-stu-id="874b6-270">Entry</span></span> | <span data-ttu-id="874b6-271">值</span><span class="sxs-lookup"><span data-stu-id="874b6-271">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="874b6-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="874b6-272">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="874b6-273">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="874b6-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="874b6-274">System-Only</span></span>            | <span data-ttu-id="874b6-275">對</span><span class="sxs-lookup"><span data-stu-id="874b6-275">True</span></span>                                       |
| <span data-ttu-id="874b6-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="874b6-276">Is-Single-Valued</span></span>       | <span data-ttu-id="874b6-277">對</span><span class="sxs-lookup"><span data-stu-id="874b6-277">True</span></span>                                       |
| <span data-ttu-id="874b6-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="874b6-278">Is Indexed</span></span>             | <span data-ttu-id="874b6-279">否</span><span class="sxs-lookup"><span data-stu-id="874b6-279">False</span></span>                                      |
| <span data-ttu-id="874b6-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="874b6-280">In Global Catalog</span></span>      | <span data-ttu-id="874b6-281">否</span><span class="sxs-lookup"><span data-stu-id="874b6-281">False</span></span>                                      |
| <span data-ttu-id="874b6-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="874b6-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="874b6-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="874b6-283">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="874b6-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="874b6-284">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="874b6-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="874b6-285">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="874b6-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-286">Search-Flags</span></span>           | <span data-ttu-id="874b6-287">0x00000008</span><span class="sxs-lookup"><span data-stu-id="874b6-287">0x00000008</span></span>                                 |
| <span data-ttu-id="874b6-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="874b6-288">System-Flags</span></span>           | <span data-ttu-id="874b6-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="874b6-289">0x00000010</span></span>                                 |
| <span data-ttu-id="874b6-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="874b6-290">Classes used in</span></span>        | [<span data-ttu-id="874b6-291">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="874b6-291">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






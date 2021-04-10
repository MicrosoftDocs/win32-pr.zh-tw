---
title: 主要群組-Token 屬性
description: 用來抓取群組成員資格清單的計算屬性，例如網域使用者。 這類群組的完整成員資格不會因調整原因而明確儲存。
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- 主要群組-Token 屬性 AD 架構
- primaryGroupToken 屬性 AD 架構
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107609"
---
# <a name="primary-group-token-attribute"></a><span data-ttu-id="282d7-106">主要群組-Token 屬性</span><span class="sxs-lookup"><span data-stu-id="282d7-106">Primary-Group-Token attribute</span></span>

<span data-ttu-id="282d7-107">用來抓取群組成員資格清單的計算屬性，例如網域使用者。</span><span class="sxs-lookup"><span data-stu-id="282d7-107">A computed attribute that is used in retrieving the membership list of a group, such as Domain Users.</span></span> <span data-ttu-id="282d7-108">這類群組的完整成員資格不會因調整原因而明確儲存。</span><span class="sxs-lookup"><span data-stu-id="282d7-108">The complete membership of such groups is not stored explicitly for scaling reasons.</span></span>



| <span data-ttu-id="282d7-109">進入</span><span class="sxs-lookup"><span data-stu-id="282d7-109">Entry</span></span> | <span data-ttu-id="282d7-110">值</span><span class="sxs-lookup"><span data-stu-id="282d7-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="282d7-111">CN</span><span class="sxs-lookup"><span data-stu-id="282d7-111">CN</span></span>                | <span data-ttu-id="282d7-112">主要群組-Token</span><span class="sxs-lookup"><span data-stu-id="282d7-112">Primary-Group-Token</span></span>                        |
| <span data-ttu-id="282d7-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="282d7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="282d7-114">primaryGroupToken</span><span class="sxs-lookup"><span data-stu-id="282d7-114">primaryGroupToken</span></span>                          |
| <span data-ttu-id="282d7-115">大小</span><span class="sxs-lookup"><span data-stu-id="282d7-115">Size</span></span>              | <span data-ttu-id="282d7-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="282d7-116">4 bytes</span></span>                                    |
| <span data-ttu-id="282d7-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="282d7-117">Update Privilege</span></span>  | <span data-ttu-id="282d7-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="282d7-118">This value is set by the system.</span></span>           |
| <span data-ttu-id="282d7-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="282d7-119">Update Frequency</span></span>  | <span data-ttu-id="282d7-120">每次物件主要群組變更時。</span><span class="sxs-lookup"><span data-stu-id="282d7-120">Whenever an objects primary group changes.</span></span> |
| <span data-ttu-id="282d7-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="282d7-121">Attribute-Id</span></span>      | <span data-ttu-id="282d7-122">1.2.840.113556.1.4.1412</span><span class="sxs-lookup"><span data-stu-id="282d7-122">1.2.840.113556.1.4.1412</span></span>                    |
| <span data-ttu-id="282d7-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="282d7-123">System-Id-Guid</span></span>    | <span data-ttu-id="282d7-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span><span class="sxs-lookup"><span data-stu-id="282d7-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span></span>       |
| <span data-ttu-id="282d7-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="282d7-125">Syntax</span></span>            | [<span data-ttu-id="282d7-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="282d7-126">**Enumeration**</span></span>](s-enumeration.md)       |



## <a name="implementations"></a><span data-ttu-id="282d7-127">實作</span><span class="sxs-lookup"><span data-stu-id="282d7-127">Implementations</span></span>

-   [<span data-ttu-id="282d7-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="282d7-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="282d7-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="282d7-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="282d7-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="282d7-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="282d7-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="282d7-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="282d7-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="282d7-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="282d7-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="282d7-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="282d7-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="282d7-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="282d7-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="282d7-135">Windows 2000 Server</span></span>



| <span data-ttu-id="282d7-136">進入</span><span class="sxs-lookup"><span data-stu-id="282d7-136">Entry</span></span> | <span data-ttu-id="282d7-137">值</span><span class="sxs-lookup"><span data-stu-id="282d7-137">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="282d7-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="282d7-138">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="282d7-139">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="282d7-140">System-Only</span></span>            | <span data-ttu-id="282d7-141">對</span><span class="sxs-lookup"><span data-stu-id="282d7-141">True</span></span>                                |
| <span data-ttu-id="282d7-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="282d7-142">Is-Single-Valued</span></span>       | <span data-ttu-id="282d7-143">對</span><span class="sxs-lookup"><span data-stu-id="282d7-143">True</span></span>                                |
| <span data-ttu-id="282d7-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="282d7-144">Is Indexed</span></span>             | <span data-ttu-id="282d7-145">否</span><span class="sxs-lookup"><span data-stu-id="282d7-145">False</span></span>                               |
| <span data-ttu-id="282d7-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="282d7-146">In Global Catalog</span></span>      | <span data-ttu-id="282d7-147">否</span><span class="sxs-lookup"><span data-stu-id="282d7-147">False</span></span>                               |
| <span data-ttu-id="282d7-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="282d7-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="282d7-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="282d7-149">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="282d7-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="282d7-150">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="282d7-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="282d7-151">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="282d7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-152">Search-Flags</span></span>           | <span data-ttu-id="282d7-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="282d7-153">0x00000000</span></span>                          |
| <span data-ttu-id="282d7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-154">System-Flags</span></span>           | <span data-ttu-id="282d7-155">0x00000014</span><span class="sxs-lookup"><span data-stu-id="282d7-155">0x00000014</span></span>                          |
| <span data-ttu-id="282d7-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="282d7-156">Classes used in</span></span>        | [<span data-ttu-id="282d7-157">**Group**</span><span class="sxs-lookup"><span data-stu-id="282d7-157">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="282d7-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="282d7-158">Windows Server 2003</span></span>



| <span data-ttu-id="282d7-159">進入</span><span class="sxs-lookup"><span data-stu-id="282d7-159">Entry</span></span> | <span data-ttu-id="282d7-160">值</span><span class="sxs-lookup"><span data-stu-id="282d7-160">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="282d7-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="282d7-161">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="282d7-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="282d7-163">System-Only</span></span>            | <span data-ttu-id="282d7-164">對</span><span class="sxs-lookup"><span data-stu-id="282d7-164">True</span></span>                                |
| <span data-ttu-id="282d7-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="282d7-165">Is-Single-Valued</span></span>       | <span data-ttu-id="282d7-166">對</span><span class="sxs-lookup"><span data-stu-id="282d7-166">True</span></span>                                |
| <span data-ttu-id="282d7-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="282d7-167">Is Indexed</span></span>             | <span data-ttu-id="282d7-168">否</span><span class="sxs-lookup"><span data-stu-id="282d7-168">False</span></span>                               |
| <span data-ttu-id="282d7-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="282d7-169">In Global Catalog</span></span>      | <span data-ttu-id="282d7-170">否</span><span class="sxs-lookup"><span data-stu-id="282d7-170">False</span></span>                               |
| <span data-ttu-id="282d7-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="282d7-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="282d7-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="282d7-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="282d7-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="282d7-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="282d7-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="282d7-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="282d7-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-175">Search-Flags</span></span>           | <span data-ttu-id="282d7-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="282d7-176">0x00000000</span></span>                          |
| <span data-ttu-id="282d7-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-177">System-Flags</span></span>           | <span data-ttu-id="282d7-178">0x00000014</span><span class="sxs-lookup"><span data-stu-id="282d7-178">0x00000014</span></span>                          |
| <span data-ttu-id="282d7-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="282d7-179">Classes used in</span></span>        | [<span data-ttu-id="282d7-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="282d7-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="282d7-181">亞當</span><span class="sxs-lookup"><span data-stu-id="282d7-181">ADAM</span></span>



| <span data-ttu-id="282d7-182">進入</span><span class="sxs-lookup"><span data-stu-id="282d7-182">Entry</span></span> | <span data-ttu-id="282d7-183">值</span><span class="sxs-lookup"><span data-stu-id="282d7-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="282d7-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="282d7-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="282d7-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="282d7-186">System-Only</span></span>            | <span data-ttu-id="282d7-187">對</span><span class="sxs-lookup"><span data-stu-id="282d7-187">True</span></span>                                |
| <span data-ttu-id="282d7-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="282d7-188">Is-Single-Valued</span></span>       | <span data-ttu-id="282d7-189">對</span><span class="sxs-lookup"><span data-stu-id="282d7-189">True</span></span>                                |
| <span data-ttu-id="282d7-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="282d7-190">Is Indexed</span></span>             | <span data-ttu-id="282d7-191">否</span><span class="sxs-lookup"><span data-stu-id="282d7-191">False</span></span>                               |
| <span data-ttu-id="282d7-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="282d7-192">In Global Catalog</span></span>      | <span data-ttu-id="282d7-193">否</span><span class="sxs-lookup"><span data-stu-id="282d7-193">False</span></span>                               |
| <span data-ttu-id="282d7-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="282d7-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="282d7-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="282d7-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="282d7-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="282d7-196">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="282d7-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="282d7-197">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="282d7-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-198">Search-Flags</span></span>           | <span data-ttu-id="282d7-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="282d7-199">0x00000000</span></span>                          |
| <span data-ttu-id="282d7-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-200">System-Flags</span></span>           | <span data-ttu-id="282d7-201">0x00000014</span><span class="sxs-lookup"><span data-stu-id="282d7-201">0x00000014</span></span>                          |
| <span data-ttu-id="282d7-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="282d7-202">Classes used in</span></span>        | [<span data-ttu-id="282d7-203">**Group**</span><span class="sxs-lookup"><span data-stu-id="282d7-203">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="282d7-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="282d7-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="282d7-205">進入</span><span class="sxs-lookup"><span data-stu-id="282d7-205">Entry</span></span> | <span data-ttu-id="282d7-206">值</span><span class="sxs-lookup"><span data-stu-id="282d7-206">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="282d7-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="282d7-207">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="282d7-208">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="282d7-209">System-Only</span></span>            | <span data-ttu-id="282d7-210">對</span><span class="sxs-lookup"><span data-stu-id="282d7-210">True</span></span>                                |
| <span data-ttu-id="282d7-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="282d7-211">Is-Single-Valued</span></span>       | <span data-ttu-id="282d7-212">對</span><span class="sxs-lookup"><span data-stu-id="282d7-212">True</span></span>                                |
| <span data-ttu-id="282d7-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="282d7-213">Is Indexed</span></span>             | <span data-ttu-id="282d7-214">否</span><span class="sxs-lookup"><span data-stu-id="282d7-214">False</span></span>                               |
| <span data-ttu-id="282d7-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="282d7-215">In Global Catalog</span></span>      | <span data-ttu-id="282d7-216">否</span><span class="sxs-lookup"><span data-stu-id="282d7-216">False</span></span>                               |
| <span data-ttu-id="282d7-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="282d7-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="282d7-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="282d7-218">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="282d7-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="282d7-219">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="282d7-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="282d7-220">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="282d7-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-221">Search-Flags</span></span>           | <span data-ttu-id="282d7-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="282d7-222">0x00000000</span></span>                          |
| <span data-ttu-id="282d7-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-223">System-Flags</span></span>           | <span data-ttu-id="282d7-224">0x00000014</span><span class="sxs-lookup"><span data-stu-id="282d7-224">0x00000014</span></span>                          |
| <span data-ttu-id="282d7-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="282d7-225">Classes used in</span></span>        | [<span data-ttu-id="282d7-226">**Group**</span><span class="sxs-lookup"><span data-stu-id="282d7-226">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="282d7-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="282d7-227">Windows Server 2008</span></span>



| <span data-ttu-id="282d7-228">進入</span><span class="sxs-lookup"><span data-stu-id="282d7-228">Entry</span></span> | <span data-ttu-id="282d7-229">值</span><span class="sxs-lookup"><span data-stu-id="282d7-229">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="282d7-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="282d7-230">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="282d7-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="282d7-232">System-Only</span></span>            | <span data-ttu-id="282d7-233">對</span><span class="sxs-lookup"><span data-stu-id="282d7-233">True</span></span>                                |
| <span data-ttu-id="282d7-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="282d7-234">Is-Single-Valued</span></span>       | <span data-ttu-id="282d7-235">對</span><span class="sxs-lookup"><span data-stu-id="282d7-235">True</span></span>                                |
| <span data-ttu-id="282d7-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="282d7-236">Is Indexed</span></span>             | <span data-ttu-id="282d7-237">否</span><span class="sxs-lookup"><span data-stu-id="282d7-237">False</span></span>                               |
| <span data-ttu-id="282d7-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="282d7-238">In Global Catalog</span></span>      | <span data-ttu-id="282d7-239">否</span><span class="sxs-lookup"><span data-stu-id="282d7-239">False</span></span>                               |
| <span data-ttu-id="282d7-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="282d7-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="282d7-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="282d7-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="282d7-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="282d7-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="282d7-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="282d7-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="282d7-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-244">Search-Flags</span></span>           | <span data-ttu-id="282d7-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="282d7-245">0x00000000</span></span>                          |
| <span data-ttu-id="282d7-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-246">System-Flags</span></span>           | <span data-ttu-id="282d7-247">0x00000014</span><span class="sxs-lookup"><span data-stu-id="282d7-247">0x00000014</span></span>                          |
| <span data-ttu-id="282d7-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="282d7-248">Classes used in</span></span>        | [<span data-ttu-id="282d7-249">**Group**</span><span class="sxs-lookup"><span data-stu-id="282d7-249">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="282d7-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="282d7-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="282d7-251">進入</span><span class="sxs-lookup"><span data-stu-id="282d7-251">Entry</span></span> | <span data-ttu-id="282d7-252">值</span><span class="sxs-lookup"><span data-stu-id="282d7-252">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="282d7-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="282d7-253">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="282d7-254">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="282d7-255">System-Only</span></span>            | <span data-ttu-id="282d7-256">對</span><span class="sxs-lookup"><span data-stu-id="282d7-256">True</span></span>                                |
| <span data-ttu-id="282d7-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="282d7-257">Is-Single-Valued</span></span>       | <span data-ttu-id="282d7-258">對</span><span class="sxs-lookup"><span data-stu-id="282d7-258">True</span></span>                                |
| <span data-ttu-id="282d7-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="282d7-259">Is Indexed</span></span>             | <span data-ttu-id="282d7-260">否</span><span class="sxs-lookup"><span data-stu-id="282d7-260">False</span></span>                               |
| <span data-ttu-id="282d7-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="282d7-261">In Global Catalog</span></span>      | <span data-ttu-id="282d7-262">否</span><span class="sxs-lookup"><span data-stu-id="282d7-262">False</span></span>                               |
| <span data-ttu-id="282d7-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="282d7-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="282d7-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="282d7-264">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="282d7-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="282d7-265">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="282d7-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="282d7-266">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="282d7-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-267">Search-Flags</span></span>           | <span data-ttu-id="282d7-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="282d7-268">0x00000000</span></span>                          |
| <span data-ttu-id="282d7-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-269">System-Flags</span></span>           | <span data-ttu-id="282d7-270">0x00000014</span><span class="sxs-lookup"><span data-stu-id="282d7-270">0x00000014</span></span>                          |
| <span data-ttu-id="282d7-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="282d7-271">Classes used in</span></span>        | [<span data-ttu-id="282d7-272">**Group**</span><span class="sxs-lookup"><span data-stu-id="282d7-272">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="282d7-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="282d7-273">Windows Server 2012</span></span>



| <span data-ttu-id="282d7-274">進入</span><span class="sxs-lookup"><span data-stu-id="282d7-274">Entry</span></span> | <span data-ttu-id="282d7-275">值</span><span class="sxs-lookup"><span data-stu-id="282d7-275">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="282d7-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="282d7-276">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="282d7-277">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="282d7-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="282d7-278">System-Only</span></span>            | <span data-ttu-id="282d7-279">對</span><span class="sxs-lookup"><span data-stu-id="282d7-279">True</span></span>                                |
| <span data-ttu-id="282d7-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="282d7-280">Is-Single-Valued</span></span>       | <span data-ttu-id="282d7-281">對</span><span class="sxs-lookup"><span data-stu-id="282d7-281">True</span></span>                                |
| <span data-ttu-id="282d7-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="282d7-282">Is Indexed</span></span>             | <span data-ttu-id="282d7-283">否</span><span class="sxs-lookup"><span data-stu-id="282d7-283">False</span></span>                               |
| <span data-ttu-id="282d7-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="282d7-284">In Global Catalog</span></span>      | <span data-ttu-id="282d7-285">否</span><span class="sxs-lookup"><span data-stu-id="282d7-285">False</span></span>                               |
| <span data-ttu-id="282d7-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="282d7-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="282d7-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="282d7-287">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="282d7-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="282d7-288">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="282d7-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="282d7-289">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="282d7-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-290">Search-Flags</span></span>           | <span data-ttu-id="282d7-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="282d7-291">0x00000000</span></span>                          |
| <span data-ttu-id="282d7-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="282d7-292">System-Flags</span></span>           | <span data-ttu-id="282d7-293">0x00000014</span><span class="sxs-lookup"><span data-stu-id="282d7-293">0x00000014</span></span>                          |
| <span data-ttu-id="282d7-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="282d7-294">Classes used in</span></span>        | [<span data-ttu-id="282d7-295">**Group**</span><span class="sxs-lookup"><span data-stu-id="282d7-295">**Group**</span></span>](c-group.md)<br/> |



 

 






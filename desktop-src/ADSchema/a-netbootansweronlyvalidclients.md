---
title: netboot-僅回應-有效-用戶端屬性
description: 判斷伺服器是否會回應所有（或僅限預先設置的）用戶端電腦。
ms.assetid: b02438ba-11b3-497c-b57f-bd9a0045e6b0
ms.tgt_platform: multiple
keywords:
- netboot-僅回應-有效-用戶端屬性 AD 架構
- netbootAnswerOnlyValidClients 屬性 AD 架構
topic_type:
- apiref
api_name:
- netboot-Answer-Only-Valid-Clients
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e28f7ecfaa569f47d79249606029760b914b5ac
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107657"
---
# <a name="netboot-answer-only-valid-clients-attribute"></a><span data-ttu-id="7d037-105">netboot-僅回應-有效-用戶端屬性</span><span class="sxs-lookup"><span data-stu-id="7d037-105">netboot-Answer-Only-Valid-Clients attribute</span></span>

<span data-ttu-id="7d037-106">判斷伺服器是否會回應所有（或僅限預先設置的）用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="7d037-106">Determines whether the server answers all, or only pre-staged, client computers.</span></span>



| <span data-ttu-id="7d037-107">進入</span><span class="sxs-lookup"><span data-stu-id="7d037-107">Entry</span></span> | <span data-ttu-id="7d037-108">值</span><span class="sxs-lookup"><span data-stu-id="7d037-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7d037-109">CN</span><span class="sxs-lookup"><span data-stu-id="7d037-109">CN</span></span>                | <span data-ttu-id="7d037-110">netboot-僅限回應-有效-用戶端</span><span class="sxs-lookup"><span data-stu-id="7d037-110">netboot-Answer-Only-Valid-Clients</span></span>    |
| <span data-ttu-id="7d037-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7d037-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7d037-112">netbootAnswerOnlyValidClients</span><span class="sxs-lookup"><span data-stu-id="7d037-112">netbootAnswerOnlyValidClients</span></span>        |
| <span data-ttu-id="7d037-113">大小</span><span class="sxs-lookup"><span data-stu-id="7d037-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="7d037-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7d037-114">Update Privilege</span></span>  | <span data-ttu-id="7d037-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7d037-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="7d037-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7d037-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7d037-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7d037-117">Attribute-Id</span></span>      | <span data-ttu-id="7d037-118">1.2.840.113556.1.4.854</span><span class="sxs-lookup"><span data-stu-id="7d037-118">1.2.840.113556.1.4.854</span></span>               |
| <span data-ttu-id="7d037-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7d037-119">System-Id-Guid</span></span>    | <span data-ttu-id="7d037-120">0738307b-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7d037-120">0738307b-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="7d037-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d037-121">Syntax</span></span>            | [<span data-ttu-id="7d037-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7d037-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="7d037-123">實作</span><span class="sxs-lookup"><span data-stu-id="7d037-123">Implementations</span></span>

-   [<span data-ttu-id="7d037-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7d037-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7d037-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7d037-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7d037-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7d037-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7d037-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7d037-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7d037-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7d037-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7d037-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7d037-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7d037-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7d037-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7d037-131">進入</span><span class="sxs-lookup"><span data-stu-id="7d037-131">Entry</span></span> | <span data-ttu-id="7d037-132">值</span><span class="sxs-lookup"><span data-stu-id="7d037-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d037-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d037-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d037-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d037-135">System-Only</span></span>            | <span data-ttu-id="7d037-136">否</span><span class="sxs-lookup"><span data-stu-id="7d037-136">False</span></span>                                                      |
| <span data-ttu-id="7d037-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d037-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7d037-138">對</span><span class="sxs-lookup"><span data-stu-id="7d037-138">True</span></span>                                                       |
| <span data-ttu-id="7d037-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d037-139">Is Indexed</span></span>             | <span data-ttu-id="7d037-140">否</span><span class="sxs-lookup"><span data-stu-id="7d037-140">False</span></span>                                                      |
| <span data-ttu-id="7d037-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d037-141">In Global Catalog</span></span>      | <span data-ttu-id="7d037-142">否</span><span class="sxs-lookup"><span data-stu-id="7d037-142">False</span></span>                                                      |
| <span data-ttu-id="7d037-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d037-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d037-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d037-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="7d037-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d037-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d037-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-147">Search-Flags</span></span>           | <span data-ttu-id="7d037-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d037-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="7d037-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-149">System-Flags</span></span>           | <span data-ttu-id="7d037-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d037-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="7d037-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d037-151">Classes used in</span></span>        | [<span data-ttu-id="7d037-152">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="7d037-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7d037-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7d037-153">Windows Server 2003</span></span>



| <span data-ttu-id="7d037-154">進入</span><span class="sxs-lookup"><span data-stu-id="7d037-154">Entry</span></span> | <span data-ttu-id="7d037-155">值</span><span class="sxs-lookup"><span data-stu-id="7d037-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d037-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d037-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d037-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d037-158">System-Only</span></span>            | <span data-ttu-id="7d037-159">否</span><span class="sxs-lookup"><span data-stu-id="7d037-159">False</span></span>                                                      |
| <span data-ttu-id="7d037-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d037-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7d037-161">對</span><span class="sxs-lookup"><span data-stu-id="7d037-161">True</span></span>                                                       |
| <span data-ttu-id="7d037-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d037-162">Is Indexed</span></span>             | <span data-ttu-id="7d037-163">否</span><span class="sxs-lookup"><span data-stu-id="7d037-163">False</span></span>                                                      |
| <span data-ttu-id="7d037-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d037-164">In Global Catalog</span></span>      | <span data-ttu-id="7d037-165">否</span><span class="sxs-lookup"><span data-stu-id="7d037-165">False</span></span>                                                      |
| <span data-ttu-id="7d037-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d037-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d037-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d037-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="7d037-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d037-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d037-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-170">Search-Flags</span></span>           | <span data-ttu-id="7d037-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d037-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="7d037-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-172">System-Flags</span></span>           | <span data-ttu-id="7d037-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d037-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="7d037-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d037-174">Classes used in</span></span>        | [<span data-ttu-id="7d037-175">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="7d037-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7d037-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7d037-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7d037-177">進入</span><span class="sxs-lookup"><span data-stu-id="7d037-177">Entry</span></span> | <span data-ttu-id="7d037-178">值</span><span class="sxs-lookup"><span data-stu-id="7d037-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d037-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d037-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d037-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d037-181">System-Only</span></span>            | <span data-ttu-id="7d037-182">否</span><span class="sxs-lookup"><span data-stu-id="7d037-182">False</span></span>                                                      |
| <span data-ttu-id="7d037-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d037-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7d037-184">對</span><span class="sxs-lookup"><span data-stu-id="7d037-184">True</span></span>                                                       |
| <span data-ttu-id="7d037-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d037-185">Is Indexed</span></span>             | <span data-ttu-id="7d037-186">否</span><span class="sxs-lookup"><span data-stu-id="7d037-186">False</span></span>                                                      |
| <span data-ttu-id="7d037-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d037-187">In Global Catalog</span></span>      | <span data-ttu-id="7d037-188">否</span><span class="sxs-lookup"><span data-stu-id="7d037-188">False</span></span>                                                      |
| <span data-ttu-id="7d037-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d037-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d037-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d037-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="7d037-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d037-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d037-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-193">Search-Flags</span></span>           | <span data-ttu-id="7d037-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d037-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="7d037-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-195">System-Flags</span></span>           | <span data-ttu-id="7d037-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d037-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="7d037-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d037-197">Classes used in</span></span>        | [<span data-ttu-id="7d037-198">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="7d037-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7d037-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d037-199">Windows Server 2008</span></span>



| <span data-ttu-id="7d037-200">進入</span><span class="sxs-lookup"><span data-stu-id="7d037-200">Entry</span></span> | <span data-ttu-id="7d037-201">值</span><span class="sxs-lookup"><span data-stu-id="7d037-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d037-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d037-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d037-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d037-204">System-Only</span></span>            | <span data-ttu-id="7d037-205">否</span><span class="sxs-lookup"><span data-stu-id="7d037-205">False</span></span>                                                      |
| <span data-ttu-id="7d037-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d037-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7d037-207">對</span><span class="sxs-lookup"><span data-stu-id="7d037-207">True</span></span>                                                       |
| <span data-ttu-id="7d037-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d037-208">Is Indexed</span></span>             | <span data-ttu-id="7d037-209">否</span><span class="sxs-lookup"><span data-stu-id="7d037-209">False</span></span>                                                      |
| <span data-ttu-id="7d037-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d037-210">In Global Catalog</span></span>      | <span data-ttu-id="7d037-211">否</span><span class="sxs-lookup"><span data-stu-id="7d037-211">False</span></span>                                                      |
| <span data-ttu-id="7d037-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d037-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d037-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d037-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="7d037-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d037-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d037-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-216">Search-Flags</span></span>           | <span data-ttu-id="7d037-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d037-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="7d037-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-218">System-Flags</span></span>           | <span data-ttu-id="7d037-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d037-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="7d037-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d037-220">Classes used in</span></span>        | [<span data-ttu-id="7d037-221">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="7d037-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7d037-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d037-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7d037-223">進入</span><span class="sxs-lookup"><span data-stu-id="7d037-223">Entry</span></span> | <span data-ttu-id="7d037-224">值</span><span class="sxs-lookup"><span data-stu-id="7d037-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d037-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d037-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d037-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d037-227">System-Only</span></span>            | <span data-ttu-id="7d037-228">否</span><span class="sxs-lookup"><span data-stu-id="7d037-228">False</span></span>                                                      |
| <span data-ttu-id="7d037-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d037-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7d037-230">對</span><span class="sxs-lookup"><span data-stu-id="7d037-230">True</span></span>                                                       |
| <span data-ttu-id="7d037-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d037-231">Is Indexed</span></span>             | <span data-ttu-id="7d037-232">否</span><span class="sxs-lookup"><span data-stu-id="7d037-232">False</span></span>                                                      |
| <span data-ttu-id="7d037-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d037-233">In Global Catalog</span></span>      | <span data-ttu-id="7d037-234">否</span><span class="sxs-lookup"><span data-stu-id="7d037-234">False</span></span>                                                      |
| <span data-ttu-id="7d037-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d037-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d037-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d037-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="7d037-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d037-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d037-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-239">Search-Flags</span></span>           | <span data-ttu-id="7d037-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d037-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="7d037-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-241">System-Flags</span></span>           | <span data-ttu-id="7d037-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d037-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="7d037-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d037-243">Classes used in</span></span>        | [<span data-ttu-id="7d037-244">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="7d037-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7d037-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d037-245">Windows Server 2012</span></span>



| <span data-ttu-id="7d037-246">進入</span><span class="sxs-lookup"><span data-stu-id="7d037-246">Entry</span></span> | <span data-ttu-id="7d037-247">值</span><span class="sxs-lookup"><span data-stu-id="7d037-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d037-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d037-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d037-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="7d037-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d037-250">System-Only</span></span>            | <span data-ttu-id="7d037-251">否</span><span class="sxs-lookup"><span data-stu-id="7d037-251">False</span></span>                                                      |
| <span data-ttu-id="7d037-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d037-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7d037-253">對</span><span class="sxs-lookup"><span data-stu-id="7d037-253">True</span></span>                                                       |
| <span data-ttu-id="7d037-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d037-254">Is Indexed</span></span>             | <span data-ttu-id="7d037-255">否</span><span class="sxs-lookup"><span data-stu-id="7d037-255">False</span></span>                                                      |
| <span data-ttu-id="7d037-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d037-256">In Global Catalog</span></span>      | <span data-ttu-id="7d037-257">否</span><span class="sxs-lookup"><span data-stu-id="7d037-257">False</span></span>                                                      |
| <span data-ttu-id="7d037-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d037-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d037-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d037-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="7d037-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d037-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d037-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="7d037-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-262">Search-Flags</span></span>           | <span data-ttu-id="7d037-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d037-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="7d037-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d037-264">System-Flags</span></span>           | <span data-ttu-id="7d037-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d037-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="7d037-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d037-266">Classes used in</span></span>        | [<span data-ttu-id="7d037-267">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="7d037-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 






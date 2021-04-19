---
title: netboot-回答-要求屬性
description: 讓 RIS 伺服器接受任何 RIS 要求。
ms.assetid: fb57762f-d7af-45ae-80f2-5dd52b5688a9
ms.tgt_platform: multiple
keywords:
- netboot-解答-要求屬性 AD 架構
- netbootAnswerRequests 屬性 AD 架構
topic_type:
- apiref
api_name:
- netboot-Answer-Requests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3552517189635da9c2ed464e286c06bb3c8d19
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970483"
---
# <a name="netboot-answer-requests-attribute"></a><span data-ttu-id="8a1f0-105">netboot-回答-要求屬性</span><span class="sxs-lookup"><span data-stu-id="8a1f0-105">netboot-Answer-Requests attribute</span></span>

<span data-ttu-id="8a1f0-106">讓 RIS 伺服器接受任何 RIS 要求。</span><span class="sxs-lookup"><span data-stu-id="8a1f0-106">Enables the RIS server to accept any RIS requests.</span></span>



| <span data-ttu-id="8a1f0-107">進入</span><span class="sxs-lookup"><span data-stu-id="8a1f0-107">Entry</span></span> | <span data-ttu-id="8a1f0-108">值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8a1f0-109">CN</span><span class="sxs-lookup"><span data-stu-id="8a1f0-109">CN</span></span>                | <span data-ttu-id="8a1f0-110">netboot-解答-要求</span><span class="sxs-lookup"><span data-stu-id="8a1f0-110">netboot-Answer-Requests</span></span>              |
| <span data-ttu-id="8a1f0-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8a1f0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8a1f0-112">netbootAnswerRequests</span><span class="sxs-lookup"><span data-stu-id="8a1f0-112">netbootAnswerRequests</span></span>                |
| <span data-ttu-id="8a1f0-113">大小</span><span class="sxs-lookup"><span data-stu-id="8a1f0-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="8a1f0-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8a1f0-114">Update Privilege</span></span>  | <span data-ttu-id="8a1f0-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="8a1f0-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="8a1f0-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8a1f0-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8a1f0-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8a1f0-117">Attribute-Id</span></span>      | <span data-ttu-id="8a1f0-118">1.2.840.113556.1.4.853</span><span class="sxs-lookup"><span data-stu-id="8a1f0-118">1.2.840.113556.1.4.853</span></span>               |
| <span data-ttu-id="8a1f0-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8a1f0-119">System-Id-Guid</span></span>    | <span data-ttu-id="8a1f0-120">0738307a-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8a1f0-120">0738307a-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="8a1f0-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a1f0-121">Syntax</span></span>            | [<span data-ttu-id="8a1f0-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="8a1f0-123">實作</span><span class="sxs-lookup"><span data-stu-id="8a1f0-123">Implementations</span></span>

-   [<span data-ttu-id="8a1f0-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8a1f0-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8a1f0-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8a1f0-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8a1f0-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8a1f0-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8a1f0-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a1f0-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8a1f0-131">進入</span><span class="sxs-lookup"><span data-stu-id="8a1f0-131">Entry</span></span> | <span data-ttu-id="8a1f0-132">值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8a1f0-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8a1f0-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a1f0-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a1f0-135">System-Only</span></span>            | <span data-ttu-id="8a1f0-136">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-136">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8a1f0-138">對</span><span class="sxs-lookup"><span data-stu-id="8a1f0-138">True</span></span>                                                       |
| <span data-ttu-id="8a1f0-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8a1f0-139">Is Indexed</span></span>             | <span data-ttu-id="8a1f0-140">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-140">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8a1f0-141">In Global Catalog</span></span>      | <span data-ttu-id="8a1f0-142">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-142">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8a1f0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a1f0-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8a1f0-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8a1f0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a1f0-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a1f0-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-147">Search-Flags</span></span>           | <span data-ttu-id="8a1f0-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a1f0-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="8a1f0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-149">System-Flags</span></span>           | <span data-ttu-id="8a1f0-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a1f0-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="8a1f0-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8a1f0-151">Classes used in</span></span>        | [<span data-ttu-id="8a1f0-152">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8a1f0-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a1f0-153">Windows Server 2003</span></span>



| <span data-ttu-id="8a1f0-154">進入</span><span class="sxs-lookup"><span data-stu-id="8a1f0-154">Entry</span></span> | <span data-ttu-id="8a1f0-155">值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8a1f0-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8a1f0-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a1f0-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a1f0-158">System-Only</span></span>            | <span data-ttu-id="8a1f0-159">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-159">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8a1f0-161">對</span><span class="sxs-lookup"><span data-stu-id="8a1f0-161">True</span></span>                                                       |
| <span data-ttu-id="8a1f0-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8a1f0-162">Is Indexed</span></span>             | <span data-ttu-id="8a1f0-163">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-163">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8a1f0-164">In Global Catalog</span></span>      | <span data-ttu-id="8a1f0-165">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-165">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8a1f0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a1f0-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8a1f0-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8a1f0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a1f0-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a1f0-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-170">Search-Flags</span></span>           | <span data-ttu-id="8a1f0-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a1f0-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="8a1f0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-172">System-Flags</span></span>           | <span data-ttu-id="8a1f0-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a1f0-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="8a1f0-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8a1f0-174">Classes used in</span></span>        | [<span data-ttu-id="8a1f0-175">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8a1f0-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8a1f0-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8a1f0-177">進入</span><span class="sxs-lookup"><span data-stu-id="8a1f0-177">Entry</span></span> | <span data-ttu-id="8a1f0-178">值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8a1f0-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8a1f0-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a1f0-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a1f0-181">System-Only</span></span>            | <span data-ttu-id="8a1f0-182">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-182">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8a1f0-184">對</span><span class="sxs-lookup"><span data-stu-id="8a1f0-184">True</span></span>                                                       |
| <span data-ttu-id="8a1f0-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8a1f0-185">Is Indexed</span></span>             | <span data-ttu-id="8a1f0-186">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-186">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8a1f0-187">In Global Catalog</span></span>      | <span data-ttu-id="8a1f0-188">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-188">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8a1f0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a1f0-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8a1f0-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8a1f0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a1f0-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a1f0-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-193">Search-Flags</span></span>           | <span data-ttu-id="8a1f0-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a1f0-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="8a1f0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-195">System-Flags</span></span>           | <span data-ttu-id="8a1f0-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a1f0-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="8a1f0-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8a1f0-197">Classes used in</span></span>        | [<span data-ttu-id="8a1f0-198">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8a1f0-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a1f0-199">Windows Server 2008</span></span>



| <span data-ttu-id="8a1f0-200">進入</span><span class="sxs-lookup"><span data-stu-id="8a1f0-200">Entry</span></span> | <span data-ttu-id="8a1f0-201">值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8a1f0-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8a1f0-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a1f0-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a1f0-204">System-Only</span></span>            | <span data-ttu-id="8a1f0-205">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-205">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8a1f0-207">對</span><span class="sxs-lookup"><span data-stu-id="8a1f0-207">True</span></span>                                                       |
| <span data-ttu-id="8a1f0-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8a1f0-208">Is Indexed</span></span>             | <span data-ttu-id="8a1f0-209">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-209">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8a1f0-210">In Global Catalog</span></span>      | <span data-ttu-id="8a1f0-211">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-211">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8a1f0-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a1f0-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8a1f0-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8a1f0-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a1f0-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a1f0-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-216">Search-Flags</span></span>           | <span data-ttu-id="8a1f0-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a1f0-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="8a1f0-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-218">System-Flags</span></span>           | <span data-ttu-id="8a1f0-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a1f0-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="8a1f0-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8a1f0-220">Classes used in</span></span>        | [<span data-ttu-id="8a1f0-221">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8a1f0-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a1f0-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8a1f0-223">進入</span><span class="sxs-lookup"><span data-stu-id="8a1f0-223">Entry</span></span> | <span data-ttu-id="8a1f0-224">值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8a1f0-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8a1f0-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a1f0-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a1f0-227">System-Only</span></span>            | <span data-ttu-id="8a1f0-228">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-228">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8a1f0-230">對</span><span class="sxs-lookup"><span data-stu-id="8a1f0-230">True</span></span>                                                       |
| <span data-ttu-id="8a1f0-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8a1f0-231">Is Indexed</span></span>             | <span data-ttu-id="8a1f0-232">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-232">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8a1f0-233">In Global Catalog</span></span>      | <span data-ttu-id="8a1f0-234">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-234">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8a1f0-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a1f0-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8a1f0-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8a1f0-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a1f0-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a1f0-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-239">Search-Flags</span></span>           | <span data-ttu-id="8a1f0-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a1f0-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="8a1f0-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-241">System-Flags</span></span>           | <span data-ttu-id="8a1f0-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a1f0-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="8a1f0-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8a1f0-243">Classes used in</span></span>        | [<span data-ttu-id="8a1f0-244">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8a1f0-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a1f0-245">Windows Server 2012</span></span>



| <span data-ttu-id="8a1f0-246">進入</span><span class="sxs-lookup"><span data-stu-id="8a1f0-246">Entry</span></span> | <span data-ttu-id="8a1f0-247">值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8a1f0-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8a1f0-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a1f0-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8a1f0-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a1f0-250">System-Only</span></span>            | <span data-ttu-id="8a1f0-251">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-251">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8a1f0-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8a1f0-253">對</span><span class="sxs-lookup"><span data-stu-id="8a1f0-253">True</span></span>                                                       |
| <span data-ttu-id="8a1f0-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8a1f0-254">Is Indexed</span></span>             | <span data-ttu-id="8a1f0-255">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-255">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8a1f0-256">In Global Catalog</span></span>      | <span data-ttu-id="8a1f0-257">否</span><span class="sxs-lookup"><span data-stu-id="8a1f0-257">False</span></span>                                                      |
| <span data-ttu-id="8a1f0-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8a1f0-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a1f0-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8a1f0-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8a1f0-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a1f0-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a1f0-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8a1f0-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-262">Search-Flags</span></span>           | <span data-ttu-id="8a1f0-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a1f0-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="8a1f0-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1f0-264">System-Flags</span></span>           | <span data-ttu-id="8a1f0-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a1f0-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="8a1f0-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8a1f0-266">Classes used in</span></span>        | [<span data-ttu-id="8a1f0-267">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8a1f0-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 






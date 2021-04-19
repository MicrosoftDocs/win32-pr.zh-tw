---
title: 網站間-拓撲-更新屬性
description: 這個類別指出網站間拓撲產生器更新傳送至相同網站中的網域控制站之 keep-alive 訊息的頻率。
ms.assetid: 523d8161-0678-482f-8d66-55a112995fe5
ms.tgt_platform: multiple
keywords:
- 網站間-拓撲-更新屬性 AD 架構
- interSiteTopologyRenew 屬性 AD 架構
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Renew
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821bd294f777fd29738ff102955cd170a42205e2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971077"
---
# <a name="inter-site-topology-renew-attribute"></a><span data-ttu-id="e8bbb-105">網站間-拓撲-更新屬性</span><span class="sxs-lookup"><span data-stu-id="e8bbb-105">Inter-Site-Topology-Renew attribute</span></span>

<span data-ttu-id="e8bbb-106">這個類別指出網站間拓撲產生器更新傳送至相同網站中的網域控制站之 keep-alive 訊息的頻率。</span><span class="sxs-lookup"><span data-stu-id="e8bbb-106">This class indicates how often the intersite topology generator updates the keep-alive message that is sent to domain controllers contained in the same site.</span></span>



| <span data-ttu-id="e8bbb-107">進入</span><span class="sxs-lookup"><span data-stu-id="e8bbb-107">Entry</span></span> | <span data-ttu-id="e8bbb-108">值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e8bbb-109">CN</span><span class="sxs-lookup"><span data-stu-id="e8bbb-109">CN</span></span>                | <span data-ttu-id="e8bbb-110">網站間-拓撲-更新</span><span class="sxs-lookup"><span data-stu-id="e8bbb-110">Inter-Site-Topology-Renew</span></span>            |
| <span data-ttu-id="e8bbb-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e8bbb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e8bbb-112">interSiteTopologyRenew</span><span class="sxs-lookup"><span data-stu-id="e8bbb-112">interSiteTopologyRenew</span></span>               |
| <span data-ttu-id="e8bbb-113">大小</span><span class="sxs-lookup"><span data-stu-id="e8bbb-113">Size</span></span>              | <span data-ttu-id="e8bbb-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="e8bbb-114">4 bytes</span></span>                              |
| <span data-ttu-id="e8bbb-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e8bbb-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e8bbb-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e8bbb-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e8bbb-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e8bbb-117">Attribute-Id</span></span>      | <span data-ttu-id="e8bbb-118">1.2.840.113556.1.4.1247</span><span class="sxs-lookup"><span data-stu-id="e8bbb-118">1.2.840.113556.1.4.1247</span></span>              |
| <span data-ttu-id="e8bbb-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e8bbb-119">System-Id-Guid</span></span>    | <span data-ttu-id="e8bbb-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="e8bbb-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="e8bbb-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8bbb-121">Syntax</span></span>            | [<span data-ttu-id="e8bbb-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e8bbb-123">實作</span><span class="sxs-lookup"><span data-stu-id="e8bbb-123">Implementations</span></span>

-   [<span data-ttu-id="e8bbb-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e8bbb-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e8bbb-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e8bbb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e8bbb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e8bbb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e8bbb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e8bbb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e8bbb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e8bbb-132">進入</span><span class="sxs-lookup"><span data-stu-id="e8bbb-132">Entry</span></span> | <span data-ttu-id="e8bbb-133">值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e8bbb-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8bbb-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8bbb-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8bbb-136">System-Only</span></span>            | <span data-ttu-id="e8bbb-137">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-137">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e8bbb-139">對</span><span class="sxs-lookup"><span data-stu-id="e8bbb-139">True</span></span>                                                        |
| <span data-ttu-id="e8bbb-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8bbb-140">Is Indexed</span></span>             | <span data-ttu-id="e8bbb-141">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-141">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8bbb-142">In Global Catalog</span></span>      | <span data-ttu-id="e8bbb-143">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-143">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8bbb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8bbb-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8bbb-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="e8bbb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8bbb-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8bbb-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-148">Search-Flags</span></span>           | <span data-ttu-id="e8bbb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8bbb-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="e8bbb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-150">System-Flags</span></span>           | <span data-ttu-id="e8bbb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8bbb-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="e8bbb-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8bbb-152">Classes used in</span></span>        | [<span data-ttu-id="e8bbb-153">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e8bbb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8bbb-154">Windows Server 2003</span></span>



| <span data-ttu-id="e8bbb-155">進入</span><span class="sxs-lookup"><span data-stu-id="e8bbb-155">Entry</span></span> | <span data-ttu-id="e8bbb-156">值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e8bbb-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8bbb-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8bbb-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8bbb-159">System-Only</span></span>            | <span data-ttu-id="e8bbb-160">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-160">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e8bbb-162">對</span><span class="sxs-lookup"><span data-stu-id="e8bbb-162">True</span></span>                                                        |
| <span data-ttu-id="e8bbb-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8bbb-163">Is Indexed</span></span>             | <span data-ttu-id="e8bbb-164">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-164">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8bbb-165">In Global Catalog</span></span>      | <span data-ttu-id="e8bbb-166">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-166">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8bbb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8bbb-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8bbb-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="e8bbb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8bbb-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8bbb-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-171">Search-Flags</span></span>           | <span data-ttu-id="e8bbb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8bbb-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="e8bbb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-173">System-Flags</span></span>           | <span data-ttu-id="e8bbb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8bbb-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="e8bbb-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8bbb-175">Classes used in</span></span>        | [<span data-ttu-id="e8bbb-176">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e8bbb-177">亞當</span><span class="sxs-lookup"><span data-stu-id="e8bbb-177">ADAM</span></span>



| <span data-ttu-id="e8bbb-178">進入</span><span class="sxs-lookup"><span data-stu-id="e8bbb-178">Entry</span></span> | <span data-ttu-id="e8bbb-179">值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e8bbb-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8bbb-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8bbb-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8bbb-182">System-Only</span></span>            | <span data-ttu-id="e8bbb-183">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-183">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e8bbb-185">對</span><span class="sxs-lookup"><span data-stu-id="e8bbb-185">True</span></span>                                                        |
| <span data-ttu-id="e8bbb-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8bbb-186">Is Indexed</span></span>             | <span data-ttu-id="e8bbb-187">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-187">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8bbb-188">In Global Catalog</span></span>      | <span data-ttu-id="e8bbb-189">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-189">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8bbb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8bbb-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8bbb-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="e8bbb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8bbb-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8bbb-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-194">Search-Flags</span></span>           | <span data-ttu-id="e8bbb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8bbb-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="e8bbb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-196">System-Flags</span></span>           | <span data-ttu-id="e8bbb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8bbb-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="e8bbb-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8bbb-198">Classes used in</span></span>        | [<span data-ttu-id="e8bbb-199">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e8bbb-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e8bbb-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e8bbb-201">進入</span><span class="sxs-lookup"><span data-stu-id="e8bbb-201">Entry</span></span> | <span data-ttu-id="e8bbb-202">值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e8bbb-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8bbb-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8bbb-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8bbb-205">System-Only</span></span>            | <span data-ttu-id="e8bbb-206">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-206">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e8bbb-208">對</span><span class="sxs-lookup"><span data-stu-id="e8bbb-208">True</span></span>                                                        |
| <span data-ttu-id="e8bbb-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8bbb-209">Is Indexed</span></span>             | <span data-ttu-id="e8bbb-210">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-210">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8bbb-211">In Global Catalog</span></span>      | <span data-ttu-id="e8bbb-212">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-212">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8bbb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8bbb-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8bbb-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="e8bbb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8bbb-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8bbb-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-217">Search-Flags</span></span>           | <span data-ttu-id="e8bbb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8bbb-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="e8bbb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-219">System-Flags</span></span>           | <span data-ttu-id="e8bbb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8bbb-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="e8bbb-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8bbb-221">Classes used in</span></span>        | [<span data-ttu-id="e8bbb-222">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e8bbb-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8bbb-223">Windows Server 2008</span></span>



| <span data-ttu-id="e8bbb-224">進入</span><span class="sxs-lookup"><span data-stu-id="e8bbb-224">Entry</span></span> | <span data-ttu-id="e8bbb-225">值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e8bbb-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8bbb-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8bbb-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8bbb-228">System-Only</span></span>            | <span data-ttu-id="e8bbb-229">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-229">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e8bbb-231">對</span><span class="sxs-lookup"><span data-stu-id="e8bbb-231">True</span></span>                                                        |
| <span data-ttu-id="e8bbb-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8bbb-232">Is Indexed</span></span>             | <span data-ttu-id="e8bbb-233">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-233">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8bbb-234">In Global Catalog</span></span>      | <span data-ttu-id="e8bbb-235">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-235">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8bbb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8bbb-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8bbb-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="e8bbb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8bbb-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8bbb-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-240">Search-Flags</span></span>           | <span data-ttu-id="e8bbb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8bbb-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="e8bbb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-242">System-Flags</span></span>           | <span data-ttu-id="e8bbb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8bbb-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="e8bbb-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8bbb-244">Classes used in</span></span>        | [<span data-ttu-id="e8bbb-245">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e8bbb-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8bbb-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e8bbb-247">進入</span><span class="sxs-lookup"><span data-stu-id="e8bbb-247">Entry</span></span> | <span data-ttu-id="e8bbb-248">值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e8bbb-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8bbb-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8bbb-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8bbb-251">System-Only</span></span>            | <span data-ttu-id="e8bbb-252">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-252">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e8bbb-254">對</span><span class="sxs-lookup"><span data-stu-id="e8bbb-254">True</span></span>                                                        |
| <span data-ttu-id="e8bbb-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8bbb-255">Is Indexed</span></span>             | <span data-ttu-id="e8bbb-256">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-256">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8bbb-257">In Global Catalog</span></span>      | <span data-ttu-id="e8bbb-258">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-258">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8bbb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8bbb-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8bbb-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="e8bbb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8bbb-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8bbb-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-263">Search-Flags</span></span>           | <span data-ttu-id="e8bbb-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8bbb-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="e8bbb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-265">System-Flags</span></span>           | <span data-ttu-id="e8bbb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8bbb-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="e8bbb-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8bbb-267">Classes used in</span></span>        | [<span data-ttu-id="e8bbb-268">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e8bbb-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8bbb-269">Windows Server 2012</span></span>



| <span data-ttu-id="e8bbb-270">進入</span><span class="sxs-lookup"><span data-stu-id="e8bbb-270">Entry</span></span> | <span data-ttu-id="e8bbb-271">值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e8bbb-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8bbb-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8bbb-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="e8bbb-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8bbb-274">System-Only</span></span>            | <span data-ttu-id="e8bbb-275">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-275">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8bbb-276">Is-Single-Valued</span></span>       | <span data-ttu-id="e8bbb-277">對</span><span class="sxs-lookup"><span data-stu-id="e8bbb-277">True</span></span>                                                        |
| <span data-ttu-id="e8bbb-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8bbb-278">Is Indexed</span></span>             | <span data-ttu-id="e8bbb-279">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-279">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8bbb-280">In Global Catalog</span></span>      | <span data-ttu-id="e8bbb-281">否</span><span class="sxs-lookup"><span data-stu-id="e8bbb-281">False</span></span>                                                       |
| <span data-ttu-id="e8bbb-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8bbb-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8bbb-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8bbb-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="e8bbb-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8bbb-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8bbb-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="e8bbb-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-286">Search-Flags</span></span>           | <span data-ttu-id="e8bbb-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8bbb-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="e8bbb-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8bbb-288">System-Flags</span></span>           | <span data-ttu-id="e8bbb-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8bbb-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="e8bbb-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8bbb-290">Classes used in</span></span>        | [<span data-ttu-id="e8bbb-291">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="e8bbb-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 






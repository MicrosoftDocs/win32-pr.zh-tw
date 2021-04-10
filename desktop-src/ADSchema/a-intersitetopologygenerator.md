---
title: 網站間拓撲-產生器屬性
description: 這個屬性將用來支援指定網站中執行知識一致性檢查程式產生的電腦上的容錯移轉。
ms.assetid: 077f4331-ead9-4f17-942e-d55cf253d03b
ms.tgt_platform: multiple
keywords:
- 網站間拓撲-產生器屬性 AD 架構
- interSiteTopologyGenerator 屬性 AD 架構
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Generator
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7b354d05e882373715e4c49498c9daff41652
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107027"
---
# <a name="inter-site-topology-generator-attribute"></a><span data-ttu-id="2f836-105">網站間拓撲-產生器屬性</span><span class="sxs-lookup"><span data-stu-id="2f836-105">Inter-Site-Topology-Generator attribute</span></span>

<span data-ttu-id="2f836-106">這個屬性將用來支援指定網站中執行知識一致性檢查程式產生的電腦上的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="2f836-106">This attribute will be used to support failover for the computer designated as the one that runs Knowledge Consistency Checker inter-site topology generation in a given site.</span></span>



| <span data-ttu-id="2f836-107">進入</span><span class="sxs-lookup"><span data-stu-id="2f836-107">Entry</span></span> | <span data-ttu-id="2f836-108">值</span><span class="sxs-lookup"><span data-stu-id="2f836-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2f836-109">CN</span><span class="sxs-lookup"><span data-stu-id="2f836-109">CN</span></span>                | <span data-ttu-id="2f836-110">網站間拓撲-產生器</span><span class="sxs-lookup"><span data-stu-id="2f836-110">Inter-Site-Topology-Generator</span></span>           |
| <span data-ttu-id="2f836-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2f836-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2f836-112">interSiteTopologyGenerator</span><span class="sxs-lookup"><span data-stu-id="2f836-112">interSiteTopologyGenerator</span></span>              |
| <span data-ttu-id="2f836-113">大小</span><span class="sxs-lookup"><span data-stu-id="2f836-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="2f836-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2f836-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="2f836-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2f836-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2f836-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2f836-116">Attribute-Id</span></span>      | <span data-ttu-id="2f836-117">1.2.840.113556.1.4.1246</span><span class="sxs-lookup"><span data-stu-id="2f836-117">1.2.840.113556.1.4.1246</span></span>                 |
| <span data-ttu-id="2f836-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2f836-118">System-Id-Guid</span></span>    | <span data-ttu-id="2f836-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="2f836-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span></span>    |
| <span data-ttu-id="2f836-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f836-120">Syntax</span></span>            | [<span data-ttu-id="2f836-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2f836-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2f836-122">實作</span><span class="sxs-lookup"><span data-stu-id="2f836-122">Implementations</span></span>

-   [<span data-ttu-id="2f836-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2f836-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2f836-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2f836-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2f836-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="2f836-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2f836-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2f836-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2f836-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2f836-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2f836-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2f836-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2f836-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2f836-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2f836-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f836-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2f836-131">進入</span><span class="sxs-lookup"><span data-stu-id="2f836-131">Entry</span></span> | <span data-ttu-id="2f836-132">值</span><span class="sxs-lookup"><span data-stu-id="2f836-132">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f836-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2f836-133">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f836-134">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f836-135">System-Only</span></span>            | <span data-ttu-id="2f836-136">否</span><span class="sxs-lookup"><span data-stu-id="2f836-136">False</span></span>                                                       |
| <span data-ttu-id="2f836-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2f836-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2f836-138">對</span><span class="sxs-lookup"><span data-stu-id="2f836-138">True</span></span>                                                        |
| <span data-ttu-id="2f836-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2f836-139">Is Indexed</span></span>             | <span data-ttu-id="2f836-140">否</span><span class="sxs-lookup"><span data-stu-id="2f836-140">False</span></span>                                                       |
| <span data-ttu-id="2f836-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2f836-141">In Global Catalog</span></span>      | <span data-ttu-id="2f836-142">否</span><span class="sxs-lookup"><span data-stu-id="2f836-142">False</span></span>                                                       |
| <span data-ttu-id="2f836-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2f836-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f836-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2f836-144">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f836-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f836-145">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f836-146">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-147">Search-Flags</span></span>           | <span data-ttu-id="2f836-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f836-148">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f836-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-149">System-Flags</span></span>           | <span data-ttu-id="2f836-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f836-150">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f836-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2f836-151">Classes used in</span></span>        | [<span data-ttu-id="2f836-152">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="2f836-152">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2f836-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2f836-153">Windows Server 2003</span></span>



| <span data-ttu-id="2f836-154">進入</span><span class="sxs-lookup"><span data-stu-id="2f836-154">Entry</span></span> | <span data-ttu-id="2f836-155">值</span><span class="sxs-lookup"><span data-stu-id="2f836-155">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f836-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2f836-156">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f836-157">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f836-158">System-Only</span></span>            | <span data-ttu-id="2f836-159">否</span><span class="sxs-lookup"><span data-stu-id="2f836-159">False</span></span>                                                       |
| <span data-ttu-id="2f836-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2f836-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2f836-161">對</span><span class="sxs-lookup"><span data-stu-id="2f836-161">True</span></span>                                                        |
| <span data-ttu-id="2f836-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2f836-162">Is Indexed</span></span>             | <span data-ttu-id="2f836-163">否</span><span class="sxs-lookup"><span data-stu-id="2f836-163">False</span></span>                                                       |
| <span data-ttu-id="2f836-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2f836-164">In Global Catalog</span></span>      | <span data-ttu-id="2f836-165">否</span><span class="sxs-lookup"><span data-stu-id="2f836-165">False</span></span>                                                       |
| <span data-ttu-id="2f836-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2f836-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f836-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2f836-167">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f836-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f836-168">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f836-169">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-170">Search-Flags</span></span>           | <span data-ttu-id="2f836-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f836-171">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f836-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-172">System-Flags</span></span>           | <span data-ttu-id="2f836-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f836-173">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f836-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2f836-174">Classes used in</span></span>        | [<span data-ttu-id="2f836-175">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="2f836-175">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2f836-176">亞當</span><span class="sxs-lookup"><span data-stu-id="2f836-176">ADAM</span></span>



| <span data-ttu-id="2f836-177">進入</span><span class="sxs-lookup"><span data-stu-id="2f836-177">Entry</span></span> | <span data-ttu-id="2f836-178">值</span><span class="sxs-lookup"><span data-stu-id="2f836-178">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f836-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2f836-179">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f836-180">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f836-181">System-Only</span></span>            | <span data-ttu-id="2f836-182">否</span><span class="sxs-lookup"><span data-stu-id="2f836-182">False</span></span>                                                       |
| <span data-ttu-id="2f836-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2f836-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2f836-184">對</span><span class="sxs-lookup"><span data-stu-id="2f836-184">True</span></span>                                                        |
| <span data-ttu-id="2f836-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2f836-185">Is Indexed</span></span>             | <span data-ttu-id="2f836-186">否</span><span class="sxs-lookup"><span data-stu-id="2f836-186">False</span></span>                                                       |
| <span data-ttu-id="2f836-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2f836-187">In Global Catalog</span></span>      | <span data-ttu-id="2f836-188">否</span><span class="sxs-lookup"><span data-stu-id="2f836-188">False</span></span>                                                       |
| <span data-ttu-id="2f836-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2f836-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f836-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2f836-190">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f836-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f836-191">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f836-192">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-193">Search-Flags</span></span>           | <span data-ttu-id="2f836-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f836-194">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f836-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-195">System-Flags</span></span>           | <span data-ttu-id="2f836-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f836-196">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f836-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2f836-197">Classes used in</span></span>        | [<span data-ttu-id="2f836-198">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="2f836-198">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2f836-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2f836-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2f836-200">進入</span><span class="sxs-lookup"><span data-stu-id="2f836-200">Entry</span></span> | <span data-ttu-id="2f836-201">值</span><span class="sxs-lookup"><span data-stu-id="2f836-201">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f836-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2f836-202">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f836-203">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f836-204">System-Only</span></span>            | <span data-ttu-id="2f836-205">否</span><span class="sxs-lookup"><span data-stu-id="2f836-205">False</span></span>                                                       |
| <span data-ttu-id="2f836-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2f836-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2f836-207">對</span><span class="sxs-lookup"><span data-stu-id="2f836-207">True</span></span>                                                        |
| <span data-ttu-id="2f836-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2f836-208">Is Indexed</span></span>             | <span data-ttu-id="2f836-209">否</span><span class="sxs-lookup"><span data-stu-id="2f836-209">False</span></span>                                                       |
| <span data-ttu-id="2f836-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2f836-210">In Global Catalog</span></span>      | <span data-ttu-id="2f836-211">否</span><span class="sxs-lookup"><span data-stu-id="2f836-211">False</span></span>                                                       |
| <span data-ttu-id="2f836-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2f836-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f836-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2f836-213">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f836-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f836-214">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f836-215">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-216">Search-Flags</span></span>           | <span data-ttu-id="2f836-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f836-217">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f836-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-218">System-Flags</span></span>           | <span data-ttu-id="2f836-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f836-219">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f836-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2f836-220">Classes used in</span></span>        | [<span data-ttu-id="2f836-221">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="2f836-221">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2f836-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f836-222">Windows Server 2008</span></span>



| <span data-ttu-id="2f836-223">進入</span><span class="sxs-lookup"><span data-stu-id="2f836-223">Entry</span></span> | <span data-ttu-id="2f836-224">值</span><span class="sxs-lookup"><span data-stu-id="2f836-224">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f836-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2f836-225">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f836-226">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f836-227">System-Only</span></span>            | <span data-ttu-id="2f836-228">否</span><span class="sxs-lookup"><span data-stu-id="2f836-228">False</span></span>                                                       |
| <span data-ttu-id="2f836-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2f836-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2f836-230">對</span><span class="sxs-lookup"><span data-stu-id="2f836-230">True</span></span>                                                        |
| <span data-ttu-id="2f836-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2f836-231">Is Indexed</span></span>             | <span data-ttu-id="2f836-232">否</span><span class="sxs-lookup"><span data-stu-id="2f836-232">False</span></span>                                                       |
| <span data-ttu-id="2f836-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2f836-233">In Global Catalog</span></span>      | <span data-ttu-id="2f836-234">否</span><span class="sxs-lookup"><span data-stu-id="2f836-234">False</span></span>                                                       |
| <span data-ttu-id="2f836-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2f836-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f836-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2f836-236">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f836-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f836-237">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f836-238">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-239">Search-Flags</span></span>           | <span data-ttu-id="2f836-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f836-240">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f836-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-241">System-Flags</span></span>           | <span data-ttu-id="2f836-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f836-242">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f836-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2f836-243">Classes used in</span></span>        | [<span data-ttu-id="2f836-244">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="2f836-244">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2f836-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f836-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2f836-246">進入</span><span class="sxs-lookup"><span data-stu-id="2f836-246">Entry</span></span> | <span data-ttu-id="2f836-247">值</span><span class="sxs-lookup"><span data-stu-id="2f836-247">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f836-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2f836-248">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f836-249">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f836-250">System-Only</span></span>            | <span data-ttu-id="2f836-251">否</span><span class="sxs-lookup"><span data-stu-id="2f836-251">False</span></span>                                                       |
| <span data-ttu-id="2f836-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2f836-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2f836-253">對</span><span class="sxs-lookup"><span data-stu-id="2f836-253">True</span></span>                                                        |
| <span data-ttu-id="2f836-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2f836-254">Is Indexed</span></span>             | <span data-ttu-id="2f836-255">否</span><span class="sxs-lookup"><span data-stu-id="2f836-255">False</span></span>                                                       |
| <span data-ttu-id="2f836-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2f836-256">In Global Catalog</span></span>      | <span data-ttu-id="2f836-257">否</span><span class="sxs-lookup"><span data-stu-id="2f836-257">False</span></span>                                                       |
| <span data-ttu-id="2f836-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2f836-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f836-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2f836-259">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f836-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f836-260">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f836-261">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-262">Search-Flags</span></span>           | <span data-ttu-id="2f836-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f836-263">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f836-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-264">System-Flags</span></span>           | <span data-ttu-id="2f836-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f836-265">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f836-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2f836-266">Classes used in</span></span>        | [<span data-ttu-id="2f836-267">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="2f836-267">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2f836-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f836-268">Windows Server 2012</span></span>



| <span data-ttu-id="2f836-269">進入</span><span class="sxs-lookup"><span data-stu-id="2f836-269">Entry</span></span> | <span data-ttu-id="2f836-270">值</span><span class="sxs-lookup"><span data-stu-id="2f836-270">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f836-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2f836-271">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f836-272">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f836-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f836-273">System-Only</span></span>            | <span data-ttu-id="2f836-274">否</span><span class="sxs-lookup"><span data-stu-id="2f836-274">False</span></span>                                                       |
| <span data-ttu-id="2f836-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2f836-275">Is-Single-Valued</span></span>       | <span data-ttu-id="2f836-276">對</span><span class="sxs-lookup"><span data-stu-id="2f836-276">True</span></span>                                                        |
| <span data-ttu-id="2f836-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2f836-277">Is Indexed</span></span>             | <span data-ttu-id="2f836-278">否</span><span class="sxs-lookup"><span data-stu-id="2f836-278">False</span></span>                                                       |
| <span data-ttu-id="2f836-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2f836-279">In Global Catalog</span></span>      | <span data-ttu-id="2f836-280">否</span><span class="sxs-lookup"><span data-stu-id="2f836-280">False</span></span>                                                       |
| <span data-ttu-id="2f836-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2f836-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f836-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2f836-282">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f836-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f836-283">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f836-284">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f836-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-285">Search-Flags</span></span>           | <span data-ttu-id="2f836-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f836-286">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f836-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f836-287">System-Flags</span></span>           | <span data-ttu-id="2f836-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f836-288">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f836-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2f836-289">Classes used in</span></span>        | [<span data-ttu-id="2f836-290">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="2f836-290">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 






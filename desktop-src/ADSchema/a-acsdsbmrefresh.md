---
title: ACS-DSBM-Refresh 屬性
description: 此屬性包含的間隔計時器值，可決定指定的子網路頻寬管理員 (DSBM) 送出重新整理訊息 (\_ 我 \_) 到網域中的所有子網路頻寬管理員。
ms.assetid: 018fd748-ca2e-41e1-a920-224a32e13e21
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-Refresh 屬性 AD 架構
- aCSDSBMRefresh 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-DSBM-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d662b886a8c97f3d155d3c1b40efcef67f7f1f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935304"
---
# <a name="acs-dsbm-refresh-attribute"></a><span data-ttu-id="c94b4-105">ACS-DSBM-Refresh 屬性</span><span class="sxs-lookup"><span data-stu-id="c94b4-105">ACS-DSBM-Refresh attribute</span></span>

<span data-ttu-id="c94b4-106">此屬性包含的間隔計時器值，可決定指定的子網路頻寬管理員 (DSBM) 送出重新整理訊息 (\_ 我 \_) 到網域中的所有子網路頻寬管理員。</span><span class="sxs-lookup"><span data-stu-id="c94b4-106">This attribute contains the interval timer value that determines when the Designated Subnet Bandwidth Manager (DSBM) sends out a refresh message (I\_AM\_DSBM) to all of the Subnet Bandwidth Managers in a domain.</span></span>



| <span data-ttu-id="c94b4-107">進入</span><span class="sxs-lookup"><span data-stu-id="c94b4-107">Entry</span></span> | <span data-ttu-id="c94b4-108">值</span><span class="sxs-lookup"><span data-stu-id="c94b4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c94b4-109">CN</span><span class="sxs-lookup"><span data-stu-id="c94b4-109">CN</span></span>                | <span data-ttu-id="c94b4-110">ACS-DSBM-重新整理</span><span class="sxs-lookup"><span data-stu-id="c94b4-110">ACS-DSBM-Refresh</span></span>                     |
| <span data-ttu-id="c94b4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c94b4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c94b4-112">aCSDSBMRefresh</span><span class="sxs-lookup"><span data-stu-id="c94b4-112">aCSDSBMRefresh</span></span>                       |
| <span data-ttu-id="c94b4-113">大小</span><span class="sxs-lookup"><span data-stu-id="c94b4-113">Size</span></span>              | <span data-ttu-id="c94b4-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="c94b4-114">4 bytes</span></span>                              |
| <span data-ttu-id="c94b4-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c94b4-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c94b4-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c94b4-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c94b4-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c94b4-117">Attribute-Id</span></span>      | <span data-ttu-id="c94b4-118">1.2.840.113556.1.4.777</span><span class="sxs-lookup"><span data-stu-id="c94b4-118">1.2.840.113556.1.4.777</span></span>               |
| <span data-ttu-id="c94b4-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c94b4-119">System-Id-Guid</span></span>    | <span data-ttu-id="c94b4-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c94b4-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="c94b4-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c94b4-121">Syntax</span></span>            | [<span data-ttu-id="c94b4-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="c94b4-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c94b4-123">實作</span><span class="sxs-lookup"><span data-stu-id="c94b4-123">Implementations</span></span>

-   [<span data-ttu-id="c94b4-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c94b4-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c94b4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c94b4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c94b4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c94b4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c94b4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c94b4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c94b4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c94b4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c94b4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c94b4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c94b4-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c94b4-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c94b4-131">進入</span><span class="sxs-lookup"><span data-stu-id="c94b4-131">Entry</span></span> | <span data-ttu-id="c94b4-132">值</span><span class="sxs-lookup"><span data-stu-id="c94b4-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c94b4-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c94b4-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c94b4-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c94b4-135">System-Only</span></span>            | <span data-ttu-id="c94b4-136">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-136">False</span></span>                                        |
| <span data-ttu-id="c94b4-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c94b4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c94b4-138">對</span><span class="sxs-lookup"><span data-stu-id="c94b4-138">True</span></span>                                         |
| <span data-ttu-id="c94b4-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c94b4-139">Is Indexed</span></span>             | <span data-ttu-id="c94b4-140">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-140">False</span></span>                                        |
| <span data-ttu-id="c94b4-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c94b4-141">In Global Catalog</span></span>      | <span data-ttu-id="c94b4-142">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-142">False</span></span>                                        |
| <span data-ttu-id="c94b4-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c94b4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c94b4-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c94b4-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c94b4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c94b4-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c94b4-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-147">Search-Flags</span></span>           | <span data-ttu-id="c94b4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c94b4-148">0x00000000</span></span>                                   |
| <span data-ttu-id="c94b4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-149">System-Flags</span></span>           | <span data-ttu-id="c94b4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c94b4-150">0x00000010</span></span>                                   |
| <span data-ttu-id="c94b4-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c94b4-151">Classes used in</span></span>        | [<span data-ttu-id="c94b4-152">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c94b4-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c94b4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c94b4-153">Windows Server 2003</span></span>



| <span data-ttu-id="c94b4-154">進入</span><span class="sxs-lookup"><span data-stu-id="c94b4-154">Entry</span></span> | <span data-ttu-id="c94b4-155">值</span><span class="sxs-lookup"><span data-stu-id="c94b4-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c94b4-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c94b4-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c94b4-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c94b4-158">System-Only</span></span>            | <span data-ttu-id="c94b4-159">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-159">False</span></span>                                        |
| <span data-ttu-id="c94b4-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c94b4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c94b4-161">對</span><span class="sxs-lookup"><span data-stu-id="c94b4-161">True</span></span>                                         |
| <span data-ttu-id="c94b4-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c94b4-162">Is Indexed</span></span>             | <span data-ttu-id="c94b4-163">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-163">False</span></span>                                        |
| <span data-ttu-id="c94b4-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c94b4-164">In Global Catalog</span></span>      | <span data-ttu-id="c94b4-165">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-165">False</span></span>                                        |
| <span data-ttu-id="c94b4-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c94b4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c94b4-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c94b4-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c94b4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c94b4-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c94b4-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-170">Search-Flags</span></span>           | <span data-ttu-id="c94b4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c94b4-171">0x00000000</span></span>                                   |
| <span data-ttu-id="c94b4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-172">System-Flags</span></span>           | <span data-ttu-id="c94b4-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c94b4-173">0x00000010</span></span>                                   |
| <span data-ttu-id="c94b4-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c94b4-174">Classes used in</span></span>        | [<span data-ttu-id="c94b4-175">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c94b4-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c94b4-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c94b4-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c94b4-177">進入</span><span class="sxs-lookup"><span data-stu-id="c94b4-177">Entry</span></span> | <span data-ttu-id="c94b4-178">值</span><span class="sxs-lookup"><span data-stu-id="c94b4-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c94b4-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c94b4-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c94b4-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c94b4-181">System-Only</span></span>            | <span data-ttu-id="c94b4-182">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-182">False</span></span>                                        |
| <span data-ttu-id="c94b4-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c94b4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c94b4-184">對</span><span class="sxs-lookup"><span data-stu-id="c94b4-184">True</span></span>                                         |
| <span data-ttu-id="c94b4-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c94b4-185">Is Indexed</span></span>             | <span data-ttu-id="c94b4-186">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-186">False</span></span>                                        |
| <span data-ttu-id="c94b4-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c94b4-187">In Global Catalog</span></span>      | <span data-ttu-id="c94b4-188">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-188">False</span></span>                                        |
| <span data-ttu-id="c94b4-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c94b4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c94b4-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c94b4-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c94b4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c94b4-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c94b4-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-193">Search-Flags</span></span>           | <span data-ttu-id="c94b4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c94b4-194">0x00000000</span></span>                                   |
| <span data-ttu-id="c94b4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-195">System-Flags</span></span>           | <span data-ttu-id="c94b4-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c94b4-196">0x00000010</span></span>                                   |
| <span data-ttu-id="c94b4-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c94b4-197">Classes used in</span></span>        | [<span data-ttu-id="c94b4-198">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c94b4-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c94b4-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c94b4-199">Windows Server 2008</span></span>



| <span data-ttu-id="c94b4-200">進入</span><span class="sxs-lookup"><span data-stu-id="c94b4-200">Entry</span></span> | <span data-ttu-id="c94b4-201">值</span><span class="sxs-lookup"><span data-stu-id="c94b4-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c94b4-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c94b4-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c94b4-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c94b4-204">System-Only</span></span>            | <span data-ttu-id="c94b4-205">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-205">False</span></span>                                        |
| <span data-ttu-id="c94b4-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c94b4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c94b4-207">對</span><span class="sxs-lookup"><span data-stu-id="c94b4-207">True</span></span>                                         |
| <span data-ttu-id="c94b4-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c94b4-208">Is Indexed</span></span>             | <span data-ttu-id="c94b4-209">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-209">False</span></span>                                        |
| <span data-ttu-id="c94b4-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c94b4-210">In Global Catalog</span></span>      | <span data-ttu-id="c94b4-211">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-211">False</span></span>                                        |
| <span data-ttu-id="c94b4-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c94b4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c94b4-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c94b4-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c94b4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c94b4-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c94b4-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-216">Search-Flags</span></span>           | <span data-ttu-id="c94b4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c94b4-217">0x00000000</span></span>                                   |
| <span data-ttu-id="c94b4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-218">System-Flags</span></span>           | <span data-ttu-id="c94b4-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c94b4-219">0x00000010</span></span>                                   |
| <span data-ttu-id="c94b4-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c94b4-220">Classes used in</span></span>        | [<span data-ttu-id="c94b4-221">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c94b4-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c94b4-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c94b4-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c94b4-223">進入</span><span class="sxs-lookup"><span data-stu-id="c94b4-223">Entry</span></span> | <span data-ttu-id="c94b4-224">值</span><span class="sxs-lookup"><span data-stu-id="c94b4-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c94b4-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c94b4-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c94b4-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c94b4-227">System-Only</span></span>            | <span data-ttu-id="c94b4-228">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-228">False</span></span>                                        |
| <span data-ttu-id="c94b4-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c94b4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c94b4-230">對</span><span class="sxs-lookup"><span data-stu-id="c94b4-230">True</span></span>                                         |
| <span data-ttu-id="c94b4-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c94b4-231">Is Indexed</span></span>             | <span data-ttu-id="c94b4-232">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-232">False</span></span>                                        |
| <span data-ttu-id="c94b4-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c94b4-233">In Global Catalog</span></span>      | <span data-ttu-id="c94b4-234">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-234">False</span></span>                                        |
| <span data-ttu-id="c94b4-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c94b4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c94b4-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c94b4-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c94b4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c94b4-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c94b4-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-239">Search-Flags</span></span>           | <span data-ttu-id="c94b4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c94b4-240">0x00000000</span></span>                                   |
| <span data-ttu-id="c94b4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-241">System-Flags</span></span>           | <span data-ttu-id="c94b4-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c94b4-242">0x00000010</span></span>                                   |
| <span data-ttu-id="c94b4-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c94b4-243">Classes used in</span></span>        | [<span data-ttu-id="c94b4-244">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c94b4-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c94b4-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c94b4-245">Windows Server 2012</span></span>



| <span data-ttu-id="c94b4-246">進入</span><span class="sxs-lookup"><span data-stu-id="c94b4-246">Entry</span></span> | <span data-ttu-id="c94b4-247">值</span><span class="sxs-lookup"><span data-stu-id="c94b4-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c94b4-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c94b4-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c94b4-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c94b4-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c94b4-250">System-Only</span></span>            | <span data-ttu-id="c94b4-251">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-251">False</span></span>                                        |
| <span data-ttu-id="c94b4-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c94b4-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c94b4-253">對</span><span class="sxs-lookup"><span data-stu-id="c94b4-253">True</span></span>                                         |
| <span data-ttu-id="c94b4-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c94b4-254">Is Indexed</span></span>             | <span data-ttu-id="c94b4-255">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-255">False</span></span>                                        |
| <span data-ttu-id="c94b4-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c94b4-256">In Global Catalog</span></span>      | <span data-ttu-id="c94b4-257">否</span><span class="sxs-lookup"><span data-stu-id="c94b4-257">False</span></span>                                        |
| <span data-ttu-id="c94b4-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c94b4-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c94b4-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c94b4-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c94b4-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c94b4-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c94b4-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c94b4-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-262">Search-Flags</span></span>           | <span data-ttu-id="c94b4-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c94b4-263">0x00000000</span></span>                                   |
| <span data-ttu-id="c94b4-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c94b4-264">System-Flags</span></span>           | <span data-ttu-id="c94b4-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c94b4-265">0x00000010</span></span>                                   |
| <span data-ttu-id="c94b4-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c94b4-266">Classes used in</span></span>        | [<span data-ttu-id="c94b4-267">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c94b4-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






---
title: ACS-每個流程的最大持續時間屬性
description: 任何單一流程的最大持續時間（以秒為單位）。
ms.assetid: 070d3ffe-1d54-4f78-b5a7-3c8ef39d9346
ms.tgt_platform: multiple
keywords:
- ACS-最大持續時間-每一流量的屬性 AD 架構
- aCSMaxDurationPerFlow 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Max-Duration-Per-Flow
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db53a2116087cadb1e58af234a1741e144fbf916
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971085"
---
# <a name="acs-max-duration-per-flow-attribute"></a><span data-ttu-id="ffd6f-105">ACS-每個流程的最大持續時間屬性</span><span class="sxs-lookup"><span data-stu-id="ffd6f-105">ACS-Max-Duration-Per-Flow attribute</span></span>

<span data-ttu-id="ffd6f-106">任何單一流程的最大持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ffd6f-106">The maximum duration, in seconds, of any single flow.</span></span>



| <span data-ttu-id="ffd6f-107">進入</span><span class="sxs-lookup"><span data-stu-id="ffd6f-107">Entry</span></span> | <span data-ttu-id="ffd6f-108">值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ffd6f-109">CN</span><span class="sxs-lookup"><span data-stu-id="ffd6f-109">CN</span></span>                | <span data-ttu-id="ffd6f-110">ACS-每個流程的最大持續時間</span><span class="sxs-lookup"><span data-stu-id="ffd6f-110">ACS-Max-Duration-Per-Flow</span></span>            |
| <span data-ttu-id="ffd6f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ffd6f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ffd6f-112">aCSMaxDurationPerFlow</span><span class="sxs-lookup"><span data-stu-id="ffd6f-112">aCSMaxDurationPerFlow</span></span>                |
| <span data-ttu-id="ffd6f-113">大小</span><span class="sxs-lookup"><span data-stu-id="ffd6f-113">Size</span></span>              | <span data-ttu-id="ffd6f-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ffd6f-114">4 bytes</span></span>                              |
| <span data-ttu-id="ffd6f-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ffd6f-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ffd6f-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ffd6f-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ffd6f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ffd6f-117">Attribute-Id</span></span>      | <span data-ttu-id="ffd6f-118">1.2.840.113556.1.4.761</span><span class="sxs-lookup"><span data-stu-id="ffd6f-118">1.2.840.113556.1.4.761</span></span>               |
| <span data-ttu-id="ffd6f-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ffd6f-119">System-Id-Guid</span></span>    | <span data-ttu-id="ffd6f-120">7f56127e-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ffd6f-120">7f56127e-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="ffd6f-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffd6f-121">Syntax</span></span>            | [<span data-ttu-id="ffd6f-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ffd6f-123">實作</span><span class="sxs-lookup"><span data-stu-id="ffd6f-123">Implementations</span></span>

-   [<span data-ttu-id="ffd6f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ffd6f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ffd6f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ffd6f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ffd6f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ffd6f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ffd6f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ffd6f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ffd6f-131">進入</span><span class="sxs-lookup"><span data-stu-id="ffd6f-131">Entry</span></span> | <span data-ttu-id="ffd6f-132">值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd6f-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd6f-133">Link-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd6f-134">MAPI-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd6f-135">System-Only</span></span>            | <span data-ttu-id="ffd6f-136">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-136">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd6f-138">對</span><span class="sxs-lookup"><span data-stu-id="ffd6f-138">True</span></span>                                                                                      |
| <span data-ttu-id="ffd6f-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd6f-139">Is Indexed</span></span>             | <span data-ttu-id="ffd6f-140">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-140">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd6f-141">In Global Catalog</span></span>      | <span data-ttu-id="ffd6f-142">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-142">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd6f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd6f-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd6f-144">O:BAG:BAD:S:</span></span>                                                                              |
| <span data-ttu-id="ffd6f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd6f-145">Range-Lower</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd6f-146">Range-Upper</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-147">Search-Flags</span></span>           | <span data-ttu-id="ffd6f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffd6f-148">0x00000000</span></span>                                                                                |
| <span data-ttu-id="ffd6f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-149">System-Flags</span></span>           | <span data-ttu-id="ffd6f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffd6f-150">0x00000010</span></span>                                                                                |
| <span data-ttu-id="ffd6f-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd6f-151">Classes used in</span></span>        | [<span data-ttu-id="ffd6f-152">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="ffd6f-153">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ffd6f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ffd6f-154">Windows Server 2003</span></span>



| <span data-ttu-id="ffd6f-155">進入</span><span class="sxs-lookup"><span data-stu-id="ffd6f-155">Entry</span></span> | <span data-ttu-id="ffd6f-156">值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd6f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd6f-157">Link-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd6f-158">MAPI-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd6f-159">System-Only</span></span>            | <span data-ttu-id="ffd6f-160">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-160">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd6f-162">對</span><span class="sxs-lookup"><span data-stu-id="ffd6f-162">True</span></span>                                                                                      |
| <span data-ttu-id="ffd6f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd6f-163">Is Indexed</span></span>             | <span data-ttu-id="ffd6f-164">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-164">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd6f-165">In Global Catalog</span></span>      | <span data-ttu-id="ffd6f-166">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-166">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd6f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd6f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd6f-168">O:BAG:BAD:S:</span></span>                                                                              |
| <span data-ttu-id="ffd6f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd6f-169">Range-Lower</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd6f-170">Range-Upper</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-171">Search-Flags</span></span>           | <span data-ttu-id="ffd6f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffd6f-172">0x00000000</span></span>                                                                                |
| <span data-ttu-id="ffd6f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-173">System-Flags</span></span>           | <span data-ttu-id="ffd6f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffd6f-174">0x00000010</span></span>                                                                                |
| <span data-ttu-id="ffd6f-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd6f-175">Classes used in</span></span>        | [<span data-ttu-id="ffd6f-176">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="ffd6f-177">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ffd6f-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ffd6f-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ffd6f-179">進入</span><span class="sxs-lookup"><span data-stu-id="ffd6f-179">Entry</span></span> | <span data-ttu-id="ffd6f-180">值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd6f-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd6f-181">Link-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd6f-182">MAPI-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd6f-183">System-Only</span></span>            | <span data-ttu-id="ffd6f-184">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-184">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd6f-186">對</span><span class="sxs-lookup"><span data-stu-id="ffd6f-186">True</span></span>                                                                                      |
| <span data-ttu-id="ffd6f-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd6f-187">Is Indexed</span></span>             | <span data-ttu-id="ffd6f-188">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-188">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd6f-189">In Global Catalog</span></span>      | <span data-ttu-id="ffd6f-190">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-190">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd6f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd6f-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd6f-192">O:BAG:BAD:S:</span></span>                                                                              |
| <span data-ttu-id="ffd6f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd6f-193">Range-Lower</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd6f-194">Range-Upper</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-195">Search-Flags</span></span>           | <span data-ttu-id="ffd6f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffd6f-196">0x00000000</span></span>                                                                                |
| <span data-ttu-id="ffd6f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-197">System-Flags</span></span>           | <span data-ttu-id="ffd6f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffd6f-198">0x00000010</span></span>                                                                                |
| <span data-ttu-id="ffd6f-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd6f-199">Classes used in</span></span>        | [<span data-ttu-id="ffd6f-200">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-200">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="ffd6f-201">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-201">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ffd6f-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffd6f-202">Windows Server 2008</span></span>



| <span data-ttu-id="ffd6f-203">進入</span><span class="sxs-lookup"><span data-stu-id="ffd6f-203">Entry</span></span> | <span data-ttu-id="ffd6f-204">值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd6f-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd6f-205">Link-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd6f-206">MAPI-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd6f-207">System-Only</span></span>            | <span data-ttu-id="ffd6f-208">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-208">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-209">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd6f-210">對</span><span class="sxs-lookup"><span data-stu-id="ffd6f-210">True</span></span>                                                                                      |
| <span data-ttu-id="ffd6f-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd6f-211">Is Indexed</span></span>             | <span data-ttu-id="ffd6f-212">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-212">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd6f-213">In Global Catalog</span></span>      | <span data-ttu-id="ffd6f-214">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-214">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd6f-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd6f-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd6f-216">O:BAG:BAD:S:</span></span>                                                                              |
| <span data-ttu-id="ffd6f-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd6f-217">Range-Lower</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd6f-218">Range-Upper</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-219">Search-Flags</span></span>           | <span data-ttu-id="ffd6f-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffd6f-220">0x00000000</span></span>                                                                                |
| <span data-ttu-id="ffd6f-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-221">System-Flags</span></span>           | <span data-ttu-id="ffd6f-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffd6f-222">0x00000010</span></span>                                                                                |
| <span data-ttu-id="ffd6f-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd6f-223">Classes used in</span></span>        | [<span data-ttu-id="ffd6f-224">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-224">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="ffd6f-225">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-225">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ffd6f-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffd6f-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ffd6f-227">進入</span><span class="sxs-lookup"><span data-stu-id="ffd6f-227">Entry</span></span> | <span data-ttu-id="ffd6f-228">值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-228">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd6f-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd6f-229">Link-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd6f-230">MAPI-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd6f-231">System-Only</span></span>            | <span data-ttu-id="ffd6f-232">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-232">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd6f-234">對</span><span class="sxs-lookup"><span data-stu-id="ffd6f-234">True</span></span>                                                                                      |
| <span data-ttu-id="ffd6f-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd6f-235">Is Indexed</span></span>             | <span data-ttu-id="ffd6f-236">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-236">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd6f-237">In Global Catalog</span></span>      | <span data-ttu-id="ffd6f-238">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-238">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd6f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd6f-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd6f-240">O:BAG:BAD:S:</span></span>                                                                              |
| <span data-ttu-id="ffd6f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd6f-241">Range-Lower</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd6f-242">Range-Upper</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-243">Search-Flags</span></span>           | <span data-ttu-id="ffd6f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffd6f-244">0x00000000</span></span>                                                                                |
| <span data-ttu-id="ffd6f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-245">System-Flags</span></span>           | <span data-ttu-id="ffd6f-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffd6f-246">0x00000010</span></span>                                                                                |
| <span data-ttu-id="ffd6f-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd6f-247">Classes used in</span></span>        | [<span data-ttu-id="ffd6f-248">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-248">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="ffd6f-249">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-249">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ffd6f-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffd6f-250">Windows Server 2012</span></span>



| <span data-ttu-id="ffd6f-251">進入</span><span class="sxs-lookup"><span data-stu-id="ffd6f-251">Entry</span></span> | <span data-ttu-id="ffd6f-252">值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-252">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd6f-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffd6f-253">Link-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffd6f-254">MAPI-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="ffd6f-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffd6f-255">System-Only</span></span>            | <span data-ttu-id="ffd6f-256">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-256">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffd6f-257">Is-Single-Valued</span></span>       | <span data-ttu-id="ffd6f-258">對</span><span class="sxs-lookup"><span data-stu-id="ffd6f-258">True</span></span>                                                                                      |
| <span data-ttu-id="ffd6f-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffd6f-259">Is Indexed</span></span>             | <span data-ttu-id="ffd6f-260">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-260">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffd6f-261">In Global Catalog</span></span>      | <span data-ttu-id="ffd6f-262">否</span><span class="sxs-lookup"><span data-stu-id="ffd6f-262">False</span></span>                                                                                     |
| <span data-ttu-id="ffd6f-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffd6f-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffd6f-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffd6f-264">O:BAG:BAD:S:</span></span>                                                                              |
| <span data-ttu-id="ffd6f-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffd6f-265">Range-Lower</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffd6f-266">Range-Upper</span></span>            | \-                                                                                        |
| <span data-ttu-id="ffd6f-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-267">Search-Flags</span></span>           | <span data-ttu-id="ffd6f-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffd6f-268">0x00000000</span></span>                                                                                |
| <span data-ttu-id="ffd6f-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffd6f-269">System-Flags</span></span>           | <span data-ttu-id="ffd6f-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffd6f-270">0x00000010</span></span>                                                                                |
| <span data-ttu-id="ffd6f-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffd6f-271">Classes used in</span></span>        | [<span data-ttu-id="ffd6f-272">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-272">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="ffd6f-273">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="ffd6f-273">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






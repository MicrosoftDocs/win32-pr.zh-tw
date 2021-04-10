---
title: ACS-最大權杖-每個流程的速率-每個流程屬性
description: 特定使用者的所有單一流程可能具有的最大權杖速率。
ms.assetid: 2898b7a6-f2b1-4e08-aba6-9e1ac655a4db
ms.tgt_platform: multiple
keywords:
- ACS-最大權杖-每個流程的每個流程屬性 AD 架構
- aCSMaxTokenRatePerFlow 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Max-Token-Rate-Per-Flow
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5165c20a27f7d1a389b9aada118d89786c015d2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104025539"
---
# <a name="acs-max-token-rate-per-flow-attribute"></a><span data-ttu-id="0af13-105">ACS-最大權杖-每個流程的速率-每個流程屬性</span><span class="sxs-lookup"><span data-stu-id="0af13-105">ACS-Max-Token-Rate-Per-Flow attribute</span></span>

<span data-ttu-id="0af13-106">特定使用者的所有單一流程可能具有的最大權杖速率。</span><span class="sxs-lookup"><span data-stu-id="0af13-106">The maximum token rate any single flow may have for a given user.</span></span>



| <span data-ttu-id="0af13-107">進入</span><span class="sxs-lookup"><span data-stu-id="0af13-107">Entry</span></span> | <span data-ttu-id="0af13-108">值</span><span class="sxs-lookup"><span data-stu-id="0af13-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0af13-109">CN</span><span class="sxs-lookup"><span data-stu-id="0af13-109">CN</span></span>                | <span data-ttu-id="0af13-110">ACS-最大權杖-每個流程的速率</span><span class="sxs-lookup"><span data-stu-id="0af13-110">ACS-Max-Token-Rate-Per-Flow</span></span>          |
| <span data-ttu-id="0af13-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0af13-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0af13-112">aCSMaxTokenRatePerFlow</span><span class="sxs-lookup"><span data-stu-id="0af13-112">aCSMaxTokenRatePerFlow</span></span>               |
| <span data-ttu-id="0af13-113">大小</span><span class="sxs-lookup"><span data-stu-id="0af13-113">Size</span></span>              | <span data-ttu-id="0af13-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="0af13-114">8 bytes</span></span>                              |
| <span data-ttu-id="0af13-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0af13-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="0af13-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0af13-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0af13-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0af13-117">Attribute-Id</span></span>      | <span data-ttu-id="0af13-118">1.2.840.113556.1.4.758</span><span class="sxs-lookup"><span data-stu-id="0af13-118">1.2.840.113556.1.4.758</span></span>               |
| <span data-ttu-id="0af13-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0af13-119">System-Id-Guid</span></span>    | <span data-ttu-id="0af13-120">7f56127b-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0af13-120">7f56127b-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="0af13-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="0af13-121">Syntax</span></span>            | [<span data-ttu-id="0af13-122">**間隔**</span><span class="sxs-lookup"><span data-stu-id="0af13-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0af13-123">實作</span><span class="sxs-lookup"><span data-stu-id="0af13-123">Implementations</span></span>

-   [<span data-ttu-id="0af13-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0af13-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0af13-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0af13-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0af13-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0af13-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0af13-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0af13-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0af13-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0af13-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0af13-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0af13-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0af13-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0af13-130">Windows 2000 Server</span></span>



| <span data-ttu-id="0af13-131">進入</span><span class="sxs-lookup"><span data-stu-id="0af13-131">Entry</span></span> | <span data-ttu-id="0af13-132">值</span><span class="sxs-lookup"><span data-stu-id="0af13-132">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af13-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0af13-133">Link-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af13-134">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af13-135">System-Only</span></span>            | <span data-ttu-id="0af13-136">否</span><span class="sxs-lookup"><span data-stu-id="0af13-136">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0af13-137">Is-Single-Valued</span></span>       | <span data-ttu-id="0af13-138">對</span><span class="sxs-lookup"><span data-stu-id="0af13-138">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="0af13-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0af13-139">Is Indexed</span></span>             | <span data-ttu-id="0af13-140">否</span><span class="sxs-lookup"><span data-stu-id="0af13-140">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0af13-141">In Global Catalog</span></span>      | <span data-ttu-id="0af13-142">否</span><span class="sxs-lookup"><span data-stu-id="0af13-142">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0af13-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af13-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0af13-144">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="0af13-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af13-145">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af13-146">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-147">Search-Flags</span></span>           | <span data-ttu-id="0af13-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af13-148">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-149">System-Flags</span></span>           | <span data-ttu-id="0af13-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af13-150">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0af13-151">Classes used in</span></span>        | [<span data-ttu-id="0af13-152">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="0af13-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="0af13-153">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="0af13-153">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="0af13-154">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0af13-154">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0af13-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0af13-155">Windows Server 2003</span></span>



| <span data-ttu-id="0af13-156">進入</span><span class="sxs-lookup"><span data-stu-id="0af13-156">Entry</span></span> | <span data-ttu-id="0af13-157">值</span><span class="sxs-lookup"><span data-stu-id="0af13-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af13-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0af13-158">Link-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af13-159">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af13-160">System-Only</span></span>            | <span data-ttu-id="0af13-161">否</span><span class="sxs-lookup"><span data-stu-id="0af13-161">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0af13-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0af13-163">對</span><span class="sxs-lookup"><span data-stu-id="0af13-163">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="0af13-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0af13-164">Is Indexed</span></span>             | <span data-ttu-id="0af13-165">否</span><span class="sxs-lookup"><span data-stu-id="0af13-165">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0af13-166">In Global Catalog</span></span>      | <span data-ttu-id="0af13-167">否</span><span class="sxs-lookup"><span data-stu-id="0af13-167">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0af13-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af13-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0af13-169">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="0af13-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af13-170">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af13-171">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-172">Search-Flags</span></span>           | <span data-ttu-id="0af13-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af13-173">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-174">System-Flags</span></span>           | <span data-ttu-id="0af13-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af13-175">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0af13-176">Classes used in</span></span>        | [<span data-ttu-id="0af13-177">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="0af13-177">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="0af13-178">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="0af13-178">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="0af13-179">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0af13-179">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0af13-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0af13-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0af13-181">進入</span><span class="sxs-lookup"><span data-stu-id="0af13-181">Entry</span></span> | <span data-ttu-id="0af13-182">值</span><span class="sxs-lookup"><span data-stu-id="0af13-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af13-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0af13-183">Link-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af13-184">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af13-185">System-Only</span></span>            | <span data-ttu-id="0af13-186">否</span><span class="sxs-lookup"><span data-stu-id="0af13-186">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0af13-187">Is-Single-Valued</span></span>       | <span data-ttu-id="0af13-188">對</span><span class="sxs-lookup"><span data-stu-id="0af13-188">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="0af13-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0af13-189">Is Indexed</span></span>             | <span data-ttu-id="0af13-190">否</span><span class="sxs-lookup"><span data-stu-id="0af13-190">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0af13-191">In Global Catalog</span></span>      | <span data-ttu-id="0af13-192">否</span><span class="sxs-lookup"><span data-stu-id="0af13-192">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0af13-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af13-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0af13-194">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="0af13-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af13-195">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af13-196">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-197">Search-Flags</span></span>           | <span data-ttu-id="0af13-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af13-198">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-199">System-Flags</span></span>           | <span data-ttu-id="0af13-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af13-200">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0af13-201">Classes used in</span></span>        | [<span data-ttu-id="0af13-202">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="0af13-202">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="0af13-203">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="0af13-203">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="0af13-204">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0af13-204">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0af13-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0af13-205">Windows Server 2008</span></span>



| <span data-ttu-id="0af13-206">進入</span><span class="sxs-lookup"><span data-stu-id="0af13-206">Entry</span></span> | <span data-ttu-id="0af13-207">值</span><span class="sxs-lookup"><span data-stu-id="0af13-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af13-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0af13-208">Link-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af13-209">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af13-210">System-Only</span></span>            | <span data-ttu-id="0af13-211">否</span><span class="sxs-lookup"><span data-stu-id="0af13-211">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0af13-212">Is-Single-Valued</span></span>       | <span data-ttu-id="0af13-213">對</span><span class="sxs-lookup"><span data-stu-id="0af13-213">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="0af13-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0af13-214">Is Indexed</span></span>             | <span data-ttu-id="0af13-215">否</span><span class="sxs-lookup"><span data-stu-id="0af13-215">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0af13-216">In Global Catalog</span></span>      | <span data-ttu-id="0af13-217">否</span><span class="sxs-lookup"><span data-stu-id="0af13-217">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0af13-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af13-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0af13-219">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="0af13-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af13-220">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af13-221">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-222">Search-Flags</span></span>           | <span data-ttu-id="0af13-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af13-223">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-224">System-Flags</span></span>           | <span data-ttu-id="0af13-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af13-225">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0af13-226">Classes used in</span></span>        | [<span data-ttu-id="0af13-227">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="0af13-227">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="0af13-228">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="0af13-228">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="0af13-229">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0af13-229">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0af13-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0af13-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0af13-231">進入</span><span class="sxs-lookup"><span data-stu-id="0af13-231">Entry</span></span> | <span data-ttu-id="0af13-232">值</span><span class="sxs-lookup"><span data-stu-id="0af13-232">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af13-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0af13-233">Link-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af13-234">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af13-235">System-Only</span></span>            | <span data-ttu-id="0af13-236">否</span><span class="sxs-lookup"><span data-stu-id="0af13-236">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0af13-237">Is-Single-Valued</span></span>       | <span data-ttu-id="0af13-238">對</span><span class="sxs-lookup"><span data-stu-id="0af13-238">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="0af13-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0af13-239">Is Indexed</span></span>             | <span data-ttu-id="0af13-240">否</span><span class="sxs-lookup"><span data-stu-id="0af13-240">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0af13-241">In Global Catalog</span></span>      | <span data-ttu-id="0af13-242">否</span><span class="sxs-lookup"><span data-stu-id="0af13-242">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0af13-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af13-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0af13-244">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="0af13-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af13-245">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af13-246">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-247">Search-Flags</span></span>           | <span data-ttu-id="0af13-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af13-248">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-249">System-Flags</span></span>           | <span data-ttu-id="0af13-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af13-250">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0af13-251">Classes used in</span></span>        | [<span data-ttu-id="0af13-252">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="0af13-252">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="0af13-253">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="0af13-253">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="0af13-254">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0af13-254">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0af13-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0af13-255">Windows Server 2012</span></span>



| <span data-ttu-id="0af13-256">進入</span><span class="sxs-lookup"><span data-stu-id="0af13-256">Entry</span></span> | <span data-ttu-id="0af13-257">值</span><span class="sxs-lookup"><span data-stu-id="0af13-257">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af13-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0af13-258">Link-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0af13-259">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="0af13-260">System-Only</span></span>            | <span data-ttu-id="0af13-261">否</span><span class="sxs-lookup"><span data-stu-id="0af13-261">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0af13-262">Is-Single-Valued</span></span>       | <span data-ttu-id="0af13-263">對</span><span class="sxs-lookup"><span data-stu-id="0af13-263">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="0af13-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0af13-264">Is Indexed</span></span>             | <span data-ttu-id="0af13-265">否</span><span class="sxs-lookup"><span data-stu-id="0af13-265">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0af13-266">In Global Catalog</span></span>      | <span data-ttu-id="0af13-267">否</span><span class="sxs-lookup"><span data-stu-id="0af13-267">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="0af13-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0af13-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="0af13-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0af13-269">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="0af13-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0af13-270">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0af13-271">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="0af13-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-272">Search-Flags</span></span>           | <span data-ttu-id="0af13-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0af13-273">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0af13-274">System-Flags</span></span>           | <span data-ttu-id="0af13-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0af13-275">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="0af13-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0af13-276">Classes used in</span></span>        | [<span data-ttu-id="0af13-277">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="0af13-277">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="0af13-278">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="0af13-278">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="0af13-279">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0af13-279">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






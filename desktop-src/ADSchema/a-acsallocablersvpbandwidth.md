---
title: ACS-Allocable-RSVP-頻寬屬性
description: 可以保留的最大頻寬。
ms.assetid: 18d9a5c5-e44c-49e9-a8f0-9386a7b1ff97
ms.tgt_platform: multiple
keywords:
- ACS-Allocable-RSVP-頻寬屬性 AD 架構
- aCSAllocableRSVPBandwidth 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Allocable-RSVP-Bandwidth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6bfe98d30fb8ef959f2e75d078b3a04b325b6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845655"
---
# <a name="acs-allocable-rsvp-bandwidth-attribute"></a><span data-ttu-id="c1030-105">ACS-Allocable-RSVP-頻寬屬性</span><span class="sxs-lookup"><span data-stu-id="c1030-105">ACS-Allocable-RSVP-Bandwidth attribute</span></span>

<span data-ttu-id="c1030-106">可以保留的最大頻寬。</span><span class="sxs-lookup"><span data-stu-id="c1030-106">The maximum bandwidth that can be reserved.</span></span>



| <span data-ttu-id="c1030-107">進入</span><span class="sxs-lookup"><span data-stu-id="c1030-107">Entry</span></span> | <span data-ttu-id="c1030-108">值</span><span class="sxs-lookup"><span data-stu-id="c1030-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c1030-109">CN</span><span class="sxs-lookup"><span data-stu-id="c1030-109">CN</span></span>                | <span data-ttu-id="c1030-110">ACS-Allocable-RSVP-頻寬</span><span class="sxs-lookup"><span data-stu-id="c1030-110">ACS-Allocable-RSVP-Bandwidth</span></span>         |
| <span data-ttu-id="c1030-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c1030-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c1030-112">aCSAllocableRSVPBandwidth</span><span class="sxs-lookup"><span data-stu-id="c1030-112">aCSAllocableRSVPBandwidth</span></span>            |
| <span data-ttu-id="c1030-113">大小</span><span class="sxs-lookup"><span data-stu-id="c1030-113">Size</span></span>              | <span data-ttu-id="c1030-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="c1030-114">8 bytes</span></span>                              |
| <span data-ttu-id="c1030-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c1030-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c1030-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c1030-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c1030-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c1030-117">Attribute-Id</span></span>      | <span data-ttu-id="c1030-118">1.2.840.113556.1.4.766</span><span class="sxs-lookup"><span data-stu-id="c1030-118">1.2.840.113556.1.4.766</span></span>               |
| <span data-ttu-id="c1030-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c1030-119">System-Id-Guid</span></span>    | <span data-ttu-id="c1030-120">7f561283-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c1030-120">7f561283-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="c1030-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1030-121">Syntax</span></span>            | [<span data-ttu-id="c1030-122">**間隔**</span><span class="sxs-lookup"><span data-stu-id="c1030-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c1030-123">實作</span><span class="sxs-lookup"><span data-stu-id="c1030-123">Implementations</span></span>

-   [<span data-ttu-id="c1030-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c1030-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c1030-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c1030-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c1030-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c1030-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c1030-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c1030-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c1030-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c1030-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c1030-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c1030-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c1030-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1030-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c1030-131">進入</span><span class="sxs-lookup"><span data-stu-id="c1030-131">Entry</span></span> | <span data-ttu-id="c1030-132">值</span><span class="sxs-lookup"><span data-stu-id="c1030-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1030-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1030-133">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1030-134">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1030-135">System-Only</span></span>            | <span data-ttu-id="c1030-136">否</span><span class="sxs-lookup"><span data-stu-id="c1030-136">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1030-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c1030-138">對</span><span class="sxs-lookup"><span data-stu-id="c1030-138">True</span></span>                                                                                                       |
| <span data-ttu-id="c1030-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1030-139">Is Indexed</span></span>             | <span data-ttu-id="c1030-140">否</span><span class="sxs-lookup"><span data-stu-id="c1030-140">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1030-141">In Global Catalog</span></span>      | <span data-ttu-id="c1030-142">否</span><span class="sxs-lookup"><span data-stu-id="c1030-142">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1030-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1030-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1030-144">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c1030-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1030-145">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1030-146">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-147">Search-Flags</span></span>           | <span data-ttu-id="c1030-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1030-148">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c1030-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-149">System-Flags</span></span>           | <span data-ttu-id="c1030-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1030-150">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c1030-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1030-151">Classes used in</span></span>        | [<span data-ttu-id="c1030-152">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="c1030-152">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="c1030-153">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c1030-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c1030-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1030-154">Windows Server 2003</span></span>



| <span data-ttu-id="c1030-155">進入</span><span class="sxs-lookup"><span data-stu-id="c1030-155">Entry</span></span> | <span data-ttu-id="c1030-156">值</span><span class="sxs-lookup"><span data-stu-id="c1030-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1030-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1030-157">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1030-158">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1030-159">System-Only</span></span>            | <span data-ttu-id="c1030-160">否</span><span class="sxs-lookup"><span data-stu-id="c1030-160">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1030-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c1030-162">對</span><span class="sxs-lookup"><span data-stu-id="c1030-162">True</span></span>                                                                                                       |
| <span data-ttu-id="c1030-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1030-163">Is Indexed</span></span>             | <span data-ttu-id="c1030-164">否</span><span class="sxs-lookup"><span data-stu-id="c1030-164">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1030-165">In Global Catalog</span></span>      | <span data-ttu-id="c1030-166">否</span><span class="sxs-lookup"><span data-stu-id="c1030-166">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1030-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1030-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1030-168">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c1030-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1030-169">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1030-170">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-171">Search-Flags</span></span>           | <span data-ttu-id="c1030-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1030-172">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c1030-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-173">System-Flags</span></span>           | <span data-ttu-id="c1030-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1030-174">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c1030-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1030-175">Classes used in</span></span>        | [<span data-ttu-id="c1030-176">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="c1030-176">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="c1030-177">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c1030-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c1030-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c1030-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c1030-179">進入</span><span class="sxs-lookup"><span data-stu-id="c1030-179">Entry</span></span> | <span data-ttu-id="c1030-180">值</span><span class="sxs-lookup"><span data-stu-id="c1030-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1030-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1030-181">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1030-182">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1030-183">System-Only</span></span>            | <span data-ttu-id="c1030-184">否</span><span class="sxs-lookup"><span data-stu-id="c1030-184">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1030-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c1030-186">對</span><span class="sxs-lookup"><span data-stu-id="c1030-186">True</span></span>                                                                                                       |
| <span data-ttu-id="c1030-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1030-187">Is Indexed</span></span>             | <span data-ttu-id="c1030-188">否</span><span class="sxs-lookup"><span data-stu-id="c1030-188">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1030-189">In Global Catalog</span></span>      | <span data-ttu-id="c1030-190">否</span><span class="sxs-lookup"><span data-stu-id="c1030-190">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1030-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1030-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1030-192">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c1030-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1030-193">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1030-194">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-195">Search-Flags</span></span>           | <span data-ttu-id="c1030-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1030-196">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c1030-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-197">System-Flags</span></span>           | <span data-ttu-id="c1030-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1030-198">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c1030-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1030-199">Classes used in</span></span>        | [<span data-ttu-id="c1030-200">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="c1030-200">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="c1030-201">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c1030-201">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c1030-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1030-202">Windows Server 2008</span></span>



| <span data-ttu-id="c1030-203">進入</span><span class="sxs-lookup"><span data-stu-id="c1030-203">Entry</span></span> | <span data-ttu-id="c1030-204">值</span><span class="sxs-lookup"><span data-stu-id="c1030-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1030-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1030-205">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1030-206">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1030-207">System-Only</span></span>            | <span data-ttu-id="c1030-208">否</span><span class="sxs-lookup"><span data-stu-id="c1030-208">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1030-209">Is-Single-Valued</span></span>       | <span data-ttu-id="c1030-210">對</span><span class="sxs-lookup"><span data-stu-id="c1030-210">True</span></span>                                                                                                       |
| <span data-ttu-id="c1030-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1030-211">Is Indexed</span></span>             | <span data-ttu-id="c1030-212">否</span><span class="sxs-lookup"><span data-stu-id="c1030-212">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1030-213">In Global Catalog</span></span>      | <span data-ttu-id="c1030-214">否</span><span class="sxs-lookup"><span data-stu-id="c1030-214">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1030-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1030-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1030-216">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c1030-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1030-217">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1030-218">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-219">Search-Flags</span></span>           | <span data-ttu-id="c1030-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1030-220">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c1030-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-221">System-Flags</span></span>           | <span data-ttu-id="c1030-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1030-222">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c1030-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1030-223">Classes used in</span></span>        | [<span data-ttu-id="c1030-224">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="c1030-224">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="c1030-225">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c1030-225">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c1030-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1030-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c1030-227">進入</span><span class="sxs-lookup"><span data-stu-id="c1030-227">Entry</span></span> | <span data-ttu-id="c1030-228">值</span><span class="sxs-lookup"><span data-stu-id="c1030-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1030-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1030-229">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1030-230">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1030-231">System-Only</span></span>            | <span data-ttu-id="c1030-232">否</span><span class="sxs-lookup"><span data-stu-id="c1030-232">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1030-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c1030-234">對</span><span class="sxs-lookup"><span data-stu-id="c1030-234">True</span></span>                                                                                                       |
| <span data-ttu-id="c1030-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1030-235">Is Indexed</span></span>             | <span data-ttu-id="c1030-236">否</span><span class="sxs-lookup"><span data-stu-id="c1030-236">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1030-237">In Global Catalog</span></span>      | <span data-ttu-id="c1030-238">否</span><span class="sxs-lookup"><span data-stu-id="c1030-238">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1030-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1030-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1030-240">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c1030-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1030-241">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1030-242">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-243">Search-Flags</span></span>           | <span data-ttu-id="c1030-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1030-244">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c1030-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-245">System-Flags</span></span>           | <span data-ttu-id="c1030-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1030-246">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c1030-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1030-247">Classes used in</span></span>        | [<span data-ttu-id="c1030-248">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="c1030-248">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="c1030-249">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c1030-249">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c1030-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1030-250">Windows Server 2012</span></span>



| <span data-ttu-id="c1030-251">進入</span><span class="sxs-lookup"><span data-stu-id="c1030-251">Entry</span></span> | <span data-ttu-id="c1030-252">值</span><span class="sxs-lookup"><span data-stu-id="c1030-252">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1030-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1030-253">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1030-254">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="c1030-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1030-255">System-Only</span></span>            | <span data-ttu-id="c1030-256">否</span><span class="sxs-lookup"><span data-stu-id="c1030-256">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1030-257">Is-Single-Valued</span></span>       | <span data-ttu-id="c1030-258">對</span><span class="sxs-lookup"><span data-stu-id="c1030-258">True</span></span>                                                                                                       |
| <span data-ttu-id="c1030-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1030-259">Is Indexed</span></span>             | <span data-ttu-id="c1030-260">否</span><span class="sxs-lookup"><span data-stu-id="c1030-260">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1030-261">In Global Catalog</span></span>      | <span data-ttu-id="c1030-262">否</span><span class="sxs-lookup"><span data-stu-id="c1030-262">False</span></span>                                                                                                      |
| <span data-ttu-id="c1030-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1030-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1030-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1030-264">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="c1030-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1030-265">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1030-266">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="c1030-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-267">Search-Flags</span></span>           | <span data-ttu-id="c1030-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1030-268">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="c1030-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1030-269">System-Flags</span></span>           | <span data-ttu-id="c1030-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1030-270">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="c1030-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1030-271">Classes used in</span></span>        | [<span data-ttu-id="c1030-272">**ACS-資源-限制**</span><span class="sxs-lookup"><span data-stu-id="c1030-272">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="c1030-273">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="c1030-273">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






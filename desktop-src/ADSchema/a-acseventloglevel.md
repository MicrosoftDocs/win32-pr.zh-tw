---
title: ACS-事件-記錄層級屬性
description: RSVP 記錄層級。
ms.assetid: 2f3c645d-a064-40fb-965c-388b2fac61bc
ms.tgt_platform: multiple
keywords:
- ACS-事件-記錄層級屬性 AD 架構
- aCSEventLogLevel 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Event-Log-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bb5701f665a3685845368eb2adc72fc33d10bd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686891"
---
# <a name="acs-event-log-level-attribute"></a><span data-ttu-id="6f9e5-105">ACS-事件-記錄層級屬性</span><span class="sxs-lookup"><span data-stu-id="6f9e5-105">ACS-Event-Log-Level attribute</span></span>

<span data-ttu-id="6f9e5-106">RSVP 記錄層級。</span><span class="sxs-lookup"><span data-stu-id="6f9e5-106">RSVP logging level.</span></span>



| <span data-ttu-id="6f9e5-107">進入</span><span class="sxs-lookup"><span data-stu-id="6f9e5-107">Entry</span></span> | <span data-ttu-id="6f9e5-108">值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="6f9e5-109">CN</span><span class="sxs-lookup"><span data-stu-id="6f9e5-109">CN</span></span>                | <span data-ttu-id="6f9e5-110">ACS-事件-記錄層級</span><span class="sxs-lookup"><span data-stu-id="6f9e5-110">ACS-Event-Log-Level</span></span>                     |
| <span data-ttu-id="6f9e5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6f9e5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6f9e5-112">aCSEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="6f9e5-112">aCSEventLogLevel</span></span>                        |
| <span data-ttu-id="6f9e5-113">大小</span><span class="sxs-lookup"><span data-stu-id="6f9e5-113">Size</span></span>              | <span data-ttu-id="6f9e5-114">4個位元組的值可以是0、1、2和3。</span><span class="sxs-lookup"><span data-stu-id="6f9e5-114">4 bytes can have values 0, 1, 2, and 3.</span></span> |
| <span data-ttu-id="6f9e5-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6f9e5-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="6f9e5-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6f9e5-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="6f9e5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6f9e5-117">Attribute-Id</span></span>      | <span data-ttu-id="6f9e5-118">1.2.840.113556.1.4.769</span><span class="sxs-lookup"><span data-stu-id="6f9e5-118">1.2.840.113556.1.4.769</span></span>                  |
| <span data-ttu-id="6f9e5-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6f9e5-119">System-Id-Guid</span></span>    | <span data-ttu-id="6f9e5-120">7f561286-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6f9e5-120">7f561286-5301-11d1-a9c5-0000f80367c1</span></span>    |
| <span data-ttu-id="6f9e5-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f9e5-121">Syntax</span></span>            | [<span data-ttu-id="6f9e5-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-122">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="6f9e5-123">實作</span><span class="sxs-lookup"><span data-stu-id="6f9e5-123">Implementations</span></span>

-   [<span data-ttu-id="6f9e5-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6f9e5-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6f9e5-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6f9e5-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6f9e5-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6f9e5-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6f9e5-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f9e5-130">Windows 2000 Server</span></span>



| <span data-ttu-id="6f9e5-131">進入</span><span class="sxs-lookup"><span data-stu-id="6f9e5-131">Entry</span></span> | <span data-ttu-id="6f9e5-132">值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6f9e5-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f9e5-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f9e5-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f9e5-135">System-Only</span></span>            | <span data-ttu-id="6f9e5-136">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-136">False</span></span>                                        |
| <span data-ttu-id="6f9e5-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6f9e5-138">對</span><span class="sxs-lookup"><span data-stu-id="6f9e5-138">True</span></span>                                         |
| <span data-ttu-id="6f9e5-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f9e5-139">Is Indexed</span></span>             | <span data-ttu-id="6f9e5-140">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-140">False</span></span>                                        |
| <span data-ttu-id="6f9e5-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f9e5-141">In Global Catalog</span></span>      | <span data-ttu-id="6f9e5-142">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-142">False</span></span>                                        |
| <span data-ttu-id="6f9e5-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f9e5-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f9e5-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f9e5-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6f9e5-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f9e5-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f9e5-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-147">Search-Flags</span></span>           | <span data-ttu-id="6f9e5-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f9e5-148">0x00000000</span></span>                                   |
| <span data-ttu-id="6f9e5-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-149">System-Flags</span></span>           | <span data-ttu-id="6f9e5-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f9e5-150">0x00000010</span></span>                                   |
| <span data-ttu-id="6f9e5-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f9e5-151">Classes used in</span></span>        | [<span data-ttu-id="6f9e5-152">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6f9e5-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f9e5-153">Windows Server 2003</span></span>



| <span data-ttu-id="6f9e5-154">進入</span><span class="sxs-lookup"><span data-stu-id="6f9e5-154">Entry</span></span> | <span data-ttu-id="6f9e5-155">值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6f9e5-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f9e5-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f9e5-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f9e5-158">System-Only</span></span>            | <span data-ttu-id="6f9e5-159">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-159">False</span></span>                                        |
| <span data-ttu-id="6f9e5-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-160">Is-Single-Valued</span></span>       | <span data-ttu-id="6f9e5-161">對</span><span class="sxs-lookup"><span data-stu-id="6f9e5-161">True</span></span>                                         |
| <span data-ttu-id="6f9e5-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f9e5-162">Is Indexed</span></span>             | <span data-ttu-id="6f9e5-163">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-163">False</span></span>                                        |
| <span data-ttu-id="6f9e5-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f9e5-164">In Global Catalog</span></span>      | <span data-ttu-id="6f9e5-165">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-165">False</span></span>                                        |
| <span data-ttu-id="6f9e5-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f9e5-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f9e5-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f9e5-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6f9e5-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f9e5-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f9e5-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-170">Search-Flags</span></span>           | <span data-ttu-id="6f9e5-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f9e5-171">0x00000000</span></span>                                   |
| <span data-ttu-id="6f9e5-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-172">System-Flags</span></span>           | <span data-ttu-id="6f9e5-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f9e5-173">0x00000010</span></span>                                   |
| <span data-ttu-id="6f9e5-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f9e5-174">Classes used in</span></span>        | [<span data-ttu-id="6f9e5-175">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6f9e5-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f9e5-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6f9e5-177">進入</span><span class="sxs-lookup"><span data-stu-id="6f9e5-177">Entry</span></span> | <span data-ttu-id="6f9e5-178">值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6f9e5-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f9e5-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f9e5-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f9e5-181">System-Only</span></span>            | <span data-ttu-id="6f9e5-182">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-182">False</span></span>                                        |
| <span data-ttu-id="6f9e5-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-183">Is-Single-Valued</span></span>       | <span data-ttu-id="6f9e5-184">對</span><span class="sxs-lookup"><span data-stu-id="6f9e5-184">True</span></span>                                         |
| <span data-ttu-id="6f9e5-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f9e5-185">Is Indexed</span></span>             | <span data-ttu-id="6f9e5-186">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-186">False</span></span>                                        |
| <span data-ttu-id="6f9e5-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f9e5-187">In Global Catalog</span></span>      | <span data-ttu-id="6f9e5-188">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-188">False</span></span>                                        |
| <span data-ttu-id="6f9e5-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f9e5-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f9e5-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f9e5-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6f9e5-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f9e5-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f9e5-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-193">Search-Flags</span></span>           | <span data-ttu-id="6f9e5-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f9e5-194">0x00000000</span></span>                                   |
| <span data-ttu-id="6f9e5-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-195">System-Flags</span></span>           | <span data-ttu-id="6f9e5-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f9e5-196">0x00000010</span></span>                                   |
| <span data-ttu-id="6f9e5-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f9e5-197">Classes used in</span></span>        | [<span data-ttu-id="6f9e5-198">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6f9e5-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f9e5-199">Windows Server 2008</span></span>



| <span data-ttu-id="6f9e5-200">進入</span><span class="sxs-lookup"><span data-stu-id="6f9e5-200">Entry</span></span> | <span data-ttu-id="6f9e5-201">值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6f9e5-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f9e5-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f9e5-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f9e5-204">System-Only</span></span>            | <span data-ttu-id="6f9e5-205">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-205">False</span></span>                                        |
| <span data-ttu-id="6f9e5-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-206">Is-Single-Valued</span></span>       | <span data-ttu-id="6f9e5-207">對</span><span class="sxs-lookup"><span data-stu-id="6f9e5-207">True</span></span>                                         |
| <span data-ttu-id="6f9e5-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f9e5-208">Is Indexed</span></span>             | <span data-ttu-id="6f9e5-209">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-209">False</span></span>                                        |
| <span data-ttu-id="6f9e5-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f9e5-210">In Global Catalog</span></span>      | <span data-ttu-id="6f9e5-211">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-211">False</span></span>                                        |
| <span data-ttu-id="6f9e5-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f9e5-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f9e5-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f9e5-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6f9e5-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f9e5-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f9e5-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-216">Search-Flags</span></span>           | <span data-ttu-id="6f9e5-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f9e5-217">0x00000000</span></span>                                   |
| <span data-ttu-id="6f9e5-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-218">System-Flags</span></span>           | <span data-ttu-id="6f9e5-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f9e5-219">0x00000010</span></span>                                   |
| <span data-ttu-id="6f9e5-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f9e5-220">Classes used in</span></span>        | [<span data-ttu-id="6f9e5-221">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6f9e5-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f9e5-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6f9e5-223">進入</span><span class="sxs-lookup"><span data-stu-id="6f9e5-223">Entry</span></span> | <span data-ttu-id="6f9e5-224">值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6f9e5-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f9e5-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f9e5-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f9e5-227">System-Only</span></span>            | <span data-ttu-id="6f9e5-228">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-228">False</span></span>                                        |
| <span data-ttu-id="6f9e5-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-229">Is-Single-Valued</span></span>       | <span data-ttu-id="6f9e5-230">對</span><span class="sxs-lookup"><span data-stu-id="6f9e5-230">True</span></span>                                         |
| <span data-ttu-id="6f9e5-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f9e5-231">Is Indexed</span></span>             | <span data-ttu-id="6f9e5-232">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-232">False</span></span>                                        |
| <span data-ttu-id="6f9e5-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f9e5-233">In Global Catalog</span></span>      | <span data-ttu-id="6f9e5-234">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-234">False</span></span>                                        |
| <span data-ttu-id="6f9e5-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f9e5-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f9e5-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f9e5-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6f9e5-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f9e5-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f9e5-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-239">Search-Flags</span></span>           | <span data-ttu-id="6f9e5-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f9e5-240">0x00000000</span></span>                                   |
| <span data-ttu-id="6f9e5-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-241">System-Flags</span></span>           | <span data-ttu-id="6f9e5-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f9e5-242">0x00000010</span></span>                                   |
| <span data-ttu-id="6f9e5-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f9e5-243">Classes used in</span></span>        | [<span data-ttu-id="6f9e5-244">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6f9e5-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f9e5-245">Windows Server 2012</span></span>



| <span data-ttu-id="6f9e5-246">進入</span><span class="sxs-lookup"><span data-stu-id="6f9e5-246">Entry</span></span> | <span data-ttu-id="6f9e5-247">值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6f9e5-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6f9e5-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f9e5-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6f9e5-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f9e5-250">System-Only</span></span>            | <span data-ttu-id="6f9e5-251">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-251">False</span></span>                                        |
| <span data-ttu-id="6f9e5-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6f9e5-252">Is-Single-Valued</span></span>       | <span data-ttu-id="6f9e5-253">對</span><span class="sxs-lookup"><span data-stu-id="6f9e5-253">True</span></span>                                         |
| <span data-ttu-id="6f9e5-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6f9e5-254">Is Indexed</span></span>             | <span data-ttu-id="6f9e5-255">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-255">False</span></span>                                        |
| <span data-ttu-id="6f9e5-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6f9e5-256">In Global Catalog</span></span>      | <span data-ttu-id="6f9e5-257">否</span><span class="sxs-lookup"><span data-stu-id="6f9e5-257">False</span></span>                                        |
| <span data-ttu-id="6f9e5-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6f9e5-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f9e5-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6f9e5-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6f9e5-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f9e5-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f9e5-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6f9e5-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-262">Search-Flags</span></span>           | <span data-ttu-id="6f9e5-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f9e5-263">0x00000000</span></span>                                   |
| <span data-ttu-id="6f9e5-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f9e5-264">System-Flags</span></span>           | <span data-ttu-id="6f9e5-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f9e5-265">0x00000010</span></span>                                   |
| <span data-ttu-id="6f9e5-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6f9e5-266">Classes used in</span></span>        | [<span data-ttu-id="6f9e5-267">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="6f9e5-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






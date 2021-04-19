---
title: ACS-當日時間屬性
description: 套用此原則的當日時間。
ms.assetid: aacd604a-45cb-4815-bc6b-332cf090f4a2
ms.tgt_platform: multiple
keywords:
- ACS-當日時間屬性 AD 架構
- aCSTimeOfDay 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Time-Of-Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212719ffa9e1aa37439def10a0991b256dd61fcb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970272"
---
# <a name="acs-time-of-day-attribute"></a><span data-ttu-id="afa22-105">ACS-當日時間屬性</span><span class="sxs-lookup"><span data-stu-id="afa22-105">ACS-Time-Of-Day attribute</span></span>

<span data-ttu-id="afa22-106">套用此原則的當日時間。</span><span class="sxs-lookup"><span data-stu-id="afa22-106">Times of day at which this policy applies.</span></span>



| <span data-ttu-id="afa22-107">進入</span><span class="sxs-lookup"><span data-stu-id="afa22-107">Entry</span></span> | <span data-ttu-id="afa22-108">值</span><span class="sxs-lookup"><span data-stu-id="afa22-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="afa22-109">CN</span><span class="sxs-lookup"><span data-stu-id="afa22-109">CN</span></span>                | <span data-ttu-id="afa22-110">ACS-當日時間</span><span class="sxs-lookup"><span data-stu-id="afa22-110">ACS-Time-Of-Day</span></span>                             |
| <span data-ttu-id="afa22-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="afa22-111">Ldap-Display-Name</span></span> | <span data-ttu-id="afa22-112">aCSTimeOfDay</span><span class="sxs-lookup"><span data-stu-id="afa22-112">aCSTimeOfDay</span></span>                                |
| <span data-ttu-id="afa22-113">大小</span><span class="sxs-lookup"><span data-stu-id="afa22-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="afa22-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="afa22-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="afa22-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="afa22-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="afa22-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="afa22-116">Attribute-Id</span></span>      | <span data-ttu-id="afa22-117">1.2.840.113556.1.4.756</span><span class="sxs-lookup"><span data-stu-id="afa22-117">1.2.840.113556.1.4.756</span></span>                      |
| <span data-ttu-id="afa22-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="afa22-118">System-Id-Guid</span></span>    | <span data-ttu-id="afa22-119">7f561279-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="afa22-119">7f561279-5301-11d1-a9c5-0000f80367c1</span></span>        |
| <span data-ttu-id="afa22-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="afa22-120">Syntax</span></span>            | [<span data-ttu-id="afa22-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="afa22-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="afa22-122">實作</span><span class="sxs-lookup"><span data-stu-id="afa22-122">Implementations</span></span>

-   [<span data-ttu-id="afa22-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="afa22-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="afa22-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="afa22-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="afa22-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="afa22-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="afa22-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="afa22-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="afa22-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="afa22-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="afa22-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="afa22-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="afa22-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="afa22-129">Windows 2000 Server</span></span>



| <span data-ttu-id="afa22-130">進入</span><span class="sxs-lookup"><span data-stu-id="afa22-130">Entry</span></span> | <span data-ttu-id="afa22-131">值</span><span class="sxs-lookup"><span data-stu-id="afa22-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="afa22-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="afa22-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afa22-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="afa22-134">System-Only</span></span>            | <span data-ttu-id="afa22-135">否</span><span class="sxs-lookup"><span data-stu-id="afa22-135">False</span></span>                                        |
| <span data-ttu-id="afa22-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="afa22-136">Is-Single-Valued</span></span>       | <span data-ttu-id="afa22-137">對</span><span class="sxs-lookup"><span data-stu-id="afa22-137">True</span></span>                                         |
| <span data-ttu-id="afa22-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="afa22-138">Is Indexed</span></span>             | <span data-ttu-id="afa22-139">否</span><span class="sxs-lookup"><span data-stu-id="afa22-139">False</span></span>                                        |
| <span data-ttu-id="afa22-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="afa22-140">In Global Catalog</span></span>      | <span data-ttu-id="afa22-141">否</span><span class="sxs-lookup"><span data-stu-id="afa22-141">False</span></span>                                        |
| <span data-ttu-id="afa22-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="afa22-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="afa22-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="afa22-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="afa22-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afa22-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="afa22-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afa22-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="afa22-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-146">Search-Flags</span></span>           | <span data-ttu-id="afa22-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afa22-147">0x00000000</span></span>                                   |
| <span data-ttu-id="afa22-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-148">System-Flags</span></span>           | <span data-ttu-id="afa22-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afa22-149">0x00000010</span></span>                                   |
| <span data-ttu-id="afa22-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="afa22-150">Classes used in</span></span>        | [<span data-ttu-id="afa22-151">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="afa22-151">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="afa22-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afa22-152">Windows Server 2003</span></span>



| <span data-ttu-id="afa22-153">進入</span><span class="sxs-lookup"><span data-stu-id="afa22-153">Entry</span></span> | <span data-ttu-id="afa22-154">值</span><span class="sxs-lookup"><span data-stu-id="afa22-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="afa22-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="afa22-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afa22-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="afa22-157">System-Only</span></span>            | <span data-ttu-id="afa22-158">否</span><span class="sxs-lookup"><span data-stu-id="afa22-158">False</span></span>                                        |
| <span data-ttu-id="afa22-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="afa22-159">Is-Single-Valued</span></span>       | <span data-ttu-id="afa22-160">對</span><span class="sxs-lookup"><span data-stu-id="afa22-160">True</span></span>                                         |
| <span data-ttu-id="afa22-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="afa22-161">Is Indexed</span></span>             | <span data-ttu-id="afa22-162">否</span><span class="sxs-lookup"><span data-stu-id="afa22-162">False</span></span>                                        |
| <span data-ttu-id="afa22-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="afa22-163">In Global Catalog</span></span>      | <span data-ttu-id="afa22-164">否</span><span class="sxs-lookup"><span data-stu-id="afa22-164">False</span></span>                                        |
| <span data-ttu-id="afa22-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="afa22-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="afa22-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="afa22-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="afa22-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afa22-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="afa22-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afa22-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="afa22-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-169">Search-Flags</span></span>           | <span data-ttu-id="afa22-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afa22-170">0x00000000</span></span>                                   |
| <span data-ttu-id="afa22-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-171">System-Flags</span></span>           | <span data-ttu-id="afa22-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afa22-172">0x00000010</span></span>                                   |
| <span data-ttu-id="afa22-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="afa22-173">Classes used in</span></span>        | [<span data-ttu-id="afa22-174">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="afa22-174">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="afa22-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="afa22-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="afa22-176">進入</span><span class="sxs-lookup"><span data-stu-id="afa22-176">Entry</span></span> | <span data-ttu-id="afa22-177">值</span><span class="sxs-lookup"><span data-stu-id="afa22-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="afa22-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="afa22-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afa22-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="afa22-180">System-Only</span></span>            | <span data-ttu-id="afa22-181">否</span><span class="sxs-lookup"><span data-stu-id="afa22-181">False</span></span>                                        |
| <span data-ttu-id="afa22-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="afa22-182">Is-Single-Valued</span></span>       | <span data-ttu-id="afa22-183">對</span><span class="sxs-lookup"><span data-stu-id="afa22-183">True</span></span>                                         |
| <span data-ttu-id="afa22-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="afa22-184">Is Indexed</span></span>             | <span data-ttu-id="afa22-185">否</span><span class="sxs-lookup"><span data-stu-id="afa22-185">False</span></span>                                        |
| <span data-ttu-id="afa22-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="afa22-186">In Global Catalog</span></span>      | <span data-ttu-id="afa22-187">否</span><span class="sxs-lookup"><span data-stu-id="afa22-187">False</span></span>                                        |
| <span data-ttu-id="afa22-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="afa22-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="afa22-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="afa22-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="afa22-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afa22-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="afa22-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afa22-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="afa22-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-192">Search-Flags</span></span>           | <span data-ttu-id="afa22-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afa22-193">0x00000000</span></span>                                   |
| <span data-ttu-id="afa22-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-194">System-Flags</span></span>           | <span data-ttu-id="afa22-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afa22-195">0x00000010</span></span>                                   |
| <span data-ttu-id="afa22-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="afa22-196">Classes used in</span></span>        | [<span data-ttu-id="afa22-197">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="afa22-197">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="afa22-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afa22-198">Windows Server 2008</span></span>



| <span data-ttu-id="afa22-199">進入</span><span class="sxs-lookup"><span data-stu-id="afa22-199">Entry</span></span> | <span data-ttu-id="afa22-200">值</span><span class="sxs-lookup"><span data-stu-id="afa22-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="afa22-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="afa22-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afa22-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="afa22-203">System-Only</span></span>            | <span data-ttu-id="afa22-204">否</span><span class="sxs-lookup"><span data-stu-id="afa22-204">False</span></span>                                        |
| <span data-ttu-id="afa22-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="afa22-205">Is-Single-Valued</span></span>       | <span data-ttu-id="afa22-206">對</span><span class="sxs-lookup"><span data-stu-id="afa22-206">True</span></span>                                         |
| <span data-ttu-id="afa22-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="afa22-207">Is Indexed</span></span>             | <span data-ttu-id="afa22-208">否</span><span class="sxs-lookup"><span data-stu-id="afa22-208">False</span></span>                                        |
| <span data-ttu-id="afa22-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="afa22-209">In Global Catalog</span></span>      | <span data-ttu-id="afa22-210">否</span><span class="sxs-lookup"><span data-stu-id="afa22-210">False</span></span>                                        |
| <span data-ttu-id="afa22-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="afa22-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="afa22-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="afa22-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="afa22-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afa22-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="afa22-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afa22-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="afa22-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-215">Search-Flags</span></span>           | <span data-ttu-id="afa22-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afa22-216">0x00000000</span></span>                                   |
| <span data-ttu-id="afa22-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-217">System-Flags</span></span>           | <span data-ttu-id="afa22-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afa22-218">0x00000010</span></span>                                   |
| <span data-ttu-id="afa22-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="afa22-219">Classes used in</span></span>        | [<span data-ttu-id="afa22-220">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="afa22-220">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="afa22-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afa22-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="afa22-222">進入</span><span class="sxs-lookup"><span data-stu-id="afa22-222">Entry</span></span> | <span data-ttu-id="afa22-223">值</span><span class="sxs-lookup"><span data-stu-id="afa22-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="afa22-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="afa22-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afa22-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="afa22-226">System-Only</span></span>            | <span data-ttu-id="afa22-227">否</span><span class="sxs-lookup"><span data-stu-id="afa22-227">False</span></span>                                        |
| <span data-ttu-id="afa22-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="afa22-228">Is-Single-Valued</span></span>       | <span data-ttu-id="afa22-229">對</span><span class="sxs-lookup"><span data-stu-id="afa22-229">True</span></span>                                         |
| <span data-ttu-id="afa22-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="afa22-230">Is Indexed</span></span>             | <span data-ttu-id="afa22-231">否</span><span class="sxs-lookup"><span data-stu-id="afa22-231">False</span></span>                                        |
| <span data-ttu-id="afa22-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="afa22-232">In Global Catalog</span></span>      | <span data-ttu-id="afa22-233">否</span><span class="sxs-lookup"><span data-stu-id="afa22-233">False</span></span>                                        |
| <span data-ttu-id="afa22-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="afa22-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="afa22-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="afa22-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="afa22-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afa22-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="afa22-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afa22-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="afa22-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-238">Search-Flags</span></span>           | <span data-ttu-id="afa22-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afa22-239">0x00000000</span></span>                                   |
| <span data-ttu-id="afa22-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-240">System-Flags</span></span>           | <span data-ttu-id="afa22-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afa22-241">0x00000010</span></span>                                   |
| <span data-ttu-id="afa22-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="afa22-242">Classes used in</span></span>        | [<span data-ttu-id="afa22-243">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="afa22-243">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="afa22-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afa22-244">Windows Server 2012</span></span>



| <span data-ttu-id="afa22-245">進入</span><span class="sxs-lookup"><span data-stu-id="afa22-245">Entry</span></span> | <span data-ttu-id="afa22-246">值</span><span class="sxs-lookup"><span data-stu-id="afa22-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="afa22-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="afa22-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afa22-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="afa22-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="afa22-249">System-Only</span></span>            | <span data-ttu-id="afa22-250">否</span><span class="sxs-lookup"><span data-stu-id="afa22-250">False</span></span>                                        |
| <span data-ttu-id="afa22-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="afa22-251">Is-Single-Valued</span></span>       | <span data-ttu-id="afa22-252">對</span><span class="sxs-lookup"><span data-stu-id="afa22-252">True</span></span>                                         |
| <span data-ttu-id="afa22-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="afa22-253">Is Indexed</span></span>             | <span data-ttu-id="afa22-254">否</span><span class="sxs-lookup"><span data-stu-id="afa22-254">False</span></span>                                        |
| <span data-ttu-id="afa22-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="afa22-255">In Global Catalog</span></span>      | <span data-ttu-id="afa22-256">否</span><span class="sxs-lookup"><span data-stu-id="afa22-256">False</span></span>                                        |
| <span data-ttu-id="afa22-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="afa22-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="afa22-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="afa22-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="afa22-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afa22-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="afa22-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afa22-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="afa22-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-261">Search-Flags</span></span>           | <span data-ttu-id="afa22-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afa22-262">0x00000000</span></span>                                   |
| <span data-ttu-id="afa22-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afa22-263">System-Flags</span></span>           | <span data-ttu-id="afa22-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afa22-264">0x00000010</span></span>                                   |
| <span data-ttu-id="afa22-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="afa22-265">Classes used in</span></span>        | [<span data-ttu-id="afa22-266">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="afa22-266">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






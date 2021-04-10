---
title: ACS-DSBM-DeadTime 屬性
description: 此屬性包含網域 (DSBMDeadInterval) 的選舉出貨時間間隔。
ms.assetid: c3a0780c-1786-4631-b870-77146de87f18
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-DeadTime 屬性 AD 架構
- aCSDSBMDeadTime 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-DSBM-DeadTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8b1c980175dc985c3a718d15323be0b8d1b411
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107340"
---
# <a name="acs-dsbm-deadtime-attribute"></a><span data-ttu-id="818b3-105">ACS-DSBM-DeadTime 屬性</span><span class="sxs-lookup"><span data-stu-id="818b3-105">ACS-DSBM-DeadTime attribute</span></span>

<span data-ttu-id="818b3-106">此屬性包含網域 (DSBMDeadInterval) 的選舉出貨時間間隔。</span><span class="sxs-lookup"><span data-stu-id="818b3-106">This attribute contains the election dead time interval (DSBMDeadInterval) for a domain.</span></span> <span data-ttu-id="818b3-107">如果指定的子網路頻寬管理員在此間隔期間未送出「我的 \_ \_ DSBM」通告，則其他子網路頻寬管理員 () SBMs 在網域中選擇新的 DSBM。</span><span class="sxs-lookup"><span data-stu-id="818b3-107">If the Designated Subnet Bandwidth Manager does not send out an I\_AM\_DSBM advertisement during this interval, then the other Subnet Bandwidth Managers (SBMs) in the domain elect a new DSBM.</span></span>



| <span data-ttu-id="818b3-108">進入</span><span class="sxs-lookup"><span data-stu-id="818b3-108">Entry</span></span> | <span data-ttu-id="818b3-109">值</span><span class="sxs-lookup"><span data-stu-id="818b3-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="818b3-110">CN</span><span class="sxs-lookup"><span data-stu-id="818b3-110">CN</span></span>                | <span data-ttu-id="818b3-111">ACS-DSBM-DeadTime</span><span class="sxs-lookup"><span data-stu-id="818b3-111">ACS-DSBM-DeadTime</span></span>                    |
| <span data-ttu-id="818b3-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="818b3-112">Ldap-Display-Name</span></span> | <span data-ttu-id="818b3-113">aCSDSBMDeadTime</span><span class="sxs-lookup"><span data-stu-id="818b3-113">aCSDSBMDeadTime</span></span>                      |
| <span data-ttu-id="818b3-114">大小</span><span class="sxs-lookup"><span data-stu-id="818b3-114">Size</span></span>              | <span data-ttu-id="818b3-115">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="818b3-115">4 bytes</span></span>                              |
| <span data-ttu-id="818b3-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="818b3-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="818b3-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="818b3-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="818b3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="818b3-118">Attribute-Id</span></span>      | <span data-ttu-id="818b3-119">1.2.840.113556.1.4.778</span><span class="sxs-lookup"><span data-stu-id="818b3-119">1.2.840.113556.1.4.778</span></span>               |
| <span data-ttu-id="818b3-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="818b3-120">System-Id-Guid</span></span>    | <span data-ttu-id="818b3-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="818b3-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="818b3-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="818b3-122">Syntax</span></span>            | [<span data-ttu-id="818b3-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="818b3-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="818b3-124">實作</span><span class="sxs-lookup"><span data-stu-id="818b3-124">Implementations</span></span>

-   [<span data-ttu-id="818b3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="818b3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="818b3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="818b3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="818b3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="818b3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="818b3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="818b3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="818b3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="818b3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="818b3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="818b3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="818b3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="818b3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="818b3-132">進入</span><span class="sxs-lookup"><span data-stu-id="818b3-132">Entry</span></span> | <span data-ttu-id="818b3-133">值</span><span class="sxs-lookup"><span data-stu-id="818b3-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="818b3-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="818b3-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="818b3-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="818b3-136">System-Only</span></span>            | <span data-ttu-id="818b3-137">否</span><span class="sxs-lookup"><span data-stu-id="818b3-137">False</span></span>                                        |
| <span data-ttu-id="818b3-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="818b3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="818b3-139">對</span><span class="sxs-lookup"><span data-stu-id="818b3-139">True</span></span>                                         |
| <span data-ttu-id="818b3-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="818b3-140">Is Indexed</span></span>             | <span data-ttu-id="818b3-141">否</span><span class="sxs-lookup"><span data-stu-id="818b3-141">False</span></span>                                        |
| <span data-ttu-id="818b3-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="818b3-142">In Global Catalog</span></span>      | <span data-ttu-id="818b3-143">否</span><span class="sxs-lookup"><span data-stu-id="818b3-143">False</span></span>                                        |
| <span data-ttu-id="818b3-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="818b3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="818b3-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="818b3-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="818b3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="818b3-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="818b3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="818b3-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="818b3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-148">Search-Flags</span></span>           | <span data-ttu-id="818b3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="818b3-149">0x00000000</span></span>                                   |
| <span data-ttu-id="818b3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-150">System-Flags</span></span>           | <span data-ttu-id="818b3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="818b3-151">0x00000010</span></span>                                   |
| <span data-ttu-id="818b3-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="818b3-152">Classes used in</span></span>        | [<span data-ttu-id="818b3-153">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="818b3-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="818b3-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="818b3-154">Windows Server 2003</span></span>



| <span data-ttu-id="818b3-155">進入</span><span class="sxs-lookup"><span data-stu-id="818b3-155">Entry</span></span> | <span data-ttu-id="818b3-156">值</span><span class="sxs-lookup"><span data-stu-id="818b3-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="818b3-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="818b3-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="818b3-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="818b3-159">System-Only</span></span>            | <span data-ttu-id="818b3-160">否</span><span class="sxs-lookup"><span data-stu-id="818b3-160">False</span></span>                                        |
| <span data-ttu-id="818b3-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="818b3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="818b3-162">對</span><span class="sxs-lookup"><span data-stu-id="818b3-162">True</span></span>                                         |
| <span data-ttu-id="818b3-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="818b3-163">Is Indexed</span></span>             | <span data-ttu-id="818b3-164">否</span><span class="sxs-lookup"><span data-stu-id="818b3-164">False</span></span>                                        |
| <span data-ttu-id="818b3-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="818b3-165">In Global Catalog</span></span>      | <span data-ttu-id="818b3-166">否</span><span class="sxs-lookup"><span data-stu-id="818b3-166">False</span></span>                                        |
| <span data-ttu-id="818b3-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="818b3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="818b3-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="818b3-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="818b3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="818b3-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="818b3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="818b3-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="818b3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-171">Search-Flags</span></span>           | <span data-ttu-id="818b3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="818b3-172">0x00000000</span></span>                                   |
| <span data-ttu-id="818b3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-173">System-Flags</span></span>           | <span data-ttu-id="818b3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="818b3-174">0x00000010</span></span>                                   |
| <span data-ttu-id="818b3-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="818b3-175">Classes used in</span></span>        | [<span data-ttu-id="818b3-176">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="818b3-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="818b3-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="818b3-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="818b3-178">進入</span><span class="sxs-lookup"><span data-stu-id="818b3-178">Entry</span></span> | <span data-ttu-id="818b3-179">值</span><span class="sxs-lookup"><span data-stu-id="818b3-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="818b3-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="818b3-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="818b3-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="818b3-182">System-Only</span></span>            | <span data-ttu-id="818b3-183">否</span><span class="sxs-lookup"><span data-stu-id="818b3-183">False</span></span>                                        |
| <span data-ttu-id="818b3-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="818b3-184">Is-Single-Valued</span></span>       | <span data-ttu-id="818b3-185">對</span><span class="sxs-lookup"><span data-stu-id="818b3-185">True</span></span>                                         |
| <span data-ttu-id="818b3-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="818b3-186">Is Indexed</span></span>             | <span data-ttu-id="818b3-187">否</span><span class="sxs-lookup"><span data-stu-id="818b3-187">False</span></span>                                        |
| <span data-ttu-id="818b3-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="818b3-188">In Global Catalog</span></span>      | <span data-ttu-id="818b3-189">否</span><span class="sxs-lookup"><span data-stu-id="818b3-189">False</span></span>                                        |
| <span data-ttu-id="818b3-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="818b3-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="818b3-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="818b3-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="818b3-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="818b3-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="818b3-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="818b3-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="818b3-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-194">Search-Flags</span></span>           | <span data-ttu-id="818b3-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="818b3-195">0x00000000</span></span>                                   |
| <span data-ttu-id="818b3-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-196">System-Flags</span></span>           | <span data-ttu-id="818b3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="818b3-197">0x00000010</span></span>                                   |
| <span data-ttu-id="818b3-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="818b3-198">Classes used in</span></span>        | [<span data-ttu-id="818b3-199">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="818b3-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="818b3-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="818b3-200">Windows Server 2008</span></span>



| <span data-ttu-id="818b3-201">進入</span><span class="sxs-lookup"><span data-stu-id="818b3-201">Entry</span></span> | <span data-ttu-id="818b3-202">值</span><span class="sxs-lookup"><span data-stu-id="818b3-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="818b3-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="818b3-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="818b3-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="818b3-205">System-Only</span></span>            | <span data-ttu-id="818b3-206">否</span><span class="sxs-lookup"><span data-stu-id="818b3-206">False</span></span>                                        |
| <span data-ttu-id="818b3-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="818b3-207">Is-Single-Valued</span></span>       | <span data-ttu-id="818b3-208">對</span><span class="sxs-lookup"><span data-stu-id="818b3-208">True</span></span>                                         |
| <span data-ttu-id="818b3-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="818b3-209">Is Indexed</span></span>             | <span data-ttu-id="818b3-210">否</span><span class="sxs-lookup"><span data-stu-id="818b3-210">False</span></span>                                        |
| <span data-ttu-id="818b3-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="818b3-211">In Global Catalog</span></span>      | <span data-ttu-id="818b3-212">否</span><span class="sxs-lookup"><span data-stu-id="818b3-212">False</span></span>                                        |
| <span data-ttu-id="818b3-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="818b3-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="818b3-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="818b3-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="818b3-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="818b3-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="818b3-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="818b3-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="818b3-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-217">Search-Flags</span></span>           | <span data-ttu-id="818b3-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="818b3-218">0x00000000</span></span>                                   |
| <span data-ttu-id="818b3-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-219">System-Flags</span></span>           | <span data-ttu-id="818b3-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="818b3-220">0x00000010</span></span>                                   |
| <span data-ttu-id="818b3-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="818b3-221">Classes used in</span></span>        | [<span data-ttu-id="818b3-222">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="818b3-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="818b3-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="818b3-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="818b3-224">進入</span><span class="sxs-lookup"><span data-stu-id="818b3-224">Entry</span></span> | <span data-ttu-id="818b3-225">值</span><span class="sxs-lookup"><span data-stu-id="818b3-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="818b3-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="818b3-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="818b3-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="818b3-228">System-Only</span></span>            | <span data-ttu-id="818b3-229">否</span><span class="sxs-lookup"><span data-stu-id="818b3-229">False</span></span>                                        |
| <span data-ttu-id="818b3-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="818b3-230">Is-Single-Valued</span></span>       | <span data-ttu-id="818b3-231">對</span><span class="sxs-lookup"><span data-stu-id="818b3-231">True</span></span>                                         |
| <span data-ttu-id="818b3-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="818b3-232">Is Indexed</span></span>             | <span data-ttu-id="818b3-233">否</span><span class="sxs-lookup"><span data-stu-id="818b3-233">False</span></span>                                        |
| <span data-ttu-id="818b3-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="818b3-234">In Global Catalog</span></span>      | <span data-ttu-id="818b3-235">否</span><span class="sxs-lookup"><span data-stu-id="818b3-235">False</span></span>                                        |
| <span data-ttu-id="818b3-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="818b3-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="818b3-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="818b3-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="818b3-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="818b3-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="818b3-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="818b3-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="818b3-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-240">Search-Flags</span></span>           | <span data-ttu-id="818b3-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="818b3-241">0x00000000</span></span>                                   |
| <span data-ttu-id="818b3-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-242">System-Flags</span></span>           | <span data-ttu-id="818b3-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="818b3-243">0x00000010</span></span>                                   |
| <span data-ttu-id="818b3-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="818b3-244">Classes used in</span></span>        | [<span data-ttu-id="818b3-245">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="818b3-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="818b3-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="818b3-246">Windows Server 2012</span></span>



| <span data-ttu-id="818b3-247">進入</span><span class="sxs-lookup"><span data-stu-id="818b3-247">Entry</span></span> | <span data-ttu-id="818b3-248">值</span><span class="sxs-lookup"><span data-stu-id="818b3-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="818b3-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="818b3-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="818b3-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="818b3-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="818b3-251">System-Only</span></span>            | <span data-ttu-id="818b3-252">否</span><span class="sxs-lookup"><span data-stu-id="818b3-252">False</span></span>                                        |
| <span data-ttu-id="818b3-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="818b3-253">Is-Single-Valued</span></span>       | <span data-ttu-id="818b3-254">對</span><span class="sxs-lookup"><span data-stu-id="818b3-254">True</span></span>                                         |
| <span data-ttu-id="818b3-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="818b3-255">Is Indexed</span></span>             | <span data-ttu-id="818b3-256">否</span><span class="sxs-lookup"><span data-stu-id="818b3-256">False</span></span>                                        |
| <span data-ttu-id="818b3-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="818b3-257">In Global Catalog</span></span>      | <span data-ttu-id="818b3-258">否</span><span class="sxs-lookup"><span data-stu-id="818b3-258">False</span></span>                                        |
| <span data-ttu-id="818b3-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="818b3-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="818b3-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="818b3-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="818b3-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="818b3-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="818b3-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="818b3-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="818b3-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-263">Search-Flags</span></span>           | <span data-ttu-id="818b3-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="818b3-264">0x00000000</span></span>                                   |
| <span data-ttu-id="818b3-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="818b3-265">System-Flags</span></span>           | <span data-ttu-id="818b3-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="818b3-266">0x00000010</span></span>                                   |
| <span data-ttu-id="818b3-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="818b3-267">Classes used in</span></span>        | [<span data-ttu-id="818b3-268">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="818b3-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






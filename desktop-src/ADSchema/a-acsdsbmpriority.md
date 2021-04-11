---
title: ACS-DSBM-Priority 屬性
description: 此屬性包含此子網路頻寬管理員 (SBM) 的優先順序。
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-Priority 屬性 AD 架構
- aCSDSBMPriority 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108324"
---
# <a name="acs-dsbm-priority-attribute"></a><span data-ttu-id="436be-105">ACS-DSBM-Priority 屬性</span><span class="sxs-lookup"><span data-stu-id="436be-105">ACS-DSBM-Priority attribute</span></span>

<span data-ttu-id="436be-106">此屬性包含此子網路頻寬管理員 (SBM) 的優先順序。</span><span class="sxs-lookup"><span data-stu-id="436be-106">This attributes contains the priority for this Subnet Bandwidth Manager (SBM).</span></span> <span data-ttu-id="436be-107">若需要選擇新的指定子網路頻寬管理員 (DSBM) ，此值會傳送至網域中的其他 SBMs，作為 DSBM 的 \_ 訊息。</span><span class="sxs-lookup"><span data-stu-id="436be-107">When a new Designated Subnet Bandwidth Manager (DSBM) needs to be elected, this value is sent to other SBMs in the domain as part of a DSBM\_willing message.</span></span> <span data-ttu-id="436be-108">具有最高優先順序的 SBM 會被選擇為新的 DSBM。</span><span class="sxs-lookup"><span data-stu-id="436be-108">The SBM with the highest priority is elected as the new DSBM.</span></span>



| <span data-ttu-id="436be-109">進入</span><span class="sxs-lookup"><span data-stu-id="436be-109">Entry</span></span> | <span data-ttu-id="436be-110">值</span><span class="sxs-lookup"><span data-stu-id="436be-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="436be-111">CN</span><span class="sxs-lookup"><span data-stu-id="436be-111">CN</span></span>                | <span data-ttu-id="436be-112">ACS-DSBM-Priority</span><span class="sxs-lookup"><span data-stu-id="436be-112">ACS-DSBM-Priority</span></span>                    |
| <span data-ttu-id="436be-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="436be-113">Ldap-Display-Name</span></span> | <span data-ttu-id="436be-114">aCSDSBMPriority</span><span class="sxs-lookup"><span data-stu-id="436be-114">aCSDSBMPriority</span></span>                      |
| <span data-ttu-id="436be-115">大小</span><span class="sxs-lookup"><span data-stu-id="436be-115">Size</span></span>              | <span data-ttu-id="436be-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="436be-116">4 bytes</span></span>                              |
| <span data-ttu-id="436be-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="436be-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="436be-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="436be-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="436be-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="436be-119">Attribute-Id</span></span>      | <span data-ttu-id="436be-120">1.2.840.113556.1.4.776</span><span class="sxs-lookup"><span data-stu-id="436be-120">1.2.840.113556.1.4.776</span></span>               |
| <span data-ttu-id="436be-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="436be-121">System-Id-Guid</span></span>    | <span data-ttu-id="436be-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="436be-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="436be-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="436be-123">Syntax</span></span>            | [<span data-ttu-id="436be-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="436be-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="436be-125">實作</span><span class="sxs-lookup"><span data-stu-id="436be-125">Implementations</span></span>

-   [<span data-ttu-id="436be-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="436be-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="436be-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="436be-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="436be-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="436be-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="436be-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="436be-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="436be-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="436be-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="436be-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="436be-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="436be-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="436be-132">Windows 2000 Server</span></span>



| <span data-ttu-id="436be-133">進入</span><span class="sxs-lookup"><span data-stu-id="436be-133">Entry</span></span> | <span data-ttu-id="436be-134">值</span><span class="sxs-lookup"><span data-stu-id="436be-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="436be-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="436be-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="436be-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="436be-137">System-Only</span></span>            | <span data-ttu-id="436be-138">否</span><span class="sxs-lookup"><span data-stu-id="436be-138">False</span></span>                                        |
| <span data-ttu-id="436be-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="436be-139">Is-Single-Valued</span></span>       | <span data-ttu-id="436be-140">對</span><span class="sxs-lookup"><span data-stu-id="436be-140">True</span></span>                                         |
| <span data-ttu-id="436be-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="436be-141">Is Indexed</span></span>             | <span data-ttu-id="436be-142">否</span><span class="sxs-lookup"><span data-stu-id="436be-142">False</span></span>                                        |
| <span data-ttu-id="436be-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="436be-143">In Global Catalog</span></span>      | <span data-ttu-id="436be-144">否</span><span class="sxs-lookup"><span data-stu-id="436be-144">False</span></span>                                        |
| <span data-ttu-id="436be-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="436be-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="436be-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="436be-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="436be-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="436be-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="436be-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="436be-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="436be-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-149">Search-Flags</span></span>           | <span data-ttu-id="436be-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="436be-150">0x00000000</span></span>                                   |
| <span data-ttu-id="436be-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-151">System-Flags</span></span>           | <span data-ttu-id="436be-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="436be-152">0x00000010</span></span>                                   |
| <span data-ttu-id="436be-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="436be-153">Classes used in</span></span>        | [<span data-ttu-id="436be-154">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="436be-154">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="436be-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="436be-155">Windows Server 2003</span></span>



| <span data-ttu-id="436be-156">進入</span><span class="sxs-lookup"><span data-stu-id="436be-156">Entry</span></span> | <span data-ttu-id="436be-157">值</span><span class="sxs-lookup"><span data-stu-id="436be-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="436be-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="436be-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="436be-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="436be-160">System-Only</span></span>            | <span data-ttu-id="436be-161">否</span><span class="sxs-lookup"><span data-stu-id="436be-161">False</span></span>                                        |
| <span data-ttu-id="436be-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="436be-162">Is-Single-Valued</span></span>       | <span data-ttu-id="436be-163">對</span><span class="sxs-lookup"><span data-stu-id="436be-163">True</span></span>                                         |
| <span data-ttu-id="436be-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="436be-164">Is Indexed</span></span>             | <span data-ttu-id="436be-165">否</span><span class="sxs-lookup"><span data-stu-id="436be-165">False</span></span>                                        |
| <span data-ttu-id="436be-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="436be-166">In Global Catalog</span></span>      | <span data-ttu-id="436be-167">否</span><span class="sxs-lookup"><span data-stu-id="436be-167">False</span></span>                                        |
| <span data-ttu-id="436be-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="436be-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="436be-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="436be-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="436be-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="436be-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="436be-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="436be-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="436be-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-172">Search-Flags</span></span>           | <span data-ttu-id="436be-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="436be-173">0x00000000</span></span>                                   |
| <span data-ttu-id="436be-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-174">System-Flags</span></span>           | <span data-ttu-id="436be-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="436be-175">0x00000010</span></span>                                   |
| <span data-ttu-id="436be-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="436be-176">Classes used in</span></span>        | [<span data-ttu-id="436be-177">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="436be-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="436be-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="436be-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="436be-179">進入</span><span class="sxs-lookup"><span data-stu-id="436be-179">Entry</span></span> | <span data-ttu-id="436be-180">值</span><span class="sxs-lookup"><span data-stu-id="436be-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="436be-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="436be-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="436be-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="436be-183">System-Only</span></span>            | <span data-ttu-id="436be-184">否</span><span class="sxs-lookup"><span data-stu-id="436be-184">False</span></span>                                        |
| <span data-ttu-id="436be-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="436be-185">Is-Single-Valued</span></span>       | <span data-ttu-id="436be-186">對</span><span class="sxs-lookup"><span data-stu-id="436be-186">True</span></span>                                         |
| <span data-ttu-id="436be-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="436be-187">Is Indexed</span></span>             | <span data-ttu-id="436be-188">否</span><span class="sxs-lookup"><span data-stu-id="436be-188">False</span></span>                                        |
| <span data-ttu-id="436be-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="436be-189">In Global Catalog</span></span>      | <span data-ttu-id="436be-190">否</span><span class="sxs-lookup"><span data-stu-id="436be-190">False</span></span>                                        |
| <span data-ttu-id="436be-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="436be-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="436be-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="436be-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="436be-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="436be-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="436be-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="436be-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="436be-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-195">Search-Flags</span></span>           | <span data-ttu-id="436be-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="436be-196">0x00000000</span></span>                                   |
| <span data-ttu-id="436be-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-197">System-Flags</span></span>           | <span data-ttu-id="436be-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="436be-198">0x00000010</span></span>                                   |
| <span data-ttu-id="436be-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="436be-199">Classes used in</span></span>        | [<span data-ttu-id="436be-200">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="436be-200">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="436be-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="436be-201">Windows Server 2008</span></span>



| <span data-ttu-id="436be-202">進入</span><span class="sxs-lookup"><span data-stu-id="436be-202">Entry</span></span> | <span data-ttu-id="436be-203">值</span><span class="sxs-lookup"><span data-stu-id="436be-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="436be-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="436be-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="436be-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="436be-206">System-Only</span></span>            | <span data-ttu-id="436be-207">否</span><span class="sxs-lookup"><span data-stu-id="436be-207">False</span></span>                                        |
| <span data-ttu-id="436be-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="436be-208">Is-Single-Valued</span></span>       | <span data-ttu-id="436be-209">對</span><span class="sxs-lookup"><span data-stu-id="436be-209">True</span></span>                                         |
| <span data-ttu-id="436be-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="436be-210">Is Indexed</span></span>             | <span data-ttu-id="436be-211">否</span><span class="sxs-lookup"><span data-stu-id="436be-211">False</span></span>                                        |
| <span data-ttu-id="436be-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="436be-212">In Global Catalog</span></span>      | <span data-ttu-id="436be-213">否</span><span class="sxs-lookup"><span data-stu-id="436be-213">False</span></span>                                        |
| <span data-ttu-id="436be-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="436be-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="436be-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="436be-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="436be-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="436be-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="436be-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="436be-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="436be-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-218">Search-Flags</span></span>           | <span data-ttu-id="436be-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="436be-219">0x00000000</span></span>                                   |
| <span data-ttu-id="436be-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-220">System-Flags</span></span>           | <span data-ttu-id="436be-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="436be-221">0x00000010</span></span>                                   |
| <span data-ttu-id="436be-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="436be-222">Classes used in</span></span>        | [<span data-ttu-id="436be-223">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="436be-223">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="436be-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="436be-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="436be-225">進入</span><span class="sxs-lookup"><span data-stu-id="436be-225">Entry</span></span> | <span data-ttu-id="436be-226">值</span><span class="sxs-lookup"><span data-stu-id="436be-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="436be-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="436be-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="436be-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="436be-229">System-Only</span></span>            | <span data-ttu-id="436be-230">否</span><span class="sxs-lookup"><span data-stu-id="436be-230">False</span></span>                                        |
| <span data-ttu-id="436be-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="436be-231">Is-Single-Valued</span></span>       | <span data-ttu-id="436be-232">對</span><span class="sxs-lookup"><span data-stu-id="436be-232">True</span></span>                                         |
| <span data-ttu-id="436be-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="436be-233">Is Indexed</span></span>             | <span data-ttu-id="436be-234">否</span><span class="sxs-lookup"><span data-stu-id="436be-234">False</span></span>                                        |
| <span data-ttu-id="436be-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="436be-235">In Global Catalog</span></span>      | <span data-ttu-id="436be-236">否</span><span class="sxs-lookup"><span data-stu-id="436be-236">False</span></span>                                        |
| <span data-ttu-id="436be-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="436be-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="436be-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="436be-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="436be-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="436be-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="436be-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="436be-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="436be-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-241">Search-Flags</span></span>           | <span data-ttu-id="436be-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="436be-242">0x00000000</span></span>                                   |
| <span data-ttu-id="436be-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-243">System-Flags</span></span>           | <span data-ttu-id="436be-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="436be-244">0x00000010</span></span>                                   |
| <span data-ttu-id="436be-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="436be-245">Classes used in</span></span>        | [<span data-ttu-id="436be-246">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="436be-246">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="436be-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="436be-247">Windows Server 2012</span></span>



| <span data-ttu-id="436be-248">進入</span><span class="sxs-lookup"><span data-stu-id="436be-248">Entry</span></span> | <span data-ttu-id="436be-249">值</span><span class="sxs-lookup"><span data-stu-id="436be-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="436be-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="436be-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="436be-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="436be-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="436be-252">System-Only</span></span>            | <span data-ttu-id="436be-253">否</span><span class="sxs-lookup"><span data-stu-id="436be-253">False</span></span>                                        |
| <span data-ttu-id="436be-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="436be-254">Is-Single-Valued</span></span>       | <span data-ttu-id="436be-255">對</span><span class="sxs-lookup"><span data-stu-id="436be-255">True</span></span>                                         |
| <span data-ttu-id="436be-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="436be-256">Is Indexed</span></span>             | <span data-ttu-id="436be-257">否</span><span class="sxs-lookup"><span data-stu-id="436be-257">False</span></span>                                        |
| <span data-ttu-id="436be-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="436be-258">In Global Catalog</span></span>      | <span data-ttu-id="436be-259">否</span><span class="sxs-lookup"><span data-stu-id="436be-259">False</span></span>                                        |
| <span data-ttu-id="436be-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="436be-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="436be-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="436be-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="436be-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="436be-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="436be-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="436be-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="436be-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-264">Search-Flags</span></span>           | <span data-ttu-id="436be-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="436be-265">0x00000000</span></span>                                   |
| <span data-ttu-id="436be-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="436be-266">System-Flags</span></span>           | <span data-ttu-id="436be-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="436be-267">0x00000010</span></span>                                   |
| <span data-ttu-id="436be-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="436be-268">Classes used in</span></span>        | [<span data-ttu-id="436be-269">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="436be-269">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






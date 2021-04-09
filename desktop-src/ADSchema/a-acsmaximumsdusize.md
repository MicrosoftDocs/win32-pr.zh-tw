---
title: ACS-SDU 大小上限屬性
description: ACS-最大 SDU 大小屬性僅供內部使用。
ms.assetid: 60dc8b92-888f-4eaf-8c7a-70d1ee12b490
ms.tgt_platform: multiple
keywords:
- ACS-SDU 大小上限屬性 AD 架構
- aCSMaximumSDUSize 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Maximum-SDU-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9fa6260b3e0370f8a3d6e0ddfdab206d41db02
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686888"
---
# <a name="acs-maximum-sdu-size-attribute"></a><span data-ttu-id="14277-105">ACS-SDU 大小上限屬性</span><span class="sxs-lookup"><span data-stu-id="14277-105">ACS-Maximum-SDU-Size attribute</span></span>

<span data-ttu-id="14277-106">**ACS-最大 SDU 大小** 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="14277-106">The **ACS-Maximum-SDU-Size** attribute is for internal use only.</span></span> <span data-ttu-id="14277-107">以 RFC2210 為基礎。</span><span class="sxs-lookup"><span data-stu-id="14277-107">Based on RFC2210.</span></span>



| <span data-ttu-id="14277-108">進入</span><span class="sxs-lookup"><span data-stu-id="14277-108">Entry</span></span> | <span data-ttu-id="14277-109">值</span><span class="sxs-lookup"><span data-stu-id="14277-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="14277-110">CN</span><span class="sxs-lookup"><span data-stu-id="14277-110">CN</span></span>                | <span data-ttu-id="14277-111">ACS-最大-SDU-大小</span><span class="sxs-lookup"><span data-stu-id="14277-111">ACS-Maximum-SDU-Size</span></span>                 |
| <span data-ttu-id="14277-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="14277-112">Ldap-Display-Name</span></span> | <span data-ttu-id="14277-113">aCSMaximumSDUSize</span><span class="sxs-lookup"><span data-stu-id="14277-113">aCSMaximumSDUSize</span></span>                    |
| <span data-ttu-id="14277-114">大小</span><span class="sxs-lookup"><span data-stu-id="14277-114">Size</span></span>              | <span data-ttu-id="14277-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="14277-115">8 bytes</span></span>                              |
| <span data-ttu-id="14277-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="14277-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="14277-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="14277-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="14277-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="14277-118">Attribute-Id</span></span>      | <span data-ttu-id="14277-119">1.2.840.113556.1.4.1314</span><span class="sxs-lookup"><span data-stu-id="14277-119">1.2.840.113556.1.4.1314</span></span>              |
| <span data-ttu-id="14277-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="14277-120">System-Id-Guid</span></span>    | <span data-ttu-id="14277-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="14277-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="14277-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="14277-122">Syntax</span></span>            | [<span data-ttu-id="14277-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="14277-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="14277-124">實作</span><span class="sxs-lookup"><span data-stu-id="14277-124">Implementations</span></span>

-   [<span data-ttu-id="14277-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="14277-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="14277-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="14277-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="14277-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="14277-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="14277-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="14277-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="14277-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14277-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="14277-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="14277-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="14277-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14277-131">Windows 2000 Server</span></span>



| <span data-ttu-id="14277-132">進入</span><span class="sxs-lookup"><span data-stu-id="14277-132">Entry</span></span> | <span data-ttu-id="14277-133">值</span><span class="sxs-lookup"><span data-stu-id="14277-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="14277-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14277-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14277-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="14277-136">System-Only</span></span>            | <span data-ttu-id="14277-137">否</span><span class="sxs-lookup"><span data-stu-id="14277-137">False</span></span>                                        |
| <span data-ttu-id="14277-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14277-138">Is-Single-Valued</span></span>       | <span data-ttu-id="14277-139">對</span><span class="sxs-lookup"><span data-stu-id="14277-139">True</span></span>                                         |
| <span data-ttu-id="14277-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14277-140">Is Indexed</span></span>             | <span data-ttu-id="14277-141">否</span><span class="sxs-lookup"><span data-stu-id="14277-141">False</span></span>                                        |
| <span data-ttu-id="14277-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14277-142">In Global Catalog</span></span>      | <span data-ttu-id="14277-143">否</span><span class="sxs-lookup"><span data-stu-id="14277-143">False</span></span>                                        |
| <span data-ttu-id="14277-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14277-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="14277-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14277-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="14277-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14277-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="14277-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14277-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="14277-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-148">Search-Flags</span></span>           | <span data-ttu-id="14277-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14277-149">0x00000000</span></span>                                   |
| <span data-ttu-id="14277-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-150">System-Flags</span></span>           | <span data-ttu-id="14277-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14277-151">0x00000010</span></span>                                   |
| <span data-ttu-id="14277-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14277-152">Classes used in</span></span>        | [<span data-ttu-id="14277-153">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="14277-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="14277-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14277-154">Windows Server 2003</span></span>



| <span data-ttu-id="14277-155">進入</span><span class="sxs-lookup"><span data-stu-id="14277-155">Entry</span></span> | <span data-ttu-id="14277-156">值</span><span class="sxs-lookup"><span data-stu-id="14277-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="14277-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14277-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14277-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="14277-159">System-Only</span></span>            | <span data-ttu-id="14277-160">否</span><span class="sxs-lookup"><span data-stu-id="14277-160">False</span></span>                                        |
| <span data-ttu-id="14277-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14277-161">Is-Single-Valued</span></span>       | <span data-ttu-id="14277-162">對</span><span class="sxs-lookup"><span data-stu-id="14277-162">True</span></span>                                         |
| <span data-ttu-id="14277-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14277-163">Is Indexed</span></span>             | <span data-ttu-id="14277-164">否</span><span class="sxs-lookup"><span data-stu-id="14277-164">False</span></span>                                        |
| <span data-ttu-id="14277-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14277-165">In Global Catalog</span></span>      | <span data-ttu-id="14277-166">否</span><span class="sxs-lookup"><span data-stu-id="14277-166">False</span></span>                                        |
| <span data-ttu-id="14277-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14277-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="14277-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14277-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="14277-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14277-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="14277-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14277-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="14277-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-171">Search-Flags</span></span>           | <span data-ttu-id="14277-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14277-172">0x00000000</span></span>                                   |
| <span data-ttu-id="14277-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-173">System-Flags</span></span>           | <span data-ttu-id="14277-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14277-174">0x00000010</span></span>                                   |
| <span data-ttu-id="14277-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14277-175">Classes used in</span></span>        | [<span data-ttu-id="14277-176">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="14277-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="14277-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="14277-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="14277-178">進入</span><span class="sxs-lookup"><span data-stu-id="14277-178">Entry</span></span> | <span data-ttu-id="14277-179">值</span><span class="sxs-lookup"><span data-stu-id="14277-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="14277-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14277-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14277-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="14277-182">System-Only</span></span>            | <span data-ttu-id="14277-183">否</span><span class="sxs-lookup"><span data-stu-id="14277-183">False</span></span>                                        |
| <span data-ttu-id="14277-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14277-184">Is-Single-Valued</span></span>       | <span data-ttu-id="14277-185">對</span><span class="sxs-lookup"><span data-stu-id="14277-185">True</span></span>                                         |
| <span data-ttu-id="14277-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14277-186">Is Indexed</span></span>             | <span data-ttu-id="14277-187">否</span><span class="sxs-lookup"><span data-stu-id="14277-187">False</span></span>                                        |
| <span data-ttu-id="14277-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14277-188">In Global Catalog</span></span>      | <span data-ttu-id="14277-189">否</span><span class="sxs-lookup"><span data-stu-id="14277-189">False</span></span>                                        |
| <span data-ttu-id="14277-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14277-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="14277-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14277-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="14277-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14277-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="14277-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14277-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="14277-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-194">Search-Flags</span></span>           | <span data-ttu-id="14277-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14277-195">0x00000000</span></span>                                   |
| <span data-ttu-id="14277-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-196">System-Flags</span></span>           | <span data-ttu-id="14277-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14277-197">0x00000010</span></span>                                   |
| <span data-ttu-id="14277-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14277-198">Classes used in</span></span>        | [<span data-ttu-id="14277-199">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="14277-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="14277-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14277-200">Windows Server 2008</span></span>



| <span data-ttu-id="14277-201">進入</span><span class="sxs-lookup"><span data-stu-id="14277-201">Entry</span></span> | <span data-ttu-id="14277-202">值</span><span class="sxs-lookup"><span data-stu-id="14277-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="14277-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14277-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14277-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="14277-205">System-Only</span></span>            | <span data-ttu-id="14277-206">否</span><span class="sxs-lookup"><span data-stu-id="14277-206">False</span></span>                                        |
| <span data-ttu-id="14277-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14277-207">Is-Single-Valued</span></span>       | <span data-ttu-id="14277-208">對</span><span class="sxs-lookup"><span data-stu-id="14277-208">True</span></span>                                         |
| <span data-ttu-id="14277-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14277-209">Is Indexed</span></span>             | <span data-ttu-id="14277-210">否</span><span class="sxs-lookup"><span data-stu-id="14277-210">False</span></span>                                        |
| <span data-ttu-id="14277-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14277-211">In Global Catalog</span></span>      | <span data-ttu-id="14277-212">否</span><span class="sxs-lookup"><span data-stu-id="14277-212">False</span></span>                                        |
| <span data-ttu-id="14277-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14277-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="14277-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14277-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="14277-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14277-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="14277-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14277-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="14277-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-217">Search-Flags</span></span>           | <span data-ttu-id="14277-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14277-218">0x00000000</span></span>                                   |
| <span data-ttu-id="14277-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-219">System-Flags</span></span>           | <span data-ttu-id="14277-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14277-220">0x00000010</span></span>                                   |
| <span data-ttu-id="14277-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14277-221">Classes used in</span></span>        | [<span data-ttu-id="14277-222">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="14277-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="14277-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14277-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="14277-224">進入</span><span class="sxs-lookup"><span data-stu-id="14277-224">Entry</span></span> | <span data-ttu-id="14277-225">值</span><span class="sxs-lookup"><span data-stu-id="14277-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="14277-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14277-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14277-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="14277-228">System-Only</span></span>            | <span data-ttu-id="14277-229">否</span><span class="sxs-lookup"><span data-stu-id="14277-229">False</span></span>                                        |
| <span data-ttu-id="14277-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14277-230">Is-Single-Valued</span></span>       | <span data-ttu-id="14277-231">對</span><span class="sxs-lookup"><span data-stu-id="14277-231">True</span></span>                                         |
| <span data-ttu-id="14277-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14277-232">Is Indexed</span></span>             | <span data-ttu-id="14277-233">否</span><span class="sxs-lookup"><span data-stu-id="14277-233">False</span></span>                                        |
| <span data-ttu-id="14277-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14277-234">In Global Catalog</span></span>      | <span data-ttu-id="14277-235">否</span><span class="sxs-lookup"><span data-stu-id="14277-235">False</span></span>                                        |
| <span data-ttu-id="14277-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14277-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="14277-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14277-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="14277-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14277-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="14277-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14277-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="14277-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-240">Search-Flags</span></span>           | <span data-ttu-id="14277-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14277-241">0x00000000</span></span>                                   |
| <span data-ttu-id="14277-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-242">System-Flags</span></span>           | <span data-ttu-id="14277-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14277-243">0x00000010</span></span>                                   |
| <span data-ttu-id="14277-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14277-244">Classes used in</span></span>        | [<span data-ttu-id="14277-245">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="14277-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="14277-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14277-246">Windows Server 2012</span></span>



| <span data-ttu-id="14277-247">進入</span><span class="sxs-lookup"><span data-stu-id="14277-247">Entry</span></span> | <span data-ttu-id="14277-248">值</span><span class="sxs-lookup"><span data-stu-id="14277-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="14277-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14277-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14277-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="14277-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="14277-251">System-Only</span></span>            | <span data-ttu-id="14277-252">否</span><span class="sxs-lookup"><span data-stu-id="14277-252">False</span></span>                                        |
| <span data-ttu-id="14277-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14277-253">Is-Single-Valued</span></span>       | <span data-ttu-id="14277-254">對</span><span class="sxs-lookup"><span data-stu-id="14277-254">True</span></span>                                         |
| <span data-ttu-id="14277-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14277-255">Is Indexed</span></span>             | <span data-ttu-id="14277-256">否</span><span class="sxs-lookup"><span data-stu-id="14277-256">False</span></span>                                        |
| <span data-ttu-id="14277-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14277-257">In Global Catalog</span></span>      | <span data-ttu-id="14277-258">否</span><span class="sxs-lookup"><span data-stu-id="14277-258">False</span></span>                                        |
| <span data-ttu-id="14277-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14277-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="14277-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14277-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="14277-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14277-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="14277-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14277-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="14277-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-263">Search-Flags</span></span>           | <span data-ttu-id="14277-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14277-264">0x00000000</span></span>                                   |
| <span data-ttu-id="14277-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14277-265">System-Flags</span></span>           | <span data-ttu-id="14277-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14277-266">0x00000010</span></span>                                   |
| <span data-ttu-id="14277-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14277-267">Classes used in</span></span>        | [<span data-ttu-id="14277-268">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="14277-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






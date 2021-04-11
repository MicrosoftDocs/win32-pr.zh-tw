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
# <a name="acs-maximum-sdu-size-attribute"></a><span data-ttu-id="931bb-105">ACS-SDU 大小上限屬性</span><span class="sxs-lookup"><span data-stu-id="931bb-105">ACS-Maximum-SDU-Size attribute</span></span>

<span data-ttu-id="931bb-106">**ACS-最大 SDU 大小** 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="931bb-106">The **ACS-Maximum-SDU-Size** attribute is for internal use only.</span></span> <span data-ttu-id="931bb-107">以 RFC2210 為基礎。</span><span class="sxs-lookup"><span data-stu-id="931bb-107">Based on RFC2210.</span></span>



| <span data-ttu-id="931bb-108">進入</span><span class="sxs-lookup"><span data-stu-id="931bb-108">Entry</span></span> | <span data-ttu-id="931bb-109">值</span><span class="sxs-lookup"><span data-stu-id="931bb-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="931bb-110">CN</span><span class="sxs-lookup"><span data-stu-id="931bb-110">CN</span></span>                | <span data-ttu-id="931bb-111">ACS-最大-SDU-大小</span><span class="sxs-lookup"><span data-stu-id="931bb-111">ACS-Maximum-SDU-Size</span></span>                 |
| <span data-ttu-id="931bb-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="931bb-112">Ldap-Display-Name</span></span> | <span data-ttu-id="931bb-113">aCSMaximumSDUSize</span><span class="sxs-lookup"><span data-stu-id="931bb-113">aCSMaximumSDUSize</span></span>                    |
| <span data-ttu-id="931bb-114">大小</span><span class="sxs-lookup"><span data-stu-id="931bb-114">Size</span></span>              | <span data-ttu-id="931bb-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="931bb-115">8 bytes</span></span>                              |
| <span data-ttu-id="931bb-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="931bb-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="931bb-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="931bb-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="931bb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="931bb-118">Attribute-Id</span></span>      | <span data-ttu-id="931bb-119">1.2.840.113556.1.4.1314</span><span class="sxs-lookup"><span data-stu-id="931bb-119">1.2.840.113556.1.4.1314</span></span>              |
| <span data-ttu-id="931bb-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="931bb-120">System-Id-Guid</span></span>    | <span data-ttu-id="931bb-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="931bb-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="931bb-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="931bb-122">Syntax</span></span>            | [<span data-ttu-id="931bb-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="931bb-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="931bb-124">實作</span><span class="sxs-lookup"><span data-stu-id="931bb-124">Implementations</span></span>

-   [<span data-ttu-id="931bb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="931bb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="931bb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="931bb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="931bb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="931bb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="931bb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="931bb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="931bb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="931bb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="931bb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="931bb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="931bb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="931bb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="931bb-132">進入</span><span class="sxs-lookup"><span data-stu-id="931bb-132">Entry</span></span> | <span data-ttu-id="931bb-133">值</span><span class="sxs-lookup"><span data-stu-id="931bb-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="931bb-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="931bb-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931bb-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="931bb-136">System-Only</span></span>            | <span data-ttu-id="931bb-137">否</span><span class="sxs-lookup"><span data-stu-id="931bb-137">False</span></span>                                        |
| <span data-ttu-id="931bb-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="931bb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="931bb-139">對</span><span class="sxs-lookup"><span data-stu-id="931bb-139">True</span></span>                                         |
| <span data-ttu-id="931bb-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="931bb-140">Is Indexed</span></span>             | <span data-ttu-id="931bb-141">否</span><span class="sxs-lookup"><span data-stu-id="931bb-141">False</span></span>                                        |
| <span data-ttu-id="931bb-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="931bb-142">In Global Catalog</span></span>      | <span data-ttu-id="931bb-143">否</span><span class="sxs-lookup"><span data-stu-id="931bb-143">False</span></span>                                        |
| <span data-ttu-id="931bb-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="931bb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="931bb-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="931bb-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="931bb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931bb-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="931bb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931bb-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="931bb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-148">Search-Flags</span></span>           | <span data-ttu-id="931bb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931bb-149">0x00000000</span></span>                                   |
| <span data-ttu-id="931bb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-150">System-Flags</span></span>           | <span data-ttu-id="931bb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931bb-151">0x00000010</span></span>                                   |
| <span data-ttu-id="931bb-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="931bb-152">Classes used in</span></span>        | [<span data-ttu-id="931bb-153">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="931bb-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="931bb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="931bb-154">Windows Server 2003</span></span>



| <span data-ttu-id="931bb-155">進入</span><span class="sxs-lookup"><span data-stu-id="931bb-155">Entry</span></span> | <span data-ttu-id="931bb-156">值</span><span class="sxs-lookup"><span data-stu-id="931bb-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="931bb-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="931bb-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931bb-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="931bb-159">System-Only</span></span>            | <span data-ttu-id="931bb-160">否</span><span class="sxs-lookup"><span data-stu-id="931bb-160">False</span></span>                                        |
| <span data-ttu-id="931bb-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="931bb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="931bb-162">對</span><span class="sxs-lookup"><span data-stu-id="931bb-162">True</span></span>                                         |
| <span data-ttu-id="931bb-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="931bb-163">Is Indexed</span></span>             | <span data-ttu-id="931bb-164">否</span><span class="sxs-lookup"><span data-stu-id="931bb-164">False</span></span>                                        |
| <span data-ttu-id="931bb-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="931bb-165">In Global Catalog</span></span>      | <span data-ttu-id="931bb-166">否</span><span class="sxs-lookup"><span data-stu-id="931bb-166">False</span></span>                                        |
| <span data-ttu-id="931bb-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="931bb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="931bb-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="931bb-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="931bb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931bb-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="931bb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931bb-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="931bb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-171">Search-Flags</span></span>           | <span data-ttu-id="931bb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931bb-172">0x00000000</span></span>                                   |
| <span data-ttu-id="931bb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-173">System-Flags</span></span>           | <span data-ttu-id="931bb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931bb-174">0x00000010</span></span>                                   |
| <span data-ttu-id="931bb-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="931bb-175">Classes used in</span></span>        | [<span data-ttu-id="931bb-176">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="931bb-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="931bb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="931bb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="931bb-178">進入</span><span class="sxs-lookup"><span data-stu-id="931bb-178">Entry</span></span> | <span data-ttu-id="931bb-179">值</span><span class="sxs-lookup"><span data-stu-id="931bb-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="931bb-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="931bb-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931bb-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="931bb-182">System-Only</span></span>            | <span data-ttu-id="931bb-183">否</span><span class="sxs-lookup"><span data-stu-id="931bb-183">False</span></span>                                        |
| <span data-ttu-id="931bb-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="931bb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="931bb-185">對</span><span class="sxs-lookup"><span data-stu-id="931bb-185">True</span></span>                                         |
| <span data-ttu-id="931bb-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="931bb-186">Is Indexed</span></span>             | <span data-ttu-id="931bb-187">否</span><span class="sxs-lookup"><span data-stu-id="931bb-187">False</span></span>                                        |
| <span data-ttu-id="931bb-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="931bb-188">In Global Catalog</span></span>      | <span data-ttu-id="931bb-189">否</span><span class="sxs-lookup"><span data-stu-id="931bb-189">False</span></span>                                        |
| <span data-ttu-id="931bb-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="931bb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="931bb-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="931bb-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="931bb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931bb-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="931bb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931bb-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="931bb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-194">Search-Flags</span></span>           | <span data-ttu-id="931bb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931bb-195">0x00000000</span></span>                                   |
| <span data-ttu-id="931bb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-196">System-Flags</span></span>           | <span data-ttu-id="931bb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931bb-197">0x00000010</span></span>                                   |
| <span data-ttu-id="931bb-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="931bb-198">Classes used in</span></span>        | [<span data-ttu-id="931bb-199">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="931bb-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="931bb-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="931bb-200">Windows Server 2008</span></span>



| <span data-ttu-id="931bb-201">進入</span><span class="sxs-lookup"><span data-stu-id="931bb-201">Entry</span></span> | <span data-ttu-id="931bb-202">值</span><span class="sxs-lookup"><span data-stu-id="931bb-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="931bb-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="931bb-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931bb-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="931bb-205">System-Only</span></span>            | <span data-ttu-id="931bb-206">否</span><span class="sxs-lookup"><span data-stu-id="931bb-206">False</span></span>                                        |
| <span data-ttu-id="931bb-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="931bb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="931bb-208">對</span><span class="sxs-lookup"><span data-stu-id="931bb-208">True</span></span>                                         |
| <span data-ttu-id="931bb-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="931bb-209">Is Indexed</span></span>             | <span data-ttu-id="931bb-210">否</span><span class="sxs-lookup"><span data-stu-id="931bb-210">False</span></span>                                        |
| <span data-ttu-id="931bb-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="931bb-211">In Global Catalog</span></span>      | <span data-ttu-id="931bb-212">否</span><span class="sxs-lookup"><span data-stu-id="931bb-212">False</span></span>                                        |
| <span data-ttu-id="931bb-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="931bb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="931bb-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="931bb-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="931bb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931bb-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="931bb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931bb-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="931bb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-217">Search-Flags</span></span>           | <span data-ttu-id="931bb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931bb-218">0x00000000</span></span>                                   |
| <span data-ttu-id="931bb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-219">System-Flags</span></span>           | <span data-ttu-id="931bb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931bb-220">0x00000010</span></span>                                   |
| <span data-ttu-id="931bb-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="931bb-221">Classes used in</span></span>        | [<span data-ttu-id="931bb-222">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="931bb-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="931bb-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="931bb-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="931bb-224">進入</span><span class="sxs-lookup"><span data-stu-id="931bb-224">Entry</span></span> | <span data-ttu-id="931bb-225">值</span><span class="sxs-lookup"><span data-stu-id="931bb-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="931bb-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="931bb-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931bb-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="931bb-228">System-Only</span></span>            | <span data-ttu-id="931bb-229">否</span><span class="sxs-lookup"><span data-stu-id="931bb-229">False</span></span>                                        |
| <span data-ttu-id="931bb-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="931bb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="931bb-231">對</span><span class="sxs-lookup"><span data-stu-id="931bb-231">True</span></span>                                         |
| <span data-ttu-id="931bb-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="931bb-232">Is Indexed</span></span>             | <span data-ttu-id="931bb-233">否</span><span class="sxs-lookup"><span data-stu-id="931bb-233">False</span></span>                                        |
| <span data-ttu-id="931bb-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="931bb-234">In Global Catalog</span></span>      | <span data-ttu-id="931bb-235">否</span><span class="sxs-lookup"><span data-stu-id="931bb-235">False</span></span>                                        |
| <span data-ttu-id="931bb-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="931bb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="931bb-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="931bb-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="931bb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931bb-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="931bb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931bb-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="931bb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-240">Search-Flags</span></span>           | <span data-ttu-id="931bb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931bb-241">0x00000000</span></span>                                   |
| <span data-ttu-id="931bb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-242">System-Flags</span></span>           | <span data-ttu-id="931bb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931bb-243">0x00000010</span></span>                                   |
| <span data-ttu-id="931bb-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="931bb-244">Classes used in</span></span>        | [<span data-ttu-id="931bb-245">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="931bb-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="931bb-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="931bb-246">Windows Server 2012</span></span>



| <span data-ttu-id="931bb-247">進入</span><span class="sxs-lookup"><span data-stu-id="931bb-247">Entry</span></span> | <span data-ttu-id="931bb-248">值</span><span class="sxs-lookup"><span data-stu-id="931bb-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="931bb-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="931bb-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931bb-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="931bb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="931bb-251">System-Only</span></span>            | <span data-ttu-id="931bb-252">否</span><span class="sxs-lookup"><span data-stu-id="931bb-252">False</span></span>                                        |
| <span data-ttu-id="931bb-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="931bb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="931bb-254">對</span><span class="sxs-lookup"><span data-stu-id="931bb-254">True</span></span>                                         |
| <span data-ttu-id="931bb-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="931bb-255">Is Indexed</span></span>             | <span data-ttu-id="931bb-256">否</span><span class="sxs-lookup"><span data-stu-id="931bb-256">False</span></span>                                        |
| <span data-ttu-id="931bb-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="931bb-257">In Global Catalog</span></span>      | <span data-ttu-id="931bb-258">否</span><span class="sxs-lookup"><span data-stu-id="931bb-258">False</span></span>                                        |
| <span data-ttu-id="931bb-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="931bb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="931bb-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="931bb-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="931bb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931bb-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="931bb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931bb-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="931bb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-263">Search-Flags</span></span>           | <span data-ttu-id="931bb-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931bb-264">0x00000000</span></span>                                   |
| <span data-ttu-id="931bb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931bb-265">System-Flags</span></span>           | <span data-ttu-id="931bb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931bb-266">0x00000010</span></span>                                   |
| <span data-ttu-id="931bb-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="931bb-267">Classes used in</span></span>        | [<span data-ttu-id="931bb-268">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="931bb-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






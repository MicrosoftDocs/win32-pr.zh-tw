---
title: ACS-最小延遲屬性
description: '[ACS-最小延遲] 屬性僅供內部使用。'
ms.assetid: ec2cca55-9e31-49da-98aa-aa2f6664ea90
ms.tgt_platform: multiple
keywords:
- ACS-最小延遲屬性 AD 架構
- aCSMinimumLatency 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Minimum-Latency
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab7e9e6d5a9ccf626cdf8849ffe0e29504b4a0b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104025538"
---
# <a name="acs-minimum-latency-attribute"></a><span data-ttu-id="e72be-105">ACS-最小延遲屬性</span><span class="sxs-lookup"><span data-stu-id="e72be-105">ACS-Minimum-Latency attribute</span></span>

<span data-ttu-id="e72be-106">[ **ACS-最小延遲** ] 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="e72be-106">The **ACS-Minimum-Latency** attribute is for internal use only.</span></span> <span data-ttu-id="e72be-107">以 RFC2210 為基礎。</span><span class="sxs-lookup"><span data-stu-id="e72be-107">Based on RFC2210.</span></span>



| <span data-ttu-id="e72be-108">進入</span><span class="sxs-lookup"><span data-stu-id="e72be-108">Entry</span></span> | <span data-ttu-id="e72be-109">值</span><span class="sxs-lookup"><span data-stu-id="e72be-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e72be-110">CN</span><span class="sxs-lookup"><span data-stu-id="e72be-110">CN</span></span>                | <span data-ttu-id="e72be-111">ACS-最小延遲</span><span class="sxs-lookup"><span data-stu-id="e72be-111">ACS-Minimum-Latency</span></span>                  |
| <span data-ttu-id="e72be-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e72be-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e72be-113">aCSMinimumLatency</span><span class="sxs-lookup"><span data-stu-id="e72be-113">aCSMinimumLatency</span></span>                    |
| <span data-ttu-id="e72be-114">大小</span><span class="sxs-lookup"><span data-stu-id="e72be-114">Size</span></span>              | <span data-ttu-id="e72be-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="e72be-115">8 bytes</span></span>                              |
| <span data-ttu-id="e72be-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e72be-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e72be-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e72be-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e72be-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e72be-118">Attribute-Id</span></span>      | <span data-ttu-id="e72be-119">1.2.840.113556.1.4.1316</span><span class="sxs-lookup"><span data-stu-id="e72be-119">1.2.840.113556.1.4.1316</span></span>              |
| <span data-ttu-id="e72be-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e72be-120">System-Id-Guid</span></span>    | <span data-ttu-id="e72be-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="e72be-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="e72be-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e72be-122">Syntax</span></span>            | [<span data-ttu-id="e72be-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="e72be-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e72be-124">實作</span><span class="sxs-lookup"><span data-stu-id="e72be-124">Implementations</span></span>

-   [<span data-ttu-id="e72be-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e72be-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e72be-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e72be-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e72be-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e72be-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e72be-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e72be-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e72be-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e72be-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e72be-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e72be-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e72be-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e72be-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e72be-132">進入</span><span class="sxs-lookup"><span data-stu-id="e72be-132">Entry</span></span> | <span data-ttu-id="e72be-133">值</span><span class="sxs-lookup"><span data-stu-id="e72be-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e72be-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e72be-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e72be-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e72be-136">System-Only</span></span>            | <span data-ttu-id="e72be-137">否</span><span class="sxs-lookup"><span data-stu-id="e72be-137">False</span></span>                                        |
| <span data-ttu-id="e72be-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e72be-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e72be-139">對</span><span class="sxs-lookup"><span data-stu-id="e72be-139">True</span></span>                                         |
| <span data-ttu-id="e72be-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e72be-140">Is Indexed</span></span>             | <span data-ttu-id="e72be-141">否</span><span class="sxs-lookup"><span data-stu-id="e72be-141">False</span></span>                                        |
| <span data-ttu-id="e72be-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e72be-142">In Global Catalog</span></span>      | <span data-ttu-id="e72be-143">否</span><span class="sxs-lookup"><span data-stu-id="e72be-143">False</span></span>                                        |
| <span data-ttu-id="e72be-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e72be-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e72be-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e72be-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e72be-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e72be-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e72be-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e72be-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e72be-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-148">Search-Flags</span></span>           | <span data-ttu-id="e72be-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e72be-149">0x00000000</span></span>                                   |
| <span data-ttu-id="e72be-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-150">System-Flags</span></span>           | <span data-ttu-id="e72be-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e72be-151">0x00000010</span></span>                                   |
| <span data-ttu-id="e72be-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e72be-152">Classes used in</span></span>        | [<span data-ttu-id="e72be-153">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="e72be-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e72be-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e72be-154">Windows Server 2003</span></span>



| <span data-ttu-id="e72be-155">進入</span><span class="sxs-lookup"><span data-stu-id="e72be-155">Entry</span></span> | <span data-ttu-id="e72be-156">值</span><span class="sxs-lookup"><span data-stu-id="e72be-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e72be-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e72be-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e72be-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e72be-159">System-Only</span></span>            | <span data-ttu-id="e72be-160">否</span><span class="sxs-lookup"><span data-stu-id="e72be-160">False</span></span>                                        |
| <span data-ttu-id="e72be-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e72be-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e72be-162">對</span><span class="sxs-lookup"><span data-stu-id="e72be-162">True</span></span>                                         |
| <span data-ttu-id="e72be-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e72be-163">Is Indexed</span></span>             | <span data-ttu-id="e72be-164">否</span><span class="sxs-lookup"><span data-stu-id="e72be-164">False</span></span>                                        |
| <span data-ttu-id="e72be-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e72be-165">In Global Catalog</span></span>      | <span data-ttu-id="e72be-166">否</span><span class="sxs-lookup"><span data-stu-id="e72be-166">False</span></span>                                        |
| <span data-ttu-id="e72be-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e72be-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e72be-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e72be-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e72be-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e72be-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e72be-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e72be-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e72be-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-171">Search-Flags</span></span>           | <span data-ttu-id="e72be-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e72be-172">0x00000000</span></span>                                   |
| <span data-ttu-id="e72be-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-173">System-Flags</span></span>           | <span data-ttu-id="e72be-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e72be-174">0x00000010</span></span>                                   |
| <span data-ttu-id="e72be-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e72be-175">Classes used in</span></span>        | [<span data-ttu-id="e72be-176">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="e72be-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e72be-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e72be-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e72be-178">進入</span><span class="sxs-lookup"><span data-stu-id="e72be-178">Entry</span></span> | <span data-ttu-id="e72be-179">值</span><span class="sxs-lookup"><span data-stu-id="e72be-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e72be-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e72be-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e72be-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e72be-182">System-Only</span></span>            | <span data-ttu-id="e72be-183">否</span><span class="sxs-lookup"><span data-stu-id="e72be-183">False</span></span>                                        |
| <span data-ttu-id="e72be-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e72be-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e72be-185">對</span><span class="sxs-lookup"><span data-stu-id="e72be-185">True</span></span>                                         |
| <span data-ttu-id="e72be-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e72be-186">Is Indexed</span></span>             | <span data-ttu-id="e72be-187">否</span><span class="sxs-lookup"><span data-stu-id="e72be-187">False</span></span>                                        |
| <span data-ttu-id="e72be-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e72be-188">In Global Catalog</span></span>      | <span data-ttu-id="e72be-189">否</span><span class="sxs-lookup"><span data-stu-id="e72be-189">False</span></span>                                        |
| <span data-ttu-id="e72be-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e72be-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e72be-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e72be-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e72be-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e72be-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e72be-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e72be-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e72be-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-194">Search-Flags</span></span>           | <span data-ttu-id="e72be-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e72be-195">0x00000000</span></span>                                   |
| <span data-ttu-id="e72be-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-196">System-Flags</span></span>           | <span data-ttu-id="e72be-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e72be-197">0x00000010</span></span>                                   |
| <span data-ttu-id="e72be-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e72be-198">Classes used in</span></span>        | [<span data-ttu-id="e72be-199">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="e72be-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e72be-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e72be-200">Windows Server 2008</span></span>



| <span data-ttu-id="e72be-201">進入</span><span class="sxs-lookup"><span data-stu-id="e72be-201">Entry</span></span> | <span data-ttu-id="e72be-202">值</span><span class="sxs-lookup"><span data-stu-id="e72be-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e72be-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e72be-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e72be-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e72be-205">System-Only</span></span>            | <span data-ttu-id="e72be-206">否</span><span class="sxs-lookup"><span data-stu-id="e72be-206">False</span></span>                                        |
| <span data-ttu-id="e72be-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e72be-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e72be-208">對</span><span class="sxs-lookup"><span data-stu-id="e72be-208">True</span></span>                                         |
| <span data-ttu-id="e72be-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e72be-209">Is Indexed</span></span>             | <span data-ttu-id="e72be-210">否</span><span class="sxs-lookup"><span data-stu-id="e72be-210">False</span></span>                                        |
| <span data-ttu-id="e72be-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e72be-211">In Global Catalog</span></span>      | <span data-ttu-id="e72be-212">否</span><span class="sxs-lookup"><span data-stu-id="e72be-212">False</span></span>                                        |
| <span data-ttu-id="e72be-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e72be-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e72be-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e72be-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e72be-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e72be-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e72be-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e72be-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e72be-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-217">Search-Flags</span></span>           | <span data-ttu-id="e72be-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e72be-218">0x00000000</span></span>                                   |
| <span data-ttu-id="e72be-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-219">System-Flags</span></span>           | <span data-ttu-id="e72be-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e72be-220">0x00000010</span></span>                                   |
| <span data-ttu-id="e72be-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e72be-221">Classes used in</span></span>        | [<span data-ttu-id="e72be-222">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="e72be-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e72be-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e72be-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e72be-224">進入</span><span class="sxs-lookup"><span data-stu-id="e72be-224">Entry</span></span> | <span data-ttu-id="e72be-225">值</span><span class="sxs-lookup"><span data-stu-id="e72be-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e72be-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e72be-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e72be-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e72be-228">System-Only</span></span>            | <span data-ttu-id="e72be-229">否</span><span class="sxs-lookup"><span data-stu-id="e72be-229">False</span></span>                                        |
| <span data-ttu-id="e72be-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e72be-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e72be-231">對</span><span class="sxs-lookup"><span data-stu-id="e72be-231">True</span></span>                                         |
| <span data-ttu-id="e72be-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e72be-232">Is Indexed</span></span>             | <span data-ttu-id="e72be-233">否</span><span class="sxs-lookup"><span data-stu-id="e72be-233">False</span></span>                                        |
| <span data-ttu-id="e72be-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e72be-234">In Global Catalog</span></span>      | <span data-ttu-id="e72be-235">否</span><span class="sxs-lookup"><span data-stu-id="e72be-235">False</span></span>                                        |
| <span data-ttu-id="e72be-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e72be-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e72be-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e72be-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e72be-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e72be-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e72be-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e72be-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e72be-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-240">Search-Flags</span></span>           | <span data-ttu-id="e72be-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e72be-241">0x00000000</span></span>                                   |
| <span data-ttu-id="e72be-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-242">System-Flags</span></span>           | <span data-ttu-id="e72be-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e72be-243">0x00000010</span></span>                                   |
| <span data-ttu-id="e72be-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e72be-244">Classes used in</span></span>        | [<span data-ttu-id="e72be-245">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="e72be-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e72be-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e72be-246">Windows Server 2012</span></span>



| <span data-ttu-id="e72be-247">進入</span><span class="sxs-lookup"><span data-stu-id="e72be-247">Entry</span></span> | <span data-ttu-id="e72be-248">值</span><span class="sxs-lookup"><span data-stu-id="e72be-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e72be-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e72be-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e72be-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e72be-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e72be-251">System-Only</span></span>            | <span data-ttu-id="e72be-252">否</span><span class="sxs-lookup"><span data-stu-id="e72be-252">False</span></span>                                        |
| <span data-ttu-id="e72be-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e72be-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e72be-254">對</span><span class="sxs-lookup"><span data-stu-id="e72be-254">True</span></span>                                         |
| <span data-ttu-id="e72be-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e72be-255">Is Indexed</span></span>             | <span data-ttu-id="e72be-256">否</span><span class="sxs-lookup"><span data-stu-id="e72be-256">False</span></span>                                        |
| <span data-ttu-id="e72be-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e72be-257">In Global Catalog</span></span>      | <span data-ttu-id="e72be-258">否</span><span class="sxs-lookup"><span data-stu-id="e72be-258">False</span></span>                                        |
| <span data-ttu-id="e72be-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e72be-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e72be-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e72be-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e72be-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e72be-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e72be-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e72be-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e72be-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-263">Search-Flags</span></span>           | <span data-ttu-id="e72be-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e72be-264">0x00000000</span></span>                                   |
| <span data-ttu-id="e72be-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e72be-265">System-Flags</span></span>           | <span data-ttu-id="e72be-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e72be-266">0x00000010</span></span>                                   |
| <span data-ttu-id="e72be-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e72be-267">Classes used in</span></span>        | [<span data-ttu-id="e72be-268">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="e72be-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






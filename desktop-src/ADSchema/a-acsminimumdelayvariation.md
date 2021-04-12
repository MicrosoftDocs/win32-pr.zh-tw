---
title: ACS-最小延遲-變化屬性
description: ACS-最小延遲變化屬性僅供內部使用。
ms.assetid: eb82ac12-d570-4edc-bbfa-2de63d8f5088
ms.tgt_platform: multiple
keywords:
- ACS-最小延遲-變化屬性 AD 架構
- aCSMinimumDelayVariation 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Minimum-Delay-Variation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4f360e87bd2d9c36da1651800e5765a0a6f924
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509734"
---
# <a name="acs-minimum-delay-variation-attribute"></a><span data-ttu-id="b319a-105">ACS-最小延遲-變化屬性</span><span class="sxs-lookup"><span data-stu-id="b319a-105">ACS-Minimum-Delay-Variation attribute</span></span>

<span data-ttu-id="b319a-106">**ACS-最小延遲變化** 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="b319a-106">The **ACS-Minimum-Delay-Variation** attribute is for internal use only.</span></span> <span data-ttu-id="b319a-107">以 RFC2210 為基礎。</span><span class="sxs-lookup"><span data-stu-id="b319a-107">Based on RFC2210.</span></span>



| <span data-ttu-id="b319a-108">進入</span><span class="sxs-lookup"><span data-stu-id="b319a-108">Entry</span></span> | <span data-ttu-id="b319a-109">值</span><span class="sxs-lookup"><span data-stu-id="b319a-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b319a-110">CN</span><span class="sxs-lookup"><span data-stu-id="b319a-110">CN</span></span>                | <span data-ttu-id="b319a-111">ACS-最小延遲-變化</span><span class="sxs-lookup"><span data-stu-id="b319a-111">ACS-Minimum-Delay-Variation</span></span>          |
| <span data-ttu-id="b319a-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b319a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b319a-113">aCSMinimumDelayVariation</span><span class="sxs-lookup"><span data-stu-id="b319a-113">aCSMinimumDelayVariation</span></span>             |
| <span data-ttu-id="b319a-114">大小</span><span class="sxs-lookup"><span data-stu-id="b319a-114">Size</span></span>              | <span data-ttu-id="b319a-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="b319a-115">8 bytes</span></span>                              |
| <span data-ttu-id="b319a-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b319a-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b319a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b319a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b319a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b319a-118">Attribute-Id</span></span>      | <span data-ttu-id="b319a-119">1.2.840.113556.1.4.1317</span><span class="sxs-lookup"><span data-stu-id="b319a-119">1.2.840.113556.1.4.1317</span></span>              |
| <span data-ttu-id="b319a-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b319a-120">System-Id-Guid</span></span>    | <span data-ttu-id="b319a-121">9c65329b-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="b319a-121">9c65329b-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="b319a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b319a-122">Syntax</span></span>            | [<span data-ttu-id="b319a-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="b319a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b319a-124">實作</span><span class="sxs-lookup"><span data-stu-id="b319a-124">Implementations</span></span>

-   [<span data-ttu-id="b319a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b319a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b319a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b319a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b319a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b319a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b319a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b319a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b319a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b319a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b319a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b319a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b319a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b319a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b319a-132">進入</span><span class="sxs-lookup"><span data-stu-id="b319a-132">Entry</span></span> | <span data-ttu-id="b319a-133">值</span><span class="sxs-lookup"><span data-stu-id="b319a-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b319a-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b319a-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b319a-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b319a-136">System-Only</span></span>            | <span data-ttu-id="b319a-137">否</span><span class="sxs-lookup"><span data-stu-id="b319a-137">False</span></span>                                        |
| <span data-ttu-id="b319a-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b319a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b319a-139">對</span><span class="sxs-lookup"><span data-stu-id="b319a-139">True</span></span>                                         |
| <span data-ttu-id="b319a-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b319a-140">Is Indexed</span></span>             | <span data-ttu-id="b319a-141">否</span><span class="sxs-lookup"><span data-stu-id="b319a-141">False</span></span>                                        |
| <span data-ttu-id="b319a-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b319a-142">In Global Catalog</span></span>      | <span data-ttu-id="b319a-143">否</span><span class="sxs-lookup"><span data-stu-id="b319a-143">False</span></span>                                        |
| <span data-ttu-id="b319a-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b319a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b319a-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b319a-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b319a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b319a-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b319a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b319a-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b319a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-148">Search-Flags</span></span>           | <span data-ttu-id="b319a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b319a-149">0x00000000</span></span>                                   |
| <span data-ttu-id="b319a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-150">System-Flags</span></span>           | <span data-ttu-id="b319a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b319a-151">0x00000010</span></span>                                   |
| <span data-ttu-id="b319a-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b319a-152">Classes used in</span></span>        | [<span data-ttu-id="b319a-153">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="b319a-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b319a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b319a-154">Windows Server 2003</span></span>



| <span data-ttu-id="b319a-155">進入</span><span class="sxs-lookup"><span data-stu-id="b319a-155">Entry</span></span> | <span data-ttu-id="b319a-156">值</span><span class="sxs-lookup"><span data-stu-id="b319a-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b319a-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b319a-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b319a-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b319a-159">System-Only</span></span>            | <span data-ttu-id="b319a-160">否</span><span class="sxs-lookup"><span data-stu-id="b319a-160">False</span></span>                                        |
| <span data-ttu-id="b319a-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b319a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b319a-162">對</span><span class="sxs-lookup"><span data-stu-id="b319a-162">True</span></span>                                         |
| <span data-ttu-id="b319a-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b319a-163">Is Indexed</span></span>             | <span data-ttu-id="b319a-164">否</span><span class="sxs-lookup"><span data-stu-id="b319a-164">False</span></span>                                        |
| <span data-ttu-id="b319a-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b319a-165">In Global Catalog</span></span>      | <span data-ttu-id="b319a-166">否</span><span class="sxs-lookup"><span data-stu-id="b319a-166">False</span></span>                                        |
| <span data-ttu-id="b319a-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b319a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b319a-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b319a-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b319a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b319a-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b319a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b319a-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b319a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-171">Search-Flags</span></span>           | <span data-ttu-id="b319a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b319a-172">0x00000000</span></span>                                   |
| <span data-ttu-id="b319a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-173">System-Flags</span></span>           | <span data-ttu-id="b319a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b319a-174">0x00000010</span></span>                                   |
| <span data-ttu-id="b319a-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b319a-175">Classes used in</span></span>        | [<span data-ttu-id="b319a-176">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="b319a-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b319a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b319a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b319a-178">進入</span><span class="sxs-lookup"><span data-stu-id="b319a-178">Entry</span></span> | <span data-ttu-id="b319a-179">值</span><span class="sxs-lookup"><span data-stu-id="b319a-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b319a-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b319a-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b319a-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b319a-182">System-Only</span></span>            | <span data-ttu-id="b319a-183">否</span><span class="sxs-lookup"><span data-stu-id="b319a-183">False</span></span>                                        |
| <span data-ttu-id="b319a-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b319a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b319a-185">對</span><span class="sxs-lookup"><span data-stu-id="b319a-185">True</span></span>                                         |
| <span data-ttu-id="b319a-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b319a-186">Is Indexed</span></span>             | <span data-ttu-id="b319a-187">否</span><span class="sxs-lookup"><span data-stu-id="b319a-187">False</span></span>                                        |
| <span data-ttu-id="b319a-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b319a-188">In Global Catalog</span></span>      | <span data-ttu-id="b319a-189">否</span><span class="sxs-lookup"><span data-stu-id="b319a-189">False</span></span>                                        |
| <span data-ttu-id="b319a-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b319a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b319a-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b319a-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b319a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b319a-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b319a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b319a-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b319a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-194">Search-Flags</span></span>           | <span data-ttu-id="b319a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b319a-195">0x00000000</span></span>                                   |
| <span data-ttu-id="b319a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-196">System-Flags</span></span>           | <span data-ttu-id="b319a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b319a-197">0x00000010</span></span>                                   |
| <span data-ttu-id="b319a-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b319a-198">Classes used in</span></span>        | [<span data-ttu-id="b319a-199">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="b319a-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b319a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b319a-200">Windows Server 2008</span></span>



| <span data-ttu-id="b319a-201">進入</span><span class="sxs-lookup"><span data-stu-id="b319a-201">Entry</span></span> | <span data-ttu-id="b319a-202">值</span><span class="sxs-lookup"><span data-stu-id="b319a-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b319a-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b319a-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b319a-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b319a-205">System-Only</span></span>            | <span data-ttu-id="b319a-206">否</span><span class="sxs-lookup"><span data-stu-id="b319a-206">False</span></span>                                        |
| <span data-ttu-id="b319a-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b319a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b319a-208">對</span><span class="sxs-lookup"><span data-stu-id="b319a-208">True</span></span>                                         |
| <span data-ttu-id="b319a-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b319a-209">Is Indexed</span></span>             | <span data-ttu-id="b319a-210">否</span><span class="sxs-lookup"><span data-stu-id="b319a-210">False</span></span>                                        |
| <span data-ttu-id="b319a-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b319a-211">In Global Catalog</span></span>      | <span data-ttu-id="b319a-212">否</span><span class="sxs-lookup"><span data-stu-id="b319a-212">False</span></span>                                        |
| <span data-ttu-id="b319a-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b319a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b319a-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b319a-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b319a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b319a-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b319a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b319a-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b319a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-217">Search-Flags</span></span>           | <span data-ttu-id="b319a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b319a-218">0x00000000</span></span>                                   |
| <span data-ttu-id="b319a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-219">System-Flags</span></span>           | <span data-ttu-id="b319a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b319a-220">0x00000010</span></span>                                   |
| <span data-ttu-id="b319a-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b319a-221">Classes used in</span></span>        | [<span data-ttu-id="b319a-222">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="b319a-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b319a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b319a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b319a-224">進入</span><span class="sxs-lookup"><span data-stu-id="b319a-224">Entry</span></span> | <span data-ttu-id="b319a-225">值</span><span class="sxs-lookup"><span data-stu-id="b319a-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b319a-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b319a-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b319a-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b319a-228">System-Only</span></span>            | <span data-ttu-id="b319a-229">否</span><span class="sxs-lookup"><span data-stu-id="b319a-229">False</span></span>                                        |
| <span data-ttu-id="b319a-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b319a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b319a-231">對</span><span class="sxs-lookup"><span data-stu-id="b319a-231">True</span></span>                                         |
| <span data-ttu-id="b319a-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b319a-232">Is Indexed</span></span>             | <span data-ttu-id="b319a-233">否</span><span class="sxs-lookup"><span data-stu-id="b319a-233">False</span></span>                                        |
| <span data-ttu-id="b319a-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b319a-234">In Global Catalog</span></span>      | <span data-ttu-id="b319a-235">否</span><span class="sxs-lookup"><span data-stu-id="b319a-235">False</span></span>                                        |
| <span data-ttu-id="b319a-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b319a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b319a-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b319a-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b319a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b319a-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b319a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b319a-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b319a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-240">Search-Flags</span></span>           | <span data-ttu-id="b319a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b319a-241">0x00000000</span></span>                                   |
| <span data-ttu-id="b319a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-242">System-Flags</span></span>           | <span data-ttu-id="b319a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b319a-243">0x00000010</span></span>                                   |
| <span data-ttu-id="b319a-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b319a-244">Classes used in</span></span>        | [<span data-ttu-id="b319a-245">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="b319a-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b319a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b319a-246">Windows Server 2012</span></span>



| <span data-ttu-id="b319a-247">進入</span><span class="sxs-lookup"><span data-stu-id="b319a-247">Entry</span></span> | <span data-ttu-id="b319a-248">值</span><span class="sxs-lookup"><span data-stu-id="b319a-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b319a-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b319a-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b319a-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b319a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b319a-251">System-Only</span></span>            | <span data-ttu-id="b319a-252">否</span><span class="sxs-lookup"><span data-stu-id="b319a-252">False</span></span>                                        |
| <span data-ttu-id="b319a-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b319a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b319a-254">對</span><span class="sxs-lookup"><span data-stu-id="b319a-254">True</span></span>                                         |
| <span data-ttu-id="b319a-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b319a-255">Is Indexed</span></span>             | <span data-ttu-id="b319a-256">否</span><span class="sxs-lookup"><span data-stu-id="b319a-256">False</span></span>                                        |
| <span data-ttu-id="b319a-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b319a-257">In Global Catalog</span></span>      | <span data-ttu-id="b319a-258">否</span><span class="sxs-lookup"><span data-stu-id="b319a-258">False</span></span>                                        |
| <span data-ttu-id="b319a-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b319a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b319a-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b319a-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b319a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b319a-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b319a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b319a-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b319a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-263">Search-Flags</span></span>           | <span data-ttu-id="b319a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b319a-264">0x00000000</span></span>                                   |
| <span data-ttu-id="b319a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b319a-265">System-Flags</span></span>           | <span data-ttu-id="b319a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b319a-266">0x00000010</span></span>                                   |
| <span data-ttu-id="b319a-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b319a-267">Classes used in</span></span>        | [<span data-ttu-id="b319a-268">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="b319a-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






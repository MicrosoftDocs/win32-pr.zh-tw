---
title: ACS-最大權杖-每個流程的 Bucket-每個流程屬性
description: 「ACS-最大權杖-每個流程」屬性僅供內部使用。
ms.assetid: 2c269bda-7b0d-4ef4-8c67-9f5e7c52e3ae
ms.tgt_platform: multiple
keywords:
- ACS-最大權杖-每個流程的每個流程屬性 AD 架構
- aCSMaxTokenBucketPerFlow 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Max-Token-Bucket-Per-Flow
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb323af82b270c20478e8af4aafc3ee4142125ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108312"
---
# <a name="acs-max-token-bucket-per-flow-attribute"></a><span data-ttu-id="3d10e-105">ACS-最大權杖-每個流程的 Bucket-每個流程屬性</span><span class="sxs-lookup"><span data-stu-id="3d10e-105">ACS-Max-Token-Bucket-Per-Flow attribute</span></span>

<span data-ttu-id="3d10e-106">「 **ACS-最大權杖-每個流程** 」屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="3d10e-106">The **ACS-Max-Token-Bucket-Per-Flow** attribute is for internal use only.</span></span> <span data-ttu-id="3d10e-107">以 RFC2210 為基礎。</span><span class="sxs-lookup"><span data-stu-id="3d10e-107">Based on RFC2210.</span></span>



| <span data-ttu-id="3d10e-108">進入</span><span class="sxs-lookup"><span data-stu-id="3d10e-108">Entry</span></span> | <span data-ttu-id="3d10e-109">值</span><span class="sxs-lookup"><span data-stu-id="3d10e-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3d10e-110">CN</span><span class="sxs-lookup"><span data-stu-id="3d10e-110">CN</span></span>                | <span data-ttu-id="3d10e-111">ACS-最大權杖-每個流程的 Bucket</span><span class="sxs-lookup"><span data-stu-id="3d10e-111">ACS-Max-Token-Bucket-Per-Flow</span></span>        |
| <span data-ttu-id="3d10e-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3d10e-112">Ldap-Display-Name</span></span> | <span data-ttu-id="3d10e-113">aCSMaxTokenBucketPerFlow</span><span class="sxs-lookup"><span data-stu-id="3d10e-113">aCSMaxTokenBucketPerFlow</span></span>             |
| <span data-ttu-id="3d10e-114">大小</span><span class="sxs-lookup"><span data-stu-id="3d10e-114">Size</span></span>              | <span data-ttu-id="3d10e-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="3d10e-115">8 bytes</span></span>                              |
| <span data-ttu-id="3d10e-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3d10e-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="3d10e-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3d10e-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3d10e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d10e-118">Attribute-Id</span></span>      | <span data-ttu-id="3d10e-119">1.2.840.113556.1.4.1313</span><span class="sxs-lookup"><span data-stu-id="3d10e-119">1.2.840.113556.1.4.1313</span></span>              |
| <span data-ttu-id="3d10e-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3d10e-120">System-Id-Guid</span></span>    | <span data-ttu-id="3d10e-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="3d10e-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="3d10e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d10e-122">Syntax</span></span>            | [<span data-ttu-id="3d10e-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="3d10e-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="3d10e-124">實作</span><span class="sxs-lookup"><span data-stu-id="3d10e-124">Implementations</span></span>

-   [<span data-ttu-id="3d10e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3d10e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3d10e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d10e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d10e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d10e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d10e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d10e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d10e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d10e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d10e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d10e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3d10e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d10e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="3d10e-132">進入</span><span class="sxs-lookup"><span data-stu-id="3d10e-132">Entry</span></span> | <span data-ttu-id="3d10e-133">值</span><span class="sxs-lookup"><span data-stu-id="3d10e-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d10e-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d10e-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d10e-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d10e-136">System-Only</span></span>            | <span data-ttu-id="3d10e-137">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-137">False</span></span>                                        |
| <span data-ttu-id="3d10e-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d10e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="3d10e-139">對</span><span class="sxs-lookup"><span data-stu-id="3d10e-139">True</span></span>                                         |
| <span data-ttu-id="3d10e-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d10e-140">Is Indexed</span></span>             | <span data-ttu-id="3d10e-141">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-141">False</span></span>                                        |
| <span data-ttu-id="3d10e-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d10e-142">In Global Catalog</span></span>      | <span data-ttu-id="3d10e-143">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-143">False</span></span>                                        |
| <span data-ttu-id="3d10e-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d10e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d10e-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d10e-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d10e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d10e-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d10e-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-148">Search-Flags</span></span>           | <span data-ttu-id="3d10e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d10e-149">0x00000000</span></span>                                   |
| <span data-ttu-id="3d10e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-150">System-Flags</span></span>           | <span data-ttu-id="3d10e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d10e-151">0x00000010</span></span>                                   |
| <span data-ttu-id="3d10e-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d10e-152">Classes used in</span></span>        | [<span data-ttu-id="3d10e-153">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="3d10e-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3d10e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d10e-154">Windows Server 2003</span></span>



| <span data-ttu-id="3d10e-155">進入</span><span class="sxs-lookup"><span data-stu-id="3d10e-155">Entry</span></span> | <span data-ttu-id="3d10e-156">值</span><span class="sxs-lookup"><span data-stu-id="3d10e-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d10e-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d10e-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d10e-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d10e-159">System-Only</span></span>            | <span data-ttu-id="3d10e-160">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-160">False</span></span>                                        |
| <span data-ttu-id="3d10e-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d10e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3d10e-162">對</span><span class="sxs-lookup"><span data-stu-id="3d10e-162">True</span></span>                                         |
| <span data-ttu-id="3d10e-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d10e-163">Is Indexed</span></span>             | <span data-ttu-id="3d10e-164">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-164">False</span></span>                                        |
| <span data-ttu-id="3d10e-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d10e-165">In Global Catalog</span></span>      | <span data-ttu-id="3d10e-166">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-166">False</span></span>                                        |
| <span data-ttu-id="3d10e-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d10e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d10e-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d10e-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d10e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d10e-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d10e-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-171">Search-Flags</span></span>           | <span data-ttu-id="3d10e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d10e-172">0x00000000</span></span>                                   |
| <span data-ttu-id="3d10e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-173">System-Flags</span></span>           | <span data-ttu-id="3d10e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d10e-174">0x00000010</span></span>                                   |
| <span data-ttu-id="3d10e-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d10e-175">Classes used in</span></span>        | [<span data-ttu-id="3d10e-176">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="3d10e-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d10e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d10e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d10e-178">進入</span><span class="sxs-lookup"><span data-stu-id="3d10e-178">Entry</span></span> | <span data-ttu-id="3d10e-179">值</span><span class="sxs-lookup"><span data-stu-id="3d10e-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d10e-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d10e-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d10e-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d10e-182">System-Only</span></span>            | <span data-ttu-id="3d10e-183">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-183">False</span></span>                                        |
| <span data-ttu-id="3d10e-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d10e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="3d10e-185">對</span><span class="sxs-lookup"><span data-stu-id="3d10e-185">True</span></span>                                         |
| <span data-ttu-id="3d10e-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d10e-186">Is Indexed</span></span>             | <span data-ttu-id="3d10e-187">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-187">False</span></span>                                        |
| <span data-ttu-id="3d10e-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d10e-188">In Global Catalog</span></span>      | <span data-ttu-id="3d10e-189">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-189">False</span></span>                                        |
| <span data-ttu-id="3d10e-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d10e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d10e-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d10e-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d10e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d10e-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d10e-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-194">Search-Flags</span></span>           | <span data-ttu-id="3d10e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d10e-195">0x00000000</span></span>                                   |
| <span data-ttu-id="3d10e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-196">System-Flags</span></span>           | <span data-ttu-id="3d10e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d10e-197">0x00000010</span></span>                                   |
| <span data-ttu-id="3d10e-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d10e-198">Classes used in</span></span>        | [<span data-ttu-id="3d10e-199">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="3d10e-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d10e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d10e-200">Windows Server 2008</span></span>



| <span data-ttu-id="3d10e-201">進入</span><span class="sxs-lookup"><span data-stu-id="3d10e-201">Entry</span></span> | <span data-ttu-id="3d10e-202">值</span><span class="sxs-lookup"><span data-stu-id="3d10e-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d10e-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d10e-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d10e-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d10e-205">System-Only</span></span>            | <span data-ttu-id="3d10e-206">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-206">False</span></span>                                        |
| <span data-ttu-id="3d10e-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d10e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="3d10e-208">對</span><span class="sxs-lookup"><span data-stu-id="3d10e-208">True</span></span>                                         |
| <span data-ttu-id="3d10e-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d10e-209">Is Indexed</span></span>             | <span data-ttu-id="3d10e-210">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-210">False</span></span>                                        |
| <span data-ttu-id="3d10e-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d10e-211">In Global Catalog</span></span>      | <span data-ttu-id="3d10e-212">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-212">False</span></span>                                        |
| <span data-ttu-id="3d10e-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d10e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d10e-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d10e-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d10e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d10e-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d10e-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-217">Search-Flags</span></span>           | <span data-ttu-id="3d10e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d10e-218">0x00000000</span></span>                                   |
| <span data-ttu-id="3d10e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-219">System-Flags</span></span>           | <span data-ttu-id="3d10e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d10e-220">0x00000010</span></span>                                   |
| <span data-ttu-id="3d10e-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d10e-221">Classes used in</span></span>        | [<span data-ttu-id="3d10e-222">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="3d10e-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d10e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d10e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d10e-224">進入</span><span class="sxs-lookup"><span data-stu-id="3d10e-224">Entry</span></span> | <span data-ttu-id="3d10e-225">值</span><span class="sxs-lookup"><span data-stu-id="3d10e-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d10e-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d10e-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d10e-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d10e-228">System-Only</span></span>            | <span data-ttu-id="3d10e-229">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-229">False</span></span>                                        |
| <span data-ttu-id="3d10e-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d10e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="3d10e-231">對</span><span class="sxs-lookup"><span data-stu-id="3d10e-231">True</span></span>                                         |
| <span data-ttu-id="3d10e-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d10e-232">Is Indexed</span></span>             | <span data-ttu-id="3d10e-233">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-233">False</span></span>                                        |
| <span data-ttu-id="3d10e-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d10e-234">In Global Catalog</span></span>      | <span data-ttu-id="3d10e-235">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-235">False</span></span>                                        |
| <span data-ttu-id="3d10e-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d10e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d10e-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d10e-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d10e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d10e-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d10e-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-240">Search-Flags</span></span>           | <span data-ttu-id="3d10e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d10e-241">0x00000000</span></span>                                   |
| <span data-ttu-id="3d10e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-242">System-Flags</span></span>           | <span data-ttu-id="3d10e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d10e-243">0x00000010</span></span>                                   |
| <span data-ttu-id="3d10e-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d10e-244">Classes used in</span></span>        | [<span data-ttu-id="3d10e-245">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="3d10e-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d10e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d10e-246">Windows Server 2012</span></span>



| <span data-ttu-id="3d10e-247">進入</span><span class="sxs-lookup"><span data-stu-id="3d10e-247">Entry</span></span> | <span data-ttu-id="3d10e-248">值</span><span class="sxs-lookup"><span data-stu-id="3d10e-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3d10e-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d10e-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d10e-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3d10e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d10e-251">System-Only</span></span>            | <span data-ttu-id="3d10e-252">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-252">False</span></span>                                        |
| <span data-ttu-id="3d10e-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d10e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="3d10e-254">對</span><span class="sxs-lookup"><span data-stu-id="3d10e-254">True</span></span>                                         |
| <span data-ttu-id="3d10e-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d10e-255">Is Indexed</span></span>             | <span data-ttu-id="3d10e-256">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-256">False</span></span>                                        |
| <span data-ttu-id="3d10e-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d10e-257">In Global Catalog</span></span>      | <span data-ttu-id="3d10e-258">否</span><span class="sxs-lookup"><span data-stu-id="3d10e-258">False</span></span>                                        |
| <span data-ttu-id="3d10e-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d10e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d10e-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d10e-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3d10e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d10e-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d10e-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3d10e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-263">Search-Flags</span></span>           | <span data-ttu-id="3d10e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d10e-264">0x00000000</span></span>                                   |
| <span data-ttu-id="3d10e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d10e-265">System-Flags</span></span>           | <span data-ttu-id="3d10e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d10e-266">0x00000010</span></span>                                   |
| <span data-ttu-id="3d10e-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d10e-267">Classes used in</span></span>        | [<span data-ttu-id="3d10e-268">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="3d10e-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






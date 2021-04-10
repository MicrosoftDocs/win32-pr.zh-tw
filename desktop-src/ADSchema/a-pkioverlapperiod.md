---
title: PKI-重迭-期間屬性
description: 憑證到期前的更新時間。
ms.assetid: 394c78b2-7476-4c2d-9a95-f781c779ea4d
ms.tgt_platform: multiple
keywords:
- PKI-重迭-期間屬性 AD 架構
- pKIOverlapPeriod 屬性 AD 架構
topic_type:
- apiref
api_name:
- PKI-Overlap-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad34a30086c4a6de8f96ae18e99c2f8a71682ef
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844960"
---
# <a name="pki-overlap-period-attribute"></a><span data-ttu-id="2a591-105">PKI-重迭-期間屬性</span><span class="sxs-lookup"><span data-stu-id="2a591-105">PKI-Overlap-Period attribute</span></span>

<span data-ttu-id="2a591-106">憑證到期前的更新時間。</span><span class="sxs-lookup"><span data-stu-id="2a591-106">The period by when the certificate should be renewed before it is expired.</span></span>



| <span data-ttu-id="2a591-107">進入</span><span class="sxs-lookup"><span data-stu-id="2a591-107">Entry</span></span> | <span data-ttu-id="2a591-108">值</span><span class="sxs-lookup"><span data-stu-id="2a591-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2a591-109">CN</span><span class="sxs-lookup"><span data-stu-id="2a591-109">CN</span></span>                | <span data-ttu-id="2a591-110">PKI-重迭-期間</span><span class="sxs-lookup"><span data-stu-id="2a591-110">PKI-Overlap-Period</span></span>                                    |
| <span data-ttu-id="2a591-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2a591-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2a591-112">pKIOverlapPeriod</span><span class="sxs-lookup"><span data-stu-id="2a591-112">pKIOverlapPeriod</span></span>                                      |
| <span data-ttu-id="2a591-113">大小</span><span class="sxs-lookup"><span data-stu-id="2a591-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="2a591-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2a591-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="2a591-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2a591-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="2a591-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2a591-116">Attribute-Id</span></span>      | <span data-ttu-id="2a591-117">1.2.840.113556.1.4.1332</span><span class="sxs-lookup"><span data-stu-id="2a591-117">1.2.840.113556.1.4.1332</span></span>                               |
| <span data-ttu-id="2a591-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2a591-118">System-Id-Guid</span></span>    | <span data-ttu-id="2a591-119">1219a3ec-3b9e-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="2a591-119">1219a3ec-3b9e-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="2a591-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a591-120">Syntax</span></span>            | [<span data-ttu-id="2a591-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="2a591-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="2a591-122">實作</span><span class="sxs-lookup"><span data-stu-id="2a591-122">Implementations</span></span>

-   [<span data-ttu-id="2a591-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2a591-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2a591-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2a591-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2a591-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2a591-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2a591-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2a591-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2a591-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2a591-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2a591-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2a591-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2a591-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a591-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2a591-130">進入</span><span class="sxs-lookup"><span data-stu-id="2a591-130">Entry</span></span> | <span data-ttu-id="2a591-131">值</span><span class="sxs-lookup"><span data-stu-id="2a591-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2a591-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a591-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a591-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a591-134">System-Only</span></span>            | <span data-ttu-id="2a591-135">否</span><span class="sxs-lookup"><span data-stu-id="2a591-135">False</span></span>                                                                   |
| <span data-ttu-id="2a591-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a591-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2a591-137">對</span><span class="sxs-lookup"><span data-stu-id="2a591-137">True</span></span>                                                                    |
| <span data-ttu-id="2a591-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a591-138">Is Indexed</span></span>             | <span data-ttu-id="2a591-139">否</span><span class="sxs-lookup"><span data-stu-id="2a591-139">False</span></span>                                                                   |
| <span data-ttu-id="2a591-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a591-140">In Global Catalog</span></span>      | <span data-ttu-id="2a591-141">對</span><span class="sxs-lookup"><span data-stu-id="2a591-141">True</span></span>                                                                    |
| <span data-ttu-id="2a591-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a591-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a591-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a591-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2a591-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a591-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a591-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-146">Search-Flags</span></span>           | <span data-ttu-id="2a591-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a591-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="2a591-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-148">System-Flags</span></span>           | <span data-ttu-id="2a591-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a591-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="2a591-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a591-150">Classes used in</span></span>        | [<span data-ttu-id="2a591-151">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2a591-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2a591-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a591-152">Windows Server 2003</span></span>



| <span data-ttu-id="2a591-153">進入</span><span class="sxs-lookup"><span data-stu-id="2a591-153">Entry</span></span> | <span data-ttu-id="2a591-154">值</span><span class="sxs-lookup"><span data-stu-id="2a591-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2a591-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a591-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a591-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a591-157">System-Only</span></span>            | <span data-ttu-id="2a591-158">否</span><span class="sxs-lookup"><span data-stu-id="2a591-158">False</span></span>                                                                   |
| <span data-ttu-id="2a591-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a591-159">Is-Single-Valued</span></span>       | <span data-ttu-id="2a591-160">對</span><span class="sxs-lookup"><span data-stu-id="2a591-160">True</span></span>                                                                    |
| <span data-ttu-id="2a591-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a591-161">Is Indexed</span></span>             | <span data-ttu-id="2a591-162">否</span><span class="sxs-lookup"><span data-stu-id="2a591-162">False</span></span>                                                                   |
| <span data-ttu-id="2a591-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a591-163">In Global Catalog</span></span>      | <span data-ttu-id="2a591-164">對</span><span class="sxs-lookup"><span data-stu-id="2a591-164">True</span></span>                                                                    |
| <span data-ttu-id="2a591-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a591-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a591-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a591-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2a591-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a591-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a591-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-169">Search-Flags</span></span>           | <span data-ttu-id="2a591-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a591-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="2a591-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-171">System-Flags</span></span>           | <span data-ttu-id="2a591-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a591-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="2a591-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a591-173">Classes used in</span></span>        | [<span data-ttu-id="2a591-174">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2a591-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2a591-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2a591-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2a591-176">進入</span><span class="sxs-lookup"><span data-stu-id="2a591-176">Entry</span></span> | <span data-ttu-id="2a591-177">值</span><span class="sxs-lookup"><span data-stu-id="2a591-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2a591-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a591-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a591-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a591-180">System-Only</span></span>            | <span data-ttu-id="2a591-181">否</span><span class="sxs-lookup"><span data-stu-id="2a591-181">False</span></span>                                                                   |
| <span data-ttu-id="2a591-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a591-182">Is-Single-Valued</span></span>       | <span data-ttu-id="2a591-183">對</span><span class="sxs-lookup"><span data-stu-id="2a591-183">True</span></span>                                                                    |
| <span data-ttu-id="2a591-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a591-184">Is Indexed</span></span>             | <span data-ttu-id="2a591-185">否</span><span class="sxs-lookup"><span data-stu-id="2a591-185">False</span></span>                                                                   |
| <span data-ttu-id="2a591-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a591-186">In Global Catalog</span></span>      | <span data-ttu-id="2a591-187">對</span><span class="sxs-lookup"><span data-stu-id="2a591-187">True</span></span>                                                                    |
| <span data-ttu-id="2a591-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a591-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a591-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a591-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2a591-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a591-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a591-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-192">Search-Flags</span></span>           | <span data-ttu-id="2a591-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a591-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="2a591-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-194">System-Flags</span></span>           | <span data-ttu-id="2a591-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a591-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="2a591-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a591-196">Classes used in</span></span>        | [<span data-ttu-id="2a591-197">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2a591-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2a591-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a591-198">Windows Server 2008</span></span>



| <span data-ttu-id="2a591-199">進入</span><span class="sxs-lookup"><span data-stu-id="2a591-199">Entry</span></span> | <span data-ttu-id="2a591-200">值</span><span class="sxs-lookup"><span data-stu-id="2a591-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2a591-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a591-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a591-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a591-203">System-Only</span></span>            | <span data-ttu-id="2a591-204">否</span><span class="sxs-lookup"><span data-stu-id="2a591-204">False</span></span>                                                                   |
| <span data-ttu-id="2a591-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a591-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2a591-206">對</span><span class="sxs-lookup"><span data-stu-id="2a591-206">True</span></span>                                                                    |
| <span data-ttu-id="2a591-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a591-207">Is Indexed</span></span>             | <span data-ttu-id="2a591-208">否</span><span class="sxs-lookup"><span data-stu-id="2a591-208">False</span></span>                                                                   |
| <span data-ttu-id="2a591-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a591-209">In Global Catalog</span></span>      | <span data-ttu-id="2a591-210">對</span><span class="sxs-lookup"><span data-stu-id="2a591-210">True</span></span>                                                                    |
| <span data-ttu-id="2a591-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a591-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a591-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a591-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2a591-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a591-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a591-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-215">Search-Flags</span></span>           | <span data-ttu-id="2a591-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a591-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="2a591-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-217">System-Flags</span></span>           | <span data-ttu-id="2a591-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a591-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="2a591-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a591-219">Classes used in</span></span>        | [<span data-ttu-id="2a591-220">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2a591-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2a591-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a591-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2a591-222">進入</span><span class="sxs-lookup"><span data-stu-id="2a591-222">Entry</span></span> | <span data-ttu-id="2a591-223">值</span><span class="sxs-lookup"><span data-stu-id="2a591-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2a591-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a591-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a591-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a591-226">System-Only</span></span>            | <span data-ttu-id="2a591-227">否</span><span class="sxs-lookup"><span data-stu-id="2a591-227">False</span></span>                                                                   |
| <span data-ttu-id="2a591-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a591-228">Is-Single-Valued</span></span>       | <span data-ttu-id="2a591-229">對</span><span class="sxs-lookup"><span data-stu-id="2a591-229">True</span></span>                                                                    |
| <span data-ttu-id="2a591-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a591-230">Is Indexed</span></span>             | <span data-ttu-id="2a591-231">否</span><span class="sxs-lookup"><span data-stu-id="2a591-231">False</span></span>                                                                   |
| <span data-ttu-id="2a591-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a591-232">In Global Catalog</span></span>      | <span data-ttu-id="2a591-233">對</span><span class="sxs-lookup"><span data-stu-id="2a591-233">True</span></span>                                                                    |
| <span data-ttu-id="2a591-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a591-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a591-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a591-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2a591-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a591-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a591-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-238">Search-Flags</span></span>           | <span data-ttu-id="2a591-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a591-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="2a591-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-240">System-Flags</span></span>           | <span data-ttu-id="2a591-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a591-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="2a591-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a591-242">Classes used in</span></span>        | [<span data-ttu-id="2a591-243">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2a591-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2a591-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a591-244">Windows Server 2012</span></span>



| <span data-ttu-id="2a591-245">進入</span><span class="sxs-lookup"><span data-stu-id="2a591-245">Entry</span></span> | <span data-ttu-id="2a591-246">值</span><span class="sxs-lookup"><span data-stu-id="2a591-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2a591-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2a591-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2a591-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="2a591-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="2a591-249">System-Only</span></span>            | <span data-ttu-id="2a591-250">否</span><span class="sxs-lookup"><span data-stu-id="2a591-250">False</span></span>                                                                   |
| <span data-ttu-id="2a591-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2a591-251">Is-Single-Valued</span></span>       | <span data-ttu-id="2a591-252">對</span><span class="sxs-lookup"><span data-stu-id="2a591-252">True</span></span>                                                                    |
| <span data-ttu-id="2a591-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2a591-253">Is Indexed</span></span>             | <span data-ttu-id="2a591-254">否</span><span class="sxs-lookup"><span data-stu-id="2a591-254">False</span></span>                                                                   |
| <span data-ttu-id="2a591-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2a591-255">In Global Catalog</span></span>      | <span data-ttu-id="2a591-256">對</span><span class="sxs-lookup"><span data-stu-id="2a591-256">True</span></span>                                                                    |
| <span data-ttu-id="2a591-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2a591-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="2a591-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2a591-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="2a591-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2a591-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2a591-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="2a591-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-261">Search-Flags</span></span>           | <span data-ttu-id="2a591-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a591-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="2a591-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2a591-263">System-Flags</span></span>           | <span data-ttu-id="2a591-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a591-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="2a591-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2a591-265">Classes used in</span></span>        | [<span data-ttu-id="2a591-266">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="2a591-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






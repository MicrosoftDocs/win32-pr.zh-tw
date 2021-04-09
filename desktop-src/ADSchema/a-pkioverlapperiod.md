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
# <a name="pki-overlap-period-attribute"></a><span data-ttu-id="b3c4f-105">PKI-重迭-期間屬性</span><span class="sxs-lookup"><span data-stu-id="b3c4f-105">PKI-Overlap-Period attribute</span></span>

<span data-ttu-id="b3c4f-106">憑證到期前的更新時間。</span><span class="sxs-lookup"><span data-stu-id="b3c4f-106">The period by when the certificate should be renewed before it is expired.</span></span>



| <span data-ttu-id="b3c4f-107">進入</span><span class="sxs-lookup"><span data-stu-id="b3c4f-107">Entry</span></span> | <span data-ttu-id="b3c4f-108">值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b3c4f-109">CN</span><span class="sxs-lookup"><span data-stu-id="b3c4f-109">CN</span></span>                | <span data-ttu-id="b3c4f-110">PKI-重迭-期間</span><span class="sxs-lookup"><span data-stu-id="b3c4f-110">PKI-Overlap-Period</span></span>                                    |
| <span data-ttu-id="b3c4f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b3c4f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b3c4f-112">pKIOverlapPeriod</span><span class="sxs-lookup"><span data-stu-id="b3c4f-112">pKIOverlapPeriod</span></span>                                      |
| <span data-ttu-id="b3c4f-113">大小</span><span class="sxs-lookup"><span data-stu-id="b3c4f-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b3c4f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b3c4f-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="b3c4f-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b3c4f-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b3c4f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b3c4f-116">Attribute-Id</span></span>      | <span data-ttu-id="b3c4f-117">1.2.840.113556.1.4.1332</span><span class="sxs-lookup"><span data-stu-id="b3c4f-117">1.2.840.113556.1.4.1332</span></span>                               |
| <span data-ttu-id="b3c4f-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b3c4f-118">System-Id-Guid</span></span>    | <span data-ttu-id="b3c4f-119">1219a3ec-3b9e-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="b3c4f-119">1219a3ec-3b9e-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="b3c4f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3c4f-120">Syntax</span></span>            | [<span data-ttu-id="b3c4f-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b3c4f-122">實作</span><span class="sxs-lookup"><span data-stu-id="b3c4f-122">Implementations</span></span>

-   [<span data-ttu-id="b3c4f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b3c4f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b3c4f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b3c4f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b3c4f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b3c4f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b3c4f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3c4f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b3c4f-130">進入</span><span class="sxs-lookup"><span data-stu-id="b3c4f-130">Entry</span></span> | <span data-ttu-id="b3c4f-131">值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b3c4f-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3c4f-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3c4f-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3c4f-134">System-Only</span></span>            | <span data-ttu-id="b3c4f-135">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-135">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b3c4f-137">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-137">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3c4f-138">Is Indexed</span></span>             | <span data-ttu-id="b3c4f-139">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-139">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3c4f-140">In Global Catalog</span></span>      | <span data-ttu-id="b3c4f-141">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-141">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3c4f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3c4f-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3c4f-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b3c4f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3c4f-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3c4f-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-146">Search-Flags</span></span>           | <span data-ttu-id="b3c4f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3c4f-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="b3c4f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-148">System-Flags</span></span>           | <span data-ttu-id="b3c4f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3c4f-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="b3c4f-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3c4f-150">Classes used in</span></span>        | [<span data-ttu-id="b3c4f-151">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b3c4f-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b3c4f-152">Windows Server 2003</span></span>



| <span data-ttu-id="b3c4f-153">進入</span><span class="sxs-lookup"><span data-stu-id="b3c4f-153">Entry</span></span> | <span data-ttu-id="b3c4f-154">值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b3c4f-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3c4f-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3c4f-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3c4f-157">System-Only</span></span>            | <span data-ttu-id="b3c4f-158">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-158">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="b3c4f-160">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-160">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3c4f-161">Is Indexed</span></span>             | <span data-ttu-id="b3c4f-162">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-162">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3c4f-163">In Global Catalog</span></span>      | <span data-ttu-id="b3c4f-164">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-164">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3c4f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3c4f-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3c4f-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b3c4f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3c4f-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3c4f-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-169">Search-Flags</span></span>           | <span data-ttu-id="b3c4f-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3c4f-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="b3c4f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-171">System-Flags</span></span>           | <span data-ttu-id="b3c4f-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3c4f-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="b3c4f-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3c4f-173">Classes used in</span></span>        | [<span data-ttu-id="b3c4f-174">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b3c4f-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b3c4f-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b3c4f-176">進入</span><span class="sxs-lookup"><span data-stu-id="b3c4f-176">Entry</span></span> | <span data-ttu-id="b3c4f-177">值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b3c4f-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3c4f-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3c4f-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3c4f-180">System-Only</span></span>            | <span data-ttu-id="b3c4f-181">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-181">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-182">Is-Single-Valued</span></span>       | <span data-ttu-id="b3c4f-183">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-183">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3c4f-184">Is Indexed</span></span>             | <span data-ttu-id="b3c4f-185">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-185">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3c4f-186">In Global Catalog</span></span>      | <span data-ttu-id="b3c4f-187">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-187">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3c4f-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3c4f-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3c4f-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b3c4f-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3c4f-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3c4f-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-192">Search-Flags</span></span>           | <span data-ttu-id="b3c4f-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3c4f-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="b3c4f-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-194">System-Flags</span></span>           | <span data-ttu-id="b3c4f-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3c4f-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="b3c4f-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3c4f-196">Classes used in</span></span>        | [<span data-ttu-id="b3c4f-197">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b3c4f-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3c4f-198">Windows Server 2008</span></span>



| <span data-ttu-id="b3c4f-199">進入</span><span class="sxs-lookup"><span data-stu-id="b3c4f-199">Entry</span></span> | <span data-ttu-id="b3c4f-200">值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b3c4f-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3c4f-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3c4f-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3c4f-203">System-Only</span></span>            | <span data-ttu-id="b3c4f-204">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-204">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-205">Is-Single-Valued</span></span>       | <span data-ttu-id="b3c4f-206">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-206">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3c4f-207">Is Indexed</span></span>             | <span data-ttu-id="b3c4f-208">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-208">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3c4f-209">In Global Catalog</span></span>      | <span data-ttu-id="b3c4f-210">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-210">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3c4f-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3c4f-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3c4f-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b3c4f-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3c4f-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3c4f-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-215">Search-Flags</span></span>           | <span data-ttu-id="b3c4f-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3c4f-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="b3c4f-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-217">System-Flags</span></span>           | <span data-ttu-id="b3c4f-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3c4f-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="b3c4f-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3c4f-219">Classes used in</span></span>        | [<span data-ttu-id="b3c4f-220">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b3c4f-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3c4f-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b3c4f-222">進入</span><span class="sxs-lookup"><span data-stu-id="b3c4f-222">Entry</span></span> | <span data-ttu-id="b3c4f-223">值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b3c4f-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3c4f-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3c4f-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3c4f-226">System-Only</span></span>            | <span data-ttu-id="b3c4f-227">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-227">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-228">Is-Single-Valued</span></span>       | <span data-ttu-id="b3c4f-229">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-229">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3c4f-230">Is Indexed</span></span>             | <span data-ttu-id="b3c4f-231">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-231">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3c4f-232">In Global Catalog</span></span>      | <span data-ttu-id="b3c4f-233">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-233">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3c4f-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3c4f-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3c4f-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b3c4f-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3c4f-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3c4f-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-238">Search-Flags</span></span>           | <span data-ttu-id="b3c4f-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3c4f-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="b3c4f-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-240">System-Flags</span></span>           | <span data-ttu-id="b3c4f-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3c4f-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="b3c4f-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3c4f-242">Classes used in</span></span>        | [<span data-ttu-id="b3c4f-243">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b3c4f-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3c4f-244">Windows Server 2012</span></span>



| <span data-ttu-id="b3c4f-245">進入</span><span class="sxs-lookup"><span data-stu-id="b3c4f-245">Entry</span></span> | <span data-ttu-id="b3c4f-246">值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b3c4f-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3c4f-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3c4f-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b3c4f-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3c4f-249">System-Only</span></span>            | <span data-ttu-id="b3c4f-250">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-250">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3c4f-251">Is-Single-Valued</span></span>       | <span data-ttu-id="b3c4f-252">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-252">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3c4f-253">Is Indexed</span></span>             | <span data-ttu-id="b3c4f-254">否</span><span class="sxs-lookup"><span data-stu-id="b3c4f-254">False</span></span>                                                                   |
| <span data-ttu-id="b3c4f-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3c4f-255">In Global Catalog</span></span>      | <span data-ttu-id="b3c4f-256">對</span><span class="sxs-lookup"><span data-stu-id="b3c4f-256">True</span></span>                                                                    |
| <span data-ttu-id="b3c4f-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3c4f-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3c4f-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3c4f-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b3c4f-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3c4f-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3c4f-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b3c4f-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-261">Search-Flags</span></span>           | <span data-ttu-id="b3c4f-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3c4f-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="b3c4f-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3c4f-263">System-Flags</span></span>           | <span data-ttu-id="b3c4f-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3c4f-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="b3c4f-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3c4f-265">Classes used in</span></span>        | [<span data-ttu-id="b3c4f-266">**PKI-憑證-範本**</span><span class="sxs-lookup"><span data-stu-id="b3c4f-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






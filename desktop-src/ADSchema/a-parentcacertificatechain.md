---
title: 父系 CA-憑證鏈屬性
description: 父憑證授權單位單位的 DER 編碼 x.509v3 憑證。
ms.assetid: 37e04c7b-5350-4e48-b3fd-22f97959d26a
ms.tgt_platform: multiple
keywords:
- 父系-CA-憑證鏈屬性 AD 架構
- parentCACertificateChain 屬性 AD 架構
topic_type:
- apiref
api_name:
- Parent-CA-Certificate-Chain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f27bacb77fb7ab3f1ae712920dace7cb525efc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467254"
---
# <a name="parent-ca-certificate-chain-attribute"></a><span data-ttu-id="bd0fe-105">父系 CA-憑證鏈屬性</span><span class="sxs-lookup"><span data-stu-id="bd0fe-105">Parent-CA-Certificate-Chain attribute</span></span>

<span data-ttu-id="bd0fe-106">父憑證授權單位單位的 DER 編碼 x.509v3 憑證。</span><span class="sxs-lookup"><span data-stu-id="bd0fe-106">DER-encoded X.509v3 certificate for the parent certification authority.</span></span>



| <span data-ttu-id="bd0fe-107">進入</span><span class="sxs-lookup"><span data-stu-id="bd0fe-107">Entry</span></span> | <span data-ttu-id="bd0fe-108">值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="bd0fe-109">CN</span><span class="sxs-lookup"><span data-stu-id="bd0fe-109">CN</span></span>                | <span data-ttu-id="bd0fe-110">上層 CA-憑證鏈</span><span class="sxs-lookup"><span data-stu-id="bd0fe-110">Parent-CA-Certificate-Chain</span></span>                           |
| <span data-ttu-id="bd0fe-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bd0fe-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bd0fe-112">parentCACertificateChain</span><span class="sxs-lookup"><span data-stu-id="bd0fe-112">parentCACertificateChain</span></span>                              |
| <span data-ttu-id="bd0fe-113">大小</span><span class="sxs-lookup"><span data-stu-id="bd0fe-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="bd0fe-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="bd0fe-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="bd0fe-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="bd0fe-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="bd0fe-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bd0fe-116">Attribute-Id</span></span>      | <span data-ttu-id="bd0fe-117">1.2.840.113556.1.4.685</span><span class="sxs-lookup"><span data-stu-id="bd0fe-117">1.2.840.113556.1.4.685</span></span>                                |
| <span data-ttu-id="bd0fe-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="bd0fe-118">System-Id-Guid</span></span>    | <span data-ttu-id="bd0fe-119">963d2733-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="bd0fe-119">963d2733-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="bd0fe-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd0fe-120">Syntax</span></span>            | [<span data-ttu-id="bd0fe-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="bd0fe-122">實作</span><span class="sxs-lookup"><span data-stu-id="bd0fe-122">Implementations</span></span>

-   [<span data-ttu-id="bd0fe-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bd0fe-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bd0fe-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bd0fe-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bd0fe-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bd0fe-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bd0fe-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bd0fe-129">Windows 2000 Server</span></span>



| <span data-ttu-id="bd0fe-130">進入</span><span class="sxs-lookup"><span data-stu-id="bd0fe-130">Entry</span></span> | <span data-ttu-id="bd0fe-131">值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="bd0fe-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd0fe-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd0fe-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd0fe-134">System-Only</span></span>            | <span data-ttu-id="bd0fe-135">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-135">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-136">Is-Single-Valued</span></span>       | <span data-ttu-id="bd0fe-137">對</span><span class="sxs-lookup"><span data-stu-id="bd0fe-137">True</span></span>                                                                   |
| <span data-ttu-id="bd0fe-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd0fe-138">Is Indexed</span></span>             | <span data-ttu-id="bd0fe-139">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-139">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd0fe-140">In Global Catalog</span></span>      | <span data-ttu-id="bd0fe-141">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-141">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd0fe-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd0fe-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd0fe-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="bd0fe-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd0fe-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd0fe-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-146">Search-Flags</span></span>           | <span data-ttu-id="bd0fe-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd0fe-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="bd0fe-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-148">System-Flags</span></span>           | <span data-ttu-id="bd0fe-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd0fe-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="bd0fe-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd0fe-150">Classes used in</span></span>        | [<span data-ttu-id="bd0fe-151">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bd0fe-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bd0fe-152">Windows Server 2003</span></span>



| <span data-ttu-id="bd0fe-153">進入</span><span class="sxs-lookup"><span data-stu-id="bd0fe-153">Entry</span></span> | <span data-ttu-id="bd0fe-154">值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="bd0fe-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd0fe-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd0fe-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd0fe-157">System-Only</span></span>            | <span data-ttu-id="bd0fe-158">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-158">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-159">Is-Single-Valued</span></span>       | <span data-ttu-id="bd0fe-160">對</span><span class="sxs-lookup"><span data-stu-id="bd0fe-160">True</span></span>                                                                   |
| <span data-ttu-id="bd0fe-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd0fe-161">Is Indexed</span></span>             | <span data-ttu-id="bd0fe-162">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-162">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd0fe-163">In Global Catalog</span></span>      | <span data-ttu-id="bd0fe-164">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-164">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd0fe-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd0fe-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd0fe-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="bd0fe-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd0fe-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd0fe-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-169">Search-Flags</span></span>           | <span data-ttu-id="bd0fe-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd0fe-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="bd0fe-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-171">System-Flags</span></span>           | <span data-ttu-id="bd0fe-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd0fe-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="bd0fe-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd0fe-173">Classes used in</span></span>        | [<span data-ttu-id="bd0fe-174">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bd0fe-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bd0fe-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bd0fe-176">進入</span><span class="sxs-lookup"><span data-stu-id="bd0fe-176">Entry</span></span> | <span data-ttu-id="bd0fe-177">值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="bd0fe-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd0fe-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd0fe-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd0fe-180">System-Only</span></span>            | <span data-ttu-id="bd0fe-181">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-181">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-182">Is-Single-Valued</span></span>       | <span data-ttu-id="bd0fe-183">對</span><span class="sxs-lookup"><span data-stu-id="bd0fe-183">True</span></span>                                                                   |
| <span data-ttu-id="bd0fe-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd0fe-184">Is Indexed</span></span>             | <span data-ttu-id="bd0fe-185">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-185">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd0fe-186">In Global Catalog</span></span>      | <span data-ttu-id="bd0fe-187">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-187">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd0fe-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd0fe-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd0fe-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="bd0fe-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd0fe-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd0fe-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-192">Search-Flags</span></span>           | <span data-ttu-id="bd0fe-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd0fe-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="bd0fe-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-194">System-Flags</span></span>           | <span data-ttu-id="bd0fe-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd0fe-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="bd0fe-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd0fe-196">Classes used in</span></span>        | [<span data-ttu-id="bd0fe-197">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bd0fe-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd0fe-198">Windows Server 2008</span></span>



| <span data-ttu-id="bd0fe-199">進入</span><span class="sxs-lookup"><span data-stu-id="bd0fe-199">Entry</span></span> | <span data-ttu-id="bd0fe-200">值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="bd0fe-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd0fe-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd0fe-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd0fe-203">System-Only</span></span>            | <span data-ttu-id="bd0fe-204">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-204">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-205">Is-Single-Valued</span></span>       | <span data-ttu-id="bd0fe-206">對</span><span class="sxs-lookup"><span data-stu-id="bd0fe-206">True</span></span>                                                                   |
| <span data-ttu-id="bd0fe-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd0fe-207">Is Indexed</span></span>             | <span data-ttu-id="bd0fe-208">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-208">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd0fe-209">In Global Catalog</span></span>      | <span data-ttu-id="bd0fe-210">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-210">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd0fe-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd0fe-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd0fe-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="bd0fe-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd0fe-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd0fe-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-215">Search-Flags</span></span>           | <span data-ttu-id="bd0fe-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd0fe-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="bd0fe-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-217">System-Flags</span></span>           | <span data-ttu-id="bd0fe-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd0fe-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="bd0fe-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd0fe-219">Classes used in</span></span>        | [<span data-ttu-id="bd0fe-220">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bd0fe-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bd0fe-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bd0fe-222">進入</span><span class="sxs-lookup"><span data-stu-id="bd0fe-222">Entry</span></span> | <span data-ttu-id="bd0fe-223">值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="bd0fe-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd0fe-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd0fe-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd0fe-226">System-Only</span></span>            | <span data-ttu-id="bd0fe-227">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-227">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-228">Is-Single-Valued</span></span>       | <span data-ttu-id="bd0fe-229">對</span><span class="sxs-lookup"><span data-stu-id="bd0fe-229">True</span></span>                                                                   |
| <span data-ttu-id="bd0fe-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd0fe-230">Is Indexed</span></span>             | <span data-ttu-id="bd0fe-231">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-231">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd0fe-232">In Global Catalog</span></span>      | <span data-ttu-id="bd0fe-233">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-233">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd0fe-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd0fe-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd0fe-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="bd0fe-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd0fe-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd0fe-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-238">Search-Flags</span></span>           | <span data-ttu-id="bd0fe-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd0fe-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="bd0fe-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-240">System-Flags</span></span>           | <span data-ttu-id="bd0fe-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd0fe-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="bd0fe-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd0fe-242">Classes used in</span></span>        | [<span data-ttu-id="bd0fe-243">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bd0fe-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bd0fe-244">Windows Server 2012</span></span>



| <span data-ttu-id="bd0fe-245">進入</span><span class="sxs-lookup"><span data-stu-id="bd0fe-245">Entry</span></span> | <span data-ttu-id="bd0fe-246">值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="bd0fe-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd0fe-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd0fe-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="bd0fe-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd0fe-249">System-Only</span></span>            | <span data-ttu-id="bd0fe-250">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-250">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd0fe-251">Is-Single-Valued</span></span>       | <span data-ttu-id="bd0fe-252">對</span><span class="sxs-lookup"><span data-stu-id="bd0fe-252">True</span></span>                                                                   |
| <span data-ttu-id="bd0fe-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd0fe-253">Is Indexed</span></span>             | <span data-ttu-id="bd0fe-254">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-254">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd0fe-255">In Global Catalog</span></span>      | <span data-ttu-id="bd0fe-256">否</span><span class="sxs-lookup"><span data-stu-id="bd0fe-256">False</span></span>                                                                  |
| <span data-ttu-id="bd0fe-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd0fe-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd0fe-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd0fe-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="bd0fe-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd0fe-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd0fe-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="bd0fe-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-261">Search-Flags</span></span>           | <span data-ttu-id="bd0fe-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd0fe-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="bd0fe-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd0fe-263">System-Flags</span></span>           | <span data-ttu-id="bd0fe-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd0fe-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="bd0fe-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd0fe-265">Classes used in</span></span>        | [<span data-ttu-id="bd0fe-266">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="bd0fe-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 






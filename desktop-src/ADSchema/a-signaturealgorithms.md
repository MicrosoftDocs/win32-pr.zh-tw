---
title: Signature-Algorithms 屬性
description: 這個屬性工作表示在驗證過程中，必須用來解碼數位簽章的演算法類型。
ms.assetid: f602a009-6823-42e7-b5e4-fb433535b4cc
ms.tgt_platform: multiple
keywords:
- Signature-Algorithms 屬性 AD 架構
- signatureAlgorithms 屬性 AD 架構
topic_type:
- apiref
api_name:
- Signature-Algorithms
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6487155ed8d13735a8201a41c9d1d5b087bb3711
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104187350"
---
# <a name="signature-algorithms-attribute"></a><span data-ttu-id="fa7f5-105">Signature-Algorithms 屬性</span><span class="sxs-lookup"><span data-stu-id="fa7f5-105">Signature-Algorithms attribute</span></span>

<span data-ttu-id="fa7f5-106">這個屬性工作表示在驗證過程中，必須用來解碼數位簽章的演算法類型。</span><span class="sxs-lookup"><span data-stu-id="fa7f5-106">This attribute indicates the type of algorithm that must be used to decode a digital signature during the authentication process.</span></span>



| <span data-ttu-id="fa7f5-107">進入</span><span class="sxs-lookup"><span data-stu-id="fa7f5-107">Entry</span></span> | <span data-ttu-id="fa7f5-108">值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="fa7f5-109">CN</span><span class="sxs-lookup"><span data-stu-id="fa7f5-109">CN</span></span>                | <span data-ttu-id="fa7f5-110">Signature-Algorithms</span><span class="sxs-lookup"><span data-stu-id="fa7f5-110">Signature-Algorithms</span></span>                        |
| <span data-ttu-id="fa7f5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fa7f5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fa7f5-112">signatureAlgorithms</span><span class="sxs-lookup"><span data-stu-id="fa7f5-112">signatureAlgorithms</span></span>                         |
| <span data-ttu-id="fa7f5-113">大小</span><span class="sxs-lookup"><span data-stu-id="fa7f5-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="fa7f5-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fa7f5-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="fa7f5-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fa7f5-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="fa7f5-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fa7f5-116">Attribute-Id</span></span>      | <span data-ttu-id="fa7f5-117">1.2.840.113556.1.4.824</span><span class="sxs-lookup"><span data-stu-id="fa7f5-117">1.2.840.113556.1.4.824</span></span>                      |
| <span data-ttu-id="fa7f5-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fa7f5-118">System-Id-Guid</span></span>    | <span data-ttu-id="fa7f5-119">2a39c5b2-8960-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="fa7f5-119">2a39c5b2-8960-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="fa7f5-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa7f5-120">Syntax</span></span>            | [<span data-ttu-id="fa7f5-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="fa7f5-122">實作</span><span class="sxs-lookup"><span data-stu-id="fa7f5-122">Implementations</span></span>

-   [<span data-ttu-id="fa7f5-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fa7f5-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fa7f5-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fa7f5-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fa7f5-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fa7f5-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fa7f5-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fa7f5-129">Windows 2000 Server</span></span>



| <span data-ttu-id="fa7f5-130">進入</span><span class="sxs-lookup"><span data-stu-id="fa7f5-130">Entry</span></span> | <span data-ttu-id="fa7f5-131">值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7f5-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa7f5-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa7f5-133">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa7f5-134">System-Only</span></span>            | <span data-ttu-id="fa7f5-135">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-135">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-136">Is-Single-Valued</span></span>       | <span data-ttu-id="fa7f5-137">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-137">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa7f5-138">Is Indexed</span></span>             | <span data-ttu-id="fa7f5-139">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-139">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa7f5-140">In Global Catalog</span></span>      | <span data-ttu-id="fa7f5-141">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-141">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa7f5-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa7f5-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa7f5-143">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="fa7f5-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa7f5-144">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa7f5-145">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-146">Search-Flags</span></span>           | <span data-ttu-id="fa7f5-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa7f5-147">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-148">System-Flags</span></span>           | <span data-ttu-id="fa7f5-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa7f5-149">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa7f5-150">Classes used in</span></span>        | [<span data-ttu-id="fa7f5-151">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="fa7f5-152">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-152">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fa7f5-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa7f5-153">Windows Server 2003</span></span>



| <span data-ttu-id="fa7f5-154">進入</span><span class="sxs-lookup"><span data-stu-id="fa7f5-154">Entry</span></span> | <span data-ttu-id="fa7f5-155">值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7f5-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa7f5-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa7f5-157">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa7f5-158">System-Only</span></span>            | <span data-ttu-id="fa7f5-159">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-159">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-160">Is-Single-Valued</span></span>       | <span data-ttu-id="fa7f5-161">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-161">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa7f5-162">Is Indexed</span></span>             | <span data-ttu-id="fa7f5-163">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa7f5-164">In Global Catalog</span></span>      | <span data-ttu-id="fa7f5-165">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-165">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa7f5-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa7f5-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa7f5-167">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="fa7f5-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa7f5-168">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa7f5-169">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-170">Search-Flags</span></span>           | <span data-ttu-id="fa7f5-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa7f5-171">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-172">System-Flags</span></span>           | <span data-ttu-id="fa7f5-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa7f5-173">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa7f5-174">Classes used in</span></span>        | [<span data-ttu-id="fa7f5-175">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-175">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="fa7f5-176">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-176">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fa7f5-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fa7f5-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fa7f5-178">進入</span><span class="sxs-lookup"><span data-stu-id="fa7f5-178">Entry</span></span> | <span data-ttu-id="fa7f5-179">值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7f5-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa7f5-180">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa7f5-181">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa7f5-182">System-Only</span></span>            | <span data-ttu-id="fa7f5-183">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-183">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fa7f5-185">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-185">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa7f5-186">Is Indexed</span></span>             | <span data-ttu-id="fa7f5-187">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-187">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa7f5-188">In Global Catalog</span></span>      | <span data-ttu-id="fa7f5-189">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-189">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa7f5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa7f5-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa7f5-191">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="fa7f5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa7f5-192">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa7f5-193">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-194">Search-Flags</span></span>           | <span data-ttu-id="fa7f5-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa7f5-195">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-196">System-Flags</span></span>           | <span data-ttu-id="fa7f5-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa7f5-197">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa7f5-198">Classes used in</span></span>        | [<span data-ttu-id="fa7f5-199">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-199">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="fa7f5-200">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-200">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fa7f5-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa7f5-201">Windows Server 2008</span></span>



| <span data-ttu-id="fa7f5-202">進入</span><span class="sxs-lookup"><span data-stu-id="fa7f5-202">Entry</span></span> | <span data-ttu-id="fa7f5-203">值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7f5-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa7f5-204">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa7f5-205">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa7f5-206">System-Only</span></span>            | <span data-ttu-id="fa7f5-207">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-207">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-208">Is-Single-Valued</span></span>       | <span data-ttu-id="fa7f5-209">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-209">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa7f5-210">Is Indexed</span></span>             | <span data-ttu-id="fa7f5-211">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa7f5-212">In Global Catalog</span></span>      | <span data-ttu-id="fa7f5-213">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa7f5-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa7f5-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa7f5-215">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="fa7f5-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa7f5-216">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa7f5-217">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-218">Search-Flags</span></span>           | <span data-ttu-id="fa7f5-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa7f5-219">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-220">System-Flags</span></span>           | <span data-ttu-id="fa7f5-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa7f5-221">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa7f5-222">Classes used in</span></span>        | [<span data-ttu-id="fa7f5-223">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-223">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="fa7f5-224">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-224">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fa7f5-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fa7f5-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fa7f5-226">進入</span><span class="sxs-lookup"><span data-stu-id="fa7f5-226">Entry</span></span> | <span data-ttu-id="fa7f5-227">值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7f5-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa7f5-228">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa7f5-229">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa7f5-230">System-Only</span></span>            | <span data-ttu-id="fa7f5-231">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-231">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-232">Is-Single-Valued</span></span>       | <span data-ttu-id="fa7f5-233">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-233">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa7f5-234">Is Indexed</span></span>             | <span data-ttu-id="fa7f5-235">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-235">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa7f5-236">In Global Catalog</span></span>      | <span data-ttu-id="fa7f5-237">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-237">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa7f5-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa7f5-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa7f5-239">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="fa7f5-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa7f5-240">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa7f5-241">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-242">Search-Flags</span></span>           | <span data-ttu-id="fa7f5-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa7f5-243">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-244">System-Flags</span></span>           | <span data-ttu-id="fa7f5-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa7f5-245">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa7f5-246">Classes used in</span></span>        | [<span data-ttu-id="fa7f5-247">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-247">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="fa7f5-248">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-248">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fa7f5-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa7f5-249">Windows Server 2012</span></span>



| <span data-ttu-id="fa7f5-250">進入</span><span class="sxs-lookup"><span data-stu-id="fa7f5-250">Entry</span></span> | <span data-ttu-id="fa7f5-251">值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7f5-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa7f5-252">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa7f5-253">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa7f5-254">System-Only</span></span>            | <span data-ttu-id="fa7f5-255">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-255">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa7f5-256">Is-Single-Valued</span></span>       | <span data-ttu-id="fa7f5-257">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-257">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa7f5-258">Is Indexed</span></span>             | <span data-ttu-id="fa7f5-259">否</span><span class="sxs-lookup"><span data-stu-id="fa7f5-259">False</span></span>                                                                                                                                      |
| <span data-ttu-id="fa7f5-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa7f5-260">In Global Catalog</span></span>      | <span data-ttu-id="fa7f5-261">對</span><span class="sxs-lookup"><span data-stu-id="fa7f5-261">True</span></span>                                                                                                                                       |
| <span data-ttu-id="fa7f5-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa7f5-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa7f5-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa7f5-263">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="fa7f5-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa7f5-264">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa7f5-265">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="fa7f5-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-266">Search-Flags</span></span>           | <span data-ttu-id="fa7f5-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa7f5-267">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa7f5-268">System-Flags</span></span>           | <span data-ttu-id="fa7f5-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa7f5-269">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="fa7f5-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa7f5-270">Classes used in</span></span>        | [<span data-ttu-id="fa7f5-271">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-271">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="fa7f5-272">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="fa7f5-272">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



 

 






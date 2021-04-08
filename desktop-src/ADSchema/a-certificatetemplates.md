---
title: Certificate-Templates 屬性
description: 包含憑證伺服器所發出之憑證的資訊。
ms.assetid: 1434b8f8-15d9-4dca-bb7b-26c97e269b01
ms.tgt_platform: multiple
keywords:
- Certificate-Templates 屬性 AD 架構
- 右鍵屬性 AD 架構
topic_type:
- apiref
api_name:
- Certificate-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20701d4b904a21af26ac86fdfa90eff13cddf22
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687291"
---
# <a name="certificate-templates-attribute"></a><span data-ttu-id="e51fd-105">Certificate-Templates 屬性</span><span class="sxs-lookup"><span data-stu-id="e51fd-105">Certificate-Templates attribute</span></span>

<span data-ttu-id="e51fd-106">包含憑證伺服器所發出之憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="e51fd-106">Contains information for a certificate issued by a Certificate Server.</span></span>



| <span data-ttu-id="e51fd-107">進入</span><span class="sxs-lookup"><span data-stu-id="e51fd-107">Entry</span></span> | <span data-ttu-id="e51fd-108">值</span><span class="sxs-lookup"><span data-stu-id="e51fd-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e51fd-109">CN</span><span class="sxs-lookup"><span data-stu-id="e51fd-109">CN</span></span>                | <span data-ttu-id="e51fd-110">Certificate-Templates</span><span class="sxs-lookup"><span data-stu-id="e51fd-110">Certificate-Templates</span></span>                       |
| <span data-ttu-id="e51fd-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e51fd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e51fd-112">右鍵</span><span class="sxs-lookup"><span data-stu-id="e51fd-112">certificateTemplates</span></span>                        |
| <span data-ttu-id="e51fd-113">大小</span><span class="sxs-lookup"><span data-stu-id="e51fd-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e51fd-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e51fd-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e51fd-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e51fd-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e51fd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e51fd-116">Attribute-Id</span></span>      | <span data-ttu-id="e51fd-117">1.2.840.113556.1.4.823</span><span class="sxs-lookup"><span data-stu-id="e51fd-117">1.2.840.113556.1.4.823</span></span>                      |
| <span data-ttu-id="e51fd-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e51fd-118">System-Id-Guid</span></span>    | <span data-ttu-id="e51fd-119">2a39c5b1-8960-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e51fd-119">2a39c5b1-8960-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="e51fd-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="e51fd-120">Syntax</span></span>            | [<span data-ttu-id="e51fd-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e51fd-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e51fd-122">實作</span><span class="sxs-lookup"><span data-stu-id="e51fd-122">Implementations</span></span>

-   [<span data-ttu-id="e51fd-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e51fd-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e51fd-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e51fd-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e51fd-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e51fd-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e51fd-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e51fd-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e51fd-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e51fd-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e51fd-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e51fd-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e51fd-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e51fd-129">Windows 2000 Server</span></span>



| <span data-ttu-id="e51fd-130">進入</span><span class="sxs-lookup"><span data-stu-id="e51fd-130">Entry</span></span> | <span data-ttu-id="e51fd-131">值</span><span class="sxs-lookup"><span data-stu-id="e51fd-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51fd-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e51fd-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e51fd-133">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e51fd-134">System-Only</span></span>            | <span data-ttu-id="e51fd-135">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-135">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e51fd-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e51fd-137">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-137">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e51fd-138">Is Indexed</span></span>             | <span data-ttu-id="e51fd-139">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-139">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e51fd-140">In Global Catalog</span></span>      | <span data-ttu-id="e51fd-141">對</span><span class="sxs-lookup"><span data-stu-id="e51fd-141">True</span></span>                                                                                                                                       |
| <span data-ttu-id="e51fd-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e51fd-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e51fd-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e51fd-143">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e51fd-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e51fd-144">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e51fd-145">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-146">Search-Flags</span></span>           | <span data-ttu-id="e51fd-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e51fd-147">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-148">System-Flags</span></span>           | <span data-ttu-id="e51fd-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e51fd-149">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e51fd-150">Classes used in</span></span>        | [<span data-ttu-id="e51fd-151">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="e51fd-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="e51fd-152">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="e51fd-152">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e51fd-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e51fd-153">Windows Server 2003</span></span>



| <span data-ttu-id="e51fd-154">進入</span><span class="sxs-lookup"><span data-stu-id="e51fd-154">Entry</span></span> | <span data-ttu-id="e51fd-155">值</span><span class="sxs-lookup"><span data-stu-id="e51fd-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51fd-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e51fd-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e51fd-157">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e51fd-158">System-Only</span></span>            | <span data-ttu-id="e51fd-159">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-159">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e51fd-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e51fd-161">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e51fd-162">Is Indexed</span></span>             | <span data-ttu-id="e51fd-163">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e51fd-164">In Global Catalog</span></span>      | <span data-ttu-id="e51fd-165">對</span><span class="sxs-lookup"><span data-stu-id="e51fd-165">True</span></span>                                                                                                                                       |
| <span data-ttu-id="e51fd-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e51fd-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e51fd-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e51fd-167">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e51fd-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e51fd-168">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e51fd-169">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-170">Search-Flags</span></span>           | <span data-ttu-id="e51fd-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e51fd-171">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-172">System-Flags</span></span>           | <span data-ttu-id="e51fd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e51fd-173">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e51fd-174">Classes used in</span></span>        | [<span data-ttu-id="e51fd-175">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="e51fd-175">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="e51fd-176">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="e51fd-176">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e51fd-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e51fd-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e51fd-178">進入</span><span class="sxs-lookup"><span data-stu-id="e51fd-178">Entry</span></span> | <span data-ttu-id="e51fd-179">值</span><span class="sxs-lookup"><span data-stu-id="e51fd-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51fd-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e51fd-180">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e51fd-181">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e51fd-182">System-Only</span></span>            | <span data-ttu-id="e51fd-183">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-183">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e51fd-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e51fd-185">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-185">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e51fd-186">Is Indexed</span></span>             | <span data-ttu-id="e51fd-187">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-187">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e51fd-188">In Global Catalog</span></span>      | <span data-ttu-id="e51fd-189">對</span><span class="sxs-lookup"><span data-stu-id="e51fd-189">True</span></span>                                                                                                                                       |
| <span data-ttu-id="e51fd-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e51fd-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e51fd-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e51fd-191">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e51fd-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e51fd-192">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e51fd-193">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-194">Search-Flags</span></span>           | <span data-ttu-id="e51fd-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e51fd-195">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-196">System-Flags</span></span>           | <span data-ttu-id="e51fd-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e51fd-197">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e51fd-198">Classes used in</span></span>        | [<span data-ttu-id="e51fd-199">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="e51fd-199">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="e51fd-200">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="e51fd-200">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e51fd-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e51fd-201">Windows Server 2008</span></span>



| <span data-ttu-id="e51fd-202">進入</span><span class="sxs-lookup"><span data-stu-id="e51fd-202">Entry</span></span> | <span data-ttu-id="e51fd-203">值</span><span class="sxs-lookup"><span data-stu-id="e51fd-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51fd-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e51fd-204">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e51fd-205">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e51fd-206">System-Only</span></span>            | <span data-ttu-id="e51fd-207">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-207">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e51fd-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e51fd-209">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-209">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e51fd-210">Is Indexed</span></span>             | <span data-ttu-id="e51fd-211">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e51fd-212">In Global Catalog</span></span>      | <span data-ttu-id="e51fd-213">對</span><span class="sxs-lookup"><span data-stu-id="e51fd-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="e51fd-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e51fd-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e51fd-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e51fd-215">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e51fd-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e51fd-216">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e51fd-217">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-218">Search-Flags</span></span>           | <span data-ttu-id="e51fd-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e51fd-219">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-220">System-Flags</span></span>           | <span data-ttu-id="e51fd-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e51fd-221">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e51fd-222">Classes used in</span></span>        | [<span data-ttu-id="e51fd-223">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="e51fd-223">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="e51fd-224">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="e51fd-224">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e51fd-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e51fd-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e51fd-226">進入</span><span class="sxs-lookup"><span data-stu-id="e51fd-226">Entry</span></span> | <span data-ttu-id="e51fd-227">值</span><span class="sxs-lookup"><span data-stu-id="e51fd-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51fd-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e51fd-228">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e51fd-229">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="e51fd-230">System-Only</span></span>            | <span data-ttu-id="e51fd-231">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-231">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e51fd-232">Is-Single-Valued</span></span>       | <span data-ttu-id="e51fd-233">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-233">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e51fd-234">Is Indexed</span></span>             | <span data-ttu-id="e51fd-235">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-235">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e51fd-236">In Global Catalog</span></span>      | <span data-ttu-id="e51fd-237">對</span><span class="sxs-lookup"><span data-stu-id="e51fd-237">True</span></span>                                                                                                                                       |
| <span data-ttu-id="e51fd-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e51fd-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="e51fd-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e51fd-239">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e51fd-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e51fd-240">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e51fd-241">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-242">Search-Flags</span></span>           | <span data-ttu-id="e51fd-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e51fd-243">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-244">System-Flags</span></span>           | <span data-ttu-id="e51fd-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e51fd-245">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e51fd-246">Classes used in</span></span>        | [<span data-ttu-id="e51fd-247">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="e51fd-247">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="e51fd-248">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="e51fd-248">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e51fd-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e51fd-249">Windows Server 2012</span></span>



| <span data-ttu-id="e51fd-250">進入</span><span class="sxs-lookup"><span data-stu-id="e51fd-250">Entry</span></span> | <span data-ttu-id="e51fd-251">值</span><span class="sxs-lookup"><span data-stu-id="e51fd-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51fd-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e51fd-252">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e51fd-253">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="e51fd-254">System-Only</span></span>            | <span data-ttu-id="e51fd-255">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-255">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e51fd-256">Is-Single-Valued</span></span>       | <span data-ttu-id="e51fd-257">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-257">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e51fd-258">Is Indexed</span></span>             | <span data-ttu-id="e51fd-259">否</span><span class="sxs-lookup"><span data-stu-id="e51fd-259">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e51fd-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e51fd-260">In Global Catalog</span></span>      | <span data-ttu-id="e51fd-261">對</span><span class="sxs-lookup"><span data-stu-id="e51fd-261">True</span></span>                                                                                                                                       |
| <span data-ttu-id="e51fd-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e51fd-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="e51fd-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e51fd-263">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e51fd-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e51fd-264">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e51fd-265">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e51fd-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-266">Search-Flags</span></span>           | <span data-ttu-id="e51fd-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e51fd-267">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e51fd-268">System-Flags</span></span>           | <span data-ttu-id="e51fd-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e51fd-269">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="e51fd-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e51fd-270">Classes used in</span></span>        | [<span data-ttu-id="e51fd-271">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="e51fd-271">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="e51fd-272">**PKI-註冊-服務**</span><span class="sxs-lookup"><span data-stu-id="e51fd-272">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



 

 






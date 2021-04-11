---
title: UPN-Suffixes 屬性
description: 網域的使用者主體名稱尾碼清單。
ms.assetid: ad861d2d-b643-468c-a346-36ad6a828359
ms.tgt_platform: multiple
keywords:
- UPN-Suffixes 屬性 AD 架構
- uPNSuffixes 屬性 AD 架構
topic_type:
- apiref
api_name:
- UPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4aa5fb9398478e4b91fb8f36b8cf96a244935fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845271"
---
# <a name="upn-suffixes-attribute"></a><span data-ttu-id="80f0e-105">UPN-Suffixes 屬性</span><span class="sxs-lookup"><span data-stu-id="80f0e-105">UPN-Suffixes attribute</span></span>

<span data-ttu-id="80f0e-106">網域的使用者主體名稱尾碼清單。</span><span class="sxs-lookup"><span data-stu-id="80f0e-106">The list of User-Principal-Name suffixes for a domain.</span></span>



| <span data-ttu-id="80f0e-107">進入</span><span class="sxs-lookup"><span data-stu-id="80f0e-107">Entry</span></span> | <span data-ttu-id="80f0e-108">值</span><span class="sxs-lookup"><span data-stu-id="80f0e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="80f0e-109">CN</span><span class="sxs-lookup"><span data-stu-id="80f0e-109">CN</span></span>                | <span data-ttu-id="80f0e-110">UPN-Suffixes</span><span class="sxs-lookup"><span data-stu-id="80f0e-110">UPN-Suffixes</span></span>                                |
| <span data-ttu-id="80f0e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="80f0e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="80f0e-112">uPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="80f0e-112">uPNSuffixes</span></span>                                 |
| <span data-ttu-id="80f0e-113">大小</span><span class="sxs-lookup"><span data-stu-id="80f0e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="80f0e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="80f0e-114">Update Privilege</span></span>  | <span data-ttu-id="80f0e-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="80f0e-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="80f0e-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="80f0e-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="80f0e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="80f0e-117">Attribute-Id</span></span>      | <span data-ttu-id="80f0e-118">1.2.840.113556.1.4.890</span><span class="sxs-lookup"><span data-stu-id="80f0e-118">1.2.840.113556.1.4.890</span></span>                      |
| <span data-ttu-id="80f0e-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="80f0e-119">System-Id-Guid</span></span>    | <span data-ttu-id="80f0e-120">032160bf-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="80f0e-120">032160bf-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="80f0e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="80f0e-121">Syntax</span></span>            | [<span data-ttu-id="80f0e-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="80f0e-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="80f0e-123">實作</span><span class="sxs-lookup"><span data-stu-id="80f0e-123">Implementations</span></span>

-   [<span data-ttu-id="80f0e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="80f0e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="80f0e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="80f0e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="80f0e-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="80f0e-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="80f0e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="80f0e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="80f0e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="80f0e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="80f0e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="80f0e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="80f0e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="80f0e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="80f0e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80f0e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="80f0e-132">進入</span><span class="sxs-lookup"><span data-stu-id="80f0e-132">Entry</span></span> | <span data-ttu-id="80f0e-133">值</span><span class="sxs-lookup"><span data-stu-id="80f0e-133">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f0e-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="80f0e-134">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80f0e-135">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="80f0e-136">System-Only</span></span>            | <span data-ttu-id="80f0e-137">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-137">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="80f0e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="80f0e-139">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-139">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="80f0e-140">Is Indexed</span></span>             | <span data-ttu-id="80f0e-141">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-141">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="80f0e-142">In Global Catalog</span></span>      | <span data-ttu-id="80f0e-143">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-143">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="80f0e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="80f0e-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="80f0e-145">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="80f0e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80f0e-146">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80f0e-147">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-148">Search-Flags</span></span>           | <span data-ttu-id="80f0e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80f0e-149">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-150">System-Flags</span></span>           | <span data-ttu-id="80f0e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80f0e-151">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="80f0e-152">Classes used in</span></span>        | [<span data-ttu-id="80f0e-153">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="80f0e-153">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="80f0e-154">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="80f0e-154">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="80f0e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80f0e-155">Windows Server 2003</span></span>



| <span data-ttu-id="80f0e-156">進入</span><span class="sxs-lookup"><span data-stu-id="80f0e-156">Entry</span></span> | <span data-ttu-id="80f0e-157">值</span><span class="sxs-lookup"><span data-stu-id="80f0e-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f0e-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="80f0e-158">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80f0e-159">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="80f0e-160">System-Only</span></span>            | <span data-ttu-id="80f0e-161">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-161">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="80f0e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="80f0e-163">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-163">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="80f0e-164">Is Indexed</span></span>             | <span data-ttu-id="80f0e-165">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-165">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="80f0e-166">In Global Catalog</span></span>      | <span data-ttu-id="80f0e-167">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-167">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="80f0e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="80f0e-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="80f0e-169">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="80f0e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80f0e-170">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80f0e-171">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-172">Search-Flags</span></span>           | <span data-ttu-id="80f0e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80f0e-173">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-174">System-Flags</span></span>           | <span data-ttu-id="80f0e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80f0e-175">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="80f0e-176">Classes used in</span></span>        | [<span data-ttu-id="80f0e-177">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="80f0e-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="80f0e-178">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="80f0e-178">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="80f0e-179">亞當</span><span class="sxs-lookup"><span data-stu-id="80f0e-179">ADAM</span></span>



| <span data-ttu-id="80f0e-180">進入</span><span class="sxs-lookup"><span data-stu-id="80f0e-180">Entry</span></span> | <span data-ttu-id="80f0e-181">值</span><span class="sxs-lookup"><span data-stu-id="80f0e-181">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f0e-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="80f0e-182">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80f0e-183">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="80f0e-184">System-Only</span></span>            | <span data-ttu-id="80f0e-185">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-185">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="80f0e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="80f0e-187">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-187">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="80f0e-188">Is Indexed</span></span>             | <span data-ttu-id="80f0e-189">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-189">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="80f0e-190">In Global Catalog</span></span>      | <span data-ttu-id="80f0e-191">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-191">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="80f0e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="80f0e-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="80f0e-193">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="80f0e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80f0e-194">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80f0e-195">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-196">Search-Flags</span></span>           | <span data-ttu-id="80f0e-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80f0e-197">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-198">System-Flags</span></span>           | <span data-ttu-id="80f0e-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80f0e-199">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="80f0e-200">Classes used in</span></span>        | [<span data-ttu-id="80f0e-201">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="80f0e-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="80f0e-202">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="80f0e-202">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="80f0e-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="80f0e-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="80f0e-204">進入</span><span class="sxs-lookup"><span data-stu-id="80f0e-204">Entry</span></span> | <span data-ttu-id="80f0e-205">值</span><span class="sxs-lookup"><span data-stu-id="80f0e-205">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f0e-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="80f0e-206">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80f0e-207">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="80f0e-208">System-Only</span></span>            | <span data-ttu-id="80f0e-209">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-209">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="80f0e-210">Is-Single-Valued</span></span>       | <span data-ttu-id="80f0e-211">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-211">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="80f0e-212">Is Indexed</span></span>             | <span data-ttu-id="80f0e-213">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-213">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="80f0e-214">In Global Catalog</span></span>      | <span data-ttu-id="80f0e-215">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-215">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="80f0e-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="80f0e-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="80f0e-217">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="80f0e-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80f0e-218">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80f0e-219">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-220">Search-Flags</span></span>           | <span data-ttu-id="80f0e-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80f0e-221">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-222">System-Flags</span></span>           | <span data-ttu-id="80f0e-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80f0e-223">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="80f0e-224">Classes used in</span></span>        | [<span data-ttu-id="80f0e-225">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="80f0e-225">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="80f0e-226">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="80f0e-226">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="80f0e-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80f0e-227">Windows Server 2008</span></span>



| <span data-ttu-id="80f0e-228">進入</span><span class="sxs-lookup"><span data-stu-id="80f0e-228">Entry</span></span> | <span data-ttu-id="80f0e-229">值</span><span class="sxs-lookup"><span data-stu-id="80f0e-229">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f0e-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="80f0e-230">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80f0e-231">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="80f0e-232">System-Only</span></span>            | <span data-ttu-id="80f0e-233">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-233">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="80f0e-234">Is-Single-Valued</span></span>       | <span data-ttu-id="80f0e-235">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-235">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="80f0e-236">Is Indexed</span></span>             | <span data-ttu-id="80f0e-237">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-237">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="80f0e-238">In Global Catalog</span></span>      | <span data-ttu-id="80f0e-239">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-239">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="80f0e-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="80f0e-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="80f0e-241">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="80f0e-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80f0e-242">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80f0e-243">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-244">Search-Flags</span></span>           | <span data-ttu-id="80f0e-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80f0e-245">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-246">System-Flags</span></span>           | <span data-ttu-id="80f0e-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80f0e-247">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="80f0e-248">Classes used in</span></span>        | [<span data-ttu-id="80f0e-249">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="80f0e-249">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="80f0e-250">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="80f0e-250">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="80f0e-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80f0e-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="80f0e-252">進入</span><span class="sxs-lookup"><span data-stu-id="80f0e-252">Entry</span></span> | <span data-ttu-id="80f0e-253">值</span><span class="sxs-lookup"><span data-stu-id="80f0e-253">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f0e-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="80f0e-254">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80f0e-255">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="80f0e-256">System-Only</span></span>            | <span data-ttu-id="80f0e-257">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-257">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="80f0e-258">Is-Single-Valued</span></span>       | <span data-ttu-id="80f0e-259">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-259">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="80f0e-260">Is Indexed</span></span>             | <span data-ttu-id="80f0e-261">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-261">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="80f0e-262">In Global Catalog</span></span>      | <span data-ttu-id="80f0e-263">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-263">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="80f0e-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="80f0e-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="80f0e-265">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="80f0e-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80f0e-266">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80f0e-267">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-268">Search-Flags</span></span>           | <span data-ttu-id="80f0e-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80f0e-269">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-270">System-Flags</span></span>           | <span data-ttu-id="80f0e-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80f0e-271">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="80f0e-272">Classes used in</span></span>        | [<span data-ttu-id="80f0e-273">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="80f0e-273">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="80f0e-274">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="80f0e-274">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="80f0e-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80f0e-275">Windows Server 2012</span></span>



| <span data-ttu-id="80f0e-276">進入</span><span class="sxs-lookup"><span data-stu-id="80f0e-276">Entry</span></span> | <span data-ttu-id="80f0e-277">值</span><span class="sxs-lookup"><span data-stu-id="80f0e-277">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f0e-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="80f0e-278">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80f0e-279">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="80f0e-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="80f0e-280">System-Only</span></span>            | <span data-ttu-id="80f0e-281">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-281">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-282">是-單一值</span><span class="sxs-lookup"><span data-stu-id="80f0e-282">Is-Single-Valued</span></span>       | <span data-ttu-id="80f0e-283">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-283">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-284">已編制索引</span><span class="sxs-lookup"><span data-stu-id="80f0e-284">Is Indexed</span></span>             | <span data-ttu-id="80f0e-285">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-285">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-286">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="80f0e-286">In Global Catalog</span></span>      | <span data-ttu-id="80f0e-287">否</span><span class="sxs-lookup"><span data-stu-id="80f0e-287">False</span></span>                                                                                                                        |
| <span data-ttu-id="80f0e-288">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="80f0e-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="80f0e-289">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="80f0e-289">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="80f0e-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80f0e-290">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80f0e-291">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="80f0e-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-292">Search-Flags</span></span>           | <span data-ttu-id="80f0e-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80f0e-293">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80f0e-294">System-Flags</span></span>           | <span data-ttu-id="80f0e-295">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80f0e-295">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="80f0e-296">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="80f0e-296">Classes used in</span></span>        | [<span data-ttu-id="80f0e-297">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="80f0e-297">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="80f0e-298">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="80f0e-298">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 






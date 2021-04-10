---
title: Authentication-Options 屬性
description: ADSI 中用來系結至目錄服務物件的驗證選項。
ms.assetid: a6dc4591-d825-456a-8f77-78cb3c91af9f
ms.tgt_platform: multiple
keywords:
- Authentication-Options 屬性 AD 架構
- authenticationOptions 屬性 AD 架構
topic_type:
- apiref
api_name:
- Authentication-Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa9c422dfe196ab002c02c361759461f43965d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107292"
---
# <a name="authentication-options-attribute"></a><span data-ttu-id="a26e9-105">Authentication-Options 屬性</span><span class="sxs-lookup"><span data-stu-id="a26e9-105">Authentication-Options attribute</span></span>

<span data-ttu-id="a26e9-106">ADSI 中用來系結至目錄服務物件的驗證選項。</span><span class="sxs-lookup"><span data-stu-id="a26e9-106">The authentication options used in ADSI to bind to directory services objects.</span></span>



| <span data-ttu-id="a26e9-107">進入</span><span class="sxs-lookup"><span data-stu-id="a26e9-107">Entry</span></span> | <span data-ttu-id="a26e9-108">值</span><span class="sxs-lookup"><span data-stu-id="a26e9-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a26e9-109">CN</span><span class="sxs-lookup"><span data-stu-id="a26e9-109">CN</span></span>                | <span data-ttu-id="a26e9-110">Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="a26e9-110">Authentication-Options</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a26e9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a26e9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a26e9-112">authenticationOptions</span><span class="sxs-lookup"><span data-stu-id="a26e9-112">authenticationOptions</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a26e9-113">大小</span><span class="sxs-lookup"><span data-stu-id="a26e9-113">Size</span></span>              | <span data-ttu-id="a26e9-114">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="a26e9-114">4 bytes.</span></span> <span data-ttu-id="a26e9-115">在 IADS 中定義的值： ADS \_ 安全 \_ 驗證0X1、ads \_ 使用 \_ 加密0x2、ads \_ 使用 \_ SSL 0x2、ads \_ READONLY \_ SERVER 0x4、ads \_ 提示 \_ 認證0x8、ads \_ 無 \_ 驗證0x10、ads \_ 快速系結 \_ 0x20、ads \_ 使用 \_ 簽署0x40、ads \_ 使用 \_ 密封0x80</span><span class="sxs-lookup"><span data-stu-id="a26e9-115">Values defined in IADS.h: ADS\_SECURE\_AUTHENTICATION 0x1, ADS\_USE\_ENCRYPTION 0x2, ADS\_USE\_SSL 0x2, ADS\_READONLY\_SERVER 0x4, ADS\_PROMPT\_CREDENTIALS 0x8, ADS\_NO\_AUTHENTICATION 0x10, ADS\_FAST\_BIND 0x20, ADS\_USE\_SIGNING 0x40, ADS\_USE\_SEALING 0x80</span></span> |
| <span data-ttu-id="a26e9-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a26e9-116">Update Privilege</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a26e9-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a26e9-117">Update Frequency</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a26e9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a26e9-118">Attribute-Id</span></span>      | <span data-ttu-id="a26e9-119">1.2.840.113556.1.4.11</span><span class="sxs-lookup"><span data-stu-id="a26e9-119">1.2.840.113556.1.4.11</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a26e9-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a26e9-120">System-Id-Guid</span></span>    | <span data-ttu-id="a26e9-121">bf967928-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a26e9-121">bf967928-0de6-11d0-a285-00aa003049e2</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="a26e9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a26e9-122">Syntax</span></span>            | [<span data-ttu-id="a26e9-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="a26e9-123">**Enumeration**</span></span>](s-enumeration.md)                                                                                                                                                                                                                                         |



## <a name="implementations"></a><span data-ttu-id="a26e9-124">實作</span><span class="sxs-lookup"><span data-stu-id="a26e9-124">Implementations</span></span>

-   [<span data-ttu-id="a26e9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a26e9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a26e9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a26e9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a26e9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a26e9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a26e9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a26e9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a26e9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a26e9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a26e9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a26e9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a26e9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a26e9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a26e9-132">進入</span><span class="sxs-lookup"><span data-stu-id="a26e9-132">Entry</span></span> | <span data-ttu-id="a26e9-133">值</span><span class="sxs-lookup"><span data-stu-id="a26e9-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a26e9-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a26e9-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a26e9-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a26e9-136">System-Only</span></span>            | <span data-ttu-id="a26e9-137">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-137">False</span></span>                                              |
| <span data-ttu-id="a26e9-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a26e9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a26e9-139">對</span><span class="sxs-lookup"><span data-stu-id="a26e9-139">True</span></span>                                               |
| <span data-ttu-id="a26e9-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a26e9-140">Is Indexed</span></span>             | <span data-ttu-id="a26e9-141">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-141">False</span></span>                                              |
| <span data-ttu-id="a26e9-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a26e9-142">In Global Catalog</span></span>      | <span data-ttu-id="a26e9-143">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-143">False</span></span>                                              |
| <span data-ttu-id="a26e9-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a26e9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a26e9-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a26e9-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a26e9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a26e9-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a26e9-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-148">Search-Flags</span></span>           | <span data-ttu-id="a26e9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a26e9-149">0x00000000</span></span>                                         |
| <span data-ttu-id="a26e9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-150">System-Flags</span></span>           | <span data-ttu-id="a26e9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a26e9-151">0x00000010</span></span>                                         |
| <span data-ttu-id="a26e9-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a26e9-152">Classes used in</span></span>        | [<span data-ttu-id="a26e9-153">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="a26e9-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a26e9-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a26e9-154">Windows Server 2003</span></span>



| <span data-ttu-id="a26e9-155">進入</span><span class="sxs-lookup"><span data-stu-id="a26e9-155">Entry</span></span> | <span data-ttu-id="a26e9-156">值</span><span class="sxs-lookup"><span data-stu-id="a26e9-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a26e9-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a26e9-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a26e9-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a26e9-159">System-Only</span></span>            | <span data-ttu-id="a26e9-160">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-160">False</span></span>                                              |
| <span data-ttu-id="a26e9-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a26e9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a26e9-162">對</span><span class="sxs-lookup"><span data-stu-id="a26e9-162">True</span></span>                                               |
| <span data-ttu-id="a26e9-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a26e9-163">Is Indexed</span></span>             | <span data-ttu-id="a26e9-164">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-164">False</span></span>                                              |
| <span data-ttu-id="a26e9-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a26e9-165">In Global Catalog</span></span>      | <span data-ttu-id="a26e9-166">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-166">False</span></span>                                              |
| <span data-ttu-id="a26e9-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a26e9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a26e9-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a26e9-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a26e9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a26e9-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a26e9-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-171">Search-Flags</span></span>           | <span data-ttu-id="a26e9-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a26e9-172">0x00000000</span></span>                                         |
| <span data-ttu-id="a26e9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-173">System-Flags</span></span>           | <span data-ttu-id="a26e9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a26e9-174">0x00000010</span></span>                                         |
| <span data-ttu-id="a26e9-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a26e9-175">Classes used in</span></span>        | [<span data-ttu-id="a26e9-176">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="a26e9-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a26e9-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a26e9-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a26e9-178">進入</span><span class="sxs-lookup"><span data-stu-id="a26e9-178">Entry</span></span> | <span data-ttu-id="a26e9-179">值</span><span class="sxs-lookup"><span data-stu-id="a26e9-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a26e9-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a26e9-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a26e9-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a26e9-182">System-Only</span></span>            | <span data-ttu-id="a26e9-183">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-183">False</span></span>                                              |
| <span data-ttu-id="a26e9-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a26e9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a26e9-185">對</span><span class="sxs-lookup"><span data-stu-id="a26e9-185">True</span></span>                                               |
| <span data-ttu-id="a26e9-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a26e9-186">Is Indexed</span></span>             | <span data-ttu-id="a26e9-187">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-187">False</span></span>                                              |
| <span data-ttu-id="a26e9-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a26e9-188">In Global Catalog</span></span>      | <span data-ttu-id="a26e9-189">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-189">False</span></span>                                              |
| <span data-ttu-id="a26e9-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a26e9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a26e9-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a26e9-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a26e9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a26e9-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a26e9-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-194">Search-Flags</span></span>           | <span data-ttu-id="a26e9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a26e9-195">0x00000000</span></span>                                         |
| <span data-ttu-id="a26e9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-196">System-Flags</span></span>           | <span data-ttu-id="a26e9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a26e9-197">0x00000010</span></span>                                         |
| <span data-ttu-id="a26e9-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a26e9-198">Classes used in</span></span>        | [<span data-ttu-id="a26e9-199">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="a26e9-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a26e9-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a26e9-200">Windows Server 2008</span></span>



| <span data-ttu-id="a26e9-201">進入</span><span class="sxs-lookup"><span data-stu-id="a26e9-201">Entry</span></span> | <span data-ttu-id="a26e9-202">值</span><span class="sxs-lookup"><span data-stu-id="a26e9-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a26e9-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a26e9-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a26e9-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a26e9-205">System-Only</span></span>            | <span data-ttu-id="a26e9-206">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-206">False</span></span>                                              |
| <span data-ttu-id="a26e9-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a26e9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a26e9-208">對</span><span class="sxs-lookup"><span data-stu-id="a26e9-208">True</span></span>                                               |
| <span data-ttu-id="a26e9-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a26e9-209">Is Indexed</span></span>             | <span data-ttu-id="a26e9-210">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-210">False</span></span>                                              |
| <span data-ttu-id="a26e9-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a26e9-211">In Global Catalog</span></span>      | <span data-ttu-id="a26e9-212">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-212">False</span></span>                                              |
| <span data-ttu-id="a26e9-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a26e9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a26e9-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a26e9-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a26e9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a26e9-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a26e9-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-217">Search-Flags</span></span>           | <span data-ttu-id="a26e9-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a26e9-218">0x00000000</span></span>                                         |
| <span data-ttu-id="a26e9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-219">System-Flags</span></span>           | <span data-ttu-id="a26e9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a26e9-220">0x00000010</span></span>                                         |
| <span data-ttu-id="a26e9-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a26e9-221">Classes used in</span></span>        | [<span data-ttu-id="a26e9-222">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="a26e9-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a26e9-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a26e9-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a26e9-224">進入</span><span class="sxs-lookup"><span data-stu-id="a26e9-224">Entry</span></span> | <span data-ttu-id="a26e9-225">值</span><span class="sxs-lookup"><span data-stu-id="a26e9-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a26e9-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a26e9-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a26e9-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a26e9-228">System-Only</span></span>            | <span data-ttu-id="a26e9-229">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-229">False</span></span>                                              |
| <span data-ttu-id="a26e9-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a26e9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a26e9-231">對</span><span class="sxs-lookup"><span data-stu-id="a26e9-231">True</span></span>                                               |
| <span data-ttu-id="a26e9-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a26e9-232">Is Indexed</span></span>             | <span data-ttu-id="a26e9-233">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-233">False</span></span>                                              |
| <span data-ttu-id="a26e9-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a26e9-234">In Global Catalog</span></span>      | <span data-ttu-id="a26e9-235">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-235">False</span></span>                                              |
| <span data-ttu-id="a26e9-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a26e9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a26e9-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a26e9-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a26e9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a26e9-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a26e9-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-240">Search-Flags</span></span>           | <span data-ttu-id="a26e9-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a26e9-241">0x00000000</span></span>                                         |
| <span data-ttu-id="a26e9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-242">System-Flags</span></span>           | <span data-ttu-id="a26e9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a26e9-243">0x00000010</span></span>                                         |
| <span data-ttu-id="a26e9-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a26e9-244">Classes used in</span></span>        | [<span data-ttu-id="a26e9-245">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="a26e9-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a26e9-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a26e9-246">Windows Server 2012</span></span>



| <span data-ttu-id="a26e9-247">進入</span><span class="sxs-lookup"><span data-stu-id="a26e9-247">Entry</span></span> | <span data-ttu-id="a26e9-248">值</span><span class="sxs-lookup"><span data-stu-id="a26e9-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a26e9-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a26e9-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a26e9-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a26e9-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a26e9-251">System-Only</span></span>            | <span data-ttu-id="a26e9-252">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-252">False</span></span>                                              |
| <span data-ttu-id="a26e9-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a26e9-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a26e9-254">對</span><span class="sxs-lookup"><span data-stu-id="a26e9-254">True</span></span>                                               |
| <span data-ttu-id="a26e9-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a26e9-255">Is Indexed</span></span>             | <span data-ttu-id="a26e9-256">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-256">False</span></span>                                              |
| <span data-ttu-id="a26e9-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a26e9-257">In Global Catalog</span></span>      | <span data-ttu-id="a26e9-258">否</span><span class="sxs-lookup"><span data-stu-id="a26e9-258">False</span></span>                                              |
| <span data-ttu-id="a26e9-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a26e9-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a26e9-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a26e9-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a26e9-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a26e9-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a26e9-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a26e9-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-263">Search-Flags</span></span>           | <span data-ttu-id="a26e9-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a26e9-264">0x00000000</span></span>                                         |
| <span data-ttu-id="a26e9-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a26e9-265">System-Flags</span></span>           | <span data-ttu-id="a26e9-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a26e9-266">0x00000010</span></span>                                         |
| <span data-ttu-id="a26e9-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a26e9-267">Classes used in</span></span>        | [<span data-ttu-id="a26e9-268">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="a26e9-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 






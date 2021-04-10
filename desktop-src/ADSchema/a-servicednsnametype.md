---
title: 服務-DNS-名稱-類型屬性
description: 要查閱此服務的 DNS 記錄類型。 例如，或 SRV。
ms.assetid: 9a1ab2ae-b63f-4c70-b0df-de97c482bc5a
ms.tgt_platform: multiple
keywords:
- 服務-DNS-名稱-類型屬性 AD 架構
- serviceDNSNameType 屬性 AD 架構
topic_type:
- apiref
api_name:
- Service-DNS-Name-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369bf644cac226788332cb4a2935973a5d5ffeae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844923"
---
# <a name="service-dns-name-type-attribute"></a><span data-ttu-id="88e6d-106">服務-DNS-名稱-類型屬性</span><span class="sxs-lookup"><span data-stu-id="88e6d-106">Service-DNS-Name-Type attribute</span></span>

<span data-ttu-id="88e6d-107">要查閱此服務的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="88e6d-107">Type of DNS Record to look up for this service.</span></span> <span data-ttu-id="88e6d-108">例如，或 SRV。</span><span class="sxs-lookup"><span data-stu-id="88e6d-108">For example, A or SRV.</span></span>



| <span data-ttu-id="88e6d-109">進入</span><span class="sxs-lookup"><span data-stu-id="88e6d-109">Entry</span></span> | <span data-ttu-id="88e6d-110">值</span><span class="sxs-lookup"><span data-stu-id="88e6d-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="88e6d-111">CN</span><span class="sxs-lookup"><span data-stu-id="88e6d-111">CN</span></span>                | <span data-ttu-id="88e6d-112">服務-DNS-名稱-類型</span><span class="sxs-lookup"><span data-stu-id="88e6d-112">Service-DNS-Name-Type</span></span>                       |
| <span data-ttu-id="88e6d-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="88e6d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="88e6d-114">serviceDNSNameType</span><span class="sxs-lookup"><span data-stu-id="88e6d-114">serviceDNSNameType</span></span>                          |
| <span data-ttu-id="88e6d-115">大小</span><span class="sxs-lookup"><span data-stu-id="88e6d-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="88e6d-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="88e6d-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="88e6d-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="88e6d-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="88e6d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88e6d-118">Attribute-Id</span></span>      | <span data-ttu-id="88e6d-119">1.2.840.113556.1.4.659</span><span class="sxs-lookup"><span data-stu-id="88e6d-119">1.2.840.113556.1.4.659</span></span>                      |
| <span data-ttu-id="88e6d-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="88e6d-120">System-Id-Guid</span></span>    | <span data-ttu-id="88e6d-121">28630eba-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="88e6d-121">28630eba-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="88e6d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="88e6d-122">Syntax</span></span>            | [<span data-ttu-id="88e6d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="88e6d-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="88e6d-124">實作</span><span class="sxs-lookup"><span data-stu-id="88e6d-124">Implementations</span></span>

-   [<span data-ttu-id="88e6d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="88e6d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="88e6d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="88e6d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="88e6d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="88e6d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="88e6d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88e6d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88e6d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88e6d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88e6d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88e6d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="88e6d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88e6d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="88e6d-132">進入</span><span class="sxs-lookup"><span data-stu-id="88e6d-132">Entry</span></span> | <span data-ttu-id="88e6d-133">值</span><span class="sxs-lookup"><span data-stu-id="88e6d-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88e6d-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88e6d-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="88e6d-136">System-Only</span></span>            | <span data-ttu-id="88e6d-137">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-137">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88e6d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="88e6d-139">對</span><span class="sxs-lookup"><span data-stu-id="88e6d-139">True</span></span>                                                                    |
| <span data-ttu-id="88e6d-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88e6d-140">Is Indexed</span></span>             | <span data-ttu-id="88e6d-141">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-141">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88e6d-142">In Global Catalog</span></span>      | <span data-ttu-id="88e6d-143">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-143">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88e6d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="88e6d-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88e6d-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="88e6d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88e6d-146">Range-Lower</span></span>            | <span data-ttu-id="88e6d-147">1</span><span class="sxs-lookup"><span data-stu-id="88e6d-147">1</span></span>                                                                       |
| <span data-ttu-id="88e6d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88e6d-148">Range-Upper</span></span>            | <span data-ttu-id="88e6d-149">256</span><span class="sxs-lookup"><span data-stu-id="88e6d-149">256</span></span>                                                                     |
| <span data-ttu-id="88e6d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-150">Search-Flags</span></span>           | <span data-ttu-id="88e6d-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88e6d-151">0x00000000</span></span>                                                              |
| <span data-ttu-id="88e6d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-152">System-Flags</span></span>           | <span data-ttu-id="88e6d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88e6d-153">0x00000010</span></span>                                                              |
| <span data-ttu-id="88e6d-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88e6d-154">Classes used in</span></span>        | [<span data-ttu-id="88e6d-155">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="88e6d-155">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="88e6d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88e6d-156">Windows Server 2003</span></span>



| <span data-ttu-id="88e6d-157">進入</span><span class="sxs-lookup"><span data-stu-id="88e6d-157">Entry</span></span> | <span data-ttu-id="88e6d-158">值</span><span class="sxs-lookup"><span data-stu-id="88e6d-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88e6d-159">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88e6d-160">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="88e6d-161">System-Only</span></span>            | <span data-ttu-id="88e6d-162">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-162">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88e6d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="88e6d-164">對</span><span class="sxs-lookup"><span data-stu-id="88e6d-164">True</span></span>                                                                    |
| <span data-ttu-id="88e6d-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88e6d-165">Is Indexed</span></span>             | <span data-ttu-id="88e6d-166">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-166">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88e6d-167">In Global Catalog</span></span>      | <span data-ttu-id="88e6d-168">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-168">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88e6d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="88e6d-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88e6d-170">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="88e6d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88e6d-171">Range-Lower</span></span>            | <span data-ttu-id="88e6d-172">1</span><span class="sxs-lookup"><span data-stu-id="88e6d-172">1</span></span>                                                                       |
| <span data-ttu-id="88e6d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88e6d-173">Range-Upper</span></span>            | <span data-ttu-id="88e6d-174">256</span><span class="sxs-lookup"><span data-stu-id="88e6d-174">256</span></span>                                                                     |
| <span data-ttu-id="88e6d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-175">Search-Flags</span></span>           | <span data-ttu-id="88e6d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88e6d-176">0x00000000</span></span>                                                              |
| <span data-ttu-id="88e6d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-177">System-Flags</span></span>           | <span data-ttu-id="88e6d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88e6d-178">0x00000010</span></span>                                                              |
| <span data-ttu-id="88e6d-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88e6d-179">Classes used in</span></span>        | [<span data-ttu-id="88e6d-180">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="88e6d-180">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="88e6d-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="88e6d-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="88e6d-182">進入</span><span class="sxs-lookup"><span data-stu-id="88e6d-182">Entry</span></span> | <span data-ttu-id="88e6d-183">值</span><span class="sxs-lookup"><span data-stu-id="88e6d-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88e6d-184">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88e6d-185">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="88e6d-186">System-Only</span></span>            | <span data-ttu-id="88e6d-187">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-187">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88e6d-188">Is-Single-Valued</span></span>       | <span data-ttu-id="88e6d-189">對</span><span class="sxs-lookup"><span data-stu-id="88e6d-189">True</span></span>                                                                    |
| <span data-ttu-id="88e6d-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88e6d-190">Is Indexed</span></span>             | <span data-ttu-id="88e6d-191">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-191">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88e6d-192">In Global Catalog</span></span>      | <span data-ttu-id="88e6d-193">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-193">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88e6d-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="88e6d-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88e6d-195">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="88e6d-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88e6d-196">Range-Lower</span></span>            | <span data-ttu-id="88e6d-197">1</span><span class="sxs-lookup"><span data-stu-id="88e6d-197">1</span></span>                                                                       |
| <span data-ttu-id="88e6d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88e6d-198">Range-Upper</span></span>            | <span data-ttu-id="88e6d-199">256</span><span class="sxs-lookup"><span data-stu-id="88e6d-199">256</span></span>                                                                     |
| <span data-ttu-id="88e6d-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-200">Search-Flags</span></span>           | <span data-ttu-id="88e6d-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88e6d-201">0x00000000</span></span>                                                              |
| <span data-ttu-id="88e6d-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-202">System-Flags</span></span>           | <span data-ttu-id="88e6d-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88e6d-203">0x00000010</span></span>                                                              |
| <span data-ttu-id="88e6d-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88e6d-204">Classes used in</span></span>        | [<span data-ttu-id="88e6d-205">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="88e6d-205">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="88e6d-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88e6d-206">Windows Server 2008</span></span>



| <span data-ttu-id="88e6d-207">進入</span><span class="sxs-lookup"><span data-stu-id="88e6d-207">Entry</span></span> | <span data-ttu-id="88e6d-208">值</span><span class="sxs-lookup"><span data-stu-id="88e6d-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88e6d-209">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88e6d-210">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="88e6d-211">System-Only</span></span>            | <span data-ttu-id="88e6d-212">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-212">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88e6d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="88e6d-214">對</span><span class="sxs-lookup"><span data-stu-id="88e6d-214">True</span></span>                                                                    |
| <span data-ttu-id="88e6d-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88e6d-215">Is Indexed</span></span>             | <span data-ttu-id="88e6d-216">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-216">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88e6d-217">In Global Catalog</span></span>      | <span data-ttu-id="88e6d-218">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-218">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88e6d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="88e6d-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88e6d-220">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="88e6d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88e6d-221">Range-Lower</span></span>            | <span data-ttu-id="88e6d-222">1</span><span class="sxs-lookup"><span data-stu-id="88e6d-222">1</span></span>                                                                       |
| <span data-ttu-id="88e6d-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88e6d-223">Range-Upper</span></span>            | <span data-ttu-id="88e6d-224">256</span><span class="sxs-lookup"><span data-stu-id="88e6d-224">256</span></span>                                                                     |
| <span data-ttu-id="88e6d-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-225">Search-Flags</span></span>           | <span data-ttu-id="88e6d-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88e6d-226">0x00000000</span></span>                                                              |
| <span data-ttu-id="88e6d-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-227">System-Flags</span></span>           | <span data-ttu-id="88e6d-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88e6d-228">0x00000010</span></span>                                                              |
| <span data-ttu-id="88e6d-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88e6d-229">Classes used in</span></span>        | [<span data-ttu-id="88e6d-230">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="88e6d-230">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88e6d-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88e6d-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88e6d-232">進入</span><span class="sxs-lookup"><span data-stu-id="88e6d-232">Entry</span></span> | <span data-ttu-id="88e6d-233">值</span><span class="sxs-lookup"><span data-stu-id="88e6d-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88e6d-234">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88e6d-235">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="88e6d-236">System-Only</span></span>            | <span data-ttu-id="88e6d-237">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-237">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88e6d-238">Is-Single-Valued</span></span>       | <span data-ttu-id="88e6d-239">對</span><span class="sxs-lookup"><span data-stu-id="88e6d-239">True</span></span>                                                                    |
| <span data-ttu-id="88e6d-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88e6d-240">Is Indexed</span></span>             | <span data-ttu-id="88e6d-241">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-241">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88e6d-242">In Global Catalog</span></span>      | <span data-ttu-id="88e6d-243">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-243">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88e6d-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="88e6d-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88e6d-245">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="88e6d-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88e6d-246">Range-Lower</span></span>            | <span data-ttu-id="88e6d-247">1</span><span class="sxs-lookup"><span data-stu-id="88e6d-247">1</span></span>                                                                       |
| <span data-ttu-id="88e6d-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88e6d-248">Range-Upper</span></span>            | <span data-ttu-id="88e6d-249">256</span><span class="sxs-lookup"><span data-stu-id="88e6d-249">256</span></span>                                                                     |
| <span data-ttu-id="88e6d-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-250">Search-Flags</span></span>           | <span data-ttu-id="88e6d-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88e6d-251">0x00000000</span></span>                                                              |
| <span data-ttu-id="88e6d-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-252">System-Flags</span></span>           | <span data-ttu-id="88e6d-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88e6d-253">0x00000010</span></span>                                                              |
| <span data-ttu-id="88e6d-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88e6d-254">Classes used in</span></span>        | [<span data-ttu-id="88e6d-255">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="88e6d-255">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88e6d-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88e6d-256">Windows Server 2012</span></span>



| <span data-ttu-id="88e6d-257">進入</span><span class="sxs-lookup"><span data-stu-id="88e6d-257">Entry</span></span> | <span data-ttu-id="88e6d-258">值</span><span class="sxs-lookup"><span data-stu-id="88e6d-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88e6d-259">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88e6d-260">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="88e6d-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="88e6d-261">System-Only</span></span>            | <span data-ttu-id="88e6d-262">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-262">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88e6d-263">Is-Single-Valued</span></span>       | <span data-ttu-id="88e6d-264">對</span><span class="sxs-lookup"><span data-stu-id="88e6d-264">True</span></span>                                                                    |
| <span data-ttu-id="88e6d-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88e6d-265">Is Indexed</span></span>             | <span data-ttu-id="88e6d-266">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-266">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88e6d-267">In Global Catalog</span></span>      | <span data-ttu-id="88e6d-268">否</span><span class="sxs-lookup"><span data-stu-id="88e6d-268">False</span></span>                                                                   |
| <span data-ttu-id="88e6d-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88e6d-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="88e6d-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88e6d-270">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="88e6d-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88e6d-271">Range-Lower</span></span>            | <span data-ttu-id="88e6d-272">1</span><span class="sxs-lookup"><span data-stu-id="88e6d-272">1</span></span>                                                                       |
| <span data-ttu-id="88e6d-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88e6d-273">Range-Upper</span></span>            | <span data-ttu-id="88e6d-274">256</span><span class="sxs-lookup"><span data-stu-id="88e6d-274">256</span></span>                                                                     |
| <span data-ttu-id="88e6d-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-275">Search-Flags</span></span>           | <span data-ttu-id="88e6d-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88e6d-276">0x00000000</span></span>                                                              |
| <span data-ttu-id="88e6d-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88e6d-277">System-Flags</span></span>           | <span data-ttu-id="88e6d-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88e6d-278">0x00000010</span></span>                                                              |
| <span data-ttu-id="88e6d-279">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88e6d-279">Classes used in</span></span>        | [<span data-ttu-id="88e6d-280">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="88e6d-280">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



 

 






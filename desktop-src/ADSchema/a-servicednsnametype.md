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
# <a name="service-dns-name-type-attribute"></a><span data-ttu-id="7ecf3-106">服務-DNS-名稱-類型屬性</span><span class="sxs-lookup"><span data-stu-id="7ecf3-106">Service-DNS-Name-Type attribute</span></span>

<span data-ttu-id="7ecf3-107">要查閱此服務的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="7ecf3-107">Type of DNS Record to look up for this service.</span></span> <span data-ttu-id="7ecf3-108">例如，或 SRV。</span><span class="sxs-lookup"><span data-stu-id="7ecf3-108">For example, A or SRV.</span></span>



| <span data-ttu-id="7ecf3-109">進入</span><span class="sxs-lookup"><span data-stu-id="7ecf3-109">Entry</span></span> | <span data-ttu-id="7ecf3-110">值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7ecf3-111">CN</span><span class="sxs-lookup"><span data-stu-id="7ecf3-111">CN</span></span>                | <span data-ttu-id="7ecf3-112">服務-DNS-名稱-類型</span><span class="sxs-lookup"><span data-stu-id="7ecf3-112">Service-DNS-Name-Type</span></span>                       |
| <span data-ttu-id="7ecf3-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7ecf3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7ecf3-114">serviceDNSNameType</span><span class="sxs-lookup"><span data-stu-id="7ecf3-114">serviceDNSNameType</span></span>                          |
| <span data-ttu-id="7ecf3-115">大小</span><span class="sxs-lookup"><span data-stu-id="7ecf3-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="7ecf3-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7ecf3-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="7ecf3-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7ecf3-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="7ecf3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ecf3-118">Attribute-Id</span></span>      | <span data-ttu-id="7ecf3-119">1.2.840.113556.1.4.659</span><span class="sxs-lookup"><span data-stu-id="7ecf3-119">1.2.840.113556.1.4.659</span></span>                      |
| <span data-ttu-id="7ecf3-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7ecf3-120">System-Id-Guid</span></span>    | <span data-ttu-id="7ecf3-121">28630eba-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7ecf3-121">28630eba-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="7ecf3-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ecf3-122">Syntax</span></span>            | [<span data-ttu-id="7ecf3-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7ecf3-124">實作</span><span class="sxs-lookup"><span data-stu-id="7ecf3-124">Implementations</span></span>

-   [<span data-ttu-id="7ecf3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7ecf3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ecf3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ecf3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ecf3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ecf3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7ecf3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ecf3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7ecf3-132">進入</span><span class="sxs-lookup"><span data-stu-id="7ecf3-132">Entry</span></span> | <span data-ttu-id="7ecf3-133">值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7ecf3-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ecf3-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ecf3-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ecf3-136">System-Only</span></span>            | <span data-ttu-id="7ecf3-137">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-137">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7ecf3-139">對</span><span class="sxs-lookup"><span data-stu-id="7ecf3-139">True</span></span>                                                                    |
| <span data-ttu-id="7ecf3-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ecf3-140">Is Indexed</span></span>             | <span data-ttu-id="7ecf3-141">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-141">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ecf3-142">In Global Catalog</span></span>      | <span data-ttu-id="7ecf3-143">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-143">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ecf3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ecf3-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ecf3-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7ecf3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ecf3-146">Range-Lower</span></span>            | <span data-ttu-id="7ecf3-147">1</span><span class="sxs-lookup"><span data-stu-id="7ecf3-147">1</span></span>                                                                       |
| <span data-ttu-id="7ecf3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ecf3-148">Range-Upper</span></span>            | <span data-ttu-id="7ecf3-149">256</span><span class="sxs-lookup"><span data-stu-id="7ecf3-149">256</span></span>                                                                     |
| <span data-ttu-id="7ecf3-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-150">Search-Flags</span></span>           | <span data-ttu-id="7ecf3-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ecf3-151">0x00000000</span></span>                                                              |
| <span data-ttu-id="7ecf3-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-152">System-Flags</span></span>           | <span data-ttu-id="7ecf3-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ecf3-153">0x00000010</span></span>                                                              |
| <span data-ttu-id="7ecf3-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ecf3-154">Classes used in</span></span>        | [<span data-ttu-id="7ecf3-155">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-155">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7ecf3-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ecf3-156">Windows Server 2003</span></span>



| <span data-ttu-id="7ecf3-157">進入</span><span class="sxs-lookup"><span data-stu-id="7ecf3-157">Entry</span></span> | <span data-ttu-id="7ecf3-158">值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7ecf3-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ecf3-159">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ecf3-160">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ecf3-161">System-Only</span></span>            | <span data-ttu-id="7ecf3-162">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-162">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-163">Is-Single-Valued</span></span>       | <span data-ttu-id="7ecf3-164">對</span><span class="sxs-lookup"><span data-stu-id="7ecf3-164">True</span></span>                                                                    |
| <span data-ttu-id="7ecf3-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ecf3-165">Is Indexed</span></span>             | <span data-ttu-id="7ecf3-166">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-166">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ecf3-167">In Global Catalog</span></span>      | <span data-ttu-id="7ecf3-168">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-168">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ecf3-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ecf3-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ecf3-170">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7ecf3-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ecf3-171">Range-Lower</span></span>            | <span data-ttu-id="7ecf3-172">1</span><span class="sxs-lookup"><span data-stu-id="7ecf3-172">1</span></span>                                                                       |
| <span data-ttu-id="7ecf3-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ecf3-173">Range-Upper</span></span>            | <span data-ttu-id="7ecf3-174">256</span><span class="sxs-lookup"><span data-stu-id="7ecf3-174">256</span></span>                                                                     |
| <span data-ttu-id="7ecf3-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-175">Search-Flags</span></span>           | <span data-ttu-id="7ecf3-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ecf3-176">0x00000000</span></span>                                                              |
| <span data-ttu-id="7ecf3-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-177">System-Flags</span></span>           | <span data-ttu-id="7ecf3-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ecf3-178">0x00000010</span></span>                                                              |
| <span data-ttu-id="7ecf3-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ecf3-179">Classes used in</span></span>        | [<span data-ttu-id="7ecf3-180">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-180">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ecf3-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ecf3-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ecf3-182">進入</span><span class="sxs-lookup"><span data-stu-id="7ecf3-182">Entry</span></span> | <span data-ttu-id="7ecf3-183">值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7ecf3-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ecf3-184">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ecf3-185">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ecf3-186">System-Only</span></span>            | <span data-ttu-id="7ecf3-187">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-187">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-188">Is-Single-Valued</span></span>       | <span data-ttu-id="7ecf3-189">對</span><span class="sxs-lookup"><span data-stu-id="7ecf3-189">True</span></span>                                                                    |
| <span data-ttu-id="7ecf3-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ecf3-190">Is Indexed</span></span>             | <span data-ttu-id="7ecf3-191">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-191">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ecf3-192">In Global Catalog</span></span>      | <span data-ttu-id="7ecf3-193">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-193">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ecf3-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ecf3-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ecf3-195">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7ecf3-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ecf3-196">Range-Lower</span></span>            | <span data-ttu-id="7ecf3-197">1</span><span class="sxs-lookup"><span data-stu-id="7ecf3-197">1</span></span>                                                                       |
| <span data-ttu-id="7ecf3-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ecf3-198">Range-Upper</span></span>            | <span data-ttu-id="7ecf3-199">256</span><span class="sxs-lookup"><span data-stu-id="7ecf3-199">256</span></span>                                                                     |
| <span data-ttu-id="7ecf3-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-200">Search-Flags</span></span>           | <span data-ttu-id="7ecf3-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ecf3-201">0x00000000</span></span>                                                              |
| <span data-ttu-id="7ecf3-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-202">System-Flags</span></span>           | <span data-ttu-id="7ecf3-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ecf3-203">0x00000010</span></span>                                                              |
| <span data-ttu-id="7ecf3-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ecf3-204">Classes used in</span></span>        | [<span data-ttu-id="7ecf3-205">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-205">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ecf3-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ecf3-206">Windows Server 2008</span></span>



| <span data-ttu-id="7ecf3-207">進入</span><span class="sxs-lookup"><span data-stu-id="7ecf3-207">Entry</span></span> | <span data-ttu-id="7ecf3-208">值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7ecf3-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ecf3-209">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ecf3-210">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ecf3-211">System-Only</span></span>            | <span data-ttu-id="7ecf3-212">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-212">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-213">Is-Single-Valued</span></span>       | <span data-ttu-id="7ecf3-214">對</span><span class="sxs-lookup"><span data-stu-id="7ecf3-214">True</span></span>                                                                    |
| <span data-ttu-id="7ecf3-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ecf3-215">Is Indexed</span></span>             | <span data-ttu-id="7ecf3-216">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-216">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ecf3-217">In Global Catalog</span></span>      | <span data-ttu-id="7ecf3-218">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-218">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ecf3-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ecf3-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ecf3-220">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7ecf3-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ecf3-221">Range-Lower</span></span>            | <span data-ttu-id="7ecf3-222">1</span><span class="sxs-lookup"><span data-stu-id="7ecf3-222">1</span></span>                                                                       |
| <span data-ttu-id="7ecf3-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ecf3-223">Range-Upper</span></span>            | <span data-ttu-id="7ecf3-224">256</span><span class="sxs-lookup"><span data-stu-id="7ecf3-224">256</span></span>                                                                     |
| <span data-ttu-id="7ecf3-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-225">Search-Flags</span></span>           | <span data-ttu-id="7ecf3-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ecf3-226">0x00000000</span></span>                                                              |
| <span data-ttu-id="7ecf3-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-227">System-Flags</span></span>           | <span data-ttu-id="7ecf3-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ecf3-228">0x00000010</span></span>                                                              |
| <span data-ttu-id="7ecf3-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ecf3-229">Classes used in</span></span>        | [<span data-ttu-id="7ecf3-230">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-230">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ecf3-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ecf3-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ecf3-232">進入</span><span class="sxs-lookup"><span data-stu-id="7ecf3-232">Entry</span></span> | <span data-ttu-id="7ecf3-233">值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7ecf3-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ecf3-234">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ecf3-235">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ecf3-236">System-Only</span></span>            | <span data-ttu-id="7ecf3-237">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-237">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-238">Is-Single-Valued</span></span>       | <span data-ttu-id="7ecf3-239">對</span><span class="sxs-lookup"><span data-stu-id="7ecf3-239">True</span></span>                                                                    |
| <span data-ttu-id="7ecf3-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ecf3-240">Is Indexed</span></span>             | <span data-ttu-id="7ecf3-241">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-241">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ecf3-242">In Global Catalog</span></span>      | <span data-ttu-id="7ecf3-243">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-243">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ecf3-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ecf3-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ecf3-245">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7ecf3-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ecf3-246">Range-Lower</span></span>            | <span data-ttu-id="7ecf3-247">1</span><span class="sxs-lookup"><span data-stu-id="7ecf3-247">1</span></span>                                                                       |
| <span data-ttu-id="7ecf3-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ecf3-248">Range-Upper</span></span>            | <span data-ttu-id="7ecf3-249">256</span><span class="sxs-lookup"><span data-stu-id="7ecf3-249">256</span></span>                                                                     |
| <span data-ttu-id="7ecf3-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-250">Search-Flags</span></span>           | <span data-ttu-id="7ecf3-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ecf3-251">0x00000000</span></span>                                                              |
| <span data-ttu-id="7ecf3-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-252">System-Flags</span></span>           | <span data-ttu-id="7ecf3-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ecf3-253">0x00000010</span></span>                                                              |
| <span data-ttu-id="7ecf3-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ecf3-254">Classes used in</span></span>        | [<span data-ttu-id="7ecf3-255">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-255">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ecf3-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ecf3-256">Windows Server 2012</span></span>



| <span data-ttu-id="7ecf3-257">進入</span><span class="sxs-lookup"><span data-stu-id="7ecf3-257">Entry</span></span> | <span data-ttu-id="7ecf3-258">值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7ecf3-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ecf3-259">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ecf3-260">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7ecf3-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ecf3-261">System-Only</span></span>            | <span data-ttu-id="7ecf3-262">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-262">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ecf3-263">Is-Single-Valued</span></span>       | <span data-ttu-id="7ecf3-264">對</span><span class="sxs-lookup"><span data-stu-id="7ecf3-264">True</span></span>                                                                    |
| <span data-ttu-id="7ecf3-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ecf3-265">Is Indexed</span></span>             | <span data-ttu-id="7ecf3-266">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-266">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ecf3-267">In Global Catalog</span></span>      | <span data-ttu-id="7ecf3-268">否</span><span class="sxs-lookup"><span data-stu-id="7ecf3-268">False</span></span>                                                                   |
| <span data-ttu-id="7ecf3-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ecf3-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ecf3-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ecf3-270">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7ecf3-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ecf3-271">Range-Lower</span></span>            | <span data-ttu-id="7ecf3-272">1</span><span class="sxs-lookup"><span data-stu-id="7ecf3-272">1</span></span>                                                                       |
| <span data-ttu-id="7ecf3-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ecf3-273">Range-Upper</span></span>            | <span data-ttu-id="7ecf3-274">256</span><span class="sxs-lookup"><span data-stu-id="7ecf3-274">256</span></span>                                                                     |
| <span data-ttu-id="7ecf3-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-275">Search-Flags</span></span>           | <span data-ttu-id="7ecf3-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ecf3-276">0x00000000</span></span>                                                              |
| <span data-ttu-id="7ecf3-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ecf3-277">System-Flags</span></span>           | <span data-ttu-id="7ecf3-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ecf3-278">0x00000010</span></span>                                                              |
| <span data-ttu-id="7ecf3-279">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ecf3-279">Classes used in</span></span>        | [<span data-ttu-id="7ecf3-280">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7ecf3-280">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



 

 






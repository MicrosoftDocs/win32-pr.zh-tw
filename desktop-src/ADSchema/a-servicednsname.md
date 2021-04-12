---
title: 服務-DNS-名稱屬性
description: 要查詢以尋找執行此服務之伺服器的 DNS 名稱。
ms.assetid: b2852276-30f5-4c2a-9f72-9df0d7c0c994
ms.tgt_platform: multiple
keywords:
- 服務-DNS-名稱屬性 AD 架構
- serviceDNSName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Service-DNS-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b881587a1358a6e7a3a814efb80af122ac5669
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509662"
---
# <a name="service-dns-name-attribute"></a><span data-ttu-id="7c32f-105">服務-DNS-名稱屬性</span><span class="sxs-lookup"><span data-stu-id="7c32f-105">Service-DNS-Name attribute</span></span>

<span data-ttu-id="7c32f-106">要查詢以尋找執行此服務之伺服器的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="7c32f-106">The DNS name to look up to find a server running this service.</span></span>



| <span data-ttu-id="7c32f-107">進入</span><span class="sxs-lookup"><span data-stu-id="7c32f-107">Entry</span></span> | <span data-ttu-id="7c32f-108">值</span><span class="sxs-lookup"><span data-stu-id="7c32f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7c32f-109">CN</span><span class="sxs-lookup"><span data-stu-id="7c32f-109">CN</span></span>                | <span data-ttu-id="7c32f-110">服務-DNS-名稱</span><span class="sxs-lookup"><span data-stu-id="7c32f-110">Service-DNS-Name</span></span>                            |
| <span data-ttu-id="7c32f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7c32f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7c32f-112">serviceDNSName</span><span class="sxs-lookup"><span data-stu-id="7c32f-112">serviceDNSName</span></span>                              |
| <span data-ttu-id="7c32f-113">大小</span><span class="sxs-lookup"><span data-stu-id="7c32f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="7c32f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7c32f-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="7c32f-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7c32f-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="7c32f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7c32f-116">Attribute-Id</span></span>      | <span data-ttu-id="7c32f-117">1.2.840.113556.1.4.657</span><span class="sxs-lookup"><span data-stu-id="7c32f-117">1.2.840.113556.1.4.657</span></span>                      |
| <span data-ttu-id="7c32f-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7c32f-118">System-Id-Guid</span></span>    | <span data-ttu-id="7c32f-119">28630eb8-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7c32f-119">28630eb8-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="7c32f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c32f-120">Syntax</span></span>            | [<span data-ttu-id="7c32f-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7c32f-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7c32f-122">實作</span><span class="sxs-lookup"><span data-stu-id="7c32f-122">Implementations</span></span>

-   [<span data-ttu-id="7c32f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7c32f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7c32f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7c32f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7c32f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7c32f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7c32f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7c32f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7c32f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7c32f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7c32f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7c32f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7c32f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c32f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="7c32f-130">進入</span><span class="sxs-lookup"><span data-stu-id="7c32f-130">Entry</span></span> | <span data-ttu-id="7c32f-131">值</span><span class="sxs-lookup"><span data-stu-id="7c32f-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c32f-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7c32f-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c32f-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c32f-134">System-Only</span></span>            | <span data-ttu-id="7c32f-135">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-135">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7c32f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="7c32f-137">對</span><span class="sxs-lookup"><span data-stu-id="7c32f-137">True</span></span>                                                                    |
| <span data-ttu-id="7c32f-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7c32f-138">Is Indexed</span></span>             | <span data-ttu-id="7c32f-139">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-139">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7c32f-140">In Global Catalog</span></span>      | <span data-ttu-id="7c32f-141">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-141">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7c32f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c32f-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7c32f-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c32f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c32f-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c32f-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-146">Search-Flags</span></span>           | <span data-ttu-id="7c32f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c32f-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c32f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-148">System-Flags</span></span>           | <span data-ttu-id="7c32f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c32f-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c32f-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7c32f-150">Classes used in</span></span>        | [<span data-ttu-id="7c32f-151">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7c32f-151">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7c32f-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c32f-152">Windows Server 2003</span></span>



| <span data-ttu-id="7c32f-153">進入</span><span class="sxs-lookup"><span data-stu-id="7c32f-153">Entry</span></span> | <span data-ttu-id="7c32f-154">值</span><span class="sxs-lookup"><span data-stu-id="7c32f-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c32f-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7c32f-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c32f-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c32f-157">System-Only</span></span>            | <span data-ttu-id="7c32f-158">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-158">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7c32f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="7c32f-160">對</span><span class="sxs-lookup"><span data-stu-id="7c32f-160">True</span></span>                                                                    |
| <span data-ttu-id="7c32f-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7c32f-161">Is Indexed</span></span>             | <span data-ttu-id="7c32f-162">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-162">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7c32f-163">In Global Catalog</span></span>      | <span data-ttu-id="7c32f-164">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-164">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7c32f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c32f-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7c32f-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c32f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c32f-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c32f-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-169">Search-Flags</span></span>           | <span data-ttu-id="7c32f-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c32f-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c32f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-171">System-Flags</span></span>           | <span data-ttu-id="7c32f-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c32f-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c32f-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7c32f-173">Classes used in</span></span>        | [<span data-ttu-id="7c32f-174">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7c32f-174">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7c32f-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7c32f-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7c32f-176">進入</span><span class="sxs-lookup"><span data-stu-id="7c32f-176">Entry</span></span> | <span data-ttu-id="7c32f-177">值</span><span class="sxs-lookup"><span data-stu-id="7c32f-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c32f-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7c32f-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c32f-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c32f-180">System-Only</span></span>            | <span data-ttu-id="7c32f-181">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-181">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7c32f-182">Is-Single-Valued</span></span>       | <span data-ttu-id="7c32f-183">對</span><span class="sxs-lookup"><span data-stu-id="7c32f-183">True</span></span>                                                                    |
| <span data-ttu-id="7c32f-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7c32f-184">Is Indexed</span></span>             | <span data-ttu-id="7c32f-185">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-185">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7c32f-186">In Global Catalog</span></span>      | <span data-ttu-id="7c32f-187">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-187">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7c32f-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c32f-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7c32f-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c32f-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c32f-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c32f-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-192">Search-Flags</span></span>           | <span data-ttu-id="7c32f-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c32f-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c32f-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-194">System-Flags</span></span>           | <span data-ttu-id="7c32f-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c32f-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c32f-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7c32f-196">Classes used in</span></span>        | [<span data-ttu-id="7c32f-197">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7c32f-197">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7c32f-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c32f-198">Windows Server 2008</span></span>



| <span data-ttu-id="7c32f-199">進入</span><span class="sxs-lookup"><span data-stu-id="7c32f-199">Entry</span></span> | <span data-ttu-id="7c32f-200">值</span><span class="sxs-lookup"><span data-stu-id="7c32f-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c32f-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7c32f-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c32f-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c32f-203">System-Only</span></span>            | <span data-ttu-id="7c32f-204">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-204">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7c32f-205">Is-Single-Valued</span></span>       | <span data-ttu-id="7c32f-206">對</span><span class="sxs-lookup"><span data-stu-id="7c32f-206">True</span></span>                                                                    |
| <span data-ttu-id="7c32f-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7c32f-207">Is Indexed</span></span>             | <span data-ttu-id="7c32f-208">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-208">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7c32f-209">In Global Catalog</span></span>      | <span data-ttu-id="7c32f-210">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-210">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7c32f-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c32f-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7c32f-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c32f-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c32f-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c32f-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-215">Search-Flags</span></span>           | <span data-ttu-id="7c32f-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c32f-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c32f-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-217">System-Flags</span></span>           | <span data-ttu-id="7c32f-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c32f-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c32f-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7c32f-219">Classes used in</span></span>        | [<span data-ttu-id="7c32f-220">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7c32f-220">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7c32f-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c32f-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7c32f-222">進入</span><span class="sxs-lookup"><span data-stu-id="7c32f-222">Entry</span></span> | <span data-ttu-id="7c32f-223">值</span><span class="sxs-lookup"><span data-stu-id="7c32f-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c32f-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7c32f-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c32f-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c32f-226">System-Only</span></span>            | <span data-ttu-id="7c32f-227">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-227">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7c32f-228">Is-Single-Valued</span></span>       | <span data-ttu-id="7c32f-229">對</span><span class="sxs-lookup"><span data-stu-id="7c32f-229">True</span></span>                                                                    |
| <span data-ttu-id="7c32f-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7c32f-230">Is Indexed</span></span>             | <span data-ttu-id="7c32f-231">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-231">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7c32f-232">In Global Catalog</span></span>      | <span data-ttu-id="7c32f-233">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-233">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7c32f-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c32f-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7c32f-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c32f-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c32f-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c32f-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-238">Search-Flags</span></span>           | <span data-ttu-id="7c32f-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c32f-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c32f-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-240">System-Flags</span></span>           | <span data-ttu-id="7c32f-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c32f-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c32f-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7c32f-242">Classes used in</span></span>        | [<span data-ttu-id="7c32f-243">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7c32f-243">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7c32f-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c32f-244">Windows Server 2012</span></span>



| <span data-ttu-id="7c32f-245">進入</span><span class="sxs-lookup"><span data-stu-id="7c32f-245">Entry</span></span> | <span data-ttu-id="7c32f-246">值</span><span class="sxs-lookup"><span data-stu-id="7c32f-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c32f-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7c32f-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c32f-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c32f-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c32f-249">System-Only</span></span>            | <span data-ttu-id="7c32f-250">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-250">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7c32f-251">Is-Single-Valued</span></span>       | <span data-ttu-id="7c32f-252">對</span><span class="sxs-lookup"><span data-stu-id="7c32f-252">True</span></span>                                                                    |
| <span data-ttu-id="7c32f-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7c32f-253">Is Indexed</span></span>             | <span data-ttu-id="7c32f-254">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-254">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7c32f-255">In Global Catalog</span></span>      | <span data-ttu-id="7c32f-256">否</span><span class="sxs-lookup"><span data-stu-id="7c32f-256">False</span></span>                                                                   |
| <span data-ttu-id="7c32f-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7c32f-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c32f-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7c32f-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c32f-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c32f-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c32f-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c32f-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-261">Search-Flags</span></span>           | <span data-ttu-id="7c32f-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c32f-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c32f-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c32f-263">System-Flags</span></span>           | <span data-ttu-id="7c32f-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c32f-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c32f-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7c32f-265">Classes used in</span></span>        | [<span data-ttu-id="7c32f-266">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="7c32f-266">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



 

 






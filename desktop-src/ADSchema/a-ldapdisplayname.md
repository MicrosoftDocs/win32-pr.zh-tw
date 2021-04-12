---
title: LDAP-顯示名稱屬性
description: LDAP 用戶端所使用的名稱，例如 ADSI LDAP 提供者，使用 LDAP 通訊協定來讀取和寫入屬性。
ms.assetid: 9cb0b2f0-16cf-4fc6-85b2-d21ff71bc477
ms.tgt_platform: multiple
keywords:
- LDAP-顯示名稱屬性 AD 架構
- lDAPDisplayName 屬性 AD 架構
topic_type:
- apiref
api_name:
- LDAP-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ffa25777ec4b5139a41ba9e56d8d5f0a9a3d92
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104187330"
---
# <a name="ldap-display-name-attribute"></a><span data-ttu-id="14d8f-105">LDAP-顯示名稱屬性</span><span class="sxs-lookup"><span data-stu-id="14d8f-105">LDAP-Display-Name attribute</span></span>

<span data-ttu-id="14d8f-106">LDAP 用戶端所使用的名稱，例如 ADSI LDAP 提供者，使用 LDAP 通訊協定來讀取和寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="14d8f-106">The name used by LDAP clients, such as the ADSI LDAP provider, to read and write the attribute by using the LDAP protocol.</span></span>



| <span data-ttu-id="14d8f-107">進入</span><span class="sxs-lookup"><span data-stu-id="14d8f-107">Entry</span></span> | <span data-ttu-id="14d8f-108">值</span><span class="sxs-lookup"><span data-stu-id="14d8f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="14d8f-109">CN</span><span class="sxs-lookup"><span data-stu-id="14d8f-109">CN</span></span>                | <span data-ttu-id="14d8f-110">LDAP-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="14d8f-110">LDAP-Display-Name</span></span>                           |
| <span data-ttu-id="14d8f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="14d8f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="14d8f-112">lDAPDisplayName</span><span class="sxs-lookup"><span data-stu-id="14d8f-112">lDAPDisplayName</span></span>                             |
| <span data-ttu-id="14d8f-113">大小</span><span class="sxs-lookup"><span data-stu-id="14d8f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="14d8f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="14d8f-114">Update Privilege</span></span>  | <span data-ttu-id="14d8f-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="14d8f-115">Schema administrator</span></span>                        |
| <span data-ttu-id="14d8f-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="14d8f-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="14d8f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="14d8f-117">Attribute-Id</span></span>      | <span data-ttu-id="14d8f-118">1.2.840.113556.1.2.460</span><span class="sxs-lookup"><span data-stu-id="14d8f-118">1.2.840.113556.1.2.460</span></span>                      |
| <span data-ttu-id="14d8f-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="14d8f-119">System-Id-Guid</span></span>    | <span data-ttu-id="14d8f-120">bf96799a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="14d8f-120">bf96799a-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="14d8f-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="14d8f-121">Syntax</span></span>            | [<span data-ttu-id="14d8f-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="14d8f-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="14d8f-123">實作</span><span class="sxs-lookup"><span data-stu-id="14d8f-123">Implementations</span></span>

-   [<span data-ttu-id="14d8f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="14d8f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="14d8f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="14d8f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="14d8f-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="14d8f-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="14d8f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="14d8f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="14d8f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="14d8f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="14d8f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14d8f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="14d8f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="14d8f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="14d8f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14d8f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="14d8f-132">進入</span><span class="sxs-lookup"><span data-stu-id="14d8f-132">Entry</span></span> | <span data-ttu-id="14d8f-133">值</span><span class="sxs-lookup"><span data-stu-id="14d8f-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d8f-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14d8f-134">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="14d8f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14d8f-135">MAPI-Id</span></span>                | <span data-ttu-id="14d8f-136">0x8171</span><span class="sxs-lookup"><span data-stu-id="14d8f-136">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="14d8f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="14d8f-137">System-Only</span></span>            | <span data-ttu-id="14d8f-138">否</span><span class="sxs-lookup"><span data-stu-id="14d8f-138">False</span></span>                                                                                                     |
| <span data-ttu-id="14d8f-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14d8f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="14d8f-140">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-140">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14d8f-141">Is Indexed</span></span>             | <span data-ttu-id="14d8f-142">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-142">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14d8f-143">In Global Catalog</span></span>      | <span data-ttu-id="14d8f-144">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-144">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14d8f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="14d8f-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14d8f-146">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="14d8f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14d8f-147">Range-Lower</span></span>            | <span data-ttu-id="14d8f-148">1</span><span class="sxs-lookup"><span data-stu-id="14d8f-148">1</span></span>                                                                                                         |
| <span data-ttu-id="14d8f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14d8f-149">Range-Upper</span></span>            | <span data-ttu-id="14d8f-150">256</span><span class="sxs-lookup"><span data-stu-id="14d8f-150">256</span></span>                                                                                                       |
| <span data-ttu-id="14d8f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-151">Search-Flags</span></span>           | <span data-ttu-id="14d8f-152">0x00000009</span><span class="sxs-lookup"><span data-stu-id="14d8f-152">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="14d8f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-153">System-Flags</span></span>           | <span data-ttu-id="14d8f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14d8f-154">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="14d8f-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14d8f-155">Classes used in</span></span>        | [<span data-ttu-id="14d8f-156">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="14d8f-157">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-157">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="14d8f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14d8f-158">Windows Server 2003</span></span>



| <span data-ttu-id="14d8f-159">進入</span><span class="sxs-lookup"><span data-stu-id="14d8f-159">Entry</span></span> | <span data-ttu-id="14d8f-160">值</span><span class="sxs-lookup"><span data-stu-id="14d8f-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d8f-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14d8f-161">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="14d8f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14d8f-162">MAPI-Id</span></span>                | <span data-ttu-id="14d8f-163">0x8171</span><span class="sxs-lookup"><span data-stu-id="14d8f-163">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="14d8f-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="14d8f-164">System-Only</span></span>            | <span data-ttu-id="14d8f-165">否</span><span class="sxs-lookup"><span data-stu-id="14d8f-165">False</span></span>                                                                                                     |
| <span data-ttu-id="14d8f-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14d8f-166">Is-Single-Valued</span></span>       | <span data-ttu-id="14d8f-167">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-167">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14d8f-168">Is Indexed</span></span>             | <span data-ttu-id="14d8f-169">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-169">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14d8f-170">In Global Catalog</span></span>      | <span data-ttu-id="14d8f-171">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-171">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14d8f-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="14d8f-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14d8f-173">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="14d8f-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14d8f-174">Range-Lower</span></span>            | <span data-ttu-id="14d8f-175">1</span><span class="sxs-lookup"><span data-stu-id="14d8f-175">1</span></span>                                                                                                         |
| <span data-ttu-id="14d8f-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14d8f-176">Range-Upper</span></span>            | <span data-ttu-id="14d8f-177">256</span><span class="sxs-lookup"><span data-stu-id="14d8f-177">256</span></span>                                                                                                       |
| <span data-ttu-id="14d8f-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-178">Search-Flags</span></span>           | <span data-ttu-id="14d8f-179">0x00000009</span><span class="sxs-lookup"><span data-stu-id="14d8f-179">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="14d8f-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-180">System-Flags</span></span>           | <span data-ttu-id="14d8f-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14d8f-181">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="14d8f-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14d8f-182">Classes used in</span></span>        | [<span data-ttu-id="14d8f-183">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-183">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="14d8f-184">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-184">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="14d8f-185">亞當</span><span class="sxs-lookup"><span data-stu-id="14d8f-185">ADAM</span></span>



| <span data-ttu-id="14d8f-186">進入</span><span class="sxs-lookup"><span data-stu-id="14d8f-186">Entry</span></span> | <span data-ttu-id="14d8f-187">值</span><span class="sxs-lookup"><span data-stu-id="14d8f-187">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d8f-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14d8f-188">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="14d8f-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14d8f-189">MAPI-Id</span></span>                | <span data-ttu-id="14d8f-190">0x8171</span><span class="sxs-lookup"><span data-stu-id="14d8f-190">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="14d8f-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="14d8f-191">System-Only</span></span>            | <span data-ttu-id="14d8f-192">否</span><span class="sxs-lookup"><span data-stu-id="14d8f-192">False</span></span>                                                                                                     |
| <span data-ttu-id="14d8f-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14d8f-193">Is-Single-Valued</span></span>       | <span data-ttu-id="14d8f-194">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-194">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14d8f-195">Is Indexed</span></span>             | <span data-ttu-id="14d8f-196">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-196">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14d8f-197">In Global Catalog</span></span>      | <span data-ttu-id="14d8f-198">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-198">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14d8f-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="14d8f-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14d8f-200">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="14d8f-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14d8f-201">Range-Lower</span></span>            | <span data-ttu-id="14d8f-202">1</span><span class="sxs-lookup"><span data-stu-id="14d8f-202">1</span></span>                                                                                                         |
| <span data-ttu-id="14d8f-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14d8f-203">Range-Upper</span></span>            | <span data-ttu-id="14d8f-204">256</span><span class="sxs-lookup"><span data-stu-id="14d8f-204">256</span></span>                                                                                                       |
| <span data-ttu-id="14d8f-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-205">Search-Flags</span></span>           | <span data-ttu-id="14d8f-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="14d8f-206">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="14d8f-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-207">System-Flags</span></span>           | <span data-ttu-id="14d8f-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14d8f-208">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="14d8f-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14d8f-209">Classes used in</span></span>        | [<span data-ttu-id="14d8f-210">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-210">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="14d8f-211">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-211">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="14d8f-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="14d8f-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="14d8f-213">進入</span><span class="sxs-lookup"><span data-stu-id="14d8f-213">Entry</span></span> | <span data-ttu-id="14d8f-214">值</span><span class="sxs-lookup"><span data-stu-id="14d8f-214">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d8f-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14d8f-215">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="14d8f-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14d8f-216">MAPI-Id</span></span>                | <span data-ttu-id="14d8f-217">0x8171</span><span class="sxs-lookup"><span data-stu-id="14d8f-217">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="14d8f-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="14d8f-218">System-Only</span></span>            | <span data-ttu-id="14d8f-219">否</span><span class="sxs-lookup"><span data-stu-id="14d8f-219">False</span></span>                                                                                                     |
| <span data-ttu-id="14d8f-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14d8f-220">Is-Single-Valued</span></span>       | <span data-ttu-id="14d8f-221">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-221">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14d8f-222">Is Indexed</span></span>             | <span data-ttu-id="14d8f-223">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-223">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14d8f-224">In Global Catalog</span></span>      | <span data-ttu-id="14d8f-225">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-225">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14d8f-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="14d8f-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14d8f-227">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="14d8f-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14d8f-228">Range-Lower</span></span>            | <span data-ttu-id="14d8f-229">1</span><span class="sxs-lookup"><span data-stu-id="14d8f-229">1</span></span>                                                                                                         |
| <span data-ttu-id="14d8f-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14d8f-230">Range-Upper</span></span>            | <span data-ttu-id="14d8f-231">256</span><span class="sxs-lookup"><span data-stu-id="14d8f-231">256</span></span>                                                                                                       |
| <span data-ttu-id="14d8f-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-232">Search-Flags</span></span>           | <span data-ttu-id="14d8f-233">0x00000009</span><span class="sxs-lookup"><span data-stu-id="14d8f-233">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="14d8f-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-234">System-Flags</span></span>           | <span data-ttu-id="14d8f-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14d8f-235">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="14d8f-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14d8f-236">Classes used in</span></span>        | [<span data-ttu-id="14d8f-237">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-237">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="14d8f-238">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="14d8f-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14d8f-239">Windows Server 2008</span></span>



| <span data-ttu-id="14d8f-240">進入</span><span class="sxs-lookup"><span data-stu-id="14d8f-240">Entry</span></span> | <span data-ttu-id="14d8f-241">值</span><span class="sxs-lookup"><span data-stu-id="14d8f-241">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d8f-242">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14d8f-242">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="14d8f-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14d8f-243">MAPI-Id</span></span>                | <span data-ttu-id="14d8f-244">0x8171</span><span class="sxs-lookup"><span data-stu-id="14d8f-244">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="14d8f-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="14d8f-245">System-Only</span></span>            | <span data-ttu-id="14d8f-246">否</span><span class="sxs-lookup"><span data-stu-id="14d8f-246">False</span></span>                                                                                                     |
| <span data-ttu-id="14d8f-247">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14d8f-247">Is-Single-Valued</span></span>       | <span data-ttu-id="14d8f-248">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-248">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-249">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14d8f-249">Is Indexed</span></span>             | <span data-ttu-id="14d8f-250">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-250">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-251">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14d8f-251">In Global Catalog</span></span>      | <span data-ttu-id="14d8f-252">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-252">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-253">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14d8f-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="14d8f-254">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14d8f-254">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="14d8f-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14d8f-255">Range-Lower</span></span>            | <span data-ttu-id="14d8f-256">1</span><span class="sxs-lookup"><span data-stu-id="14d8f-256">1</span></span>                                                                                                         |
| <span data-ttu-id="14d8f-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14d8f-257">Range-Upper</span></span>            | <span data-ttu-id="14d8f-258">256</span><span class="sxs-lookup"><span data-stu-id="14d8f-258">256</span></span>                                                                                                       |
| <span data-ttu-id="14d8f-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-259">Search-Flags</span></span>           | <span data-ttu-id="14d8f-260">0x00000009</span><span class="sxs-lookup"><span data-stu-id="14d8f-260">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="14d8f-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-261">System-Flags</span></span>           | <span data-ttu-id="14d8f-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14d8f-262">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="14d8f-263">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14d8f-263">Classes used in</span></span>        | [<span data-ttu-id="14d8f-264">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-264">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="14d8f-265">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-265">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="14d8f-266">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14d8f-266">Windows Server 2008 R2</span></span>



| <span data-ttu-id="14d8f-267">進入</span><span class="sxs-lookup"><span data-stu-id="14d8f-267">Entry</span></span> | <span data-ttu-id="14d8f-268">值</span><span class="sxs-lookup"><span data-stu-id="14d8f-268">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d8f-269">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14d8f-269">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="14d8f-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14d8f-270">MAPI-Id</span></span>                | <span data-ttu-id="14d8f-271">0x8171</span><span class="sxs-lookup"><span data-stu-id="14d8f-271">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="14d8f-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="14d8f-272">System-Only</span></span>            | <span data-ttu-id="14d8f-273">否</span><span class="sxs-lookup"><span data-stu-id="14d8f-273">False</span></span>                                                                                                     |
| <span data-ttu-id="14d8f-274">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14d8f-274">Is-Single-Valued</span></span>       | <span data-ttu-id="14d8f-275">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-275">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-276">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14d8f-276">Is Indexed</span></span>             | <span data-ttu-id="14d8f-277">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-277">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-278">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14d8f-278">In Global Catalog</span></span>      | <span data-ttu-id="14d8f-279">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-279">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-280">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14d8f-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="14d8f-281">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14d8f-281">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="14d8f-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14d8f-282">Range-Lower</span></span>            | <span data-ttu-id="14d8f-283">1</span><span class="sxs-lookup"><span data-stu-id="14d8f-283">1</span></span>                                                                                                         |
| <span data-ttu-id="14d8f-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14d8f-284">Range-Upper</span></span>            | <span data-ttu-id="14d8f-285">256</span><span class="sxs-lookup"><span data-stu-id="14d8f-285">256</span></span>                                                                                                       |
| <span data-ttu-id="14d8f-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-286">Search-Flags</span></span>           | <span data-ttu-id="14d8f-287">0x00000009</span><span class="sxs-lookup"><span data-stu-id="14d8f-287">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="14d8f-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-288">System-Flags</span></span>           | <span data-ttu-id="14d8f-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14d8f-289">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="14d8f-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14d8f-290">Classes used in</span></span>        | [<span data-ttu-id="14d8f-291">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="14d8f-292">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="14d8f-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14d8f-293">Windows Server 2012</span></span>



| <span data-ttu-id="14d8f-294">進入</span><span class="sxs-lookup"><span data-stu-id="14d8f-294">Entry</span></span> | <span data-ttu-id="14d8f-295">值</span><span class="sxs-lookup"><span data-stu-id="14d8f-295">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d8f-296">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14d8f-296">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="14d8f-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14d8f-297">MAPI-Id</span></span>                | <span data-ttu-id="14d8f-298">0x8171</span><span class="sxs-lookup"><span data-stu-id="14d8f-298">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="14d8f-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="14d8f-299">System-Only</span></span>            | <span data-ttu-id="14d8f-300">否</span><span class="sxs-lookup"><span data-stu-id="14d8f-300">False</span></span>                                                                                                     |
| <span data-ttu-id="14d8f-301">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14d8f-301">Is-Single-Valued</span></span>       | <span data-ttu-id="14d8f-302">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-302">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-303">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14d8f-303">Is Indexed</span></span>             | <span data-ttu-id="14d8f-304">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-304">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-305">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14d8f-305">In Global Catalog</span></span>      | <span data-ttu-id="14d8f-306">對</span><span class="sxs-lookup"><span data-stu-id="14d8f-306">True</span></span>                                                                                                      |
| <span data-ttu-id="14d8f-307">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14d8f-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="14d8f-308">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14d8f-308">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="14d8f-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14d8f-309">Range-Lower</span></span>            | <span data-ttu-id="14d8f-310">1</span><span class="sxs-lookup"><span data-stu-id="14d8f-310">1</span></span>                                                                                                         |
| <span data-ttu-id="14d8f-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14d8f-311">Range-Upper</span></span>            | <span data-ttu-id="14d8f-312">256</span><span class="sxs-lookup"><span data-stu-id="14d8f-312">256</span></span>                                                                                                       |
| <span data-ttu-id="14d8f-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-313">Search-Flags</span></span>           | <span data-ttu-id="14d8f-314">0x00000009</span><span class="sxs-lookup"><span data-stu-id="14d8f-314">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="14d8f-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14d8f-315">System-Flags</span></span>           | <span data-ttu-id="14d8f-316">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14d8f-316">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="14d8f-317">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14d8f-317">Classes used in</span></span>        | [<span data-ttu-id="14d8f-318">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-318">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="14d8f-319">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="14d8f-319">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 






---
title: Dns-Root 屬性
description: 指派給網域/目錄分割的最上層 DNS 功能變數名稱。
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Dns-Root 屬性 AD 架構
- dnsRoot 屬性 AD 架構
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106968812"
---
# <a name="dns-root-attribute"></a><span data-ttu-id="37802-105">Dns-Root 屬性</span><span class="sxs-lookup"><span data-stu-id="37802-105">Dns-Root attribute</span></span>

<span data-ttu-id="37802-106">指派給網域/目錄分割的最上層 DNS 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="37802-106">The uppermost DNS domain name assigned to a domain/directory partition.</span></span> <span data-ttu-id="37802-107">這是在交叉參考物件上設定的，並且用於參考產生的其他專案。</span><span class="sxs-lookup"><span data-stu-id="37802-107">This is set on a crossRef object and is used, among other things, for referral generation.</span></span> <span data-ttu-id="37802-108">搜尋整個網域樹狀結構時，必須在 Dns-Root 物件起始搜尋。</span><span class="sxs-lookup"><span data-stu-id="37802-108">When searching through an entire domain tree, the search must be initiated at the Dns-Root object.</span></span> <span data-ttu-id="37802-109">這個屬性可以是多重值，在這種情況下，會產生多個參考。</span><span class="sxs-lookup"><span data-stu-id="37802-109">This attribute can be multi-valued, in which case multiple referrals are generated.</span></span>



| <span data-ttu-id="37802-110">進入</span><span class="sxs-lookup"><span data-stu-id="37802-110">Entry</span></span> | <span data-ttu-id="37802-111">值</span><span class="sxs-lookup"><span data-stu-id="37802-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="37802-112">CN</span><span class="sxs-lookup"><span data-stu-id="37802-112">CN</span></span>                | <span data-ttu-id="37802-113">Dns-Root</span><span class="sxs-lookup"><span data-stu-id="37802-113">Dns-Root</span></span>                                    |
| <span data-ttu-id="37802-114">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="37802-114">Ldap-Display-Name</span></span> | <span data-ttu-id="37802-115">dnsRoot</span><span class="sxs-lookup"><span data-stu-id="37802-115">dnsRoot</span></span>                                     |
| <span data-ttu-id="37802-116">大小</span><span class="sxs-lookup"><span data-stu-id="37802-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="37802-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="37802-117">Update Privilege</span></span>  | <span data-ttu-id="37802-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="37802-118">This value is set by the system.</span></span>            |
| <span data-ttu-id="37802-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="37802-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="37802-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37802-120">Attribute-Id</span></span>      | <span data-ttu-id="37802-121">1.2.840.113556.1.4.28</span><span class="sxs-lookup"><span data-stu-id="37802-121">1.2.840.113556.1.4.28</span></span>                       |
| <span data-ttu-id="37802-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="37802-122">System-Id-Guid</span></span>    | <span data-ttu-id="37802-123">bf967959-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="37802-123">bf967959-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="37802-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="37802-124">Syntax</span></span>            | [<span data-ttu-id="37802-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="37802-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="37802-126">實作</span><span class="sxs-lookup"><span data-stu-id="37802-126">Implementations</span></span>

-   [<span data-ttu-id="37802-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="37802-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="37802-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37802-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37802-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="37802-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="37802-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37802-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37802-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37802-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37802-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37802-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37802-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37802-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="37802-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37802-134">Windows 2000 Server</span></span>



| <span data-ttu-id="37802-135">進入</span><span class="sxs-lookup"><span data-stu-id="37802-135">Entry</span></span> | <span data-ttu-id="37802-136">值</span><span class="sxs-lookup"><span data-stu-id="37802-136">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="37802-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37802-137">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37802-138">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="37802-139">System-Only</span></span>            | <span data-ttu-id="37802-140">否</span><span class="sxs-lookup"><span data-stu-id="37802-140">False</span></span>                                      |
| <span data-ttu-id="37802-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37802-141">Is-Single-Valued</span></span>       | <span data-ttu-id="37802-142">否</span><span class="sxs-lookup"><span data-stu-id="37802-142">False</span></span>                                      |
| <span data-ttu-id="37802-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37802-143">Is Indexed</span></span>             | <span data-ttu-id="37802-144">對</span><span class="sxs-lookup"><span data-stu-id="37802-144">True</span></span>                                       |
| <span data-ttu-id="37802-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37802-145">In Global Catalog</span></span>      | <span data-ttu-id="37802-146">否</span><span class="sxs-lookup"><span data-stu-id="37802-146">False</span></span>                                      |
| <span data-ttu-id="37802-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37802-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="37802-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37802-148">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="37802-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37802-149">Range-Lower</span></span>            | <span data-ttu-id="37802-150">1</span><span class="sxs-lookup"><span data-stu-id="37802-150">1</span></span>                                          |
| <span data-ttu-id="37802-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37802-151">Range-Upper</span></span>            | <span data-ttu-id="37802-152">255</span><span class="sxs-lookup"><span data-stu-id="37802-152">255</span></span>                                        |
| <span data-ttu-id="37802-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-153">Search-Flags</span></span>           | <span data-ttu-id="37802-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="37802-154">0x00000001</span></span>                                 |
| <span data-ttu-id="37802-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-155">System-Flags</span></span>           | <span data-ttu-id="37802-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37802-156">0x00000010</span></span>                                 |
| <span data-ttu-id="37802-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37802-157">Classes used in</span></span>        | [<span data-ttu-id="37802-158">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="37802-158">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="37802-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37802-159">Windows Server 2003</span></span>



| <span data-ttu-id="37802-160">進入</span><span class="sxs-lookup"><span data-stu-id="37802-160">Entry</span></span> | <span data-ttu-id="37802-161">值</span><span class="sxs-lookup"><span data-stu-id="37802-161">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="37802-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37802-162">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37802-163">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="37802-164">System-Only</span></span>            | <span data-ttu-id="37802-165">否</span><span class="sxs-lookup"><span data-stu-id="37802-165">False</span></span>                                      |
| <span data-ttu-id="37802-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37802-166">Is-Single-Valued</span></span>       | <span data-ttu-id="37802-167">否</span><span class="sxs-lookup"><span data-stu-id="37802-167">False</span></span>                                      |
| <span data-ttu-id="37802-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37802-168">Is Indexed</span></span>             | <span data-ttu-id="37802-169">對</span><span class="sxs-lookup"><span data-stu-id="37802-169">True</span></span>                                       |
| <span data-ttu-id="37802-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37802-170">In Global Catalog</span></span>      | <span data-ttu-id="37802-171">否</span><span class="sxs-lookup"><span data-stu-id="37802-171">False</span></span>                                      |
| <span data-ttu-id="37802-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37802-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="37802-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37802-173">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="37802-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37802-174">Range-Lower</span></span>            | <span data-ttu-id="37802-175">1</span><span class="sxs-lookup"><span data-stu-id="37802-175">1</span></span>                                          |
| <span data-ttu-id="37802-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37802-176">Range-Upper</span></span>            | <span data-ttu-id="37802-177">255</span><span class="sxs-lookup"><span data-stu-id="37802-177">255</span></span>                                        |
| <span data-ttu-id="37802-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-178">Search-Flags</span></span>           | <span data-ttu-id="37802-179">0x00000001</span><span class="sxs-lookup"><span data-stu-id="37802-179">0x00000001</span></span>                                 |
| <span data-ttu-id="37802-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-180">System-Flags</span></span>           | <span data-ttu-id="37802-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37802-181">0x00000010</span></span>                                 |
| <span data-ttu-id="37802-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37802-182">Classes used in</span></span>        | [<span data-ttu-id="37802-183">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="37802-183">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="37802-184">亞當</span><span class="sxs-lookup"><span data-stu-id="37802-184">ADAM</span></span>



| <span data-ttu-id="37802-185">進入</span><span class="sxs-lookup"><span data-stu-id="37802-185">Entry</span></span> | <span data-ttu-id="37802-186">值</span><span class="sxs-lookup"><span data-stu-id="37802-186">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="37802-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37802-187">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37802-188">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="37802-189">System-Only</span></span>            | <span data-ttu-id="37802-190">否</span><span class="sxs-lookup"><span data-stu-id="37802-190">False</span></span>                                      |
| <span data-ttu-id="37802-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37802-191">Is-Single-Valued</span></span>       | <span data-ttu-id="37802-192">否</span><span class="sxs-lookup"><span data-stu-id="37802-192">False</span></span>                                      |
| <span data-ttu-id="37802-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37802-193">Is Indexed</span></span>             | <span data-ttu-id="37802-194">對</span><span class="sxs-lookup"><span data-stu-id="37802-194">True</span></span>                                       |
| <span data-ttu-id="37802-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37802-195">In Global Catalog</span></span>      | <span data-ttu-id="37802-196">否</span><span class="sxs-lookup"><span data-stu-id="37802-196">False</span></span>                                      |
| <span data-ttu-id="37802-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37802-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="37802-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37802-198">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="37802-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37802-199">Range-Lower</span></span>            | <span data-ttu-id="37802-200">1</span><span class="sxs-lookup"><span data-stu-id="37802-200">1</span></span>                                          |
| <span data-ttu-id="37802-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37802-201">Range-Upper</span></span>            | <span data-ttu-id="37802-202">255</span><span class="sxs-lookup"><span data-stu-id="37802-202">255</span></span>                                        |
| <span data-ttu-id="37802-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-203">Search-Flags</span></span>           | <span data-ttu-id="37802-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="37802-204">0x00000001</span></span>                                 |
| <span data-ttu-id="37802-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-205">System-Flags</span></span>           | <span data-ttu-id="37802-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37802-206">0x00000010</span></span>                                 |
| <span data-ttu-id="37802-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37802-207">Classes used in</span></span>        | [<span data-ttu-id="37802-208">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="37802-208">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37802-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37802-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37802-210">進入</span><span class="sxs-lookup"><span data-stu-id="37802-210">Entry</span></span> | <span data-ttu-id="37802-211">值</span><span class="sxs-lookup"><span data-stu-id="37802-211">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="37802-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37802-212">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37802-213">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="37802-214">System-Only</span></span>            | <span data-ttu-id="37802-215">否</span><span class="sxs-lookup"><span data-stu-id="37802-215">False</span></span>                                      |
| <span data-ttu-id="37802-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37802-216">Is-Single-Valued</span></span>       | <span data-ttu-id="37802-217">否</span><span class="sxs-lookup"><span data-stu-id="37802-217">False</span></span>                                      |
| <span data-ttu-id="37802-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37802-218">Is Indexed</span></span>             | <span data-ttu-id="37802-219">對</span><span class="sxs-lookup"><span data-stu-id="37802-219">True</span></span>                                       |
| <span data-ttu-id="37802-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37802-220">In Global Catalog</span></span>      | <span data-ttu-id="37802-221">否</span><span class="sxs-lookup"><span data-stu-id="37802-221">False</span></span>                                      |
| <span data-ttu-id="37802-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37802-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="37802-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37802-223">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="37802-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37802-224">Range-Lower</span></span>            | <span data-ttu-id="37802-225">1</span><span class="sxs-lookup"><span data-stu-id="37802-225">1</span></span>                                          |
| <span data-ttu-id="37802-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37802-226">Range-Upper</span></span>            | <span data-ttu-id="37802-227">255</span><span class="sxs-lookup"><span data-stu-id="37802-227">255</span></span>                                        |
| <span data-ttu-id="37802-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-228">Search-Flags</span></span>           | <span data-ttu-id="37802-229">0x00000001</span><span class="sxs-lookup"><span data-stu-id="37802-229">0x00000001</span></span>                                 |
| <span data-ttu-id="37802-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-230">System-Flags</span></span>           | <span data-ttu-id="37802-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37802-231">0x00000010</span></span>                                 |
| <span data-ttu-id="37802-232">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37802-232">Classes used in</span></span>        | [<span data-ttu-id="37802-233">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="37802-233">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37802-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37802-234">Windows Server 2008</span></span>



| <span data-ttu-id="37802-235">進入</span><span class="sxs-lookup"><span data-stu-id="37802-235">Entry</span></span> | <span data-ttu-id="37802-236">值</span><span class="sxs-lookup"><span data-stu-id="37802-236">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="37802-237">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37802-237">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37802-238">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="37802-239">System-Only</span></span>            | <span data-ttu-id="37802-240">否</span><span class="sxs-lookup"><span data-stu-id="37802-240">False</span></span>                                      |
| <span data-ttu-id="37802-241">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37802-241">Is-Single-Valued</span></span>       | <span data-ttu-id="37802-242">否</span><span class="sxs-lookup"><span data-stu-id="37802-242">False</span></span>                                      |
| <span data-ttu-id="37802-243">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37802-243">Is Indexed</span></span>             | <span data-ttu-id="37802-244">對</span><span class="sxs-lookup"><span data-stu-id="37802-244">True</span></span>                                       |
| <span data-ttu-id="37802-245">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37802-245">In Global Catalog</span></span>      | <span data-ttu-id="37802-246">否</span><span class="sxs-lookup"><span data-stu-id="37802-246">False</span></span>                                      |
| <span data-ttu-id="37802-247">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37802-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="37802-248">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37802-248">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="37802-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37802-249">Range-Lower</span></span>            | <span data-ttu-id="37802-250">1</span><span class="sxs-lookup"><span data-stu-id="37802-250">1</span></span>                                          |
| <span data-ttu-id="37802-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37802-251">Range-Upper</span></span>            | <span data-ttu-id="37802-252">255</span><span class="sxs-lookup"><span data-stu-id="37802-252">255</span></span>                                        |
| <span data-ttu-id="37802-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-253">Search-Flags</span></span>           | <span data-ttu-id="37802-254">0x00000001</span><span class="sxs-lookup"><span data-stu-id="37802-254">0x00000001</span></span>                                 |
| <span data-ttu-id="37802-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-255">System-Flags</span></span>           | <span data-ttu-id="37802-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37802-256">0x00000010</span></span>                                 |
| <span data-ttu-id="37802-257">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37802-257">Classes used in</span></span>        | [<span data-ttu-id="37802-258">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="37802-258">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37802-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37802-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37802-260">進入</span><span class="sxs-lookup"><span data-stu-id="37802-260">Entry</span></span> | <span data-ttu-id="37802-261">值</span><span class="sxs-lookup"><span data-stu-id="37802-261">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="37802-262">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37802-262">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37802-263">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="37802-264">System-Only</span></span>            | <span data-ttu-id="37802-265">否</span><span class="sxs-lookup"><span data-stu-id="37802-265">False</span></span>                                      |
| <span data-ttu-id="37802-266">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37802-266">Is-Single-Valued</span></span>       | <span data-ttu-id="37802-267">否</span><span class="sxs-lookup"><span data-stu-id="37802-267">False</span></span>                                      |
| <span data-ttu-id="37802-268">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37802-268">Is Indexed</span></span>             | <span data-ttu-id="37802-269">對</span><span class="sxs-lookup"><span data-stu-id="37802-269">True</span></span>                                       |
| <span data-ttu-id="37802-270">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37802-270">In Global Catalog</span></span>      | <span data-ttu-id="37802-271">否</span><span class="sxs-lookup"><span data-stu-id="37802-271">False</span></span>                                      |
| <span data-ttu-id="37802-272">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37802-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="37802-273">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37802-273">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="37802-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37802-274">Range-Lower</span></span>            | <span data-ttu-id="37802-275">1</span><span class="sxs-lookup"><span data-stu-id="37802-275">1</span></span>                                          |
| <span data-ttu-id="37802-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37802-276">Range-Upper</span></span>            | <span data-ttu-id="37802-277">255</span><span class="sxs-lookup"><span data-stu-id="37802-277">255</span></span>                                        |
| <span data-ttu-id="37802-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-278">Search-Flags</span></span>           | <span data-ttu-id="37802-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="37802-279">0x00000001</span></span>                                 |
| <span data-ttu-id="37802-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-280">System-Flags</span></span>           | <span data-ttu-id="37802-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37802-281">0x00000010</span></span>                                 |
| <span data-ttu-id="37802-282">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37802-282">Classes used in</span></span>        | [<span data-ttu-id="37802-283">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="37802-283">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37802-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37802-284">Windows Server 2012</span></span>



| <span data-ttu-id="37802-285">進入</span><span class="sxs-lookup"><span data-stu-id="37802-285">Entry</span></span> | <span data-ttu-id="37802-286">值</span><span class="sxs-lookup"><span data-stu-id="37802-286">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="37802-287">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37802-287">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37802-288">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="37802-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="37802-289">System-Only</span></span>            | <span data-ttu-id="37802-290">否</span><span class="sxs-lookup"><span data-stu-id="37802-290">False</span></span>                                      |
| <span data-ttu-id="37802-291">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37802-291">Is-Single-Valued</span></span>       | <span data-ttu-id="37802-292">否</span><span class="sxs-lookup"><span data-stu-id="37802-292">False</span></span>                                      |
| <span data-ttu-id="37802-293">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37802-293">Is Indexed</span></span>             | <span data-ttu-id="37802-294">對</span><span class="sxs-lookup"><span data-stu-id="37802-294">True</span></span>                                       |
| <span data-ttu-id="37802-295">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37802-295">In Global Catalog</span></span>      | <span data-ttu-id="37802-296">否</span><span class="sxs-lookup"><span data-stu-id="37802-296">False</span></span>                                      |
| <span data-ttu-id="37802-297">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37802-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="37802-298">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37802-298">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="37802-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37802-299">Range-Lower</span></span>            | <span data-ttu-id="37802-300">1</span><span class="sxs-lookup"><span data-stu-id="37802-300">1</span></span>                                          |
| <span data-ttu-id="37802-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37802-301">Range-Upper</span></span>            | <span data-ttu-id="37802-302">255</span><span class="sxs-lookup"><span data-stu-id="37802-302">255</span></span>                                        |
| <span data-ttu-id="37802-303">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-303">Search-Flags</span></span>           | <span data-ttu-id="37802-304">0x00000001</span><span class="sxs-lookup"><span data-stu-id="37802-304">0x00000001</span></span>                                 |
| <span data-ttu-id="37802-305">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37802-305">System-Flags</span></span>           | <span data-ttu-id="37802-306">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37802-306">0x00000010</span></span>                                 |
| <span data-ttu-id="37802-307">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37802-307">Classes used in</span></span>        | [<span data-ttu-id="37802-308">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="37802-308">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






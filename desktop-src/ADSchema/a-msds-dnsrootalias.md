---
title: DnsRootAlias 屬性
description: 用來儲存網域別名。
ms.assetid: 36b64363-947f-4af9-947f-eefead55bb02
ms.tgt_platform: multiple
keywords:
- DnsRootAlias 屬性 AD 架構
- DnsRootAlias 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-DnsRootAlias
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0b20b9316aaa9e68ab1ed907135c5640c1480f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687263"
---
# <a name="ms-ds-dnsrootalias-attribute"></a><span data-ttu-id="01d31-105">DnsRootAlias 屬性</span><span class="sxs-lookup"><span data-stu-id="01d31-105">ms-DS-DnsRootAlias attribute</span></span>

<span data-ttu-id="01d31-106">用來儲存網域別名。</span><span class="sxs-lookup"><span data-stu-id="01d31-106">Used to store the domain alias.</span></span>



| <span data-ttu-id="01d31-107">進入</span><span class="sxs-lookup"><span data-stu-id="01d31-107">Entry</span></span> | <span data-ttu-id="01d31-108">值</span><span class="sxs-lookup"><span data-stu-id="01d31-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="01d31-109">CN</span><span class="sxs-lookup"><span data-stu-id="01d31-109">CN</span></span>                | <span data-ttu-id="01d31-110">DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="01d31-110">ms-DS-DnsRootAlias</span></span>                          |
| <span data-ttu-id="01d31-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="01d31-111">Ldap-Display-Name</span></span> | <span data-ttu-id="01d31-112">DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="01d31-112">msDS-DnsRootAlias</span></span>                           |
| <span data-ttu-id="01d31-113">大小</span><span class="sxs-lookup"><span data-stu-id="01d31-113">Size</span></span>              | <span data-ttu-id="01d31-114">大小上限為255個位元組。</span><span class="sxs-lookup"><span data-stu-id="01d31-114">Maximum size 255 bytes.</span></span>                     |
| <span data-ttu-id="01d31-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="01d31-115">Update Privilege</span></span>  | <span data-ttu-id="01d31-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="01d31-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="01d31-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="01d31-117">Update Frequency</span></span>  | <span data-ttu-id="01d31-118">只有在網域重建時。</span><span class="sxs-lookup"><span data-stu-id="01d31-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="01d31-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="01d31-119">Attribute-Id</span></span>      | <span data-ttu-id="01d31-120">1.2.840.113556.1.4.1719</span><span class="sxs-lookup"><span data-stu-id="01d31-120">1.2.840.113556.1.4.1719</span></span>                     |
| <span data-ttu-id="01d31-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="01d31-121">System-Id-Guid</span></span>    | <span data-ttu-id="01d31-122">2143acca-eead-4d29-b591-85fa49ce9173</span><span class="sxs-lookup"><span data-stu-id="01d31-122">2143acca-eead-4d29-b591-85fa49ce9173</span></span>        |
| <span data-ttu-id="01d31-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="01d31-123">Syntax</span></span>            | [<span data-ttu-id="01d31-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="01d31-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="01d31-125">實作</span><span class="sxs-lookup"><span data-stu-id="01d31-125">Implementations</span></span>

-   [<span data-ttu-id="01d31-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="01d31-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="01d31-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="01d31-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="01d31-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="01d31-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="01d31-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="01d31-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="01d31-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="01d31-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="01d31-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="01d31-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="01d31-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01d31-132">Windows Server 2003</span></span>



| <span data-ttu-id="01d31-133">進入</span><span class="sxs-lookup"><span data-stu-id="01d31-133">Entry</span></span> | <span data-ttu-id="01d31-134">值</span><span class="sxs-lookup"><span data-stu-id="01d31-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="01d31-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01d31-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01d31-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="01d31-137">System-Only</span></span>            | <span data-ttu-id="01d31-138">否</span><span class="sxs-lookup"><span data-stu-id="01d31-138">False</span></span>                                      |
| <span data-ttu-id="01d31-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01d31-139">Is-Single-Valued</span></span>       | <span data-ttu-id="01d31-140">對</span><span class="sxs-lookup"><span data-stu-id="01d31-140">True</span></span>                                       |
| <span data-ttu-id="01d31-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01d31-141">Is Indexed</span></span>             | <span data-ttu-id="01d31-142">否</span><span class="sxs-lookup"><span data-stu-id="01d31-142">False</span></span>                                      |
| <span data-ttu-id="01d31-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01d31-143">In Global Catalog</span></span>      | <span data-ttu-id="01d31-144">否</span><span class="sxs-lookup"><span data-stu-id="01d31-144">False</span></span>                                      |
| <span data-ttu-id="01d31-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01d31-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="01d31-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01d31-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="01d31-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01d31-147">Range-Lower</span></span>            | <span data-ttu-id="01d31-148">0</span><span class="sxs-lookup"><span data-stu-id="01d31-148">0</span></span>                                          |
| <span data-ttu-id="01d31-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01d31-149">Range-Upper</span></span>            | <span data-ttu-id="01d31-150">255</span><span class="sxs-lookup"><span data-stu-id="01d31-150">255</span></span>                                        |
| <span data-ttu-id="01d31-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-151">Search-Flags</span></span>           | <span data-ttu-id="01d31-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01d31-152">0x00000000</span></span>                                 |
| <span data-ttu-id="01d31-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-153">System-Flags</span></span>           | <span data-ttu-id="01d31-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01d31-154">0x00000010</span></span>                                 |
| <span data-ttu-id="01d31-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01d31-155">Classes used in</span></span>        | [<span data-ttu-id="01d31-156">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="01d31-156">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="01d31-157">亞當</span><span class="sxs-lookup"><span data-stu-id="01d31-157">ADAM</span></span>



| <span data-ttu-id="01d31-158">進入</span><span class="sxs-lookup"><span data-stu-id="01d31-158">Entry</span></span> | <span data-ttu-id="01d31-159">值</span><span class="sxs-lookup"><span data-stu-id="01d31-159">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="01d31-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01d31-160">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01d31-161">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="01d31-162">System-Only</span></span>            | <span data-ttu-id="01d31-163">否</span><span class="sxs-lookup"><span data-stu-id="01d31-163">False</span></span>                                      |
| <span data-ttu-id="01d31-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01d31-164">Is-Single-Valued</span></span>       | <span data-ttu-id="01d31-165">對</span><span class="sxs-lookup"><span data-stu-id="01d31-165">True</span></span>                                       |
| <span data-ttu-id="01d31-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01d31-166">Is Indexed</span></span>             | <span data-ttu-id="01d31-167">否</span><span class="sxs-lookup"><span data-stu-id="01d31-167">False</span></span>                                      |
| <span data-ttu-id="01d31-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01d31-168">In Global Catalog</span></span>      | <span data-ttu-id="01d31-169">否</span><span class="sxs-lookup"><span data-stu-id="01d31-169">False</span></span>                                      |
| <span data-ttu-id="01d31-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01d31-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="01d31-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01d31-171">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="01d31-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01d31-172">Range-Lower</span></span>            | <span data-ttu-id="01d31-173">0</span><span class="sxs-lookup"><span data-stu-id="01d31-173">0</span></span>                                          |
| <span data-ttu-id="01d31-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01d31-174">Range-Upper</span></span>            | <span data-ttu-id="01d31-175">255</span><span class="sxs-lookup"><span data-stu-id="01d31-175">255</span></span>                                        |
| <span data-ttu-id="01d31-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-176">Search-Flags</span></span>           | <span data-ttu-id="01d31-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01d31-177">0x00000000</span></span>                                 |
| <span data-ttu-id="01d31-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-178">System-Flags</span></span>           | <span data-ttu-id="01d31-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01d31-179">0x00000010</span></span>                                 |
| <span data-ttu-id="01d31-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01d31-180">Classes used in</span></span>        | [<span data-ttu-id="01d31-181">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="01d31-181">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="01d31-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01d31-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="01d31-183">進入</span><span class="sxs-lookup"><span data-stu-id="01d31-183">Entry</span></span> | <span data-ttu-id="01d31-184">值</span><span class="sxs-lookup"><span data-stu-id="01d31-184">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="01d31-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01d31-185">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01d31-186">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="01d31-187">System-Only</span></span>            | <span data-ttu-id="01d31-188">否</span><span class="sxs-lookup"><span data-stu-id="01d31-188">False</span></span>                                      |
| <span data-ttu-id="01d31-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01d31-189">Is-Single-Valued</span></span>       | <span data-ttu-id="01d31-190">對</span><span class="sxs-lookup"><span data-stu-id="01d31-190">True</span></span>                                       |
| <span data-ttu-id="01d31-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01d31-191">Is Indexed</span></span>             | <span data-ttu-id="01d31-192">否</span><span class="sxs-lookup"><span data-stu-id="01d31-192">False</span></span>                                      |
| <span data-ttu-id="01d31-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01d31-193">In Global Catalog</span></span>      | <span data-ttu-id="01d31-194">否</span><span class="sxs-lookup"><span data-stu-id="01d31-194">False</span></span>                                      |
| <span data-ttu-id="01d31-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01d31-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="01d31-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01d31-196">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="01d31-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01d31-197">Range-Lower</span></span>            | <span data-ttu-id="01d31-198">0</span><span class="sxs-lookup"><span data-stu-id="01d31-198">0</span></span>                                          |
| <span data-ttu-id="01d31-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01d31-199">Range-Upper</span></span>            | <span data-ttu-id="01d31-200">255</span><span class="sxs-lookup"><span data-stu-id="01d31-200">255</span></span>                                        |
| <span data-ttu-id="01d31-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-201">Search-Flags</span></span>           | <span data-ttu-id="01d31-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01d31-202">0x00000000</span></span>                                 |
| <span data-ttu-id="01d31-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-203">System-Flags</span></span>           | <span data-ttu-id="01d31-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01d31-204">0x00000010</span></span>                                 |
| <span data-ttu-id="01d31-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01d31-205">Classes used in</span></span>        | [<span data-ttu-id="01d31-206">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="01d31-206">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="01d31-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01d31-207">Windows Server 2008</span></span>



| <span data-ttu-id="01d31-208">進入</span><span class="sxs-lookup"><span data-stu-id="01d31-208">Entry</span></span> | <span data-ttu-id="01d31-209">值</span><span class="sxs-lookup"><span data-stu-id="01d31-209">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="01d31-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01d31-210">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01d31-211">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="01d31-212">System-Only</span></span>            | <span data-ttu-id="01d31-213">否</span><span class="sxs-lookup"><span data-stu-id="01d31-213">False</span></span>                                      |
| <span data-ttu-id="01d31-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01d31-214">Is-Single-Valued</span></span>       | <span data-ttu-id="01d31-215">對</span><span class="sxs-lookup"><span data-stu-id="01d31-215">True</span></span>                                       |
| <span data-ttu-id="01d31-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01d31-216">Is Indexed</span></span>             | <span data-ttu-id="01d31-217">否</span><span class="sxs-lookup"><span data-stu-id="01d31-217">False</span></span>                                      |
| <span data-ttu-id="01d31-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01d31-218">In Global Catalog</span></span>      | <span data-ttu-id="01d31-219">否</span><span class="sxs-lookup"><span data-stu-id="01d31-219">False</span></span>                                      |
| <span data-ttu-id="01d31-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01d31-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="01d31-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01d31-221">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="01d31-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01d31-222">Range-Lower</span></span>            | <span data-ttu-id="01d31-223">0</span><span class="sxs-lookup"><span data-stu-id="01d31-223">0</span></span>                                          |
| <span data-ttu-id="01d31-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01d31-224">Range-Upper</span></span>            | <span data-ttu-id="01d31-225">255</span><span class="sxs-lookup"><span data-stu-id="01d31-225">255</span></span>                                        |
| <span data-ttu-id="01d31-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-226">Search-Flags</span></span>           | <span data-ttu-id="01d31-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01d31-227">0x00000000</span></span>                                 |
| <span data-ttu-id="01d31-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-228">System-Flags</span></span>           | <span data-ttu-id="01d31-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01d31-229">0x00000010</span></span>                                 |
| <span data-ttu-id="01d31-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01d31-230">Classes used in</span></span>        | [<span data-ttu-id="01d31-231">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="01d31-231">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="01d31-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01d31-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="01d31-233">進入</span><span class="sxs-lookup"><span data-stu-id="01d31-233">Entry</span></span> | <span data-ttu-id="01d31-234">值</span><span class="sxs-lookup"><span data-stu-id="01d31-234">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="01d31-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01d31-235">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01d31-236">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="01d31-237">System-Only</span></span>            | <span data-ttu-id="01d31-238">否</span><span class="sxs-lookup"><span data-stu-id="01d31-238">False</span></span>                                      |
| <span data-ttu-id="01d31-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01d31-239">Is-Single-Valued</span></span>       | <span data-ttu-id="01d31-240">對</span><span class="sxs-lookup"><span data-stu-id="01d31-240">True</span></span>                                       |
| <span data-ttu-id="01d31-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01d31-241">Is Indexed</span></span>             | <span data-ttu-id="01d31-242">否</span><span class="sxs-lookup"><span data-stu-id="01d31-242">False</span></span>                                      |
| <span data-ttu-id="01d31-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01d31-243">In Global Catalog</span></span>      | <span data-ttu-id="01d31-244">否</span><span class="sxs-lookup"><span data-stu-id="01d31-244">False</span></span>                                      |
| <span data-ttu-id="01d31-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01d31-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="01d31-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01d31-246">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="01d31-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01d31-247">Range-Lower</span></span>            | <span data-ttu-id="01d31-248">0</span><span class="sxs-lookup"><span data-stu-id="01d31-248">0</span></span>                                          |
| <span data-ttu-id="01d31-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01d31-249">Range-Upper</span></span>            | <span data-ttu-id="01d31-250">255</span><span class="sxs-lookup"><span data-stu-id="01d31-250">255</span></span>                                        |
| <span data-ttu-id="01d31-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-251">Search-Flags</span></span>           | <span data-ttu-id="01d31-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01d31-252">0x00000000</span></span>                                 |
| <span data-ttu-id="01d31-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-253">System-Flags</span></span>           | <span data-ttu-id="01d31-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01d31-254">0x00000010</span></span>                                 |
| <span data-ttu-id="01d31-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01d31-255">Classes used in</span></span>        | [<span data-ttu-id="01d31-256">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="01d31-256">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="01d31-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01d31-257">Windows Server 2012</span></span>



| <span data-ttu-id="01d31-258">進入</span><span class="sxs-lookup"><span data-stu-id="01d31-258">Entry</span></span> | <span data-ttu-id="01d31-259">值</span><span class="sxs-lookup"><span data-stu-id="01d31-259">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="01d31-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="01d31-260">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01d31-261">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="01d31-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="01d31-262">System-Only</span></span>            | <span data-ttu-id="01d31-263">否</span><span class="sxs-lookup"><span data-stu-id="01d31-263">False</span></span>                                      |
| <span data-ttu-id="01d31-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="01d31-264">Is-Single-Valued</span></span>       | <span data-ttu-id="01d31-265">對</span><span class="sxs-lookup"><span data-stu-id="01d31-265">True</span></span>                                       |
| <span data-ttu-id="01d31-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="01d31-266">Is Indexed</span></span>             | <span data-ttu-id="01d31-267">否</span><span class="sxs-lookup"><span data-stu-id="01d31-267">False</span></span>                                      |
| <span data-ttu-id="01d31-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="01d31-268">In Global Catalog</span></span>      | <span data-ttu-id="01d31-269">否</span><span class="sxs-lookup"><span data-stu-id="01d31-269">False</span></span>                                      |
| <span data-ttu-id="01d31-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="01d31-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="01d31-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="01d31-271">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="01d31-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01d31-272">Range-Lower</span></span>            | <span data-ttu-id="01d31-273">0</span><span class="sxs-lookup"><span data-stu-id="01d31-273">0</span></span>                                          |
| <span data-ttu-id="01d31-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01d31-274">Range-Upper</span></span>            | <span data-ttu-id="01d31-275">255</span><span class="sxs-lookup"><span data-stu-id="01d31-275">255</span></span>                                        |
| <span data-ttu-id="01d31-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-276">Search-Flags</span></span>           | <span data-ttu-id="01d31-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01d31-277">0x00000000</span></span>                                 |
| <span data-ttu-id="01d31-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01d31-278">System-Flags</span></span>           | <span data-ttu-id="01d31-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01d31-279">0x00000010</span></span>                                 |
| <span data-ttu-id="01d31-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="01d31-280">Classes used in</span></span>        | [<span data-ttu-id="01d31-281">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="01d31-281">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






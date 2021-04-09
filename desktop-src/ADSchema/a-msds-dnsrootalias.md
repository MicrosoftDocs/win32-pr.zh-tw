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
# <a name="ms-ds-dnsrootalias-attribute"></a><span data-ttu-id="8419d-105">DnsRootAlias 屬性</span><span class="sxs-lookup"><span data-stu-id="8419d-105">ms-DS-DnsRootAlias attribute</span></span>

<span data-ttu-id="8419d-106">用來儲存網域別名。</span><span class="sxs-lookup"><span data-stu-id="8419d-106">Used to store the domain alias.</span></span>



| <span data-ttu-id="8419d-107">進入</span><span class="sxs-lookup"><span data-stu-id="8419d-107">Entry</span></span> | <span data-ttu-id="8419d-108">值</span><span class="sxs-lookup"><span data-stu-id="8419d-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8419d-109">CN</span><span class="sxs-lookup"><span data-stu-id="8419d-109">CN</span></span>                | <span data-ttu-id="8419d-110">DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="8419d-110">ms-DS-DnsRootAlias</span></span>                          |
| <span data-ttu-id="8419d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8419d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8419d-112">DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="8419d-112">msDS-DnsRootAlias</span></span>                           |
| <span data-ttu-id="8419d-113">大小</span><span class="sxs-lookup"><span data-stu-id="8419d-113">Size</span></span>              | <span data-ttu-id="8419d-114">大小上限為255個位元組。</span><span class="sxs-lookup"><span data-stu-id="8419d-114">Maximum size 255 bytes.</span></span>                     |
| <span data-ttu-id="8419d-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8419d-115">Update Privilege</span></span>  | <span data-ttu-id="8419d-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="8419d-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="8419d-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8419d-117">Update Frequency</span></span>  | <span data-ttu-id="8419d-118">只有在網域重建時。</span><span class="sxs-lookup"><span data-stu-id="8419d-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="8419d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8419d-119">Attribute-Id</span></span>      | <span data-ttu-id="8419d-120">1.2.840.113556.1.4.1719</span><span class="sxs-lookup"><span data-stu-id="8419d-120">1.2.840.113556.1.4.1719</span></span>                     |
| <span data-ttu-id="8419d-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8419d-121">System-Id-Guid</span></span>    | <span data-ttu-id="8419d-122">2143acca-eead-4d29-b591-85fa49ce9173</span><span class="sxs-lookup"><span data-stu-id="8419d-122">2143acca-eead-4d29-b591-85fa49ce9173</span></span>        |
| <span data-ttu-id="8419d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="8419d-123">Syntax</span></span>            | [<span data-ttu-id="8419d-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8419d-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8419d-125">實作</span><span class="sxs-lookup"><span data-stu-id="8419d-125">Implementations</span></span>

-   [<span data-ttu-id="8419d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8419d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8419d-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="8419d-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8419d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8419d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8419d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8419d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8419d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8419d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8419d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8419d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8419d-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8419d-132">Windows Server 2003</span></span>



| <span data-ttu-id="8419d-133">進入</span><span class="sxs-lookup"><span data-stu-id="8419d-133">Entry</span></span> | <span data-ttu-id="8419d-134">值</span><span class="sxs-lookup"><span data-stu-id="8419d-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="8419d-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8419d-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8419d-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8419d-137">System-Only</span></span>            | <span data-ttu-id="8419d-138">否</span><span class="sxs-lookup"><span data-stu-id="8419d-138">False</span></span>                                      |
| <span data-ttu-id="8419d-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8419d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8419d-140">對</span><span class="sxs-lookup"><span data-stu-id="8419d-140">True</span></span>                                       |
| <span data-ttu-id="8419d-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8419d-141">Is Indexed</span></span>             | <span data-ttu-id="8419d-142">否</span><span class="sxs-lookup"><span data-stu-id="8419d-142">False</span></span>                                      |
| <span data-ttu-id="8419d-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8419d-143">In Global Catalog</span></span>      | <span data-ttu-id="8419d-144">否</span><span class="sxs-lookup"><span data-stu-id="8419d-144">False</span></span>                                      |
| <span data-ttu-id="8419d-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8419d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8419d-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8419d-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="8419d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8419d-147">Range-Lower</span></span>            | <span data-ttu-id="8419d-148">0</span><span class="sxs-lookup"><span data-stu-id="8419d-148">0</span></span>                                          |
| <span data-ttu-id="8419d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8419d-149">Range-Upper</span></span>            | <span data-ttu-id="8419d-150">255</span><span class="sxs-lookup"><span data-stu-id="8419d-150">255</span></span>                                        |
| <span data-ttu-id="8419d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-151">Search-Flags</span></span>           | <span data-ttu-id="8419d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8419d-152">0x00000000</span></span>                                 |
| <span data-ttu-id="8419d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-153">System-Flags</span></span>           | <span data-ttu-id="8419d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8419d-154">0x00000010</span></span>                                 |
| <span data-ttu-id="8419d-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8419d-155">Classes used in</span></span>        | [<span data-ttu-id="8419d-156">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="8419d-156">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8419d-157">亞當</span><span class="sxs-lookup"><span data-stu-id="8419d-157">ADAM</span></span>



| <span data-ttu-id="8419d-158">進入</span><span class="sxs-lookup"><span data-stu-id="8419d-158">Entry</span></span> | <span data-ttu-id="8419d-159">值</span><span class="sxs-lookup"><span data-stu-id="8419d-159">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="8419d-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8419d-160">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8419d-161">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="8419d-162">System-Only</span></span>            | <span data-ttu-id="8419d-163">否</span><span class="sxs-lookup"><span data-stu-id="8419d-163">False</span></span>                                      |
| <span data-ttu-id="8419d-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8419d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="8419d-165">對</span><span class="sxs-lookup"><span data-stu-id="8419d-165">True</span></span>                                       |
| <span data-ttu-id="8419d-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8419d-166">Is Indexed</span></span>             | <span data-ttu-id="8419d-167">否</span><span class="sxs-lookup"><span data-stu-id="8419d-167">False</span></span>                                      |
| <span data-ttu-id="8419d-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8419d-168">In Global Catalog</span></span>      | <span data-ttu-id="8419d-169">否</span><span class="sxs-lookup"><span data-stu-id="8419d-169">False</span></span>                                      |
| <span data-ttu-id="8419d-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8419d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="8419d-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8419d-171">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="8419d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8419d-172">Range-Lower</span></span>            | <span data-ttu-id="8419d-173">0</span><span class="sxs-lookup"><span data-stu-id="8419d-173">0</span></span>                                          |
| <span data-ttu-id="8419d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8419d-174">Range-Upper</span></span>            | <span data-ttu-id="8419d-175">255</span><span class="sxs-lookup"><span data-stu-id="8419d-175">255</span></span>                                        |
| <span data-ttu-id="8419d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-176">Search-Flags</span></span>           | <span data-ttu-id="8419d-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8419d-177">0x00000000</span></span>                                 |
| <span data-ttu-id="8419d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-178">System-Flags</span></span>           | <span data-ttu-id="8419d-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8419d-179">0x00000010</span></span>                                 |
| <span data-ttu-id="8419d-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8419d-180">Classes used in</span></span>        | [<span data-ttu-id="8419d-181">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="8419d-181">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8419d-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8419d-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8419d-183">進入</span><span class="sxs-lookup"><span data-stu-id="8419d-183">Entry</span></span> | <span data-ttu-id="8419d-184">值</span><span class="sxs-lookup"><span data-stu-id="8419d-184">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="8419d-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8419d-185">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8419d-186">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8419d-187">System-Only</span></span>            | <span data-ttu-id="8419d-188">否</span><span class="sxs-lookup"><span data-stu-id="8419d-188">False</span></span>                                      |
| <span data-ttu-id="8419d-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8419d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8419d-190">對</span><span class="sxs-lookup"><span data-stu-id="8419d-190">True</span></span>                                       |
| <span data-ttu-id="8419d-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8419d-191">Is Indexed</span></span>             | <span data-ttu-id="8419d-192">否</span><span class="sxs-lookup"><span data-stu-id="8419d-192">False</span></span>                                      |
| <span data-ttu-id="8419d-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8419d-193">In Global Catalog</span></span>      | <span data-ttu-id="8419d-194">否</span><span class="sxs-lookup"><span data-stu-id="8419d-194">False</span></span>                                      |
| <span data-ttu-id="8419d-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8419d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8419d-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8419d-196">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="8419d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8419d-197">Range-Lower</span></span>            | <span data-ttu-id="8419d-198">0</span><span class="sxs-lookup"><span data-stu-id="8419d-198">0</span></span>                                          |
| <span data-ttu-id="8419d-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8419d-199">Range-Upper</span></span>            | <span data-ttu-id="8419d-200">255</span><span class="sxs-lookup"><span data-stu-id="8419d-200">255</span></span>                                        |
| <span data-ttu-id="8419d-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-201">Search-Flags</span></span>           | <span data-ttu-id="8419d-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8419d-202">0x00000000</span></span>                                 |
| <span data-ttu-id="8419d-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-203">System-Flags</span></span>           | <span data-ttu-id="8419d-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8419d-204">0x00000010</span></span>                                 |
| <span data-ttu-id="8419d-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8419d-205">Classes used in</span></span>        | [<span data-ttu-id="8419d-206">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="8419d-206">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8419d-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8419d-207">Windows Server 2008</span></span>



| <span data-ttu-id="8419d-208">進入</span><span class="sxs-lookup"><span data-stu-id="8419d-208">Entry</span></span> | <span data-ttu-id="8419d-209">值</span><span class="sxs-lookup"><span data-stu-id="8419d-209">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="8419d-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8419d-210">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8419d-211">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="8419d-212">System-Only</span></span>            | <span data-ttu-id="8419d-213">否</span><span class="sxs-lookup"><span data-stu-id="8419d-213">False</span></span>                                      |
| <span data-ttu-id="8419d-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8419d-214">Is-Single-Valued</span></span>       | <span data-ttu-id="8419d-215">對</span><span class="sxs-lookup"><span data-stu-id="8419d-215">True</span></span>                                       |
| <span data-ttu-id="8419d-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8419d-216">Is Indexed</span></span>             | <span data-ttu-id="8419d-217">否</span><span class="sxs-lookup"><span data-stu-id="8419d-217">False</span></span>                                      |
| <span data-ttu-id="8419d-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8419d-218">In Global Catalog</span></span>      | <span data-ttu-id="8419d-219">否</span><span class="sxs-lookup"><span data-stu-id="8419d-219">False</span></span>                                      |
| <span data-ttu-id="8419d-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8419d-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="8419d-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8419d-221">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="8419d-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8419d-222">Range-Lower</span></span>            | <span data-ttu-id="8419d-223">0</span><span class="sxs-lookup"><span data-stu-id="8419d-223">0</span></span>                                          |
| <span data-ttu-id="8419d-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8419d-224">Range-Upper</span></span>            | <span data-ttu-id="8419d-225">255</span><span class="sxs-lookup"><span data-stu-id="8419d-225">255</span></span>                                        |
| <span data-ttu-id="8419d-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-226">Search-Flags</span></span>           | <span data-ttu-id="8419d-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8419d-227">0x00000000</span></span>                                 |
| <span data-ttu-id="8419d-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-228">System-Flags</span></span>           | <span data-ttu-id="8419d-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8419d-229">0x00000010</span></span>                                 |
| <span data-ttu-id="8419d-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8419d-230">Classes used in</span></span>        | [<span data-ttu-id="8419d-231">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="8419d-231">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8419d-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8419d-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8419d-233">進入</span><span class="sxs-lookup"><span data-stu-id="8419d-233">Entry</span></span> | <span data-ttu-id="8419d-234">值</span><span class="sxs-lookup"><span data-stu-id="8419d-234">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="8419d-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8419d-235">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8419d-236">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="8419d-237">System-Only</span></span>            | <span data-ttu-id="8419d-238">否</span><span class="sxs-lookup"><span data-stu-id="8419d-238">False</span></span>                                      |
| <span data-ttu-id="8419d-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8419d-239">Is-Single-Valued</span></span>       | <span data-ttu-id="8419d-240">對</span><span class="sxs-lookup"><span data-stu-id="8419d-240">True</span></span>                                       |
| <span data-ttu-id="8419d-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8419d-241">Is Indexed</span></span>             | <span data-ttu-id="8419d-242">否</span><span class="sxs-lookup"><span data-stu-id="8419d-242">False</span></span>                                      |
| <span data-ttu-id="8419d-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8419d-243">In Global Catalog</span></span>      | <span data-ttu-id="8419d-244">否</span><span class="sxs-lookup"><span data-stu-id="8419d-244">False</span></span>                                      |
| <span data-ttu-id="8419d-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8419d-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="8419d-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8419d-246">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="8419d-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8419d-247">Range-Lower</span></span>            | <span data-ttu-id="8419d-248">0</span><span class="sxs-lookup"><span data-stu-id="8419d-248">0</span></span>                                          |
| <span data-ttu-id="8419d-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8419d-249">Range-Upper</span></span>            | <span data-ttu-id="8419d-250">255</span><span class="sxs-lookup"><span data-stu-id="8419d-250">255</span></span>                                        |
| <span data-ttu-id="8419d-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-251">Search-Flags</span></span>           | <span data-ttu-id="8419d-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8419d-252">0x00000000</span></span>                                 |
| <span data-ttu-id="8419d-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-253">System-Flags</span></span>           | <span data-ttu-id="8419d-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8419d-254">0x00000010</span></span>                                 |
| <span data-ttu-id="8419d-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8419d-255">Classes used in</span></span>        | [<span data-ttu-id="8419d-256">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="8419d-256">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8419d-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8419d-257">Windows Server 2012</span></span>



| <span data-ttu-id="8419d-258">進入</span><span class="sxs-lookup"><span data-stu-id="8419d-258">Entry</span></span> | <span data-ttu-id="8419d-259">值</span><span class="sxs-lookup"><span data-stu-id="8419d-259">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="8419d-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8419d-260">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8419d-261">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="8419d-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="8419d-262">System-Only</span></span>            | <span data-ttu-id="8419d-263">否</span><span class="sxs-lookup"><span data-stu-id="8419d-263">False</span></span>                                      |
| <span data-ttu-id="8419d-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8419d-264">Is-Single-Valued</span></span>       | <span data-ttu-id="8419d-265">對</span><span class="sxs-lookup"><span data-stu-id="8419d-265">True</span></span>                                       |
| <span data-ttu-id="8419d-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8419d-266">Is Indexed</span></span>             | <span data-ttu-id="8419d-267">否</span><span class="sxs-lookup"><span data-stu-id="8419d-267">False</span></span>                                      |
| <span data-ttu-id="8419d-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8419d-268">In Global Catalog</span></span>      | <span data-ttu-id="8419d-269">否</span><span class="sxs-lookup"><span data-stu-id="8419d-269">False</span></span>                                      |
| <span data-ttu-id="8419d-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8419d-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="8419d-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8419d-271">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="8419d-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8419d-272">Range-Lower</span></span>            | <span data-ttu-id="8419d-273">0</span><span class="sxs-lookup"><span data-stu-id="8419d-273">0</span></span>                                          |
| <span data-ttu-id="8419d-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8419d-274">Range-Upper</span></span>            | <span data-ttu-id="8419d-275">255</span><span class="sxs-lookup"><span data-stu-id="8419d-275">255</span></span>                                        |
| <span data-ttu-id="8419d-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-276">Search-Flags</span></span>           | <span data-ttu-id="8419d-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8419d-277">0x00000000</span></span>                                 |
| <span data-ttu-id="8419d-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8419d-278">System-Flags</span></span>           | <span data-ttu-id="8419d-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8419d-279">0x00000010</span></span>                                 |
| <span data-ttu-id="8419d-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8419d-280">Classes used in</span></span>        | [<span data-ttu-id="8419d-281">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="8419d-281">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






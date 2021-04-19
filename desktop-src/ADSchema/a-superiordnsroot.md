---
title: 高階 DNS-根屬性
description: 這是用於產生參考的系統屬性。
ms.assetid: 421f8315-26e2-457d-ae76-868b7fc6551a
ms.tgt_platform: multiple
keywords:
- 高階 DNS-根屬性 AD 架構
- superiorDNSRoot 屬性 AD 架構
topic_type:
- apiref
api_name:
- Superior-DNS-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6561839cf5137968adbac628ad6046b8b86dab85
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966581"
---
# <a name="superior-dns-root-attribute"></a><span data-ttu-id="9e77e-105">高階 DNS-根屬性</span><span class="sxs-lookup"><span data-stu-id="9e77e-105">Superior-DNS-Root attribute</span></span>

<span data-ttu-id="9e77e-106">這是用於產生參考的系統屬性。</span><span class="sxs-lookup"><span data-stu-id="9e77e-106">This is a system attribute that is used for referrals generation.</span></span>



| <span data-ttu-id="9e77e-107">進入</span><span class="sxs-lookup"><span data-stu-id="9e77e-107">Entry</span></span> | <span data-ttu-id="9e77e-108">值</span><span class="sxs-lookup"><span data-stu-id="9e77e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9e77e-109">CN</span><span class="sxs-lookup"><span data-stu-id="9e77e-109">CN</span></span>                | <span data-ttu-id="9e77e-110">高階 DNS-根目錄</span><span class="sxs-lookup"><span data-stu-id="9e77e-110">Superior-DNS-Root</span></span>                           |
| <span data-ttu-id="9e77e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9e77e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9e77e-112">superiorDNSRoot</span><span class="sxs-lookup"><span data-stu-id="9e77e-112">superiorDNSRoot</span></span>                             |
| <span data-ttu-id="9e77e-113">大小</span><span class="sxs-lookup"><span data-stu-id="9e77e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9e77e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9e77e-114">Update Privilege</span></span>  | <span data-ttu-id="9e77e-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="9e77e-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="9e77e-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9e77e-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9e77e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9e77e-117">Attribute-Id</span></span>      | <span data-ttu-id="9e77e-118">1.2.840.113556.1.4.532</span><span class="sxs-lookup"><span data-stu-id="9e77e-118">1.2.840.113556.1.4.532</span></span>                      |
| <span data-ttu-id="9e77e-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9e77e-119">System-Id-Guid</span></span>    | <span data-ttu-id="9e77e-120">5245801d-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9e77e-120">5245801d-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="9e77e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e77e-121">Syntax</span></span>            | [<span data-ttu-id="9e77e-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9e77e-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9e77e-123">實作</span><span class="sxs-lookup"><span data-stu-id="9e77e-123">Implementations</span></span>

-   [<span data-ttu-id="9e77e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9e77e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9e77e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9e77e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9e77e-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="9e77e-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9e77e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9e77e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9e77e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9e77e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9e77e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9e77e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9e77e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9e77e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9e77e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e77e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9e77e-132">進入</span><span class="sxs-lookup"><span data-stu-id="9e77e-132">Entry</span></span> | <span data-ttu-id="9e77e-133">值</span><span class="sxs-lookup"><span data-stu-id="9e77e-133">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9e77e-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e77e-134">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e77e-135">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e77e-136">System-Only</span></span>            | <span data-ttu-id="9e77e-137">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-137">False</span></span>                                      |
| <span data-ttu-id="9e77e-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e77e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9e77e-139">對</span><span class="sxs-lookup"><span data-stu-id="9e77e-139">True</span></span>                                       |
| <span data-ttu-id="9e77e-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e77e-140">Is Indexed</span></span>             | <span data-ttu-id="9e77e-141">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-141">False</span></span>                                      |
| <span data-ttu-id="9e77e-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e77e-142">In Global Catalog</span></span>      | <span data-ttu-id="9e77e-143">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-143">False</span></span>                                      |
| <span data-ttu-id="9e77e-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e77e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e77e-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e77e-145">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9e77e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e77e-146">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e77e-147">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-148">Search-Flags</span></span>           | <span data-ttu-id="9e77e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e77e-149">0x00000000</span></span>                                 |
| <span data-ttu-id="9e77e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-150">System-Flags</span></span>           | <span data-ttu-id="9e77e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e77e-151">0x00000010</span></span>                                 |
| <span data-ttu-id="9e77e-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e77e-152">Classes used in</span></span>        | [<span data-ttu-id="9e77e-153">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="9e77e-153">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9e77e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e77e-154">Windows Server 2003</span></span>



| <span data-ttu-id="9e77e-155">進入</span><span class="sxs-lookup"><span data-stu-id="9e77e-155">Entry</span></span> | <span data-ttu-id="9e77e-156">值</span><span class="sxs-lookup"><span data-stu-id="9e77e-156">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9e77e-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e77e-157">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e77e-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e77e-159">System-Only</span></span>            | <span data-ttu-id="9e77e-160">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-160">False</span></span>                                      |
| <span data-ttu-id="9e77e-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e77e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9e77e-162">對</span><span class="sxs-lookup"><span data-stu-id="9e77e-162">True</span></span>                                       |
| <span data-ttu-id="9e77e-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e77e-163">Is Indexed</span></span>             | <span data-ttu-id="9e77e-164">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-164">False</span></span>                                      |
| <span data-ttu-id="9e77e-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e77e-165">In Global Catalog</span></span>      | <span data-ttu-id="9e77e-166">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-166">False</span></span>                                      |
| <span data-ttu-id="9e77e-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e77e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e77e-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e77e-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9e77e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e77e-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e77e-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-171">Search-Flags</span></span>           | <span data-ttu-id="9e77e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e77e-172">0x00000000</span></span>                                 |
| <span data-ttu-id="9e77e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-173">System-Flags</span></span>           | <span data-ttu-id="9e77e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e77e-174">0x00000010</span></span>                                 |
| <span data-ttu-id="9e77e-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e77e-175">Classes used in</span></span>        | [<span data-ttu-id="9e77e-176">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="9e77e-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9e77e-177">亞當</span><span class="sxs-lookup"><span data-stu-id="9e77e-177">ADAM</span></span>



| <span data-ttu-id="9e77e-178">進入</span><span class="sxs-lookup"><span data-stu-id="9e77e-178">Entry</span></span> | <span data-ttu-id="9e77e-179">值</span><span class="sxs-lookup"><span data-stu-id="9e77e-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9e77e-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e77e-180">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e77e-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e77e-182">System-Only</span></span>            | <span data-ttu-id="9e77e-183">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-183">False</span></span>                                      |
| <span data-ttu-id="9e77e-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e77e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9e77e-185">對</span><span class="sxs-lookup"><span data-stu-id="9e77e-185">True</span></span>                                       |
| <span data-ttu-id="9e77e-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e77e-186">Is Indexed</span></span>             | <span data-ttu-id="9e77e-187">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-187">False</span></span>                                      |
| <span data-ttu-id="9e77e-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e77e-188">In Global Catalog</span></span>      | <span data-ttu-id="9e77e-189">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-189">False</span></span>                                      |
| <span data-ttu-id="9e77e-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e77e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e77e-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e77e-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9e77e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e77e-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e77e-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-194">Search-Flags</span></span>           | <span data-ttu-id="9e77e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e77e-195">0x00000000</span></span>                                 |
| <span data-ttu-id="9e77e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-196">System-Flags</span></span>           | <span data-ttu-id="9e77e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e77e-197">0x00000010</span></span>                                 |
| <span data-ttu-id="9e77e-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e77e-198">Classes used in</span></span>        | [<span data-ttu-id="9e77e-199">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="9e77e-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9e77e-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9e77e-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9e77e-201">進入</span><span class="sxs-lookup"><span data-stu-id="9e77e-201">Entry</span></span> | <span data-ttu-id="9e77e-202">值</span><span class="sxs-lookup"><span data-stu-id="9e77e-202">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9e77e-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e77e-203">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e77e-204">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e77e-205">System-Only</span></span>            | <span data-ttu-id="9e77e-206">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-206">False</span></span>                                      |
| <span data-ttu-id="9e77e-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e77e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9e77e-208">對</span><span class="sxs-lookup"><span data-stu-id="9e77e-208">True</span></span>                                       |
| <span data-ttu-id="9e77e-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e77e-209">Is Indexed</span></span>             | <span data-ttu-id="9e77e-210">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-210">False</span></span>                                      |
| <span data-ttu-id="9e77e-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e77e-211">In Global Catalog</span></span>      | <span data-ttu-id="9e77e-212">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-212">False</span></span>                                      |
| <span data-ttu-id="9e77e-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e77e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e77e-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e77e-214">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9e77e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e77e-215">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e77e-216">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-217">Search-Flags</span></span>           | <span data-ttu-id="9e77e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e77e-218">0x00000000</span></span>                                 |
| <span data-ttu-id="9e77e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-219">System-Flags</span></span>           | <span data-ttu-id="9e77e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e77e-220">0x00000010</span></span>                                 |
| <span data-ttu-id="9e77e-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e77e-221">Classes used in</span></span>        | [<span data-ttu-id="9e77e-222">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="9e77e-222">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9e77e-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e77e-223">Windows Server 2008</span></span>



| <span data-ttu-id="9e77e-224">進入</span><span class="sxs-lookup"><span data-stu-id="9e77e-224">Entry</span></span> | <span data-ttu-id="9e77e-225">值</span><span class="sxs-lookup"><span data-stu-id="9e77e-225">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9e77e-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e77e-226">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e77e-227">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e77e-228">System-Only</span></span>            | <span data-ttu-id="9e77e-229">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-229">False</span></span>                                      |
| <span data-ttu-id="9e77e-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e77e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9e77e-231">對</span><span class="sxs-lookup"><span data-stu-id="9e77e-231">True</span></span>                                       |
| <span data-ttu-id="9e77e-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e77e-232">Is Indexed</span></span>             | <span data-ttu-id="9e77e-233">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-233">False</span></span>                                      |
| <span data-ttu-id="9e77e-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e77e-234">In Global Catalog</span></span>      | <span data-ttu-id="9e77e-235">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-235">False</span></span>                                      |
| <span data-ttu-id="9e77e-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e77e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e77e-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e77e-237">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9e77e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e77e-238">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e77e-239">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-240">Search-Flags</span></span>           | <span data-ttu-id="9e77e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e77e-241">0x00000000</span></span>                                 |
| <span data-ttu-id="9e77e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-242">System-Flags</span></span>           | <span data-ttu-id="9e77e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e77e-243">0x00000010</span></span>                                 |
| <span data-ttu-id="9e77e-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e77e-244">Classes used in</span></span>        | [<span data-ttu-id="9e77e-245">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="9e77e-245">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9e77e-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e77e-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9e77e-247">進入</span><span class="sxs-lookup"><span data-stu-id="9e77e-247">Entry</span></span> | <span data-ttu-id="9e77e-248">值</span><span class="sxs-lookup"><span data-stu-id="9e77e-248">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9e77e-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e77e-249">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e77e-250">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e77e-251">System-Only</span></span>            | <span data-ttu-id="9e77e-252">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-252">False</span></span>                                      |
| <span data-ttu-id="9e77e-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e77e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9e77e-254">對</span><span class="sxs-lookup"><span data-stu-id="9e77e-254">True</span></span>                                       |
| <span data-ttu-id="9e77e-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e77e-255">Is Indexed</span></span>             | <span data-ttu-id="9e77e-256">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-256">False</span></span>                                      |
| <span data-ttu-id="9e77e-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e77e-257">In Global Catalog</span></span>      | <span data-ttu-id="9e77e-258">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-258">False</span></span>                                      |
| <span data-ttu-id="9e77e-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e77e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e77e-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e77e-260">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9e77e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e77e-261">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e77e-262">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-263">Search-Flags</span></span>           | <span data-ttu-id="9e77e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e77e-264">0x00000000</span></span>                                 |
| <span data-ttu-id="9e77e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-265">System-Flags</span></span>           | <span data-ttu-id="9e77e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e77e-266">0x00000010</span></span>                                 |
| <span data-ttu-id="9e77e-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e77e-267">Classes used in</span></span>        | [<span data-ttu-id="9e77e-268">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="9e77e-268">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9e77e-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e77e-269">Windows Server 2012</span></span>



| <span data-ttu-id="9e77e-270">進入</span><span class="sxs-lookup"><span data-stu-id="9e77e-270">Entry</span></span> | <span data-ttu-id="9e77e-271">值</span><span class="sxs-lookup"><span data-stu-id="9e77e-271">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="9e77e-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9e77e-272">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e77e-273">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="9e77e-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e77e-274">System-Only</span></span>            | <span data-ttu-id="9e77e-275">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-275">False</span></span>                                      |
| <span data-ttu-id="9e77e-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9e77e-276">Is-Single-Valued</span></span>       | <span data-ttu-id="9e77e-277">對</span><span class="sxs-lookup"><span data-stu-id="9e77e-277">True</span></span>                                       |
| <span data-ttu-id="9e77e-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9e77e-278">Is Indexed</span></span>             | <span data-ttu-id="9e77e-279">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-279">False</span></span>                                      |
| <span data-ttu-id="9e77e-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9e77e-280">In Global Catalog</span></span>      | <span data-ttu-id="9e77e-281">否</span><span class="sxs-lookup"><span data-stu-id="9e77e-281">False</span></span>                                      |
| <span data-ttu-id="9e77e-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9e77e-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e77e-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9e77e-283">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="9e77e-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e77e-284">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e77e-285">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="9e77e-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-286">Search-Flags</span></span>           | <span data-ttu-id="9e77e-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e77e-287">0x00000000</span></span>                                 |
| <span data-ttu-id="9e77e-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e77e-288">System-Flags</span></span>           | <span data-ttu-id="9e77e-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e77e-289">0x00000010</span></span>                                 |
| <span data-ttu-id="9e77e-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9e77e-290">Classes used in</span></span>        | [<span data-ttu-id="9e77e-291">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="9e77e-291">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






---
title: NT-混合網域屬性
description: 指出網域處於原生模式或混合模式。 這個屬性是在網域的 domainDNS (head) 物件中找到。
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- NT-Mixed-Domain attribute AD 架構
- nTMixedDomain 屬性 AD 架構
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971891"
---
# <a name="nt-mixed-domain-attribute"></a><span data-ttu-id="50c8b-106">NT-混合網域屬性</span><span class="sxs-lookup"><span data-stu-id="50c8b-106">NT-Mixed-Domain attribute</span></span>

<span data-ttu-id="50c8b-107">指出網域處於原生模式或混合模式。</span><span class="sxs-lookup"><span data-stu-id="50c8b-107">Indicates that the domain is in native mode or mixed mode.</span></span> <span data-ttu-id="50c8b-108">這個屬性是在網域的 domainDNS (head) 物件中找到。</span><span class="sxs-lookup"><span data-stu-id="50c8b-108">This attribute is found in the domainDNS (head) object for the domain.</span></span>



| <span data-ttu-id="50c8b-109">進入</span><span class="sxs-lookup"><span data-stu-id="50c8b-109">Entry</span></span> | <span data-ttu-id="50c8b-110">值</span><span class="sxs-lookup"><span data-stu-id="50c8b-110">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="50c8b-111">CN</span><span class="sxs-lookup"><span data-stu-id="50c8b-111">CN</span></span>                | <span data-ttu-id="50c8b-112">NT-混合網域</span><span class="sxs-lookup"><span data-stu-id="50c8b-112">NT-Mixed-Domain</span></span>                       |
| <span data-ttu-id="50c8b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="50c8b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="50c8b-114">nTMixedDomain</span><span class="sxs-lookup"><span data-stu-id="50c8b-114">nTMixedDomain</span></span>                         |
| <span data-ttu-id="50c8b-115">大小</span><span class="sxs-lookup"><span data-stu-id="50c8b-115">Size</span></span>              | <span data-ttu-id="50c8b-116">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="50c8b-116">4 bytes.</span></span> <span data-ttu-id="50c8b-117">混合模式1，原生模式0。</span><span class="sxs-lookup"><span data-stu-id="50c8b-117">Mixed mode 1, native mode 0.</span></span> |
| <span data-ttu-id="50c8b-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="50c8b-118">Update Privilege</span></span>  | \-                                    |
| <span data-ttu-id="50c8b-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="50c8b-119">Update Frequency</span></span>  | \-                                    |
| <span data-ttu-id="50c8b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="50c8b-120">Attribute-Id</span></span>      | <span data-ttu-id="50c8b-121">1.2.840.113556.1.4.357</span><span class="sxs-lookup"><span data-stu-id="50c8b-121">1.2.840.113556.1.4.357</span></span>                |
| <span data-ttu-id="50c8b-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="50c8b-122">System-Id-Guid</span></span>    | <span data-ttu-id="50c8b-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="50c8b-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span></span>  |
| <span data-ttu-id="50c8b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="50c8b-124">Syntax</span></span>            | [<span data-ttu-id="50c8b-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="50c8b-125">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="50c8b-126">實作</span><span class="sxs-lookup"><span data-stu-id="50c8b-126">Implementations</span></span>

-   [<span data-ttu-id="50c8b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="50c8b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="50c8b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="50c8b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="50c8b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="50c8b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="50c8b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="50c8b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="50c8b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50c8b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="50c8b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50c8b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="50c8b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="50c8b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="50c8b-134">進入</span><span class="sxs-lookup"><span data-stu-id="50c8b-134">Entry</span></span> | <span data-ttu-id="50c8b-135">值</span><span class="sxs-lookup"><span data-stu-id="50c8b-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="50c8b-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50c8b-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="50c8b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50c8b-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="50c8b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="50c8b-138">System-Only</span></span>            | <span data-ttu-id="50c8b-139">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-139">False</span></span>                                        |
| <span data-ttu-id="50c8b-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50c8b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="50c8b-141">對</span><span class="sxs-lookup"><span data-stu-id="50c8b-141">True</span></span>                                         |
| <span data-ttu-id="50c8b-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50c8b-142">Is Indexed</span></span>             | <span data-ttu-id="50c8b-143">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-143">False</span></span>                                        |
| <span data-ttu-id="50c8b-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50c8b-144">In Global Catalog</span></span>      | <span data-ttu-id="50c8b-145">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-145">False</span></span>                                        |
| <span data-ttu-id="50c8b-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50c8b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="50c8b-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50c8b-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="50c8b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50c8b-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="50c8b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50c8b-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="50c8b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-150">Search-Flags</span></span>           | <span data-ttu-id="50c8b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50c8b-151">0x00000000</span></span>                                   |
| <span data-ttu-id="50c8b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-152">System-Flags</span></span>           | <span data-ttu-id="50c8b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50c8b-153">0x00000010</span></span>                                   |
| <span data-ttu-id="50c8b-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50c8b-154">Classes used in</span></span>        | [<span data-ttu-id="50c8b-155">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50c8b-155">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="50c8b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50c8b-156">Windows Server 2003</span></span>



| <span data-ttu-id="50c8b-157">進入</span><span class="sxs-lookup"><span data-stu-id="50c8b-157">Entry</span></span> | <span data-ttu-id="50c8b-158">值</span><span class="sxs-lookup"><span data-stu-id="50c8b-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50c8b-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50c8b-159">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50c8b-160">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="50c8b-161">System-Only</span></span>            | <span data-ttu-id="50c8b-162">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-162">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50c8b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="50c8b-164">對</span><span class="sxs-lookup"><span data-stu-id="50c8b-164">True</span></span>                                                                                    |
| <span data-ttu-id="50c8b-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50c8b-165">Is Indexed</span></span>             | <span data-ttu-id="50c8b-166">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-166">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50c8b-167">In Global Catalog</span></span>      | <span data-ttu-id="50c8b-168">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-168">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50c8b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="50c8b-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50c8b-170">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="50c8b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50c8b-171">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50c8b-172">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-173">Search-Flags</span></span>           | <span data-ttu-id="50c8b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50c8b-174">0x00000000</span></span>                                                                              |
| <span data-ttu-id="50c8b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-175">System-Flags</span></span>           | <span data-ttu-id="50c8b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50c8b-176">0x00000010</span></span>                                                                              |
| <span data-ttu-id="50c8b-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50c8b-177">Classes used in</span></span>        | [<span data-ttu-id="50c8b-178">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50c8b-178">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="50c8b-179">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50c8b-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="50c8b-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="50c8b-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="50c8b-181">進入</span><span class="sxs-lookup"><span data-stu-id="50c8b-181">Entry</span></span> | <span data-ttu-id="50c8b-182">值</span><span class="sxs-lookup"><span data-stu-id="50c8b-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50c8b-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50c8b-183">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50c8b-184">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="50c8b-185">System-Only</span></span>            | <span data-ttu-id="50c8b-186">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-186">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50c8b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="50c8b-188">對</span><span class="sxs-lookup"><span data-stu-id="50c8b-188">True</span></span>                                                                                    |
| <span data-ttu-id="50c8b-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50c8b-189">Is Indexed</span></span>             | <span data-ttu-id="50c8b-190">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-190">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50c8b-191">In Global Catalog</span></span>      | <span data-ttu-id="50c8b-192">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-192">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50c8b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="50c8b-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50c8b-194">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="50c8b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50c8b-195">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50c8b-196">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-197">Search-Flags</span></span>           | <span data-ttu-id="50c8b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50c8b-198">0x00000000</span></span>                                                                              |
| <span data-ttu-id="50c8b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-199">System-Flags</span></span>           | <span data-ttu-id="50c8b-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50c8b-200">0x00000010</span></span>                                                                              |
| <span data-ttu-id="50c8b-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50c8b-201">Classes used in</span></span>        | [<span data-ttu-id="50c8b-202">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50c8b-202">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="50c8b-203">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50c8b-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="50c8b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50c8b-204">Windows Server 2008</span></span>



| <span data-ttu-id="50c8b-205">進入</span><span class="sxs-lookup"><span data-stu-id="50c8b-205">Entry</span></span> | <span data-ttu-id="50c8b-206">值</span><span class="sxs-lookup"><span data-stu-id="50c8b-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50c8b-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50c8b-207">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50c8b-208">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="50c8b-209">System-Only</span></span>            | <span data-ttu-id="50c8b-210">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-210">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50c8b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="50c8b-212">對</span><span class="sxs-lookup"><span data-stu-id="50c8b-212">True</span></span>                                                                                    |
| <span data-ttu-id="50c8b-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50c8b-213">Is Indexed</span></span>             | <span data-ttu-id="50c8b-214">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-214">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50c8b-215">In Global Catalog</span></span>      | <span data-ttu-id="50c8b-216">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-216">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50c8b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="50c8b-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50c8b-218">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="50c8b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50c8b-219">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50c8b-220">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-221">Search-Flags</span></span>           | <span data-ttu-id="50c8b-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50c8b-222">0x00000000</span></span>                                                                              |
| <span data-ttu-id="50c8b-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-223">System-Flags</span></span>           | <span data-ttu-id="50c8b-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50c8b-224">0x00000010</span></span>                                                                              |
| <span data-ttu-id="50c8b-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50c8b-225">Classes used in</span></span>        | [<span data-ttu-id="50c8b-226">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50c8b-226">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="50c8b-227">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50c8b-227">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="50c8b-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50c8b-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="50c8b-229">進入</span><span class="sxs-lookup"><span data-stu-id="50c8b-229">Entry</span></span> | <span data-ttu-id="50c8b-230">值</span><span class="sxs-lookup"><span data-stu-id="50c8b-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50c8b-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50c8b-231">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50c8b-232">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="50c8b-233">System-Only</span></span>            | <span data-ttu-id="50c8b-234">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-234">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50c8b-235">Is-Single-Valued</span></span>       | <span data-ttu-id="50c8b-236">對</span><span class="sxs-lookup"><span data-stu-id="50c8b-236">True</span></span>                                                                                    |
| <span data-ttu-id="50c8b-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50c8b-237">Is Indexed</span></span>             | <span data-ttu-id="50c8b-238">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-238">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50c8b-239">In Global Catalog</span></span>      | <span data-ttu-id="50c8b-240">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-240">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50c8b-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="50c8b-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50c8b-242">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="50c8b-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50c8b-243">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50c8b-244">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-245">Search-Flags</span></span>           | <span data-ttu-id="50c8b-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50c8b-246">0x00000000</span></span>                                                                              |
| <span data-ttu-id="50c8b-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-247">System-Flags</span></span>           | <span data-ttu-id="50c8b-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50c8b-248">0x00000010</span></span>                                                                              |
| <span data-ttu-id="50c8b-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50c8b-249">Classes used in</span></span>        | [<span data-ttu-id="50c8b-250">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50c8b-250">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="50c8b-251">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50c8b-251">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="50c8b-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50c8b-252">Windows Server 2012</span></span>



| <span data-ttu-id="50c8b-253">進入</span><span class="sxs-lookup"><span data-stu-id="50c8b-253">Entry</span></span> | <span data-ttu-id="50c8b-254">值</span><span class="sxs-lookup"><span data-stu-id="50c8b-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50c8b-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50c8b-255">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50c8b-256">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="50c8b-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="50c8b-257">System-Only</span></span>            | <span data-ttu-id="50c8b-258">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-258">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50c8b-259">Is-Single-Valued</span></span>       | <span data-ttu-id="50c8b-260">對</span><span class="sxs-lookup"><span data-stu-id="50c8b-260">True</span></span>                                                                                    |
| <span data-ttu-id="50c8b-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50c8b-261">Is Indexed</span></span>             | <span data-ttu-id="50c8b-262">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-262">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50c8b-263">In Global Catalog</span></span>      | <span data-ttu-id="50c8b-264">否</span><span class="sxs-lookup"><span data-stu-id="50c8b-264">False</span></span>                                                                                   |
| <span data-ttu-id="50c8b-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50c8b-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="50c8b-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50c8b-266">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="50c8b-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50c8b-267">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50c8b-268">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="50c8b-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-269">Search-Flags</span></span>           | <span data-ttu-id="50c8b-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50c8b-270">0x00000000</span></span>                                                                              |
| <span data-ttu-id="50c8b-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50c8b-271">System-Flags</span></span>           | <span data-ttu-id="50c8b-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50c8b-272">0x00000010</span></span>                                                                              |
| <span data-ttu-id="50c8b-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50c8b-273">Classes used in</span></span>        | [<span data-ttu-id="50c8b-274">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="50c8b-274">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="50c8b-275">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50c8b-275">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






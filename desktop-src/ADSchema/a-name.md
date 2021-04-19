---
title: RDN 屬性
description: 物件的相對辨別名稱 (RDN) 。
ms.assetid: 07fe0e81-1b18-4dbb-abca-a059a8bf993e
ms.tgt_platform: multiple
keywords:
- RDN 屬性 AD 架構
- 名稱屬性 AD 架構
topic_type:
- apiref
api_name:
- RDN
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe49bd525d0fa3f4ed95874f2020d9d2a5eb9554
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106991787"
---
# <a name="rdn-attribute"></a><span data-ttu-id="ba4da-105">RDN 屬性</span><span class="sxs-lookup"><span data-stu-id="ba4da-105">RDN attribute</span></span>

<span data-ttu-id="ba4da-106">物件的相對辨別名稱 (RDN) 。</span><span class="sxs-lookup"><span data-stu-id="ba4da-106">The Relative Distinguished Name (RDN) of an object.</span></span> <span data-ttu-id="ba4da-107">RDN 是辨別名稱的相對部分 (DN) ，可唯一識別 LDAP 物件。</span><span class="sxs-lookup"><span data-stu-id="ba4da-107">An RDN is the relative portion of a distinguished name (DN), which uniquely identifies an LDAP object.</span></span>



| <span data-ttu-id="ba4da-108">進入</span><span class="sxs-lookup"><span data-stu-id="ba4da-108">Entry</span></span> | <span data-ttu-id="ba4da-109">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="ba4da-110">CN</span><span class="sxs-lookup"><span data-stu-id="ba4da-110">CN</span></span>                | <span data-ttu-id="ba4da-111">RDN</span><span class="sxs-lookup"><span data-stu-id="ba4da-111">RDN</span></span>                                            |
| <span data-ttu-id="ba4da-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ba4da-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ba4da-113">NAME</span><span class="sxs-lookup"><span data-stu-id="ba4da-113">name</span></span>                                           |
| <span data-ttu-id="ba4da-114">大小</span><span class="sxs-lookup"><span data-stu-id="ba4da-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="ba4da-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ba4da-115">Update Privilege</span></span>  | <span data-ttu-id="ba4da-116">此值是由架構管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="ba4da-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="ba4da-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ba4da-117">Update Frequency</span></span>  | \-                                             |
| <span data-ttu-id="ba4da-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ba4da-118">Attribute-Id</span></span>      | <span data-ttu-id="ba4da-119">1.2.840.113556.1.4.1</span><span class="sxs-lookup"><span data-stu-id="ba4da-119">1.2.840.113556.1.4.1</span></span>                           |
| <span data-ttu-id="ba4da-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ba4da-120">System-Id-Guid</span></span>    | <span data-ttu-id="ba4da-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ba4da-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="ba4da-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba4da-122">Syntax</span></span>            | [<span data-ttu-id="ba4da-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ba4da-123">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="ba4da-124">實作</span><span class="sxs-lookup"><span data-stu-id="ba4da-124">Implementations</span></span>

-   [<span data-ttu-id="ba4da-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ba4da-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ba4da-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ba4da-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ba4da-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ba4da-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ba4da-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ba4da-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ba4da-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ba4da-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ba4da-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ba4da-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ba4da-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ba4da-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ba4da-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ba4da-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ba4da-133">進入</span><span class="sxs-lookup"><span data-stu-id="ba4da-133">Entry</span></span> | <span data-ttu-id="ba4da-134">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba4da-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba4da-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba4da-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba4da-136">MAPI-Id</span></span>                | <span data-ttu-id="ba4da-137">0x8202</span><span class="sxs-lookup"><span data-stu-id="ba4da-137">0x8202</span></span>                          |
| <span data-ttu-id="ba4da-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba4da-138">System-Only</span></span>            | <span data-ttu-id="ba4da-139">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-139">True</span></span>                            |
| <span data-ttu-id="ba4da-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba4da-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ba4da-141">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-141">True</span></span>                            |
| <span data-ttu-id="ba4da-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba4da-142">Is Indexed</span></span>             | <span data-ttu-id="ba4da-143">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-143">True</span></span>                            |
| <span data-ttu-id="ba4da-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba4da-144">In Global Catalog</span></span>      | <span data-ttu-id="ba4da-145">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-145">True</span></span>                            |
| <span data-ttu-id="ba4da-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba4da-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba4da-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba4da-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba4da-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba4da-148">Range-Lower</span></span>            | <span data-ttu-id="ba4da-149">1</span><span class="sxs-lookup"><span data-stu-id="ba4da-149">1</span></span>                               |
| <span data-ttu-id="ba4da-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba4da-150">Range-Upper</span></span>            | <span data-ttu-id="ba4da-151">255</span><span class="sxs-lookup"><span data-stu-id="ba4da-151">255</span></span>                             |
| <span data-ttu-id="ba4da-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-152">Search-Flags</span></span>           | <span data-ttu-id="ba4da-153">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="ba4da-153">0x0000000D</span></span>                      |
| <span data-ttu-id="ba4da-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-154">System-Flags</span></span>           | <span data-ttu-id="ba4da-155">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ba4da-155">0x00000012</span></span>                      |
| <span data-ttu-id="ba4da-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba4da-156">Classes used in</span></span>        | [<span data-ttu-id="ba4da-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ba4da-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ba4da-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba4da-158">Windows Server 2003</span></span>



| <span data-ttu-id="ba4da-159">進入</span><span class="sxs-lookup"><span data-stu-id="ba4da-159">Entry</span></span> | <span data-ttu-id="ba4da-160">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba4da-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba4da-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba4da-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba4da-162">MAPI-Id</span></span>                | <span data-ttu-id="ba4da-163">0x8202</span><span class="sxs-lookup"><span data-stu-id="ba4da-163">0x8202</span></span>                          |
| <span data-ttu-id="ba4da-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba4da-164">System-Only</span></span>            | <span data-ttu-id="ba4da-165">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-165">True</span></span>                            |
| <span data-ttu-id="ba4da-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba4da-166">Is-Single-Valued</span></span>       | <span data-ttu-id="ba4da-167">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-167">True</span></span>                            |
| <span data-ttu-id="ba4da-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba4da-168">Is Indexed</span></span>             | <span data-ttu-id="ba4da-169">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-169">True</span></span>                            |
| <span data-ttu-id="ba4da-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba4da-170">In Global Catalog</span></span>      | <span data-ttu-id="ba4da-171">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-171">True</span></span>                            |
| <span data-ttu-id="ba4da-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba4da-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba4da-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba4da-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba4da-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba4da-174">Range-Lower</span></span>            | <span data-ttu-id="ba4da-175">1</span><span class="sxs-lookup"><span data-stu-id="ba4da-175">1</span></span>                               |
| <span data-ttu-id="ba4da-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba4da-176">Range-Upper</span></span>            | <span data-ttu-id="ba4da-177">255</span><span class="sxs-lookup"><span data-stu-id="ba4da-177">255</span></span>                             |
| <span data-ttu-id="ba4da-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-178">Search-Flags</span></span>           | <span data-ttu-id="ba4da-179">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="ba4da-179">0x0000000D</span></span>                      |
| <span data-ttu-id="ba4da-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-180">System-Flags</span></span>           | <span data-ttu-id="ba4da-181">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ba4da-181">0x00000012</span></span>                      |
| <span data-ttu-id="ba4da-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba4da-182">Classes used in</span></span>        | [<span data-ttu-id="ba4da-183">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ba4da-183">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ba4da-184">亞當</span><span class="sxs-lookup"><span data-stu-id="ba4da-184">ADAM</span></span>



| <span data-ttu-id="ba4da-185">進入</span><span class="sxs-lookup"><span data-stu-id="ba4da-185">Entry</span></span> | <span data-ttu-id="ba4da-186">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-186">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba4da-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba4da-187">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba4da-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba4da-188">MAPI-Id</span></span>                | <span data-ttu-id="ba4da-189">0x8202</span><span class="sxs-lookup"><span data-stu-id="ba4da-189">0x8202</span></span>                          |
| <span data-ttu-id="ba4da-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba4da-190">System-Only</span></span>            | <span data-ttu-id="ba4da-191">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-191">True</span></span>                            |
| <span data-ttu-id="ba4da-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba4da-192">Is-Single-Valued</span></span>       | <span data-ttu-id="ba4da-193">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-193">True</span></span>                            |
| <span data-ttu-id="ba4da-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba4da-194">Is Indexed</span></span>             | <span data-ttu-id="ba4da-195">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-195">True</span></span>                            |
| <span data-ttu-id="ba4da-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba4da-196">In Global Catalog</span></span>      | <span data-ttu-id="ba4da-197">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-197">True</span></span>                            |
| <span data-ttu-id="ba4da-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba4da-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba4da-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba4da-199">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba4da-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba4da-200">Range-Lower</span></span>            | <span data-ttu-id="ba4da-201">1</span><span class="sxs-lookup"><span data-stu-id="ba4da-201">1</span></span>                               |
| <span data-ttu-id="ba4da-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba4da-202">Range-Upper</span></span>            | <span data-ttu-id="ba4da-203">255</span><span class="sxs-lookup"><span data-stu-id="ba4da-203">255</span></span>                             |
| <span data-ttu-id="ba4da-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-204">Search-Flags</span></span>           | <span data-ttu-id="ba4da-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="ba4da-205">0x0000000D</span></span>                      |
| <span data-ttu-id="ba4da-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-206">System-Flags</span></span>           | <span data-ttu-id="ba4da-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ba4da-207">0x00000012</span></span>                      |
| <span data-ttu-id="ba4da-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba4da-208">Classes used in</span></span>        | [<span data-ttu-id="ba4da-209">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ba4da-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ba4da-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ba4da-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ba4da-211">進入</span><span class="sxs-lookup"><span data-stu-id="ba4da-211">Entry</span></span> | <span data-ttu-id="ba4da-212">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba4da-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba4da-213">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba4da-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba4da-214">MAPI-Id</span></span>                | <span data-ttu-id="ba4da-215">0x8202</span><span class="sxs-lookup"><span data-stu-id="ba4da-215">0x8202</span></span>                          |
| <span data-ttu-id="ba4da-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba4da-216">System-Only</span></span>            | <span data-ttu-id="ba4da-217">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-217">True</span></span>                            |
| <span data-ttu-id="ba4da-218">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba4da-218">Is-Single-Valued</span></span>       | <span data-ttu-id="ba4da-219">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-219">True</span></span>                            |
| <span data-ttu-id="ba4da-220">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba4da-220">Is Indexed</span></span>             | <span data-ttu-id="ba4da-221">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-221">True</span></span>                            |
| <span data-ttu-id="ba4da-222">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba4da-222">In Global Catalog</span></span>      | <span data-ttu-id="ba4da-223">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-223">True</span></span>                            |
| <span data-ttu-id="ba4da-224">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba4da-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba4da-225">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba4da-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba4da-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba4da-226">Range-Lower</span></span>            | <span data-ttu-id="ba4da-227">1</span><span class="sxs-lookup"><span data-stu-id="ba4da-227">1</span></span>                               |
| <span data-ttu-id="ba4da-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba4da-228">Range-Upper</span></span>            | <span data-ttu-id="ba4da-229">255</span><span class="sxs-lookup"><span data-stu-id="ba4da-229">255</span></span>                             |
| <span data-ttu-id="ba4da-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-230">Search-Flags</span></span>           | <span data-ttu-id="ba4da-231">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="ba4da-231">0x0000000D</span></span>                      |
| <span data-ttu-id="ba4da-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-232">System-Flags</span></span>           | <span data-ttu-id="ba4da-233">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ba4da-233">0x00000012</span></span>                      |
| <span data-ttu-id="ba4da-234">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba4da-234">Classes used in</span></span>        | [<span data-ttu-id="ba4da-235">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ba4da-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ba4da-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba4da-236">Windows Server 2008</span></span>



| <span data-ttu-id="ba4da-237">進入</span><span class="sxs-lookup"><span data-stu-id="ba4da-237">Entry</span></span> | <span data-ttu-id="ba4da-238">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba4da-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba4da-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba4da-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba4da-240">MAPI-Id</span></span>                | <span data-ttu-id="ba4da-241">0x8202</span><span class="sxs-lookup"><span data-stu-id="ba4da-241">0x8202</span></span>                          |
| <span data-ttu-id="ba4da-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba4da-242">System-Only</span></span>            | <span data-ttu-id="ba4da-243">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-243">True</span></span>                            |
| <span data-ttu-id="ba4da-244">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba4da-244">Is-Single-Valued</span></span>       | <span data-ttu-id="ba4da-245">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-245">True</span></span>                            |
| <span data-ttu-id="ba4da-246">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba4da-246">Is Indexed</span></span>             | <span data-ttu-id="ba4da-247">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-247">True</span></span>                            |
| <span data-ttu-id="ba4da-248">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba4da-248">In Global Catalog</span></span>      | <span data-ttu-id="ba4da-249">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-249">True</span></span>                            |
| <span data-ttu-id="ba4da-250">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba4da-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba4da-251">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba4da-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba4da-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba4da-252">Range-Lower</span></span>            | <span data-ttu-id="ba4da-253">1</span><span class="sxs-lookup"><span data-stu-id="ba4da-253">1</span></span>                               |
| <span data-ttu-id="ba4da-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba4da-254">Range-Upper</span></span>            | <span data-ttu-id="ba4da-255">255</span><span class="sxs-lookup"><span data-stu-id="ba4da-255">255</span></span>                             |
| <span data-ttu-id="ba4da-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-256">Search-Flags</span></span>           | <span data-ttu-id="ba4da-257">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="ba4da-257">0x0000000D</span></span>                      |
| <span data-ttu-id="ba4da-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-258">System-Flags</span></span>           | <span data-ttu-id="ba4da-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ba4da-259">0x00000012</span></span>                      |
| <span data-ttu-id="ba4da-260">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba4da-260">Classes used in</span></span>        | [<span data-ttu-id="ba4da-261">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ba4da-261">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ba4da-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba4da-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ba4da-263">進入</span><span class="sxs-lookup"><span data-stu-id="ba4da-263">Entry</span></span> | <span data-ttu-id="ba4da-264">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-264">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba4da-265">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba4da-265">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba4da-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba4da-266">MAPI-Id</span></span>                | <span data-ttu-id="ba4da-267">0x8202</span><span class="sxs-lookup"><span data-stu-id="ba4da-267">0x8202</span></span>                          |
| <span data-ttu-id="ba4da-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba4da-268">System-Only</span></span>            | <span data-ttu-id="ba4da-269">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-269">True</span></span>                            |
| <span data-ttu-id="ba4da-270">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba4da-270">Is-Single-Valued</span></span>       | <span data-ttu-id="ba4da-271">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-271">True</span></span>                            |
| <span data-ttu-id="ba4da-272">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba4da-272">Is Indexed</span></span>             | <span data-ttu-id="ba4da-273">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-273">True</span></span>                            |
| <span data-ttu-id="ba4da-274">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba4da-274">In Global Catalog</span></span>      | <span data-ttu-id="ba4da-275">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-275">True</span></span>                            |
| <span data-ttu-id="ba4da-276">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba4da-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba4da-277">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba4da-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba4da-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba4da-278">Range-Lower</span></span>            | <span data-ttu-id="ba4da-279">1</span><span class="sxs-lookup"><span data-stu-id="ba4da-279">1</span></span>                               |
| <span data-ttu-id="ba4da-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba4da-280">Range-Upper</span></span>            | <span data-ttu-id="ba4da-281">255</span><span class="sxs-lookup"><span data-stu-id="ba4da-281">255</span></span>                             |
| <span data-ttu-id="ba4da-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-282">Search-Flags</span></span>           | <span data-ttu-id="ba4da-283">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="ba4da-283">0x0000000D</span></span>                      |
| <span data-ttu-id="ba4da-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-284">System-Flags</span></span>           | <span data-ttu-id="ba4da-285">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ba4da-285">0x00000012</span></span>                      |
| <span data-ttu-id="ba4da-286">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba4da-286">Classes used in</span></span>        | [<span data-ttu-id="ba4da-287">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ba4da-287">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ba4da-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ba4da-288">Windows Server 2012</span></span>



| <span data-ttu-id="ba4da-289">進入</span><span class="sxs-lookup"><span data-stu-id="ba4da-289">Entry</span></span> | <span data-ttu-id="ba4da-290">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-290">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ba4da-291">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ba4da-291">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ba4da-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba4da-292">MAPI-Id</span></span>                | <span data-ttu-id="ba4da-293">0x8202</span><span class="sxs-lookup"><span data-stu-id="ba4da-293">0x8202</span></span>                          |
| <span data-ttu-id="ba4da-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba4da-294">System-Only</span></span>            | <span data-ttu-id="ba4da-295">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-295">True</span></span>                            |
| <span data-ttu-id="ba4da-296">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ba4da-296">Is-Single-Valued</span></span>       | <span data-ttu-id="ba4da-297">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-297">True</span></span>                            |
| <span data-ttu-id="ba4da-298">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ba4da-298">Is Indexed</span></span>             | <span data-ttu-id="ba4da-299">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-299">True</span></span>                            |
| <span data-ttu-id="ba4da-300">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ba4da-300">In Global Catalog</span></span>      | <span data-ttu-id="ba4da-301">對</span><span class="sxs-lookup"><span data-stu-id="ba4da-301">True</span></span>                            |
| <span data-ttu-id="ba4da-302">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ba4da-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba4da-303">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ba4da-303">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ba4da-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba4da-304">Range-Lower</span></span>            | <span data-ttu-id="ba4da-305">1</span><span class="sxs-lookup"><span data-stu-id="ba4da-305">1</span></span>                               |
| <span data-ttu-id="ba4da-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba4da-306">Range-Upper</span></span>            | <span data-ttu-id="ba4da-307">255</span><span class="sxs-lookup"><span data-stu-id="ba4da-307">255</span></span>                             |
| <span data-ttu-id="ba4da-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-308">Search-Flags</span></span>           | <span data-ttu-id="ba4da-309">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="ba4da-309">0x0000000D</span></span>                      |
| <span data-ttu-id="ba4da-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba4da-310">System-Flags</span></span>           | <span data-ttu-id="ba4da-311">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ba4da-311">0x00000012</span></span>                      |
| <span data-ttu-id="ba4da-312">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ba4da-312">Classes used in</span></span>        | [<span data-ttu-id="ba4da-313">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ba4da-313">**Top**</span></span>](c-top.md)<br/> |



 

 






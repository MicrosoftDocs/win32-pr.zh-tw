---
title: 站台連結清單屬性
description: 與此橋接器相關聯的站台連結清單。
ms.assetid: 79ec0ae2-ceb3-4321-8b6d-ce5c3bda667a
ms.tgt_platform: multiple
keywords:
- 站台連結清單屬性 AD 架構
- siteLinkList 屬性 AD 架構
topic_type:
- apiref
api_name:
- Site-Link-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e71284e4650a3cb146b1656c846483e33a6dd66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385422"
---
# <a name="site-link-list-attribute"></a><span data-ttu-id="99bcd-105">站台連結清單屬性</span><span class="sxs-lookup"><span data-stu-id="99bcd-105">Site-Link-List attribute</span></span>

<span data-ttu-id="99bcd-106">與此橋接器相關聯的站台連結清單。</span><span class="sxs-lookup"><span data-stu-id="99bcd-106">List of site links that are associated with this bridge.</span></span>



| <span data-ttu-id="99bcd-107">進入</span><span class="sxs-lookup"><span data-stu-id="99bcd-107">Entry</span></span> | <span data-ttu-id="99bcd-108">值</span><span class="sxs-lookup"><span data-stu-id="99bcd-108">Value</span></span> |
|-------------------|--------------------------------------------------------------|
| <span data-ttu-id="99bcd-109">CN</span><span class="sxs-lookup"><span data-stu-id="99bcd-109">CN</span></span>                | <span data-ttu-id="99bcd-110">網站連結清單</span><span class="sxs-lookup"><span data-stu-id="99bcd-110">Site-Link-List</span></span>                                               |
| <span data-ttu-id="99bcd-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="99bcd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="99bcd-112">siteLinkList</span><span class="sxs-lookup"><span data-stu-id="99bcd-112">siteLinkList</span></span>                                                 |
| <span data-ttu-id="99bcd-113">大小</span><span class="sxs-lookup"><span data-stu-id="99bcd-113">Size</span></span>              | \-                                                           |
| <span data-ttu-id="99bcd-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="99bcd-114">Update Privilege</span></span>  | <span data-ttu-id="99bcd-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="99bcd-115">Domain administrator</span></span>                                         |
| <span data-ttu-id="99bcd-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="99bcd-116">Update Frequency</span></span>  | <span data-ttu-id="99bcd-117">每次在橋接器新增或移除站台連結時。</span><span class="sxs-lookup"><span data-stu-id="99bcd-117">Whenever a site link is added to or removed from the bridge.</span></span> |
| <span data-ttu-id="99bcd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="99bcd-118">Attribute-Id</span></span>      | <span data-ttu-id="99bcd-119">1.2.840.113556.1.4.822</span><span class="sxs-lookup"><span data-stu-id="99bcd-119">1.2.840.113556.1.4.822</span></span>                                       |
| <span data-ttu-id="99bcd-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="99bcd-120">System-Id-Guid</span></span>    | <span data-ttu-id="99bcd-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="99bcd-121">d50c2cdd-8951-11d1-aebc-0000f80367c1</span></span>                         |
| <span data-ttu-id="99bcd-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="99bcd-122">Syntax</span></span>            | [<span data-ttu-id="99bcd-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="99bcd-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                      |



## <a name="implementations"></a><span data-ttu-id="99bcd-124">實作</span><span class="sxs-lookup"><span data-stu-id="99bcd-124">Implementations</span></span>

-   [<span data-ttu-id="99bcd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="99bcd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="99bcd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="99bcd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="99bcd-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="99bcd-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="99bcd-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="99bcd-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="99bcd-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="99bcd-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="99bcd-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="99bcd-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="99bcd-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="99bcd-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="99bcd-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="99bcd-132">Windows 2000 Server</span></span>



| <span data-ttu-id="99bcd-133">進入</span><span class="sxs-lookup"><span data-stu-id="99bcd-133">Entry</span></span> | <span data-ttu-id="99bcd-134">值</span><span class="sxs-lookup"><span data-stu-id="99bcd-134">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="99bcd-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bcd-135">Link-Id</span></span>                | <span data-ttu-id="99bcd-136">142</span><span class="sxs-lookup"><span data-stu-id="99bcd-136">142</span></span>                                                     |
| <span data-ttu-id="99bcd-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bcd-137">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="99bcd-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bcd-138">System-Only</span></span>            | <span data-ttu-id="99bcd-139">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-139">False</span></span>                                                   |
| <span data-ttu-id="99bcd-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bcd-140">Is-Single-Valued</span></span>       | <span data-ttu-id="99bcd-141">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-141">False</span></span>                                                   |
| <span data-ttu-id="99bcd-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bcd-142">Is Indexed</span></span>             | <span data-ttu-id="99bcd-143">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-143">False</span></span>                                                   |
| <span data-ttu-id="99bcd-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bcd-144">In Global Catalog</span></span>      | <span data-ttu-id="99bcd-145">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-145">False</span></span>                                                   |
| <span data-ttu-id="99bcd-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bcd-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bcd-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bcd-147">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="99bcd-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bcd-148">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bcd-149">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-150">Search-Flags</span></span>           | <span data-ttu-id="99bcd-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bcd-151">0x00000000</span></span>                                              |
| <span data-ttu-id="99bcd-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-152">System-Flags</span></span>           | <span data-ttu-id="99bcd-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bcd-153">0x00000010</span></span>                                              |
| <span data-ttu-id="99bcd-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bcd-154">Classes used in</span></span>        | [<span data-ttu-id="99bcd-155">**網站-連結-橋接器**</span><span class="sxs-lookup"><span data-stu-id="99bcd-155">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="99bcd-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99bcd-156">Windows Server 2003</span></span>



| <span data-ttu-id="99bcd-157">進入</span><span class="sxs-lookup"><span data-stu-id="99bcd-157">Entry</span></span> | <span data-ttu-id="99bcd-158">值</span><span class="sxs-lookup"><span data-stu-id="99bcd-158">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="99bcd-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bcd-159">Link-Id</span></span>                | <span data-ttu-id="99bcd-160">142</span><span class="sxs-lookup"><span data-stu-id="99bcd-160">142</span></span>                                                     |
| <span data-ttu-id="99bcd-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bcd-161">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="99bcd-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bcd-162">System-Only</span></span>            | <span data-ttu-id="99bcd-163">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-163">False</span></span>                                                   |
| <span data-ttu-id="99bcd-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bcd-164">Is-Single-Valued</span></span>       | <span data-ttu-id="99bcd-165">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-165">False</span></span>                                                   |
| <span data-ttu-id="99bcd-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bcd-166">Is Indexed</span></span>             | <span data-ttu-id="99bcd-167">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-167">False</span></span>                                                   |
| <span data-ttu-id="99bcd-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bcd-168">In Global Catalog</span></span>      | <span data-ttu-id="99bcd-169">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-169">False</span></span>                                                   |
| <span data-ttu-id="99bcd-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bcd-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bcd-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bcd-171">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="99bcd-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bcd-172">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bcd-173">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-174">Search-Flags</span></span>           | <span data-ttu-id="99bcd-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bcd-175">0x00000000</span></span>                                              |
| <span data-ttu-id="99bcd-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-176">System-Flags</span></span>           | <span data-ttu-id="99bcd-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bcd-177">0x00000010</span></span>                                              |
| <span data-ttu-id="99bcd-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bcd-178">Classes used in</span></span>        | [<span data-ttu-id="99bcd-179">**網站-連結-橋接器**</span><span class="sxs-lookup"><span data-stu-id="99bcd-179">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="adam"></a><span data-ttu-id="99bcd-180">亞當</span><span class="sxs-lookup"><span data-stu-id="99bcd-180">ADAM</span></span>



| <span data-ttu-id="99bcd-181">進入</span><span class="sxs-lookup"><span data-stu-id="99bcd-181">Entry</span></span> | <span data-ttu-id="99bcd-182">值</span><span class="sxs-lookup"><span data-stu-id="99bcd-182">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="99bcd-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bcd-183">Link-Id</span></span>                | <span data-ttu-id="99bcd-184">142</span><span class="sxs-lookup"><span data-stu-id="99bcd-184">142</span></span>                                                     |
| <span data-ttu-id="99bcd-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bcd-185">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="99bcd-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bcd-186">System-Only</span></span>            | <span data-ttu-id="99bcd-187">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-187">False</span></span>                                                   |
| <span data-ttu-id="99bcd-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bcd-188">Is-Single-Valued</span></span>       | <span data-ttu-id="99bcd-189">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-189">False</span></span>                                                   |
| <span data-ttu-id="99bcd-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bcd-190">Is Indexed</span></span>             | <span data-ttu-id="99bcd-191">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-191">False</span></span>                                                   |
| <span data-ttu-id="99bcd-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bcd-192">In Global Catalog</span></span>      | <span data-ttu-id="99bcd-193">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-193">False</span></span>                                                   |
| <span data-ttu-id="99bcd-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bcd-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bcd-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bcd-195">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="99bcd-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bcd-196">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bcd-197">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-198">Search-Flags</span></span>           | <span data-ttu-id="99bcd-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bcd-199">0x00000000</span></span>                                              |
| <span data-ttu-id="99bcd-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-200">System-Flags</span></span>           | <span data-ttu-id="99bcd-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bcd-201">0x00000010</span></span>                                              |
| <span data-ttu-id="99bcd-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bcd-202">Classes used in</span></span>        | [<span data-ttu-id="99bcd-203">**網站-連結-橋接器**</span><span class="sxs-lookup"><span data-stu-id="99bcd-203">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="99bcd-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="99bcd-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="99bcd-205">進入</span><span class="sxs-lookup"><span data-stu-id="99bcd-205">Entry</span></span> | <span data-ttu-id="99bcd-206">值</span><span class="sxs-lookup"><span data-stu-id="99bcd-206">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="99bcd-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bcd-207">Link-Id</span></span>                | <span data-ttu-id="99bcd-208">142</span><span class="sxs-lookup"><span data-stu-id="99bcd-208">142</span></span>                                                     |
| <span data-ttu-id="99bcd-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bcd-209">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="99bcd-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bcd-210">System-Only</span></span>            | <span data-ttu-id="99bcd-211">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-211">False</span></span>                                                   |
| <span data-ttu-id="99bcd-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bcd-212">Is-Single-Valued</span></span>       | <span data-ttu-id="99bcd-213">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-213">False</span></span>                                                   |
| <span data-ttu-id="99bcd-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bcd-214">Is Indexed</span></span>             | <span data-ttu-id="99bcd-215">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-215">False</span></span>                                                   |
| <span data-ttu-id="99bcd-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bcd-216">In Global Catalog</span></span>      | <span data-ttu-id="99bcd-217">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-217">False</span></span>                                                   |
| <span data-ttu-id="99bcd-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bcd-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bcd-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bcd-219">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="99bcd-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bcd-220">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bcd-221">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-222">Search-Flags</span></span>           | <span data-ttu-id="99bcd-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bcd-223">0x00000000</span></span>                                              |
| <span data-ttu-id="99bcd-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-224">System-Flags</span></span>           | <span data-ttu-id="99bcd-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bcd-225">0x00000010</span></span>                                              |
| <span data-ttu-id="99bcd-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bcd-226">Classes used in</span></span>        | [<span data-ttu-id="99bcd-227">**網站-連結-橋接器**</span><span class="sxs-lookup"><span data-stu-id="99bcd-227">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="99bcd-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99bcd-228">Windows Server 2008</span></span>



| <span data-ttu-id="99bcd-229">進入</span><span class="sxs-lookup"><span data-stu-id="99bcd-229">Entry</span></span> | <span data-ttu-id="99bcd-230">值</span><span class="sxs-lookup"><span data-stu-id="99bcd-230">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="99bcd-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bcd-231">Link-Id</span></span>                | <span data-ttu-id="99bcd-232">142</span><span class="sxs-lookup"><span data-stu-id="99bcd-232">142</span></span>                                                     |
| <span data-ttu-id="99bcd-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bcd-233">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="99bcd-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bcd-234">System-Only</span></span>            | <span data-ttu-id="99bcd-235">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-235">False</span></span>                                                   |
| <span data-ttu-id="99bcd-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bcd-236">Is-Single-Valued</span></span>       | <span data-ttu-id="99bcd-237">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-237">False</span></span>                                                   |
| <span data-ttu-id="99bcd-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bcd-238">Is Indexed</span></span>             | <span data-ttu-id="99bcd-239">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-239">False</span></span>                                                   |
| <span data-ttu-id="99bcd-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bcd-240">In Global Catalog</span></span>      | <span data-ttu-id="99bcd-241">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-241">False</span></span>                                                   |
| <span data-ttu-id="99bcd-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bcd-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bcd-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bcd-243">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="99bcd-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bcd-244">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bcd-245">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-246">Search-Flags</span></span>           | <span data-ttu-id="99bcd-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bcd-247">0x00000000</span></span>                                              |
| <span data-ttu-id="99bcd-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-248">System-Flags</span></span>           | <span data-ttu-id="99bcd-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bcd-249">0x00000010</span></span>                                              |
| <span data-ttu-id="99bcd-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bcd-250">Classes used in</span></span>        | [<span data-ttu-id="99bcd-251">**網站-連結-橋接器**</span><span class="sxs-lookup"><span data-stu-id="99bcd-251">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="99bcd-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99bcd-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="99bcd-253">進入</span><span class="sxs-lookup"><span data-stu-id="99bcd-253">Entry</span></span> | <span data-ttu-id="99bcd-254">值</span><span class="sxs-lookup"><span data-stu-id="99bcd-254">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="99bcd-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bcd-255">Link-Id</span></span>                | <span data-ttu-id="99bcd-256">142</span><span class="sxs-lookup"><span data-stu-id="99bcd-256">142</span></span>                                                     |
| <span data-ttu-id="99bcd-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bcd-257">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="99bcd-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bcd-258">System-Only</span></span>            | <span data-ttu-id="99bcd-259">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-259">False</span></span>                                                   |
| <span data-ttu-id="99bcd-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bcd-260">Is-Single-Valued</span></span>       | <span data-ttu-id="99bcd-261">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-261">False</span></span>                                                   |
| <span data-ttu-id="99bcd-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bcd-262">Is Indexed</span></span>             | <span data-ttu-id="99bcd-263">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-263">False</span></span>                                                   |
| <span data-ttu-id="99bcd-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bcd-264">In Global Catalog</span></span>      | <span data-ttu-id="99bcd-265">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-265">False</span></span>                                                   |
| <span data-ttu-id="99bcd-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bcd-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bcd-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bcd-267">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="99bcd-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bcd-268">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bcd-269">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-270">Search-Flags</span></span>           | <span data-ttu-id="99bcd-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bcd-271">0x00000000</span></span>                                              |
| <span data-ttu-id="99bcd-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-272">System-Flags</span></span>           | <span data-ttu-id="99bcd-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bcd-273">0x00000010</span></span>                                              |
| <span data-ttu-id="99bcd-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bcd-274">Classes used in</span></span>        | [<span data-ttu-id="99bcd-275">**網站-連結-橋接器**</span><span class="sxs-lookup"><span data-stu-id="99bcd-275">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="99bcd-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99bcd-276">Windows Server 2012</span></span>



| <span data-ttu-id="99bcd-277">進入</span><span class="sxs-lookup"><span data-stu-id="99bcd-277">Entry</span></span> | <span data-ttu-id="99bcd-278">值</span><span class="sxs-lookup"><span data-stu-id="99bcd-278">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="99bcd-279">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bcd-279">Link-Id</span></span>                | <span data-ttu-id="99bcd-280">142</span><span class="sxs-lookup"><span data-stu-id="99bcd-280">142</span></span>                                                     |
| <span data-ttu-id="99bcd-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bcd-281">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="99bcd-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bcd-282">System-Only</span></span>            | <span data-ttu-id="99bcd-283">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-283">False</span></span>                                                   |
| <span data-ttu-id="99bcd-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bcd-284">Is-Single-Valued</span></span>       | <span data-ttu-id="99bcd-285">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-285">False</span></span>                                                   |
| <span data-ttu-id="99bcd-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bcd-286">Is Indexed</span></span>             | <span data-ttu-id="99bcd-287">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-287">False</span></span>                                                   |
| <span data-ttu-id="99bcd-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bcd-288">In Global Catalog</span></span>      | <span data-ttu-id="99bcd-289">否</span><span class="sxs-lookup"><span data-stu-id="99bcd-289">False</span></span>                                                   |
| <span data-ttu-id="99bcd-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bcd-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bcd-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bcd-291">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="99bcd-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bcd-292">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bcd-293">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="99bcd-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-294">Search-Flags</span></span>           | <span data-ttu-id="99bcd-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bcd-295">0x00000000</span></span>                                              |
| <span data-ttu-id="99bcd-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bcd-296">System-Flags</span></span>           | <span data-ttu-id="99bcd-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bcd-297">0x00000010</span></span>                                              |
| <span data-ttu-id="99bcd-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bcd-298">Classes used in</span></span>        | [<span data-ttu-id="99bcd-299">**網站-連結-橋接器**</span><span class="sxs-lookup"><span data-stu-id="99bcd-299">**Site-Link-Bridge**</span></span>](c-sitelinkbridge.md)<br/> |



 

 






---
title: 管理-屬性頁屬性
description: 要在 Active Directory 管理畫面上顯示之物件的屬性頁的順序編號和 GUID。 如需詳細資訊，請參閱檔，擴充目錄物件的消費者介面。
ms.assetid: 70455768-11e0-4d12-ad44-4b3115aa1594
ms.tgt_platform: multiple
keywords:
- 管理-屬性頁屬性 AD 架構
- adminPropertyPages 屬性 AD 架構
topic_type:
- apiref
api_name:
- Admin-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d4e3814662cc8acf1a987cb92a1b9579cc43a4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "107000035"
---
# <a name="admin-property-pages-attribute"></a><span data-ttu-id="53540-106">管理-屬性頁屬性</span><span class="sxs-lookup"><span data-stu-id="53540-106">Admin-Property-Pages attribute</span></span>

<span data-ttu-id="53540-107">要在 Active Directory 管理畫面上顯示之物件的屬性頁的順序編號和 GUID。</span><span class="sxs-lookup"><span data-stu-id="53540-107">The order number and GUID of the property pages for an object to be displayed on Active Directory administration screens.</span></span> <span data-ttu-id="53540-108">如需詳細資訊，請參閱檔，擴充目錄物件的消費者介面。</span><span class="sxs-lookup"><span data-stu-id="53540-108">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="53540-109">進入</span><span class="sxs-lookup"><span data-stu-id="53540-109">Entry</span></span> | <span data-ttu-id="53540-110">值</span><span class="sxs-lookup"><span data-stu-id="53540-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="53540-111">CN</span><span class="sxs-lookup"><span data-stu-id="53540-111">CN</span></span>                | <span data-ttu-id="53540-112">管理-屬性頁</span><span class="sxs-lookup"><span data-stu-id="53540-112">Admin-Property-Pages</span></span>                           |
| <span data-ttu-id="53540-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="53540-113">Ldap-Display-Name</span></span> | <span data-ttu-id="53540-114">adminPropertyPages</span><span class="sxs-lookup"><span data-stu-id="53540-114">adminPropertyPages</span></span>                             |
| <span data-ttu-id="53540-115">大小</span><span class="sxs-lookup"><span data-stu-id="53540-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="53540-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="53540-116">Update Privilege</span></span>  | <span data-ttu-id="53540-117">網域系統管理員或應用程式開發人員。</span><span class="sxs-lookup"><span data-stu-id="53540-117">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="53540-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="53540-118">Update Frequency</span></span>  | <span data-ttu-id="53540-119">每當加入或移除屬性頁時。</span><span class="sxs-lookup"><span data-stu-id="53540-119">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="53540-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53540-120">Attribute-Id</span></span>      | <span data-ttu-id="53540-121">1.2.840.113556.1.4.562</span><span class="sxs-lookup"><span data-stu-id="53540-121">1.2.840.113556.1.4.562</span></span>                         |
| <span data-ttu-id="53540-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="53540-122">System-Id-Guid</span></span>    | <span data-ttu-id="53540-123">52458038-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="53540-123">52458038-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="53540-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="53540-124">Syntax</span></span>            | [<span data-ttu-id="53540-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="53540-125">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="53540-126">實作</span><span class="sxs-lookup"><span data-stu-id="53540-126">Implementations</span></span>

-   [<span data-ttu-id="53540-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="53540-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="53540-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="53540-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="53540-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="53540-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="53540-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="53540-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="53540-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="53540-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="53540-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53540-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="53540-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53540-133">Windows 2000 Server</span></span>



| <span data-ttu-id="53540-134">進入</span><span class="sxs-lookup"><span data-stu-id="53540-134">Entry</span></span> | <span data-ttu-id="53540-135">值</span><span class="sxs-lookup"><span data-stu-id="53540-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="53540-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="53540-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53540-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="53540-138">System-Only</span></span>            | <span data-ttu-id="53540-139">否</span><span class="sxs-lookup"><span data-stu-id="53540-139">False</span></span>                                                      |
| <span data-ttu-id="53540-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="53540-140">Is-Single-Valued</span></span>       | <span data-ttu-id="53540-141">否</span><span class="sxs-lookup"><span data-stu-id="53540-141">False</span></span>                                                      |
| <span data-ttu-id="53540-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="53540-142">Is Indexed</span></span>             | <span data-ttu-id="53540-143">否</span><span class="sxs-lookup"><span data-stu-id="53540-143">False</span></span>                                                      |
| <span data-ttu-id="53540-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="53540-144">In Global Catalog</span></span>      | <span data-ttu-id="53540-145">否</span><span class="sxs-lookup"><span data-stu-id="53540-145">False</span></span>                                                      |
| <span data-ttu-id="53540-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="53540-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="53540-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="53540-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="53540-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53540-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="53540-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53540-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="53540-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-150">Search-Flags</span></span>           | <span data-ttu-id="53540-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53540-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="53540-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-152">System-Flags</span></span>           | <span data-ttu-id="53540-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53540-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="53540-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="53540-154">Classes used in</span></span>        | [<span data-ttu-id="53540-155">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="53540-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="53540-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53540-156">Windows Server 2003</span></span>



| <span data-ttu-id="53540-157">進入</span><span class="sxs-lookup"><span data-stu-id="53540-157">Entry</span></span> | <span data-ttu-id="53540-158">值</span><span class="sxs-lookup"><span data-stu-id="53540-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="53540-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="53540-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53540-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="53540-161">System-Only</span></span>            | <span data-ttu-id="53540-162">否</span><span class="sxs-lookup"><span data-stu-id="53540-162">False</span></span>                                                      |
| <span data-ttu-id="53540-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="53540-163">Is-Single-Valued</span></span>       | <span data-ttu-id="53540-164">否</span><span class="sxs-lookup"><span data-stu-id="53540-164">False</span></span>                                                      |
| <span data-ttu-id="53540-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="53540-165">Is Indexed</span></span>             | <span data-ttu-id="53540-166">否</span><span class="sxs-lookup"><span data-stu-id="53540-166">False</span></span>                                                      |
| <span data-ttu-id="53540-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="53540-167">In Global Catalog</span></span>      | <span data-ttu-id="53540-168">否</span><span class="sxs-lookup"><span data-stu-id="53540-168">False</span></span>                                                      |
| <span data-ttu-id="53540-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="53540-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="53540-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="53540-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="53540-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53540-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="53540-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53540-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="53540-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-173">Search-Flags</span></span>           | <span data-ttu-id="53540-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53540-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="53540-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-175">System-Flags</span></span>           | <span data-ttu-id="53540-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53540-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="53540-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="53540-177">Classes used in</span></span>        | [<span data-ttu-id="53540-178">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="53540-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="53540-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="53540-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="53540-180">進入</span><span class="sxs-lookup"><span data-stu-id="53540-180">Entry</span></span> | <span data-ttu-id="53540-181">值</span><span class="sxs-lookup"><span data-stu-id="53540-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="53540-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="53540-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53540-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="53540-184">System-Only</span></span>            | <span data-ttu-id="53540-185">否</span><span class="sxs-lookup"><span data-stu-id="53540-185">False</span></span>                                                      |
| <span data-ttu-id="53540-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="53540-186">Is-Single-Valued</span></span>       | <span data-ttu-id="53540-187">否</span><span class="sxs-lookup"><span data-stu-id="53540-187">False</span></span>                                                      |
| <span data-ttu-id="53540-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="53540-188">Is Indexed</span></span>             | <span data-ttu-id="53540-189">否</span><span class="sxs-lookup"><span data-stu-id="53540-189">False</span></span>                                                      |
| <span data-ttu-id="53540-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="53540-190">In Global Catalog</span></span>      | <span data-ttu-id="53540-191">否</span><span class="sxs-lookup"><span data-stu-id="53540-191">False</span></span>                                                      |
| <span data-ttu-id="53540-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="53540-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="53540-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="53540-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="53540-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53540-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="53540-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53540-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="53540-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-196">Search-Flags</span></span>           | <span data-ttu-id="53540-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53540-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="53540-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-198">System-Flags</span></span>           | <span data-ttu-id="53540-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53540-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="53540-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="53540-200">Classes used in</span></span>        | [<span data-ttu-id="53540-201">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="53540-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="53540-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53540-202">Windows Server 2008</span></span>



| <span data-ttu-id="53540-203">進入</span><span class="sxs-lookup"><span data-stu-id="53540-203">Entry</span></span> | <span data-ttu-id="53540-204">值</span><span class="sxs-lookup"><span data-stu-id="53540-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="53540-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="53540-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53540-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="53540-207">System-Only</span></span>            | <span data-ttu-id="53540-208">否</span><span class="sxs-lookup"><span data-stu-id="53540-208">False</span></span>                                                      |
| <span data-ttu-id="53540-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="53540-209">Is-Single-Valued</span></span>       | <span data-ttu-id="53540-210">否</span><span class="sxs-lookup"><span data-stu-id="53540-210">False</span></span>                                                      |
| <span data-ttu-id="53540-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="53540-211">Is Indexed</span></span>             | <span data-ttu-id="53540-212">否</span><span class="sxs-lookup"><span data-stu-id="53540-212">False</span></span>                                                      |
| <span data-ttu-id="53540-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="53540-213">In Global Catalog</span></span>      | <span data-ttu-id="53540-214">否</span><span class="sxs-lookup"><span data-stu-id="53540-214">False</span></span>                                                      |
| <span data-ttu-id="53540-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="53540-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="53540-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="53540-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="53540-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53540-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="53540-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53540-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="53540-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-219">Search-Flags</span></span>           | <span data-ttu-id="53540-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53540-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="53540-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-221">System-Flags</span></span>           | <span data-ttu-id="53540-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53540-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="53540-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="53540-223">Classes used in</span></span>        | [<span data-ttu-id="53540-224">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="53540-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="53540-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53540-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="53540-226">進入</span><span class="sxs-lookup"><span data-stu-id="53540-226">Entry</span></span> | <span data-ttu-id="53540-227">值</span><span class="sxs-lookup"><span data-stu-id="53540-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="53540-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="53540-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53540-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="53540-230">System-Only</span></span>            | <span data-ttu-id="53540-231">否</span><span class="sxs-lookup"><span data-stu-id="53540-231">False</span></span>                                                      |
| <span data-ttu-id="53540-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="53540-232">Is-Single-Valued</span></span>       | <span data-ttu-id="53540-233">否</span><span class="sxs-lookup"><span data-stu-id="53540-233">False</span></span>                                                      |
| <span data-ttu-id="53540-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="53540-234">Is Indexed</span></span>             | <span data-ttu-id="53540-235">否</span><span class="sxs-lookup"><span data-stu-id="53540-235">False</span></span>                                                      |
| <span data-ttu-id="53540-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="53540-236">In Global Catalog</span></span>      | <span data-ttu-id="53540-237">否</span><span class="sxs-lookup"><span data-stu-id="53540-237">False</span></span>                                                      |
| <span data-ttu-id="53540-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="53540-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="53540-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="53540-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="53540-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53540-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="53540-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53540-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="53540-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-242">Search-Flags</span></span>           | <span data-ttu-id="53540-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53540-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="53540-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-244">System-Flags</span></span>           | <span data-ttu-id="53540-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53540-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="53540-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="53540-246">Classes used in</span></span>        | [<span data-ttu-id="53540-247">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="53540-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="53540-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53540-248">Windows Server 2012</span></span>



| <span data-ttu-id="53540-249">進入</span><span class="sxs-lookup"><span data-stu-id="53540-249">Entry</span></span> | <span data-ttu-id="53540-250">值</span><span class="sxs-lookup"><span data-stu-id="53540-250">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="53540-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="53540-251">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53540-252">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="53540-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="53540-253">System-Only</span></span>            | <span data-ttu-id="53540-254">否</span><span class="sxs-lookup"><span data-stu-id="53540-254">False</span></span>                                                      |
| <span data-ttu-id="53540-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="53540-255">Is-Single-Valued</span></span>       | <span data-ttu-id="53540-256">否</span><span class="sxs-lookup"><span data-stu-id="53540-256">False</span></span>                                                      |
| <span data-ttu-id="53540-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="53540-257">Is Indexed</span></span>             | <span data-ttu-id="53540-258">否</span><span class="sxs-lookup"><span data-stu-id="53540-258">False</span></span>                                                      |
| <span data-ttu-id="53540-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="53540-259">In Global Catalog</span></span>      | <span data-ttu-id="53540-260">否</span><span class="sxs-lookup"><span data-stu-id="53540-260">False</span></span>                                                      |
| <span data-ttu-id="53540-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="53540-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="53540-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="53540-262">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="53540-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53540-263">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="53540-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53540-264">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="53540-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-265">Search-Flags</span></span>           | <span data-ttu-id="53540-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53540-266">0x00000000</span></span>                                                 |
| <span data-ttu-id="53540-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53540-267">System-Flags</span></span>           | <span data-ttu-id="53540-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53540-268">0x00000010</span></span>                                                 |
| <span data-ttu-id="53540-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="53540-269">Classes used in</span></span>        | [<span data-ttu-id="53540-270">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="53540-270">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 






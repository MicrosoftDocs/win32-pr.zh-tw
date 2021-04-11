---
title: Shell-屬性頁屬性
description: 用來管理 Active Directory 物件的屬性頁的順序編號和 GUID。 您可以從 Windows shell 存取這些屬性頁。 如需詳細資訊，請參閱檔，擴充目錄物件的消費者介面。
ms.assetid: e0edd91b-bdb6-47aa-9be2-8a23a89adb26
ms.tgt_platform: multiple
keywords:
- Shell-屬性頁屬性 AD 架構
- shellPropertyPages 屬性 AD 架構
topic_type:
- apiref
api_name:
- Shell-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: befad2334a754843fa0ae412565db8c82260f7cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107525"
---
# <a name="shell-property-pages-attribute"></a><span data-ttu-id="39d8b-107">Shell-屬性頁屬性</span><span class="sxs-lookup"><span data-stu-id="39d8b-107">Shell-Property-Pages attribute</span></span>

<span data-ttu-id="39d8b-108">用來管理 Active Directory 物件的屬性頁的順序編號和 GUID。</span><span class="sxs-lookup"><span data-stu-id="39d8b-108">The order number and GUID of property pages for managing Active Directory objects.</span></span> <span data-ttu-id="39d8b-109">您可以從 Windows shell 存取這些屬性頁。</span><span class="sxs-lookup"><span data-stu-id="39d8b-109">These property pages can be accessed from the Windows shell.</span></span> <span data-ttu-id="39d8b-110">如需詳細資訊，請參閱檔，擴充目錄物件的消費者介面。</span><span class="sxs-lookup"><span data-stu-id="39d8b-110">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="39d8b-111">進入</span><span class="sxs-lookup"><span data-stu-id="39d8b-111">Entry</span></span> | <span data-ttu-id="39d8b-112">值</span><span class="sxs-lookup"><span data-stu-id="39d8b-112">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="39d8b-113">CN</span><span class="sxs-lookup"><span data-stu-id="39d8b-113">CN</span></span>                | <span data-ttu-id="39d8b-114">Shell-屬性頁</span><span class="sxs-lookup"><span data-stu-id="39d8b-114">Shell-Property-Pages</span></span>                           |
| <span data-ttu-id="39d8b-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="39d8b-115">Ldap-Display-Name</span></span> | <span data-ttu-id="39d8b-116">shellPropertyPages</span><span class="sxs-lookup"><span data-stu-id="39d8b-116">shellPropertyPages</span></span>                             |
| <span data-ttu-id="39d8b-117">大小</span><span class="sxs-lookup"><span data-stu-id="39d8b-117">Size</span></span>              | \-                                             |
| <span data-ttu-id="39d8b-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="39d8b-118">Update Privilege</span></span>  | <span data-ttu-id="39d8b-119">網域系統管理員或應用程式開發人員。</span><span class="sxs-lookup"><span data-stu-id="39d8b-119">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="39d8b-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="39d8b-120">Update Frequency</span></span>  | <span data-ttu-id="39d8b-121">每當加入或移除屬性頁時。</span><span class="sxs-lookup"><span data-stu-id="39d8b-121">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="39d8b-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39d8b-122">Attribute-Id</span></span>      | <span data-ttu-id="39d8b-123">1.2.840.113556.1.4.563</span><span class="sxs-lookup"><span data-stu-id="39d8b-123">1.2.840.113556.1.4.563</span></span>                         |
| <span data-ttu-id="39d8b-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="39d8b-124">System-Id-Guid</span></span>    | <span data-ttu-id="39d8b-125">52458039-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="39d8b-125">52458039-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="39d8b-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="39d8b-126">Syntax</span></span>            | [<span data-ttu-id="39d8b-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="39d8b-127">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="39d8b-128">實作</span><span class="sxs-lookup"><span data-stu-id="39d8b-128">Implementations</span></span>

-   [<span data-ttu-id="39d8b-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39d8b-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39d8b-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39d8b-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39d8b-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39d8b-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39d8b-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39d8b-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39d8b-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39d8b-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39d8b-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39d8b-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39d8b-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39d8b-135">Windows 2000 Server</span></span>



| <span data-ttu-id="39d8b-136">進入</span><span class="sxs-lookup"><span data-stu-id="39d8b-136">Entry</span></span> | <span data-ttu-id="39d8b-137">值</span><span class="sxs-lookup"><span data-stu-id="39d8b-137">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="39d8b-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="39d8b-138">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39d8b-139">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="39d8b-140">System-Only</span></span>            | <span data-ttu-id="39d8b-141">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-141">False</span></span>                                                      |
| <span data-ttu-id="39d8b-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="39d8b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="39d8b-143">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-143">False</span></span>                                                      |
| <span data-ttu-id="39d8b-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="39d8b-144">Is Indexed</span></span>             | <span data-ttu-id="39d8b-145">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-145">False</span></span>                                                      |
| <span data-ttu-id="39d8b-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="39d8b-146">In Global Catalog</span></span>      | <span data-ttu-id="39d8b-147">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-147">False</span></span>                                                      |
| <span data-ttu-id="39d8b-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="39d8b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="39d8b-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="39d8b-149">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="39d8b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39d8b-150">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39d8b-151">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-152">Search-Flags</span></span>           | <span data-ttu-id="39d8b-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39d8b-153">0x00000000</span></span>                                                 |
| <span data-ttu-id="39d8b-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-154">System-Flags</span></span>           | <span data-ttu-id="39d8b-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39d8b-155">0x00000010</span></span>                                                 |
| <span data-ttu-id="39d8b-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="39d8b-156">Classes used in</span></span>        | [<span data-ttu-id="39d8b-157">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="39d8b-157">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39d8b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39d8b-158">Windows Server 2003</span></span>



| <span data-ttu-id="39d8b-159">進入</span><span class="sxs-lookup"><span data-stu-id="39d8b-159">Entry</span></span> | <span data-ttu-id="39d8b-160">值</span><span class="sxs-lookup"><span data-stu-id="39d8b-160">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="39d8b-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="39d8b-161">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39d8b-162">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="39d8b-163">System-Only</span></span>            | <span data-ttu-id="39d8b-164">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-164">False</span></span>                                                      |
| <span data-ttu-id="39d8b-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="39d8b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="39d8b-166">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-166">False</span></span>                                                      |
| <span data-ttu-id="39d8b-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="39d8b-167">Is Indexed</span></span>             | <span data-ttu-id="39d8b-168">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-168">False</span></span>                                                      |
| <span data-ttu-id="39d8b-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="39d8b-169">In Global Catalog</span></span>      | <span data-ttu-id="39d8b-170">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-170">False</span></span>                                                      |
| <span data-ttu-id="39d8b-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="39d8b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="39d8b-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="39d8b-172">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="39d8b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39d8b-173">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39d8b-174">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-175">Search-Flags</span></span>           | <span data-ttu-id="39d8b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39d8b-176">0x00000000</span></span>                                                 |
| <span data-ttu-id="39d8b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-177">System-Flags</span></span>           | <span data-ttu-id="39d8b-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39d8b-178">0x00000010</span></span>                                                 |
| <span data-ttu-id="39d8b-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="39d8b-179">Classes used in</span></span>        | [<span data-ttu-id="39d8b-180">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="39d8b-180">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39d8b-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39d8b-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39d8b-182">進入</span><span class="sxs-lookup"><span data-stu-id="39d8b-182">Entry</span></span> | <span data-ttu-id="39d8b-183">值</span><span class="sxs-lookup"><span data-stu-id="39d8b-183">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="39d8b-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="39d8b-184">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39d8b-185">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="39d8b-186">System-Only</span></span>            | <span data-ttu-id="39d8b-187">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-187">False</span></span>                                                      |
| <span data-ttu-id="39d8b-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="39d8b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="39d8b-189">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-189">False</span></span>                                                      |
| <span data-ttu-id="39d8b-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="39d8b-190">Is Indexed</span></span>             | <span data-ttu-id="39d8b-191">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-191">False</span></span>                                                      |
| <span data-ttu-id="39d8b-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="39d8b-192">In Global Catalog</span></span>      | <span data-ttu-id="39d8b-193">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-193">False</span></span>                                                      |
| <span data-ttu-id="39d8b-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="39d8b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="39d8b-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="39d8b-195">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="39d8b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39d8b-196">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39d8b-197">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-198">Search-Flags</span></span>           | <span data-ttu-id="39d8b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39d8b-199">0x00000000</span></span>                                                 |
| <span data-ttu-id="39d8b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-200">System-Flags</span></span>           | <span data-ttu-id="39d8b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39d8b-201">0x00000010</span></span>                                                 |
| <span data-ttu-id="39d8b-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="39d8b-202">Classes used in</span></span>        | [<span data-ttu-id="39d8b-203">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="39d8b-203">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39d8b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39d8b-204">Windows Server 2008</span></span>



| <span data-ttu-id="39d8b-205">進入</span><span class="sxs-lookup"><span data-stu-id="39d8b-205">Entry</span></span> | <span data-ttu-id="39d8b-206">值</span><span class="sxs-lookup"><span data-stu-id="39d8b-206">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="39d8b-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="39d8b-207">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39d8b-208">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="39d8b-209">System-Only</span></span>            | <span data-ttu-id="39d8b-210">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-210">False</span></span>                                                      |
| <span data-ttu-id="39d8b-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="39d8b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="39d8b-212">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-212">False</span></span>                                                      |
| <span data-ttu-id="39d8b-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="39d8b-213">Is Indexed</span></span>             | <span data-ttu-id="39d8b-214">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-214">False</span></span>                                                      |
| <span data-ttu-id="39d8b-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="39d8b-215">In Global Catalog</span></span>      | <span data-ttu-id="39d8b-216">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-216">False</span></span>                                                      |
| <span data-ttu-id="39d8b-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="39d8b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="39d8b-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="39d8b-218">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="39d8b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39d8b-219">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39d8b-220">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-221">Search-Flags</span></span>           | <span data-ttu-id="39d8b-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39d8b-222">0x00000000</span></span>                                                 |
| <span data-ttu-id="39d8b-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-223">System-Flags</span></span>           | <span data-ttu-id="39d8b-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39d8b-224">0x00000010</span></span>                                                 |
| <span data-ttu-id="39d8b-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="39d8b-225">Classes used in</span></span>        | [<span data-ttu-id="39d8b-226">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="39d8b-226">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39d8b-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39d8b-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39d8b-228">進入</span><span class="sxs-lookup"><span data-stu-id="39d8b-228">Entry</span></span> | <span data-ttu-id="39d8b-229">值</span><span class="sxs-lookup"><span data-stu-id="39d8b-229">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="39d8b-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="39d8b-230">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39d8b-231">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="39d8b-232">System-Only</span></span>            | <span data-ttu-id="39d8b-233">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-233">False</span></span>                                                      |
| <span data-ttu-id="39d8b-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="39d8b-234">Is-Single-Valued</span></span>       | <span data-ttu-id="39d8b-235">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-235">False</span></span>                                                      |
| <span data-ttu-id="39d8b-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="39d8b-236">Is Indexed</span></span>             | <span data-ttu-id="39d8b-237">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-237">False</span></span>                                                      |
| <span data-ttu-id="39d8b-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="39d8b-238">In Global Catalog</span></span>      | <span data-ttu-id="39d8b-239">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-239">False</span></span>                                                      |
| <span data-ttu-id="39d8b-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="39d8b-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="39d8b-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="39d8b-241">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="39d8b-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39d8b-242">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39d8b-243">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-244">Search-Flags</span></span>           | <span data-ttu-id="39d8b-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39d8b-245">0x00000000</span></span>                                                 |
| <span data-ttu-id="39d8b-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-246">System-Flags</span></span>           | <span data-ttu-id="39d8b-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39d8b-247">0x00000010</span></span>                                                 |
| <span data-ttu-id="39d8b-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="39d8b-248">Classes used in</span></span>        | [<span data-ttu-id="39d8b-249">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="39d8b-249">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39d8b-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39d8b-250">Windows Server 2012</span></span>



| <span data-ttu-id="39d8b-251">進入</span><span class="sxs-lookup"><span data-stu-id="39d8b-251">Entry</span></span> | <span data-ttu-id="39d8b-252">值</span><span class="sxs-lookup"><span data-stu-id="39d8b-252">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="39d8b-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="39d8b-253">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39d8b-254">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="39d8b-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="39d8b-255">System-Only</span></span>            | <span data-ttu-id="39d8b-256">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-256">False</span></span>                                                      |
| <span data-ttu-id="39d8b-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="39d8b-257">Is-Single-Valued</span></span>       | <span data-ttu-id="39d8b-258">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-258">False</span></span>                                                      |
| <span data-ttu-id="39d8b-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="39d8b-259">Is Indexed</span></span>             | <span data-ttu-id="39d8b-260">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-260">False</span></span>                                                      |
| <span data-ttu-id="39d8b-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="39d8b-261">In Global Catalog</span></span>      | <span data-ttu-id="39d8b-262">否</span><span class="sxs-lookup"><span data-stu-id="39d8b-262">False</span></span>                                                      |
| <span data-ttu-id="39d8b-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="39d8b-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="39d8b-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="39d8b-264">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="39d8b-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39d8b-265">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39d8b-266">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="39d8b-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-267">Search-Flags</span></span>           | <span data-ttu-id="39d8b-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39d8b-268">0x00000000</span></span>                                                 |
| <span data-ttu-id="39d8b-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39d8b-269">System-Flags</span></span>           | <span data-ttu-id="39d8b-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39d8b-270">0x00000010</span></span>                                                 |
| <span data-ttu-id="39d8b-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="39d8b-271">Classes used in</span></span>        | [<span data-ttu-id="39d8b-272">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="39d8b-272">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 






---
title: 系統管理-多重複選-屬性頁屬性
description: 這是多值屬性，其值為代表加入頁面之順序的數位，以及為 AD 使用者和電腦嵌入式管理單元執行多重選取屬性頁的 COM 物件 GUID。
ms.assetid: b2b4aafe-ac2d-44b3-80eb-910ba9852bb0
ms.tgt_platform: multiple
keywords:
- 系統管理員-多重複選屬性-Pages 屬性 AD 架構
- adminMultiselectPropertyPages 屬性 AD 架構
topic_type:
- apiref
api_name:
- Admin-Multiselect-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e653568d4f8f6653e4c7dc939c91a7d3cd8b83c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972711"
---
# <a name="admin-multiselect-property-pages-attribute"></a><span data-ttu-id="cadf3-105">系統管理-多重複選-屬性頁屬性</span><span class="sxs-lookup"><span data-stu-id="cadf3-105">Admin-Multiselect-Property-Pages attribute</span></span>

<span data-ttu-id="cadf3-106">這是多值屬性，其值為代表加入頁面之順序的數位，以及為 AD 使用者和電腦嵌入式管理單元執行多重選取屬性頁的 COM 物件 GUID。</span><span class="sxs-lookup"><span data-stu-id="cadf3-106">This is a multivalued attribute whose values are a number that represents the order in which the pages are added and a GUID of a COM object that implements multi-select property pages for the AD Users and Computers snap-in.</span></span>



| <span data-ttu-id="cadf3-107">進入</span><span class="sxs-lookup"><span data-stu-id="cadf3-107">Entry</span></span> | <span data-ttu-id="cadf3-108">值</span><span class="sxs-lookup"><span data-stu-id="cadf3-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cadf3-109">CN</span><span class="sxs-lookup"><span data-stu-id="cadf3-109">CN</span></span>                | <span data-ttu-id="cadf3-110">系統管理-多重複選-屬性頁</span><span class="sxs-lookup"><span data-stu-id="cadf3-110">Admin-Multiselect-Property-Pages</span></span>                                                                                                            |
| <span data-ttu-id="cadf3-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="cadf3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cadf3-112">adminMultiselectPropertyPages</span><span class="sxs-lookup"><span data-stu-id="cadf3-112">adminMultiselectPropertyPages</span></span>                                                                                                               |
| <span data-ttu-id="cadf3-113">大小</span><span class="sxs-lookup"><span data-stu-id="cadf3-113">Size</span></span>              | <span data-ttu-id="cadf3-114">40位元組</span><span class="sxs-lookup"><span data-stu-id="cadf3-114">40 bytes</span></span>                                                                                                                                    |
| <span data-ttu-id="cadf3-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="cadf3-115">Update Privilege</span></span>  | <span data-ttu-id="cadf3-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="cadf3-116">Domain administrator</span></span>                                                                                                                        |
| <span data-ttu-id="cadf3-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="cadf3-117">Update Frequency</span></span>  | <span data-ttu-id="cadf3-118">只有在已安裝的服務（例如 Exchange 或終端機伺服器）上執行時，才會更新，以執行自己的多重選取屬性頁。</span><span class="sxs-lookup"><span data-stu-id="cadf3-118">This will only be updated if a service like Exchange or Terminal Server is installed that implements their own multi-select property pages.</span></span> |
| <span data-ttu-id="cadf3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cadf3-119">Attribute-Id</span></span>      | <span data-ttu-id="cadf3-120">1.2.840.113556.1.4.1690</span><span class="sxs-lookup"><span data-stu-id="cadf3-120">1.2.840.113556.1.4.1690</span></span>                                                                                                                     |
| <span data-ttu-id="cadf3-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="cadf3-121">System-Id-Guid</span></span>    | <span data-ttu-id="cadf3-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span><span class="sxs-lookup"><span data-stu-id="cadf3-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span></span>                                                                                                        |
| <span data-ttu-id="cadf3-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="cadf3-123">Syntax</span></span>            | [<span data-ttu-id="cadf3-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cadf3-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                 |



## <a name="implementations"></a><span data-ttu-id="cadf3-125">實作</span><span class="sxs-lookup"><span data-stu-id="cadf3-125">Implementations</span></span>

-   [<span data-ttu-id="cadf3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cadf3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cadf3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cadf3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cadf3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cadf3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cadf3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cadf3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cadf3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cadf3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cadf3-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cadf3-131">Windows Server 2003</span></span>



| <span data-ttu-id="cadf3-132">進入</span><span class="sxs-lookup"><span data-stu-id="cadf3-132">Entry</span></span> | <span data-ttu-id="cadf3-133">值</span><span class="sxs-lookup"><span data-stu-id="cadf3-133">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="cadf3-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cadf3-134">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cadf3-135">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cadf3-136">System-Only</span></span>            | <span data-ttu-id="cadf3-137">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-137">False</span></span>                                                      |
| <span data-ttu-id="cadf3-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cadf3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cadf3-139">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-139">False</span></span>                                                      |
| <span data-ttu-id="cadf3-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cadf3-140">Is Indexed</span></span>             | <span data-ttu-id="cadf3-141">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-141">False</span></span>                                                      |
| <span data-ttu-id="cadf3-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cadf3-142">In Global Catalog</span></span>      | <span data-ttu-id="cadf3-143">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-143">False</span></span>                                                      |
| <span data-ttu-id="cadf3-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cadf3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cadf3-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cadf3-145">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="cadf3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cadf3-146">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cadf3-147">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-148">Search-Flags</span></span>           | <span data-ttu-id="cadf3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cadf3-149">0x00000000</span></span>                                                 |
| <span data-ttu-id="cadf3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-150">System-Flags</span></span>           | <span data-ttu-id="cadf3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cadf3-151">0x00000010</span></span>                                                 |
| <span data-ttu-id="cadf3-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cadf3-152">Classes used in</span></span>        | [<span data-ttu-id="cadf3-153">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="cadf3-153">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cadf3-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cadf3-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cadf3-155">進入</span><span class="sxs-lookup"><span data-stu-id="cadf3-155">Entry</span></span> | <span data-ttu-id="cadf3-156">值</span><span class="sxs-lookup"><span data-stu-id="cadf3-156">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="cadf3-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cadf3-157">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cadf3-158">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cadf3-159">System-Only</span></span>            | <span data-ttu-id="cadf3-160">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-160">False</span></span>                                                      |
| <span data-ttu-id="cadf3-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cadf3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cadf3-162">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-162">False</span></span>                                                      |
| <span data-ttu-id="cadf3-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cadf3-163">Is Indexed</span></span>             | <span data-ttu-id="cadf3-164">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-164">False</span></span>                                                      |
| <span data-ttu-id="cadf3-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cadf3-165">In Global Catalog</span></span>      | <span data-ttu-id="cadf3-166">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-166">False</span></span>                                                      |
| <span data-ttu-id="cadf3-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cadf3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cadf3-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cadf3-168">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="cadf3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cadf3-169">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cadf3-170">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-171">Search-Flags</span></span>           | <span data-ttu-id="cadf3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cadf3-172">0x00000000</span></span>                                                 |
| <span data-ttu-id="cadf3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-173">System-Flags</span></span>           | <span data-ttu-id="cadf3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cadf3-174">0x00000010</span></span>                                                 |
| <span data-ttu-id="cadf3-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cadf3-175">Classes used in</span></span>        | [<span data-ttu-id="cadf3-176">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="cadf3-176">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cadf3-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cadf3-177">Windows Server 2008</span></span>



| <span data-ttu-id="cadf3-178">進入</span><span class="sxs-lookup"><span data-stu-id="cadf3-178">Entry</span></span> | <span data-ttu-id="cadf3-179">值</span><span class="sxs-lookup"><span data-stu-id="cadf3-179">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="cadf3-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cadf3-180">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cadf3-181">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="cadf3-182">System-Only</span></span>            | <span data-ttu-id="cadf3-183">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-183">False</span></span>                                                      |
| <span data-ttu-id="cadf3-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cadf3-184">Is-Single-Valued</span></span>       | <span data-ttu-id="cadf3-185">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-185">False</span></span>                                                      |
| <span data-ttu-id="cadf3-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cadf3-186">Is Indexed</span></span>             | <span data-ttu-id="cadf3-187">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-187">False</span></span>                                                      |
| <span data-ttu-id="cadf3-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cadf3-188">In Global Catalog</span></span>      | <span data-ttu-id="cadf3-189">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-189">False</span></span>                                                      |
| <span data-ttu-id="cadf3-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cadf3-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="cadf3-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cadf3-191">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="cadf3-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cadf3-192">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cadf3-193">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-194">Search-Flags</span></span>           | <span data-ttu-id="cadf3-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cadf3-195">0x00000000</span></span>                                                 |
| <span data-ttu-id="cadf3-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-196">System-Flags</span></span>           | <span data-ttu-id="cadf3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cadf3-197">0x00000010</span></span>                                                 |
| <span data-ttu-id="cadf3-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cadf3-198">Classes used in</span></span>        | [<span data-ttu-id="cadf3-199">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="cadf3-199">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cadf3-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cadf3-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cadf3-201">進入</span><span class="sxs-lookup"><span data-stu-id="cadf3-201">Entry</span></span> | <span data-ttu-id="cadf3-202">值</span><span class="sxs-lookup"><span data-stu-id="cadf3-202">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="cadf3-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cadf3-203">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cadf3-204">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="cadf3-205">System-Only</span></span>            | <span data-ttu-id="cadf3-206">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-206">False</span></span>                                                      |
| <span data-ttu-id="cadf3-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cadf3-207">Is-Single-Valued</span></span>       | <span data-ttu-id="cadf3-208">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-208">False</span></span>                                                      |
| <span data-ttu-id="cadf3-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cadf3-209">Is Indexed</span></span>             | <span data-ttu-id="cadf3-210">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-210">False</span></span>                                                      |
| <span data-ttu-id="cadf3-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cadf3-211">In Global Catalog</span></span>      | <span data-ttu-id="cadf3-212">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-212">False</span></span>                                                      |
| <span data-ttu-id="cadf3-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cadf3-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="cadf3-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cadf3-214">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="cadf3-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cadf3-215">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cadf3-216">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-217">Search-Flags</span></span>           | <span data-ttu-id="cadf3-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cadf3-218">0x00000000</span></span>                                                 |
| <span data-ttu-id="cadf3-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-219">System-Flags</span></span>           | <span data-ttu-id="cadf3-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cadf3-220">0x00000010</span></span>                                                 |
| <span data-ttu-id="cadf3-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cadf3-221">Classes used in</span></span>        | [<span data-ttu-id="cadf3-222">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="cadf3-222">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cadf3-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cadf3-223">Windows Server 2012</span></span>



| <span data-ttu-id="cadf3-224">進入</span><span class="sxs-lookup"><span data-stu-id="cadf3-224">Entry</span></span> | <span data-ttu-id="cadf3-225">值</span><span class="sxs-lookup"><span data-stu-id="cadf3-225">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="cadf3-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cadf3-226">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cadf3-227">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="cadf3-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="cadf3-228">System-Only</span></span>            | <span data-ttu-id="cadf3-229">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-229">False</span></span>                                                      |
| <span data-ttu-id="cadf3-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cadf3-230">Is-Single-Valued</span></span>       | <span data-ttu-id="cadf3-231">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-231">False</span></span>                                                      |
| <span data-ttu-id="cadf3-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cadf3-232">Is Indexed</span></span>             | <span data-ttu-id="cadf3-233">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-233">False</span></span>                                                      |
| <span data-ttu-id="cadf3-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cadf3-234">In Global Catalog</span></span>      | <span data-ttu-id="cadf3-235">否</span><span class="sxs-lookup"><span data-stu-id="cadf3-235">False</span></span>                                                      |
| <span data-ttu-id="cadf3-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cadf3-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="cadf3-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cadf3-237">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="cadf3-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cadf3-238">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cadf3-239">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="cadf3-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-240">Search-Flags</span></span>           | <span data-ttu-id="cadf3-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cadf3-241">0x00000000</span></span>                                                 |
| <span data-ttu-id="cadf3-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cadf3-242">System-Flags</span></span>           | <span data-ttu-id="cadf3-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cadf3-243">0x00000010</span></span>                                                 |
| <span data-ttu-id="cadf3-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cadf3-244">Classes used in</span></span>        | [<span data-ttu-id="cadf3-245">**顯示規範**</span><span class="sxs-lookup"><span data-stu-id="cadf3-245">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 






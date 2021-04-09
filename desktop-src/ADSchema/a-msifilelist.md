---
title: Msi 檔案清單屬性
description: 此屬性包含 Microsoft installer 檔案的清單，例如基礎 MSI 檔案 ( .msi) 和 MST 轉換檔案 ( .mst) 。
ms.assetid: 259a13a2-bb34-49aa-862e-4159e887310c
ms.tgt_platform: multiple
keywords:
- Msi-檔案清單屬性 AD 架構
- msiFileList 屬性 AD 架構
topic_type:
- apiref
api_name:
- Msi-File-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05608cdf443ab053549fde7db509ca79be08b3a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108112"
---
# <a name="msi-file-list-attribute"></a><span data-ttu-id="e25dd-105">Msi 檔案清單屬性</span><span class="sxs-lookup"><span data-stu-id="e25dd-105">Msi-File-List attribute</span></span>

<span data-ttu-id="e25dd-106">此屬性包含 Microsoft installer 檔案的清單，例如基礎 MSI 檔案 ( .msi) 和 MST 轉換檔案 ( .mst) 。</span><span class="sxs-lookup"><span data-stu-id="e25dd-106">This attribute contains a list of Microsoft installer files, such as the base MSI file (.msi) and MST transform files (.mst).</span></span>



| <span data-ttu-id="e25dd-107">進入</span><span class="sxs-lookup"><span data-stu-id="e25dd-107">Entry</span></span> | <span data-ttu-id="e25dd-108">值</span><span class="sxs-lookup"><span data-stu-id="e25dd-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e25dd-109">CN</span><span class="sxs-lookup"><span data-stu-id="e25dd-109">CN</span></span>                | <span data-ttu-id="e25dd-110">Msi-檔案清單</span><span class="sxs-lookup"><span data-stu-id="e25dd-110">Msi-File-List</span></span>                               |
| <span data-ttu-id="e25dd-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e25dd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e25dd-112">msiFileList</span><span class="sxs-lookup"><span data-stu-id="e25dd-112">msiFileList</span></span>                                 |
| <span data-ttu-id="e25dd-113">大小</span><span class="sxs-lookup"><span data-stu-id="e25dd-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e25dd-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e25dd-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e25dd-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e25dd-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e25dd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e25dd-116">Attribute-Id</span></span>      | <span data-ttu-id="e25dd-117">1.2.840.113556.1.4.671</span><span class="sxs-lookup"><span data-stu-id="e25dd-117">1.2.840.113556.1.4.671</span></span>                      |
| <span data-ttu-id="e25dd-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e25dd-118">System-Id-Guid</span></span>    | <span data-ttu-id="e25dd-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e25dd-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="e25dd-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="e25dd-120">Syntax</span></span>            | [<span data-ttu-id="e25dd-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e25dd-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e25dd-122">實作</span><span class="sxs-lookup"><span data-stu-id="e25dd-122">Implementations</span></span>

-   [<span data-ttu-id="e25dd-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e25dd-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e25dd-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e25dd-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e25dd-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e25dd-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e25dd-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e25dd-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e25dd-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e25dd-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e25dd-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e25dd-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e25dd-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e25dd-129">Windows 2000 Server</span></span>



| <span data-ttu-id="e25dd-130">進入</span><span class="sxs-lookup"><span data-stu-id="e25dd-130">Entry</span></span> | <span data-ttu-id="e25dd-131">值</span><span class="sxs-lookup"><span data-stu-id="e25dd-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e25dd-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e25dd-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e25dd-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e25dd-134">System-Only</span></span>            | <span data-ttu-id="e25dd-135">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-135">False</span></span>                                                            |
| <span data-ttu-id="e25dd-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e25dd-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e25dd-137">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-137">False</span></span>                                                            |
| <span data-ttu-id="e25dd-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e25dd-138">Is Indexed</span></span>             | <span data-ttu-id="e25dd-139">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-139">False</span></span>                                                            |
| <span data-ttu-id="e25dd-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e25dd-140">In Global Catalog</span></span>      | <span data-ttu-id="e25dd-141">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-141">False</span></span>                                                            |
| <span data-ttu-id="e25dd-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e25dd-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e25dd-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e25dd-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e25dd-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e25dd-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e25dd-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-146">Search-Flags</span></span>           | <span data-ttu-id="e25dd-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e25dd-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="e25dd-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-148">System-Flags</span></span>           | <span data-ttu-id="e25dd-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e25dd-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="e25dd-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e25dd-150">Classes used in</span></span>        | [<span data-ttu-id="e25dd-151">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="e25dd-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e25dd-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e25dd-152">Windows Server 2003</span></span>



| <span data-ttu-id="e25dd-153">進入</span><span class="sxs-lookup"><span data-stu-id="e25dd-153">Entry</span></span> | <span data-ttu-id="e25dd-154">值</span><span class="sxs-lookup"><span data-stu-id="e25dd-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e25dd-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e25dd-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e25dd-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="e25dd-157">System-Only</span></span>            | <span data-ttu-id="e25dd-158">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-158">False</span></span>                                                            |
| <span data-ttu-id="e25dd-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e25dd-159">Is-Single-Valued</span></span>       | <span data-ttu-id="e25dd-160">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-160">False</span></span>                                                            |
| <span data-ttu-id="e25dd-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e25dd-161">Is Indexed</span></span>             | <span data-ttu-id="e25dd-162">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-162">False</span></span>                                                            |
| <span data-ttu-id="e25dd-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e25dd-163">In Global Catalog</span></span>      | <span data-ttu-id="e25dd-164">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-164">False</span></span>                                                            |
| <span data-ttu-id="e25dd-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e25dd-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="e25dd-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e25dd-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e25dd-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e25dd-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e25dd-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-169">Search-Flags</span></span>           | <span data-ttu-id="e25dd-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e25dd-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="e25dd-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-171">System-Flags</span></span>           | <span data-ttu-id="e25dd-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e25dd-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="e25dd-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e25dd-173">Classes used in</span></span>        | [<span data-ttu-id="e25dd-174">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="e25dd-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e25dd-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e25dd-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e25dd-176">進入</span><span class="sxs-lookup"><span data-stu-id="e25dd-176">Entry</span></span> | <span data-ttu-id="e25dd-177">值</span><span class="sxs-lookup"><span data-stu-id="e25dd-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e25dd-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e25dd-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e25dd-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="e25dd-180">System-Only</span></span>            | <span data-ttu-id="e25dd-181">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-181">False</span></span>                                                            |
| <span data-ttu-id="e25dd-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e25dd-182">Is-Single-Valued</span></span>       | <span data-ttu-id="e25dd-183">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-183">False</span></span>                                                            |
| <span data-ttu-id="e25dd-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e25dd-184">Is Indexed</span></span>             | <span data-ttu-id="e25dd-185">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-185">False</span></span>                                                            |
| <span data-ttu-id="e25dd-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e25dd-186">In Global Catalog</span></span>      | <span data-ttu-id="e25dd-187">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-187">False</span></span>                                                            |
| <span data-ttu-id="e25dd-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e25dd-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="e25dd-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e25dd-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e25dd-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e25dd-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e25dd-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-192">Search-Flags</span></span>           | <span data-ttu-id="e25dd-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e25dd-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="e25dd-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-194">System-Flags</span></span>           | <span data-ttu-id="e25dd-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e25dd-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="e25dd-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e25dd-196">Classes used in</span></span>        | [<span data-ttu-id="e25dd-197">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="e25dd-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e25dd-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e25dd-198">Windows Server 2008</span></span>



| <span data-ttu-id="e25dd-199">進入</span><span class="sxs-lookup"><span data-stu-id="e25dd-199">Entry</span></span> | <span data-ttu-id="e25dd-200">值</span><span class="sxs-lookup"><span data-stu-id="e25dd-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e25dd-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e25dd-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e25dd-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="e25dd-203">System-Only</span></span>            | <span data-ttu-id="e25dd-204">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-204">False</span></span>                                                            |
| <span data-ttu-id="e25dd-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e25dd-205">Is-Single-Valued</span></span>       | <span data-ttu-id="e25dd-206">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-206">False</span></span>                                                            |
| <span data-ttu-id="e25dd-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e25dd-207">Is Indexed</span></span>             | <span data-ttu-id="e25dd-208">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-208">False</span></span>                                                            |
| <span data-ttu-id="e25dd-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e25dd-209">In Global Catalog</span></span>      | <span data-ttu-id="e25dd-210">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-210">False</span></span>                                                            |
| <span data-ttu-id="e25dd-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e25dd-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="e25dd-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e25dd-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e25dd-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e25dd-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e25dd-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-215">Search-Flags</span></span>           | <span data-ttu-id="e25dd-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e25dd-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="e25dd-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-217">System-Flags</span></span>           | <span data-ttu-id="e25dd-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e25dd-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="e25dd-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e25dd-219">Classes used in</span></span>        | [<span data-ttu-id="e25dd-220">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="e25dd-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e25dd-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e25dd-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e25dd-222">進入</span><span class="sxs-lookup"><span data-stu-id="e25dd-222">Entry</span></span> | <span data-ttu-id="e25dd-223">值</span><span class="sxs-lookup"><span data-stu-id="e25dd-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e25dd-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e25dd-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e25dd-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="e25dd-226">System-Only</span></span>            | <span data-ttu-id="e25dd-227">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-227">False</span></span>                                                            |
| <span data-ttu-id="e25dd-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e25dd-228">Is-Single-Valued</span></span>       | <span data-ttu-id="e25dd-229">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-229">False</span></span>                                                            |
| <span data-ttu-id="e25dd-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e25dd-230">Is Indexed</span></span>             | <span data-ttu-id="e25dd-231">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-231">False</span></span>                                                            |
| <span data-ttu-id="e25dd-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e25dd-232">In Global Catalog</span></span>      | <span data-ttu-id="e25dd-233">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-233">False</span></span>                                                            |
| <span data-ttu-id="e25dd-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e25dd-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="e25dd-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e25dd-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e25dd-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e25dd-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e25dd-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-238">Search-Flags</span></span>           | <span data-ttu-id="e25dd-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e25dd-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="e25dd-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-240">System-Flags</span></span>           | <span data-ttu-id="e25dd-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e25dd-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="e25dd-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e25dd-242">Classes used in</span></span>        | [<span data-ttu-id="e25dd-243">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="e25dd-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e25dd-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e25dd-244">Windows Server 2012</span></span>



| <span data-ttu-id="e25dd-245">進入</span><span class="sxs-lookup"><span data-stu-id="e25dd-245">Entry</span></span> | <span data-ttu-id="e25dd-246">值</span><span class="sxs-lookup"><span data-stu-id="e25dd-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e25dd-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e25dd-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e25dd-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e25dd-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="e25dd-249">System-Only</span></span>            | <span data-ttu-id="e25dd-250">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-250">False</span></span>                                                            |
| <span data-ttu-id="e25dd-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e25dd-251">Is-Single-Valued</span></span>       | <span data-ttu-id="e25dd-252">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-252">False</span></span>                                                            |
| <span data-ttu-id="e25dd-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e25dd-253">Is Indexed</span></span>             | <span data-ttu-id="e25dd-254">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-254">False</span></span>                                                            |
| <span data-ttu-id="e25dd-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e25dd-255">In Global Catalog</span></span>      | <span data-ttu-id="e25dd-256">否</span><span class="sxs-lookup"><span data-stu-id="e25dd-256">False</span></span>                                                            |
| <span data-ttu-id="e25dd-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e25dd-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="e25dd-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e25dd-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e25dd-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e25dd-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e25dd-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e25dd-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-261">Search-Flags</span></span>           | <span data-ttu-id="e25dd-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e25dd-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="e25dd-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e25dd-263">System-Flags</span></span>           | <span data-ttu-id="e25dd-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e25dd-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="e25dd-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e25dd-265">Classes used in</span></span>        | [<span data-ttu-id="e25dd-266">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="e25dd-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 






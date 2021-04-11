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
# <a name="msi-file-list-attribute"></a><span data-ttu-id="a6c3a-105">Msi 檔案清單屬性</span><span class="sxs-lookup"><span data-stu-id="a6c3a-105">Msi-File-List attribute</span></span>

<span data-ttu-id="a6c3a-106">此屬性包含 Microsoft installer 檔案的清單，例如基礎 MSI 檔案 ( .msi) 和 MST 轉換檔案 ( .mst) 。</span><span class="sxs-lookup"><span data-stu-id="a6c3a-106">This attribute contains a list of Microsoft installer files, such as the base MSI file (.msi) and MST transform files (.mst).</span></span>



| <span data-ttu-id="a6c3a-107">進入</span><span class="sxs-lookup"><span data-stu-id="a6c3a-107">Entry</span></span> | <span data-ttu-id="a6c3a-108">值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a6c3a-109">CN</span><span class="sxs-lookup"><span data-stu-id="a6c3a-109">CN</span></span>                | <span data-ttu-id="a6c3a-110">Msi-檔案清單</span><span class="sxs-lookup"><span data-stu-id="a6c3a-110">Msi-File-List</span></span>                               |
| <span data-ttu-id="a6c3a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a6c3a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a6c3a-112">msiFileList</span><span class="sxs-lookup"><span data-stu-id="a6c3a-112">msiFileList</span></span>                                 |
| <span data-ttu-id="a6c3a-113">大小</span><span class="sxs-lookup"><span data-stu-id="a6c3a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a6c3a-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a6c3a-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="a6c3a-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a6c3a-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a6c3a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a6c3a-116">Attribute-Id</span></span>      | <span data-ttu-id="a6c3a-117">1.2.840.113556.1.4.671</span><span class="sxs-lookup"><span data-stu-id="a6c3a-117">1.2.840.113556.1.4.671</span></span>                      |
| <span data-ttu-id="a6c3a-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a6c3a-118">System-Id-Guid</span></span>    | <span data-ttu-id="a6c3a-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a6c3a-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="a6c3a-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6c3a-120">Syntax</span></span>            | [<span data-ttu-id="a6c3a-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a6c3a-122">實作</span><span class="sxs-lookup"><span data-stu-id="a6c3a-122">Implementations</span></span>

-   [<span data-ttu-id="a6c3a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a6c3a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a6c3a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a6c3a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a6c3a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a6c3a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a6c3a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a6c3a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="a6c3a-130">進入</span><span class="sxs-lookup"><span data-stu-id="a6c3a-130">Entry</span></span> | <span data-ttu-id="a6c3a-131">值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a6c3a-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6c3a-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6c3a-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6c3a-134">System-Only</span></span>            | <span data-ttu-id="a6c3a-135">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-135">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a6c3a-137">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-137">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6c3a-138">Is Indexed</span></span>             | <span data-ttu-id="a6c3a-139">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-139">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6c3a-140">In Global Catalog</span></span>      | <span data-ttu-id="a6c3a-141">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-141">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6c3a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6c3a-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6c3a-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a6c3a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6c3a-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6c3a-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-146">Search-Flags</span></span>           | <span data-ttu-id="a6c3a-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6c3a-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="a6c3a-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-148">System-Flags</span></span>           | <span data-ttu-id="a6c3a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6c3a-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="a6c3a-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6c3a-150">Classes used in</span></span>        | [<span data-ttu-id="a6c3a-151">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a6c3a-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a6c3a-152">Windows Server 2003</span></span>



| <span data-ttu-id="a6c3a-153">進入</span><span class="sxs-lookup"><span data-stu-id="a6c3a-153">Entry</span></span> | <span data-ttu-id="a6c3a-154">值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a6c3a-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6c3a-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6c3a-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6c3a-157">System-Only</span></span>            | <span data-ttu-id="a6c3a-158">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-158">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-159">Is-Single-Valued</span></span>       | <span data-ttu-id="a6c3a-160">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-160">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6c3a-161">Is Indexed</span></span>             | <span data-ttu-id="a6c3a-162">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-162">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6c3a-163">In Global Catalog</span></span>      | <span data-ttu-id="a6c3a-164">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-164">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6c3a-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6c3a-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6c3a-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a6c3a-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6c3a-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6c3a-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-169">Search-Flags</span></span>           | <span data-ttu-id="a6c3a-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6c3a-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="a6c3a-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-171">System-Flags</span></span>           | <span data-ttu-id="a6c3a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6c3a-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="a6c3a-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6c3a-173">Classes used in</span></span>        | [<span data-ttu-id="a6c3a-174">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a6c3a-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a6c3a-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a6c3a-176">進入</span><span class="sxs-lookup"><span data-stu-id="a6c3a-176">Entry</span></span> | <span data-ttu-id="a6c3a-177">值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a6c3a-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6c3a-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6c3a-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6c3a-180">System-Only</span></span>            | <span data-ttu-id="a6c3a-181">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-181">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-182">Is-Single-Valued</span></span>       | <span data-ttu-id="a6c3a-183">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-183">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6c3a-184">Is Indexed</span></span>             | <span data-ttu-id="a6c3a-185">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-185">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6c3a-186">In Global Catalog</span></span>      | <span data-ttu-id="a6c3a-187">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-187">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6c3a-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6c3a-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6c3a-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a6c3a-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6c3a-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6c3a-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-192">Search-Flags</span></span>           | <span data-ttu-id="a6c3a-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6c3a-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="a6c3a-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-194">System-Flags</span></span>           | <span data-ttu-id="a6c3a-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6c3a-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="a6c3a-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6c3a-196">Classes used in</span></span>        | [<span data-ttu-id="a6c3a-197">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a6c3a-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6c3a-198">Windows Server 2008</span></span>



| <span data-ttu-id="a6c3a-199">進入</span><span class="sxs-lookup"><span data-stu-id="a6c3a-199">Entry</span></span> | <span data-ttu-id="a6c3a-200">值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a6c3a-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6c3a-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6c3a-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6c3a-203">System-Only</span></span>            | <span data-ttu-id="a6c3a-204">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-204">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-205">Is-Single-Valued</span></span>       | <span data-ttu-id="a6c3a-206">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-206">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6c3a-207">Is Indexed</span></span>             | <span data-ttu-id="a6c3a-208">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-208">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6c3a-209">In Global Catalog</span></span>      | <span data-ttu-id="a6c3a-210">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-210">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6c3a-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6c3a-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6c3a-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a6c3a-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6c3a-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6c3a-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-215">Search-Flags</span></span>           | <span data-ttu-id="a6c3a-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6c3a-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="a6c3a-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-217">System-Flags</span></span>           | <span data-ttu-id="a6c3a-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6c3a-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="a6c3a-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6c3a-219">Classes used in</span></span>        | [<span data-ttu-id="a6c3a-220">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a6c3a-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6c3a-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a6c3a-222">進入</span><span class="sxs-lookup"><span data-stu-id="a6c3a-222">Entry</span></span> | <span data-ttu-id="a6c3a-223">值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a6c3a-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6c3a-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6c3a-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6c3a-226">System-Only</span></span>            | <span data-ttu-id="a6c3a-227">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-227">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-228">Is-Single-Valued</span></span>       | <span data-ttu-id="a6c3a-229">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-229">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6c3a-230">Is Indexed</span></span>             | <span data-ttu-id="a6c3a-231">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-231">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6c3a-232">In Global Catalog</span></span>      | <span data-ttu-id="a6c3a-233">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-233">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6c3a-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6c3a-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6c3a-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a6c3a-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6c3a-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6c3a-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-238">Search-Flags</span></span>           | <span data-ttu-id="a6c3a-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6c3a-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="a6c3a-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-240">System-Flags</span></span>           | <span data-ttu-id="a6c3a-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6c3a-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="a6c3a-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6c3a-242">Classes used in</span></span>        | [<span data-ttu-id="a6c3a-243">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a6c3a-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a6c3a-244">Windows Server 2012</span></span>



| <span data-ttu-id="a6c3a-245">進入</span><span class="sxs-lookup"><span data-stu-id="a6c3a-245">Entry</span></span> | <span data-ttu-id="a6c3a-246">值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a6c3a-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6c3a-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6c3a-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="a6c3a-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6c3a-249">System-Only</span></span>            | <span data-ttu-id="a6c3a-250">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-250">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6c3a-251">Is-Single-Valued</span></span>       | <span data-ttu-id="a6c3a-252">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-252">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6c3a-253">Is Indexed</span></span>             | <span data-ttu-id="a6c3a-254">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-254">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6c3a-255">In Global Catalog</span></span>      | <span data-ttu-id="a6c3a-256">否</span><span class="sxs-lookup"><span data-stu-id="a6c3a-256">False</span></span>                                                            |
| <span data-ttu-id="a6c3a-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6c3a-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6c3a-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6c3a-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="a6c3a-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6c3a-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6c3a-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="a6c3a-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-261">Search-Flags</span></span>           | <span data-ttu-id="a6c3a-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6c3a-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="a6c3a-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6c3a-263">System-Flags</span></span>           | <span data-ttu-id="a6c3a-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6c3a-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="a6c3a-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6c3a-265">Classes used in</span></span>        | [<span data-ttu-id="a6c3a-266">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="a6c3a-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 






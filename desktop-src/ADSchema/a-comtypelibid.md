---
title: COM-Typelib-Id 屬性
description: 這個屬性會儲存此應用程式封裝中包含的類型程式庫識別碼清單。
ms.assetid: 3dcd2d1f-8b6d-46f6-9707-4af006f0e610
ms.tgt_platform: multiple
keywords:
- COM-Typelib-Id 屬性 AD 架構
- cOMTypelibId 屬性 AD 架構
topic_type:
- apiref
api_name:
- COM-Typelib-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0be116963137dcdba4d97aa3de751bdf7308c335
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106991578"
---
# <a name="com-typelib-id-attribute"></a><span data-ttu-id="944f2-105">COM-Typelib-Id 屬性</span><span class="sxs-lookup"><span data-stu-id="944f2-105">COM-Typelib-Id attribute</span></span>

<span data-ttu-id="944f2-106">這個屬性會儲存此應用程式封裝中包含的類型程式庫識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="944f2-106">This attribute stores the list of type library IDs contained in this application package.</span></span>



| <span data-ttu-id="944f2-107">進入</span><span class="sxs-lookup"><span data-stu-id="944f2-107">Entry</span></span> | <span data-ttu-id="944f2-108">值</span><span class="sxs-lookup"><span data-stu-id="944f2-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="944f2-109">CN</span><span class="sxs-lookup"><span data-stu-id="944f2-109">CN</span></span>                | <span data-ttu-id="944f2-110">COM-Typelib-Id</span><span class="sxs-lookup"><span data-stu-id="944f2-110">COM-Typelib-Id</span></span>                                                                   |
| <span data-ttu-id="944f2-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="944f2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="944f2-112">cOMTypelibId</span><span class="sxs-lookup"><span data-stu-id="944f2-112">cOMTypelibId</span></span>                                                                     |
| <span data-ttu-id="944f2-113">大小</span><span class="sxs-lookup"><span data-stu-id="944f2-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="944f2-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="944f2-114">Update Privilege</span></span>  | <span data-ttu-id="944f2-115">任何人都可以根據所建立物件的安全性來更新這個物件。</span><span class="sxs-lookup"><span data-stu-id="944f2-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="944f2-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="944f2-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="944f2-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="944f2-117">Attribute-Id</span></span>      | <span data-ttu-id="944f2-118">1.2.840.113556.1.4.254</span><span class="sxs-lookup"><span data-stu-id="944f2-118">1.2.840.113556.1.4.254</span></span>                                                           |
| <span data-ttu-id="944f2-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="944f2-119">System-Id-Guid</span></span>    | <span data-ttu-id="944f2-120">281416de-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="944f2-120">281416de-1968-11d0-a28f-00aa003049e2</span></span>                                             |
| <span data-ttu-id="944f2-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="944f2-121">Syntax</span></span>            | [<span data-ttu-id="944f2-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="944f2-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="944f2-123">實作</span><span class="sxs-lookup"><span data-stu-id="944f2-123">Implementations</span></span>

-   [<span data-ttu-id="944f2-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="944f2-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="944f2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="944f2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="944f2-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="944f2-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="944f2-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="944f2-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="944f2-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="944f2-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="944f2-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="944f2-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="944f2-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="944f2-130">Windows 2000 Server</span></span>



| <span data-ttu-id="944f2-131">進入</span><span class="sxs-lookup"><span data-stu-id="944f2-131">Entry</span></span> | <span data-ttu-id="944f2-132">值</span><span class="sxs-lookup"><span data-stu-id="944f2-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="944f2-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="944f2-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="944f2-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="944f2-135">System-Only</span></span>            | <span data-ttu-id="944f2-136">否</span><span class="sxs-lookup"><span data-stu-id="944f2-136">False</span></span>                                                            |
| <span data-ttu-id="944f2-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="944f2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="944f2-138">否</span><span class="sxs-lookup"><span data-stu-id="944f2-138">False</span></span>                                                            |
| <span data-ttu-id="944f2-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="944f2-139">Is Indexed</span></span>             | <span data-ttu-id="944f2-140">否</span><span class="sxs-lookup"><span data-stu-id="944f2-140">False</span></span>                                                            |
| <span data-ttu-id="944f2-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="944f2-141">In Global Catalog</span></span>      | <span data-ttu-id="944f2-142">否</span><span class="sxs-lookup"><span data-stu-id="944f2-142">False</span></span>                                                            |
| <span data-ttu-id="944f2-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="944f2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="944f2-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="944f2-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="944f2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="944f2-145">Range-Lower</span></span>            | <span data-ttu-id="944f2-146">36</span><span class="sxs-lookup"><span data-stu-id="944f2-146">36</span></span>                                                               |
| <span data-ttu-id="944f2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="944f2-147">Range-Upper</span></span>            | <span data-ttu-id="944f2-148">36</span><span class="sxs-lookup"><span data-stu-id="944f2-148">36</span></span>                                                               |
| <span data-ttu-id="944f2-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-149">Search-Flags</span></span>           | <span data-ttu-id="944f2-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="944f2-150">0x00000000</span></span>                                                       |
| <span data-ttu-id="944f2-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-151">System-Flags</span></span>           | <span data-ttu-id="944f2-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="944f2-152">0x00000010</span></span>                                                       |
| <span data-ttu-id="944f2-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="944f2-153">Classes used in</span></span>        | [<span data-ttu-id="944f2-154">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="944f2-154">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="944f2-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="944f2-155">Windows Server 2003</span></span>



| <span data-ttu-id="944f2-156">進入</span><span class="sxs-lookup"><span data-stu-id="944f2-156">Entry</span></span> | <span data-ttu-id="944f2-157">值</span><span class="sxs-lookup"><span data-stu-id="944f2-157">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="944f2-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="944f2-158">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="944f2-159">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="944f2-160">System-Only</span></span>            | <span data-ttu-id="944f2-161">否</span><span class="sxs-lookup"><span data-stu-id="944f2-161">False</span></span>                                                            |
| <span data-ttu-id="944f2-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="944f2-162">Is-Single-Valued</span></span>       | <span data-ttu-id="944f2-163">否</span><span class="sxs-lookup"><span data-stu-id="944f2-163">False</span></span>                                                            |
| <span data-ttu-id="944f2-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="944f2-164">Is Indexed</span></span>             | <span data-ttu-id="944f2-165">否</span><span class="sxs-lookup"><span data-stu-id="944f2-165">False</span></span>                                                            |
| <span data-ttu-id="944f2-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="944f2-166">In Global Catalog</span></span>      | <span data-ttu-id="944f2-167">否</span><span class="sxs-lookup"><span data-stu-id="944f2-167">False</span></span>                                                            |
| <span data-ttu-id="944f2-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="944f2-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="944f2-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="944f2-169">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="944f2-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="944f2-170">Range-Lower</span></span>            | <span data-ttu-id="944f2-171">36</span><span class="sxs-lookup"><span data-stu-id="944f2-171">36</span></span>                                                               |
| <span data-ttu-id="944f2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="944f2-172">Range-Upper</span></span>            | <span data-ttu-id="944f2-173">36</span><span class="sxs-lookup"><span data-stu-id="944f2-173">36</span></span>                                                               |
| <span data-ttu-id="944f2-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-174">Search-Flags</span></span>           | <span data-ttu-id="944f2-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="944f2-175">0x00000000</span></span>                                                       |
| <span data-ttu-id="944f2-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-176">System-Flags</span></span>           | <span data-ttu-id="944f2-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="944f2-177">0x00000010</span></span>                                                       |
| <span data-ttu-id="944f2-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="944f2-178">Classes used in</span></span>        | [<span data-ttu-id="944f2-179">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="944f2-179">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="944f2-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="944f2-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="944f2-181">進入</span><span class="sxs-lookup"><span data-stu-id="944f2-181">Entry</span></span> | <span data-ttu-id="944f2-182">值</span><span class="sxs-lookup"><span data-stu-id="944f2-182">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="944f2-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="944f2-183">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="944f2-184">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="944f2-185">System-Only</span></span>            | <span data-ttu-id="944f2-186">否</span><span class="sxs-lookup"><span data-stu-id="944f2-186">False</span></span>                                                            |
| <span data-ttu-id="944f2-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="944f2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="944f2-188">否</span><span class="sxs-lookup"><span data-stu-id="944f2-188">False</span></span>                                                            |
| <span data-ttu-id="944f2-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="944f2-189">Is Indexed</span></span>             | <span data-ttu-id="944f2-190">否</span><span class="sxs-lookup"><span data-stu-id="944f2-190">False</span></span>                                                            |
| <span data-ttu-id="944f2-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="944f2-191">In Global Catalog</span></span>      | <span data-ttu-id="944f2-192">否</span><span class="sxs-lookup"><span data-stu-id="944f2-192">False</span></span>                                                            |
| <span data-ttu-id="944f2-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="944f2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="944f2-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="944f2-194">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="944f2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="944f2-195">Range-Lower</span></span>            | <span data-ttu-id="944f2-196">36</span><span class="sxs-lookup"><span data-stu-id="944f2-196">36</span></span>                                                               |
| <span data-ttu-id="944f2-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="944f2-197">Range-Upper</span></span>            | <span data-ttu-id="944f2-198">36</span><span class="sxs-lookup"><span data-stu-id="944f2-198">36</span></span>                                                               |
| <span data-ttu-id="944f2-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-199">Search-Flags</span></span>           | <span data-ttu-id="944f2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="944f2-200">0x00000000</span></span>                                                       |
| <span data-ttu-id="944f2-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-201">System-Flags</span></span>           | <span data-ttu-id="944f2-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="944f2-202">0x00000010</span></span>                                                       |
| <span data-ttu-id="944f2-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="944f2-203">Classes used in</span></span>        | [<span data-ttu-id="944f2-204">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="944f2-204">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="944f2-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="944f2-205">Windows Server 2008</span></span>



| <span data-ttu-id="944f2-206">進入</span><span class="sxs-lookup"><span data-stu-id="944f2-206">Entry</span></span> | <span data-ttu-id="944f2-207">值</span><span class="sxs-lookup"><span data-stu-id="944f2-207">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="944f2-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="944f2-208">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="944f2-209">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="944f2-210">System-Only</span></span>            | <span data-ttu-id="944f2-211">否</span><span class="sxs-lookup"><span data-stu-id="944f2-211">False</span></span>                                                            |
| <span data-ttu-id="944f2-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="944f2-212">Is-Single-Valued</span></span>       | <span data-ttu-id="944f2-213">否</span><span class="sxs-lookup"><span data-stu-id="944f2-213">False</span></span>                                                            |
| <span data-ttu-id="944f2-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="944f2-214">Is Indexed</span></span>             | <span data-ttu-id="944f2-215">否</span><span class="sxs-lookup"><span data-stu-id="944f2-215">False</span></span>                                                            |
| <span data-ttu-id="944f2-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="944f2-216">In Global Catalog</span></span>      | <span data-ttu-id="944f2-217">否</span><span class="sxs-lookup"><span data-stu-id="944f2-217">False</span></span>                                                            |
| <span data-ttu-id="944f2-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="944f2-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="944f2-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="944f2-219">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="944f2-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="944f2-220">Range-Lower</span></span>            | <span data-ttu-id="944f2-221">36</span><span class="sxs-lookup"><span data-stu-id="944f2-221">36</span></span>                                                               |
| <span data-ttu-id="944f2-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="944f2-222">Range-Upper</span></span>            | <span data-ttu-id="944f2-223">36</span><span class="sxs-lookup"><span data-stu-id="944f2-223">36</span></span>                                                               |
| <span data-ttu-id="944f2-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-224">Search-Flags</span></span>           | <span data-ttu-id="944f2-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="944f2-225">0x00000000</span></span>                                                       |
| <span data-ttu-id="944f2-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-226">System-Flags</span></span>           | <span data-ttu-id="944f2-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="944f2-227">0x00000010</span></span>                                                       |
| <span data-ttu-id="944f2-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="944f2-228">Classes used in</span></span>        | [<span data-ttu-id="944f2-229">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="944f2-229">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="944f2-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="944f2-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="944f2-231">進入</span><span class="sxs-lookup"><span data-stu-id="944f2-231">Entry</span></span> | <span data-ttu-id="944f2-232">值</span><span class="sxs-lookup"><span data-stu-id="944f2-232">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="944f2-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="944f2-233">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="944f2-234">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="944f2-235">System-Only</span></span>            | <span data-ttu-id="944f2-236">否</span><span class="sxs-lookup"><span data-stu-id="944f2-236">False</span></span>                                                            |
| <span data-ttu-id="944f2-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="944f2-237">Is-Single-Valued</span></span>       | <span data-ttu-id="944f2-238">否</span><span class="sxs-lookup"><span data-stu-id="944f2-238">False</span></span>                                                            |
| <span data-ttu-id="944f2-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="944f2-239">Is Indexed</span></span>             | <span data-ttu-id="944f2-240">否</span><span class="sxs-lookup"><span data-stu-id="944f2-240">False</span></span>                                                            |
| <span data-ttu-id="944f2-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="944f2-241">In Global Catalog</span></span>      | <span data-ttu-id="944f2-242">否</span><span class="sxs-lookup"><span data-stu-id="944f2-242">False</span></span>                                                            |
| <span data-ttu-id="944f2-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="944f2-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="944f2-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="944f2-244">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="944f2-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="944f2-245">Range-Lower</span></span>            | <span data-ttu-id="944f2-246">36</span><span class="sxs-lookup"><span data-stu-id="944f2-246">36</span></span>                                                               |
| <span data-ttu-id="944f2-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="944f2-247">Range-Upper</span></span>            | <span data-ttu-id="944f2-248">36</span><span class="sxs-lookup"><span data-stu-id="944f2-248">36</span></span>                                                               |
| <span data-ttu-id="944f2-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-249">Search-Flags</span></span>           | <span data-ttu-id="944f2-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="944f2-250">0x00000000</span></span>                                                       |
| <span data-ttu-id="944f2-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-251">System-Flags</span></span>           | <span data-ttu-id="944f2-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="944f2-252">0x00000010</span></span>                                                       |
| <span data-ttu-id="944f2-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="944f2-253">Classes used in</span></span>        | [<span data-ttu-id="944f2-254">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="944f2-254">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="944f2-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="944f2-255">Windows Server 2012</span></span>



| <span data-ttu-id="944f2-256">進入</span><span class="sxs-lookup"><span data-stu-id="944f2-256">Entry</span></span> | <span data-ttu-id="944f2-257">值</span><span class="sxs-lookup"><span data-stu-id="944f2-257">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="944f2-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="944f2-258">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="944f2-259">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="944f2-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="944f2-260">System-Only</span></span>            | <span data-ttu-id="944f2-261">否</span><span class="sxs-lookup"><span data-stu-id="944f2-261">False</span></span>                                                            |
| <span data-ttu-id="944f2-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="944f2-262">Is-Single-Valued</span></span>       | <span data-ttu-id="944f2-263">否</span><span class="sxs-lookup"><span data-stu-id="944f2-263">False</span></span>                                                            |
| <span data-ttu-id="944f2-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="944f2-264">Is Indexed</span></span>             | <span data-ttu-id="944f2-265">否</span><span class="sxs-lookup"><span data-stu-id="944f2-265">False</span></span>                                                            |
| <span data-ttu-id="944f2-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="944f2-266">In Global Catalog</span></span>      | <span data-ttu-id="944f2-267">否</span><span class="sxs-lookup"><span data-stu-id="944f2-267">False</span></span>                                                            |
| <span data-ttu-id="944f2-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="944f2-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="944f2-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="944f2-269">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="944f2-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="944f2-270">Range-Lower</span></span>            | <span data-ttu-id="944f2-271">36</span><span class="sxs-lookup"><span data-stu-id="944f2-271">36</span></span>                                                               |
| <span data-ttu-id="944f2-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="944f2-272">Range-Upper</span></span>            | <span data-ttu-id="944f2-273">36</span><span class="sxs-lookup"><span data-stu-id="944f2-273">36</span></span>                                                               |
| <span data-ttu-id="944f2-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-274">Search-Flags</span></span>           | <span data-ttu-id="944f2-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="944f2-275">0x00000000</span></span>                                                       |
| <span data-ttu-id="944f2-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="944f2-276">System-Flags</span></span>           | <span data-ttu-id="944f2-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="944f2-277">0x00000010</span></span>                                                       |
| <span data-ttu-id="944f2-278">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="944f2-278">Classes used in</span></span>        | [<span data-ttu-id="944f2-279">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="944f2-279">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 






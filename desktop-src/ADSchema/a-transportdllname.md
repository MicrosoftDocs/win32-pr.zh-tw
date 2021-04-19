---
title: 傳輸-DLL-名稱屬性
description: 將管理傳輸的 DLL 名稱。
ms.assetid: a6b078ec-8738-4c57-9d94-05a96dbc645b
ms.tgt_platform: multiple
keywords:
- 傳輸-DLL-名稱屬性 AD 架構
- transportDLLName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Transport-DLL-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c118a2f7553c86de4b3c36b2904a3b7d75518a2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106984533"
---
# <a name="transport-dll-name-attribute"></a><span data-ttu-id="33e86-105">傳輸-DLL-名稱屬性</span><span class="sxs-lookup"><span data-stu-id="33e86-105">Transport-DLL-Name attribute</span></span>

<span data-ttu-id="33e86-106">將管理傳輸的 DLL 名稱。</span><span class="sxs-lookup"><span data-stu-id="33e86-106">The name of the DLL that will manage a transport.</span></span>



| <span data-ttu-id="33e86-107">進入</span><span class="sxs-lookup"><span data-stu-id="33e86-107">Entry</span></span> | <span data-ttu-id="33e86-108">值</span><span class="sxs-lookup"><span data-stu-id="33e86-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="33e86-109">CN</span><span class="sxs-lookup"><span data-stu-id="33e86-109">CN</span></span>                | <span data-ttu-id="33e86-110">傳輸-DLL-名稱</span><span class="sxs-lookup"><span data-stu-id="33e86-110">Transport-DLL-Name</span></span>                          |
| <span data-ttu-id="33e86-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="33e86-111">Ldap-Display-Name</span></span> | <span data-ttu-id="33e86-112">transportDLLName</span><span class="sxs-lookup"><span data-stu-id="33e86-112">transportDLLName</span></span>                            |
| <span data-ttu-id="33e86-113">大小</span><span class="sxs-lookup"><span data-stu-id="33e86-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="33e86-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="33e86-114">Update Privilege</span></span>  | <span data-ttu-id="33e86-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="33e86-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="33e86-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="33e86-116">Update Frequency</span></span>  | <span data-ttu-id="33e86-117">連接網站時。</span><span class="sxs-lookup"><span data-stu-id="33e86-117">When connecting sites.</span></span>                      |
| <span data-ttu-id="33e86-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="33e86-118">Attribute-Id</span></span>      | <span data-ttu-id="33e86-119">1.2.840.113556.1.4.789</span><span class="sxs-lookup"><span data-stu-id="33e86-119">1.2.840.113556.1.4.789</span></span>                      |
| <span data-ttu-id="33e86-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="33e86-120">System-Id-Guid</span></span>    | <span data-ttu-id="33e86-121">26d97372-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="33e86-121">26d97372-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="33e86-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="33e86-122">Syntax</span></span>            | [<span data-ttu-id="33e86-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="33e86-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="33e86-124">實作</span><span class="sxs-lookup"><span data-stu-id="33e86-124">Implementations</span></span>

-   [<span data-ttu-id="33e86-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="33e86-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="33e86-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="33e86-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="33e86-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="33e86-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="33e86-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="33e86-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="33e86-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="33e86-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="33e86-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="33e86-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="33e86-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="33e86-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="33e86-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="33e86-132">Windows 2000 Server</span></span>



| <span data-ttu-id="33e86-133">進入</span><span class="sxs-lookup"><span data-stu-id="33e86-133">Entry</span></span> | <span data-ttu-id="33e86-134">值</span><span class="sxs-lookup"><span data-stu-id="33e86-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="33e86-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33e86-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33e86-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="33e86-137">System-Only</span></span>            | <span data-ttu-id="33e86-138">否</span><span class="sxs-lookup"><span data-stu-id="33e86-138">False</span></span>                                                           |
| <span data-ttu-id="33e86-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33e86-139">Is-Single-Valued</span></span>       | <span data-ttu-id="33e86-140">對</span><span class="sxs-lookup"><span data-stu-id="33e86-140">True</span></span>                                                            |
| <span data-ttu-id="33e86-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33e86-141">Is Indexed</span></span>             | <span data-ttu-id="33e86-142">否</span><span class="sxs-lookup"><span data-stu-id="33e86-142">False</span></span>                                                           |
| <span data-ttu-id="33e86-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33e86-143">In Global Catalog</span></span>      | <span data-ttu-id="33e86-144">否</span><span class="sxs-lookup"><span data-stu-id="33e86-144">False</span></span>                                                           |
| <span data-ttu-id="33e86-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33e86-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="33e86-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33e86-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="33e86-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33e86-147">Range-Lower</span></span>            | <span data-ttu-id="33e86-148">0</span><span class="sxs-lookup"><span data-stu-id="33e86-148">0</span></span>                                                               |
| <span data-ttu-id="33e86-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33e86-149">Range-Upper</span></span>            | <span data-ttu-id="33e86-150">1024</span><span class="sxs-lookup"><span data-stu-id="33e86-150">1024</span></span>                                                            |
| <span data-ttu-id="33e86-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-151">Search-Flags</span></span>           | <span data-ttu-id="33e86-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33e86-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="33e86-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-153">System-Flags</span></span>           | <span data-ttu-id="33e86-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33e86-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="33e86-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33e86-155">Classes used in</span></span>        | [<span data-ttu-id="33e86-156">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="33e86-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="33e86-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="33e86-157">Windows Server 2003</span></span>



| <span data-ttu-id="33e86-158">進入</span><span class="sxs-lookup"><span data-stu-id="33e86-158">Entry</span></span> | <span data-ttu-id="33e86-159">值</span><span class="sxs-lookup"><span data-stu-id="33e86-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="33e86-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33e86-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33e86-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="33e86-162">System-Only</span></span>            | <span data-ttu-id="33e86-163">否</span><span class="sxs-lookup"><span data-stu-id="33e86-163">False</span></span>                                                           |
| <span data-ttu-id="33e86-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33e86-164">Is-Single-Valued</span></span>       | <span data-ttu-id="33e86-165">對</span><span class="sxs-lookup"><span data-stu-id="33e86-165">True</span></span>                                                            |
| <span data-ttu-id="33e86-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33e86-166">Is Indexed</span></span>             | <span data-ttu-id="33e86-167">否</span><span class="sxs-lookup"><span data-stu-id="33e86-167">False</span></span>                                                           |
| <span data-ttu-id="33e86-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33e86-168">In Global Catalog</span></span>      | <span data-ttu-id="33e86-169">否</span><span class="sxs-lookup"><span data-stu-id="33e86-169">False</span></span>                                                           |
| <span data-ttu-id="33e86-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33e86-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="33e86-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33e86-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="33e86-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33e86-172">Range-Lower</span></span>            | <span data-ttu-id="33e86-173">0</span><span class="sxs-lookup"><span data-stu-id="33e86-173">0</span></span>                                                               |
| <span data-ttu-id="33e86-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33e86-174">Range-Upper</span></span>            | <span data-ttu-id="33e86-175">1024</span><span class="sxs-lookup"><span data-stu-id="33e86-175">1024</span></span>                                                            |
| <span data-ttu-id="33e86-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-176">Search-Flags</span></span>           | <span data-ttu-id="33e86-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33e86-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="33e86-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-178">System-Flags</span></span>           | <span data-ttu-id="33e86-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33e86-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="33e86-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33e86-180">Classes used in</span></span>        | [<span data-ttu-id="33e86-181">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="33e86-181">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="adam"></a><span data-ttu-id="33e86-182">亞當</span><span class="sxs-lookup"><span data-stu-id="33e86-182">ADAM</span></span>



| <span data-ttu-id="33e86-183">進入</span><span class="sxs-lookup"><span data-stu-id="33e86-183">Entry</span></span> | <span data-ttu-id="33e86-184">值</span><span class="sxs-lookup"><span data-stu-id="33e86-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="33e86-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33e86-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33e86-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="33e86-187">System-Only</span></span>            | <span data-ttu-id="33e86-188">否</span><span class="sxs-lookup"><span data-stu-id="33e86-188">False</span></span>                                                           |
| <span data-ttu-id="33e86-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33e86-189">Is-Single-Valued</span></span>       | <span data-ttu-id="33e86-190">對</span><span class="sxs-lookup"><span data-stu-id="33e86-190">True</span></span>                                                            |
| <span data-ttu-id="33e86-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33e86-191">Is Indexed</span></span>             | <span data-ttu-id="33e86-192">否</span><span class="sxs-lookup"><span data-stu-id="33e86-192">False</span></span>                                                           |
| <span data-ttu-id="33e86-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33e86-193">In Global Catalog</span></span>      | <span data-ttu-id="33e86-194">否</span><span class="sxs-lookup"><span data-stu-id="33e86-194">False</span></span>                                                           |
| <span data-ttu-id="33e86-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33e86-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="33e86-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33e86-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="33e86-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33e86-197">Range-Lower</span></span>            | <span data-ttu-id="33e86-198">0</span><span class="sxs-lookup"><span data-stu-id="33e86-198">0</span></span>                                                               |
| <span data-ttu-id="33e86-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33e86-199">Range-Upper</span></span>            | <span data-ttu-id="33e86-200">1024</span><span class="sxs-lookup"><span data-stu-id="33e86-200">1024</span></span>                                                            |
| <span data-ttu-id="33e86-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-201">Search-Flags</span></span>           | <span data-ttu-id="33e86-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33e86-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="33e86-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-203">System-Flags</span></span>           | <span data-ttu-id="33e86-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33e86-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="33e86-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33e86-205">Classes used in</span></span>        | [<span data-ttu-id="33e86-206">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="33e86-206">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="33e86-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="33e86-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="33e86-208">進入</span><span class="sxs-lookup"><span data-stu-id="33e86-208">Entry</span></span> | <span data-ttu-id="33e86-209">值</span><span class="sxs-lookup"><span data-stu-id="33e86-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="33e86-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33e86-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33e86-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="33e86-212">System-Only</span></span>            | <span data-ttu-id="33e86-213">否</span><span class="sxs-lookup"><span data-stu-id="33e86-213">False</span></span>                                                           |
| <span data-ttu-id="33e86-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33e86-214">Is-Single-Valued</span></span>       | <span data-ttu-id="33e86-215">對</span><span class="sxs-lookup"><span data-stu-id="33e86-215">True</span></span>                                                            |
| <span data-ttu-id="33e86-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33e86-216">Is Indexed</span></span>             | <span data-ttu-id="33e86-217">否</span><span class="sxs-lookup"><span data-stu-id="33e86-217">False</span></span>                                                           |
| <span data-ttu-id="33e86-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33e86-218">In Global Catalog</span></span>      | <span data-ttu-id="33e86-219">否</span><span class="sxs-lookup"><span data-stu-id="33e86-219">False</span></span>                                                           |
| <span data-ttu-id="33e86-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33e86-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="33e86-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33e86-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="33e86-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33e86-222">Range-Lower</span></span>            | <span data-ttu-id="33e86-223">0</span><span class="sxs-lookup"><span data-stu-id="33e86-223">0</span></span>                                                               |
| <span data-ttu-id="33e86-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33e86-224">Range-Upper</span></span>            | <span data-ttu-id="33e86-225">1024</span><span class="sxs-lookup"><span data-stu-id="33e86-225">1024</span></span>                                                            |
| <span data-ttu-id="33e86-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-226">Search-Flags</span></span>           | <span data-ttu-id="33e86-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33e86-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="33e86-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-228">System-Flags</span></span>           | <span data-ttu-id="33e86-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33e86-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="33e86-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33e86-230">Classes used in</span></span>        | [<span data-ttu-id="33e86-231">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="33e86-231">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="33e86-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33e86-232">Windows Server 2008</span></span>



| <span data-ttu-id="33e86-233">進入</span><span class="sxs-lookup"><span data-stu-id="33e86-233">Entry</span></span> | <span data-ttu-id="33e86-234">值</span><span class="sxs-lookup"><span data-stu-id="33e86-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="33e86-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33e86-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33e86-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="33e86-237">System-Only</span></span>            | <span data-ttu-id="33e86-238">否</span><span class="sxs-lookup"><span data-stu-id="33e86-238">False</span></span>                                                           |
| <span data-ttu-id="33e86-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33e86-239">Is-Single-Valued</span></span>       | <span data-ttu-id="33e86-240">對</span><span class="sxs-lookup"><span data-stu-id="33e86-240">True</span></span>                                                            |
| <span data-ttu-id="33e86-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33e86-241">Is Indexed</span></span>             | <span data-ttu-id="33e86-242">否</span><span class="sxs-lookup"><span data-stu-id="33e86-242">False</span></span>                                                           |
| <span data-ttu-id="33e86-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33e86-243">In Global Catalog</span></span>      | <span data-ttu-id="33e86-244">否</span><span class="sxs-lookup"><span data-stu-id="33e86-244">False</span></span>                                                           |
| <span data-ttu-id="33e86-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33e86-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="33e86-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33e86-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="33e86-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33e86-247">Range-Lower</span></span>            | <span data-ttu-id="33e86-248">0</span><span class="sxs-lookup"><span data-stu-id="33e86-248">0</span></span>                                                               |
| <span data-ttu-id="33e86-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33e86-249">Range-Upper</span></span>            | <span data-ttu-id="33e86-250">1024</span><span class="sxs-lookup"><span data-stu-id="33e86-250">1024</span></span>                                                            |
| <span data-ttu-id="33e86-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-251">Search-Flags</span></span>           | <span data-ttu-id="33e86-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33e86-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="33e86-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-253">System-Flags</span></span>           | <span data-ttu-id="33e86-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33e86-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="33e86-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33e86-255">Classes used in</span></span>        | [<span data-ttu-id="33e86-256">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="33e86-256">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="33e86-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33e86-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="33e86-258">進入</span><span class="sxs-lookup"><span data-stu-id="33e86-258">Entry</span></span> | <span data-ttu-id="33e86-259">值</span><span class="sxs-lookup"><span data-stu-id="33e86-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="33e86-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33e86-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33e86-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="33e86-262">System-Only</span></span>            | <span data-ttu-id="33e86-263">否</span><span class="sxs-lookup"><span data-stu-id="33e86-263">False</span></span>                                                           |
| <span data-ttu-id="33e86-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33e86-264">Is-Single-Valued</span></span>       | <span data-ttu-id="33e86-265">對</span><span class="sxs-lookup"><span data-stu-id="33e86-265">True</span></span>                                                            |
| <span data-ttu-id="33e86-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33e86-266">Is Indexed</span></span>             | <span data-ttu-id="33e86-267">否</span><span class="sxs-lookup"><span data-stu-id="33e86-267">False</span></span>                                                           |
| <span data-ttu-id="33e86-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33e86-268">In Global Catalog</span></span>      | <span data-ttu-id="33e86-269">否</span><span class="sxs-lookup"><span data-stu-id="33e86-269">False</span></span>                                                           |
| <span data-ttu-id="33e86-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33e86-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="33e86-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33e86-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="33e86-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33e86-272">Range-Lower</span></span>            | <span data-ttu-id="33e86-273">0</span><span class="sxs-lookup"><span data-stu-id="33e86-273">0</span></span>                                                               |
| <span data-ttu-id="33e86-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33e86-274">Range-Upper</span></span>            | <span data-ttu-id="33e86-275">1024</span><span class="sxs-lookup"><span data-stu-id="33e86-275">1024</span></span>                                                            |
| <span data-ttu-id="33e86-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-276">Search-Flags</span></span>           | <span data-ttu-id="33e86-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33e86-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="33e86-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-278">System-Flags</span></span>           | <span data-ttu-id="33e86-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33e86-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="33e86-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33e86-280">Classes used in</span></span>        | [<span data-ttu-id="33e86-281">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="33e86-281">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="33e86-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33e86-282">Windows Server 2012</span></span>



| <span data-ttu-id="33e86-283">進入</span><span class="sxs-lookup"><span data-stu-id="33e86-283">Entry</span></span> | <span data-ttu-id="33e86-284">值</span><span class="sxs-lookup"><span data-stu-id="33e86-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="33e86-285">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33e86-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33e86-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="33e86-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="33e86-287">System-Only</span></span>            | <span data-ttu-id="33e86-288">否</span><span class="sxs-lookup"><span data-stu-id="33e86-288">False</span></span>                                                           |
| <span data-ttu-id="33e86-289">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33e86-289">Is-Single-Valued</span></span>       | <span data-ttu-id="33e86-290">對</span><span class="sxs-lookup"><span data-stu-id="33e86-290">True</span></span>                                                            |
| <span data-ttu-id="33e86-291">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33e86-291">Is Indexed</span></span>             | <span data-ttu-id="33e86-292">否</span><span class="sxs-lookup"><span data-stu-id="33e86-292">False</span></span>                                                           |
| <span data-ttu-id="33e86-293">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33e86-293">In Global Catalog</span></span>      | <span data-ttu-id="33e86-294">否</span><span class="sxs-lookup"><span data-stu-id="33e86-294">False</span></span>                                                           |
| <span data-ttu-id="33e86-295">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33e86-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="33e86-296">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33e86-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="33e86-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33e86-297">Range-Lower</span></span>            | <span data-ttu-id="33e86-298">0</span><span class="sxs-lookup"><span data-stu-id="33e86-298">0</span></span>                                                               |
| <span data-ttu-id="33e86-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33e86-299">Range-Upper</span></span>            | <span data-ttu-id="33e86-300">1024</span><span class="sxs-lookup"><span data-stu-id="33e86-300">1024</span></span>                                                            |
| <span data-ttu-id="33e86-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-301">Search-Flags</span></span>           | <span data-ttu-id="33e86-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33e86-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="33e86-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33e86-303">System-Flags</span></span>           | <span data-ttu-id="33e86-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33e86-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="33e86-305">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33e86-305">Classes used in</span></span>        | [<span data-ttu-id="33e86-306">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="33e86-306">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



 

 






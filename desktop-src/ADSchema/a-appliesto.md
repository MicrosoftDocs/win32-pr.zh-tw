---
title: Applies-To 屬性
description: 包含擴充許可權適用的物件類別清單。 在清單中，物件類別是由其 schemaClass 物件的 schemaIDGUID 屬性所代表。
ms.assetid: 8333e508-627c-42ce-865b-db061a5603db
ms.tgt_platform: multiple
keywords:
- Applies-To 屬性 AD 架構
- appliesTo 屬性 AD 架構
topic_type:
- apiref
api_name:
- Applies-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b96a2690f420259b038b54b6d2b070b41f56d4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108300"
---
# <a name="applies-to-attribute"></a><span data-ttu-id="5218f-106">Applies-To 屬性</span><span class="sxs-lookup"><span data-stu-id="5218f-106">Applies-To attribute</span></span>

<span data-ttu-id="5218f-107">包含擴充許可權適用的物件類別清單。</span><span class="sxs-lookup"><span data-stu-id="5218f-107">Contains the list of object classes that the extended right applies to.</span></span> <span data-ttu-id="5218f-108">在清單中，物件類別是由其 schemaClass 物件的 schemaIDGUID 屬性所代表。</span><span class="sxs-lookup"><span data-stu-id="5218f-108">In the list, an object class is represented by the schemaIDGUID property for its schemaClass object.</span></span>



| <span data-ttu-id="5218f-109">進入</span><span class="sxs-lookup"><span data-stu-id="5218f-109">Entry</span></span> | <span data-ttu-id="5218f-110">值</span><span class="sxs-lookup"><span data-stu-id="5218f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5218f-111">CN</span><span class="sxs-lookup"><span data-stu-id="5218f-111">CN</span></span>                | <span data-ttu-id="5218f-112">Applies-To</span><span class="sxs-lookup"><span data-stu-id="5218f-112">Applies-To</span></span>                                  |
| <span data-ttu-id="5218f-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5218f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5218f-114">appliesTo</span><span class="sxs-lookup"><span data-stu-id="5218f-114">appliesTo</span></span>                                   |
| <span data-ttu-id="5218f-115">大小</span><span class="sxs-lookup"><span data-stu-id="5218f-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="5218f-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5218f-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5218f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5218f-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5218f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5218f-118">Attribute-Id</span></span>      | <span data-ttu-id="5218f-119">1.2.840.113556.1.4.341</span><span class="sxs-lookup"><span data-stu-id="5218f-119">1.2.840.113556.1.4.341</span></span>                      |
| <span data-ttu-id="5218f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5218f-120">System-Id-Guid</span></span>    | <span data-ttu-id="5218f-121">8297931d-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="5218f-121">8297931d-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="5218f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5218f-122">Syntax</span></span>            | [<span data-ttu-id="5218f-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5218f-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5218f-124">實作</span><span class="sxs-lookup"><span data-stu-id="5218f-124">Implementations</span></span>

-   [<span data-ttu-id="5218f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5218f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5218f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5218f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5218f-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="5218f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5218f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5218f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5218f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5218f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5218f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5218f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5218f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5218f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5218f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5218f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="5218f-133">進入</span><span class="sxs-lookup"><span data-stu-id="5218f-133">Entry</span></span> | <span data-ttu-id="5218f-134">值</span><span class="sxs-lookup"><span data-stu-id="5218f-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5218f-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5218f-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5218f-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5218f-137">System-Only</span></span>            | <span data-ttu-id="5218f-138">否</span><span class="sxs-lookup"><span data-stu-id="5218f-138">False</span></span>                                                           |
| <span data-ttu-id="5218f-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5218f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5218f-140">否</span><span class="sxs-lookup"><span data-stu-id="5218f-140">False</span></span>                                                           |
| <span data-ttu-id="5218f-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5218f-141">Is Indexed</span></span>             | <span data-ttu-id="5218f-142">否</span><span class="sxs-lookup"><span data-stu-id="5218f-142">False</span></span>                                                           |
| <span data-ttu-id="5218f-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5218f-143">In Global Catalog</span></span>      | <span data-ttu-id="5218f-144">否</span><span class="sxs-lookup"><span data-stu-id="5218f-144">False</span></span>                                                           |
| <span data-ttu-id="5218f-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5218f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5218f-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5218f-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5218f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5218f-147">Range-Lower</span></span>            | <span data-ttu-id="5218f-148">36</span><span class="sxs-lookup"><span data-stu-id="5218f-148">36</span></span>                                                              |
| <span data-ttu-id="5218f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5218f-149">Range-Upper</span></span>            | <span data-ttu-id="5218f-150">36</span><span class="sxs-lookup"><span data-stu-id="5218f-150">36</span></span>                                                              |
| <span data-ttu-id="5218f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-151">Search-Flags</span></span>           | <span data-ttu-id="5218f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5218f-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="5218f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-153">System-Flags</span></span>           | <span data-ttu-id="5218f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5218f-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="5218f-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5218f-155">Classes used in</span></span>        | [<span data-ttu-id="5218f-156">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="5218f-156">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5218f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5218f-157">Windows Server 2003</span></span>



| <span data-ttu-id="5218f-158">進入</span><span class="sxs-lookup"><span data-stu-id="5218f-158">Entry</span></span> | <span data-ttu-id="5218f-159">值</span><span class="sxs-lookup"><span data-stu-id="5218f-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5218f-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5218f-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5218f-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="5218f-162">System-Only</span></span>            | <span data-ttu-id="5218f-163">否</span><span class="sxs-lookup"><span data-stu-id="5218f-163">False</span></span>                                                           |
| <span data-ttu-id="5218f-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5218f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="5218f-165">否</span><span class="sxs-lookup"><span data-stu-id="5218f-165">False</span></span>                                                           |
| <span data-ttu-id="5218f-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5218f-166">Is Indexed</span></span>             | <span data-ttu-id="5218f-167">否</span><span class="sxs-lookup"><span data-stu-id="5218f-167">False</span></span>                                                           |
| <span data-ttu-id="5218f-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5218f-168">In Global Catalog</span></span>      | <span data-ttu-id="5218f-169">否</span><span class="sxs-lookup"><span data-stu-id="5218f-169">False</span></span>                                                           |
| <span data-ttu-id="5218f-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5218f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="5218f-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5218f-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5218f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5218f-172">Range-Lower</span></span>            | <span data-ttu-id="5218f-173">36</span><span class="sxs-lookup"><span data-stu-id="5218f-173">36</span></span>                                                              |
| <span data-ttu-id="5218f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5218f-174">Range-Upper</span></span>            | <span data-ttu-id="5218f-175">36</span><span class="sxs-lookup"><span data-stu-id="5218f-175">36</span></span>                                                              |
| <span data-ttu-id="5218f-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-176">Search-Flags</span></span>           | <span data-ttu-id="5218f-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5218f-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="5218f-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-178">System-Flags</span></span>           | <span data-ttu-id="5218f-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5218f-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="5218f-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5218f-180">Classes used in</span></span>        | [<span data-ttu-id="5218f-181">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="5218f-181">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5218f-182">亞當</span><span class="sxs-lookup"><span data-stu-id="5218f-182">ADAM</span></span>



| <span data-ttu-id="5218f-183">進入</span><span class="sxs-lookup"><span data-stu-id="5218f-183">Entry</span></span> | <span data-ttu-id="5218f-184">值</span><span class="sxs-lookup"><span data-stu-id="5218f-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5218f-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5218f-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5218f-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="5218f-187">System-Only</span></span>            | <span data-ttu-id="5218f-188">否</span><span class="sxs-lookup"><span data-stu-id="5218f-188">False</span></span>                                                           |
| <span data-ttu-id="5218f-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5218f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="5218f-190">否</span><span class="sxs-lookup"><span data-stu-id="5218f-190">False</span></span>                                                           |
| <span data-ttu-id="5218f-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5218f-191">Is Indexed</span></span>             | <span data-ttu-id="5218f-192">否</span><span class="sxs-lookup"><span data-stu-id="5218f-192">False</span></span>                                                           |
| <span data-ttu-id="5218f-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5218f-193">In Global Catalog</span></span>      | <span data-ttu-id="5218f-194">否</span><span class="sxs-lookup"><span data-stu-id="5218f-194">False</span></span>                                                           |
| <span data-ttu-id="5218f-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5218f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="5218f-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5218f-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5218f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5218f-197">Range-Lower</span></span>            | <span data-ttu-id="5218f-198">36</span><span class="sxs-lookup"><span data-stu-id="5218f-198">36</span></span>                                                              |
| <span data-ttu-id="5218f-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5218f-199">Range-Upper</span></span>            | <span data-ttu-id="5218f-200">36</span><span class="sxs-lookup"><span data-stu-id="5218f-200">36</span></span>                                                              |
| <span data-ttu-id="5218f-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-201">Search-Flags</span></span>           | <span data-ttu-id="5218f-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5218f-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="5218f-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-203">System-Flags</span></span>           | <span data-ttu-id="5218f-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5218f-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="5218f-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5218f-205">Classes used in</span></span>        | [<span data-ttu-id="5218f-206">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="5218f-206">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5218f-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5218f-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5218f-208">進入</span><span class="sxs-lookup"><span data-stu-id="5218f-208">Entry</span></span> | <span data-ttu-id="5218f-209">值</span><span class="sxs-lookup"><span data-stu-id="5218f-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5218f-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5218f-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5218f-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="5218f-212">System-Only</span></span>            | <span data-ttu-id="5218f-213">否</span><span class="sxs-lookup"><span data-stu-id="5218f-213">False</span></span>                                                           |
| <span data-ttu-id="5218f-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5218f-214">Is-Single-Valued</span></span>       | <span data-ttu-id="5218f-215">否</span><span class="sxs-lookup"><span data-stu-id="5218f-215">False</span></span>                                                           |
| <span data-ttu-id="5218f-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5218f-216">Is Indexed</span></span>             | <span data-ttu-id="5218f-217">否</span><span class="sxs-lookup"><span data-stu-id="5218f-217">False</span></span>                                                           |
| <span data-ttu-id="5218f-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5218f-218">In Global Catalog</span></span>      | <span data-ttu-id="5218f-219">否</span><span class="sxs-lookup"><span data-stu-id="5218f-219">False</span></span>                                                           |
| <span data-ttu-id="5218f-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5218f-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="5218f-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5218f-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5218f-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5218f-222">Range-Lower</span></span>            | <span data-ttu-id="5218f-223">36</span><span class="sxs-lookup"><span data-stu-id="5218f-223">36</span></span>                                                              |
| <span data-ttu-id="5218f-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5218f-224">Range-Upper</span></span>            | <span data-ttu-id="5218f-225">36</span><span class="sxs-lookup"><span data-stu-id="5218f-225">36</span></span>                                                              |
| <span data-ttu-id="5218f-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-226">Search-Flags</span></span>           | <span data-ttu-id="5218f-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5218f-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="5218f-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-228">System-Flags</span></span>           | <span data-ttu-id="5218f-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5218f-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="5218f-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5218f-230">Classes used in</span></span>        | [<span data-ttu-id="5218f-231">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="5218f-231">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5218f-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5218f-232">Windows Server 2008</span></span>



| <span data-ttu-id="5218f-233">進入</span><span class="sxs-lookup"><span data-stu-id="5218f-233">Entry</span></span> | <span data-ttu-id="5218f-234">值</span><span class="sxs-lookup"><span data-stu-id="5218f-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5218f-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5218f-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5218f-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="5218f-237">System-Only</span></span>            | <span data-ttu-id="5218f-238">否</span><span class="sxs-lookup"><span data-stu-id="5218f-238">False</span></span>                                                           |
| <span data-ttu-id="5218f-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5218f-239">Is-Single-Valued</span></span>       | <span data-ttu-id="5218f-240">否</span><span class="sxs-lookup"><span data-stu-id="5218f-240">False</span></span>                                                           |
| <span data-ttu-id="5218f-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5218f-241">Is Indexed</span></span>             | <span data-ttu-id="5218f-242">否</span><span class="sxs-lookup"><span data-stu-id="5218f-242">False</span></span>                                                           |
| <span data-ttu-id="5218f-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5218f-243">In Global Catalog</span></span>      | <span data-ttu-id="5218f-244">否</span><span class="sxs-lookup"><span data-stu-id="5218f-244">False</span></span>                                                           |
| <span data-ttu-id="5218f-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5218f-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="5218f-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5218f-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5218f-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5218f-247">Range-Lower</span></span>            | <span data-ttu-id="5218f-248">36</span><span class="sxs-lookup"><span data-stu-id="5218f-248">36</span></span>                                                              |
| <span data-ttu-id="5218f-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5218f-249">Range-Upper</span></span>            | <span data-ttu-id="5218f-250">36</span><span class="sxs-lookup"><span data-stu-id="5218f-250">36</span></span>                                                              |
| <span data-ttu-id="5218f-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-251">Search-Flags</span></span>           | <span data-ttu-id="5218f-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5218f-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="5218f-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-253">System-Flags</span></span>           | <span data-ttu-id="5218f-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5218f-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="5218f-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5218f-255">Classes used in</span></span>        | [<span data-ttu-id="5218f-256">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="5218f-256">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5218f-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5218f-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5218f-258">進入</span><span class="sxs-lookup"><span data-stu-id="5218f-258">Entry</span></span> | <span data-ttu-id="5218f-259">值</span><span class="sxs-lookup"><span data-stu-id="5218f-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5218f-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5218f-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5218f-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="5218f-262">System-Only</span></span>            | <span data-ttu-id="5218f-263">否</span><span class="sxs-lookup"><span data-stu-id="5218f-263">False</span></span>                                                           |
| <span data-ttu-id="5218f-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5218f-264">Is-Single-Valued</span></span>       | <span data-ttu-id="5218f-265">否</span><span class="sxs-lookup"><span data-stu-id="5218f-265">False</span></span>                                                           |
| <span data-ttu-id="5218f-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5218f-266">Is Indexed</span></span>             | <span data-ttu-id="5218f-267">否</span><span class="sxs-lookup"><span data-stu-id="5218f-267">False</span></span>                                                           |
| <span data-ttu-id="5218f-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5218f-268">In Global Catalog</span></span>      | <span data-ttu-id="5218f-269">否</span><span class="sxs-lookup"><span data-stu-id="5218f-269">False</span></span>                                                           |
| <span data-ttu-id="5218f-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5218f-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="5218f-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5218f-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5218f-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5218f-272">Range-Lower</span></span>            | <span data-ttu-id="5218f-273">36</span><span class="sxs-lookup"><span data-stu-id="5218f-273">36</span></span>                                                              |
| <span data-ttu-id="5218f-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5218f-274">Range-Upper</span></span>            | <span data-ttu-id="5218f-275">36</span><span class="sxs-lookup"><span data-stu-id="5218f-275">36</span></span>                                                              |
| <span data-ttu-id="5218f-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-276">Search-Flags</span></span>           | <span data-ttu-id="5218f-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5218f-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="5218f-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-278">System-Flags</span></span>           | <span data-ttu-id="5218f-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5218f-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="5218f-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5218f-280">Classes used in</span></span>        | [<span data-ttu-id="5218f-281">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="5218f-281">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5218f-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5218f-282">Windows Server 2012</span></span>



| <span data-ttu-id="5218f-283">進入</span><span class="sxs-lookup"><span data-stu-id="5218f-283">Entry</span></span> | <span data-ttu-id="5218f-284">值</span><span class="sxs-lookup"><span data-stu-id="5218f-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5218f-285">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5218f-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5218f-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5218f-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="5218f-287">System-Only</span></span>            | <span data-ttu-id="5218f-288">否</span><span class="sxs-lookup"><span data-stu-id="5218f-288">False</span></span>                                                           |
| <span data-ttu-id="5218f-289">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5218f-289">Is-Single-Valued</span></span>       | <span data-ttu-id="5218f-290">否</span><span class="sxs-lookup"><span data-stu-id="5218f-290">False</span></span>                                                           |
| <span data-ttu-id="5218f-291">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5218f-291">Is Indexed</span></span>             | <span data-ttu-id="5218f-292">否</span><span class="sxs-lookup"><span data-stu-id="5218f-292">False</span></span>                                                           |
| <span data-ttu-id="5218f-293">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5218f-293">In Global Catalog</span></span>      | <span data-ttu-id="5218f-294">否</span><span class="sxs-lookup"><span data-stu-id="5218f-294">False</span></span>                                                           |
| <span data-ttu-id="5218f-295">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5218f-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="5218f-296">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5218f-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5218f-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5218f-297">Range-Lower</span></span>            | <span data-ttu-id="5218f-298">36</span><span class="sxs-lookup"><span data-stu-id="5218f-298">36</span></span>                                                              |
| <span data-ttu-id="5218f-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5218f-299">Range-Upper</span></span>            | <span data-ttu-id="5218f-300">36</span><span class="sxs-lookup"><span data-stu-id="5218f-300">36</span></span>                                                              |
| <span data-ttu-id="5218f-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-301">Search-Flags</span></span>           | <span data-ttu-id="5218f-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5218f-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="5218f-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5218f-303">System-Flags</span></span>           | <span data-ttu-id="5218f-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5218f-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="5218f-305">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5218f-305">Classes used in</span></span>        | [<span data-ttu-id="5218f-306">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="5218f-306">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 






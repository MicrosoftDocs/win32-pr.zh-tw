---
title: UpdateScript 屬性
description: 這是用來以網域重建指令來保存腳本。
ms.assetid: a9dd205d-f6c3-4eeb-95dc-491bfe30ab8b
ms.tgt_platform: multiple
keywords:
- UpdateScript 屬性 AD 架構
- UpdateScript 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-UpdateScript
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7809bf6fdbaabb38976068d1998cacfb12bdaf3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971910"
---
# <a name="ms-ds-updatescript-attribute"></a><span data-ttu-id="b1ea8-105">UpdateScript 屬性</span><span class="sxs-lookup"><span data-stu-id="b1ea8-105">ms-DS-UpdateScript attribute</span></span>

<span data-ttu-id="b1ea8-106">這是用來以網域重建指令來保存腳本。</span><span class="sxs-lookup"><span data-stu-id="b1ea8-106">This is used to hold the script with the domain restructure instructions.</span></span>



| <span data-ttu-id="b1ea8-107">進入</span><span class="sxs-lookup"><span data-stu-id="b1ea8-107">Entry</span></span> | <span data-ttu-id="b1ea8-108">值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b1ea8-109">CN</span><span class="sxs-lookup"><span data-stu-id="b1ea8-109">CN</span></span>                | <span data-ttu-id="b1ea8-110">UpdateScript</span><span class="sxs-lookup"><span data-stu-id="b1ea8-110">ms-DS-UpdateScript</span></span>                          |
| <span data-ttu-id="b1ea8-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b1ea8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b1ea8-112">UpdateScript</span><span class="sxs-lookup"><span data-stu-id="b1ea8-112">msDS-UpdateScript</span></span>                           |
| <span data-ttu-id="b1ea8-113">大小</span><span class="sxs-lookup"><span data-stu-id="b1ea8-113">Size</span></span>              | <span data-ttu-id="b1ea8-114">大小上限為10K 個位元組。</span><span class="sxs-lookup"><span data-stu-id="b1ea8-114">Maximum size 10K bytes.</span></span>                     |
| <span data-ttu-id="b1ea8-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b1ea8-115">Update Privilege</span></span>  | <span data-ttu-id="b1ea8-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="b1ea8-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="b1ea8-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b1ea8-117">Update Frequency</span></span>  | <span data-ttu-id="b1ea8-118">只有在網域重建時。</span><span class="sxs-lookup"><span data-stu-id="b1ea8-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="b1ea8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1ea8-119">Attribute-Id</span></span>      | <span data-ttu-id="b1ea8-120">1.2.840.113556.1.4.1721</span><span class="sxs-lookup"><span data-stu-id="b1ea8-120">1.2.840.113556.1.4.1721</span></span>                     |
| <span data-ttu-id="b1ea8-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b1ea8-121">System-Id-Guid</span></span>    | <span data-ttu-id="b1ea8-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span><span class="sxs-lookup"><span data-stu-id="b1ea8-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span></span>        |
| <span data-ttu-id="b1ea8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1ea8-123">Syntax</span></span>            | [<span data-ttu-id="b1ea8-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b1ea8-125">實作</span><span class="sxs-lookup"><span data-stu-id="b1ea8-125">Implementations</span></span>

-   [<span data-ttu-id="b1ea8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1ea8-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b1ea8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1ea8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1ea8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1ea8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b1ea8-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1ea8-132">Windows Server 2003</span></span>



| <span data-ttu-id="b1ea8-133">進入</span><span class="sxs-lookup"><span data-stu-id="b1ea8-133">Entry</span></span> | <span data-ttu-id="b1ea8-134">值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b1ea8-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1ea8-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1ea8-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1ea8-137">System-Only</span></span>            | <span data-ttu-id="b1ea8-138">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-138">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b1ea8-140">對</span><span class="sxs-lookup"><span data-stu-id="b1ea8-140">True</span></span>                                                          |
| <span data-ttu-id="b1ea8-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1ea8-141">Is Indexed</span></span>             | <span data-ttu-id="b1ea8-142">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-142">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1ea8-143">In Global Catalog</span></span>      | <span data-ttu-id="b1ea8-144">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-144">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1ea8-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1ea8-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1ea8-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b1ea8-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1ea8-147">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1ea8-148">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-149">Search-Flags</span></span>           | <span data-ttu-id="b1ea8-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1ea8-150">0x00000000</span></span>                                                    |
| <span data-ttu-id="b1ea8-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-151">System-Flags</span></span>           | <span data-ttu-id="b1ea8-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1ea8-152">0x00000010</span></span>                                                    |
| <span data-ttu-id="b1ea8-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1ea8-153">Classes used in</span></span>        | [<span data-ttu-id="b1ea8-154">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b1ea8-155">亞當</span><span class="sxs-lookup"><span data-stu-id="b1ea8-155">ADAM</span></span>



| <span data-ttu-id="b1ea8-156">進入</span><span class="sxs-lookup"><span data-stu-id="b1ea8-156">Entry</span></span> | <span data-ttu-id="b1ea8-157">值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-157">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b1ea8-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1ea8-158">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1ea8-159">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1ea8-160">System-Only</span></span>            | <span data-ttu-id="b1ea8-161">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-161">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b1ea8-163">對</span><span class="sxs-lookup"><span data-stu-id="b1ea8-163">True</span></span>                                                          |
| <span data-ttu-id="b1ea8-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1ea8-164">Is Indexed</span></span>             | <span data-ttu-id="b1ea8-165">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-165">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1ea8-166">In Global Catalog</span></span>      | <span data-ttu-id="b1ea8-167">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-167">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1ea8-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1ea8-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1ea8-169">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b1ea8-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1ea8-170">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1ea8-171">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-172">Search-Flags</span></span>           | <span data-ttu-id="b1ea8-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1ea8-173">0x00000000</span></span>                                                    |
| <span data-ttu-id="b1ea8-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-174">System-Flags</span></span>           | <span data-ttu-id="b1ea8-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1ea8-175">0x00000010</span></span>                                                    |
| <span data-ttu-id="b1ea8-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1ea8-176">Classes used in</span></span>        | [<span data-ttu-id="b1ea8-177">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1ea8-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1ea8-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1ea8-179">進入</span><span class="sxs-lookup"><span data-stu-id="b1ea8-179">Entry</span></span> | <span data-ttu-id="b1ea8-180">值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-180">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b1ea8-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1ea8-181">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1ea8-182">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1ea8-183">System-Only</span></span>            | <span data-ttu-id="b1ea8-184">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-184">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b1ea8-186">對</span><span class="sxs-lookup"><span data-stu-id="b1ea8-186">True</span></span>                                                          |
| <span data-ttu-id="b1ea8-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1ea8-187">Is Indexed</span></span>             | <span data-ttu-id="b1ea8-188">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-188">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1ea8-189">In Global Catalog</span></span>      | <span data-ttu-id="b1ea8-190">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-190">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1ea8-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1ea8-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1ea8-192">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b1ea8-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1ea8-193">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1ea8-194">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-195">Search-Flags</span></span>           | <span data-ttu-id="b1ea8-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1ea8-196">0x00000000</span></span>                                                    |
| <span data-ttu-id="b1ea8-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-197">System-Flags</span></span>           | <span data-ttu-id="b1ea8-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1ea8-198">0x00000010</span></span>                                                    |
| <span data-ttu-id="b1ea8-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1ea8-199">Classes used in</span></span>        | [<span data-ttu-id="b1ea8-200">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-200">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1ea8-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1ea8-201">Windows Server 2008</span></span>



| <span data-ttu-id="b1ea8-202">進入</span><span class="sxs-lookup"><span data-stu-id="b1ea8-202">Entry</span></span> | <span data-ttu-id="b1ea8-203">值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-203">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b1ea8-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1ea8-204">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1ea8-205">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1ea8-206">System-Only</span></span>            | <span data-ttu-id="b1ea8-207">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-207">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b1ea8-209">對</span><span class="sxs-lookup"><span data-stu-id="b1ea8-209">True</span></span>                                                          |
| <span data-ttu-id="b1ea8-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1ea8-210">Is Indexed</span></span>             | <span data-ttu-id="b1ea8-211">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-211">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1ea8-212">In Global Catalog</span></span>      | <span data-ttu-id="b1ea8-213">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-213">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1ea8-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1ea8-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1ea8-215">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b1ea8-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1ea8-216">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1ea8-217">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-218">Search-Flags</span></span>           | <span data-ttu-id="b1ea8-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1ea8-219">0x00000000</span></span>                                                    |
| <span data-ttu-id="b1ea8-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-220">System-Flags</span></span>           | <span data-ttu-id="b1ea8-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1ea8-221">0x00000010</span></span>                                                    |
| <span data-ttu-id="b1ea8-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1ea8-222">Classes used in</span></span>        | [<span data-ttu-id="b1ea8-223">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-223">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1ea8-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1ea8-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1ea8-225">進入</span><span class="sxs-lookup"><span data-stu-id="b1ea8-225">Entry</span></span> | <span data-ttu-id="b1ea8-226">值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-226">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b1ea8-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1ea8-227">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1ea8-228">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1ea8-229">System-Only</span></span>            | <span data-ttu-id="b1ea8-230">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-230">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b1ea8-232">對</span><span class="sxs-lookup"><span data-stu-id="b1ea8-232">True</span></span>                                                          |
| <span data-ttu-id="b1ea8-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1ea8-233">Is Indexed</span></span>             | <span data-ttu-id="b1ea8-234">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-234">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1ea8-235">In Global Catalog</span></span>      | <span data-ttu-id="b1ea8-236">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-236">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1ea8-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1ea8-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1ea8-238">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b1ea8-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1ea8-239">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1ea8-240">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-241">Search-Flags</span></span>           | <span data-ttu-id="b1ea8-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1ea8-242">0x00000000</span></span>                                                    |
| <span data-ttu-id="b1ea8-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-243">System-Flags</span></span>           | <span data-ttu-id="b1ea8-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1ea8-244">0x00000010</span></span>                                                    |
| <span data-ttu-id="b1ea8-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1ea8-245">Classes used in</span></span>        | [<span data-ttu-id="b1ea8-246">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-246">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1ea8-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1ea8-247">Windows Server 2012</span></span>



| <span data-ttu-id="b1ea8-248">進入</span><span class="sxs-lookup"><span data-stu-id="b1ea8-248">Entry</span></span> | <span data-ttu-id="b1ea8-249">值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-249">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b1ea8-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1ea8-250">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1ea8-251">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b1ea8-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1ea8-252">System-Only</span></span>            | <span data-ttu-id="b1ea8-253">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-253">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1ea8-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b1ea8-255">對</span><span class="sxs-lookup"><span data-stu-id="b1ea8-255">True</span></span>                                                          |
| <span data-ttu-id="b1ea8-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1ea8-256">Is Indexed</span></span>             | <span data-ttu-id="b1ea8-257">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-257">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1ea8-258">In Global Catalog</span></span>      | <span data-ttu-id="b1ea8-259">否</span><span class="sxs-lookup"><span data-stu-id="b1ea8-259">False</span></span>                                                         |
| <span data-ttu-id="b1ea8-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1ea8-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1ea8-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1ea8-261">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b1ea8-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1ea8-262">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1ea8-263">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b1ea8-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-264">Search-Flags</span></span>           | <span data-ttu-id="b1ea8-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1ea8-265">0x00000000</span></span>                                                    |
| <span data-ttu-id="b1ea8-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1ea8-266">System-Flags</span></span>           | <span data-ttu-id="b1ea8-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1ea8-267">0x00000010</span></span>                                                    |
| <span data-ttu-id="b1ea8-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1ea8-268">Classes used in</span></span>        | [<span data-ttu-id="b1ea8-269">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="b1ea8-269">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 






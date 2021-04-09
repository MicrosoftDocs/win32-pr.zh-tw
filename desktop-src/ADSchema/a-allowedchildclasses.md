---
title: 允許的-子類別屬性
description: 類別可包含的類別。
ms.assetid: 3bfeefe3-b728-40a2-8b0a-3064a9ca42d0
ms.tgt_platform: multiple
keywords:
- 允許的-子類別屬性 AD 架構
- allowedChildClasses 屬性 AD 架構
topic_type:
- apiref
api_name:
- Allowed-Child-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45c295036ad8b1c132e2dbf97d2e0d9ab38f9598
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687328"
---
# <a name="allowed-child-classes-attribute"></a><span data-ttu-id="7f6e4-105">允許的-子類別屬性</span><span class="sxs-lookup"><span data-stu-id="7f6e4-105">Allowed-Child-Classes attribute</span></span>

<span data-ttu-id="7f6e4-106">類別可包含的類別。</span><span class="sxs-lookup"><span data-stu-id="7f6e4-106">Classes that can be contained by a class.</span></span>



| <span data-ttu-id="7f6e4-107">進入</span><span class="sxs-lookup"><span data-stu-id="7f6e4-107">Entry</span></span> | <span data-ttu-id="7f6e4-108">值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="7f6e4-109">CN</span><span class="sxs-lookup"><span data-stu-id="7f6e4-109">CN</span></span>                | <span data-ttu-id="7f6e4-110">允許-子類別</span><span class="sxs-lookup"><span data-stu-id="7f6e4-110">Allowed-Child-Classes</span></span>                                           |
| <span data-ttu-id="7f6e4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7f6e4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7f6e4-112">allowedChildClasses</span><span class="sxs-lookup"><span data-stu-id="7f6e4-112">allowedChildClasses</span></span>                                             |
| <span data-ttu-id="7f6e4-113">大小</span><span class="sxs-lookup"><span data-stu-id="7f6e4-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="7f6e4-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7f6e4-114">Update Privilege</span></span>  | \-                                                              |
| <span data-ttu-id="7f6e4-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7f6e4-115">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="7f6e4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7f6e4-116">Attribute-Id</span></span>      | <span data-ttu-id="7f6e4-117">1.2.840.113556.1.4.911</span><span class="sxs-lookup"><span data-stu-id="7f6e4-117">1.2.840.113556.1.4.911</span></span>                                          |
| <span data-ttu-id="7f6e4-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7f6e4-118">System-Id-Guid</span></span>    | <span data-ttu-id="7f6e4-119">9a7ad942-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="7f6e4-119">9a7ad942-ca53-11d1-bbd0-0080c76670c0</span></span>                            |
| <span data-ttu-id="7f6e4-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f6e4-120">Syntax</span></span>            | [<span data-ttu-id="7f6e4-121">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-121">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="7f6e4-122">實作</span><span class="sxs-lookup"><span data-stu-id="7f6e4-122">Implementations</span></span>

-   [<span data-ttu-id="7f6e4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7f6e4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7f6e4-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7f6e4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7f6e4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7f6e4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7f6e4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7f6e4-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f6e4-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7f6e4-131">進入</span><span class="sxs-lookup"><span data-stu-id="7f6e4-131">Entry</span></span> | <span data-ttu-id="7f6e4-132">值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f6e4-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f6e4-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f6e4-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f6e4-135">System-Only</span></span>            | <span data-ttu-id="7f6e4-136">對</span><span class="sxs-lookup"><span data-stu-id="7f6e4-136">True</span></span>                            |
| <span data-ttu-id="7f6e4-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7f6e4-138">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-138">False</span></span>                           |
| <span data-ttu-id="7f6e4-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f6e4-139">Is Indexed</span></span>             | <span data-ttu-id="7f6e4-140">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-140">False</span></span>                           |
| <span data-ttu-id="7f6e4-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f6e4-141">In Global Catalog</span></span>      | <span data-ttu-id="7f6e4-142">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-142">False</span></span>                           |
| <span data-ttu-id="7f6e4-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f6e4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f6e4-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f6e4-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f6e4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f6e4-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f6e4-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-147">Search-Flags</span></span>           | <span data-ttu-id="7f6e4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f6e4-148">0x00000000</span></span>                      |
| <span data-ttu-id="7f6e4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-149">System-Flags</span></span>           | <span data-ttu-id="7f6e4-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7f6e4-150">0x08000014</span></span>                      |
| <span data-ttu-id="7f6e4-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f6e4-151">Classes used in</span></span>        | [<span data-ttu-id="7f6e4-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7f6e4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7f6e4-153">Windows Server 2003</span></span>



| <span data-ttu-id="7f6e4-154">進入</span><span class="sxs-lookup"><span data-stu-id="7f6e4-154">Entry</span></span> | <span data-ttu-id="7f6e4-155">值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f6e4-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f6e4-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f6e4-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f6e4-158">System-Only</span></span>            | <span data-ttu-id="7f6e4-159">對</span><span class="sxs-lookup"><span data-stu-id="7f6e4-159">True</span></span>                            |
| <span data-ttu-id="7f6e4-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7f6e4-161">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-161">False</span></span>                           |
| <span data-ttu-id="7f6e4-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f6e4-162">Is Indexed</span></span>             | <span data-ttu-id="7f6e4-163">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-163">False</span></span>                           |
| <span data-ttu-id="7f6e4-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f6e4-164">In Global Catalog</span></span>      | <span data-ttu-id="7f6e4-165">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-165">False</span></span>                           |
| <span data-ttu-id="7f6e4-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f6e4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f6e4-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f6e4-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f6e4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f6e4-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f6e4-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-170">Search-Flags</span></span>           | <span data-ttu-id="7f6e4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f6e4-171">0x00000000</span></span>                      |
| <span data-ttu-id="7f6e4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-172">System-Flags</span></span>           | <span data-ttu-id="7f6e4-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7f6e4-173">0x08000014</span></span>                      |
| <span data-ttu-id="7f6e4-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f6e4-174">Classes used in</span></span>        | [<span data-ttu-id="7f6e4-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7f6e4-176">亞當</span><span class="sxs-lookup"><span data-stu-id="7f6e4-176">ADAM</span></span>



| <span data-ttu-id="7f6e4-177">進入</span><span class="sxs-lookup"><span data-stu-id="7f6e4-177">Entry</span></span> | <span data-ttu-id="7f6e4-178">值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f6e4-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f6e4-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f6e4-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f6e4-181">System-Only</span></span>            | <span data-ttu-id="7f6e4-182">對</span><span class="sxs-lookup"><span data-stu-id="7f6e4-182">True</span></span>                            |
| <span data-ttu-id="7f6e4-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7f6e4-184">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-184">False</span></span>                           |
| <span data-ttu-id="7f6e4-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f6e4-185">Is Indexed</span></span>             | <span data-ttu-id="7f6e4-186">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-186">False</span></span>                           |
| <span data-ttu-id="7f6e4-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f6e4-187">In Global Catalog</span></span>      | <span data-ttu-id="7f6e4-188">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-188">False</span></span>                           |
| <span data-ttu-id="7f6e4-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f6e4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f6e4-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f6e4-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f6e4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f6e4-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f6e4-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-193">Search-Flags</span></span>           | <span data-ttu-id="7f6e4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f6e4-194">0x00000000</span></span>                      |
| <span data-ttu-id="7f6e4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-195">System-Flags</span></span>           | <span data-ttu-id="7f6e4-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7f6e4-196">0x08000014</span></span>                      |
| <span data-ttu-id="7f6e4-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f6e4-197">Classes used in</span></span>        | [<span data-ttu-id="7f6e4-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7f6e4-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7f6e4-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7f6e4-200">進入</span><span class="sxs-lookup"><span data-stu-id="7f6e4-200">Entry</span></span> | <span data-ttu-id="7f6e4-201">值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f6e4-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f6e4-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f6e4-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f6e4-204">System-Only</span></span>            | <span data-ttu-id="7f6e4-205">對</span><span class="sxs-lookup"><span data-stu-id="7f6e4-205">True</span></span>                            |
| <span data-ttu-id="7f6e4-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7f6e4-207">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-207">False</span></span>                           |
| <span data-ttu-id="7f6e4-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f6e4-208">Is Indexed</span></span>             | <span data-ttu-id="7f6e4-209">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-209">False</span></span>                           |
| <span data-ttu-id="7f6e4-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f6e4-210">In Global Catalog</span></span>      | <span data-ttu-id="7f6e4-211">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-211">False</span></span>                           |
| <span data-ttu-id="7f6e4-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f6e4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f6e4-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f6e4-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f6e4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f6e4-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f6e4-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-216">Search-Flags</span></span>           | <span data-ttu-id="7f6e4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f6e4-217">0x00000000</span></span>                      |
| <span data-ttu-id="7f6e4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-218">System-Flags</span></span>           | <span data-ttu-id="7f6e4-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7f6e4-219">0x08000014</span></span>                      |
| <span data-ttu-id="7f6e4-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f6e4-220">Classes used in</span></span>        | [<span data-ttu-id="7f6e4-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7f6e4-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f6e4-222">Windows Server 2008</span></span>



| <span data-ttu-id="7f6e4-223">進入</span><span class="sxs-lookup"><span data-stu-id="7f6e4-223">Entry</span></span> | <span data-ttu-id="7f6e4-224">值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f6e4-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f6e4-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f6e4-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f6e4-227">System-Only</span></span>            | <span data-ttu-id="7f6e4-228">對</span><span class="sxs-lookup"><span data-stu-id="7f6e4-228">True</span></span>                            |
| <span data-ttu-id="7f6e4-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7f6e4-230">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-230">False</span></span>                           |
| <span data-ttu-id="7f6e4-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f6e4-231">Is Indexed</span></span>             | <span data-ttu-id="7f6e4-232">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-232">False</span></span>                           |
| <span data-ttu-id="7f6e4-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f6e4-233">In Global Catalog</span></span>      | <span data-ttu-id="7f6e4-234">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-234">False</span></span>                           |
| <span data-ttu-id="7f6e4-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f6e4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f6e4-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f6e4-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f6e4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f6e4-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f6e4-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-239">Search-Flags</span></span>           | <span data-ttu-id="7f6e4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f6e4-240">0x00000000</span></span>                      |
| <span data-ttu-id="7f6e4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-241">System-Flags</span></span>           | <span data-ttu-id="7f6e4-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7f6e4-242">0x08000014</span></span>                      |
| <span data-ttu-id="7f6e4-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f6e4-243">Classes used in</span></span>        | [<span data-ttu-id="7f6e4-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7f6e4-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7f6e4-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7f6e4-246">進入</span><span class="sxs-lookup"><span data-stu-id="7f6e4-246">Entry</span></span> | <span data-ttu-id="7f6e4-247">值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f6e4-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f6e4-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f6e4-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f6e4-250">System-Only</span></span>            | <span data-ttu-id="7f6e4-251">對</span><span class="sxs-lookup"><span data-stu-id="7f6e4-251">True</span></span>                            |
| <span data-ttu-id="7f6e4-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7f6e4-253">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-253">False</span></span>                           |
| <span data-ttu-id="7f6e4-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f6e4-254">Is Indexed</span></span>             | <span data-ttu-id="7f6e4-255">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-255">False</span></span>                           |
| <span data-ttu-id="7f6e4-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f6e4-256">In Global Catalog</span></span>      | <span data-ttu-id="7f6e4-257">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-257">False</span></span>                           |
| <span data-ttu-id="7f6e4-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f6e4-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f6e4-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f6e4-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f6e4-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f6e4-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f6e4-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-262">Search-Flags</span></span>           | <span data-ttu-id="7f6e4-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f6e4-263">0x00000000</span></span>                      |
| <span data-ttu-id="7f6e4-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-264">System-Flags</span></span>           | <span data-ttu-id="7f6e4-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7f6e4-265">0x08000014</span></span>                      |
| <span data-ttu-id="7f6e4-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f6e4-266">Classes used in</span></span>        | [<span data-ttu-id="7f6e4-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7f6e4-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f6e4-268">Windows Server 2012</span></span>



| <span data-ttu-id="7f6e4-269">進入</span><span class="sxs-lookup"><span data-stu-id="7f6e4-269">Entry</span></span> | <span data-ttu-id="7f6e4-270">值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f6e4-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f6e4-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f6e4-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f6e4-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f6e4-273">System-Only</span></span>            | <span data-ttu-id="7f6e4-274">對</span><span class="sxs-lookup"><span data-stu-id="7f6e4-274">True</span></span>                            |
| <span data-ttu-id="7f6e4-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f6e4-275">Is-Single-Valued</span></span>       | <span data-ttu-id="7f6e4-276">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-276">False</span></span>                           |
| <span data-ttu-id="7f6e4-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f6e4-277">Is Indexed</span></span>             | <span data-ttu-id="7f6e4-278">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-278">False</span></span>                           |
| <span data-ttu-id="7f6e4-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f6e4-279">In Global Catalog</span></span>      | <span data-ttu-id="7f6e4-280">否</span><span class="sxs-lookup"><span data-stu-id="7f6e4-280">False</span></span>                           |
| <span data-ttu-id="7f6e4-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f6e4-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f6e4-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f6e4-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f6e4-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f6e4-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f6e4-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f6e4-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-285">Search-Flags</span></span>           | <span data-ttu-id="7f6e4-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f6e4-286">0x00000000</span></span>                      |
| <span data-ttu-id="7f6e4-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f6e4-287">System-Flags</span></span>           | <span data-ttu-id="7f6e4-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7f6e4-288">0x08000014</span></span>                      |
| <span data-ttu-id="7f6e4-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f6e4-289">Classes used in</span></span>        | [<span data-ttu-id="7f6e4-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7f6e4-290">**Top**</span></span>](c-top.md)<br/> |



 

 






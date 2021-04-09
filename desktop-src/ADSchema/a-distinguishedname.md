---
title: Obj-Dist-Name 屬性
description: 與物件的辨別名稱相同。 供 Exchange 使用。
ms.assetid: 0dc2855c-2707-49d8-80e6-27f163a59bc8
ms.tgt_platform: multiple
keywords:
- Obj-Dist-Name 屬性 AD 架構
- distinguishedName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Obj-Dist-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42cd118f38de78546b7b792bca3c8c9ef6d229cb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844683"
---
# <a name="obj-dist-name-attribute"></a><span data-ttu-id="09e0d-106">Obj-Dist-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="09e0d-106">Obj-Dist-Name attribute</span></span>

<span data-ttu-id="09e0d-107">與物件的辨別名稱相同。</span><span class="sxs-lookup"><span data-stu-id="09e0d-107">Same as the Distinguished Name for an object.</span></span> <span data-ttu-id="09e0d-108">供 Exchange 使用。</span><span class="sxs-lookup"><span data-stu-id="09e0d-108">Used by Exchange.</span></span>



| <span data-ttu-id="09e0d-109">進入</span><span class="sxs-lookup"><span data-stu-id="09e0d-109">Entry</span></span> | <span data-ttu-id="09e0d-110">值</span><span class="sxs-lookup"><span data-stu-id="09e0d-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="09e0d-111">CN</span><span class="sxs-lookup"><span data-stu-id="09e0d-111">CN</span></span>                | <span data-ttu-id="09e0d-112">Obj-Dist 名稱</span><span class="sxs-lookup"><span data-stu-id="09e0d-112">Obj-Dist-Name</span></span>                           |
| <span data-ttu-id="09e0d-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="09e0d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="09e0d-114">distinguishedName</span><span class="sxs-lookup"><span data-stu-id="09e0d-114">distinguishedName</span></span>                       |
| <span data-ttu-id="09e0d-115">大小</span><span class="sxs-lookup"><span data-stu-id="09e0d-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="09e0d-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="09e0d-116">Update Privilege</span></span>  | <span data-ttu-id="09e0d-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="09e0d-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="09e0d-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="09e0d-118">Update Frequency</span></span>  | <span data-ttu-id="09e0d-119">每次建立或移動物件時。</span><span class="sxs-lookup"><span data-stu-id="09e0d-119">Whenever an object is created or moved.</span></span> |
| <span data-ttu-id="09e0d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09e0d-120">Attribute-Id</span></span>      | <span data-ttu-id="09e0d-121">2.5.4.49</span><span class="sxs-lookup"><span data-stu-id="09e0d-121">2.5.4.49</span></span>                                |
| <span data-ttu-id="09e0d-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="09e0d-122">System-Id-Guid</span></span>    | <span data-ttu-id="09e0d-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="09e0d-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="09e0d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="09e0d-124">Syntax</span></span>            | [<span data-ttu-id="09e0d-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="09e0d-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="09e0d-126">實作</span><span class="sxs-lookup"><span data-stu-id="09e0d-126">Implementations</span></span>

-   [<span data-ttu-id="09e0d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="09e0d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="09e0d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="09e0d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="09e0d-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="09e0d-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="09e0d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="09e0d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="09e0d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="09e0d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="09e0d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="09e0d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="09e0d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09e0d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="09e0d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09e0d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="09e0d-135">進入</span><span class="sxs-lookup"><span data-stu-id="09e0d-135">Entry</span></span> | <span data-ttu-id="09e0d-136">值</span><span class="sxs-lookup"><span data-stu-id="09e0d-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09e0d-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="09e0d-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09e0d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e0d-138">MAPI-Id</span></span>                | <span data-ttu-id="09e0d-139">0x803C</span><span class="sxs-lookup"><span data-stu-id="09e0d-139">0x803C</span></span>                          |
| <span data-ttu-id="09e0d-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e0d-140">System-Only</span></span>            | <span data-ttu-id="09e0d-141">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-141">True</span></span>                            |
| <span data-ttu-id="09e0d-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="09e0d-142">Is-Single-Valued</span></span>       | <span data-ttu-id="09e0d-143">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-143">True</span></span>                            |
| <span data-ttu-id="09e0d-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="09e0d-144">Is Indexed</span></span>             | <span data-ttu-id="09e0d-145">否</span><span class="sxs-lookup"><span data-stu-id="09e0d-145">False</span></span>                           |
| <span data-ttu-id="09e0d-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="09e0d-146">In Global Catalog</span></span>      | <span data-ttu-id="09e0d-147">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-147">True</span></span>                            |
| <span data-ttu-id="09e0d-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="09e0d-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e0d-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="09e0d-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09e0d-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e0d-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09e0d-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e0d-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09e0d-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-152">Search-Flags</span></span>           | <span data-ttu-id="09e0d-153">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09e0d-153">0x00000008</span></span>                      |
| <span data-ttu-id="09e0d-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-154">System-Flags</span></span>           | <span data-ttu-id="09e0d-155">0x00000013</span><span class="sxs-lookup"><span data-stu-id="09e0d-155">0x00000013</span></span>                      |
| <span data-ttu-id="09e0d-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="09e0d-156">Classes used in</span></span>        | [<span data-ttu-id="09e0d-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="09e0d-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="09e0d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09e0d-158">Windows Server 2003</span></span>



| <span data-ttu-id="09e0d-159">進入</span><span class="sxs-lookup"><span data-stu-id="09e0d-159">Entry</span></span> | <span data-ttu-id="09e0d-160">值</span><span class="sxs-lookup"><span data-stu-id="09e0d-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09e0d-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="09e0d-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09e0d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e0d-162">MAPI-Id</span></span>                | <span data-ttu-id="09e0d-163">0x803C</span><span class="sxs-lookup"><span data-stu-id="09e0d-163">0x803C</span></span>                          |
| <span data-ttu-id="09e0d-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e0d-164">System-Only</span></span>            | <span data-ttu-id="09e0d-165">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-165">True</span></span>                            |
| <span data-ttu-id="09e0d-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="09e0d-166">Is-Single-Valued</span></span>       | <span data-ttu-id="09e0d-167">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-167">True</span></span>                            |
| <span data-ttu-id="09e0d-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="09e0d-168">Is Indexed</span></span>             | <span data-ttu-id="09e0d-169">否</span><span class="sxs-lookup"><span data-stu-id="09e0d-169">False</span></span>                           |
| <span data-ttu-id="09e0d-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="09e0d-170">In Global Catalog</span></span>      | <span data-ttu-id="09e0d-171">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-171">True</span></span>                            |
| <span data-ttu-id="09e0d-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="09e0d-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e0d-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="09e0d-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09e0d-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e0d-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09e0d-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e0d-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09e0d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-176">Search-Flags</span></span>           | <span data-ttu-id="09e0d-177">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09e0d-177">0x00000008</span></span>                      |
| <span data-ttu-id="09e0d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-178">System-Flags</span></span>           | <span data-ttu-id="09e0d-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="09e0d-179">0x00000013</span></span>                      |
| <span data-ttu-id="09e0d-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="09e0d-180">Classes used in</span></span>        | [<span data-ttu-id="09e0d-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="09e0d-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="09e0d-182">亞當</span><span class="sxs-lookup"><span data-stu-id="09e0d-182">ADAM</span></span>



| <span data-ttu-id="09e0d-183">進入</span><span class="sxs-lookup"><span data-stu-id="09e0d-183">Entry</span></span> | <span data-ttu-id="09e0d-184">值</span><span class="sxs-lookup"><span data-stu-id="09e0d-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09e0d-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="09e0d-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09e0d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e0d-186">MAPI-Id</span></span>                | <span data-ttu-id="09e0d-187">0x803C</span><span class="sxs-lookup"><span data-stu-id="09e0d-187">0x803C</span></span>                          |
| <span data-ttu-id="09e0d-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e0d-188">System-Only</span></span>            | <span data-ttu-id="09e0d-189">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-189">True</span></span>                            |
| <span data-ttu-id="09e0d-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="09e0d-190">Is-Single-Valued</span></span>       | <span data-ttu-id="09e0d-191">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-191">True</span></span>                            |
| <span data-ttu-id="09e0d-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="09e0d-192">Is Indexed</span></span>             | <span data-ttu-id="09e0d-193">否</span><span class="sxs-lookup"><span data-stu-id="09e0d-193">False</span></span>                           |
| <span data-ttu-id="09e0d-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="09e0d-194">In Global Catalog</span></span>      | <span data-ttu-id="09e0d-195">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-195">True</span></span>                            |
| <span data-ttu-id="09e0d-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="09e0d-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e0d-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="09e0d-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09e0d-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e0d-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09e0d-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e0d-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09e0d-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-200">Search-Flags</span></span>           | <span data-ttu-id="09e0d-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09e0d-201">0x00000008</span></span>                      |
| <span data-ttu-id="09e0d-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-202">System-Flags</span></span>           | <span data-ttu-id="09e0d-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="09e0d-203">0x00000013</span></span>                      |
| <span data-ttu-id="09e0d-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="09e0d-204">Classes used in</span></span>        | [<span data-ttu-id="09e0d-205">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="09e0d-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="09e0d-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09e0d-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="09e0d-207">進入</span><span class="sxs-lookup"><span data-stu-id="09e0d-207">Entry</span></span> | <span data-ttu-id="09e0d-208">值</span><span class="sxs-lookup"><span data-stu-id="09e0d-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09e0d-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="09e0d-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09e0d-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e0d-210">MAPI-Id</span></span>                | <span data-ttu-id="09e0d-211">0x803C</span><span class="sxs-lookup"><span data-stu-id="09e0d-211">0x803C</span></span>                          |
| <span data-ttu-id="09e0d-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e0d-212">System-Only</span></span>            | <span data-ttu-id="09e0d-213">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-213">True</span></span>                            |
| <span data-ttu-id="09e0d-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="09e0d-214">Is-Single-Valued</span></span>       | <span data-ttu-id="09e0d-215">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-215">True</span></span>                            |
| <span data-ttu-id="09e0d-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="09e0d-216">Is Indexed</span></span>             | <span data-ttu-id="09e0d-217">否</span><span class="sxs-lookup"><span data-stu-id="09e0d-217">False</span></span>                           |
| <span data-ttu-id="09e0d-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="09e0d-218">In Global Catalog</span></span>      | <span data-ttu-id="09e0d-219">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-219">True</span></span>                            |
| <span data-ttu-id="09e0d-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="09e0d-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e0d-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="09e0d-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09e0d-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e0d-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09e0d-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e0d-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09e0d-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-224">Search-Flags</span></span>           | <span data-ttu-id="09e0d-225">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09e0d-225">0x00000008</span></span>                      |
| <span data-ttu-id="09e0d-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-226">System-Flags</span></span>           | <span data-ttu-id="09e0d-227">0x00000013</span><span class="sxs-lookup"><span data-stu-id="09e0d-227">0x00000013</span></span>                      |
| <span data-ttu-id="09e0d-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="09e0d-228">Classes used in</span></span>        | [<span data-ttu-id="09e0d-229">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="09e0d-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="09e0d-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09e0d-230">Windows Server 2008</span></span>



| <span data-ttu-id="09e0d-231">進入</span><span class="sxs-lookup"><span data-stu-id="09e0d-231">Entry</span></span> | <span data-ttu-id="09e0d-232">值</span><span class="sxs-lookup"><span data-stu-id="09e0d-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09e0d-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="09e0d-233">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09e0d-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e0d-234">MAPI-Id</span></span>                | <span data-ttu-id="09e0d-235">0x803C</span><span class="sxs-lookup"><span data-stu-id="09e0d-235">0x803C</span></span>                          |
| <span data-ttu-id="09e0d-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e0d-236">System-Only</span></span>            | <span data-ttu-id="09e0d-237">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-237">True</span></span>                            |
| <span data-ttu-id="09e0d-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="09e0d-238">Is-Single-Valued</span></span>       | <span data-ttu-id="09e0d-239">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-239">True</span></span>                            |
| <span data-ttu-id="09e0d-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="09e0d-240">Is Indexed</span></span>             | <span data-ttu-id="09e0d-241">否</span><span class="sxs-lookup"><span data-stu-id="09e0d-241">False</span></span>                           |
| <span data-ttu-id="09e0d-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="09e0d-242">In Global Catalog</span></span>      | <span data-ttu-id="09e0d-243">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-243">True</span></span>                            |
| <span data-ttu-id="09e0d-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="09e0d-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e0d-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="09e0d-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09e0d-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e0d-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09e0d-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e0d-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09e0d-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-248">Search-Flags</span></span>           | <span data-ttu-id="09e0d-249">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09e0d-249">0x00000008</span></span>                      |
| <span data-ttu-id="09e0d-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-250">System-Flags</span></span>           | <span data-ttu-id="09e0d-251">0x00000013</span><span class="sxs-lookup"><span data-stu-id="09e0d-251">0x00000013</span></span>                      |
| <span data-ttu-id="09e0d-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="09e0d-252">Classes used in</span></span>        | [<span data-ttu-id="09e0d-253">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="09e0d-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="09e0d-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09e0d-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="09e0d-255">進入</span><span class="sxs-lookup"><span data-stu-id="09e0d-255">Entry</span></span> | <span data-ttu-id="09e0d-256">值</span><span class="sxs-lookup"><span data-stu-id="09e0d-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09e0d-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="09e0d-257">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09e0d-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e0d-258">MAPI-Id</span></span>                | <span data-ttu-id="09e0d-259">0x803C</span><span class="sxs-lookup"><span data-stu-id="09e0d-259">0x803C</span></span>                          |
| <span data-ttu-id="09e0d-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e0d-260">System-Only</span></span>            | <span data-ttu-id="09e0d-261">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-261">True</span></span>                            |
| <span data-ttu-id="09e0d-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="09e0d-262">Is-Single-Valued</span></span>       | <span data-ttu-id="09e0d-263">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-263">True</span></span>                            |
| <span data-ttu-id="09e0d-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="09e0d-264">Is Indexed</span></span>             | <span data-ttu-id="09e0d-265">否</span><span class="sxs-lookup"><span data-stu-id="09e0d-265">False</span></span>                           |
| <span data-ttu-id="09e0d-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="09e0d-266">In Global Catalog</span></span>      | <span data-ttu-id="09e0d-267">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-267">True</span></span>                            |
| <span data-ttu-id="09e0d-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="09e0d-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e0d-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="09e0d-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09e0d-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e0d-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09e0d-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e0d-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09e0d-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-272">Search-Flags</span></span>           | <span data-ttu-id="09e0d-273">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09e0d-273">0x00000008</span></span>                      |
| <span data-ttu-id="09e0d-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-274">System-Flags</span></span>           | <span data-ttu-id="09e0d-275">0x00000013</span><span class="sxs-lookup"><span data-stu-id="09e0d-275">0x00000013</span></span>                      |
| <span data-ttu-id="09e0d-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="09e0d-276">Classes used in</span></span>        | [<span data-ttu-id="09e0d-277">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="09e0d-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="09e0d-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09e0d-278">Windows Server 2012</span></span>



| <span data-ttu-id="09e0d-279">進入</span><span class="sxs-lookup"><span data-stu-id="09e0d-279">Entry</span></span> | <span data-ttu-id="09e0d-280">值</span><span class="sxs-lookup"><span data-stu-id="09e0d-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09e0d-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="09e0d-281">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09e0d-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09e0d-282">MAPI-Id</span></span>                | <span data-ttu-id="09e0d-283">0x803C</span><span class="sxs-lookup"><span data-stu-id="09e0d-283">0x803C</span></span>                          |
| <span data-ttu-id="09e0d-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="09e0d-284">System-Only</span></span>            | <span data-ttu-id="09e0d-285">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-285">True</span></span>                            |
| <span data-ttu-id="09e0d-286">是-單一值</span><span class="sxs-lookup"><span data-stu-id="09e0d-286">Is-Single-Valued</span></span>       | <span data-ttu-id="09e0d-287">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-287">True</span></span>                            |
| <span data-ttu-id="09e0d-288">已編制索引</span><span class="sxs-lookup"><span data-stu-id="09e0d-288">Is Indexed</span></span>             | <span data-ttu-id="09e0d-289">否</span><span class="sxs-lookup"><span data-stu-id="09e0d-289">False</span></span>                           |
| <span data-ttu-id="09e0d-290">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="09e0d-290">In Global Catalog</span></span>      | <span data-ttu-id="09e0d-291">對</span><span class="sxs-lookup"><span data-stu-id="09e0d-291">True</span></span>                            |
| <span data-ttu-id="09e0d-292">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="09e0d-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="09e0d-293">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="09e0d-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09e0d-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09e0d-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09e0d-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09e0d-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09e0d-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-296">Search-Flags</span></span>           | <span data-ttu-id="09e0d-297">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09e0d-297">0x00000008</span></span>                      |
| <span data-ttu-id="09e0d-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09e0d-298">System-Flags</span></span>           | <span data-ttu-id="09e0d-299">0x00000013</span><span class="sxs-lookup"><span data-stu-id="09e0d-299">0x00000013</span></span>                      |
| <span data-ttu-id="09e0d-300">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="09e0d-300">Classes used in</span></span>        | [<span data-ttu-id="09e0d-301">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="09e0d-301">**Top**</span></span>](c-top.md)<br/> |



 

 






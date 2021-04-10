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
# <a name="obj-dist-name-attribute"></a><span data-ttu-id="9f9f2-106">Obj-Dist-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="9f9f2-106">Obj-Dist-Name attribute</span></span>

<span data-ttu-id="9f9f2-107">與物件的辨別名稱相同。</span><span class="sxs-lookup"><span data-stu-id="9f9f2-107">Same as the Distinguished Name for an object.</span></span> <span data-ttu-id="9f9f2-108">供 Exchange 使用。</span><span class="sxs-lookup"><span data-stu-id="9f9f2-108">Used by Exchange.</span></span>



| <span data-ttu-id="9f9f2-109">進入</span><span class="sxs-lookup"><span data-stu-id="9f9f2-109">Entry</span></span> | <span data-ttu-id="9f9f2-110">值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="9f9f2-111">CN</span><span class="sxs-lookup"><span data-stu-id="9f9f2-111">CN</span></span>                | <span data-ttu-id="9f9f2-112">Obj-Dist 名稱</span><span class="sxs-lookup"><span data-stu-id="9f9f2-112">Obj-Dist-Name</span></span>                           |
| <span data-ttu-id="9f9f2-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9f9f2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9f9f2-114">distinguishedName</span><span class="sxs-lookup"><span data-stu-id="9f9f2-114">distinguishedName</span></span>                       |
| <span data-ttu-id="9f9f2-115">大小</span><span class="sxs-lookup"><span data-stu-id="9f9f2-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="9f9f2-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9f9f2-116">Update Privilege</span></span>  | <span data-ttu-id="9f9f2-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="9f9f2-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="9f9f2-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9f9f2-118">Update Frequency</span></span>  | <span data-ttu-id="9f9f2-119">每次建立或移動物件時。</span><span class="sxs-lookup"><span data-stu-id="9f9f2-119">Whenever an object is created or moved.</span></span> |
| <span data-ttu-id="9f9f2-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9f9f2-120">Attribute-Id</span></span>      | <span data-ttu-id="9f9f2-121">2.5.4.49</span><span class="sxs-lookup"><span data-stu-id="9f9f2-121">2.5.4.49</span></span>                                |
| <span data-ttu-id="9f9f2-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9f9f2-122">System-Id-Guid</span></span>    | <span data-ttu-id="9f9f2-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9f9f2-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="9f9f2-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f9f2-124">Syntax</span></span>            | [<span data-ttu-id="9f9f2-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="9f9f2-126">實作</span><span class="sxs-lookup"><span data-stu-id="9f9f2-126">Implementations</span></span>

-   [<span data-ttu-id="9f9f2-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9f9f2-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9f9f2-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9f9f2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9f9f2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9f9f2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9f9f2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9f9f2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f9f2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="9f9f2-135">進入</span><span class="sxs-lookup"><span data-stu-id="9f9f2-135">Entry</span></span> | <span data-ttu-id="9f9f2-136">值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f9f2-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f9f2-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f9f2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9f2-138">MAPI-Id</span></span>                | <span data-ttu-id="9f9f2-139">0x803C</span><span class="sxs-lookup"><span data-stu-id="9f9f2-139">0x803C</span></span>                          |
| <span data-ttu-id="9f9f2-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9f2-140">System-Only</span></span>            | <span data-ttu-id="9f9f2-141">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-141">True</span></span>                            |
| <span data-ttu-id="9f9f2-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-142">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9f2-143">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-143">True</span></span>                            |
| <span data-ttu-id="9f9f2-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f9f2-144">Is Indexed</span></span>             | <span data-ttu-id="9f9f2-145">否</span><span class="sxs-lookup"><span data-stu-id="9f9f2-145">False</span></span>                           |
| <span data-ttu-id="9f9f2-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f9f2-146">In Global Catalog</span></span>      | <span data-ttu-id="9f9f2-147">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-147">True</span></span>                            |
| <span data-ttu-id="9f9f2-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f9f2-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9f2-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f9f2-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f9f2-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9f2-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9f2-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-152">Search-Flags</span></span>           | <span data-ttu-id="9f9f2-153">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9f9f2-153">0x00000008</span></span>                      |
| <span data-ttu-id="9f9f2-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-154">System-Flags</span></span>           | <span data-ttu-id="9f9f2-155">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f9f2-155">0x00000013</span></span>                      |
| <span data-ttu-id="9f9f2-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f9f2-156">Classes used in</span></span>        | [<span data-ttu-id="9f9f2-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9f9f2-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f9f2-158">Windows Server 2003</span></span>



| <span data-ttu-id="9f9f2-159">進入</span><span class="sxs-lookup"><span data-stu-id="9f9f2-159">Entry</span></span> | <span data-ttu-id="9f9f2-160">值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f9f2-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f9f2-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f9f2-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9f2-162">MAPI-Id</span></span>                | <span data-ttu-id="9f9f2-163">0x803C</span><span class="sxs-lookup"><span data-stu-id="9f9f2-163">0x803C</span></span>                          |
| <span data-ttu-id="9f9f2-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9f2-164">System-Only</span></span>            | <span data-ttu-id="9f9f2-165">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-165">True</span></span>                            |
| <span data-ttu-id="9f9f2-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-166">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9f2-167">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-167">True</span></span>                            |
| <span data-ttu-id="9f9f2-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f9f2-168">Is Indexed</span></span>             | <span data-ttu-id="9f9f2-169">否</span><span class="sxs-lookup"><span data-stu-id="9f9f2-169">False</span></span>                           |
| <span data-ttu-id="9f9f2-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f9f2-170">In Global Catalog</span></span>      | <span data-ttu-id="9f9f2-171">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-171">True</span></span>                            |
| <span data-ttu-id="9f9f2-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f9f2-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9f2-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f9f2-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f9f2-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9f2-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9f2-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-176">Search-Flags</span></span>           | <span data-ttu-id="9f9f2-177">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9f9f2-177">0x00000008</span></span>                      |
| <span data-ttu-id="9f9f2-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-178">System-Flags</span></span>           | <span data-ttu-id="9f9f2-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f9f2-179">0x00000013</span></span>                      |
| <span data-ttu-id="9f9f2-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f9f2-180">Classes used in</span></span>        | [<span data-ttu-id="9f9f2-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9f9f2-182">亞當</span><span class="sxs-lookup"><span data-stu-id="9f9f2-182">ADAM</span></span>



| <span data-ttu-id="9f9f2-183">進入</span><span class="sxs-lookup"><span data-stu-id="9f9f2-183">Entry</span></span> | <span data-ttu-id="9f9f2-184">值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f9f2-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f9f2-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f9f2-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9f2-186">MAPI-Id</span></span>                | <span data-ttu-id="9f9f2-187">0x803C</span><span class="sxs-lookup"><span data-stu-id="9f9f2-187">0x803C</span></span>                          |
| <span data-ttu-id="9f9f2-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9f2-188">System-Only</span></span>            | <span data-ttu-id="9f9f2-189">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-189">True</span></span>                            |
| <span data-ttu-id="9f9f2-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-190">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9f2-191">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-191">True</span></span>                            |
| <span data-ttu-id="9f9f2-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f9f2-192">Is Indexed</span></span>             | <span data-ttu-id="9f9f2-193">否</span><span class="sxs-lookup"><span data-stu-id="9f9f2-193">False</span></span>                           |
| <span data-ttu-id="9f9f2-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f9f2-194">In Global Catalog</span></span>      | <span data-ttu-id="9f9f2-195">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-195">True</span></span>                            |
| <span data-ttu-id="9f9f2-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f9f2-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9f2-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f9f2-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f9f2-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9f2-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9f2-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-200">Search-Flags</span></span>           | <span data-ttu-id="9f9f2-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9f9f2-201">0x00000008</span></span>                      |
| <span data-ttu-id="9f9f2-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-202">System-Flags</span></span>           | <span data-ttu-id="9f9f2-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f9f2-203">0x00000013</span></span>                      |
| <span data-ttu-id="9f9f2-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f9f2-204">Classes used in</span></span>        | [<span data-ttu-id="9f9f2-205">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9f9f2-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9f9f2-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9f9f2-207">進入</span><span class="sxs-lookup"><span data-stu-id="9f9f2-207">Entry</span></span> | <span data-ttu-id="9f9f2-208">值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f9f2-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f9f2-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f9f2-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9f2-210">MAPI-Id</span></span>                | <span data-ttu-id="9f9f2-211">0x803C</span><span class="sxs-lookup"><span data-stu-id="9f9f2-211">0x803C</span></span>                          |
| <span data-ttu-id="9f9f2-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9f2-212">System-Only</span></span>            | <span data-ttu-id="9f9f2-213">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-213">True</span></span>                            |
| <span data-ttu-id="9f9f2-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-214">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9f2-215">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-215">True</span></span>                            |
| <span data-ttu-id="9f9f2-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f9f2-216">Is Indexed</span></span>             | <span data-ttu-id="9f9f2-217">否</span><span class="sxs-lookup"><span data-stu-id="9f9f2-217">False</span></span>                           |
| <span data-ttu-id="9f9f2-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f9f2-218">In Global Catalog</span></span>      | <span data-ttu-id="9f9f2-219">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-219">True</span></span>                            |
| <span data-ttu-id="9f9f2-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f9f2-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9f2-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f9f2-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f9f2-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9f2-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9f2-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-224">Search-Flags</span></span>           | <span data-ttu-id="9f9f2-225">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9f9f2-225">0x00000008</span></span>                      |
| <span data-ttu-id="9f9f2-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-226">System-Flags</span></span>           | <span data-ttu-id="9f9f2-227">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f9f2-227">0x00000013</span></span>                      |
| <span data-ttu-id="9f9f2-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f9f2-228">Classes used in</span></span>        | [<span data-ttu-id="9f9f2-229">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9f9f2-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f9f2-230">Windows Server 2008</span></span>



| <span data-ttu-id="9f9f2-231">進入</span><span class="sxs-lookup"><span data-stu-id="9f9f2-231">Entry</span></span> | <span data-ttu-id="9f9f2-232">值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f9f2-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f9f2-233">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f9f2-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9f2-234">MAPI-Id</span></span>                | <span data-ttu-id="9f9f2-235">0x803C</span><span class="sxs-lookup"><span data-stu-id="9f9f2-235">0x803C</span></span>                          |
| <span data-ttu-id="9f9f2-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9f2-236">System-Only</span></span>            | <span data-ttu-id="9f9f2-237">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-237">True</span></span>                            |
| <span data-ttu-id="9f9f2-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-238">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9f2-239">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-239">True</span></span>                            |
| <span data-ttu-id="9f9f2-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f9f2-240">Is Indexed</span></span>             | <span data-ttu-id="9f9f2-241">否</span><span class="sxs-lookup"><span data-stu-id="9f9f2-241">False</span></span>                           |
| <span data-ttu-id="9f9f2-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f9f2-242">In Global Catalog</span></span>      | <span data-ttu-id="9f9f2-243">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-243">True</span></span>                            |
| <span data-ttu-id="9f9f2-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f9f2-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9f2-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f9f2-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f9f2-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9f2-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9f2-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-248">Search-Flags</span></span>           | <span data-ttu-id="9f9f2-249">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9f9f2-249">0x00000008</span></span>                      |
| <span data-ttu-id="9f9f2-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-250">System-Flags</span></span>           | <span data-ttu-id="9f9f2-251">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f9f2-251">0x00000013</span></span>                      |
| <span data-ttu-id="9f9f2-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f9f2-252">Classes used in</span></span>        | [<span data-ttu-id="9f9f2-253">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9f9f2-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f9f2-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9f9f2-255">進入</span><span class="sxs-lookup"><span data-stu-id="9f9f2-255">Entry</span></span> | <span data-ttu-id="9f9f2-256">值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f9f2-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f9f2-257">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f9f2-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9f2-258">MAPI-Id</span></span>                | <span data-ttu-id="9f9f2-259">0x803C</span><span class="sxs-lookup"><span data-stu-id="9f9f2-259">0x803C</span></span>                          |
| <span data-ttu-id="9f9f2-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9f2-260">System-Only</span></span>            | <span data-ttu-id="9f9f2-261">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-261">True</span></span>                            |
| <span data-ttu-id="9f9f2-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-262">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9f2-263">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-263">True</span></span>                            |
| <span data-ttu-id="9f9f2-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f9f2-264">Is Indexed</span></span>             | <span data-ttu-id="9f9f2-265">否</span><span class="sxs-lookup"><span data-stu-id="9f9f2-265">False</span></span>                           |
| <span data-ttu-id="9f9f2-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f9f2-266">In Global Catalog</span></span>      | <span data-ttu-id="9f9f2-267">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-267">True</span></span>                            |
| <span data-ttu-id="9f9f2-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f9f2-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9f2-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f9f2-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f9f2-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9f2-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9f2-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-272">Search-Flags</span></span>           | <span data-ttu-id="9f9f2-273">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9f9f2-273">0x00000008</span></span>                      |
| <span data-ttu-id="9f9f2-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-274">System-Flags</span></span>           | <span data-ttu-id="9f9f2-275">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f9f2-275">0x00000013</span></span>                      |
| <span data-ttu-id="9f9f2-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f9f2-276">Classes used in</span></span>        | [<span data-ttu-id="9f9f2-277">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9f9f2-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f9f2-278">Windows Server 2012</span></span>



| <span data-ttu-id="9f9f2-279">進入</span><span class="sxs-lookup"><span data-stu-id="9f9f2-279">Entry</span></span> | <span data-ttu-id="9f9f2-280">值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f9f2-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f9f2-281">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f9f2-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9f2-282">MAPI-Id</span></span>                | <span data-ttu-id="9f9f2-283">0x803C</span><span class="sxs-lookup"><span data-stu-id="9f9f2-283">0x803C</span></span>                          |
| <span data-ttu-id="9f9f2-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9f2-284">System-Only</span></span>            | <span data-ttu-id="9f9f2-285">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-285">True</span></span>                            |
| <span data-ttu-id="9f9f2-286">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f9f2-286">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9f2-287">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-287">True</span></span>                            |
| <span data-ttu-id="9f9f2-288">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f9f2-288">Is Indexed</span></span>             | <span data-ttu-id="9f9f2-289">否</span><span class="sxs-lookup"><span data-stu-id="9f9f2-289">False</span></span>                           |
| <span data-ttu-id="9f9f2-290">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f9f2-290">In Global Catalog</span></span>      | <span data-ttu-id="9f9f2-291">對</span><span class="sxs-lookup"><span data-stu-id="9f9f2-291">True</span></span>                            |
| <span data-ttu-id="9f9f2-292">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f9f2-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9f2-293">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f9f2-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f9f2-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9f2-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9f2-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f9f2-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-296">Search-Flags</span></span>           | <span data-ttu-id="9f9f2-297">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9f9f2-297">0x00000008</span></span>                      |
| <span data-ttu-id="9f9f2-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9f2-298">System-Flags</span></span>           | <span data-ttu-id="9f9f2-299">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f9f2-299">0x00000013</span></span>                      |
| <span data-ttu-id="9f9f2-300">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f9f2-300">Classes used in</span></span>        | [<span data-ttu-id="9f9f2-301">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f9f2-301">**Top**</span></span>](c-top.md)<br/> |



 

 






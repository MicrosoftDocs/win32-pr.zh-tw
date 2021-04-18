---
title: Proxy-物件名稱屬性
description: 這個屬性是由 Active Directory 在內部使用，以協助追蹤有域移動的移動。
ms.assetid: 661ea322-f78c-44dc-8d64-4f28ead1a7aa
ms.tgt_platform: multiple
keywords:
- Proxy-物件名稱屬性 AD 架構
- proxiedObjectName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Proxied-Object-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ffafbbea411c950954102a788226c29589029e1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106965545"
---
# <a name="proxied-object-name-attribute"></a><span data-ttu-id="95b50-105">Proxy-物件名稱屬性</span><span class="sxs-lookup"><span data-stu-id="95b50-105">Proxied-Object-Name attribute</span></span>

<span data-ttu-id="95b50-106">這個屬性是由 Active Directory 在內部使用，以協助追蹤有域移動的移動。</span><span class="sxs-lookup"><span data-stu-id="95b50-106">This attribute is used internally by Active Directory to help track interdomain moves.</span></span>



| <span data-ttu-id="95b50-107">進入</span><span class="sxs-lookup"><span data-stu-id="95b50-107">Entry</span></span> | <span data-ttu-id="95b50-108">值</span><span class="sxs-lookup"><span data-stu-id="95b50-108">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="95b50-109">CN</span><span class="sxs-lookup"><span data-stu-id="95b50-109">CN</span></span>                | <span data-ttu-id="95b50-110">Proxy-物件名稱</span><span class="sxs-lookup"><span data-stu-id="95b50-110">Proxied-Object-Name</span></span>                             |
| <span data-ttu-id="95b50-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="95b50-111">Ldap-Display-Name</span></span> | <span data-ttu-id="95b50-112">proxiedObjectName</span><span class="sxs-lookup"><span data-stu-id="95b50-112">proxiedObjectName</span></span>                               |
| <span data-ttu-id="95b50-113">大小</span><span class="sxs-lookup"><span data-stu-id="95b50-113">Size</span></span>              | \-                                              |
| <span data-ttu-id="95b50-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="95b50-114">Update Privilege</span></span>  | <span data-ttu-id="95b50-115">系統會使用此方法。</span><span class="sxs-lookup"><span data-stu-id="95b50-115">This is used by the system.</span></span>                     |
| <span data-ttu-id="95b50-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="95b50-116">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="95b50-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="95b50-117">Attribute-Id</span></span>      | <span data-ttu-id="95b50-118">1.2.840.113556.1.4.1249</span><span class="sxs-lookup"><span data-stu-id="95b50-118">1.2.840.113556.1.4.1249</span></span>                         |
| <span data-ttu-id="95b50-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="95b50-119">System-Id-Guid</span></span>    | <span data-ttu-id="95b50-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="95b50-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span></span>            |
| <span data-ttu-id="95b50-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="95b50-121">Syntax</span></span>            | [<span data-ttu-id="95b50-122">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="95b50-122">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="95b50-123">實作</span><span class="sxs-lookup"><span data-stu-id="95b50-123">Implementations</span></span>

-   [<span data-ttu-id="95b50-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="95b50-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="95b50-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="95b50-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="95b50-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="95b50-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="95b50-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="95b50-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="95b50-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="95b50-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="95b50-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="95b50-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="95b50-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="95b50-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="95b50-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="95b50-131">Windows 2000 Server</span></span>



| <span data-ttu-id="95b50-132">進入</span><span class="sxs-lookup"><span data-stu-id="95b50-132">Entry</span></span> | <span data-ttu-id="95b50-133">值</span><span class="sxs-lookup"><span data-stu-id="95b50-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="95b50-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95b50-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95b50-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="95b50-136">System-Only</span></span>            | <span data-ttu-id="95b50-137">對</span><span class="sxs-lookup"><span data-stu-id="95b50-137">True</span></span>                            |
| <span data-ttu-id="95b50-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95b50-138">Is-Single-Valued</span></span>       | <span data-ttu-id="95b50-139">對</span><span class="sxs-lookup"><span data-stu-id="95b50-139">True</span></span>                            |
| <span data-ttu-id="95b50-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95b50-140">Is Indexed</span></span>             | <span data-ttu-id="95b50-141">否</span><span class="sxs-lookup"><span data-stu-id="95b50-141">False</span></span>                           |
| <span data-ttu-id="95b50-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95b50-142">In Global Catalog</span></span>      | <span data-ttu-id="95b50-143">對</span><span class="sxs-lookup"><span data-stu-id="95b50-143">True</span></span>                            |
| <span data-ttu-id="95b50-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95b50-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="95b50-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95b50-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="95b50-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95b50-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="95b50-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95b50-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="95b50-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-148">Search-Flags</span></span>           | <span data-ttu-id="95b50-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95b50-149">0x00000000</span></span>                      |
| <span data-ttu-id="95b50-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-150">System-Flags</span></span>           | <span data-ttu-id="95b50-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="95b50-151">0x00000012</span></span>                      |
| <span data-ttu-id="95b50-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95b50-152">Classes used in</span></span>        | [<span data-ttu-id="95b50-153">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="95b50-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="95b50-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="95b50-154">Windows Server 2003</span></span>



| <span data-ttu-id="95b50-155">進入</span><span class="sxs-lookup"><span data-stu-id="95b50-155">Entry</span></span> | <span data-ttu-id="95b50-156">值</span><span class="sxs-lookup"><span data-stu-id="95b50-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="95b50-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95b50-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95b50-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="95b50-159">System-Only</span></span>            | <span data-ttu-id="95b50-160">對</span><span class="sxs-lookup"><span data-stu-id="95b50-160">True</span></span>                            |
| <span data-ttu-id="95b50-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95b50-161">Is-Single-Valued</span></span>       | <span data-ttu-id="95b50-162">對</span><span class="sxs-lookup"><span data-stu-id="95b50-162">True</span></span>                            |
| <span data-ttu-id="95b50-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95b50-163">Is Indexed</span></span>             | <span data-ttu-id="95b50-164">否</span><span class="sxs-lookup"><span data-stu-id="95b50-164">False</span></span>                           |
| <span data-ttu-id="95b50-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95b50-165">In Global Catalog</span></span>      | <span data-ttu-id="95b50-166">對</span><span class="sxs-lookup"><span data-stu-id="95b50-166">True</span></span>                            |
| <span data-ttu-id="95b50-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95b50-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="95b50-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95b50-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="95b50-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95b50-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="95b50-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95b50-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="95b50-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-171">Search-Flags</span></span>           | <span data-ttu-id="95b50-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95b50-172">0x00000000</span></span>                      |
| <span data-ttu-id="95b50-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-173">System-Flags</span></span>           | <span data-ttu-id="95b50-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="95b50-174">0x00000012</span></span>                      |
| <span data-ttu-id="95b50-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95b50-175">Classes used in</span></span>        | [<span data-ttu-id="95b50-176">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="95b50-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="95b50-177">亞當</span><span class="sxs-lookup"><span data-stu-id="95b50-177">ADAM</span></span>



| <span data-ttu-id="95b50-178">進入</span><span class="sxs-lookup"><span data-stu-id="95b50-178">Entry</span></span> | <span data-ttu-id="95b50-179">值</span><span class="sxs-lookup"><span data-stu-id="95b50-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="95b50-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95b50-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95b50-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="95b50-182">System-Only</span></span>            | <span data-ttu-id="95b50-183">對</span><span class="sxs-lookup"><span data-stu-id="95b50-183">True</span></span>                            |
| <span data-ttu-id="95b50-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95b50-184">Is-Single-Valued</span></span>       | <span data-ttu-id="95b50-185">對</span><span class="sxs-lookup"><span data-stu-id="95b50-185">True</span></span>                            |
| <span data-ttu-id="95b50-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95b50-186">Is Indexed</span></span>             | <span data-ttu-id="95b50-187">否</span><span class="sxs-lookup"><span data-stu-id="95b50-187">False</span></span>                           |
| <span data-ttu-id="95b50-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95b50-188">In Global Catalog</span></span>      | <span data-ttu-id="95b50-189">對</span><span class="sxs-lookup"><span data-stu-id="95b50-189">True</span></span>                            |
| <span data-ttu-id="95b50-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95b50-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="95b50-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95b50-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="95b50-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95b50-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="95b50-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95b50-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="95b50-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-194">Search-Flags</span></span>           | <span data-ttu-id="95b50-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95b50-195">0x00000000</span></span>                      |
| <span data-ttu-id="95b50-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-196">System-Flags</span></span>           | <span data-ttu-id="95b50-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="95b50-197">0x00000012</span></span>                      |
| <span data-ttu-id="95b50-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95b50-198">Classes used in</span></span>        | [<span data-ttu-id="95b50-199">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="95b50-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="95b50-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="95b50-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="95b50-201">進入</span><span class="sxs-lookup"><span data-stu-id="95b50-201">Entry</span></span> | <span data-ttu-id="95b50-202">值</span><span class="sxs-lookup"><span data-stu-id="95b50-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="95b50-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95b50-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95b50-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="95b50-205">System-Only</span></span>            | <span data-ttu-id="95b50-206">對</span><span class="sxs-lookup"><span data-stu-id="95b50-206">True</span></span>                            |
| <span data-ttu-id="95b50-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95b50-207">Is-Single-Valued</span></span>       | <span data-ttu-id="95b50-208">對</span><span class="sxs-lookup"><span data-stu-id="95b50-208">True</span></span>                            |
| <span data-ttu-id="95b50-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95b50-209">Is Indexed</span></span>             | <span data-ttu-id="95b50-210">否</span><span class="sxs-lookup"><span data-stu-id="95b50-210">False</span></span>                           |
| <span data-ttu-id="95b50-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95b50-211">In Global Catalog</span></span>      | <span data-ttu-id="95b50-212">對</span><span class="sxs-lookup"><span data-stu-id="95b50-212">True</span></span>                            |
| <span data-ttu-id="95b50-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95b50-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="95b50-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95b50-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="95b50-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95b50-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="95b50-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95b50-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="95b50-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-217">Search-Flags</span></span>           | <span data-ttu-id="95b50-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95b50-218">0x00000000</span></span>                      |
| <span data-ttu-id="95b50-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-219">System-Flags</span></span>           | <span data-ttu-id="95b50-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="95b50-220">0x00000012</span></span>                      |
| <span data-ttu-id="95b50-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95b50-221">Classes used in</span></span>        | [<span data-ttu-id="95b50-222">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="95b50-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="95b50-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95b50-223">Windows Server 2008</span></span>



| <span data-ttu-id="95b50-224">進入</span><span class="sxs-lookup"><span data-stu-id="95b50-224">Entry</span></span> | <span data-ttu-id="95b50-225">值</span><span class="sxs-lookup"><span data-stu-id="95b50-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="95b50-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95b50-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95b50-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="95b50-228">System-Only</span></span>            | <span data-ttu-id="95b50-229">對</span><span class="sxs-lookup"><span data-stu-id="95b50-229">True</span></span>                            |
| <span data-ttu-id="95b50-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95b50-230">Is-Single-Valued</span></span>       | <span data-ttu-id="95b50-231">對</span><span class="sxs-lookup"><span data-stu-id="95b50-231">True</span></span>                            |
| <span data-ttu-id="95b50-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95b50-232">Is Indexed</span></span>             | <span data-ttu-id="95b50-233">否</span><span class="sxs-lookup"><span data-stu-id="95b50-233">False</span></span>                           |
| <span data-ttu-id="95b50-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95b50-234">In Global Catalog</span></span>      | <span data-ttu-id="95b50-235">對</span><span class="sxs-lookup"><span data-stu-id="95b50-235">True</span></span>                            |
| <span data-ttu-id="95b50-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95b50-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="95b50-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95b50-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="95b50-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95b50-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="95b50-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95b50-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="95b50-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-240">Search-Flags</span></span>           | <span data-ttu-id="95b50-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95b50-241">0x00000000</span></span>                      |
| <span data-ttu-id="95b50-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-242">System-Flags</span></span>           | <span data-ttu-id="95b50-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="95b50-243">0x00000012</span></span>                      |
| <span data-ttu-id="95b50-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95b50-244">Classes used in</span></span>        | [<span data-ttu-id="95b50-245">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="95b50-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="95b50-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="95b50-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="95b50-247">進入</span><span class="sxs-lookup"><span data-stu-id="95b50-247">Entry</span></span> | <span data-ttu-id="95b50-248">值</span><span class="sxs-lookup"><span data-stu-id="95b50-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="95b50-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95b50-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95b50-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="95b50-251">System-Only</span></span>            | <span data-ttu-id="95b50-252">對</span><span class="sxs-lookup"><span data-stu-id="95b50-252">True</span></span>                            |
| <span data-ttu-id="95b50-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95b50-253">Is-Single-Valued</span></span>       | <span data-ttu-id="95b50-254">對</span><span class="sxs-lookup"><span data-stu-id="95b50-254">True</span></span>                            |
| <span data-ttu-id="95b50-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95b50-255">Is Indexed</span></span>             | <span data-ttu-id="95b50-256">否</span><span class="sxs-lookup"><span data-stu-id="95b50-256">False</span></span>                           |
| <span data-ttu-id="95b50-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95b50-257">In Global Catalog</span></span>      | <span data-ttu-id="95b50-258">對</span><span class="sxs-lookup"><span data-stu-id="95b50-258">True</span></span>                            |
| <span data-ttu-id="95b50-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95b50-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="95b50-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95b50-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="95b50-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95b50-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="95b50-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95b50-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="95b50-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-263">Search-Flags</span></span>           | <span data-ttu-id="95b50-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95b50-264">0x00000000</span></span>                      |
| <span data-ttu-id="95b50-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-265">System-Flags</span></span>           | <span data-ttu-id="95b50-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="95b50-266">0x00000012</span></span>                      |
| <span data-ttu-id="95b50-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95b50-267">Classes used in</span></span>        | [<span data-ttu-id="95b50-268">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="95b50-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="95b50-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95b50-269">Windows Server 2012</span></span>



| <span data-ttu-id="95b50-270">進入</span><span class="sxs-lookup"><span data-stu-id="95b50-270">Entry</span></span> | <span data-ttu-id="95b50-271">值</span><span class="sxs-lookup"><span data-stu-id="95b50-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="95b50-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95b50-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95b50-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="95b50-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="95b50-274">System-Only</span></span>            | <span data-ttu-id="95b50-275">對</span><span class="sxs-lookup"><span data-stu-id="95b50-275">True</span></span>                            |
| <span data-ttu-id="95b50-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95b50-276">Is-Single-Valued</span></span>       | <span data-ttu-id="95b50-277">對</span><span class="sxs-lookup"><span data-stu-id="95b50-277">True</span></span>                            |
| <span data-ttu-id="95b50-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95b50-278">Is Indexed</span></span>             | <span data-ttu-id="95b50-279">否</span><span class="sxs-lookup"><span data-stu-id="95b50-279">False</span></span>                           |
| <span data-ttu-id="95b50-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95b50-280">In Global Catalog</span></span>      | <span data-ttu-id="95b50-281">對</span><span class="sxs-lookup"><span data-stu-id="95b50-281">True</span></span>                            |
| <span data-ttu-id="95b50-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95b50-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="95b50-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95b50-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="95b50-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95b50-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="95b50-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95b50-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="95b50-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-286">Search-Flags</span></span>           | <span data-ttu-id="95b50-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95b50-287">0x00000000</span></span>                      |
| <span data-ttu-id="95b50-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95b50-288">System-Flags</span></span>           | <span data-ttu-id="95b50-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="95b50-289">0x00000012</span></span>                      |
| <span data-ttu-id="95b50-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95b50-290">Classes used in</span></span>        | [<span data-ttu-id="95b50-291">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="95b50-291">**Top**</span></span>](c-top.md)<br/> |



 

 






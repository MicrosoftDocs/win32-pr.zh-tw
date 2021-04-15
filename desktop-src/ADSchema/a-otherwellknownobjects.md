---
title: 其他知名物件屬性
description: 包含依 GUID 和辨別名稱的容器清單。 這可讓您只使用 GUID 和功能變數名稱來移動物件。 只要移動物件，系統就會自動更新分辨名稱。
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- 其他知名物件的屬性 AD 架構
- otherWellKnownObjects 屬性 AD 架構
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467328"
---
# <a name="other-well-known-objects-attribute"></a><span data-ttu-id="ccd71-107">其他知名物件屬性</span><span class="sxs-lookup"><span data-stu-id="ccd71-107">Other-Well-Known-Objects attribute</span></span>

<span data-ttu-id="ccd71-108">包含依 GUID 和辨別名稱的容器清單。</span><span class="sxs-lookup"><span data-stu-id="ccd71-108">Contains a list of containers by GUID and Distinguished Name.</span></span> <span data-ttu-id="ccd71-109">這可讓您只使用 GUID 和功能變數名稱來移動物件。</span><span class="sxs-lookup"><span data-stu-id="ccd71-109">This permits retrieving an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="ccd71-110">只要移動物件，系統就會自動更新分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="ccd71-110">Whenever the object is moved, the system automatically updates the Distinguished Name.</span></span>



| <span data-ttu-id="ccd71-111">進入</span><span class="sxs-lookup"><span data-stu-id="ccd71-111">Entry</span></span> | <span data-ttu-id="ccd71-112">值</span><span class="sxs-lookup"><span data-stu-id="ccd71-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd71-113">CN</span><span class="sxs-lookup"><span data-stu-id="ccd71-113">CN</span></span>                | <span data-ttu-id="ccd71-114">其他知名物件</span><span class="sxs-lookup"><span data-stu-id="ccd71-114">Other-Well-Known-Objects</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="ccd71-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ccd71-115">Ldap-Display-Name</span></span> | <span data-ttu-id="ccd71-116">otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="ccd71-116">otherWellKnownObjects</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="ccd71-117">大小</span><span class="sxs-lookup"><span data-stu-id="ccd71-117">Size</span></span>              | <span data-ttu-id="ccd71-118">用來在 microsoft 網域中取出使用者容器的範例： LDAP:// (WKGUID = a9d1ca15768811d1aded00c04fd8d5cd，dc = microsoft，dc = com) 。</span><span class="sxs-lookup"><span data-stu-id="ccd71-118">Sample for retrieving the Users container in the microsoft domain: LDAP://(WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=microsoft,dc=com).</span></span> <span data-ttu-id="ccd71-119">注意：以括弧取代角括弧，以避免 XML 衝突。</span><span class="sxs-lookup"><span data-stu-id="ccd71-119">NOTE: Angle brackets replaced by parentheses to avoid XML conflicts.</span></span> |
| <span data-ttu-id="ccd71-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ccd71-120">Update Privilege</span></span>  | <span data-ttu-id="ccd71-121">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="ccd71-121">Schema administrator</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="ccd71-122">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ccd71-122">Update Frequency</span></span>  | <span data-ttu-id="ccd71-123">每次移動物件時。</span><span class="sxs-lookup"><span data-stu-id="ccd71-123">Whenever the object is moved.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="ccd71-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ccd71-124">Attribute-Id</span></span>      | <span data-ttu-id="ccd71-125">1.2.840.113556.1.4.1359</span><span class="sxs-lookup"><span data-stu-id="ccd71-125">1.2.840.113556.1.4.1359</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="ccd71-126">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ccd71-126">System-Id-Guid</span></span>    | <span data-ttu-id="ccd71-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="ccd71-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span></span>                                                                                                                                                                          |
| <span data-ttu-id="ccd71-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccd71-128">Syntax</span></span>            | [<span data-ttu-id="ccd71-129">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="ccd71-129">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                               |



## <a name="implementations"></a><span data-ttu-id="ccd71-130">實作</span><span class="sxs-lookup"><span data-stu-id="ccd71-130">Implementations</span></span>

-   [<span data-ttu-id="ccd71-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ccd71-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ccd71-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ccd71-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ccd71-133">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ccd71-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ccd71-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ccd71-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ccd71-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ccd71-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ccd71-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ccd71-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ccd71-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ccd71-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ccd71-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ccd71-138">Windows 2000 Server</span></span>



| <span data-ttu-id="ccd71-139">進入</span><span class="sxs-lookup"><span data-stu-id="ccd71-139">Entry</span></span> | <span data-ttu-id="ccd71-140">值</span><span class="sxs-lookup"><span data-stu-id="ccd71-140">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ccd71-141">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ccd71-141">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ccd71-142">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="ccd71-143">System-Only</span></span>            | <span data-ttu-id="ccd71-144">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-144">False</span></span>                           |
| <span data-ttu-id="ccd71-145">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ccd71-145">Is-Single-Valued</span></span>       | <span data-ttu-id="ccd71-146">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-146">False</span></span>                           |
| <span data-ttu-id="ccd71-147">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ccd71-147">Is Indexed</span></span>             | <span data-ttu-id="ccd71-148">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-148">False</span></span>                           |
| <span data-ttu-id="ccd71-149">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ccd71-149">In Global Catalog</span></span>      | <span data-ttu-id="ccd71-150">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-150">False</span></span>                           |
| <span data-ttu-id="ccd71-151">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ccd71-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="ccd71-152">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ccd71-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ccd71-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ccd71-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ccd71-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ccd71-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ccd71-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-155">Search-Flags</span></span>           | <span data-ttu-id="ccd71-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ccd71-156">0x00000000</span></span>                      |
| <span data-ttu-id="ccd71-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-157">System-Flags</span></span>           | <span data-ttu-id="ccd71-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ccd71-158">0x00000010</span></span>                      |
| <span data-ttu-id="ccd71-159">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ccd71-159">Classes used in</span></span>        | [<span data-ttu-id="ccd71-160">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ccd71-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ccd71-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ccd71-161">Windows Server 2003</span></span>



| <span data-ttu-id="ccd71-162">進入</span><span class="sxs-lookup"><span data-stu-id="ccd71-162">Entry</span></span> | <span data-ttu-id="ccd71-163">值</span><span class="sxs-lookup"><span data-stu-id="ccd71-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ccd71-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ccd71-164">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ccd71-165">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="ccd71-166">System-Only</span></span>            | <span data-ttu-id="ccd71-167">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-167">False</span></span>                           |
| <span data-ttu-id="ccd71-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ccd71-168">Is-Single-Valued</span></span>       | <span data-ttu-id="ccd71-169">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-169">False</span></span>                           |
| <span data-ttu-id="ccd71-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ccd71-170">Is Indexed</span></span>             | <span data-ttu-id="ccd71-171">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-171">False</span></span>                           |
| <span data-ttu-id="ccd71-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ccd71-172">In Global Catalog</span></span>      | <span data-ttu-id="ccd71-173">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-173">False</span></span>                           |
| <span data-ttu-id="ccd71-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ccd71-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="ccd71-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ccd71-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ccd71-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ccd71-176">Range-Lower</span></span>            | <span data-ttu-id="ccd71-177">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-177">16</span></span>                              |
| <span data-ttu-id="ccd71-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ccd71-178">Range-Upper</span></span>            | <span data-ttu-id="ccd71-179">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-179">16</span></span>                              |
| <span data-ttu-id="ccd71-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-180">Search-Flags</span></span>           | <span data-ttu-id="ccd71-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ccd71-181">0x00000000</span></span>                      |
| <span data-ttu-id="ccd71-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-182">System-Flags</span></span>           | <span data-ttu-id="ccd71-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ccd71-183">0x00000010</span></span>                      |
| <span data-ttu-id="ccd71-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ccd71-184">Classes used in</span></span>        | [<span data-ttu-id="ccd71-185">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ccd71-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ccd71-186">亞當</span><span class="sxs-lookup"><span data-stu-id="ccd71-186">ADAM</span></span>



| <span data-ttu-id="ccd71-187">進入</span><span class="sxs-lookup"><span data-stu-id="ccd71-187">Entry</span></span> | <span data-ttu-id="ccd71-188">值</span><span class="sxs-lookup"><span data-stu-id="ccd71-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ccd71-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ccd71-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ccd71-190">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="ccd71-191">System-Only</span></span>            | <span data-ttu-id="ccd71-192">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-192">False</span></span>                           |
| <span data-ttu-id="ccd71-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ccd71-193">Is-Single-Valued</span></span>       | <span data-ttu-id="ccd71-194">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-194">False</span></span>                           |
| <span data-ttu-id="ccd71-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ccd71-195">Is Indexed</span></span>             | <span data-ttu-id="ccd71-196">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-196">False</span></span>                           |
| <span data-ttu-id="ccd71-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ccd71-197">In Global Catalog</span></span>      | <span data-ttu-id="ccd71-198">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-198">False</span></span>                           |
| <span data-ttu-id="ccd71-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ccd71-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="ccd71-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ccd71-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ccd71-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ccd71-201">Range-Lower</span></span>            | <span data-ttu-id="ccd71-202">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-202">16</span></span>                              |
| <span data-ttu-id="ccd71-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ccd71-203">Range-Upper</span></span>            | <span data-ttu-id="ccd71-204">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-204">16</span></span>                              |
| <span data-ttu-id="ccd71-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-205">Search-Flags</span></span>           | <span data-ttu-id="ccd71-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ccd71-206">0x00000000</span></span>                      |
| <span data-ttu-id="ccd71-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-207">System-Flags</span></span>           | <span data-ttu-id="ccd71-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ccd71-208">0x00000010</span></span>                      |
| <span data-ttu-id="ccd71-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ccd71-209">Classes used in</span></span>        | [<span data-ttu-id="ccd71-210">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ccd71-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ccd71-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ccd71-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ccd71-212">進入</span><span class="sxs-lookup"><span data-stu-id="ccd71-212">Entry</span></span> | <span data-ttu-id="ccd71-213">值</span><span class="sxs-lookup"><span data-stu-id="ccd71-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ccd71-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ccd71-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ccd71-215">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="ccd71-216">System-Only</span></span>            | <span data-ttu-id="ccd71-217">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-217">False</span></span>                           |
| <span data-ttu-id="ccd71-218">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ccd71-218">Is-Single-Valued</span></span>       | <span data-ttu-id="ccd71-219">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-219">False</span></span>                           |
| <span data-ttu-id="ccd71-220">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ccd71-220">Is Indexed</span></span>             | <span data-ttu-id="ccd71-221">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-221">False</span></span>                           |
| <span data-ttu-id="ccd71-222">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ccd71-222">In Global Catalog</span></span>      | <span data-ttu-id="ccd71-223">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-223">False</span></span>                           |
| <span data-ttu-id="ccd71-224">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ccd71-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="ccd71-225">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ccd71-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ccd71-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ccd71-226">Range-Lower</span></span>            | <span data-ttu-id="ccd71-227">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-227">16</span></span>                              |
| <span data-ttu-id="ccd71-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ccd71-228">Range-Upper</span></span>            | <span data-ttu-id="ccd71-229">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-229">16</span></span>                              |
| <span data-ttu-id="ccd71-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-230">Search-Flags</span></span>           | <span data-ttu-id="ccd71-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ccd71-231">0x00000000</span></span>                      |
| <span data-ttu-id="ccd71-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-232">System-Flags</span></span>           | <span data-ttu-id="ccd71-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ccd71-233">0x00000010</span></span>                      |
| <span data-ttu-id="ccd71-234">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ccd71-234">Classes used in</span></span>        | [<span data-ttu-id="ccd71-235">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ccd71-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ccd71-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccd71-236">Windows Server 2008</span></span>



| <span data-ttu-id="ccd71-237">進入</span><span class="sxs-lookup"><span data-stu-id="ccd71-237">Entry</span></span> | <span data-ttu-id="ccd71-238">值</span><span class="sxs-lookup"><span data-stu-id="ccd71-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ccd71-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ccd71-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ccd71-240">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="ccd71-241">System-Only</span></span>            | <span data-ttu-id="ccd71-242">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-242">False</span></span>                           |
| <span data-ttu-id="ccd71-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ccd71-243">Is-Single-Valued</span></span>       | <span data-ttu-id="ccd71-244">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-244">False</span></span>                           |
| <span data-ttu-id="ccd71-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ccd71-245">Is Indexed</span></span>             | <span data-ttu-id="ccd71-246">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-246">False</span></span>                           |
| <span data-ttu-id="ccd71-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ccd71-247">In Global Catalog</span></span>      | <span data-ttu-id="ccd71-248">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-248">False</span></span>                           |
| <span data-ttu-id="ccd71-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ccd71-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="ccd71-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ccd71-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ccd71-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ccd71-251">Range-Lower</span></span>            | <span data-ttu-id="ccd71-252">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-252">16</span></span>                              |
| <span data-ttu-id="ccd71-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ccd71-253">Range-Upper</span></span>            | <span data-ttu-id="ccd71-254">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-254">16</span></span>                              |
| <span data-ttu-id="ccd71-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-255">Search-Flags</span></span>           | <span data-ttu-id="ccd71-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ccd71-256">0x00000000</span></span>                      |
| <span data-ttu-id="ccd71-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-257">System-Flags</span></span>           | <span data-ttu-id="ccd71-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ccd71-258">0x00000010</span></span>                      |
| <span data-ttu-id="ccd71-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ccd71-259">Classes used in</span></span>        | [<span data-ttu-id="ccd71-260">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ccd71-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ccd71-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ccd71-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ccd71-262">進入</span><span class="sxs-lookup"><span data-stu-id="ccd71-262">Entry</span></span> | <span data-ttu-id="ccd71-263">值</span><span class="sxs-lookup"><span data-stu-id="ccd71-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ccd71-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ccd71-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ccd71-265">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="ccd71-266">System-Only</span></span>            | <span data-ttu-id="ccd71-267">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-267">False</span></span>                           |
| <span data-ttu-id="ccd71-268">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ccd71-268">Is-Single-Valued</span></span>       | <span data-ttu-id="ccd71-269">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-269">False</span></span>                           |
| <span data-ttu-id="ccd71-270">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ccd71-270">Is Indexed</span></span>             | <span data-ttu-id="ccd71-271">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-271">False</span></span>                           |
| <span data-ttu-id="ccd71-272">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ccd71-272">In Global Catalog</span></span>      | <span data-ttu-id="ccd71-273">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-273">False</span></span>                           |
| <span data-ttu-id="ccd71-274">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ccd71-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="ccd71-275">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ccd71-275">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ccd71-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ccd71-276">Range-Lower</span></span>            | <span data-ttu-id="ccd71-277">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-277">16</span></span>                              |
| <span data-ttu-id="ccd71-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ccd71-278">Range-Upper</span></span>            | <span data-ttu-id="ccd71-279">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-279">16</span></span>                              |
| <span data-ttu-id="ccd71-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-280">Search-Flags</span></span>           | <span data-ttu-id="ccd71-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ccd71-281">0x00000000</span></span>                      |
| <span data-ttu-id="ccd71-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-282">System-Flags</span></span>           | <span data-ttu-id="ccd71-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ccd71-283">0x00000010</span></span>                      |
| <span data-ttu-id="ccd71-284">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ccd71-284">Classes used in</span></span>        | [<span data-ttu-id="ccd71-285">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ccd71-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ccd71-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ccd71-286">Windows Server 2012</span></span>



| <span data-ttu-id="ccd71-287">進入</span><span class="sxs-lookup"><span data-stu-id="ccd71-287">Entry</span></span> | <span data-ttu-id="ccd71-288">值</span><span class="sxs-lookup"><span data-stu-id="ccd71-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ccd71-289">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ccd71-289">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-290">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ccd71-290">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ccd71-291">System-Only</span><span class="sxs-lookup"><span data-stu-id="ccd71-291">System-Only</span></span>            | <span data-ttu-id="ccd71-292">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-292">False</span></span>                           |
| <span data-ttu-id="ccd71-293">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ccd71-293">Is-Single-Valued</span></span>       | <span data-ttu-id="ccd71-294">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-294">False</span></span>                           |
| <span data-ttu-id="ccd71-295">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ccd71-295">Is Indexed</span></span>             | <span data-ttu-id="ccd71-296">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-296">False</span></span>                           |
| <span data-ttu-id="ccd71-297">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ccd71-297">In Global Catalog</span></span>      | <span data-ttu-id="ccd71-298">否</span><span class="sxs-lookup"><span data-stu-id="ccd71-298">False</span></span>                           |
| <span data-ttu-id="ccd71-299">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ccd71-299">NT-Security-Descriptor</span></span> | <span data-ttu-id="ccd71-300">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ccd71-300">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ccd71-301">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ccd71-301">Range-Lower</span></span>            | <span data-ttu-id="ccd71-302">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-302">16</span></span>                              |
| <span data-ttu-id="ccd71-303">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ccd71-303">Range-Upper</span></span>            | <span data-ttu-id="ccd71-304">16</span><span class="sxs-lookup"><span data-stu-id="ccd71-304">16</span></span>                              |
| <span data-ttu-id="ccd71-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-305">Search-Flags</span></span>           | <span data-ttu-id="ccd71-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ccd71-306">0x00000000</span></span>                      |
| <span data-ttu-id="ccd71-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ccd71-307">System-Flags</span></span>           | <span data-ttu-id="ccd71-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ccd71-308">0x00000010</span></span>                      |
| <span data-ttu-id="ccd71-309">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ccd71-309">Classes used in</span></span>        | [<span data-ttu-id="ccd71-310">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ccd71-310">**Top**</span></span>](c-top.md)<br/> |



 

 






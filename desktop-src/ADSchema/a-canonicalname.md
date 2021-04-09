---
title: Canonical-Name 屬性
description: 標準格式的物件名稱。
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Canonical-Name 屬性 AD 架構
- canonicalName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 487476271456fa0465e8d47791f5376f33617eb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845580"
---
# <a name="canonical-name-attribute"></a><span data-ttu-id="129db-105">Canonical-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="129db-105">Canonical-Name attribute</span></span>

<span data-ttu-id="129db-106">標準格式的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="129db-106">The name of the object in canonical format.</span></span> <span data-ttu-id="129db-107">myserver2.fabrikam.com/users/jeffsmith 是標準格式的辨別名稱範例。</span><span class="sxs-lookup"><span data-stu-id="129db-107">myserver2.fabrikam.com/users/jeffsmith is an example of a distinguished name in canonical format.</span></span> <span data-ttu-id="129db-108">這是一個結構化屬性。</span><span class="sxs-lookup"><span data-stu-id="129db-108">This is a constructed attribute.</span></span> <span data-ttu-id="129db-109">傳回的結果與下列 Active Directory 函數所傳回的結果相同： DsCrackNames (Null、DS \_ 名稱 \_ 旗標 \_ \_ 僅限語法、ds \_ FQDN \_ 1779 \_ 名稱、ds 正式 \_ \_ 名稱、... ) 。</span><span class="sxs-lookup"><span data-stu-id="129db-109">The results returned are identical to those returned by the following Active Directory function: DsCrackNames(NULL, DS\_NAME\_FLAG\_SYNTACTICAL\_ONLY, DS\_FQDN\_1779\_NAME, DS\_CANONICAL\_NAME, ...).</span></span>

<span data-ttu-id="129db-110">如需有關名稱格式的詳細資訊，請參閱 [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa)。</span><span class="sxs-lookup"><span data-stu-id="129db-110">For more information about name formats, see [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span></span>



| <span data-ttu-id="129db-111">進入</span><span class="sxs-lookup"><span data-stu-id="129db-111">Entry</span></span> | <span data-ttu-id="129db-112">值</span><span class="sxs-lookup"><span data-stu-id="129db-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="129db-113">CN</span><span class="sxs-lookup"><span data-stu-id="129db-113">CN</span></span>                | <span data-ttu-id="129db-114">Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="129db-114">Canonical-Name</span></span>                              |
| <span data-ttu-id="129db-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="129db-115">Ldap-Display-Name</span></span> | <span data-ttu-id="129db-116">canonicalName</span><span class="sxs-lookup"><span data-stu-id="129db-116">canonicalName</span></span>                               |
| <span data-ttu-id="129db-117">大小</span><span class="sxs-lookup"><span data-stu-id="129db-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="129db-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="129db-118">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="129db-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="129db-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="129db-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="129db-120">Attribute-Id</span></span>      | <span data-ttu-id="129db-121">1.2.840.113556.1.4.916</span><span class="sxs-lookup"><span data-stu-id="129db-121">1.2.840.113556.1.4.916</span></span>                      |
| <span data-ttu-id="129db-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="129db-122">System-Id-Guid</span></span>    | <span data-ttu-id="129db-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="129db-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="129db-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="129db-124">Syntax</span></span>            | [<span data-ttu-id="129db-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="129db-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="129db-126">實作</span><span class="sxs-lookup"><span data-stu-id="129db-126">Implementations</span></span>

-   [<span data-ttu-id="129db-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="129db-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="129db-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="129db-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="129db-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="129db-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="129db-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="129db-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="129db-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="129db-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="129db-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="129db-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="129db-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="129db-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="129db-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="129db-134">Windows 2000 Server</span></span>



| <span data-ttu-id="129db-135">進入</span><span class="sxs-lookup"><span data-stu-id="129db-135">Entry</span></span> | <span data-ttu-id="129db-136">值</span><span class="sxs-lookup"><span data-stu-id="129db-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="129db-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="129db-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129db-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="129db-139">System-Only</span></span>            | <span data-ttu-id="129db-140">對</span><span class="sxs-lookup"><span data-stu-id="129db-140">True</span></span>                            |
| <span data-ttu-id="129db-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="129db-141">Is-Single-Valued</span></span>       | <span data-ttu-id="129db-142">否</span><span class="sxs-lookup"><span data-stu-id="129db-142">False</span></span>                           |
| <span data-ttu-id="129db-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="129db-143">Is Indexed</span></span>             | <span data-ttu-id="129db-144">否</span><span class="sxs-lookup"><span data-stu-id="129db-144">False</span></span>                           |
| <span data-ttu-id="129db-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="129db-145">In Global Catalog</span></span>      | <span data-ttu-id="129db-146">否</span><span class="sxs-lookup"><span data-stu-id="129db-146">False</span></span>                           |
| <span data-ttu-id="129db-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="129db-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="129db-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="129db-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="129db-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129db-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="129db-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129db-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="129db-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-151">Search-Flags</span></span>           | <span data-ttu-id="129db-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129db-152">0x00000000</span></span>                      |
| <span data-ttu-id="129db-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-153">System-Flags</span></span>           | <span data-ttu-id="129db-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="129db-154">0x08000014</span></span>                      |
| <span data-ttu-id="129db-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="129db-155">Classes used in</span></span>        | [<span data-ttu-id="129db-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="129db-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="129db-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="129db-157">Windows Server 2003</span></span>



| <span data-ttu-id="129db-158">進入</span><span class="sxs-lookup"><span data-stu-id="129db-158">Entry</span></span> | <span data-ttu-id="129db-159">值</span><span class="sxs-lookup"><span data-stu-id="129db-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="129db-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="129db-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129db-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="129db-162">System-Only</span></span>            | <span data-ttu-id="129db-163">對</span><span class="sxs-lookup"><span data-stu-id="129db-163">True</span></span>                            |
| <span data-ttu-id="129db-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="129db-164">Is-Single-Valued</span></span>       | <span data-ttu-id="129db-165">否</span><span class="sxs-lookup"><span data-stu-id="129db-165">False</span></span>                           |
| <span data-ttu-id="129db-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="129db-166">Is Indexed</span></span>             | <span data-ttu-id="129db-167">否</span><span class="sxs-lookup"><span data-stu-id="129db-167">False</span></span>                           |
| <span data-ttu-id="129db-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="129db-168">In Global Catalog</span></span>      | <span data-ttu-id="129db-169">否</span><span class="sxs-lookup"><span data-stu-id="129db-169">False</span></span>                           |
| <span data-ttu-id="129db-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="129db-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="129db-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="129db-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="129db-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129db-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="129db-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129db-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="129db-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-174">Search-Flags</span></span>           | <span data-ttu-id="129db-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129db-175">0x00000000</span></span>                      |
| <span data-ttu-id="129db-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-176">System-Flags</span></span>           | <span data-ttu-id="129db-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="129db-177">0x08000014</span></span>                      |
| <span data-ttu-id="129db-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="129db-178">Classes used in</span></span>        | [<span data-ttu-id="129db-179">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="129db-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="129db-180">亞當</span><span class="sxs-lookup"><span data-stu-id="129db-180">ADAM</span></span>



| <span data-ttu-id="129db-181">進入</span><span class="sxs-lookup"><span data-stu-id="129db-181">Entry</span></span> | <span data-ttu-id="129db-182">值</span><span class="sxs-lookup"><span data-stu-id="129db-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="129db-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="129db-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129db-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="129db-185">System-Only</span></span>            | <span data-ttu-id="129db-186">對</span><span class="sxs-lookup"><span data-stu-id="129db-186">True</span></span>                            |
| <span data-ttu-id="129db-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="129db-187">Is-Single-Valued</span></span>       | <span data-ttu-id="129db-188">否</span><span class="sxs-lookup"><span data-stu-id="129db-188">False</span></span>                           |
| <span data-ttu-id="129db-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="129db-189">Is Indexed</span></span>             | <span data-ttu-id="129db-190">否</span><span class="sxs-lookup"><span data-stu-id="129db-190">False</span></span>                           |
| <span data-ttu-id="129db-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="129db-191">In Global Catalog</span></span>      | <span data-ttu-id="129db-192">否</span><span class="sxs-lookup"><span data-stu-id="129db-192">False</span></span>                           |
| <span data-ttu-id="129db-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="129db-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="129db-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="129db-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="129db-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129db-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="129db-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129db-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="129db-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-197">Search-Flags</span></span>           | <span data-ttu-id="129db-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129db-198">0x00000000</span></span>                      |
| <span data-ttu-id="129db-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-199">System-Flags</span></span>           | <span data-ttu-id="129db-200">0x08000014</span><span class="sxs-lookup"><span data-stu-id="129db-200">0x08000014</span></span>                      |
| <span data-ttu-id="129db-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="129db-201">Classes used in</span></span>        | [<span data-ttu-id="129db-202">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="129db-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="129db-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="129db-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="129db-204">進入</span><span class="sxs-lookup"><span data-stu-id="129db-204">Entry</span></span> | <span data-ttu-id="129db-205">值</span><span class="sxs-lookup"><span data-stu-id="129db-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="129db-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="129db-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129db-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="129db-208">System-Only</span></span>            | <span data-ttu-id="129db-209">對</span><span class="sxs-lookup"><span data-stu-id="129db-209">True</span></span>                            |
| <span data-ttu-id="129db-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="129db-210">Is-Single-Valued</span></span>       | <span data-ttu-id="129db-211">否</span><span class="sxs-lookup"><span data-stu-id="129db-211">False</span></span>                           |
| <span data-ttu-id="129db-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="129db-212">Is Indexed</span></span>             | <span data-ttu-id="129db-213">否</span><span class="sxs-lookup"><span data-stu-id="129db-213">False</span></span>                           |
| <span data-ttu-id="129db-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="129db-214">In Global Catalog</span></span>      | <span data-ttu-id="129db-215">否</span><span class="sxs-lookup"><span data-stu-id="129db-215">False</span></span>                           |
| <span data-ttu-id="129db-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="129db-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="129db-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="129db-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="129db-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129db-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="129db-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129db-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="129db-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-220">Search-Flags</span></span>           | <span data-ttu-id="129db-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129db-221">0x00000000</span></span>                      |
| <span data-ttu-id="129db-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-222">System-Flags</span></span>           | <span data-ttu-id="129db-223">0x08000014</span><span class="sxs-lookup"><span data-stu-id="129db-223">0x08000014</span></span>                      |
| <span data-ttu-id="129db-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="129db-224">Classes used in</span></span>        | [<span data-ttu-id="129db-225">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="129db-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="129db-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="129db-226">Windows Server 2008</span></span>



| <span data-ttu-id="129db-227">進入</span><span class="sxs-lookup"><span data-stu-id="129db-227">Entry</span></span> | <span data-ttu-id="129db-228">值</span><span class="sxs-lookup"><span data-stu-id="129db-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="129db-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="129db-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129db-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="129db-231">System-Only</span></span>            | <span data-ttu-id="129db-232">對</span><span class="sxs-lookup"><span data-stu-id="129db-232">True</span></span>                            |
| <span data-ttu-id="129db-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="129db-233">Is-Single-Valued</span></span>       | <span data-ttu-id="129db-234">否</span><span class="sxs-lookup"><span data-stu-id="129db-234">False</span></span>                           |
| <span data-ttu-id="129db-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="129db-235">Is Indexed</span></span>             | <span data-ttu-id="129db-236">否</span><span class="sxs-lookup"><span data-stu-id="129db-236">False</span></span>                           |
| <span data-ttu-id="129db-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="129db-237">In Global Catalog</span></span>      | <span data-ttu-id="129db-238">否</span><span class="sxs-lookup"><span data-stu-id="129db-238">False</span></span>                           |
| <span data-ttu-id="129db-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="129db-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="129db-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="129db-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="129db-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129db-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="129db-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129db-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="129db-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-243">Search-Flags</span></span>           | <span data-ttu-id="129db-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129db-244">0x00000000</span></span>                      |
| <span data-ttu-id="129db-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-245">System-Flags</span></span>           | <span data-ttu-id="129db-246">0x08000014</span><span class="sxs-lookup"><span data-stu-id="129db-246">0x08000014</span></span>                      |
| <span data-ttu-id="129db-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="129db-247">Classes used in</span></span>        | [<span data-ttu-id="129db-248">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="129db-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="129db-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="129db-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="129db-250">進入</span><span class="sxs-lookup"><span data-stu-id="129db-250">Entry</span></span> | <span data-ttu-id="129db-251">值</span><span class="sxs-lookup"><span data-stu-id="129db-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="129db-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="129db-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129db-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="129db-254">System-Only</span></span>            | <span data-ttu-id="129db-255">對</span><span class="sxs-lookup"><span data-stu-id="129db-255">True</span></span>                            |
| <span data-ttu-id="129db-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="129db-256">Is-Single-Valued</span></span>       | <span data-ttu-id="129db-257">否</span><span class="sxs-lookup"><span data-stu-id="129db-257">False</span></span>                           |
| <span data-ttu-id="129db-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="129db-258">Is Indexed</span></span>             | <span data-ttu-id="129db-259">否</span><span class="sxs-lookup"><span data-stu-id="129db-259">False</span></span>                           |
| <span data-ttu-id="129db-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="129db-260">In Global Catalog</span></span>      | <span data-ttu-id="129db-261">否</span><span class="sxs-lookup"><span data-stu-id="129db-261">False</span></span>                           |
| <span data-ttu-id="129db-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="129db-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="129db-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="129db-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="129db-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129db-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="129db-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129db-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="129db-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-266">Search-Flags</span></span>           | <span data-ttu-id="129db-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129db-267">0x00000000</span></span>                      |
| <span data-ttu-id="129db-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-268">System-Flags</span></span>           | <span data-ttu-id="129db-269">0x08000014</span><span class="sxs-lookup"><span data-stu-id="129db-269">0x08000014</span></span>                      |
| <span data-ttu-id="129db-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="129db-270">Classes used in</span></span>        | [<span data-ttu-id="129db-271">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="129db-271">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="129db-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="129db-272">Windows Server 2012</span></span>



| <span data-ttu-id="129db-273">進入</span><span class="sxs-lookup"><span data-stu-id="129db-273">Entry</span></span> | <span data-ttu-id="129db-274">值</span><span class="sxs-lookup"><span data-stu-id="129db-274">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="129db-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="129db-275">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129db-276">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="129db-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="129db-277">System-Only</span></span>            | <span data-ttu-id="129db-278">對</span><span class="sxs-lookup"><span data-stu-id="129db-278">True</span></span>                            |
| <span data-ttu-id="129db-279">是-單一值</span><span class="sxs-lookup"><span data-stu-id="129db-279">Is-Single-Valued</span></span>       | <span data-ttu-id="129db-280">否</span><span class="sxs-lookup"><span data-stu-id="129db-280">False</span></span>                           |
| <span data-ttu-id="129db-281">已編制索引</span><span class="sxs-lookup"><span data-stu-id="129db-281">Is Indexed</span></span>             | <span data-ttu-id="129db-282">否</span><span class="sxs-lookup"><span data-stu-id="129db-282">False</span></span>                           |
| <span data-ttu-id="129db-283">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="129db-283">In Global Catalog</span></span>      | <span data-ttu-id="129db-284">否</span><span class="sxs-lookup"><span data-stu-id="129db-284">False</span></span>                           |
| <span data-ttu-id="129db-285">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="129db-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="129db-286">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="129db-286">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="129db-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129db-287">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="129db-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129db-288">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="129db-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-289">Search-Flags</span></span>           | <span data-ttu-id="129db-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129db-290">0x00000000</span></span>                      |
| <span data-ttu-id="129db-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129db-291">System-Flags</span></span>           | <span data-ttu-id="129db-292">0x08000014</span><span class="sxs-lookup"><span data-stu-id="129db-292">0x08000014</span></span>                      |
| <span data-ttu-id="129db-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="129db-293">Classes used in</span></span>        | [<span data-ttu-id="129db-294">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="129db-294">**Top**</span></span>](c-top.md)<br/> |



 


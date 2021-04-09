---
title: Proxy-Addresses 屬性
description: Proxy 位址是在外部郵件系統中辨識 Microsoft Exchange Server 收件者物件的位址。 所有收件者物件都需要 Proxy 位址，例如自訂收件者和通訊群組清單。
ms.assetid: 7bb299d8-e67a-4062-91a3-b579fd71d5c9
ms.tgt_platform: multiple
keywords:
- Proxy-Addresses 屬性 AD 架構
- proxyAddresses 屬性 AD 架構
topic_type:
- apiref
api_name:
- Proxy-Addresses
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03542cef9bca48dbba1585e3837056b53673f34
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845327"
---
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="9f816-106">Proxy-Addresses 屬性</span><span class="sxs-lookup"><span data-stu-id="9f816-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="9f816-107">Proxy 位址是在外部郵件系統中辨識 Microsoft Exchange Server 收件者物件的位址。</span><span class="sxs-lookup"><span data-stu-id="9f816-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="9f816-108">所有收件者物件都需要 Proxy 位址，例如自訂收件者和通訊群組清單。</span><span class="sxs-lookup"><span data-stu-id="9f816-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="9f816-109">進入</span><span class="sxs-lookup"><span data-stu-id="9f816-109">Entry</span></span> | <span data-ttu-id="9f816-110">值</span><span class="sxs-lookup"><span data-stu-id="9f816-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f816-111">CN</span><span class="sxs-lookup"><span data-stu-id="9f816-111">CN</span></span>                | <span data-ttu-id="9f816-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="9f816-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="9f816-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9f816-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9f816-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="9f816-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="9f816-115">大小</span><span class="sxs-lookup"><span data-stu-id="9f816-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="9f816-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9f816-116">Update Privilege</span></span>  | <span data-ttu-id="9f816-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="9f816-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="9f816-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9f816-118">Update Frequency</span></span>  | <span data-ttu-id="9f816-119">在安裝網址類別型時，由 Address-Type directory 物件提供的 DLL 所建立。</span><span class="sxs-lookup"><span data-stu-id="9f816-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="9f816-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9f816-120">Attribute-Id</span></span>      | <span data-ttu-id="9f816-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="9f816-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="9f816-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9f816-122">System-Id-Guid</span></span>    | <span data-ttu-id="9f816-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9f816-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="9f816-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f816-124">Syntax</span></span>            | [<span data-ttu-id="9f816-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9f816-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="9f816-126">實作</span><span class="sxs-lookup"><span data-stu-id="9f816-126">Implementations</span></span>

-   [<span data-ttu-id="9f816-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9f816-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9f816-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9f816-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9f816-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="9f816-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9f816-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9f816-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9f816-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9f816-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9f816-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9f816-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9f816-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9f816-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9f816-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f816-134">Windows 2000 Server</span></span>



| <span data-ttu-id="9f816-135">進入</span><span class="sxs-lookup"><span data-stu-id="9f816-135">Entry</span></span> | <span data-ttu-id="9f816-136">值</span><span class="sxs-lookup"><span data-stu-id="9f816-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f816-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f816-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f816-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f816-138">MAPI-Id</span></span>                | <span data-ttu-id="9f816-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="9f816-139">0x800F</span></span>                          |
| <span data-ttu-id="9f816-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f816-140">System-Only</span></span>            | <span data-ttu-id="9f816-141">否</span><span class="sxs-lookup"><span data-stu-id="9f816-141">False</span></span>                           |
| <span data-ttu-id="9f816-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f816-142">Is-Single-Valued</span></span>       | <span data-ttu-id="9f816-143">否</span><span class="sxs-lookup"><span data-stu-id="9f816-143">False</span></span>                           |
| <span data-ttu-id="9f816-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f816-144">Is Indexed</span></span>             | <span data-ttu-id="9f816-145">對</span><span class="sxs-lookup"><span data-stu-id="9f816-145">True</span></span>                            |
| <span data-ttu-id="9f816-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f816-146">In Global Catalog</span></span>      | <span data-ttu-id="9f816-147">否</span><span class="sxs-lookup"><span data-stu-id="9f816-147">False</span></span>                           |
| <span data-ttu-id="9f816-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f816-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f816-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f816-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f816-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f816-150">Range-Lower</span></span>            | <span data-ttu-id="9f816-151">1</span><span class="sxs-lookup"><span data-stu-id="9f816-151">1</span></span>                               |
| <span data-ttu-id="9f816-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f816-152">Range-Upper</span></span>            | <span data-ttu-id="9f816-153">1123</span><span class="sxs-lookup"><span data-stu-id="9f816-153">1123</span></span>                            |
| <span data-ttu-id="9f816-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-154">Search-Flags</span></span>           | <span data-ttu-id="9f816-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="9f816-155">0x00000005</span></span>                      |
| <span data-ttu-id="9f816-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-156">System-Flags</span></span>           | <span data-ttu-id="9f816-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f816-157">0x00000010</span></span>                      |
| <span data-ttu-id="9f816-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f816-158">Classes used in</span></span>        | [<span data-ttu-id="9f816-159">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f816-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9f816-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f816-160">Windows Server 2003</span></span>



| <span data-ttu-id="9f816-161">進入</span><span class="sxs-lookup"><span data-stu-id="9f816-161">Entry</span></span> | <span data-ttu-id="9f816-162">值</span><span class="sxs-lookup"><span data-stu-id="9f816-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f816-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f816-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f816-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f816-164">MAPI-Id</span></span>                | <span data-ttu-id="9f816-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="9f816-165">0x800F</span></span>                          |
| <span data-ttu-id="9f816-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f816-166">System-Only</span></span>            | <span data-ttu-id="9f816-167">否</span><span class="sxs-lookup"><span data-stu-id="9f816-167">False</span></span>                           |
| <span data-ttu-id="9f816-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f816-168">Is-Single-Valued</span></span>       | <span data-ttu-id="9f816-169">否</span><span class="sxs-lookup"><span data-stu-id="9f816-169">False</span></span>                           |
| <span data-ttu-id="9f816-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f816-170">Is Indexed</span></span>             | <span data-ttu-id="9f816-171">對</span><span class="sxs-lookup"><span data-stu-id="9f816-171">True</span></span>                            |
| <span data-ttu-id="9f816-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f816-172">In Global Catalog</span></span>      | <span data-ttu-id="9f816-173">否</span><span class="sxs-lookup"><span data-stu-id="9f816-173">False</span></span>                           |
| <span data-ttu-id="9f816-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f816-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f816-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f816-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f816-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f816-176">Range-Lower</span></span>            | <span data-ttu-id="9f816-177">1</span><span class="sxs-lookup"><span data-stu-id="9f816-177">1</span></span>                               |
| <span data-ttu-id="9f816-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f816-178">Range-Upper</span></span>            | <span data-ttu-id="9f816-179">1123</span><span class="sxs-lookup"><span data-stu-id="9f816-179">1123</span></span>                            |
| <span data-ttu-id="9f816-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-180">Search-Flags</span></span>           | <span data-ttu-id="9f816-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="9f816-181">0x00000005</span></span>                      |
| <span data-ttu-id="9f816-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-182">System-Flags</span></span>           | <span data-ttu-id="9f816-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f816-183">0x00000010</span></span>                      |
| <span data-ttu-id="9f816-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f816-184">Classes used in</span></span>        | [<span data-ttu-id="9f816-185">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f816-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9f816-186">亞當</span><span class="sxs-lookup"><span data-stu-id="9f816-186">ADAM</span></span>



| <span data-ttu-id="9f816-187">進入</span><span class="sxs-lookup"><span data-stu-id="9f816-187">Entry</span></span> | <span data-ttu-id="9f816-188">值</span><span class="sxs-lookup"><span data-stu-id="9f816-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f816-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f816-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f816-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f816-190">MAPI-Id</span></span>                | <span data-ttu-id="9f816-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="9f816-191">0x800F</span></span>                          |
| <span data-ttu-id="9f816-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f816-192">System-Only</span></span>            | <span data-ttu-id="9f816-193">否</span><span class="sxs-lookup"><span data-stu-id="9f816-193">False</span></span>                           |
| <span data-ttu-id="9f816-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f816-194">Is-Single-Valued</span></span>       | <span data-ttu-id="9f816-195">否</span><span class="sxs-lookup"><span data-stu-id="9f816-195">False</span></span>                           |
| <span data-ttu-id="9f816-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f816-196">Is Indexed</span></span>             | <span data-ttu-id="9f816-197">對</span><span class="sxs-lookup"><span data-stu-id="9f816-197">True</span></span>                            |
| <span data-ttu-id="9f816-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f816-198">In Global Catalog</span></span>      | <span data-ttu-id="9f816-199">否</span><span class="sxs-lookup"><span data-stu-id="9f816-199">False</span></span>                           |
| <span data-ttu-id="9f816-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f816-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f816-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f816-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f816-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f816-202">Range-Lower</span></span>            | <span data-ttu-id="9f816-203">1</span><span class="sxs-lookup"><span data-stu-id="9f816-203">1</span></span>                               |
| <span data-ttu-id="9f816-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f816-204">Range-Upper</span></span>            | <span data-ttu-id="9f816-205">1123</span><span class="sxs-lookup"><span data-stu-id="9f816-205">1123</span></span>                            |
| <span data-ttu-id="9f816-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-206">Search-Flags</span></span>           | <span data-ttu-id="9f816-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="9f816-207">0x00000005</span></span>                      |
| <span data-ttu-id="9f816-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-208">System-Flags</span></span>           | <span data-ttu-id="9f816-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f816-209">0x00000010</span></span>                      |
| <span data-ttu-id="9f816-210">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f816-210">Classes used in</span></span>        | [<span data-ttu-id="9f816-211">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f816-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9f816-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9f816-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9f816-213">進入</span><span class="sxs-lookup"><span data-stu-id="9f816-213">Entry</span></span> | <span data-ttu-id="9f816-214">值</span><span class="sxs-lookup"><span data-stu-id="9f816-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f816-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f816-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f816-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f816-216">MAPI-Id</span></span>                | <span data-ttu-id="9f816-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="9f816-217">0x800F</span></span>                          |
| <span data-ttu-id="9f816-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f816-218">System-Only</span></span>            | <span data-ttu-id="9f816-219">否</span><span class="sxs-lookup"><span data-stu-id="9f816-219">False</span></span>                           |
| <span data-ttu-id="9f816-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f816-220">Is-Single-Valued</span></span>       | <span data-ttu-id="9f816-221">否</span><span class="sxs-lookup"><span data-stu-id="9f816-221">False</span></span>                           |
| <span data-ttu-id="9f816-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f816-222">Is Indexed</span></span>             | <span data-ttu-id="9f816-223">對</span><span class="sxs-lookup"><span data-stu-id="9f816-223">True</span></span>                            |
| <span data-ttu-id="9f816-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f816-224">In Global Catalog</span></span>      | <span data-ttu-id="9f816-225">否</span><span class="sxs-lookup"><span data-stu-id="9f816-225">False</span></span>                           |
| <span data-ttu-id="9f816-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f816-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f816-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f816-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f816-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f816-228">Range-Lower</span></span>            | <span data-ttu-id="9f816-229">1</span><span class="sxs-lookup"><span data-stu-id="9f816-229">1</span></span>                               |
| <span data-ttu-id="9f816-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f816-230">Range-Upper</span></span>            | <span data-ttu-id="9f816-231">1123</span><span class="sxs-lookup"><span data-stu-id="9f816-231">1123</span></span>                            |
| <span data-ttu-id="9f816-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-232">Search-Flags</span></span>           | <span data-ttu-id="9f816-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="9f816-233">0x00000005</span></span>                      |
| <span data-ttu-id="9f816-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-234">System-Flags</span></span>           | <span data-ttu-id="9f816-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f816-235">0x00000010</span></span>                      |
| <span data-ttu-id="9f816-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f816-236">Classes used in</span></span>        | [<span data-ttu-id="9f816-237">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f816-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9f816-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f816-238">Windows Server 2008</span></span>



| <span data-ttu-id="9f816-239">進入</span><span class="sxs-lookup"><span data-stu-id="9f816-239">Entry</span></span> | <span data-ttu-id="9f816-240">值</span><span class="sxs-lookup"><span data-stu-id="9f816-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f816-241">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f816-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f816-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f816-242">MAPI-Id</span></span>                | <span data-ttu-id="9f816-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="9f816-243">0x800F</span></span>                          |
| <span data-ttu-id="9f816-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f816-244">System-Only</span></span>            | <span data-ttu-id="9f816-245">否</span><span class="sxs-lookup"><span data-stu-id="9f816-245">False</span></span>                           |
| <span data-ttu-id="9f816-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f816-246">Is-Single-Valued</span></span>       | <span data-ttu-id="9f816-247">否</span><span class="sxs-lookup"><span data-stu-id="9f816-247">False</span></span>                           |
| <span data-ttu-id="9f816-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f816-248">Is Indexed</span></span>             | <span data-ttu-id="9f816-249">對</span><span class="sxs-lookup"><span data-stu-id="9f816-249">True</span></span>                            |
| <span data-ttu-id="9f816-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f816-250">In Global Catalog</span></span>      | <span data-ttu-id="9f816-251">否</span><span class="sxs-lookup"><span data-stu-id="9f816-251">False</span></span>                           |
| <span data-ttu-id="9f816-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f816-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f816-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f816-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f816-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f816-254">Range-Lower</span></span>            | <span data-ttu-id="9f816-255">1</span><span class="sxs-lookup"><span data-stu-id="9f816-255">1</span></span>                               |
| <span data-ttu-id="9f816-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f816-256">Range-Upper</span></span>            | <span data-ttu-id="9f816-257">1123</span><span class="sxs-lookup"><span data-stu-id="9f816-257">1123</span></span>                            |
| <span data-ttu-id="9f816-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-258">Search-Flags</span></span>           | <span data-ttu-id="9f816-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="9f816-259">0x00000005</span></span>                      |
| <span data-ttu-id="9f816-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-260">System-Flags</span></span>           | <span data-ttu-id="9f816-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f816-261">0x00000010</span></span>                      |
| <span data-ttu-id="9f816-262">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f816-262">Classes used in</span></span>        | [<span data-ttu-id="9f816-263">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f816-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9f816-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f816-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9f816-265">進入</span><span class="sxs-lookup"><span data-stu-id="9f816-265">Entry</span></span> | <span data-ttu-id="9f816-266">值</span><span class="sxs-lookup"><span data-stu-id="9f816-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f816-267">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f816-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f816-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f816-268">MAPI-Id</span></span>                | <span data-ttu-id="9f816-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="9f816-269">0x800F</span></span>                          |
| <span data-ttu-id="9f816-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f816-270">System-Only</span></span>            | <span data-ttu-id="9f816-271">否</span><span class="sxs-lookup"><span data-stu-id="9f816-271">False</span></span>                           |
| <span data-ttu-id="9f816-272">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f816-272">Is-Single-Valued</span></span>       | <span data-ttu-id="9f816-273">否</span><span class="sxs-lookup"><span data-stu-id="9f816-273">False</span></span>                           |
| <span data-ttu-id="9f816-274">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f816-274">Is Indexed</span></span>             | <span data-ttu-id="9f816-275">對</span><span class="sxs-lookup"><span data-stu-id="9f816-275">True</span></span>                            |
| <span data-ttu-id="9f816-276">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f816-276">In Global Catalog</span></span>      | <span data-ttu-id="9f816-277">否</span><span class="sxs-lookup"><span data-stu-id="9f816-277">False</span></span>                           |
| <span data-ttu-id="9f816-278">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f816-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f816-279">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f816-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f816-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f816-280">Range-Lower</span></span>            | <span data-ttu-id="9f816-281">1</span><span class="sxs-lookup"><span data-stu-id="9f816-281">1</span></span>                               |
| <span data-ttu-id="9f816-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f816-282">Range-Upper</span></span>            | <span data-ttu-id="9f816-283">1123</span><span class="sxs-lookup"><span data-stu-id="9f816-283">1123</span></span>                            |
| <span data-ttu-id="9f816-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-284">Search-Flags</span></span>           | <span data-ttu-id="9f816-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="9f816-285">0x00000005</span></span>                      |
| <span data-ttu-id="9f816-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-286">System-Flags</span></span>           | <span data-ttu-id="9f816-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f816-287">0x00000010</span></span>                      |
| <span data-ttu-id="9f816-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f816-288">Classes used in</span></span>        | [<span data-ttu-id="9f816-289">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f816-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9f816-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f816-290">Windows Server 2012</span></span>



| <span data-ttu-id="9f816-291">進入</span><span class="sxs-lookup"><span data-stu-id="9f816-291">Entry</span></span> | <span data-ttu-id="9f816-292">值</span><span class="sxs-lookup"><span data-stu-id="9f816-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f816-293">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9f816-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f816-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f816-294">MAPI-Id</span></span>                | <span data-ttu-id="9f816-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="9f816-295">0x800F</span></span>                          |
| <span data-ttu-id="9f816-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f816-296">System-Only</span></span>            | <span data-ttu-id="9f816-297">否</span><span class="sxs-lookup"><span data-stu-id="9f816-297">False</span></span>                           |
| <span data-ttu-id="9f816-298">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9f816-298">Is-Single-Valued</span></span>       | <span data-ttu-id="9f816-299">否</span><span class="sxs-lookup"><span data-stu-id="9f816-299">False</span></span>                           |
| <span data-ttu-id="9f816-300">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9f816-300">Is Indexed</span></span>             | <span data-ttu-id="9f816-301">對</span><span class="sxs-lookup"><span data-stu-id="9f816-301">True</span></span>                            |
| <span data-ttu-id="9f816-302">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9f816-302">In Global Catalog</span></span>      | <span data-ttu-id="9f816-303">否</span><span class="sxs-lookup"><span data-stu-id="9f816-303">False</span></span>                           |
| <span data-ttu-id="9f816-304">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9f816-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f816-305">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9f816-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f816-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f816-306">Range-Lower</span></span>            | <span data-ttu-id="9f816-307">1</span><span class="sxs-lookup"><span data-stu-id="9f816-307">1</span></span>                               |
| <span data-ttu-id="9f816-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f816-308">Range-Upper</span></span>            | <span data-ttu-id="9f816-309">1123</span><span class="sxs-lookup"><span data-stu-id="9f816-309">1123</span></span>                            |
| <span data-ttu-id="9f816-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-310">Search-Flags</span></span>           | <span data-ttu-id="9f816-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="9f816-311">0x00000005</span></span>                      |
| <span data-ttu-id="9f816-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f816-312">System-Flags</span></span>           | <span data-ttu-id="9f816-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f816-313">0x00000010</span></span>                      |
| <span data-ttu-id="9f816-314">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9f816-314">Classes used in</span></span>        | [<span data-ttu-id="9f816-315">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="9f816-315">**Top**</span></span>](c-top.md)<br/> |



 

 






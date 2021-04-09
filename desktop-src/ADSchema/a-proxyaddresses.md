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
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="7282d-106">Proxy-Addresses 屬性</span><span class="sxs-lookup"><span data-stu-id="7282d-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="7282d-107">Proxy 位址是在外部郵件系統中辨識 Microsoft Exchange Server 收件者物件的位址。</span><span class="sxs-lookup"><span data-stu-id="7282d-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="7282d-108">所有收件者物件都需要 Proxy 位址，例如自訂收件者和通訊群組清單。</span><span class="sxs-lookup"><span data-stu-id="7282d-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="7282d-109">進入</span><span class="sxs-lookup"><span data-stu-id="7282d-109">Entry</span></span> | <span data-ttu-id="7282d-110">值</span><span class="sxs-lookup"><span data-stu-id="7282d-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7282d-111">CN</span><span class="sxs-lookup"><span data-stu-id="7282d-111">CN</span></span>                | <span data-ttu-id="7282d-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="7282d-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="7282d-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7282d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7282d-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="7282d-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="7282d-115">大小</span><span class="sxs-lookup"><span data-stu-id="7282d-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="7282d-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7282d-116">Update Privilege</span></span>  | <span data-ttu-id="7282d-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7282d-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="7282d-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7282d-118">Update Frequency</span></span>  | <span data-ttu-id="7282d-119">在安裝網址類別型時，由 Address-Type directory 物件提供的 DLL 所建立。</span><span class="sxs-lookup"><span data-stu-id="7282d-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="7282d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7282d-120">Attribute-Id</span></span>      | <span data-ttu-id="7282d-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="7282d-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="7282d-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7282d-122">System-Id-Guid</span></span>    | <span data-ttu-id="7282d-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7282d-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="7282d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="7282d-124">Syntax</span></span>            | [<span data-ttu-id="7282d-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7282d-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="7282d-126">實作</span><span class="sxs-lookup"><span data-stu-id="7282d-126">Implementations</span></span>

-   [<span data-ttu-id="7282d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7282d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7282d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7282d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7282d-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7282d-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7282d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7282d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7282d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7282d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7282d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7282d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7282d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7282d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7282d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7282d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="7282d-135">進入</span><span class="sxs-lookup"><span data-stu-id="7282d-135">Entry</span></span> | <span data-ttu-id="7282d-136">值</span><span class="sxs-lookup"><span data-stu-id="7282d-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7282d-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7282d-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7282d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7282d-138">MAPI-Id</span></span>                | <span data-ttu-id="7282d-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="7282d-139">0x800F</span></span>                          |
| <span data-ttu-id="7282d-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="7282d-140">System-Only</span></span>            | <span data-ttu-id="7282d-141">否</span><span class="sxs-lookup"><span data-stu-id="7282d-141">False</span></span>                           |
| <span data-ttu-id="7282d-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7282d-142">Is-Single-Valued</span></span>       | <span data-ttu-id="7282d-143">否</span><span class="sxs-lookup"><span data-stu-id="7282d-143">False</span></span>                           |
| <span data-ttu-id="7282d-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7282d-144">Is Indexed</span></span>             | <span data-ttu-id="7282d-145">對</span><span class="sxs-lookup"><span data-stu-id="7282d-145">True</span></span>                            |
| <span data-ttu-id="7282d-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7282d-146">In Global Catalog</span></span>      | <span data-ttu-id="7282d-147">否</span><span class="sxs-lookup"><span data-stu-id="7282d-147">False</span></span>                           |
| <span data-ttu-id="7282d-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7282d-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="7282d-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7282d-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7282d-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7282d-150">Range-Lower</span></span>            | <span data-ttu-id="7282d-151">1</span><span class="sxs-lookup"><span data-stu-id="7282d-151">1</span></span>                               |
| <span data-ttu-id="7282d-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7282d-152">Range-Upper</span></span>            | <span data-ttu-id="7282d-153">1123</span><span class="sxs-lookup"><span data-stu-id="7282d-153">1123</span></span>                            |
| <span data-ttu-id="7282d-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-154">Search-Flags</span></span>           | <span data-ttu-id="7282d-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7282d-155">0x00000005</span></span>                      |
| <span data-ttu-id="7282d-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-156">System-Flags</span></span>           | <span data-ttu-id="7282d-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7282d-157">0x00000010</span></span>                      |
| <span data-ttu-id="7282d-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7282d-158">Classes used in</span></span>        | [<span data-ttu-id="7282d-159">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7282d-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7282d-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7282d-160">Windows Server 2003</span></span>



| <span data-ttu-id="7282d-161">進入</span><span class="sxs-lookup"><span data-stu-id="7282d-161">Entry</span></span> | <span data-ttu-id="7282d-162">值</span><span class="sxs-lookup"><span data-stu-id="7282d-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7282d-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7282d-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7282d-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7282d-164">MAPI-Id</span></span>                | <span data-ttu-id="7282d-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="7282d-165">0x800F</span></span>                          |
| <span data-ttu-id="7282d-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="7282d-166">System-Only</span></span>            | <span data-ttu-id="7282d-167">否</span><span class="sxs-lookup"><span data-stu-id="7282d-167">False</span></span>                           |
| <span data-ttu-id="7282d-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7282d-168">Is-Single-Valued</span></span>       | <span data-ttu-id="7282d-169">否</span><span class="sxs-lookup"><span data-stu-id="7282d-169">False</span></span>                           |
| <span data-ttu-id="7282d-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7282d-170">Is Indexed</span></span>             | <span data-ttu-id="7282d-171">對</span><span class="sxs-lookup"><span data-stu-id="7282d-171">True</span></span>                            |
| <span data-ttu-id="7282d-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7282d-172">In Global Catalog</span></span>      | <span data-ttu-id="7282d-173">否</span><span class="sxs-lookup"><span data-stu-id="7282d-173">False</span></span>                           |
| <span data-ttu-id="7282d-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7282d-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="7282d-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7282d-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7282d-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7282d-176">Range-Lower</span></span>            | <span data-ttu-id="7282d-177">1</span><span class="sxs-lookup"><span data-stu-id="7282d-177">1</span></span>                               |
| <span data-ttu-id="7282d-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7282d-178">Range-Upper</span></span>            | <span data-ttu-id="7282d-179">1123</span><span class="sxs-lookup"><span data-stu-id="7282d-179">1123</span></span>                            |
| <span data-ttu-id="7282d-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-180">Search-Flags</span></span>           | <span data-ttu-id="7282d-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7282d-181">0x00000005</span></span>                      |
| <span data-ttu-id="7282d-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-182">System-Flags</span></span>           | <span data-ttu-id="7282d-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7282d-183">0x00000010</span></span>                      |
| <span data-ttu-id="7282d-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7282d-184">Classes used in</span></span>        | [<span data-ttu-id="7282d-185">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7282d-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7282d-186">亞當</span><span class="sxs-lookup"><span data-stu-id="7282d-186">ADAM</span></span>



| <span data-ttu-id="7282d-187">進入</span><span class="sxs-lookup"><span data-stu-id="7282d-187">Entry</span></span> | <span data-ttu-id="7282d-188">值</span><span class="sxs-lookup"><span data-stu-id="7282d-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7282d-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7282d-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7282d-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7282d-190">MAPI-Id</span></span>                | <span data-ttu-id="7282d-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="7282d-191">0x800F</span></span>                          |
| <span data-ttu-id="7282d-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="7282d-192">System-Only</span></span>            | <span data-ttu-id="7282d-193">否</span><span class="sxs-lookup"><span data-stu-id="7282d-193">False</span></span>                           |
| <span data-ttu-id="7282d-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7282d-194">Is-Single-Valued</span></span>       | <span data-ttu-id="7282d-195">否</span><span class="sxs-lookup"><span data-stu-id="7282d-195">False</span></span>                           |
| <span data-ttu-id="7282d-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7282d-196">Is Indexed</span></span>             | <span data-ttu-id="7282d-197">對</span><span class="sxs-lookup"><span data-stu-id="7282d-197">True</span></span>                            |
| <span data-ttu-id="7282d-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7282d-198">In Global Catalog</span></span>      | <span data-ttu-id="7282d-199">否</span><span class="sxs-lookup"><span data-stu-id="7282d-199">False</span></span>                           |
| <span data-ttu-id="7282d-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7282d-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="7282d-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7282d-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7282d-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7282d-202">Range-Lower</span></span>            | <span data-ttu-id="7282d-203">1</span><span class="sxs-lookup"><span data-stu-id="7282d-203">1</span></span>                               |
| <span data-ttu-id="7282d-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7282d-204">Range-Upper</span></span>            | <span data-ttu-id="7282d-205">1123</span><span class="sxs-lookup"><span data-stu-id="7282d-205">1123</span></span>                            |
| <span data-ttu-id="7282d-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-206">Search-Flags</span></span>           | <span data-ttu-id="7282d-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7282d-207">0x00000005</span></span>                      |
| <span data-ttu-id="7282d-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-208">System-Flags</span></span>           | <span data-ttu-id="7282d-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7282d-209">0x00000010</span></span>                      |
| <span data-ttu-id="7282d-210">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7282d-210">Classes used in</span></span>        | [<span data-ttu-id="7282d-211">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7282d-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7282d-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7282d-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7282d-213">進入</span><span class="sxs-lookup"><span data-stu-id="7282d-213">Entry</span></span> | <span data-ttu-id="7282d-214">值</span><span class="sxs-lookup"><span data-stu-id="7282d-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7282d-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7282d-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7282d-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7282d-216">MAPI-Id</span></span>                | <span data-ttu-id="7282d-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="7282d-217">0x800F</span></span>                          |
| <span data-ttu-id="7282d-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="7282d-218">System-Only</span></span>            | <span data-ttu-id="7282d-219">否</span><span class="sxs-lookup"><span data-stu-id="7282d-219">False</span></span>                           |
| <span data-ttu-id="7282d-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7282d-220">Is-Single-Valued</span></span>       | <span data-ttu-id="7282d-221">否</span><span class="sxs-lookup"><span data-stu-id="7282d-221">False</span></span>                           |
| <span data-ttu-id="7282d-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7282d-222">Is Indexed</span></span>             | <span data-ttu-id="7282d-223">對</span><span class="sxs-lookup"><span data-stu-id="7282d-223">True</span></span>                            |
| <span data-ttu-id="7282d-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7282d-224">In Global Catalog</span></span>      | <span data-ttu-id="7282d-225">否</span><span class="sxs-lookup"><span data-stu-id="7282d-225">False</span></span>                           |
| <span data-ttu-id="7282d-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7282d-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="7282d-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7282d-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7282d-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7282d-228">Range-Lower</span></span>            | <span data-ttu-id="7282d-229">1</span><span class="sxs-lookup"><span data-stu-id="7282d-229">1</span></span>                               |
| <span data-ttu-id="7282d-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7282d-230">Range-Upper</span></span>            | <span data-ttu-id="7282d-231">1123</span><span class="sxs-lookup"><span data-stu-id="7282d-231">1123</span></span>                            |
| <span data-ttu-id="7282d-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-232">Search-Flags</span></span>           | <span data-ttu-id="7282d-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7282d-233">0x00000005</span></span>                      |
| <span data-ttu-id="7282d-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-234">System-Flags</span></span>           | <span data-ttu-id="7282d-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7282d-235">0x00000010</span></span>                      |
| <span data-ttu-id="7282d-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7282d-236">Classes used in</span></span>        | [<span data-ttu-id="7282d-237">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7282d-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7282d-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7282d-238">Windows Server 2008</span></span>



| <span data-ttu-id="7282d-239">進入</span><span class="sxs-lookup"><span data-stu-id="7282d-239">Entry</span></span> | <span data-ttu-id="7282d-240">值</span><span class="sxs-lookup"><span data-stu-id="7282d-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7282d-241">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7282d-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7282d-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7282d-242">MAPI-Id</span></span>                | <span data-ttu-id="7282d-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="7282d-243">0x800F</span></span>                          |
| <span data-ttu-id="7282d-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="7282d-244">System-Only</span></span>            | <span data-ttu-id="7282d-245">否</span><span class="sxs-lookup"><span data-stu-id="7282d-245">False</span></span>                           |
| <span data-ttu-id="7282d-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7282d-246">Is-Single-Valued</span></span>       | <span data-ttu-id="7282d-247">否</span><span class="sxs-lookup"><span data-stu-id="7282d-247">False</span></span>                           |
| <span data-ttu-id="7282d-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7282d-248">Is Indexed</span></span>             | <span data-ttu-id="7282d-249">對</span><span class="sxs-lookup"><span data-stu-id="7282d-249">True</span></span>                            |
| <span data-ttu-id="7282d-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7282d-250">In Global Catalog</span></span>      | <span data-ttu-id="7282d-251">否</span><span class="sxs-lookup"><span data-stu-id="7282d-251">False</span></span>                           |
| <span data-ttu-id="7282d-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7282d-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="7282d-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7282d-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7282d-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7282d-254">Range-Lower</span></span>            | <span data-ttu-id="7282d-255">1</span><span class="sxs-lookup"><span data-stu-id="7282d-255">1</span></span>                               |
| <span data-ttu-id="7282d-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7282d-256">Range-Upper</span></span>            | <span data-ttu-id="7282d-257">1123</span><span class="sxs-lookup"><span data-stu-id="7282d-257">1123</span></span>                            |
| <span data-ttu-id="7282d-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-258">Search-Flags</span></span>           | <span data-ttu-id="7282d-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7282d-259">0x00000005</span></span>                      |
| <span data-ttu-id="7282d-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-260">System-Flags</span></span>           | <span data-ttu-id="7282d-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7282d-261">0x00000010</span></span>                      |
| <span data-ttu-id="7282d-262">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7282d-262">Classes used in</span></span>        | [<span data-ttu-id="7282d-263">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7282d-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7282d-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7282d-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7282d-265">進入</span><span class="sxs-lookup"><span data-stu-id="7282d-265">Entry</span></span> | <span data-ttu-id="7282d-266">值</span><span class="sxs-lookup"><span data-stu-id="7282d-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7282d-267">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7282d-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7282d-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7282d-268">MAPI-Id</span></span>                | <span data-ttu-id="7282d-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="7282d-269">0x800F</span></span>                          |
| <span data-ttu-id="7282d-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="7282d-270">System-Only</span></span>            | <span data-ttu-id="7282d-271">否</span><span class="sxs-lookup"><span data-stu-id="7282d-271">False</span></span>                           |
| <span data-ttu-id="7282d-272">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7282d-272">Is-Single-Valued</span></span>       | <span data-ttu-id="7282d-273">否</span><span class="sxs-lookup"><span data-stu-id="7282d-273">False</span></span>                           |
| <span data-ttu-id="7282d-274">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7282d-274">Is Indexed</span></span>             | <span data-ttu-id="7282d-275">對</span><span class="sxs-lookup"><span data-stu-id="7282d-275">True</span></span>                            |
| <span data-ttu-id="7282d-276">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7282d-276">In Global Catalog</span></span>      | <span data-ttu-id="7282d-277">否</span><span class="sxs-lookup"><span data-stu-id="7282d-277">False</span></span>                           |
| <span data-ttu-id="7282d-278">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7282d-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="7282d-279">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7282d-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7282d-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7282d-280">Range-Lower</span></span>            | <span data-ttu-id="7282d-281">1</span><span class="sxs-lookup"><span data-stu-id="7282d-281">1</span></span>                               |
| <span data-ttu-id="7282d-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7282d-282">Range-Upper</span></span>            | <span data-ttu-id="7282d-283">1123</span><span class="sxs-lookup"><span data-stu-id="7282d-283">1123</span></span>                            |
| <span data-ttu-id="7282d-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-284">Search-Flags</span></span>           | <span data-ttu-id="7282d-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7282d-285">0x00000005</span></span>                      |
| <span data-ttu-id="7282d-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-286">System-Flags</span></span>           | <span data-ttu-id="7282d-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7282d-287">0x00000010</span></span>                      |
| <span data-ttu-id="7282d-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7282d-288">Classes used in</span></span>        | [<span data-ttu-id="7282d-289">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7282d-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7282d-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7282d-290">Windows Server 2012</span></span>



| <span data-ttu-id="7282d-291">進入</span><span class="sxs-lookup"><span data-stu-id="7282d-291">Entry</span></span> | <span data-ttu-id="7282d-292">值</span><span class="sxs-lookup"><span data-stu-id="7282d-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7282d-293">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7282d-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7282d-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7282d-294">MAPI-Id</span></span>                | <span data-ttu-id="7282d-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="7282d-295">0x800F</span></span>                          |
| <span data-ttu-id="7282d-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="7282d-296">System-Only</span></span>            | <span data-ttu-id="7282d-297">否</span><span class="sxs-lookup"><span data-stu-id="7282d-297">False</span></span>                           |
| <span data-ttu-id="7282d-298">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7282d-298">Is-Single-Valued</span></span>       | <span data-ttu-id="7282d-299">否</span><span class="sxs-lookup"><span data-stu-id="7282d-299">False</span></span>                           |
| <span data-ttu-id="7282d-300">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7282d-300">Is Indexed</span></span>             | <span data-ttu-id="7282d-301">對</span><span class="sxs-lookup"><span data-stu-id="7282d-301">True</span></span>                            |
| <span data-ttu-id="7282d-302">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7282d-302">In Global Catalog</span></span>      | <span data-ttu-id="7282d-303">否</span><span class="sxs-lookup"><span data-stu-id="7282d-303">False</span></span>                           |
| <span data-ttu-id="7282d-304">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7282d-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="7282d-305">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7282d-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7282d-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7282d-306">Range-Lower</span></span>            | <span data-ttu-id="7282d-307">1</span><span class="sxs-lookup"><span data-stu-id="7282d-307">1</span></span>                               |
| <span data-ttu-id="7282d-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7282d-308">Range-Upper</span></span>            | <span data-ttu-id="7282d-309">1123</span><span class="sxs-lookup"><span data-stu-id="7282d-309">1123</span></span>                            |
| <span data-ttu-id="7282d-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-310">Search-Flags</span></span>           | <span data-ttu-id="7282d-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7282d-311">0x00000005</span></span>                      |
| <span data-ttu-id="7282d-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7282d-312">System-Flags</span></span>           | <span data-ttu-id="7282d-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7282d-313">0x00000010</span></span>                      |
| <span data-ttu-id="7282d-314">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7282d-314">Classes used in</span></span>        | [<span data-ttu-id="7282d-315">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7282d-315">**Top**</span></span>](c-top.md)<br/> |



 

 






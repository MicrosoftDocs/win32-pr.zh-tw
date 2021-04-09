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
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="3a78a-106">Proxy-Addresses 屬性</span><span class="sxs-lookup"><span data-stu-id="3a78a-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="3a78a-107">Proxy 位址是在外部郵件系統中辨識 Microsoft Exchange Server 收件者物件的位址。</span><span class="sxs-lookup"><span data-stu-id="3a78a-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="3a78a-108">所有收件者物件都需要 Proxy 位址，例如自訂收件者和通訊群組清單。</span><span class="sxs-lookup"><span data-stu-id="3a78a-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="3a78a-109">進入</span><span class="sxs-lookup"><span data-stu-id="3a78a-109">Entry</span></span> | <span data-ttu-id="3a78a-110">值</span><span class="sxs-lookup"><span data-stu-id="3a78a-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a78a-111">CN</span><span class="sxs-lookup"><span data-stu-id="3a78a-111">CN</span></span>                | <span data-ttu-id="3a78a-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="3a78a-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="3a78a-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3a78a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3a78a-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="3a78a-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="3a78a-115">大小</span><span class="sxs-lookup"><span data-stu-id="3a78a-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="3a78a-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3a78a-116">Update Privilege</span></span>  | <span data-ttu-id="3a78a-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="3a78a-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="3a78a-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3a78a-118">Update Frequency</span></span>  | <span data-ttu-id="3a78a-119">在安裝網址類別型時，由 Address-Type directory 物件提供的 DLL 所建立。</span><span class="sxs-lookup"><span data-stu-id="3a78a-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="3a78a-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3a78a-120">Attribute-Id</span></span>      | <span data-ttu-id="3a78a-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="3a78a-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="3a78a-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3a78a-122">System-Id-Guid</span></span>    | <span data-ttu-id="3a78a-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3a78a-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="3a78a-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a78a-124">Syntax</span></span>            | [<span data-ttu-id="3a78a-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3a78a-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="3a78a-126">實作</span><span class="sxs-lookup"><span data-stu-id="3a78a-126">Implementations</span></span>

-   [<span data-ttu-id="3a78a-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3a78a-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3a78a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3a78a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3a78a-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="3a78a-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3a78a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3a78a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3a78a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3a78a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3a78a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3a78a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3a78a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3a78a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3a78a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3a78a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="3a78a-135">進入</span><span class="sxs-lookup"><span data-stu-id="3a78a-135">Entry</span></span> | <span data-ttu-id="3a78a-136">值</span><span class="sxs-lookup"><span data-stu-id="3a78a-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3a78a-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3a78a-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3a78a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a78a-138">MAPI-Id</span></span>                | <span data-ttu-id="3a78a-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="3a78a-139">0x800F</span></span>                          |
| <span data-ttu-id="3a78a-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a78a-140">System-Only</span></span>            | <span data-ttu-id="3a78a-141">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-141">False</span></span>                           |
| <span data-ttu-id="3a78a-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3a78a-142">Is-Single-Valued</span></span>       | <span data-ttu-id="3a78a-143">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-143">False</span></span>                           |
| <span data-ttu-id="3a78a-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3a78a-144">Is Indexed</span></span>             | <span data-ttu-id="3a78a-145">對</span><span class="sxs-lookup"><span data-stu-id="3a78a-145">True</span></span>                            |
| <span data-ttu-id="3a78a-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3a78a-146">In Global Catalog</span></span>      | <span data-ttu-id="3a78a-147">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-147">False</span></span>                           |
| <span data-ttu-id="3a78a-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3a78a-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a78a-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3a78a-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3a78a-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a78a-150">Range-Lower</span></span>            | <span data-ttu-id="3a78a-151">1</span><span class="sxs-lookup"><span data-stu-id="3a78a-151">1</span></span>                               |
| <span data-ttu-id="3a78a-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a78a-152">Range-Upper</span></span>            | <span data-ttu-id="3a78a-153">1123</span><span class="sxs-lookup"><span data-stu-id="3a78a-153">1123</span></span>                            |
| <span data-ttu-id="3a78a-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-154">Search-Flags</span></span>           | <span data-ttu-id="3a78a-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="3a78a-155">0x00000005</span></span>                      |
| <span data-ttu-id="3a78a-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-156">System-Flags</span></span>           | <span data-ttu-id="3a78a-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a78a-157">0x00000010</span></span>                      |
| <span data-ttu-id="3a78a-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3a78a-158">Classes used in</span></span>        | [<span data-ttu-id="3a78a-159">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="3a78a-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3a78a-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3a78a-160">Windows Server 2003</span></span>



| <span data-ttu-id="3a78a-161">進入</span><span class="sxs-lookup"><span data-stu-id="3a78a-161">Entry</span></span> | <span data-ttu-id="3a78a-162">值</span><span class="sxs-lookup"><span data-stu-id="3a78a-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3a78a-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3a78a-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3a78a-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a78a-164">MAPI-Id</span></span>                | <span data-ttu-id="3a78a-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="3a78a-165">0x800F</span></span>                          |
| <span data-ttu-id="3a78a-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a78a-166">System-Only</span></span>            | <span data-ttu-id="3a78a-167">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-167">False</span></span>                           |
| <span data-ttu-id="3a78a-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3a78a-168">Is-Single-Valued</span></span>       | <span data-ttu-id="3a78a-169">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-169">False</span></span>                           |
| <span data-ttu-id="3a78a-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3a78a-170">Is Indexed</span></span>             | <span data-ttu-id="3a78a-171">對</span><span class="sxs-lookup"><span data-stu-id="3a78a-171">True</span></span>                            |
| <span data-ttu-id="3a78a-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3a78a-172">In Global Catalog</span></span>      | <span data-ttu-id="3a78a-173">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-173">False</span></span>                           |
| <span data-ttu-id="3a78a-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3a78a-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a78a-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3a78a-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3a78a-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a78a-176">Range-Lower</span></span>            | <span data-ttu-id="3a78a-177">1</span><span class="sxs-lookup"><span data-stu-id="3a78a-177">1</span></span>                               |
| <span data-ttu-id="3a78a-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a78a-178">Range-Upper</span></span>            | <span data-ttu-id="3a78a-179">1123</span><span class="sxs-lookup"><span data-stu-id="3a78a-179">1123</span></span>                            |
| <span data-ttu-id="3a78a-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-180">Search-Flags</span></span>           | <span data-ttu-id="3a78a-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="3a78a-181">0x00000005</span></span>                      |
| <span data-ttu-id="3a78a-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-182">System-Flags</span></span>           | <span data-ttu-id="3a78a-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a78a-183">0x00000010</span></span>                      |
| <span data-ttu-id="3a78a-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3a78a-184">Classes used in</span></span>        | [<span data-ttu-id="3a78a-185">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="3a78a-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3a78a-186">亞當</span><span class="sxs-lookup"><span data-stu-id="3a78a-186">ADAM</span></span>



| <span data-ttu-id="3a78a-187">進入</span><span class="sxs-lookup"><span data-stu-id="3a78a-187">Entry</span></span> | <span data-ttu-id="3a78a-188">值</span><span class="sxs-lookup"><span data-stu-id="3a78a-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3a78a-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3a78a-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3a78a-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a78a-190">MAPI-Id</span></span>                | <span data-ttu-id="3a78a-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="3a78a-191">0x800F</span></span>                          |
| <span data-ttu-id="3a78a-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a78a-192">System-Only</span></span>            | <span data-ttu-id="3a78a-193">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-193">False</span></span>                           |
| <span data-ttu-id="3a78a-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3a78a-194">Is-Single-Valued</span></span>       | <span data-ttu-id="3a78a-195">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-195">False</span></span>                           |
| <span data-ttu-id="3a78a-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3a78a-196">Is Indexed</span></span>             | <span data-ttu-id="3a78a-197">對</span><span class="sxs-lookup"><span data-stu-id="3a78a-197">True</span></span>                            |
| <span data-ttu-id="3a78a-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3a78a-198">In Global Catalog</span></span>      | <span data-ttu-id="3a78a-199">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-199">False</span></span>                           |
| <span data-ttu-id="3a78a-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3a78a-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a78a-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3a78a-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3a78a-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a78a-202">Range-Lower</span></span>            | <span data-ttu-id="3a78a-203">1</span><span class="sxs-lookup"><span data-stu-id="3a78a-203">1</span></span>                               |
| <span data-ttu-id="3a78a-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a78a-204">Range-Upper</span></span>            | <span data-ttu-id="3a78a-205">1123</span><span class="sxs-lookup"><span data-stu-id="3a78a-205">1123</span></span>                            |
| <span data-ttu-id="3a78a-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-206">Search-Flags</span></span>           | <span data-ttu-id="3a78a-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="3a78a-207">0x00000005</span></span>                      |
| <span data-ttu-id="3a78a-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-208">System-Flags</span></span>           | <span data-ttu-id="3a78a-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a78a-209">0x00000010</span></span>                      |
| <span data-ttu-id="3a78a-210">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3a78a-210">Classes used in</span></span>        | [<span data-ttu-id="3a78a-211">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="3a78a-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3a78a-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3a78a-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3a78a-213">進入</span><span class="sxs-lookup"><span data-stu-id="3a78a-213">Entry</span></span> | <span data-ttu-id="3a78a-214">值</span><span class="sxs-lookup"><span data-stu-id="3a78a-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3a78a-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3a78a-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3a78a-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a78a-216">MAPI-Id</span></span>                | <span data-ttu-id="3a78a-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="3a78a-217">0x800F</span></span>                          |
| <span data-ttu-id="3a78a-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a78a-218">System-Only</span></span>            | <span data-ttu-id="3a78a-219">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-219">False</span></span>                           |
| <span data-ttu-id="3a78a-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3a78a-220">Is-Single-Valued</span></span>       | <span data-ttu-id="3a78a-221">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-221">False</span></span>                           |
| <span data-ttu-id="3a78a-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3a78a-222">Is Indexed</span></span>             | <span data-ttu-id="3a78a-223">對</span><span class="sxs-lookup"><span data-stu-id="3a78a-223">True</span></span>                            |
| <span data-ttu-id="3a78a-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3a78a-224">In Global Catalog</span></span>      | <span data-ttu-id="3a78a-225">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-225">False</span></span>                           |
| <span data-ttu-id="3a78a-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3a78a-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a78a-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3a78a-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3a78a-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a78a-228">Range-Lower</span></span>            | <span data-ttu-id="3a78a-229">1</span><span class="sxs-lookup"><span data-stu-id="3a78a-229">1</span></span>                               |
| <span data-ttu-id="3a78a-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a78a-230">Range-Upper</span></span>            | <span data-ttu-id="3a78a-231">1123</span><span class="sxs-lookup"><span data-stu-id="3a78a-231">1123</span></span>                            |
| <span data-ttu-id="3a78a-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-232">Search-Flags</span></span>           | <span data-ttu-id="3a78a-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="3a78a-233">0x00000005</span></span>                      |
| <span data-ttu-id="3a78a-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-234">System-Flags</span></span>           | <span data-ttu-id="3a78a-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a78a-235">0x00000010</span></span>                      |
| <span data-ttu-id="3a78a-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3a78a-236">Classes used in</span></span>        | [<span data-ttu-id="3a78a-237">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="3a78a-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3a78a-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a78a-238">Windows Server 2008</span></span>



| <span data-ttu-id="3a78a-239">進入</span><span class="sxs-lookup"><span data-stu-id="3a78a-239">Entry</span></span> | <span data-ttu-id="3a78a-240">值</span><span class="sxs-lookup"><span data-stu-id="3a78a-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3a78a-241">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3a78a-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3a78a-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a78a-242">MAPI-Id</span></span>                | <span data-ttu-id="3a78a-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="3a78a-243">0x800F</span></span>                          |
| <span data-ttu-id="3a78a-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a78a-244">System-Only</span></span>            | <span data-ttu-id="3a78a-245">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-245">False</span></span>                           |
| <span data-ttu-id="3a78a-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3a78a-246">Is-Single-Valued</span></span>       | <span data-ttu-id="3a78a-247">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-247">False</span></span>                           |
| <span data-ttu-id="3a78a-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3a78a-248">Is Indexed</span></span>             | <span data-ttu-id="3a78a-249">對</span><span class="sxs-lookup"><span data-stu-id="3a78a-249">True</span></span>                            |
| <span data-ttu-id="3a78a-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3a78a-250">In Global Catalog</span></span>      | <span data-ttu-id="3a78a-251">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-251">False</span></span>                           |
| <span data-ttu-id="3a78a-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3a78a-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a78a-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3a78a-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3a78a-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a78a-254">Range-Lower</span></span>            | <span data-ttu-id="3a78a-255">1</span><span class="sxs-lookup"><span data-stu-id="3a78a-255">1</span></span>                               |
| <span data-ttu-id="3a78a-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a78a-256">Range-Upper</span></span>            | <span data-ttu-id="3a78a-257">1123</span><span class="sxs-lookup"><span data-stu-id="3a78a-257">1123</span></span>                            |
| <span data-ttu-id="3a78a-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-258">Search-Flags</span></span>           | <span data-ttu-id="3a78a-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="3a78a-259">0x00000005</span></span>                      |
| <span data-ttu-id="3a78a-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-260">System-Flags</span></span>           | <span data-ttu-id="3a78a-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a78a-261">0x00000010</span></span>                      |
| <span data-ttu-id="3a78a-262">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3a78a-262">Classes used in</span></span>        | [<span data-ttu-id="3a78a-263">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="3a78a-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3a78a-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3a78a-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3a78a-265">進入</span><span class="sxs-lookup"><span data-stu-id="3a78a-265">Entry</span></span> | <span data-ttu-id="3a78a-266">值</span><span class="sxs-lookup"><span data-stu-id="3a78a-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3a78a-267">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3a78a-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3a78a-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a78a-268">MAPI-Id</span></span>                | <span data-ttu-id="3a78a-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="3a78a-269">0x800F</span></span>                          |
| <span data-ttu-id="3a78a-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a78a-270">System-Only</span></span>            | <span data-ttu-id="3a78a-271">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-271">False</span></span>                           |
| <span data-ttu-id="3a78a-272">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3a78a-272">Is-Single-Valued</span></span>       | <span data-ttu-id="3a78a-273">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-273">False</span></span>                           |
| <span data-ttu-id="3a78a-274">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3a78a-274">Is Indexed</span></span>             | <span data-ttu-id="3a78a-275">對</span><span class="sxs-lookup"><span data-stu-id="3a78a-275">True</span></span>                            |
| <span data-ttu-id="3a78a-276">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3a78a-276">In Global Catalog</span></span>      | <span data-ttu-id="3a78a-277">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-277">False</span></span>                           |
| <span data-ttu-id="3a78a-278">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3a78a-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a78a-279">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3a78a-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3a78a-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a78a-280">Range-Lower</span></span>            | <span data-ttu-id="3a78a-281">1</span><span class="sxs-lookup"><span data-stu-id="3a78a-281">1</span></span>                               |
| <span data-ttu-id="3a78a-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a78a-282">Range-Upper</span></span>            | <span data-ttu-id="3a78a-283">1123</span><span class="sxs-lookup"><span data-stu-id="3a78a-283">1123</span></span>                            |
| <span data-ttu-id="3a78a-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-284">Search-Flags</span></span>           | <span data-ttu-id="3a78a-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="3a78a-285">0x00000005</span></span>                      |
| <span data-ttu-id="3a78a-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-286">System-Flags</span></span>           | <span data-ttu-id="3a78a-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a78a-287">0x00000010</span></span>                      |
| <span data-ttu-id="3a78a-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3a78a-288">Classes used in</span></span>        | [<span data-ttu-id="3a78a-289">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="3a78a-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3a78a-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a78a-290">Windows Server 2012</span></span>



| <span data-ttu-id="3a78a-291">進入</span><span class="sxs-lookup"><span data-stu-id="3a78a-291">Entry</span></span> | <span data-ttu-id="3a78a-292">值</span><span class="sxs-lookup"><span data-stu-id="3a78a-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3a78a-293">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3a78a-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3a78a-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a78a-294">MAPI-Id</span></span>                | <span data-ttu-id="3a78a-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="3a78a-295">0x800F</span></span>                          |
| <span data-ttu-id="3a78a-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a78a-296">System-Only</span></span>            | <span data-ttu-id="3a78a-297">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-297">False</span></span>                           |
| <span data-ttu-id="3a78a-298">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3a78a-298">Is-Single-Valued</span></span>       | <span data-ttu-id="3a78a-299">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-299">False</span></span>                           |
| <span data-ttu-id="3a78a-300">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3a78a-300">Is Indexed</span></span>             | <span data-ttu-id="3a78a-301">對</span><span class="sxs-lookup"><span data-stu-id="3a78a-301">True</span></span>                            |
| <span data-ttu-id="3a78a-302">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3a78a-302">In Global Catalog</span></span>      | <span data-ttu-id="3a78a-303">否</span><span class="sxs-lookup"><span data-stu-id="3a78a-303">False</span></span>                           |
| <span data-ttu-id="3a78a-304">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3a78a-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a78a-305">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3a78a-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3a78a-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a78a-306">Range-Lower</span></span>            | <span data-ttu-id="3a78a-307">1</span><span class="sxs-lookup"><span data-stu-id="3a78a-307">1</span></span>                               |
| <span data-ttu-id="3a78a-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a78a-308">Range-Upper</span></span>            | <span data-ttu-id="3a78a-309">1123</span><span class="sxs-lookup"><span data-stu-id="3a78a-309">1123</span></span>                            |
| <span data-ttu-id="3a78a-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-310">Search-Flags</span></span>           | <span data-ttu-id="3a78a-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="3a78a-311">0x00000005</span></span>                      |
| <span data-ttu-id="3a78a-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a78a-312">System-Flags</span></span>           | <span data-ttu-id="3a78a-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a78a-313">0x00000010</span></span>                      |
| <span data-ttu-id="3a78a-314">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3a78a-314">Classes used in</span></span>        | [<span data-ttu-id="3a78a-315">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="3a78a-315">**Top**</span></span>](c-top.md)<br/> |



 

 






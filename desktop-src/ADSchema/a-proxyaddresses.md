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
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="4a8a5-106">Proxy-Addresses 屬性</span><span class="sxs-lookup"><span data-stu-id="4a8a5-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="4a8a5-107">Proxy 位址是在外部郵件系統中辨識 Microsoft Exchange Server 收件者物件的位址。</span><span class="sxs-lookup"><span data-stu-id="4a8a5-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="4a8a5-108">所有收件者物件都需要 Proxy 位址，例如自訂收件者和通訊群組清單。</span><span class="sxs-lookup"><span data-stu-id="4a8a5-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="4a8a5-109">進入</span><span class="sxs-lookup"><span data-stu-id="4a8a5-109">Entry</span></span> | <span data-ttu-id="4a8a5-110">值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8a5-111">CN</span><span class="sxs-lookup"><span data-stu-id="4a8a5-111">CN</span></span>                | <span data-ttu-id="4a8a5-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="4a8a5-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="4a8a5-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4a8a5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4a8a5-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="4a8a5-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="4a8a5-115">大小</span><span class="sxs-lookup"><span data-stu-id="4a8a5-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="4a8a5-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4a8a5-116">Update Privilege</span></span>  | <span data-ttu-id="4a8a5-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="4a8a5-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="4a8a5-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4a8a5-118">Update Frequency</span></span>  | <span data-ttu-id="4a8a5-119">在安裝網址類別型時，由 Address-Type directory 物件提供的 DLL 所建立。</span><span class="sxs-lookup"><span data-stu-id="4a8a5-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="4a8a5-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4a8a5-120">Attribute-Id</span></span>      | <span data-ttu-id="4a8a5-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="4a8a5-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="4a8a5-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4a8a5-122">System-Id-Guid</span></span>    | <span data-ttu-id="4a8a5-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4a8a5-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="4a8a5-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a8a5-124">Syntax</span></span>            | [<span data-ttu-id="4a8a5-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="4a8a5-126">實作</span><span class="sxs-lookup"><span data-stu-id="4a8a5-126">Implementations</span></span>

-   [<span data-ttu-id="4a8a5-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4a8a5-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4a8a5-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4a8a5-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4a8a5-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4a8a5-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4a8a5-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4a8a5-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a8a5-134">Windows 2000 Server</span></span>



| <span data-ttu-id="4a8a5-135">進入</span><span class="sxs-lookup"><span data-stu-id="4a8a5-135">Entry</span></span> | <span data-ttu-id="4a8a5-136">值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a8a5-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4a8a5-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a8a5-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a8a5-138">MAPI-Id</span></span>                | <span data-ttu-id="4a8a5-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="4a8a5-139">0x800F</span></span>                          |
| <span data-ttu-id="4a8a5-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a8a5-140">System-Only</span></span>            | <span data-ttu-id="4a8a5-141">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-141">False</span></span>                           |
| <span data-ttu-id="4a8a5-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-142">Is-Single-Valued</span></span>       | <span data-ttu-id="4a8a5-143">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-143">False</span></span>                           |
| <span data-ttu-id="4a8a5-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4a8a5-144">Is Indexed</span></span>             | <span data-ttu-id="4a8a5-145">對</span><span class="sxs-lookup"><span data-stu-id="4a8a5-145">True</span></span>                            |
| <span data-ttu-id="4a8a5-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4a8a5-146">In Global Catalog</span></span>      | <span data-ttu-id="4a8a5-147">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-147">False</span></span>                           |
| <span data-ttu-id="4a8a5-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4a8a5-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a8a5-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4a8a5-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a8a5-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a8a5-150">Range-Lower</span></span>            | <span data-ttu-id="4a8a5-151">1</span><span class="sxs-lookup"><span data-stu-id="4a8a5-151">1</span></span>                               |
| <span data-ttu-id="4a8a5-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a8a5-152">Range-Upper</span></span>            | <span data-ttu-id="4a8a5-153">1123</span><span class="sxs-lookup"><span data-stu-id="4a8a5-153">1123</span></span>                            |
| <span data-ttu-id="4a8a5-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-154">Search-Flags</span></span>           | <span data-ttu-id="4a8a5-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4a8a5-155">0x00000005</span></span>                      |
| <span data-ttu-id="4a8a5-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-156">System-Flags</span></span>           | <span data-ttu-id="4a8a5-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a8a5-157">0x00000010</span></span>                      |
| <span data-ttu-id="4a8a5-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4a8a5-158">Classes used in</span></span>        | [<span data-ttu-id="4a8a5-159">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4a8a5-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a8a5-160">Windows Server 2003</span></span>



| <span data-ttu-id="4a8a5-161">進入</span><span class="sxs-lookup"><span data-stu-id="4a8a5-161">Entry</span></span> | <span data-ttu-id="4a8a5-162">值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a8a5-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4a8a5-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a8a5-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a8a5-164">MAPI-Id</span></span>                | <span data-ttu-id="4a8a5-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="4a8a5-165">0x800F</span></span>                          |
| <span data-ttu-id="4a8a5-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a8a5-166">System-Only</span></span>            | <span data-ttu-id="4a8a5-167">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-167">False</span></span>                           |
| <span data-ttu-id="4a8a5-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-168">Is-Single-Valued</span></span>       | <span data-ttu-id="4a8a5-169">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-169">False</span></span>                           |
| <span data-ttu-id="4a8a5-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4a8a5-170">Is Indexed</span></span>             | <span data-ttu-id="4a8a5-171">對</span><span class="sxs-lookup"><span data-stu-id="4a8a5-171">True</span></span>                            |
| <span data-ttu-id="4a8a5-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4a8a5-172">In Global Catalog</span></span>      | <span data-ttu-id="4a8a5-173">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-173">False</span></span>                           |
| <span data-ttu-id="4a8a5-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4a8a5-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a8a5-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4a8a5-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a8a5-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a8a5-176">Range-Lower</span></span>            | <span data-ttu-id="4a8a5-177">1</span><span class="sxs-lookup"><span data-stu-id="4a8a5-177">1</span></span>                               |
| <span data-ttu-id="4a8a5-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a8a5-178">Range-Upper</span></span>            | <span data-ttu-id="4a8a5-179">1123</span><span class="sxs-lookup"><span data-stu-id="4a8a5-179">1123</span></span>                            |
| <span data-ttu-id="4a8a5-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-180">Search-Flags</span></span>           | <span data-ttu-id="4a8a5-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4a8a5-181">0x00000005</span></span>                      |
| <span data-ttu-id="4a8a5-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-182">System-Flags</span></span>           | <span data-ttu-id="4a8a5-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a8a5-183">0x00000010</span></span>                      |
| <span data-ttu-id="4a8a5-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4a8a5-184">Classes used in</span></span>        | [<span data-ttu-id="4a8a5-185">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4a8a5-186">亞當</span><span class="sxs-lookup"><span data-stu-id="4a8a5-186">ADAM</span></span>



| <span data-ttu-id="4a8a5-187">進入</span><span class="sxs-lookup"><span data-stu-id="4a8a5-187">Entry</span></span> | <span data-ttu-id="4a8a5-188">值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a8a5-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4a8a5-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a8a5-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a8a5-190">MAPI-Id</span></span>                | <span data-ttu-id="4a8a5-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="4a8a5-191">0x800F</span></span>                          |
| <span data-ttu-id="4a8a5-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a8a5-192">System-Only</span></span>            | <span data-ttu-id="4a8a5-193">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-193">False</span></span>                           |
| <span data-ttu-id="4a8a5-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-194">Is-Single-Valued</span></span>       | <span data-ttu-id="4a8a5-195">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-195">False</span></span>                           |
| <span data-ttu-id="4a8a5-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4a8a5-196">Is Indexed</span></span>             | <span data-ttu-id="4a8a5-197">對</span><span class="sxs-lookup"><span data-stu-id="4a8a5-197">True</span></span>                            |
| <span data-ttu-id="4a8a5-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4a8a5-198">In Global Catalog</span></span>      | <span data-ttu-id="4a8a5-199">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-199">False</span></span>                           |
| <span data-ttu-id="4a8a5-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4a8a5-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a8a5-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4a8a5-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a8a5-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a8a5-202">Range-Lower</span></span>            | <span data-ttu-id="4a8a5-203">1</span><span class="sxs-lookup"><span data-stu-id="4a8a5-203">1</span></span>                               |
| <span data-ttu-id="4a8a5-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a8a5-204">Range-Upper</span></span>            | <span data-ttu-id="4a8a5-205">1123</span><span class="sxs-lookup"><span data-stu-id="4a8a5-205">1123</span></span>                            |
| <span data-ttu-id="4a8a5-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-206">Search-Flags</span></span>           | <span data-ttu-id="4a8a5-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4a8a5-207">0x00000005</span></span>                      |
| <span data-ttu-id="4a8a5-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-208">System-Flags</span></span>           | <span data-ttu-id="4a8a5-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a8a5-209">0x00000010</span></span>                      |
| <span data-ttu-id="4a8a5-210">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4a8a5-210">Classes used in</span></span>        | [<span data-ttu-id="4a8a5-211">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4a8a5-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4a8a5-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4a8a5-213">進入</span><span class="sxs-lookup"><span data-stu-id="4a8a5-213">Entry</span></span> | <span data-ttu-id="4a8a5-214">值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a8a5-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4a8a5-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a8a5-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a8a5-216">MAPI-Id</span></span>                | <span data-ttu-id="4a8a5-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="4a8a5-217">0x800F</span></span>                          |
| <span data-ttu-id="4a8a5-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a8a5-218">System-Only</span></span>            | <span data-ttu-id="4a8a5-219">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-219">False</span></span>                           |
| <span data-ttu-id="4a8a5-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-220">Is-Single-Valued</span></span>       | <span data-ttu-id="4a8a5-221">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-221">False</span></span>                           |
| <span data-ttu-id="4a8a5-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4a8a5-222">Is Indexed</span></span>             | <span data-ttu-id="4a8a5-223">對</span><span class="sxs-lookup"><span data-stu-id="4a8a5-223">True</span></span>                            |
| <span data-ttu-id="4a8a5-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4a8a5-224">In Global Catalog</span></span>      | <span data-ttu-id="4a8a5-225">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-225">False</span></span>                           |
| <span data-ttu-id="4a8a5-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4a8a5-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a8a5-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4a8a5-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a8a5-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a8a5-228">Range-Lower</span></span>            | <span data-ttu-id="4a8a5-229">1</span><span class="sxs-lookup"><span data-stu-id="4a8a5-229">1</span></span>                               |
| <span data-ttu-id="4a8a5-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a8a5-230">Range-Upper</span></span>            | <span data-ttu-id="4a8a5-231">1123</span><span class="sxs-lookup"><span data-stu-id="4a8a5-231">1123</span></span>                            |
| <span data-ttu-id="4a8a5-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-232">Search-Flags</span></span>           | <span data-ttu-id="4a8a5-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4a8a5-233">0x00000005</span></span>                      |
| <span data-ttu-id="4a8a5-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-234">System-Flags</span></span>           | <span data-ttu-id="4a8a5-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a8a5-235">0x00000010</span></span>                      |
| <span data-ttu-id="4a8a5-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4a8a5-236">Classes used in</span></span>        | [<span data-ttu-id="4a8a5-237">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4a8a5-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a8a5-238">Windows Server 2008</span></span>



| <span data-ttu-id="4a8a5-239">進入</span><span class="sxs-lookup"><span data-stu-id="4a8a5-239">Entry</span></span> | <span data-ttu-id="4a8a5-240">值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a8a5-241">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4a8a5-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a8a5-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a8a5-242">MAPI-Id</span></span>                | <span data-ttu-id="4a8a5-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="4a8a5-243">0x800F</span></span>                          |
| <span data-ttu-id="4a8a5-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a8a5-244">System-Only</span></span>            | <span data-ttu-id="4a8a5-245">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-245">False</span></span>                           |
| <span data-ttu-id="4a8a5-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-246">Is-Single-Valued</span></span>       | <span data-ttu-id="4a8a5-247">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-247">False</span></span>                           |
| <span data-ttu-id="4a8a5-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4a8a5-248">Is Indexed</span></span>             | <span data-ttu-id="4a8a5-249">對</span><span class="sxs-lookup"><span data-stu-id="4a8a5-249">True</span></span>                            |
| <span data-ttu-id="4a8a5-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4a8a5-250">In Global Catalog</span></span>      | <span data-ttu-id="4a8a5-251">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-251">False</span></span>                           |
| <span data-ttu-id="4a8a5-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4a8a5-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a8a5-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4a8a5-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a8a5-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a8a5-254">Range-Lower</span></span>            | <span data-ttu-id="4a8a5-255">1</span><span class="sxs-lookup"><span data-stu-id="4a8a5-255">1</span></span>                               |
| <span data-ttu-id="4a8a5-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a8a5-256">Range-Upper</span></span>            | <span data-ttu-id="4a8a5-257">1123</span><span class="sxs-lookup"><span data-stu-id="4a8a5-257">1123</span></span>                            |
| <span data-ttu-id="4a8a5-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-258">Search-Flags</span></span>           | <span data-ttu-id="4a8a5-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4a8a5-259">0x00000005</span></span>                      |
| <span data-ttu-id="4a8a5-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-260">System-Flags</span></span>           | <span data-ttu-id="4a8a5-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a8a5-261">0x00000010</span></span>                      |
| <span data-ttu-id="4a8a5-262">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4a8a5-262">Classes used in</span></span>        | [<span data-ttu-id="4a8a5-263">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4a8a5-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a8a5-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4a8a5-265">進入</span><span class="sxs-lookup"><span data-stu-id="4a8a5-265">Entry</span></span> | <span data-ttu-id="4a8a5-266">值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a8a5-267">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4a8a5-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a8a5-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a8a5-268">MAPI-Id</span></span>                | <span data-ttu-id="4a8a5-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="4a8a5-269">0x800F</span></span>                          |
| <span data-ttu-id="4a8a5-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a8a5-270">System-Only</span></span>            | <span data-ttu-id="4a8a5-271">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-271">False</span></span>                           |
| <span data-ttu-id="4a8a5-272">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-272">Is-Single-Valued</span></span>       | <span data-ttu-id="4a8a5-273">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-273">False</span></span>                           |
| <span data-ttu-id="4a8a5-274">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4a8a5-274">Is Indexed</span></span>             | <span data-ttu-id="4a8a5-275">對</span><span class="sxs-lookup"><span data-stu-id="4a8a5-275">True</span></span>                            |
| <span data-ttu-id="4a8a5-276">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4a8a5-276">In Global Catalog</span></span>      | <span data-ttu-id="4a8a5-277">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-277">False</span></span>                           |
| <span data-ttu-id="4a8a5-278">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4a8a5-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a8a5-279">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4a8a5-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a8a5-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a8a5-280">Range-Lower</span></span>            | <span data-ttu-id="4a8a5-281">1</span><span class="sxs-lookup"><span data-stu-id="4a8a5-281">1</span></span>                               |
| <span data-ttu-id="4a8a5-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a8a5-282">Range-Upper</span></span>            | <span data-ttu-id="4a8a5-283">1123</span><span class="sxs-lookup"><span data-stu-id="4a8a5-283">1123</span></span>                            |
| <span data-ttu-id="4a8a5-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-284">Search-Flags</span></span>           | <span data-ttu-id="4a8a5-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4a8a5-285">0x00000005</span></span>                      |
| <span data-ttu-id="4a8a5-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-286">System-Flags</span></span>           | <span data-ttu-id="4a8a5-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a8a5-287">0x00000010</span></span>                      |
| <span data-ttu-id="4a8a5-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4a8a5-288">Classes used in</span></span>        | [<span data-ttu-id="4a8a5-289">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4a8a5-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a8a5-290">Windows Server 2012</span></span>



| <span data-ttu-id="4a8a5-291">進入</span><span class="sxs-lookup"><span data-stu-id="4a8a5-291">Entry</span></span> | <span data-ttu-id="4a8a5-292">值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a8a5-293">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4a8a5-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a8a5-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a8a5-294">MAPI-Id</span></span>                | <span data-ttu-id="4a8a5-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="4a8a5-295">0x800F</span></span>                          |
| <span data-ttu-id="4a8a5-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a8a5-296">System-Only</span></span>            | <span data-ttu-id="4a8a5-297">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-297">False</span></span>                           |
| <span data-ttu-id="4a8a5-298">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4a8a5-298">Is-Single-Valued</span></span>       | <span data-ttu-id="4a8a5-299">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-299">False</span></span>                           |
| <span data-ttu-id="4a8a5-300">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4a8a5-300">Is Indexed</span></span>             | <span data-ttu-id="4a8a5-301">對</span><span class="sxs-lookup"><span data-stu-id="4a8a5-301">True</span></span>                            |
| <span data-ttu-id="4a8a5-302">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4a8a5-302">In Global Catalog</span></span>      | <span data-ttu-id="4a8a5-303">否</span><span class="sxs-lookup"><span data-stu-id="4a8a5-303">False</span></span>                           |
| <span data-ttu-id="4a8a5-304">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4a8a5-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a8a5-305">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4a8a5-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a8a5-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a8a5-306">Range-Lower</span></span>            | <span data-ttu-id="4a8a5-307">1</span><span class="sxs-lookup"><span data-stu-id="4a8a5-307">1</span></span>                               |
| <span data-ttu-id="4a8a5-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a8a5-308">Range-Upper</span></span>            | <span data-ttu-id="4a8a5-309">1123</span><span class="sxs-lookup"><span data-stu-id="4a8a5-309">1123</span></span>                            |
| <span data-ttu-id="4a8a5-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-310">Search-Flags</span></span>           | <span data-ttu-id="4a8a5-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4a8a5-311">0x00000005</span></span>                      |
| <span data-ttu-id="4a8a5-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a8a5-312">System-Flags</span></span>           | <span data-ttu-id="4a8a5-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a8a5-313">0x00000010</span></span>                      |
| <span data-ttu-id="4a8a5-314">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4a8a5-314">Classes used in</span></span>        | [<span data-ttu-id="4a8a5-315">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4a8a5-315">**Top**</span></span>](c-top.md)<br/> |



 

 






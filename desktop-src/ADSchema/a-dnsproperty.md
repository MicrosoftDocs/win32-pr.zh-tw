---
title: DNS-Property 屬性
description: 用來將二進位設定 (屬性) 儲存在 DNS 區域物件上。
ms.assetid: 55ea38cd-6b5b-4500-8e68-ae4d35e4b177
ms.tgt_platform: multiple
keywords:
- DNS-Property 屬性 AD 架構
- dNSProperty 屬性 AD 架構
topic_type:
- apiref
api_name:
- DNS-Property
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f8fd18f4524ec0bf61a609d21a361668ed295b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106967779"
---
# <a name="dns-property-attribute"></a><span data-ttu-id="1d1da-105">DNS-Property 屬性</span><span class="sxs-lookup"><span data-stu-id="1d1da-105">DNS-Property attribute</span></span>

<span data-ttu-id="1d1da-106">用來將二進位設定 (屬性) 儲存在 DNS 區域物件上。</span><span class="sxs-lookup"><span data-stu-id="1d1da-106">Used to store binary settings (properties) on DNS zone objects.</span></span>



| <span data-ttu-id="1d1da-107">進入</span><span class="sxs-lookup"><span data-stu-id="1d1da-107">Entry</span></span> | <span data-ttu-id="1d1da-108">值</span><span class="sxs-lookup"><span data-stu-id="1d1da-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="1d1da-109">CN</span><span class="sxs-lookup"><span data-stu-id="1d1da-109">CN</span></span>                | <span data-ttu-id="1d1da-110">DNS-Property</span><span class="sxs-lookup"><span data-stu-id="1d1da-110">DNS-Property</span></span>                                          |
| <span data-ttu-id="1d1da-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1d1da-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1d1da-112">dNSProperty</span><span class="sxs-lookup"><span data-stu-id="1d1da-112">dNSProperty</span></span>                                           |
| <span data-ttu-id="1d1da-113">大小</span><span class="sxs-lookup"><span data-stu-id="1d1da-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="1d1da-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1d1da-114">Update Privilege</span></span>  | <span data-ttu-id="1d1da-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="1d1da-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="1d1da-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1d1da-116">Update Frequency</span></span>  | <span data-ttu-id="1d1da-117">每次 DNS 區域記錄變更時。</span><span class="sxs-lookup"><span data-stu-id="1d1da-117">Whenever DNS zone records change.</span></span>                     |
| <span data-ttu-id="1d1da-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1d1da-118">Attribute-Id</span></span>      | <span data-ttu-id="1d1da-119">1.2.840.113556.1.4.1306</span><span class="sxs-lookup"><span data-stu-id="1d1da-119">1.2.840.113556.1.4.1306</span></span>                               |
| <span data-ttu-id="1d1da-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1d1da-120">System-Id-Guid</span></span>    | <span data-ttu-id="1d1da-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="1d1da-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="1d1da-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d1da-122">Syntax</span></span>            | [<span data-ttu-id="1d1da-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="1d1da-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="1d1da-124">實作</span><span class="sxs-lookup"><span data-stu-id="1d1da-124">Implementations</span></span>

-   [<span data-ttu-id="1d1da-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1d1da-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1d1da-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1d1da-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1d1da-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1d1da-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1d1da-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1d1da-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1d1da-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1d1da-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1d1da-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1d1da-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1d1da-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d1da-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1d1da-132">進入</span><span class="sxs-lookup"><span data-stu-id="1d1da-132">Entry</span></span> | <span data-ttu-id="1d1da-133">值</span><span class="sxs-lookup"><span data-stu-id="1d1da-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1d1da-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d1da-134">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d1da-135">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d1da-136">System-Only</span></span>            | <span data-ttu-id="1d1da-137">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-137">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d1da-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1d1da-139">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-139">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d1da-140">Is Indexed</span></span>             | <span data-ttu-id="1d1da-141">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-141">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d1da-142">In Global Catalog</span></span>      | <span data-ttu-id="1d1da-143">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-143">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d1da-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d1da-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d1da-145">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="1d1da-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d1da-146">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d1da-147">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-148">Search-Flags</span></span>           | <span data-ttu-id="1d1da-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d1da-149">0x00000000</span></span>                                                                        |
| <span data-ttu-id="1d1da-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-150">System-Flags</span></span>           | <span data-ttu-id="1d1da-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d1da-151">0x00000010</span></span>                                                                        |
| <span data-ttu-id="1d1da-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d1da-152">Classes used in</span></span>        | [<span data-ttu-id="1d1da-153">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="1d1da-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="1d1da-154">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="1d1da-154">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1d1da-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d1da-155">Windows Server 2003</span></span>



| <span data-ttu-id="1d1da-156">進入</span><span class="sxs-lookup"><span data-stu-id="1d1da-156">Entry</span></span> | <span data-ttu-id="1d1da-157">值</span><span class="sxs-lookup"><span data-stu-id="1d1da-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1d1da-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d1da-158">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d1da-159">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d1da-160">System-Only</span></span>            | <span data-ttu-id="1d1da-161">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-161">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d1da-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1d1da-163">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-163">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d1da-164">Is Indexed</span></span>             | <span data-ttu-id="1d1da-165">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-165">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d1da-166">In Global Catalog</span></span>      | <span data-ttu-id="1d1da-167">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-167">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d1da-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d1da-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d1da-169">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="1d1da-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d1da-170">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d1da-171">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-172">Search-Flags</span></span>           | <span data-ttu-id="1d1da-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d1da-173">0x00000000</span></span>                                                                        |
| <span data-ttu-id="1d1da-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-174">System-Flags</span></span>           | <span data-ttu-id="1d1da-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d1da-175">0x00000010</span></span>                                                                        |
| <span data-ttu-id="1d1da-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d1da-176">Classes used in</span></span>        | [<span data-ttu-id="1d1da-177">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="1d1da-177">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="1d1da-178">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="1d1da-178">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1d1da-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1d1da-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1d1da-180">進入</span><span class="sxs-lookup"><span data-stu-id="1d1da-180">Entry</span></span> | <span data-ttu-id="1d1da-181">值</span><span class="sxs-lookup"><span data-stu-id="1d1da-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1d1da-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d1da-182">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d1da-183">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d1da-184">System-Only</span></span>            | <span data-ttu-id="1d1da-185">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-185">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d1da-186">Is-Single-Valued</span></span>       | <span data-ttu-id="1d1da-187">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-187">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d1da-188">Is Indexed</span></span>             | <span data-ttu-id="1d1da-189">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-189">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d1da-190">In Global Catalog</span></span>      | <span data-ttu-id="1d1da-191">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-191">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d1da-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d1da-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d1da-193">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="1d1da-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d1da-194">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d1da-195">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-196">Search-Flags</span></span>           | <span data-ttu-id="1d1da-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d1da-197">0x00000000</span></span>                                                                        |
| <span data-ttu-id="1d1da-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-198">System-Flags</span></span>           | <span data-ttu-id="1d1da-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d1da-199">0x00000010</span></span>                                                                        |
| <span data-ttu-id="1d1da-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d1da-200">Classes used in</span></span>        | [<span data-ttu-id="1d1da-201">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="1d1da-201">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="1d1da-202">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="1d1da-202">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1d1da-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d1da-203">Windows Server 2008</span></span>



| <span data-ttu-id="1d1da-204">進入</span><span class="sxs-lookup"><span data-stu-id="1d1da-204">Entry</span></span> | <span data-ttu-id="1d1da-205">值</span><span class="sxs-lookup"><span data-stu-id="1d1da-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1d1da-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d1da-206">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d1da-207">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d1da-208">System-Only</span></span>            | <span data-ttu-id="1d1da-209">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-209">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d1da-210">Is-Single-Valued</span></span>       | <span data-ttu-id="1d1da-211">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-211">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d1da-212">Is Indexed</span></span>             | <span data-ttu-id="1d1da-213">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-213">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d1da-214">In Global Catalog</span></span>      | <span data-ttu-id="1d1da-215">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-215">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d1da-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d1da-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d1da-217">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="1d1da-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d1da-218">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d1da-219">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-220">Search-Flags</span></span>           | <span data-ttu-id="1d1da-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d1da-221">0x00000000</span></span>                                                                        |
| <span data-ttu-id="1d1da-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-222">System-Flags</span></span>           | <span data-ttu-id="1d1da-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d1da-223">0x00000010</span></span>                                                                        |
| <span data-ttu-id="1d1da-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d1da-224">Classes used in</span></span>        | [<span data-ttu-id="1d1da-225">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="1d1da-225">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="1d1da-226">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="1d1da-226">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1d1da-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d1da-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1d1da-228">進入</span><span class="sxs-lookup"><span data-stu-id="1d1da-228">Entry</span></span> | <span data-ttu-id="1d1da-229">值</span><span class="sxs-lookup"><span data-stu-id="1d1da-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1d1da-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d1da-230">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d1da-231">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d1da-232">System-Only</span></span>            | <span data-ttu-id="1d1da-233">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-233">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d1da-234">Is-Single-Valued</span></span>       | <span data-ttu-id="1d1da-235">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-235">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d1da-236">Is Indexed</span></span>             | <span data-ttu-id="1d1da-237">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-237">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d1da-238">In Global Catalog</span></span>      | <span data-ttu-id="1d1da-239">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-239">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d1da-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d1da-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d1da-241">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="1d1da-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d1da-242">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d1da-243">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-244">Search-Flags</span></span>           | <span data-ttu-id="1d1da-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d1da-245">0x00000000</span></span>                                                                        |
| <span data-ttu-id="1d1da-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-246">System-Flags</span></span>           | <span data-ttu-id="1d1da-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d1da-247">0x00000010</span></span>                                                                        |
| <span data-ttu-id="1d1da-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d1da-248">Classes used in</span></span>        | [<span data-ttu-id="1d1da-249">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="1d1da-249">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="1d1da-250">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="1d1da-250">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1d1da-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d1da-251">Windows Server 2012</span></span>



| <span data-ttu-id="1d1da-252">進入</span><span class="sxs-lookup"><span data-stu-id="1d1da-252">Entry</span></span> | <span data-ttu-id="1d1da-253">值</span><span class="sxs-lookup"><span data-stu-id="1d1da-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1d1da-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1d1da-254">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d1da-255">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="1d1da-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d1da-256">System-Only</span></span>            | <span data-ttu-id="1d1da-257">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-257">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1d1da-258">Is-Single-Valued</span></span>       | <span data-ttu-id="1d1da-259">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-259">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1d1da-260">Is Indexed</span></span>             | <span data-ttu-id="1d1da-261">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-261">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1d1da-262">In Global Catalog</span></span>      | <span data-ttu-id="1d1da-263">否</span><span class="sxs-lookup"><span data-stu-id="1d1da-263">False</span></span>                                                                             |
| <span data-ttu-id="1d1da-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1d1da-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d1da-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1d1da-265">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="1d1da-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d1da-266">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d1da-267">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="1d1da-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-268">Search-Flags</span></span>           | <span data-ttu-id="1d1da-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d1da-269">0x00000000</span></span>                                                                        |
| <span data-ttu-id="1d1da-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d1da-270">System-Flags</span></span>           | <span data-ttu-id="1d1da-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d1da-271">0x00000010</span></span>                                                                        |
| <span data-ttu-id="1d1da-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1d1da-272">Classes used in</span></span>        | [<span data-ttu-id="1d1da-273">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="1d1da-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="1d1da-274">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="1d1da-274">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 






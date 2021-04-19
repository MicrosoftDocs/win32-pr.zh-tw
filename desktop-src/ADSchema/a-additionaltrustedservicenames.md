---
title: 其他受信任的服務名稱屬性
description: 網域中可信任的服務清單。 AD 未使用。
ms.assetid: 0c574a99-4036-408b-807c-b4b3394624c7
ms.tgt_platform: multiple
keywords:
- 其他受信任的服務名稱屬性 AD 架構
- additionalTrustedServiceNames 屬性 AD 架構
topic_type:
- apiref
api_name:
- Additional-Trusted-Service-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8066190082cfe0f1bbb8825768ad135090a7a4f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971918"
---
# <a name="additional-trusted-service-names-attribute"></a><span data-ttu-id="a9385-106">其他受信任的服務名稱屬性</span><span class="sxs-lookup"><span data-stu-id="a9385-106">Additional-Trusted-Service-Names attribute</span></span>

<span data-ttu-id="a9385-107">網域中可信任的服務清單。</span><span class="sxs-lookup"><span data-stu-id="a9385-107">A list of services in the domain that can be trusted.</span></span> <span data-ttu-id="a9385-108">AD 未使用。</span><span class="sxs-lookup"><span data-stu-id="a9385-108">Not used by AD.</span></span>



| <span data-ttu-id="a9385-109">進入</span><span class="sxs-lookup"><span data-stu-id="a9385-109">Entry</span></span> | <span data-ttu-id="a9385-110">值</span><span class="sxs-lookup"><span data-stu-id="a9385-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a9385-111">CN</span><span class="sxs-lookup"><span data-stu-id="a9385-111">CN</span></span>                | <span data-ttu-id="a9385-112">其他受信任的服務名稱</span><span class="sxs-lookup"><span data-stu-id="a9385-112">Additional-Trusted-Service-Names</span></span>            |
| <span data-ttu-id="a9385-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a9385-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a9385-114">additionalTrustedServiceNames</span><span class="sxs-lookup"><span data-stu-id="a9385-114">additionalTrustedServiceNames</span></span>               |
| <span data-ttu-id="a9385-115">大小</span><span class="sxs-lookup"><span data-stu-id="a9385-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="a9385-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a9385-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="a9385-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a9385-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a9385-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a9385-118">Attribute-Id</span></span>      | <span data-ttu-id="a9385-119">1.2.840.113556.1.4.889</span><span class="sxs-lookup"><span data-stu-id="a9385-119">1.2.840.113556.1.4.889</span></span>                      |
| <span data-ttu-id="a9385-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a9385-120">System-Id-Guid</span></span>    | <span data-ttu-id="a9385-121">032160be-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a9385-121">032160be-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="a9385-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9385-122">Syntax</span></span>            | [<span data-ttu-id="a9385-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a9385-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a9385-124">實作</span><span class="sxs-lookup"><span data-stu-id="a9385-124">Implementations</span></span>

-   [<span data-ttu-id="a9385-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a9385-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a9385-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a9385-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a9385-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a9385-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a9385-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a9385-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a9385-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a9385-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a9385-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a9385-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a9385-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9385-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a9385-132">進入</span><span class="sxs-lookup"><span data-stu-id="a9385-132">Entry</span></span> | <span data-ttu-id="a9385-133">值</span><span class="sxs-lookup"><span data-stu-id="a9385-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a9385-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a9385-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9385-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9385-136">System-Only</span></span>            | <span data-ttu-id="a9385-137">否</span><span class="sxs-lookup"><span data-stu-id="a9385-137">False</span></span>                                                |
| <span data-ttu-id="a9385-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a9385-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a9385-139">否</span><span class="sxs-lookup"><span data-stu-id="a9385-139">False</span></span>                                                |
| <span data-ttu-id="a9385-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a9385-140">Is Indexed</span></span>             | <span data-ttu-id="a9385-141">否</span><span class="sxs-lookup"><span data-stu-id="a9385-141">False</span></span>                                                |
| <span data-ttu-id="a9385-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a9385-142">In Global Catalog</span></span>      | <span data-ttu-id="a9385-143">否</span><span class="sxs-lookup"><span data-stu-id="a9385-143">False</span></span>                                                |
| <span data-ttu-id="a9385-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a9385-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9385-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a9385-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a9385-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9385-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9385-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-148">Search-Flags</span></span>           | <span data-ttu-id="a9385-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9385-149">0x00000000</span></span>                                           |
| <span data-ttu-id="a9385-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-150">System-Flags</span></span>           | <span data-ttu-id="a9385-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9385-151">0x00000010</span></span>                                           |
| <span data-ttu-id="a9385-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a9385-152">Classes used in</span></span>        | [<span data-ttu-id="a9385-153">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a9385-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a9385-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9385-154">Windows Server 2003</span></span>



| <span data-ttu-id="a9385-155">進入</span><span class="sxs-lookup"><span data-stu-id="a9385-155">Entry</span></span> | <span data-ttu-id="a9385-156">值</span><span class="sxs-lookup"><span data-stu-id="a9385-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a9385-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a9385-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9385-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9385-159">System-Only</span></span>            | <span data-ttu-id="a9385-160">否</span><span class="sxs-lookup"><span data-stu-id="a9385-160">False</span></span>                                                |
| <span data-ttu-id="a9385-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a9385-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a9385-162">否</span><span class="sxs-lookup"><span data-stu-id="a9385-162">False</span></span>                                                |
| <span data-ttu-id="a9385-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a9385-163">Is Indexed</span></span>             | <span data-ttu-id="a9385-164">否</span><span class="sxs-lookup"><span data-stu-id="a9385-164">False</span></span>                                                |
| <span data-ttu-id="a9385-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a9385-165">In Global Catalog</span></span>      | <span data-ttu-id="a9385-166">否</span><span class="sxs-lookup"><span data-stu-id="a9385-166">False</span></span>                                                |
| <span data-ttu-id="a9385-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a9385-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9385-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a9385-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a9385-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9385-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9385-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-171">Search-Flags</span></span>           | <span data-ttu-id="a9385-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9385-172">0x00000000</span></span>                                           |
| <span data-ttu-id="a9385-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-173">System-Flags</span></span>           | <span data-ttu-id="a9385-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9385-174">0x00000010</span></span>                                           |
| <span data-ttu-id="a9385-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a9385-175">Classes used in</span></span>        | [<span data-ttu-id="a9385-176">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a9385-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a9385-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a9385-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a9385-178">進入</span><span class="sxs-lookup"><span data-stu-id="a9385-178">Entry</span></span> | <span data-ttu-id="a9385-179">值</span><span class="sxs-lookup"><span data-stu-id="a9385-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a9385-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a9385-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9385-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9385-182">System-Only</span></span>            | <span data-ttu-id="a9385-183">否</span><span class="sxs-lookup"><span data-stu-id="a9385-183">False</span></span>                                                |
| <span data-ttu-id="a9385-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a9385-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a9385-185">否</span><span class="sxs-lookup"><span data-stu-id="a9385-185">False</span></span>                                                |
| <span data-ttu-id="a9385-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a9385-186">Is Indexed</span></span>             | <span data-ttu-id="a9385-187">否</span><span class="sxs-lookup"><span data-stu-id="a9385-187">False</span></span>                                                |
| <span data-ttu-id="a9385-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a9385-188">In Global Catalog</span></span>      | <span data-ttu-id="a9385-189">否</span><span class="sxs-lookup"><span data-stu-id="a9385-189">False</span></span>                                                |
| <span data-ttu-id="a9385-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a9385-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9385-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a9385-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a9385-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9385-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9385-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-194">Search-Flags</span></span>           | <span data-ttu-id="a9385-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9385-195">0x00000000</span></span>                                           |
| <span data-ttu-id="a9385-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-196">System-Flags</span></span>           | <span data-ttu-id="a9385-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9385-197">0x00000010</span></span>                                           |
| <span data-ttu-id="a9385-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a9385-198">Classes used in</span></span>        | [<span data-ttu-id="a9385-199">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a9385-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a9385-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9385-200">Windows Server 2008</span></span>



| <span data-ttu-id="a9385-201">進入</span><span class="sxs-lookup"><span data-stu-id="a9385-201">Entry</span></span> | <span data-ttu-id="a9385-202">值</span><span class="sxs-lookup"><span data-stu-id="a9385-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a9385-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a9385-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9385-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9385-205">System-Only</span></span>            | <span data-ttu-id="a9385-206">否</span><span class="sxs-lookup"><span data-stu-id="a9385-206">False</span></span>                                                |
| <span data-ttu-id="a9385-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a9385-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a9385-208">否</span><span class="sxs-lookup"><span data-stu-id="a9385-208">False</span></span>                                                |
| <span data-ttu-id="a9385-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a9385-209">Is Indexed</span></span>             | <span data-ttu-id="a9385-210">否</span><span class="sxs-lookup"><span data-stu-id="a9385-210">False</span></span>                                                |
| <span data-ttu-id="a9385-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a9385-211">In Global Catalog</span></span>      | <span data-ttu-id="a9385-212">否</span><span class="sxs-lookup"><span data-stu-id="a9385-212">False</span></span>                                                |
| <span data-ttu-id="a9385-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a9385-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9385-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a9385-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a9385-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9385-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9385-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-217">Search-Flags</span></span>           | <span data-ttu-id="a9385-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9385-218">0x00000000</span></span>                                           |
| <span data-ttu-id="a9385-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-219">System-Flags</span></span>           | <span data-ttu-id="a9385-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9385-220">0x00000010</span></span>                                           |
| <span data-ttu-id="a9385-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a9385-221">Classes used in</span></span>        | [<span data-ttu-id="a9385-222">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a9385-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a9385-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9385-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a9385-224">進入</span><span class="sxs-lookup"><span data-stu-id="a9385-224">Entry</span></span> | <span data-ttu-id="a9385-225">值</span><span class="sxs-lookup"><span data-stu-id="a9385-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a9385-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a9385-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9385-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9385-228">System-Only</span></span>            | <span data-ttu-id="a9385-229">否</span><span class="sxs-lookup"><span data-stu-id="a9385-229">False</span></span>                                                |
| <span data-ttu-id="a9385-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a9385-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a9385-231">否</span><span class="sxs-lookup"><span data-stu-id="a9385-231">False</span></span>                                                |
| <span data-ttu-id="a9385-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a9385-232">Is Indexed</span></span>             | <span data-ttu-id="a9385-233">否</span><span class="sxs-lookup"><span data-stu-id="a9385-233">False</span></span>                                                |
| <span data-ttu-id="a9385-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a9385-234">In Global Catalog</span></span>      | <span data-ttu-id="a9385-235">否</span><span class="sxs-lookup"><span data-stu-id="a9385-235">False</span></span>                                                |
| <span data-ttu-id="a9385-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a9385-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9385-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a9385-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a9385-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9385-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9385-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-240">Search-Flags</span></span>           | <span data-ttu-id="a9385-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9385-241">0x00000000</span></span>                                           |
| <span data-ttu-id="a9385-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-242">System-Flags</span></span>           | <span data-ttu-id="a9385-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9385-243">0x00000010</span></span>                                           |
| <span data-ttu-id="a9385-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a9385-244">Classes used in</span></span>        | [<span data-ttu-id="a9385-245">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a9385-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a9385-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9385-246">Windows Server 2012</span></span>



| <span data-ttu-id="a9385-247">進入</span><span class="sxs-lookup"><span data-stu-id="a9385-247">Entry</span></span> | <span data-ttu-id="a9385-248">值</span><span class="sxs-lookup"><span data-stu-id="a9385-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a9385-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a9385-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9385-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a9385-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9385-251">System-Only</span></span>            | <span data-ttu-id="a9385-252">否</span><span class="sxs-lookup"><span data-stu-id="a9385-252">False</span></span>                                                |
| <span data-ttu-id="a9385-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a9385-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a9385-254">否</span><span class="sxs-lookup"><span data-stu-id="a9385-254">False</span></span>                                                |
| <span data-ttu-id="a9385-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a9385-255">Is Indexed</span></span>             | <span data-ttu-id="a9385-256">否</span><span class="sxs-lookup"><span data-stu-id="a9385-256">False</span></span>                                                |
| <span data-ttu-id="a9385-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a9385-257">In Global Catalog</span></span>      | <span data-ttu-id="a9385-258">否</span><span class="sxs-lookup"><span data-stu-id="a9385-258">False</span></span>                                                |
| <span data-ttu-id="a9385-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a9385-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9385-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a9385-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a9385-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9385-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9385-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a9385-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-263">Search-Flags</span></span>           | <span data-ttu-id="a9385-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9385-264">0x00000000</span></span>                                           |
| <span data-ttu-id="a9385-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9385-265">System-Flags</span></span>           | <span data-ttu-id="a9385-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9385-266">0x00000010</span></span>                                           |
| <span data-ttu-id="a9385-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a9385-267">Classes used in</span></span>        | [<span data-ttu-id="a9385-268">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a9385-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






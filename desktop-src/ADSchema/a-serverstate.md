---
title: Server-State 屬性
description: 指出伺服器是否已啟用或停用。
ms.assetid: e062cbcf-c845-4dfd-9e9b-e21079276a3c
ms.tgt_platform: multiple
keywords:
- Server-State 屬性 AD 架構
- serverState 屬性 AD 架構
topic_type:
- apiref
api_name:
- Server-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be4e236254486cd512eed480b380058048061fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106969016"
---
# <a name="server-state-attribute"></a><span data-ttu-id="c3e3f-105">Server-State 屬性</span><span class="sxs-lookup"><span data-stu-id="c3e3f-105">Server-State attribute</span></span>

<span data-ttu-id="c3e3f-106">指出伺服器是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="c3e3f-106">Indicates whether the server is enabled or disabled.</span></span> <span data-ttu-id="c3e3f-107">值為1表示已啟用伺服器。</span><span class="sxs-lookup"><span data-stu-id="c3e3f-107">A value of 1 indicates that the server is enabled.</span></span> <span data-ttu-id="c3e3f-108">值為2表示伺服器已停用。</span><span class="sxs-lookup"><span data-stu-id="c3e3f-108">A value of 2 indicates that the server is disabled.</span></span> <span data-ttu-id="c3e3f-109">所有其他值都無效。</span><span class="sxs-lookup"><span data-stu-id="c3e3f-109">All other values are invalid.</span></span>



| <span data-ttu-id="c3e3f-110">進入</span><span class="sxs-lookup"><span data-stu-id="c3e3f-110">Entry</span></span> | <span data-ttu-id="c3e3f-111">值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-111">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c3e3f-112">CN</span><span class="sxs-lookup"><span data-stu-id="c3e3f-112">CN</span></span>                | <span data-ttu-id="c3e3f-113">Server-State</span><span class="sxs-lookup"><span data-stu-id="c3e3f-113">Server-State</span></span>                         |
| <span data-ttu-id="c3e3f-114">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c3e3f-114">Ldap-Display-Name</span></span> | <span data-ttu-id="c3e3f-115">serverState</span><span class="sxs-lookup"><span data-stu-id="c3e3f-115">serverState</span></span>                          |
| <span data-ttu-id="c3e3f-116">大小</span><span class="sxs-lookup"><span data-stu-id="c3e3f-116">Size</span></span>              | \-                                   |
| <span data-ttu-id="c3e3f-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c3e3f-117">Update Privilege</span></span>  | <span data-ttu-id="c3e3f-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="c3e3f-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="c3e3f-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c3e3f-119">Update Frequency</span></span>  | <span data-ttu-id="c3e3f-120">當使用者的原則變更時。</span><span class="sxs-lookup"><span data-stu-id="c3e3f-120">When the policy for a user changes.</span></span>  |
| <span data-ttu-id="c3e3f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3e3f-121">Attribute-Id</span></span>      | <span data-ttu-id="c3e3f-122">1.2.840.113556.1.4.154</span><span class="sxs-lookup"><span data-stu-id="c3e3f-122">1.2.840.113556.1.4.154</span></span>               |
| <span data-ttu-id="c3e3f-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c3e3f-123">System-Id-Guid</span></span>    | <span data-ttu-id="c3e3f-124">bf967a34-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c3e3f-124">bf967a34-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="c3e3f-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3e3f-125">Syntax</span></span>            | [<span data-ttu-id="c3e3f-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c3e3f-127">實作</span><span class="sxs-lookup"><span data-stu-id="c3e3f-127">Implementations</span></span>

-   [<span data-ttu-id="c3e3f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c3e3f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c3e3f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c3e3f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3e3f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3e3f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c3e3f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c3e3f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c3e3f-135">進入</span><span class="sxs-lookup"><span data-stu-id="c3e3f-135">Entry</span></span> | <span data-ttu-id="c3e3f-136">值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-136">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="c3e3f-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3e3f-137">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3e3f-138">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3e3f-139">System-Only</span></span>            | <span data-ttu-id="c3e3f-140">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-140">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c3e3f-142">對</span><span class="sxs-lookup"><span data-stu-id="c3e3f-142">True</span></span>                                                  |
| <span data-ttu-id="c3e3f-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3e3f-143">Is Indexed</span></span>             | <span data-ttu-id="c3e3f-144">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-144">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3e3f-145">In Global Catalog</span></span>      | <span data-ttu-id="c3e3f-146">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-146">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3e3f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3e3f-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3e3f-148">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="c3e3f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3e3f-149">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3e3f-150">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-151">Search-Flags</span></span>           | <span data-ttu-id="c3e3f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3e3f-152">0x00000000</span></span>                                            |
| <span data-ttu-id="c3e3f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-153">System-Flags</span></span>           | <span data-ttu-id="c3e3f-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3e3f-154">0x00000011</span></span>                                            |
| <span data-ttu-id="c3e3f-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3e3f-155">Classes used in</span></span>        | [<span data-ttu-id="c3e3f-156">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c3e3f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3e3f-157">Windows Server 2003</span></span>



| <span data-ttu-id="c3e3f-158">進入</span><span class="sxs-lookup"><span data-stu-id="c3e3f-158">Entry</span></span> | <span data-ttu-id="c3e3f-159">值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-159">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="c3e3f-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3e3f-160">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3e3f-161">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3e3f-162">System-Only</span></span>            | <span data-ttu-id="c3e3f-163">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-163">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c3e3f-165">對</span><span class="sxs-lookup"><span data-stu-id="c3e3f-165">True</span></span>                                                  |
| <span data-ttu-id="c3e3f-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3e3f-166">Is Indexed</span></span>             | <span data-ttu-id="c3e3f-167">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-167">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3e3f-168">In Global Catalog</span></span>      | <span data-ttu-id="c3e3f-169">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-169">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3e3f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3e3f-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3e3f-171">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="c3e3f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3e3f-172">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3e3f-173">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-174">Search-Flags</span></span>           | <span data-ttu-id="c3e3f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3e3f-175">0x00000000</span></span>                                            |
| <span data-ttu-id="c3e3f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-176">System-Flags</span></span>           | <span data-ttu-id="c3e3f-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3e3f-177">0x00000011</span></span>                                            |
| <span data-ttu-id="c3e3f-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3e3f-178">Classes used in</span></span>        | [<span data-ttu-id="c3e3f-179">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c3e3f-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c3e3f-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c3e3f-181">進入</span><span class="sxs-lookup"><span data-stu-id="c3e3f-181">Entry</span></span> | <span data-ttu-id="c3e3f-182">值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-182">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="c3e3f-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3e3f-183">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3e3f-184">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3e3f-185">System-Only</span></span>            | <span data-ttu-id="c3e3f-186">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-186">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c3e3f-188">對</span><span class="sxs-lookup"><span data-stu-id="c3e3f-188">True</span></span>                                                  |
| <span data-ttu-id="c3e3f-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3e3f-189">Is Indexed</span></span>             | <span data-ttu-id="c3e3f-190">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-190">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3e3f-191">In Global Catalog</span></span>      | <span data-ttu-id="c3e3f-192">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-192">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3e3f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3e3f-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3e3f-194">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="c3e3f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3e3f-195">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3e3f-196">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-197">Search-Flags</span></span>           | <span data-ttu-id="c3e3f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3e3f-198">0x00000000</span></span>                                            |
| <span data-ttu-id="c3e3f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-199">System-Flags</span></span>           | <span data-ttu-id="c3e3f-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3e3f-200">0x00000011</span></span>                                            |
| <span data-ttu-id="c3e3f-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3e3f-201">Classes used in</span></span>        | [<span data-ttu-id="c3e3f-202">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c3e3f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3e3f-203">Windows Server 2008</span></span>



| <span data-ttu-id="c3e3f-204">進入</span><span class="sxs-lookup"><span data-stu-id="c3e3f-204">Entry</span></span> | <span data-ttu-id="c3e3f-205">值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-205">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="c3e3f-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3e3f-206">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3e3f-207">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3e3f-208">System-Only</span></span>            | <span data-ttu-id="c3e3f-209">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-209">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c3e3f-211">對</span><span class="sxs-lookup"><span data-stu-id="c3e3f-211">True</span></span>                                                  |
| <span data-ttu-id="c3e3f-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3e3f-212">Is Indexed</span></span>             | <span data-ttu-id="c3e3f-213">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-213">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3e3f-214">In Global Catalog</span></span>      | <span data-ttu-id="c3e3f-215">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-215">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3e3f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3e3f-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3e3f-217">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="c3e3f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3e3f-218">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3e3f-219">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-220">Search-Flags</span></span>           | <span data-ttu-id="c3e3f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3e3f-221">0x00000000</span></span>                                            |
| <span data-ttu-id="c3e3f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-222">System-Flags</span></span>           | <span data-ttu-id="c3e3f-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3e3f-223">0x00000011</span></span>                                            |
| <span data-ttu-id="c3e3f-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3e3f-224">Classes used in</span></span>        | [<span data-ttu-id="c3e3f-225">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-225">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3e3f-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3e3f-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3e3f-227">進入</span><span class="sxs-lookup"><span data-stu-id="c3e3f-227">Entry</span></span> | <span data-ttu-id="c3e3f-228">值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-228">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="c3e3f-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3e3f-229">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3e3f-230">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3e3f-231">System-Only</span></span>            | <span data-ttu-id="c3e3f-232">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-232">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c3e3f-234">對</span><span class="sxs-lookup"><span data-stu-id="c3e3f-234">True</span></span>                                                  |
| <span data-ttu-id="c3e3f-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3e3f-235">Is Indexed</span></span>             | <span data-ttu-id="c3e3f-236">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-236">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3e3f-237">In Global Catalog</span></span>      | <span data-ttu-id="c3e3f-238">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-238">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3e3f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3e3f-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3e3f-240">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="c3e3f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3e3f-241">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3e3f-242">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-243">Search-Flags</span></span>           | <span data-ttu-id="c3e3f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3e3f-244">0x00000000</span></span>                                            |
| <span data-ttu-id="c3e3f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-245">System-Flags</span></span>           | <span data-ttu-id="c3e3f-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3e3f-246">0x00000011</span></span>                                            |
| <span data-ttu-id="c3e3f-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3e3f-247">Classes used in</span></span>        | [<span data-ttu-id="c3e3f-248">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-248">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3e3f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3e3f-249">Windows Server 2012</span></span>



| <span data-ttu-id="c3e3f-250">進入</span><span class="sxs-lookup"><span data-stu-id="c3e3f-250">Entry</span></span> | <span data-ttu-id="c3e3f-251">值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-251">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="c3e3f-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3e3f-252">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3e3f-253">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="c3e3f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3e3f-254">System-Only</span></span>            | <span data-ttu-id="c3e3f-255">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-255">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3e3f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c3e3f-257">對</span><span class="sxs-lookup"><span data-stu-id="c3e3f-257">True</span></span>                                                  |
| <span data-ttu-id="c3e3f-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3e3f-258">Is Indexed</span></span>             | <span data-ttu-id="c3e3f-259">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-259">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3e3f-260">In Global Catalog</span></span>      | <span data-ttu-id="c3e3f-261">否</span><span class="sxs-lookup"><span data-stu-id="c3e3f-261">False</span></span>                                                 |
| <span data-ttu-id="c3e3f-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3e3f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3e3f-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3e3f-263">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="c3e3f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3e3f-264">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3e3f-265">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="c3e3f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-266">Search-Flags</span></span>           | <span data-ttu-id="c3e3f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3e3f-267">0x00000000</span></span>                                            |
| <span data-ttu-id="c3e3f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3e3f-268">System-Flags</span></span>           | <span data-ttu-id="c3e3f-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c3e3f-269">0x00000011</span></span>                                            |
| <span data-ttu-id="c3e3f-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3e3f-270">Classes used in</span></span>        | [<span data-ttu-id="c3e3f-271">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-271">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 






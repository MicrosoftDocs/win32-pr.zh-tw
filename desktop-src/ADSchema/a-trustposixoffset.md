---
title: Trust-Posix-Offset 屬性
description: 適用于受信任網域的可移植作業系統介面 (POSIX) 位移。
ms.assetid: a1263f9f-1577-44b8-b7cc-317a8ecb37f1
ms.tgt_platform: multiple
keywords:
- 信任-Posix-Offset 屬性 AD 架構
- trustPosixOffset 屬性 AD 架構
topic_type:
- apiref
api_name:
- Trust-Posix-Offset
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8f3dca090d44ea545dcc290b04d99131d50dc7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104025568"
---
# <a name="trust-posix-offset-attribute"></a><span data-ttu-id="d27e3-105">Trust-Posix-Offset 屬性</span><span class="sxs-lookup"><span data-stu-id="d27e3-105">Trust-Posix-Offset attribute</span></span>

<span data-ttu-id="d27e3-106">適用于受信任網域的可移植作業系統介面 (POSIX) 位移。</span><span class="sxs-lookup"><span data-stu-id="d27e3-106">The Portable Operating System Interface (POSIX) offset for the trusted domain.</span></span>



| <span data-ttu-id="d27e3-107">進入</span><span class="sxs-lookup"><span data-stu-id="d27e3-107">Entry</span></span> | <span data-ttu-id="d27e3-108">值</span><span class="sxs-lookup"><span data-stu-id="d27e3-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d27e3-109">CN</span><span class="sxs-lookup"><span data-stu-id="d27e3-109">CN</span></span>                | <span data-ttu-id="d27e3-110">信任-Posix-Offset</span><span class="sxs-lookup"><span data-stu-id="d27e3-110">Trust-Posix-Offset</span></span>                   |
| <span data-ttu-id="d27e3-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d27e3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d27e3-112">trustPosixOffset</span><span class="sxs-lookup"><span data-stu-id="d27e3-112">trustPosixOffset</span></span>                     |
| <span data-ttu-id="d27e3-113">大小</span><span class="sxs-lookup"><span data-stu-id="d27e3-113">Size</span></span>              | <span data-ttu-id="d27e3-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="d27e3-114">4 bytes</span></span>                              |
| <span data-ttu-id="d27e3-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d27e3-115">Update Privilege</span></span>  | <span data-ttu-id="d27e3-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="d27e3-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="d27e3-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d27e3-117">Update Frequency</span></span>  | <span data-ttu-id="d27e3-118">當新的信任建立時。</span><span class="sxs-lookup"><span data-stu-id="d27e3-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="d27e3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d27e3-119">Attribute-Id</span></span>      | <span data-ttu-id="d27e3-120">1.2.840.113556.1.4.134</span><span class="sxs-lookup"><span data-stu-id="d27e3-120">1.2.840.113556.1.4.134</span></span>               |
| <span data-ttu-id="d27e3-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d27e3-121">System-Id-Guid</span></span>    | <span data-ttu-id="d27e3-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d27e3-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="d27e3-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d27e3-123">Syntax</span></span>            | [<span data-ttu-id="d27e3-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="d27e3-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d27e3-125">實作</span><span class="sxs-lookup"><span data-stu-id="d27e3-125">Implementations</span></span>

-   [<span data-ttu-id="d27e3-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d27e3-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d27e3-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d27e3-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d27e3-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d27e3-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d27e3-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d27e3-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d27e3-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d27e3-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d27e3-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d27e3-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d27e3-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d27e3-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d27e3-133">進入</span><span class="sxs-lookup"><span data-stu-id="d27e3-133">Entry</span></span> | <span data-ttu-id="d27e3-134">值</span><span class="sxs-lookup"><span data-stu-id="d27e3-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d27e3-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d27e3-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27e3-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27e3-137">System-Only</span></span>            | <span data-ttu-id="d27e3-138">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-138">False</span></span>                                                |
| <span data-ttu-id="d27e3-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d27e3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d27e3-140">對</span><span class="sxs-lookup"><span data-stu-id="d27e3-140">True</span></span>                                                 |
| <span data-ttu-id="d27e3-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d27e3-141">Is Indexed</span></span>             | <span data-ttu-id="d27e3-142">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-142">False</span></span>                                                |
| <span data-ttu-id="d27e3-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d27e3-143">In Global Catalog</span></span>      | <span data-ttu-id="d27e3-144">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-144">False</span></span>                                                |
| <span data-ttu-id="d27e3-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d27e3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27e3-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d27e3-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d27e3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27e3-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27e3-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-149">Search-Flags</span></span>           | <span data-ttu-id="d27e3-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27e3-150">0x00000000</span></span>                                           |
| <span data-ttu-id="d27e3-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-151">System-Flags</span></span>           | <span data-ttu-id="d27e3-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27e3-152">0x00000010</span></span>                                           |
| <span data-ttu-id="d27e3-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d27e3-153">Classes used in</span></span>        | [<span data-ttu-id="d27e3-154">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="d27e3-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d27e3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d27e3-155">Windows Server 2003</span></span>



| <span data-ttu-id="d27e3-156">進入</span><span class="sxs-lookup"><span data-stu-id="d27e3-156">Entry</span></span> | <span data-ttu-id="d27e3-157">值</span><span class="sxs-lookup"><span data-stu-id="d27e3-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d27e3-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d27e3-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27e3-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27e3-160">System-Only</span></span>            | <span data-ttu-id="d27e3-161">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-161">False</span></span>                                                |
| <span data-ttu-id="d27e3-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d27e3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d27e3-163">對</span><span class="sxs-lookup"><span data-stu-id="d27e3-163">True</span></span>                                                 |
| <span data-ttu-id="d27e3-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d27e3-164">Is Indexed</span></span>             | <span data-ttu-id="d27e3-165">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-165">False</span></span>                                                |
| <span data-ttu-id="d27e3-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d27e3-166">In Global Catalog</span></span>      | <span data-ttu-id="d27e3-167">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-167">False</span></span>                                                |
| <span data-ttu-id="d27e3-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d27e3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27e3-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d27e3-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d27e3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27e3-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27e3-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-172">Search-Flags</span></span>           | <span data-ttu-id="d27e3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27e3-173">0x00000000</span></span>                                           |
| <span data-ttu-id="d27e3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-174">System-Flags</span></span>           | <span data-ttu-id="d27e3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27e3-175">0x00000010</span></span>                                           |
| <span data-ttu-id="d27e3-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d27e3-176">Classes used in</span></span>        | [<span data-ttu-id="d27e3-177">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="d27e3-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d27e3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d27e3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d27e3-179">進入</span><span class="sxs-lookup"><span data-stu-id="d27e3-179">Entry</span></span> | <span data-ttu-id="d27e3-180">值</span><span class="sxs-lookup"><span data-stu-id="d27e3-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d27e3-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d27e3-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27e3-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27e3-183">System-Only</span></span>            | <span data-ttu-id="d27e3-184">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-184">False</span></span>                                                |
| <span data-ttu-id="d27e3-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d27e3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d27e3-186">對</span><span class="sxs-lookup"><span data-stu-id="d27e3-186">True</span></span>                                                 |
| <span data-ttu-id="d27e3-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d27e3-187">Is Indexed</span></span>             | <span data-ttu-id="d27e3-188">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-188">False</span></span>                                                |
| <span data-ttu-id="d27e3-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d27e3-189">In Global Catalog</span></span>      | <span data-ttu-id="d27e3-190">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-190">False</span></span>                                                |
| <span data-ttu-id="d27e3-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d27e3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27e3-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d27e3-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d27e3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27e3-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27e3-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-195">Search-Flags</span></span>           | <span data-ttu-id="d27e3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27e3-196">0x00000000</span></span>                                           |
| <span data-ttu-id="d27e3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-197">System-Flags</span></span>           | <span data-ttu-id="d27e3-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27e3-198">0x00000010</span></span>                                           |
| <span data-ttu-id="d27e3-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d27e3-199">Classes used in</span></span>        | [<span data-ttu-id="d27e3-200">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="d27e3-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d27e3-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d27e3-201">Windows Server 2008</span></span>



| <span data-ttu-id="d27e3-202">進入</span><span class="sxs-lookup"><span data-stu-id="d27e3-202">Entry</span></span> | <span data-ttu-id="d27e3-203">值</span><span class="sxs-lookup"><span data-stu-id="d27e3-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d27e3-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d27e3-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27e3-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27e3-206">System-Only</span></span>            | <span data-ttu-id="d27e3-207">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-207">False</span></span>                                                |
| <span data-ttu-id="d27e3-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d27e3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d27e3-209">對</span><span class="sxs-lookup"><span data-stu-id="d27e3-209">True</span></span>                                                 |
| <span data-ttu-id="d27e3-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d27e3-210">Is Indexed</span></span>             | <span data-ttu-id="d27e3-211">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-211">False</span></span>                                                |
| <span data-ttu-id="d27e3-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d27e3-212">In Global Catalog</span></span>      | <span data-ttu-id="d27e3-213">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-213">False</span></span>                                                |
| <span data-ttu-id="d27e3-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d27e3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27e3-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d27e3-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d27e3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27e3-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27e3-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-218">Search-Flags</span></span>           | <span data-ttu-id="d27e3-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27e3-219">0x00000000</span></span>                                           |
| <span data-ttu-id="d27e3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-220">System-Flags</span></span>           | <span data-ttu-id="d27e3-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27e3-221">0x00000010</span></span>                                           |
| <span data-ttu-id="d27e3-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d27e3-222">Classes used in</span></span>        | [<span data-ttu-id="d27e3-223">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="d27e3-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d27e3-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d27e3-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d27e3-225">進入</span><span class="sxs-lookup"><span data-stu-id="d27e3-225">Entry</span></span> | <span data-ttu-id="d27e3-226">值</span><span class="sxs-lookup"><span data-stu-id="d27e3-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d27e3-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d27e3-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27e3-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27e3-229">System-Only</span></span>            | <span data-ttu-id="d27e3-230">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-230">False</span></span>                                                |
| <span data-ttu-id="d27e3-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d27e3-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d27e3-232">對</span><span class="sxs-lookup"><span data-stu-id="d27e3-232">True</span></span>                                                 |
| <span data-ttu-id="d27e3-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d27e3-233">Is Indexed</span></span>             | <span data-ttu-id="d27e3-234">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-234">False</span></span>                                                |
| <span data-ttu-id="d27e3-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d27e3-235">In Global Catalog</span></span>      | <span data-ttu-id="d27e3-236">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-236">False</span></span>                                                |
| <span data-ttu-id="d27e3-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d27e3-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27e3-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d27e3-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d27e3-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27e3-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27e3-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-241">Search-Flags</span></span>           | <span data-ttu-id="d27e3-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27e3-242">0x00000000</span></span>                                           |
| <span data-ttu-id="d27e3-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-243">System-Flags</span></span>           | <span data-ttu-id="d27e3-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27e3-244">0x00000010</span></span>                                           |
| <span data-ttu-id="d27e3-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d27e3-245">Classes used in</span></span>        | [<span data-ttu-id="d27e3-246">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="d27e3-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d27e3-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d27e3-247">Windows Server 2012</span></span>



| <span data-ttu-id="d27e3-248">進入</span><span class="sxs-lookup"><span data-stu-id="d27e3-248">Entry</span></span> | <span data-ttu-id="d27e3-249">值</span><span class="sxs-lookup"><span data-stu-id="d27e3-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d27e3-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d27e3-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d27e3-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d27e3-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d27e3-252">System-Only</span></span>            | <span data-ttu-id="d27e3-253">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-253">False</span></span>                                                |
| <span data-ttu-id="d27e3-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d27e3-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d27e3-255">對</span><span class="sxs-lookup"><span data-stu-id="d27e3-255">True</span></span>                                                 |
| <span data-ttu-id="d27e3-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d27e3-256">Is Indexed</span></span>             | <span data-ttu-id="d27e3-257">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-257">False</span></span>                                                |
| <span data-ttu-id="d27e3-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d27e3-258">In Global Catalog</span></span>      | <span data-ttu-id="d27e3-259">否</span><span class="sxs-lookup"><span data-stu-id="d27e3-259">False</span></span>                                                |
| <span data-ttu-id="d27e3-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d27e3-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d27e3-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d27e3-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d27e3-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d27e3-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d27e3-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d27e3-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-264">Search-Flags</span></span>           | <span data-ttu-id="d27e3-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d27e3-265">0x00000000</span></span>                                           |
| <span data-ttu-id="d27e3-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d27e3-266">System-Flags</span></span>           | <span data-ttu-id="d27e3-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d27e3-267">0x00000010</span></span>                                           |
| <span data-ttu-id="d27e3-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d27e3-268">Classes used in</span></span>        | [<span data-ttu-id="d27e3-269">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="d27e3-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






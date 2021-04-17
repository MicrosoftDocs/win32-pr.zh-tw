---
title: Enabled-Connection 屬性
description: 指出連接是否可供使用。
ms.assetid: 577c06fc-afb5-4e11-80a0-ee046ec68fb8
ms.tgt_platform: multiple
keywords:
- Enabled-Connection 屬性 AD 架構
- enabledConnection 屬性 AD 架構
topic_type:
- apiref
api_name:
- Enabled-Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104280a36e54ce73c98a3aea2ba9789bbebd75b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385330"
---
# <a name="enabled-connection-attribute"></a><span data-ttu-id="f10a2-105">Enabled-Connection 屬性</span><span class="sxs-lookup"><span data-stu-id="f10a2-105">Enabled-Connection attribute</span></span>

<span data-ttu-id="f10a2-106">指出連接是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="f10a2-106">Indicates whether a connection is available for use.</span></span>



| <span data-ttu-id="f10a2-107">進入</span><span class="sxs-lookup"><span data-stu-id="f10a2-107">Entry</span></span> | <span data-ttu-id="f10a2-108">值</span><span class="sxs-lookup"><span data-stu-id="f10a2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f10a2-109">CN</span><span class="sxs-lookup"><span data-stu-id="f10a2-109">CN</span></span>                | <span data-ttu-id="f10a2-110">Enabled-Connection</span><span class="sxs-lookup"><span data-stu-id="f10a2-110">Enabled-Connection</span></span>                   |
| <span data-ttu-id="f10a2-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f10a2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f10a2-112">enabledConnection</span><span class="sxs-lookup"><span data-stu-id="f10a2-112">enabledConnection</span></span>                    |
| <span data-ttu-id="f10a2-113">大小</span><span class="sxs-lookup"><span data-stu-id="f10a2-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="f10a2-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f10a2-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f10a2-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f10a2-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f10a2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f10a2-116">Attribute-Id</span></span>      | <span data-ttu-id="f10a2-117">1.2.840.113556.1.4.36</span><span class="sxs-lookup"><span data-stu-id="f10a2-117">1.2.840.113556.1.4.36</span></span>                |
| <span data-ttu-id="f10a2-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f10a2-118">System-Id-Guid</span></span>    | <span data-ttu-id="f10a2-119">bf967963-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f10a2-119">bf967963-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="f10a2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f10a2-120">Syntax</span></span>            | [<span data-ttu-id="f10a2-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f10a2-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="f10a2-122">實作</span><span class="sxs-lookup"><span data-stu-id="f10a2-122">Implementations</span></span>

-   [<span data-ttu-id="f10a2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f10a2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f10a2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f10a2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f10a2-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f10a2-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f10a2-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f10a2-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f10a2-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f10a2-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f10a2-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f10a2-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f10a2-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f10a2-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f10a2-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f10a2-130">Windows 2000 Server</span></span>



| <span data-ttu-id="f10a2-131">進入</span><span class="sxs-lookup"><span data-stu-id="f10a2-131">Entry</span></span> | <span data-ttu-id="f10a2-132">值</span><span class="sxs-lookup"><span data-stu-id="f10a2-132">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f10a2-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f10a2-133">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f10a2-134">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="f10a2-135">System-Only</span></span>            | <span data-ttu-id="f10a2-136">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-136">False</span></span>                                                  |
| <span data-ttu-id="f10a2-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f10a2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="f10a2-138">對</span><span class="sxs-lookup"><span data-stu-id="f10a2-138">True</span></span>                                                   |
| <span data-ttu-id="f10a2-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f10a2-139">Is Indexed</span></span>             | <span data-ttu-id="f10a2-140">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-140">False</span></span>                                                  |
| <span data-ttu-id="f10a2-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f10a2-141">In Global Catalog</span></span>      | <span data-ttu-id="f10a2-142">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-142">False</span></span>                                                  |
| <span data-ttu-id="f10a2-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f10a2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="f10a2-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f10a2-144">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f10a2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f10a2-145">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f10a2-146">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-147">Search-Flags</span></span>           | <span data-ttu-id="f10a2-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f10a2-148">0x00000000</span></span>                                             |
| <span data-ttu-id="f10a2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-149">System-Flags</span></span>           | <span data-ttu-id="f10a2-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f10a2-150">0x00000010</span></span>                                             |
| <span data-ttu-id="f10a2-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f10a2-151">Classes used in</span></span>        | [<span data-ttu-id="f10a2-152">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="f10a2-152">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f10a2-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f10a2-153">Windows Server 2003</span></span>



| <span data-ttu-id="f10a2-154">進入</span><span class="sxs-lookup"><span data-stu-id="f10a2-154">Entry</span></span> | <span data-ttu-id="f10a2-155">值</span><span class="sxs-lookup"><span data-stu-id="f10a2-155">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f10a2-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f10a2-156">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f10a2-157">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f10a2-158">System-Only</span></span>            | <span data-ttu-id="f10a2-159">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-159">False</span></span>                                                  |
| <span data-ttu-id="f10a2-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f10a2-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f10a2-161">對</span><span class="sxs-lookup"><span data-stu-id="f10a2-161">True</span></span>                                                   |
| <span data-ttu-id="f10a2-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f10a2-162">Is Indexed</span></span>             | <span data-ttu-id="f10a2-163">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-163">False</span></span>                                                  |
| <span data-ttu-id="f10a2-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f10a2-164">In Global Catalog</span></span>      | <span data-ttu-id="f10a2-165">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-165">False</span></span>                                                  |
| <span data-ttu-id="f10a2-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f10a2-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f10a2-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f10a2-167">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f10a2-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f10a2-168">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f10a2-169">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-170">Search-Flags</span></span>           | <span data-ttu-id="f10a2-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f10a2-171">0x00000000</span></span>                                             |
| <span data-ttu-id="f10a2-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-172">System-Flags</span></span>           | <span data-ttu-id="f10a2-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f10a2-173">0x00000010</span></span>                                             |
| <span data-ttu-id="f10a2-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f10a2-174">Classes used in</span></span>        | [<span data-ttu-id="f10a2-175">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="f10a2-175">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f10a2-176">亞當</span><span class="sxs-lookup"><span data-stu-id="f10a2-176">ADAM</span></span>



| <span data-ttu-id="f10a2-177">進入</span><span class="sxs-lookup"><span data-stu-id="f10a2-177">Entry</span></span> | <span data-ttu-id="f10a2-178">值</span><span class="sxs-lookup"><span data-stu-id="f10a2-178">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f10a2-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f10a2-179">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f10a2-180">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="f10a2-181">System-Only</span></span>            | <span data-ttu-id="f10a2-182">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-182">False</span></span>                                                  |
| <span data-ttu-id="f10a2-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f10a2-183">Is-Single-Valued</span></span>       | <span data-ttu-id="f10a2-184">對</span><span class="sxs-lookup"><span data-stu-id="f10a2-184">True</span></span>                                                   |
| <span data-ttu-id="f10a2-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f10a2-185">Is Indexed</span></span>             | <span data-ttu-id="f10a2-186">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-186">False</span></span>                                                  |
| <span data-ttu-id="f10a2-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f10a2-187">In Global Catalog</span></span>      | <span data-ttu-id="f10a2-188">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-188">False</span></span>                                                  |
| <span data-ttu-id="f10a2-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f10a2-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="f10a2-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f10a2-190">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f10a2-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f10a2-191">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f10a2-192">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-193">Search-Flags</span></span>           | <span data-ttu-id="f10a2-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f10a2-194">0x00000000</span></span>                                             |
| <span data-ttu-id="f10a2-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-195">System-Flags</span></span>           | <span data-ttu-id="f10a2-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f10a2-196">0x00000010</span></span>                                             |
| <span data-ttu-id="f10a2-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f10a2-197">Classes used in</span></span>        | [<span data-ttu-id="f10a2-198">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="f10a2-198">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f10a2-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f10a2-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f10a2-200">進入</span><span class="sxs-lookup"><span data-stu-id="f10a2-200">Entry</span></span> | <span data-ttu-id="f10a2-201">值</span><span class="sxs-lookup"><span data-stu-id="f10a2-201">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f10a2-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f10a2-202">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f10a2-203">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="f10a2-204">System-Only</span></span>            | <span data-ttu-id="f10a2-205">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-205">False</span></span>                                                  |
| <span data-ttu-id="f10a2-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f10a2-206">Is-Single-Valued</span></span>       | <span data-ttu-id="f10a2-207">對</span><span class="sxs-lookup"><span data-stu-id="f10a2-207">True</span></span>                                                   |
| <span data-ttu-id="f10a2-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f10a2-208">Is Indexed</span></span>             | <span data-ttu-id="f10a2-209">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-209">False</span></span>                                                  |
| <span data-ttu-id="f10a2-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f10a2-210">In Global Catalog</span></span>      | <span data-ttu-id="f10a2-211">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-211">False</span></span>                                                  |
| <span data-ttu-id="f10a2-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f10a2-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="f10a2-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f10a2-213">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f10a2-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f10a2-214">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f10a2-215">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-216">Search-Flags</span></span>           | <span data-ttu-id="f10a2-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f10a2-217">0x00000000</span></span>                                             |
| <span data-ttu-id="f10a2-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-218">System-Flags</span></span>           | <span data-ttu-id="f10a2-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f10a2-219">0x00000010</span></span>                                             |
| <span data-ttu-id="f10a2-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f10a2-220">Classes used in</span></span>        | [<span data-ttu-id="f10a2-221">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="f10a2-221">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f10a2-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f10a2-222">Windows Server 2008</span></span>



| <span data-ttu-id="f10a2-223">進入</span><span class="sxs-lookup"><span data-stu-id="f10a2-223">Entry</span></span> | <span data-ttu-id="f10a2-224">值</span><span class="sxs-lookup"><span data-stu-id="f10a2-224">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f10a2-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f10a2-225">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f10a2-226">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="f10a2-227">System-Only</span></span>            | <span data-ttu-id="f10a2-228">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-228">False</span></span>                                                  |
| <span data-ttu-id="f10a2-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f10a2-229">Is-Single-Valued</span></span>       | <span data-ttu-id="f10a2-230">對</span><span class="sxs-lookup"><span data-stu-id="f10a2-230">True</span></span>                                                   |
| <span data-ttu-id="f10a2-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f10a2-231">Is Indexed</span></span>             | <span data-ttu-id="f10a2-232">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-232">False</span></span>                                                  |
| <span data-ttu-id="f10a2-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f10a2-233">In Global Catalog</span></span>      | <span data-ttu-id="f10a2-234">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-234">False</span></span>                                                  |
| <span data-ttu-id="f10a2-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f10a2-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="f10a2-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f10a2-236">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f10a2-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f10a2-237">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f10a2-238">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-239">Search-Flags</span></span>           | <span data-ttu-id="f10a2-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f10a2-240">0x00000000</span></span>                                             |
| <span data-ttu-id="f10a2-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-241">System-Flags</span></span>           | <span data-ttu-id="f10a2-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f10a2-242">0x00000010</span></span>                                             |
| <span data-ttu-id="f10a2-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f10a2-243">Classes used in</span></span>        | [<span data-ttu-id="f10a2-244">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="f10a2-244">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f10a2-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f10a2-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f10a2-246">進入</span><span class="sxs-lookup"><span data-stu-id="f10a2-246">Entry</span></span> | <span data-ttu-id="f10a2-247">值</span><span class="sxs-lookup"><span data-stu-id="f10a2-247">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f10a2-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f10a2-248">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f10a2-249">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="f10a2-250">System-Only</span></span>            | <span data-ttu-id="f10a2-251">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-251">False</span></span>                                                  |
| <span data-ttu-id="f10a2-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f10a2-252">Is-Single-Valued</span></span>       | <span data-ttu-id="f10a2-253">對</span><span class="sxs-lookup"><span data-stu-id="f10a2-253">True</span></span>                                                   |
| <span data-ttu-id="f10a2-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f10a2-254">Is Indexed</span></span>             | <span data-ttu-id="f10a2-255">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-255">False</span></span>                                                  |
| <span data-ttu-id="f10a2-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f10a2-256">In Global Catalog</span></span>      | <span data-ttu-id="f10a2-257">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-257">False</span></span>                                                  |
| <span data-ttu-id="f10a2-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f10a2-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="f10a2-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f10a2-259">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f10a2-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f10a2-260">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f10a2-261">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-262">Search-Flags</span></span>           | <span data-ttu-id="f10a2-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f10a2-263">0x00000000</span></span>                                             |
| <span data-ttu-id="f10a2-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-264">System-Flags</span></span>           | <span data-ttu-id="f10a2-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f10a2-265">0x00000010</span></span>                                             |
| <span data-ttu-id="f10a2-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f10a2-266">Classes used in</span></span>        | [<span data-ttu-id="f10a2-267">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="f10a2-267">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f10a2-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f10a2-268">Windows Server 2012</span></span>



| <span data-ttu-id="f10a2-269">進入</span><span class="sxs-lookup"><span data-stu-id="f10a2-269">Entry</span></span> | <span data-ttu-id="f10a2-270">值</span><span class="sxs-lookup"><span data-stu-id="f10a2-270">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f10a2-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f10a2-271">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f10a2-272">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f10a2-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="f10a2-273">System-Only</span></span>            | <span data-ttu-id="f10a2-274">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-274">False</span></span>                                                  |
| <span data-ttu-id="f10a2-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f10a2-275">Is-Single-Valued</span></span>       | <span data-ttu-id="f10a2-276">對</span><span class="sxs-lookup"><span data-stu-id="f10a2-276">True</span></span>                                                   |
| <span data-ttu-id="f10a2-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f10a2-277">Is Indexed</span></span>             | <span data-ttu-id="f10a2-278">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-278">False</span></span>                                                  |
| <span data-ttu-id="f10a2-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f10a2-279">In Global Catalog</span></span>      | <span data-ttu-id="f10a2-280">否</span><span class="sxs-lookup"><span data-stu-id="f10a2-280">False</span></span>                                                  |
| <span data-ttu-id="f10a2-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f10a2-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="f10a2-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f10a2-282">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f10a2-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f10a2-283">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f10a2-284">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f10a2-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-285">Search-Flags</span></span>           | <span data-ttu-id="f10a2-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f10a2-286">0x00000000</span></span>                                             |
| <span data-ttu-id="f10a2-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f10a2-287">System-Flags</span></span>           | <span data-ttu-id="f10a2-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f10a2-288">0x00000010</span></span>                                             |
| <span data-ttu-id="f10a2-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f10a2-289">Classes used in</span></span>        | [<span data-ttu-id="f10a2-290">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="f10a2-290">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 






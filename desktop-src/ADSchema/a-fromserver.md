---
title: From-Server 屬性
description: 複寫來源伺服器的分辨名稱。
ms.assetid: c4ff05fe-21a7-4b59-90f8-f3bd723285fa
ms.tgt_platform: multiple
keywords:
- From-Server 屬性 AD 架構
- fromServer 屬性 AD 架構
topic_type:
- apiref
api_name:
- From-Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd24e6c19ab10e1537d908405d8d13f7e9db5e2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935251"
---
# <a name="from-server-attribute"></a><span data-ttu-id="78b2c-105">From-Server 屬性</span><span class="sxs-lookup"><span data-stu-id="78b2c-105">From-Server attribute</span></span>

<span data-ttu-id="78b2c-106">複寫來源伺服器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="78b2c-106">The distinguished name of the replication source server.</span></span>



| <span data-ttu-id="78b2c-107">進入</span><span class="sxs-lookup"><span data-stu-id="78b2c-107">Entry</span></span> | <span data-ttu-id="78b2c-108">值</span><span class="sxs-lookup"><span data-stu-id="78b2c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="78b2c-109">CN</span><span class="sxs-lookup"><span data-stu-id="78b2c-109">CN</span></span>                | <span data-ttu-id="78b2c-110">From-Server</span><span class="sxs-lookup"><span data-stu-id="78b2c-110">From-Server</span></span>                             |
| <span data-ttu-id="78b2c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="78b2c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="78b2c-112">fromServer</span><span class="sxs-lookup"><span data-stu-id="78b2c-112">fromServer</span></span>                              |
| <span data-ttu-id="78b2c-113">大小</span><span class="sxs-lookup"><span data-stu-id="78b2c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="78b2c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="78b2c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="78b2c-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="78b2c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="78b2c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78b2c-116">Attribute-Id</span></span>      | <span data-ttu-id="78b2c-117">1.2.840.113556.1.4.40</span><span class="sxs-lookup"><span data-stu-id="78b2c-117">1.2.840.113556.1.4.40</span></span>                   |
| <span data-ttu-id="78b2c-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="78b2c-118">System-Id-Guid</span></span>    | <span data-ttu-id="78b2c-119">bf967979-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="78b2c-119">bf967979-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="78b2c-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="78b2c-120">Syntax</span></span>            | [<span data-ttu-id="78b2c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="78b2c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="78b2c-122">實作</span><span class="sxs-lookup"><span data-stu-id="78b2c-122">Implementations</span></span>

-   [<span data-ttu-id="78b2c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="78b2c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="78b2c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78b2c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78b2c-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="78b2c-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="78b2c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78b2c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78b2c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78b2c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78b2c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78b2c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78b2c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78b2c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="78b2c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78b2c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="78b2c-131">進入</span><span class="sxs-lookup"><span data-stu-id="78b2c-131">Entry</span></span> | <span data-ttu-id="78b2c-132">值</span><span class="sxs-lookup"><span data-stu-id="78b2c-132">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="78b2c-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b2c-133">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b2c-134">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b2c-135">System-Only</span></span>            | <span data-ttu-id="78b2c-136">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-136">False</span></span>                                                  |
| <span data-ttu-id="78b2c-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b2c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="78b2c-138">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-138">True</span></span>                                                   |
| <span data-ttu-id="78b2c-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b2c-139">Is Indexed</span></span>             | <span data-ttu-id="78b2c-140">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-140">False</span></span>                                                  |
| <span data-ttu-id="78b2c-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b2c-141">In Global Catalog</span></span>      | <span data-ttu-id="78b2c-142">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-142">False</span></span>                                                  |
| <span data-ttu-id="78b2c-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b2c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b2c-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b2c-144">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="78b2c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b2c-145">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b2c-146">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-147">Search-Flags</span></span>           | <span data-ttu-id="78b2c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b2c-148">0x00000000</span></span>                                             |
| <span data-ttu-id="78b2c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-149">System-Flags</span></span>           | <span data-ttu-id="78b2c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b2c-150">0x00000010</span></span>                                             |
| <span data-ttu-id="78b2c-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b2c-151">Classes used in</span></span>        | [<span data-ttu-id="78b2c-152">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="78b2c-152">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="78b2c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78b2c-153">Windows Server 2003</span></span>



| <span data-ttu-id="78b2c-154">進入</span><span class="sxs-lookup"><span data-stu-id="78b2c-154">Entry</span></span> | <span data-ttu-id="78b2c-155">值</span><span class="sxs-lookup"><span data-stu-id="78b2c-155">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="78b2c-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b2c-156">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b2c-157">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b2c-158">System-Only</span></span>            | <span data-ttu-id="78b2c-159">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-159">False</span></span>                                                  |
| <span data-ttu-id="78b2c-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b2c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="78b2c-161">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-161">True</span></span>                                                   |
| <span data-ttu-id="78b2c-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b2c-162">Is Indexed</span></span>             | <span data-ttu-id="78b2c-163">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-163">False</span></span>                                                  |
| <span data-ttu-id="78b2c-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b2c-164">In Global Catalog</span></span>      | <span data-ttu-id="78b2c-165">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-165">False</span></span>                                                  |
| <span data-ttu-id="78b2c-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b2c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b2c-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b2c-167">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="78b2c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b2c-168">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b2c-169">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-170">Search-Flags</span></span>           | <span data-ttu-id="78b2c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b2c-171">0x00000000</span></span>                                             |
| <span data-ttu-id="78b2c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-172">System-Flags</span></span>           | <span data-ttu-id="78b2c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b2c-173">0x00000010</span></span>                                             |
| <span data-ttu-id="78b2c-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b2c-174">Classes used in</span></span>        | [<span data-ttu-id="78b2c-175">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="78b2c-175">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="78b2c-176">亞當</span><span class="sxs-lookup"><span data-stu-id="78b2c-176">ADAM</span></span>



| <span data-ttu-id="78b2c-177">進入</span><span class="sxs-lookup"><span data-stu-id="78b2c-177">Entry</span></span> | <span data-ttu-id="78b2c-178">值</span><span class="sxs-lookup"><span data-stu-id="78b2c-178">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="78b2c-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b2c-179">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b2c-180">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b2c-181">System-Only</span></span>            | <span data-ttu-id="78b2c-182">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-182">False</span></span>                                                  |
| <span data-ttu-id="78b2c-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b2c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="78b2c-184">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-184">True</span></span>                                                   |
| <span data-ttu-id="78b2c-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b2c-185">Is Indexed</span></span>             | <span data-ttu-id="78b2c-186">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-186">False</span></span>                                                  |
| <span data-ttu-id="78b2c-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b2c-187">In Global Catalog</span></span>      | <span data-ttu-id="78b2c-188">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-188">False</span></span>                                                  |
| <span data-ttu-id="78b2c-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b2c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b2c-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b2c-190">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="78b2c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b2c-191">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b2c-192">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-193">Search-Flags</span></span>           | <span data-ttu-id="78b2c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b2c-194">0x00000000</span></span>                                             |
| <span data-ttu-id="78b2c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-195">System-Flags</span></span>           | <span data-ttu-id="78b2c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b2c-196">0x00000010</span></span>                                             |
| <span data-ttu-id="78b2c-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b2c-197">Classes used in</span></span>        | [<span data-ttu-id="78b2c-198">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="78b2c-198">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78b2c-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78b2c-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78b2c-200">進入</span><span class="sxs-lookup"><span data-stu-id="78b2c-200">Entry</span></span> | <span data-ttu-id="78b2c-201">值</span><span class="sxs-lookup"><span data-stu-id="78b2c-201">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="78b2c-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b2c-202">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b2c-203">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b2c-204">System-Only</span></span>            | <span data-ttu-id="78b2c-205">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-205">False</span></span>                                                  |
| <span data-ttu-id="78b2c-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b2c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="78b2c-207">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-207">True</span></span>                                                   |
| <span data-ttu-id="78b2c-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b2c-208">Is Indexed</span></span>             | <span data-ttu-id="78b2c-209">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-209">False</span></span>                                                  |
| <span data-ttu-id="78b2c-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b2c-210">In Global Catalog</span></span>      | <span data-ttu-id="78b2c-211">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-211">False</span></span>                                                  |
| <span data-ttu-id="78b2c-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b2c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b2c-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b2c-213">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="78b2c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b2c-214">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b2c-215">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-216">Search-Flags</span></span>           | <span data-ttu-id="78b2c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b2c-217">0x00000000</span></span>                                             |
| <span data-ttu-id="78b2c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-218">System-Flags</span></span>           | <span data-ttu-id="78b2c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b2c-219">0x00000010</span></span>                                             |
| <span data-ttu-id="78b2c-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b2c-220">Classes used in</span></span>        | [<span data-ttu-id="78b2c-221">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="78b2c-221">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78b2c-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78b2c-222">Windows Server 2008</span></span>



| <span data-ttu-id="78b2c-223">進入</span><span class="sxs-lookup"><span data-stu-id="78b2c-223">Entry</span></span> | <span data-ttu-id="78b2c-224">值</span><span class="sxs-lookup"><span data-stu-id="78b2c-224">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="78b2c-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b2c-225">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b2c-226">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b2c-227">System-Only</span></span>            | <span data-ttu-id="78b2c-228">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-228">False</span></span>                                                  |
| <span data-ttu-id="78b2c-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b2c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="78b2c-230">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-230">True</span></span>                                                   |
| <span data-ttu-id="78b2c-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b2c-231">Is Indexed</span></span>             | <span data-ttu-id="78b2c-232">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-232">True</span></span>                                                   |
| <span data-ttu-id="78b2c-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b2c-233">In Global Catalog</span></span>      | <span data-ttu-id="78b2c-234">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-234">False</span></span>                                                  |
| <span data-ttu-id="78b2c-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b2c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b2c-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b2c-236">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="78b2c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b2c-237">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b2c-238">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-239">Search-Flags</span></span>           | <span data-ttu-id="78b2c-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78b2c-240">0x00000001</span></span>                                             |
| <span data-ttu-id="78b2c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-241">System-Flags</span></span>           | <span data-ttu-id="78b2c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b2c-242">0x00000010</span></span>                                             |
| <span data-ttu-id="78b2c-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b2c-243">Classes used in</span></span>        | [<span data-ttu-id="78b2c-244">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="78b2c-244">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78b2c-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78b2c-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78b2c-246">進入</span><span class="sxs-lookup"><span data-stu-id="78b2c-246">Entry</span></span> | <span data-ttu-id="78b2c-247">值</span><span class="sxs-lookup"><span data-stu-id="78b2c-247">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="78b2c-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b2c-248">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b2c-249">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b2c-250">System-Only</span></span>            | <span data-ttu-id="78b2c-251">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-251">False</span></span>                                                  |
| <span data-ttu-id="78b2c-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b2c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="78b2c-253">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-253">True</span></span>                                                   |
| <span data-ttu-id="78b2c-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b2c-254">Is Indexed</span></span>             | <span data-ttu-id="78b2c-255">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-255">True</span></span>                                                   |
| <span data-ttu-id="78b2c-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b2c-256">In Global Catalog</span></span>      | <span data-ttu-id="78b2c-257">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-257">False</span></span>                                                  |
| <span data-ttu-id="78b2c-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b2c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b2c-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b2c-259">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="78b2c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b2c-260">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b2c-261">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-262">Search-Flags</span></span>           | <span data-ttu-id="78b2c-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78b2c-263">0x00000001</span></span>                                             |
| <span data-ttu-id="78b2c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-264">System-Flags</span></span>           | <span data-ttu-id="78b2c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b2c-265">0x00000010</span></span>                                             |
| <span data-ttu-id="78b2c-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b2c-266">Classes used in</span></span>        | [<span data-ttu-id="78b2c-267">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="78b2c-267">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78b2c-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78b2c-268">Windows Server 2012</span></span>



| <span data-ttu-id="78b2c-269">進入</span><span class="sxs-lookup"><span data-stu-id="78b2c-269">Entry</span></span> | <span data-ttu-id="78b2c-270">值</span><span class="sxs-lookup"><span data-stu-id="78b2c-270">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="78b2c-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78b2c-271">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78b2c-272">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="78b2c-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="78b2c-273">System-Only</span></span>            | <span data-ttu-id="78b2c-274">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-274">False</span></span>                                                  |
| <span data-ttu-id="78b2c-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78b2c-275">Is-Single-Valued</span></span>       | <span data-ttu-id="78b2c-276">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-276">True</span></span>                                                   |
| <span data-ttu-id="78b2c-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78b2c-277">Is Indexed</span></span>             | <span data-ttu-id="78b2c-278">對</span><span class="sxs-lookup"><span data-stu-id="78b2c-278">True</span></span>                                                   |
| <span data-ttu-id="78b2c-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78b2c-279">In Global Catalog</span></span>      | <span data-ttu-id="78b2c-280">否</span><span class="sxs-lookup"><span data-stu-id="78b2c-280">False</span></span>                                                  |
| <span data-ttu-id="78b2c-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78b2c-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="78b2c-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78b2c-282">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="78b2c-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78b2c-283">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78b2c-284">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="78b2c-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-285">Search-Flags</span></span>           | <span data-ttu-id="78b2c-286">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78b2c-286">0x00000001</span></span>                                             |
| <span data-ttu-id="78b2c-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78b2c-287">System-Flags</span></span>           | <span data-ttu-id="78b2c-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b2c-288">0x00000010</span></span>                                             |
| <span data-ttu-id="78b2c-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78b2c-289">Classes used in</span></span>        | [<span data-ttu-id="78b2c-290">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="78b2c-290">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 






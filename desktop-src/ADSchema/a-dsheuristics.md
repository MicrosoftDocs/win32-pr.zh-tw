---
title: DS-Heuristics 屬性
description: 包含整個樹系的全域設定。
ms.assetid: d5fd990b-7bbf-4ede-a3af-7f3f7ac959b3
ms.tgt_platform: multiple
keywords:
- DS-Heuristics 屬性 AD 架構
- dSHeuristics 屬性 AD 架構
topic_type:
- apiref
api_name:
- DS-Heuristics
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65922b580975ec05877ae33d213ff3a3675ec72f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106965337"
---
# <a name="ds-heuristics-attribute"></a><span data-ttu-id="fe7b8-105">DS-Heuristics 屬性</span><span class="sxs-lookup"><span data-stu-id="fe7b8-105">DS-Heuristics attribute</span></span>

<span data-ttu-id="fe7b8-106">包含整個樹系的全域設定。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-106">Contains global settings for the entire forest.</span></span>

<span data-ttu-id="fe7b8-107">Microsoft 說明及支援網站上的 adminSDholder 排除位有相關資訊，文章編號 [817433，委派的許可權無法使用，而且繼承會自動停用](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433)。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-107">There is information about adminSDholder exclusion bits available on the Microsoft Help and Support website in an article number [817433, Delegated permissions are not available and inheritance is automatically disabled](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span></span>



| <span data-ttu-id="fe7b8-108">進入</span><span class="sxs-lookup"><span data-stu-id="fe7b8-108">Entry</span></span> | <span data-ttu-id="fe7b8-109">值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="fe7b8-110">CN</span><span class="sxs-lookup"><span data-stu-id="fe7b8-110">CN</span></span>                | <span data-ttu-id="fe7b8-111">DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="fe7b8-111">DS-Heuristics</span></span>                               |
| <span data-ttu-id="fe7b8-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fe7b8-112">Ldap-Display-Name</span></span> | <span data-ttu-id="fe7b8-113">dSHeuristics</span><span class="sxs-lookup"><span data-stu-id="fe7b8-113">dSHeuristics</span></span>                                |
| <span data-ttu-id="fe7b8-114">大小</span><span class="sxs-lookup"><span data-stu-id="fe7b8-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="fe7b8-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fe7b8-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="fe7b8-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fe7b8-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="fe7b8-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fe7b8-117">Attribute-Id</span></span>      | <span data-ttu-id="fe7b8-118">1.2.840.113556.1.2.212</span><span class="sxs-lookup"><span data-stu-id="fe7b8-118">1.2.840.113556.1.2.212</span></span>                      |
| <span data-ttu-id="fe7b8-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fe7b8-119">System-Id-Guid</span></span>    | <span data-ttu-id="fe7b8-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="fe7b8-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="fe7b8-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe7b8-121">Syntax</span></span>            | [<span data-ttu-id="fe7b8-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="fe7b8-123">實作</span><span class="sxs-lookup"><span data-stu-id="fe7b8-123">Implementations</span></span>

-   [<span data-ttu-id="fe7b8-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fe7b8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fe7b8-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fe7b8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fe7b8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fe7b8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fe7b8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fe7b8-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fe7b8-131">Windows 2000 Server</span></span>



| <span data-ttu-id="fe7b8-132">進入</span><span class="sxs-lookup"><span data-stu-id="fe7b8-132">Entry</span></span> | <span data-ttu-id="fe7b8-133">值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="fe7b8-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe7b8-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe7b8-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe7b8-136">System-Only</span></span>            | <span data-ttu-id="fe7b8-137">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-137">False</span></span>                                            |
| <span data-ttu-id="fe7b8-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fe7b8-139">對</span><span class="sxs-lookup"><span data-stu-id="fe7b8-139">True</span></span>                                             |
| <span data-ttu-id="fe7b8-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe7b8-140">Is Indexed</span></span>             | <span data-ttu-id="fe7b8-141">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-141">False</span></span>                                            |
| <span data-ttu-id="fe7b8-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe7b8-142">In Global Catalog</span></span>      | <span data-ttu-id="fe7b8-143">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-143">False</span></span>                                            |
| <span data-ttu-id="fe7b8-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe7b8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe7b8-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe7b8-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="fe7b8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe7b8-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe7b8-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-148">Search-Flags</span></span>           | <span data-ttu-id="fe7b8-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe7b8-149">0x00000000</span></span>                                       |
| <span data-ttu-id="fe7b8-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-150">System-Flags</span></span>           | <span data-ttu-id="fe7b8-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe7b8-151">0x00000010</span></span>                                       |
| <span data-ttu-id="fe7b8-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe7b8-152">Classes used in</span></span>        | [<span data-ttu-id="fe7b8-153">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-153">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fe7b8-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe7b8-154">Windows Server 2003</span></span>



| <span data-ttu-id="fe7b8-155">進入</span><span class="sxs-lookup"><span data-stu-id="fe7b8-155">Entry</span></span> | <span data-ttu-id="fe7b8-156">值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="fe7b8-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe7b8-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe7b8-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe7b8-159">System-Only</span></span>            | <span data-ttu-id="fe7b8-160">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-160">False</span></span>                                            |
| <span data-ttu-id="fe7b8-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fe7b8-162">對</span><span class="sxs-lookup"><span data-stu-id="fe7b8-162">True</span></span>                                             |
| <span data-ttu-id="fe7b8-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe7b8-163">Is Indexed</span></span>             | <span data-ttu-id="fe7b8-164">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-164">False</span></span>                                            |
| <span data-ttu-id="fe7b8-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe7b8-165">In Global Catalog</span></span>      | <span data-ttu-id="fe7b8-166">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-166">False</span></span>                                            |
| <span data-ttu-id="fe7b8-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe7b8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe7b8-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe7b8-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="fe7b8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe7b8-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe7b8-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-171">Search-Flags</span></span>           | <span data-ttu-id="fe7b8-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe7b8-172">0x00000000</span></span>                                       |
| <span data-ttu-id="fe7b8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-173">System-Flags</span></span>           | <span data-ttu-id="fe7b8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe7b8-174">0x00000010</span></span>                                       |
| <span data-ttu-id="fe7b8-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe7b8-175">Classes used in</span></span>        | [<span data-ttu-id="fe7b8-176">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-176">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fe7b8-177">亞當</span><span class="sxs-lookup"><span data-stu-id="fe7b8-177">ADAM</span></span>



| <span data-ttu-id="fe7b8-178">進入</span><span class="sxs-lookup"><span data-stu-id="fe7b8-178">Entry</span></span> | <span data-ttu-id="fe7b8-179">值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="fe7b8-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe7b8-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe7b8-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe7b8-182">System-Only</span></span>            | <span data-ttu-id="fe7b8-183">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-183">False</span></span>                                            |
| <span data-ttu-id="fe7b8-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fe7b8-185">對</span><span class="sxs-lookup"><span data-stu-id="fe7b8-185">True</span></span>                                             |
| <span data-ttu-id="fe7b8-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe7b8-186">Is Indexed</span></span>             | <span data-ttu-id="fe7b8-187">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-187">False</span></span>                                            |
| <span data-ttu-id="fe7b8-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe7b8-188">In Global Catalog</span></span>      | <span data-ttu-id="fe7b8-189">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-189">False</span></span>                                            |
| <span data-ttu-id="fe7b8-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe7b8-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe7b8-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe7b8-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="fe7b8-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe7b8-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe7b8-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-194">Search-Flags</span></span>           | <span data-ttu-id="fe7b8-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe7b8-195">0x00000000</span></span>                                       |
| <span data-ttu-id="fe7b8-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-196">System-Flags</span></span>           | <span data-ttu-id="fe7b8-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe7b8-197">0x00000010</span></span>                                       |
| <span data-ttu-id="fe7b8-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe7b8-198">Classes used in</span></span>        | [<span data-ttu-id="fe7b8-199">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-199">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fe7b8-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fe7b8-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fe7b8-201">進入</span><span class="sxs-lookup"><span data-stu-id="fe7b8-201">Entry</span></span> | <span data-ttu-id="fe7b8-202">值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="fe7b8-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe7b8-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe7b8-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe7b8-205">System-Only</span></span>            | <span data-ttu-id="fe7b8-206">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-206">False</span></span>                                            |
| <span data-ttu-id="fe7b8-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-207">Is-Single-Valued</span></span>       | <span data-ttu-id="fe7b8-208">對</span><span class="sxs-lookup"><span data-stu-id="fe7b8-208">True</span></span>                                             |
| <span data-ttu-id="fe7b8-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe7b8-209">Is Indexed</span></span>             | <span data-ttu-id="fe7b8-210">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-210">False</span></span>                                            |
| <span data-ttu-id="fe7b8-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe7b8-211">In Global Catalog</span></span>      | <span data-ttu-id="fe7b8-212">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-212">False</span></span>                                            |
| <span data-ttu-id="fe7b8-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe7b8-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe7b8-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe7b8-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="fe7b8-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe7b8-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe7b8-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-217">Search-Flags</span></span>           | <span data-ttu-id="fe7b8-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe7b8-218">0x00000000</span></span>                                       |
| <span data-ttu-id="fe7b8-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-219">System-Flags</span></span>           | <span data-ttu-id="fe7b8-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe7b8-220">0x00000010</span></span>                                       |
| <span data-ttu-id="fe7b8-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe7b8-221">Classes used in</span></span>        | [<span data-ttu-id="fe7b8-222">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-222">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fe7b8-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe7b8-223">Windows Server 2008</span></span>



| <span data-ttu-id="fe7b8-224">進入</span><span class="sxs-lookup"><span data-stu-id="fe7b8-224">Entry</span></span> | <span data-ttu-id="fe7b8-225">值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="fe7b8-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe7b8-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe7b8-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe7b8-228">System-Only</span></span>            | <span data-ttu-id="fe7b8-229">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-229">False</span></span>                                            |
| <span data-ttu-id="fe7b8-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-230">Is-Single-Valued</span></span>       | <span data-ttu-id="fe7b8-231">對</span><span class="sxs-lookup"><span data-stu-id="fe7b8-231">True</span></span>                                             |
| <span data-ttu-id="fe7b8-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe7b8-232">Is Indexed</span></span>             | <span data-ttu-id="fe7b8-233">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-233">False</span></span>                                            |
| <span data-ttu-id="fe7b8-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe7b8-234">In Global Catalog</span></span>      | <span data-ttu-id="fe7b8-235">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-235">False</span></span>                                            |
| <span data-ttu-id="fe7b8-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe7b8-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe7b8-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe7b8-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="fe7b8-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe7b8-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe7b8-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-240">Search-Flags</span></span>           | <span data-ttu-id="fe7b8-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe7b8-241">0x00000000</span></span>                                       |
| <span data-ttu-id="fe7b8-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-242">System-Flags</span></span>           | <span data-ttu-id="fe7b8-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe7b8-243">0x00000010</span></span>                                       |
| <span data-ttu-id="fe7b8-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe7b8-244">Classes used in</span></span>        | [<span data-ttu-id="fe7b8-245">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-245">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fe7b8-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe7b8-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fe7b8-247">進入</span><span class="sxs-lookup"><span data-stu-id="fe7b8-247">Entry</span></span> | <span data-ttu-id="fe7b8-248">值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="fe7b8-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe7b8-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe7b8-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe7b8-251">System-Only</span></span>            | <span data-ttu-id="fe7b8-252">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-252">False</span></span>                                            |
| <span data-ttu-id="fe7b8-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-253">Is-Single-Valued</span></span>       | <span data-ttu-id="fe7b8-254">對</span><span class="sxs-lookup"><span data-stu-id="fe7b8-254">True</span></span>                                             |
| <span data-ttu-id="fe7b8-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe7b8-255">Is Indexed</span></span>             | <span data-ttu-id="fe7b8-256">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-256">False</span></span>                                            |
| <span data-ttu-id="fe7b8-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe7b8-257">In Global Catalog</span></span>      | <span data-ttu-id="fe7b8-258">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-258">False</span></span>                                            |
| <span data-ttu-id="fe7b8-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe7b8-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe7b8-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe7b8-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="fe7b8-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe7b8-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe7b8-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-263">Search-Flags</span></span>           | <span data-ttu-id="fe7b8-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe7b8-264">0x00000000</span></span>                                       |
| <span data-ttu-id="fe7b8-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-265">System-Flags</span></span>           | <span data-ttu-id="fe7b8-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe7b8-266">0x00000010</span></span>                                       |
| <span data-ttu-id="fe7b8-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe7b8-267">Classes used in</span></span>        | [<span data-ttu-id="fe7b8-268">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-268">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fe7b8-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe7b8-269">Windows Server 2012</span></span>



| <span data-ttu-id="fe7b8-270">進入</span><span class="sxs-lookup"><span data-stu-id="fe7b8-270">Entry</span></span> | <span data-ttu-id="fe7b8-271">值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="fe7b8-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe7b8-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe7b8-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="fe7b8-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe7b8-274">System-Only</span></span>            | <span data-ttu-id="fe7b8-275">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-275">False</span></span>                                            |
| <span data-ttu-id="fe7b8-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe7b8-276">Is-Single-Valued</span></span>       | <span data-ttu-id="fe7b8-277">對</span><span class="sxs-lookup"><span data-stu-id="fe7b8-277">True</span></span>                                             |
| <span data-ttu-id="fe7b8-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe7b8-278">Is Indexed</span></span>             | <span data-ttu-id="fe7b8-279">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-279">False</span></span>                                            |
| <span data-ttu-id="fe7b8-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe7b8-280">In Global Catalog</span></span>      | <span data-ttu-id="fe7b8-281">否</span><span class="sxs-lookup"><span data-stu-id="fe7b8-281">False</span></span>                                            |
| <span data-ttu-id="fe7b8-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe7b8-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe7b8-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe7b8-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="fe7b8-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe7b8-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe7b8-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="fe7b8-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-286">Search-Flags</span></span>           | <span data-ttu-id="fe7b8-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe7b8-287">0x00000000</span></span>                                       |
| <span data-ttu-id="fe7b8-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe7b8-288">System-Flags</span></span>           | <span data-ttu-id="fe7b8-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe7b8-289">0x00000010</span></span>                                       |
| <span data-ttu-id="fe7b8-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe7b8-290">Classes used in</span></span>        | [<span data-ttu-id="fe7b8-291">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-291">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fe7b8-292">備註</span><span class="sxs-lookup"><span data-stu-id="fe7b8-292">Remarks</span></span>

<span data-ttu-id="fe7b8-293">每個 Active Directory 樹系都包含 DS-Heuristics 屬性，其中包含整個樹系的設定。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-293">Each Active Directory forest contains a DS-Heuristics attribute that contains settings for the entire forest.</span></span> <span data-ttu-id="fe7b8-294">DS-Heuristics 屬性是 "CN = Directory Service，CN = Windows NT，CN = Services，CN = Configuration， <Domain> " 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-294">The DS-Heuristics attribute is an attribute of the "CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,<Domain>" object.</span></span>

<span data-ttu-id="fe7b8-295">DS-Heuristics 是 Unicode 字串，其中每個字元都包含單一定義域範圍設定的值。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-295">DS-Heuristics is a Unicode string in which each character contains a value for a single domain-wide setting.</span></span> <span data-ttu-id="fe7b8-296">DS-Heuristics 字串採用下列格式。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-296">The DS-Heuristics string takes the following format.</span></span>

``` syntax
|<1>|<2>|<3>|<4>|<5>|<6>|<7>|<8>|<9>|<10>|<11>|<12>|<13>|<14>|<15>|<16>|<17>|<18>|<19>|<20>|<21>|<22>|<23>|<24>|<25>|
```

<span data-ttu-id="fe7b8-297">為了提供資料驗證，每十個字元會設定為字元數除以10。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-297">To provide data validation, each tenth character is set to the character number divided by ten.</span></span> <span data-ttu-id="fe7b8-298">例如，第十個字元是 ' 1 ';第二十個字元為 ' 2 '，依此類推。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-298">For example, the tenth character is '1'; the twentieth character is '2', and so on.</span></span>

<span data-ttu-id="fe7b8-299">未設定的任何字元都會假設為 ' 0 '。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-299">Any character that is not set is assumed to be a '0'.</span></span> <span data-ttu-id="fe7b8-300">如果未設定 DS-Heuristics 屬性，則會假設所有值都是 ' 0 '。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-300">If the DS-Heuristics attribute is not set, all values are assumed to be '0'.</span></span> <span data-ttu-id="fe7b8-301">目前正在使用25個字元，且不需要填補字串來填滿25個字元。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-301">There are currently 25 characters being used and it is not necessary to pad the string to fill all 25 characters.</span></span> <span data-ttu-id="fe7b8-302">例如，如果所使用的最大字元是7，則字串 "0000002" 是可接受的。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-302">For example, if the highest character being used is 7, then the string "0000002" is acceptable.</span></span>

<span data-ttu-id="fe7b8-303">如需每個字元的詳細資訊，請參閱 [dSHeuristics 中的 \[ ADTS \] Active Directory 技術規格](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-303">For details about each character, see [dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span></span>

### <a name="anr-search-filters"></a><span data-ttu-id="fe7b8-304">ANR 搜尋篩選</span><span class="sxs-lookup"><span data-stu-id="fe7b8-304">ANR Search Filters</span></span>

<span data-ttu-id="fe7b8-305">字元1、2和4用來修改 ANR 搜尋篩選器的行為。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-305">Characters 1, 2, and 4 are used to modify the behavior of ANR search filters.</span></span> <span data-ttu-id="fe7b8-306">如果字元1設定為 ' 1 '，則在) 停用時，ANR 篩選器的展開以包含 **GivenName**  -  **姓氏** (。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-306">If character 1 is set to '1', then the expansion of the ANR filter to include **GivenName** - **Surname** (when space is found) is disabled.</span></span> <span data-ttu-id="fe7b8-307">如果字元2設定為 ' 1 '，則會停用 ANR 篩選準則的擴充以包含 **姓氏**  -  **GivenName** 。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-307">If character 2 is set to '1', the expansion of the ANR filter to include **Surname** - **GivenName** is disabled.</span></span> <span data-ttu-id="fe7b8-308">如果搜尋字串中有內嵌的空間，搜尋字串通常會分成兩個字串，而這些字串會與 **GivenName** 和 **姓氏** 屬性的成對成對比較。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-308">If an embedded space is present in the search string, the search string will normally be divided into two strings, which are compared pair-wise against the **GivenName** and **Surname** attributes.</span></span> <span data-ttu-id="fe7b8-309">將字元1和2設定為 ' 1 ' 將會防止嘗試這些相符專案。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-309">Setting characters 1 and 2 to '1' will prevent those matches from being attempted.</span></span> <span data-ttu-id="fe7b8-310">如果系統管理員確信搜尋 "Jeff Smith" 時一律會提供「jeff smith」，而不是「Smith，Jeff」，則可能會停用這項對應。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-310">This matching might be disabled if the administrator is confident that searches for "Jeff Smith" would always be provided as "jeff smith" and not "smith, jeff".</span></span> <span data-ttu-id="fe7b8-311">根據本機慣例，通常只會隱藏一個或另一個相符的。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-311">Normally only one or the other match would be suppressed, according to local convention.</span></span>

<span data-ttu-id="fe7b8-312">如果字元4設定為 ' 1 '，Active Directory 將會執行「搶先昵稱解析」。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-312">If the character 4 is set to '1' then Active Directory will perform "pre-emptive nickname resolution".</span></span> <span data-ttu-id="fe7b8-313">也就是說，如果搜尋字串完全符合搜尋範圍中剛好一個物件的昵稱，則會傳回一個物件做為搜尋的結果，並略過其餘的 ANR。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-313">That is, if the search string exactly matches the nickname of exactly one object in the search scope, that one object is returned as the result of the search, and the rest of ANR is skipped.</span></span> <span data-ttu-id="fe7b8-314">請注意，雖然 ANR 搜尋的其餘部分可透過 LDAP 取得，但 (也稱為「昵稱貼齊」 ) 只能透過 MAPI 使用。</span><span class="sxs-lookup"><span data-stu-id="fe7b8-314">Note that while the rest of ANR searching is available through LDAP, pre-emptive nickname resolution (also known as "nickname snap") is available only through MAPI.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe7b8-315">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe7b8-315">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe7b8-316">[dSHeuristics in \[ MS-ADTS \] Active Directory 技術規格](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span><span class="sxs-lookup"><span data-stu-id="fe7b8-316">[dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span></span>
</dt> </dl>

 


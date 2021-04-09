---
title: ms DS-其他-設定屬性
description: 此多重值屬性是用來儲存以名稱值格式儲存的 DS 任何可設定的設定。
ms.assetid: e7d17c8e-6264-43d1-9010-9d589f93a086
ms.tgt_platform: multiple
keywords:
- ms DS-其他設定屬性 AD 架構
- 其他設定屬性的 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Other-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3699ac7983f33730cb73bb0f1eab0c13e72cbce
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845147"
---
# <a name="ms-ds-other-settings-attribute"></a><span data-ttu-id="9c9f2-105">ms DS-其他-設定屬性</span><span class="sxs-lookup"><span data-stu-id="9c9f2-105">ms-DS-Other-Settings attribute</span></span>

<span data-ttu-id="9c9f2-106">此多重值屬性是用來儲存以 NAME = VALUE 格式儲存的 DS 任何可設定的設定。</span><span class="sxs-lookup"><span data-stu-id="9c9f2-106">This multiple-valued attribute is used to store any configurable setting for the DS stored in the NAME=VALUE format.</span></span>



| <span data-ttu-id="9c9f2-107">進入</span><span class="sxs-lookup"><span data-stu-id="9c9f2-107">Entry</span></span> | <span data-ttu-id="9c9f2-108">值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9c9f2-109">CN</span><span class="sxs-lookup"><span data-stu-id="9c9f2-109">CN</span></span>                | <span data-ttu-id="9c9f2-110">ms DS-其他-設定</span><span class="sxs-lookup"><span data-stu-id="9c9f2-110">ms-DS-Other-Settings</span></span>                        |
| <span data-ttu-id="9c9f2-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9c9f2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9c9f2-112">其他設定</span><span class="sxs-lookup"><span data-stu-id="9c9f2-112">msDS-Other-Settings</span></span>                         |
| <span data-ttu-id="9c9f2-113">大小</span><span class="sxs-lookup"><span data-stu-id="9c9f2-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9c9f2-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9c9f2-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9c9f2-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9c9f2-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9c9f2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9c9f2-116">Attribute-Id</span></span>      | <span data-ttu-id="9c9f2-117">1.2.840.113556.1.4.1621</span><span class="sxs-lookup"><span data-stu-id="9c9f2-117">1.2.840.113556.1.4.1621</span></span>                     |
| <span data-ttu-id="9c9f2-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9c9f2-118">System-Id-Guid</span></span>    | <span data-ttu-id="9c9f2-119">79d2f34c-9d7d-42bb-838f-866b3e4400e2</span><span class="sxs-lookup"><span data-stu-id="9c9f2-119">79d2f34c-9d7d-42bb-838f-866b3e4400e2</span></span>        |
| <span data-ttu-id="9c9f2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c9f2-120">Syntax</span></span>            | [<span data-ttu-id="9c9f2-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9c9f2-122">實作</span><span class="sxs-lookup"><span data-stu-id="9c9f2-122">Implementations</span></span>

-   [<span data-ttu-id="9c9f2-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9c9f2-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9c9f2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9c9f2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9c9f2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9c9f2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9c9f2-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c9f2-129">Windows Server 2003</span></span>



| <span data-ttu-id="9c9f2-130">進入</span><span class="sxs-lookup"><span data-stu-id="9c9f2-130">Entry</span></span> | <span data-ttu-id="9c9f2-131">值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-131">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9c9f2-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9c9f2-132">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c9f2-133">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c9f2-134">System-Only</span></span>            | <span data-ttu-id="9c9f2-135">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-135">False</span></span>                                            |
| <span data-ttu-id="9c9f2-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9c9f2-137">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-137">False</span></span>                                            |
| <span data-ttu-id="9c9f2-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9c9f2-138">Is Indexed</span></span>             | <span data-ttu-id="9c9f2-139">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-139">False</span></span>                                            |
| <span data-ttu-id="9c9f2-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9c9f2-140">In Global Catalog</span></span>      | <span data-ttu-id="9c9f2-141">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-141">False</span></span>                                            |
| <span data-ttu-id="9c9f2-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9c9f2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c9f2-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9c9f2-143">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9c9f2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c9f2-144">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c9f2-145">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-146">Search-Flags</span></span>           | <span data-ttu-id="9c9f2-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c9f2-147">0x00000000</span></span>                                       |
| <span data-ttu-id="9c9f2-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-148">System-Flags</span></span>           | <span data-ttu-id="9c9f2-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c9f2-149">0x00000010</span></span>                                       |
| <span data-ttu-id="9c9f2-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9c9f2-150">Classes used in</span></span>        | [<span data-ttu-id="9c9f2-151">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-151">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9c9f2-152">亞當</span><span class="sxs-lookup"><span data-stu-id="9c9f2-152">ADAM</span></span>



| <span data-ttu-id="9c9f2-153">進入</span><span class="sxs-lookup"><span data-stu-id="9c9f2-153">Entry</span></span> | <span data-ttu-id="9c9f2-154">值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-154">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9c9f2-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9c9f2-155">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c9f2-156">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c9f2-157">System-Only</span></span>            | <span data-ttu-id="9c9f2-158">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-158">False</span></span>                                            |
| <span data-ttu-id="9c9f2-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9c9f2-160">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-160">False</span></span>                                            |
| <span data-ttu-id="9c9f2-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9c9f2-161">Is Indexed</span></span>             | <span data-ttu-id="9c9f2-162">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-162">False</span></span>                                            |
| <span data-ttu-id="9c9f2-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9c9f2-163">In Global Catalog</span></span>      | <span data-ttu-id="9c9f2-164">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-164">False</span></span>                                            |
| <span data-ttu-id="9c9f2-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9c9f2-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c9f2-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9c9f2-166">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9c9f2-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c9f2-167">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c9f2-168">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-169">Search-Flags</span></span>           | <span data-ttu-id="9c9f2-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c9f2-170">0x00000000</span></span>                                       |
| <span data-ttu-id="9c9f2-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-171">System-Flags</span></span>           | <span data-ttu-id="9c9f2-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c9f2-172">0x00000010</span></span>                                       |
| <span data-ttu-id="9c9f2-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9c9f2-173">Classes used in</span></span>        | [<span data-ttu-id="9c9f2-174">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-174">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9c9f2-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9c9f2-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9c9f2-176">進入</span><span class="sxs-lookup"><span data-stu-id="9c9f2-176">Entry</span></span> | <span data-ttu-id="9c9f2-177">值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-177">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9c9f2-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9c9f2-178">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c9f2-179">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c9f2-180">System-Only</span></span>            | <span data-ttu-id="9c9f2-181">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-181">False</span></span>                                            |
| <span data-ttu-id="9c9f2-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9c9f2-183">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-183">False</span></span>                                            |
| <span data-ttu-id="9c9f2-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9c9f2-184">Is Indexed</span></span>             | <span data-ttu-id="9c9f2-185">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-185">False</span></span>                                            |
| <span data-ttu-id="9c9f2-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9c9f2-186">In Global Catalog</span></span>      | <span data-ttu-id="9c9f2-187">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-187">False</span></span>                                            |
| <span data-ttu-id="9c9f2-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9c9f2-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c9f2-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9c9f2-189">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9c9f2-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c9f2-190">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c9f2-191">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-192">Search-Flags</span></span>           | <span data-ttu-id="9c9f2-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c9f2-193">0x00000000</span></span>                                       |
| <span data-ttu-id="9c9f2-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-194">System-Flags</span></span>           | <span data-ttu-id="9c9f2-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c9f2-195">0x00000010</span></span>                                       |
| <span data-ttu-id="9c9f2-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9c9f2-196">Classes used in</span></span>        | [<span data-ttu-id="9c9f2-197">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-197">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9c9f2-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c9f2-198">Windows Server 2008</span></span>



| <span data-ttu-id="9c9f2-199">進入</span><span class="sxs-lookup"><span data-stu-id="9c9f2-199">Entry</span></span> | <span data-ttu-id="9c9f2-200">值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-200">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9c9f2-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9c9f2-201">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c9f2-202">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c9f2-203">System-Only</span></span>            | <span data-ttu-id="9c9f2-204">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-204">False</span></span>                                            |
| <span data-ttu-id="9c9f2-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9c9f2-206">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-206">False</span></span>                                            |
| <span data-ttu-id="9c9f2-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9c9f2-207">Is Indexed</span></span>             | <span data-ttu-id="9c9f2-208">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-208">False</span></span>                                            |
| <span data-ttu-id="9c9f2-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9c9f2-209">In Global Catalog</span></span>      | <span data-ttu-id="9c9f2-210">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-210">False</span></span>                                            |
| <span data-ttu-id="9c9f2-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9c9f2-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c9f2-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9c9f2-212">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9c9f2-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c9f2-213">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c9f2-214">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-215">Search-Flags</span></span>           | <span data-ttu-id="9c9f2-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c9f2-216">0x00000000</span></span>                                       |
| <span data-ttu-id="9c9f2-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-217">System-Flags</span></span>           | <span data-ttu-id="9c9f2-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c9f2-218">0x00000010</span></span>                                       |
| <span data-ttu-id="9c9f2-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9c9f2-219">Classes used in</span></span>        | [<span data-ttu-id="9c9f2-220">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-220">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9c9f2-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c9f2-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9c9f2-222">進入</span><span class="sxs-lookup"><span data-stu-id="9c9f2-222">Entry</span></span> | <span data-ttu-id="9c9f2-223">值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-223">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9c9f2-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9c9f2-224">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c9f2-225">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c9f2-226">System-Only</span></span>            | <span data-ttu-id="9c9f2-227">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-227">False</span></span>                                            |
| <span data-ttu-id="9c9f2-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-228">Is-Single-Valued</span></span>       | <span data-ttu-id="9c9f2-229">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-229">False</span></span>                                            |
| <span data-ttu-id="9c9f2-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9c9f2-230">Is Indexed</span></span>             | <span data-ttu-id="9c9f2-231">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-231">False</span></span>                                            |
| <span data-ttu-id="9c9f2-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9c9f2-232">In Global Catalog</span></span>      | <span data-ttu-id="9c9f2-233">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-233">False</span></span>                                            |
| <span data-ttu-id="9c9f2-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9c9f2-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c9f2-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9c9f2-235">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9c9f2-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c9f2-236">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c9f2-237">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-238">Search-Flags</span></span>           | <span data-ttu-id="9c9f2-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c9f2-239">0x00000000</span></span>                                       |
| <span data-ttu-id="9c9f2-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-240">System-Flags</span></span>           | <span data-ttu-id="9c9f2-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c9f2-241">0x00000010</span></span>                                       |
| <span data-ttu-id="9c9f2-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9c9f2-242">Classes used in</span></span>        | [<span data-ttu-id="9c9f2-243">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-243">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9c9f2-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c9f2-244">Windows Server 2012</span></span>



| <span data-ttu-id="9c9f2-245">進入</span><span class="sxs-lookup"><span data-stu-id="9c9f2-245">Entry</span></span> | <span data-ttu-id="9c9f2-246">值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-246">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9c9f2-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9c9f2-247">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c9f2-248">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9c9f2-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c9f2-249">System-Only</span></span>            | <span data-ttu-id="9c9f2-250">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-250">False</span></span>                                            |
| <span data-ttu-id="9c9f2-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9c9f2-251">Is-Single-Valued</span></span>       | <span data-ttu-id="9c9f2-252">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-252">False</span></span>                                            |
| <span data-ttu-id="9c9f2-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9c9f2-253">Is Indexed</span></span>             | <span data-ttu-id="9c9f2-254">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-254">False</span></span>                                            |
| <span data-ttu-id="9c9f2-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9c9f2-255">In Global Catalog</span></span>      | <span data-ttu-id="9c9f2-256">否</span><span class="sxs-lookup"><span data-stu-id="9c9f2-256">False</span></span>                                            |
| <span data-ttu-id="9c9f2-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9c9f2-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c9f2-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9c9f2-258">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9c9f2-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c9f2-259">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c9f2-260">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9c9f2-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-261">Search-Flags</span></span>           | <span data-ttu-id="9c9f2-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c9f2-262">0x00000000</span></span>                                       |
| <span data-ttu-id="9c9f2-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c9f2-263">System-Flags</span></span>           | <span data-ttu-id="9c9f2-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c9f2-264">0x00000010</span></span>                                       |
| <span data-ttu-id="9c9f2-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9c9f2-265">Classes used in</span></span>        | [<span data-ttu-id="9c9f2-266">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="9c9f2-266">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 






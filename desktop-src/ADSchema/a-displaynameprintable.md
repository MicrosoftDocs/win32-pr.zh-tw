---
title: 顯示名稱-可列印屬性
description: 物件的可列印顯示名稱。
ms.assetid: e8e5ff25-66dd-4c74-9571-9ec765d6d1af
ms.tgt_platform: multiple
keywords:
- 顯示名稱-可列印的屬性 AD 架構
- displayNamePrintable 屬性 AD 架構
topic_type:
- apiref
api_name:
- Display-Name-Printable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eff05c2279f026e3a94b707b522509b4801ff27
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845571"
---
# <a name="display-name-printable-attribute"></a><span data-ttu-id="c5b15-105">顯示名稱-可列印屬性</span><span class="sxs-lookup"><span data-stu-id="c5b15-105">Display-Name-Printable attribute</span></span>

<span data-ttu-id="c5b15-106">物件的可列印顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c5b15-106">The printable display name for an object.</span></span> <span data-ttu-id="c5b15-107">可列印的顯示名稱通常是使用者名字、中間名縮寫和姓氏的組合。</span><span class="sxs-lookup"><span data-stu-id="c5b15-107">The printable display name is usually the combination of the user's first name, middle initial, and last name.</span></span>



| <span data-ttu-id="c5b15-108">進入</span><span class="sxs-lookup"><span data-stu-id="c5b15-108">Entry</span></span> | <span data-ttu-id="c5b15-109">值</span><span class="sxs-lookup"><span data-stu-id="c5b15-109">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="c5b15-110">CN</span><span class="sxs-lookup"><span data-stu-id="c5b15-110">CN</span></span>                | <span data-ttu-id="c5b15-111">顯示-名稱-可列印</span><span class="sxs-lookup"><span data-stu-id="c5b15-111">Display-Name-Printable</span></span>                 |
| <span data-ttu-id="c5b15-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c5b15-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c5b15-113">displayNamePrintable</span><span class="sxs-lookup"><span data-stu-id="c5b15-113">displayNamePrintable</span></span>                   |
| <span data-ttu-id="c5b15-114">大小</span><span class="sxs-lookup"><span data-stu-id="c5b15-114">Size</span></span>              | \-                                     |
| <span data-ttu-id="c5b15-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c5b15-115">Update Privilege</span></span>  | <span data-ttu-id="c5b15-116">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="c5b15-116">Domain administrator or account owner.</span></span> |
| <span data-ttu-id="c5b15-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c5b15-117">Update Frequency</span></span>  | \-                                     |
| <span data-ttu-id="c5b15-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c5b15-118">Attribute-Id</span></span>      | <span data-ttu-id="c5b15-119">1.2.840.113556.1.2.353</span><span class="sxs-lookup"><span data-stu-id="c5b15-119">1.2.840.113556.1.2.353</span></span>                 |
| <span data-ttu-id="c5b15-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c5b15-120">System-Id-Guid</span></span>    | <span data-ttu-id="c5b15-121">bf967954-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c5b15-121">bf967954-0de6-11d0-a285-00aa003049e2</span></span>   |
| <span data-ttu-id="c5b15-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5b15-122">Syntax</span></span>            | [<span data-ttu-id="c5b15-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="c5b15-123">**String(IA5)**</span></span>](s-string-ia5.md)    |



## <a name="implementations"></a><span data-ttu-id="c5b15-124">實作</span><span class="sxs-lookup"><span data-stu-id="c5b15-124">Implementations</span></span>

-   [<span data-ttu-id="c5b15-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c5b15-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c5b15-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c5b15-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c5b15-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c5b15-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c5b15-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c5b15-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c5b15-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c5b15-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c5b15-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c5b15-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c5b15-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5b15-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c5b15-132">進入</span><span class="sxs-lookup"><span data-stu-id="c5b15-132">Entry</span></span> | <span data-ttu-id="c5b15-133">值</span><span class="sxs-lookup"><span data-stu-id="c5b15-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5b15-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c5b15-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5b15-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5b15-135">MAPI-Id</span></span>                | <span data-ttu-id="c5b15-136">0x39FF</span><span class="sxs-lookup"><span data-stu-id="c5b15-136">0x39FF</span></span>                          |
| <span data-ttu-id="c5b15-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5b15-137">System-Only</span></span>            | <span data-ttu-id="c5b15-138">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-138">False</span></span>                           |
| <span data-ttu-id="c5b15-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c5b15-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c5b15-140">對</span><span class="sxs-lookup"><span data-stu-id="c5b15-140">True</span></span>                            |
| <span data-ttu-id="c5b15-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c5b15-141">Is Indexed</span></span>             | <span data-ttu-id="c5b15-142">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-142">False</span></span>                           |
| <span data-ttu-id="c5b15-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c5b15-143">In Global Catalog</span></span>      | <span data-ttu-id="c5b15-144">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-144">False</span></span>                           |
| <span data-ttu-id="c5b15-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c5b15-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5b15-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c5b15-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5b15-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5b15-147">Range-Lower</span></span>            | <span data-ttu-id="c5b15-148">1</span><span class="sxs-lookup"><span data-stu-id="c5b15-148">1</span></span>                               |
| <span data-ttu-id="c5b15-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5b15-149">Range-Upper</span></span>            | <span data-ttu-id="c5b15-150">256</span><span class="sxs-lookup"><span data-stu-id="c5b15-150">256</span></span>                             |
| <span data-ttu-id="c5b15-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-151">Search-Flags</span></span>           | <span data-ttu-id="c5b15-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5b15-152">0x00000000</span></span>                      |
| <span data-ttu-id="c5b15-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-153">System-Flags</span></span>           | <span data-ttu-id="c5b15-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5b15-154">0x00000010</span></span>                      |
| <span data-ttu-id="c5b15-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c5b15-155">Classes used in</span></span>        | [<span data-ttu-id="c5b15-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c5b15-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c5b15-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5b15-157">Windows Server 2003</span></span>



| <span data-ttu-id="c5b15-158">進入</span><span class="sxs-lookup"><span data-stu-id="c5b15-158">Entry</span></span> | <span data-ttu-id="c5b15-159">值</span><span class="sxs-lookup"><span data-stu-id="c5b15-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5b15-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c5b15-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5b15-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5b15-161">MAPI-Id</span></span>                | <span data-ttu-id="c5b15-162">0x39FF</span><span class="sxs-lookup"><span data-stu-id="c5b15-162">0x39FF</span></span>                          |
| <span data-ttu-id="c5b15-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5b15-163">System-Only</span></span>            | <span data-ttu-id="c5b15-164">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-164">False</span></span>                           |
| <span data-ttu-id="c5b15-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c5b15-165">Is-Single-Valued</span></span>       | <span data-ttu-id="c5b15-166">對</span><span class="sxs-lookup"><span data-stu-id="c5b15-166">True</span></span>                            |
| <span data-ttu-id="c5b15-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c5b15-167">Is Indexed</span></span>             | <span data-ttu-id="c5b15-168">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-168">False</span></span>                           |
| <span data-ttu-id="c5b15-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c5b15-169">In Global Catalog</span></span>      | <span data-ttu-id="c5b15-170">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-170">False</span></span>                           |
| <span data-ttu-id="c5b15-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c5b15-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5b15-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c5b15-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5b15-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5b15-173">Range-Lower</span></span>            | <span data-ttu-id="c5b15-174">1</span><span class="sxs-lookup"><span data-stu-id="c5b15-174">1</span></span>                               |
| <span data-ttu-id="c5b15-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5b15-175">Range-Upper</span></span>            | <span data-ttu-id="c5b15-176">256</span><span class="sxs-lookup"><span data-stu-id="c5b15-176">256</span></span>                             |
| <span data-ttu-id="c5b15-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-177">Search-Flags</span></span>           | <span data-ttu-id="c5b15-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5b15-178">0x00000000</span></span>                      |
| <span data-ttu-id="c5b15-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-179">System-Flags</span></span>           | <span data-ttu-id="c5b15-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5b15-180">0x00000010</span></span>                      |
| <span data-ttu-id="c5b15-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c5b15-181">Classes used in</span></span>        | [<span data-ttu-id="c5b15-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c5b15-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c5b15-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c5b15-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c5b15-184">進入</span><span class="sxs-lookup"><span data-stu-id="c5b15-184">Entry</span></span> | <span data-ttu-id="c5b15-185">值</span><span class="sxs-lookup"><span data-stu-id="c5b15-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5b15-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c5b15-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5b15-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5b15-187">MAPI-Id</span></span>                | <span data-ttu-id="c5b15-188">0x39FF</span><span class="sxs-lookup"><span data-stu-id="c5b15-188">0x39FF</span></span>                          |
| <span data-ttu-id="c5b15-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5b15-189">System-Only</span></span>            | <span data-ttu-id="c5b15-190">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-190">False</span></span>                           |
| <span data-ttu-id="c5b15-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c5b15-191">Is-Single-Valued</span></span>       | <span data-ttu-id="c5b15-192">對</span><span class="sxs-lookup"><span data-stu-id="c5b15-192">True</span></span>                            |
| <span data-ttu-id="c5b15-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c5b15-193">Is Indexed</span></span>             | <span data-ttu-id="c5b15-194">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-194">False</span></span>                           |
| <span data-ttu-id="c5b15-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c5b15-195">In Global Catalog</span></span>      | <span data-ttu-id="c5b15-196">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-196">False</span></span>                           |
| <span data-ttu-id="c5b15-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c5b15-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5b15-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c5b15-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5b15-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5b15-199">Range-Lower</span></span>            | <span data-ttu-id="c5b15-200">1</span><span class="sxs-lookup"><span data-stu-id="c5b15-200">1</span></span>                               |
| <span data-ttu-id="c5b15-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5b15-201">Range-Upper</span></span>            | <span data-ttu-id="c5b15-202">256</span><span class="sxs-lookup"><span data-stu-id="c5b15-202">256</span></span>                             |
| <span data-ttu-id="c5b15-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-203">Search-Flags</span></span>           | <span data-ttu-id="c5b15-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5b15-204">0x00000000</span></span>                      |
| <span data-ttu-id="c5b15-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-205">System-Flags</span></span>           | <span data-ttu-id="c5b15-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5b15-206">0x00000010</span></span>                      |
| <span data-ttu-id="c5b15-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c5b15-207">Classes used in</span></span>        | [<span data-ttu-id="c5b15-208">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c5b15-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c5b15-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5b15-209">Windows Server 2008</span></span>



| <span data-ttu-id="c5b15-210">進入</span><span class="sxs-lookup"><span data-stu-id="c5b15-210">Entry</span></span> | <span data-ttu-id="c5b15-211">值</span><span class="sxs-lookup"><span data-stu-id="c5b15-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5b15-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c5b15-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5b15-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5b15-213">MAPI-Id</span></span>                | <span data-ttu-id="c5b15-214">0x39FF</span><span class="sxs-lookup"><span data-stu-id="c5b15-214">0x39FF</span></span>                          |
| <span data-ttu-id="c5b15-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5b15-215">System-Only</span></span>            | <span data-ttu-id="c5b15-216">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-216">False</span></span>                           |
| <span data-ttu-id="c5b15-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c5b15-217">Is-Single-Valued</span></span>       | <span data-ttu-id="c5b15-218">對</span><span class="sxs-lookup"><span data-stu-id="c5b15-218">True</span></span>                            |
| <span data-ttu-id="c5b15-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c5b15-219">Is Indexed</span></span>             | <span data-ttu-id="c5b15-220">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-220">False</span></span>                           |
| <span data-ttu-id="c5b15-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c5b15-221">In Global Catalog</span></span>      | <span data-ttu-id="c5b15-222">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-222">False</span></span>                           |
| <span data-ttu-id="c5b15-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c5b15-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5b15-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c5b15-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5b15-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5b15-225">Range-Lower</span></span>            | <span data-ttu-id="c5b15-226">1</span><span class="sxs-lookup"><span data-stu-id="c5b15-226">1</span></span>                               |
| <span data-ttu-id="c5b15-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5b15-227">Range-Upper</span></span>            | <span data-ttu-id="c5b15-228">256</span><span class="sxs-lookup"><span data-stu-id="c5b15-228">256</span></span>                             |
| <span data-ttu-id="c5b15-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-229">Search-Flags</span></span>           | <span data-ttu-id="c5b15-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5b15-230">0x00000000</span></span>                      |
| <span data-ttu-id="c5b15-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-231">System-Flags</span></span>           | <span data-ttu-id="c5b15-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5b15-232">0x00000010</span></span>                      |
| <span data-ttu-id="c5b15-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c5b15-233">Classes used in</span></span>        | [<span data-ttu-id="c5b15-234">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c5b15-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c5b15-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c5b15-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c5b15-236">進入</span><span class="sxs-lookup"><span data-stu-id="c5b15-236">Entry</span></span> | <span data-ttu-id="c5b15-237">值</span><span class="sxs-lookup"><span data-stu-id="c5b15-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5b15-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c5b15-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5b15-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5b15-239">MAPI-Id</span></span>                | <span data-ttu-id="c5b15-240">0x39FF</span><span class="sxs-lookup"><span data-stu-id="c5b15-240">0x39FF</span></span>                          |
| <span data-ttu-id="c5b15-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5b15-241">System-Only</span></span>            | <span data-ttu-id="c5b15-242">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-242">False</span></span>                           |
| <span data-ttu-id="c5b15-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c5b15-243">Is-Single-Valued</span></span>       | <span data-ttu-id="c5b15-244">對</span><span class="sxs-lookup"><span data-stu-id="c5b15-244">True</span></span>                            |
| <span data-ttu-id="c5b15-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c5b15-245">Is Indexed</span></span>             | <span data-ttu-id="c5b15-246">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-246">False</span></span>                           |
| <span data-ttu-id="c5b15-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c5b15-247">In Global Catalog</span></span>      | <span data-ttu-id="c5b15-248">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-248">False</span></span>                           |
| <span data-ttu-id="c5b15-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c5b15-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5b15-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c5b15-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5b15-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5b15-251">Range-Lower</span></span>            | <span data-ttu-id="c5b15-252">1</span><span class="sxs-lookup"><span data-stu-id="c5b15-252">1</span></span>                               |
| <span data-ttu-id="c5b15-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5b15-253">Range-Upper</span></span>            | <span data-ttu-id="c5b15-254">256</span><span class="sxs-lookup"><span data-stu-id="c5b15-254">256</span></span>                             |
| <span data-ttu-id="c5b15-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-255">Search-Flags</span></span>           | <span data-ttu-id="c5b15-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5b15-256">0x00000000</span></span>                      |
| <span data-ttu-id="c5b15-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-257">System-Flags</span></span>           | <span data-ttu-id="c5b15-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5b15-258">0x00000010</span></span>                      |
| <span data-ttu-id="c5b15-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c5b15-259">Classes used in</span></span>        | [<span data-ttu-id="c5b15-260">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c5b15-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c5b15-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5b15-261">Windows Server 2012</span></span>



| <span data-ttu-id="c5b15-262">進入</span><span class="sxs-lookup"><span data-stu-id="c5b15-262">Entry</span></span> | <span data-ttu-id="c5b15-263">值</span><span class="sxs-lookup"><span data-stu-id="c5b15-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5b15-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c5b15-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5b15-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5b15-265">MAPI-Id</span></span>                | <span data-ttu-id="c5b15-266">0x39FF</span><span class="sxs-lookup"><span data-stu-id="c5b15-266">0x39FF</span></span>                          |
| <span data-ttu-id="c5b15-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5b15-267">System-Only</span></span>            | <span data-ttu-id="c5b15-268">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-268">False</span></span>                           |
| <span data-ttu-id="c5b15-269">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c5b15-269">Is-Single-Valued</span></span>       | <span data-ttu-id="c5b15-270">對</span><span class="sxs-lookup"><span data-stu-id="c5b15-270">True</span></span>                            |
| <span data-ttu-id="c5b15-271">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c5b15-271">Is Indexed</span></span>             | <span data-ttu-id="c5b15-272">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-272">False</span></span>                           |
| <span data-ttu-id="c5b15-273">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c5b15-273">In Global Catalog</span></span>      | <span data-ttu-id="c5b15-274">否</span><span class="sxs-lookup"><span data-stu-id="c5b15-274">False</span></span>                           |
| <span data-ttu-id="c5b15-275">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c5b15-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5b15-276">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c5b15-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5b15-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5b15-277">Range-Lower</span></span>            | <span data-ttu-id="c5b15-278">1</span><span class="sxs-lookup"><span data-stu-id="c5b15-278">1</span></span>                               |
| <span data-ttu-id="c5b15-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5b15-279">Range-Upper</span></span>            | <span data-ttu-id="c5b15-280">256</span><span class="sxs-lookup"><span data-stu-id="c5b15-280">256</span></span>                             |
| <span data-ttu-id="c5b15-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-281">Search-Flags</span></span>           | <span data-ttu-id="c5b15-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5b15-282">0x00000000</span></span>                      |
| <span data-ttu-id="c5b15-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5b15-283">System-Flags</span></span>           | <span data-ttu-id="c5b15-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5b15-284">0x00000010</span></span>                      |
| <span data-ttu-id="c5b15-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c5b15-285">Classes used in</span></span>        | [<span data-ttu-id="c5b15-286">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c5b15-286">**Top**</span></span>](c-top.md)<br/> |



 

 






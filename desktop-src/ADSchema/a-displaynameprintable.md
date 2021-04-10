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
# <a name="display-name-printable-attribute"></a><span data-ttu-id="40a0a-105">顯示名稱-可列印屬性</span><span class="sxs-lookup"><span data-stu-id="40a0a-105">Display-Name-Printable attribute</span></span>

<span data-ttu-id="40a0a-106">物件的可列印顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="40a0a-106">The printable display name for an object.</span></span> <span data-ttu-id="40a0a-107">可列印的顯示名稱通常是使用者名字、中間名縮寫和姓氏的組合。</span><span class="sxs-lookup"><span data-stu-id="40a0a-107">The printable display name is usually the combination of the user's first name, middle initial, and last name.</span></span>



| <span data-ttu-id="40a0a-108">進入</span><span class="sxs-lookup"><span data-stu-id="40a0a-108">Entry</span></span> | <span data-ttu-id="40a0a-109">值</span><span class="sxs-lookup"><span data-stu-id="40a0a-109">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="40a0a-110">CN</span><span class="sxs-lookup"><span data-stu-id="40a0a-110">CN</span></span>                | <span data-ttu-id="40a0a-111">顯示-名稱-可列印</span><span class="sxs-lookup"><span data-stu-id="40a0a-111">Display-Name-Printable</span></span>                 |
| <span data-ttu-id="40a0a-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="40a0a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="40a0a-113">displayNamePrintable</span><span class="sxs-lookup"><span data-stu-id="40a0a-113">displayNamePrintable</span></span>                   |
| <span data-ttu-id="40a0a-114">大小</span><span class="sxs-lookup"><span data-stu-id="40a0a-114">Size</span></span>              | \-                                     |
| <span data-ttu-id="40a0a-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="40a0a-115">Update Privilege</span></span>  | <span data-ttu-id="40a0a-116">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="40a0a-116">Domain administrator or account owner.</span></span> |
| <span data-ttu-id="40a0a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="40a0a-117">Update Frequency</span></span>  | \-                                     |
| <span data-ttu-id="40a0a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="40a0a-118">Attribute-Id</span></span>      | <span data-ttu-id="40a0a-119">1.2.840.113556.1.2.353</span><span class="sxs-lookup"><span data-stu-id="40a0a-119">1.2.840.113556.1.2.353</span></span>                 |
| <span data-ttu-id="40a0a-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="40a0a-120">System-Id-Guid</span></span>    | <span data-ttu-id="40a0a-121">bf967954-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="40a0a-121">bf967954-0de6-11d0-a285-00aa003049e2</span></span>   |
| <span data-ttu-id="40a0a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="40a0a-122">Syntax</span></span>            | [<span data-ttu-id="40a0a-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="40a0a-123">**String(IA5)**</span></span>](s-string-ia5.md)    |



## <a name="implementations"></a><span data-ttu-id="40a0a-124">實作</span><span class="sxs-lookup"><span data-stu-id="40a0a-124">Implementations</span></span>

-   [<span data-ttu-id="40a0a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="40a0a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="40a0a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="40a0a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="40a0a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="40a0a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="40a0a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="40a0a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="40a0a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="40a0a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="40a0a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="40a0a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="40a0a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="40a0a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="40a0a-132">進入</span><span class="sxs-lookup"><span data-stu-id="40a0a-132">Entry</span></span> | <span data-ttu-id="40a0a-133">值</span><span class="sxs-lookup"><span data-stu-id="40a0a-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="40a0a-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="40a0a-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="40a0a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40a0a-135">MAPI-Id</span></span>                | <span data-ttu-id="40a0a-136">0x39FF</span><span class="sxs-lookup"><span data-stu-id="40a0a-136">0x39FF</span></span>                          |
| <span data-ttu-id="40a0a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="40a0a-137">System-Only</span></span>            | <span data-ttu-id="40a0a-138">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-138">False</span></span>                           |
| <span data-ttu-id="40a0a-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="40a0a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="40a0a-140">對</span><span class="sxs-lookup"><span data-stu-id="40a0a-140">True</span></span>                            |
| <span data-ttu-id="40a0a-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="40a0a-141">Is Indexed</span></span>             | <span data-ttu-id="40a0a-142">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-142">False</span></span>                           |
| <span data-ttu-id="40a0a-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="40a0a-143">In Global Catalog</span></span>      | <span data-ttu-id="40a0a-144">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-144">False</span></span>                           |
| <span data-ttu-id="40a0a-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="40a0a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="40a0a-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="40a0a-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="40a0a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40a0a-147">Range-Lower</span></span>            | <span data-ttu-id="40a0a-148">1</span><span class="sxs-lookup"><span data-stu-id="40a0a-148">1</span></span>                               |
| <span data-ttu-id="40a0a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40a0a-149">Range-Upper</span></span>            | <span data-ttu-id="40a0a-150">256</span><span class="sxs-lookup"><span data-stu-id="40a0a-150">256</span></span>                             |
| <span data-ttu-id="40a0a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-151">Search-Flags</span></span>           | <span data-ttu-id="40a0a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40a0a-152">0x00000000</span></span>                      |
| <span data-ttu-id="40a0a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-153">System-Flags</span></span>           | <span data-ttu-id="40a0a-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40a0a-154">0x00000010</span></span>                      |
| <span data-ttu-id="40a0a-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="40a0a-155">Classes used in</span></span>        | [<span data-ttu-id="40a0a-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="40a0a-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="40a0a-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40a0a-157">Windows Server 2003</span></span>



| <span data-ttu-id="40a0a-158">進入</span><span class="sxs-lookup"><span data-stu-id="40a0a-158">Entry</span></span> | <span data-ttu-id="40a0a-159">值</span><span class="sxs-lookup"><span data-stu-id="40a0a-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="40a0a-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="40a0a-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="40a0a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40a0a-161">MAPI-Id</span></span>                | <span data-ttu-id="40a0a-162">0x39FF</span><span class="sxs-lookup"><span data-stu-id="40a0a-162">0x39FF</span></span>                          |
| <span data-ttu-id="40a0a-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="40a0a-163">System-Only</span></span>            | <span data-ttu-id="40a0a-164">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-164">False</span></span>                           |
| <span data-ttu-id="40a0a-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="40a0a-165">Is-Single-Valued</span></span>       | <span data-ttu-id="40a0a-166">對</span><span class="sxs-lookup"><span data-stu-id="40a0a-166">True</span></span>                            |
| <span data-ttu-id="40a0a-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="40a0a-167">Is Indexed</span></span>             | <span data-ttu-id="40a0a-168">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-168">False</span></span>                           |
| <span data-ttu-id="40a0a-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="40a0a-169">In Global Catalog</span></span>      | <span data-ttu-id="40a0a-170">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-170">False</span></span>                           |
| <span data-ttu-id="40a0a-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="40a0a-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="40a0a-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="40a0a-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="40a0a-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40a0a-173">Range-Lower</span></span>            | <span data-ttu-id="40a0a-174">1</span><span class="sxs-lookup"><span data-stu-id="40a0a-174">1</span></span>                               |
| <span data-ttu-id="40a0a-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40a0a-175">Range-Upper</span></span>            | <span data-ttu-id="40a0a-176">256</span><span class="sxs-lookup"><span data-stu-id="40a0a-176">256</span></span>                             |
| <span data-ttu-id="40a0a-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-177">Search-Flags</span></span>           | <span data-ttu-id="40a0a-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40a0a-178">0x00000000</span></span>                      |
| <span data-ttu-id="40a0a-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-179">System-Flags</span></span>           | <span data-ttu-id="40a0a-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40a0a-180">0x00000010</span></span>                      |
| <span data-ttu-id="40a0a-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="40a0a-181">Classes used in</span></span>        | [<span data-ttu-id="40a0a-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="40a0a-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="40a0a-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="40a0a-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="40a0a-184">進入</span><span class="sxs-lookup"><span data-stu-id="40a0a-184">Entry</span></span> | <span data-ttu-id="40a0a-185">值</span><span class="sxs-lookup"><span data-stu-id="40a0a-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="40a0a-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="40a0a-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="40a0a-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40a0a-187">MAPI-Id</span></span>                | <span data-ttu-id="40a0a-188">0x39FF</span><span class="sxs-lookup"><span data-stu-id="40a0a-188">0x39FF</span></span>                          |
| <span data-ttu-id="40a0a-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="40a0a-189">System-Only</span></span>            | <span data-ttu-id="40a0a-190">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-190">False</span></span>                           |
| <span data-ttu-id="40a0a-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="40a0a-191">Is-Single-Valued</span></span>       | <span data-ttu-id="40a0a-192">對</span><span class="sxs-lookup"><span data-stu-id="40a0a-192">True</span></span>                            |
| <span data-ttu-id="40a0a-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="40a0a-193">Is Indexed</span></span>             | <span data-ttu-id="40a0a-194">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-194">False</span></span>                           |
| <span data-ttu-id="40a0a-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="40a0a-195">In Global Catalog</span></span>      | <span data-ttu-id="40a0a-196">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-196">False</span></span>                           |
| <span data-ttu-id="40a0a-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="40a0a-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="40a0a-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="40a0a-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="40a0a-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40a0a-199">Range-Lower</span></span>            | <span data-ttu-id="40a0a-200">1</span><span class="sxs-lookup"><span data-stu-id="40a0a-200">1</span></span>                               |
| <span data-ttu-id="40a0a-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40a0a-201">Range-Upper</span></span>            | <span data-ttu-id="40a0a-202">256</span><span class="sxs-lookup"><span data-stu-id="40a0a-202">256</span></span>                             |
| <span data-ttu-id="40a0a-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-203">Search-Flags</span></span>           | <span data-ttu-id="40a0a-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40a0a-204">0x00000000</span></span>                      |
| <span data-ttu-id="40a0a-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-205">System-Flags</span></span>           | <span data-ttu-id="40a0a-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40a0a-206">0x00000010</span></span>                      |
| <span data-ttu-id="40a0a-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="40a0a-207">Classes used in</span></span>        | [<span data-ttu-id="40a0a-208">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="40a0a-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="40a0a-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40a0a-209">Windows Server 2008</span></span>



| <span data-ttu-id="40a0a-210">進入</span><span class="sxs-lookup"><span data-stu-id="40a0a-210">Entry</span></span> | <span data-ttu-id="40a0a-211">值</span><span class="sxs-lookup"><span data-stu-id="40a0a-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="40a0a-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="40a0a-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="40a0a-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40a0a-213">MAPI-Id</span></span>                | <span data-ttu-id="40a0a-214">0x39FF</span><span class="sxs-lookup"><span data-stu-id="40a0a-214">0x39FF</span></span>                          |
| <span data-ttu-id="40a0a-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="40a0a-215">System-Only</span></span>            | <span data-ttu-id="40a0a-216">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-216">False</span></span>                           |
| <span data-ttu-id="40a0a-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="40a0a-217">Is-Single-Valued</span></span>       | <span data-ttu-id="40a0a-218">對</span><span class="sxs-lookup"><span data-stu-id="40a0a-218">True</span></span>                            |
| <span data-ttu-id="40a0a-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="40a0a-219">Is Indexed</span></span>             | <span data-ttu-id="40a0a-220">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-220">False</span></span>                           |
| <span data-ttu-id="40a0a-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="40a0a-221">In Global Catalog</span></span>      | <span data-ttu-id="40a0a-222">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-222">False</span></span>                           |
| <span data-ttu-id="40a0a-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="40a0a-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="40a0a-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="40a0a-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="40a0a-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40a0a-225">Range-Lower</span></span>            | <span data-ttu-id="40a0a-226">1</span><span class="sxs-lookup"><span data-stu-id="40a0a-226">1</span></span>                               |
| <span data-ttu-id="40a0a-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40a0a-227">Range-Upper</span></span>            | <span data-ttu-id="40a0a-228">256</span><span class="sxs-lookup"><span data-stu-id="40a0a-228">256</span></span>                             |
| <span data-ttu-id="40a0a-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-229">Search-Flags</span></span>           | <span data-ttu-id="40a0a-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40a0a-230">0x00000000</span></span>                      |
| <span data-ttu-id="40a0a-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-231">System-Flags</span></span>           | <span data-ttu-id="40a0a-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40a0a-232">0x00000010</span></span>                      |
| <span data-ttu-id="40a0a-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="40a0a-233">Classes used in</span></span>        | [<span data-ttu-id="40a0a-234">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="40a0a-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="40a0a-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="40a0a-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="40a0a-236">進入</span><span class="sxs-lookup"><span data-stu-id="40a0a-236">Entry</span></span> | <span data-ttu-id="40a0a-237">值</span><span class="sxs-lookup"><span data-stu-id="40a0a-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="40a0a-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="40a0a-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="40a0a-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40a0a-239">MAPI-Id</span></span>                | <span data-ttu-id="40a0a-240">0x39FF</span><span class="sxs-lookup"><span data-stu-id="40a0a-240">0x39FF</span></span>                          |
| <span data-ttu-id="40a0a-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="40a0a-241">System-Only</span></span>            | <span data-ttu-id="40a0a-242">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-242">False</span></span>                           |
| <span data-ttu-id="40a0a-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="40a0a-243">Is-Single-Valued</span></span>       | <span data-ttu-id="40a0a-244">對</span><span class="sxs-lookup"><span data-stu-id="40a0a-244">True</span></span>                            |
| <span data-ttu-id="40a0a-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="40a0a-245">Is Indexed</span></span>             | <span data-ttu-id="40a0a-246">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-246">False</span></span>                           |
| <span data-ttu-id="40a0a-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="40a0a-247">In Global Catalog</span></span>      | <span data-ttu-id="40a0a-248">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-248">False</span></span>                           |
| <span data-ttu-id="40a0a-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="40a0a-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="40a0a-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="40a0a-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="40a0a-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40a0a-251">Range-Lower</span></span>            | <span data-ttu-id="40a0a-252">1</span><span class="sxs-lookup"><span data-stu-id="40a0a-252">1</span></span>                               |
| <span data-ttu-id="40a0a-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40a0a-253">Range-Upper</span></span>            | <span data-ttu-id="40a0a-254">256</span><span class="sxs-lookup"><span data-stu-id="40a0a-254">256</span></span>                             |
| <span data-ttu-id="40a0a-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-255">Search-Flags</span></span>           | <span data-ttu-id="40a0a-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40a0a-256">0x00000000</span></span>                      |
| <span data-ttu-id="40a0a-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-257">System-Flags</span></span>           | <span data-ttu-id="40a0a-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40a0a-258">0x00000010</span></span>                      |
| <span data-ttu-id="40a0a-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="40a0a-259">Classes used in</span></span>        | [<span data-ttu-id="40a0a-260">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="40a0a-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="40a0a-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="40a0a-261">Windows Server 2012</span></span>



| <span data-ttu-id="40a0a-262">進入</span><span class="sxs-lookup"><span data-stu-id="40a0a-262">Entry</span></span> | <span data-ttu-id="40a0a-263">值</span><span class="sxs-lookup"><span data-stu-id="40a0a-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="40a0a-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="40a0a-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="40a0a-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40a0a-265">MAPI-Id</span></span>                | <span data-ttu-id="40a0a-266">0x39FF</span><span class="sxs-lookup"><span data-stu-id="40a0a-266">0x39FF</span></span>                          |
| <span data-ttu-id="40a0a-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="40a0a-267">System-Only</span></span>            | <span data-ttu-id="40a0a-268">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-268">False</span></span>                           |
| <span data-ttu-id="40a0a-269">是-單一值</span><span class="sxs-lookup"><span data-stu-id="40a0a-269">Is-Single-Valued</span></span>       | <span data-ttu-id="40a0a-270">對</span><span class="sxs-lookup"><span data-stu-id="40a0a-270">True</span></span>                            |
| <span data-ttu-id="40a0a-271">已編制索引</span><span class="sxs-lookup"><span data-stu-id="40a0a-271">Is Indexed</span></span>             | <span data-ttu-id="40a0a-272">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-272">False</span></span>                           |
| <span data-ttu-id="40a0a-273">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="40a0a-273">In Global Catalog</span></span>      | <span data-ttu-id="40a0a-274">否</span><span class="sxs-lookup"><span data-stu-id="40a0a-274">False</span></span>                           |
| <span data-ttu-id="40a0a-275">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="40a0a-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="40a0a-276">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="40a0a-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="40a0a-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40a0a-277">Range-Lower</span></span>            | <span data-ttu-id="40a0a-278">1</span><span class="sxs-lookup"><span data-stu-id="40a0a-278">1</span></span>                               |
| <span data-ttu-id="40a0a-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40a0a-279">Range-Upper</span></span>            | <span data-ttu-id="40a0a-280">256</span><span class="sxs-lookup"><span data-stu-id="40a0a-280">256</span></span>                             |
| <span data-ttu-id="40a0a-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-281">Search-Flags</span></span>           | <span data-ttu-id="40a0a-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40a0a-282">0x00000000</span></span>                      |
| <span data-ttu-id="40a0a-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40a0a-283">System-Flags</span></span>           | <span data-ttu-id="40a0a-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40a0a-284">0x00000010</span></span>                      |
| <span data-ttu-id="40a0a-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="40a0a-285">Classes used in</span></span>        | [<span data-ttu-id="40a0a-286">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="40a0a-286">**Top**</span></span>](c-top.md)<br/> |



 

 






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
# <a name="display-name-printable-attribute"></a><span data-ttu-id="8e8e3-105">顯示名稱-可列印屬性</span><span class="sxs-lookup"><span data-stu-id="8e8e3-105">Display-Name-Printable attribute</span></span>

<span data-ttu-id="8e8e3-106">物件的可列印顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8e8e3-106">The printable display name for an object.</span></span> <span data-ttu-id="8e8e3-107">可列印的顯示名稱通常是使用者名字、中間名縮寫和姓氏的組合。</span><span class="sxs-lookup"><span data-stu-id="8e8e3-107">The printable display name is usually the combination of the user's first name, middle initial, and last name.</span></span>



| <span data-ttu-id="8e8e3-108">進入</span><span class="sxs-lookup"><span data-stu-id="8e8e3-108">Entry</span></span> | <span data-ttu-id="8e8e3-109">值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-109">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="8e8e3-110">CN</span><span class="sxs-lookup"><span data-stu-id="8e8e3-110">CN</span></span>                | <span data-ttu-id="8e8e3-111">顯示-名稱-可列印</span><span class="sxs-lookup"><span data-stu-id="8e8e3-111">Display-Name-Printable</span></span>                 |
| <span data-ttu-id="8e8e3-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8e8e3-112">Ldap-Display-Name</span></span> | <span data-ttu-id="8e8e3-113">displayNamePrintable</span><span class="sxs-lookup"><span data-stu-id="8e8e3-113">displayNamePrintable</span></span>                   |
| <span data-ttu-id="8e8e3-114">大小</span><span class="sxs-lookup"><span data-stu-id="8e8e3-114">Size</span></span>              | \-                                     |
| <span data-ttu-id="8e8e3-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8e8e3-115">Update Privilege</span></span>  | <span data-ttu-id="8e8e3-116">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="8e8e3-116">Domain administrator or account owner.</span></span> |
| <span data-ttu-id="8e8e3-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8e8e3-117">Update Frequency</span></span>  | \-                                     |
| <span data-ttu-id="8e8e3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8e8e3-118">Attribute-Id</span></span>      | <span data-ttu-id="8e8e3-119">1.2.840.113556.1.2.353</span><span class="sxs-lookup"><span data-stu-id="8e8e3-119">1.2.840.113556.1.2.353</span></span>                 |
| <span data-ttu-id="8e8e3-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8e8e3-120">System-Id-Guid</span></span>    | <span data-ttu-id="8e8e3-121">bf967954-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8e8e3-121">bf967954-0de6-11d0-a285-00aa003049e2</span></span>   |
| <span data-ttu-id="8e8e3-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e8e3-122">Syntax</span></span>            | [<span data-ttu-id="8e8e3-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-123">**String(IA5)**</span></span>](s-string-ia5.md)    |



## <a name="implementations"></a><span data-ttu-id="8e8e3-124">實作</span><span class="sxs-lookup"><span data-stu-id="8e8e3-124">Implementations</span></span>

-   [<span data-ttu-id="8e8e3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8e8e3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8e8e3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8e8e3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e8e3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e8e3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8e8e3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8e8e3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8e8e3-132">進入</span><span class="sxs-lookup"><span data-stu-id="8e8e3-132">Entry</span></span> | <span data-ttu-id="8e8e3-133">值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8e8e3-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8e8e3-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8e8e3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e8e3-135">MAPI-Id</span></span>                | <span data-ttu-id="8e8e3-136">0x39FF</span><span class="sxs-lookup"><span data-stu-id="8e8e3-136">0x39FF</span></span>                          |
| <span data-ttu-id="8e8e3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e8e3-137">System-Only</span></span>            | <span data-ttu-id="8e8e3-138">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-138">False</span></span>                           |
| <span data-ttu-id="8e8e3-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8e8e3-140">對</span><span class="sxs-lookup"><span data-stu-id="8e8e3-140">True</span></span>                            |
| <span data-ttu-id="8e8e3-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8e8e3-141">Is Indexed</span></span>             | <span data-ttu-id="8e8e3-142">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-142">False</span></span>                           |
| <span data-ttu-id="8e8e3-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8e8e3-143">In Global Catalog</span></span>      | <span data-ttu-id="8e8e3-144">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-144">False</span></span>                           |
| <span data-ttu-id="8e8e3-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8e8e3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e8e3-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8e8e3-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8e8e3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e8e3-147">Range-Lower</span></span>            | <span data-ttu-id="8e8e3-148">1</span><span class="sxs-lookup"><span data-stu-id="8e8e3-148">1</span></span>                               |
| <span data-ttu-id="8e8e3-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e8e3-149">Range-Upper</span></span>            | <span data-ttu-id="8e8e3-150">256</span><span class="sxs-lookup"><span data-stu-id="8e8e3-150">256</span></span>                             |
| <span data-ttu-id="8e8e3-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-151">Search-Flags</span></span>           | <span data-ttu-id="8e8e3-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e8e3-152">0x00000000</span></span>                      |
| <span data-ttu-id="8e8e3-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-153">System-Flags</span></span>           | <span data-ttu-id="8e8e3-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e8e3-154">0x00000010</span></span>                      |
| <span data-ttu-id="8e8e3-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8e8e3-155">Classes used in</span></span>        | [<span data-ttu-id="8e8e3-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8e8e3-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e8e3-157">Windows Server 2003</span></span>



| <span data-ttu-id="8e8e3-158">進入</span><span class="sxs-lookup"><span data-stu-id="8e8e3-158">Entry</span></span> | <span data-ttu-id="8e8e3-159">值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8e8e3-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8e8e3-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8e8e3-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e8e3-161">MAPI-Id</span></span>                | <span data-ttu-id="8e8e3-162">0x39FF</span><span class="sxs-lookup"><span data-stu-id="8e8e3-162">0x39FF</span></span>                          |
| <span data-ttu-id="8e8e3-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e8e3-163">System-Only</span></span>            | <span data-ttu-id="8e8e3-164">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-164">False</span></span>                           |
| <span data-ttu-id="8e8e3-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8e8e3-166">對</span><span class="sxs-lookup"><span data-stu-id="8e8e3-166">True</span></span>                            |
| <span data-ttu-id="8e8e3-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8e8e3-167">Is Indexed</span></span>             | <span data-ttu-id="8e8e3-168">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-168">False</span></span>                           |
| <span data-ttu-id="8e8e3-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8e8e3-169">In Global Catalog</span></span>      | <span data-ttu-id="8e8e3-170">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-170">False</span></span>                           |
| <span data-ttu-id="8e8e3-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8e8e3-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e8e3-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8e8e3-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8e8e3-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e8e3-173">Range-Lower</span></span>            | <span data-ttu-id="8e8e3-174">1</span><span class="sxs-lookup"><span data-stu-id="8e8e3-174">1</span></span>                               |
| <span data-ttu-id="8e8e3-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e8e3-175">Range-Upper</span></span>            | <span data-ttu-id="8e8e3-176">256</span><span class="sxs-lookup"><span data-stu-id="8e8e3-176">256</span></span>                             |
| <span data-ttu-id="8e8e3-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-177">Search-Flags</span></span>           | <span data-ttu-id="8e8e3-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e8e3-178">0x00000000</span></span>                      |
| <span data-ttu-id="8e8e3-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-179">System-Flags</span></span>           | <span data-ttu-id="8e8e3-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e8e3-180">0x00000010</span></span>                      |
| <span data-ttu-id="8e8e3-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8e8e3-181">Classes used in</span></span>        | [<span data-ttu-id="8e8e3-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8e8e3-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8e8e3-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8e8e3-184">進入</span><span class="sxs-lookup"><span data-stu-id="8e8e3-184">Entry</span></span> | <span data-ttu-id="8e8e3-185">值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8e8e3-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8e8e3-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8e8e3-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e8e3-187">MAPI-Id</span></span>                | <span data-ttu-id="8e8e3-188">0x39FF</span><span class="sxs-lookup"><span data-stu-id="8e8e3-188">0x39FF</span></span>                          |
| <span data-ttu-id="8e8e3-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e8e3-189">System-Only</span></span>            | <span data-ttu-id="8e8e3-190">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-190">False</span></span>                           |
| <span data-ttu-id="8e8e3-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-191">Is-Single-Valued</span></span>       | <span data-ttu-id="8e8e3-192">對</span><span class="sxs-lookup"><span data-stu-id="8e8e3-192">True</span></span>                            |
| <span data-ttu-id="8e8e3-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8e8e3-193">Is Indexed</span></span>             | <span data-ttu-id="8e8e3-194">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-194">False</span></span>                           |
| <span data-ttu-id="8e8e3-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8e8e3-195">In Global Catalog</span></span>      | <span data-ttu-id="8e8e3-196">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-196">False</span></span>                           |
| <span data-ttu-id="8e8e3-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8e8e3-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e8e3-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8e8e3-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8e8e3-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e8e3-199">Range-Lower</span></span>            | <span data-ttu-id="8e8e3-200">1</span><span class="sxs-lookup"><span data-stu-id="8e8e3-200">1</span></span>                               |
| <span data-ttu-id="8e8e3-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e8e3-201">Range-Upper</span></span>            | <span data-ttu-id="8e8e3-202">256</span><span class="sxs-lookup"><span data-stu-id="8e8e3-202">256</span></span>                             |
| <span data-ttu-id="8e8e3-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-203">Search-Flags</span></span>           | <span data-ttu-id="8e8e3-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e8e3-204">0x00000000</span></span>                      |
| <span data-ttu-id="8e8e3-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-205">System-Flags</span></span>           | <span data-ttu-id="8e8e3-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e8e3-206">0x00000010</span></span>                      |
| <span data-ttu-id="8e8e3-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8e8e3-207">Classes used in</span></span>        | [<span data-ttu-id="8e8e3-208">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8e8e3-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e8e3-209">Windows Server 2008</span></span>



| <span data-ttu-id="8e8e3-210">進入</span><span class="sxs-lookup"><span data-stu-id="8e8e3-210">Entry</span></span> | <span data-ttu-id="8e8e3-211">值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8e8e3-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8e8e3-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8e8e3-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e8e3-213">MAPI-Id</span></span>                | <span data-ttu-id="8e8e3-214">0x39FF</span><span class="sxs-lookup"><span data-stu-id="8e8e3-214">0x39FF</span></span>                          |
| <span data-ttu-id="8e8e3-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e8e3-215">System-Only</span></span>            | <span data-ttu-id="8e8e3-216">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-216">False</span></span>                           |
| <span data-ttu-id="8e8e3-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-217">Is-Single-Valued</span></span>       | <span data-ttu-id="8e8e3-218">對</span><span class="sxs-lookup"><span data-stu-id="8e8e3-218">True</span></span>                            |
| <span data-ttu-id="8e8e3-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8e8e3-219">Is Indexed</span></span>             | <span data-ttu-id="8e8e3-220">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-220">False</span></span>                           |
| <span data-ttu-id="8e8e3-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8e8e3-221">In Global Catalog</span></span>      | <span data-ttu-id="8e8e3-222">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-222">False</span></span>                           |
| <span data-ttu-id="8e8e3-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8e8e3-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e8e3-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8e8e3-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8e8e3-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e8e3-225">Range-Lower</span></span>            | <span data-ttu-id="8e8e3-226">1</span><span class="sxs-lookup"><span data-stu-id="8e8e3-226">1</span></span>                               |
| <span data-ttu-id="8e8e3-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e8e3-227">Range-Upper</span></span>            | <span data-ttu-id="8e8e3-228">256</span><span class="sxs-lookup"><span data-stu-id="8e8e3-228">256</span></span>                             |
| <span data-ttu-id="8e8e3-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-229">Search-Flags</span></span>           | <span data-ttu-id="8e8e3-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e8e3-230">0x00000000</span></span>                      |
| <span data-ttu-id="8e8e3-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-231">System-Flags</span></span>           | <span data-ttu-id="8e8e3-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e8e3-232">0x00000010</span></span>                      |
| <span data-ttu-id="8e8e3-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8e8e3-233">Classes used in</span></span>        | [<span data-ttu-id="8e8e3-234">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e8e3-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e8e3-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e8e3-236">進入</span><span class="sxs-lookup"><span data-stu-id="8e8e3-236">Entry</span></span> | <span data-ttu-id="8e8e3-237">值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8e8e3-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8e8e3-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8e8e3-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e8e3-239">MAPI-Id</span></span>                | <span data-ttu-id="8e8e3-240">0x39FF</span><span class="sxs-lookup"><span data-stu-id="8e8e3-240">0x39FF</span></span>                          |
| <span data-ttu-id="8e8e3-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e8e3-241">System-Only</span></span>            | <span data-ttu-id="8e8e3-242">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-242">False</span></span>                           |
| <span data-ttu-id="8e8e3-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-243">Is-Single-Valued</span></span>       | <span data-ttu-id="8e8e3-244">對</span><span class="sxs-lookup"><span data-stu-id="8e8e3-244">True</span></span>                            |
| <span data-ttu-id="8e8e3-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8e8e3-245">Is Indexed</span></span>             | <span data-ttu-id="8e8e3-246">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-246">False</span></span>                           |
| <span data-ttu-id="8e8e3-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8e8e3-247">In Global Catalog</span></span>      | <span data-ttu-id="8e8e3-248">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-248">False</span></span>                           |
| <span data-ttu-id="8e8e3-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8e8e3-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e8e3-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8e8e3-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8e8e3-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e8e3-251">Range-Lower</span></span>            | <span data-ttu-id="8e8e3-252">1</span><span class="sxs-lookup"><span data-stu-id="8e8e3-252">1</span></span>                               |
| <span data-ttu-id="8e8e3-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e8e3-253">Range-Upper</span></span>            | <span data-ttu-id="8e8e3-254">256</span><span class="sxs-lookup"><span data-stu-id="8e8e3-254">256</span></span>                             |
| <span data-ttu-id="8e8e3-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-255">Search-Flags</span></span>           | <span data-ttu-id="8e8e3-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e8e3-256">0x00000000</span></span>                      |
| <span data-ttu-id="8e8e3-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-257">System-Flags</span></span>           | <span data-ttu-id="8e8e3-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e8e3-258">0x00000010</span></span>                      |
| <span data-ttu-id="8e8e3-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8e8e3-259">Classes used in</span></span>        | [<span data-ttu-id="8e8e3-260">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8e8e3-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e8e3-261">Windows Server 2012</span></span>



| <span data-ttu-id="8e8e3-262">進入</span><span class="sxs-lookup"><span data-stu-id="8e8e3-262">Entry</span></span> | <span data-ttu-id="8e8e3-263">值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8e8e3-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8e8e3-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8e8e3-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e8e3-265">MAPI-Id</span></span>                | <span data-ttu-id="8e8e3-266">0x39FF</span><span class="sxs-lookup"><span data-stu-id="8e8e3-266">0x39FF</span></span>                          |
| <span data-ttu-id="8e8e3-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e8e3-267">System-Only</span></span>            | <span data-ttu-id="8e8e3-268">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-268">False</span></span>                           |
| <span data-ttu-id="8e8e3-269">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8e8e3-269">Is-Single-Valued</span></span>       | <span data-ttu-id="8e8e3-270">對</span><span class="sxs-lookup"><span data-stu-id="8e8e3-270">True</span></span>                            |
| <span data-ttu-id="8e8e3-271">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8e8e3-271">Is Indexed</span></span>             | <span data-ttu-id="8e8e3-272">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-272">False</span></span>                           |
| <span data-ttu-id="8e8e3-273">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8e8e3-273">In Global Catalog</span></span>      | <span data-ttu-id="8e8e3-274">否</span><span class="sxs-lookup"><span data-stu-id="8e8e3-274">False</span></span>                           |
| <span data-ttu-id="8e8e3-275">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8e8e3-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e8e3-276">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8e8e3-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8e8e3-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e8e3-277">Range-Lower</span></span>            | <span data-ttu-id="8e8e3-278">1</span><span class="sxs-lookup"><span data-stu-id="8e8e3-278">1</span></span>                               |
| <span data-ttu-id="8e8e3-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e8e3-279">Range-Upper</span></span>            | <span data-ttu-id="8e8e3-280">256</span><span class="sxs-lookup"><span data-stu-id="8e8e3-280">256</span></span>                             |
| <span data-ttu-id="8e8e3-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-281">Search-Flags</span></span>           | <span data-ttu-id="8e8e3-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e8e3-282">0x00000000</span></span>                      |
| <span data-ttu-id="8e8e3-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e8e3-283">System-Flags</span></span>           | <span data-ttu-id="8e8e3-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e8e3-284">0x00000010</span></span>                      |
| <span data-ttu-id="8e8e3-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8e8e3-285">Classes used in</span></span>        | [<span data-ttu-id="8e8e3-286">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8e8e3-286">**Top**</span></span>](c-top.md)<br/> |



 

 






---
title: Vol-資料表-GUID 屬性
description: 連結追蹤磁片區資料表專案的唯一識別碼。
ms.assetid: 3a63406a-e751-4234-a601-8f5a57f0a3b7
ms.tgt_platform: multiple
keywords:
- Vol-資料表-GUID 屬性 AD 架構
- volTableGUID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Vol-Table-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a23bcd088304b4a683ce3ff0f203d3c82fecf8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467229"
---
# <a name="vol-table-guid-attribute"></a><span data-ttu-id="f4e4c-105">Vol-資料表-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="f4e4c-105">Vol-Table-GUID attribute</span></span>

<span data-ttu-id="f4e4c-106">連結追蹤磁片區資料表專案的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4e4c-106">The unique identifier for a Link-Track-Volume table entry.</span></span>



| <span data-ttu-id="f4e4c-107">進入</span><span class="sxs-lookup"><span data-stu-id="f4e4c-107">Entry</span></span> | <span data-ttu-id="f4e4c-108">值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f4e4c-109">CN</span><span class="sxs-lookup"><span data-stu-id="f4e4c-109">CN</span></span>                | <span data-ttu-id="f4e4c-110">Vol-資料表-GUID</span><span class="sxs-lookup"><span data-stu-id="f4e4c-110">Vol-Table-GUID</span></span>                                        |
| <span data-ttu-id="f4e4c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f4e4c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f4e4c-112">volTableGUID</span><span class="sxs-lookup"><span data-stu-id="f4e4c-112">volTableGUID</span></span>                                          |
| <span data-ttu-id="f4e4c-113">大小</span><span class="sxs-lookup"><span data-stu-id="f4e4c-113">Size</span></span>              | <span data-ttu-id="f4e4c-114">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="f4e4c-114">16 bytes</span></span>                                              |
| <span data-ttu-id="f4e4c-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f4e4c-115">Update Privilege</span></span>  | <span data-ttu-id="f4e4c-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="f4e4c-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="f4e4c-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f4e4c-117">Update Frequency</span></span>  | <span data-ttu-id="f4e4c-118">只要建立新的檔案連結。</span><span class="sxs-lookup"><span data-stu-id="f4e4c-118">Whenever a new link to a file is created.</span></span>             |
| <span data-ttu-id="f4e4c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f4e4c-119">Attribute-Id</span></span>      | <span data-ttu-id="f4e4c-120">1.2.840.113556.1.4.336</span><span class="sxs-lookup"><span data-stu-id="f4e4c-120">1.2.840.113556.1.4.336</span></span>                                |
| <span data-ttu-id="f4e4c-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f4e4c-121">System-Id-Guid</span></span>    | <span data-ttu-id="f4e4c-122">1f0075fd-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f4e4c-122">1f0075fd-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="f4e4c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4e4c-123">Syntax</span></span>            | [<span data-ttu-id="f4e4c-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f4e4c-125">實作</span><span class="sxs-lookup"><span data-stu-id="f4e4c-125">Implementations</span></span>

-   [<span data-ttu-id="f4e4c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f4e4c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f4e4c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f4e4c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f4e4c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f4e4c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f4e4c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4e4c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f4e4c-133">進入</span><span class="sxs-lookup"><span data-stu-id="f4e4c-133">Entry</span></span> | <span data-ttu-id="f4e4c-134">值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f4e4c-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e4c-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e4c-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e4c-137">System-Only</span></span>            | <span data-ttu-id="f4e4c-138">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-138">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e4c-140">對</span><span class="sxs-lookup"><span data-stu-id="f4e4c-140">True</span></span>                                                           |
| <span data-ttu-id="f4e4c-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e4c-141">Is Indexed</span></span>             | <span data-ttu-id="f4e4c-142">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-142">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e4c-143">In Global Catalog</span></span>      | <span data-ttu-id="f4e4c-144">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-144">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e4c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e4c-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e4c-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f4e4c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e4c-147">Range-Lower</span></span>            | <span data-ttu-id="f4e4c-148">0</span><span class="sxs-lookup"><span data-stu-id="f4e4c-148">0</span></span>                                                              |
| <span data-ttu-id="f4e4c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e4c-149">Range-Upper</span></span>            | <span data-ttu-id="f4e4c-150">16</span><span class="sxs-lookup"><span data-stu-id="f4e4c-150">16</span></span>                                                             |
| <span data-ttu-id="f4e4c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-151">Search-Flags</span></span>           | <span data-ttu-id="f4e4c-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4e4c-152">0x00000000</span></span>                                                     |
| <span data-ttu-id="f4e4c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-153">System-Flags</span></span>           | <span data-ttu-id="f4e4c-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e4c-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="f4e4c-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e4c-155">Classes used in</span></span>        | [<span data-ttu-id="f4e4c-156">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-156">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f4e4c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4e4c-157">Windows Server 2003</span></span>



| <span data-ttu-id="f4e4c-158">進入</span><span class="sxs-lookup"><span data-stu-id="f4e4c-158">Entry</span></span> | <span data-ttu-id="f4e4c-159">值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f4e4c-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e4c-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e4c-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e4c-162">System-Only</span></span>            | <span data-ttu-id="f4e4c-163">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-163">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e4c-165">對</span><span class="sxs-lookup"><span data-stu-id="f4e4c-165">True</span></span>                                                           |
| <span data-ttu-id="f4e4c-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e4c-166">Is Indexed</span></span>             | <span data-ttu-id="f4e4c-167">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-167">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e4c-168">In Global Catalog</span></span>      | <span data-ttu-id="f4e4c-169">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-169">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e4c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e4c-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e4c-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f4e4c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e4c-172">Range-Lower</span></span>            | <span data-ttu-id="f4e4c-173">0</span><span class="sxs-lookup"><span data-stu-id="f4e4c-173">0</span></span>                                                              |
| <span data-ttu-id="f4e4c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e4c-174">Range-Upper</span></span>            | <span data-ttu-id="f4e4c-175">16</span><span class="sxs-lookup"><span data-stu-id="f4e4c-175">16</span></span>                                                             |
| <span data-ttu-id="f4e4c-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-176">Search-Flags</span></span>           | <span data-ttu-id="f4e4c-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4e4c-177">0x00000000</span></span>                                                     |
| <span data-ttu-id="f4e4c-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-178">System-Flags</span></span>           | <span data-ttu-id="f4e4c-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e4c-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="f4e4c-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e4c-180">Classes used in</span></span>        | [<span data-ttu-id="f4e4c-181">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-181">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f4e4c-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f4e4c-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f4e4c-183">進入</span><span class="sxs-lookup"><span data-stu-id="f4e4c-183">Entry</span></span> | <span data-ttu-id="f4e4c-184">值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f4e4c-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e4c-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e4c-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e4c-187">System-Only</span></span>            | <span data-ttu-id="f4e4c-188">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-188">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-189">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e4c-190">對</span><span class="sxs-lookup"><span data-stu-id="f4e4c-190">True</span></span>                                                           |
| <span data-ttu-id="f4e4c-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e4c-191">Is Indexed</span></span>             | <span data-ttu-id="f4e4c-192">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-192">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e4c-193">In Global Catalog</span></span>      | <span data-ttu-id="f4e4c-194">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-194">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e4c-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e4c-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e4c-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f4e4c-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e4c-197">Range-Lower</span></span>            | <span data-ttu-id="f4e4c-198">0</span><span class="sxs-lookup"><span data-stu-id="f4e4c-198">0</span></span>                                                              |
| <span data-ttu-id="f4e4c-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e4c-199">Range-Upper</span></span>            | <span data-ttu-id="f4e4c-200">16</span><span class="sxs-lookup"><span data-stu-id="f4e4c-200">16</span></span>                                                             |
| <span data-ttu-id="f4e4c-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-201">Search-Flags</span></span>           | <span data-ttu-id="f4e4c-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4e4c-202">0x00000000</span></span>                                                     |
| <span data-ttu-id="f4e4c-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-203">System-Flags</span></span>           | <span data-ttu-id="f4e4c-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e4c-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="f4e4c-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e4c-205">Classes used in</span></span>        | [<span data-ttu-id="f4e4c-206">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-206">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f4e4c-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4e4c-207">Windows Server 2008</span></span>



| <span data-ttu-id="f4e4c-208">進入</span><span class="sxs-lookup"><span data-stu-id="f4e4c-208">Entry</span></span> | <span data-ttu-id="f4e4c-209">值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f4e4c-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e4c-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e4c-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e4c-212">System-Only</span></span>            | <span data-ttu-id="f4e4c-213">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-213">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-214">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e4c-215">對</span><span class="sxs-lookup"><span data-stu-id="f4e4c-215">True</span></span>                                                           |
| <span data-ttu-id="f4e4c-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e4c-216">Is Indexed</span></span>             | <span data-ttu-id="f4e4c-217">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-217">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e4c-218">In Global Catalog</span></span>      | <span data-ttu-id="f4e4c-219">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-219">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e4c-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e4c-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e4c-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f4e4c-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e4c-222">Range-Lower</span></span>            | <span data-ttu-id="f4e4c-223">0</span><span class="sxs-lookup"><span data-stu-id="f4e4c-223">0</span></span>                                                              |
| <span data-ttu-id="f4e4c-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e4c-224">Range-Upper</span></span>            | <span data-ttu-id="f4e4c-225">16</span><span class="sxs-lookup"><span data-stu-id="f4e4c-225">16</span></span>                                                             |
| <span data-ttu-id="f4e4c-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-226">Search-Flags</span></span>           | <span data-ttu-id="f4e4c-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4e4c-227">0x00000000</span></span>                                                     |
| <span data-ttu-id="f4e4c-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-228">System-Flags</span></span>           | <span data-ttu-id="f4e4c-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e4c-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="f4e4c-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e4c-230">Classes used in</span></span>        | [<span data-ttu-id="f4e4c-231">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-231">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f4e4c-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4e4c-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f4e4c-233">進入</span><span class="sxs-lookup"><span data-stu-id="f4e4c-233">Entry</span></span> | <span data-ttu-id="f4e4c-234">值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f4e4c-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e4c-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e4c-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e4c-237">System-Only</span></span>            | <span data-ttu-id="f4e4c-238">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-238">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-239">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e4c-240">對</span><span class="sxs-lookup"><span data-stu-id="f4e4c-240">True</span></span>                                                           |
| <span data-ttu-id="f4e4c-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e4c-241">Is Indexed</span></span>             | <span data-ttu-id="f4e4c-242">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-242">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e4c-243">In Global Catalog</span></span>      | <span data-ttu-id="f4e4c-244">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-244">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e4c-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e4c-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e4c-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f4e4c-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e4c-247">Range-Lower</span></span>            | <span data-ttu-id="f4e4c-248">0</span><span class="sxs-lookup"><span data-stu-id="f4e4c-248">0</span></span>                                                              |
| <span data-ttu-id="f4e4c-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e4c-249">Range-Upper</span></span>            | <span data-ttu-id="f4e4c-250">16</span><span class="sxs-lookup"><span data-stu-id="f4e4c-250">16</span></span>                                                             |
| <span data-ttu-id="f4e4c-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-251">Search-Flags</span></span>           | <span data-ttu-id="f4e4c-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4e4c-252">0x00000000</span></span>                                                     |
| <span data-ttu-id="f4e4c-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-253">System-Flags</span></span>           | <span data-ttu-id="f4e4c-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e4c-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="f4e4c-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e4c-255">Classes used in</span></span>        | [<span data-ttu-id="f4e4c-256">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-256">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f4e4c-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4e4c-257">Windows Server 2012</span></span>



| <span data-ttu-id="f4e4c-258">進入</span><span class="sxs-lookup"><span data-stu-id="f4e4c-258">Entry</span></span> | <span data-ttu-id="f4e4c-259">值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f4e4c-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e4c-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e4c-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="f4e4c-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e4c-262">System-Only</span></span>            | <span data-ttu-id="f4e4c-263">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-263">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e4c-264">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e4c-265">對</span><span class="sxs-lookup"><span data-stu-id="f4e4c-265">True</span></span>                                                           |
| <span data-ttu-id="f4e4c-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e4c-266">Is Indexed</span></span>             | <span data-ttu-id="f4e4c-267">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-267">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e4c-268">In Global Catalog</span></span>      | <span data-ttu-id="f4e4c-269">否</span><span class="sxs-lookup"><span data-stu-id="f4e4c-269">False</span></span>                                                          |
| <span data-ttu-id="f4e4c-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e4c-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e4c-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e4c-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="f4e4c-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e4c-272">Range-Lower</span></span>            | <span data-ttu-id="f4e4c-273">0</span><span class="sxs-lookup"><span data-stu-id="f4e4c-273">0</span></span>                                                              |
| <span data-ttu-id="f4e4c-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e4c-274">Range-Upper</span></span>            | <span data-ttu-id="f4e4c-275">16</span><span class="sxs-lookup"><span data-stu-id="f4e4c-275">16</span></span>                                                             |
| <span data-ttu-id="f4e4c-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-276">Search-Flags</span></span>           | <span data-ttu-id="f4e4c-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4e4c-277">0x00000000</span></span>                                                     |
| <span data-ttu-id="f4e4c-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e4c-278">System-Flags</span></span>           | <span data-ttu-id="f4e4c-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e4c-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="f4e4c-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e4c-280">Classes used in</span></span>        | [<span data-ttu-id="f4e4c-281">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="f4e4c-281">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 






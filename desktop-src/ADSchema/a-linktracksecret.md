---
title: 連結-追蹤-秘密屬性
description: 這個屬性會儲存秘密金鑰的連結，讓加密的檔案能夠轉譯為純文字。
ms.assetid: e476f4af-71a8-4bd9-a81d-f825bfbf267b
ms.tgt_platform: multiple
keywords:
- 連結-追蹤-秘密屬性 AD 架構
- linkTrackSecret 屬性 AD 架構
topic_type:
- apiref
api_name:
- Link-Track-Secret
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb172ec0985acc7c93c62796881c369c7ad0b82
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970040"
---
# <a name="link-track-secret-attribute"></a><span data-ttu-id="9cd09-105">連結-追蹤-秘密屬性</span><span class="sxs-lookup"><span data-stu-id="9cd09-105">Link-Track-Secret attribute</span></span>

<span data-ttu-id="9cd09-106">這個屬性會儲存秘密金鑰的連結，讓加密的檔案能夠轉譯為純文字。</span><span class="sxs-lookup"><span data-stu-id="9cd09-106">This attribute stores a link to a secret key that allows an encrypted file to be translated to plaintext.</span></span>



| <span data-ttu-id="9cd09-107">進入</span><span class="sxs-lookup"><span data-stu-id="9cd09-107">Entry</span></span> | <span data-ttu-id="9cd09-108">值</span><span class="sxs-lookup"><span data-stu-id="9cd09-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="9cd09-109">CN</span><span class="sxs-lookup"><span data-stu-id="9cd09-109">CN</span></span>                | <span data-ttu-id="9cd09-110">連結-追蹤-秘密</span><span class="sxs-lookup"><span data-stu-id="9cd09-110">Link-Track-Secret</span></span>                                     |
| <span data-ttu-id="9cd09-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9cd09-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9cd09-112">linkTrackSecret</span><span class="sxs-lookup"><span data-stu-id="9cd09-112">linkTrackSecret</span></span>                                       |
| <span data-ttu-id="9cd09-113">大小</span><span class="sxs-lookup"><span data-stu-id="9cd09-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="9cd09-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9cd09-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="9cd09-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9cd09-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="9cd09-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9cd09-116">Attribute-Id</span></span>      | <span data-ttu-id="9cd09-117">1.2.840.113556.1.4.269</span><span class="sxs-lookup"><span data-stu-id="9cd09-117">1.2.840.113556.1.4.269</span></span>                                |
| <span data-ttu-id="9cd09-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9cd09-118">System-Id-Guid</span></span>    | <span data-ttu-id="9cd09-119">2ae80fe2-47b4-11d0-a1a4-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="9cd09-119">2ae80fe2-47b4-11d0-a1a4-00c04fd930c9</span></span>                  |
| <span data-ttu-id="9cd09-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cd09-120">Syntax</span></span>            | [<span data-ttu-id="9cd09-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="9cd09-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="9cd09-122">實作</span><span class="sxs-lookup"><span data-stu-id="9cd09-122">Implementations</span></span>

-   [<span data-ttu-id="9cd09-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9cd09-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9cd09-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9cd09-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9cd09-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9cd09-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9cd09-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9cd09-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9cd09-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9cd09-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9cd09-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9cd09-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9cd09-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9cd09-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9cd09-130">進入</span><span class="sxs-lookup"><span data-stu-id="9cd09-130">Entry</span></span> | <span data-ttu-id="9cd09-131">值</span><span class="sxs-lookup"><span data-stu-id="9cd09-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9cd09-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9cd09-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cd09-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cd09-134">System-Only</span></span>            | <span data-ttu-id="9cd09-135">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-135">False</span></span>                                                          |
| <span data-ttu-id="9cd09-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9cd09-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9cd09-137">對</span><span class="sxs-lookup"><span data-stu-id="9cd09-137">True</span></span>                                                           |
| <span data-ttu-id="9cd09-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9cd09-138">Is Indexed</span></span>             | <span data-ttu-id="9cd09-139">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-139">False</span></span>                                                          |
| <span data-ttu-id="9cd09-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9cd09-140">In Global Catalog</span></span>      | <span data-ttu-id="9cd09-141">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-141">False</span></span>                                                          |
| <span data-ttu-id="9cd09-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9cd09-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cd09-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9cd09-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9cd09-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cd09-144">Range-Lower</span></span>            | <span data-ttu-id="9cd09-145">0</span><span class="sxs-lookup"><span data-stu-id="9cd09-145">0</span></span>                                                              |
| <span data-ttu-id="9cd09-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cd09-146">Range-Upper</span></span>            | <span data-ttu-id="9cd09-147">16</span><span class="sxs-lookup"><span data-stu-id="9cd09-147">16</span></span>                                                             |
| <span data-ttu-id="9cd09-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-148">Search-Flags</span></span>           | <span data-ttu-id="9cd09-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9cd09-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="9cd09-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-150">System-Flags</span></span>           | <span data-ttu-id="9cd09-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cd09-151">0x00000010</span></span>                                                     |
| <span data-ttu-id="9cd09-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9cd09-152">Classes used in</span></span>        | [<span data-ttu-id="9cd09-153">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="9cd09-153">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9cd09-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9cd09-154">Windows Server 2003</span></span>



| <span data-ttu-id="9cd09-155">進入</span><span class="sxs-lookup"><span data-stu-id="9cd09-155">Entry</span></span> | <span data-ttu-id="9cd09-156">值</span><span class="sxs-lookup"><span data-stu-id="9cd09-156">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9cd09-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9cd09-157">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cd09-158">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cd09-159">System-Only</span></span>            | <span data-ttu-id="9cd09-160">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-160">False</span></span>                                                          |
| <span data-ttu-id="9cd09-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9cd09-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9cd09-162">對</span><span class="sxs-lookup"><span data-stu-id="9cd09-162">True</span></span>                                                           |
| <span data-ttu-id="9cd09-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9cd09-163">Is Indexed</span></span>             | <span data-ttu-id="9cd09-164">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-164">False</span></span>                                                          |
| <span data-ttu-id="9cd09-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9cd09-165">In Global Catalog</span></span>      | <span data-ttu-id="9cd09-166">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-166">False</span></span>                                                          |
| <span data-ttu-id="9cd09-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9cd09-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cd09-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9cd09-168">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9cd09-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cd09-169">Range-Lower</span></span>            | <span data-ttu-id="9cd09-170">0</span><span class="sxs-lookup"><span data-stu-id="9cd09-170">0</span></span>                                                              |
| <span data-ttu-id="9cd09-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cd09-171">Range-Upper</span></span>            | <span data-ttu-id="9cd09-172">16</span><span class="sxs-lookup"><span data-stu-id="9cd09-172">16</span></span>                                                             |
| <span data-ttu-id="9cd09-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-173">Search-Flags</span></span>           | <span data-ttu-id="9cd09-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9cd09-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="9cd09-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-175">System-Flags</span></span>           | <span data-ttu-id="9cd09-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cd09-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="9cd09-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9cd09-177">Classes used in</span></span>        | [<span data-ttu-id="9cd09-178">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="9cd09-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9cd09-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9cd09-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9cd09-180">進入</span><span class="sxs-lookup"><span data-stu-id="9cd09-180">Entry</span></span> | <span data-ttu-id="9cd09-181">值</span><span class="sxs-lookup"><span data-stu-id="9cd09-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9cd09-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9cd09-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cd09-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cd09-184">System-Only</span></span>            | <span data-ttu-id="9cd09-185">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-185">False</span></span>                                                          |
| <span data-ttu-id="9cd09-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9cd09-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9cd09-187">對</span><span class="sxs-lookup"><span data-stu-id="9cd09-187">True</span></span>                                                           |
| <span data-ttu-id="9cd09-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9cd09-188">Is Indexed</span></span>             | <span data-ttu-id="9cd09-189">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-189">False</span></span>                                                          |
| <span data-ttu-id="9cd09-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9cd09-190">In Global Catalog</span></span>      | <span data-ttu-id="9cd09-191">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-191">False</span></span>                                                          |
| <span data-ttu-id="9cd09-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9cd09-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cd09-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9cd09-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9cd09-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cd09-194">Range-Lower</span></span>            | <span data-ttu-id="9cd09-195">0</span><span class="sxs-lookup"><span data-stu-id="9cd09-195">0</span></span>                                                              |
| <span data-ttu-id="9cd09-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cd09-196">Range-Upper</span></span>            | <span data-ttu-id="9cd09-197">16</span><span class="sxs-lookup"><span data-stu-id="9cd09-197">16</span></span>                                                             |
| <span data-ttu-id="9cd09-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-198">Search-Flags</span></span>           | <span data-ttu-id="9cd09-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9cd09-199">0x00000000</span></span>                                                     |
| <span data-ttu-id="9cd09-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-200">System-Flags</span></span>           | <span data-ttu-id="9cd09-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cd09-201">0x00000010</span></span>                                                     |
| <span data-ttu-id="9cd09-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9cd09-202">Classes used in</span></span>        | [<span data-ttu-id="9cd09-203">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="9cd09-203">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9cd09-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cd09-204">Windows Server 2008</span></span>



| <span data-ttu-id="9cd09-205">進入</span><span class="sxs-lookup"><span data-stu-id="9cd09-205">Entry</span></span> | <span data-ttu-id="9cd09-206">值</span><span class="sxs-lookup"><span data-stu-id="9cd09-206">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9cd09-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9cd09-207">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cd09-208">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cd09-209">System-Only</span></span>            | <span data-ttu-id="9cd09-210">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-210">False</span></span>                                                          |
| <span data-ttu-id="9cd09-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9cd09-211">Is-Single-Valued</span></span>       | <span data-ttu-id="9cd09-212">對</span><span class="sxs-lookup"><span data-stu-id="9cd09-212">True</span></span>                                                           |
| <span data-ttu-id="9cd09-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9cd09-213">Is Indexed</span></span>             | <span data-ttu-id="9cd09-214">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-214">False</span></span>                                                          |
| <span data-ttu-id="9cd09-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9cd09-215">In Global Catalog</span></span>      | <span data-ttu-id="9cd09-216">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-216">False</span></span>                                                          |
| <span data-ttu-id="9cd09-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9cd09-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cd09-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9cd09-218">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9cd09-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cd09-219">Range-Lower</span></span>            | <span data-ttu-id="9cd09-220">0</span><span class="sxs-lookup"><span data-stu-id="9cd09-220">0</span></span>                                                              |
| <span data-ttu-id="9cd09-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cd09-221">Range-Upper</span></span>            | <span data-ttu-id="9cd09-222">16</span><span class="sxs-lookup"><span data-stu-id="9cd09-222">16</span></span>                                                             |
| <span data-ttu-id="9cd09-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-223">Search-Flags</span></span>           | <span data-ttu-id="9cd09-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9cd09-224">0x00000000</span></span>                                                     |
| <span data-ttu-id="9cd09-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-225">System-Flags</span></span>           | <span data-ttu-id="9cd09-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cd09-226">0x00000010</span></span>                                                     |
| <span data-ttu-id="9cd09-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9cd09-227">Classes used in</span></span>        | [<span data-ttu-id="9cd09-228">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="9cd09-228">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9cd09-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9cd09-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9cd09-230">進入</span><span class="sxs-lookup"><span data-stu-id="9cd09-230">Entry</span></span> | <span data-ttu-id="9cd09-231">值</span><span class="sxs-lookup"><span data-stu-id="9cd09-231">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9cd09-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9cd09-232">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cd09-233">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cd09-234">System-Only</span></span>            | <span data-ttu-id="9cd09-235">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-235">False</span></span>                                                          |
| <span data-ttu-id="9cd09-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9cd09-236">Is-Single-Valued</span></span>       | <span data-ttu-id="9cd09-237">對</span><span class="sxs-lookup"><span data-stu-id="9cd09-237">True</span></span>                                                           |
| <span data-ttu-id="9cd09-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9cd09-238">Is Indexed</span></span>             | <span data-ttu-id="9cd09-239">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-239">False</span></span>                                                          |
| <span data-ttu-id="9cd09-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9cd09-240">In Global Catalog</span></span>      | <span data-ttu-id="9cd09-241">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-241">False</span></span>                                                          |
| <span data-ttu-id="9cd09-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9cd09-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cd09-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9cd09-243">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9cd09-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cd09-244">Range-Lower</span></span>            | <span data-ttu-id="9cd09-245">0</span><span class="sxs-lookup"><span data-stu-id="9cd09-245">0</span></span>                                                              |
| <span data-ttu-id="9cd09-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cd09-246">Range-Upper</span></span>            | <span data-ttu-id="9cd09-247">16</span><span class="sxs-lookup"><span data-stu-id="9cd09-247">16</span></span>                                                             |
| <span data-ttu-id="9cd09-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-248">Search-Flags</span></span>           | <span data-ttu-id="9cd09-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9cd09-249">0x00000000</span></span>                                                     |
| <span data-ttu-id="9cd09-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-250">System-Flags</span></span>           | <span data-ttu-id="9cd09-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cd09-251">0x00000010</span></span>                                                     |
| <span data-ttu-id="9cd09-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9cd09-252">Classes used in</span></span>        | [<span data-ttu-id="9cd09-253">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="9cd09-253">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9cd09-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9cd09-254">Windows Server 2012</span></span>



| <span data-ttu-id="9cd09-255">進入</span><span class="sxs-lookup"><span data-stu-id="9cd09-255">Entry</span></span> | <span data-ttu-id="9cd09-256">值</span><span class="sxs-lookup"><span data-stu-id="9cd09-256">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9cd09-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9cd09-257">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cd09-258">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9cd09-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cd09-259">System-Only</span></span>            | <span data-ttu-id="9cd09-260">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-260">False</span></span>                                                          |
| <span data-ttu-id="9cd09-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9cd09-261">Is-Single-Valued</span></span>       | <span data-ttu-id="9cd09-262">對</span><span class="sxs-lookup"><span data-stu-id="9cd09-262">True</span></span>                                                           |
| <span data-ttu-id="9cd09-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9cd09-263">Is Indexed</span></span>             | <span data-ttu-id="9cd09-264">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-264">False</span></span>                                                          |
| <span data-ttu-id="9cd09-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9cd09-265">In Global Catalog</span></span>      | <span data-ttu-id="9cd09-266">否</span><span class="sxs-lookup"><span data-stu-id="9cd09-266">False</span></span>                                                          |
| <span data-ttu-id="9cd09-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9cd09-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cd09-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9cd09-268">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9cd09-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cd09-269">Range-Lower</span></span>            | <span data-ttu-id="9cd09-270">0</span><span class="sxs-lookup"><span data-stu-id="9cd09-270">0</span></span>                                                              |
| <span data-ttu-id="9cd09-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cd09-271">Range-Upper</span></span>            | <span data-ttu-id="9cd09-272">16</span><span class="sxs-lookup"><span data-stu-id="9cd09-272">16</span></span>                                                             |
| <span data-ttu-id="9cd09-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-273">Search-Flags</span></span>           | <span data-ttu-id="9cd09-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9cd09-274">0x00000000</span></span>                                                     |
| <span data-ttu-id="9cd09-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cd09-275">System-Flags</span></span>           | <span data-ttu-id="9cd09-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cd09-276">0x00000010</span></span>                                                     |
| <span data-ttu-id="9cd09-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9cd09-277">Classes used in</span></span>        | [<span data-ttu-id="9cd09-278">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="9cd09-278">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 






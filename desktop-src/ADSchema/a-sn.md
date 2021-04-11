---
title: 姓氏屬性
description: 此屬性包含使用者的系列或姓氏。
ms.assetid: d9d53c9f-4efa-47c4-aec4-518fb8a868b3
ms.tgt_platform: multiple
keywords:
- 姓氏屬性 AD 架構
- sn 屬性 AD 架構
topic_type:
- apiref
api_name:
- Surname
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453352574a7aec10c56492060ac2de6ceeca030f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935348"
---
# <a name="surname-attribute"></a><span data-ttu-id="8acb5-105">姓氏屬性</span><span class="sxs-lookup"><span data-stu-id="8acb5-105">Surname attribute</span></span>

<span data-ttu-id="8acb5-106">此屬性包含使用者的系列或姓氏。</span><span class="sxs-lookup"><span data-stu-id="8acb5-106">This attribute contains the family or last name for a user.</span></span>



| <span data-ttu-id="8acb5-107">進入</span><span class="sxs-lookup"><span data-stu-id="8acb5-107">Entry</span></span> | <span data-ttu-id="8acb5-108">值</span><span class="sxs-lookup"><span data-stu-id="8acb5-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8acb5-109">CN</span><span class="sxs-lookup"><span data-stu-id="8acb5-109">CN</span></span>                | <span data-ttu-id="8acb5-110">Surname</span><span class="sxs-lookup"><span data-stu-id="8acb5-110">Surname</span></span>                                                                          |
| <span data-ttu-id="8acb5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8acb5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8acb5-112">sn</span><span class="sxs-lookup"><span data-stu-id="8acb5-112">sn</span></span>                                                                               |
| <span data-ttu-id="8acb5-113">大小</span><span class="sxs-lookup"><span data-stu-id="8acb5-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="8acb5-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8acb5-114">Update Privilege</span></span>  | <span data-ttu-id="8acb5-115">任何人都可以根據所建立物件的安全性來更新這個物件。</span><span class="sxs-lookup"><span data-stu-id="8acb5-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="8acb5-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8acb5-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="8acb5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8acb5-117">Attribute-Id</span></span>      | <span data-ttu-id="8acb5-118">2.5.4.4</span><span class="sxs-lookup"><span data-stu-id="8acb5-118">2.5.4.4</span></span>                                                                          |
| <span data-ttu-id="8acb5-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8acb5-119">System-Id-Guid</span></span>    | <span data-ttu-id="8acb5-120">bf967a41-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8acb5-120">bf967a41-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="8acb5-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8acb5-121">Syntax</span></span>            | [<span data-ttu-id="8acb5-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8acb5-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="8acb5-123">實作</span><span class="sxs-lookup"><span data-stu-id="8acb5-123">Implementations</span></span>

-   [<span data-ttu-id="8acb5-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8acb5-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8acb5-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8acb5-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8acb5-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8acb5-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8acb5-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8acb5-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8acb5-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8acb5-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8acb5-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8acb5-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8acb5-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8acb5-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8acb5-131">進入</span><span class="sxs-lookup"><span data-stu-id="8acb5-131">Entry</span></span> | <span data-ttu-id="8acb5-132">值</span><span class="sxs-lookup"><span data-stu-id="8acb5-132">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="8acb5-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8acb5-133">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="8acb5-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acb5-134">MAPI-Id</span></span>                | <span data-ttu-id="8acb5-135">0x3A11</span><span class="sxs-lookup"><span data-stu-id="8acb5-135">0x3A11</span></span>                                |
| <span data-ttu-id="8acb5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acb5-136">System-Only</span></span>            | <span data-ttu-id="8acb5-137">否</span><span class="sxs-lookup"><span data-stu-id="8acb5-137">False</span></span>                                 |
| <span data-ttu-id="8acb5-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8acb5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8acb5-139">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-139">True</span></span>                                  |
| <span data-ttu-id="8acb5-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8acb5-140">Is Indexed</span></span>             | <span data-ttu-id="8acb5-141">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-141">True</span></span>                                  |
| <span data-ttu-id="8acb5-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8acb5-142">In Global Catalog</span></span>      | <span data-ttu-id="8acb5-143">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-143">True</span></span>                                  |
| <span data-ttu-id="8acb5-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8acb5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acb5-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8acb5-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="8acb5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acb5-146">Range-Lower</span></span>            | <span data-ttu-id="8acb5-147">1</span><span class="sxs-lookup"><span data-stu-id="8acb5-147">1</span></span>                                     |
| <span data-ttu-id="8acb5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acb5-148">Range-Upper</span></span>            | <span data-ttu-id="8acb5-149">64</span><span class="sxs-lookup"><span data-stu-id="8acb5-149">64</span></span>                                    |
| <span data-ttu-id="8acb5-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-150">Search-Flags</span></span>           | <span data-ttu-id="8acb5-151">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8acb5-151">0x00000005</span></span>                            |
| <span data-ttu-id="8acb5-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-152">System-Flags</span></span>           | <span data-ttu-id="8acb5-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acb5-153">0x00000010</span></span>                            |
| <span data-ttu-id="8acb5-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8acb5-154">Classes used in</span></span>        | [<span data-ttu-id="8acb5-155">**個人**</span><span class="sxs-lookup"><span data-stu-id="8acb5-155">**Person**</span></span>](c-person.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8acb5-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8acb5-156">Windows Server 2003</span></span>



| <span data-ttu-id="8acb5-157">進入</span><span class="sxs-lookup"><span data-stu-id="8acb5-157">Entry</span></span> | <span data-ttu-id="8acb5-158">值</span><span class="sxs-lookup"><span data-stu-id="8acb5-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acb5-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8acb5-159">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acb5-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acb5-160">MAPI-Id</span></span>                | <span data-ttu-id="8acb5-161">0x3A11</span><span class="sxs-lookup"><span data-stu-id="8acb5-161">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="8acb5-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acb5-162">System-Only</span></span>            | <span data-ttu-id="8acb5-163">否</span><span class="sxs-lookup"><span data-stu-id="8acb5-163">False</span></span>                                                                                         |
| <span data-ttu-id="8acb5-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8acb5-164">Is-Single-Valued</span></span>       | <span data-ttu-id="8acb5-165">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-165">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8acb5-166">Is Indexed</span></span>             | <span data-ttu-id="8acb5-167">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-167">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8acb5-168">In Global Catalog</span></span>      | <span data-ttu-id="8acb5-169">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-169">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8acb5-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acb5-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8acb5-171">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acb5-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acb5-172">Range-Lower</span></span>            | <span data-ttu-id="8acb5-173">1</span><span class="sxs-lookup"><span data-stu-id="8acb5-173">1</span></span>                                                                                             |
| <span data-ttu-id="8acb5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acb5-174">Range-Upper</span></span>            | <span data-ttu-id="8acb5-175">64</span><span class="sxs-lookup"><span data-stu-id="8acb5-175">64</span></span>                                                                                            |
| <span data-ttu-id="8acb5-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-176">Search-Flags</span></span>           | <span data-ttu-id="8acb5-177">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8acb5-177">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="8acb5-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-178">System-Flags</span></span>           | <span data-ttu-id="8acb5-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acb5-179">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acb5-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8acb5-180">Classes used in</span></span>        | [<span data-ttu-id="8acb5-181">**個人**</span><span class="sxs-lookup"><span data-stu-id="8acb5-181">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="8acb5-182">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="8acb5-182">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8acb5-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8acb5-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8acb5-184">進入</span><span class="sxs-lookup"><span data-stu-id="8acb5-184">Entry</span></span> | <span data-ttu-id="8acb5-185">值</span><span class="sxs-lookup"><span data-stu-id="8acb5-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acb5-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8acb5-186">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acb5-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acb5-187">MAPI-Id</span></span>                | <span data-ttu-id="8acb5-188">0x3A11</span><span class="sxs-lookup"><span data-stu-id="8acb5-188">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="8acb5-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acb5-189">System-Only</span></span>            | <span data-ttu-id="8acb5-190">否</span><span class="sxs-lookup"><span data-stu-id="8acb5-190">False</span></span>                                                                                         |
| <span data-ttu-id="8acb5-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8acb5-191">Is-Single-Valued</span></span>       | <span data-ttu-id="8acb5-192">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-192">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8acb5-193">Is Indexed</span></span>             | <span data-ttu-id="8acb5-194">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-194">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8acb5-195">In Global Catalog</span></span>      | <span data-ttu-id="8acb5-196">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-196">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8acb5-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acb5-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8acb5-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acb5-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acb5-199">Range-Lower</span></span>            | <span data-ttu-id="8acb5-200">1</span><span class="sxs-lookup"><span data-stu-id="8acb5-200">1</span></span>                                                                                             |
| <span data-ttu-id="8acb5-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acb5-201">Range-Upper</span></span>            | <span data-ttu-id="8acb5-202">64</span><span class="sxs-lookup"><span data-stu-id="8acb5-202">64</span></span>                                                                                            |
| <span data-ttu-id="8acb5-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-203">Search-Flags</span></span>           | <span data-ttu-id="8acb5-204">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8acb5-204">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="8acb5-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-205">System-Flags</span></span>           | <span data-ttu-id="8acb5-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acb5-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acb5-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8acb5-207">Classes used in</span></span>        | [<span data-ttu-id="8acb5-208">**個人**</span><span class="sxs-lookup"><span data-stu-id="8acb5-208">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="8acb5-209">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="8acb5-209">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8acb5-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8acb5-210">Windows Server 2008</span></span>



| <span data-ttu-id="8acb5-211">進入</span><span class="sxs-lookup"><span data-stu-id="8acb5-211">Entry</span></span> | <span data-ttu-id="8acb5-212">值</span><span class="sxs-lookup"><span data-stu-id="8acb5-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acb5-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8acb5-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acb5-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acb5-214">MAPI-Id</span></span>                | <span data-ttu-id="8acb5-215">0x3A11</span><span class="sxs-lookup"><span data-stu-id="8acb5-215">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="8acb5-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acb5-216">System-Only</span></span>            | <span data-ttu-id="8acb5-217">否</span><span class="sxs-lookup"><span data-stu-id="8acb5-217">False</span></span>                                                                                         |
| <span data-ttu-id="8acb5-218">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8acb5-218">Is-Single-Valued</span></span>       | <span data-ttu-id="8acb5-219">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-219">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-220">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8acb5-220">Is Indexed</span></span>             | <span data-ttu-id="8acb5-221">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-221">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-222">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8acb5-222">In Global Catalog</span></span>      | <span data-ttu-id="8acb5-223">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-223">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-224">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8acb5-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acb5-225">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8acb5-225">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acb5-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acb5-226">Range-Lower</span></span>            | <span data-ttu-id="8acb5-227">1</span><span class="sxs-lookup"><span data-stu-id="8acb5-227">1</span></span>                                                                                             |
| <span data-ttu-id="8acb5-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acb5-228">Range-Upper</span></span>            | <span data-ttu-id="8acb5-229">64</span><span class="sxs-lookup"><span data-stu-id="8acb5-229">64</span></span>                                                                                            |
| <span data-ttu-id="8acb5-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-230">Search-Flags</span></span>           | <span data-ttu-id="8acb5-231">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8acb5-231">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="8acb5-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-232">System-Flags</span></span>           | <span data-ttu-id="8acb5-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acb5-233">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acb5-234">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8acb5-234">Classes used in</span></span>        | [<span data-ttu-id="8acb5-235">**個人**</span><span class="sxs-lookup"><span data-stu-id="8acb5-235">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="8acb5-236">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="8acb5-236">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8acb5-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8acb5-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8acb5-238">進入</span><span class="sxs-lookup"><span data-stu-id="8acb5-238">Entry</span></span> | <span data-ttu-id="8acb5-239">值</span><span class="sxs-lookup"><span data-stu-id="8acb5-239">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acb5-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8acb5-240">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acb5-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acb5-241">MAPI-Id</span></span>                | <span data-ttu-id="8acb5-242">0x3A11</span><span class="sxs-lookup"><span data-stu-id="8acb5-242">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="8acb5-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acb5-243">System-Only</span></span>            | <span data-ttu-id="8acb5-244">否</span><span class="sxs-lookup"><span data-stu-id="8acb5-244">False</span></span>                                                                                         |
| <span data-ttu-id="8acb5-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8acb5-245">Is-Single-Valued</span></span>       | <span data-ttu-id="8acb5-246">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-246">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8acb5-247">Is Indexed</span></span>             | <span data-ttu-id="8acb5-248">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-248">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8acb5-249">In Global Catalog</span></span>      | <span data-ttu-id="8acb5-250">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-250">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8acb5-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acb5-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8acb5-252">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acb5-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acb5-253">Range-Lower</span></span>            | <span data-ttu-id="8acb5-254">1</span><span class="sxs-lookup"><span data-stu-id="8acb5-254">1</span></span>                                                                                             |
| <span data-ttu-id="8acb5-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acb5-255">Range-Upper</span></span>            | <span data-ttu-id="8acb5-256">64</span><span class="sxs-lookup"><span data-stu-id="8acb5-256">64</span></span>                                                                                            |
| <span data-ttu-id="8acb5-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-257">Search-Flags</span></span>           | <span data-ttu-id="8acb5-258">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8acb5-258">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="8acb5-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-259">System-Flags</span></span>           | <span data-ttu-id="8acb5-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acb5-260">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acb5-261">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8acb5-261">Classes used in</span></span>        | [<span data-ttu-id="8acb5-262">**個人**</span><span class="sxs-lookup"><span data-stu-id="8acb5-262">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="8acb5-263">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="8acb5-263">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8acb5-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8acb5-264">Windows Server 2012</span></span>



| <span data-ttu-id="8acb5-265">進入</span><span class="sxs-lookup"><span data-stu-id="8acb5-265">Entry</span></span> | <span data-ttu-id="8acb5-266">值</span><span class="sxs-lookup"><span data-stu-id="8acb5-266">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acb5-267">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8acb5-267">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="8acb5-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8acb5-268">MAPI-Id</span></span>                | <span data-ttu-id="8acb5-269">0x3A11</span><span class="sxs-lookup"><span data-stu-id="8acb5-269">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="8acb5-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="8acb5-270">System-Only</span></span>            | <span data-ttu-id="8acb5-271">否</span><span class="sxs-lookup"><span data-stu-id="8acb5-271">False</span></span>                                                                                         |
| <span data-ttu-id="8acb5-272">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8acb5-272">Is-Single-Valued</span></span>       | <span data-ttu-id="8acb5-273">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-273">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-274">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8acb5-274">Is Indexed</span></span>             | <span data-ttu-id="8acb5-275">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-275">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-276">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8acb5-276">In Global Catalog</span></span>      | <span data-ttu-id="8acb5-277">對</span><span class="sxs-lookup"><span data-stu-id="8acb5-277">True</span></span>                                                                                          |
| <span data-ttu-id="8acb5-278">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8acb5-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="8acb5-279">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8acb5-279">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="8acb5-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8acb5-280">Range-Lower</span></span>            | <span data-ttu-id="8acb5-281">1</span><span class="sxs-lookup"><span data-stu-id="8acb5-281">1</span></span>                                                                                             |
| <span data-ttu-id="8acb5-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8acb5-282">Range-Upper</span></span>            | <span data-ttu-id="8acb5-283">64</span><span class="sxs-lookup"><span data-stu-id="8acb5-283">64</span></span>                                                                                            |
| <span data-ttu-id="8acb5-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-284">Search-Flags</span></span>           | <span data-ttu-id="8acb5-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8acb5-285">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="8acb5-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8acb5-286">System-Flags</span></span>           | <span data-ttu-id="8acb5-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8acb5-287">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="8acb5-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8acb5-288">Classes used in</span></span>        | [<span data-ttu-id="8acb5-289">**個人**</span><span class="sxs-lookup"><span data-stu-id="8acb5-289">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="8acb5-290">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="8acb5-290">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



 

 






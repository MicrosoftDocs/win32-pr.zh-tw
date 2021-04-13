---
title: ms DS-非安全性群組-額外類別屬性
description: 可透過 Active Directory 消費者和電腦嵌入式管理單元新增至非安全性群組之非標準類別的一般名稱。
ms.assetid: 5b89c8d2-0450-480b-9252-17ae375e3a57
ms.tgt_platform: multiple
keywords:
- ms DS-非安全性群組-額外類別的屬性 AD 架構
- 非安全性群組-額外類別的屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Non-Security-Group-Extra-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c436151eeef2a08a2b1d0208b046e23dc8d1559b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385450"
---
# <a name="ms-ds-non-security-group-extra-classes-attribute"></a><span data-ttu-id="1e507-105">ms DS-非安全性群組-額外類別屬性</span><span class="sxs-lookup"><span data-stu-id="1e507-105">ms-DS-Non-Security-Group-Extra-Classes attribute</span></span>

<span data-ttu-id="1e507-106">可透過 Active Directory 消費者和電腦嵌入式管理單元新增至非安全性群組之非標準類別的一般名稱。</span><span class="sxs-lookup"><span data-stu-id="1e507-106">The common names of the nonstandard classes that can be added to a nonsecurity group through the Active Directory Users and Computers snap-in.</span></span>



| <span data-ttu-id="1e507-107">進入</span><span class="sxs-lookup"><span data-stu-id="1e507-107">Entry</span></span> | <span data-ttu-id="1e507-108">值</span><span class="sxs-lookup"><span data-stu-id="1e507-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1e507-109">CN</span><span class="sxs-lookup"><span data-stu-id="1e507-109">CN</span></span>                | <span data-ttu-id="1e507-110">ms DS-非安全性群組-額外類別</span><span class="sxs-lookup"><span data-stu-id="1e507-110">ms-DS-Non-Security-Group-Extra-Classes</span></span>      |
| <span data-ttu-id="1e507-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1e507-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1e507-112">非安全性群組-額外類別</span><span class="sxs-lookup"><span data-stu-id="1e507-112">msDS-Non-Security-Group-Extra-Classes</span></span>       |
| <span data-ttu-id="1e507-113">大小</span><span class="sxs-lookup"><span data-stu-id="1e507-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1e507-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1e507-114">Update Privilege</span></span>  | <span data-ttu-id="1e507-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="1e507-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="1e507-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1e507-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1e507-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1e507-117">Attribute-Id</span></span>      | <span data-ttu-id="1e507-118">1.2.840.113556.1.4.1689</span><span class="sxs-lookup"><span data-stu-id="1e507-118">1.2.840.113556.1.4.1689</span></span>                     |
| <span data-ttu-id="1e507-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1e507-119">System-Id-Guid</span></span>    | <span data-ttu-id="1e507-120">2de144fc-1f52-486f-bdf4-16fcc3084e54</span><span class="sxs-lookup"><span data-stu-id="1e507-120">2de144fc-1f52-486f-bdf4-16fcc3084e54</span></span>        |
| <span data-ttu-id="1e507-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e507-121">Syntax</span></span>            | [<span data-ttu-id="1e507-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1e507-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1e507-123">實作</span><span class="sxs-lookup"><span data-stu-id="1e507-123">Implementations</span></span>

-   [<span data-ttu-id="1e507-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1e507-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1e507-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1e507-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1e507-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1e507-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1e507-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1e507-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1e507-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1e507-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1e507-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e507-129">Windows Server 2003</span></span>



| <span data-ttu-id="1e507-130">進入</span><span class="sxs-lookup"><span data-stu-id="1e507-130">Entry</span></span> | <span data-ttu-id="1e507-131">值</span><span class="sxs-lookup"><span data-stu-id="1e507-131">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1e507-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e507-132">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e507-133">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e507-134">System-Only</span></span>            | <span data-ttu-id="1e507-135">否</span><span class="sxs-lookup"><span data-stu-id="1e507-135">False</span></span>                                               |
| <span data-ttu-id="1e507-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e507-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1e507-137">否</span><span class="sxs-lookup"><span data-stu-id="1e507-137">False</span></span>                                               |
| <span data-ttu-id="1e507-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e507-138">Is Indexed</span></span>             | <span data-ttu-id="1e507-139">否</span><span class="sxs-lookup"><span data-stu-id="1e507-139">False</span></span>                                               |
| <span data-ttu-id="1e507-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e507-140">In Global Catalog</span></span>      | <span data-ttu-id="1e507-141">否</span><span class="sxs-lookup"><span data-stu-id="1e507-141">False</span></span>                                               |
| <span data-ttu-id="1e507-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e507-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e507-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e507-143">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1e507-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e507-144">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e507-145">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-146">Search-Flags</span></span>           | <span data-ttu-id="1e507-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e507-147">0x00000000</span></span>                                          |
| <span data-ttu-id="1e507-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-148">System-Flags</span></span>           | <span data-ttu-id="1e507-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e507-149">0x00000010</span></span>                                          |
| <span data-ttu-id="1e507-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e507-150">Classes used in</span></span>        | [<span data-ttu-id="1e507-151">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1e507-151">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1e507-152">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1e507-152">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1e507-153">進入</span><span class="sxs-lookup"><span data-stu-id="1e507-153">Entry</span></span> | <span data-ttu-id="1e507-154">值</span><span class="sxs-lookup"><span data-stu-id="1e507-154">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1e507-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e507-155">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e507-156">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e507-157">System-Only</span></span>            | <span data-ttu-id="1e507-158">否</span><span class="sxs-lookup"><span data-stu-id="1e507-158">False</span></span>                                               |
| <span data-ttu-id="1e507-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e507-159">Is-Single-Valued</span></span>       | <span data-ttu-id="1e507-160">否</span><span class="sxs-lookup"><span data-stu-id="1e507-160">False</span></span>                                               |
| <span data-ttu-id="1e507-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e507-161">Is Indexed</span></span>             | <span data-ttu-id="1e507-162">否</span><span class="sxs-lookup"><span data-stu-id="1e507-162">False</span></span>                                               |
| <span data-ttu-id="1e507-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e507-163">In Global Catalog</span></span>      | <span data-ttu-id="1e507-164">否</span><span class="sxs-lookup"><span data-stu-id="1e507-164">False</span></span>                                               |
| <span data-ttu-id="1e507-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e507-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e507-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e507-166">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1e507-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e507-167">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e507-168">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-169">Search-Flags</span></span>           | <span data-ttu-id="1e507-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e507-170">0x00000000</span></span>                                          |
| <span data-ttu-id="1e507-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-171">System-Flags</span></span>           | <span data-ttu-id="1e507-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e507-172">0x00000010</span></span>                                          |
| <span data-ttu-id="1e507-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e507-173">Classes used in</span></span>        | [<span data-ttu-id="1e507-174">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1e507-174">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1e507-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e507-175">Windows Server 2008</span></span>



| <span data-ttu-id="1e507-176">進入</span><span class="sxs-lookup"><span data-stu-id="1e507-176">Entry</span></span> | <span data-ttu-id="1e507-177">值</span><span class="sxs-lookup"><span data-stu-id="1e507-177">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1e507-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e507-178">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e507-179">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e507-180">System-Only</span></span>            | <span data-ttu-id="1e507-181">否</span><span class="sxs-lookup"><span data-stu-id="1e507-181">False</span></span>                                               |
| <span data-ttu-id="1e507-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e507-182">Is-Single-Valued</span></span>       | <span data-ttu-id="1e507-183">否</span><span class="sxs-lookup"><span data-stu-id="1e507-183">False</span></span>                                               |
| <span data-ttu-id="1e507-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e507-184">Is Indexed</span></span>             | <span data-ttu-id="1e507-185">否</span><span class="sxs-lookup"><span data-stu-id="1e507-185">False</span></span>                                               |
| <span data-ttu-id="1e507-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e507-186">In Global Catalog</span></span>      | <span data-ttu-id="1e507-187">否</span><span class="sxs-lookup"><span data-stu-id="1e507-187">False</span></span>                                               |
| <span data-ttu-id="1e507-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e507-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e507-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e507-189">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1e507-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e507-190">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e507-191">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-192">Search-Flags</span></span>           | <span data-ttu-id="1e507-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e507-193">0x00000000</span></span>                                          |
| <span data-ttu-id="1e507-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-194">System-Flags</span></span>           | <span data-ttu-id="1e507-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e507-195">0x00000010</span></span>                                          |
| <span data-ttu-id="1e507-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e507-196">Classes used in</span></span>        | [<span data-ttu-id="1e507-197">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1e507-197">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1e507-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e507-198">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1e507-199">進入</span><span class="sxs-lookup"><span data-stu-id="1e507-199">Entry</span></span> | <span data-ttu-id="1e507-200">值</span><span class="sxs-lookup"><span data-stu-id="1e507-200">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1e507-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e507-201">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e507-202">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e507-203">System-Only</span></span>            | <span data-ttu-id="1e507-204">否</span><span class="sxs-lookup"><span data-stu-id="1e507-204">False</span></span>                                               |
| <span data-ttu-id="1e507-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e507-205">Is-Single-Valued</span></span>       | <span data-ttu-id="1e507-206">否</span><span class="sxs-lookup"><span data-stu-id="1e507-206">False</span></span>                                               |
| <span data-ttu-id="1e507-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e507-207">Is Indexed</span></span>             | <span data-ttu-id="1e507-208">否</span><span class="sxs-lookup"><span data-stu-id="1e507-208">False</span></span>                                               |
| <span data-ttu-id="1e507-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e507-209">In Global Catalog</span></span>      | <span data-ttu-id="1e507-210">否</span><span class="sxs-lookup"><span data-stu-id="1e507-210">False</span></span>                                               |
| <span data-ttu-id="1e507-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e507-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e507-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e507-212">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1e507-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e507-213">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e507-214">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-215">Search-Flags</span></span>           | <span data-ttu-id="1e507-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e507-216">0x00000000</span></span>                                          |
| <span data-ttu-id="1e507-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-217">System-Flags</span></span>           | <span data-ttu-id="1e507-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e507-218">0x00000010</span></span>                                          |
| <span data-ttu-id="1e507-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e507-219">Classes used in</span></span>        | [<span data-ttu-id="1e507-220">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1e507-220">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1e507-221">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e507-221">Windows Server 2012</span></span>



| <span data-ttu-id="1e507-222">進入</span><span class="sxs-lookup"><span data-stu-id="1e507-222">Entry</span></span> | <span data-ttu-id="1e507-223">值</span><span class="sxs-lookup"><span data-stu-id="1e507-223">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1e507-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e507-224">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e507-225">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1e507-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e507-226">System-Only</span></span>            | <span data-ttu-id="1e507-227">否</span><span class="sxs-lookup"><span data-stu-id="1e507-227">False</span></span>                                               |
| <span data-ttu-id="1e507-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e507-228">Is-Single-Valued</span></span>       | <span data-ttu-id="1e507-229">否</span><span class="sxs-lookup"><span data-stu-id="1e507-229">False</span></span>                                               |
| <span data-ttu-id="1e507-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e507-230">Is Indexed</span></span>             | <span data-ttu-id="1e507-231">否</span><span class="sxs-lookup"><span data-stu-id="1e507-231">False</span></span>                                               |
| <span data-ttu-id="1e507-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e507-232">In Global Catalog</span></span>      | <span data-ttu-id="1e507-233">否</span><span class="sxs-lookup"><span data-stu-id="1e507-233">False</span></span>                                               |
| <span data-ttu-id="1e507-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e507-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e507-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e507-235">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1e507-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e507-236">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e507-237">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1e507-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-238">Search-Flags</span></span>           | <span data-ttu-id="1e507-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e507-239">0x00000000</span></span>                                          |
| <span data-ttu-id="1e507-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e507-240">System-Flags</span></span>           | <span data-ttu-id="1e507-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e507-241">0x00000010</span></span>                                          |
| <span data-ttu-id="1e507-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e507-242">Classes used in</span></span>        | [<span data-ttu-id="1e507-243">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1e507-243">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1e507-244">備註</span><span class="sxs-lookup"><span data-stu-id="1e507-244">Remarks</span></span>

<span data-ttu-id="1e507-245">下列清單會識別可透過 Active Directory 消費者和電腦嵌入式管理單元新增至群組的標準類別。</span><span class="sxs-lookup"><span data-stu-id="1e507-245">The following list identifies the standard classes that can be added to a group through the Active Directory Users and Computers snap-in.</span></span>

-   [<span data-ttu-id="1e507-246">**Group**</span><span class="sxs-lookup"><span data-stu-id="1e507-246">**Group**</span></span>](c-group.md)
-   [<span data-ttu-id="1e507-247">**User**</span><span class="sxs-lookup"><span data-stu-id="1e507-247">**User**</span></span>](c-user.md)
-   [<span data-ttu-id="1e507-248">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1e507-248">**inetOrgPerson**</span></span>](c-inetorgperson.md)
-   [<span data-ttu-id="1e507-249">**Contact**</span><span class="sxs-lookup"><span data-stu-id="1e507-249">**Contact**</span></span>](c-contact.md)
-   [<span data-ttu-id="1e507-250">**電腦**</span><span class="sxs-lookup"><span data-stu-id="1e507-250">**Computer**</span></span>](c-computer.md)

## <a name="see-also"></a><span data-ttu-id="1e507-251">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e507-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e507-252">**ms-DS-安全性群組-額外類別**</span><span class="sxs-lookup"><span data-stu-id="1e507-252">**ms-DS-Security-Group-Extra-Classes**</span></span>](a-msds-security-group-extra-classes.md)
</dt> </dl>

 

 






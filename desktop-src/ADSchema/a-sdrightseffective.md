---
title: SD-Rights-有效屬性
description: 此結構化屬性會傳回單一 DWORD 值，最多可以有三個位設定擁有者 \_ 安全性 \_ INFORMATIONDACL \_ 安全性 \_ INFORMATIONSACL \_ 安全性 \_ 資訊（如果已設定位），然後使用者就可以對安全描述項的對應部分進行寫入存取。 擁有者表示擁有者和群組。
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- SD-Rights-有效的屬性 AD 架構
- sDRightsEffective 屬性 AD 架構
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac449cd18b3fb75a61f04fffc266c290b7763295
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844935"
---
# <a name="sd-rights-effective-attribute"></a><span data-ttu-id="e3b49-106">SD-Rights-有效屬性</span><span class="sxs-lookup"><span data-stu-id="e3b49-106">SD-Rights-Effective attribute</span></span>

<span data-ttu-id="e3b49-107">這個已建立的屬性會傳回單一 **DWORD** 值，最多可設定三個位：</span><span class="sxs-lookup"><span data-stu-id="e3b49-107">This constructed attribute returns a single **DWORD** value that can have up to three bits set:</span></span>

-   <span data-ttu-id="e3b49-108">擁有者 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="e3b49-108">OWNER\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="e3b49-109">DACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="e3b49-109">DACL\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="e3b49-110">SACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="e3b49-110">SACL\_SECURITY\_INFORMATION</span></span>

<span data-ttu-id="e3b49-111">如果設定了位，則使用者會擁有安全描述項之對應部分的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="e3b49-111">If a bit is set, then the user has write access to the corresponding part of the security descriptor.</span></span> <span data-ttu-id="e3b49-112">擁有者表示擁有者和群組。</span><span class="sxs-lookup"><span data-stu-id="e3b49-112">Owner means both owner and group.</span></span>



| <span data-ttu-id="e3b49-113">進入</span><span class="sxs-lookup"><span data-stu-id="e3b49-113">Entry</span></span> | <span data-ttu-id="e3b49-114">值</span><span class="sxs-lookup"><span data-stu-id="e3b49-114">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e3b49-115">CN</span><span class="sxs-lookup"><span data-stu-id="e3b49-115">CN</span></span>                | <span data-ttu-id="e3b49-116">SD-Rights-有效</span><span class="sxs-lookup"><span data-stu-id="e3b49-116">SD-Rights-Effective</span></span>                  |
| <span data-ttu-id="e3b49-117">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e3b49-117">Ldap-Display-Name</span></span> | <span data-ttu-id="e3b49-118">sDRightsEffective</span><span class="sxs-lookup"><span data-stu-id="e3b49-118">sDRightsEffective</span></span>                    |
| <span data-ttu-id="e3b49-119">大小</span><span class="sxs-lookup"><span data-stu-id="e3b49-119">Size</span></span>              | \-                                   |
| <span data-ttu-id="e3b49-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e3b49-120">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e3b49-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e3b49-121">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e3b49-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e3b49-122">Attribute-Id</span></span>      | <span data-ttu-id="e3b49-123">1.2.840.113556.1.4.1304</span><span class="sxs-lookup"><span data-stu-id="e3b49-123">1.2.840.113556.1.4.1304</span></span>              |
| <span data-ttu-id="e3b49-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e3b49-124">System-Id-Guid</span></span>    | <span data-ttu-id="e3b49-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e3b49-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="e3b49-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3b49-126">Syntax</span></span>            | [<span data-ttu-id="e3b49-127">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="e3b49-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e3b49-128">實作</span><span class="sxs-lookup"><span data-stu-id="e3b49-128">Implementations</span></span>

-   [<span data-ttu-id="e3b49-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e3b49-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e3b49-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e3b49-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e3b49-131">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e3b49-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e3b49-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e3b49-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e3b49-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e3b49-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e3b49-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e3b49-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e3b49-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e3b49-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e3b49-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e3b49-136">Windows 2000 Server</span></span>



| <span data-ttu-id="e3b49-137">進入</span><span class="sxs-lookup"><span data-stu-id="e3b49-137">Entry</span></span> | <span data-ttu-id="e3b49-138">值</span><span class="sxs-lookup"><span data-stu-id="e3b49-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3b49-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e3b49-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3b49-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3b49-141">System-Only</span></span>            | <span data-ttu-id="e3b49-142">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-142">False</span></span>                           |
| <span data-ttu-id="e3b49-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e3b49-143">Is-Single-Valued</span></span>       | <span data-ttu-id="e3b49-144">對</span><span class="sxs-lookup"><span data-stu-id="e3b49-144">True</span></span>                            |
| <span data-ttu-id="e3b49-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e3b49-145">Is Indexed</span></span>             | <span data-ttu-id="e3b49-146">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-146">False</span></span>                           |
| <span data-ttu-id="e3b49-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e3b49-147">In Global Catalog</span></span>      | <span data-ttu-id="e3b49-148">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-148">False</span></span>                           |
| <span data-ttu-id="e3b49-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e3b49-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3b49-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e3b49-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3b49-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3b49-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3b49-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3b49-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3b49-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-153">Search-Flags</span></span>           | <span data-ttu-id="e3b49-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3b49-154">0x00000000</span></span>                      |
| <span data-ttu-id="e3b49-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-155">System-Flags</span></span>           | <span data-ttu-id="e3b49-156">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e3b49-156">0x08000014</span></span>                      |
| <span data-ttu-id="e3b49-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e3b49-157">Classes used in</span></span>        | [<span data-ttu-id="e3b49-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e3b49-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e3b49-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3b49-159">Windows Server 2003</span></span>



| <span data-ttu-id="e3b49-160">進入</span><span class="sxs-lookup"><span data-stu-id="e3b49-160">Entry</span></span> | <span data-ttu-id="e3b49-161">值</span><span class="sxs-lookup"><span data-stu-id="e3b49-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3b49-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e3b49-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3b49-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3b49-164">System-Only</span></span>            | <span data-ttu-id="e3b49-165">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-165">False</span></span>                           |
| <span data-ttu-id="e3b49-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e3b49-166">Is-Single-Valued</span></span>       | <span data-ttu-id="e3b49-167">對</span><span class="sxs-lookup"><span data-stu-id="e3b49-167">True</span></span>                            |
| <span data-ttu-id="e3b49-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e3b49-168">Is Indexed</span></span>             | <span data-ttu-id="e3b49-169">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-169">False</span></span>                           |
| <span data-ttu-id="e3b49-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e3b49-170">In Global Catalog</span></span>      | <span data-ttu-id="e3b49-171">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-171">False</span></span>                           |
| <span data-ttu-id="e3b49-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e3b49-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3b49-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e3b49-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3b49-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3b49-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3b49-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3b49-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3b49-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-176">Search-Flags</span></span>           | <span data-ttu-id="e3b49-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3b49-177">0x00000000</span></span>                      |
| <span data-ttu-id="e3b49-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-178">System-Flags</span></span>           | <span data-ttu-id="e3b49-179">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e3b49-179">0x08000014</span></span>                      |
| <span data-ttu-id="e3b49-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e3b49-180">Classes used in</span></span>        | [<span data-ttu-id="e3b49-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e3b49-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e3b49-182">亞當</span><span class="sxs-lookup"><span data-stu-id="e3b49-182">ADAM</span></span>



| <span data-ttu-id="e3b49-183">進入</span><span class="sxs-lookup"><span data-stu-id="e3b49-183">Entry</span></span> | <span data-ttu-id="e3b49-184">值</span><span class="sxs-lookup"><span data-stu-id="e3b49-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3b49-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e3b49-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3b49-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3b49-187">System-Only</span></span>            | <span data-ttu-id="e3b49-188">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-188">False</span></span>                           |
| <span data-ttu-id="e3b49-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e3b49-189">Is-Single-Valued</span></span>       | <span data-ttu-id="e3b49-190">對</span><span class="sxs-lookup"><span data-stu-id="e3b49-190">True</span></span>                            |
| <span data-ttu-id="e3b49-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e3b49-191">Is Indexed</span></span>             | <span data-ttu-id="e3b49-192">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-192">False</span></span>                           |
| <span data-ttu-id="e3b49-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e3b49-193">In Global Catalog</span></span>      | <span data-ttu-id="e3b49-194">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-194">False</span></span>                           |
| <span data-ttu-id="e3b49-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e3b49-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3b49-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e3b49-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3b49-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3b49-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3b49-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3b49-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3b49-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-199">Search-Flags</span></span>           | <span data-ttu-id="e3b49-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3b49-200">0x00000000</span></span>                      |
| <span data-ttu-id="e3b49-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-201">System-Flags</span></span>           | <span data-ttu-id="e3b49-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e3b49-202">0x08000014</span></span>                      |
| <span data-ttu-id="e3b49-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e3b49-203">Classes used in</span></span>        | [<span data-ttu-id="e3b49-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e3b49-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e3b49-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e3b49-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e3b49-206">進入</span><span class="sxs-lookup"><span data-stu-id="e3b49-206">Entry</span></span> | <span data-ttu-id="e3b49-207">值</span><span class="sxs-lookup"><span data-stu-id="e3b49-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3b49-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e3b49-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3b49-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3b49-210">System-Only</span></span>            | <span data-ttu-id="e3b49-211">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-211">False</span></span>                           |
| <span data-ttu-id="e3b49-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e3b49-212">Is-Single-Valued</span></span>       | <span data-ttu-id="e3b49-213">對</span><span class="sxs-lookup"><span data-stu-id="e3b49-213">True</span></span>                            |
| <span data-ttu-id="e3b49-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e3b49-214">Is Indexed</span></span>             | <span data-ttu-id="e3b49-215">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-215">False</span></span>                           |
| <span data-ttu-id="e3b49-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e3b49-216">In Global Catalog</span></span>      | <span data-ttu-id="e3b49-217">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-217">False</span></span>                           |
| <span data-ttu-id="e3b49-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e3b49-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3b49-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e3b49-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3b49-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3b49-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3b49-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3b49-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3b49-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-222">Search-Flags</span></span>           | <span data-ttu-id="e3b49-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3b49-223">0x00000000</span></span>                      |
| <span data-ttu-id="e3b49-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-224">System-Flags</span></span>           | <span data-ttu-id="e3b49-225">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e3b49-225">0x08000014</span></span>                      |
| <span data-ttu-id="e3b49-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e3b49-226">Classes used in</span></span>        | [<span data-ttu-id="e3b49-227">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e3b49-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e3b49-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3b49-228">Windows Server 2008</span></span>



| <span data-ttu-id="e3b49-229">進入</span><span class="sxs-lookup"><span data-stu-id="e3b49-229">Entry</span></span> | <span data-ttu-id="e3b49-230">值</span><span class="sxs-lookup"><span data-stu-id="e3b49-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3b49-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e3b49-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3b49-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3b49-233">System-Only</span></span>            | <span data-ttu-id="e3b49-234">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-234">False</span></span>                           |
| <span data-ttu-id="e3b49-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e3b49-235">Is-Single-Valued</span></span>       | <span data-ttu-id="e3b49-236">對</span><span class="sxs-lookup"><span data-stu-id="e3b49-236">True</span></span>                            |
| <span data-ttu-id="e3b49-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e3b49-237">Is Indexed</span></span>             | <span data-ttu-id="e3b49-238">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-238">False</span></span>                           |
| <span data-ttu-id="e3b49-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e3b49-239">In Global Catalog</span></span>      | <span data-ttu-id="e3b49-240">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-240">False</span></span>                           |
| <span data-ttu-id="e3b49-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e3b49-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3b49-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e3b49-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3b49-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3b49-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3b49-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3b49-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3b49-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-245">Search-Flags</span></span>           | <span data-ttu-id="e3b49-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3b49-246">0x00000000</span></span>                      |
| <span data-ttu-id="e3b49-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-247">System-Flags</span></span>           | <span data-ttu-id="e3b49-248">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e3b49-248">0x08000014</span></span>                      |
| <span data-ttu-id="e3b49-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e3b49-249">Classes used in</span></span>        | [<span data-ttu-id="e3b49-250">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e3b49-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e3b49-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3b49-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e3b49-252">進入</span><span class="sxs-lookup"><span data-stu-id="e3b49-252">Entry</span></span> | <span data-ttu-id="e3b49-253">值</span><span class="sxs-lookup"><span data-stu-id="e3b49-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3b49-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e3b49-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3b49-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3b49-256">System-Only</span></span>            | <span data-ttu-id="e3b49-257">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-257">False</span></span>                           |
| <span data-ttu-id="e3b49-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e3b49-258">Is-Single-Valued</span></span>       | <span data-ttu-id="e3b49-259">對</span><span class="sxs-lookup"><span data-stu-id="e3b49-259">True</span></span>                            |
| <span data-ttu-id="e3b49-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e3b49-260">Is Indexed</span></span>             | <span data-ttu-id="e3b49-261">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-261">False</span></span>                           |
| <span data-ttu-id="e3b49-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e3b49-262">In Global Catalog</span></span>      | <span data-ttu-id="e3b49-263">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-263">False</span></span>                           |
| <span data-ttu-id="e3b49-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e3b49-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3b49-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e3b49-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3b49-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3b49-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3b49-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3b49-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3b49-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-268">Search-Flags</span></span>           | <span data-ttu-id="e3b49-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3b49-269">0x00000000</span></span>                      |
| <span data-ttu-id="e3b49-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-270">System-Flags</span></span>           | <span data-ttu-id="e3b49-271">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e3b49-271">0x08000014</span></span>                      |
| <span data-ttu-id="e3b49-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e3b49-272">Classes used in</span></span>        | [<span data-ttu-id="e3b49-273">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e3b49-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e3b49-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3b49-274">Windows Server 2012</span></span>



| <span data-ttu-id="e3b49-275">進入</span><span class="sxs-lookup"><span data-stu-id="e3b49-275">Entry</span></span> | <span data-ttu-id="e3b49-276">值</span><span class="sxs-lookup"><span data-stu-id="e3b49-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3b49-277">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e3b49-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3b49-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3b49-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3b49-279">System-Only</span></span>            | <span data-ttu-id="e3b49-280">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-280">False</span></span>                           |
| <span data-ttu-id="e3b49-281">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e3b49-281">Is-Single-Valued</span></span>       | <span data-ttu-id="e3b49-282">對</span><span class="sxs-lookup"><span data-stu-id="e3b49-282">True</span></span>                            |
| <span data-ttu-id="e3b49-283">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e3b49-283">Is Indexed</span></span>             | <span data-ttu-id="e3b49-284">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-284">False</span></span>                           |
| <span data-ttu-id="e3b49-285">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e3b49-285">In Global Catalog</span></span>      | <span data-ttu-id="e3b49-286">否</span><span class="sxs-lookup"><span data-stu-id="e3b49-286">False</span></span>                           |
| <span data-ttu-id="e3b49-287">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e3b49-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3b49-288">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e3b49-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3b49-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3b49-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3b49-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3b49-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3b49-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-291">Search-Flags</span></span>           | <span data-ttu-id="e3b49-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3b49-292">0x00000000</span></span>                      |
| <span data-ttu-id="e3b49-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3b49-293">System-Flags</span></span>           | <span data-ttu-id="e3b49-294">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e3b49-294">0x08000014</span></span>                      |
| <span data-ttu-id="e3b49-295">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e3b49-295">Classes used in</span></span>        | [<span data-ttu-id="e3b49-296">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e3b49-296">**Top**</span></span>](c-top.md)<br/> |



 

 






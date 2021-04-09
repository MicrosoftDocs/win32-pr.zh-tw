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
# <a name="sd-rights-effective-attribute"></a><span data-ttu-id="49dde-106">SD-Rights-有效屬性</span><span class="sxs-lookup"><span data-stu-id="49dde-106">SD-Rights-Effective attribute</span></span>

<span data-ttu-id="49dde-107">這個已建立的屬性會傳回單一 **DWORD** 值，最多可設定三個位：</span><span class="sxs-lookup"><span data-stu-id="49dde-107">This constructed attribute returns a single **DWORD** value that can have up to three bits set:</span></span>

-   <span data-ttu-id="49dde-108">擁有者 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="49dde-108">OWNER\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="49dde-109">DACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="49dde-109">DACL\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="49dde-110">SACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="49dde-110">SACL\_SECURITY\_INFORMATION</span></span>

<span data-ttu-id="49dde-111">如果設定了位，則使用者會擁有安全描述項之對應部分的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="49dde-111">If a bit is set, then the user has write access to the corresponding part of the security descriptor.</span></span> <span data-ttu-id="49dde-112">擁有者表示擁有者和群組。</span><span class="sxs-lookup"><span data-stu-id="49dde-112">Owner means both owner and group.</span></span>



| <span data-ttu-id="49dde-113">進入</span><span class="sxs-lookup"><span data-stu-id="49dde-113">Entry</span></span> | <span data-ttu-id="49dde-114">值</span><span class="sxs-lookup"><span data-stu-id="49dde-114">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="49dde-115">CN</span><span class="sxs-lookup"><span data-stu-id="49dde-115">CN</span></span>                | <span data-ttu-id="49dde-116">SD-Rights-有效</span><span class="sxs-lookup"><span data-stu-id="49dde-116">SD-Rights-Effective</span></span>                  |
| <span data-ttu-id="49dde-117">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="49dde-117">Ldap-Display-Name</span></span> | <span data-ttu-id="49dde-118">sDRightsEffective</span><span class="sxs-lookup"><span data-stu-id="49dde-118">sDRightsEffective</span></span>                    |
| <span data-ttu-id="49dde-119">大小</span><span class="sxs-lookup"><span data-stu-id="49dde-119">Size</span></span>              | \-                                   |
| <span data-ttu-id="49dde-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="49dde-120">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="49dde-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="49dde-121">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="49dde-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="49dde-122">Attribute-Id</span></span>      | <span data-ttu-id="49dde-123">1.2.840.113556.1.4.1304</span><span class="sxs-lookup"><span data-stu-id="49dde-123">1.2.840.113556.1.4.1304</span></span>              |
| <span data-ttu-id="49dde-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="49dde-124">System-Id-Guid</span></span>    | <span data-ttu-id="49dde-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="49dde-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="49dde-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="49dde-126">Syntax</span></span>            | [<span data-ttu-id="49dde-127">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="49dde-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="49dde-128">實作</span><span class="sxs-lookup"><span data-stu-id="49dde-128">Implementations</span></span>

-   [<span data-ttu-id="49dde-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="49dde-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="49dde-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="49dde-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="49dde-131">**亞當**</span><span class="sxs-lookup"><span data-stu-id="49dde-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="49dde-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="49dde-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="49dde-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="49dde-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="49dde-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="49dde-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="49dde-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="49dde-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="49dde-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49dde-136">Windows 2000 Server</span></span>



| <span data-ttu-id="49dde-137">進入</span><span class="sxs-lookup"><span data-stu-id="49dde-137">Entry</span></span> | <span data-ttu-id="49dde-138">值</span><span class="sxs-lookup"><span data-stu-id="49dde-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="49dde-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49dde-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49dde-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="49dde-141">System-Only</span></span>            | <span data-ttu-id="49dde-142">否</span><span class="sxs-lookup"><span data-stu-id="49dde-142">False</span></span>                           |
| <span data-ttu-id="49dde-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49dde-143">Is-Single-Valued</span></span>       | <span data-ttu-id="49dde-144">對</span><span class="sxs-lookup"><span data-stu-id="49dde-144">True</span></span>                            |
| <span data-ttu-id="49dde-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49dde-145">Is Indexed</span></span>             | <span data-ttu-id="49dde-146">否</span><span class="sxs-lookup"><span data-stu-id="49dde-146">False</span></span>                           |
| <span data-ttu-id="49dde-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49dde-147">In Global Catalog</span></span>      | <span data-ttu-id="49dde-148">否</span><span class="sxs-lookup"><span data-stu-id="49dde-148">False</span></span>                           |
| <span data-ttu-id="49dde-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49dde-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="49dde-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49dde-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="49dde-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49dde-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="49dde-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49dde-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="49dde-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-153">Search-Flags</span></span>           | <span data-ttu-id="49dde-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49dde-154">0x00000000</span></span>                      |
| <span data-ttu-id="49dde-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-155">System-Flags</span></span>           | <span data-ttu-id="49dde-156">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49dde-156">0x08000014</span></span>                      |
| <span data-ttu-id="49dde-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49dde-157">Classes used in</span></span>        | [<span data-ttu-id="49dde-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="49dde-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="49dde-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49dde-159">Windows Server 2003</span></span>



| <span data-ttu-id="49dde-160">進入</span><span class="sxs-lookup"><span data-stu-id="49dde-160">Entry</span></span> | <span data-ttu-id="49dde-161">值</span><span class="sxs-lookup"><span data-stu-id="49dde-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="49dde-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49dde-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49dde-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="49dde-164">System-Only</span></span>            | <span data-ttu-id="49dde-165">否</span><span class="sxs-lookup"><span data-stu-id="49dde-165">False</span></span>                           |
| <span data-ttu-id="49dde-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49dde-166">Is-Single-Valued</span></span>       | <span data-ttu-id="49dde-167">對</span><span class="sxs-lookup"><span data-stu-id="49dde-167">True</span></span>                            |
| <span data-ttu-id="49dde-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49dde-168">Is Indexed</span></span>             | <span data-ttu-id="49dde-169">否</span><span class="sxs-lookup"><span data-stu-id="49dde-169">False</span></span>                           |
| <span data-ttu-id="49dde-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49dde-170">In Global Catalog</span></span>      | <span data-ttu-id="49dde-171">否</span><span class="sxs-lookup"><span data-stu-id="49dde-171">False</span></span>                           |
| <span data-ttu-id="49dde-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49dde-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="49dde-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49dde-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="49dde-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49dde-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="49dde-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49dde-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="49dde-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-176">Search-Flags</span></span>           | <span data-ttu-id="49dde-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49dde-177">0x00000000</span></span>                      |
| <span data-ttu-id="49dde-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-178">System-Flags</span></span>           | <span data-ttu-id="49dde-179">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49dde-179">0x08000014</span></span>                      |
| <span data-ttu-id="49dde-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49dde-180">Classes used in</span></span>        | [<span data-ttu-id="49dde-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="49dde-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="49dde-182">亞當</span><span class="sxs-lookup"><span data-stu-id="49dde-182">ADAM</span></span>



| <span data-ttu-id="49dde-183">進入</span><span class="sxs-lookup"><span data-stu-id="49dde-183">Entry</span></span> | <span data-ttu-id="49dde-184">值</span><span class="sxs-lookup"><span data-stu-id="49dde-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="49dde-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49dde-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49dde-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="49dde-187">System-Only</span></span>            | <span data-ttu-id="49dde-188">否</span><span class="sxs-lookup"><span data-stu-id="49dde-188">False</span></span>                           |
| <span data-ttu-id="49dde-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49dde-189">Is-Single-Valued</span></span>       | <span data-ttu-id="49dde-190">對</span><span class="sxs-lookup"><span data-stu-id="49dde-190">True</span></span>                            |
| <span data-ttu-id="49dde-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49dde-191">Is Indexed</span></span>             | <span data-ttu-id="49dde-192">否</span><span class="sxs-lookup"><span data-stu-id="49dde-192">False</span></span>                           |
| <span data-ttu-id="49dde-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49dde-193">In Global Catalog</span></span>      | <span data-ttu-id="49dde-194">否</span><span class="sxs-lookup"><span data-stu-id="49dde-194">False</span></span>                           |
| <span data-ttu-id="49dde-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49dde-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="49dde-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49dde-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="49dde-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49dde-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="49dde-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49dde-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="49dde-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-199">Search-Flags</span></span>           | <span data-ttu-id="49dde-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49dde-200">0x00000000</span></span>                      |
| <span data-ttu-id="49dde-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-201">System-Flags</span></span>           | <span data-ttu-id="49dde-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49dde-202">0x08000014</span></span>                      |
| <span data-ttu-id="49dde-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49dde-203">Classes used in</span></span>        | [<span data-ttu-id="49dde-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="49dde-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="49dde-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="49dde-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="49dde-206">進入</span><span class="sxs-lookup"><span data-stu-id="49dde-206">Entry</span></span> | <span data-ttu-id="49dde-207">值</span><span class="sxs-lookup"><span data-stu-id="49dde-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="49dde-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49dde-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49dde-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="49dde-210">System-Only</span></span>            | <span data-ttu-id="49dde-211">否</span><span class="sxs-lookup"><span data-stu-id="49dde-211">False</span></span>                           |
| <span data-ttu-id="49dde-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49dde-212">Is-Single-Valued</span></span>       | <span data-ttu-id="49dde-213">對</span><span class="sxs-lookup"><span data-stu-id="49dde-213">True</span></span>                            |
| <span data-ttu-id="49dde-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49dde-214">Is Indexed</span></span>             | <span data-ttu-id="49dde-215">否</span><span class="sxs-lookup"><span data-stu-id="49dde-215">False</span></span>                           |
| <span data-ttu-id="49dde-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49dde-216">In Global Catalog</span></span>      | <span data-ttu-id="49dde-217">否</span><span class="sxs-lookup"><span data-stu-id="49dde-217">False</span></span>                           |
| <span data-ttu-id="49dde-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49dde-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="49dde-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49dde-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="49dde-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49dde-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="49dde-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49dde-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="49dde-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-222">Search-Flags</span></span>           | <span data-ttu-id="49dde-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49dde-223">0x00000000</span></span>                      |
| <span data-ttu-id="49dde-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-224">System-Flags</span></span>           | <span data-ttu-id="49dde-225">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49dde-225">0x08000014</span></span>                      |
| <span data-ttu-id="49dde-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49dde-226">Classes used in</span></span>        | [<span data-ttu-id="49dde-227">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="49dde-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="49dde-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49dde-228">Windows Server 2008</span></span>



| <span data-ttu-id="49dde-229">進入</span><span class="sxs-lookup"><span data-stu-id="49dde-229">Entry</span></span> | <span data-ttu-id="49dde-230">值</span><span class="sxs-lookup"><span data-stu-id="49dde-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="49dde-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49dde-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49dde-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="49dde-233">System-Only</span></span>            | <span data-ttu-id="49dde-234">否</span><span class="sxs-lookup"><span data-stu-id="49dde-234">False</span></span>                           |
| <span data-ttu-id="49dde-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49dde-235">Is-Single-Valued</span></span>       | <span data-ttu-id="49dde-236">對</span><span class="sxs-lookup"><span data-stu-id="49dde-236">True</span></span>                            |
| <span data-ttu-id="49dde-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49dde-237">Is Indexed</span></span>             | <span data-ttu-id="49dde-238">否</span><span class="sxs-lookup"><span data-stu-id="49dde-238">False</span></span>                           |
| <span data-ttu-id="49dde-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49dde-239">In Global Catalog</span></span>      | <span data-ttu-id="49dde-240">否</span><span class="sxs-lookup"><span data-stu-id="49dde-240">False</span></span>                           |
| <span data-ttu-id="49dde-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49dde-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="49dde-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49dde-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="49dde-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49dde-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="49dde-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49dde-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="49dde-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-245">Search-Flags</span></span>           | <span data-ttu-id="49dde-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49dde-246">0x00000000</span></span>                      |
| <span data-ttu-id="49dde-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-247">System-Flags</span></span>           | <span data-ttu-id="49dde-248">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49dde-248">0x08000014</span></span>                      |
| <span data-ttu-id="49dde-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49dde-249">Classes used in</span></span>        | [<span data-ttu-id="49dde-250">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="49dde-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="49dde-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="49dde-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="49dde-252">進入</span><span class="sxs-lookup"><span data-stu-id="49dde-252">Entry</span></span> | <span data-ttu-id="49dde-253">值</span><span class="sxs-lookup"><span data-stu-id="49dde-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="49dde-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49dde-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49dde-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="49dde-256">System-Only</span></span>            | <span data-ttu-id="49dde-257">否</span><span class="sxs-lookup"><span data-stu-id="49dde-257">False</span></span>                           |
| <span data-ttu-id="49dde-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49dde-258">Is-Single-Valued</span></span>       | <span data-ttu-id="49dde-259">對</span><span class="sxs-lookup"><span data-stu-id="49dde-259">True</span></span>                            |
| <span data-ttu-id="49dde-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49dde-260">Is Indexed</span></span>             | <span data-ttu-id="49dde-261">否</span><span class="sxs-lookup"><span data-stu-id="49dde-261">False</span></span>                           |
| <span data-ttu-id="49dde-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49dde-262">In Global Catalog</span></span>      | <span data-ttu-id="49dde-263">否</span><span class="sxs-lookup"><span data-stu-id="49dde-263">False</span></span>                           |
| <span data-ttu-id="49dde-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49dde-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="49dde-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49dde-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="49dde-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49dde-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="49dde-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49dde-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="49dde-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-268">Search-Flags</span></span>           | <span data-ttu-id="49dde-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49dde-269">0x00000000</span></span>                      |
| <span data-ttu-id="49dde-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-270">System-Flags</span></span>           | <span data-ttu-id="49dde-271">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49dde-271">0x08000014</span></span>                      |
| <span data-ttu-id="49dde-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49dde-272">Classes used in</span></span>        | [<span data-ttu-id="49dde-273">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="49dde-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="49dde-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49dde-274">Windows Server 2012</span></span>



| <span data-ttu-id="49dde-275">進入</span><span class="sxs-lookup"><span data-stu-id="49dde-275">Entry</span></span> | <span data-ttu-id="49dde-276">值</span><span class="sxs-lookup"><span data-stu-id="49dde-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="49dde-277">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49dde-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49dde-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="49dde-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="49dde-279">System-Only</span></span>            | <span data-ttu-id="49dde-280">否</span><span class="sxs-lookup"><span data-stu-id="49dde-280">False</span></span>                           |
| <span data-ttu-id="49dde-281">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49dde-281">Is-Single-Valued</span></span>       | <span data-ttu-id="49dde-282">對</span><span class="sxs-lookup"><span data-stu-id="49dde-282">True</span></span>                            |
| <span data-ttu-id="49dde-283">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49dde-283">Is Indexed</span></span>             | <span data-ttu-id="49dde-284">否</span><span class="sxs-lookup"><span data-stu-id="49dde-284">False</span></span>                           |
| <span data-ttu-id="49dde-285">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49dde-285">In Global Catalog</span></span>      | <span data-ttu-id="49dde-286">否</span><span class="sxs-lookup"><span data-stu-id="49dde-286">False</span></span>                           |
| <span data-ttu-id="49dde-287">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49dde-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="49dde-288">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49dde-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="49dde-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49dde-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="49dde-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49dde-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="49dde-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-291">Search-Flags</span></span>           | <span data-ttu-id="49dde-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49dde-292">0x00000000</span></span>                      |
| <span data-ttu-id="49dde-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49dde-293">System-Flags</span></span>           | <span data-ttu-id="49dde-294">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49dde-294">0x08000014</span></span>                      |
| <span data-ttu-id="49dde-295">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49dde-295">Classes used in</span></span>        | [<span data-ttu-id="49dde-296">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="49dde-296">**Top**</span></span>](c-top.md)<br/> |



 

 






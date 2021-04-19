---
title: ms DS-使用者-帳戶-控制項計算的屬性
description: 使用者帳戶-控制項計算很像 userAccountControl，但是屬性的值可能包含不會保存的額外位。
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- ms DS-使用者-帳戶-控制項計算的屬性 AD 架構
- 使用者帳戶-控制項計算的屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972898"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a><span data-ttu-id="e46d1-105">ms DS-使用者-帳戶-控制項計算的屬性</span><span class="sxs-lookup"><span data-stu-id="e46d1-105">ms-DS-User-Account-Control-Computed attribute</span></span>

<span data-ttu-id="e46d1-106">**使用者帳戶-控制項計算** 很像 [**userAccountControl**](a-useraccountcontrol.md)，但是屬性的值可能包含不會保存的額外位。</span><span class="sxs-lookup"><span data-stu-id="e46d1-106">**msDS-User-Account-Control-Computed** is much like [**userAccountControl**](a-useraccountcontrol.md), but the attribute's value can contain additional bits that are not persisted.</span></span> <span data-ttu-id="e46d1-107">計算的位包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="e46d1-107">The computed bits include the following.</span></span>



| <span data-ttu-id="e46d1-108">值</span><span class="sxs-lookup"><span data-stu-id="e46d1-108">Value</span></span>                | <span data-ttu-id="e46d1-109">Iads 中定義的名稱 () </span><span class="sxs-lookup"><span data-stu-id="e46d1-109">Name (defined in Iads.h)</span></span>                     |
|----------------------|----------------------------------------------|
| <span data-ttu-id="e46d1-110">0x0010</span><span class="sxs-lookup"><span data-stu-id="e46d1-110">0x0010</span></span><br/>    | <span data-ttu-id="e46d1-111">**UF \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="e46d1-111">**UF\_LOCKOUT**</span></span><br/>                   |
| <span data-ttu-id="e46d1-112">0x800000</span><span class="sxs-lookup"><span data-stu-id="e46d1-112">0x800000</span></span><br/>  | <span data-ttu-id="e46d1-113">**UF \_ 密碼已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="e46d1-113">**UF\_PASSWORD\_EXPIRED**</span></span><br/>         |
| <span data-ttu-id="e46d1-114">0x4000000</span><span class="sxs-lookup"><span data-stu-id="e46d1-114">0x4000000</span></span><br/> | <span data-ttu-id="e46d1-115">**UF \_ 部分 \_ 秘密 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="e46d1-115">**UF\_PARTIAL\_SECRETS\_ACCOUNT**</span></span><br/> |
| <span data-ttu-id="e46d1-116">0x8000000</span><span class="sxs-lookup"><span data-stu-id="e46d1-116">0x8000000</span></span><br/> | <span data-ttu-id="e46d1-117">**UF \_ 使用 \_ AES \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="e46d1-117">**UF\_USE\_AES\_KEYS**</span></span><br/>            |



 

<span data-ttu-id="e46d1-118">您可以在使用者 **帳戶控制** 參考頁面中 [**找到使用者帳戶控制項和使用者**](a-useraccountcontrol.md)帳戶控制 **計算** 的完整位清單， (對應到 [ [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset]) 或 [**使用者 \_ 資訊 \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008)結構的 [網路管理參考] 頁面。</span><span class="sxs-lookup"><span data-stu-id="e46d1-118">The full list of bits that [**User-Account-Control**](a-useraccountcontrol.md) and therefore **msDS-User-Account-Control-Computed** can also contain can be found in the **User-Account-Control** reference page (mapped through the [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset) or on the network management reference pages for the [**user\_info\_1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) structure.</span></span>



| <span data-ttu-id="e46d1-119">進入</span><span class="sxs-lookup"><span data-stu-id="e46d1-119">Entry</span></span> | <span data-ttu-id="e46d1-120">值</span><span class="sxs-lookup"><span data-stu-id="e46d1-120">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e46d1-121">CN</span><span class="sxs-lookup"><span data-stu-id="e46d1-121">CN</span></span>                | <span data-ttu-id="e46d1-122">ms-DS-使用者-帳戶-控制項計算</span><span class="sxs-lookup"><span data-stu-id="e46d1-122">ms-DS-User-Account-Control-Computed</span></span>  |
| <span data-ttu-id="e46d1-123">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e46d1-123">Ldap-Display-Name</span></span> | <span data-ttu-id="e46d1-124">使用者-帳戶-控制項計算</span><span class="sxs-lookup"><span data-stu-id="e46d1-124">msDS-User-Account-Control-Computed</span></span>   |
| <span data-ttu-id="e46d1-125">大小</span><span class="sxs-lookup"><span data-stu-id="e46d1-125">Size</span></span>              | \-                                   |
| <span data-ttu-id="e46d1-126">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e46d1-126">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e46d1-127">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e46d1-127">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e46d1-128">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e46d1-128">Attribute-Id</span></span>      | <span data-ttu-id="e46d1-129">1.2.840.113556.1.4.1460</span><span class="sxs-lookup"><span data-stu-id="e46d1-129">1.2.840.113556.1.4.1460</span></span>              |
| <span data-ttu-id="e46d1-130">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e46d1-130">System-Id-Guid</span></span>    | <span data-ttu-id="e46d1-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span><span class="sxs-lookup"><span data-stu-id="e46d1-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span></span> |
| <span data-ttu-id="e46d1-132">Syntax</span><span class="sxs-lookup"><span data-stu-id="e46d1-132">Syntax</span></span>            | [<span data-ttu-id="e46d1-133">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="e46d1-133">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e46d1-134">實作</span><span class="sxs-lookup"><span data-stu-id="e46d1-134">Implementations</span></span>

-   [<span data-ttu-id="e46d1-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e46d1-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e46d1-136">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e46d1-136">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e46d1-137">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e46d1-137">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e46d1-138">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e46d1-138">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e46d1-139">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e46d1-139">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e46d1-140">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e46d1-140">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e46d1-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e46d1-141">Windows Server 2003</span></span>



| <span data-ttu-id="e46d1-142">進入</span><span class="sxs-lookup"><span data-stu-id="e46d1-142">Entry</span></span> | <span data-ttu-id="e46d1-143">值</span><span class="sxs-lookup"><span data-stu-id="e46d1-143">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e46d1-144">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e46d1-144">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-145">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e46d1-145">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-146">System-Only</span><span class="sxs-lookup"><span data-stu-id="e46d1-146">System-Only</span></span>            | <span data-ttu-id="e46d1-147">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-147">False</span></span>                             |
| <span data-ttu-id="e46d1-148">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e46d1-148">Is-Single-Valued</span></span>       | <span data-ttu-id="e46d1-149">對</span><span class="sxs-lookup"><span data-stu-id="e46d1-149">True</span></span>                              |
| <span data-ttu-id="e46d1-150">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e46d1-150">Is Indexed</span></span>             | <span data-ttu-id="e46d1-151">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-151">False</span></span>                             |
| <span data-ttu-id="e46d1-152">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e46d1-152">In Global Catalog</span></span>      | <span data-ttu-id="e46d1-153">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-153">False</span></span>                             |
| <span data-ttu-id="e46d1-154">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e46d1-154">NT-Security-Descriptor</span></span> | <span data-ttu-id="e46d1-155">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e46d1-155">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e46d1-156">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e46d1-156">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e46d1-157">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e46d1-157">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e46d1-158">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-158">Search-Flags</span></span>           | <span data-ttu-id="e46d1-159">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e46d1-159">0x00000000</span></span>                        |
| <span data-ttu-id="e46d1-160">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-160">System-Flags</span></span>           | <span data-ttu-id="e46d1-161">0x00000014</span><span class="sxs-lookup"><span data-stu-id="e46d1-161">0x00000014</span></span>                        |
| <span data-ttu-id="e46d1-162">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e46d1-162">Classes used in</span></span>        | [<span data-ttu-id="e46d1-163">**User**</span><span class="sxs-lookup"><span data-stu-id="e46d1-163">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e46d1-164">亞當</span><span class="sxs-lookup"><span data-stu-id="e46d1-164">ADAM</span></span>



| <span data-ttu-id="e46d1-165">進入</span><span class="sxs-lookup"><span data-stu-id="e46d1-165">Entry</span></span> | <span data-ttu-id="e46d1-166">值</span><span class="sxs-lookup"><span data-stu-id="e46d1-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e46d1-167">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e46d1-167">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e46d1-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e46d1-168">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e46d1-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="e46d1-169">System-Only</span></span>            | <span data-ttu-id="e46d1-170">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-170">False</span></span>                                                             |
| <span data-ttu-id="e46d1-171">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e46d1-171">Is-Single-Valued</span></span>       | <span data-ttu-id="e46d1-172">對</span><span class="sxs-lookup"><span data-stu-id="e46d1-172">True</span></span>                                                              |
| <span data-ttu-id="e46d1-173">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e46d1-173">Is Indexed</span></span>             | <span data-ttu-id="e46d1-174">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-174">False</span></span>                                                             |
| <span data-ttu-id="e46d1-175">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e46d1-175">In Global Catalog</span></span>      | <span data-ttu-id="e46d1-176">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-176">False</span></span>                                                             |
| <span data-ttu-id="e46d1-177">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e46d1-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="e46d1-178">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e46d1-178">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e46d1-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e46d1-179">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="e46d1-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e46d1-180">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="e46d1-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-181">Search-Flags</span></span>           | <span data-ttu-id="e46d1-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e46d1-182">0x00000000</span></span>                                                        |
| <span data-ttu-id="e46d1-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-183">System-Flags</span></span>           | <span data-ttu-id="e46d1-184">0x00000014</span><span class="sxs-lookup"><span data-stu-id="e46d1-184">0x00000014</span></span>                                                        |
| <span data-ttu-id="e46d1-185">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e46d1-185">Classes used in</span></span>        | [<span data-ttu-id="e46d1-186">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="e46d1-186">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e46d1-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e46d1-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e46d1-188">進入</span><span class="sxs-lookup"><span data-stu-id="e46d1-188">Entry</span></span> | <span data-ttu-id="e46d1-189">值</span><span class="sxs-lookup"><span data-stu-id="e46d1-189">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e46d1-190">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e46d1-190">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e46d1-191">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="e46d1-192">System-Only</span></span>            | <span data-ttu-id="e46d1-193">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-193">False</span></span>                             |
| <span data-ttu-id="e46d1-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e46d1-194">Is-Single-Valued</span></span>       | <span data-ttu-id="e46d1-195">對</span><span class="sxs-lookup"><span data-stu-id="e46d1-195">True</span></span>                              |
| <span data-ttu-id="e46d1-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e46d1-196">Is Indexed</span></span>             | <span data-ttu-id="e46d1-197">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-197">False</span></span>                             |
| <span data-ttu-id="e46d1-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e46d1-198">In Global Catalog</span></span>      | <span data-ttu-id="e46d1-199">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-199">False</span></span>                             |
| <span data-ttu-id="e46d1-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e46d1-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="e46d1-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e46d1-201">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e46d1-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e46d1-202">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e46d1-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e46d1-203">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e46d1-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-204">Search-Flags</span></span>           | <span data-ttu-id="e46d1-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e46d1-205">0x00000000</span></span>                        |
| <span data-ttu-id="e46d1-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-206">System-Flags</span></span>           | <span data-ttu-id="e46d1-207">0x00000014</span><span class="sxs-lookup"><span data-stu-id="e46d1-207">0x00000014</span></span>                        |
| <span data-ttu-id="e46d1-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e46d1-208">Classes used in</span></span>        | [<span data-ttu-id="e46d1-209">**User**</span><span class="sxs-lookup"><span data-stu-id="e46d1-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e46d1-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e46d1-210">Windows Server 2008</span></span>



| <span data-ttu-id="e46d1-211">進入</span><span class="sxs-lookup"><span data-stu-id="e46d1-211">Entry</span></span> | <span data-ttu-id="e46d1-212">值</span><span class="sxs-lookup"><span data-stu-id="e46d1-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e46d1-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e46d1-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e46d1-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="e46d1-215">System-Only</span></span>            | <span data-ttu-id="e46d1-216">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-216">False</span></span>                             |
| <span data-ttu-id="e46d1-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e46d1-217">Is-Single-Valued</span></span>       | <span data-ttu-id="e46d1-218">對</span><span class="sxs-lookup"><span data-stu-id="e46d1-218">True</span></span>                              |
| <span data-ttu-id="e46d1-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e46d1-219">Is Indexed</span></span>             | <span data-ttu-id="e46d1-220">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-220">False</span></span>                             |
| <span data-ttu-id="e46d1-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e46d1-221">In Global Catalog</span></span>      | <span data-ttu-id="e46d1-222">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-222">False</span></span>                             |
| <span data-ttu-id="e46d1-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e46d1-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="e46d1-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e46d1-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e46d1-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e46d1-225">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e46d1-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e46d1-226">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e46d1-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-227">Search-Flags</span></span>           | <span data-ttu-id="e46d1-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e46d1-228">0x00000000</span></span>                        |
| <span data-ttu-id="e46d1-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-229">System-Flags</span></span>           | <span data-ttu-id="e46d1-230">0x00000014</span><span class="sxs-lookup"><span data-stu-id="e46d1-230">0x00000014</span></span>                        |
| <span data-ttu-id="e46d1-231">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e46d1-231">Classes used in</span></span>        | [<span data-ttu-id="e46d1-232">**User**</span><span class="sxs-lookup"><span data-stu-id="e46d1-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e46d1-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e46d1-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e46d1-234">進入</span><span class="sxs-lookup"><span data-stu-id="e46d1-234">Entry</span></span> | <span data-ttu-id="e46d1-235">值</span><span class="sxs-lookup"><span data-stu-id="e46d1-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e46d1-236">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e46d1-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e46d1-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="e46d1-238">System-Only</span></span>            | <span data-ttu-id="e46d1-239">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-239">False</span></span>                             |
| <span data-ttu-id="e46d1-240">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e46d1-240">Is-Single-Valued</span></span>       | <span data-ttu-id="e46d1-241">對</span><span class="sxs-lookup"><span data-stu-id="e46d1-241">True</span></span>                              |
| <span data-ttu-id="e46d1-242">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e46d1-242">Is Indexed</span></span>             | <span data-ttu-id="e46d1-243">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-243">False</span></span>                             |
| <span data-ttu-id="e46d1-244">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e46d1-244">In Global Catalog</span></span>      | <span data-ttu-id="e46d1-245">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-245">False</span></span>                             |
| <span data-ttu-id="e46d1-246">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e46d1-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="e46d1-247">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e46d1-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e46d1-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e46d1-248">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e46d1-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e46d1-249">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e46d1-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-250">Search-Flags</span></span>           | <span data-ttu-id="e46d1-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e46d1-251">0x00000000</span></span>                        |
| <span data-ttu-id="e46d1-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-252">System-Flags</span></span>           | <span data-ttu-id="e46d1-253">0x00000014</span><span class="sxs-lookup"><span data-stu-id="e46d1-253">0x00000014</span></span>                        |
| <span data-ttu-id="e46d1-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e46d1-254">Classes used in</span></span>        | [<span data-ttu-id="e46d1-255">**User**</span><span class="sxs-lookup"><span data-stu-id="e46d1-255">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e46d1-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e46d1-256">Windows Server 2012</span></span>



| <span data-ttu-id="e46d1-257">進入</span><span class="sxs-lookup"><span data-stu-id="e46d1-257">Entry</span></span> | <span data-ttu-id="e46d1-258">值</span><span class="sxs-lookup"><span data-stu-id="e46d1-258">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e46d1-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e46d1-259">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e46d1-260">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e46d1-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="e46d1-261">System-Only</span></span>            | <span data-ttu-id="e46d1-262">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-262">False</span></span>                             |
| <span data-ttu-id="e46d1-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e46d1-263">Is-Single-Valued</span></span>       | <span data-ttu-id="e46d1-264">對</span><span class="sxs-lookup"><span data-stu-id="e46d1-264">True</span></span>                              |
| <span data-ttu-id="e46d1-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e46d1-265">Is Indexed</span></span>             | <span data-ttu-id="e46d1-266">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-266">False</span></span>                             |
| <span data-ttu-id="e46d1-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e46d1-267">In Global Catalog</span></span>      | <span data-ttu-id="e46d1-268">否</span><span class="sxs-lookup"><span data-stu-id="e46d1-268">False</span></span>                             |
| <span data-ttu-id="e46d1-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e46d1-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="e46d1-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e46d1-270">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e46d1-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e46d1-271">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e46d1-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e46d1-272">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e46d1-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-273">Search-Flags</span></span>           | <span data-ttu-id="e46d1-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e46d1-274">0x00000000</span></span>                        |
| <span data-ttu-id="e46d1-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e46d1-275">System-Flags</span></span>           | <span data-ttu-id="e46d1-276">0x00000014</span><span class="sxs-lookup"><span data-stu-id="e46d1-276">0x00000014</span></span>                        |
| <span data-ttu-id="e46d1-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e46d1-277">Classes used in</span></span>        | [<span data-ttu-id="e46d1-278">**User**</span><span class="sxs-lookup"><span data-stu-id="e46d1-278">**User**</span></span>](c-user.md)<br/> |



 


---
title: ACS-Identity-Name 屬性
description: 此屬性包含使用者或 OU 的 DN，而且是此 QoS 原則所套用的使用者或使用者群組的身分識別。
ms.assetid: 00e6e2bd-aec8-426f-b89e-0661c15cfd46
ms.tgt_platform: multiple
keywords:
- ACS-身分識別名稱屬性 AD 架構
- aCSIdentityName 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Identity-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33ef1db92b908ef8474dfb125aca678d3c22d09f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108316"
---
# <a name="acs-identity-name-attribute"></a><span data-ttu-id="d1789-105">ACS-Identity-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="d1789-105">ACS-Identity-Name attribute</span></span>

<span data-ttu-id="d1789-106">此屬性包含使用者或 OU 的 DN，而且是此 QoS 原則所套用的使用者或使用者群組的身分識別。</span><span class="sxs-lookup"><span data-stu-id="d1789-106">This attribute contains the DN of a user or OU and is the identity of a user or a group of users to which this QoS policy applies.</span></span>



| <span data-ttu-id="d1789-107">進入</span><span class="sxs-lookup"><span data-stu-id="d1789-107">Entry</span></span> | <span data-ttu-id="d1789-108">值</span><span class="sxs-lookup"><span data-stu-id="d1789-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d1789-109">CN</span><span class="sxs-lookup"><span data-stu-id="d1789-109">CN</span></span>                | <span data-ttu-id="d1789-110">ACS-身分識別名稱</span><span class="sxs-lookup"><span data-stu-id="d1789-110">ACS-Identity-Name</span></span>                           |
| <span data-ttu-id="d1789-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d1789-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d1789-112">aCSIdentityName</span><span class="sxs-lookup"><span data-stu-id="d1789-112">aCSIdentityName</span></span>                             |
| <span data-ttu-id="d1789-113">大小</span><span class="sxs-lookup"><span data-stu-id="d1789-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="d1789-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d1789-114">Update Privilege</span></span>  | <span data-ttu-id="d1789-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="d1789-115">Domain administrator</span></span>                        |
| <span data-ttu-id="d1789-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d1789-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d1789-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d1789-117">Attribute-Id</span></span>      | <span data-ttu-id="d1789-118">1.2.840.113556.1.4.784</span><span class="sxs-lookup"><span data-stu-id="d1789-118">1.2.840.113556.1.4.784</span></span>                      |
| <span data-ttu-id="d1789-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d1789-119">System-Id-Guid</span></span>    | <span data-ttu-id="d1789-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="d1789-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span></span>        |
| <span data-ttu-id="d1789-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1789-121">Syntax</span></span>            | [<span data-ttu-id="d1789-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d1789-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d1789-123">實作</span><span class="sxs-lookup"><span data-stu-id="d1789-123">Implementations</span></span>

-   [<span data-ttu-id="d1789-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d1789-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d1789-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d1789-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d1789-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d1789-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d1789-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d1789-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d1789-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d1789-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d1789-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d1789-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d1789-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1789-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d1789-131">進入</span><span class="sxs-lookup"><span data-stu-id="d1789-131">Entry</span></span> | <span data-ttu-id="d1789-132">值</span><span class="sxs-lookup"><span data-stu-id="d1789-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d1789-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d1789-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1789-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1789-135">System-Only</span></span>            | <span data-ttu-id="d1789-136">否</span><span class="sxs-lookup"><span data-stu-id="d1789-136">False</span></span>                                        |
| <span data-ttu-id="d1789-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d1789-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d1789-138">否</span><span class="sxs-lookup"><span data-stu-id="d1789-138">False</span></span>                                        |
| <span data-ttu-id="d1789-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d1789-139">Is Indexed</span></span>             | <span data-ttu-id="d1789-140">否</span><span class="sxs-lookup"><span data-stu-id="d1789-140">False</span></span>                                        |
| <span data-ttu-id="d1789-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d1789-141">In Global Catalog</span></span>      | <span data-ttu-id="d1789-142">否</span><span class="sxs-lookup"><span data-stu-id="d1789-142">False</span></span>                                        |
| <span data-ttu-id="d1789-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d1789-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1789-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d1789-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d1789-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1789-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d1789-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1789-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d1789-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-147">Search-Flags</span></span>           | <span data-ttu-id="d1789-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1789-148">0x00000000</span></span>                                   |
| <span data-ttu-id="d1789-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-149">System-Flags</span></span>           | <span data-ttu-id="d1789-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1789-150">0x00000010</span></span>                                   |
| <span data-ttu-id="d1789-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d1789-151">Classes used in</span></span>        | [<span data-ttu-id="d1789-152">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="d1789-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d1789-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1789-153">Windows Server 2003</span></span>



| <span data-ttu-id="d1789-154">進入</span><span class="sxs-lookup"><span data-stu-id="d1789-154">Entry</span></span> | <span data-ttu-id="d1789-155">值</span><span class="sxs-lookup"><span data-stu-id="d1789-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d1789-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d1789-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1789-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1789-158">System-Only</span></span>            | <span data-ttu-id="d1789-159">否</span><span class="sxs-lookup"><span data-stu-id="d1789-159">False</span></span>                                        |
| <span data-ttu-id="d1789-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d1789-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d1789-161">否</span><span class="sxs-lookup"><span data-stu-id="d1789-161">False</span></span>                                        |
| <span data-ttu-id="d1789-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d1789-162">Is Indexed</span></span>             | <span data-ttu-id="d1789-163">否</span><span class="sxs-lookup"><span data-stu-id="d1789-163">False</span></span>                                        |
| <span data-ttu-id="d1789-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d1789-164">In Global Catalog</span></span>      | <span data-ttu-id="d1789-165">否</span><span class="sxs-lookup"><span data-stu-id="d1789-165">False</span></span>                                        |
| <span data-ttu-id="d1789-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d1789-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1789-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d1789-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d1789-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1789-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d1789-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1789-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d1789-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-170">Search-Flags</span></span>           | <span data-ttu-id="d1789-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1789-171">0x00000000</span></span>                                   |
| <span data-ttu-id="d1789-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-172">System-Flags</span></span>           | <span data-ttu-id="d1789-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1789-173">0x00000010</span></span>                                   |
| <span data-ttu-id="d1789-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d1789-174">Classes used in</span></span>        | [<span data-ttu-id="d1789-175">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="d1789-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d1789-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d1789-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d1789-177">進入</span><span class="sxs-lookup"><span data-stu-id="d1789-177">Entry</span></span> | <span data-ttu-id="d1789-178">值</span><span class="sxs-lookup"><span data-stu-id="d1789-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d1789-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d1789-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1789-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1789-181">System-Only</span></span>            | <span data-ttu-id="d1789-182">否</span><span class="sxs-lookup"><span data-stu-id="d1789-182">False</span></span>                                        |
| <span data-ttu-id="d1789-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d1789-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d1789-184">否</span><span class="sxs-lookup"><span data-stu-id="d1789-184">False</span></span>                                        |
| <span data-ttu-id="d1789-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d1789-185">Is Indexed</span></span>             | <span data-ttu-id="d1789-186">否</span><span class="sxs-lookup"><span data-stu-id="d1789-186">False</span></span>                                        |
| <span data-ttu-id="d1789-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d1789-187">In Global Catalog</span></span>      | <span data-ttu-id="d1789-188">否</span><span class="sxs-lookup"><span data-stu-id="d1789-188">False</span></span>                                        |
| <span data-ttu-id="d1789-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d1789-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1789-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d1789-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d1789-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1789-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d1789-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1789-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d1789-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-193">Search-Flags</span></span>           | <span data-ttu-id="d1789-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1789-194">0x00000000</span></span>                                   |
| <span data-ttu-id="d1789-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-195">System-Flags</span></span>           | <span data-ttu-id="d1789-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1789-196">0x00000010</span></span>                                   |
| <span data-ttu-id="d1789-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d1789-197">Classes used in</span></span>        | [<span data-ttu-id="d1789-198">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="d1789-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d1789-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1789-199">Windows Server 2008</span></span>



| <span data-ttu-id="d1789-200">進入</span><span class="sxs-lookup"><span data-stu-id="d1789-200">Entry</span></span> | <span data-ttu-id="d1789-201">值</span><span class="sxs-lookup"><span data-stu-id="d1789-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d1789-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d1789-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1789-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1789-204">System-Only</span></span>            | <span data-ttu-id="d1789-205">否</span><span class="sxs-lookup"><span data-stu-id="d1789-205">False</span></span>                                        |
| <span data-ttu-id="d1789-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d1789-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d1789-207">否</span><span class="sxs-lookup"><span data-stu-id="d1789-207">False</span></span>                                        |
| <span data-ttu-id="d1789-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d1789-208">Is Indexed</span></span>             | <span data-ttu-id="d1789-209">否</span><span class="sxs-lookup"><span data-stu-id="d1789-209">False</span></span>                                        |
| <span data-ttu-id="d1789-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d1789-210">In Global Catalog</span></span>      | <span data-ttu-id="d1789-211">否</span><span class="sxs-lookup"><span data-stu-id="d1789-211">False</span></span>                                        |
| <span data-ttu-id="d1789-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d1789-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1789-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d1789-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d1789-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1789-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d1789-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1789-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d1789-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-216">Search-Flags</span></span>           | <span data-ttu-id="d1789-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1789-217">0x00000000</span></span>                                   |
| <span data-ttu-id="d1789-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-218">System-Flags</span></span>           | <span data-ttu-id="d1789-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1789-219">0x00000010</span></span>                                   |
| <span data-ttu-id="d1789-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d1789-220">Classes used in</span></span>        | [<span data-ttu-id="d1789-221">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="d1789-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d1789-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d1789-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d1789-223">進入</span><span class="sxs-lookup"><span data-stu-id="d1789-223">Entry</span></span> | <span data-ttu-id="d1789-224">值</span><span class="sxs-lookup"><span data-stu-id="d1789-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d1789-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d1789-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1789-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1789-227">System-Only</span></span>            | <span data-ttu-id="d1789-228">否</span><span class="sxs-lookup"><span data-stu-id="d1789-228">False</span></span>                                        |
| <span data-ttu-id="d1789-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d1789-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d1789-230">否</span><span class="sxs-lookup"><span data-stu-id="d1789-230">False</span></span>                                        |
| <span data-ttu-id="d1789-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d1789-231">Is Indexed</span></span>             | <span data-ttu-id="d1789-232">否</span><span class="sxs-lookup"><span data-stu-id="d1789-232">False</span></span>                                        |
| <span data-ttu-id="d1789-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d1789-233">In Global Catalog</span></span>      | <span data-ttu-id="d1789-234">否</span><span class="sxs-lookup"><span data-stu-id="d1789-234">False</span></span>                                        |
| <span data-ttu-id="d1789-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d1789-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1789-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d1789-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d1789-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1789-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d1789-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1789-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d1789-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-239">Search-Flags</span></span>           | <span data-ttu-id="d1789-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1789-240">0x00000000</span></span>                                   |
| <span data-ttu-id="d1789-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-241">System-Flags</span></span>           | <span data-ttu-id="d1789-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1789-242">0x00000010</span></span>                                   |
| <span data-ttu-id="d1789-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d1789-243">Classes used in</span></span>        | [<span data-ttu-id="d1789-244">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="d1789-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d1789-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1789-245">Windows Server 2012</span></span>



| <span data-ttu-id="d1789-246">進入</span><span class="sxs-lookup"><span data-stu-id="d1789-246">Entry</span></span> | <span data-ttu-id="d1789-247">值</span><span class="sxs-lookup"><span data-stu-id="d1789-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d1789-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d1789-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1789-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d1789-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1789-250">System-Only</span></span>            | <span data-ttu-id="d1789-251">否</span><span class="sxs-lookup"><span data-stu-id="d1789-251">False</span></span>                                        |
| <span data-ttu-id="d1789-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d1789-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d1789-253">否</span><span class="sxs-lookup"><span data-stu-id="d1789-253">False</span></span>                                        |
| <span data-ttu-id="d1789-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d1789-254">Is Indexed</span></span>             | <span data-ttu-id="d1789-255">否</span><span class="sxs-lookup"><span data-stu-id="d1789-255">False</span></span>                                        |
| <span data-ttu-id="d1789-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d1789-256">In Global Catalog</span></span>      | <span data-ttu-id="d1789-257">否</span><span class="sxs-lookup"><span data-stu-id="d1789-257">False</span></span>                                        |
| <span data-ttu-id="d1789-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d1789-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1789-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d1789-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d1789-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1789-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d1789-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1789-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d1789-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-262">Search-Flags</span></span>           | <span data-ttu-id="d1789-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1789-263">0x00000000</span></span>                                   |
| <span data-ttu-id="d1789-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1789-264">System-Flags</span></span>           | <span data-ttu-id="d1789-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1789-265">0x00000010</span></span>                                   |
| <span data-ttu-id="d1789-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d1789-266">Classes used in</span></span>        | [<span data-ttu-id="d1789-267">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="d1789-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






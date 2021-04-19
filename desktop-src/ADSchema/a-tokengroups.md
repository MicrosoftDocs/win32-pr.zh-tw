---
title: Token-Groups 屬性
description: 包含 Sid 清單的計算屬性，此屬性是由指定使用者或電腦上的可轉移群組成員資格擴充作業所造成。 如果沒有任何通用類別目錄可取得可轉移的反向成員資格，則無法抓取權杖群組。
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Token-Groups 屬性 AD 架構
- tokenGroups 屬性 AD 架構
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5342d1ff2bf549796340532b0514d5c5b060c2c1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970044"
---
# <a name="token-groups-attribute"></a><span data-ttu-id="a72a1-106">Token-Groups 屬性</span><span class="sxs-lookup"><span data-stu-id="a72a1-106">Token-Groups attribute</span></span>

<span data-ttu-id="a72a1-107">包含 Sid 清單的計算屬性，此屬性是由指定使用者或電腦上的可轉移群組成員資格擴充作業所造成。</span><span class="sxs-lookup"><span data-stu-id="a72a1-107">A computed attribute that contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="a72a1-108">如果沒有任何通用類別目錄可取得可轉移的反向成員資格，則無法抓取權杖群組。</span><span class="sxs-lookup"><span data-stu-id="a72a1-108">Token Groups cannot be retrieved if no Global Catalog is present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="a72a1-109">進入</span><span class="sxs-lookup"><span data-stu-id="a72a1-109">Entry</span></span> | <span data-ttu-id="a72a1-110">值</span><span class="sxs-lookup"><span data-stu-id="a72a1-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a72a1-111">CN</span><span class="sxs-lookup"><span data-stu-id="a72a1-111">CN</span></span>                | <span data-ttu-id="a72a1-112">Token-Groups</span><span class="sxs-lookup"><span data-stu-id="a72a1-112">Token-Groups</span></span>                         |
| <span data-ttu-id="a72a1-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a72a1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a72a1-114">tokenGroups</span><span class="sxs-lookup"><span data-stu-id="a72a1-114">tokenGroups</span></span>                          |
| <span data-ttu-id="a72a1-115">大小</span><span class="sxs-lookup"><span data-stu-id="a72a1-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="a72a1-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a72a1-116">Update Privilege</span></span>  | <span data-ttu-id="a72a1-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="a72a1-117">This value is set by the system.</span></span>     |
| <span data-ttu-id="a72a1-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a72a1-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a72a1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a72a1-119">Attribute-Id</span></span>      | <span data-ttu-id="a72a1-120">1.2.840.113556.1.4.1301</span><span class="sxs-lookup"><span data-stu-id="a72a1-120">1.2.840.113556.1.4.1301</span></span>              |
| <span data-ttu-id="a72a1-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a72a1-121">System-Id-Guid</span></span>    | <span data-ttu-id="a72a1-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="a72a1-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="a72a1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a72a1-123">Syntax</span></span>            | [<span data-ttu-id="a72a1-124">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="a72a1-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="a72a1-125">實作</span><span class="sxs-lookup"><span data-stu-id="a72a1-125">Implementations</span></span>

-   [<span data-ttu-id="a72a1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a72a1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a72a1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a72a1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a72a1-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a72a1-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a72a1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a72a1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a72a1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a72a1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a72a1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a72a1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a72a1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a72a1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a72a1-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a72a1-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a72a1-134">進入</span><span class="sxs-lookup"><span data-stu-id="a72a1-134">Entry</span></span> | <span data-ttu-id="a72a1-135">值</span><span class="sxs-lookup"><span data-stu-id="a72a1-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a72a1-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a72a1-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72a1-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72a1-138">System-Only</span></span>            | <span data-ttu-id="a72a1-139">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-139">False</span></span>                                                        |
| <span data-ttu-id="a72a1-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a72a1-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a72a1-141">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-141">False</span></span>                                                        |
| <span data-ttu-id="a72a1-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a72a1-142">Is Indexed</span></span>             | <span data-ttu-id="a72a1-143">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-143">False</span></span>                                                        |
| <span data-ttu-id="a72a1-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a72a1-144">In Global Catalog</span></span>      | <span data-ttu-id="a72a1-145">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-145">False</span></span>                                                        |
| <span data-ttu-id="a72a1-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a72a1-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72a1-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a72a1-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a72a1-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72a1-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72a1-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-150">Search-Flags</span></span>           | <span data-ttu-id="a72a1-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72a1-151">0x00000000</span></span>                                                   |
| <span data-ttu-id="a72a1-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-152">System-Flags</span></span>           | <span data-ttu-id="a72a1-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a72a1-153">0x08000014</span></span>                                                   |
| <span data-ttu-id="a72a1-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a72a1-154">Classes used in</span></span>        | [<span data-ttu-id="a72a1-155">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a72a1-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a72a1-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a72a1-156">Windows Server 2003</span></span>



| <span data-ttu-id="a72a1-157">進入</span><span class="sxs-lookup"><span data-stu-id="a72a1-157">Entry</span></span> | <span data-ttu-id="a72a1-158">值</span><span class="sxs-lookup"><span data-stu-id="a72a1-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a72a1-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a72a1-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72a1-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72a1-161">System-Only</span></span>            | <span data-ttu-id="a72a1-162">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-162">False</span></span>                                                        |
| <span data-ttu-id="a72a1-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a72a1-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a72a1-164">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-164">False</span></span>                                                        |
| <span data-ttu-id="a72a1-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a72a1-165">Is Indexed</span></span>             | <span data-ttu-id="a72a1-166">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-166">False</span></span>                                                        |
| <span data-ttu-id="a72a1-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a72a1-167">In Global Catalog</span></span>      | <span data-ttu-id="a72a1-168">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-168">False</span></span>                                                        |
| <span data-ttu-id="a72a1-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a72a1-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72a1-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a72a1-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a72a1-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72a1-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72a1-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-173">Search-Flags</span></span>           | <span data-ttu-id="a72a1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72a1-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="a72a1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-175">System-Flags</span></span>           | <span data-ttu-id="a72a1-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a72a1-176">0x08000014</span></span>                                                   |
| <span data-ttu-id="a72a1-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a72a1-177">Classes used in</span></span>        | [<span data-ttu-id="a72a1-178">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a72a1-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a72a1-179">亞當</span><span class="sxs-lookup"><span data-stu-id="a72a1-179">ADAM</span></span>



| <span data-ttu-id="a72a1-180">進入</span><span class="sxs-lookup"><span data-stu-id="a72a1-180">Entry</span></span> | <span data-ttu-id="a72a1-181">值</span><span class="sxs-lookup"><span data-stu-id="a72a1-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a72a1-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a72a1-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72a1-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72a1-184">System-Only</span></span>            | <span data-ttu-id="a72a1-185">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-185">False</span></span>                                                        |
| <span data-ttu-id="a72a1-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a72a1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a72a1-187">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-187">False</span></span>                                                        |
| <span data-ttu-id="a72a1-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a72a1-188">Is Indexed</span></span>             | <span data-ttu-id="a72a1-189">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-189">False</span></span>                                                        |
| <span data-ttu-id="a72a1-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a72a1-190">In Global Catalog</span></span>      | <span data-ttu-id="a72a1-191">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-191">False</span></span>                                                        |
| <span data-ttu-id="a72a1-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a72a1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72a1-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a72a1-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a72a1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72a1-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72a1-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-196">Search-Flags</span></span>           | <span data-ttu-id="a72a1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72a1-197">0x00000000</span></span>                                                   |
| <span data-ttu-id="a72a1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-198">System-Flags</span></span>           | <span data-ttu-id="a72a1-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a72a1-199">0x08000014</span></span>                                                   |
| <span data-ttu-id="a72a1-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a72a1-200">Classes used in</span></span>        | [<span data-ttu-id="a72a1-201">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a72a1-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a72a1-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a72a1-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a72a1-203">進入</span><span class="sxs-lookup"><span data-stu-id="a72a1-203">Entry</span></span> | <span data-ttu-id="a72a1-204">值</span><span class="sxs-lookup"><span data-stu-id="a72a1-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a72a1-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a72a1-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72a1-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72a1-207">System-Only</span></span>            | <span data-ttu-id="a72a1-208">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-208">False</span></span>                                                        |
| <span data-ttu-id="a72a1-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a72a1-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a72a1-210">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-210">False</span></span>                                                        |
| <span data-ttu-id="a72a1-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a72a1-211">Is Indexed</span></span>             | <span data-ttu-id="a72a1-212">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-212">False</span></span>                                                        |
| <span data-ttu-id="a72a1-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a72a1-213">In Global Catalog</span></span>      | <span data-ttu-id="a72a1-214">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-214">False</span></span>                                                        |
| <span data-ttu-id="a72a1-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a72a1-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72a1-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a72a1-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a72a1-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72a1-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72a1-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-219">Search-Flags</span></span>           | <span data-ttu-id="a72a1-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72a1-220">0x00000000</span></span>                                                   |
| <span data-ttu-id="a72a1-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-221">System-Flags</span></span>           | <span data-ttu-id="a72a1-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a72a1-222">0x08000014</span></span>                                                   |
| <span data-ttu-id="a72a1-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a72a1-223">Classes used in</span></span>        | [<span data-ttu-id="a72a1-224">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a72a1-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a72a1-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a72a1-225">Windows Server 2008</span></span>



| <span data-ttu-id="a72a1-226">進入</span><span class="sxs-lookup"><span data-stu-id="a72a1-226">Entry</span></span> | <span data-ttu-id="a72a1-227">值</span><span class="sxs-lookup"><span data-stu-id="a72a1-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a72a1-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a72a1-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72a1-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72a1-230">System-Only</span></span>            | <span data-ttu-id="a72a1-231">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-231">False</span></span>                                                        |
| <span data-ttu-id="a72a1-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a72a1-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a72a1-233">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-233">False</span></span>                                                        |
| <span data-ttu-id="a72a1-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a72a1-234">Is Indexed</span></span>             | <span data-ttu-id="a72a1-235">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-235">False</span></span>                                                        |
| <span data-ttu-id="a72a1-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a72a1-236">In Global Catalog</span></span>      | <span data-ttu-id="a72a1-237">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-237">False</span></span>                                                        |
| <span data-ttu-id="a72a1-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a72a1-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72a1-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a72a1-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a72a1-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72a1-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72a1-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-242">Search-Flags</span></span>           | <span data-ttu-id="a72a1-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72a1-243">0x00000000</span></span>                                                   |
| <span data-ttu-id="a72a1-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-244">System-Flags</span></span>           | <span data-ttu-id="a72a1-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a72a1-245">0x08000014</span></span>                                                   |
| <span data-ttu-id="a72a1-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a72a1-246">Classes used in</span></span>        | [<span data-ttu-id="a72a1-247">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a72a1-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a72a1-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a72a1-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a72a1-249">進入</span><span class="sxs-lookup"><span data-stu-id="a72a1-249">Entry</span></span> | <span data-ttu-id="a72a1-250">值</span><span class="sxs-lookup"><span data-stu-id="a72a1-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a72a1-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a72a1-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72a1-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72a1-253">System-Only</span></span>            | <span data-ttu-id="a72a1-254">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-254">False</span></span>                                                        |
| <span data-ttu-id="a72a1-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a72a1-255">Is-Single-Valued</span></span>       | <span data-ttu-id="a72a1-256">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-256">False</span></span>                                                        |
| <span data-ttu-id="a72a1-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a72a1-257">Is Indexed</span></span>             | <span data-ttu-id="a72a1-258">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-258">False</span></span>                                                        |
| <span data-ttu-id="a72a1-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a72a1-259">In Global Catalog</span></span>      | <span data-ttu-id="a72a1-260">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-260">False</span></span>                                                        |
| <span data-ttu-id="a72a1-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a72a1-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72a1-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a72a1-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a72a1-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72a1-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72a1-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-265">Search-Flags</span></span>           | <span data-ttu-id="a72a1-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72a1-266">0x00000000</span></span>                                                   |
| <span data-ttu-id="a72a1-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-267">System-Flags</span></span>           | <span data-ttu-id="a72a1-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a72a1-268">0x08000014</span></span>                                                   |
| <span data-ttu-id="a72a1-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a72a1-269">Classes used in</span></span>        | [<span data-ttu-id="a72a1-270">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a72a1-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a72a1-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a72a1-271">Windows Server 2012</span></span>



| <span data-ttu-id="a72a1-272">進入</span><span class="sxs-lookup"><span data-stu-id="a72a1-272">Entry</span></span> | <span data-ttu-id="a72a1-273">值</span><span class="sxs-lookup"><span data-stu-id="a72a1-273">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a72a1-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a72a1-274">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72a1-275">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a72a1-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72a1-276">System-Only</span></span>            | <span data-ttu-id="a72a1-277">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-277">False</span></span>                                                        |
| <span data-ttu-id="a72a1-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a72a1-278">Is-Single-Valued</span></span>       | <span data-ttu-id="a72a1-279">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-279">False</span></span>                                                        |
| <span data-ttu-id="a72a1-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a72a1-280">Is Indexed</span></span>             | <span data-ttu-id="a72a1-281">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-281">False</span></span>                                                        |
| <span data-ttu-id="a72a1-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a72a1-282">In Global Catalog</span></span>      | <span data-ttu-id="a72a1-283">否</span><span class="sxs-lookup"><span data-stu-id="a72a1-283">False</span></span>                                                        |
| <span data-ttu-id="a72a1-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a72a1-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72a1-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a72a1-285">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a72a1-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72a1-286">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72a1-287">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a72a1-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-288">Search-Flags</span></span>           | <span data-ttu-id="a72a1-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72a1-289">0x00000000</span></span>                                                   |
| <span data-ttu-id="a72a1-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72a1-290">System-Flags</span></span>           | <span data-ttu-id="a72a1-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a72a1-291">0x08000014</span></span>                                                   |
| <span data-ttu-id="a72a1-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a72a1-292">Classes used in</span></span>        | [<span data-ttu-id="a72a1-293">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a72a1-293">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 






---
title: MS DS-電腦-帳戶-配額屬性
description: 允許使用者在網域中建立的電腦帳戶數目。
ms.assetid: bcfc6a9c-b891-48c2-9c42-8154345caf08
ms.tgt_platform: multiple
keywords:
- MS DS-電腦-帳戶-配額屬性 AD 架構
- MachineAccountQuota 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-Machine-Account-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86de012aa876e5a0d52ac866048801872a365f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107873"
---
# <a name="ms-ds-machine-account-quota-attribute"></a><span data-ttu-id="5798f-105">MS DS-電腦-帳戶-配額屬性</span><span class="sxs-lookup"><span data-stu-id="5798f-105">MS-DS-Machine-Account-Quota attribute</span></span>

<span data-ttu-id="5798f-106">允許使用者在網域中建立的電腦帳戶數目。</span><span class="sxs-lookup"><span data-stu-id="5798f-106">The number of computer accounts that a user is allowed to create in a domain.</span></span>



| <span data-ttu-id="5798f-107">進入</span><span class="sxs-lookup"><span data-stu-id="5798f-107">Entry</span></span> | <span data-ttu-id="5798f-108">值</span><span class="sxs-lookup"><span data-stu-id="5798f-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="5798f-109">CN</span><span class="sxs-lookup"><span data-stu-id="5798f-109">CN</span></span>                | <span data-ttu-id="5798f-110">MS-DS-電腦帳戶-配額</span><span class="sxs-lookup"><span data-stu-id="5798f-110">MS-DS-Machine-Account-Quota</span></span>                      |
| <span data-ttu-id="5798f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5798f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5798f-112">MachineAccountQuota</span><span class="sxs-lookup"><span data-stu-id="5798f-112">ms-DS-MachineAccountQuota</span></span>                        |
| <span data-ttu-id="5798f-113">大小</span><span class="sxs-lookup"><span data-stu-id="5798f-113">Size</span></span>              | <span data-ttu-id="5798f-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="5798f-114">4 bytes</span></span>                                          |
| <span data-ttu-id="5798f-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5798f-115">Update Privilege</span></span>  | <span data-ttu-id="5798f-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="5798f-116">Domain administrator</span></span>                             |
| <span data-ttu-id="5798f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5798f-117">Update Frequency</span></span>  | <span data-ttu-id="5798f-118">每當網域的配額需要變更時。</span><span class="sxs-lookup"><span data-stu-id="5798f-118">Whenever the quota for a domain needs to change.</span></span> |
| <span data-ttu-id="5798f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5798f-119">Attribute-Id</span></span>      | <span data-ttu-id="5798f-120">1.2.840.113556.1.4.1411</span><span class="sxs-lookup"><span data-stu-id="5798f-120">1.2.840.113556.1.4.1411</span></span>                          |
| <span data-ttu-id="5798f-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5798f-121">System-Id-Guid</span></span>    | <span data-ttu-id="5798f-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="5798f-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span></span>             |
| <span data-ttu-id="5798f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="5798f-123">Syntax</span></span>            | [<span data-ttu-id="5798f-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="5798f-124">**Enumeration**</span></span>](s-enumeration.md)             |



## <a name="implementations"></a><span data-ttu-id="5798f-125">實作</span><span class="sxs-lookup"><span data-stu-id="5798f-125">Implementations</span></span>

-   [<span data-ttu-id="5798f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5798f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5798f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5798f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5798f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5798f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5798f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5798f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5798f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5798f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5798f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5798f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5798f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5798f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="5798f-133">進入</span><span class="sxs-lookup"><span data-stu-id="5798f-133">Entry</span></span> | <span data-ttu-id="5798f-134">值</span><span class="sxs-lookup"><span data-stu-id="5798f-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5798f-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5798f-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5798f-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5798f-137">System-Only</span></span>            | <span data-ttu-id="5798f-138">否</span><span class="sxs-lookup"><span data-stu-id="5798f-138">False</span></span>                                        |
| <span data-ttu-id="5798f-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5798f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5798f-140">對</span><span class="sxs-lookup"><span data-stu-id="5798f-140">True</span></span>                                         |
| <span data-ttu-id="5798f-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5798f-141">Is Indexed</span></span>             | <span data-ttu-id="5798f-142">否</span><span class="sxs-lookup"><span data-stu-id="5798f-142">False</span></span>                                        |
| <span data-ttu-id="5798f-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5798f-143">In Global Catalog</span></span>      | <span data-ttu-id="5798f-144">否</span><span class="sxs-lookup"><span data-stu-id="5798f-144">False</span></span>                                        |
| <span data-ttu-id="5798f-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5798f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5798f-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5798f-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5798f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5798f-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5798f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5798f-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5798f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-149">Search-Flags</span></span>           | <span data-ttu-id="5798f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5798f-150">0x00000000</span></span>                                   |
| <span data-ttu-id="5798f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-151">System-Flags</span></span>           | <span data-ttu-id="5798f-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5798f-152">0x00000010</span></span>                                   |
| <span data-ttu-id="5798f-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5798f-153">Classes used in</span></span>        | [<span data-ttu-id="5798f-154">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="5798f-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5798f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5798f-155">Windows Server 2003</span></span>



| <span data-ttu-id="5798f-156">進入</span><span class="sxs-lookup"><span data-stu-id="5798f-156">Entry</span></span> | <span data-ttu-id="5798f-157">值</span><span class="sxs-lookup"><span data-stu-id="5798f-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5798f-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5798f-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5798f-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5798f-160">System-Only</span></span>            | <span data-ttu-id="5798f-161">否</span><span class="sxs-lookup"><span data-stu-id="5798f-161">False</span></span>                                        |
| <span data-ttu-id="5798f-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5798f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5798f-163">對</span><span class="sxs-lookup"><span data-stu-id="5798f-163">True</span></span>                                         |
| <span data-ttu-id="5798f-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5798f-164">Is Indexed</span></span>             | <span data-ttu-id="5798f-165">否</span><span class="sxs-lookup"><span data-stu-id="5798f-165">False</span></span>                                        |
| <span data-ttu-id="5798f-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5798f-166">In Global Catalog</span></span>      | <span data-ttu-id="5798f-167">否</span><span class="sxs-lookup"><span data-stu-id="5798f-167">False</span></span>                                        |
| <span data-ttu-id="5798f-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5798f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5798f-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5798f-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5798f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5798f-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5798f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5798f-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5798f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-172">Search-Flags</span></span>           | <span data-ttu-id="5798f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5798f-173">0x00000000</span></span>                                   |
| <span data-ttu-id="5798f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-174">System-Flags</span></span>           | <span data-ttu-id="5798f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5798f-175">0x00000010</span></span>                                   |
| <span data-ttu-id="5798f-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5798f-176">Classes used in</span></span>        | [<span data-ttu-id="5798f-177">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="5798f-177">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5798f-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5798f-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5798f-179">進入</span><span class="sxs-lookup"><span data-stu-id="5798f-179">Entry</span></span> | <span data-ttu-id="5798f-180">值</span><span class="sxs-lookup"><span data-stu-id="5798f-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5798f-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5798f-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5798f-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="5798f-183">System-Only</span></span>            | <span data-ttu-id="5798f-184">否</span><span class="sxs-lookup"><span data-stu-id="5798f-184">False</span></span>                                        |
| <span data-ttu-id="5798f-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5798f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="5798f-186">對</span><span class="sxs-lookup"><span data-stu-id="5798f-186">True</span></span>                                         |
| <span data-ttu-id="5798f-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5798f-187">Is Indexed</span></span>             | <span data-ttu-id="5798f-188">否</span><span class="sxs-lookup"><span data-stu-id="5798f-188">False</span></span>                                        |
| <span data-ttu-id="5798f-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5798f-189">In Global Catalog</span></span>      | <span data-ttu-id="5798f-190">否</span><span class="sxs-lookup"><span data-stu-id="5798f-190">False</span></span>                                        |
| <span data-ttu-id="5798f-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5798f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="5798f-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5798f-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5798f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5798f-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5798f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5798f-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5798f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-195">Search-Flags</span></span>           | <span data-ttu-id="5798f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5798f-196">0x00000000</span></span>                                   |
| <span data-ttu-id="5798f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-197">System-Flags</span></span>           | <span data-ttu-id="5798f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5798f-198">0x00000010</span></span>                                   |
| <span data-ttu-id="5798f-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5798f-199">Classes used in</span></span>        | [<span data-ttu-id="5798f-200">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="5798f-200">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5798f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5798f-201">Windows Server 2008</span></span>



| <span data-ttu-id="5798f-202">進入</span><span class="sxs-lookup"><span data-stu-id="5798f-202">Entry</span></span> | <span data-ttu-id="5798f-203">值</span><span class="sxs-lookup"><span data-stu-id="5798f-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5798f-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5798f-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5798f-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="5798f-206">System-Only</span></span>            | <span data-ttu-id="5798f-207">否</span><span class="sxs-lookup"><span data-stu-id="5798f-207">False</span></span>                                        |
| <span data-ttu-id="5798f-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5798f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="5798f-209">對</span><span class="sxs-lookup"><span data-stu-id="5798f-209">True</span></span>                                         |
| <span data-ttu-id="5798f-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5798f-210">Is Indexed</span></span>             | <span data-ttu-id="5798f-211">否</span><span class="sxs-lookup"><span data-stu-id="5798f-211">False</span></span>                                        |
| <span data-ttu-id="5798f-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5798f-212">In Global Catalog</span></span>      | <span data-ttu-id="5798f-213">否</span><span class="sxs-lookup"><span data-stu-id="5798f-213">False</span></span>                                        |
| <span data-ttu-id="5798f-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5798f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="5798f-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5798f-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5798f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5798f-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5798f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5798f-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5798f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-218">Search-Flags</span></span>           | <span data-ttu-id="5798f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5798f-219">0x00000000</span></span>                                   |
| <span data-ttu-id="5798f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-220">System-Flags</span></span>           | <span data-ttu-id="5798f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5798f-221">0x00000010</span></span>                                   |
| <span data-ttu-id="5798f-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5798f-222">Classes used in</span></span>        | [<span data-ttu-id="5798f-223">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="5798f-223">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5798f-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5798f-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5798f-225">進入</span><span class="sxs-lookup"><span data-stu-id="5798f-225">Entry</span></span> | <span data-ttu-id="5798f-226">值</span><span class="sxs-lookup"><span data-stu-id="5798f-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5798f-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5798f-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5798f-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="5798f-229">System-Only</span></span>            | <span data-ttu-id="5798f-230">否</span><span class="sxs-lookup"><span data-stu-id="5798f-230">False</span></span>                                        |
| <span data-ttu-id="5798f-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5798f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="5798f-232">對</span><span class="sxs-lookup"><span data-stu-id="5798f-232">True</span></span>                                         |
| <span data-ttu-id="5798f-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5798f-233">Is Indexed</span></span>             | <span data-ttu-id="5798f-234">否</span><span class="sxs-lookup"><span data-stu-id="5798f-234">False</span></span>                                        |
| <span data-ttu-id="5798f-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5798f-235">In Global Catalog</span></span>      | <span data-ttu-id="5798f-236">否</span><span class="sxs-lookup"><span data-stu-id="5798f-236">False</span></span>                                        |
| <span data-ttu-id="5798f-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5798f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="5798f-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5798f-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5798f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5798f-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5798f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5798f-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5798f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-241">Search-Flags</span></span>           | <span data-ttu-id="5798f-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5798f-242">0x00000000</span></span>                                   |
| <span data-ttu-id="5798f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-243">System-Flags</span></span>           | <span data-ttu-id="5798f-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5798f-244">0x00000010</span></span>                                   |
| <span data-ttu-id="5798f-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5798f-245">Classes used in</span></span>        | [<span data-ttu-id="5798f-246">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="5798f-246">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5798f-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5798f-247">Windows Server 2012</span></span>



| <span data-ttu-id="5798f-248">進入</span><span class="sxs-lookup"><span data-stu-id="5798f-248">Entry</span></span> | <span data-ttu-id="5798f-249">值</span><span class="sxs-lookup"><span data-stu-id="5798f-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5798f-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5798f-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5798f-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5798f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="5798f-252">System-Only</span></span>            | <span data-ttu-id="5798f-253">否</span><span class="sxs-lookup"><span data-stu-id="5798f-253">False</span></span>                                        |
| <span data-ttu-id="5798f-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5798f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="5798f-255">對</span><span class="sxs-lookup"><span data-stu-id="5798f-255">True</span></span>                                         |
| <span data-ttu-id="5798f-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5798f-256">Is Indexed</span></span>             | <span data-ttu-id="5798f-257">否</span><span class="sxs-lookup"><span data-stu-id="5798f-257">False</span></span>                                        |
| <span data-ttu-id="5798f-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5798f-258">In Global Catalog</span></span>      | <span data-ttu-id="5798f-259">否</span><span class="sxs-lookup"><span data-stu-id="5798f-259">False</span></span>                                        |
| <span data-ttu-id="5798f-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5798f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="5798f-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5798f-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5798f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5798f-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5798f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5798f-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5798f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-264">Search-Flags</span></span>           | <span data-ttu-id="5798f-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5798f-265">0x00000000</span></span>                                   |
| <span data-ttu-id="5798f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5798f-266">System-Flags</span></span>           | <span data-ttu-id="5798f-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5798f-267">0x00000010</span></span>                                   |
| <span data-ttu-id="5798f-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5798f-268">Classes used in</span></span>        | [<span data-ttu-id="5798f-269">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="5798f-269">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






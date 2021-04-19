---
title: MSMQ-簽署-憑證-Svrmig.mig 屬性
description: 在 MSMQ 混合模式中，屬性包含先前的 mSMQSignCertificates 值。 MSMQ 支援從 MSMQ 1.0 DS 遷移至 Windows 2000 DS，而混合模式則指定某些 DS 的部分未升級為 Windows 2000 的狀態。
ms.assetid: 0dbc5d97-39e6-4863-a386-541ea2abaadc
ms.tgt_platform: multiple
keywords:
- MSMQ-簽署-憑證-Svrmig.mig 屬性 AD 架構
- mSMQSignCertificatesMig 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates-Mig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1916cf98d15da1bd84603a2305543e899d868
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106991328"
---
# <a name="msmq-sign-certificates-mig-attribute"></a><span data-ttu-id="37e7b-106">MSMQ-簽署-憑證-Svrmig.mig 屬性</span><span class="sxs-lookup"><span data-stu-id="37e7b-106">MSMQ-Sign-Certificates-Mig attribute</span></span>

<span data-ttu-id="37e7b-107">在 MSMQ 混合模式中，屬性包含先前的 mSMQSignCertificates 值。</span><span class="sxs-lookup"><span data-stu-id="37e7b-107">In MSMQ mixed-mode, the attribute contains the previous value of mSMQSignCertificates.</span></span> <span data-ttu-id="37e7b-108">MSMQ 支援從 MSMQ 1.0 DS 遷移至 Windows 2000 DS，而混合模式則指定某些 DS 的部分未升級為 Windows 2000 的狀態。</span><span class="sxs-lookup"><span data-stu-id="37e7b-108">MSMQ supports migration from the MSMQ 1.0 DS to the Windows 2000 DS, and mixed mode specifies a state in which some of the DS severs were not upgraded to Windows 2000.</span></span>



| <span data-ttu-id="37e7b-109">進入</span><span class="sxs-lookup"><span data-stu-id="37e7b-109">Entry</span></span> | <span data-ttu-id="37e7b-110">值</span><span class="sxs-lookup"><span data-stu-id="37e7b-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="37e7b-111">CN</span><span class="sxs-lookup"><span data-stu-id="37e7b-111">CN</span></span>                | <span data-ttu-id="37e7b-112">MSMQ-簽署-憑證-Svrmig.mig</span><span class="sxs-lookup"><span data-stu-id="37e7b-112">MSMQ-Sign-Certificates-Mig</span></span>                            |
| <span data-ttu-id="37e7b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="37e7b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="37e7b-114">mSMQSignCertificatesMig</span><span class="sxs-lookup"><span data-stu-id="37e7b-114">mSMQSignCertificatesMig</span></span>                               |
| <span data-ttu-id="37e7b-115">大小</span><span class="sxs-lookup"><span data-stu-id="37e7b-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="37e7b-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="37e7b-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="37e7b-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="37e7b-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="37e7b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37e7b-118">Attribute-Id</span></span>      | <span data-ttu-id="37e7b-119">1.2.840.113556.1.4.967</span><span class="sxs-lookup"><span data-stu-id="37e7b-119">1.2.840.113556.1.4.967</span></span>                                |
| <span data-ttu-id="37e7b-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="37e7b-120">System-Id-Guid</span></span>    | <span data-ttu-id="37e7b-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="37e7b-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="37e7b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="37e7b-122">Syntax</span></span>            | [<span data-ttu-id="37e7b-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="37e7b-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="37e7b-124">實作</span><span class="sxs-lookup"><span data-stu-id="37e7b-124">Implementations</span></span>

-   [<span data-ttu-id="37e7b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="37e7b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="37e7b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37e7b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37e7b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37e7b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37e7b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37e7b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37e7b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37e7b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37e7b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37e7b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="37e7b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37e7b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="37e7b-132">進入</span><span class="sxs-lookup"><span data-stu-id="37e7b-132">Entry</span></span> | <span data-ttu-id="37e7b-133">值</span><span class="sxs-lookup"><span data-stu-id="37e7b-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e7b-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e7b-134">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e7b-135">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e7b-136">System-Only</span></span>            | <span data-ttu-id="37e7b-137">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-137">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e7b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="37e7b-139">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-139">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e7b-140">Is Indexed</span></span>             | <span data-ttu-id="37e7b-141">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-141">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e7b-142">In Global Catalog</span></span>      | <span data-ttu-id="37e7b-143">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-143">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e7b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e7b-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e7b-145">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="37e7b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e7b-146">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e7b-147">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-148">Search-Flags</span></span>           | <span data-ttu-id="37e7b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e7b-149">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="37e7b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-150">System-Flags</span></span>           | <span data-ttu-id="37e7b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e7b-151">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="37e7b-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e7b-152">Classes used in</span></span>        | [<span data-ttu-id="37e7b-153">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="37e7b-153">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="37e7b-154">**User**</span><span class="sxs-lookup"><span data-stu-id="37e7b-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="37e7b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37e7b-155">Windows Server 2003</span></span>



| <span data-ttu-id="37e7b-156">進入</span><span class="sxs-lookup"><span data-stu-id="37e7b-156">Entry</span></span> | <span data-ttu-id="37e7b-157">值</span><span class="sxs-lookup"><span data-stu-id="37e7b-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e7b-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e7b-158">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e7b-159">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e7b-160">System-Only</span></span>            | <span data-ttu-id="37e7b-161">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-161">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e7b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="37e7b-163">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-163">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e7b-164">Is Indexed</span></span>             | <span data-ttu-id="37e7b-165">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-165">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e7b-166">In Global Catalog</span></span>      | <span data-ttu-id="37e7b-167">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-167">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e7b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e7b-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e7b-169">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="37e7b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e7b-170">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e7b-171">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-172">Search-Flags</span></span>           | <span data-ttu-id="37e7b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e7b-173">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="37e7b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-174">System-Flags</span></span>           | <span data-ttu-id="37e7b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e7b-175">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="37e7b-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e7b-176">Classes used in</span></span>        | [<span data-ttu-id="37e7b-177">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="37e7b-177">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="37e7b-178">**User**</span><span class="sxs-lookup"><span data-stu-id="37e7b-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37e7b-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37e7b-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37e7b-180">進入</span><span class="sxs-lookup"><span data-stu-id="37e7b-180">Entry</span></span> | <span data-ttu-id="37e7b-181">值</span><span class="sxs-lookup"><span data-stu-id="37e7b-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e7b-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e7b-182">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e7b-183">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e7b-184">System-Only</span></span>            | <span data-ttu-id="37e7b-185">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-185">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e7b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="37e7b-187">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-187">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e7b-188">Is Indexed</span></span>             | <span data-ttu-id="37e7b-189">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-189">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e7b-190">In Global Catalog</span></span>      | <span data-ttu-id="37e7b-191">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-191">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e7b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e7b-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e7b-193">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="37e7b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e7b-194">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e7b-195">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-196">Search-Flags</span></span>           | <span data-ttu-id="37e7b-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e7b-197">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="37e7b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-198">System-Flags</span></span>           | <span data-ttu-id="37e7b-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e7b-199">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="37e7b-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e7b-200">Classes used in</span></span>        | [<span data-ttu-id="37e7b-201">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="37e7b-201">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="37e7b-202">**User**</span><span class="sxs-lookup"><span data-stu-id="37e7b-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37e7b-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37e7b-203">Windows Server 2008</span></span>



| <span data-ttu-id="37e7b-204">進入</span><span class="sxs-lookup"><span data-stu-id="37e7b-204">Entry</span></span> | <span data-ttu-id="37e7b-205">值</span><span class="sxs-lookup"><span data-stu-id="37e7b-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e7b-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e7b-206">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e7b-207">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e7b-208">System-Only</span></span>            | <span data-ttu-id="37e7b-209">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-209">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e7b-210">Is-Single-Valued</span></span>       | <span data-ttu-id="37e7b-211">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-211">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e7b-212">Is Indexed</span></span>             | <span data-ttu-id="37e7b-213">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-213">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e7b-214">In Global Catalog</span></span>      | <span data-ttu-id="37e7b-215">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-215">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e7b-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e7b-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e7b-217">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="37e7b-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e7b-218">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e7b-219">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-220">Search-Flags</span></span>           | <span data-ttu-id="37e7b-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e7b-221">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="37e7b-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-222">System-Flags</span></span>           | <span data-ttu-id="37e7b-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e7b-223">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="37e7b-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e7b-224">Classes used in</span></span>        | [<span data-ttu-id="37e7b-225">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="37e7b-225">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="37e7b-226">**User**</span><span class="sxs-lookup"><span data-stu-id="37e7b-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37e7b-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37e7b-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37e7b-228">進入</span><span class="sxs-lookup"><span data-stu-id="37e7b-228">Entry</span></span> | <span data-ttu-id="37e7b-229">值</span><span class="sxs-lookup"><span data-stu-id="37e7b-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e7b-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e7b-230">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e7b-231">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e7b-232">System-Only</span></span>            | <span data-ttu-id="37e7b-233">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-233">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e7b-234">Is-Single-Valued</span></span>       | <span data-ttu-id="37e7b-235">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-235">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e7b-236">Is Indexed</span></span>             | <span data-ttu-id="37e7b-237">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-237">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e7b-238">In Global Catalog</span></span>      | <span data-ttu-id="37e7b-239">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-239">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e7b-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e7b-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e7b-241">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="37e7b-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e7b-242">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e7b-243">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-244">Search-Flags</span></span>           | <span data-ttu-id="37e7b-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e7b-245">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="37e7b-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-246">System-Flags</span></span>           | <span data-ttu-id="37e7b-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e7b-247">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="37e7b-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e7b-248">Classes used in</span></span>        | [<span data-ttu-id="37e7b-249">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="37e7b-249">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="37e7b-250">**User**</span><span class="sxs-lookup"><span data-stu-id="37e7b-250">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37e7b-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37e7b-251">Windows Server 2012</span></span>



| <span data-ttu-id="37e7b-252">進入</span><span class="sxs-lookup"><span data-stu-id="37e7b-252">Entry</span></span> | <span data-ttu-id="37e7b-253">值</span><span class="sxs-lookup"><span data-stu-id="37e7b-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e7b-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e7b-254">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e7b-255">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="37e7b-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e7b-256">System-Only</span></span>            | <span data-ttu-id="37e7b-257">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-257">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e7b-258">Is-Single-Valued</span></span>       | <span data-ttu-id="37e7b-259">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-259">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e7b-260">Is Indexed</span></span>             | <span data-ttu-id="37e7b-261">否</span><span class="sxs-lookup"><span data-stu-id="37e7b-261">False</span></span>                                                                                         |
| <span data-ttu-id="37e7b-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e7b-262">In Global Catalog</span></span>      | <span data-ttu-id="37e7b-263">對</span><span class="sxs-lookup"><span data-stu-id="37e7b-263">True</span></span>                                                                                          |
| <span data-ttu-id="37e7b-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e7b-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e7b-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e7b-265">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="37e7b-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e7b-266">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e7b-267">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="37e7b-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-268">Search-Flags</span></span>           | <span data-ttu-id="37e7b-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e7b-269">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="37e7b-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e7b-270">System-Flags</span></span>           | <span data-ttu-id="37e7b-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e7b-271">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="37e7b-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e7b-272">Classes used in</span></span>        | [<span data-ttu-id="37e7b-273">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="37e7b-273">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="37e7b-274">**User**</span><span class="sxs-lookup"><span data-stu-id="37e7b-274">**User**</span></span>](c-user.md)<br/> |



 

 






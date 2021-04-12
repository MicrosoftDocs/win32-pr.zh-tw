---
title: NETBIOS-Name 屬性
description: 要在 NetBIOS 上使用的物件名稱。
ms.assetid: 03cbfa61-b747-4f3e-9bf5-17fd6da2e7be
ms.tgt_platform: multiple
keywords:
- NETBIOS-Name 屬性 AD 架構
- nETBIOSName 屬性 AD 架構
topic_type:
- apiref
api_name:
- NETBIOS-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4063b842200bf99910a3652b8f3bea9419c2728f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107658"
---
# <a name="netbios-name-attribute"></a><span data-ttu-id="dce1c-105">NETBIOS-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="dce1c-105">NETBIOS-Name attribute</span></span>

<span data-ttu-id="dce1c-106">要在 NetBIOS 上使用的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="dce1c-106">The name of the object to be used over NetBIOS.</span></span>



| <span data-ttu-id="dce1c-107">進入</span><span class="sxs-lookup"><span data-stu-id="dce1c-107">Entry</span></span> | <span data-ttu-id="dce1c-108">值</span><span class="sxs-lookup"><span data-stu-id="dce1c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="dce1c-109">CN</span><span class="sxs-lookup"><span data-stu-id="dce1c-109">CN</span></span>                | <span data-ttu-id="dce1c-110">NETBIOS-Name</span><span class="sxs-lookup"><span data-stu-id="dce1c-110">NETBIOS-Name</span></span>                                |
| <span data-ttu-id="dce1c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dce1c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dce1c-112">nETBIOSName</span><span class="sxs-lookup"><span data-stu-id="dce1c-112">nETBIOSName</span></span>                                 |
| <span data-ttu-id="dce1c-113">大小</span><span class="sxs-lookup"><span data-stu-id="dce1c-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="dce1c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dce1c-114">Update Privilege</span></span>  | <span data-ttu-id="dce1c-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="dce1c-115">Domain administrator</span></span>                        |
| <span data-ttu-id="dce1c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dce1c-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="dce1c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dce1c-117">Attribute-Id</span></span>      | <span data-ttu-id="dce1c-118">1.2.840.113556.1.4.87</span><span class="sxs-lookup"><span data-stu-id="dce1c-118">1.2.840.113556.1.4.87</span></span>                       |
| <span data-ttu-id="dce1c-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dce1c-119">System-Id-Guid</span></span>    | <span data-ttu-id="dce1c-120">bf9679d8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dce1c-120">bf9679d8-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="dce1c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="dce1c-121">Syntax</span></span>            | [<span data-ttu-id="dce1c-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dce1c-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="dce1c-123">實作</span><span class="sxs-lookup"><span data-stu-id="dce1c-123">Implementations</span></span>

-   [<span data-ttu-id="dce1c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dce1c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dce1c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dce1c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dce1c-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="dce1c-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dce1c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dce1c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dce1c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dce1c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dce1c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dce1c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dce1c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dce1c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dce1c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dce1c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="dce1c-132">進入</span><span class="sxs-lookup"><span data-stu-id="dce1c-132">Entry</span></span> | <span data-ttu-id="dce1c-133">值</span><span class="sxs-lookup"><span data-stu-id="dce1c-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce1c-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dce1c-134">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce1c-135">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce1c-136">System-Only</span></span>            | <span data-ttu-id="dce1c-137">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-137">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dce1c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="dce1c-139">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-139">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dce1c-140">Is Indexed</span></span>             | <span data-ttu-id="dce1c-141">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-141">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dce1c-142">In Global Catalog</span></span>      | <span data-ttu-id="dce1c-143">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-143">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dce1c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce1c-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dce1c-145">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="dce1c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce1c-146">Range-Lower</span></span>            | <span data-ttu-id="dce1c-147">1</span><span class="sxs-lookup"><span data-stu-id="dce1c-147">1</span></span>                                                                                       |
| <span data-ttu-id="dce1c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce1c-148">Range-Upper</span></span>            | <span data-ttu-id="dce1c-149">16</span><span class="sxs-lookup"><span data-stu-id="dce1c-149">16</span></span>                                                                                      |
| <span data-ttu-id="dce1c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-150">Search-Flags</span></span>           | <span data-ttu-id="dce1c-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dce1c-151">0x00000001</span></span>                                                                              |
| <span data-ttu-id="dce1c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-152">System-Flags</span></span>           | <span data-ttu-id="dce1c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dce1c-153">0x00000010</span></span>                                                                              |
| <span data-ttu-id="dce1c-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dce1c-154">Classes used in</span></span>        | [<span data-ttu-id="dce1c-155">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="dce1c-155">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="dce1c-156">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="dce1c-156">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dce1c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dce1c-157">Windows Server 2003</span></span>



| <span data-ttu-id="dce1c-158">進入</span><span class="sxs-lookup"><span data-stu-id="dce1c-158">Entry</span></span> | <span data-ttu-id="dce1c-159">值</span><span class="sxs-lookup"><span data-stu-id="dce1c-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce1c-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dce1c-160">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce1c-161">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce1c-162">System-Only</span></span>            | <span data-ttu-id="dce1c-163">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-163">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dce1c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="dce1c-165">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-165">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dce1c-166">Is Indexed</span></span>             | <span data-ttu-id="dce1c-167">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-167">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dce1c-168">In Global Catalog</span></span>      | <span data-ttu-id="dce1c-169">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-169">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dce1c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce1c-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dce1c-171">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="dce1c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce1c-172">Range-Lower</span></span>            | <span data-ttu-id="dce1c-173">1</span><span class="sxs-lookup"><span data-stu-id="dce1c-173">1</span></span>                                                                                       |
| <span data-ttu-id="dce1c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce1c-174">Range-Upper</span></span>            | <span data-ttu-id="dce1c-175">16</span><span class="sxs-lookup"><span data-stu-id="dce1c-175">16</span></span>                                                                                      |
| <span data-ttu-id="dce1c-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-176">Search-Flags</span></span>           | <span data-ttu-id="dce1c-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dce1c-177">0x00000001</span></span>                                                                              |
| <span data-ttu-id="dce1c-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-178">System-Flags</span></span>           | <span data-ttu-id="dce1c-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dce1c-179">0x00000010</span></span>                                                                              |
| <span data-ttu-id="dce1c-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dce1c-180">Classes used in</span></span>        | [<span data-ttu-id="dce1c-181">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="dce1c-181">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="dce1c-182">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="dce1c-182">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dce1c-183">亞當</span><span class="sxs-lookup"><span data-stu-id="dce1c-183">ADAM</span></span>



| <span data-ttu-id="dce1c-184">進入</span><span class="sxs-lookup"><span data-stu-id="dce1c-184">Entry</span></span> | <span data-ttu-id="dce1c-185">值</span><span class="sxs-lookup"><span data-stu-id="dce1c-185">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dce1c-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dce1c-186">Link-Id</span></span>                | \-                                                                               |
| <span data-ttu-id="dce1c-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce1c-187">MAPI-Id</span></span>                | \-                                                                               |
| <span data-ttu-id="dce1c-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce1c-188">System-Only</span></span>            | <span data-ttu-id="dce1c-189">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-189">False</span></span>                                                                            |
| <span data-ttu-id="dce1c-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dce1c-190">Is-Single-Valued</span></span>       | <span data-ttu-id="dce1c-191">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-191">True</span></span>                                                                             |
| <span data-ttu-id="dce1c-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dce1c-192">Is Indexed</span></span>             | <span data-ttu-id="dce1c-193">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-193">True</span></span>                                                                             |
| <span data-ttu-id="dce1c-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dce1c-194">In Global Catalog</span></span>      | <span data-ttu-id="dce1c-195">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-195">False</span></span>                                                                            |
| <span data-ttu-id="dce1c-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dce1c-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce1c-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dce1c-197">O:BAG:BAD:S:</span></span>                                                                     |
| <span data-ttu-id="dce1c-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce1c-198">Range-Lower</span></span>            | <span data-ttu-id="dce1c-199">1</span><span class="sxs-lookup"><span data-stu-id="dce1c-199">1</span></span>                                                                                |
| <span data-ttu-id="dce1c-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce1c-200">Range-Upper</span></span>            | <span data-ttu-id="dce1c-201">16</span><span class="sxs-lookup"><span data-stu-id="dce1c-201">16</span></span>                                                                               |
| <span data-ttu-id="dce1c-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-202">Search-Flags</span></span>           | <span data-ttu-id="dce1c-203">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dce1c-203">0x00000001</span></span>                                                                       |
| <span data-ttu-id="dce1c-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-204">System-Flags</span></span>           | <span data-ttu-id="dce1c-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dce1c-205">0x00000010</span></span>                                                                       |
| <span data-ttu-id="dce1c-206">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dce1c-206">Classes used in</span></span>        | [<span data-ttu-id="dce1c-207">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="dce1c-207">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="dce1c-208">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="dce1c-208">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dce1c-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dce1c-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dce1c-210">進入</span><span class="sxs-lookup"><span data-stu-id="dce1c-210">Entry</span></span> | <span data-ttu-id="dce1c-211">值</span><span class="sxs-lookup"><span data-stu-id="dce1c-211">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce1c-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dce1c-212">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce1c-213">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce1c-214">System-Only</span></span>            | <span data-ttu-id="dce1c-215">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-215">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dce1c-216">Is-Single-Valued</span></span>       | <span data-ttu-id="dce1c-217">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-217">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dce1c-218">Is Indexed</span></span>             | <span data-ttu-id="dce1c-219">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-219">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dce1c-220">In Global Catalog</span></span>      | <span data-ttu-id="dce1c-221">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-221">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dce1c-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce1c-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dce1c-223">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="dce1c-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce1c-224">Range-Lower</span></span>            | <span data-ttu-id="dce1c-225">1</span><span class="sxs-lookup"><span data-stu-id="dce1c-225">1</span></span>                                                                                       |
| <span data-ttu-id="dce1c-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce1c-226">Range-Upper</span></span>            | <span data-ttu-id="dce1c-227">16</span><span class="sxs-lookup"><span data-stu-id="dce1c-227">16</span></span>                                                                                      |
| <span data-ttu-id="dce1c-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-228">Search-Flags</span></span>           | <span data-ttu-id="dce1c-229">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dce1c-229">0x00000001</span></span>                                                                              |
| <span data-ttu-id="dce1c-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-230">System-Flags</span></span>           | <span data-ttu-id="dce1c-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dce1c-231">0x00000010</span></span>                                                                              |
| <span data-ttu-id="dce1c-232">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dce1c-232">Classes used in</span></span>        | [<span data-ttu-id="dce1c-233">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="dce1c-233">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="dce1c-234">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="dce1c-234">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dce1c-235">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dce1c-235">Windows Server 2008</span></span>



| <span data-ttu-id="dce1c-236">進入</span><span class="sxs-lookup"><span data-stu-id="dce1c-236">Entry</span></span> | <span data-ttu-id="dce1c-237">值</span><span class="sxs-lookup"><span data-stu-id="dce1c-237">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce1c-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dce1c-238">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce1c-239">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce1c-240">System-Only</span></span>            | <span data-ttu-id="dce1c-241">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-241">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-242">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dce1c-242">Is-Single-Valued</span></span>       | <span data-ttu-id="dce1c-243">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-243">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-244">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dce1c-244">Is Indexed</span></span>             | <span data-ttu-id="dce1c-245">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-245">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-246">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dce1c-246">In Global Catalog</span></span>      | <span data-ttu-id="dce1c-247">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-247">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-248">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dce1c-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce1c-249">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dce1c-249">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="dce1c-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce1c-250">Range-Lower</span></span>            | <span data-ttu-id="dce1c-251">1</span><span class="sxs-lookup"><span data-stu-id="dce1c-251">1</span></span>                                                                                       |
| <span data-ttu-id="dce1c-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce1c-252">Range-Upper</span></span>            | <span data-ttu-id="dce1c-253">16</span><span class="sxs-lookup"><span data-stu-id="dce1c-253">16</span></span>                                                                                      |
| <span data-ttu-id="dce1c-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-254">Search-Flags</span></span>           | <span data-ttu-id="dce1c-255">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dce1c-255">0x00000001</span></span>                                                                              |
| <span data-ttu-id="dce1c-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-256">System-Flags</span></span>           | <span data-ttu-id="dce1c-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dce1c-257">0x00000010</span></span>                                                                              |
| <span data-ttu-id="dce1c-258">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dce1c-258">Classes used in</span></span>        | [<span data-ttu-id="dce1c-259">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="dce1c-259">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="dce1c-260">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="dce1c-260">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dce1c-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dce1c-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dce1c-262">進入</span><span class="sxs-lookup"><span data-stu-id="dce1c-262">Entry</span></span> | <span data-ttu-id="dce1c-263">值</span><span class="sxs-lookup"><span data-stu-id="dce1c-263">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce1c-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dce1c-264">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce1c-265">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce1c-266">System-Only</span></span>            | <span data-ttu-id="dce1c-267">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-267">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-268">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dce1c-268">Is-Single-Valued</span></span>       | <span data-ttu-id="dce1c-269">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-269">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-270">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dce1c-270">Is Indexed</span></span>             | <span data-ttu-id="dce1c-271">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-271">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-272">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dce1c-272">In Global Catalog</span></span>      | <span data-ttu-id="dce1c-273">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-273">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-274">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dce1c-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce1c-275">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dce1c-275">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="dce1c-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce1c-276">Range-Lower</span></span>            | <span data-ttu-id="dce1c-277">1</span><span class="sxs-lookup"><span data-stu-id="dce1c-277">1</span></span>                                                                                       |
| <span data-ttu-id="dce1c-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce1c-278">Range-Upper</span></span>            | <span data-ttu-id="dce1c-279">16</span><span class="sxs-lookup"><span data-stu-id="dce1c-279">16</span></span>                                                                                      |
| <span data-ttu-id="dce1c-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-280">Search-Flags</span></span>           | <span data-ttu-id="dce1c-281">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dce1c-281">0x00000001</span></span>                                                                              |
| <span data-ttu-id="dce1c-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-282">System-Flags</span></span>           | <span data-ttu-id="dce1c-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dce1c-283">0x00000010</span></span>                                                                              |
| <span data-ttu-id="dce1c-284">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dce1c-284">Classes used in</span></span>        | [<span data-ttu-id="dce1c-285">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="dce1c-285">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="dce1c-286">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="dce1c-286">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dce1c-287">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dce1c-287">Windows Server 2012</span></span>



| <span data-ttu-id="dce1c-288">進入</span><span class="sxs-lookup"><span data-stu-id="dce1c-288">Entry</span></span> | <span data-ttu-id="dce1c-289">值</span><span class="sxs-lookup"><span data-stu-id="dce1c-289">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce1c-290">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dce1c-290">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce1c-291">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="dce1c-292">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce1c-292">System-Only</span></span>            | <span data-ttu-id="dce1c-293">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-293">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-294">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dce1c-294">Is-Single-Valued</span></span>       | <span data-ttu-id="dce1c-295">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-295">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-296">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dce1c-296">Is Indexed</span></span>             | <span data-ttu-id="dce1c-297">對</span><span class="sxs-lookup"><span data-stu-id="dce1c-297">True</span></span>                                                                                    |
| <span data-ttu-id="dce1c-298">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dce1c-298">In Global Catalog</span></span>      | <span data-ttu-id="dce1c-299">否</span><span class="sxs-lookup"><span data-stu-id="dce1c-299">False</span></span>                                                                                   |
| <span data-ttu-id="dce1c-300">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dce1c-300">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce1c-301">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dce1c-301">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="dce1c-302">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce1c-302">Range-Lower</span></span>            | <span data-ttu-id="dce1c-303">1</span><span class="sxs-lookup"><span data-stu-id="dce1c-303">1</span></span>                                                                                       |
| <span data-ttu-id="dce1c-304">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce1c-304">Range-Upper</span></span>            | <span data-ttu-id="dce1c-305">16</span><span class="sxs-lookup"><span data-stu-id="dce1c-305">16</span></span>                                                                                      |
| <span data-ttu-id="dce1c-306">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-306">Search-Flags</span></span>           | <span data-ttu-id="dce1c-307">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dce1c-307">0x00000001</span></span>                                                                              |
| <span data-ttu-id="dce1c-308">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce1c-308">System-Flags</span></span>           | <span data-ttu-id="dce1c-309">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dce1c-309">0x00000010</span></span>                                                                              |
| <span data-ttu-id="dce1c-310">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dce1c-310">Classes used in</span></span>        | [<span data-ttu-id="dce1c-311">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="dce1c-311">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="dce1c-312">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="dce1c-312">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






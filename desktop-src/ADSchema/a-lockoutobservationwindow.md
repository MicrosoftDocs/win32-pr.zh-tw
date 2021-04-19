---
title: 鎖定-觀察-視窗屬性
description: 系統遞增不正確登入計數的時間範圍（以 100-毫微秒間隔為單位）。
ms.assetid: a1929c32-cd05-43ca-9d4a-554683991696
ms.tgt_platform: multiple
keywords:
- 鎖定-觀察-視窗屬性 AD 架構
- Msds-lockoutobservationwindow 屬性 AD 架構
topic_type:
- apiref
api_name:
- Lock-Out-Observation-Window
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa00a71ba504ff4aa772cc43838f95c326db04c5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972901"
---
# <a name="lock-out-observation-window-attribute"></a><span data-ttu-id="77dc8-105">鎖定-觀察-視窗屬性</span><span class="sxs-lookup"><span data-stu-id="77dc8-105">Lock-Out-Observation-Window attribute</span></span>

<span data-ttu-id="77dc8-106">系統遞增不正確登入計數的時間範圍（以 100-毫微秒間隔為單位）。</span><span class="sxs-lookup"><span data-stu-id="77dc8-106">The range of time, in 100-nanosecond intervals, in which the system increments the incorrect logon count.</span></span>



| <span data-ttu-id="77dc8-107">進入</span><span class="sxs-lookup"><span data-stu-id="77dc8-107">Entry</span></span> | <span data-ttu-id="77dc8-108">值</span><span class="sxs-lookup"><span data-stu-id="77dc8-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="77dc8-109">CN</span><span class="sxs-lookup"><span data-stu-id="77dc8-109">CN</span></span>                | <span data-ttu-id="77dc8-110">鎖定-觀察-視窗</span><span class="sxs-lookup"><span data-stu-id="77dc8-110">Lock-Out-Observation-Window</span></span>          |
| <span data-ttu-id="77dc8-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="77dc8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="77dc8-112">Msds-lockoutobservationwindow</span><span class="sxs-lookup"><span data-stu-id="77dc8-112">lockOutObservationWindow</span></span>             |
| <span data-ttu-id="77dc8-113">大小</span><span class="sxs-lookup"><span data-stu-id="77dc8-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="77dc8-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="77dc8-114">Update Privilege</span></span>  | <span data-ttu-id="77dc8-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="77dc8-115">Domain administrator</span></span>                 |
| <span data-ttu-id="77dc8-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="77dc8-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="77dc8-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="77dc8-117">Attribute-Id</span></span>      | <span data-ttu-id="77dc8-118">1.2.840.113556.1.4.61</span><span class="sxs-lookup"><span data-stu-id="77dc8-118">1.2.840.113556.1.4.61</span></span>                |
| <span data-ttu-id="77dc8-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="77dc8-119">System-Id-Guid</span></span>    | <span data-ttu-id="77dc8-120">bf9679a4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="77dc8-120">bf9679a4-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="77dc8-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="77dc8-121">Syntax</span></span>            | [<span data-ttu-id="77dc8-122">**間隔**</span><span class="sxs-lookup"><span data-stu-id="77dc8-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="77dc8-123">實作</span><span class="sxs-lookup"><span data-stu-id="77dc8-123">Implementations</span></span>

-   [<span data-ttu-id="77dc8-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="77dc8-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="77dc8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="77dc8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="77dc8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="77dc8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="77dc8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="77dc8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="77dc8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="77dc8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="77dc8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="77dc8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="77dc8-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="77dc8-130">Windows 2000 Server</span></span>



| <span data-ttu-id="77dc8-131">進入</span><span class="sxs-lookup"><span data-stu-id="77dc8-131">Entry</span></span> | <span data-ttu-id="77dc8-132">值</span><span class="sxs-lookup"><span data-stu-id="77dc8-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77dc8-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77dc8-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77dc8-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="77dc8-135">System-Only</span></span>            | <span data-ttu-id="77dc8-136">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77dc8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="77dc8-138">對</span><span class="sxs-lookup"><span data-stu-id="77dc8-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="77dc8-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77dc8-139">Is Indexed</span></span>             | <span data-ttu-id="77dc8-140">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77dc8-141">In Global Catalog</span></span>      | <span data-ttu-id="77dc8-142">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77dc8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="77dc8-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77dc8-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="77dc8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77dc8-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77dc8-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-147">Search-Flags</span></span>           | <span data-ttu-id="77dc8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77dc8-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-149">System-Flags</span></span>           | <span data-ttu-id="77dc8-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77dc8-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77dc8-151">Classes used in</span></span>        | [<span data-ttu-id="77dc8-152">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="77dc8-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="77dc8-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="77dc8-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="77dc8-154">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="77dc8-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="77dc8-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="77dc8-155">Windows Server 2003</span></span>



| <span data-ttu-id="77dc8-156">進入</span><span class="sxs-lookup"><span data-stu-id="77dc8-156">Entry</span></span> | <span data-ttu-id="77dc8-157">值</span><span class="sxs-lookup"><span data-stu-id="77dc8-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77dc8-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77dc8-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77dc8-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="77dc8-160">System-Only</span></span>            | <span data-ttu-id="77dc8-161">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77dc8-162">Is-Single-Valued</span></span>       | <span data-ttu-id="77dc8-163">對</span><span class="sxs-lookup"><span data-stu-id="77dc8-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="77dc8-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77dc8-164">Is Indexed</span></span>             | <span data-ttu-id="77dc8-165">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77dc8-166">In Global Catalog</span></span>      | <span data-ttu-id="77dc8-167">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77dc8-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="77dc8-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77dc8-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="77dc8-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77dc8-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77dc8-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-172">Search-Flags</span></span>           | <span data-ttu-id="77dc8-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77dc8-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-174">System-Flags</span></span>           | <span data-ttu-id="77dc8-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77dc8-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77dc8-176">Classes used in</span></span>        | [<span data-ttu-id="77dc8-177">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="77dc8-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="77dc8-178">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="77dc8-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="77dc8-179">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="77dc8-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="77dc8-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="77dc8-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="77dc8-181">進入</span><span class="sxs-lookup"><span data-stu-id="77dc8-181">Entry</span></span> | <span data-ttu-id="77dc8-182">值</span><span class="sxs-lookup"><span data-stu-id="77dc8-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77dc8-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77dc8-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77dc8-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="77dc8-185">System-Only</span></span>            | <span data-ttu-id="77dc8-186">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77dc8-187">Is-Single-Valued</span></span>       | <span data-ttu-id="77dc8-188">對</span><span class="sxs-lookup"><span data-stu-id="77dc8-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="77dc8-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77dc8-189">Is Indexed</span></span>             | <span data-ttu-id="77dc8-190">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77dc8-191">In Global Catalog</span></span>      | <span data-ttu-id="77dc8-192">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77dc8-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="77dc8-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77dc8-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="77dc8-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77dc8-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77dc8-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-197">Search-Flags</span></span>           | <span data-ttu-id="77dc8-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77dc8-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-199">System-Flags</span></span>           | <span data-ttu-id="77dc8-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77dc8-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77dc8-201">Classes used in</span></span>        | [<span data-ttu-id="77dc8-202">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="77dc8-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="77dc8-203">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="77dc8-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="77dc8-204">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="77dc8-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="77dc8-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77dc8-205">Windows Server 2008</span></span>



| <span data-ttu-id="77dc8-206">進入</span><span class="sxs-lookup"><span data-stu-id="77dc8-206">Entry</span></span> | <span data-ttu-id="77dc8-207">值</span><span class="sxs-lookup"><span data-stu-id="77dc8-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77dc8-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77dc8-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77dc8-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="77dc8-210">System-Only</span></span>            | <span data-ttu-id="77dc8-211">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77dc8-212">Is-Single-Valued</span></span>       | <span data-ttu-id="77dc8-213">對</span><span class="sxs-lookup"><span data-stu-id="77dc8-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="77dc8-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77dc8-214">Is Indexed</span></span>             | <span data-ttu-id="77dc8-215">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77dc8-216">In Global Catalog</span></span>      | <span data-ttu-id="77dc8-217">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77dc8-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="77dc8-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77dc8-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="77dc8-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77dc8-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77dc8-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-222">Search-Flags</span></span>           | <span data-ttu-id="77dc8-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77dc8-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-224">System-Flags</span></span>           | <span data-ttu-id="77dc8-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77dc8-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77dc8-226">Classes used in</span></span>        | [<span data-ttu-id="77dc8-227">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="77dc8-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="77dc8-228">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="77dc8-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="77dc8-229">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="77dc8-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="77dc8-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77dc8-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="77dc8-231">進入</span><span class="sxs-lookup"><span data-stu-id="77dc8-231">Entry</span></span> | <span data-ttu-id="77dc8-232">值</span><span class="sxs-lookup"><span data-stu-id="77dc8-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77dc8-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77dc8-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77dc8-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="77dc8-235">System-Only</span></span>            | <span data-ttu-id="77dc8-236">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77dc8-237">Is-Single-Valued</span></span>       | <span data-ttu-id="77dc8-238">對</span><span class="sxs-lookup"><span data-stu-id="77dc8-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="77dc8-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77dc8-239">Is Indexed</span></span>             | <span data-ttu-id="77dc8-240">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77dc8-241">In Global Catalog</span></span>      | <span data-ttu-id="77dc8-242">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77dc8-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="77dc8-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77dc8-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="77dc8-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77dc8-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77dc8-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-247">Search-Flags</span></span>           | <span data-ttu-id="77dc8-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77dc8-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-249">System-Flags</span></span>           | <span data-ttu-id="77dc8-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77dc8-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77dc8-251">Classes used in</span></span>        | [<span data-ttu-id="77dc8-252">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="77dc8-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="77dc8-253">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="77dc8-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="77dc8-254">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="77dc8-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="77dc8-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77dc8-255">Windows Server 2012</span></span>



| <span data-ttu-id="77dc8-256">進入</span><span class="sxs-lookup"><span data-stu-id="77dc8-256">Entry</span></span> | <span data-ttu-id="77dc8-257">值</span><span class="sxs-lookup"><span data-stu-id="77dc8-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77dc8-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77dc8-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77dc8-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="77dc8-260">System-Only</span></span>            | <span data-ttu-id="77dc8-261">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77dc8-262">Is-Single-Valued</span></span>       | <span data-ttu-id="77dc8-263">對</span><span class="sxs-lookup"><span data-stu-id="77dc8-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="77dc8-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77dc8-264">Is Indexed</span></span>             | <span data-ttu-id="77dc8-265">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77dc8-266">In Global Catalog</span></span>      | <span data-ttu-id="77dc8-267">否</span><span class="sxs-lookup"><span data-stu-id="77dc8-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="77dc8-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77dc8-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="77dc8-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77dc8-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="77dc8-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77dc8-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77dc8-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="77dc8-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-272">Search-Flags</span></span>           | <span data-ttu-id="77dc8-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77dc8-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77dc8-274">System-Flags</span></span>           | <span data-ttu-id="77dc8-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77dc8-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="77dc8-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77dc8-276">Classes used in</span></span>        | [<span data-ttu-id="77dc8-277">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="77dc8-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="77dc8-278">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="77dc8-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="77dc8-279">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="77dc8-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 






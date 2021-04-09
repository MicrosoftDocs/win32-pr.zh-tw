---
title: Title 屬性
description: 包含使用者職稱。 這個屬性通常用來指出正式的職稱，例如資深程式設計師，而非 occupational 類別，例如程式設計師。 它通常不會用於尾碼標題（例如 Esq）。 或 DDS。
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Title 屬性 AD 架構
- title 屬性 AD 架構
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbb4dae862db9fc363b22647bd5e56a98e9e60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845280"
---
# <a name="title-attribute-ad-schema"></a><span data-ttu-id="49023-108">標題屬性 (AD 架構) </span><span class="sxs-lookup"><span data-stu-id="49023-108">Title attribute (AD Schema)</span></span>

<span data-ttu-id="49023-109">包含使用者職稱。</span><span class="sxs-lookup"><span data-stu-id="49023-109">Contains the user's job title.</span></span> <span data-ttu-id="49023-110">這個屬性通常用來指出正式的職稱，例如資深程式設計師，而非 occupational 類別，例如程式設計師。</span><span class="sxs-lookup"><span data-stu-id="49023-110">This property is commonly used to indicate the formal job title, such as Senior Programmer, rather than occupational class, such as programmer.</span></span> <span data-ttu-id="49023-111">它通常不會用於尾碼標題（例如 Esq）。</span><span class="sxs-lookup"><span data-stu-id="49023-111">It is not typically used for suffix titles such as Esq.</span></span> <span data-ttu-id="49023-112">或 DDS。</span><span class="sxs-lookup"><span data-stu-id="49023-112">or DDS.</span></span>



| <span data-ttu-id="49023-113">進入</span><span class="sxs-lookup"><span data-stu-id="49023-113">Entry</span></span> | <span data-ttu-id="49023-114">值</span><span class="sxs-lookup"><span data-stu-id="49023-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="49023-115">CN</span><span class="sxs-lookup"><span data-stu-id="49023-115">CN</span></span>                | <span data-ttu-id="49023-116">標題</span><span class="sxs-lookup"><span data-stu-id="49023-116">Title</span></span>                                                                     |
| <span data-ttu-id="49023-117">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="49023-117">Ldap-Display-Name</span></span> | <span data-ttu-id="49023-118">title</span><span class="sxs-lookup"><span data-stu-id="49023-118">title</span></span>                                                                     |
| <span data-ttu-id="49023-119">大小</span><span class="sxs-lookup"><span data-stu-id="49023-119">Size</span></span>              | \-                                                                        |
| <span data-ttu-id="49023-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="49023-120">Update Privilege</span></span>  | <span data-ttu-id="49023-121">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="49023-121">Domain administrator or account owner.</span></span>                                    |
| <span data-ttu-id="49023-122">更新頻率</span><span class="sxs-lookup"><span data-stu-id="49023-122">Update Frequency</span></span>  | <span data-ttu-id="49023-123">當使用者的記錄建立時，以及每次需要變更標題時。</span><span class="sxs-lookup"><span data-stu-id="49023-123">When the user's record is created and whenever the title needs to change.</span></span> |
| <span data-ttu-id="49023-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="49023-124">Attribute-Id</span></span>      | <span data-ttu-id="49023-125">2.5.4.12</span><span class="sxs-lookup"><span data-stu-id="49023-125">2.5.4.12</span></span>                                                                  |
| <span data-ttu-id="49023-126">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="49023-126">System-Id-Guid</span></span>    | <span data-ttu-id="49023-127">bf967a55-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="49023-127">bf967a55-0de6-11d0-a285-00aa003049e2</span></span>                                      |
| <span data-ttu-id="49023-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="49023-128">Syntax</span></span>            | [<span data-ttu-id="49023-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="49023-129">**String(Unicode)**</span></span>](s-string-unicode.md)                               |



## <a name="implementations"></a><span data-ttu-id="49023-130">實作</span><span class="sxs-lookup"><span data-stu-id="49023-130">Implementations</span></span>

-   [<span data-ttu-id="49023-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="49023-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="49023-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="49023-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="49023-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="49023-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="49023-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="49023-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="49023-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="49023-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="49023-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="49023-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="49023-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49023-137">Windows 2000 Server</span></span>



| <span data-ttu-id="49023-138">進入</span><span class="sxs-lookup"><span data-stu-id="49023-138">Entry</span></span> | <span data-ttu-id="49023-139">值</span><span class="sxs-lookup"><span data-stu-id="49023-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49023-140">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49023-140">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="49023-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49023-141">MAPI-Id</span></span>                | <span data-ttu-id="49023-142">0x3A17</span><span class="sxs-lookup"><span data-stu-id="49023-142">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="49023-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="49023-143">System-Only</span></span>            | <span data-ttu-id="49023-144">否</span><span class="sxs-lookup"><span data-stu-id="49023-144">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-145">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49023-145">Is-Single-Valued</span></span>       | <span data-ttu-id="49023-146">對</span><span class="sxs-lookup"><span data-stu-id="49023-146">True</span></span>                                                                                                                            |
| <span data-ttu-id="49023-147">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49023-147">Is Indexed</span></span>             | <span data-ttu-id="49023-148">否</span><span class="sxs-lookup"><span data-stu-id="49023-148">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-149">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49023-149">In Global Catalog</span></span>      | <span data-ttu-id="49023-150">否</span><span class="sxs-lookup"><span data-stu-id="49023-150">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-151">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49023-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="49023-152">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49023-152">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="49023-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49023-153">Range-Lower</span></span>            | <span data-ttu-id="49023-154">1</span><span class="sxs-lookup"><span data-stu-id="49023-154">1</span></span>                                                                                                                               |
| <span data-ttu-id="49023-155">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49023-155">Range-Upper</span></span>            | <span data-ttu-id="49023-156">64</span><span class="sxs-lookup"><span data-stu-id="49023-156">64</span></span>                                                                                                                              |
| <span data-ttu-id="49023-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-157">Search-Flags</span></span>           | <span data-ttu-id="49023-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49023-158">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="49023-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-159">System-Flags</span></span>           | <span data-ttu-id="49023-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49023-160">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="49023-161">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49023-161">Classes used in</span></span>        | [<span data-ttu-id="49023-162">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="49023-162">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="49023-163">**居住人**</span><span class="sxs-lookup"><span data-stu-id="49023-163">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="49023-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49023-164">Windows Server 2003</span></span>



| <span data-ttu-id="49023-165">進入</span><span class="sxs-lookup"><span data-stu-id="49023-165">Entry</span></span> | <span data-ttu-id="49023-166">值</span><span class="sxs-lookup"><span data-stu-id="49023-166">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49023-167">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49023-167">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="49023-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49023-168">MAPI-Id</span></span>                | <span data-ttu-id="49023-169">0x3A17</span><span class="sxs-lookup"><span data-stu-id="49023-169">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="49023-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="49023-170">System-Only</span></span>            | <span data-ttu-id="49023-171">否</span><span class="sxs-lookup"><span data-stu-id="49023-171">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-172">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49023-172">Is-Single-Valued</span></span>       | <span data-ttu-id="49023-173">對</span><span class="sxs-lookup"><span data-stu-id="49023-173">True</span></span>                                                                                                                            |
| <span data-ttu-id="49023-174">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49023-174">Is Indexed</span></span>             | <span data-ttu-id="49023-175">否</span><span class="sxs-lookup"><span data-stu-id="49023-175">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-176">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49023-176">In Global Catalog</span></span>      | <span data-ttu-id="49023-177">否</span><span class="sxs-lookup"><span data-stu-id="49023-177">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-178">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49023-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="49023-179">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49023-179">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="49023-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49023-180">Range-Lower</span></span>            | <span data-ttu-id="49023-181">1</span><span class="sxs-lookup"><span data-stu-id="49023-181">1</span></span>                                                                                                                               |
| <span data-ttu-id="49023-182">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49023-182">Range-Upper</span></span>            | <span data-ttu-id="49023-183">64</span><span class="sxs-lookup"><span data-stu-id="49023-183">64</span></span>                                                                                                                              |
| <span data-ttu-id="49023-184">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-184">Search-Flags</span></span>           | <span data-ttu-id="49023-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49023-185">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="49023-186">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-186">System-Flags</span></span>           | <span data-ttu-id="49023-187">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49023-187">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="49023-188">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49023-188">Classes used in</span></span>        | [<span data-ttu-id="49023-189">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="49023-189">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="49023-190">**居住人**</span><span class="sxs-lookup"><span data-stu-id="49023-190">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="49023-191">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="49023-191">Windows Server 2003 R2</span></span>



| <span data-ttu-id="49023-192">進入</span><span class="sxs-lookup"><span data-stu-id="49023-192">Entry</span></span> | <span data-ttu-id="49023-193">值</span><span class="sxs-lookup"><span data-stu-id="49023-193">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49023-194">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49023-194">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="49023-195">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49023-195">MAPI-Id</span></span>                | <span data-ttu-id="49023-196">0x3A17</span><span class="sxs-lookup"><span data-stu-id="49023-196">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="49023-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="49023-197">System-Only</span></span>            | <span data-ttu-id="49023-198">否</span><span class="sxs-lookup"><span data-stu-id="49023-198">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-199">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49023-199">Is-Single-Valued</span></span>       | <span data-ttu-id="49023-200">對</span><span class="sxs-lookup"><span data-stu-id="49023-200">True</span></span>                                                                                                                            |
| <span data-ttu-id="49023-201">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49023-201">Is Indexed</span></span>             | <span data-ttu-id="49023-202">否</span><span class="sxs-lookup"><span data-stu-id="49023-202">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-203">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49023-203">In Global Catalog</span></span>      | <span data-ttu-id="49023-204">否</span><span class="sxs-lookup"><span data-stu-id="49023-204">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-205">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49023-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="49023-206">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49023-206">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="49023-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49023-207">Range-Lower</span></span>            | <span data-ttu-id="49023-208">1</span><span class="sxs-lookup"><span data-stu-id="49023-208">1</span></span>                                                                                                                               |
| <span data-ttu-id="49023-209">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49023-209">Range-Upper</span></span>            | <span data-ttu-id="49023-210">64</span><span class="sxs-lookup"><span data-stu-id="49023-210">64</span></span>                                                                                                                              |
| <span data-ttu-id="49023-211">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-211">Search-Flags</span></span>           | <span data-ttu-id="49023-212">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49023-212">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="49023-213">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-213">System-Flags</span></span>           | <span data-ttu-id="49023-214">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49023-214">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="49023-215">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49023-215">Classes used in</span></span>        | [<span data-ttu-id="49023-216">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="49023-216">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="49023-217">**居住人**</span><span class="sxs-lookup"><span data-stu-id="49023-217">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="49023-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49023-218">Windows Server 2008</span></span>



| <span data-ttu-id="49023-219">進入</span><span class="sxs-lookup"><span data-stu-id="49023-219">Entry</span></span> | <span data-ttu-id="49023-220">值</span><span class="sxs-lookup"><span data-stu-id="49023-220">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49023-221">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49023-221">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="49023-222">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49023-222">MAPI-Id</span></span>                | <span data-ttu-id="49023-223">0x3A17</span><span class="sxs-lookup"><span data-stu-id="49023-223">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="49023-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="49023-224">System-Only</span></span>            | <span data-ttu-id="49023-225">否</span><span class="sxs-lookup"><span data-stu-id="49023-225">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-226">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49023-226">Is-Single-Valued</span></span>       | <span data-ttu-id="49023-227">對</span><span class="sxs-lookup"><span data-stu-id="49023-227">True</span></span>                                                                                                                            |
| <span data-ttu-id="49023-228">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49023-228">Is Indexed</span></span>             | <span data-ttu-id="49023-229">否</span><span class="sxs-lookup"><span data-stu-id="49023-229">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-230">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49023-230">In Global Catalog</span></span>      | <span data-ttu-id="49023-231">否</span><span class="sxs-lookup"><span data-stu-id="49023-231">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-232">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49023-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="49023-233">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49023-233">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="49023-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49023-234">Range-Lower</span></span>            | <span data-ttu-id="49023-235">1</span><span class="sxs-lookup"><span data-stu-id="49023-235">1</span></span>                                                                                                                               |
| <span data-ttu-id="49023-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49023-236">Range-Upper</span></span>            | <span data-ttu-id="49023-237">128</span><span class="sxs-lookup"><span data-stu-id="49023-237">128</span></span>                                                                                                                             |
| <span data-ttu-id="49023-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-238">Search-Flags</span></span>           | <span data-ttu-id="49023-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49023-239">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="49023-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-240">System-Flags</span></span>           | <span data-ttu-id="49023-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49023-241">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="49023-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49023-242">Classes used in</span></span>        | [<span data-ttu-id="49023-243">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="49023-243">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="49023-244">**居住人**</span><span class="sxs-lookup"><span data-stu-id="49023-244">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="49023-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="49023-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="49023-246">進入</span><span class="sxs-lookup"><span data-stu-id="49023-246">Entry</span></span> | <span data-ttu-id="49023-247">值</span><span class="sxs-lookup"><span data-stu-id="49023-247">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49023-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49023-248">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="49023-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49023-249">MAPI-Id</span></span>                | <span data-ttu-id="49023-250">0x3A17</span><span class="sxs-lookup"><span data-stu-id="49023-250">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="49023-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="49023-251">System-Only</span></span>            | <span data-ttu-id="49023-252">否</span><span class="sxs-lookup"><span data-stu-id="49023-252">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49023-253">Is-Single-Valued</span></span>       | <span data-ttu-id="49023-254">對</span><span class="sxs-lookup"><span data-stu-id="49023-254">True</span></span>                                                                                                                            |
| <span data-ttu-id="49023-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49023-255">Is Indexed</span></span>             | <span data-ttu-id="49023-256">否</span><span class="sxs-lookup"><span data-stu-id="49023-256">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49023-257">In Global Catalog</span></span>      | <span data-ttu-id="49023-258">否</span><span class="sxs-lookup"><span data-stu-id="49023-258">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49023-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="49023-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49023-260">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="49023-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49023-261">Range-Lower</span></span>            | <span data-ttu-id="49023-262">1</span><span class="sxs-lookup"><span data-stu-id="49023-262">1</span></span>                                                                                                                               |
| <span data-ttu-id="49023-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49023-263">Range-Upper</span></span>            | <span data-ttu-id="49023-264">128</span><span class="sxs-lookup"><span data-stu-id="49023-264">128</span></span>                                                                                                                             |
| <span data-ttu-id="49023-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-265">Search-Flags</span></span>           | <span data-ttu-id="49023-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49023-266">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="49023-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-267">System-Flags</span></span>           | <span data-ttu-id="49023-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49023-268">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="49023-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49023-269">Classes used in</span></span>        | [<span data-ttu-id="49023-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="49023-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="49023-271">**居住人**</span><span class="sxs-lookup"><span data-stu-id="49023-271">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="49023-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49023-272">Windows Server 2012</span></span>



| <span data-ttu-id="49023-273">進入</span><span class="sxs-lookup"><span data-stu-id="49023-273">Entry</span></span> | <span data-ttu-id="49023-274">值</span><span class="sxs-lookup"><span data-stu-id="49023-274">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49023-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49023-275">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="49023-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49023-276">MAPI-Id</span></span>                | <span data-ttu-id="49023-277">0x3A17</span><span class="sxs-lookup"><span data-stu-id="49023-277">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="49023-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="49023-278">System-Only</span></span>            | <span data-ttu-id="49023-279">否</span><span class="sxs-lookup"><span data-stu-id="49023-279">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49023-280">Is-Single-Valued</span></span>       | <span data-ttu-id="49023-281">對</span><span class="sxs-lookup"><span data-stu-id="49023-281">True</span></span>                                                                                                                            |
| <span data-ttu-id="49023-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49023-282">Is Indexed</span></span>             | <span data-ttu-id="49023-283">否</span><span class="sxs-lookup"><span data-stu-id="49023-283">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49023-284">In Global Catalog</span></span>      | <span data-ttu-id="49023-285">否</span><span class="sxs-lookup"><span data-stu-id="49023-285">False</span></span>                                                                                                                           |
| <span data-ttu-id="49023-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49023-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="49023-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49023-287">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="49023-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49023-288">Range-Lower</span></span>            | <span data-ttu-id="49023-289">1</span><span class="sxs-lookup"><span data-stu-id="49023-289">1</span></span>                                                                                                                               |
| <span data-ttu-id="49023-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49023-290">Range-Upper</span></span>            | <span data-ttu-id="49023-291">128</span><span class="sxs-lookup"><span data-stu-id="49023-291">128</span></span>                                                                                                                             |
| <span data-ttu-id="49023-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-292">Search-Flags</span></span>           | <span data-ttu-id="49023-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49023-293">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="49023-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49023-294">System-Flags</span></span>           | <span data-ttu-id="49023-295">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49023-295">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="49023-296">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49023-296">Classes used in</span></span>        | [<span data-ttu-id="49023-297">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="49023-297">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="49023-298">**居住人**</span><span class="sxs-lookup"><span data-stu-id="49023-298">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



 

 






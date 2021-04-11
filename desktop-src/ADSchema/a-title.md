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
# <a name="title-attribute-ad-schema"></a><span data-ttu-id="7ab7f-108">標題屬性 (AD 架構) </span><span class="sxs-lookup"><span data-stu-id="7ab7f-108">Title attribute (AD Schema)</span></span>

<span data-ttu-id="7ab7f-109">包含使用者職稱。</span><span class="sxs-lookup"><span data-stu-id="7ab7f-109">Contains the user's job title.</span></span> <span data-ttu-id="7ab7f-110">這個屬性通常用來指出正式的職稱，例如資深程式設計師，而非 occupational 類別，例如程式設計師。</span><span class="sxs-lookup"><span data-stu-id="7ab7f-110">This property is commonly used to indicate the formal job title, such as Senior Programmer, rather than occupational class, such as programmer.</span></span> <span data-ttu-id="7ab7f-111">它通常不會用於尾碼標題（例如 Esq）。</span><span class="sxs-lookup"><span data-stu-id="7ab7f-111">It is not typically used for suffix titles such as Esq.</span></span> <span data-ttu-id="7ab7f-112">或 DDS。</span><span class="sxs-lookup"><span data-stu-id="7ab7f-112">or DDS.</span></span>



| <span data-ttu-id="7ab7f-113">進入</span><span class="sxs-lookup"><span data-stu-id="7ab7f-113">Entry</span></span> | <span data-ttu-id="7ab7f-114">值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="7ab7f-115">CN</span><span class="sxs-lookup"><span data-stu-id="7ab7f-115">CN</span></span>                | <span data-ttu-id="7ab7f-116">標題</span><span class="sxs-lookup"><span data-stu-id="7ab7f-116">Title</span></span>                                                                     |
| <span data-ttu-id="7ab7f-117">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7ab7f-117">Ldap-Display-Name</span></span> | <span data-ttu-id="7ab7f-118">title</span><span class="sxs-lookup"><span data-stu-id="7ab7f-118">title</span></span>                                                                     |
| <span data-ttu-id="7ab7f-119">大小</span><span class="sxs-lookup"><span data-stu-id="7ab7f-119">Size</span></span>              | \-                                                                        |
| <span data-ttu-id="7ab7f-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7ab7f-120">Update Privilege</span></span>  | <span data-ttu-id="7ab7f-121">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="7ab7f-121">Domain administrator or account owner.</span></span>                                    |
| <span data-ttu-id="7ab7f-122">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7ab7f-122">Update Frequency</span></span>  | <span data-ttu-id="7ab7f-123">當使用者的記錄建立時，以及每次需要變更標題時。</span><span class="sxs-lookup"><span data-stu-id="7ab7f-123">When the user's record is created and whenever the title needs to change.</span></span> |
| <span data-ttu-id="7ab7f-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ab7f-124">Attribute-Id</span></span>      | <span data-ttu-id="7ab7f-125">2.5.4.12</span><span class="sxs-lookup"><span data-stu-id="7ab7f-125">2.5.4.12</span></span>                                                                  |
| <span data-ttu-id="7ab7f-126">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7ab7f-126">System-Id-Guid</span></span>    | <span data-ttu-id="7ab7f-127">bf967a55-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7ab7f-127">bf967a55-0de6-11d0-a285-00aa003049e2</span></span>                                      |
| <span data-ttu-id="7ab7f-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ab7f-128">Syntax</span></span>            | [<span data-ttu-id="7ab7f-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-129">**String(Unicode)**</span></span>](s-string-unicode.md)                               |



## <a name="implementations"></a><span data-ttu-id="7ab7f-130">實作</span><span class="sxs-lookup"><span data-stu-id="7ab7f-130">Implementations</span></span>

-   [<span data-ttu-id="7ab7f-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7ab7f-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ab7f-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ab7f-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ab7f-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ab7f-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7ab7f-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ab7f-137">Windows 2000 Server</span></span>



| <span data-ttu-id="7ab7f-138">進入</span><span class="sxs-lookup"><span data-stu-id="7ab7f-138">Entry</span></span> | <span data-ttu-id="7ab7f-139">值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab7f-140">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ab7f-140">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="7ab7f-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ab7f-141">MAPI-Id</span></span>                | <span data-ttu-id="7ab7f-142">0x3A17</span><span class="sxs-lookup"><span data-stu-id="7ab7f-142">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="7ab7f-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ab7f-143">System-Only</span></span>            | <span data-ttu-id="7ab7f-144">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-144">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-145">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-145">Is-Single-Valued</span></span>       | <span data-ttu-id="7ab7f-146">對</span><span class="sxs-lookup"><span data-stu-id="7ab7f-146">True</span></span>                                                                                                                            |
| <span data-ttu-id="7ab7f-147">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ab7f-147">Is Indexed</span></span>             | <span data-ttu-id="7ab7f-148">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-148">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-149">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ab7f-149">In Global Catalog</span></span>      | <span data-ttu-id="7ab7f-150">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-150">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-151">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ab7f-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ab7f-152">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ab7f-152">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="7ab7f-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ab7f-153">Range-Lower</span></span>            | <span data-ttu-id="7ab7f-154">1</span><span class="sxs-lookup"><span data-stu-id="7ab7f-154">1</span></span>                                                                                                                               |
| <span data-ttu-id="7ab7f-155">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ab7f-155">Range-Upper</span></span>            | <span data-ttu-id="7ab7f-156">64</span><span class="sxs-lookup"><span data-stu-id="7ab7f-156">64</span></span>                                                                                                                              |
| <span data-ttu-id="7ab7f-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-157">Search-Flags</span></span>           | <span data-ttu-id="7ab7f-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ab7f-158">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-159">System-Flags</span></span>           | <span data-ttu-id="7ab7f-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ab7f-160">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-161">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ab7f-161">Classes used in</span></span>        | [<span data-ttu-id="7ab7f-162">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-162">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="7ab7f-163">**居住人**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-163">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7ab7f-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ab7f-164">Windows Server 2003</span></span>



| <span data-ttu-id="7ab7f-165">進入</span><span class="sxs-lookup"><span data-stu-id="7ab7f-165">Entry</span></span> | <span data-ttu-id="7ab7f-166">值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-166">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab7f-167">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ab7f-167">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="7ab7f-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ab7f-168">MAPI-Id</span></span>                | <span data-ttu-id="7ab7f-169">0x3A17</span><span class="sxs-lookup"><span data-stu-id="7ab7f-169">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="7ab7f-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ab7f-170">System-Only</span></span>            | <span data-ttu-id="7ab7f-171">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-171">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-172">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-172">Is-Single-Valued</span></span>       | <span data-ttu-id="7ab7f-173">對</span><span class="sxs-lookup"><span data-stu-id="7ab7f-173">True</span></span>                                                                                                                            |
| <span data-ttu-id="7ab7f-174">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ab7f-174">Is Indexed</span></span>             | <span data-ttu-id="7ab7f-175">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-175">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-176">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ab7f-176">In Global Catalog</span></span>      | <span data-ttu-id="7ab7f-177">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-177">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-178">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ab7f-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ab7f-179">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ab7f-179">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="7ab7f-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ab7f-180">Range-Lower</span></span>            | <span data-ttu-id="7ab7f-181">1</span><span class="sxs-lookup"><span data-stu-id="7ab7f-181">1</span></span>                                                                                                                               |
| <span data-ttu-id="7ab7f-182">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ab7f-182">Range-Upper</span></span>            | <span data-ttu-id="7ab7f-183">64</span><span class="sxs-lookup"><span data-stu-id="7ab7f-183">64</span></span>                                                                                                                              |
| <span data-ttu-id="7ab7f-184">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-184">Search-Flags</span></span>           | <span data-ttu-id="7ab7f-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ab7f-185">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-186">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-186">System-Flags</span></span>           | <span data-ttu-id="7ab7f-187">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ab7f-187">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-188">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ab7f-188">Classes used in</span></span>        | [<span data-ttu-id="7ab7f-189">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-189">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="7ab7f-190">**居住人**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-190">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ab7f-191">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ab7f-191">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ab7f-192">進入</span><span class="sxs-lookup"><span data-stu-id="7ab7f-192">Entry</span></span> | <span data-ttu-id="7ab7f-193">值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-193">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab7f-194">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ab7f-194">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="7ab7f-195">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ab7f-195">MAPI-Id</span></span>                | <span data-ttu-id="7ab7f-196">0x3A17</span><span class="sxs-lookup"><span data-stu-id="7ab7f-196">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="7ab7f-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ab7f-197">System-Only</span></span>            | <span data-ttu-id="7ab7f-198">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-198">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-199">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-199">Is-Single-Valued</span></span>       | <span data-ttu-id="7ab7f-200">對</span><span class="sxs-lookup"><span data-stu-id="7ab7f-200">True</span></span>                                                                                                                            |
| <span data-ttu-id="7ab7f-201">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ab7f-201">Is Indexed</span></span>             | <span data-ttu-id="7ab7f-202">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-202">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-203">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ab7f-203">In Global Catalog</span></span>      | <span data-ttu-id="7ab7f-204">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-204">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-205">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ab7f-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ab7f-206">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ab7f-206">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="7ab7f-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ab7f-207">Range-Lower</span></span>            | <span data-ttu-id="7ab7f-208">1</span><span class="sxs-lookup"><span data-stu-id="7ab7f-208">1</span></span>                                                                                                                               |
| <span data-ttu-id="7ab7f-209">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ab7f-209">Range-Upper</span></span>            | <span data-ttu-id="7ab7f-210">64</span><span class="sxs-lookup"><span data-stu-id="7ab7f-210">64</span></span>                                                                                                                              |
| <span data-ttu-id="7ab7f-211">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-211">Search-Flags</span></span>           | <span data-ttu-id="7ab7f-212">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ab7f-212">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-213">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-213">System-Flags</span></span>           | <span data-ttu-id="7ab7f-214">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ab7f-214">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-215">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ab7f-215">Classes used in</span></span>        | [<span data-ttu-id="7ab7f-216">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-216">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="7ab7f-217">**居住人**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-217">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ab7f-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ab7f-218">Windows Server 2008</span></span>



| <span data-ttu-id="7ab7f-219">進入</span><span class="sxs-lookup"><span data-stu-id="7ab7f-219">Entry</span></span> | <span data-ttu-id="7ab7f-220">值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-220">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab7f-221">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ab7f-221">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="7ab7f-222">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ab7f-222">MAPI-Id</span></span>                | <span data-ttu-id="7ab7f-223">0x3A17</span><span class="sxs-lookup"><span data-stu-id="7ab7f-223">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="7ab7f-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ab7f-224">System-Only</span></span>            | <span data-ttu-id="7ab7f-225">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-225">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-226">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-226">Is-Single-Valued</span></span>       | <span data-ttu-id="7ab7f-227">對</span><span class="sxs-lookup"><span data-stu-id="7ab7f-227">True</span></span>                                                                                                                            |
| <span data-ttu-id="7ab7f-228">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ab7f-228">Is Indexed</span></span>             | <span data-ttu-id="7ab7f-229">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-229">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-230">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ab7f-230">In Global Catalog</span></span>      | <span data-ttu-id="7ab7f-231">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-231">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-232">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ab7f-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ab7f-233">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ab7f-233">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="7ab7f-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ab7f-234">Range-Lower</span></span>            | <span data-ttu-id="7ab7f-235">1</span><span class="sxs-lookup"><span data-stu-id="7ab7f-235">1</span></span>                                                                                                                               |
| <span data-ttu-id="7ab7f-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ab7f-236">Range-Upper</span></span>            | <span data-ttu-id="7ab7f-237">128</span><span class="sxs-lookup"><span data-stu-id="7ab7f-237">128</span></span>                                                                                                                             |
| <span data-ttu-id="7ab7f-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-238">Search-Flags</span></span>           | <span data-ttu-id="7ab7f-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ab7f-239">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-240">System-Flags</span></span>           | <span data-ttu-id="7ab7f-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ab7f-241">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ab7f-242">Classes used in</span></span>        | [<span data-ttu-id="7ab7f-243">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-243">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="7ab7f-244">**居住人**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-244">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ab7f-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ab7f-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ab7f-246">進入</span><span class="sxs-lookup"><span data-stu-id="7ab7f-246">Entry</span></span> | <span data-ttu-id="7ab7f-247">值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-247">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab7f-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ab7f-248">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="7ab7f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ab7f-249">MAPI-Id</span></span>                | <span data-ttu-id="7ab7f-250">0x3A17</span><span class="sxs-lookup"><span data-stu-id="7ab7f-250">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="7ab7f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ab7f-251">System-Only</span></span>            | <span data-ttu-id="7ab7f-252">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-252">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7ab7f-254">對</span><span class="sxs-lookup"><span data-stu-id="7ab7f-254">True</span></span>                                                                                                                            |
| <span data-ttu-id="7ab7f-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ab7f-255">Is Indexed</span></span>             | <span data-ttu-id="7ab7f-256">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-256">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ab7f-257">In Global Catalog</span></span>      | <span data-ttu-id="7ab7f-258">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-258">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ab7f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ab7f-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ab7f-260">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="7ab7f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ab7f-261">Range-Lower</span></span>            | <span data-ttu-id="7ab7f-262">1</span><span class="sxs-lookup"><span data-stu-id="7ab7f-262">1</span></span>                                                                                                                               |
| <span data-ttu-id="7ab7f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ab7f-263">Range-Upper</span></span>            | <span data-ttu-id="7ab7f-264">128</span><span class="sxs-lookup"><span data-stu-id="7ab7f-264">128</span></span>                                                                                                                             |
| <span data-ttu-id="7ab7f-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-265">Search-Flags</span></span>           | <span data-ttu-id="7ab7f-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ab7f-266">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-267">System-Flags</span></span>           | <span data-ttu-id="7ab7f-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ab7f-268">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ab7f-269">Classes used in</span></span>        | [<span data-ttu-id="7ab7f-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="7ab7f-271">**居住人**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-271">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ab7f-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ab7f-272">Windows Server 2012</span></span>



| <span data-ttu-id="7ab7f-273">進入</span><span class="sxs-lookup"><span data-stu-id="7ab7f-273">Entry</span></span> | <span data-ttu-id="7ab7f-274">值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-274">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab7f-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ab7f-275">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="7ab7f-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ab7f-276">MAPI-Id</span></span>                | <span data-ttu-id="7ab7f-277">0x3A17</span><span class="sxs-lookup"><span data-stu-id="7ab7f-277">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="7ab7f-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ab7f-278">System-Only</span></span>            | <span data-ttu-id="7ab7f-279">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-279">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ab7f-280">Is-Single-Valued</span></span>       | <span data-ttu-id="7ab7f-281">對</span><span class="sxs-lookup"><span data-stu-id="7ab7f-281">True</span></span>                                                                                                                            |
| <span data-ttu-id="7ab7f-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ab7f-282">Is Indexed</span></span>             | <span data-ttu-id="7ab7f-283">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-283">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ab7f-284">In Global Catalog</span></span>      | <span data-ttu-id="7ab7f-285">否</span><span class="sxs-lookup"><span data-stu-id="7ab7f-285">False</span></span>                                                                                                                           |
| <span data-ttu-id="7ab7f-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ab7f-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ab7f-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ab7f-287">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="7ab7f-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ab7f-288">Range-Lower</span></span>            | <span data-ttu-id="7ab7f-289">1</span><span class="sxs-lookup"><span data-stu-id="7ab7f-289">1</span></span>                                                                                                                               |
| <span data-ttu-id="7ab7f-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ab7f-290">Range-Upper</span></span>            | <span data-ttu-id="7ab7f-291">128</span><span class="sxs-lookup"><span data-stu-id="7ab7f-291">128</span></span>                                                                                                                             |
| <span data-ttu-id="7ab7f-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-292">Search-Flags</span></span>           | <span data-ttu-id="7ab7f-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ab7f-293">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ab7f-294">System-Flags</span></span>           | <span data-ttu-id="7ab7f-295">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ab7f-295">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="7ab7f-296">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ab7f-296">Classes used in</span></span>        | [<span data-ttu-id="7ab7f-297">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-297">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="7ab7f-298">**居住人**</span><span class="sxs-lookup"><span data-stu-id="7ab7f-298">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



 

 






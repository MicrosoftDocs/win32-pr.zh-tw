---
title: DS-UI-管理通知屬性
description: 這是 COM 物件的 Guid 清單，支援在物件上透過 UI 執行動作時 DSAdmin 呼叫的回呼介面。
ms.assetid: 4845c221-087f-49f5-a95d-71f58a4e8819
ms.tgt_platform: multiple
keywords:
- DS-UI-管理-通知屬性 AD 架構
- dSUIAdminNotification 屬性 AD 架構
topic_type:
- apiref
api_name:
- DS-UI-Admin-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7082d7a8fd751fa001ac796d2a86b60a28463e8b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970246"
---
# <a name="ds-ui-admin-notification-attribute"></a><span data-ttu-id="1a012-105">DS-UI-管理通知屬性</span><span class="sxs-lookup"><span data-stu-id="1a012-105">DS-UI-Admin-Notification attribute</span></span>

<span data-ttu-id="1a012-106">這是 COM 物件的 Guid 清單，支援在物件上透過 UI 執行動作時 DSAdmin 呼叫的回呼介面。</span><span class="sxs-lookup"><span data-stu-id="1a012-106">This is a list of the GUIDs of COM objects that support a callback interface that DSAdmin calls when an action has occurred on an object through the UI.</span></span>



| <span data-ttu-id="1a012-107">進入</span><span class="sxs-lookup"><span data-stu-id="1a012-107">Entry</span></span> | <span data-ttu-id="1a012-108">值</span><span class="sxs-lookup"><span data-stu-id="1a012-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1a012-109">CN</span><span class="sxs-lookup"><span data-stu-id="1a012-109">CN</span></span>                | <span data-ttu-id="1a012-110">DS-UI-系統管理-通知</span><span class="sxs-lookup"><span data-stu-id="1a012-110">DS-UI-Admin-Notification</span></span>                    |
| <span data-ttu-id="1a012-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1a012-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1a012-112">dSUIAdminNotification</span><span class="sxs-lookup"><span data-stu-id="1a012-112">dSUIAdminNotification</span></span>                       |
| <span data-ttu-id="1a012-113">大小</span><span class="sxs-lookup"><span data-stu-id="1a012-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1a012-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1a012-114">Update Privilege</span></span>  | <span data-ttu-id="1a012-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="1a012-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="1a012-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1a012-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1a012-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1a012-117">Attribute-Id</span></span>      | <span data-ttu-id="1a012-118">1.2.840.113556.1.4.1343</span><span class="sxs-lookup"><span data-stu-id="1a012-118">1.2.840.113556.1.4.1343</span></span>                     |
| <span data-ttu-id="1a012-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1a012-119">System-Id-Guid</span></span>    | <span data-ttu-id="1a012-120">f6ea0a94-6f91-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="1a012-120">f6ea0a94-6f91-11d2-9905-0000f87a57d4</span></span>        |
| <span data-ttu-id="1a012-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a012-121">Syntax</span></span>            | [<span data-ttu-id="1a012-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1a012-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1a012-123">實作</span><span class="sxs-lookup"><span data-stu-id="1a012-123">Implementations</span></span>

-   [<span data-ttu-id="1a012-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1a012-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1a012-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1a012-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1a012-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1a012-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1a012-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1a012-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1a012-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1a012-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1a012-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1a012-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1a012-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1a012-130">Windows 2000 Server</span></span>



| <span data-ttu-id="1a012-131">進入</span><span class="sxs-lookup"><span data-stu-id="1a012-131">Entry</span></span> | <span data-ttu-id="1a012-132">值</span><span class="sxs-lookup"><span data-stu-id="1a012-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1a012-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a012-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a012-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a012-135">System-Only</span></span>            | <span data-ttu-id="1a012-136">否</span><span class="sxs-lookup"><span data-stu-id="1a012-136">False</span></span>                                               |
| <span data-ttu-id="1a012-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a012-137">Is-Single-Valued</span></span>       | <span data-ttu-id="1a012-138">否</span><span class="sxs-lookup"><span data-stu-id="1a012-138">False</span></span>                                               |
| <span data-ttu-id="1a012-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a012-139">Is Indexed</span></span>             | <span data-ttu-id="1a012-140">否</span><span class="sxs-lookup"><span data-stu-id="1a012-140">False</span></span>                                               |
| <span data-ttu-id="1a012-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a012-141">In Global Catalog</span></span>      | <span data-ttu-id="1a012-142">否</span><span class="sxs-lookup"><span data-stu-id="1a012-142">False</span></span>                                               |
| <span data-ttu-id="1a012-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a012-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a012-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a012-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1a012-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a012-145">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a012-146">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-147">Search-Flags</span></span>           | <span data-ttu-id="1a012-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a012-148">0x00000000</span></span>                                          |
| <span data-ttu-id="1a012-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-149">System-Flags</span></span>           | <span data-ttu-id="1a012-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a012-150">0x00000010</span></span>                                          |
| <span data-ttu-id="1a012-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a012-151">Classes used in</span></span>        | [<span data-ttu-id="1a012-152">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1a012-152">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1a012-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1a012-153">Windows Server 2003</span></span>



| <span data-ttu-id="1a012-154">進入</span><span class="sxs-lookup"><span data-stu-id="1a012-154">Entry</span></span> | <span data-ttu-id="1a012-155">值</span><span class="sxs-lookup"><span data-stu-id="1a012-155">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1a012-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a012-156">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a012-157">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a012-158">System-Only</span></span>            | <span data-ttu-id="1a012-159">否</span><span class="sxs-lookup"><span data-stu-id="1a012-159">False</span></span>                                               |
| <span data-ttu-id="1a012-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a012-160">Is-Single-Valued</span></span>       | <span data-ttu-id="1a012-161">否</span><span class="sxs-lookup"><span data-stu-id="1a012-161">False</span></span>                                               |
| <span data-ttu-id="1a012-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a012-162">Is Indexed</span></span>             | <span data-ttu-id="1a012-163">否</span><span class="sxs-lookup"><span data-stu-id="1a012-163">False</span></span>                                               |
| <span data-ttu-id="1a012-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a012-164">In Global Catalog</span></span>      | <span data-ttu-id="1a012-165">否</span><span class="sxs-lookup"><span data-stu-id="1a012-165">False</span></span>                                               |
| <span data-ttu-id="1a012-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a012-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a012-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a012-167">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1a012-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a012-168">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a012-169">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-170">Search-Flags</span></span>           | <span data-ttu-id="1a012-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a012-171">0x00000000</span></span>                                          |
| <span data-ttu-id="1a012-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-172">System-Flags</span></span>           | <span data-ttu-id="1a012-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a012-173">0x00000010</span></span>                                          |
| <span data-ttu-id="1a012-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a012-174">Classes used in</span></span>        | [<span data-ttu-id="1a012-175">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1a012-175">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1a012-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1a012-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1a012-177">進入</span><span class="sxs-lookup"><span data-stu-id="1a012-177">Entry</span></span> | <span data-ttu-id="1a012-178">值</span><span class="sxs-lookup"><span data-stu-id="1a012-178">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1a012-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a012-179">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a012-180">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a012-181">System-Only</span></span>            | <span data-ttu-id="1a012-182">否</span><span class="sxs-lookup"><span data-stu-id="1a012-182">False</span></span>                                               |
| <span data-ttu-id="1a012-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a012-183">Is-Single-Valued</span></span>       | <span data-ttu-id="1a012-184">否</span><span class="sxs-lookup"><span data-stu-id="1a012-184">False</span></span>                                               |
| <span data-ttu-id="1a012-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a012-185">Is Indexed</span></span>             | <span data-ttu-id="1a012-186">否</span><span class="sxs-lookup"><span data-stu-id="1a012-186">False</span></span>                                               |
| <span data-ttu-id="1a012-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a012-187">In Global Catalog</span></span>      | <span data-ttu-id="1a012-188">否</span><span class="sxs-lookup"><span data-stu-id="1a012-188">False</span></span>                                               |
| <span data-ttu-id="1a012-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a012-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a012-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a012-190">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1a012-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a012-191">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a012-192">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-193">Search-Flags</span></span>           | <span data-ttu-id="1a012-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a012-194">0x00000000</span></span>                                          |
| <span data-ttu-id="1a012-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-195">System-Flags</span></span>           | <span data-ttu-id="1a012-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a012-196">0x00000010</span></span>                                          |
| <span data-ttu-id="1a012-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a012-197">Classes used in</span></span>        | [<span data-ttu-id="1a012-198">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1a012-198">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1a012-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a012-199">Windows Server 2008</span></span>



| <span data-ttu-id="1a012-200">進入</span><span class="sxs-lookup"><span data-stu-id="1a012-200">Entry</span></span> | <span data-ttu-id="1a012-201">值</span><span class="sxs-lookup"><span data-stu-id="1a012-201">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1a012-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a012-202">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a012-203">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a012-204">System-Only</span></span>            | <span data-ttu-id="1a012-205">否</span><span class="sxs-lookup"><span data-stu-id="1a012-205">False</span></span>                                               |
| <span data-ttu-id="1a012-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a012-206">Is-Single-Valued</span></span>       | <span data-ttu-id="1a012-207">否</span><span class="sxs-lookup"><span data-stu-id="1a012-207">False</span></span>                                               |
| <span data-ttu-id="1a012-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a012-208">Is Indexed</span></span>             | <span data-ttu-id="1a012-209">否</span><span class="sxs-lookup"><span data-stu-id="1a012-209">False</span></span>                                               |
| <span data-ttu-id="1a012-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a012-210">In Global Catalog</span></span>      | <span data-ttu-id="1a012-211">否</span><span class="sxs-lookup"><span data-stu-id="1a012-211">False</span></span>                                               |
| <span data-ttu-id="1a012-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a012-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a012-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a012-213">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1a012-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a012-214">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a012-215">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-216">Search-Flags</span></span>           | <span data-ttu-id="1a012-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a012-217">0x00000000</span></span>                                          |
| <span data-ttu-id="1a012-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-218">System-Flags</span></span>           | <span data-ttu-id="1a012-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a012-219">0x00000010</span></span>                                          |
| <span data-ttu-id="1a012-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a012-220">Classes used in</span></span>        | [<span data-ttu-id="1a012-221">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1a012-221">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1a012-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1a012-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1a012-223">進入</span><span class="sxs-lookup"><span data-stu-id="1a012-223">Entry</span></span> | <span data-ttu-id="1a012-224">值</span><span class="sxs-lookup"><span data-stu-id="1a012-224">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1a012-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a012-225">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a012-226">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a012-227">System-Only</span></span>            | <span data-ttu-id="1a012-228">否</span><span class="sxs-lookup"><span data-stu-id="1a012-228">False</span></span>                                               |
| <span data-ttu-id="1a012-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a012-229">Is-Single-Valued</span></span>       | <span data-ttu-id="1a012-230">否</span><span class="sxs-lookup"><span data-stu-id="1a012-230">False</span></span>                                               |
| <span data-ttu-id="1a012-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a012-231">Is Indexed</span></span>             | <span data-ttu-id="1a012-232">否</span><span class="sxs-lookup"><span data-stu-id="1a012-232">False</span></span>                                               |
| <span data-ttu-id="1a012-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a012-233">In Global Catalog</span></span>      | <span data-ttu-id="1a012-234">否</span><span class="sxs-lookup"><span data-stu-id="1a012-234">False</span></span>                                               |
| <span data-ttu-id="1a012-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a012-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a012-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a012-236">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1a012-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a012-237">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a012-238">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-239">Search-Flags</span></span>           | <span data-ttu-id="1a012-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a012-240">0x00000000</span></span>                                          |
| <span data-ttu-id="1a012-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-241">System-Flags</span></span>           | <span data-ttu-id="1a012-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a012-242">0x00000010</span></span>                                          |
| <span data-ttu-id="1a012-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a012-243">Classes used in</span></span>        | [<span data-ttu-id="1a012-244">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1a012-244">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1a012-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1a012-245">Windows Server 2012</span></span>



| <span data-ttu-id="1a012-246">進入</span><span class="sxs-lookup"><span data-stu-id="1a012-246">Entry</span></span> | <span data-ttu-id="1a012-247">值</span><span class="sxs-lookup"><span data-stu-id="1a012-247">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="1a012-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a012-248">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a012-249">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="1a012-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a012-250">System-Only</span></span>            | <span data-ttu-id="1a012-251">否</span><span class="sxs-lookup"><span data-stu-id="1a012-251">False</span></span>                                               |
| <span data-ttu-id="1a012-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a012-252">Is-Single-Valued</span></span>       | <span data-ttu-id="1a012-253">否</span><span class="sxs-lookup"><span data-stu-id="1a012-253">False</span></span>                                               |
| <span data-ttu-id="1a012-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a012-254">Is Indexed</span></span>             | <span data-ttu-id="1a012-255">否</span><span class="sxs-lookup"><span data-stu-id="1a012-255">False</span></span>                                               |
| <span data-ttu-id="1a012-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a012-256">In Global Catalog</span></span>      | <span data-ttu-id="1a012-257">否</span><span class="sxs-lookup"><span data-stu-id="1a012-257">False</span></span>                                               |
| <span data-ttu-id="1a012-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a012-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a012-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a012-259">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="1a012-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a012-260">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a012-261">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="1a012-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-262">Search-Flags</span></span>           | <span data-ttu-id="1a012-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a012-263">0x00000000</span></span>                                          |
| <span data-ttu-id="1a012-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a012-264">System-Flags</span></span>           | <span data-ttu-id="1a012-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a012-265">0x00000010</span></span>                                          |
| <span data-ttu-id="1a012-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a012-266">Classes used in</span></span>        | [<span data-ttu-id="1a012-267">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="1a012-267">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



 

 






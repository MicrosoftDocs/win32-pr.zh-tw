---
title: 知名物件屬性
description: 此屬性包含依 GUID 和辨別名稱的已知物件容器清單。
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- 知名物件屬性的 AD 架構
- wellKnownObjects 屬性 AD 架構
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467310"
---
# <a name="well-known-objects-attribute"></a><span data-ttu-id="00ec7-105">知名物件屬性</span><span class="sxs-lookup"><span data-stu-id="00ec7-105">Well-Known-Objects attribute</span></span>

<span data-ttu-id="00ec7-106">此屬性包含依 GUID 和辨別名稱的已知物件容器清單。</span><span class="sxs-lookup"><span data-stu-id="00ec7-106">This attribute contains a list of well-known object containers by GUID and distinguished name.</span></span> <span data-ttu-id="00ec7-107">已知的物件是系統容器。</span><span class="sxs-lookup"><span data-stu-id="00ec7-107">The well-known objects are system containers.</span></span> <span data-ttu-id="00ec7-108">這項資訊是用來在只使用 GUID 和功能變數名稱移動之後，用來取出物件。</span><span class="sxs-lookup"><span data-stu-id="00ec7-108">This information is used to retrieve an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="00ec7-109">當移動物件時，系統會自動更新參考物件之已知物件值的分辨名稱部分。</span><span class="sxs-lookup"><span data-stu-id="00ec7-109">Whenever the object is moved, the system automatically updates the Distinguished Name portion of the Well-Known-Objects values that referred to the object.</span></span> <span data-ttu-id="00ec7-110">Ntdsapi 檔案包含下列定義，可用來取出物件 (與這些物件相關聯的 Guid 會包含在 Ntdsapi 中) ：</span><span class="sxs-lookup"><span data-stu-id="00ec7-110">The file Ntdsapi.h contains the following definitions, which can be used to retrieve an object (the GUIDs that are associated to these objects are contained in Ntdsapi.h):</span></span>

-   <span data-ttu-id="00ec7-111">GUID \_ 使用者 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-111">GUID\_USERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-112">GUID \_ COMPUTRS \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-112">GUID\_COMPUTRS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-113">GUID \_ 系統 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-113">GUID\_SYSTEMS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-114">GUID \_ 域 \_ 控制器 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-114">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-115">GUID \_ 基礎結構 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-115">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-116">GUID \_ 刪除的 \_ 物件 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-116">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-117">GUID \_ LOSTANDFOUND \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-117">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-118">GUID \_ FOREIGNSECURITYPRINCIPALS \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-118">GUID\_FOREIGNSECURITYPRINCIPALS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-119">GUID \_ 程式 \_ 資料 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-119">GUID\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-120">GUID \_ MICROSOFT \_ 程式 \_ 資料 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-120">GUID\_MICROSOFT\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="00ec7-121">GUID \_ NTDS \_ 配額 \_ 容器 \_ W</span><span class="sxs-lookup"><span data-stu-id="00ec7-121">GUID\_NTDS\_QUOTAS\_CONTAINER\_W</span></span>



| <span data-ttu-id="00ec7-122">進入</span><span class="sxs-lookup"><span data-stu-id="00ec7-122">Entry</span></span> | <span data-ttu-id="00ec7-123">值</span><span class="sxs-lookup"><span data-stu-id="00ec7-123">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="00ec7-124">CN</span><span class="sxs-lookup"><span data-stu-id="00ec7-124">CN</span></span>                | <span data-ttu-id="00ec7-125">知名物件</span><span class="sxs-lookup"><span data-stu-id="00ec7-125">Well-Known-Objects</span></span>                              |
| <span data-ttu-id="00ec7-126">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="00ec7-126">Ldap-Display-Name</span></span> | <span data-ttu-id="00ec7-127">wellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="00ec7-127">wellKnownObjects</span></span>                                |
| <span data-ttu-id="00ec7-128">大小</span><span class="sxs-lookup"><span data-stu-id="00ec7-128">Size</span></span>              | \-                                              |
| <span data-ttu-id="00ec7-129">更新許可權</span><span class="sxs-lookup"><span data-stu-id="00ec7-129">Update Privilege</span></span>  | <span data-ttu-id="00ec7-130">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="00ec7-130">This value is set by the system.</span></span>                |
| <span data-ttu-id="00ec7-131">更新頻率</span><span class="sxs-lookup"><span data-stu-id="00ec7-131">Update Frequency</span></span>  | <span data-ttu-id="00ec7-132">每次移動其中一個系統容器時。</span><span class="sxs-lookup"><span data-stu-id="00ec7-132">Whenever one of the system containers is moved.</span></span> |
| <span data-ttu-id="00ec7-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="00ec7-133">Attribute-Id</span></span>      | <span data-ttu-id="00ec7-134">1.2.840.113556.1.4.618</span><span class="sxs-lookup"><span data-stu-id="00ec7-134">1.2.840.113556.1.4.618</span></span>                          |
| <span data-ttu-id="00ec7-135">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="00ec7-135">System-Id-Guid</span></span>    | <span data-ttu-id="00ec7-136">05308983-7688-11d1-aded-00c04fd8d5cd</span><span class="sxs-lookup"><span data-stu-id="00ec7-136">05308983-7688-11d1-aded-00c04fd8d5cd</span></span>            |
| <span data-ttu-id="00ec7-137">Syntax</span><span class="sxs-lookup"><span data-stu-id="00ec7-137">Syntax</span></span>            | [<span data-ttu-id="00ec7-138">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="00ec7-138">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="00ec7-139">實作</span><span class="sxs-lookup"><span data-stu-id="00ec7-139">Implementations</span></span>

-   [<span data-ttu-id="00ec7-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="00ec7-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="00ec7-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="00ec7-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="00ec7-142">**亞當**</span><span class="sxs-lookup"><span data-stu-id="00ec7-142">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="00ec7-143">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="00ec7-143">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="00ec7-144">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="00ec7-144">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="00ec7-145">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="00ec7-145">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="00ec7-146">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="00ec7-146">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="00ec7-147">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00ec7-147">Windows 2000 Server</span></span>



| <span data-ttu-id="00ec7-148">進入</span><span class="sxs-lookup"><span data-stu-id="00ec7-148">Entry</span></span> | <span data-ttu-id="00ec7-149">值</span><span class="sxs-lookup"><span data-stu-id="00ec7-149">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00ec7-150">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00ec7-150">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-151">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00ec7-151">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-152">System-Only</span><span class="sxs-lookup"><span data-stu-id="00ec7-152">System-Only</span></span>            | <span data-ttu-id="00ec7-153">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-153">True</span></span>                            |
| <span data-ttu-id="00ec7-154">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00ec7-154">Is-Single-Valued</span></span>       | <span data-ttu-id="00ec7-155">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-155">False</span></span>                           |
| <span data-ttu-id="00ec7-156">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00ec7-156">Is Indexed</span></span>             | <span data-ttu-id="00ec7-157">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-157">False</span></span>                           |
| <span data-ttu-id="00ec7-158">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00ec7-158">In Global Catalog</span></span>      | <span data-ttu-id="00ec7-159">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-159">True</span></span>                            |
| <span data-ttu-id="00ec7-160">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00ec7-160">NT-Security-Descriptor</span></span> | <span data-ttu-id="00ec7-161">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00ec7-161">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00ec7-162">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00ec7-162">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00ec7-163">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00ec7-163">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00ec7-164">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-164">Search-Flags</span></span>           | <span data-ttu-id="00ec7-165">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00ec7-165">0x00000000</span></span>                      |
| <span data-ttu-id="00ec7-166">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-166">System-Flags</span></span>           | <span data-ttu-id="00ec7-167">0x00000012</span><span class="sxs-lookup"><span data-stu-id="00ec7-167">0x00000012</span></span>                      |
| <span data-ttu-id="00ec7-168">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00ec7-168">Classes used in</span></span>        | [<span data-ttu-id="00ec7-169">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00ec7-169">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="00ec7-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00ec7-170">Windows Server 2003</span></span>



| <span data-ttu-id="00ec7-171">進入</span><span class="sxs-lookup"><span data-stu-id="00ec7-171">Entry</span></span> | <span data-ttu-id="00ec7-172">值</span><span class="sxs-lookup"><span data-stu-id="00ec7-172">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00ec7-173">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00ec7-173">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-174">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00ec7-174">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-175">System-Only</span><span class="sxs-lookup"><span data-stu-id="00ec7-175">System-Only</span></span>            | <span data-ttu-id="00ec7-176">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-176">True</span></span>                            |
| <span data-ttu-id="00ec7-177">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00ec7-177">Is-Single-Valued</span></span>       | <span data-ttu-id="00ec7-178">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-178">False</span></span>                           |
| <span data-ttu-id="00ec7-179">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00ec7-179">Is Indexed</span></span>             | <span data-ttu-id="00ec7-180">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-180">False</span></span>                           |
| <span data-ttu-id="00ec7-181">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00ec7-181">In Global Catalog</span></span>      | <span data-ttu-id="00ec7-182">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-182">True</span></span>                            |
| <span data-ttu-id="00ec7-183">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00ec7-183">NT-Security-Descriptor</span></span> | <span data-ttu-id="00ec7-184">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00ec7-184">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00ec7-185">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00ec7-185">Range-Lower</span></span>            | <span data-ttu-id="00ec7-186">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-186">16</span></span>                              |
| <span data-ttu-id="00ec7-187">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00ec7-187">Range-Upper</span></span>            | <span data-ttu-id="00ec7-188">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-188">16</span></span>                              |
| <span data-ttu-id="00ec7-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-189">Search-Flags</span></span>           | <span data-ttu-id="00ec7-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00ec7-190">0x00000000</span></span>                      |
| <span data-ttu-id="00ec7-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-191">System-Flags</span></span>           | <span data-ttu-id="00ec7-192">0x00000012</span><span class="sxs-lookup"><span data-stu-id="00ec7-192">0x00000012</span></span>                      |
| <span data-ttu-id="00ec7-193">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00ec7-193">Classes used in</span></span>        | [<span data-ttu-id="00ec7-194">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00ec7-194">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="00ec7-195">亞當</span><span class="sxs-lookup"><span data-stu-id="00ec7-195">ADAM</span></span>



| <span data-ttu-id="00ec7-196">進入</span><span class="sxs-lookup"><span data-stu-id="00ec7-196">Entry</span></span> | <span data-ttu-id="00ec7-197">值</span><span class="sxs-lookup"><span data-stu-id="00ec7-197">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00ec7-198">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00ec7-198">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00ec7-199">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="00ec7-200">System-Only</span></span>            | <span data-ttu-id="00ec7-201">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-201">True</span></span>                            |
| <span data-ttu-id="00ec7-202">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00ec7-202">Is-Single-Valued</span></span>       | <span data-ttu-id="00ec7-203">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-203">False</span></span>                           |
| <span data-ttu-id="00ec7-204">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00ec7-204">Is Indexed</span></span>             | <span data-ttu-id="00ec7-205">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-205">False</span></span>                           |
| <span data-ttu-id="00ec7-206">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00ec7-206">In Global Catalog</span></span>      | <span data-ttu-id="00ec7-207">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-207">True</span></span>                            |
| <span data-ttu-id="00ec7-208">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00ec7-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="00ec7-209">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00ec7-209">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00ec7-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00ec7-210">Range-Lower</span></span>            | <span data-ttu-id="00ec7-211">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-211">16</span></span>                              |
| <span data-ttu-id="00ec7-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00ec7-212">Range-Upper</span></span>            | <span data-ttu-id="00ec7-213">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-213">16</span></span>                              |
| <span data-ttu-id="00ec7-214">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-214">Search-Flags</span></span>           | <span data-ttu-id="00ec7-215">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00ec7-215">0x00000000</span></span>                      |
| <span data-ttu-id="00ec7-216">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-216">System-Flags</span></span>           | <span data-ttu-id="00ec7-217">0x00000012</span><span class="sxs-lookup"><span data-stu-id="00ec7-217">0x00000012</span></span>                      |
| <span data-ttu-id="00ec7-218">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00ec7-218">Classes used in</span></span>        | [<span data-ttu-id="00ec7-219">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00ec7-219">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="00ec7-220">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="00ec7-220">Windows Server 2003 R2</span></span>



| <span data-ttu-id="00ec7-221">進入</span><span class="sxs-lookup"><span data-stu-id="00ec7-221">Entry</span></span> | <span data-ttu-id="00ec7-222">值</span><span class="sxs-lookup"><span data-stu-id="00ec7-222">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00ec7-223">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00ec7-223">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00ec7-224">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="00ec7-225">System-Only</span></span>            | <span data-ttu-id="00ec7-226">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-226">True</span></span>                            |
| <span data-ttu-id="00ec7-227">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00ec7-227">Is-Single-Valued</span></span>       | <span data-ttu-id="00ec7-228">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-228">False</span></span>                           |
| <span data-ttu-id="00ec7-229">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00ec7-229">Is Indexed</span></span>             | <span data-ttu-id="00ec7-230">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-230">False</span></span>                           |
| <span data-ttu-id="00ec7-231">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00ec7-231">In Global Catalog</span></span>      | <span data-ttu-id="00ec7-232">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-232">True</span></span>                            |
| <span data-ttu-id="00ec7-233">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00ec7-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="00ec7-234">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00ec7-234">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00ec7-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00ec7-235">Range-Lower</span></span>            | <span data-ttu-id="00ec7-236">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-236">16</span></span>                              |
| <span data-ttu-id="00ec7-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00ec7-237">Range-Upper</span></span>            | <span data-ttu-id="00ec7-238">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-238">16</span></span>                              |
| <span data-ttu-id="00ec7-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-239">Search-Flags</span></span>           | <span data-ttu-id="00ec7-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00ec7-240">0x00000000</span></span>                      |
| <span data-ttu-id="00ec7-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-241">System-Flags</span></span>           | <span data-ttu-id="00ec7-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="00ec7-242">0x00000012</span></span>                      |
| <span data-ttu-id="00ec7-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00ec7-243">Classes used in</span></span>        | [<span data-ttu-id="00ec7-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00ec7-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="00ec7-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00ec7-245">Windows Server 2008</span></span>



| <span data-ttu-id="00ec7-246">進入</span><span class="sxs-lookup"><span data-stu-id="00ec7-246">Entry</span></span> | <span data-ttu-id="00ec7-247">值</span><span class="sxs-lookup"><span data-stu-id="00ec7-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00ec7-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00ec7-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00ec7-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="00ec7-250">System-Only</span></span>            | <span data-ttu-id="00ec7-251">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-251">True</span></span>                            |
| <span data-ttu-id="00ec7-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00ec7-252">Is-Single-Valued</span></span>       | <span data-ttu-id="00ec7-253">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-253">False</span></span>                           |
| <span data-ttu-id="00ec7-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00ec7-254">Is Indexed</span></span>             | <span data-ttu-id="00ec7-255">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-255">False</span></span>                           |
| <span data-ttu-id="00ec7-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00ec7-256">In Global Catalog</span></span>      | <span data-ttu-id="00ec7-257">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-257">True</span></span>                            |
| <span data-ttu-id="00ec7-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00ec7-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="00ec7-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00ec7-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00ec7-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00ec7-260">Range-Lower</span></span>            | <span data-ttu-id="00ec7-261">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-261">16</span></span>                              |
| <span data-ttu-id="00ec7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00ec7-262">Range-Upper</span></span>            | <span data-ttu-id="00ec7-263">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-263">16</span></span>                              |
| <span data-ttu-id="00ec7-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-264">Search-Flags</span></span>           | <span data-ttu-id="00ec7-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00ec7-265">0x00000000</span></span>                      |
| <span data-ttu-id="00ec7-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-266">System-Flags</span></span>           | <span data-ttu-id="00ec7-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="00ec7-267">0x00000012</span></span>                      |
| <span data-ttu-id="00ec7-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00ec7-268">Classes used in</span></span>        | [<span data-ttu-id="00ec7-269">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00ec7-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="00ec7-270">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00ec7-270">Windows Server 2008 R2</span></span>



| <span data-ttu-id="00ec7-271">進入</span><span class="sxs-lookup"><span data-stu-id="00ec7-271">Entry</span></span> | <span data-ttu-id="00ec7-272">值</span><span class="sxs-lookup"><span data-stu-id="00ec7-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00ec7-273">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00ec7-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00ec7-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="00ec7-275">System-Only</span></span>            | <span data-ttu-id="00ec7-276">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-276">True</span></span>                            |
| <span data-ttu-id="00ec7-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00ec7-277">Is-Single-Valued</span></span>       | <span data-ttu-id="00ec7-278">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-278">False</span></span>                           |
| <span data-ttu-id="00ec7-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00ec7-279">Is Indexed</span></span>             | <span data-ttu-id="00ec7-280">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-280">False</span></span>                           |
| <span data-ttu-id="00ec7-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00ec7-281">In Global Catalog</span></span>      | <span data-ttu-id="00ec7-282">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-282">True</span></span>                            |
| <span data-ttu-id="00ec7-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00ec7-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="00ec7-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00ec7-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00ec7-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00ec7-285">Range-Lower</span></span>            | <span data-ttu-id="00ec7-286">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-286">16</span></span>                              |
| <span data-ttu-id="00ec7-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00ec7-287">Range-Upper</span></span>            | <span data-ttu-id="00ec7-288">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-288">16</span></span>                              |
| <span data-ttu-id="00ec7-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-289">Search-Flags</span></span>           | <span data-ttu-id="00ec7-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00ec7-290">0x00000000</span></span>                      |
| <span data-ttu-id="00ec7-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-291">System-Flags</span></span>           | <span data-ttu-id="00ec7-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="00ec7-292">0x00000012</span></span>                      |
| <span data-ttu-id="00ec7-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00ec7-293">Classes used in</span></span>        | [<span data-ttu-id="00ec7-294">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00ec7-294">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="00ec7-295">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00ec7-295">Windows Server 2012</span></span>



| <span data-ttu-id="00ec7-296">進入</span><span class="sxs-lookup"><span data-stu-id="00ec7-296">Entry</span></span> | <span data-ttu-id="00ec7-297">值</span><span class="sxs-lookup"><span data-stu-id="00ec7-297">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00ec7-298">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00ec7-298">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-299">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00ec7-299">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00ec7-300">System-Only</span><span class="sxs-lookup"><span data-stu-id="00ec7-300">System-Only</span></span>            | <span data-ttu-id="00ec7-301">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-301">True</span></span>                            |
| <span data-ttu-id="00ec7-302">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00ec7-302">Is-Single-Valued</span></span>       | <span data-ttu-id="00ec7-303">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-303">False</span></span>                           |
| <span data-ttu-id="00ec7-304">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00ec7-304">Is Indexed</span></span>             | <span data-ttu-id="00ec7-305">否</span><span class="sxs-lookup"><span data-stu-id="00ec7-305">False</span></span>                           |
| <span data-ttu-id="00ec7-306">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00ec7-306">In Global Catalog</span></span>      | <span data-ttu-id="00ec7-307">對</span><span class="sxs-lookup"><span data-stu-id="00ec7-307">True</span></span>                            |
| <span data-ttu-id="00ec7-308">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00ec7-308">NT-Security-Descriptor</span></span> | <span data-ttu-id="00ec7-309">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00ec7-309">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00ec7-310">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00ec7-310">Range-Lower</span></span>            | <span data-ttu-id="00ec7-311">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-311">16</span></span>                              |
| <span data-ttu-id="00ec7-312">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00ec7-312">Range-Upper</span></span>            | <span data-ttu-id="00ec7-313">16</span><span class="sxs-lookup"><span data-stu-id="00ec7-313">16</span></span>                              |
| <span data-ttu-id="00ec7-314">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-314">Search-Flags</span></span>           | <span data-ttu-id="00ec7-315">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00ec7-315">0x00000000</span></span>                      |
| <span data-ttu-id="00ec7-316">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00ec7-316">System-Flags</span></span>           | <span data-ttu-id="00ec7-317">0x00000012</span><span class="sxs-lookup"><span data-stu-id="00ec7-317">0x00000012</span></span>                      |
| <span data-ttu-id="00ec7-318">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00ec7-318">Classes used in</span></span>        | [<span data-ttu-id="00ec7-319">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00ec7-319">**Top**</span></span>](c-top.md)<br/> |



 

 






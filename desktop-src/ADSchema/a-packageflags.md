---
title: Package-Flags 屬性
description: 包含應用程式之部署狀態旗標的位位。
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- Package-Flags 屬性 AD 架構
- packageFlags 屬性 AD 架構
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7202124bdeac22347d727638dc564a145599e9c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687163"
---
# <a name="package-flags-attribute"></a><span data-ttu-id="c345a-105">Package-Flags 屬性</span><span class="sxs-lookup"><span data-stu-id="c345a-105">Package-Flags attribute</span></span>

<span data-ttu-id="c345a-106">包含應用程式之部署狀態旗標的位位。</span><span class="sxs-lookup"><span data-stu-id="c345a-106">A bitfield that contains the deployment state flags for an application.</span></span>

<span data-ttu-id="c345a-107">這個屬性可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="c345a-107">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="c345a-108">值</span><span class="sxs-lookup"><span data-stu-id="c345a-108">Value</span></span>                 | <span data-ttu-id="c345a-109">描述</span><span class="sxs-lookup"><span data-stu-id="c345a-109">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c345a-110">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c345a-110">0x00000004</span></span><br/> | <span data-ttu-id="c345a-111">在指派之前，必須先卸載此應用程式的非受控版本。</span><span class="sxs-lookup"><span data-stu-id="c345a-111">The unmanaged version of this application must be uninstalled before assigning.</span></span> <span data-ttu-id="c345a-112">**WINDOWS XP SP1 和更新版本：** 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="c345a-112">**Windows XP with SP1 and later:** This flag is not supported.</span></span><br/> <br/>                                                                                                                                          |
| <span data-ttu-id="c345a-113">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c345a-113">0x00000008</span></span><br/> | <span data-ttu-id="c345a-114">這是已發行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c345a-114">This is a published application.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="c345a-115">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c345a-115">0x00000010</span></span><br/> | <span data-ttu-id="c345a-116">這個套件是在 Windows 2000 的 Beta 3 之後部署的。</span><span class="sxs-lookup"><span data-stu-id="c345a-116">This package was deployed after Beta 3 of Windows 2000.</span></span><br/>                                                                                                                                                                                                                                             |
| <span data-ttu-id="c345a-117">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c345a-117">0x00000020</span></span><br/> | <span data-ttu-id="c345a-118">您可以使用主控台的 [ **新增或移除程式** ] 功能來安裝此應用程式。</span><span class="sxs-lookup"><span data-stu-id="c345a-118">This application can be installed with the **Add or Remove Programs** feature of the Control Panel.</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="c345a-119">0x00000040</span><span class="sxs-lookup"><span data-stu-id="c345a-119">0x00000040</span></span><br/> | <span data-ttu-id="c345a-120">您可以視需要自動安裝此應用程式。</span><span class="sxs-lookup"><span data-stu-id="c345a-120">This application can be auto-installed on demand.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c345a-121">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c345a-121">0x00000080</span></span><br/> | <span data-ttu-id="c345a-122">此應用程式是孤立的。</span><span class="sxs-lookup"><span data-stu-id="c345a-122">This application is orphaned.</span></span> <span data-ttu-id="c345a-123">如果系統管理員從可部署的應用程式清單中移除應用程式，則已發佈的應用程式可能會變成孤立。</span><span class="sxs-lookup"><span data-stu-id="c345a-123">A published application can become orphaned if the administrator removes the application from the list of deployable applications.</span></span><br/>                                                                                                                                    |
| <span data-ttu-id="c345a-124">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c345a-124">0x00000100</span></span><br/> | <span data-ttu-id="c345a-125">此應用程式應視為已卸載。</span><span class="sxs-lookup"><span data-stu-id="c345a-125">This application should be treated as uninstalled.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c345a-126">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c345a-126">0x00000200</span></span><br/> | <span data-ttu-id="c345a-127">此應用程式僅供試驗之用。</span><span class="sxs-lookup"><span data-stu-id="c345a-127">This application is available as a pilot only.</span></span><br/>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c345a-128">0x00000400</span><span class="sxs-lookup"><span data-stu-id="c345a-128">0x00000400</span></span><br/> | <span data-ttu-id="c345a-129">這是指派的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c345a-129">This is an assigned application.</span></span> <span data-ttu-id="c345a-130">使用者無法完全移除指派的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c345a-130">An assigned application cannot be fully removed by the user.</span></span> <span data-ttu-id="c345a-131">如果使用者嘗試使用主控台的 [ **新增或移除程式** ] 功能來卸載應用程式，則在移除完成時，應用程式將會重新公告至電腦。</span><span class="sxs-lookup"><span data-stu-id="c345a-131">If the user attempts to uninstall the application with the **Add or Remove Programs** feature of the Control Panel, the application will be re-advertised to the computer when the removal completes.</span></span><br/> |
| <span data-ttu-id="c345a-132">0x00000800</span><span class="sxs-lookup"><span data-stu-id="c345a-132">0x00000800</span></span><br/> | <span data-ttu-id="c345a-133">移除原則時，此應用程式是孤立的。</span><span class="sxs-lookup"><span data-stu-id="c345a-133">This application is orphaned when the policy is removed.</span></span> <span data-ttu-id="c345a-134">如果系統管理員移除與此應用程式相關的原則，系統管理員將不再控制應用程式的部署，但已安裝的應用程式將會繼續運作。</span><span class="sxs-lookup"><span data-stu-id="c345a-134">If the administrator removes the policy that is related to this application, the administrator will no longer control the deployment of the application, but the installed application will continue to function.</span></span><br/>                          |
| <span data-ttu-id="c345a-135">0x00001000</span><span class="sxs-lookup"><span data-stu-id="c345a-135">0x00001000</span></span><br/> | <span data-ttu-id="c345a-136">移除部署原則時，就會卸載此應用程式。</span><span class="sxs-lookup"><span data-stu-id="c345a-136">This application is uninstalled when the deployment policy is removed.</span></span><br/>                                                                                                                                                                                                                              |
| <span data-ttu-id="c345a-137">0x00002000</span><span class="sxs-lookup"><span data-stu-id="c345a-137">0x00002000</span></span><br/> | <span data-ttu-id="c345a-138">將會執行使用者指派應用程式的完整安裝。</span><span class="sxs-lookup"><span data-stu-id="c345a-138">A full installation of user-assigned applications will be performed.</span></span><br/>                                                                                                                                                                                                                                |
| <span data-ttu-id="c345a-139">0x00004000</span><span class="sxs-lookup"><span data-stu-id="c345a-139">0x00004000</span></span><br/> | <span data-ttu-id="c345a-140">此應用程式的舊版本必須升級為此版本。</span><span class="sxs-lookup"><span data-stu-id="c345a-140">Older versions of this application must be upgraded to this version.</span></span><br/>                                                                                                                                                                                                                                |
| <span data-ttu-id="c345a-141">0x00008000</span><span class="sxs-lookup"><span data-stu-id="c345a-141">0x00008000</span></span><br/> | <span data-ttu-id="c345a-142">此套件僅支援最基本的使用者介面，並提供安裝程式的進度列。</span><span class="sxs-lookup"><span data-stu-id="c345a-142">This package supports only a minimal user interface with a progress bar for the installation process.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="c345a-143">0x00010000</span><span class="sxs-lookup"><span data-stu-id="c345a-143">0x00010000</span></span><br/> | <span data-ttu-id="c345a-144">這是32位版 Windows 的套件，不應該在 Windows XP Professional x64 Edition 或64位版本的 Windows Server 2003 上執行。</span><span class="sxs-lookup"><span data-stu-id="c345a-144">This is a package for 32-bit versions of Windows that should not be executed on Windows XP Professional x64 Edition or 64-bit versions of Windows Server 2003.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c345a-145">0x00020000</span><span class="sxs-lookup"><span data-stu-id="c345a-145">0x00020000</span></span><br/> | <span data-ttu-id="c345a-146">此封裝適用于任何語言。</span><span class="sxs-lookup"><span data-stu-id="c345a-146">This package is suitable for any language.</span></span><br/>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c345a-147">0x00040000</span><span class="sxs-lookup"><span data-stu-id="c345a-147">0x00040000</span></span><br/> | <span data-ttu-id="c345a-148">此封裝已升級。</span><span class="sxs-lookup"><span data-stu-id="c345a-148">This package has upgrades.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c345a-149">0x00080000</span><span class="sxs-lookup"><span data-stu-id="c345a-149">0x00080000</span></span><br/> | <span data-ttu-id="c345a-150">此套件具有安裝程式的完整使用者介面。</span><span class="sxs-lookup"><span data-stu-id="c345a-150">This package has a full user interface for the installation process.</span></span><br/>                                                                                                                                                                                                                                |
| <span data-ttu-id="c345a-151">0x00100000</span><span class="sxs-lookup"><span data-stu-id="c345a-151">0x00100000</span></span><br/> | <span data-ttu-id="c345a-152">如果在網域重新命名中重新部署應用程式，則會在重新部署作業期間保留此應用程式的類別。</span><span class="sxs-lookup"><span data-stu-id="c345a-152">Classes for this application are preserved during a redeploy operation if the application is redeployed in a domain renaming.</span></span><br/>                                                                                                                                                                       |



 



| <span data-ttu-id="c345a-153">進入</span><span class="sxs-lookup"><span data-stu-id="c345a-153">Entry</span></span> | <span data-ttu-id="c345a-154">值</span><span class="sxs-lookup"><span data-stu-id="c345a-154">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c345a-155">CN</span><span class="sxs-lookup"><span data-stu-id="c345a-155">CN</span></span>                | <span data-ttu-id="c345a-156">Package-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-156">Package-Flags</span></span>                        |
| <span data-ttu-id="c345a-157">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c345a-157">Ldap-Display-Name</span></span> | <span data-ttu-id="c345a-158">packageFlags</span><span class="sxs-lookup"><span data-stu-id="c345a-158">packageFlags</span></span>                         |
| <span data-ttu-id="c345a-159">大小</span><span class="sxs-lookup"><span data-stu-id="c345a-159">Size</span></span>              | \-                                   |
| <span data-ttu-id="c345a-160">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c345a-160">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c345a-161">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c345a-161">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c345a-162">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c345a-162">Attribute-Id</span></span>      | <span data-ttu-id="c345a-163">1.2.840.113556.1.4.327</span><span class="sxs-lookup"><span data-stu-id="c345a-163">1.2.840.113556.1.4.327</span></span>               |
| <span data-ttu-id="c345a-164">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c345a-164">System-Id-Guid</span></span>    | <span data-ttu-id="c345a-165">7d6c0e99-7e20-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c345a-165">7d6c0e99-7e20-11d0-afd6-00c04fd930c9</span></span> |
| <span data-ttu-id="c345a-166">Syntax</span><span class="sxs-lookup"><span data-stu-id="c345a-166">Syntax</span></span>            | [<span data-ttu-id="c345a-167">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="c345a-167">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c345a-168">實作</span><span class="sxs-lookup"><span data-stu-id="c345a-168">Implementations</span></span>

-   [<span data-ttu-id="c345a-169">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c345a-169">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c345a-170">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c345a-170">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c345a-171">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c345a-171">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c345a-172">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c345a-172">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c345a-173">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c345a-173">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c345a-174">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c345a-174">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c345a-175">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c345a-175">Windows 2000 Server</span></span>



| <span data-ttu-id="c345a-176">進入</span><span class="sxs-lookup"><span data-stu-id="c345a-176">Entry</span></span> | <span data-ttu-id="c345a-177">值</span><span class="sxs-lookup"><span data-stu-id="c345a-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c345a-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c345a-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c345a-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c345a-180">System-Only</span></span>            | <span data-ttu-id="c345a-181">否</span><span class="sxs-lookup"><span data-stu-id="c345a-181">False</span></span>                                                            |
| <span data-ttu-id="c345a-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c345a-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c345a-183">對</span><span class="sxs-lookup"><span data-stu-id="c345a-183">True</span></span>                                                             |
| <span data-ttu-id="c345a-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c345a-184">Is Indexed</span></span>             | <span data-ttu-id="c345a-185">對</span><span class="sxs-lookup"><span data-stu-id="c345a-185">True</span></span>                                                             |
| <span data-ttu-id="c345a-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c345a-186">In Global Catalog</span></span>      | <span data-ttu-id="c345a-187">否</span><span class="sxs-lookup"><span data-stu-id="c345a-187">False</span></span>                                                            |
| <span data-ttu-id="c345a-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c345a-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c345a-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c345a-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c345a-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c345a-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c345a-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-192">Search-Flags</span></span>           | <span data-ttu-id="c345a-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c345a-193">0x00000001</span></span>                                                       |
| <span data-ttu-id="c345a-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-194">System-Flags</span></span>           | <span data-ttu-id="c345a-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c345a-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="c345a-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c345a-196">Classes used in</span></span>        | [<span data-ttu-id="c345a-197">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="c345a-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c345a-198">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c345a-198">Windows Server 2003</span></span>



| <span data-ttu-id="c345a-199">進入</span><span class="sxs-lookup"><span data-stu-id="c345a-199">Entry</span></span> | <span data-ttu-id="c345a-200">值</span><span class="sxs-lookup"><span data-stu-id="c345a-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c345a-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c345a-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c345a-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c345a-203">System-Only</span></span>            | <span data-ttu-id="c345a-204">否</span><span class="sxs-lookup"><span data-stu-id="c345a-204">False</span></span>                                                            |
| <span data-ttu-id="c345a-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c345a-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c345a-206">對</span><span class="sxs-lookup"><span data-stu-id="c345a-206">True</span></span>                                                             |
| <span data-ttu-id="c345a-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c345a-207">Is Indexed</span></span>             | <span data-ttu-id="c345a-208">對</span><span class="sxs-lookup"><span data-stu-id="c345a-208">True</span></span>                                                             |
| <span data-ttu-id="c345a-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c345a-209">In Global Catalog</span></span>      | <span data-ttu-id="c345a-210">否</span><span class="sxs-lookup"><span data-stu-id="c345a-210">False</span></span>                                                            |
| <span data-ttu-id="c345a-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c345a-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c345a-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c345a-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c345a-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c345a-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c345a-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-215">Search-Flags</span></span>           | <span data-ttu-id="c345a-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c345a-216">0x00000001</span></span>                                                       |
| <span data-ttu-id="c345a-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-217">System-Flags</span></span>           | <span data-ttu-id="c345a-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c345a-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="c345a-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c345a-219">Classes used in</span></span>        | [<span data-ttu-id="c345a-220">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="c345a-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c345a-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c345a-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c345a-222">進入</span><span class="sxs-lookup"><span data-stu-id="c345a-222">Entry</span></span> | <span data-ttu-id="c345a-223">值</span><span class="sxs-lookup"><span data-stu-id="c345a-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c345a-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c345a-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c345a-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c345a-226">System-Only</span></span>            | <span data-ttu-id="c345a-227">否</span><span class="sxs-lookup"><span data-stu-id="c345a-227">False</span></span>                                                            |
| <span data-ttu-id="c345a-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c345a-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c345a-229">對</span><span class="sxs-lookup"><span data-stu-id="c345a-229">True</span></span>                                                             |
| <span data-ttu-id="c345a-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c345a-230">Is Indexed</span></span>             | <span data-ttu-id="c345a-231">對</span><span class="sxs-lookup"><span data-stu-id="c345a-231">True</span></span>                                                             |
| <span data-ttu-id="c345a-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c345a-232">In Global Catalog</span></span>      | <span data-ttu-id="c345a-233">否</span><span class="sxs-lookup"><span data-stu-id="c345a-233">False</span></span>                                                            |
| <span data-ttu-id="c345a-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c345a-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c345a-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c345a-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c345a-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c345a-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c345a-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-238">Search-Flags</span></span>           | <span data-ttu-id="c345a-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c345a-239">0x00000001</span></span>                                                       |
| <span data-ttu-id="c345a-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-240">System-Flags</span></span>           | <span data-ttu-id="c345a-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c345a-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="c345a-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c345a-242">Classes used in</span></span>        | [<span data-ttu-id="c345a-243">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="c345a-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c345a-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c345a-244">Windows Server 2008</span></span>



| <span data-ttu-id="c345a-245">進入</span><span class="sxs-lookup"><span data-stu-id="c345a-245">Entry</span></span> | <span data-ttu-id="c345a-246">值</span><span class="sxs-lookup"><span data-stu-id="c345a-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c345a-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c345a-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c345a-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c345a-249">System-Only</span></span>            | <span data-ttu-id="c345a-250">否</span><span class="sxs-lookup"><span data-stu-id="c345a-250">False</span></span>                                                            |
| <span data-ttu-id="c345a-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c345a-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c345a-252">對</span><span class="sxs-lookup"><span data-stu-id="c345a-252">True</span></span>                                                             |
| <span data-ttu-id="c345a-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c345a-253">Is Indexed</span></span>             | <span data-ttu-id="c345a-254">對</span><span class="sxs-lookup"><span data-stu-id="c345a-254">True</span></span>                                                             |
| <span data-ttu-id="c345a-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c345a-255">In Global Catalog</span></span>      | <span data-ttu-id="c345a-256">否</span><span class="sxs-lookup"><span data-stu-id="c345a-256">False</span></span>                                                            |
| <span data-ttu-id="c345a-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c345a-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c345a-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c345a-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c345a-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c345a-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c345a-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-261">Search-Flags</span></span>           | <span data-ttu-id="c345a-262">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c345a-262">0x00000001</span></span>                                                       |
| <span data-ttu-id="c345a-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-263">System-Flags</span></span>           | <span data-ttu-id="c345a-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c345a-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="c345a-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c345a-265">Classes used in</span></span>        | [<span data-ttu-id="c345a-266">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="c345a-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c345a-267">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c345a-267">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c345a-268">進入</span><span class="sxs-lookup"><span data-stu-id="c345a-268">Entry</span></span> | <span data-ttu-id="c345a-269">值</span><span class="sxs-lookup"><span data-stu-id="c345a-269">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c345a-270">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c345a-270">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c345a-271">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="c345a-272">System-Only</span></span>            | <span data-ttu-id="c345a-273">否</span><span class="sxs-lookup"><span data-stu-id="c345a-273">False</span></span>                                                            |
| <span data-ttu-id="c345a-274">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c345a-274">Is-Single-Valued</span></span>       | <span data-ttu-id="c345a-275">對</span><span class="sxs-lookup"><span data-stu-id="c345a-275">True</span></span>                                                             |
| <span data-ttu-id="c345a-276">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c345a-276">Is Indexed</span></span>             | <span data-ttu-id="c345a-277">對</span><span class="sxs-lookup"><span data-stu-id="c345a-277">True</span></span>                                                             |
| <span data-ttu-id="c345a-278">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c345a-278">In Global Catalog</span></span>      | <span data-ttu-id="c345a-279">否</span><span class="sxs-lookup"><span data-stu-id="c345a-279">False</span></span>                                                            |
| <span data-ttu-id="c345a-280">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c345a-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="c345a-281">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c345a-281">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c345a-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c345a-282">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c345a-283">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-284">Search-Flags</span></span>           | <span data-ttu-id="c345a-285">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c345a-285">0x00000001</span></span>                                                       |
| <span data-ttu-id="c345a-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-286">System-Flags</span></span>           | <span data-ttu-id="c345a-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c345a-287">0x00000010</span></span>                                                       |
| <span data-ttu-id="c345a-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c345a-288">Classes used in</span></span>        | [<span data-ttu-id="c345a-289">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="c345a-289">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c345a-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c345a-290">Windows Server 2012</span></span>



| <span data-ttu-id="c345a-291">進入</span><span class="sxs-lookup"><span data-stu-id="c345a-291">Entry</span></span> | <span data-ttu-id="c345a-292">值</span><span class="sxs-lookup"><span data-stu-id="c345a-292">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c345a-293">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c345a-293">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c345a-294">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c345a-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="c345a-295">System-Only</span></span>            | <span data-ttu-id="c345a-296">否</span><span class="sxs-lookup"><span data-stu-id="c345a-296">False</span></span>                                                            |
| <span data-ttu-id="c345a-297">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c345a-297">Is-Single-Valued</span></span>       | <span data-ttu-id="c345a-298">對</span><span class="sxs-lookup"><span data-stu-id="c345a-298">True</span></span>                                                             |
| <span data-ttu-id="c345a-299">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c345a-299">Is Indexed</span></span>             | <span data-ttu-id="c345a-300">對</span><span class="sxs-lookup"><span data-stu-id="c345a-300">True</span></span>                                                             |
| <span data-ttu-id="c345a-301">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c345a-301">In Global Catalog</span></span>      | <span data-ttu-id="c345a-302">否</span><span class="sxs-lookup"><span data-stu-id="c345a-302">False</span></span>                                                            |
| <span data-ttu-id="c345a-303">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c345a-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="c345a-304">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c345a-304">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c345a-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c345a-305">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c345a-306">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c345a-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-307">Search-Flags</span></span>           | <span data-ttu-id="c345a-308">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c345a-308">0x00000001</span></span>                                                       |
| <span data-ttu-id="c345a-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c345a-309">System-Flags</span></span>           | <span data-ttu-id="c345a-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c345a-310">0x00000010</span></span>                                                       |
| <span data-ttu-id="c345a-311">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c345a-311">Classes used in</span></span>        | [<span data-ttu-id="c345a-312">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="c345a-312">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 






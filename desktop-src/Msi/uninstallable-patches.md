---
description: 是否可以卸載修補程式取決於修補程式的撰寫方式、用來安裝修補程式的 Windows Installer 版本，以及修補程式對應用程式所做的變更。
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: 可卸載修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad46d85318378ed81d2278d3ea1290152723704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510891"
---
# <a name="uninstallable-patches"></a><span data-ttu-id="54423-103">可卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="54423-103">Uninstallable Patches</span></span>

<span data-ttu-id="54423-104">是否可以卸載修補程式取決於修補程式的撰寫方式、用來安裝修補程式的 Windows Installer 版本，以及修補程式對應用程式所做的變更。</span><span class="sxs-lookup"><span data-stu-id="54423-104">Whether a patch can be uninstalled depends upon how the patch was authored, the version of Windows Installer used to install the patch, and the changes made by the patch to the application.</span></span> <span data-ttu-id="54423-105">如果未可卸載修補程式，則移除修補程式的唯一方法是卸載整個應用程式，並重新安裝，而不套用即將移除的修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-105">If a patch is not uninstallable, then the only way to remove the patch is to uninstall the entire application and reinstall without applying the patch being removed.</span></span>

<span data-ttu-id="54423-106">您可以使用 [命令列選項](command-line-options.md)、 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) 函式或 [**RemovePatches 方法**](installer-removepatches.md) （如 [卸載修補程式](uninstalling-patches.md) 一節中所述），呼叫卸載隨 Windows Installer 3.0 版套用的修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-106">You can call for the uninstallation of patches applied with Windows Installer version 3.0 by using [Command Line Options](command-line-options.md), the [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function, or the [**RemovePatches method**](installer-removepatches.md) as described in the [Uninstalling Patches](uninstalling-patches.md) section.</span></span> <span data-ttu-id="54423-107">Windows Installer 會確認在 [**MSIPATCHREMOVE**](msipatchremove.md) 屬性中所列出的每個修補程式都已可卸載。</span><span class="sxs-lookup"><span data-stu-id="54423-107">The Windows Installer verifies that each of the patches listed for removal in the [**MSIPATCHREMOVE**](msipatchremove.md) property is uninstallable.</span></span> <span data-ttu-id="54423-108">如果使用者沒有移除修補程式的許可權、修補程式對產品而言是未知的、修補原則會防止移除，或修補程式標示為非可卸載，則安裝程式會傳回指出失敗的安裝交易的錯誤。</span><span class="sxs-lookup"><span data-stu-id="54423-108">If the user does not have privileges to remove the patch, the patch is unknown for the product, patch policy prevents removal, or the patch was marked as not uninstallable, the installer returns an error indicating a failed installation transaction.</span></span>

<span data-ttu-id="54423-109">**Windows Installer 2.0：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="54423-109">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="54423-110">使用早于 Windows Installer 3.0 的 Windows Installer 版本所套用的修補程式則不會可卸載。</span><span class="sxs-lookup"><span data-stu-id="54423-110">Patches applied using a version of Windows Installer that is earlier than Windows Installer 3.0 are not uninstallable.</span></span>

## <a name="patches-that-are-not-uninstallable"></a><span data-ttu-id="54423-111">未可卸載的修補程式</span><span class="sxs-lookup"><span data-stu-id="54423-111">Patches that are Not Uninstallable</span></span>

<span data-ttu-id="54423-112">在下列情況下，不會可卸載套用至已安裝應用程式) 的 patch ( .msp 檔案。</span><span class="sxs-lookup"><span data-stu-id="54423-112">A patch (.msp file) applied to an installed application is not uninstallable in the following cases.</span></span> <span data-ttu-id="54423-113">移除未可卸載之修補程式的唯一方法是卸載已修補的應用程式，然後重新安裝應用程式，而不需要重新套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-113">The only method to remove a patch that is not uninstallable is to uninstall the patched application and then reinstall the application without reapplying the patch.</span></span> <span data-ttu-id="54423-114">在此情況下，您必須重新套用任何您不想要從應用程式移除的修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-114">In this case, you must reapply any patches that you do not wish to be removed from the application.</span></span>

-   <span data-ttu-id="54423-115">使用 Windows Installer 小於 Windows Installer 3.0 的版本所套用的修補程式則不會可卸載。</span><span class="sxs-lookup"><span data-stu-id="54423-115">Patches applied using a version of Windows Installer that is less than Windows Installer 3.0 are not uninstallable.</span></span>
-   <span data-ttu-id="54423-116">套用至安裝在系統管理員所設定之 [DisablePatchUninstall](disablepatchuninstall.md) 原則之電腦上的應用程式的修補程式，並不會可卸載。</span><span class="sxs-lookup"><span data-stu-id="54423-116">Patches applied to applications installed on a computer that has had the [DisablePatchUninstall](disablepatchuninstall.md) policy set by an administrator are not uninstallable.</span></span> <span data-ttu-id="54423-117">當設定此 [電腦原則](machine-policies.md)時，即使是系統管理員，也不能卸載電腦上的任何修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-117">When this [machine policy](machine-policies.md)has been set, no patches on the computer can be uninstalled, even by an administrator.</span></span>
-   <span data-ttu-id="54423-118">在資料庫中沒有 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表的修補程式不會可卸載。</span><span class="sxs-lookup"><span data-stu-id="54423-118">Patches that do not have a [MsiPatchMetadata](msipatchmetadata-table.md) table in their database are not uninstallable.</span></span>
-   <span data-ttu-id="54423-119">未在 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表中包含下列資料列的修補程式則不會可卸載。</span><span class="sxs-lookup"><span data-stu-id="54423-119">Patches that do not include the following row in their [MsiPatchMetadata](msipatchmetadata-table.md) table are not uninstallable.</span></span> <span data-ttu-id="54423-120">不會可卸載公司、屬性和值的其他值的修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-120">The patch is not uninstallable for other values of Company, Property, and Value.</span></span>

    | <span data-ttu-id="54423-121">公司</span><span class="sxs-lookup"><span data-stu-id="54423-121">Company</span></span> | <span data-ttu-id="54423-122">屬性</span><span class="sxs-lookup"><span data-stu-id="54423-122">Property</span></span>     | <span data-ttu-id="54423-123">值</span><span class="sxs-lookup"><span data-stu-id="54423-123">Value</span></span> |
    |---------|--------------|-------|
    | <span data-ttu-id="54423-124">;</span><span class="sxs-lookup"><span data-stu-id="54423-124">{Null}</span></span>  | <span data-ttu-id="54423-125">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="54423-125">AllowRemoval</span></span> | <span data-ttu-id="54423-126">1</span><span class="sxs-lookup"><span data-stu-id="54423-126">1</span></span>     |

    

     

-   <span data-ttu-id="54423-127">修補程式已套用至安裝在內容中的應用程式，但使用者沒有足夠的許可權可卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-127">The patch has been applied to an application installed in a context for which the user has insufficient privileges to uninstall patches.</span></span> <span data-ttu-id="54423-128">下表中的「不允許」單字表示系統管理員或非系統管理員的使用者無法從已在此內容中安裝的已修補應用程式卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-128">The words "Not Allowed" in the following table indicate that an administrator or non-administrator user cannot uninstall patches from patched applications installed in this context.</span></span> <span data-ttu-id="54423-129">此表格中的「允許」一字表示許可權並不會防止系統管理員或非系統管理員使用者卸載修補程式，但基於本節所討論的任何其他原因，仍然可能無法卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-129">The word "Allowed" in this table means that privileges do not prevent an administrator or non-administrator user from uninstalling patches, however for any of the other reasons discussed in this section, it still might not be possible to uninstall the patch.</span></span>

    | <span data-ttu-id="54423-130">應用程式安裝內容</span><span class="sxs-lookup"><span data-stu-id="54423-130">application Installation Context</span></span>        | <span data-ttu-id="54423-131">系統管理員卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="54423-131">Administrator Uninstall of Patch</span></span> | <span data-ttu-id="54423-132">非系統管理員卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="54423-132">Non-Administrator Uninstall of Patch</span></span>                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="54423-133">Per-Machine</span><span class="sxs-lookup"><span data-stu-id="54423-133">Per-Machine</span></span>                             | <span data-ttu-id="54423-134">允許</span><span class="sxs-lookup"><span data-stu-id="54423-134">Allowed</span></span>                          | <span data-ttu-id="54423-135">通常不允許唯一的例外狀況是使用 (LUA) 修補來套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-135">Generally Not Allowed The only exception is if the patch was applied using (LUA) patching.</span></span> <span data-ttu-id="54423-136">系統管理員或非系統管理員會可卸載標示為 LUA 修補程式的修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-136">A patch marked as a LUA patch is uninstallable by either administrators or non-administrators.</span></span> <span data-ttu-id="54423-137">LUA 修補僅適用于每台電腦從媒體安裝的套件，且需要特殊的撰寫。</span><span class="sxs-lookup"><span data-stu-id="54423-137">LUA patching is only available for packages installed per-machine from media and require special authoring.</span></span><br/> |
    | <span data-ttu-id="54423-138">針對目前使用者 Per-User 非受控</span><span class="sxs-lookup"><span data-stu-id="54423-138">Per-User Non-Managed for Current User</span></span>   | <span data-ttu-id="54423-139">允許</span><span class="sxs-lookup"><span data-stu-id="54423-139">Allowed</span></span>                          | <span data-ttu-id="54423-140">允許</span><span class="sxs-lookup"><span data-stu-id="54423-140">Allowed</span></span>                                                                                                                                                                                                                                                                                                          |
    | <span data-ttu-id="54423-141">針對不同的使用者 Per-User 非受控</span><span class="sxs-lookup"><span data-stu-id="54423-141">Per-User Non-Managed for Different User</span></span> | <span data-ttu-id="54423-142">不允許</span><span class="sxs-lookup"><span data-stu-id="54423-142">Not Allowed</span></span>                      | <span data-ttu-id="54423-143">不允許</span><span class="sxs-lookup"><span data-stu-id="54423-143">Not Allowed</span></span>                                                                                                                                                                                                                                                                                                      |
    | <span data-ttu-id="54423-144">目前使用者的 Per-User 管理</span><span class="sxs-lookup"><span data-stu-id="54423-144">Per-User Managed for Current User</span></span>       | <span data-ttu-id="54423-145">允許</span><span class="sxs-lookup"><span data-stu-id="54423-145">Allowed</span></span>                          | <span data-ttu-id="54423-146">不允許</span><span class="sxs-lookup"><span data-stu-id="54423-146">Not Allowed</span></span>                                                                                                                                                                                                                                                                                                      |
    | <span data-ttu-id="54423-147">針對不同使用者管理 Per-User</span><span class="sxs-lookup"><span data-stu-id="54423-147">Per-User Managed for Different User</span></span>     | <span data-ttu-id="54423-148">不允許</span><span class="sxs-lookup"><span data-stu-id="54423-148">Not Allowed</span></span>                      | <span data-ttu-id="54423-149">不允許</span><span class="sxs-lookup"><span data-stu-id="54423-149">Not Allowed</span></span>                                                                                                                                                                                                                                                                                                      |

    

     

-   <span data-ttu-id="54423-150">未可卸載修補程式所套用的 [主要升級](major-upgrades.md) 。</span><span class="sxs-lookup"><span data-stu-id="54423-150">A [major upgrade](major-upgrades.md) applied by a patch is not uninstallable.</span></span> <span data-ttu-id="54423-151">應用程式的主要升級應藉由將升級的應用程式安裝 ( .msi 檔案) 而不是修補程式來執行。</span><span class="sxs-lookup"><span data-stu-id="54423-151">Major Upgrades of an application should be performed by installing the upgraded application (.msi file) rather than a patch.</span></span>
-   <span data-ttu-id="54423-152">未可卸載套用至系統管理安裝的修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-152">Patches applied to an administrative installation are not uninstallable.</span></span> <span data-ttu-id="54423-153">不建議您修補系統管理安裝。</span><span class="sxs-lookup"><span data-stu-id="54423-153">Patching administrative installations is not recommended.</span></span> <span data-ttu-id="54423-154">使用者從系統管理映射安裝應用程式之後，應該在使用者的電腦上套用一組目前的修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-154">The current set of patches should be applied on the user's computer after the user installs the application from the administrative image.</span></span> <span data-ttu-id="54423-155">這可防止使用者電腦上快取的 [套件程式碼](package-codes.md) 與系統管理安裝上的套件程式碼不同。</span><span class="sxs-lookup"><span data-stu-id="54423-155">This can prevent the [package code](package-codes.md) cached on the user's computer from becoming different than the package code on the administrative installation.</span></span> <span data-ttu-id="54423-156">如果使用者電腦上快取的套件程式碼與系統管理安裝上的不同，請從系統管理安裝重新安裝該應用程式，然後再修補用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="54423-156">If the package code cached on the user's computer becomes different from that on the administrative installation, reinstall the application from the administrative installation and then patch the client computer.</span></span>
-   <span data-ttu-id="54423-157">當 patch 將新內容新增至下列清單中的任何資料表時，Windows Installer 將修補程式標示為未可卸載。</span><span class="sxs-lookup"><span data-stu-id="54423-157">When a patch adds new content to any of the tables in the following list, Windows Installer marks the patch as being not uninstallable.</span></span> <span data-ttu-id="54423-158">可卸載修補程式可以將新的資料列新增至不包含在此清單中的資料庫資料表，以將新的檔案、元件、登錄專案、元件或功能加入至安裝中。</span><span class="sxs-lookup"><span data-stu-id="54423-158">An uninstallable patch can add new files, assemblies, registry entries, components, or features to an installation by adding new rows to database tables that are not included in this list.</span></span>

    -   [<span data-ttu-id="54423-159">AppId</span><span class="sxs-lookup"><span data-stu-id="54423-159">AppId</span></span>](appid-table.md)
    -   [<span data-ttu-id="54423-160">BindImage</span><span class="sxs-lookup"><span data-stu-id="54423-160">BindImage</span></span>](bindimage-table.md)
    -   [<span data-ttu-id="54423-161">類別</span><span class="sxs-lookup"><span data-stu-id="54423-161">Class</span></span>](class-table.md)
    -   [<span data-ttu-id="54423-162">Complus</span><span class="sxs-lookup"><span data-stu-id="54423-162">Complus</span></span>](complus-table.md)
    -   [<span data-ttu-id="54423-163">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="54423-163">CreateFolder</span></span>](createfolder-table.md)
    -   [<span data-ttu-id="54423-164">DuplicateFile</span><span class="sxs-lookup"><span data-stu-id="54423-164">DuplicateFile</span></span>](duplicatefile-table.md)
    -   [<span data-ttu-id="54423-165">環境</span><span class="sxs-lookup"><span data-stu-id="54423-165">Environment</span></span>](environment-table.md)
    -   [<span data-ttu-id="54423-166">分機</span><span class="sxs-lookup"><span data-stu-id="54423-166">Extension</span></span>](extension-table.md)
    -   [<span data-ttu-id="54423-167">字型</span><span class="sxs-lookup"><span data-stu-id="54423-167">Font</span></span>](font-table.md)
    -   [<span data-ttu-id="54423-168">IniFile</span><span class="sxs-lookup"><span data-stu-id="54423-168">IniFile</span></span>](inifile-table.md)
    -   [<span data-ttu-id="54423-169">IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="54423-169">IsolatedComponent</span></span>](isolatedcomponent-table.md)
    -   [<span data-ttu-id="54423-170">LockPermissions</span><span class="sxs-lookup"><span data-stu-id="54423-170">LockPermissions</span></span>](lockpermissions-table.md)
    -   [<span data-ttu-id="54423-171">MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="54423-171">MsiLockPermissionsEx</span></span>](msilockpermissionsex-table.md)
    -   [<span data-ttu-id="54423-172">MIME</span><span class="sxs-lookup"><span data-stu-id="54423-172">MIME</span></span>](mime-table.md)
    -   [<span data-ttu-id="54423-173">MoveFile</span><span class="sxs-lookup"><span data-stu-id="54423-173">MoveFile</span></span>](movefile-table.md)
    -   [<span data-ttu-id="54423-174">MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="54423-174">MsiServiceConfig</span></span>](msiserviceconfig-table.md)
    -   [<span data-ttu-id="54423-175">MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="54423-175">MsiServiceConfigFailureActions</span></span>](msiserviceconfigfailureactions-table.md)
    -   [<span data-ttu-id="54423-176">ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="54423-176">ODBCAttribute</span></span>](odbcattribute-table.md)
    -   [<span data-ttu-id="54423-177">ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="54423-177">ODBCDataSource</span></span>](odbcdatasource-table.md)
    -   [<span data-ttu-id="54423-178">ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="54423-178">ODBCDriver</span></span>](odbcdriver-table.md)
    -   [<span data-ttu-id="54423-179">ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="54423-179">ODBCSourceAttribute</span></span>](odbcsourceattribute-table.md)
    -   [<span data-ttu-id="54423-180">ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="54423-180">ODBCTranslator</span></span>](odbctranslator-table.md)
    -   [<span data-ttu-id="54423-181">ProgId</span><span class="sxs-lookup"><span data-stu-id="54423-181">ProgId</span></span>](progid-table.md)
    -   [<span data-ttu-id="54423-182">PublishComponent</span><span class="sxs-lookup"><span data-stu-id="54423-182">PublishComponent</span></span>](publishcomponent-table.md)
    -   [<span data-ttu-id="54423-183">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="54423-183">RemoveIniFile</span></span>](removeinifile-table.md)
    -   [<span data-ttu-id="54423-184">SelfReg</span><span class="sxs-lookup"><span data-stu-id="54423-184">SelfReg</span></span>](selfreg-table.md)
    -   [<span data-ttu-id="54423-185">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="54423-185">ServiceControl</span></span>](servicecontrol-table.md)
    -   [<span data-ttu-id="54423-186">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="54423-186">ServiceInstall</span></span>](serviceinstall-table.md)
    -   [<span data-ttu-id="54423-187">類型</span><span class="sxs-lookup"><span data-stu-id="54423-187">TypeLib</span></span>](typelib-table.md)
    -   [<span data-ttu-id="54423-188">動詞</span><span class="sxs-lookup"><span data-stu-id="54423-188">Verb</span></span>](verb-table.md)
    -   [!Note]  
        > <span data-ttu-id="54423-189">如果 patch 將新內容加入至 [RemoveFile](removefile-table.md) 或 [RemoveRegistry](removeregistry-table.md) 資料表，Windows Installer 不會將修補程式標示為未可卸載。</span><span class="sxs-lookup"><span data-stu-id="54423-189">If a patch adds new content to the [RemoveFile](removefile-table.md) or [RemoveRegistry](removeregistry-table.md) tables, Windows Installer does not mark the patch as being not uninstallable.</span></span> <span data-ttu-id="54423-190">不過，除非原始安裝套件中尚未存在用來移除新內容的資源，否則不會可卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-190">However, the patch is not uninstallable unless the resource to remove the new content does not already exist in the original installation package.</span></span> <span data-ttu-id="54423-191">例如，如果 patch 將新的資料列新增至 RemoveFile 資料表，則如果檔案位於檔案 [資料表](file-table.md)外部，則無法藉由卸載修補程式來還原移除的檔案。</span><span class="sxs-lookup"><span data-stu-id="54423-191">For example, if the patch adds a new row to the RemoveFile table, the removed file cannot be restored by uninstalling the patch if the file is external to the [File table](file-table.md).</span></span> <span data-ttu-id="54423-192">檔案必須已在原始封裝的檔案資料表中撰寫，並套用修補程式以可卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="54423-192">The file must have been authored in the File table of the original package plus applied patches for the patch to be uninstallable.</span></span>

         

## <a name="related-topics"></a><span data-ttu-id="54423-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="54423-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54423-194">修補程式順序</span><span class="sxs-lookup"><span data-stu-id="54423-194">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="54423-195">移除修補程式</span><span class="sxs-lookup"><span data-stu-id="54423-195">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="54423-196">卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="54423-196">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="54423-197">修補卸載自訂動作</span><span class="sxs-lookup"><span data-stu-id="54423-197">Patch Uninstall Custom Actions</span></span>](patch-uninstall-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="54423-198">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="54423-198">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="54423-199">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="54423-199">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="54423-200">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="54423-200">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="54423-201">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="54423-201">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 





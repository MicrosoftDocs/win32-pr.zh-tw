---
description: Windows Installer 修補程式 ( .msp 檔) 是用來將更新傳遞至 Windows Installer 應用程式的檔案。
ms.assetid: f59736d7-0b5a-466c-ab60-f210ccccb07f
title: 修補套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b4bb5b7e182c8118f5a40c45be440784b92099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692483"
---
# <a name="patch-packages"></a><span data-ttu-id="7110d-103">修補套件</span><span class="sxs-lookup"><span data-stu-id="7110d-103">Patch Packages</span></span>

<span data-ttu-id="7110d-104">Windows Installer 修補程式 ( .msp 檔) 是用來將更新傳遞至 Windows Installer 應用程式的檔案。</span><span class="sxs-lookup"><span data-stu-id="7110d-104">A Windows Installer patch (.msp file) is a file used to deliver updates to Windows Installer applications.</span></span> <span data-ttu-id="7110d-105">修補程式是獨立套件，其中包含更新應用程式所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="7110d-105">The patch is a self-contained package that contains all the information required to update the application.</span></span> <span data-ttu-id="7110d-106"> ( .msp 檔) 的修補套件可能會比整個更新應用程式的 Windows Installer 套件 () .msi 檔案更小。</span><span class="sxs-lookup"><span data-stu-id="7110d-106">A patch package (.msp file) can be much smaller than the Windows Installer package (.msi file) for the entire updated application.</span></span> <span data-ttu-id="7110d-107">如需將較小的更新傳遞給應用程式的詳細資訊，請參閱 [減少修補程式大小](reducing-patch-size.md)。</span><span class="sxs-lookup"><span data-stu-id="7110d-107">For more information about delivering smaller updates to applications, see [Reducing Patch Size](reducing-patch-size.md).</span></span>

<span data-ttu-id="7110d-108">修補套件包含應用程式的實際更新，並描述應用程式可接收修補程式的版本。</span><span class="sxs-lookup"><span data-stu-id="7110d-108">A patch package contains the actual updates to the application and describes which versions of the application can receive the patch.</span></span> <span data-ttu-id="7110d-109">修補套裝程式含至少兩個資料庫轉換。</span><span class="sxs-lookup"><span data-stu-id="7110d-109">Patches contain at minimum two database transforms.</span></span> <span data-ttu-id="7110d-110">一個轉換會更新應用程式安裝資料庫中的資訊。</span><span class="sxs-lookup"><span data-stu-id="7110d-110">One transform updates the information in the installation database of the application.</span></span> <span data-ttu-id="7110d-111">另一個轉換會新增安裝程式用來修補檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="7110d-111">The other transform adds information that the installer uses for patching files.</span></span> <span data-ttu-id="7110d-112">安裝程式會使用轉換所提供的資訊來套用修補檔案，這些檔案儲存在修補程式套件的封包檔資料流程中。</span><span class="sxs-lookup"><span data-stu-id="7110d-112">The installer uses the information provided by the transforms to apply patch files that are stored in the cabinet file stream of the patch package.</span></span> <span data-ttu-id="7110d-113">Patch 封裝沒有像安裝封裝 ( .msi 檔案的資料庫。 ) </span><span class="sxs-lookup"><span data-stu-id="7110d-113">A patch package does not have a database like an installation package (.msi file.)</span></span>

<span data-ttu-id="7110d-114">從 Windows Installer 版本3.0 開始，修補封裝可以包含描述修補程式順序的資訊，相對於 [MsiPatchSequence](msipatchsequence-table.md) 資料表中的其他更新以及 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表中的其他描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="7110d-114">Beginning with Windows Installer version 3.0, patch packages can contain information that describe the patching sequence for the patch relative to other updates in the [MsiPatchSequence](msipatchsequence-table.md) table and additional descriptive information in the [MsiPatchMetadata](msipatchmetadata-table.md) table.</span></span>

<span data-ttu-id="7110d-115">使用者可以從網路管理映射安裝應用程式和更新。</span><span class="sxs-lookup"><span data-stu-id="7110d-115">Users can install applications and updates from a network administrative image.</span></span> <span data-ttu-id="7110d-116">雖然修補套件可以套用至系統管理安裝，但提供更新的建議方法是讓使用者安裝原始的應用程式，然後將修補程式套用到其電腦上的本機應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="7110d-116">Although patch packages can be applied to administrative installations, the recommended method to deliver updates is to have users install the original application and then apply the patches to the local instance of the application on to their computer.</span></span> <span data-ttu-id="7110d-117">這樣可讓使用者與系統管理映射保持同步。</span><span class="sxs-lookup"><span data-stu-id="7110d-117">This keeps users in synchronization with the administrative image.</span></span> <span data-ttu-id="7110d-118">如果將修補程式套用至系統管理安裝，該系統管理安裝的所有用戶端都必須重新安裝，並重新安裝應用程式才能接收更新。</span><span class="sxs-lookup"><span data-stu-id="7110d-118">If a patch is applied to the administrative installation, all clients of that administrative installation must recache and reinstall the application to receive the update.</span></span> <span data-ttu-id="7110d-119">在使用者 recaches 並重新安裝之前，使用者無法視需要安裝，也無法從修補的系統管理安裝修複安裝。</span><span class="sxs-lookup"><span data-stu-id="7110d-119">Until a user recaches and reinstalls, the user is unable to install-on-demand and repair installations from the patched administrative installation.</span></span>

<span data-ttu-id="7110d-120">從 Windows Installer 3.0 開始，非系統管理員可以在修補程式核准為受系統管理員信任之後，將修補程式套用到每位使用者管理的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7110d-120">Beginning with Windows Installer 3.0, non-administrators can apply patches to per-user-managed applications after the patch has been approved as trusted by an administrator.</span></span> <span data-ttu-id="7110d-121">如需如何進行此作業的詳細資訊，請參閱 [修補 Per-User 受控應用程式](patching-per-user-managed-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="7110d-121">For more information on how to do this, see [Patching Per-User Managed Applications](patching-per-user-managed-applications.md).</span></span> <span data-ttu-id="7110d-122">另一種方法是使用最低許可權的使用者帳戶修補。</span><span class="sxs-lookup"><span data-stu-id="7110d-122">Another method is to use least privileged user account patching.</span></span>

> [!Note]  
> <span data-ttu-id="7110d-123">如果已設定 [AllowLockdownPatch](allowlockdownpatch.md) 原則，非系統管理員的使用者就可以在以較高的許可權執行安裝時，將修補程式套用至現有的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7110d-123">If the [AllowLockdownPatch](allowlockdownpatch.md) policy has been set, non-administrator users can apply a patch to an existing application while running an installation at elevated privileges.</span></span> <span data-ttu-id="7110d-124">不建議使用此方法，因為它可讓未受信任的修補程式套用至可使用較高許可權執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7110d-124">This method is not recommended because it enables untrusted patches to be applied to an application that can run with elevated privileges.</span></span>

 

<span data-ttu-id="7110d-125">修補程式套件由下列元件組成。</span><span class="sxs-lookup"><span data-stu-id="7110d-125">Patch packages are comprised of the following parts.</span></span> <span data-ttu-id="7110d-126">如需修補套件之結構的詳細資訊，請參閱 [建立修補程式套件](creating-a-patch-package.md)。</span><span class="sxs-lookup"><span data-stu-id="7110d-126">For more information about the construction of patch packages, see [Creating a Patch Package](creating-a-patch-package.md).</span></span>

## <a name="summary-information-stream"></a><span data-ttu-id="7110d-127">摘要資訊串流</span><span class="sxs-lookup"><span data-stu-id="7110d-127">Summary Information Stream</span></span>

<span data-ttu-id="7110d-128">Patch 封裝的摘要資訊資料流程會提供有關修補的身分識別和用途的資訊。</span><span class="sxs-lookup"><span data-stu-id="7110d-128">The summary information stream of the patch package provides information about the identity and purpose of the patch.</span></span>

<span data-ttu-id="7110d-129">摘要資訊串流最少包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="7110d-129">The summary information stream holds a minimum of the following:</span></span>

-   <span data-ttu-id="7110d-130">可唯一識別修補程式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="7110d-130">A GUID that uniquely identifies the patch.</span></span> <span data-ttu-id="7110d-131">此修補程式的 GUID 會附加至先前修補程式所取代的 Guid 清單。</span><span class="sxs-lookup"><span data-stu-id="7110d-131">The GUID for this patch is appended with a list of GUIDs for earlier patches that are replaced by this patch.</span></span>
-   <span data-ttu-id="7110d-132">此修補程式之有效目標的產品代碼清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="7110d-132">A semicolon-delimited list of product codes for valid targets for this patch.</span></span>
-   <span data-ttu-id="7110d-133">以分號分隔的轉換 substorage 名稱清單（以其處理的順序排列）。</span><span class="sxs-lookup"><span data-stu-id="7110d-133">A semicolon-delimited list of transform substorage names in the order they are to be processed.</span></span>
-   <span data-ttu-id="7110d-134">此修補程式的來源清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="7110d-134">A semicolon-delimited list of sources for this patch.</span></span>

## <a name="transform-substorage"></a><span data-ttu-id="7110d-135">轉換 Substorage</span><span class="sxs-lookup"><span data-stu-id="7110d-135">Transform Substorage</span></span>

<span data-ttu-id="7110d-136">修補套件包含可新增或移除檔案、登錄專案、使用者介面和自訂的轉換。</span><span class="sxs-lookup"><span data-stu-id="7110d-136">A patch package contains transforms that can add or remove files, registry entries, user interfaces, and customizations.</span></span> <span data-ttu-id="7110d-137">轉換會以 substorages 的形式包含在套件中。</span><span class="sxs-lookup"><span data-stu-id="7110d-137">Transforms are included as substorages in the package.</span></span> <span data-ttu-id="7110d-138">修補套件包含每個目標資料庫的兩個轉換。</span><span class="sxs-lookup"><span data-stu-id="7110d-138">A patch package contains two transforms for each target database.</span></span> <span data-ttu-id="7110d-139">其中一個轉換是安裝資料庫的實際更新，並從安裝封裝的原始和更新映射之間的差異產生。</span><span class="sxs-lookup"><span data-stu-id="7110d-139">One transform is the actual updates to the installation database and is generated from the differences between the original and updated images of the installation package.</span></span> <span data-ttu-id="7110d-140">其他轉換會將專案新增至 [Patch](patch-table.md)、 [PatchPackage](patchpackage-table.md)、 [Media](media-table.md)、 [InstallExecuteSequence](installexecutesequence-table.md)和 [AdminExecuteSequence](adminexecutesequence-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="7110d-140">The other transform adds entries to the [Patch](patch-table.md), [PatchPackage](patchpackage-table.md), [Media](media-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [AdminExecuteSequence](adminexecutesequence-table.md) tables.</span></span> <span data-ttu-id="7110d-141">Substorage 中的資訊會將它系結至特定的 [**UpgradeCode**](upgradecode.md)、 [**ProductCode**](productcode.md)、 [**ProductVersion**](productversion.md)和 [**ProductLanguage**](productlanguage.md)。</span><span class="sxs-lookup"><span data-stu-id="7110d-141">Information in the substorage ties it to a specific [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md), and [**ProductLanguage**](productlanguage.md).</span></span> <span data-ttu-id="7110d-142">可以套用至多個目標的 patch 封裝包含一對以上的轉換。</span><span class="sxs-lookup"><span data-stu-id="7110d-142">A patch package that can be applied to multiple targets contains more than one pair of these transforms.</span></span>

## <a name="cabinet-file-stream"></a><span data-ttu-id="7110d-143">封包檔串流</span><span class="sxs-lookup"><span data-stu-id="7110d-143">Cabinet File Stream</span></span>

<span data-ttu-id="7110d-144">修補程式中包含的封包檔資料流程可以包含這些類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="7110d-144">The cabinet file stream included in a patch can contain these types of files:</span></span>

-   <span data-ttu-id="7110d-145">修補檔案，其中包含將舊版本檔案變更為新版本所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="7110d-145">Patch files containing the information required to change the old version of the file into the new version.</span></span> <span data-ttu-id="7110d-146">單一修補檔案可用來更新一或多個舊版本的檔案。</span><span class="sxs-lookup"><span data-stu-id="7110d-146">A single patch file can be used to update one or more old versions of a file.</span></span>
-   <span data-ttu-id="7110d-147">新增至應用程式的其他檔案不存在於舊版本中。</span><span class="sxs-lookup"><span data-stu-id="7110d-147">Additional files being added to the application that are not present in the old version.</span></span>
-   <span data-ttu-id="7110d-148">整個取代檔案。</span><span class="sxs-lookup"><span data-stu-id="7110d-148">An entire replacement file.</span></span> <span data-ttu-id="7110d-149">在很罕見的情況下，檔案的新版本小於更新舊版本檔案所需的修補程式時，新的檔案可以包含在完整的檔案中。</span><span class="sxs-lookup"><span data-stu-id="7110d-149">In the rare case where the new version of a file is smaller than the patch required to update the old version of that file, the new file can be included in its entirety.</span></span> <span data-ttu-id="7110d-150">這些是安裝在舊版本上的新檔案。</span><span class="sxs-lookup"><span data-stu-id="7110d-150">These are new files that are installed over their old versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7110d-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="7110d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7110d-152">建立修補程式套件</span><span class="sxs-lookup"><span data-stu-id="7110d-152">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> </dl>

 

 




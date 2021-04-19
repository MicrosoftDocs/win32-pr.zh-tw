---
description: 從 Windows Installer&\# 160; 版本&\# 160; 3.0 開始，可以建立並安裝可單獨卸載的修補程式，而不需要卸載並重新安裝整個應用程式和其他修補程式。
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: 移除修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd54db3bde3a356a0c3adb299555248bbc87a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977977"
---
# <a name="removing-patches"></a><span data-ttu-id="4cfc8-103">移除修補程式</span><span class="sxs-lookup"><span data-stu-id="4cfc8-103">Removing Patches</span></span>

<span data-ttu-id="4cfc8-104">從 Windows Installer 版本3.0 開始，您可以建立並安裝可單獨卸載的修補程式，而不需要卸載並重新安裝整個應用程式和其他修補程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-104">Beginning with Windows Installer version 3.0, it is possible to create and install patches that can be uninstalled singly, and in any order, without having to uninstall and reinstall the entire application and other patches.</span></span> <span data-ttu-id="4cfc8-105">Windows Installer 3.0 也可讓您使用包含修補程式順序資訊的[MsiPatchSequence 資料表](msipatchsequence-table.md)來撰寫[修補封裝](patch-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-105">Windows Installer 3.0 also enables [Patch Packages](patch-packages.md) to be authored with a [MsiPatchSequence Table](msipatchsequence-table.md) that contains patch sequencing information.</span></span> <span data-ttu-id="4cfc8-106">在 Windows Installer 3.0 之前的 Windows Installer 版本中，從應用程式移除特定修補程式的唯一方法，就是卸載整個已修補的應用程式，然後重新安裝，而不需要重新套用任何即將移除的修補程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-106">With versions of Windows Installer earlier than Windows Installer 3.0, the only method to remove particular patches from an application is to uninstall the entire patched application and then reinstall without reapplying any patches being removed.</span></span>

<span data-ttu-id="4cfc8-107">是否可以卸載修補程式取決於修補程式的撰寫方式、用來安裝修補程式的 Windows Installer 版本，以及修補程式對應用程式所做的變更。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-107">Whether a patch can be uninstalled depends upon how the patch was authored, the version of Windows Installer used to install the patch, and the changes made by the patch to the application.</span></span> <span data-ttu-id="4cfc8-108">如果未可卸載修補程式，則移除修補程式的唯一方法是卸載整個應用程式，並重新安裝，而不套用即將移除的修補程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-108">If a patch is not uninstallable, then the only way to remove the patch is to uninstall the entire application and reinstall without applying the patch being removed.</span></span>

<span data-ttu-id="4cfc8-109">您可以使用命令列選項、指令碼介面，或從另一個應用程式呼叫 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) ，來卸載一或多個修補程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-109">You can uninstall one or more patches using a command line option, the scripting interface, or by calling [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) from another application.</span></span> <span data-ttu-id="4cfc8-110">如需如何卸載修補程式的詳細資訊，請參閱 [卸載修補程式](uninstalling-patches.md) 。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-110">See [Uninstalling Patches](uninstalling-patches.md) for more information about how to uninstall patches.</span></span>

<span data-ttu-id="4cfc8-111">[**MSIPATCHREMOVE**](msipatchremove.md)屬性的值會列出要卸載的修補程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-111">The value of the [**MSIPATCHREMOVE**](msipatchremove.md) property lists the patches to be uninstalled.</span></span> <span data-ttu-id="4cfc8-112">針對清單中的每個修補程式，安裝程式會驗證是否已可卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-112">For each patch in the list, the installer verifies that the patch is uninstallable.</span></span> <span data-ttu-id="4cfc8-113">如果使用者沒有移除修補程式的許可權、修補程式對產品而言是未知的、修補原則會防止移除，或修補程式標示為未可卸載，安裝程式會傳回錯誤，指出安裝失敗的交易。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-113">If the user does not have privileges to remove the patch, the patch is unknown for the product, patch policy prevents removal, or the patch was marked as not uninstallable, the installer returns an error that indicates a failed installation transaction.</span></span> <span data-ttu-id="4cfc8-114">如需判斷是否有修補程式未可卸載的詳細資訊，請參閱 [可卸載修補程式](uninstallable-patches.md) 。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-114">See [Uninstallable Patches](uninstallable-patches.md) for more information about what determines whether a patch is not uninstallable.</span></span>

<span data-ttu-id="4cfc8-115">一旦將修補程式驗證為卸載式，安裝程式就會從 patch 應用程式順序中移除修補程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-115">Once the patch is verified as removable, the installer removes the patch from the patch application sequence.</span></span> <span data-ttu-id="4cfc8-116">如需 Windows Installer 3.0 如何判斷套用修補程式時所要使用之順序的詳細資訊，請參閱 [排序修補程式](sequencing-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-116">For more information about how Windows Installer 3.0 determines what sequence to use when applying patches see [Sequencing Patches](sequencing-patches.md).</span></span> <span data-ttu-id="4cfc8-117">請注意，從序列中移除修補程式可能會導致標示為已淘汰或被取代的修補程式變成作用中。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-117">Note that removing patches from the sequence can cause patches marked obsolete or superseded to become active.</span></span>

<span data-ttu-id="4cfc8-118">選取要移除的所有修補程式都會列在 [**MsiPatchRemovalList**](msipatchremovallist.md) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-118">All patches selected for removal are listed in the [**MsiPatchRemovalList**](msipatchremovallist.md) property.</span></span> <span data-ttu-id="4cfc8-119">這個屬性是由安裝程式所設定的私用屬性，可用於條件運算式或 [自訂動作](custom-actions.md)查詢。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-119">This property is a private property that is set by the installer and can be used in conditional expressions or queried by [custom actions](custom-actions.md).</span></span> <span data-ttu-id="4cfc8-120">屬性包含要移除之修補程式的修補程式程式碼 Guid 清單。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-120">The property contains the list of patch code GUIDs of patches to be removed.</span></span> <span data-ttu-id="4cfc8-121">自訂動作可以藉由呼叫 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)或 [Patch 物件](patch-object.md)的 [**PatchProperty**](patch-patchproperty.md)屬性，來決定是否要套用、淘汰或取代修補程式的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-121">A custom action can determine whether the installation state of the patch is applied, obsolete or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch Object](patch-object.md).</span></span>

<span data-ttu-id="4cfc8-122">移除修補程式之後，應用程式的狀態就會和從未安裝過修補程式一樣。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-122">After a patch is removed the state of the application is the same as if the patch was never installed.</span></span> <span data-ttu-id="4cfc8-123">如果可能的話，安裝程式會將處理常式限制為遭移除的修補程式所影響的功能子集。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-123">If possible, the installer restricts the process to the subset of features affected by the patch being removed.</span></span> <span data-ttu-id="4cfc8-124">安裝程式會自動將 [ [**重新安裝**](reinstall.md) ] 屬性設定為受影響功能的清單。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-124">The installer automatically sets the [**REINSTALL**](reinstall.md) property to the list of affected features.</span></span> <span data-ttu-id="4cfc8-125">系統會移除修補程式所新增的檔案，並覆寫修補程式所修改的檔案。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-125">Files that were added by the patch are removed and files that were modified by the patch are overwritten.</span></span> <span data-ttu-id="4cfc8-126">檔案和登錄專案會還原至產品所預期的版本減去修補程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-126">Files and registry entries are restored to the version expected by the product minus the patch.</span></span> <span data-ttu-id="4cfc8-127">修補程式所加入的功能和元件會從應用程式取消註冊。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-127">Features and components that were added by the patch are unregistered from the application.</span></span> <span data-ttu-id="4cfc8-128">請注意，如果另一個仍適用的修補程式使用內容，修補程式新增的其他內容可以保留在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-128">Note that additional content added by the patch can remain on the user's computer if the content is used by another patch that is still applicable.</span></span>

<span data-ttu-id="4cfc8-129">如果有修補程式更新共用元件的檔案，此變更會影響共用元件的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-129">If a file of a shared component is updated by a patch, the change affects all applications that share the component.</span></span> <span data-ttu-id="4cfc8-130">移除修補程式時，此變更會影響共用元件的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-130">When the patch is removed, again, the change affects all applications that share the component.</span></span> <span data-ttu-id="4cfc8-131">這表示，將修補程式移除一個應用程式，可以將共用元件的檔案還原至比其他應用程式所需的版本更低的版本。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-131">This means that removal of a patch by one application can restore the file of the shared component to a lower version than required by another application.</span></span> <span data-ttu-id="4cfc8-132">這可以修正第一個應用程式，但會導致第二個應用程式停止運作。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-132">This could fix the first application, but cause the second application to stop working.</span></span> <span data-ttu-id="4cfc8-133">在此情況下，您可以使用 [重新安裝功能或應用程式](reinstalling-a-feature-or-application.md)中所述的方法，重新安裝第二個應用程式，以修復第二個應用程式。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-133">In this case, the second application can be repaired by reinstalling the second application using the methods describe in [Reinstalling a Feature or Application](reinstalling-a-feature-or-application.md).</span></span> <span data-ttu-id="4cfc8-134">這會還原檔案的已修補版本。</span><span class="sxs-lookup"><span data-stu-id="4cfc8-134">This will restore the patched version of the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cfc8-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="4cfc8-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cfc8-136">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="4cfc8-136">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="4cfc8-137">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="4cfc8-137">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="4cfc8-138">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="4cfc8-138">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="4cfc8-139">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="4cfc8-139">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[<span data-ttu-id="4cfc8-140">修補程式順序</span><span class="sxs-lookup"><span data-stu-id="4cfc8-140">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="4cfc8-141">修補卸載自訂動作</span><span class="sxs-lookup"><span data-stu-id="4cfc8-141">Patch Uninstall Custom Actions</span></span>](patch-uninstall-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="4cfc8-142">可卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="4cfc8-142">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="4cfc8-143">卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="4cfc8-143">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> </dl>

 

 




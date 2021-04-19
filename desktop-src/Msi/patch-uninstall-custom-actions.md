---
description: 您可以使用 [自訂動作修補程式] 選項，指定安裝程式只在卸載修補程式時執行自訂動作。
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: 修補卸載自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973042"
---
# <a name="patch-uninstall-custom-actions"></a><span data-ttu-id="97ecf-103">修補卸載自訂動作</span><span class="sxs-lookup"><span data-stu-id="97ecf-103">Patch Uninstall Custom Actions</span></span>

<span data-ttu-id="97ecf-104">您可以使用 [ [自訂動作修補程式] 選項](custom-action-patch-uninstall-option.md) ，指定安裝程式只在卸載修補程式時執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="97ecf-104">You can use the [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) to specify that the installer run the custom action only when a patch is uninstalled.</span></span>

<span data-ttu-id="97ecf-105">**Windows Installer 4.5 和更新版本：** 您可以使用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md) 來指定安裝程式只在卸載修補程式時執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="97ecf-105">**Windows Installer 4.5 and later:** You can use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) to specify that the installer only run the custom action when a patch is uninstalled.</span></span>

<span data-ttu-id="97ecf-106">\*\*[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)： \* \*</span><span class="sxs-lookup"><span data-stu-id="97ecf-106">\*\*[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):  \*\*</span></span>

<span data-ttu-id="97ecf-107">無法使用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md) 。</span><span class="sxs-lookup"><span data-stu-id="97ecf-107">The [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) is not available.</span></span> <span data-ttu-id="97ecf-108">在修補程式卸載時，沒有任何方法可在修補程式套件內標記 [自訂動作](custom-actions.md) ，因為安裝程式不會套用修補套件卸載。</span><span class="sxs-lookup"><span data-stu-id="97ecf-108">There is no method for marking a [custom action](custom-actions.md) within a patch package to be run when the patch is uninstalled because the installer does not apply the patch packages being uninstalled.</span></span>

<span data-ttu-id="97ecf-109">若要在卸載特定的修補程式時執行 [自訂動作](custom-actions.md) ，自訂動作必須存在於原始應用程式中，或者必須在永遠套用之產品的修補程式中。</span><span class="sxs-lookup"><span data-stu-id="97ecf-109">To have a [custom action](custom-actions.md) run when a particular patch is uninstalled, the custom action must either be present in the original application or be in a patch for the product that is always applied.</span></span>

<span data-ttu-id="97ecf-110">開發人員可以使用 [**MsiPatchRemovalList**](msipatchremovallist.md) 屬性來撰寫 Windows Installer 套件或修補程式，以在移除修補程式時執行 [自訂動作](custom-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="97ecf-110">Developers can use the [**MsiPatchRemovalList**](msipatchremovallist.md) property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="97ecf-111">自訂動作可以撰寫至原始安裝套件、已套用至套件的修補程式，或不是 [可卸載修補](uninstallable-patches.md)程式的修補程式。</span><span class="sxs-lookup"><span data-stu-id="97ecf-111">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="97ecf-112">您可以在順序資料表的 **MsiPatchRemovalList** 屬性上 conditionalized 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="97ecf-112">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="97ecf-113">如需 conditionalizing 動作的詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md) 。</span><span class="sxs-lookup"><span data-stu-id="97ecf-113">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="97ecf-114">自訂動作可以從 [**MsiPatchRemovalList**](msipatchremovallist.md) 屬性的值取得要移除之修補程式的 guid。</span><span class="sxs-lookup"><span data-stu-id="97ecf-114">The custom action can obtain the GUIDs of patches being removed from the value of the [**MsiPatchRemovalList**](msipatchremovallist.md) property.</span></span> <span data-ttu-id="97ecf-115">自訂動作可以藉由呼叫 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)或 [Patch 物件](patch-object.md)的 [**PatchProperty**](patch-patchproperty.md)屬性，來判斷修補程式的安裝狀態是套用、淘汰或取代。</span><span class="sxs-lookup"><span data-stu-id="97ecf-115">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

<span data-ttu-id="97ecf-116">如果自訂動作需要來自修補程式的特殊中繼資料，修補程式應包含自訂動作，以在套用修補程式時，將中繼資料寫入登錄或檔案位置。</span><span class="sxs-lookup"><span data-stu-id="97ecf-116">If the custom action requires special metadata from the patch, the patch should contain a custom action that writes the metadata to a registry or file location when the patch is applied.</span></span> <span data-ttu-id="97ecf-117">原始應用程式中的自訂動作或永遠套用的修補程式，可取得移除修補程式變更所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="97ecf-117">The custom action in the original application or a patch that is always applied can obtain the information needed to remove the patch's changes.</span></span>

<span data-ttu-id="97ecf-118">進行難以復原的變更不應標示為 [可卸載修補](uninstallable-patches.md)程式的修補程式。</span><span class="sxs-lookup"><span data-stu-id="97ecf-118">Patches making changes that are difficult to undo correctly should not be marked as [uninstallable patches](uninstallable-patches.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="97ecf-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="97ecf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97ecf-120">修補程式順序</span><span class="sxs-lookup"><span data-stu-id="97ecf-120">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="97ecf-121">移除修補程式</span><span class="sxs-lookup"><span data-stu-id="97ecf-121">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="97ecf-122">可卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="97ecf-122">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="97ecf-123">卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="97ecf-123">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="97ecf-124">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="97ecf-124">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="97ecf-125">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="97ecf-125">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="97ecf-126">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="97ecf-126">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="97ecf-127">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="97ecf-127">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




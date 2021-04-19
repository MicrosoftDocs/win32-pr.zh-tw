---
description: 安裝程式會將 MsiPatchRemovalList 屬性的值設定為要在安裝期間移除的修補程式清單。
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: MsiPatchRemovalList 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993281"
---
# <a name="msipatchremovallist-property"></a><span data-ttu-id="9ea0a-103">MsiPatchRemovalList 屬性</span><span class="sxs-lookup"><span data-stu-id="9ea0a-103">MsiPatchRemovalList property</span></span>

<span data-ttu-id="9ea0a-104">安裝程式會將 **MsiPatchRemovalList** 屬性的值設定為要在安裝期間移除的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-104">The installer sets the value of the **MsiPatchRemovalList** property to a list of patches that are being removed during the installation.</span></span> <span data-ttu-id="9ea0a-105">修補程式在清單中是以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-105">The patches are represented in the list by their patch code GUIDs separated by semicolons.</span></span>

<span data-ttu-id="9ea0a-106">開發人員可以使用 **MsiPatchRemovalList** 屬性來撰寫 Windows Installer 套件或修補程式，以在移除修補程式時執行 [自訂動作](custom-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-106">Developers can use the **MsiPatchRemovalList** property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="9ea0a-107">自訂動作可以撰寫至原始安裝套件、已套用至套件的修補程式，或不是 [可卸載修補](uninstallable-patches.md)程式的修補程式。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-107">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="9ea0a-108">您可以在順序資料表的 **MsiPatchRemovalList** 屬性上 conditionalized 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-108">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="9ea0a-109">如需 conditionalizing 動作的詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md) 。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-109">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="9ea0a-110">自訂動作可以從 **MsiPatchRemovalList** 屬性的值取得要移除之修補程式的 guid。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-110">The custom action can obtain the GUIDs of patches being removed from the value of the **MsiPatchRemovalList** property.</span></span> <span data-ttu-id="9ea0a-111">自訂動作可以藉由呼叫 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)函式或 [Patch 物件](patch-object.md)的 [**PatchProperty**](patch-patchproperty.md)屬性，來判斷修補程式的安裝狀態是套用、淘汰或取代。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-111">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) function or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ea0a-112">備註</span><span class="sxs-lookup"><span data-stu-id="9ea0a-112">Remarks</span></span>

<span data-ttu-id="9ea0a-113">如需移除修補程式的詳細資訊，請參閱 [移除修補程式](removing-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-113">For more information about removing patches, see [Removing Patches](removing-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ea0a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ea0a-114">Requirements</span></span>



| <span data-ttu-id="9ea0a-115">需求</span><span class="sxs-lookup"><span data-stu-id="9ea0a-115">Requirement</span></span> | <span data-ttu-id="9ea0a-116">值</span><span class="sxs-lookup"><span data-stu-id="9ea0a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea0a-117">版本</span><span class="sxs-lookup"><span data-stu-id="9ea0a-117">Version</span></span><br/> | <span data-ttu-id="9ea0a-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9ea0a-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9ea0a-120">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-120">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9ea0a-121">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="9ea0a-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ea0a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ea0a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea0a-123">屬性</span><span class="sxs-lookup"><span data-stu-id="9ea0a-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="9ea0a-124">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="9ea0a-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





---
description: 使用下列選項旗標，指定只有在卸載修補程式時，安裝程式才執行自訂動作。 若要設定此選項，請將此資料表中的值加入至 CustomAction 資料表之 ExtendedType 欄位的值。
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: 自訂動作修補卸載選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988456"
---
# <a name="custom-action-patch-uninstall-option"></a><span data-ttu-id="bf10c-104">自訂動作修補卸載選項</span><span class="sxs-lookup"><span data-stu-id="bf10c-104">Custom Action Patch Uninstall Option</span></span>

<span data-ttu-id="bf10c-105">使用下列選項旗標，指定只有在卸載修補程式時，安裝程式才執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="bf10c-105">Use the following option flag to specify that the installer run the custom action only when a patch is being uninstalled.</span></span> <span data-ttu-id="bf10c-106">若要設定此選項，請將此資料表中的值加入至 [CustomAction 資料表](customaction-table.md)之 ExtendedType 欄位的值。</span><span class="sxs-lookup"><span data-stu-id="bf10c-106">To set the option, add the value in this table to the value in the ExtendedType field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="bf10c-107">**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="bf10c-107">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="bf10c-108">從 Windows Installer 4.5 開始，可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="bf10c-108">This option is available beginning with Windows Installer 4.5.</span></span>



| <span data-ttu-id="bf10c-109">常數</span><span class="sxs-lookup"><span data-stu-id="bf10c-109">Constant</span></span>                                | <span data-ttu-id="bf10c-110">十六進位</span><span class="sxs-lookup"><span data-stu-id="bf10c-110">Hexadecimal</span></span> | <span data-ttu-id="bf10c-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="bf10c-111">Decimal</span></span> | <span data-ttu-id="bf10c-112">Description</span><span class="sxs-lookup"><span data-stu-id="bf10c-112">Description</span></span>                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| <span data-ttu-id="bf10c-113">**msidbCustomActionTypePatchUninstall**</span><span class="sxs-lookup"><span data-stu-id="bf10c-113">**msidbCustomActionTypePatchUninstall**</span></span> | <span data-ttu-id="bf10c-114">0x8000</span><span class="sxs-lookup"><span data-stu-id="bf10c-114">0x8000</span></span>      | <span data-ttu-id="bf10c-115">32768</span><span class="sxs-lookup"><span data-stu-id="bf10c-115">32768</span></span>   | <span data-ttu-id="bf10c-116">只有在卸載修補程式時，才會執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="bf10c-116">The custom action runs only when a patch is being uninstalled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bf10c-117">備註</span><span class="sxs-lookup"><span data-stu-id="bf10c-117">Remarks</span></span>

<span data-ttu-id="bf10c-118">您可以將這個屬性加入至自訂動作，方法是在 Windows Installer 套件 ( .msi 檔案) 中撰寫它。</span><span class="sxs-lookup"><span data-stu-id="bf10c-118">This attribute can be added to a custom action by authoring it in the Windows Installer package (.msi file).</span></span> <span data-ttu-id="bf10c-119">具有這個屬性的新自訂動作可以透過修補程式來新增。</span><span class="sxs-lookup"><span data-stu-id="bf10c-119">A new custom action with this attribute can be added by a patch.</span></span> <span data-ttu-id="bf10c-120">具有這個屬性的自訂動作可以透過修補程式來更新。</span><span class="sxs-lookup"><span data-stu-id="bf10c-120">A custom action having this attribute can be updated by a patch.</span></span> <span data-ttu-id="bf10c-121">現有自訂動作的修補程式無法新增或移除這個屬性。</span><span class="sxs-lookup"><span data-stu-id="bf10c-121">This attribute cannot be added or removed by a patch to an existing custom action.</span></span>

<span data-ttu-id="bf10c-122">如果修補程式以這個屬性新增或更新自訂動作，Windows Installer 卸載修補程式時，會執行新的或更新的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="bf10c-122">If a patch adds or updates a custom action with this attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="bf10c-123">Windows Installer 會將修補程式內的更新提供給修補程式卸載自訂動作。</span><span class="sxs-lookup"><span data-stu-id="bf10c-123">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="bf10c-124">修補程式必須包含 [MsiTransformView *<PatchGUID>*](msitransformview.md)資料表，以提供此資訊給 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="bf10c-124">The patch must include a [MsiTransformView *<PatchGUID>*](msitransformview.md) table to provide this information to Windows Installer.</span></span>

<span data-ttu-id="bf10c-125">當含有 **msidbCustomActionTypePatchUninstall** 屬性之自訂動作的封裝使用早于 Windows Installer 4.0 的安裝程式版本安裝時，安裝程式將不會在修補程式卸載時呼叫自訂動作。</span><span class="sxs-lookup"><span data-stu-id="bf10c-125">When a package that contains a custom action with the **msidbCustomActionTypePatchUninstall** attribute is installed using an installer version earlier than Windows Installer 4.0, the installer does not call the custom action when the patch is uninstalled.</span></span> <span data-ttu-id="bf10c-126">安裝程式可以在安裝、修復或更新套件時執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="bf10c-126">The install can run the custom action during the installation, repair, or update of the package.</span></span>

<span data-ttu-id="bf10c-127">使用 **msidbCustomActionTypePatchUninstall** 屬性的自訂動作應使用 [**MSIPATCHREMOVE**](msipatchremove.md) 屬性，以防止在使用 Windows Installer 4.0 或更早版本的系統安裝、修復或更新時執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="bf10c-127">Custom actions with the **msidbCustomActionTypePatchUninstall** attribute should be conditioned using the [**MSIPATCHREMOVE**](msipatchremove.md) property to prevent the custom action from running when installing, repairing, or updating using a system with Windows Installer 4.0 or earlier.</span></span> <span data-ttu-id="bf10c-128">安裝 Windows Installer 4.5 和更新版本時，系統上的所有修補程式都會以 **msidbCustomActionTypePatchUninstall** 屬性標記自訂動作，在修補卸載期間執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="bf10c-128">When Windows Installer 4.5 and later is installed, all the patches on the system having custom actions marked with the **msidbCustomActionTypePatchUninstall** attribute run the custom action during patch uninstallation.</span></span> <span data-ttu-id="bf10c-129">如果從系統移除 Windows Installer 4.5 或更新版本，修補程式會遺失自訂動作修補卸載功能。</span><span class="sxs-lookup"><span data-stu-id="bf10c-129">If Windows Installer 4.5 or later is removed from the system, patches lose the custom action patch uninstall functionality.</span></span>

<span data-ttu-id="bf10c-130">如需在使用早于 Windows Installer 4.5 的版本卸載修補程式期間執行自訂動作的詳細資訊，請參閱 [修補卸載自訂動作](patch-uninstall-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="bf10c-130">For information about running a custom action during the uninstallation of a patch using a version earlier than Windows Installer 4.5, see [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf10c-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf10c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf10c-132">自訂動作 In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="bf10c-132">Custom Action In-Script Execution Options</span></span>](custom-action-in-script-execution-options.md)
</dt> <dt>

[<span data-ttu-id="bf10c-133">自訂動作參考</span><span class="sxs-lookup"><span data-stu-id="bf10c-133">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="bf10c-134">關於自訂動作</span><span class="sxs-lookup"><span data-stu-id="bf10c-134">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="bf10c-135">使用自訂動作</span><span class="sxs-lookup"><span data-stu-id="bf10c-135">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="bf10c-136">MsiTransformView *<PatchGUID>*</span><span class="sxs-lookup"><span data-stu-id="bf10c-136">MsiTransformView *<PatchGUID>*</span></span>](msitransformview.md)
</dt> </dl>

 

 




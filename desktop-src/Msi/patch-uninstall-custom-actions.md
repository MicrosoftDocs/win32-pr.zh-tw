---
description: 您可以使用 [自訂動作修補程式] 選項，指定安裝程式只在卸載修補程式時執行自訂動作。
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: 修補卸載自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69077337b80177984ff43f12038edb1daa48215f92c627f4ed22ea2f69c876b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145421"
---
# <a name="patch-uninstall-custom-actions"></a>修補卸載自訂動作

您可以使用 [ [自訂動作修補程式] 選項](custom-action-patch-uninstall-option.md) ，指定安裝程式只在卸載修補程式時執行自訂動作。

**Windows Installer 4.5 和更新版本：** 您可以使用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md)來指定安裝程式只在卸載修補程式時執行自訂動作。

**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)： * *

無法使用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md) 。 在修補程式卸載時，沒有任何方法可在修補程式套件內標記 [自訂動作](custom-actions.md) ，因為安裝程式不會套用修補套件卸載。

若要在卸載特定的修補程式時執行 [自訂動作](custom-actions.md) ，自訂動作必須存在於原始應用程式中，或者必須在永遠套用之產品的修補程式中。

開發人員可以使用 [**MsiPatchRemovalList**](msipatchremovallist.md)屬性來撰寫 Windows Installer 套件或修補程式，以在移除修補程式時執行 [自訂動作](custom-actions.md)。 自訂動作可以撰寫至原始安裝套件、已套用至套件的修補程式，或不是 [可卸載修補](uninstallable-patches.md)程式的修補程式。 您可以在順序資料表的 **MsiPatchRemovalList** 屬性上 conditionalized 自訂動作。 如需 conditionalizing 動作的詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md) 。

自訂動作可以從 [**MsiPatchRemovalList**](msipatchremovallist.md) 屬性的值取得要移除之修補程式的 guid。 自訂動作可以藉由呼叫 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)或 [Patch 物件](patch-object.md)的 [**PatchProperty**](patch-patchproperty.md)屬性，來判斷修補程式的安裝狀態是套用、淘汰或取代。

如果自訂動作需要來自修補程式的特殊中繼資料，修補程式應包含自訂動作，以在套用修補程式時，將中繼資料寫入登錄或檔案位置。 原始應用程式中的自訂動作或永遠套用的修補程式，可取得移除修補程式變更所需的資訊。

進行難以復原的變更不應標示為 [可卸載修補](uninstallable-patches.md)程式的修補程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[修補程式順序](sequencing-patches.md)
</dt> <dt>

[移除修補程式](removing-patches.md)
</dt> <dt>

[可卸載修補程式](uninstallable-patches.md)
</dt> <dt>

[卸載修補程式](uninstalling-patches.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




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
# <a name="msipatchremovallist-property"></a>MsiPatchRemovalList 屬性

安裝程式會將 **MsiPatchRemovalList** 屬性的值設定為要在安裝期間移除的修補程式清單。 修補程式在清單中是以分號分隔。

開發人員可以使用 **MsiPatchRemovalList** 屬性來撰寫 Windows Installer 套件或修補程式，以在移除修補程式時執行 [自訂動作](custom-actions.md) 。 自訂動作可以撰寫至原始安裝套件、已套用至套件的修補程式，或不是 [可卸載修補](uninstallable-patches.md)程式的修補程式。 您可以在順序資料表的 **MsiPatchRemovalList** 屬性上 conditionalized 自訂動作。 如需 conditionalizing 動作的詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md) 。

自訂動作可以從 **MsiPatchRemovalList** 屬性的值取得要移除之修補程式的 guid。 自訂動作可以藉由呼叫 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)函式或 [Patch 物件](patch-object.md)的 [**PatchProperty**](patch-patchproperty.md)屬性，來判斷修補程式的安裝狀態是套用、淘汰或取代。

## <a name="remarks"></a>備註

如需移除修補程式的詳細資訊，請參閱 [移除修補程式](removing-patches.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





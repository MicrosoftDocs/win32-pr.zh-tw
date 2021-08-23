---
description: 在命令列上或在屬性工作表中，將 MSIENFORCEUPGRADECOMPONENTRULES 屬性設定為1，以便在小型更新和特定產品的次要升級期間套用升級元件規則。
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: MSIENFORCEUPGRADECOMPONENTRULES 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11535beb45ac521e59ec31c5e5231b23549394b75e5df2372ba4295471ea8008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945042"
---
# <a name="msienforceupgradecomponentrules-property"></a>MSIENFORCEUPGRADECOMPONENTRULES 屬性

在命令列上或在 [屬性工作表](property-table.md)中，將 **MSIENFORCEUPGRADECOMPONENTRULES** 屬性設定為1，以便在 [小型更新](small-updates.md)和特定產品的 [次要升級](minor-upgrades.md)期間套用升級元件規則。 若要在小型更新和電腦上所有產品的次要升級期間套用規則，請將 [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) 原則設定為1。

當屬性或原則設定為1時， [小更新](small-updates.md) 和 [次要升級](minor-upgrades.md) 可能會失敗，因為更新會嘗試執行下列違反升級元件規則的動作：

-   將新功能新增至現有功能樹狀結構的頂端或中間。

    新的功能必須新增為現有功能樹狀目錄的新分葉功能。

    在此情況下，產品的 [**ProductCode**](productcode.md) 可以變更，並可將更新視為 [主要升級](major-upgrades.md)。

-   從功能移除元件。

    如果您變更元件的 GUID，也可能會發生這種情況。 原始 GUID 所識別的元件會被移除，而新 GUID 所識別的元件會顯示為新的元件。

    **Windows Installer 4.5 和更新版本：** 您可以藉由在 [元件資料表](component-table.md)中設定 **msidbComponentAttributesUninstallOnSupersedence** 屬性，或設定 [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)屬性，以正確地移除元件，方法是使用 Windows Installer 4.5 和更新版本。

    或者，您可以變更產品的 [**ProductCode**](productcode.md) ，也可以將更新視為 [主要升級](major-upgrades.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式3.0 或更新版本。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





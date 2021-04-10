---
description: 這是每部電腦的系統原則，可用來在小型更新和次要升級期間套用升級元件規則。
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944427"
---
# <a name="enforceupgradecomponentrules"></a>EnforceUpgradeComponentRules

這是每部電腦的 [系統原則](system-policy.md) ，可用來在 [小型更新](small-updates.md) 和 [次要升級](minor-upgrades.md)期間套用升級元件規則。

將 EnforceUpgradeComponentRules 原則設定為1，在 [小型更新](small-updates.md) 和電腦上所有產品的 [次要升級](minor-upgrades.md) 期間，套用升級元件規則。 若要在小型更新和特定產品的次要升級期間套用規則，請在命令列上或在 [屬性工作表](property-table.md)中，將 [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)屬性設定為1。

當屬性或原則設定為1時， [小更新](small-updates.md) 和 [次要升級](minor-upgrades.md) 可能會失敗，因為更新會嘗試執行下列作業：

-   將新功能新增至現有功能樹狀結構的頂端或中間。

    新的功能必須新增為現有功能樹狀目錄的新分葉功能。

    在此情況下，產品的 [**ProductCode**](productcode.md) 可以變更，而且可以將更新視為 [主要升級](major-upgrades.md)。

-   從功能移除元件。

    如果您變更元件的 GUID，也可能會發生這種情況。 原始 GUID 所識別的元件會被移除，而新 GUID 所識別的元件會顯示為新的元件。

    **Windows Installer 4.5 和更新版本：** 您可以藉由在 [元件資料表](component-table.md)中設定 **msidbComponentAttributesUninstallOnSupersedence** 屬性，或設定 [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)屬性，以正確地移除元件，方法是使用 Windows Installer 4.5 或更新版本。

    或者，您可以變更產品的 [**ProductCode**](productcode.md) ，也可以將更新視為 [主要升級](major-upgrades.md)。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




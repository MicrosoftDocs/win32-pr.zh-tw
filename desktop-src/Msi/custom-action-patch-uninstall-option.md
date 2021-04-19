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
# <a name="custom-action-patch-uninstall-option"></a>自訂動作修補卸載選項

使用下列選項旗標，指定只有在卸載修補程式時，安裝程式才執行自訂動作。 若要設定此選項，請將此資料表中的值加入至 [CustomAction 資料表](customaction-table.md)之 ExtendedType 欄位的值。

**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。 從 Windows Installer 4.5 開始，可以使用此選項。



| 常數                                | 十六進位 | Decimal | Description                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| **msidbCustomActionTypePatchUninstall** | 0x8000      | 32768   | 只有在卸載修補程式時，才會執行自訂動作。 |



 

## <a name="remarks"></a>備註

您可以將這個屬性加入至自訂動作，方法是在 Windows Installer 套件 ( .msi 檔案) 中撰寫它。 具有這個屬性的新自訂動作可以透過修補程式來新增。 具有這個屬性的自訂動作可以透過修補程式來更新。 現有自訂動作的修補程式無法新增或移除這個屬性。

如果修補程式以這個屬性新增或更新自訂動作，Windows Installer 卸載修補程式時，會執行新的或更新的自訂動作。 Windows Installer 會將修補程式內的更新提供給修補程式卸載自訂動作。 修補程式必須包含 [MsiTransformView *<PatchGUID>*](msitransformview.md)資料表，以提供此資訊給 Windows Installer。

當含有 **msidbCustomActionTypePatchUninstall** 屬性之自訂動作的封裝使用早于 Windows Installer 4.0 的安裝程式版本安裝時，安裝程式將不會在修補程式卸載時呼叫自訂動作。 安裝程式可以在安裝、修復或更新套件時執行自訂動作。

使用 **msidbCustomActionTypePatchUninstall** 屬性的自訂動作應使用 [**MSIPATCHREMOVE**](msipatchremove.md) 屬性，以防止在使用 Windows Installer 4.0 或更早版本的系統安裝、修復或更新時執行自訂動作。 安裝 Windows Installer 4.5 和更新版本時，系統上的所有修補程式都會以 **msidbCustomActionTypePatchUninstall** 屬性標記自訂動作，在修補卸載期間執行自訂動作。 如果從系統移除 Windows Installer 4.5 或更新版本，修補程式會遺失自訂動作修補卸載功能。

如需在使用早于 Windows Installer 4.5 的版本卸載修補程式期間執行自訂動作的詳細資訊，請參閱 [修補卸載自訂動作](patch-uninstall-custom-actions.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)
</dt> <dt>

[自訂動作參考](custom-action-reference.md)
</dt> <dt>

[關於自訂動作](about-custom-actions.md)
</dt> <dt>

[使用自訂動作](using-custom-actions.md)
</dt> <dt>

[MsiTransformView *<PatchGUID>*](msitransformview.md)
</dt> </dl>

 

 




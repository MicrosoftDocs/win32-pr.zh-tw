---
description: MsiConfigureServices 動作會設定系統的服務。 此動作會查詢 MsiServiceConfig 和 MsiServiceConfigFailureActions 資料表。
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: MsiConfigureServices 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f77bcb37514cc0e90cd9b3e4f65f184104a60a575f159e45391582cfed01c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945063"
---
# <a name="msiconfigureservices-action"></a>MsiConfigureServices 動作

MsiConfigureServices 動作會設定系統的服務。 此動作會查詢 [MsiServiceConfig](msiserviceconfig-table.md) 和 [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) 資料表。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用此動作。

> [!IMPORTANT]
>
> Windows服務可讓您自動執行預先定義的動作，以回應服務中的失敗。 為了支援在服務失敗時以程式設計方式設定這些復原 **動作** ， [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) 已新增至 msi 5.0 版中的 msi。 不過，這項功能不會如預期般運作。
>
> 若要解決這個問題，應用程式開發人員應該使用 MSI 中的 **自訂動作** 功能來執行 **sc.exe** 並適當地設定 **修復選項** 。

 

## <a name="sequence-restrictions"></a>順序限制

此標準動作必須以下列順序使用。

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

下列任何一個動作： [InstallFiles](installfiles-action.md)、 [RemoveFiles](removefiles-action.md)、 [DuplicateFiles](duplicatefiles-action.md)、 [MoveFiles](movefiles-action.md)、 [PatchFiles](patchfiles-action.md)和 [RemoveDuplicateFiles](removeduplicatefiles-action.md) 動作。

[InstallServices](installservices-action.md)

MsiConfigureServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

此動作會要求使用者必須是系統管理員，或擁有具有安裝服務或應用程式屬於受管理安裝之許可權的更高許可權。

 

 




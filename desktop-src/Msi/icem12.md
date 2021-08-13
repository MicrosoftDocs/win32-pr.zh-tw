---
description: ICEM12 會確認在 ModuleSequence 資料表中，標準動作具有序號和自訂動作具有 BaseAction 和之後的值。
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53e6f83b9ffccf6595719815ec4bd44cc8ff3774b989b682751dd9be1bbe5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634941"
---
# <a name="icem12"></a>ICEM12

ICEM12 會確認在 ModuleSequence 資料表中，標準動作具有序號和自訂動作具有 BaseAction 和之後的值。

此 ICEM 可在 Windows Installer 2.0 SDK 和更新版本提供的 Mergemod 檔中找到。 如需詳細資訊，請參閱[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="result"></a>結果

ICEM12 會在下列情況下張貼錯誤：

-   它會尋找模組包含沒有序號的 [標準動作](standard-actions.md) 。
-   它會發現標準動作具有在 [ModuleAdminUISequence 資料表](moduleadminuisequence-table.md)、 [ModuleAdminExecuteSequence 資料表](moduleadminexecutesequence-table.md)、 [ModuleAdvtExecuteSequence 資料表](moduleadvtexecutesequence-table.md)、 [ModuleInstallUISequence 資料表](moduleinstalluisequence-table.md)或 [ModuleInstallExecuteSequence 資料表](moduleinstallexecutesequence-table.md)的 BaseAction 或 After 欄位中輸入的值。
-   它會尋找模組包含 [自訂動作](custom-actions.md) ，而不會在 BaseAction 或 [ModuleAdminUISequence 資料表](moduleadminuisequence-table.md)、 [ModuleAdminExecuteSequence 資料表](moduleadminexecutesequence-table.md)、 [ModuleAdvtExecuteSequence 資料表](moduleadvtexecutesequence-table.md)、 [ModuleInstallUISequence 資料表](moduleinstalluisequence-table.md)或 [ModuleInstallExecuteSequence 資料表](moduleinstallexecutesequence-table.md)的欄位中輸入任何值。

ICEM12 會在找到指定序號的自訂動作時張貼警告，但不會在 BaseAction 或 After 欄位中提供任何值。

請注意，在 [CustomAction 資料表](customaction-table.md) 中找到的所有動作都會視為自訂動作。 所有其他動作都會視為標準動作。

## <a name="example"></a>範例

ICEM12 會針對包含如下所示之資料庫專案的模組，張貼下列錯誤和警告訊息：

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[CustomAction](customaction-table.md)



| 動作  | 類型 | 來源  | 目標  |
|---------|------|---------|---------|
| Action1 | 30   | source1.rc | target1 |
| Action3 | 30   | source3 | target3 |



 

[ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)



| 動作  | 順序 | BaseAction | After | 條件 |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1    | 1     | true      |
| Action3 |          |            |       | true      |



 

[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| 動作  | 順序 | BaseAction | After | 條件 |
|---------|----------|------------|-------|-----------|
| Action1 | 1        |            |       | true      |



 

若要修正這些錯誤，請嘗試下列動作：

-   移除自訂動作 Action1 的序號，並改為使用 BaseAction 和 After 欄位。
-   在 [順序]、[BaseAction] 或 [自訂動作 Action3 的欄位] 欄位中輸入值。 將 [BaseAction] 和 [After] 欄位保留為 [標準動作 Action2]。
-   請勿將 [順序] 欄位保留為 [標準動作 Action2]。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 




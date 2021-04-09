---
description: 如果合併模組必須修改目標 .msi 檔案的動作順序資料表，請在 .msm 檔案中包含 MergeModuleSequence 資料表。 合併不會將這些資料表加入至 .msi 檔案。 這些資料表只會出現在合併模組中。
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: 撰寫合併模組順序資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b21780601e626c006967cefa0dcff5700bdec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944010"
---
# <a name="authoring-merge-module-sequence-tables"></a>撰寫合併模組順序資料表

如果合併模組必須修改目標 .msi 檔案的動作 [*順序資料表*](s-gly.md) ，請在 .msm 檔案中包含 MergeModuleSequence 資料表。 合併不會將這些資料表加入至 .msi 檔案。 這些資料表只會出現在合併模組中。

如果有任何 ModuleSequence 資料表存在於 .msm 檔案中，則您也必須將對應的安裝程式順序資料表的空白複本撰寫至合併模組。 例如，如果 merge 模組包含 ModuleAdminExecuteSequence 資料表，則合併模組也必須包含空的 AdminExecuteSequence 資料表。 在合併期間，這些空白資料表會以必要的架構指導方針提供合併工具。

在合併模組順序資料表中使用 [標準動作](standard-actions.md) 時，[順序] 資料行中的值應該是標準動作的建議動作序號。 請參閱下面提供的建議動作順序，以取得每個順序資料表中的建議序號。 如果 merge module sequence 資料表中的序號與 .msi 檔案中相同動作的序號不同，則合併工具會在合併期間使用 .msi 檔案中的序號。



| MergeModuleSequence 資料表                                                    | 建議的動作順序                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)                     | [建議的 AdminUISequence](suggested-adminuisequence.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)           | [建議的 AdminExecuteSequence](suggested-adminexecutesequence.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                       | [建議的 AdvtUISequence](suggested-advtuisequence.md)                 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)             | [建議的 AdvtExecuteSequence](suggested-advtexecutesequence.md)       |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)                 | [建議的 InstallUISequence](suggested-installuisequence.md)           |
| [ModuleInstallExecuteSequence 資料表](moduleinstallexecutesequence-table.md) | [建議的 InstallExecuteSequence](suggested-installexecutesequence.md) |



 

如果在 merge module sequence 資料表的動作資料行中使用 [標準動作](standard-actions.md) ，則該記錄的 BaseAction 和 After 資料行必須是 Null。

如果自訂動作或對話方塊輸入到 [動作] 資料行中，則 [順序] 資料行必須是 Null。

如果在 [動作] 資料行中輸入傳回終止旗標的動作，[順序] 資料行應該會包含該旗標的負數值，且該記錄的 BaseAction 和 After 資料行必須是 Null。 下列負數值表示如果安裝程式傳回終止旗標，則會呼叫動作。



| 終止旗標          | 值 | 描述              |
|---------------------------|-------|--------------------------|
| msiDoActionStatusSuccess  | -1    | 順利完成。   |
| msiDoActionStatusUserExit | -2    | 使用者終止安裝。 |
| msiDoActionStatusFailure  | -3    | 嚴重結束終止。   |
| msiDoActionStatusSuspend  | -4    | 安裝已暫停。    |



 

BaseAction 資料行可包含標準動作、在合併模組的自訂動作資料表中指定的自訂動作，或在模組的對話方塊資料表中指定的對話方塊。 BaseAction 資料行是此資料表之 [動作] 資料行中的索引鍵。 它不能是 .msi 檔案中其他合併資料表或資料表的外鍵。 這表示 BaseAction 資料行中所列的每個標準動作、自訂動作或對話方塊，也必須列在此資料表中另一筆記錄的 [動作] 資料行中。

 

 




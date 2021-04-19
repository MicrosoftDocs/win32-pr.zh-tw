---
description: ICEM03 會確認模組中的所有動作都是基本動作，或衍生自有效的基底動作。
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980320"
---
# <a name="icem03"></a>ICEM03

ICEM03 會確認模組中的所有動作都是基本動作，或衍生自有效的基底動作。

Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。

## <a name="result"></a>結果

ICEM03 會張貼模組的錯誤訊息，其中包含不是基底動作或衍生自有效基底動作之順序資料表中的動作。

## <a name="example"></a>範例

ICEM03 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[ModuleInstallExecuteSequence 資料表](moduleinstallexecutesequence-table.md)



| 動作  | 順序 | BaseAction | After | 條件 |
|---------|----------|------------|-------|-----------|
| Action1 |          | Action2    | 0     |           |
| Action2 |          | Action1    | 0     |           |



 

ICEM03 會張貼這兩個動作的錯誤，因為它們會將其視為 ModuleInstallExecuteSequence 資料表中的基底動作。 [ModuleAdminUISequence](moduleadminuisequence-table.md)、 [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)、 [ModuleAdvtUISequence](moduleadvtuisequence-table.md)、 [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)、 [ModuleInstallUISequence](moduleinstalluisequence-table.md)和[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)資料表中的所有動作都必須是基底動作，或從另一個動作和前後旗標的組合衍生其位置。

若要修正這個錯誤，請判斷這兩個動作的基本動作。 使用預設序號新增基底動作的記錄。 針對 Action1 和 Action2，請在 [BaseAction] 資料行中輸入基底動作名稱，然後在 [After] 資料行中輸入0或1。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 




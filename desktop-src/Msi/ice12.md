---
description: ICE12 會驗證 Windows Installer 資料庫的 CustomAction、Directory、AdminExecuteSequence、AdminUISequence、AdvtExecuteSequence、InstallExecuteSequence 和 InstallUISequence 資料表。
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998125"
---
# <a name="ice12"></a>ICE12

ICE12 會查詢 [CustomAction](customaction-table.md)、 [Directory](directory-table.md)、 [AdminExecuteSequence](adminexecutesequence-table.md)、 [AdminUISequence](adminuisequence-table.md)、 [AdvtExecuteSequence](advtexecutesequence-table.md)、 [InstallExecuteSequence](installexecutesequence-table.md)和 [InstallUISequence](installuisequence-table.md) 資料表，以驗證下列各項：

-   [CostFinalize 動作](costfinalize-action.md)發生于任何順序資料表中，其中包含類型[自訂動作類型 35](custom-action-type-35.md)或[自訂動作類型 51](custom-action-type-51.md)的動作。
-   每個 [自訂動作類型 35](custom-action-type-35.md) 都是在 [CostFinalize 動作](costfinalize-action.md)之後。 在順序資料表中。
-   針對 CustomAction 資料表之來源資料行中的目錄資料表具有外鍵的每個 [自訂動作類型 51](custom-action-type-51.md) ，都會出現在順序資料表中的 [CostFinalize 動作](costfinalize-action.md) 之前。

請注意，ICE12 不會驗證 CustomAction 資料表的目標資料行中格式化的文字。

## <a name="result"></a>結果

如果設定目錄屬性的自訂動作驗證失敗，ICE12 會張貼錯誤訊息。

## <a name="example"></a>範例

ICE12 會針對所顯示的範例張貼三個錯誤。

-   針對 CA1，在目錄資料表中找不到資料夾 ' MyFolder '
-   若為 CA2，順序 ' 80 ' 會在 InstallExecuteSequence 資料表中 CostFinalize 之前出現。 它必須在 (之後 CF@100) 
-   若為 CA3，序列 ' 125 ' 會出現在 InstallExecuteSequence 資料表的 CostFinalize 之後。 它必須在 (之前 CF@100) 

[CustomAction 資料表](customaction-table.md) (部分) 



| 動作 | 類型 | 來源        |
|--------|------|---------------|
| CA1    | 35   | MyFolder      |
| CA2    | 35   | WindowsFolder |
| CA3    | 51   | WindowsFolder |



 

[目錄資料表](directory-table.md)



| 目錄     | 目錄 \_ 父系 | DefaultDir    |
|---------------|-------------------|---------------|
| TARGETDIR     |                   | SourceDir     |
| WindowsFolder | TARGETDIR         | WindowsFolder |



 

[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) 



| 動作       | 順序 |
|--------------|----------|
| CostFinalize | 100      |
| CA2          | 80       |
| CA3          | 125      |



 

若要修正 CA1 的錯誤，請將其 CustomAction 資料表中來源資料行的專案變更為目錄資料表中的現有專案，或將 MyFolder 加入目錄資料表中。

若要修正 CA2 的錯誤，請在 InstallExecuteSequence 資料表中變更其順序，使其在 CostFinalize 動作之後。

若要修正 CA3 的錯誤，請在 InstallExecuteSequence 資料表中變更其順序，使其在 CostFinalize 動作之前。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




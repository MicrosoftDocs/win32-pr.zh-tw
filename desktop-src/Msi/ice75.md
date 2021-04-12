---
description: ICE75 會確認所有自訂動作類型 17 (DLL) 、自訂動作類型 18 (EXE) 、自訂動作類型 21 (JScript) 和自訂動作類型 22 (VBScript) 自訂動作會在 CostFinalize 動作之後排序。
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319919"
---
# <a name="ice75"></a>ICE75

ICE75 會確認所有 [自訂動作類型 17](custom-action-type-17.md) (DLL) 、 [自訂動作類型 18](custom-action-type-18.md) (EXE) 、 [自訂動作類型 21](custom-action-type-21.md) (JScript) 和 [自訂動作類型 22](custom-action-type-22.md) (VBScript) 自訂動作會在 [CostFinalize 動作](costfinalize-action.md)之後排序。 這些類型的自訂動作會使用已安裝的檔案作為其來源。 ICE75 會檢查 [InstallUISequence 資料表](installuisequence-table.md)、 [InstallExecuteSequence 資料表](installexecutesequence-table.md)、 [AdminUISequence 資料表](adminuisequence-table.md)和 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)。 請注意，這些順序資料表中必須要有 CostFinalize 動作。

## <a name="result"></a>結果

ICE75 會在使用已安裝的檔案做為原始程式檔（未在 CostFinalize 動作之後排序）找到自訂動作時張貼錯誤。

## <a name="example"></a>範例

ICE75 會針對所顯示的範例報告下列錯誤：

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

[CustomAction 資料表](customaction-table.md) (部分) 



| 動作      | 類型 | 來源  |
|-------------|------|---------|
| CA \_ FileExe | 18   | FileExe |
| CA \_ FileDLL | 17   | FileDLL |



 

[AdminUISequence 資料表](adminuisequence-table.md) (部分) 



| 動作      | 順序 |
|-------------|----------|
| CA \_ FileExe | 1100     |



 

[AdminExecuteSequence 資料表](adminexecutesequence-table.md) (部分) 



| 動作       | 順序 |
|--------------|----------|
| CA \_ FileDLL  | 800      |
| CostFinalize | 1000     |



 

若要修正錯誤，請在 CostFinalize 動作之後排列自訂動作的順序。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




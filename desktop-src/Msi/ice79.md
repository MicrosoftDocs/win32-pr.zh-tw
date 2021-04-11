---
description: ICE79 會使用 Condition 資料類型來驗證資料庫欄位中所輸入之元件和功能的參考。
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113849"
---
# <a name="ice79"></a>ICE79

ICE79 會使用 [Condition](condition.md) 資料類型來驗證資料庫欄位中所輸入之元件和功能的參考。

## <a name="result"></a>結果

ICE79 會發佈兩個警告。



| ICE79 警告                                                                      | Description                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 資料庫缺少 \_ 驗證資料表。 無法完全檢查屬性名稱。 | 資料庫缺少[ \_ 驗證資料表](-validation-table.md)。 |
| 從 \[ \] 表1中的資料行2取出值時發生錯誤 \[ \] 。 略過資料行。         | 抓取值時發生錯誤。                                          |



 

ICE79 會張貼兩個錯誤。



| ICE79 錯誤                                                          | Description                               |
|----------------------------------------------------------------------|-------------------------------------------|
| 在資料行 '% s ' 中參考的元件 '% ls '。% s ' 的資料列% s 無效。 | 找到不正確元件參考。 |
| 在資料行 '% s ' 中參考的功能 '% ls '。% s ' 的資料列% s 無效。   | 找到不正確功能參考    |



 

## <a name="example"></a>範例

ICE79 會報告範例的下列錯誤：

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

在此範例中， [元件資料表](component-table.md) 中的 NoSuchComponent 不存在，而且 [功能資料表](feature-table.md)中沒有 NoSuchFeature。

[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) 



| 動作  | 條件                                |
|---------|------------------------------------------|
| Custom1 | TESTACTION = 1046 和 &NoSuchFeature>2  |
| Custom2 | TESTACTION = 146 和 $NoSuchComponent>2 |



 

若要修正這些錯誤，請在功能和元件資料表中輸入 NoSuchFeature 和 NoSuchComponent 的有效記錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型19。
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: 自訂動作類型19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cbbef4ec07d805e41c0de25c371f995782ce3d8df66a89ee93363afa05f55b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075058"
---
# <a name="custom-action-type-19"></a>自訂動作類型19

此自訂動作會顯示指定的錯誤訊息、傳回失敗，然後結束安裝。 顯示的錯誤訊息可提供為字串或 [錯誤資料表](error-table.md)中的索引。

## <a name="source"></a>來源

將 [CustomAction 資料表](customaction-table.md) 的來源資料行保留空白。

## <a name="type-value"></a>類型值

在 CustomAction 資料表的 Type 資料行中包含下列值，以指定基本的數數值型別。



| 常數                                                               | 十六進位 | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  + **msidbCustomActionTypeSourceFile** | 0x013       | 19      |



 

## <a name="target"></a>目標

[CustomAction 資料表](customaction-table.md)的目標資料行包含使用 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (中指定的功能來格式化的文字字串，而不含數值欄位規範) 。 要取代的參數會以方括弧（...）括住， \[ \] 而且可能是屬性、環境變數 (% prefix) 、檔案路徑 (\# 首碼) 或元件目錄路徑 ($ prefix) 。 如果將字串格式化為整數，則會使用該整數做為 [錯誤資料表](error-table.md) 的索引，以取得要顯示的訊息。 如果在格式化字串之後包含非數位字元，則字串本身會顯示為訊息。

## <a name="return-processing-options"></a>傳回處理選項

自訂動作不會使用任何選項。

## <a name="execution-scheduling-options"></a>執行排程選項

自訂動作不會使用任何選項。

## <a name="in-script-execution-options"></a>In-Script 執行選項

自訂動作不會使用任何選項。

## <a name="return-values"></a>傳回值

請參閱 [自訂動作傳回值](custom-action-return-values.md)。

## <a name="remarks"></a>備註

例如，自訂動作 CAError1、CAError2、CAError3 和 CAError4 會傳回這些訊息。

[CustomAction 資料表](customaction-table.md)



| 動作   | 類型 | 來源 | 目標                              |
|----------|------|--------|-------------------------------------|
| CAError1 | 19   |        | \[Prop1\]                           |
| CAError2 | 19   |        | 因為 Error2，所以安裝失敗。 |
| CAError3 | 19   |        | 25000                               |
| CAError4 | 19   |        | \[This.prop2\]                           |



 

[屬性工作表](property-table.md)



| 屬性 | 值                                 |
|----------|---------------------------------------|
| Prop1    | 「由於 Error1 的安裝失敗。」 |
| This.prop2    | "25100"                               |



 

[錯誤資料表](error-table.md)



| 程式碼  | 訊息                             |
|-------|-------------------------------------|
| 25000 | 因為 Error3，所以安裝失敗。 |
| 25100 | 因為 Error4，所以安裝失敗。 |



 

這些自訂動作會傳回下列錯誤訊息：



| 自訂動作 | 傳回的訊息字串             |
|---------------|-------------------------------------|
| CAError1      | 因為 Error1，所以安裝失敗。 |
| CAError2      | 因為 Error2，所以安裝失敗。 |
| CAError3      | 因為 Error3，所以安裝失敗。 |
| CAError4      | 因為 Error4，所以安裝失敗。 |



 

請注意，因為撰寫 [LaunchCondition 資料表](launchcondition-table.md)無法保證啟動狀況的評估順序，所以您應該在安裝中使用自訂動作類型19個自訂動作，以特定順序來評估條件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> </dl>

 

 




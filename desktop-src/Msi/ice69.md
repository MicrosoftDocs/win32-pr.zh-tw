---
description: ICE69 會檢查格式字串中 $componentkey 格式的所有子字串都 \[ \] 不會交互參照元件。
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194398"
---
# <a name="ice69"></a>ICE69

ICE69 會檢查格式字串中 $componentkey 格式的所有子字串都 \[ \] 不會交互參照元件。 [](formatted.md) 當 \[ 格式化字串的 $componentkey 屬性參考的元件 \] 不是儲存在資料表的元件資料行中的元件時，就會發生跨元件參考 \_ 。

跨元件參考的問題會從評估 [格式化](formatted.md) 字串的方式產生。 如果已安裝 $componentkey 屬性所參考的元件， \[ \] 但目前的安裝期間未變更 (例如，正在重新安裝、移至來源等等) ，運算式 \[ $componentkey \] 會評估為 null，因為 $componentkey 中元件的動作狀態 \[ \] 為 null。 升級和修復作業期間可能會發生類似的問題。

## <a name="result"></a>結果

如果 \[ \] [格式化](formatted.md) 字串內的 $componentkey 子字串交互參考另一個功能中的元件，ICE69 會傳回錯誤。 如果 \[ \] 格式化字串內的 $componentkey 子字串交互參考相同功能中的元件，ICE69 會傳回警告。  (使用 [FeatureComponents](featurecomponents-table.md) 資料表來判斷此對應。 它必須對應至警告的相同功能。 參考父功能中的元件或子功能中參考的元件會被視為錯誤。 ) 

如果 \[ \# \] [格式化](formatted.md)字串中的 FileKey 子字串參考[的檔案](file-table.md)未在檔案資料表中指定為屬於相同元件，ICE69 會報告錯誤。

## <a name="example"></a>範例

ICE69 會報告下列範例所示的範例。

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

若要修正這個錯誤，請不要交互參照元件。 將 \[ $componentkey 變更 \] 為符合快速鍵的元件。

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵  | 元件\_ | 引數     |
|-----------|-------------|--------------|
| 測試      | QuickTest   | -v \[ $Test\] |
| Shortcut2 | QuickTest   | \[$Test 2\]   |



 

[動詞](verb-table.md)和[延伸](extension-table.md)資料表是特殊案例，因為動詞資料表會參考屬於元件的副檔名。 不過，延伸模組可以屬於多個元件，因為擴充功能資料表的主鍵是由擴充功能和元件資料行所組成 \_ 。 在邏輯上，您可能會發生下列情況。

[動詞資料表](verb-table.md) (部分) 



| 分機 | 動詞\_ | 引數                |
|-----------|--------|-------------------------|
| Tst       | 開啟   | -v \[ $comp 1 \] \[ $comp 2\] |



 

[延伸模組資料表](extension-table.md) (部分) 



| 分機 | 元件\_ |
|-----------|-------------|
| Tst       | comp1       |
| Tst       | comp2       |



 

[FeatureComponents 資料表](featurecomponents-table.md)



| 功能\_ | 元件\_ |
|-----------|-------------|
| Feature1  | QuickTest   |
| Feature1  | 測試        |
| Feature2  | Test2       |



 

在此情況下，您必須確定至少有一個 \[ $componentkey \] 屬性評估為非 null 值。 不過，在 \[ \] 上述範例中，動詞資料表的 Argument 資料行中的每個 $componentkey 屬性 (\[ $comp 1 \] 和 \[ $comp 2 \]) 必須參考與動詞相關聯之延伸模組隨附的可能元件。 類似 \[ $comp 3 的參考 \] 會導致 ICE69 的警告。

[AppId 資料表](appid-table.md)與動詞資料表有類似的情況。 它會使用 [類別表](class-table.md) 作為其元件參考。 在此情況下，AppId 資料表的驗證方式與 Verb-Extension 驗證 (現在是 AppId 類別) 。

類別資料表的引數資料行會像 [快速鍵](shortcut-table.md) [、登錄和類似](registry-table.md)的資料表一樣進行驗證。

## <a name="table-used-during-execution-only-if-found"></a>只有在找到時，才會在執行 (中使用資料表) 

[IniFile](inifile-table.md)

[RemoveIniFile](removeinifile-table.md)

[登錄](registry-table.md)

[RemoveRegistry](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[ServiceInstall](serviceinstall-table.md)

[快速鍵](shortcut-table.md)

[動詞](verb-table.md)

[分機](extension-table.md)

[類別](class-table.md)

[AppId](appid-table.md)

[環境](environment-table.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




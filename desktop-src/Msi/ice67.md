---
description: ICE67 會檢查非公告快捷方式的目標是否屬於與快捷方式本身相同的元件，或目標群組件的屬性確定不會變更安裝位置。
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b25f3bba6bd6efaf20b55982524840348f39e8717dc53b7699a6f5f2886df01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787388"
---
# <a name="ice67"></a>ICE67

ICE67 會檢查非公告快捷方式的目標是否屬於與快捷方式本身相同的元件，或目標群組件的屬性確定不會變更安裝位置。

如果目標群組件變更狀態且來源元件不正確，則無法修正 ICE67 回報的警告或錯誤，可能會導致快捷方式無效。 例如，當目標檔案的元件設定為從來源執行時，將元件變更為本機的重新安裝會導致元件中包含未重新安裝快捷方式的元件。 因此，快捷方式會指向不正確位置。

請注意，在某些情況下，使用不同的快捷方式元件是不可避免的。 例如，如果在使用者設定檔中建立快捷方式，並將該檔案安裝至非設定檔目錄，則您可能無法對這兩個數據使用相同的元件。  (這會導致多使用者案例失敗，例如 [ICE57](ice57.md)) 中所述。 在這種情況下，您可以使用已公告的快捷方式來達到您想要的行為，也可以直接確認目標群組件不能從來源執行變更為本機。

## <a name="result"></a>結果

如果非公告快捷方式的目標不屬於與快捷方式本身相同的元件，或目標群組件的屬性不確定安裝位置不會變更，ICE67 會傳回錯誤或警告。

## <a name="example"></a>範例

ICE67 會報告下列範例所示的警告和錯誤。

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

Shortcut1 是由 Component2 所安裝，但其目標檔案 File1 是由 component1 所安裝。 目標群組件標示為選擇性 (表示它可以是本機或從來源執行) 。 可能會造成問題的其中一個可能的情況是 Component1 從來源執行變更為本機。 這會導致 Shortcut1 指向不正確位置。

若要修正此警告，請將快捷方式安裝為 Component1 的一部分，或將 Component1 標示為 LocalOnly 或 SourceOnly。

[檔資料表](file-table.md) (部分) 



| 檔案  | 元件\_ |
|-------|-------------|
| File1 | Component1  |



 

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵  | 元件\_ | 目標      |
|-----------|-------------|-------------|
| Shortcut1 | Component2  | \[\#1\] |



 

[元件資料表](component-table.md) (部分) 



| 元件  | 屬性 |
|------------|------------|
| Component1 | 2          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




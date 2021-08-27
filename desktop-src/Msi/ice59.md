---
description: ICE59 檢查公告的快捷方式屬於快捷方式的目標功能所安裝的元件。
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1a8d6318a9b4525941edd3873c9fc35bd11f488e42c8a82da71c4b2c0b9b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044018"
---
# <a name="ice59"></a>ICE59

ICE59 檢查公告的快捷方式屬於快捷方式的目標功能所安裝的元件。

ICE59 回報的錯誤通常會導致下列行為：

1.  通告的快捷方式會啟動 Windows Installer，以安裝 [目標] 資料行中所列的功能。
2.  但是，由於 [FeatureComponents 資料表](featurecomponents-table.md) 不會將目標功能對應到包含快捷方式的元件，因此不會安裝快捷方式) 所啟用之元件 (的 keyfile。
3.  因此，快捷方式會中斷，且不會進行任何動作。

## <a name="result"></a>結果

如果公告的快捷方式不屬於快捷方式的目標功能所安裝的元件，ICE59 會張貼錯誤。

## <a name="example"></a>範例

ICE59 會針對所顯示的範例報告下列錯誤：

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

在此情況下，ShortcutB 會通告 FeatureA，啟動時，會啟動 ComponentB 的金鑰檔。 但 FeatureA 永遠不會安裝 ComponentB，因此即使在隨選安裝階段完成後，快速鍵的目標也不存在。

若要修正這個錯誤，請將資料列加入至關聯 FeatureA 和 ComponentB 的 [FeatureComponents 資料表](featurecomponents-table.md) 中。

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵  | 目標   | 元件\_ |
|-----------|----------|-------------|
| ShortcutB | FeatureA | ComponentB  |



 

[FeatureComponents 資料表](featurecomponents-table.md)



| 特徵\_ | 元件\_ |
|-----------|-------------|
| FeatureA  | ComponentA  |



 

[功能表](feature-table.md) (部分) 



| 功能  | 層級 |
|----------|-------|
| FeatureA | 10    |



 

[元件資料表](component-table.md) (部分) 



| 元件  | KeyPath |
|------------|---------|
| ComponentA | >filea.docx   |
| ComponentB | >fileb.docx   |



 

[檔資料表](file-table.md) (部分) 



| 檔案  | 元件\_ | 順序 |
|-------|-------------|----------|
| >filea.docx | ComponentA  | 1        |
| >fileb.docx | ComponentB  | 2        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




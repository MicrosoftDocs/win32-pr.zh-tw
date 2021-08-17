---
description: ICE36 會驗證圖示資料表中的每個圖示至少在 ARPPRODUCTICON 屬性或類別、ProgId 或快速鍵資料表中列出一次。
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c3d951e90ac9f3dc46a564757c1a1d5a1737bf054740e3109a26c8c7b91055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635301"
---
# <a name="ice36"></a>ICE36

ICE36 會驗證圖示資料表中的每個圖示至少在 [**ARPPRODUCTICON**](arpproducticon.md) 屬性或 [類別](class-table.md)、 [ProgId](progid-table.md)或 [快速鍵](shortcut-table.md) 資料表中列出一次。

在公告期間，安裝程式會安裝使用者電腦上 [圖示表格](icon-table.md) 中所列的所有圖示。 在圖示表格中具有未使用的圖示，並不會防止安裝執行，不過它會不必要地增加 .msi 檔案的大小，以及通告功能所需的時間和空間。

如果屬性或資料表中未參考圖示，而且沒有提供 UI 可在執行時間建立參考，您應該移除圖示以達到更佳的效能。

## <a name="result"></a>結果

如果未在 [類別](class-table.md)、 [ProgId](progid-table.md)或 [快捷方式](shortcut-table.md) 表中參考的圖示表格中有圖示，且未提供可在執行時間建立這類參考的 UI，ICE36 會張貼訊息。

## <a name="example"></a>範例

ICE36 會針對所顯示的範例報告下列錯誤。

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

[圖示表格](icon-table.md) (部分) 



| Name  | 資料     |
|-------|----------|
| Icon1 | Control1 |
| Icon2 | Control2 |
| Icon3 | Control3 |
| Icon4 | Control4 |



 

[ProgID 資料表](progid-table.md) (部分) 



| ProgID    |
|-----------|
| Property1 |



 

[類別表](class-table.md) (部分) 



| CLSID                                  |
|----------------------------------------|
| {3E469ABA-3644-11d2-8892-00A0C981B015} |



 

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵  | 圖示\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




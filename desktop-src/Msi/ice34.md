---
description: ICE34 會驗證每個 RadioButtonGroup 控制項上的每個選項按鈕，在選項按鈕資料表的屬性資料行中都有一個屬性，該屬性會指定其選項按鈕群組。
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979901"
---
# <a name="ice34"></a>ICE34

ICE34 會驗證每個 [RadioButtonGroup 控制項](radiobuttongroup-control.md) 上的每個選項按鈕，在選項按鈕 [資料表](radiobutton-table.md) 的屬性資料行中都有一個屬性，該屬性會指定其選項按鈕群組。 ICE34 會驗證這個屬性是否存在，並設定為 [屬性工作表](property-table.md) 中的預設值，此值等於選項按鈕資料表之 [值] 資料行中的其中一個群組選項按鈕值。

選項按鈕群組必須有預設值，使用者才能使用 TAB 鍵來選取選擇。 這是適當的使用者協助工具所需的。

ICE34 報告遺漏的資料表。

## <a name="result"></a>結果

如果有指定無效屬性的選項按鈕，ICE34 會張貼錯誤訊息。

## <a name="example"></a>範例

ICE34 會針對所顯示的範例報告下列錯誤。



| ICE34 錯誤                                                                                                                                                                | Description                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 控制項 DialogA。 Control2 必須有屬性，因為它的類型是 RadioButtonGroup。                                                                                      | 有一個[RadioButtonGroup 控制項](radiobuttongroup-control.md)，沒有在[控制資料表](control-table.md)的 [屬性] 資料行中設定[間接控制](indirect-control-attribute.md)位，而且沒有在 [屬性] 資料行中列出屬性。 |
| 可能不是使用屬性 Property3 之 RadioButtonGroup 的有效預設值。 值必須列為 RadioButtonGroup 資料表中的選項。                 | 在 [屬性工作表](property-table.md) 的 [值] 資料行中指定的屬性預設值，不是 [選項按鈕] [資料表](radiobutton-table.md)的 [值] 資料行中所指定之選項按鈕群組的其中一個值。                  |
| 必須定義屬性 PropertyB，因為它是 RadioButtonGroup 控制項 DialogA 的間接屬性。 Control4                                                       | 這個選項按鈕群組參考的屬性是間接屬性，而間接屬性的值不是選項按鈕群組的其中一個選項。                                                                                                       |
| 可能不是屬性 PropertyA 的有效預設值。 屬性是控制項 DialogA. Control5 (的間接 RadioButtonGroup 屬性（透過屬性 Property5) ）。 | 透過控制項參考的間接屬性值不是該 RadioButtonGroup 的其中一個預設值。                                                                                                                                                    |



 

[控制資料表](control-table.md) (部分) 



| 對話  | 控制  | 類型             | 屬性 | 屬性  |
|---------|----------|------------------|------------|-----------|
| DialogA | Control1 | RadioButtonGroup | 0          | Property1 |
| DialogA | Control2 | RadioButtonGroup | 0          |           |
| DialogA | Control3 | RadioButtonGroup | 0          | Property3 |
| DialogA | Control4 | RadioButtonGroup | 8          | Property4 |
| DialogA | Control5 | RadioButtonGroup | 8          | Property5 |



 

[屬性工作表](property-table.md) (部分) 



| 屬性  | 值     |
|-----------|-----------|
| Property1 | Yes       |
| Property3 | 可能     |
| Property4 | PropertyB |
| Property5 | PropertyA |
| PropertyA | 可能     |



 

[選項按鈕資料表](radiobutton-table.md) (部分) 



| 屬性  | 單 | 值 |
|-----------|-------|-------|
| Property1 | 1     | 是   |
| Property1 | 2     | Now   |
| Property2 | 1     | 是   |
| Property2 | 2     | 否    |
| Property3 | 1     | 是   |
| Property3 | 2     | 否    |
| Property4 | 1     | 是   |
| Property4 | 2     | 否    |
| PropertyA | 1     | 是   |
| PropertyA | 2     | 否    |
| PropertyB | 1     | 是   |
| PropertyB | 2     | 否    |



 

若要修正此 ICE 回報的錯誤，請檢查下列各項：

-   沒有間接屬性集的每個選項按鈕控制項專案都有屬性欄中列出的屬性：
-   每個這類屬性在選項按鈕資料表中至少有一個對應的專案。
-   每個此類屬性都定義于屬性資料表中，其值為選項按鈕資料表中的其中一個選項。
-   在屬性工作表中，會定義在選項按鈕控制項的屬性資料行中所參考的每個屬性（attribute）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




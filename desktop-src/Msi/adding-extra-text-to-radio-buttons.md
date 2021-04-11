---
description: 螢幕讀取程式只能讀取已在選項按鈕資料表的文字資料行中撰寫之 RadioButtonGroup 控制項的文字。
ms.assetid: 92ad70ec-a3a4-4ea7-8888-40c78d73e58a
title: 在選項按鈕中加入額外的文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e73ac55e300ddee603449e9ea7ce5e10f4e0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944042"
---
# <a name="adding-extra-text-to-radio-buttons"></a>在選項按鈕中加入額外的文字

螢幕讀取程式只能讀取已在[選項按鈕資料表](radiobutton-table.md)的文字資料行中撰寫之[RadioButtonGroup 控制項](radiobuttongroup-control.md)的文字。 如果此文字是選項按鈕的不足描述，則可以加入重迭的 [文字控制項](text-control.md) 來提供額外的描述性文字。 這些文字控制項應該在對話方塊中彼此重迭，並在 [ControlCondition 資料表](controlcondition-table.md) 中設定條件，如此一來，一次只會顯示一個文字控制項。 文字控制項不能重迭 RadioButtonGroup 控制項或對話方塊中的其他控制項，因為這樣會讓螢幕讀取器看不到控制項。 當使用者將游標停留在文字控制項上方時，螢幕讀取程式會讀取額外的文字。

在下列範例中，[MySample] 對話方塊有一個名為 [色彩] 的 RadioButtonGroup 控制項，其中有兩個 [TheColor] 屬性值的選項。 針對每個選擇，都有一個具有要隱藏或顯示之條件的文字控制項，視目前針對 TheColor 選取的選擇而定。 初始 TheColor 值定義于屬性工作表中。 文字控制項具有在選項按鈕資料表的文字欄位中撰寫的額外描述性文字。 當使用者將游標停留在對話方塊中的文字控制項上方時，螢幕讀取器可以讀取目前選擇的額外描述。

[對話方塊資料表](dialog-table.md)



| 對話   | HCentering | VCentering | 寬度 | 高度 | 屬性 | 標題                    | \_先控制項 | 控制項 \_ 預設值 | 控制 \_ 取消 |
|----------|------------|------------|-------|--------|------------|--------------------------|----------------|------------------|-----------------|
| MySample | 50         | 50         | 200   | 180    | 3          | 可存取的選項按鈕 | 色彩         | 下一個             |                 |



 

[控制資料表](control-table.md)



| 對話\_ | 控制    | 類型             | X   | Y   | 寬度 | 高度 | 屬性 | 屬性 | Text                               | 控制 \_ 下一步 | Help |
|----------|------------|------------------|-----|-----|-------|--------|------------|----------|------------------------------------|---------------|------|
| MySample | 色彩     | RadioButtonGroup | 2   | 20  | 100   | 50     | 3          | TheColor |                                    | 下一個          |      |
| MySample | HowIsBlue  | Text             | 20  | 80  | 150   | 15     | 2          |          | 這就像是一天的天空。 |               |      |
| MySample | HowIsGreen | Text             | 20  | 80  | 150   | 15     | 2          |          | 這就像是彈簧中的草坪一樣。    |               |      |



 

[選項按鈕資料表](radiobutton-table.md)



| 屬性 | 單 | 值 | X   | Y   | 寬度 | 高度 | Text   | Help |
|----------|-------|-------|-----|-----|-------|--------|--------|------|
| TheColor | 1     | 藍色  | 10  | 10  | 80    | 15     | &藍色  |      |
| TheColor | 2     | 綠色 | 10  | 30  | 80    | 15     | &綠色 |      |



 

[屬性工作表](property-table.md)



| 屬性 | 值 |
|----------|-------|
| TheColor | 藍色  |



 

[ControlCondition 資料表](controlcondition-table.md)



| 對話\_ | 控制項\_  | 動作 | 條件                 |
|----------|------------|--------|---------------------------|
| MySample | HowIsBlue  | 隱藏   | TheColor <>  "Blue"  |
| MySample | HowIsBlue  | 顯示   | TheColor = "Blue"         |
| MySample | HowIsGreen | 隱藏   | TheColor <>  "綠" |
| MySample | HowIsGreen | 顯示   | TheColor = "綠"        |



 

如需詳細資訊，請參閱 [協助工具](accessibility.md)。

 

 




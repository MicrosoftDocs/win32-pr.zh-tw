---
description: 選項按鈕不會被視為個別控制項，但它們是做為 RadioButtonGroup 控制項之選項按鈕群組的一部分。 選項按鈕表格會列出所有群組的按鈕。
ms.assetid: 7f8f278a-a737-4116-9938-2850dbb611fa
title: 選項按鈕資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097f8fbe3081c865e3668631ed0fa9d43a4488cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192646"
---
# <a name="radiobutton-table"></a>選項按鈕資料表

選項按鈕不會被視為個別控制項，但它們是做為 [RadioButtonGroup 控制項](radiobuttongroup-control.md)之選項按鈕群組的一部分。 選項按鈕表格會列出所有群組的按鈕。

選項按鈕資料表具有下列資料行。



| Column   | 類型                         | 答案 | Nullable |
|----------|------------------------------|-----|----------|
| 屬性 | [識別碼](identifier.md) | Y   | N        |
| 單    | [整數](integer.md)       | Y   | N        |
| 值    | [格式 化](formatted.md)   | N   | N        |
| X        | [整數](integer.md)       | N   | N        |
| Y        | [整數](integer.md)       | N   | N        |
| 寬度    | [整數](integer.md)       | N   | N        |
| 高度   | [整數](integer.md)       | N   | N        |
| Text     | [格式 化](formatted.md)   | N   | Y        |
| Help     | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

要系結至這個選項按鈕的命名屬性。 所有系結至相同屬性的按鈕都會變成相同群組的一部分。

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>以
</dt> <dd>

用來決定某個清單中專案順序的正整數。 整數不需要是連續的。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

與這個按鈕相關聯的值字串。 選取此按鈕會將相關聯的屬性設定為此值。

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

選項按鈕之周框左上角的群組內的水準座標。 此值必須是非負數。

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

選項按鈕的周框左上角的群組內的垂直座標。 此值必須是非負數。

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>寬度
</dt> <dd>

按鈕的寬度。 此值必須是非負數。

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>高度
</dt> <dd>

按鈕的高度。 此值必須是非負數。

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本
</dt> <dd>

要指派給選項按鈕的可當地語系化、可見的標題。 如果文字太長而無法容納在控制項上，則會被截斷。 如果按鈕顯示圖示或點陣圖，則此資料行包含圖片的名稱，這是 [二進位資料表](binary-table.md)中的索引鍵。 沒有任何方法可以在按鈕上顯示圖片和文字。

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>説明
</dt> <dd>

搭配按鈕使用的說明字串。 文字是選擇性的，且可當地語系化。 字串會分割成兩個部分，並以字元 (\|) 。 字串的第一個部分是用來做為工具提示文字。 螢幕讀取器會針對包含圖片的控制項顯示此文字。 第二個部分是用於即時線上說明，雖然尚未實行內容相關的協助。 即使只有兩種類型的文字中有一種，也需要分隔符號。

</dd> </dl>

## <a name="remarks"></a>備註

X、y、寬度和高度的整數值是在 [安裝程式單位](installer-units.md)中，而不是對話方塊單位。 安裝程式單位等於10點 MS sans-serif 字型大小的一到第十二個高度。 控制項的座標相對於佈告欄。

按鈕的座標是相對於群組而提供。 如果群組的座標變更，則群組內的按鈕會維持在相同的相對位置。

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)函式會在建立控制項時將值和文字欄位的內容格式化，因此可以包含 **MsiFormatRecord** 函數可以解讀的任何運算式。 只有在建立控制項時，才會進行格式化，而且如果在控制項的存留期間修改了包含在運算式中的屬性，則不會更新。

每個 RadioButtonGroup 控制項都與屬性相關聯。 這個屬性的預設值必須在 [屬性工作表](property-table.md)中初始化。 在選項按鈕資料表中指定的每個 RadioButtonGroup 中，可能會有一個選項按鈕，其值欄位中的值符合這個屬性的預設值。 這是 RadioButtonGroup 控制項的預設按鈕。 預設按鈕最初會在控制項中顯示為已選取。

請注意，在選取群組中的其中一個按鈕之前，使用者無法藉由按下 RadioButtonGroup 控制項的 TAB 鍵，來變更對話方塊中的焦點。 若要讓焦點移至此按鈕群組，請按下 TAB 鍵，將其中一個按鈕指定為群組的預設按鈕。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE34](ice34.md)  
[ICE46](ice46.md)  
</dl>

 

 




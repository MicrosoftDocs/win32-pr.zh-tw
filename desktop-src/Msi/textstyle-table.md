---
description: 文字文字表格會列出具有文字的控制項中所使用的不同字型樣式。
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: 樣式表單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943568"
---
# <a name="textstyle-table"></a>樣式表單

文字文字表格會列出具有文字的控制項中所使用的不同字型樣式。

TextStyle 資料表具有下列資料行。



| Column    | 類型                               | 答案 | Nullable |
|-----------|------------------------------------|-----|----------|
| 文本 | [識別碼](identifier.md)       | Y   | N        |
| FaceName  | [Text](text.md)                   | N   | N        |
| 大小      | [整數](integer.md)             | N   | N        |
| Color     | [DoubleInteger](doubleinteger.md) | N   | Y        |
| StyleBits | [整數](integer.md)             | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>文本
</dt> <dd>

此資料行是字型樣式的名稱。 這個名稱可以內嵌在文字字串中，以表示樣式變更。 請注意，此欄位中使用的字型樣式名稱不能以字元： \_ UL 結尾。 請參閱 [加入控制項和文字](adding-controls-and-text.md)。

</dd> <dt>

<span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName
</dt> <dd>

指出字型名稱的字串。 字串的長度不能超過31個字元。

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>大小
</dt> <dd>

以點為單位的字型大小。 此值必須是非負數。

</dd> <dt>

<span id="Color"></span><span id="color"></span><span id="COLOR"></span>顏色
</dt> <dd>

這個資料行會指定 [文字控制項](text-control.md)所顯示的文字色彩。 所有其他類型的控制項一律會使用預設的文字色彩。 此資料行中的值應該使用下列公式來計算： 65536 \* blue + 256 \* 綠 + red，其中的紅色、綠色和藍色都在0-255 的範圍內。 值不得超過16777215，這是白色的值。 黑色的值為0、紅色為255、紅色為65280、綠色為、紅色為16711680、藍色和8421504。 將欄位保持空白會指定預設色彩。

請勿將透明 [文字控制項](text-control.md) 放在彩色點陣圖上方。 如果使用者變更顯示色彩配置，可能看不到文字。 例如，如果使用者設定協助工具的高對比參數，文字可能會變成隱藏。

</dd> <dt>

<span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits
</dt> <dd>

位的組合，表示文字的格式。

個別的樣式位具有下列值。



| 常數                             | 十六進位 | Decimal | 樣式      |
|--------------------------------------|-------------|---------|------------|
| **msidbTextStyleStyleBitsBold**      | 0x001       | 1       | 粗體       |
| **msidbTextStyleStyleBitsItalic**    | 0x002       | 2       | 斜體     |
| **msidbTextStyleStyleBitsUnderline** | 0x004       | 4       | Underline  |
| **msidbTextStyleStyleBitsStrike**    | 0x008       | 8       | 刪除 |



 

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE31](ice31.md)  
[ICE45](ice45.md)  
</dl>

 

 




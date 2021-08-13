---
description: 控制資料表會定義出現在每個對話方塊上的控制項。
ms.assetid: cbe7acd6-b916-45f3-b694-d2345c5a892a
title: 控制資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e1832a2cb600e8d7a27b43bc28c94836396d74a50a90b44d0e5013bde973c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638530"
---
# <a name="control-table"></a>控制資料表

控制資料表會定義出現在每個對話方塊上的控制項。

控制資料表具有下列資料行。



| Column        | 類型                               | 答案 | Nullable |
|---------------|------------------------------------|-----|----------|
| 對話\_      | [識別碼](identifier.md)       | Y   | N        |
| 控制       | [識別碼](identifier.md)       | Y   | N        |
| 類型          | [識別碼](identifier.md)       | N   | N        |
| X             | [整數](integer.md)             | N   | N        |
| Y             | [整數](integer.md)             | N   | N        |
| 寬度         | [整數](integer.md)             | N   | N        |
| 高度        | [整數](integer.md)             | N   | N        |
| 屬性    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| 屬性      | [識別碼](identifier.md)       | N   | Y        |
| Text          | [格式 化](formatted.md)         | N   | Y        |
| 控制 \_ 下一步 | [識別碼](identifier.md)       | N   | Y        |
| 說明          | [Text](text.md)                   | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>對話 框\_
</dt> <dd>

對話方塊 [資料表](dialog-table.md)的第一個資料行的外部索引鍵，也就是對話方塊的名稱。

</dd> <dt>

<span id="Control"></span><span id="control"></span><span id="CONTROL"></span>控制
</dt> <dd>

控制項的名稱。 這個名稱在對話方塊內必須是唯一的，但可以在不同的對話方塊上重複。 結合對話方塊資料行的控制項資料行會 \_ 形成此資料表的主要索引鍵。

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型
</dt> <dd>

控制項的類型。 如需控制項類型的清單，請參閱 [控制項](controls.md)。

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

控制項矩形界限左上角的水準座標。 此值必須是非負數。 請參閱 [Position 控制項屬性](position-control-attribute.md)。

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

控制項矩形界限左上角的垂直座標。 此值必須是非負數。 請參閱 [Position 控制項屬性](position-control-attribute.md)。

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>寬度
</dt> <dd>

控制項矩形邊界的寬度。 此值必須是非負數。 請參閱 [Position 控制項屬性](position-control-attribute.md)。

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>高度
</dt> <dd>

控制項矩形界限的高度。 此值必須是非負數。 請參閱 [Position 控制項屬性](position-control-attribute.md)。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

指定要套用至這個控制項之位旗標的32位字。 這必須是非負數，且允許的值取決於控制項的類型。 如需所有控制項屬性的清單，以及此欄位中要輸入的值，請參閱 [控制項屬性](control-attributes.md)。

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

要連結至此控制項之已定義屬性的名稱。 選項按鈕、清單方塊和下拉式方塊值會連結至相同的屬性，以系結至群組。 現用控制項需要此資料行。

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本
</dt> <dd>

可當地語系化的字串，用來設定控制項中包含的初始文字。 字串也可以包含內嵌屬性。 如需包含屬性之格式化字串的語法，請參閱 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) 函數。 藉由在文字字串前面加上 {style} 來指定文字的大小、字型和色彩 \\ ，其中 style 是在文字樣式 [表](textstyle-table.md)的文字樣式中撰寫的文字樣式。 如果文字字串太長而無法放入控制項，則會被截斷。 文字字串可能是空白的。

如果文字是顯示在具有 TrackDiskpace 屬性之對話方塊的[文字控制項](text-control.md)中，就必須在此欄位中特別撰寫[格式化](formatted.md)的文字字串。 這是在[對話方塊資料表](dialog-table.md)的屬性中顯示的[TrackDiskSpace 對話方塊樣式位](trackdiskspace-dialog-style-bit.md)所指定的情況。 在此情況下，如果控制資料表的文字資料行中的格式化字串開頭為 " \[ "，且結尾為 " \] "，則您必須在字串的結尾加上空格。 例如，如果 DlgTextFont 是將設定為 "{ \\ DlgFontBold}" 的屬性，則格式化的字串 " \[ DlgTextFont \] MyText \[ ProductName \] " 需要右括弧之後結尾的空格。 安裝程式需要這個額外的空間，才能正確地在文字控制項中顯示文字。

您可以針對 [VolumeCostList](volumecostlist-control.md)、 [ListView](listview-control.md)、 [DirectoryList](directorylist-control.md)和 [SelectionTree 控制項](selectiontree-control.md)輸入簡短的描述性文字字串。 使用者看不到此文字，但螢幕讀取器可以讀取此文字作為控制項的描述。

另請參閱 [協助工具](accessibility.md)。

</dd> <dt>

<span id="Control_Next"></span><span id="control_next"></span><span id="CONTROL_NEXT"></span>控制 \_ 下一步
</dt> <dd>

相同對話方塊上另一個控制項的名稱，以及控制資料表第二個數據行的外部索引鍵。 如果對話方塊中的焦點是在控制項資料行中的控制項上，則按下 tab 鍵會將焦點移至控制項下一個資料行中所列的控制項 \_ 。 因此，這個資料行是用來指定對話方塊上控制項的定位順序。 控制項之間的連結必須形成封閉的迴圈。 某些控制項（例如靜態文字控制項）可以離開迴圈。 在此情況下，此欄位可能會保留空白。

另請參閱 [協助工具](accessibility.md)。

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>説明
</dt> <dd>

選用的可當地語系化文字字串，與 [說明] 按鈕一起使用。 字串會依分隔符號 () 分割成兩個部分 \| 。 字串的第一個部分是用來做為工具提示文字。 螢幕讀取器會為包含圖片的控制項使用此文字。 字串的第二個部分保留供日後使用。 即使只有兩種類型的文字中有一種，也需要分隔符號。

</dd> </dl>

## <a name="remarks"></a>備註

X、y、寬度和高度的整數值是在 [安裝程式單位](installer-units.md)中，而不是對話方塊單位。 安裝程式單位等於10點 MS sans-serif 字型大小的一到第十二個高度。 控制項的座標相對於佈告欄。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE31](ice31.md)  
[ICE32](ice32.md)  
[ICE34](ice34.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE95](ice95.md)  
</dl>

 

 




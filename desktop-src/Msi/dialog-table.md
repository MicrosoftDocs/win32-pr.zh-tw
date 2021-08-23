---
description: 對話方塊資料表包含使用者介面中顯示的所有對話方塊， (UI) 全部和縮減模式。
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: 對話方塊資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554bc551b41a7ebeaa8b63b2a0d1b74a0f55cfb1d7a087936a394a060286caba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692838"
---
# <a name="dialog-table"></a>對話方塊資料表

對話方塊資料表包含使用者介面中顯示的所有對話方塊， (UI) 全部和縮減模式。

對話方塊資料表具有下列資料行。



| Column           | 類型                               | 答案 | Nullable |
|------------------|------------------------------------|-----|----------|
| 對話           | [識別碼](identifier.md)       | Y   | N        |
| HCentering       | [整數](integer.md)             | N   | N        |
| VCentering       | [整數](integer.md)             | N   | N        |
| 寬度            | [整數](integer.md)             | N   | N        |
| 高度           | [整數](integer.md)             | N   | N        |
| 屬性       | [DoubleInteger](doubleinteger.md) | N   | Y        |
| 標題            | [格式 化](formatted.md)         | N   | Y        |
| \_先控制項   | [識別碼](identifier.md)       | N   | N        |
| 控制項 \_ 預設值 | [識別碼](identifier.md)       | N   | Y        |
| 控制 \_ 取消  | [識別碼](identifier.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>對話 框
</dt> <dd>

對話方塊的主要索引鍵和名稱。

</dd> <dt>

<span id="HCentering"></span><span id="hcentering"></span><span id="HCENTERING"></span>HCentering
</dt> <dd>

對話方塊的水準位置。

範圍是0到100，螢幕左邊緣有0，右邊緣100。

</dd> <dt>

<span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>VCentering
</dt> <dd>

對話方塊的垂直位置。

範圍是0到100，在畫面的上邊緣為0，而在下邊緣是100。

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>寬度
</dt> <dd>

對話方塊矩形邊界的寬度。

此數位必須為非負數。

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>高度
</dt> <dd>

對話方塊矩形邊界的高度。

此數位必須為非負數。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

指定要套用至這個對話方塊之屬性旗標的32位字。

此數位必須為非負數。 如需詳細資訊，請參閱 [對話方塊樣式位](dialog-style-bits.md)。

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>標題
</dt> <dd>

可當地語系化的文字字串，指定要顯示在對話方塊標題列中的標題。

</dd> <dt>

<span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>\_先控制項
</dt> <dd>

[控制資料表](control-table.md)第二個數據行的外部索引鍵。

將此欄位與對話方塊欄位合併時，會指定在開啟對話方塊時取得焦點的 [控制資料表](control-table.md) 中的唯一控制項。 一般而言，這可以是 [編輯控制項](edit-control.md)、 [SelectionTree 控制項](selectiontree-control.md)，或可取得焦點的任何其他控制項。 如果 [按鈕控制項](pushbutton-control.md) 是可取得焦點之對話方塊中唯一的控制項，則在 [ControlDefault] 欄位中輸入的按鈕也必須輸入到 [控制項] 的第一個欄位中。 [錯誤對話方塊](error-dialog.md)中會忽略此資料行。

因為靜態文字無法取得焦點，所以描述[編輯控制項](edit-control.md)、 [PathEdit 控制項](pathedit-control.md)、 [ListView 控制項](listview-control.md)、 [ComboBox 控制項](combobox-control.md)或[VolumeSelectCombo 控制項](volumeselectcombo-control.md)的[文字控制項](text-control.md)必須成為對話方塊中的第一個控制項，以確保與螢幕讀取器的相容性。

</dd> <dt>

<span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>控制項 \_ 預設值
</dt> <dd>

[控制資料表](control-table.md)第二個數據行的外部索引鍵。

結合此欄位與對話方塊欄位，可指定在開啟對話方塊時取得焦點的預設控制項。 一般而言，這可以是 [按鈕控制項](pushbutton-control.md)。 如果對話方塊上沒有任何按鈕控制項具有焦點，則傳回索引鍵相當於按一下預設控制項。 如果此資料行保留空白，則沒有預設控制項。 [錯誤對話方塊](error-dialog.md)中會忽略此資料行。

</dd> <dt>

<span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>控制 \_ 取消
</dt> <dd>

[控制資料表](control-table.md)第二個數據行的外部索引鍵。

將此欄位與對話方塊欄位結合，可指定取消安裝的控制項。 此控制項會與用來取消安裝的 [ControlEvent 資料表](controlevent-table.md) 中的事件結合。 按下 ESC 鍵或按一下 [關閉] 按鈕，相當於按一下 [取消] 控制項。 [錯誤對話方塊](error-dialog.md)中會忽略此資料行

方塊。

在復原或移除備份檔案時，會隱藏取消控制項。 內部 UI 處理常式會在收到 INSTALLMESSAGE COMMONDATA 訊息時隱藏控制項 \_ 。

</dd> </dl>

## <a name="remarks"></a>備註

寬度和高度的整數值是在 [安裝程式單位](installer-units.md)中，而不是對話方塊單位。

在嚮導序列中的後續對話方塊中，會忽略兩個置中值。 對話方塊位置是由使用者設定，或與上一個對話方塊相同。 這些對話方塊順序是由 [NewDialog ControlEvent](newdialog-controlevent.md)所建立。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE27](ice27.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
</dl>

 

 




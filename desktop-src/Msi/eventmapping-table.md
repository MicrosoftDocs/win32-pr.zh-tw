---
description: EventMapping 資料表會列出訂閱某些控制項事件的控制項，並列出當其他控制項或 Windows Installer 發佈事件時要變更的屬性。
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: EventMapping 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f17380e3e91669926ef50532c36fec71f44d61eb2ed7273d053defe45fa874e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963108"
---
# <a name="eventmapping-table"></a>EventMapping 資料表

EventMapping 資料表會列出訂閱某些控制項事件的控制項，並列出當其他控制項或 Windows Installer 發佈事件時要變更的屬性。

EventMapping 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 對話\_  | [識別碼](identifier.md) | Y   | N        |
| 控制項\_ | [識別碼](identifier.md) | Y   | N        |
| 事件     | [識別碼](identifier.md) | Y   | N        |
| 屬性 | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>對話 框\_
</dt> <dd>

[對話方塊資料表](dialog-table.md)第一個資料行的外部索引鍵。 這個欄位和控制項 \_ 欄位會一起識別控制項。

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>控制\_
</dt> <dd>

[控制資料表](control-table.md)第二個數據行的外部索引鍵。 這個欄位和對話 \_ 欄位會一起識別控制項。

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件
</dt> <dd>

此欄位是指定控制項所訂閱之事件種類的識別碼。 如需詳細資訊，請參閱 [ControlEvent 總覽](controlevent-overview.md)。

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>屬性
</dt> <dd>

\_當收到事件資料行中的事件時，所設定的控制項屬性名稱。 事件的引數會以屬性呼叫的引數形式傳遞，以變更控制項的這個屬性。

</dd> </dl>

## <a name="remarks"></a>備註

[ControlEvent 資料表](controlevent-table.md)會指定使用者與[按鈕控制項](pushbutton-control.md)、 [CheckBox 控制項](checkbox-control.md)或[SelectionTree 控制項](selectiontree-control.md)互動時，所啟動的控制項事件。 這些是使用者唯一可用來起始控制項事件的控制項。

對話方塊上有一個以上的控制項可以訂閱相同的事件。

下列清單會識別 EventMapping 資料表的一般用途：

-   若要將[文字控制項](text-control.md)訂閱至[ActionText ControlEvent](actiontext-controlevent.md)、 [ActionData ControlEvent](actiondata-controlevent.md)、 [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md)或 Windows Installer 所發佈的[TimeRemaining ControlEvent。](timeremaining-controlevent.md)
-   將 [ProgressBar 控制項](progressbar-control.md) 或 [佈告欄控制項](billboard-control.md) 訂閱至 [SetProgress ControlEvent](setprogress-controlevent.md)。
-   將 [DirectoryCombo 控制項](directorycombo-control.md) 訂閱至 [IgnoreChange ControlEvent](ignorechange-controlevent.md)。
-   使用[SelectionTree 控制項](selectiontree-control.md)自動停用位於相同對話方塊上的[按鈕控制項](pushbutton-control.md)。 若要在 [SelectionTree 控制項](selectiontree-control.md)中未列出任何功能時停用推播按鈕，請使用 EventMapping 資料表來訂閱 [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md)的按鈕控制項。 在 EventMapping 資料表的 [屬性] 欄位中輸入 **Enable** 。
-   顯示 [文字控制項](text-control.md) ，顯示在相同對話方塊上， [SelectionTree 控制項](selectiontree-control.md) 中所選取之功能的安裝位置路徑。 您可以使用 EventMapping 資料表，將[文字控制項](text-control.md)訂閱至[ControlEvent 控制項](selectiontree-control.md)所發佈的[SelectionPathOn ControlEvent](selectionpathon-controlevent.md)和[SelectionPath SelectionTree](selectionpath-controlevent.md) 。
-   若要顯示 [文字控制項](text-control.md) ，以顯示在相同對話方塊上 [SelectionTree 控制項](selectiontree-control.md) 中醒目提示的專案描述，請使用 EventMapping 資料表將 [文字控制項](text-control.md) 訂閱至 [SelectionDescription ControlEvent](selectiondescription-controlevent.md)、 [SelectionSize ControlEvent](selectionsize-controlevent.md) 或 [SelectionAction ControlEvent](selectionaction-controlevent.md)。 在 [EventMapping] 資料表的 [屬性] 欄位中輸入 **文字** 。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 




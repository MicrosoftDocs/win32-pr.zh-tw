---
description: ControlEvent 資料表可讓作者指定當使用者與按鈕控制項、CheckBox 控制項或 SelectionTree 控制項互動時，所啟動的控制項事件。
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: ControlEvent 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fec4837fa7d98289495bbb0773ae7260f957485cd87214dabf1999b1e1a876c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692998"
---
# <a name="controlevent-table"></a>ControlEvent 資料表

ControlEvent 資料表可讓作者指定當使用者與[按鈕控制項](pushbutton-control.md)、 [CheckBox 控制項](checkbox-control.md)或[SelectionTree 控制項](selectiontree-control.md)互動時，所啟動的[控制項事件](control-events.md)。 這些是使用者唯一可用來起始控制項事件的控制項。 每個控制項都可以發行多個控制項事件。 安裝程式會依 [排序] 資料行中指定的順序啟動每個事件。 例如，按鈕控制項可以發行事件，以起始轉換至另一個對話方塊、結束對話方塊序列，以及開始安裝檔案。

要注意的例外狀況是每個控制項都可以發行最多一個 [NewDialog](newdialog-controlevent.md) 或一個 [SpawnDialog](spawndialog-controlevent.md) 事件。 如果您需要在此資料表中撰寫多個 NewDialog 和 SpawnDialog 控制項事件，也請在 [條件] 欄位中包含條件陳述式，以確保最多可發佈一個事件。 如果針對相同的控制項選取了多個 NewDialog 和 SpawnDialog 控制項事件，則在啟用控制項時，只會發佈 [排序] 資料行中具有最大值的事件。

ControlEvent 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 對話\_  | [識別碼](identifier.md) | Y   | N        |
| 控制項\_ | [識別碼](identifier.md) | Y   | N        |
| 事件     | [格式 化](formatted.md)   | Y   | N        |
| 引數  | [格式 化](formatted.md)   | Y   | N        |
| 條件 | [Condition](condition.md)   | Y   | Y        |
| 排序  | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>對話 框\_
</dt> <dd>

[對話方塊資料表](dialog-table.md)第一個資料行的外部索引鍵。 結合此欄位與控制項欄位，即可 \_ 識別唯一的控制項。

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>控制\_
</dt> <dd>

[控制資料表](control-table.md)第二個數據行的外部索引鍵。 將此欄位與對話方塊欄位合併會 \_ 識別唯一的控制項。

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件
</dt> <dd>

識別碼，指定當使用者與對話方塊和控制項所指定的控制項互動時應該發生的事件種類 \_ \_ 。 如需可能值的清單，請參閱 [ControlEvent 總覽](controlevent-overview.md)。

若要設定具有控制項的屬性，請將 \[ 屬性 \_ 名稱放 \] 在此欄位中，並在 [引數] 欄位中輸入新值。 將 {} 放入引數欄位以輸入 null 值。

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>參數
</dt> <dd>

當觸發特定事件時，用來做為修飾詞的值。

例如， [NewDialog ControlEvent](newdialog-controlevent.md) 或 [SpawnDialog ControlEvent](spawndialog-controlevent.md) 的引數是對話方塊的名稱，而 [安裝動作](install-action.md) 的引數則是定義安裝層級的數位。

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

條件陳述式，可判斷安裝程式是否在事件資料行中啟用事件。 如果條件欄位中的條件陳述式評估為 True，則安裝程式會觸發事件。 因此，請在此資料行中放入1，以確保安裝程式會觸發事件。 如果條件欄位包含評估為 False 的語句，安裝程式就不會觸發事件。 除非控制項的其他事件未評估為 True，否則安裝程式不會在條件欄位中觸發具有空白的事件。 如果在控制項欄位中指定之控制項的條件欄位都未 \_ 評估為 True，則安裝程式會觸發一個具有空白條件欄位的事件，如果有一個以上的條件欄位為空白，則會使用 [排序] 欄位中的最大值來觸發其中一個事件。 請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>訂購
</dt> <dd>

用來排序多個與相同控制項系結之事件的整數。 此值必須是非負數。 這個欄位可以保留空白。

</dd> </dl>

## <a name="remarks"></a>備註

[EventMapping 資料表](eventmapping-table.md)會列出訂閱某些控制項事件的控制項，並列出當另一個控制項或安裝程式發行該事件時，要變更的控制項屬性。

在 Windows XP 或更早版本的作業系統上，使用者只能透過與[Checkbox 控制項](checkbox-control.md)或[按鈕控制項](pushbutton-control.md)互動來發佈控制項事件。 使用 Windows Server 2003 時，使用者只能透過與[Checkbox 控制項](checkbox-control.md)、 [SelectionTree 控制項](selectiontree-control.md)和[按鈕控制項](pushbutton-control.md)互動，來發佈控制項事件。 列出控制項欄位中的其他控制項 \_ 不會有任何作用。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 




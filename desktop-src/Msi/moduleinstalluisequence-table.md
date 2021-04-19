---
description: 合併工具會評估 ModuleInstallUISequence 資料表，然後將計算的動作以正確的序號插入 InstallUISequence 資料表中。
ms.assetid: a125aecc-57d9-4c8e-873e-d5315eaafa56
title: ModuleInstallUISequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca6771daa0b95acbc23e2d60eddda5420e417db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971849"
---
# <a name="moduleinstalluisequence-table"></a>ModuleInstallUISequence 資料表

合併工具會評估 ModuleInstallUISequence 資料表，然後將計算的動作以正確的序號插入 [InstallUISequence 資料表](installuisequence-table.md) 中。

ModuleInstallUISequence 資料表具有下列資料行。



| Column     | 類型                         | 答案 | Nullable |
|------------|------------------------------|-----|----------|
| 動作     | [識別碼](identifier.md) | Y   | N        |
| 順序   | [整數](integer.md)       |     | Y        |
| BaseAction | [識別碼](identifier.md) |     | Y        |
| After      | [整數](integer.md)       |     | Y        |
| 條件  | [Condition](condition.md)   |     | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

要插入順序的動作。 指的是其中一個安裝程式 [標準動作](standard-actions.md)，或合併模組的 [CustomAction 資料表](customaction-table.md) 或 [對話方塊資料表](dialog-table.md)中的專案。

如果在 merge module sequence 資料表的動作資料行中使用 [標準動作](standard-actions.md) ，則該記錄的 BaseAction 和 After 資料行必須是 Null。

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列
</dt> <dd>

標準動作的序號。 如果在此資料列的 [動作] 資料行中輸入自訂動作或對話，此欄位必須設定為 Null。

在合併模組順序資料表中使用 [標準動作](standard-actions.md) 時，[順序] 資料行中的值應該是建議的動作序號。 如果合併模組中的序號與 .msi 檔案順序資料表中相同動作的序號不同，則合併工具會使用 .msi 檔案中的序號。 如需標準動作的建議序號，請參閱 [使用順序表](using-a-sequence-table.md) 中的建議序列。

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

BaseAction 資料行可包含標準動作、在合併模組的自訂動作資料表中指定的自訂動作，或在模組的對話方塊資料表中指定的對話方塊。 BaseAction 資料行是此資料表之 [動作] 資料行中的索引鍵。 它不能是 .msi 檔案中其他合併資料表或資料表的外鍵。 這表示 BaseAction 資料行中所列的每個標準動作、自訂動作或對話方塊，也必須列在此資料表中另一筆記錄的 [動作] 資料行中。

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>後
</dt> <dd>

在 BaseAction 之前或之後的動作是否為布林值。



| 值 | 意義                          |
|-------|----------------------------------|
| 0     | BaseAction 前的動作 |
| 1     | BaseAction 之後的動作  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

指出是否要執行動作的條件陳述式。 Null 評估為 true。

</dd> </dl>

## <a name="remarks"></a>備註

如果這個資料表存在，則 [InstallUISequence 資料表](installuisequence-table.md) 也必須存在於合併模組中。

 

 




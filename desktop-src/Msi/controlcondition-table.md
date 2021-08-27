---
description: ControlCondition 資料表可讓作者根據條件陳述式的結果，指定要套用至控制項的特殊動作。 例如，使用此資料表時，作者可以選擇根據 VersionNT 屬性隱藏控制項。
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: ControlCondition 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d9470af21ad1f8a15c2697ba34a6c9866c822c21c6f3a85241bac1309f76b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105248"
---
# <a name="controlcondition-table"></a>ControlCondition 資料表

ControlCondition 資料表可讓作者根據條件陳述式的結果，指定要套用至控制項的特殊動作。 例如，使用此資料表時，作者可以選擇根據 [**VersionNT**](versionnt.md) 屬性隱藏控制項。

ControlCondition 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 對話\_  | [識別碼](identifier.md) | Y   | N        |
| 控制項\_ | [識別碼](identifier.md) | Y   | N        |
| 動作    | [Text](text.md)             | Y   | N        |
| 條件 | [Condition](condition.md)   | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>對話 框\_
</dt> <dd>

[對話方塊資料表](dialog-table.md)第一個資料行的外部索引鍵。 結合此欄位與控制項欄位，即可 \_ 識別唯一的控制項。

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>控制\_
</dt> <dd>

[控制資料表](control-table.md)第二個數據行的外部索引鍵。 結合此欄位時，對話方塊 \_ 欄位會識別唯一的控制項。

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

要在控制項上採取的動作。 下表顯示可能的動作。



| 值   | 意義                     |
|---------|-----------------------------|
| 預設 | 將控制項設定為預設值。 |
| 停用 | 停用控制項。        |
| 啟用  | 啟用控制項。         |
| 隱藏    | 隱藏控制項。           |
| 顯示    | 顯示控制項。        |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

條件陳述式，指定應觸發動作的條件。 此資料行可能不會保留空白。 如果此語句未評估為 TRUE，就不會執行此動作。 如果設定為1，則一律會套用動作。 如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

</dd> </dl>

## <a name="remarks"></a>備註

如果您想要根據 [ControlCondition] 資料表的 [條件] 欄位中的條件陳述式隱藏和停用 [按鈕](pushbutton-control.md) 控制項或 [核取方塊控制項](checkbox-control.md) ，您應該針對每個控制項使用四筆記錄來停用和隱藏控制項。 快速鍵仍可存取只有隱藏的按鈕或核取方塊控制項。

例如，下列記錄會在安裝產品時，隱藏和停用 DialogA 上的 ControlA。 未安裝產品時，會顯示並啟用此控制項。



| 對話  | 控制  | 動作  | 條件                      |
|---------|----------|---------|--------------------------------|
| DialogA | ControlA | 隱藏    | [**安裝**](installed.md) |
| DialogA | ControlA | 停用 | 已安裝                      |
| DialogA | ControlA | 顯示    | 未安裝                  |
| DialogA | ControlA | 啟用  | 未安裝                  |



 

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 




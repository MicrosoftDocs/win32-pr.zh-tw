---
description: 條件資料表可以用來根據條件運算式修改特徵資料表中任何專案的選取狀態。
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: 條件資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d9ccb265d69f99a58e155657a0e9d058ba61a920088184ec2b67c3e4506a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926958"
---
# <a name="condition-table"></a>條件資料表

條件資料表可以用來根據條件運算式修改 [特徵資料表](feature-table.md) 中任何專案的選取狀態。

條件資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 特徵\_ | [識別碼](identifier.md) | Y   | N        |
| 層級     | [整數](integer.md)       | Y   | N        |
| 條件 | [Condition](condition.md)   | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_
</dt> <dd>

在功能資料表的第一個資料行中的外部索引鍵。

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>水準
</dt> <dd>

此資料表的功能資料行中功能的條件式安裝層級 \_ 。 如果 [條件] 資料行中的運算式評估為 TRUE，則安裝程式會將這項功能的安裝層級設定為此資料行中指定的層級。

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

如果此條件運算式評估為 TRUE，則會將功能資料表中的層級資料行設定為條件式安裝層級。

[條件] 資料行中的運算式不應該包含任何功能或元件之已安裝狀態的參考。 這是因為 [條件] 資料行中的運算式會在安裝程式評估功能和元件的已安裝狀態之前評估。 在條件資料表中嘗試檢查功能或元件之已安裝狀態的任何運算式一律會評估為 false。

如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

</dd> </dl>

## <a name="remarks"></a>備註

將 [層級] 資料行設定為0可永久停用功能。

層級可以根據任何條件陳述式來設定，例如平臺、作業系統或特定屬性設定的測試。

應謹慎選擇條件，以便在安裝時不啟用功能，然後在卸載時停用。 這將會孤立功能，而產品將無法卸載。

當 [CostFinalize 動作](costfinalize-action.md) 執行時，就會參考此資料表。

如果 [**預先**](preselected.md) 選取的屬性已設定為1，安裝程式就不會評估條件資料表。 只有在未設定下列任何屬性時，條件資料表才會影響功能的安裝：

<dl>

[**ADDLOCAL**](addlocal.md)  
[**刪除**](remove.md)  
[**ADDSOURCE**](addsource.md)  
[**ADDDEFAULT**](adddefault.md)  
[**REINSTALL**](reinstall.md)  
[**做廣告**](advertise.md)  
[**COMPADDLOCAL**](compaddlocal.md)  
[**COMPADDSOURCE**](compaddsource.md)  
[**COMPADDDEFAULT**](compadddefault.md)  
[**FILEADDLOCAL**](fileaddlocal.md)  
[**FILEADDSOURCE**](fileaddsource.md)  
[**FILEADDDEFAULT**](fileadddefault.md)  
</dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 




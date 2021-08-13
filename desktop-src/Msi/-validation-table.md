---
description: '\_驗證資料表是包含資料庫中所有資料表之資料行名稱和資料行值的系統資料表。'
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a42fbe2a2f8da4abceb04912eee2a12edd708ff88d979fbf45f7de8051dc80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640443"
---
# <a name="_validation-table"></a>\_驗證資料表

\_驗證資料表是包含資料庫中所有資料表之資料行名稱和資料行值的系統資料表。 在資料庫驗證過程中，會使用它來確保所有資料行都已列入考慮，而且具有正確的值。 此資料表並未隨附于安裝程式資料庫。

\_驗證資料表具有下列資料行。



| Column      | 類型                               | 答案 | Nullable |
|-------------|------------------------------------|-----|----------|
| 資料表       | [識別碼](identifier.md)       | Y   | N        |
| Column      | [識別碼](identifier.md)       | Y   | N        |
| Nullable    | [Text](text.md)                   | N   | N        |
| MinValue    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxValue    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| KeyTable    | [識別碼](identifier.md)       | N   | Y        |
| KeyColumn   | [整數](integer.md)             | N   | Y        |
| 類別    | [Text](text.md)                   | N   | Y        |
| 集合         | [Text](text.md)                   | N   | Y        |
| 描述 | [Text](text.md)                   | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>表
</dt> <dd>

用來識別特定的資料表。 此索引鍵和資料行索引鍵會形成驗證資料表的主要索引鍵 \_ 。

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>列
</dt> <dd>

用來識別資料表的特定資料行。 此索引鍵和資料表索引鍵會形成驗證資料表的主要索引鍵 \_ 。

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>空
</dt> <dd>

識別資料行是否可包含 Null 值。

此資料行可能會有下列其中一個值。



| String | 意義                                   |
|--------|-------------------------------------------|
| Y      | 是，資料行可能會有 Null 值。    |
| N      | 否，資料行的值不能是 Null。 |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue
</dt> <dd>

此欄位適用于具有數值的資料行。 欄位包含允許的最小值。 這可以是整數的最小值或日期或版本字串的最小值。

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>Timespan.maxvalue
</dt> <dd>

此欄位適用于具有數值的資料行。 欄位是允許的最大值。 這可能是整數的最大值或日期或版本字串的最大值。

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable
</dt> <dd>

此欄位會套用至屬於外部索引鍵的資料行。 在資料行中識別的欄位必須連結至在 KeyTable 中名為的資料表中，KeyColumn 所指定的資料行編號。 這可以是以分號分隔的資料表清單。

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn
</dt> <dd>

此欄位適用于外部索引鍵的資料表資料行。 在資料行中識別的欄位必須連結至在 KeyTable 中名為的資料表中，KeyColumn 所指定的資料行編號。 KeyColumn 欄位允許的範圍是1-32。

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別
</dt> <dd>

這是由驗證資料表之資料表和資料行資料行所指定的資料庫欄位所包含的資料類型 \_ 。 如果這是具有數值的類型（例如 [整數](integer.md)、 [DoubleInteger](doubleinteger.md) 或 [時間/日期](time-date.md)），請在此欄位中輸入 null，然後使用 MinValue 和 int32.maxvalue 資料行來指定值的範圍。 您可以使用 [類別] 資料行來指定資料 [行資料類型](column-data-types.md)中所描述的非數值資料類型。

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>設置
</dt> <dd>

這是此欄位允許的值清單（以分號分隔）。 此欄位通常用於列舉。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

儲存在資料行中之資料的描述。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

## <a name="remarks"></a>備註

此資料表的 [類別目錄] 欄位僅適用于字串資料。 如果資料列欄位參考了具有二進位資料的資料行，則必須在 [類別目錄] 欄位中指定二進位資料類型。 整數資料行類型在驗證期間會忽略類別目錄欄位。

 

 




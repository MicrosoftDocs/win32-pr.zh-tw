---
description: 這是唯讀的臨時表，用來以轉換視圖模式來查看轉換。 安裝程式永遠不會保存此資料表。
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: _TransformView 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513249"
---
# <a name="_transformview-table"></a>\_TransformView 資料表

這是唯讀的臨時表，用來以轉換視圖模式來查看轉換。 安裝程式永遠不會保存此資料表。

若要叫用轉換視圖模式，請取得控制碼，並開啟參考資料庫。 請參閱 [取得資料庫控制碼](obtaining-a-database-handle.md)。 使用 MSITRANSFORM 錯誤 VIEWTRANSFORM 來呼叫 [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) \_ \_ 。 這會停止將轉換套用至資料庫，並將轉換內容傾印至 \_ TransformView 資料表。 您可以使用 SQL 查詢來存取資料表中的資料。 請參閱 [使用查詢](working-with-queries.md)。

套用 \_ 其他轉換時，不會清除 TransformView 資料表。 資料表會反映後續應用程式的累積效果。 若要個別查看轉換，您必須釋放資料表。

\_TransformView 資料表具有下列資料行。



| Column  | 類型                         | 答案 | Nullable |
|---------|------------------------------|-----|----------|
| 資料表   | [識別碼](identifier.md) | Y   | N        |
| Column  | [Text](text.md)             | Y   | N        |
| 資料列     | [Text](text.md)             | Y   | Y        |
| 資料    | [Text](text.md)             | N   | Y        |
| 目前 | [Text](text.md)             | N   | Y        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>表
</dt> <dd>

改變的資料庫資料表名稱。

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>列
</dt> <dd>

改變的資料表資料行名稱，或插入、刪除、建立或卸載。

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>行
</dt> <dd>

以定位字元分隔的主鍵值清單。 Null 主鍵值是以單一空白字元表示。 此資料行中的 Null 值表示架構變更。

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>資料
</dt> <dd>

資料、資料流程的名稱或資料行定義。

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>當前
</dt> <dd>

參考資料庫的目前值，或資料行 a 數位。

</dd> </dl>

## <a name="remarks"></a>備註

\_TransformView 會透過鎖定計數保留在記憶體中，可使用下列 SQL 命令來釋放。

「ALTER TABLE \_ TRANSFORMVIEW FREE」。

您可以使用 SQL 查詢來存取資料表中的資料。 SQL 語言有兩個主要部分：「資料定義語言」 (DDL) 用來定義 SQL 資料庫中的所有物件，以及用來選取、插入、更新和刪除使用 DDL 定義之物件中資料的資料操作語言 (DML) 。

資料操作語言 (DML) 轉換作業，如下所示。 資料操作語言 (DML) 是 SQL 中可操作的語句，而不是定義資料。



| 轉換作業 | SQL 結果                                    |
|---------------------|-----------------------------------------------|
| 修改資料         | 表列排data{目前的值} |
| 插入資料列          | 表"INSERT" {row} Null null              |
| 刪除資料列          | 表"DELETE" {row} Null Null              |



 

資料定義語言 (DDL) 轉換作業如下所示。 資料定義語言 (DDL) 是 SQL 中定義，而不是運算元據的語句。



| 轉換作業 | SQL 結果                                   |
|---------------------|----------------------------------------------|
| 新增資料行          | 表列Null {定義} {資料行編號} |
| 加入資料表           | 表"CREATE" Null Null Null              |
| 卸除資料表          | 表"DROP" Null Null Null                |



 

當轉換的應用程式加入此資料表時，資料欄位會接收可解釋為16位整數值的文字。 此值描述資料列欄位中所命名的資料行。 您可以比較整數值與下表中的常數，以判斷改變的資料行的定義。



| bit                                                                                                       | Description                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7<br/>         | 十六進位： 0x0000 0x0100<br/> Decimal： 0 255<br/> 資料行寬度<br/>                                                                                                                                                                                                                                  |
| <span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>位8<br/>                  | 十六進位：0x0100<br/> Decimal：256<br/> 持續性資料行。 零表示暫時的資料行。 <br/>                                                                                                                                                                                                   |
| <span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>位9<br/>                  | 十六進位：0x0200<br/> Decimal：1023<br/> 可當地語系化的資料行。 零表示資料行不可當地語系化。<br/>                                                                                                                                                                                      |
| <span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11<br/> | 十六進位：0x0000<br/> Decimal：0<br/> 長整數<br/> 十六進位：0x0400<br/> Decimal：1024<br/> Short 整數<br/> 十六進位：0x0800<br/> Decimal：2048<br/> Binary 物件<br/> 十六進位：0x0C00<br/> Decimal：3072<br/> String<br/> |
| <span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12<br/>              | 十六進位：0x1000<br/> Decimal：4096<br/> 可為 null 的資料行。 零表示資料行不可為 null。<br/>                                                                                                                                                                                               |
| <span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13<br/>              | 十六進位：0x2000<br/> Decimal：8192<br/> 主要索引鍵資料行。 零表示這個資料行不是主要索引鍵。<br/>                                                                                                                                                                                      |
| <span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15<br/> | 十六進位： 0x4000 0x8000<br/> Decimal： 16384 32768<br/> 保留<br/>                                                                                                                                                                                                                                |



 

如需示範 TransformView 資料表的腳本範例 \_ ，請參閱「 [查看轉換](view-a-transform.md)」。

 

 





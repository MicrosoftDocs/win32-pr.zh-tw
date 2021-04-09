---
description: Windows Installer 的 SQL 查詢字串會限制為下列格式。
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: SQL 語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1b7d1179a8b6035186a9a5e78f46fdc857ac18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848840"
---
# <a name="sql-syntax"></a>SQL 語法

Windows Installer 的 SQL 查詢字串會限制為下列格式。



| 動作                             | 查詢                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 選取一組記錄          | 從 {作業清單} 的 {list} \[ \] \[ \] \[ ORDER BY {column-list} 選取不同的 {column-list}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| 從資料表中刪除記錄        | 從 {table} 刪除 \[ {operation-list}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 修改資料表中的現有記錄 | 更新 {資料表清單} SET {column} = {常數} \[ ，{column} = {常數} \] \[ ，... \] \[其中 {operation list} \] 更新查詢只適用于非主鍵資料行。<br/>                                                                                                                                                                                                                                                                                                                                      |
| 將記錄新增至資料表             | INSERT INTO {table} ( {column-list} ) 值 ( {常數清單} ) \[ 暫時 \] 二進位資料無法使用 INSERT INTO 或 UPDATE SQL 查詢直接插入資料表中。 如需詳細資訊，請參閱 [使用 SQL 將二進位資料加入至資料表](adding-binary-data-to-a-table-using-sql.md)。<br/>                                                                                                                                                                                                       |
| 新增資料表                        | \[ \] 加入資料表時，必須為每個資料行指定 CREATE TABLE {TABLE} ( {column} {column type} ) 保留資料行類型。 至少必須指定一個主鍵資料行，才能建立新的資料表。 上述 {column type} 的可能替代為： CHAR \[ ( {size} ) \] \| 字元 \[ ( {size} ) \] \| LONGCHAR \| SHORT \| INT \| 整數 \| LONG \| 物件 \[ NOT Null \] \[ 暫時性可 \] \[ 當地語系化的資料 \] \[ 行 ... \] \[ \]主要索引鍵資料行 \[ ，資料行 ... \] \[ \] 。<br/> |
| 移除資料表                     | DROP TABLE {table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 新增資料行                       | ALTER TABLE {TABLE} ADD {column} {column type} 當加入資料行時，必須指定資料行類型。 上述 {column type} 的可能替代為： CHAR \[ ( {size} ) \] \| 字元 \[ ( {size} ) \] \| LONGCHAR \| SHORT \| INT \| 整數 \| LONG \| 物件 \[ NOT Null \] \[ 暫時可 \] \[ 當地語系化 \] \[ \] 的保存。<br/>                                                                                                                                                                  |
| 保存和釋放臨時表     | ALTER TABLE {table name} HOLDALTER TABLE {table name} FREE<br/> 使用者可以使用保留和免費的命令來控制臨時表或暫存資料行的存留期範圍。 資料表上的保留計數會針對該資料表上的每個 SQL 保存作業遞增，並針對資料表上的每個 SQL FREE 作業進行遞減。 當資料表上的最後一個保存計數釋出時，所有暫存資料行都會變成無法存取。 如果所有資料行都是暫時性的，資料表就會變成無法存取。<br/>     |



 

如需詳細資訊，請參閱 [使用 SQL 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md)。

### <a name="sql-grammar"></a>SQL 文法

選擇性參數會以括弧括住 \[ \] 。 當列出數個選項時，選擇性參數會以分隔號分隔。

{常數} 可以是字串或整數。 字串必須括在單引號 ' example ' 中。 {常數清單} 是一或多個常數的逗號分隔清單。

可當地語系化的選項會設定資料行屬性，指出資料行需要當地語系化。

{Column} 是資料表欄位中值的單欄式參考。

{標記} 是查詢所提交之記錄所提供值的參數參考。 它是在 SQL 語句中，以問號表示。 如需有關使用參數的詳細資訊，請參閱 [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) 函數或 [**Execute**](view-execute.md) 方法。

Windows Installer SQL 語法不支援在字串常值中，將單引號 (ASCII 值 39) 的轉義。 不過，您可以提取或建立記錄、使用 [**至 convertfrom-stringdata**](record-stringdata.md) 或 [**IntegerData**](record-integerdata.md) 屬性設定欄位，然後呼叫 [**Modify**](view-modify.md) 方法。 或者，您可以建立記錄，並使用 [**Execute**](view-execute.md) 方法中所述 (？ ) 的參數標記。 您也可以使用資料庫函式 [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)、 [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)和 [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)來進行此作業。

其中 {operation-list} 子句是選擇性的，而是用來篩選選取專案的作業群組。 作業必須屬於下列類型：

-   {column} = {column}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {常數}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {標記}
-   {column} 為 null
-   {column} 不是 null

針對字串值，只能有 = 或 <> 運算。 物件值的比較限制為 Null，而且不是 Null。

個別作業可以依 AND 或 OR 運算子來分組。 您可以使用括弧 ( ) 來加諸順序。

ORDER BY 子句是選擇性的，會在排序期間造成初始延遲。 依字串排序會將相同的字串群組在一起，但不會將字串以字母順序排列。

DISTINCT 子句是選擇性子句，不會在傳回的結果集中重複相同的記錄。

{資料表清單} 是聯結中的一或多個資料表名稱的逗號分隔清單，稱為 {table}。

{Column list} 是一或多個資料表資料行的逗號分隔清單，其中已選取 [{column}]。 明確的資料行可能會進一步限定為 {tablename. column}。 星號可用來當做 SELECT 查詢中的資料行清單，以表示參考資料表中的所有資料行。 依資料行位置參考欄位時，請依名稱選取資料行，而不是使用星號。 在 INSERT INTO 查詢中不能使用星號做為資料行清單。

若要將與 SQL 關鍵字衝突的資料表名稱和資料行名稱進行 escape，請將名稱括在兩個音符號 \` \` (ASCII 值 96) 。 如果資料行名稱必須經過轉義且限定為 {tablename. column}，則資料表和資料行必須個別地以 {tablename 的形式來將其轉義 \` \` 。 \`資料行 \` }。 建議您以這種方式來將所有資料表名稱和資料行名稱都換行，以避免與保留字的衝突並獲得顯著的效能。

資料表名稱限制為31個字元。 如需詳細資訊，請參閱 [資料表名稱](table-names.md)。 資料表和資料行名稱會區分大小寫。 SQL 關鍵字不區分大小寫。

SQL 查詢之 WHERE 子句中的運算式數目上限限制為32。

只支援內部聯結，而且是透過比較不同資料表的資料行來指定。 不支援迴圈聯結。 圓形聯結是一種 SQL 查詢，可將三個或多個資料表一起連結到電路中。 例如，以下是迴圈聯結：

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

屬於資料表之主鍵 (s) 的資料行，必須以優先權順序定義，後面接著任何非主鍵資料行。 您必須在暫存資料行之前定義持續性資料行。 文字資料行的排序次序未定義;不過，相同的文字值一律會群組在一起。

請注意，加入或建立資料行時，您必須指定資料行類型。

資料表不能包含多個類型為 ' object ' 的資料行。

可以針對 SQL 查詢中的字串資料行明確指定的大小上限為255。 無限長度的字串資料行表示大小為0。 如需詳細資訊，請參閱資料 [行定義格式](column-definition-format.md)。

若要執行任何 SQL 語句，您必須建立一個 view。 但是，不會建立結果集的視圖（例如 CREATE TABLE 或 INSERT INTO）無法與 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 或 [**Modify**](view-modify.md) 方法搭配使用，以透過視圖來更新資料表。

請注意，您無法從某個資料庫提取包含二進位資料的記錄，然後使用該記錄將資料插入至完全不同的資料庫。 若要將二進位資料從某個資料庫移到另一個資料庫，您應該將資料匯出至檔案，然後透過查詢和 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) 函數將資料匯入至新的資料庫。 這可確保每個資料庫都有自己的二進位資料複本。

 

 





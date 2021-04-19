---
title: SQL 方言
description: 從結構化查詢語言 (SQL) 衍生的 SQL 方言會使用人類可讀取的運算式來定義查詢語句。
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- SQL 方言 ADSI
- 方言 ADSI，SQL 方言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969020"
---
# <a name="sql-dialect"></a>SQL 方言

從結構化查詢語言 (SQL) 衍生的 SQL 方言會使用人類可讀取的運算式來定義查詢語句。 使用 SQL 查詢語句搭配下列 ADSI 搜尋介面：

-   [ActiveX Data 物件 (ADO) ](searching-with-activex-data-objects-ado.md)介面，這是使用 OLE DB 的自動化介面。
-   [OLE DB](searching-with-ole-db.md)，這是一組用來查詢資料庫的 c/c + + 介面。

SQL 語句需要下列語法。


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



下表列出 SQL 查詢語句關鍵字。



| 關鍵字  | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | 指定要針對每個物件取出的屬性清單（以逗號分隔）。 如果您指定 \* ，查詢只會抓取每個物件的 ADsPath。                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | 指定搜尋基底的 ADsPath。 例如，Active Directory 網域中的 [使用者] 容器的 ADsPath 可能是 [LDAP：//CN = Users，DC = Fabrikam，DC = COM]。 請注意，路徑是以一對單引號括住 ( ' ) 。                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | 指定查詢篩選的選擇性關鍵字。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 排序依據 | 選擇性的關鍵字，如果伺服器支援 LDAP 排序控制項，則會產生伺服器端排序。 Active Directory 支援排序控制項，但可能會影響伺服器效能，特別是當結果集很大時。 排序清單是用來排序的屬性清單（以逗號分隔）。 請注意，Active Directory 只支援單一排序索引鍵。 您可以使用選擇性的 ASC 和 DESC 關鍵字來指定遞增或遞減排序次序。預設值為遞增。 ORDER BY 關鍵字會覆寫任何以 ADO 命令物件的「排序依據」屬性指定的排序索引鍵。 |



 

> [!Note]  
> 在使用多位元組字元集的情況下，如果使用 SQL 方言以 ADO 執行搜尋，則不能使用反斜線來將字元換用。 相反地，必須使用以 [特殊字元](search-filter-syntax.md) 列出的 escape 序列。 例如，針對使用語法 "samAccountName = Test" 的語句（ \( 使用反斜線 " \\ "）來 escape 左括弧 " ("，改為使用特殊字元 "28" 來取代反斜線，如下所示 \\ ： "samaccountname = \\ 28Test"。

 

下列查詢語句是 ADSI 中的 SQL 方言範例。

以搜尋所有群組物件。


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



搜尋姓氏以字母 H 開頭的所有使用者。


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



下列程式碼範例定義了 SQL 查詢的正式文法。 所有關鍵詞都不區分大小寫。


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



Active Directory 的 OLE DB 提供者不支援 SQL 內部聯結，但您可以使用 SQL 來聯結 SQL 和 Active Directory 資料。 如需詳細資訊，請參閱 [建立 SQL Server 與 Active Directory 之間的異類聯結](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[搜尋篩選語法](search-filter-syntax.md)
</dt> <dt>

[LDAP 方言](ldap-dialect.md)
</dt> <dt>

[使用 >idirectorysearch 介面搜尋](searching-with-idirectorysearch.md)
</dt> <dt>

[使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[使用 OLE DB 搜尋](searching-with-ole-db.md)
</dt> </dl>

 

 





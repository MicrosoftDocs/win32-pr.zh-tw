---
title: 搜尋篩選語法
description: 搜尋篩選器可讓您定義搜尋條件，並提供更有效率且更有效率的搜尋。
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- 搜尋篩選語法 ADSI
- 查詢，搜尋篩選語法
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106994919"
---
# <a name="search-filter-syntax"></a>搜尋篩選語法

搜尋篩選器可讓您定義搜尋條件，並提供更有效率且更有效率的搜尋。

ADSI 支援 RFC2254 中定義的 LDAP 搜尋篩選準則。 這些搜尋篩選器會以 Unicode 字串表示。 下表列出 LDAP 搜尋篩選準則的一些範例。



| 搜尋篩選                                                               | Description                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| " (objectClass = \*) "                                                          | 所有物件。                                               |
| " (& (objectCategory = person)  (objectClass = user)  (！ (cn =) ) ) "                  | 所有使用者物件，但「會」。                               |
| " (sn = sm \*) "                                                                 | 姓氏開頭為 "sm" 的所有物件。          |
| " (& (objectCategory = person)  (objectClass = contact)  (\| (sn = Smith)  (sn = Johnson) ) ) " | 姓氏等於 "Smith" 或 "Johnson" 的所有連絡人。 |



 

這些搜尋篩選器會使用下列其中一種格式。


```C++
<filter>=(<attribute><operator><value>)
```



或


```C++
(<operator><filter1><filter2>)
```



ADSI 搜尋篩選器的使用方式有兩種。 它們構成了 LDAP 方言的一部分，可透過 OLE DB 提供者提交查詢。 它們也會搭配 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面使用。

## <a name="operators"></a>運算子

下表列出常用的搜尋篩選運算子。



| 邏輯運算子 | 描述                                |
|------------------|--------------------------------------------|
| =                | 等於                                   |
| ~=               | 大約等於                     |
| <=            | 詞典編纂小於或等於    |
| >=            | 詞典編纂大於或等於 |
| &                | AND                                        |
| \|               | OR                                         |
| !                | NOT                                        |



 

除了上述運算子之外，LDAP 還會定義兩個相符的規則物件識別碼 (Oid) ，可用來執行數值的位比較。 比對規則具有下列語法。


```C++
<attribute name>:<matching rule OID>:=<value>
```



「 &lt; 屬性名稱」 &gt; 是屬性（attribute）的 **lDAPDisplayName** ，「 &lt; 規則 OID」 &gt; 是比對規則的 OID，而「 &lt; 值」 &gt; 則是要用於比較的值。 請注意，這個字串中不能使用空格。 「 &lt; 值」 &gt; 必須是十進位數，不可以是十六進位數位或常數名稱，例如 **\_ 啟用 ADS 群組 \_ 類型 \_ 安全性 \_**。 如需可用 Active Directory 屬性的詳細資訊，請參閱 [所有屬性](/windows/desktop/ADSchema/attributes-all)。

下表列出 LDAP 所執行的相符規則 Oid。



| 符合規則 OID       | 從 Ntldap (的字串識別碼)    | Description                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **LDAP \_ \_ 比對規則 \_ 位 \_ 和**  | 只有當屬性中的所有位都符合值時，才會找到相符的。 這項規則相當於位 **and** 運算子。                                                                  |
| 1.2.840.113556.1.4.804  | **LDAP \_ \_ 比對規則 \_ 位 \_ 或**   | 如果屬性中的任何位符合值，就會找到相符的結果。 這項規則相當於位 **or** 運算子。                                                                        |
| 1.2.840.113556.1.4.1941 | **\_ \_ \_ 鏈中的 LDAP 比對規則 \_** | 此規則僅限於適用于 DN 的篩選準則。 這是特殊的「擴充」比對運算子，會將物件中的上階鏈一直指向根目錄，直到找到相符的結果為止。 |



 

下列查詢字串範例會搜尋已設定 **ADS \_ 群組 \_ 類型 \_ \_ 啟用安全性** 旗標的群組物件。 請注意， **\_ \_ \_ \_ 已啟用 ADS 群組型別安全性** 的 decimal 值 (0x80000000 = 2147483648) 用於比較值。


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



**\_ \_ \_ \_ CHAIN 中的 LDAP** 比對規則是一種比對規則 OID，其設計目的是要提供方法來查詢物件的上階。 使用 AD 和 AD LDS 的許多應用程式通常會使用階層式資料，而這些資料是以父子式關聯性來排序。 之前，應用程式執行了可轉移的群組延伸，以找出使用太多網路頻寬的群組成員資格;應用程式需要進行多次往返，以找出某個物件在鏈中是否有「在鏈中」的情況。

這類查詢的其中一個範例是設計來檢查使用者 "user1" 是否為群組 "group1" 的成員。 您會將基底設定為 [使用者 DN] `(cn=user1, cn=users, dc=x)` 和 [範圍] `base` ，然後使用下列查詢。


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



同樣地，若要尋找 "user1" 為其成員的所有群組，請將基底設定為群組容器 DN;例如， `(OU=groupsOU, dc=x)` 將範圍設為 `subtree` ，並使用下列篩選。


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



請注意， **\_ \_ \_ 在 \_ CHAIN 中使用 LDAP** 比對規則時，範圍不會受到限制，其可以是 `base` 、 `one-level` 或 `subtree` 。 子樹上的某些這類查詢可能會耗用更多處理器，例如，使用高展開連結的追蹤連結;也就是，列出使用者所屬的所有群組。 無效率的搜尋會記錄適當的事件記錄檔訊息，就像任何其他類型的查詢一樣。

## <a name="wildcards"></a>萬用字元

您也可以將萬用字元和條件新增至 LDAP 搜尋篩選準則。 下列範例顯示可以用來搜尋目錄的子字串。

取得所有專案：


```C++
(objectClass=*)
```



在一般名稱中的某個位置取得包含 "bob" 的專案：


```C++
(cn=*bob*)
```



取得一般名稱大於或等於 "bob" 的專案：


```C++
(cn>='bob')
```



取得具有電子郵件屬性的所有使用者：


```C++
(&(objectClass=user)(email=*))
```



取得電子郵件屬性和姓氏等於 "smith" 的所有使用者專案：


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



取得一般名稱開頭為 "margaret"、"steve" 或 "" 的所有使用者專案：


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



取得沒有電子郵件屬性的所有專案：


```C++
(!(email=*))
```



搜尋篩選準則的正式定義如下 (從 [RFC 2254](https://tools.ietf.org/html/rfc2254)) ：


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



Token &lt; attr &gt; 是代表 AttributeType 的字串。 Token &lt; 值 &gt; 是代表 AttributeValue 的字串，其格式是由基礎目錄服務所定義。

如果 &lt; 值 &gt; 必須包含星號 (\*) 、左括弧 ( () 或右括弧 () ) 字元，則字元前面必須加上反斜線 escape 字元 (\\) 。

## <a name="special-characters"></a>特殊字元

如果下列任何特殊字元必須以常值形式出現在搜尋篩選中，則必須以所列的 escape 順序取代這些特殊字元。



| ASCII 字元 | 換用換用順序 |
|-----------------|----------------------------|
| \*              | \\之                       |
| (               | \\日                       |
| )               | \\29                       |
| \\              | \\5c                       |
| NUL             | \\演講                       |
| /               | \\2f                       |



 

> [!Note]  
> 在使用多位元組字元集的情況下，如果 ADO 使用 SQL 方言執行搜尋，就必須使用上列的 escape 序列。

 

此外，您可以使用 escape 順序語法來表示任意二進位資料，方法是使用反斜線 (\\) 後接兩個十六進位數位來編碼每個位元組的二進位資料。 例如，四位元組值的 0x00000004 \\ \\ \\ 在篩選字串中會編碼為 00 00 00 \\ 04。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[LDAP 方言](ldap-dialect.md)
</dt> <dt>

[SQL 方言](sql-dialect.md)
</dt> <dt>

[使用 >idirectorysearch 介面搜尋](searching-with-idirectorysearch.md)
</dt> <dt>

[使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[使用 OLE DB 搜尋](searching-with-ole-db.md)
</dt> </dl>

 

 

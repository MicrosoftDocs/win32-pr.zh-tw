---
title: 建立查詢篩選
description: 查詢篩選準則會指示 Active Directory Domain Services 在 LDAP 查詢語法中尋找資料。 在選擇搜尋技術主題中所列的所有指定資料存取技術都支援 LDAP 查詢語法。
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，建立查詢篩選器
- 查詢篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839087"
---
# <a name="creating-a-query-filter"></a>建立查詢篩選

查詢篩選準則會指示 Active Directory Domain Services 在 LDAP 查詢語法中尋找資料。 在 [選擇搜尋技術](choosing-the-search-technology.md) 主題中所列的所有指定資料存取技術都支援 LDAP 查詢語法。

LDAP 查詢語法如下所示：


```C++
<expression><expression>...
```



篩選可包含一或多個運算式。 運算式的格式如下：


```C++
(<logicaloperator><comparison><comparison...>)
```



其中 " &lt; logicaloperator &gt; " 是下列其中一項。



| 運算子        | 說明                |
|-----------------|----------------------------|
| "\|"<br/> | 邏輯 **OR**<br/>  |
| "&"<br/>  | 邏輯 **AND**<br/> |
| "!"<br/>  | 邏輯 **NOT**<br/> |



 

和「 &lt; 比較」 &gt; 如下：


```C++
(<attribute><operator><value>)
```



其中 " &lt; attribute &gt; " 是要評估的屬性 **lDAPDisplayName** ，「值」 &lt; &gt; 是要比較的值，而「 &lt; 運算子」 &gt; 是下列其中一個比較運算子。



| 運算子           | 描述                         |
|--------------------|-------------------------------------|
| "="<br/>     | 等於<br/>                   |
| "~="<br/>    | 大約等於<br/>     |
| "<="<br/> | 小於或等於<br/>    |
| ">="<br/> | 大於或等於<br/> |



 

此外，根據屬性語法，" &lt; value &gt; " 可以包含萬用字元符號 ( " \* " ) 。 &lt;包含萬用字元的「值」 &gt; 會檢查 "attribute" 中是否有任何值存在 &lt; &gt; 。 如果未設定 " &lt; attribute" 的值 &gt; ，測試將會失敗。

如果下列任何特殊字元必須以常值形式出現在查詢篩選中，則必須以所列的 escape 順序取代這些特殊字元。



| ASCII 字元    | 換用換用順序 |
|--------------------|----------------------------|
| \*<br/>      | " \\ 2a"<br/>          |
| (<br/>       | " \\ 28"<br/>          |
| )<br/>       | " \\ 29"<br/>          |
| \\<br/>      | " \\ 5c"<br/>          |
| **NUL**<br/> | " \\ 00"<br/>          |



 

此外，您可以使用 escape 順序語法來表示任意的二進位資料，方法是將二進位資料的每個位元組編碼為反斜線，後面接著兩個十六進位數位。 例如，四位元組值的 0x00000004 \\ 在篩選字串中會編碼為 "00 \\ 00 \\ 00 \\ 04"。

## <a name="examples"></a>範例

下列查詢字串會搜尋 "computer" 類型的所有物件。


```C++
(objectCategory=computer)
```



下列查詢字串會搜尋 "computer" 類型的所有物件，其名稱開頭為 "desktop"。


```C++
(&(objectCategory=computer)(name=desktop*))
```



下列查詢字串會搜尋 "computer" 類型的所有物件，其名稱開頭為 "desktop" 或開頭為 "筆記本" 的名稱。


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



下列查詢字串會搜尋 "user" 類型的所有物件，其具有 home 電話號碼。


```C++
(&(objectCategory=user)(homePhone=*))
```



如需查詢篩選字串和使用方式範例的詳細資訊，請參閱：

-   [依類別尋找物件](finding-objects-by-class.md)
-   [依名稱尋找物件](finding-objects-by-name.md)
-   [尋找要查詢的屬性清單](finding-a-list-of-attributes-to-query.md)
-   [檢查查詢篩選語法](checking-the-query-filter-syntax.md)
-   [如何指定比較值](how-to-specify-comparison-values.md)

 

 






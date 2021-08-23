---
description: 呼叫 PeerGroupSearchRecords 函式時，需要用來判斷搜尋基本準則的 XML 查詢字串參數。
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: 記錄搜尋查詢格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23457cfde6955927b3efdcce5ae2dff94480c7cf56849b418547fe2503a36830
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517958"
---
# <a name="record-search-query-format"></a>記錄搜尋查詢格式

呼叫 [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) 函式時，需要用來判斷搜尋基本準則的 XML 查詢字串參數。 使用下列架構來制訂 XML 字串：

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a>用於記錄搜尋的元素

記錄搜尋中的主要元素是 **peersearch**，其中包含 **xmlns** 屬性中相關聯架構 (URI) 的統一資源識別項。 使用 **peersearch** 做為子專案時，您可以使用 **and**、 **子句** 和 **或** 做為子項目。

-   **和** - **和** 元素會對開頭和結束記號所包含的一或多個子句執行邏輯 and 運算。 其他 **和** 和 **或** 標記可以是子系，而且其子子句的遞迴結果會包含在作業中。

    例如，如果您想要取得的記錄中包含的名稱等於 James Peters、最後一個更新大於2/28/2003，或是小於1/31/2003 的建立日期，請使用下列 XML 查詢字串：

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   **子句** - **子句** 元素會指定基本的比較規則，將特定記錄屬性的值與開頭和結束記號之間的值進行比較。 [ **類型** ] 和 [ **比較** ] 屬性必須提供 [ **比較** ] 表示要執行的比較作業。 例如，表示所有相符記錄的簡單搜尋必須具有等於 James Peters 的 **peercreatorid** 值，如下所示：

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    一般 **類型** 屬性包括 **int**、 **string** 和 **date**。 **Date** 屬性可以是中所述的其中一種標準日期格式 [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) 。

    **Compare** 屬性的值是 **相等**、 **notequal**、 **less**、**大於**、 **lessorequal** 和 **greaterorequal**。

<!-- -->

-   **或** - **或** 專案會對開頭和結束記號所包含的一或多個子句執行邏輯 or 運算。 其他 **或** 和 **和** 元素可以是子系，而子子句的遞迴結果則包含在作業中。 例如，如果您想要取得的記錄中包含的名稱等於 James Peters，或者是1/31/2003 到2/28/2003 之間的最後一個更新，請使用下列 XML 查詢字串：

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a>記錄搜尋的詳細資訊

**Peersearch** 之後的第一個節點層級只能有一個元素。 不過，該元素的後續子系可以有許多相同層級的元素。

下列搜尋查詢不正確：

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

查詢失敗的原因是，針對比對傳回兩個值，但未將其解析為一個 true/false 值，這表示一個子句查詢的記錄名稱等於 James Peters，而 AND 運算則符合兩個元件子句。 結果會是兩個邏輯 true/false 值互相矛盾。

若要取得名稱等於 James Peters 的所有記錄，以及介於1/31/2003 到2/28/2003 之間的最後一個更新，請將 **子句** 和 **和** 標記放在開頭和結尾 **和** 標記之間的相同層級。 下列範例會顯示成功的查詢：

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

下列清單指出您必須知道才能撰寫成功查詢的其他特定資訊：

-   在開頭和結尾 **子句** 標記之間找不到 **and** 和 **or** 標記，因為在該設定中，它們會被解釋為要比對的值的一部分，而這會導致錯誤或失敗的相符。
-   每一組 **和** 和 **或** 開頭和結束記號都必須包含至少一個或多個子節點。
-   此架構中不允許零個元素集合。

## <a name="record-attributes"></a>記錄屬性

使用者可以使用 [記錄屬性架構](record-attribute-schema.md)，建立子句專案中的 **attrib** XML 屬性所指定的記錄屬性。 您可以使用架構中指定的格式，將 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)的 **PSZATTRIBUTES** 成員設定為 XML 字串，藉以加入新記錄的屬性。

對等基礎結構會保留下列屬性名稱：

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="special-characters"></a>特殊字元

某些字元可以用來表示比對模式，或換用其他特殊字元。 下表將說明這些字元。 

| 字元模式 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | 萬用字元。 當子句值中遇到此字元時，它會比對任何值的 0-n 字元，包括空白字元和非英數位元。 例如：<br/> "<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"<br/> 這個子句會比對名字為 "James" 和姓氏開頭為 "P" 的所有 **peercreatorid** 值。<br/> |
| \\\*              | 轉義的星號。 此序列符合星號字元。                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | 單一字元的萬用字元。 當子句值中遇到此字元時，它會比對任何單一字元，包括空白字元和英數位元。例如：<br/> 「<clause attrib="filename" type="string" compare="equal">data-0？ .xml</clause>」<br/> 這個子句會比對 **檔案名** 值，例如 "data-01.xml" 和 "data-0B.xml"。<br/>                              |
| \\?               | 已標記的問號。 此序列符合問號字元。                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | 已轉義的反斜線。 此序列符合單一反斜線字元。                                                                                                                                                                                                                                                                                                                                                               |



 

如果字元序列無效， [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) 函數就會傳回錯誤 **E \_ INVALIDARG**。 不正確序列是包含 " \\ " (反斜線) 字元後面不緊接 " \* " (星號) 字元、"？" (問號) 字元或另一個 " \\ " (反斜線) 字元的序列。

 

 





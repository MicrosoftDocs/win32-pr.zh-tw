---
description: 記錄可能會有應用程式專屬的屬性，這些屬性是一系列的名稱或值組，以對等記錄結構之 pszAttributes 成員中的 XML 字串表示 \_ 。
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: 記錄屬性架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3597369d7214b51b94a74b777315bb2ce2beb280232be5fb29571376ad3fc93e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612309"
---
# <a name="record-attribute-schema"></a>記錄屬性架構

記錄可能會有應用程式專屬的屬性，這些屬性是一系列的名稱或值組，以 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)結構之 **PSZATTRIBUTES** 成員中的 XML 字串表示。 屬性是用來篩選 [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords)呼叫所起始的記錄搜尋，這會採用 [記錄搜尋查詢格式](record-search-query-format.md) 所指定的 XML 搜尋篩選作為參數。

記錄屬性可以是下列三種類型的其中一種：

-   **int** 是整數值。
-   **date** 是表示為其中一種標準格式的日期時間值 [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) 。
-   **字串** 是 Unicode 字串值。

下列清單會識別對等基礎結構所保留的特定屬性名稱：

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="example-of-defining-record-attributes"></a>定義記錄屬性的範例

下列架構範例說明如何定義記錄屬性：

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="alphanum">
       <xs:restriction base="xs:string">
          <xs:pattern value="\c+" />
       </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="attributeType">
       <xs:simpleContent>
          <xs:extension base="xs:string">
                <xs:attribute name="name" type="alphanum" />
                <xs:attribute name="type">
                    <xs:simpleType>
                        <xs:restriction base="alphanum">
                           <xs:enumeration value="string"/>
                           <xs:enumeration value="date"/>
                           <xs:enumeration value="int"/>
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
           </xs:extension>
       </xs:simpleContent>
    </xs:complexType>
    <xs:element name="attributes">
       <xs:complexType>
           <xs:sequence>
                <xs:element name="attribute" type="attributeType" minOccurs="0" maxOccurs="unbounded" />
           </xs:sequence>
       </xs:complexType>
    </xs:element>
</xs:schema>  
```

> [!Note]  
> 屬性名稱必須是英數位元的序列。 屬性名稱中不允許特殊字元，例如連字號 ( "-" ) 和底線 ( " \_ " ) 。

 

下列 XML 屬性序列範例包含自訂的 **AuthenticationType** 和 **AuthExpires** 屬性，這些屬性會出現在 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)的 **pszAttributes** 成員中。

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 




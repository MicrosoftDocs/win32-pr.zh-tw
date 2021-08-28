---
description: 這個 &lt; searchConnectorDescriptionList &gt; 元素包含的搜尋連接器清單，會對應到此程式庫中包含的位置。 每個搜尋連接器都是由 &lt; searchConnectorDescription &gt; 元素定義。 這個元素是選擇性的，且沒有任何屬性。
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: 'searchConnectorDescriptionList 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc3a3cb7353529dccca66ffa15e1604bdd1c0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885604"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>searchConnectorDescriptionList 元素 (程式庫架構) 

這個 &lt; searchConnectorDescriptionList &gt; 元素包含的搜尋連接器清單，會對應到此程式庫中包含的位置。 每個搜尋連接器都是由 &lt; searchConnectorDescription &gt; 元素定義。 這個元素是選擇性的，且沒有任何屬性。

## <a name="syntax"></a>Syntax

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a>項目資訊



| Parent 項目                                                               | 子元素                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [libraryDescription 元素 (程式庫架構) ](schema-librarydescription.md) | [searchConnectorDescription 元素 (程式庫架構) ](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a>備註

Windows 同盟搜尋和通訊協定處理常式範圍的搜尋連接器不能包含在程式庫中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式庫描述架構](library-schema-entry.md)
</dt> <dt>

[搜尋連接器描述架構](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 

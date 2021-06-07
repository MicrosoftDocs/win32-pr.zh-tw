---
description: 筆記本便箋 XML 檔案中的最上層元素。
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: JournalDocument 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432170"
---
# <a name="journaldocument-element"></a>JournalDocument 元素

筆記本便箋 XML 檔案中的最上層元素。

## <a name="definition"></a>定義

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a>父項目

無。

## <a name="child-elements"></a>子元素

[**信箋**](stationery-element.md)

[**JournalPage**](journalpage-element.md)

## <a name="attributes"></a>屬性



| 屬性             | 類型                      | 必要 | 描述                                                      | 可能的值           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **版本**           | **xs:string**             | 必要 | XML 檔案中表示的日誌檔版本。 | 1.0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | 必要 | 筆記本檔的預設頁面寬度。          | 任何非負整數。 |
| **DefaultPageHeight** | **xs:nonNegativeInteger** | 必要 | 筆記本檔頁面的預設高度。         | 任何非負整數。 |



 

## <a name="element-information"></a>項目資訊



|  元素     | 值                                                     |
|--------------|--------------------------------------------|
| 項目類型 | **JournalDocument**                        |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink |
| 結構描述名稱  | 日誌讀者                             |



 

 

 




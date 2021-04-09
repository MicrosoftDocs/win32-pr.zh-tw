---
description: 將列舉文字指派給某個範圍的值。 每個 enumRange 元素都會指定最小值，並延伸到下一個元素的最小值，或直到沒有其他 enumRange 元素為止。
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943855"
---
# <a name="enumrange"></a>enumRange

將列舉文字指派給某個範圍的值。 每個 [enumRange]() 元素都會指定最小值，並延伸到下一個元素的最小值，或直到沒有其他 enumRange 元素為止。

## <a name="syntax"></a>Syntax

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>項目資訊



| Parent 項目                                         | 子元素 |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | 無           |



 

## <a name="attributes"></a>屬性



| 屬性 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| minValue  | 公用。 必要。 範圍中的最小值。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| setValue  | 公用。 選擇性。 當使用者從 listbox 屬性控制項選取這個列舉時，此離散值會被指派為屬性值。                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| text      | 公用。 選擇性。 用來顯示列舉值的文字。 語法允許直接顯示字串或間接顯示字串參考;使用間接顯示字串，使其可以當地語系化。                                                                                                                                                                                                                                                                                                                                                                                                   |
| 助憶鍵 | **Windows 7 和更新版本。** 公用。 選擇性。 助憶鍵值的清單，可用來參考搜尋查詢中的屬性。 此清單以 ' \| ' 字元分隔。                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NAME      | 必要。 標準屬性名稱，對系統而言是唯一的;例如，系統評等。 這個屬性的限制為64個字元。 名稱區分大小寫，且應使用下列語法： PropertyName。 下列方法會傳回這個值： [**IExplorerCommand：： GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname)、 [**IPropertyDescription：： GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname)、 [**IPropertyDescription2：： GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)和 [**IPropertyUI：： GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85))。 |



 

 

 

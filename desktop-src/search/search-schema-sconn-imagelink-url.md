---
description: <url>元素指定此搜尋連接器的縮圖 URL。 如果 <imageLink> 存在，則需要這個元素。 它沒有任何子項目，而且沒有任何屬性。
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: 'imageLink url 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986309"
---
# <a name="imagelink-url-element-search-connector-schema"></a>imageLink url 元素 (搜尋連接器架構) 

<url>元素指定此搜尋連接器的縮圖 URL。 如果 <imageLink> 存在，則需要這個元素。 它沒有任何子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                                   | 子元素 |
|----------------------------------------------------------------------------------|----------------|
| [imageLink 元素 (搜尋連接器架構) ](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a>備註

值可以是本機檔案系統路徑或 URL。 影像檔案可以是 Windows 7 (PNG、BMP、JPG、GIF) 所支援的任何基本映射類型。

## <a name="example-of-an-imagelinkurl-element"></a>ImageLinkurl 元素範例


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 




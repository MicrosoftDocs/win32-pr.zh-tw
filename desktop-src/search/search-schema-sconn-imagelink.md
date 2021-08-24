---
description: 選擇性 <imageLink> 元素會指定此搜尋連接器的縮圖。 這個元素有一個必要的子項目，而且沒有任何屬性。
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: 'imageLink 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007ad8c2500e2739210646c446d9f906d5a83571ea4ac9780ab9136b73805c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711088"
---
# <a name="imagelink-element-search-connector-schema"></a>imageLink 元素 (搜尋連接器架構) 

選擇性 <imageLink> 元素會指定此搜尋連接器的縮圖。 這個元素有一個必要的子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- imageLink -->
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



| Parent 項目                                                                                                   | 子元素                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [searchConnectorDescriptionType 元素 (搜尋連接器架構) ](search-schema-searchconnectordescription.md) | [imageLink url 元素 (搜尋連接器架構) ](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>備註

ImageLink 值可以是本機檔案系統路徑或 URL。 影像檔案可以是 Windows 7 (PNG、BMP、JPG、GIF) 所支援的任何基本影像類型。

## <a name="example-of-an-imagelink-element"></a>ImageLink 元素範例


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 




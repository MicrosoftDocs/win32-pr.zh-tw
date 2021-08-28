---
description: 這個選擇性 &lt; &gt; 的 templateInfo 元素會指定資料夾類型，以顯示透過此搜尋連接器查詢的結果。 這個元素沒有任何屬性，而且只有一個強制子系。
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: 'templateInfo 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c815d04e23f1e1af9582ad93ba08d118855676
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880387"
---
# <a name="templateinfo-element-search-connector-schema"></a>templateInfo 元素 (搜尋連接器架構) 

這個選擇性 &lt; &gt; 的 templateInfo 元素會指定資料夾類型，以顯示透過此搜尋連接器查詢的結果。 這個元素沒有任何屬性，而且只有一個強制子系。

## <a name="syntax"></a>Syntax


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                                                                   | 子元素                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [searchConnectorDescriptionType 元素 (搜尋連接器架構) ](search-schema-searchconnectordescription.md) | [folderType 元素 (搜尋連接器架構) ](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a>備註

如果您未在 templateInfo 元素中指定特定的資料夾類型 &lt; &gt; ，Windows 會使用一般搜尋連接器資料夾類型 {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}。

## <a name="example-of-a-templateinfo-element"></a>TemplateInfo 元素範例


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 




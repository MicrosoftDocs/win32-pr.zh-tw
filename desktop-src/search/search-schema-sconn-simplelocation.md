---
description: 專案 <simpleLocation> 會指定以檔案系統為基礎或依通訊協定處理常式為基礎之搜尋連接器的位置。 此元素有兩個子項目，而且沒有任何屬性。
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: 'simpleLocation 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82731c5a230f8dd12b9d73cafd75dfc7d3cdd66bf1e57120701ed3ca0ba54b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862459"
---
# <a name="simplelocation-element-search-connector-schema"></a>simpleLocation 元素 (搜尋連接器架構) 

專案 <simpleLocation> 會指定以檔案系統為基礎或依通訊協定處理常式為基礎之搜尋連接器的位置。 此元素有兩個子項目，而且沒有任何屬性。

## <a name="syntax"></a>Syntax


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                                                                   | 子元素                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [searchConnectorDescriptionType 元素 (搜尋連接器架構) ](search-schema-searchconnectordescription.md) | [simpleLocation url 元素 (搜尋連接器架構) ](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | 已序列化：此元素包含指向專案中定義之位置的 base64 編碼 ShellLink <url> 。 Windows 7 會從專案的值建立 ShellLink <url> ，並在此程式庫的第一次載入時適當地更新此欄位，作者應將其保留空白。 |



 

## <a name="remarks"></a>備註

您可以使用這個元素，而不是在 <locationProvider> 檔案系統上的位置，或連接器是已知的通訊協定處理常式 (例如 mapi： ) 。 如果 <simpleLocation> 存在，就不能有 <locationProvider> 元素。 若為 web 服務提供者搜尋連接器，請改用 [<locationProvider>](search-schema-sconn-locationprovider.md) 元素。

## <a name="examples"></a>範例


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 




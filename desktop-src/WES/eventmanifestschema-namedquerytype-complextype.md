---
title: NamedQueryType 複雜類型
description: 未使用。 定義已命名查詢的清單，這些查詢會查詢事件訊息字串中的值，並執行指定的動作（如果找到的話）。 |NamedQueryType 複雜類型
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- NamedQueryType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981238"
---
# <a name="namedquerytype-complex-type"></a>NamedQueryType 複雜類型

未使用。 定義已命名查詢的清單，這些查詢會查詢事件訊息字串中的值，並執行指定的動作（如果找到的話）。

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                       | 類型                                                                             | Description                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**patternMaps**](eventmanifestschema-patternmaps-namedquerytype-element.md) | [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) | 定義用來改變訊息字串的正則運算式組清單。<br/> |



## <a name="examples"></a>範例

下列範例示範如何使用 [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) 元素。 此範例會取得訊息字串的內容，並將其插入字串 https://www 。*messagestring*.com。 然後，它會將訊息字串取代為結果。 例如，如果訊息字串包含 Microsoft，則查詢會將 Microsoft message 字串取代為 https://www.Microsoft.com 。


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 






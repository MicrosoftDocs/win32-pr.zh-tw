---
title: TemplateItemType 複雜類型
description: 此範本會定義要包含在事件中的資料。 |TemplateItemType 複雜類型
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- TemplateItemType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 147cd54f1503630cd3ea7467a7fd70162f1d2b3ab9db46178960587f164856a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936913"
---
# <a name="templateitemtype-complex-type"></a>TemplateItemType 複雜類型

此範本會定義要包含在事件中的資料。

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                   | 類型                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**二 進 制**](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | 已保留供內部使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**資料**](eventmanifestschema-data-templateitemtype-element.md)         | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)     | 定義您想要包含在事件中的資料項目。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**結構**](eventmanifestschema-struct-templateitemtype-element.md)     | [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md) | 定義結構，其中包含一個或多個您想要包含在事件中的資料項目。 提供者會將結構撰寫為 blob，而不是結構的個別成員。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) | [**XmlType**](eventmanifestschema-xmltype-complextype.md)                           | 用來呈現事件資料的 XML 片段。 如果您未包含片段，則會以範本中定義資料項目的順序轉譯事件資料。 此元素的內容是任何有效的 XML 片段。 片段必須只包含一個最上層節點，而且最上層節點必須指定它自己的命名空間。 <br/> 若要參考片段中的資料項目，請將片段中節點的文字主體設定為%*n*，其中 *n* 是資料項目清單中最上層資料項目的單一索引， (您無法參考結構) 的成員。 您指定的索引值不得大於範本中最上層資料項目的數目。<br/> 這個元素會遵循所有 **資料** 和 **結構** 元素。 <br/> |



## <a name="attributes"></a>屬性



| 名稱 | 類型   | 描述                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NAME | 字串 | 已保留供內部使用。<br/>                                                                                                                                                            |
| NAME | 字串 | 範本名稱。<br/>                                                                                                                                                                  |
| tid  | token  | 唯一識別提供者所定義之範本清單內範本的識別碼。 當您定義事件定義時，請使用這個名稱來參考範本。<br/> |



## <a name="remarks"></a>備註

範本定義必須至少有一個資料或結構子項目。 提供者必須以範本中定義之資料項目的順序來寫入事件資料。

範本中所有資料項目的大小必須小於 64 KB。

## <a name="examples"></a>範例

下列範例顯示如何建立範本定義。


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 






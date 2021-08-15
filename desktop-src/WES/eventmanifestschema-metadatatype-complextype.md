---
title: MetadataType 複雜類型
description: 定義您可以在資訊清單的 metadata 區段中定義的元資料類型。
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- MetadataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 392e0bb2940c36b541f63f55dac418312489f231d785f82014ade82c20602fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343600"
---
# <a name="metadatatype-complex-type"></a>MetadataType 複雜類型

定義您可以在資訊清單的 metadata 區段中定義的元資料類型。

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                       | 類型                                                                       | Description                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**管道**](eventmanifestschema-channels-metadatatype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md) | 定義提供者可以記錄事件的通道清單。 然後，提供者可以在其資訊清單中匯入一或多個通道。<br/>               |
| [**關鍵 字**](eventmanifestschema-keywords-metadatatype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) | 定義關鍵字清單，以決定提供者寫入的事件類別。<br/>                                                            |
| [**水準**](eventmanifestschema-levels-metadatatype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)     | 定義指定事件嚴重性的層級清單。<br/>                                                                                       |
| **message**                                                                   |                                                                            | 定義訊息字串。<br/>                                                                                                                             |
| **messageTable**                                                              |                                                                            | 定義訊息字串的清單。<br/>                                                                                                                    |
| [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)   | 定義已命名查詢的清單，這些查詢會使用正則運算式來執行事件訊息字串的尋找和取代動作。<br/>                        |
| [**碼**](eventmanifestschema-opcodes-metadatatype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)   | 定義可用於將工作中的事件群組在一起的作業碼清單。<br/>                                                                             |
| **任務**                                                                     | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)       | 定義提供者可用來群組事件的工作清單。 一般而言，您會使用工作將提供者的功能或元件的事件分組。<br/> |
| [**類型**](eventmanifestschema-types-metadatatype-element.md)               | [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)       | 定義 XML 類型的清單。<br/>                                                                                                                          |



## <a name="attributes"></a>屬性



| 名稱    | 類型                                                              | Description                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | 字串資料表中當地語系化字串的參考。<br/>                                |
| mid     | xs:string                                                         | 未使用。<br/>                                                                               |
| NAME    | anyURI                                                            | 中繼檔案的 URI。 <br/>                                                              |
| 符號  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 您希望訊息編譯器為此訊息字串建立的符號名稱。<br/> |
| 值   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | 要用來做為此訊息之訊息識別碼的數位。<br/>                           |



## <a name="remarks"></a>備註

雖然您可以建立包含中繼資料區段的資訊清單，但服務將不會使用它。服務唯一可辨識的中繼資料是 Winmeta.xml 檔案中找到的中繼資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 






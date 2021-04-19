---
title: StructDefinitionType 複雜類型
description: 定義結構，其中包含一個或多個您想要包含在事件中的資料項目。 |StructDefinitionType 複雜類型
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- StructDefinitionType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997344"
---
# <a name="structdefinitiontype-complex-type"></a>StructDefinitionType 複雜類型

定義結構，其中包含一個或多個您想要包含在事件中的資料項目。

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                               | 類型                                                                             | Description                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**資料**](eventmanifestschema-data-structdefinitiontype-element.md) | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md) | 定義您想要包含在結構中的資料項目。<br/> |



## <a name="attributes"></a>屬性



| 名稱   | 類型                                                            | 描述                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count  | [**CountType**](eventmanifestschema-counttype-simpletype.md)   | 結構陣列中的元素數目。 這個屬性指出結構正在定義結構的陣列。 您可以指定包含計數之結構外部的實際計數或資料項目目名稱。 <br/>                               |
| 長度 | [**LengthType**](eventmanifestschema-lengthtype-simpletype.md) | 不適用。<br/> **Windows Server 2008 和 Windows Vista：** 此結構的長度（以位元組為單位）。 從 Windows 7 開始無法使用。<br/>                                                                                                                            |
| NAME   | 字串                                                          | 結構的名稱。 如果您在範本中指定 [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) 區段，您可以使用名稱來參考 XML 片段中的資料項目。<br/> **Windows Vista：** 這個屬性是選擇性的。<br/> |



## <a name="remarks"></a>備註

提供者會將結構撰寫為 blob，而不是結構的個別成員。 如果您所撰寫的 C 結構包含指標 (例如，型別 LPWSTR) 的指標，事件資料將會包含指標值，而不是已取值的資料。

您不應該使用結構，而應該改為針對每個成員定義資料項目，然後個別撰寫這些資料項目。 如果您決定要使用結構，則結構只應包含整數類資料類型，而您必須確保結構的成員符合8位元組的界限。 如果不這麼做，當您嘗試存取資料時，可能會收到對齊錯誤。 請考慮使用 \# pragma pack () 指示詞來強制在8位元組的界限上對齊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 






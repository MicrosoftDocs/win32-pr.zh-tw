---
title: DebugDataType 複雜類型
description: 定義可以記錄 Windows 軟體追蹤預處理器 (WPP) 事件的資料。
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- DebugDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38d5ec0297fce91b28592dfb9a894a62d3558f516a01ff18c942d37cc9c93f2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124228"
---
# <a name="debugdatatype-complex-type"></a>DebugDataType 複雜類型

定義可以記錄 Windows 軟體追蹤預處理器 (WPP) 事件的資料。

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
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



| 元素                                                                    | 類型        | 描述                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [**元件**](eventschema-component-debugdatatype-element.md)           | 字串      | 記錄追蹤訊息的元件名稱。<br/>                                                |
| [**FileLine**](eventschema-fileline-debugdatatype-element.md)             | 字串      | 來源檔案的名稱，以及記錄追蹤訊息之原始程式檔內的行。<br/>          |
| [**FlagsName**](eventschema-flagname-debugdatatype-element.md)            | 字串      | 啟用時傳遞給提供者的旗標值。<br/>                                              |
| [**Function**](eventschema-function-debugdatatype-element.md)             | unsignedInt | 記錄追蹤訊息的函數名稱。<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | 字串      | 啟用時傳遞給提供者的層級值。<br/>                                             |
| [**消息**](eventschema-message-debugdatatype-element.md)               | 字串      | 訊息字串。 如果 WPP 事件指定了 FormattedString 欄位，XML 就會包含這個元素。<br/> |
| [**SequenceNumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | 追蹤訊息的本機或全域序號。<br/>                                               |
| [**子元件**](eventschema-subcomponent-debugdatatype-element.md)     | 字串      | 記錄追蹤訊息的子元件名稱。<br/>                                             |



## <a name="remarks"></a>備註

只有在提供者將% TRACE \_ 格式 \_ 前置詞% 環境變數設定為包含這些專案時，才會包含這些元素。 如需這些元素的詳細資訊，請參閱追蹤訊息前置詞。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 






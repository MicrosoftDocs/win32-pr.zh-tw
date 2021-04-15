---
title: 事件種類複雜類型
description: 定義事件架構的根節點。
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- 事件種類複雜類型 EventLog
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384006"
---
# <a name="eventtype-complex-type"></a>事件種類複雜類型

定義事件架構的根節點。

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
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



| 元素                                                                          | 類型                                                                               | Description                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BinaryEventData**](eventschema-binaryeventdata-eventtype-element.md)         | hexBinary                                                                          | 以二進位 blob 的形式包含事件資料。 如果轉譯函數找不到用來解碼事件的中繼資料，則會將事件資料轉譯成二進位 blob。<br/>                                                                                                                                                            |
| [**DebugData**](eventschema-debugdata-eventtype-element.md)                     | [**DebugDataType**](eventschema-debugdatatype-complextype.md)                     | 包含可針對 Windows 軟體追蹤預處理器 (WPP) 事件記錄的資料。<br/>                                                                                                                                                                                                                                    |
| [**EventData**](eventschema-eventdata-eventtype-element.md)                     | [**EventDataType**](eventschema-eventdatatype-complextype.md)                     | 包含事件資料。 範本中資料項目的順序會決定事件資料的版面配置。<br/>                                                                                                                                                                                                                 |
| [**ProcessingErrorData**](eventschema-processingerrordata-eventtype-element.md) | [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) | 包含嘗試呈現事件時所發生之錯誤的詳細資料。 如果事件資料與資訊清單中的事件資料定義不符，就會發生這種情況。 事件資料會以二進位 blob 的形式包含。<br/>                                                                                                         |
| [**RenderingInfo**](eventschema-renderinginfo-eventtype-element.md)             | [**RenderingInfoType**](eventschema-renderingtype-complextype.md)                 | 包含事件的已轉譯訊息字串 (包含事件的訊息字串，以及任何事件屬性的訊息字串，例如層級、工作和 opcode) 。 只有使用 [Windows 事件收集器](/windows/desktop/WEC/windows-event-collector) 服務所收集的事件才會包含此區段。<br/> |
| [**系統**](eventschema-system-eventtype-element.md)                           | [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)       | 包含識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**UserDataType**](eventschema-userdatatype-complextype.md)                       | 包含事件資料。 範本的 [使用者資料] 區段會決定事件資料的版面配置。<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>備註

此區段通常會包含 **EventData** 或 **UserData** 區段。 如果範本未包含 **UserData** 區段，則會使用 **EventData** 區段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 


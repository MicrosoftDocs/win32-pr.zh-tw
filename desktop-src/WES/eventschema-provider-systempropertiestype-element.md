---
title: 提供者 (SystemPropertiesType) 元素
description: 識別記錄事件的提供者。
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Provider 元素 EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024749"
---
# <a name="provider-systempropertiestype-element"></a>提供者 (SystemPropertiesType) 元素

識別記錄事件的提供者。

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

**Provider** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)複雜型別定義。

## <a name="attributes"></a>屬性



| 名稱            | 類型                                                | Description                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| EventSourceName | 字串                                              | 如果事件來源來自舊版 [事件記錄](/windows/desktop/EventLog/event-logging) API) ，則發佈事件 (事件來源的名稱。<br/> |
| Guid            | [**GUIDType**](eventschema-guidtype-simpletype.md) | 可唯一識別提供者的全域唯一識別碼。<br/>                                                                   |
| Name            | anyURI                                              | 記錄事件之事件提供者的名稱。<br/>                                                                                   |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**系統 (的系統事件)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 


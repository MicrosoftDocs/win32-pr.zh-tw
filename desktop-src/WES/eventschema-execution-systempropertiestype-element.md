---
title: 執行 (SystemPropertiesType) 元素
description: 包含記錄事件之進程和執行緒的相關資訊。
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- 執行元素 EventLog
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685622"
---
# <a name="execution-systempropertiestype-element"></a>執行 (SystemPropertiesType) 元素

包含記錄事件之進程和執行緒的相關資訊。

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

**執行** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)複雜型別定義。

## <a name="attributes"></a>屬性



| 名稱          | 類型         | Description                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| KernelTime    | unsignedInt  | 核心模式指令的已耗用執行時間，以 CPU 時間單位表示。<br/>                        |
| ProcessID     | unsignedInt  | 識別已產生事件的處理序。<br/>                                               |
| ProcessorID   | unsignedByte | 處理事件之處理器的識別碼。<br/>                          |
| ProcessorTime | unsignedInt  | 針對 ETW 私用會話，使用者模式指示的經過執行時間，以 CPU 滴答為單位。<br/> |
| SessionID     | unsignedInt  | 發生事件之終端機伺服器工作階段的識別碼。<br/>         |
| ThreadID      | unsignedInt  | 識別已產生事件的執行緒。<br/>                                                |
| UserTime      | unsignedInt  | 使用者模式指示的經過執行時間，以 CPU 時間單位表示。<br/>                          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**系統 (的系統事件)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 






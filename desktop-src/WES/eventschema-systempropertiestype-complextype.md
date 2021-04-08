---
title: SystemPropertiesType 複雜類型
description: 定義識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- SystemPropertiesType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686213"
---
# <a name="systempropertiestype-complex-type"></a>SystemPropertiesType 複雜類型

定義識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
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
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
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
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
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



| 元素                                                                         | 類型                                                        | Description                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**通路**](eventschema-channel-systempropertiestype-element.md)             | anyURI                                                      | 要記錄事件的通道。<br/>                                                                                                                                                                                                                                                                                        |
| [**電腦**](eventschema-computer-systempropertiestype-element.md)           | 字串                                                      | 發生事件之電腦的名稱。<br/>                                                                                                                                                                                                                                                                             |
| [**相關**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | 取用者可用來將相關事件群組在一起的活動識別碼。<br/>                                                                                                                                                                                                                                                 |
| [**EventID**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | 提供者用來識別事件的識別碼。<br/>                                                                                                                                                                                                                                                                      |
| [**EventRecordID**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | 記錄時指派給事件的記錄號碼。<br/>                                                                                                                                                                                                                                                                       |
| [**執行**](eventschema-execution-systempropertiestype-element.md)         |                                                             | 包含記錄事件之進程和執行緒的相關資訊。<br/>                                                                                                                                                                                                                                                          |
| [**關鍵字**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | 事件中所定義關鍵字的位元遮罩。 關鍵字是用來分類事件種類 (例如，與讀取資料) 相關聯的事件。<br/>                                                                                                                                                                                 |
| [**水準**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | 事件中定義的嚴重性層級。<br/>                                                                                                                                                                                                                                                                                          |
| [**OpCode**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | 事件中定義的操作碼。 工作和 opcode 的 typcially 是用來識別應用程式中記錄事件的位置。<br/>                                                                                                                                                                                  |
| [**提供者**](eventschema-provider-systempropertiestype-element.md)           |                                                             | 識別記錄事件的提供者。 如果提供者使用檢測資訊清單來定義其事件，則會包含 **Name** 和 **Guid** 屬性;否則，如果舊版事件提供者 (使用 [事件記錄](/windows/desktop/EventLog/event-logging)API) 記錄事件，則會包含 **EventSourceName** 屬性。<br/> |
| [**安全性**](eventschema-security-systempropertiestype-element.md)           |                                                             | 識別記錄事件的使用者。<br/>                                                                                                                                                                                                                                                                                        |
| [**Task**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | 事件中定義的工作。 工作和 opcode 通常用來識別應用程式中記錄事件的位置。<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | 識別事件記錄時間的時間戳記。 時間戳記會包含 **SystemTime** 屬性或 **RawTime** 屬性。<br/>                                                                                                                                                                           |
| [**版本**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | 事件定義的版本號碼。<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>屬性



| 名稱              | 類型                                                | Description                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | 識別目前活動的全域唯一識別碼。 以此識別碼發佈的事件是相同活動的一部分。<br/>                                                                                                                                         |
| EventSourceName   | 字串                                              | 如果事件來源來自舊版 [事件記錄](/windows/desktop/EventLog/event-logging) API) ，則發佈事件 (事件來源的名稱。<br/>                                                                                                                                                      |
| Guid              | [**GUIDType**](eventschema-guidtype-simpletype.md) | 可唯一識別提供者的全域唯一識別碼。<br/>                                                                                                                                                                                                                        |
| KernelTime        | unsignedInt                                         | 核心模式指令的已耗用執行時間，以 CPU 時間單位表示。 如果您使用的是 ETW 私用會話，請改用 ProcessorTime 成員中的值。 僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。<br/>                                               |
| Name              | anyURI                                              | 提供者的名稱。<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | 識別已產生事件的處理序。<br/>                                                                                                                                                                                                                                             |
| ProcessorID       | unsignedByte                                        | 處理事件之處理器的識別碼。 僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。<br/>                                                                                                                                             |
| ProcessorTime     | unsignedInt                                         | 針對 ETW 私用會話，使用者模式指示的經過執行時間，以 CPU 滴答為單位。 僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。<br/>                                                                                                                    |
| 限定詞        | **unsignedShort**                                   | 舊版提供者會使用32位的數位來識別其事件。 如果舊版提供者記錄此事件， **EventID** 元素的值會包含事件識別碼的低序位16位，且 **限定詞** 屬性包含事件識別碼的高序位16位。<br/> |
| RawTime           | unsignedLong                                        | 原始時間戳記值;時間戳記的格式取決於用來收集追蹤的時間來源。 未經處理的時間戳記提供比系統時間更高的精確度。 如果您搭配-rts 參數使用 TraceRpt.exe，轉譯的事件輸出只會包含原始時間。<br/>                 |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | 全域唯一識別碼，用來識別要將控制項傳送至其中的活動。 相關事件接著會有此識別碼作為其 ActivityID 識別碼。<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | 發生事件之終端機伺服器工作階段的識別碼。 僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | 記錄事件的系統時間。<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | 識別已產生事件的執行緒。<br/>                                                                                                                                                                                                                                              |
| UserID            | 字串                                              | 以字串形式 (SID) 使用者的安全識別碼。<br/>                                                                                                                                                                                                                                    |
| UserTime          | unsignedInt                                         | 使用者模式指示的經過執行時間，以 CPU 時間單位表示。 如果您使用的是 ETW 私用會話，請改用 ProcessorTime 成員中的值。 僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。<br/>                                                 |



## <a name="remarks"></a>備註

根據預設，事件會包含電腦 (FQDN) 的完整功能變數名稱。 若要使用 NETBIOS 名稱而不是 FQDN，您必須在下列登錄機碼底下建立名為 CompatFlags 的 DWORD 登錄值，並將 CompatFlags 的值設定為0x2。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 


---
title: ChannelPublishingType 複雜類型
description: 為通道所使用的會話定義記錄屬性。 |ChannelPublishingType 複雜類型
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- ChannelPublishingType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997231"
---
# <a name="channelpublishingtype-complex-type"></a>ChannelPublishingType 複雜類型

為通道所使用的會話定義記錄屬性。

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
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



| 元素                                                                              | 類型                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**bufferSize**](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | 針對每個緩衝區配置的記憶體數量（以 kb 為單位）。 如果您預期較低的事件速率，緩衝區大小應該設定為記憶體頁面大小。 如果事件速率預期會相當高，您應該指定較大的緩衝區大小並增加緩衝區的最大數目。<br/> 緩衝區大小會影響緩衝區填滿和必須排清的速率。 雖然小型緩衝區大小需要較少的記憶體，但它會增加緩衝區必須排清的速率。<br/> 分析和偵測通道的預設緩衝區大小為 4 KB，而系統管理員和運作方式為 64 KB。<br/>                                                                                                                |
| [**clockType**](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | 記錄每個事件的時間戳記時，所要使用的時鐘解析。 您可以指定 SystemTime 或 QPC。 SystemTime 提供低解析度 (10 毫秒) 時間戳記，但要取得的成本相對較低。 預設值為 SystemTime。 <br/> Query 效能計數器 (QPC) 提供高解析度的 (100 納秒) 時間戳記，但耗用的成本會相對較高。 如果您有高事件率，或取用者合併來自不同緩衝區的事件，您應該 QPC。<br/>                                                                                                                                                                                                                                 |
| [**controlGuid**](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | 識別包含 WPP 事件之 ETW 會話的會話 GUID。 這項設定只允許用於 Debug 類型的通道。 這些通道無法完全啟用，關鍵字設定為零 (0x0000000000000000) 。 它們必須啟用，並將關鍵字設為0xffffffffffffffff。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **fileMax**                                                                          | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | 啟用通道時，您要讓服務建立新記錄檔的最大次數 (包括重新開機電腦) 。 如果值為0或1，則服務會在每次啟用通道時覆寫記錄檔，而且會遺失先前的事件。 如果值大於1，則服務會在每次啟用通道時建立新的記錄檔，以便保留事件。 預設值為1，而且您可以指定的最大值為16。<br/> 服務會將三位數的十進位數附加至每個檔案名，介於0和 fileMax 1 之間。 例如，etl.xxx，其中 xxx 是三位數的十進位 *數。* 這些檔案位於% windir% \\ System32 \\ \system32\winevt\logs\application.evtx 記錄檔中 \\ 。<br/> |
| [**關鍵 字**](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | 位元遮罩，可決定寫入通道的事件分類。 如果 **關鍵字** 屬性的值為0，則提供者寫入的所有事件都會寫入至通道;否則，只有定義了 **關鍵字** 位元遮罩之關鍵字的事件會寫入至通道。 預設值是 0。<br/> 具有 controlGuid 屬性集的 Debug 通道必須將 **關鍵字** 屬性設定為0xFFFFFFFFFFFFFFFF。<br/> 會話啟用提供者時，會將關鍵字值傳遞給提供者。<br/>                                                                                                                                                                            |
| [**延遲**](eventmanifestschema-latency-channelpublishingtype-element.md)         | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | 清除緩衝區之前等候的時間（以毫秒為單位）。 如果為零，ETW 會在緩衝區填滿時立即將其清除。 如果是非零值，ETW 會根據值（即使緩衝區未滿）來排清包含事件的所有緩衝區。 一般來說，您只想要在緩衝區填滿時排清緩衝區。 強制緩衝區排清可以增加具有未填滿緩衝區空間的記錄檔大小。 系統管理員和作業記錄的預設值為1秒，分析和偵錯工具記錄檔的預設值為5秒。<br/>                                                                                                                                                                                                                               |
| [**等級**](eventmanifestschema-level-channelpublishingtype-element.md)             | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | 要寫入通道之事件的嚴重性層級。 服務會將事件寫入至層級值小於或等於指定值的通道。 預設值為0，這表示要記錄具有任何層級值的事件。<br/> 會話啟用提供者時，會將層級值傳遞給提供者。<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**maxBuffers**](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | 要配置給會話的緩衝區數目上限。 一般來說，此值是緩衝區數目下限加上二十。 此值必須大於或等於針對 minBuffers 指定的值。<br/> 分析和偵測通道的預設緩衝區數目上限為 10 KB，而系統管理員和運作方式為 64 KB。<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**minBuffers**](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | 要配置給會話的緩衝區數目下限。 預設值是零。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**sidType**](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | 決定是否要包含主體的安全識別碼 (SID) ，並將每個事件寫入通道。 若要將 SID 包含在事件中，請將此屬性設定為「發佈」。 SID 會根據寫入事件時的執行緒識別來設定。 如果您不想要在事件中包含 SID，請將此屬性設定為「無」。 預設值為「發佈」。<br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>備註

您可以針對分析和偵測通道類型或指定自訂隔離的任何通道指定此發行資訊。

雖然您可以指定層級和關鍵字，但您應該考慮這些將是您將從該通道的提供者接收的唯一事件。

當緩衝區已滿時，ETW 會將緩衝區排清到記錄檔。 如果緩衝區的填滿速度超過可以排清的緩衝區，則會配置新的緩衝區，並將其新增至會話的緩衝集區，最多可達指定的最大數目。 超過此限制，會話會捨棄傳入事件，直到緩衝區變成可用為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 






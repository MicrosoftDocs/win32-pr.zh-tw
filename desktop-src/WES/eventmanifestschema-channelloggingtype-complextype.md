---
title: ChannelLoggingType 複雜類型
description: 定義支援通道之記錄檔的屬性，例如其容量，以及是否為連續或迴圈。 |ChannelLoggingType 複雜類型
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- ChannelLoggingType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e696837b1132a0b82ad428e7404892ae73de88e4435325d988b7936b3a6ba534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032278"
---
# <a name="channelloggingtype-complex-type"></a>ChannelLoggingType 複雜類型

定義支援通道之記錄檔的屬性，例如其容量，以及是否為連續或迴圈。

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
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



| 元素                                                                         | 類型                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) | boolean                                                           | 決定當目前的記錄檔達到大小上限時，是否要建立新的記錄檔。 設定為 **true** ，要求服務在記錄檔達到其大小上限時，建立新的檔案;否則 **為 false**。 只有當 [[**保留**](eventmanifestschema-retention-channelloggingtype-element.md)] 設定為 [ **true**] 時，才可以將 [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md)設定為 [ **true** ]。 預設值為 **false**。<br/> 服務可以建立的備份檔案數目沒有限制 (只有) 可用磁碟空間的限制。 備份檔案名稱的形式為 Archive-*channelName* - *timestamp*，而且位於% windir% \\ System32 \\ \system32\winevt\logs\application.evtx \\ Logs 資料夾中。<br/> |
| [**maxSize**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | 記錄檔的大小上限（以位元組為單位）。 預設的 (和最小) 值是 1 MB。 如果實體記錄檔大小小於設定的最大大小，且記錄檔中需要額外的空間來儲存事件，則即使記錄檔的實際大小將大於設定的最大值，服務仍會配置另一個空間區塊。 服務會配置 1 MB 的區塊，因此實體大小可成長到大於設定之大小上限的 1 MB。 <br/>                                                                                                                                                                                                                                                      |
| [**保留**](eventmanifestschema-retention-channelloggingtype-element.md)   | boolean                                                           | 判斷記錄檔是否為連續或迴圈的記錄檔。 針對連續記錄檔將設定為 **true** ，並將迴圈記錄檔設為 **false** 。 系統管理員和操作通道類型的預設值為 **false** ，而針對分析和 Debug 通道類型則為 **true** 。<br/> 若要查詢迴圈記錄檔，您必須先停用通道。<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>備註

您可以為任何通道類型指定 **maxSize** 屬性。

您只能針對系統管理員和操作通道類型指定 **autoBackup** 屬性。

您可以將 [ **保留** ] 屬性設定為 false (系統管理員和操作通道類型的迴圈記錄) 。 您可以將 [**保留**] 屬性設定為 false (分析和 Debug 通道類型的迴圈記錄) ，但若要在 Windows 事件檢視器中查看事件，您必須先停用通道。 請注意，當您再次啟用通道時，會從通道中移除事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 






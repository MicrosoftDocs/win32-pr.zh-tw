---
description: 這個類別是 IDE 通道事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: SystemConfig_IDEChannel 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8cf764d266d98199e27b40c8690b36183aa82aa2cfb8ded006087ab55f3ddfca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041598"
---
# <a name="systemconfig_idechannel-class"></a>SystemConfig \_ IDEChannel 類別

這個類別是 IDE 通道事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a>成員

**SystemConfig \_ IDEChannel** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ IDEChannel** 類別具有這些屬性。

<dl> <dt>

**DeviceTimingMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，格式 ( "x" ) 
</dt> </dl>

IDE 可以運作的模式。 以下是可能的值：

-   PIO \_ MODE0 (0x1) 
-   PIO \_ 模式 1 (0x2) 
-   PIO \_ MODE2 (0x4) 
-   PIO \_ MODE3 (0x8) 
-   PIO \_ MODE4 (0x10) 
-   SWDMA \_ MODE0 (0x20) 
-   SWDMA \_ 模式 1 (0x40) 
-   SWDMA \_ MODE2 (0x80) 
-   MWDMA \_ MODE0 (0x100) 
-   MWDMA \_ MODE2 (0x200) 
-   MWDMA \_ MODE3 (0x400) 
-   UDMA \_ MODE0 (0x800) 
-   UDMA \_ 模式 1 (0x1000) 
-   UDMA \_ MODE2 (0x2000) 
-   UDMA \_ MODE3 (0x4000) 
-   UDMA \_ MODE4 (0x8000) 
-   UDMA \_ MODE5 (0x10000) 

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，格式 ( "x" ) 
</dt> </dl>

裝置類型。 以下是可能的值：

-   ATA (1) 
-   ATAPI (2) 

</dd> <dt>

**LocationInformation**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

IDE 通道 (例如，主要通道、次要通道等) 。

</dd> <dt>

**LocationInformationLen**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

**LocationInformation** 字串的長度。

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 
</dt> </dl>

磁片的識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 





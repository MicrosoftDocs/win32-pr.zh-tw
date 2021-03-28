---
description: 此類別是電源設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: SystemConfig_V0_Power 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e42af68ad12857d65d776b7a73794d2d13b2b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972105"
---
# <a name="systemconfig_v0_power-class"></a>SystemConfig \_ V0 \_ Power 類別

此類別是電源設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a>成員

**SystemConfig \_ V0 \_ Power** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ V0 \_ Power** 類別具有這些屬性。

<dl> <dt>

Pad1
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 
</dt> </dl>

保留的。

</dd> <dt>

Pad2
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) 
</dt> </dl>

保留的。

</dd> <dt>

Pad3
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (8) 
</dt> </dl>

保留的。

</dd> <dt>

s1
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 
</dt> </dl>

True 表示系統支援睡眠狀態 S1。

</dd> <dt>

s2
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

True 表示系統支援睡眠狀態 S2。

</dd> <dt>

s3
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

True 表示系統支援睡眠狀態 S3。

</dd> <dt>

s4
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

True 表示系統支援睡眠狀態 S4。

</dd> <dt>

s5
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 
</dt> </dl>

True 表示系統支援睡眠狀態 S5。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 





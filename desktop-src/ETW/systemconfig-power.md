---
description: SystemConfig_Power 類別-此類別是電源設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7065b0b0-9a1d-4fce-a494-5762d5efb239
title: SystemConfig_Power 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Power
- SystemConfig_Power.s1
- SystemConfig_Power.s2
- SystemConfig_Power.s3
- SystemConfig_Power.s4
- SystemConfig_Power.s5
- SystemConfig_Power.Pad1
- SystemConfig_Power.Pad2
- SystemConfig_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7338faad8c313847ad7db7aaac5d4000abba5be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106066"
---
# <a name="systemconfig_power-class"></a>SystemConfig \_ Power 類別

此類別是電源設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_Power : SystemConfig
{
  uint8 s1;
  uint8 s2;
  uint8 s3;
  uint8 s4;
  uint8 s5;
  uint8 Pad1;
  uint8 Pad2;
  uint8 Pad3;
};
```

## <a name="members"></a>成員

**SystemConfig \_ Power** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ Power** 類別具有這些屬性。

<dl> <dt>

Pad1
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 
</dt> </dl>

未使用。

</dd> <dt>

Pad2
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) 
</dt> </dl>

未使用。

</dd> <dt>

Pad3
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (8) 
</dt> </dl>

未使用。

</dd> <dt>

s1
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 
</dt> </dl>

True 表示系統支援睡眠狀態 S1。

</dd> <dt>

s2
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

True 表示系統支援睡眠狀態 S2。

</dd> <dt>

s3
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

True 表示系統支援睡眠狀態 S3。

</dd> <dt>

s4
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

True 表示系統支援睡眠狀態 S4。

</dd> <dt>

s5
</dt> <dd> <dl> <dt>

資料類型： **uint8**
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 





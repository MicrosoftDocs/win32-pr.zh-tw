---
description: 此類別是 CPU 配置事件的事件種類類別。
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: SystemConfig_CPU 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: d08d0eeac9aa2287576bbb6dfe0e8ce41f116e8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973408"
---
# <a name="systemconfig_cpu-class"></a>SystemConfig \_ CPU 類別

此類別是 CPU 配置事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a>成員

**SystemConfig \_ CPU** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ CPU** 類別具有這些屬性。

<dl> <dt>

**AllocationGranularity**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (5) 
</dt> </dl>

配置給虛擬記憶體的資料細微性。

</dd> <dt>

**ComputerName**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (6) ， **最大** (256) ， **格式 ( "s" )**
</dt> </dl>

電腦的名稱。

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (7) ， **最大** (132) ， **格式 ( "s" )**
</dt> </dl>

電腦所屬之網域的名稱。

</dd> <dt>

**HyperThreadingFlag**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (8) ，指標
</dt> </dl>

表示處理器的超執行緒選項是開啟或關閉。 每個位會反映電腦上 CPU 的超執行緒狀態。

</dd> <dt>

**MemSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (3) 
</dt> </dl>

作業系統可用的實體記憶體總量。

</dd> <dt>

**MHz**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (1) 
</dt> </dl>

處理器的最大速度（以 mhz 為單位）。

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (2) 
</dt> </dl>

電腦上的處理器數目。

</dd> <dt>

**PageSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (4) 
</dt> </dl>

交換頁面的大小（以位元組為單位）。

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

 

 





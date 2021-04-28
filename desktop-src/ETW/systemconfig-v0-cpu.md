---
description: SystemConfig_V0_CPU 類別-此類別是 CPU 配置事件的事件種類類別。
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: SystemConfig_V0_CPU 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: de3b63def40cb6ead40f6f4c95625603cfc581ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105986"
---
# <a name="systemconfig_v0_cpu-class"></a>SystemConfig \_ V0 \_ CPU 類別

此類別是 CPU 配置事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a>成員

**SystemConfig \_ V0 \_ CPU** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ V0 \_ CPU** 類別具有這些屬性。

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

限定詞： **WmiDataId** (6) ， **最大** (256) 
</dt> </dl>

電腦的名稱。

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (7) ， **最大** (132) 
</dt> </dl>

電腦所屬之網域的名稱。

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
| 最低支援的用戶端<br/> | 都不支援<br/>                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 





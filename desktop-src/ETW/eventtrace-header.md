---
description: 記錄檔標頭事件的事件種類類別。 此類別包含事件追蹤會話的相關資訊。
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: EventTrace_Header 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: a5d0515b9d7d720409e0a72aec7aad5dc54561637563976a35d03b3e0dec79f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829988"
---
# <a name="eventtrace_header-class"></a>EventTrace \_ 標頭類別

記錄檔標頭事件的事件種類類別。 此類別包含事件追蹤會話的相關資訊。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a>成員

**EventTrace \_ 標頭** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**EventTrace \_ 標頭** 類別具有這些屬性。

<dl> <dt>

**BootTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (17) 
</dt> </dl>

系統啟動的時間，從1601年1月1日午夜起算的 100-毫微秒間隔。

</dd> <dt>

**BufferSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (1) 
</dt> </dl>

事件追蹤會話的緩衝區大小（以 kb 為單位）。

</dd> <dt>

**BuffersLost**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (21) 
</dt> </dl>

遺失的緩衝區總數。

</dd> <dt>

**BuffersWritten**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (9) 
</dt> </dl>

事件追蹤會話所寫入的緩衝區總數。

</dd> <dt>

**CPUSpeed**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (13) 
</dt> </dl>

CPU 速度（以 mhz 為單位）。

**Windows 2000：** 不支援。

</dd> <dt>

**EndTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (5) 
</dt> </dl>

事件追蹤會話停止的時間，從1601年1月1日午夜起算的 100-毫微秒間隔時間。 如果您正在使用事件，或從提供仍在記錄事件的記錄檔中，則此值可能是0。

</dd> <dt>

**EventsLost**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (12) 
</dt> </dl>

事件追蹤會話期間遺失的事件數。

</dd> <dt>

**LogFileMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (8) ， **格式 ( "x" )**
</dt> </dl>

事件追蹤會話目前的記錄模式。 如需值的清單，請參閱記錄模式常數。

</dd> <dt>

**LogFileName**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (15) ， **指標**
</dt> </dl>

包含事件的事件追蹤記錄檔名稱。

</dd> <dt>

**LoggerName**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (14) ， **指標**
</dt> </dl>

事件追蹤會話的名稱。

</dd> <dt>

**MaxFileSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (7) 
</dt> </dl>

記錄檔的大小上限（以 mb 為單位）。

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (4) 
</dt> </dl>

系統上的處理器數目。

</dd> <dt>

**PerfFreq**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (18) 
</dt> </dl>

高解析度效能計數器的頻率（如果有的話）。

</dd> <dt>

**PointerSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (11) 
</dt> </dl>

指標資料類型的大小（以位元組為單位）。

</dd> <dt>

**ProviderVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (3) 
</dt> </dl>

作業系統的組建編號。

</dd> <dt>

**ReservedFlags**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (20) 
</dt> </dl>

保留的。

</dd> <dt>

**StartBuffers**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (10) 
</dt> </dl>

保留的。

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (19) 
</dt> </dl>

事件追蹤會話開始的時間，從1601年1月1日午夜起算的 100-毫微秒間隔。

</dd> <dt>

**TimerResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (6) 
</dt> </dl>

硬體計時器的解析度（以100毫微秒為單位）。

</dd> <dt>

**TimeZoneInformation**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (16) 、 **延伸 ( "NoPrint" )**、 **最大** (176) 
</dt> </dl>

[**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)結構，其中包含 **BootTime**、 **EndTime** 和 **StartTime** 成員的時區。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (2) 
</dt> </dl>

作業系統的版本號碼。 從低序位位元組開始，前兩個位元組包含主要版本，接下來的兩個位元組包含次要版本，接下來的兩個位元組包含 service pack 的主要版本，而最後兩個位元組包含 service pack 次要版本。

</dd> </dl>

## <a name="remarks"></a>備註

一般來說，您會想要儲存下列屬性的值，以便稍後在處理記錄檔中的事件時使用。

-   **TimerResolution**-與 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **KernelTime** 和 **UserTime** 成員一起使用，以判斷一組指示的 CPU 成本。 如需詳細資訊，請參閱 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的備註一節。
-   **PointerSize**：對於包含 **指標** 辨識符號的屬性，請使用此值來判斷指標的大小。 請注意，這個值可能不正確。 例如，在64位的電腦上，32位應用程式將會記錄4位元組指標;不過，會話會將 **PointerSize** 設定為8。
-   **LogFileMode**：用來判斷此會話是否為私用記錄器會話。 有些屬性不包含私用記錄器會話的資料。 例如，[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **KernelTime** 和 **UserTime** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EventTraceEvent**](eventtraceevent.md)
</dt> <dt>

[**TRACE \_ LOGFILE \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 

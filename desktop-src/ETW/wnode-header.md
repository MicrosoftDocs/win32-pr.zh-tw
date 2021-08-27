---
description: WNODE \_ 標頭結構是事件 \_ 追蹤屬性結構的成員 \_ 。
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: 'WNODE_HEADER 結構 (Wmistr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: 93cecb900b0c62084a3b5ea4e4a7789575c20c27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480684"
---
# <a name="wnode_header-structure"></a>WNODE \_ 標頭結構

**WNODE \_ 標頭** 結構是 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的成員。

## <a name="syntax"></a>語法


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**BufferSize**
</dt> <dd>

事件追蹤會話屬性配置的記憶體大小總計（以位元組為單位）。 記憶體的大小必須包含 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構的空間，以及在記憶體中結構後面的會話名稱字串和記錄檔名稱字串。

</dd> <dt>

**ProviderId**
</dt> <dd>

保留供內部使用。

</dd> <dt>

**HistoricalCoNtext**
</dt> <dd>

在輸出時，事件追蹤會話的控制碼。

</dd> <dt>

**版本**
</dt> <dd>

保留供內部使用。

</dd> <dt>

**連結**
</dt> <dd>

保留供內部使用。

</dd> <dt>

**KernelHandle**
</dt> <dd>

保留供內部使用。

</dd> <dt>

**時間 戳**
</dt> <dd>

此結構中資訊的更新時間，自1601年1月1日午夜起的 100-毫微秒間隔時間。

</dd> <dt>

**Guid**
</dt> <dd>

您為會話定義的 GUID。

若為 NT Kernel 記錄器會話，請將這個成員設定為 **SystemTraceControlGuid**。

如果這個成員設定為 **SystemTraceControlGuid** 或 **GlobalLoggerGuid**，記錄器將會是系統記錄器。

若為私用記錄器會話，請將這個成員設定為您要為會話啟用的提供者 GUID。

如果您啟動不是核心記錄器或私用記錄器會話的會話，就不需要指定會話 GUID。 如果您未指定 GUID，ETW 會為您建立一個 GUID。 只有當您想要變更與特定會話相關聯的預設許可權時，才需要指定會話 GUID。 如需詳細資訊，請參閱 EventAccessControl 函數。

您無法以相同的會話 GUID 啟動多個會話。

**在 Windows Vista 之前：** 您可以使用相同的會話 GUID 來啟動一個以上的會話。

</dd> <dt>

**ClientContext**
</dt> <dd>

記錄每個事件的時間戳記時所要使用的時鐘解析。 預設值是 (QPC) 的 Query 效能計數器。

**在 Windows Vista 之前：** 預設值為系統時間。

**在 Windows 10 之前，版本1703：** 任何系統記錄器都不能同時使用2個以上的不同時鐘類型。

**從 Windows 10 開始，版本1703：** 已移除時鐘類型限制。 所有三種時鐘類型現在都可以由系統記錄器同時使用。

您可以指定下列其中一個值。




| 值 | 意義 | 
|-------|---------|
| <dl><dt>1</dt></dl> |  (QPC) 的 Query 效能計數器。 QPC 計數器會提供高解析度的時間戳記，而不會受到系統時鐘的調整影響。 事件中儲存的時間戳記相當於從 QueryPerformanceCounter API 傳回的值。 如需此時間戳記特性的詳細資訊，請參閱取得 <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">高解析度的時間戳記</a>。<br /> 如果您有高事件率，或取用者合併來自不同緩衝區的事件，則應該使用此解析。 在這些情況下，QPC 時間戳記的精確度和穩定性可讓您更精確地從不同的緩衝區排序事件。 不過，QPC 時間戳記並不會反映系統時鐘的更新，例如，如果系統時鐘因為與 NTP 伺服器同步處理而在追蹤進行中進行同步處理，則追蹤中的 QPC 時間戳記會繼續反映時間，就像未發生任何更新一樣。<br /> 若要判斷解決方式，請在取用事件時使用<a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>的<strong>PerfFreq</strong>成員。<br /> 若要將事件的時間戳記轉換為 100-ns 單位，請使用下列轉換公式： <br /> scaledTimestamp = eventRecord. EventHeader. QuadPart * 10000000.0/logfileHeader. PerfFreq<br /> 請注意，在較舊的電腦上，時間戳記可能不准確，因為由於硬體錯誤，計數器有時會向前跳過。<br /> | 
| <dl><dt>2</dt></dl> | 系統時間。 系統時間會提供時間戳記來追蹤系統時鐘的變更，例如，如果系統時鐘因為與 NTP 伺服器同步處理而在追蹤進行中進行同步處理，則追蹤中的系統時間戳記也會向前跳到符合系統時鐘的新設定。 <br /><ul><li>在 Windows 10 之前的系統上，儲存在事件中的時間戳記相當於 GetSystemTimeAsFileTime API 所傳回的值。</li><li>在 Windows 10 或更新版本上，儲存在事件中的時間戳記相當於 GetSystemTimePreciseAsFileTime API 所傳回的值。</li></ul>在 Windows 10 之前，此時間戳記的解決方式是系統時鐘滴答的解析度，如 TRACE_LOGFILE_HEADER 的 TimerResolution 成員所表示。 從 Windows 10 開始，這個時間戳記的解決方法是效能計數器解析度，如 TRACE_LOGFILE_HEADER 的 PerfFreq 成員所示。<br /> 若要將事件的時間戳記轉換為 100-ns 單位，請使用下列轉換公式： <br /> scaledTimestamp = eventRecord. EventHeader. QuadPart<br /> 請注意，在 Windows 10 之前，在執行作業系統的系統上捕捉到事件時，如果事件的數量很高，則系統時間的解析可能不夠好，無法判斷事件的順序。 在此情況下，一組事件將會有相同的時間戳記，但 ETW 傳遞事件的順序可能不正確。 從 Windows 10 開始，系統會以額外的精確度來捕捉時間戳記，但在捕捉追蹤時，系統時鐘已調整的情況下，可能仍會發生某些不穩定的情況。<br /> | 
| <dl><dt>3</dt></dl> | CPU 週期計數器。 CPU 計數器提供最高的解析時間戳記，而且是要抓取的最不耗用資源。 不過，CPU 計數器不可靠，不應該用於生產環境。 例如，在某些電腦上，計時器將會因為溫度和電源變更而變更頻率，除了在某些狀態下停止。<br /> 若要判斷解決方式，請在取用事件時使用<a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>的<strong>CpuSpeedInMHz</strong>成員。<br /> 如果您的硬體不支援此時鐘類型，ETW 會使用系統時間。<br /><strong>Windows Server 2003、Windows XP SP1 和 Windows xp：</strong>此值不受支援，它是在 Windows Server 2003 SP1 和 Windows XP SP2 中引進。<br /> | 




 

**Windows 2000：** 不支援 **ClientCoNtext** 成員。

</dd> <dt>

**旗標**
</dt> <dd>

必須包含 **WNODE \_ 旗標 \_ 追蹤 \_ GUID** ，以指出此結構包含事件追蹤資訊。

</dd> </dl>

## <a name="remarks"></a>備註

設定任何成員之前，請務必將此結構的記憶體初始化為零。

若要將 ETW 時間戳記轉換成 FILETIME，請使用下列程式：

<dl> 1. 針對每個要處理的會話或記錄檔 (也就是針對每個事件追蹤記錄檔 \_ \_) ，請檢查 ProcessTraceMode 欄位，以判斷是否 \_ \_ 已設定進程追蹤模式 \_ 原始 \_ 時間戳記旗標。 依預設，不會設定此旗標。 如果未設定此旗標，ETW 執行時間會在將事件記錄傳送至您的 EventRecordCallback 函式之前，自動將每個事件記錄的時間戳記轉換 \_ 成 FILETIME \_ ，因此不需要額外的處理。 只有在使用處理程式 \_ 追蹤 \_ 模式的 \_ 原始 \_ 時間戳記旗標設定來處理追蹤時，才應該使用下列步驟。  
2. 針對每個要處理的會話或記錄檔 (也就是針對每個事件追蹤記錄檔 \_ \_) ，請檢查 LogfileHeader ReservedFlags 欄位，以判斷記錄檔的時間戳記規模。 根據 ReservedFlags 的值，遵循下列其中一個步驟來決定要在其餘步驟中用於 timeStampScale 的值： <dl> a. If ReservedFlags = = 1 (QPC) ： DOUBLE timeStampScale = 10000000.0/logFile. LogfileHeader. PerfFreq;  
b. If ReservedFlags = = 2 (系統時間) ： DOUBLE timeStampScale = 1.0;  
請注意，對於使用系統時間的事件，其餘步驟是不必要的，因為事件已經以 FILETIME 單位提供時間戳記。 其餘步驟可以運作，但不是必要的，而且會引入較小的舍入錯誤。  
c. 如果 ReservedFlags = = 3 (CPU 週期計數器) ： DOUBLE timeStampScale = 10.0/logFile. LogfileHeader. CpuSpeedInMHz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                   |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                         |
| 標頭<br/>                   | <dl> <dt>Wmistr。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[*ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 

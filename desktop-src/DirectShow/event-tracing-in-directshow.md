---
description: DirectShow 中的事件追蹤
ms.assetid: e78c4514-25f4-441d-bfd0-6dac4f7567fd
title: DirectShow 中的事件追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c567d8a2e75d838570323d8ad6be04f11502c9c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972757"
---
# <a name="event-tracing-in-directshow"></a>DirectShow 中的事件追蹤

DirectShow 支援 Windows (ETW) 的事件追蹤，可用來建立用於檢測或偵錯工具的事件記錄檔。 如需 ETW 的詳細資訊，請參閱 Windows SDK 檔。 若要在 DirectShow 應用程式中使用 ETW 事件，您必須啟用追蹤，然後處理追蹤事件。 使用下列步驟。

**設定必要的登錄機碼**

若要在使用者的電腦上啟用追蹤，請先設定下列登錄機碼：


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DirectX
    GlitchInstrumentation = 0x00000001 (REG_DWORD)
HKEY_LOCAL_MACHINE\SOFTWARE\DEBUG\Quartz.dll
    PERFLOG = 0x00000001 (REG_DWORD) 
```



這些金鑰適用于發行和調試二進位檔。

**在您的應用程式中啟用追蹤**

若要在您的應用程式中啟用追蹤，請執行下列步驟：

1.  呼叫 **StartTrace** 以啟動新的追蹤會話。
2.  呼叫 **EnableTrace** 以啟用追蹤。 適用于 DirectShow 的提供者 GUID 是 GUID \_ DSHOW \_ CTL。
3.  在應用程式結束之前，呼叫 **StopTrace** 以關閉追蹤會話。

**處理事件**

若要處理事件，請執行下列步驟：

1.  呼叫 **OpenTrace** 以開啟追蹤進行處理。
2.  呼叫 **ProcessTrace** 來處理事件。
3.  在 **ProcessTrace** 回呼中，使用事件 GUID 來尋找事件種類。 事件 GUID 表示用於事件資料的結構。 請參閱 [追蹤事件 guid](trace-guids.md)。
4.  呼叫 **CloseTrace** 以關閉追蹤控制碼。

**範例程式碼**

下列程式碼顯示可啟用追蹤的 helper 類別。 這段程式碼示範如何將事件寫入記錄檔，該檔案可以在會話完成之後處理。 您也可以即時處理事件。 如需詳細資訊，請參閱 Windows SDK 中的 ETW 檔。


```C++
#include <wmistr.h>
#include <evntrace.h>
#include <perfstruct.h>

// Event classes. These are defined in dxmperf.h.
#ifndef DXMPERF_VIDEOREND
#define DXMPERF_VIDEOREND   0x00000001
#endif

#ifndef AUDIOBREAK_BIT
#define AUDIOBREAK_BIT      0x00000010
#endif

// This structure extends the EVENT_TRACE_PROPERTIES by adding fields
// for the name of the WMI session name and the log file.
struct PERFMON_LOGGERINFO
{
    EVENT_TRACE_PROPERTIES TraceProperties;
    WCHAR wcSessionName[ MAX_PATH ];    // Session name.
    WCHAR wcLogFileName[ MAX_PATH ];    // Log file.
};

// Helper class for DirectShow event tracing.
class CTrace
{
public:
    CTrace() : m_SessionLogger((TRACEHANDLE) INVALID_HANDLE_VALUE)
    {
        ZeroMemory(&m_LogInfo, sizeof(&m_LogInfo));
    }

    // Start: Starts a trace session.
    HRESULT Start(WCHAR *wszLogFile)
    {
        const WCHAR* wszSessionName = L"PerfMon_DirectShow"; 
        HRESULT hr = S_OK;
        ULONG result; 

        ZeroMemory(&m_LogInfo, sizeof(m_LogInfo));
        
        EVENT_TRACE_PROPERTIES& prop = m_LogInfo.TraceProperties;

        prop.Wnode.BufferSize = sizeof(m_LogInfo);  // Size of the structure.
        prop.Wnode.Flags = WNODE_FLAG_TRACED_GUID;  // Must be this value.

        // Use the QPC (high resolution timer).
        prop.Wnode.ClientContext = 1;        

        prop.Wnode.Guid = GUID_DSHOW_CTL;           // Event provider GUID.
        prop.LogFileMode = 
            EVENT_TRACE_FILE_MODE_CIRCULAR | EVENT_TRACE_USE_PAGED_MEMORY; 
        prop.EnableFlags = 
            EVENT_TRACE_FLAG_PROCESS;   // Process events.

        // Set the offset from the start of the structure to the log file name.
        prop.LogFileNameOffset = 
            sizeof(m_LogInfo.TraceProperties) + sizeof(m_LogInfo.wcSessionName);  

        // Set the offset from the start of the structure to the session name.
        prop.LoggerNameOffset = sizeof(m_LogInfo.TraceProperties); 

        // Copy the names into the structure.
        StringCchCopy(m_LogInfo.wcSessionName, MAX_PATH, wszSessionName);
        StringCchCopy(m_LogInfo.wcLogFileName, MAX_PATH, wszLogFile);

        // Start the trace.
        result = StartTrace(
            &m_SessionLogger, 
            m_LogInfo.wcSessionName, 
            &m_LogInfo.TraceProperties
            );

        if (result == ERROR_SUCCESS)
        {
            result = EnableTrace(
                TRUE,                                   // Enable.
                AUDIOBREAK_BIT | DXMPERF_VIDEOREND,     // Event classes.
                TRACE_LEVEL_VERBOSE,                    // Trace level.
                &GUID_DSHOW_CTL,                        // Event provider.
                m_SessionLogger                         // Session handle.
                );
        }
        if (result != ERROR_SUCCESS)
        { 
            hr = __HRESULT_FROM_WIN32(result);
        }
        return hr;
    }

    HRESULT Stop()
    {
        HRESULT hr = S_OK;

        // Stop the trace.
        if (m_SessionLogger != (TRACEHANDLE)INVALID_HANDLE_VALUE)
        {
            LONG result = 0;

            result = EnableTrace(FALSE, 0, 0, &GUID_DSHOW_CTL, m_SessionLogger);
            if (result == ERROR_SUCCESS)
            {
                result = StopTrace(
                    m_SessionLogger, 
                    m_LogInfo.wcSessionName, 
                    &m_LogInfo.TraceProperties);
            }

            m_SessionLogger = (TRACEHANDLE)INVALID_HANDLE_VALUE;
            if (result != ERROR_SUCCESS)
            { 
                hr = __HRESULT_FROM_WIN32(result);
            }
        }
        return hr;
    }

protected:
    TRACEHANDLE         m_SessionLogger;
    PERFMON_LOGGERINFO  m_LogInfo;
};
```



下列程式碼顯示如何處理事件記錄檔：


```C++
// Callback for event processing.
VOID WINAPI EventCallback(PEVENT_TRACE pEvent)
{
    PERFINFO_DSHOW_STREAMTRACE  *pStreamTrace = NULL;
    PERFINFO_DSHOW_AVREND       *pVideoRender = NULL;
    PERFINFO_DSHOW_AUDIOBREAK   *pAudioBreak = NULL;

    if (pEvent->Header.Guid == GUID_STREAMTRACE) 
    {
        pStreamTrace = (PPERFINFO_DSHOW_STREAMTRACE)pEvent->MofData;

        switch (pStreamTrace->id)
        {
            // TODO: Handle the event.
        }
    }
    else if(pEvent->Header.Guid == GUID_VIDEOREND)
    {      
        pVideoRender = (PPERFINFO_DSHOW_AVREND)pEvent->MofData;
        // TODO: Handle the event.
    }
    else if(pEvent->Header.Guid == GUID_AUDIOBREAK)
    {
        pAudioBreak = (PPERFINFO_DSHOW_AUDIOBREAK)pEvent->MofData;
        // TODO: Handle the event.
    }
}

void ProcessTraceEvents(WCHAR *wszLogFile)
{
    ULONG result = 0;        
    EVENT_TRACE_LOGFILE logfile;

    ZeroMemory(&logfile, sizeof(logfile));
    logfile.LogFileName = wszLogFile;
    logfile.EventCallback  = EventCallback;   

    TRACEHANDLE handle = OpenTrace(&logfile);
    if (handle != (TRACEHANDLE)INVALID_HANDLE_VALUE)
    {
        result = ProcessTrace(&handle, 1, NULL, NULL);
        CloseTrace(handle);
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中進行調試](debugging-in-directshow.md)
</dt> </dl>

 

 




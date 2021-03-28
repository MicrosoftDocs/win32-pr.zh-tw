---
description: 在您可以將事件寫入追蹤會話之前，您必須先註冊您的提供者。
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: 撰寫 MOF (傳統) 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3d041e2792540d4a05637bcffdb67e1164a95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973825"
---
# <a name="writing-mof-classic-events"></a>撰寫 MOF (傳統) 事件

在您可以將事件寫入追蹤會話之前，您必須先註冊您的提供者。 註冊提供者會告知 ETW 您的提供者已準備好將事件寫入追蹤會話。 進程最多可註冊1024提供者 Guid;不過，您應該將進程註冊的提供者數目限制為一或兩個。

**在 Windows Vista 之前：** 進程可註冊的提供者數目沒有任何限制。

若要註冊傳統提供者，請呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函數。 此函式會註冊提供者的 GUID、事件追蹤類別 Guid，並識別當控制器啟用或停用提供者時 ETW 呼叫的回呼。

如果提供者呼叫 [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent)函式來記錄事件，您就不需要包含類別 guid 的陣列 (在呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)函式時，可以是 **Null**) 。 如果提供者呼叫 [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) 函數來記錄事件，您只需要包含陣列。

**WINDOWS XP 和 windows 2000：** 您一律需要包含類別 Guid 的陣列 (不能是 **Null**) 。

在提供者註冊本身並由控制器啟用之後，提供者就可以將事件記錄到控制器的追蹤會話。

在提供者結束之前，呼叫 [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) 函式以從 ETW 移除提供者的註冊。 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)函式會傳回您傳遞給 **UnregisterTraceGuids** 函數的註冊控制碼。

如果您的提供者只將事件記錄到全域記錄器會話，您就不需要向 ETW 註冊您的提供者，因為全域記錄器控制器不會啟用或停用提供者。 如需詳細資訊，請參閱設定 [和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)。

所有 [傳統](about-event-tracing.md) 提供者 (除了追蹤全域記錄器會話) 的事件之外，也必須執行 [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) 函式。 提供者會使用回呼中的資訊來判斷它是否已啟用或停用，以及應寫入的事件。

提供者會在呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函式來註冊本身時，指定回呼函式的名稱。 當控制器呼叫 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函數來啟用或停用提供者時，ETW 會呼叫回呼函式。

在您的 [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) 執行中，您必須呼叫 [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) 函數來取出會話控制碼;呼叫 [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函式時，您會使用會話控制碼。 如果您的提供者使用啟用層級或啟用旗標，您只需要在 **ControlCallback** 執行中呼叫 [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags)函式或 [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel)函數。

提供者只能將追蹤事件記錄到一個會話，但是沒有任何專案可以防止多個控制器啟用單一提供者。 為了防止另一個控制器將追蹤事件重新導向至其會話，您可能會想要將邏輯加入至 [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) 執行以比較會話控制碼，並忽略其他控制器的啟用要求。

若要記錄事件， [傳統](about-event-tracing.md) 提供者會呼叫 [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函數。 事件是由 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) 結構以及附加至標頭的任何事件特定資料所組成。

標頭必須包含下列資訊：

-   **大小** 成員必須包含要針對事件記錄的總位元組數 (包括 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的大小，以及附加至標頭) 的任何事件特定資料。
-   **Guid** 成員必須包含事件 (的類別 guid，否則 **GuidPtr** 成員必須包含) 類別 guid 的指標。

    **WINDOWS XP 和 windows 2000：** 類別 GUID 先前必須使用 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函式註冊。

-   **旗標** 成員必須包含 **WNODE \_ 旗標 \_ 追蹤 \_ GUID** 旗標。 如果您使用 **GuidPtr** 成員指定類別 GUID，也請新增 **WNODE 旗標 \_ \_ 使用 \_ GUID \_ PTR** 旗標。
-   如果您使用 MOF 來發佈事件資料的版面配置，則 **類別** 成員必須包含事件種類。
-   如果您使用 MOF 來發佈事件資料的配置，則 **類別版本** 成員必須包含事件版本。 版本是用來區別修訂至事件資料。 將初始版本號碼設定為0。

如果您同時撰寫提供者和取用者，您可以使用結構來填入附加至標頭的事件特定資料。 但是，如果您使用 MOF 來發佈事件特定資料，讓任何取用者都可以處理事件，您就不應該使用結構將事件特定資料附加到標頭。 這是因為編譯器可能會針對位元組對齊目的，在事件特定的資料中新增額外的位元組。 因為 MOF 定義不會考慮額外的位元組，所以取用者可能會取出不正確資料。

您應配置事件的記憶體區塊，並將每個事件資料項目複製到記憶體，或建立包含 [**mof \_ 欄位**](/windows/win32/api/evntrace/ns-evntrace-mof_field) 結構陣列的結構; 大部分的應用程式會建立一個結構，其中包含 **mof \_ 欄位** 結構的陣列。 請確定 **標頭大小** 反映實際在記錄事件之前設定的 **MOF \_ 欄位** 結構的實際數目。 例如，如果事件包含三個資料欄位，請將 **標頭. 大小** 設定為 SIZEOF (事件 \_ 追蹤 \_ 標頭) + (sizeof (MOF \_ 欄位) \* 3) 。

如需追蹤相關事件的詳細資訊，請參閱 [在端對端案例中撰寫相關事件](writing-related-events-in-an-end-to-end-scenario.md)。

下列範例顯示如何呼叫 [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函式來記錄事件。 此範例會參考 [針對傳統提供者發行您的事件架構](publishing-your-event-schema-for-a-classic-provider.md)時所定義的事件。


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

// GUID that identifies the category of events that the provider can log. 
// The GUID is also used in the event MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {B49D5931-AD85-4070-B1B1-3F81F1532875}
static const GUID MyCategoryGuid = 
{ 0xb49d5931, 0xad85, 0x4070, { 0xb1, 0xb1, 0x3f, 0x81, 0xf1, 0x53, 0x28, 0x75 } };

// GUID that identifies the provider that you are registering.
// The GUID is also used in the provider MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };

// Identifies the event type within the MyCategoryGuid category 
// of events to be logged. This is the same value as the EventType 
// qualifier that is defined in the event type MOF class for one of 
// the MyCategoryGuid category of events.

#define MY_EVENT_TYPE 1

// Event passed to TraceEvent

typedef struct _event
{
    EVENT_TRACE_HEADER Header;
    MOF_FIELD Data[MAX_MOF_FIELDS];  // Event-specific data
} MY_EVENT, *PMY_EVENT;

#define MAX_INDICES            3
#define MAX_SIGNATURE_LEN      32
#define EVENT_DATA_FIELDS_CNT  6

// Application data to be traced for Version 1 of the MOF class.

typedef struct _evtdata
{
    LONG Cost;
    DWORD Indices[MAX_INDICES];
    WCHAR Signature[MAX_SIGNATURE_LEN];
    BOOL IsComplete;
    GUID ID;
    DWORD Size;
}EVENT_DATA, *PEVENT_DATA;

// GUID used as the value for EVENT_DATA.ID.

// {25BAEDA9-C81A-4889-8764-184FE56750F2}
static const GUID tempID = 
{ 0x25baeda9, 0xc81a, 0x4889, { 0x87, 0x64, 0x18, 0x4f, 0xe5, 0x67, 0x50, 0xf2 } };

// Global variables to store tracing state information.

TRACEHANDLE g_SessionHandle = 0; // The handle to the session that enabled the provider.
ULONG g_EnableFlags = 0; // Determines which class of events to log.
UCHAR g_EnableLevel = 0; // Determines the severity of events to log.
BOOL g_TraceOn = FALSE;  // Used by the provider to determine whether it should log events.

ULONG WINAPI ControlCallback(WMIDPREQUESTCODE RequestCode, PVOID Context, ULONG* Reserved, PVOID Header);

// For this example to log the event, run the session example
// to enable the provider before running this example.

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_DATA EventData;
    MY_EVENT MyEvent; 
    TRACEHANDLE RegistrationHandle = 0; 
    TRACE_GUID_REGISTRATION EventClassGuids[] = {
        (LPGUID)&MyCategoryGuid, NULL
        };

    // Register the provider and specify the control callback function
    // that receives the enable/disable notifications.

    status = RegisterTraceGuids(
        (WMIDPREQUEST)ControlCallback,
        NULL,
        (LPGUID)&ProviderGuid,
        sizeof(EventClassGuids)/sizeof(TRACE_GUID_REGISTRATION),
        EventClassGuids,
        NULL,
        NULL,
        &RegistrationHandle
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegisterTraceGuids failed with %lu\n", status);
        goto cleanup;
    }

    // Set the event-specific data.

    EventData.Cost = 32;
    EventData.ID = tempID;
    EventData.Indices[0] = 4;
    EventData.Indices[1] = 5;
    EventData.Indices[2] = 6;
    EventData.IsComplete = TRUE;
    wcscpy_s(EventData.Signature, MAX_SIGNATURE_LEN, L"Signature");
    EventData.Size = 1024;

    // Log the event if the provider is enabled and the session
    // passed a severity level value >= TRACE_LEVEL_ERROR (or zero).
    // If your provider generates more than one class of events, you
    // would also need to check g_EnableFlags.

    if (g_TraceOn && (0 == g_EnableLevel || TRACE_LEVEL_ERROR <= g_EnableLevel))
    {
        // Initialize the event data structure.

        ZeroMemory(&MyEvent, sizeof(MY_EVENT));
        MyEvent.Header.Size = sizeof(EVENT_TRACE_HEADER) + (sizeof(MOF_FIELD) * EVENT_DATA_FIELDS_CNT);
        MyEvent.Header.Flags = WNODE_FLAG_TRACED_GUID | WNODE_FLAG_USE_MOF_PTR;
        MyEvent.Header.Guid = MyCategoryGuid;
        MyEvent.Header.Class.Type = MY_EVENT_TYPE;
        MyEvent.Header.Class.Version = 1;
        MyEvent.Header.Class.Level = g_EnableLevel;

        // Load the event data. You can also use the DEFINE_TRACE_MOF_FIELD
        // macro defined in evntrace.h to set the MOF_FIELD members. For example,
        // DEFINE_TRACE_MOF_FIELD(&EventData.Data[0], &EventData.Cost, sizeof(EventData.Cost), 0);

        MyEvent.Data[0].DataPtr = (ULONG64) &(EventData.Cost);
        MyEvent.Data[0].Length = sizeof(EventData.Cost);
        MyEvent.Data[1].DataPtr = (ULONG64) &(EventData.Indices);
        MyEvent.Data[1].Length = sizeof(EventData.Indices);
        MyEvent.Data[2].DataPtr = (ULONG64) &(EventData.Signature);
        MyEvent.Data[2].Length = (ULONG)(wcslen(EventData.Signature) + 1) * sizeof(WCHAR);
        MyEvent.Data[3].DataPtr = (ULONG64) &(EventData.IsComplete);
        MyEvent.Data[3].Length = sizeof(EventData.IsComplete);
        MyEvent.Data[4].DataPtr = (ULONG64) &(EventData.ID);
        MyEvent.Data[4].Length = sizeof(EventData.ID);
        MyEvent.Data[5].DataPtr = (ULONG64) &(EventData.Size);
        MyEvent.Data[5].Length = sizeof(EventData.Size);

        // Write the event.

        status = TraceEvent(g_SessionHandle, &(MyEvent.Header));

        if (ERROR_SUCCESS != status)
        {
            // Decide how you want to handle failures. Typically, you do not
            // want to terminate the application because you failed to
            // log an event. If the error is a memory failure, you may
            // may want to log a message to the system event log or turn
            // off logging.

            wprintf(L"TraceEvent() event failed with %lu\n", status);
            g_TraceOn = FALSE;
        }
    }

cleanup:

    if (RegistrationHandle)
    {
        UnregisterTraceGuids(RegistrationHandle);
    }
}


// The callback function that receives enable/disable notifications
// from one or more ETW sessions. Because more than one session
// can enable the provider, this example ignores requests from other 
// sessions if it is already enabled.

ULONG WINAPI ControlCallback(
    WMIDPREQUESTCODE RequestCode,
    PVOID Context,
    ULONG* Reserved, 
    PVOID Header
    )
{
    UNREFERENCED_PARAMETER(Context);
    UNREFERENCED_PARAMETER(Reserved);

    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE TempSessionHandle = 0; 

    switch (RequestCode)
    {
        case WMI_ENABLE_EVENTS:  // Enable the provider.
        {
            SetLastError(0);

            // If the provider is already enabled to a provider, ignore 
            // the request. Get the session handle of the enabling session.
            // You need the session handle to call the TraceEvent function.
            // The session could be enabling the provider or it could be
            // updating the level and enable flags.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (0 == g_SessionHandle)
            {
                g_SessionHandle = TempSessionHandle;
            }
            else if (g_SessionHandle != TempSessionHandle)
            {
                break;
            }

            // Get the severity level of the events that the
            // session wants you to log.

            g_EnableLevel = GetTraceEnableLevel(g_SessionHandle); 
            if (0 == g_EnableLevel)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable level means to your provider.
                    // For this example, it means log all events.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableLevel failed with, %lu.\n", status);
                    break;
                } 
            }

            // Get the enable flags that indicate the events that the
            // session wants you to log. The provider determines the
            // flags values. How it articulates the flag values and 
            // meanings to perspective sessions is up to it.

            g_EnableFlags = GetTraceEnableFlags(g_SessionHandle);
            if (0 == g_EnableFlags)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable flags value means to your provider.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableFlags failed with, %lu.\n", status);
                    break;
                }
            }

            g_TraceOn = TRUE;
            break;
        }
 
        case WMI_DISABLE_EVENTS:  // Disable the provider.
        {
            // Disable the provider only if the request is coming from the
            // session that enabled the provider.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (g_SessionHandle == TempSessionHandle)
            {
                g_TraceOn = FALSE;
                g_SessionHandle = 0;
            }
            break;
        }

        default:
        {
            status = ERROR_INVALID_PARAMETER;
            break;
        }
    }

    return status;
}
```



 

 

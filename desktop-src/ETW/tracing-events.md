---
description: 瞭解如何將 MOF 事件寫入追蹤會話。 開始註冊您的提供者，讓它準備好將事件寫入追蹤會話。
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: 撰寫 MOF (傳統) 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d081c48567851d2fb570dd7bfa5c75e687b524
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112261840"
---
# <a name="writing-mof-classic-events"></a><span data-ttu-id="5ede2-104">撰寫 MOF (傳統) 事件</span><span class="sxs-lookup"><span data-stu-id="5ede2-104">Writing MOF (Classic) Events</span></span>

<span data-ttu-id="5ede2-105">在您可以將事件寫入追蹤會話之前，您必須先註冊您的提供者。</span><span class="sxs-lookup"><span data-stu-id="5ede2-105">Before you can write events to a trace session, you must register your provider.</span></span> <span data-ttu-id="5ede2-106">註冊提供者會告知 ETW 您的提供者已準備好將事件寫入追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="5ede2-106">Registering a provider tells ETW that your provider is ready to write events to a trace session.</span></span> <span data-ttu-id="5ede2-107">進程最多可註冊1024提供者 Guid;不過，您應該將進程註冊的提供者數目限制為一或兩個。</span><span class="sxs-lookup"><span data-stu-id="5ede2-107">A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that your process registers to one or two.</span></span>

<span data-ttu-id="5ede2-108">**在 Windows Vista 之前：** 進程可註冊的提供者數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="5ede2-108">**Prior to Windows Vista:** There is no limit to the number of providers that a process can register.</span></span>

<span data-ttu-id="5ede2-109">若要註冊傳統提供者，請呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函數。</span><span class="sxs-lookup"><span data-stu-id="5ede2-109">To register a classic provider, call the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="5ede2-110">此函式會註冊提供者的 GUID、事件追蹤類別 Guid，並識別當控制器啟用或停用提供者時 ETW 呼叫的回呼。</span><span class="sxs-lookup"><span data-stu-id="5ede2-110">The function registers the provider's GUID, event trace class GUIDs, and identifies the callback that ETW calls when a controller enables or disables the provider.</span></span>

<span data-ttu-id="5ede2-111">如果提供者呼叫 [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent)函式來記錄事件，您就不需要包含類別 guid 的陣列 (在呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)函式時，可以是 **Null**) 。</span><span class="sxs-lookup"><span data-stu-id="5ede2-111">If the provider calls the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events, you do not need to include the array of class GUIDs (can be **NULL**) when calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="5ede2-112">如果提供者呼叫 [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) 函數來記錄事件，您只需要包含陣列。</span><span class="sxs-lookup"><span data-stu-id="5ede2-112">You only need to include the array if the provider calls the [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) function to log events.</span></span>

<span data-ttu-id="5ede2-113">**WINDOWS XP 和 windows 2000：** 您一律需要包含類別 Guid 的陣列 (不能是 **Null**) 。</span><span class="sxs-lookup"><span data-stu-id="5ede2-113">**Windows XP and Windows 2000:** You always need to include the array of class GUIDs (cannot be **NULL**).</span></span>

<span data-ttu-id="5ede2-114">在提供者註冊本身並由控制器啟用之後，提供者就可以將事件記錄到控制器的追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="5ede2-114">After a provider registers itself and is enabled by the controller, the provider can log events to the controller's trace session.</span></span>

<span data-ttu-id="5ede2-115">在提供者結束之前，呼叫 [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) 函式以從 ETW 移除提供者的註冊。</span><span class="sxs-lookup"><span data-stu-id="5ede2-115">Before the provider exits, call the [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) function to remove the provider's registration from ETW.</span></span> <span data-ttu-id="5ede2-116">[**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)函式會傳回您傳遞給 **UnregisterTraceGuids** 函數的註冊控制碼。</span><span class="sxs-lookup"><span data-stu-id="5ede2-116">The [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function returns the registration handle that you pass to the **UnregisterTraceGuids** function.</span></span>

<span data-ttu-id="5ede2-117">如果您的提供者只將事件記錄到全域記錄器會話，您就不需要向 ETW 註冊您的提供者，因為全域記錄器控制器不會啟用或停用提供者。</span><span class="sxs-lookup"><span data-stu-id="5ede2-117">If your provider logs events to the Global Logger session only, you do not have to register your provider with ETW because the Global Logger controller does not enable or disable providers.</span></span> <span data-ttu-id="5ede2-118">如需詳細資訊，請參閱設定 [和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="5ede2-118">For details, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="5ede2-119">所有 [傳統](about-event-tracing.md) 提供者 (除了追蹤全域記錄器會話) 的事件之外，也必須執行 [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) 函式。</span><span class="sxs-lookup"><span data-stu-id="5ede2-119">All [classic](about-event-tracing.md) providers (except those that trace events to the Global Logger session) must implement the [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) function.</span></span> <span data-ttu-id="5ede2-120">提供者會使用回呼中的資訊來判斷它是否已啟用或停用，以及應寫入的事件。</span><span class="sxs-lookup"><span data-stu-id="5ede2-120">The provider uses the information in the callback to determine if it is enabled or disabled and which events it should write.</span></span>

<span data-ttu-id="5ede2-121">提供者會在呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函式來註冊本身時，指定回呼函式的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ede2-121">The provider specifies the name of the callback function when it calls the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register itself.</span></span> <span data-ttu-id="5ede2-122">當控制器呼叫 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函數來啟用或停用提供者時，ETW 會呼叫回呼函式。</span><span class="sxs-lookup"><span data-stu-id="5ede2-122">ETW calls the callback function when the controller calls the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable or disable the provider.</span></span>

<span data-ttu-id="5ede2-123">在您的 [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) 執行中，您必須呼叫 [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) 函數來取出會話控制碼;呼叫 [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函式時，您會使用會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="5ede2-123">In your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation, you must call the [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) function to retrieve the session handle; you use the session handle when calling the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="5ede2-124">如果您的提供者使用啟用層級或啟用旗標，您只需要在 **ControlCallback** 執行中呼叫 [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags)函式或 [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel)函數。</span><span class="sxs-lookup"><span data-stu-id="5ede2-124">You only need to call the [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) function or the [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) function in your **ControlCallback** implementation if your provider uses the enable level or enable flags.</span></span>

<span data-ttu-id="5ede2-125">提供者只能將追蹤事件記錄到一個會話，但是沒有任何專案可以防止多個控制器啟用單一提供者。</span><span class="sxs-lookup"><span data-stu-id="5ede2-125">A provider can log trace events to only one session, but there is nothing to prevent multiple controllers from enabling a single provider.</span></span> <span data-ttu-id="5ede2-126">為了防止另一個控制器將追蹤事件重新導向至其會話，您可能會想要將邏輯加入至 [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) 執行以比較會話控制碼，並忽略其他控制器的啟用要求。</span><span class="sxs-lookup"><span data-stu-id="5ede2-126">To prevent another controller from redirecting your trace events to its session, you may want to add logic to your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation to compare session handles and ignore enable requests from other controllers.</span></span>

<span data-ttu-id="5ede2-127">若要記錄事件， [傳統](about-event-tracing.md) 提供者會呼叫 [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函數。</span><span class="sxs-lookup"><span data-stu-id="5ede2-127">To log events, [classic](about-event-tracing.md) providers call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="5ede2-128">事件是由 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) 結構以及附加至標頭的任何事件特定資料所組成。</span><span class="sxs-lookup"><span data-stu-id="5ede2-128">An event consists of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and any event-specific data that is appended to the header.</span></span>

<span data-ttu-id="5ede2-129">標頭必須包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="5ede2-129">The header must contain the following information:</span></span>

-   <span data-ttu-id="5ede2-130">**大小** 成員必須包含要針對事件記錄的總位元組數 (包括 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的大小，以及附加至標頭) 的任何事件特定資料。</span><span class="sxs-lookup"><span data-stu-id="5ede2-130">The **Size** member must contain the total number of bytes to be recorded for the event (including the size of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and of any event-specific data that is appended to the header).</span></span>
-   <span data-ttu-id="5ede2-131">**Guid** 成員必須包含事件 (的類別 guid，否則 **GuidPtr** 成員必須包含) 類別 guid 的指標。</span><span class="sxs-lookup"><span data-stu-id="5ede2-131">The **Guid** member must contain the class GUID of the event (or the **GuidPtr** member must contain a pointer to the class GUID).</span></span>

    <span data-ttu-id="5ede2-132">**WINDOWS XP 和 windows 2000：** 類別 GUID 先前必須使用 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函式註冊。</span><span class="sxs-lookup"><span data-stu-id="5ede2-132">**Windows XP and Windows 2000:** The class GUID must have been registered previously using the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span>

-   <span data-ttu-id="5ede2-133">**旗標** 成員必須包含 **WNODE \_ 旗標 \_ 追蹤 \_ GUID** 旗標。</span><span class="sxs-lookup"><span data-stu-id="5ede2-133">The **Flags** member must contain the **WNODE\_FLAG\_TRACED\_GUID** flag.</span></span> <span data-ttu-id="5ede2-134">如果您使用 **GuidPtr** 成員指定類別 GUID，也請新增 **WNODE 旗標 \_ \_ 使用 \_ GUID \_ PTR** 旗標。</span><span class="sxs-lookup"><span data-stu-id="5ede2-134">If you specify the class GUID using the **GuidPtr** member, also add the **WNODE\_FLAG\_USE\_GUID\_PTR** flag.</span></span>
-   <span data-ttu-id="5ede2-135">如果您使用 MOF 來發佈事件資料的版面配置，則 **類別** 成員必須包含事件種類。</span><span class="sxs-lookup"><span data-stu-id="5ede2-135">The **Class.Type** member must contain the event type, if you use MOF to publish the layout of your event data.</span></span>
-   <span data-ttu-id="5ede2-136">如果您使用 MOF 來發佈事件資料的配置，則 **類別版本** 成員必須包含事件版本。</span><span class="sxs-lookup"><span data-stu-id="5ede2-136">The **Class.Version** member must contain the event version, if you use MOF to publish the layout of your event data.</span></span> <span data-ttu-id="5ede2-137">版本是用來區別修訂至事件資料。</span><span class="sxs-lookup"><span data-stu-id="5ede2-137">The version is used to distinguish between revisions to the event data.</span></span> <span data-ttu-id="5ede2-138">將初始版本號碼設定為0。</span><span class="sxs-lookup"><span data-stu-id="5ede2-138">Set the initial version number to 0.</span></span>

<span data-ttu-id="5ede2-139">如果您同時撰寫提供者和取用者，您可以使用結構來填入附加至標頭的事件特定資料。</span><span class="sxs-lookup"><span data-stu-id="5ede2-139">If you write both the provider and the consumer, you can use a structure to populate the event-specific data that is appended to the header.</span></span> <span data-ttu-id="5ede2-140">但是，如果您使用 MOF 來發佈事件特定資料，讓任何取用者都可以處理事件，您就不應該使用結構將事件特定資料附加到標頭。</span><span class="sxs-lookup"><span data-stu-id="5ede2-140">However, if you use MOF to publish the event-specific data so that any consumer can process the event, you should not use a structure to append the event-specific data to the header.</span></span> <span data-ttu-id="5ede2-141">這是因為編譯器可能會針對位元組對齊目的，在事件特定的資料中新增額外的位元組。</span><span class="sxs-lookup"><span data-stu-id="5ede2-141">This is because the compiler may add extra bytes to the event-specific data for byte alignment purposes.</span></span> <span data-ttu-id="5ede2-142">因為 MOF 定義不會考慮額外的位元組，所以取用者可能會取出不正確資料。</span><span class="sxs-lookup"><span data-stu-id="5ede2-142">Because the MOF definition does not account for the extra bytes, the consumer may retrieve data that is not valid.</span></span>

<span data-ttu-id="5ede2-143">您應配置事件的記憶體區塊，並將每個事件資料項目複製到記憶體，或建立包含 [**mof \_ 欄位**](/windows/win32/api/evntrace/ns-evntrace-mof_field) 結構陣列的結構; 大部分的應用程式會建立一個結構，其中包含 **mof \_ 欄位** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="5ede2-143">You should either allocate a block of memory for the event and copy each event data item to the memory, or create a structure that includes an array of [**MOF\_FIELD**](/windows/win32/api/evntrace/ns-evntrace-mof_field) structures; most applications will create a structure that includes an array of **MOF\_FIELD** structures.</span></span> <span data-ttu-id="5ede2-144">請確定 **標頭大小** 反映實際在記錄事件之前設定的 **MOF \_ 欄位** 結構的實際數目。</span><span class="sxs-lookup"><span data-stu-id="5ede2-144">Make sure that **Header.Size** reflects the actual number of **MOF\_FIELD** structures that are actually set before logging the event.</span></span> <span data-ttu-id="5ede2-145">例如，如果事件包含三個資料欄位，請將 **標頭. 大小** 設定為 SIZEOF (事件 \_ 追蹤 \_ 標頭) + (sizeof (MOF \_ 欄位) \* 3) 。</span><span class="sxs-lookup"><span data-stu-id="5ede2-145">For example, if the event contains three data fields, set **Header.Size** to sizeof(EVENT\_TRACE\_HEADER) + (sizeof(MOF\_FIELD) \* 3).</span></span>

<span data-ttu-id="5ede2-146">如需追蹤相關事件的詳細資訊，請參閱 [在端對端案例中撰寫相關事件](writing-related-events-in-an-end-to-end-scenario.md)。</span><span class="sxs-lookup"><span data-stu-id="5ede2-146">For information on tracing related events, see [Writing Related Events in an End-to-End Scenario](writing-related-events-in-an-end-to-end-scenario.md).</span></span>

<span data-ttu-id="5ede2-147">下列範例顯示如何呼叫 [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函式來記錄事件。</span><span class="sxs-lookup"><span data-stu-id="5ede2-147">The following example shows how to call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events.</span></span> <span data-ttu-id="5ede2-148">此範例會參考 [針對傳統提供者發行您的事件架構](publishing-your-event-schema-for-a-classic-provider.md)時所定義的事件。</span><span class="sxs-lookup"><span data-stu-id="5ede2-148">The example references the events defined in [Publishing Your Event Schema for a Classic Provider](publishing-your-event-schema-for-a-classic-provider.md).</span></span>


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



 

 

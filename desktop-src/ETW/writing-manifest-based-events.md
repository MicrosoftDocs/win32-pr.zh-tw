---
description: 在您可以將事件寫入追蹤會話之前，您必須先註冊您的提供者。
ms.assetid: 76e7202e-74ce-40a3-a04b-9af5117fe20e
title: 撰寫以資訊清單為基礎的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a1817defe85e68860d8a628a2d3275034ce285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113964"
---
# <a name="writing-manifest-based-events"></a>撰寫以資訊清單為基礎的事件

在您可以將事件寫入追蹤會話之前，您必須先註冊您的提供者。 註冊提供者會告知 ETW 您的提供者已準備好將事件寫入追蹤會話。 進程最多可註冊1024提供者 Guid;不過，您應該將進程註冊的提供者數目限制為一或兩個。

**在 Windows Vista 之前：** 進程可註冊的提供者數目沒有任何限制。

若要註冊以資訊清單為基礎的提供者，請呼叫 [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) 函數。 此函式會註冊提供者的 GUID，並識別在控制器啟用或停用提供者時 ETW 呼叫的選擇性回呼。

在提供者結束之前，呼叫 [**EventUnregister**](/windows/desktop/api/Evntprov/nf-evntprov-eventunregister) 函式以從 ETW 移除提供者的註冊。 [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)函式會傳回您傳遞給 **EventUnregister** 函數的註冊控制碼。

以 [資訊清單為基礎的](about-event-tracing.md)提供者不需要在會話啟用或停用提供者時，執行 [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)函式來接收通知。 回呼是選擇性的，可供資訊參考之用;註冊提供者時，您不需要指定或執行回呼。 以資訊清單為基礎的提供者可以直接寫入事件，而 ETW 會決定是否要將事件記錄到追蹤會話中。 如果事件要求您執行大量工作來產生事件的資料，您可能會想要先呼叫 [**EventEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventenabled) 或 [**EventProviderEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventproviderenabled) 函式，以確認事件將會在執行工作之前寫入至會話。

一般而言，如果您的提供者要求控制器傳遞提供者定義的篩選資料 (查看提供者的 [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)) *FilterData* 參數，或提供者使用其本身註冊時所指定的內容資訊 (請參閱 [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)) 的 *CallbackCoNtext* 參數，則您會執行回呼。

以 [資訊清單為基礎](about-event-tracing.md)的提供者會呼叫 [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite)或 [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring)函數，以將事件寫入會話。 如果您的事件資料是字串，或您未定義提供者的資訊清單，且您的事件資料是單一字串，請呼叫 [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) 函式來寫入事件。 針對包含數值或複雜資料類型的事件資料，呼叫 [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) 函數來記錄事件。

下列範例示範如何使用 [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) 函數來準備要寫入的事件資料。 此範例會參考 [針對以資訊清單為基礎的提供者發行事件架構](publishing-your-event-schema-for-a-manifest-base-provider.md)時所定義的事件。


```C++
#include <windows.h>
#include <stdio.h>
#include <evntprov.h>
#include "provider.h"  // Generated from manifest

#define SUNDAY     0X1
#define MONDAY     0X2
#define TUESDAY    0X4
#define WEDNESDAY  0X8
#define THURSDAY   0X10
#define FRIDAY     0X20
#define SATURDAY   0X40

enum TRANSFER_TYPE {
  Download = 1,
  Upload,
  UploadReply
};

#define MAX_NAMEDVALUES          5  // Maximum array size
#define MAX_PAYLOAD_DESCRIPTORS  9 + (2 * MAX_NAMEDVALUES)

typedef struct _namedvalue {
  LPWSTR name;
  USHORT value;
} NAMEDVALUE, *PNAMEDVALUE;

void wmain(void)
{
    DWORD status = ERROR_SUCCESS;
    REGHANDLE RegistrationHandle = NULL; 
    EVENT_DATA_DESCRIPTOR Descriptors[MAX_PAYLOAD_DESCRIPTORS]; 
    DWORD i = 0;

    // Data to load into event descriptors

    USHORT Scores[3] = {45, 63, 21};
    ULONG pImage = (ULONG)&Scores;
    DWORD TransferType = Upload;
    DWORD Day = MONDAY | TUESDAY;
    LPWSTR Path = L"c:\\path\\folder\\file.ext";
    BYTE Cert[11] = {0x2, 0x4, 0x8, 0x10, 0x20, 0x30, 0x40, 0x50, 0x60, 0x0, 0x1};
    PBYTE Guid = (PBYTE) &ProviderGuid;
    USHORT ArraySize = MAX_NAMEDVALUES;
    BOOL IsLocal = TRUE;
    NAMEDVALUE NamedValues[MAX_NAMEDVALUES] = { 
        {L"Bill", 1},
        {L"Bob", 2},
        {L"William", 3},
        {L"Robert", 4},
        {L"", 5}
        };

    status = EventRegister(
        &ProviderGuid,      // GUID that identifies the provider
        NULL,               // Callback not used
        NULL,               // Context noot used
        &RegistrationHandle // Used when calling EventWrite and EventUnregister
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"EventRegister failed with %lu\n", status);
        goto cleanup;
    }
  
    // Load the array of data descriptors for the TransferEvent event. 
    // Add the data to the array in the order of the <data> elements
    // defined in the event's template. 
   
    EventDataDescCreate(&Descriptors[i++], &pImage, sizeof(ULONG));
    EventDataDescCreate(&Descriptors[i++], Scores, sizeof(Scores));
    EventDataDescCreate(&Descriptors[i++], Guid, sizeof(GUID));
    EventDataDescCreate(&Descriptors[i++], Cert, sizeof(Cert));
    EventDataDescCreate(&Descriptors[i++], &IsLocal, sizeof(BOOL));
    EventDataDescCreate(&Descriptors[i++], Path, (ULONG)(wcslen(Path) + 1) * sizeof(WCHAR));
    EventDataDescCreate(&Descriptors[i++], &ArraySize, sizeof(USHORT));

    // If your event contains a structure, you should write each member
    // of the structure separately. If the structure contained integral data types
    // such as DWORDs and the data types were aligned on an 8-byte boundary, you 
    // could use the following call to write the structure, however, you are 
    // encouraged to write the members separately.
    //
    // EventDataDescCreate(&EvtData, struct, sizeof(struct));
    //
    // Because the array of structures in this example contains both strings 
    // and numbers, you must write each member of the structure separately.

    for (int j = 0; j < MAX_NAMEDVALUES; j++)
    {
        EventDataDescCreate(&Descriptors[i++], NamedValues[j].name, (ULONG)(wcslen(NamedValues[j].name)+1) * sizeof(WCHAR) );
        EventDataDescCreate(&Descriptors[i++], &(NamedValues[j].value), sizeof(USHORT) );
    }

    EventDataDescCreate(&Descriptors[i++], &Day, sizeof(DWORD));
    EventDataDescCreate(&Descriptors[i++], &TransferType, sizeof(DWORD));

    // Write the event. You do not have to verify if your provider is enabled before
    // writing the event. ETW will write the event to any session that enabled
    // the provider. If no session enabled the provider, the event is not 
    // written. If you need to perform extra work to write an event that you
    // would not otherwise do, you may want to call the EventEnabled function
    // before performing the extra work. The EventEnabled function tells you if a
    // session has enabled your provider, so you know if you need to perform the 
    // extra work or not.

    status = EventWrite(
        RegistrationHandle,              // From EventRegister
        &TransferEvent,                  // EVENT_DESCRIPTOR generated from the manifest
        (ULONG)MAX_PAYLOAD_DESCRIPTORS,  // Size of the array of EVENT_DATA_DESCRIPTORs
        &Descriptors[0]                  // Array of descriptors that contain the event data
        );

    if (status != ERROR_SUCCESS) 
    {
        wprintf(L"EventWrite failed with 0x%x", status);
    }

cleanup:

    EventUnregister(RegistrationHandle);
}
```



當您編譯資訊清單時 (請參閱使用上述範例所述的 [編譯檢測資訊清單](../wes/compiling-an-instrumentation-manifest.md)) ，它會建立下列) 中所參考的標頭檔 (。


```C++
//**********************************************************************`
//* This is an include file generated by Message Compiler.             *`
//*                                                                    *`
//* Copyright (c) Microsoft Corporation. All Rights Reserved.          *`
//**********************************************************************`
#pragma once
//+
// Provider Microsoft-Windows-ETWProvider Event Count 1
//+
EXTERN_C __declspec(selectany) const GUID ProviderGuid = {0xd8909c24, 0x5be9, 0x4502, {0x98, 0xca, 0xab, 0x7b, 0xdc, 0x24, 0x89, 0x9d}};
//
// Keyword
//
#define READ_KEYWORD 0x1
#define WRITE_KEYWORD 0x2
#define LOCAL_KEYWORD 0x4
#define REMOTE_KEYWORD 0x8

//
// Event Descriptors
//
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR TransferEvent = {0x1, 0x0, 0x0, 0x4, 0x0, 0x0, 0x5};
#define TransferEvent_value 0x1
#define MSG_Provider_Name                    0x90000001L
#define MSG_Event_WhenToTransfer             0xB0000001L
#define MSG_Map_Download                     0xD0000001L
#define MSG_Map_Upload                       0xD0000002L
#define MSG_Map_UploadReply                  0xD0000003L
#define MSG_Map_Sunday                       0xF0000001L
#define MSG_Map_Monday                       0xF0000002L
#define MSG_Map_Tuesday                      0xF0000003L
#define MSG_Map_Wednesday                    0xF0000004L
#define MSG_Map_Thursday                     0xF0000005L
#define MSG_Map_Friday                       0xF0000006L
#define MSG_Map_Saturday                     0xF0000007L
```



 

 

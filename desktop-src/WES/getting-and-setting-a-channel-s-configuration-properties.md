---
title: 取得和設定通道的設定屬性
description: 通道最初是在資訊清單中設定 (請參閱定義通道) 。 若要取得通道的可設定屬性，請呼叫 EvtOpenChannelConfig 函式來取得通道的控制碼。
ms.assetid: 4ee44dae-b390-4d98-bcef-836b53b04860
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b28e96e45a8b061fac2914b2ef79847cf25a6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021240"
---
# <a name="getting-and-setting-a-channels-configuration-properties"></a>取得和設定通道的設定屬性

通道最初是在資訊清單中設定 (請參閱 [定義通道](defining-channels.md)) 。 若要取得通道的可設定屬性，請呼叫 [**EvtOpenChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtopenchannelconfig) 函式來取得通道的控制碼。 然後，呼叫 [**EvtGetChannelConfigProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtgetchannelconfigproperty) 函數，以取得通道的可設定屬性值。 如需可設定的屬性清單，請參閱 [**.Evt \_ 通道設定 \_ \_ 屬性 \_ 識別碼**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id) 列舉。 通道的名稱、值和訊息字串屬性會被視為中繼資料，而且無法使用 **EvtGetChannelConfigProperty** 函數來抓取。 如需取得這些屬性的詳細資訊，請參閱 [取得提供者的中繼資料](getting-a-provider-s-metadata-.md)。

您可以在執行時間設定許多通道的屬性。 [**.Evt \_ 通道設定 \_ \_ 屬性 \_ 識別碼**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)列舉會識別您無法設定的屬性。 若要設定通道屬性，使用者必須在 administrators 群組中，並以較高的許可權執行。 若要設定通道的可設定屬性，請呼叫 [**EvtOpenChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtopenchannelconfig) 函式來取得通道的控制碼。 然後，呼叫 [**EvtSetChannelConfigProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtsetchannelconfigproperty) 函數來設定可設定屬性的值。 設定可設定的屬性之後，請呼叫 [**EvtSaveChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtsavechannelconfig) 函式來儲存並套用變更。

如需示範如何取得及設定通道屬性的範例，請參閱下列各節：

-   [列舉通道](#enumerating-channels)
-   [取得通道屬性](#getting-and-setting-a-channels-configuration-properties)
-   [設定通道屬性](#getting-and-setting-a-channels-configuration-properties)

## <a name="enumerating-channels"></a>列舉通道

下列範例示範如何列舉電腦上已註冊的通道。


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")


void main(void)
{
    EVT_HANDLE hChannels = NULL;
    LPWSTR pBuffer = NULL;
    LPWSTR pTemp = NULL;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    // Get a handle to an enumerator that contains all the names of the 
    // channels registered on the computer.
    hChannels = EvtOpenChannelEnum(NULL, 0);

    if (NULL == hChannels)
    {
        wprintf(L"EvtOpenChannelEnum failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"List of Channels\n\n");

    // Enumerate through the list of channel names. If the buffer is not big
    // enough reallocate the buffer. To get the configuration information for
    // a channel, call the EvtOpenChannelConfig function.
    while (true)
    {
        if (!EvtNextChannelPath(hChannels, dwBufferSize, pBuffer, &dwBufferUsed))
        {
            status = GetLastError();

            if (ERROR_NO_MORE_ITEMS == status)
            {
                break;
            }
            else if (ERROR_INSUFFICIENT_BUFFER == status)
            {
                dwBufferSize = dwBufferUsed;
                pTemp = (LPWSTR)realloc(pBuffer, dwBufferSize * sizeof(WCHAR));
                if (pTemp)
                {
                    pBuffer = pTemp;
                    pTemp = NULL;
                    EvtNextChannelPath(hChannels, dwBufferSize, pBuffer, &dwBufferUsed);
                }
                else
                {
                    wprintf(L"realloc failed\n");
                    status = ERROR_OUTOFMEMORY;
                    goto cleanup;
                }
            }
            else
            {
                wprintf(L"EvtNextChannelPath failed with %lu.\n", status);
            }
        }

        wprintf(L"%s\n", pBuffer);
    }

cleanup:

    if (hChannels)
        EvtClose(hChannels);

    if (pBuffer)
        free(pBuffer);
}
```



## <a name="getting-channel-properties"></a>取得通道屬性

下列範例顯示如何取得通道的可設定屬性。


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")
#pragma comment(lib, "ole32.lib")

LPWSTR pwcsChannelTypes[] = {L"Admin", L"Operational", L"Analytic", L"Debug"};
LPWSTR pwcsIsolationTypes[] = {L"Application", L"System", L"Custom"};
LPWSTR pwcsClockTypes[] = {L"System", L"QPC"};

DWORD PrintChannelProperties(EVT_HANDLE hChannel);
DWORD PrintChannelProperty(int Id, PEVT_VARIANT pProperty);

void main(void)
{
    EVT_HANDLE hChannel = NULL;
    DWORD status = ERROR_SUCCESS;
    LPWSTR pwsChannelName = L"<name of channel goes here>";

    hChannel = EvtOpenChannelConfig(NULL, pwsChannelName, 0);

    if (NULL == hChannel) // Fails with 15007 (ERROR_EVT_CHANNEL_NOT_FOUND) if the channel is not found
    {
        wprintf(L"EvtOpenChannelConfig failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    status = PrintChannelProperties(hChannel);

cleanup:

    if (hChannel)
        EvtClose(hChannel);
}

// Print the channel's configuration properties. Use the EVT_CHANNEL_CONFIG_PROPERTY_ID
// enumeration values to loop through all the properties.
DWORD PrintChannelProperties(EVT_HANDLE hChannel)
{
    PEVT_VARIANT pProperty = NULL;  // Buffer that receives the property value
    PEVT_VARIANT pTemp = NULL;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    for (int Id = 0; Id < EvtChannelConfigPropertyIdEND; Id++)
    {
        // Get the specified property. If the buffer is too small, reallocate it.
        if  (!EvtGetChannelConfigProperty(hChannel, (EVT_CHANNEL_CONFIG_PROPERTY_ID)Id, 0, dwBufferSize, pProperty, &dwBufferUsed))
        {
            status = GetLastError();
            if (ERROR_INSUFFICIENT_BUFFER == status)
            {
                dwBufferSize = dwBufferUsed;
                pTemp = (PEVT_VARIANT)realloc(pProperty, dwBufferSize);
                if (pTemp)
                {
                    pProperty = pTemp;
                    pTemp = NULL;
                    EvtGetChannelConfigProperty(hChannel, (EVT_CHANNEL_CONFIG_PROPERTY_ID)Id, 0, dwBufferSize, pProperty, &dwBufferUsed);
                }
                else
                {
                    wprintf(L"realloc failed\n");
                    status = ERROR_OUTOFMEMORY;
                    goto cleanup;
                }
            }

            if (ERROR_SUCCESS != (status = GetLastError()))
            {
                wprintf(L"EvtGetChannelConfigProperty failed with %d\n", GetLastError());
                goto cleanup;
            }
        }

        if (status = PrintChannelProperty(Id, pProperty))
            break;
    }

cleanup:

    if (pProperty)
        free(pProperty);

    return status;
}

// Print the property value.
DWORD PrintChannelProperty(int Id, PEVT_VARIANT pProperty)
{
    DWORD status = ERROR_SUCCESS;
    WCHAR wszSessionGuid[50];
    LPWSTR lpws = NULL;

    switch(Id)
    {
        case EvtChannelConfigEnabled:
            wprintf(L"Enabled: %s\n", (TRUE == pProperty->BooleanVal) ? L"TRUE" : L"FALSE");
            break;

        case EvtChannelConfigIsolation:
            wprintf(L"Isolation: %s\n", pwcsIsolationTypes[pProperty->UInt32Val]);
            break;

        case EvtChannelConfigType:
            wprintf(L"Type: %s\n", pwcsChannelTypes[pProperty->UInt32Val]);
            break;

        // This will contain a value if the channel is imported.
        case EvtChannelConfigOwningPublisher:
            wprintf(L"Publisher that defined the channel: %s\n", pProperty->StringVal);
            break;

        case EvtChannelConfigClassicEventlog:
            wprintf(L"ClassicEventlog: %s\n", (TRUE == pProperty->BooleanVal) ? L"TRUE" : L"FALSE");
            break;

        case EvtChannelConfigAccess:
            wprintf(L"Access: %s\n", pProperty->StringVal);
            break;

        case EvtChannelLoggingConfigRetention:
            wprintf(L"Retention: %s\n", (TRUE == pProperty->BooleanVal) ? L"TRUE (Sequential)" : L"FALSE (Circular)");
            break;

        case EvtChannelLoggingConfigAutoBackup:
            wprintf(L"AutoBackup: %s\n", (TRUE == pProperty->BooleanVal) ? L"TRUE" : L"FALSE"); 
            break;

        case EvtChannelLoggingConfigMaxSize:
            wprintf(L"MaxSize: %I64u MB\n", pProperty->UInt64Val / (1024*1024));
            break;

        case EvtChannelLoggingConfigLogFilePath:
            wprintf(L"LogFilePath: %s\n", pProperty->StringVal);
            break;

        case EvtChannelPublishingConfigLevel:
            if (EvtVarTypeNull == pProperty->Type)
                wprintf(L"Level: \n");
            else
                wprintf(L"Level: %lu\n", pProperty->UInt32Val);

            break;

        // The upper 8 bits can contain reserved bit values, so do not include them
        // when checking to see if any keywords are set.
        case EvtChannelPublishingConfigKeywords:
            if (EvtVarTypeNull == pProperty->Type)
                wprintf(L"Keywords: \n");
            else
                wprintf(L"Keywords: %I64u\n", pProperty->UInt64Val & 0x00FFFFFFFFFFFFFF);

            break;

        case EvtChannelPublishingConfigControlGuid:
            if (EvtVarTypeNull == pProperty->Type)
                wprintf(L"ControlGuid: \n");
            else
            {
                StringFromGUID2(*(pProperty->GuidVal), wszSessionGuid, sizeof(wszSessionGuid)/sizeof(WCHAR));
                wprintf(L"ControlGuid: %s\n", wszSessionGuid);
            }

            break;

        case EvtChannelPublishingConfigBufferSize:
            wprintf(L"BufferSize: %lu KB\n", pProperty->UInt32Val);
            break;

        case EvtChannelPublishingConfigMinBuffers:
            wprintf(L"MinBuffers: %lu\n", pProperty->UInt32Val);
            break;

        case EvtChannelPublishingConfigMaxBuffers:
            wprintf(L"MaxBuffers: %lu\n", pProperty->UInt32Val);
            break;

        case EvtChannelPublishingConfigLatency:
            wprintf(L"Latency: %lu (sec)\n", pProperty->UInt32Val / 1000); // 1 ms
            break;

        case EvtChannelPublishingConfigClockType:
            wprintf(L"ClockType: %s\n", pwcsClockTypes[pProperty->UInt32Val]);
            break;

        case EvtChannelPublishingConfigSidType:
            wprintf(L"Include security ID (SID): %s\n", (EvtChannelSidTypeNone == pProperty->UInt32Val) ? L"No" : L"Yes");
            break;

        case EvtChannelPublisherList:

            wprintf(L"List of providers that import this channel: \n");
            for (DWORD i = 0; i < pProperty->Count; i++)
            {
                wprintf(L"  %s\n", pProperty->StringArr[i]);
            }

            break;

        case EvtChannelPublishingConfigFileMax:
            wprintf(L"FileMax: %lu\n", pProperty->UInt32Val);
            break;

        default:
            wprintf(L"Unknown property Id: %d\n", Id);
    }
    
    return status;
}
```



## <a name="setting-channel-properties"></a>設定通道屬性

下列範例顯示如何設定通道的可設定屬性。


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>
#include <winmeta.h>

// For this example, including the keywords that were defined in the header file 
// that the message compiler generated for the manifest.
//
// Keywords
//
#define READ_KEYWORD 0x10
#define WRITE_KEYWORD 0x20
// #include "myprovider.h"  // Contains the keywords defined for my provider

#pragma comment(lib, "wevtapi.lib")

void main(void)
{
    EVT_HANDLE hChannel = NULL;
    DWORD status = ERROR_SUCCESS;
    EVT_VARIANT ChannelProperty;
    DWORD dwBufferSize = sizeof(EVT_VARIANT);
    DWORD dwBufferUsed = 0;

    hChannel = EvtOpenChannelConfig(NULL, L"<name of channel goes here>", 0);
    if (NULL == hChannel)
    {
        wprintf(L"EvtOpenChannelConfig failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    RtlZeroMemory(&ChannelProperty, dwBufferSize);
    ChannelProperty.Type = EvtVarTypeBoolean;
    ChannelProperty.BooleanVal = FALSE;
    if  (!EvtSetChannelConfigProperty(hChannel, EvtChannelConfigEnabled, 0, &ChannelProperty))
    {
        wprintf(L"EvtSetChannelConfigProperty for Enabled property failed with %lu\n", GetLastError());
        goto cleanup;
    }

    RtlZeroMemory(&ChannelProperty, dwBufferSize);
    ChannelProperty.Type = EvtVarTypeUInt32;
    ChannelProperty.UInt32Val = WINEVENT_LEVEL_WARNING;  // Found in winmeta.h
    if  (!EvtSetChannelConfigProperty(hChannel, EvtChannelPublishingConfigLevel, 0, &ChannelProperty))
    {
        wprintf(L"EvtSetChannelConfigProperty for Level failed with %lu\n", GetLastError());
        goto cleanup;
    }

    RtlZeroMemory(&ChannelProperty, dwBufferSize);
    ChannelProperty.Type = EvtVarTypeUInt64;
    ChannelProperty.UInt64Val = READ_KEYWORD | WRITE_KEYWORD;
    if  (!EvtSetChannelConfigProperty(hChannel, EvtChannelPublishingConfigKeywords, 0, &ChannelProperty))
    {
        wprintf(L"EvtSetChannelConfigProperty for Keywords failed with %lu\n", GetLastError());
        goto cleanup;
    }

    RtlZeroMemory(&ChannelProperty, dwBufferSize);
    ChannelProperty.Type = EvtVarTypeBoolean;
    ChannelProperty.BooleanVal = TRUE;
    if  (!EvtSetChannelConfigProperty(hChannel, EvtChannelConfigEnabled, 0, &ChannelProperty))
    {
        wprintf(L"EvtSetChannelConfigProperty for Enabled property failed with %lu\n", GetLastError());
        goto cleanup;
    }

    // The user needs to be in the administrators group and be running with
    // elevated permissions for this call to work.
    if (!EvtSaveChannelConfig(hChannel, 0))
    {
        wprintf(L"EvtSaveChannelConfig failed with %lu\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"Channel properties updated.\n");

cleanup:

    if (hChannel)
        EvtClose(hChannel);
}
```



 

 





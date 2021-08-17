---
title: 封包時間戳記
description: IP 協助程式封包時間戳記 Api 可讓您判斷網路介面卡的時間戳記功能，並以跨時間戳記的形式從網路介面卡查詢時間戳記。
ms.topic: article
ms.date: 01/19/2021
ms.openlocfilehash: 12da7189dbae5f38085cdf4ad5f8e9ac1214cff7ddd0b683ecd97b70b2786c51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146631"
---
# <a name="packet-timestamping"></a>封包時間戳記

## <a name="introduction"></a>簡介

許多網路介面卡 (Nic 或網路介面卡) 可以在每次接收或傳輸封包時，在其硬體中產生時間戳記。 時間戳記是使用 NIC 自己的硬體時鐘產生的。 這項功能是特別針對 Precision Time Protocol (PTP) （這是時間同步處理通訊協定）所使用。 PTP 可在通訊協定本身內進行布建，以使用這類硬體時間戳記。

例如，您可以使用時間戳來計算電腦網路堆疊內的封包花費的時間，然後再傳送到網路或從中接收。 這些計算接著可以由 PTP 用來改善時間同步處理的精確度。 網路介面卡的封包時間戳記支援，有時特別適用于 PTP 通訊協定。 在其他情況下，則會提供更通用的支援。

時間戳記 api 可讓 Windows 針對適用于 PTP 第2版通訊協定的網路介面卡，支援硬體時間戳記功能的能力。 整體來說，這些功能包括提供網路介面卡驅動程式支援時間戳記的能力，並讓使用者模式應用程式使用與封包[Windows 通訊端](/windows/win32/winsock/windows-sockets-start-page-2)相關的時間戳記 (看到[Winsock 時間戳記](/windows/win32/winsock/winsock-timestamping)) 。 此外，也提供產生軟體時間戳記的功能，可讓網路驅動程式產生軟體中的時間戳記。 這類軟體時間戳記是由 NIC 驅動程式使用對等的 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) 所產生。 但是，不支援同時啟用硬體 *和* 軟體時間戳記。

特別是，本主題中所述的「網際網路通訊協定協助程式 (IP 協助程式) 封包時間戳記 Api，可讓使用者模式應用程式判斷網路介面卡的時間戳記功能，並以跨時間戳記的格式從網路介面卡查詢時間戳記 (如下) 所述。

## <a name="supporting-precision-time-protocol-version-2"></a>支援精確度時間通訊協定第2版

如先前所述，Windows 中的時間戳記支援主要目標是支援精確度時間通訊協定第2版 (PTPv2) 通訊協定。 在 PTPv2 中，並非所有的訊息都需要時間戳記。 尤其是，PTP 事件訊息會使用時間戳。 目前，支援的範圍是透過使用者資料包協定 (UDP) 的 PTPv2。 不支援透過原始乙太網路的 PTP。

在 *2 步驟* 模式中，PTPv2 操作支援時間戳記。 *2 步驟* 是指不會在硬體中即時產生 PTP 封包中的實際時間戳，而是從硬體中取出並以個別的訊息形式提供 (例如，使用追蹤訊息) 。

總而言之，您可以在 PTPv2 應用程式中使用網際網路通訊協定協助程式 (IP 協助程式) 封包時間戳記 Api 以及 Winsock 的時間戳記支援，以改善其時間同步處理的精確度。

## <a name="retrieving-the-timestamping-capabilities-of-a-network-adapter"></a>正在抓取網路介面卡的時間戳記功能

應用程式（例如 PTP 時間同步處理服務）必須判斷網路介面卡的時間戳記功能。 使用抓取的功能，應用程式可以決定是否要使用時間戳。

即使網路介面卡支援時間戳記 *，仍必須* 維持預設關閉的功能。 介面卡會在指示時開啟時間戳記。 Windows 提供應用程式的 api 來取得硬體的功能，以及開啟了哪些功能。

若要取得網路介面卡支援的時間戳記功能，請呼叫 [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) 函式，提供網路介面卡 (LUID) 的本機唯一識別碼，並傳回以 [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) 物件的形式取得支援的時間戳記功能。

從 **GetInterfaceSupportedTimestampCapabilities** 傳回的程式碼會指出呼叫是否成功，以及是否已抓取填入的 **INTERFACE_TIMESTAMP_CAPABILITIES** 值。

若要取得網路介面卡目前已啟用的時間戳記功能，請呼叫 [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) 函式，提供網路介面卡 (LUID) 的本機唯一識別碼，並以 [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) 物件的形式傳回已啟用的時間戳記功能。

同樣地，從 **GetInterfaceActiveTimestampCapabilities** 傳回的程式碼會指出成功或失敗，以及是否已抓取有效的 **INTERFACE_TIMESTAMP_CAPABILITIES** 值。

網路介面卡可支援各種時間戳記功能。 例如，某些介面卡可以在傳送和接收期間將每封包加上時間戳記，而有些則只支援 PTPv2 封包。 [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities)結構描述網路介面卡所支援的確切功能。

## <a name="retrieving-cross-timestamps-from-a-network-adapter"></a>從網路介面卡取回跨時間戳記

使用硬體時間戳記時，PTP 應用程式需要建立關聯 (例如，在網路介面卡的硬體時鐘和系統時鐘之間使用適當的數學技巧) 。 這是必要的，因此以一個時鐘單位表示時間的值可以轉換成另一個時鐘的單位。 針對此用途提供跨時間戳記，而您的應用程式可以定期取樣跨時間戳記，以建立這類關聯性。

若要這樣做，請呼叫 [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) 函式，提供網路介面卡 (LUID) 的本機唯一識別碼，並從網路介面卡以 [**INTERFACE_HARDWARE_CROSSTIMESTAMP**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) 物件的格式傳回時間戳記。

## <a name="timestamp-capability-change-notifications"></a>時間戳記功能變更通知

若要在網路介面卡變更時間戳記功能時收到通知，請呼叫 [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) 函式，並提供您已實回呼函式的指標，以及選擇性的呼叫端配置內容。

**RegisterInterfaceTimestampConfigChange** 會傳回一個控制碼，您接著可以將它傳遞至 [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) ，以取消註冊回呼函式。

## <a name="code-example-1mdashretrieving-timestamp-capabilities-and-cross-timestamps"></a>程式碼範例 1 &mdash; 取出時間戳記功能和跨時間戳記

```c
// main.cpp in a Console App project.

#include <stdio.h>
#include <winsock2.h>
#include <iphlpapi.h>
#pragma comment(lib, "Iphlpapi")

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv4(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv6(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// This function checks and returns the supported timestamp capabilities for an interface for
// a PTPv2 application
SupportedTimestampType
CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities;
    SupportedTimestampType supportedType = TimestampTypeNone;

    result = GetInterfaceActiveTimestampCapabilities(
                 &interfaceLuid,
                 &timestampCapabilities);
    if (result != NO_ERROR)
    {
        printf("Error retrieving hardware timestamp capabilities: %d\n", result);
        goto Exit;
    }

    if (IsPTPv2HardwareTimestampingSupportedForIPv4(&timestampCapabilities) &&
        IsPTPv2HardwareTimestampingSupportedForIPv6(&timestampCapabilities))
    {
        supportedType = TimestampTypeHardware;
        goto Exit;
    }
    else
    {
        if ((timestampCapabilities.SoftwareCapabilities.AllReceive) &&
            ((timestampCapabilities.SoftwareCapabilities.AllTransmit) ||
             (timestampCapabilities.SoftwareCapabilities.TaggedTransmit)))
        {
            supportedType = TimestampTypeSoftware;
        }
    }

Exit:
    return supportedType;
}

// Helper function which does the correlation between hardware and system clock
// using mathematical techniques
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// An application would call this function periodically to gather a set 
// of matching timestamps for use in converting hardware timestamps to
// system timestamps
DWORD
RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp;

    result = CaptureInterfaceHardwareCrossTimestamp(
                 &interfaceLuid,
                 &crossTimestamp);
    if (result != NO_ERROR)
    {
        printf("Error retrieving cross timestamp for the interface: %d\n", result);
        goto Exit;
    }

    // Process crossTimestamp further to create a relation between the hardware clock
    // of the NIC and the QPC values using appropriate mathematical techniques
    ComputeCorrelationOfHardwareAndSystemTimestamps(&crossTimestamp);

Exit:
    return result;
}

int main()
{
}
```

## <a name="code-example-2mdashregistering-for-timestamp-capability-change-notifications"></a>&mdash;針對時間戳記功能變更通知註冊的程式碼範例2

此範例會示範您的應用程式如何使用端對端的時間戳記。

```c
// main.cpp in a Console App project.

#include <stdlib.h>
#include <stdio.h>
#include <winsock2.h>
#include <mswsock.h>
#include <iphlpapi.h>
#include <mstcpip.h>
#pragma comment(lib, "Ws2_32")
#pragma comment(lib, "Iphlpapi")

// Globals and function declarations used by the application.
// The sample functions and skeletons demonstrate:
// - Checking timestamp configuration for an interface to determine if timestamping can be used
// - If timestamping is enabled, starts tracking changes in timestamp configuration
// - Performing correlation between hardware and system timestamps using cross timestamps
//   on a separate thread depending on the timestamp type configured
// - Receiving a packet and computing the latency between when the timestamp
//   was generated on packet reception, and when the packet was received by
//   the application through the socket
// The sample tries to demonstrate how an application could use timestamps. It is not thread safe 
// and does not do exhaustive error checking.
// Lot of the functions are provided as skeletons, or only declared and invoked
// but are not defined. It is up to
// the application to implement these suitably.

// An application could use the functions below by e.g.
// - Call InitializeTimestampingForInterface for the interface it wants to track for timestamping capability.
// - Call EstimateReceiveLatency to estimate the receive latency of a packet depending on the timestamp 
//   type configured for the interface.

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// interfaceBeingTracked is the interface the PTPv2 application
// intends to use for timestamping purpose.
wchar_t* interfaceBeingTracked;

// The active timestamping type determined for
// interfaceBeingTracked.
SupportedTimestampType timestampTypeEnabledForInterface;

HANDLE correlationThread;
HANDLE threadStopEvent;
HIFTIMESTAMPCHANGE TimestampChangeNotificationHandle = NULL;

// Function from sample above to check if an interface supports timestamping for PTPv2.
SupportedTimestampType CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid);

// Function from sample above to retrieve cross timestamps and process them further.
DWORD RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid);

// Helper function which registers for timestamp configuration changes.
DWORD RegisterTimestampChangeNotifications();

// Callback function which is invoked when timestamp configuration changes
// for some network interface.
INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK TimestampConfigChangeCallback;

// Function which does the correlation between hardware and system clock
// using mathematical techniques. It is periodically invoked and provided
// a sample of cross timestamp to compute a correlation.
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// Helper function which converts a hardware timestamp from the NIC clock
// to system timestamp (QPC) values. It is assumed that this works together
// with the ComputeCorrelationOfHardwareAndSystemTimestamps function
// to derive the correlation.
ULONG64 ConvertHardwareTimestampToQpc(ULONG64 HardwareTimestamp);

// Start function of thread which periodically samples
// cross timestamps to correlate hardware and software timestamps.
DWORD WINAPI CorrelateHardwareAndSystemTimestamps(LPVOID);

// Helper function which starts a new thread at CorrelateHardwareAndSystemTimestamps.
DWORD StartCorrelatingHardwareAndSytemTimestamps();

// Helper function which restarts correlation when some change is detected.
DWORD RestartCorrelatingHardwareAndSystemTimestamps();

// Stops the correlation thread.
DWORD StopCorrelatingHardwareAndSystemTimestamps();

DWORD
FindInterfaceFromFriendlyName(wchar_t* friendlyName, NET_LUID* interfaceLuid)
{
    DWORD result = 0;
    ULONG flags = 0;
    ULONG outBufLen = 0;
    PIP_ADAPTER_ADDRESSES pAddresses = NULL;
    PIP_ADAPTER_ADDRESSES currentAddresses = NULL;

    result = GetAdaptersAddresses(0,
        flags,
        NULL,
        pAddresses,
        &outBufLen);
    if (result == ERROR_BUFFER_OVERFLOW)
    {
        pAddresses = (PIP_ADAPTER_ADDRESSES)malloc(outBufLen);

        result = GetAdaptersAddresses(0,
            flags,
            NULL,
            pAddresses,
            &outBufLen);
        if (result != NO_ERROR)
        {
            goto Done;
        }
    }
    else if (result != NO_ERROR)
    {
        goto Done;
    }

    currentAddresses = pAddresses;
    while (currentAddresses != NULL)
    {
        if (wcscmp(friendlyName, currentAddresses->FriendlyName) == 0)
        {
            result = ConvertInterfaceIndexToLuid(currentAddresses->IfIndex, interfaceLuid);
            goto Done;
        }

        currentAddresses = currentAddresses->Next;
    }

    result = ERROR_NOT_FOUND;

Done:

    if (pAddresses != NULL)
    {
        free(pAddresses);
    }

    return result;
}

// This function checks if an interface is suitable for
// timestamping for PTPv2. If so, it registers for timestamp
// configuration changes and initializes some globals.
// If hardware  timestamping is enabled it also starts
// correlation thread.
DWORD
InitializeTimestampingForInterface(wchar_t* friendlyName)
{
    DWORD error;
    SupportedTimestampType supportedType = TimestampTypeNone;

    NET_LUID interfaceLuid;

    error = FindInterfaceFromFriendlyName(friendlyName, &interfaceLuid);
    if (error != 0)
    {
        return error;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if (supportedType != TimestampTypeNone)
    {
        error = RegisterTimestampChangeNotifications();
        if (error != NO_ERROR)
        {
            return error;
        }

        if (supportedType == TimestampTypeHardware)
        {
            threadStopEvent = CreateEvent(
                NULL,
                FALSE,
                FALSE,
                NULL
            );
            if (threadStopEvent == NULL)
            {
                return GetLastError();
            }            

            error = StartCorrelatingHardwareAndSytemTimestamps();
            if (error != 0)
            {
                return error;
            }
        }

        interfaceBeingTracked = friendlyName;
        timestampTypeEnabledForInterface = supportedType;

        return error;
    }

    return ERROR_NOT_SUPPORTED;
}

DWORD
RegisterTimestampChangeNotifications()
{
    DWORD retcode = NO_ERROR;

    // Register with NULL context
    retcode = RegisterInterfaceTimestampConfigChange(TimestampConfigChangeCallback, NULL, &TimestampChangeNotificationHandle);
    if (retcode != NO_ERROR)
    {
        printf("Error when calling RegisterIfTimestampConfigChange %d\n", retcode);
    }

    return retcode;
}

// The callback invoked when change in some interface’s timestamping configuration
// happens. The callback takes appropriate action based on the new capability of the
// interface. The callback assumes that there is only 1 NIC. If multiple NICs are being
// tracked for timestamping then the application would need to check all of them.
VOID
WINAPI
TimestampConfigChangeCallback(
    _In_ PVOID /*CallerContext*/
    )
{
    SupportedTimestampType supportedType;

    NET_LUID interfaceLuid;
    DWORD error;

    error = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (error != NO_ERROR)
    {
        if (timestampTypeEnabledForInterface == TimestampTypeHardware)
        {
            StopCorrelatingHardwareAndSystemTimestamps();
            timestampTypeEnabledForInterface = TimestampTypeNone;
        }
        return;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if ((supportedType == TimestampTypeHardware) &&
        (timestampTypeEnabledForInterface == TimestampTypeHardware))
    {
        // NIC could have been restarted, restart the correlation between hardware and 
        // system timestamps.
        RestartCorrelatingHardwareAndSystemTimestamps();
    }
    else if (supportedType == TimestampTypeHardware)
    {
        // Start thread correlating hardware and software timestamps
        StartCorrelatingHardwareAndSytemTimestamps();
    }
    else if (supportedType != TimestampTypeHardware)
    {
        // Hardware timestamps are not enabled, stop correlation
        StopCorrelatingHardwareAndSystemTimestamps();
    }

    timestampTypeEnabledForInterface = supportedType;
}

DWORD 
StartCorrelatingHardwareAndSytemTimestamps()
{
    // Create a new thread which starts at CorrelateHardwareAndSoftwareTimestamps
    correlationThread = CreateThread(
        NULL,
        0,
        CorrelateHardwareAndSystemTimestamps,
        NULL,
        0,
        NULL); 

    if (correlationThread == NULL)
    {
        return GetLastError();
    }
}

// Thread which periodically invokes functions to 
// sample cross timestamps and use them to compute
// correlation between hardware and system timestamps.
DWORD WINAPI
CorrelateHardwareAndSystemTimestamps(LPVOID /*lpParameter*/)
{
    DWORD error;
    NET_LUID interfaceLuid;
    DWORD result;

    result = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (result != 0)
    {
        return result;
    }

    while (TRUE)
    {
        error = RetrieveAndProcessCrossTimestamp(interfaceLuid);

        // Sleep and repeat till the thread gets a signal to stop
        result = WaitForSingleObject(threadStopEvent, 5000);
        if (result != WAIT_TIMEOUT)
        {
            if (result == WAIT_OBJECT_0)
            {
                return 0;
            }
            else if (result == WAIT_FAILED)            
            {
                return GetLastError();
            }

            return result;
        }
    }
}

DWORD
StopCorrelatingHardwareAndSystemTimestamps()
{
    SetEvent(threadStopEvent);
    return 0;
}

// Function which receives a packet and estimates the latency between the 
// point at which receive timestamp (of appropriate type) was generated
// and when the packet was received in the app through the socket.
// The sample assumes that there is only 1 NIC in the system. This is the NIC which is tracked through
// interfaceBeingTracked for correlation purpose, and through which packets are being
// received by the socket.
// The recvmsg parameter is of type LPFN_WSARECVMSG and an application can
// retrieve it by issuing WSAIoctl
// with SIO_GET_EXTENSION_FUNCTION_POINTER control
// and WSAID_WSARECVMSG. Please refer to msdn.
void EstimateReceiveLatency(SOCKET sock, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;
    ULONG64 packetReceivedTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.Flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR)
    {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR)
    {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    if (timestampTypeEnabledForInterface != TimestampTypeNone)
    {
        // Capture system timestamp (QPC) upon message reception.
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;

        printf("received packet\n");

        // Look for socket rx timestamp returned via control message.
        BOOLEAN retrievedTimestamp = FALSE;
        PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
        while (cmsg != NULL)
        {
            if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP)
            {
                socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
                retrievedTimestamp = TRUE;
                break;
            }
            cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
        }

        if (retrievedTimestamp)
        {
            // Compute socket receive path latency.
            LARGE_INTEGER clockFrequency;
            ULONG64 elapsedMicroseconds;

            if (timestampTypeEnabledForInterface == TimestampTypeHardware)
            {
                packetReceivedTimestamp = ConvertHardwareTimestampToQpc(socketTimestamp);
            }
            else
            {
                packetReceivedTimestamp = socketTimestamp;
            }
        
            QueryPerformanceFrequency(&clockFrequency);

            // Compute socket receive path latency.
            elapsedMicroseconds = appLevelTimestamp - packetReceivedTimestamp;
            elapsedMicroseconds *= 1000000;
            elapsedMicroseconds /= clockFrequency.QuadPart;
            printf("RX latency estimation: %lld microseconds\n",
                 elapsedMicroseconds);
        }
        else
        {
            printf("failed to retrieve RX timestamp\n");
        }
    }
}

int main()
{
}
```

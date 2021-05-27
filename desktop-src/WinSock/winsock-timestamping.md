---
title: Winsock 時間戳記
description: 封包時間戳記對於許多時鐘同步處理應用程式來說是很重要 &mdash; 的功能，例如，精確度時間通訊協定。 時間戳記的產生越接近網路介面卡硬體接收/傳送封包的時間，同步處理應用程式就越精確。
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: eae0dce8c2c16bc187ef5522f323e7f36d7fc0b4
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559940"
---
# <a name="winsock-timestamping"></a>Winsock 時間戳記

## <a name="introduction"></a>簡介

封包時間戳記對於許多時鐘同步處理應用程式來說是很重要 &mdash; 的功能，例如，精確度時間通訊協定。 時間戳記的產生越接近網路介面卡硬體接收/傳送封包的時間，同步處理應用程式就越精確。

因此，本主題中所述的時間戳記 Api 可為您的應用程式提供一種機制，以報告應用層底下所產生的時間戳記。 具體而言，是在位於微型網路介面和 NDIS 之間的介面上的軟體時間戳記，以及 NIC 硬體中的硬體時間戳記。 時間戳記 API 可大幅提升時鐘同步處理的精確度。 目前，支援的範圍是 (UDP) 通訊端的使用者資料包協定。

## <a name="receive-timestamps"></a>接收時間戳記

您可以透過 [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL 來設定接收時間戳記的接收。 您可以使用該 IOCTL 來啟用接收時間戳記的接收。 當您使用 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式接收資料包時，其時間戳記 (如果 [可用的) ] 包含在 **SO_TIMESTAMP** 控制訊息中。

**SO_TIMESTAMP** (0x300A) 是在中定義 `mstcpip.h` 。 控制訊息資料會以 **UINT64** 的形式傳回。

## <a name="transmit-timestamps"></a>傳輸時間戳記

傳輸時間戳記接收也是透過 [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL 來設定。 您可以使用該 IOCTL 來啟用傳輸時間戳記接收，以及指定系統將緩衝的傳輸時間戳記數目。 產生傳輸時間戳記時，它們會新增至緩衝區。 如果緩衝區已滿，則會捨棄新的傳輸時間戳記。

傳送資料包時，請將資料包與 **SO_TIMESTAMP_ID** 控制訊息產生關聯。 這應該包含唯一識別碼。 使用 [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg)傳送資料包以及其 **SO_TIMESTAMP_ID** 的控制訊息。 **WSASendMsg** 傳回之後，傳輸時間戳記可能無法立即可用。 當傳輸時間戳記變成可用時，它們就會放入每個通訊端的緩衝區中。 使用 [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL 依識別碼輪詢時間戳記。 如果時間戳記可用，則會從緩衝區中移除並傳回。 如果無法使用時間戳，則 [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) 會傳回 **WSAEWOULDBLOCK**。 如果緩衝區已滿時產生傳輸時間戳記，則會捨棄新的時間戳記。

**SO_TIMESTAMP_ID** (0x300B) 是在中定義 `mstcpip.h` 。 您應以 **UINT32** 形式提供控制訊息資料。

時間戳記會以64位計數器值表示。 計數器的頻率取決於時間戳記的來源。 針對軟體時間戳記，計數器是 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) 值，而且您可以透過 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)判斷其頻率。 針對 NIC 硬體時間戳記，計數器頻率取決於 NIC 硬體，您可以使用 [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)所提供的其他資訊來決定它。 若要判斷時間戳記的來源，請使用 [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) 和 [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) 函數。

除了使用 [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) 通訊端選項來啟用通訊端的時間戳記接收之外，還需要系統層級設定的通訊端層級設定。

## <a name="estimating-latency-of-socket-send-path"></a>估計通訊端傳送路徑的延遲

在本節中，我們將使用傳輸時間戳記來估計通訊端傳送路徑的延遲。 如果您的現有應用程式會使用應用層級 IO 時間戳記 &mdash; ，其中的時間戳記必須盡可能接近實際的傳輸點， &mdash; 則此範例會提供量化的描述，以瞭解 Winsock 時間戳記 api 可改善應用程式精確度的程度。

此範例假設系統中只有一張網路介面卡 (NIC) ，而且 *interfaceLuid* 是該介面卡的 LUID。

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_send_latency(SOCKET sock,
    PSOCKADDR_STORAGE addr,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT32))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure tx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_TX;
    config.txTimestampsBuffered = 1;
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
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    // Assign a tx timestamp ID to this datagram.
    UINT32 txTimestampId = 123;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(UINT32));
    cmsg->cmsg_level = SOL_SOCKET;
    cmsg->cmsg_type = SO_TIMESTAMP_ID;
    *(PUINT32)WSA_CMSG_DATA(cmsg) = txTimestampId;

    // Capture app-layer timestamp prior to send call.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    error =
        sendmsg(
            sock,
            &wsaMsg,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("sendmsg failed %d\n", WSAGetLastError());
        return;
    }

    printf("sent packet\n");

    // Poll for the socket tx timestamp value. The timestamp may not be available
    // immediately.
    UINT64 socketTimestamp;
    ULONG maxTimestampPollAttempts = 6;
    ULONG txTstampRetrieveIntervalMs = 1;
    BOOLEAN retrievedTimestamp = FALSE;
    for (ULONG i = 0; i < maxTimestampPollAttempts; i++) {
        error =
            WSAIoctl(
                sock,
                SIO_GET_TX_TIMESTAMP,
                &txTimestampId,
                sizeof(txTimestampId),
                &socketTimestamp,
                sizeof(socketTimestamp),
                &numBytes,
                NULL,
                NULL);
        if (error != SOCKET_ERROR) {
            ASSERT(numBytes == sizeof(timestamp));
            ASSERT(timestamp != 0);
            retrievedTimestamp = TRUE;
            break;
        }

        error = WSAGetLastError();
        if (error != WSAEWOULDBLOCK) {
            printf(“WSAIoctl failed % d\n”, error);
            break;
        }

        Sleep(txTstampRetrieveIntervalMs);
        txTstampRetrieveIntervalMs *= 2;
    }

    if (retrievedTimestamp) {
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = socketTimestamp - appLevelTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("socket send path latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve TX timestamp\n");
    }
}
```

## <a name="estimating-latency-of-socket-receive-path"></a>估計通訊端接收路徑的延遲

以下是接收路徑的類似範例。 此範例假設系統中只有一張網路介面卡 (NIC) ，而且 *interfaceLuid* 是該介面卡的 LUID。

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_receive_latency(SOCKET sock,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
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
    config.flags |= TIMESTAMPING_FLAG_RX;
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
    if (error == SOCKET_ERROR) {
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
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    // Capture app-layer timestamp upon message reception.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    printf("received packet\n");

    // Look for socket rx timestamp returned via control message.
    BOOLEAN retrievedTimestamp = FALSE;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP) {
            socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
            retrievedTimestamp = TRUE;
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    if (retrievedTimestamp) {
        // Compute socket receive path latency.
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = appLevelTimestamp - socketTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("RX latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve RX timestamp\n");
    }
}
```

## <a name="a-limitation"></a>限制

Winsock 時間戳記 Api 有一項限制，就是呼叫 [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) 一律是非封鎖的作業。 即使目前沒有可用的傳輸時間戳記，以重迭的方式呼叫 IOCTL 也會導致立即傳回 **WSAEWOULDBLOCK** 。 因為 [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) 傳回之後，傳輸時間戳記可能無法立即使用，所以您的應用程式必須輪詢 IOCTL，直到有可用的時間戳記為止。 如果傳送時間戳記緩衝區未滿，就保證在成功 **WSASendMsg** 呼叫之後可以使用傳輸時間戳記。

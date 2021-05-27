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
# <a name="winsock-timestamping"></a><span data-ttu-id="e9b04-104">Winsock 時間戳記</span><span class="sxs-lookup"><span data-stu-id="e9b04-104">Winsock timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="e9b04-105">簡介</span><span class="sxs-lookup"><span data-stu-id="e9b04-105">Introduction</span></span>

<span data-ttu-id="e9b04-106">封包時間戳記對於許多時鐘同步處理應用程式來說是很重要 &mdash; 的功能，例如，精確度時間通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e9b04-106">Packet timestamps are a crucial feature to many clock synchronization applications&mdash;for example, Precision Time Protocol.</span></span> <span data-ttu-id="e9b04-107">時間戳記的產生越接近網路介面卡硬體接收/傳送封包的時間，同步處理應用程式就越精確。</span><span class="sxs-lookup"><span data-stu-id="e9b04-107">The closer the timestamp generation is to when a packet is received/sent by the network adapter hardware, the more accurate the synchronization application can be.</span></span>

<span data-ttu-id="e9b04-108">因此，本主題中所述的時間戳記 Api 可為您的應用程式提供一種機制，以報告應用層底下所產生的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e9b04-108">So the timestamping APIs described in this topic provide your application with a mechanism to report timestamps that are generated well below the application layer.</span></span> <span data-ttu-id="e9b04-109">具體而言，是在位於微型網路介面和 NDIS 之間的介面上的軟體時間戳記，以及 NIC 硬體中的硬體時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e9b04-109">Specifically, a software timestamp at the interface between the miniport and NDIS, and a hardware timestamp in the NIC hardware.</span></span> <span data-ttu-id="e9b04-110">時間戳記 API 可大幅提升時鐘同步處理的精確度。</span><span class="sxs-lookup"><span data-stu-id="e9b04-110">The timestamping API can greatly improve clock synchronization accuracy.</span></span> <span data-ttu-id="e9b04-111">目前，支援的範圍是 (UDP) 通訊端的使用者資料包協定。</span><span class="sxs-lookup"><span data-stu-id="e9b04-111">Currently, support is scoped to User Datagram Protocol (UDP) sockets.</span></span>

## <a name="receive-timestamps"></a><span data-ttu-id="e9b04-112">接收時間戳記</span><span class="sxs-lookup"><span data-stu-id="e9b04-112">Receive timestamps</span></span>

<span data-ttu-id="e9b04-113">您可以透過 [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL 來設定接收時間戳記的接收。</span><span class="sxs-lookup"><span data-stu-id="e9b04-113">You configure receive timestamp reception through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="e9b04-114">您可以使用該 IOCTL 來啟用接收時間戳記的接收。</span><span class="sxs-lookup"><span data-stu-id="e9b04-114">Use that IOCTL to enable receive timestamp reception.</span></span> <span data-ttu-id="e9b04-115">當您使用 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式接收資料包時，其時間戳記 (如果 [可用的) ] 包含在 **SO_TIMESTAMP** 控制訊息中。</span><span class="sxs-lookup"><span data-stu-id="e9b04-115">When you receive a datagram using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function, its timestamp (if available) is contained in the **SO_TIMESTAMP** control message.</span></span>

<span data-ttu-id="e9b04-116">**SO_TIMESTAMP** (0x300A) 是在中定義 `mstcpip.h` 。</span><span class="sxs-lookup"><span data-stu-id="e9b04-116">**SO_TIMESTAMP** (0x300A) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="e9b04-117">控制訊息資料會以 **UINT64** 的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="e9b04-117">The control message data is returned as a **UINT64**.</span></span>

## <a name="transmit-timestamps"></a><span data-ttu-id="e9b04-118">傳輸時間戳記</span><span class="sxs-lookup"><span data-stu-id="e9b04-118">Transmit timestamps</span></span>

<span data-ttu-id="e9b04-119">傳輸時間戳記接收也是透過 [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL 來設定。</span><span class="sxs-lookup"><span data-stu-id="e9b04-119">Transmit timestamp reception is also configured through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="e9b04-120">您可以使用該 IOCTL 來啟用傳輸時間戳記接收，以及指定系統將緩衝的傳輸時間戳記數目。</span><span class="sxs-lookup"><span data-stu-id="e9b04-120">Use that IOCTL to enable transmit timestamp reception, and specify the number of transmit timestamps that the system will buffer.</span></span> <span data-ttu-id="e9b04-121">產生傳輸時間戳記時，它們會新增至緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e9b04-121">As transmit timestamps are generated, they are added to the buffer.</span></span> <span data-ttu-id="e9b04-122">如果緩衝區已滿，則會捨棄新的傳輸時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e9b04-122">If the buffer is full, new transmit timestamps are discarded.</span></span>

<span data-ttu-id="e9b04-123">傳送資料包時，請將資料包與 **SO_TIMESTAMP_ID** 控制訊息產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e9b04-123">When sending a datagram, associate the datagram with an **SO_TIMESTAMP_ID** control message.</span></span> <span data-ttu-id="e9b04-124">這應該包含唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9b04-124">This should contain a unique identifier.</span></span> <span data-ttu-id="e9b04-125">使用 [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg)傳送資料包以及其 **SO_TIMESTAMP_ID** 的控制訊息。</span><span class="sxs-lookup"><span data-stu-id="e9b04-125">Send the datagram, along with its **SO_TIMESTAMP_ID** control message, using [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span></span> <span data-ttu-id="e9b04-126">**WSASendMsg** 傳回之後，傳輸時間戳記可能無法立即可用。</span><span class="sxs-lookup"><span data-stu-id="e9b04-126">Transmit timestamps might not be immediately available after **WSASendMsg** returns.</span></span> <span data-ttu-id="e9b04-127">當傳輸時間戳記變成可用時，它們就會放入每個通訊端的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="e9b04-127">As transmit timestamps become available, they are placed into a per-socket buffer.</span></span> <span data-ttu-id="e9b04-128">使用 [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL 依識別碼輪詢時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e9b04-128">Use the [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL to poll for the timestamp by its ID.</span></span> <span data-ttu-id="e9b04-129">如果時間戳記可用，則會從緩衝區中移除並傳回。</span><span class="sxs-lookup"><span data-stu-id="e9b04-129">If the timestamp is available, then it is removed from the buffer and returned.</span></span> <span data-ttu-id="e9b04-130">如果無法使用時間戳，則 [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) 會傳回 **WSAEWOULDBLOCK**。</span><span class="sxs-lookup"><span data-stu-id="e9b04-130">If the timestamp is not available, then [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) returns **WSAEWOULDBLOCK**.</span></span> <span data-ttu-id="e9b04-131">如果緩衝區已滿時產生傳輸時間戳記，則會捨棄新的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e9b04-131">If a transmit timestamp is generated while the buffer is full, the new timestamp is discarded.</span></span>

<span data-ttu-id="e9b04-132">**SO_TIMESTAMP_ID** (0x300B) 是在中定義 `mstcpip.h` 。</span><span class="sxs-lookup"><span data-stu-id="e9b04-132">**SO_TIMESTAMP_ID** (0x300B) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="e9b04-133">您應以 **UINT32** 形式提供控制訊息資料。</span><span class="sxs-lookup"><span data-stu-id="e9b04-133">You should supply the control message data as a **UINT32**.</span></span>

<span data-ttu-id="e9b04-134">時間戳記會以64位計數器值表示。</span><span class="sxs-lookup"><span data-stu-id="e9b04-134">Timestamps are represented as a 64-bit counter value.</span></span> <span data-ttu-id="e9b04-135">計數器的頻率取決於時間戳記的來源。</span><span class="sxs-lookup"><span data-stu-id="e9b04-135">The frequency of the counter depends on the source of the timestamp.</span></span> <span data-ttu-id="e9b04-136">針對軟體時間戳記，計數器是 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) 值，而且您可以透過 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)判斷其頻率。</span><span class="sxs-lookup"><span data-stu-id="e9b04-136">For software timestamps, the counter is a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) value, and you can determine its frequency via [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span></span> <span data-ttu-id="e9b04-137">針對 NIC 硬體時間戳記，計數器頻率取決於 NIC 硬體，您可以使用 [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)所提供的其他資訊來決定它。</span><span class="sxs-lookup"><span data-stu-id="e9b04-137">For NIC hardware timestamps, the counter frequency is dependent on the NIC hardware, and you can determine it with additional information given by [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span></span> <span data-ttu-id="e9b04-138">若要判斷時間戳記的來源，請使用 [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) 和 [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) 函數。</span><span class="sxs-lookup"><span data-stu-id="e9b04-138">To determine the source of timestamps, use the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) and [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) functions.</span></span>

<span data-ttu-id="e9b04-139">除了使用 [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) 通訊端選項來啟用通訊端的時間戳記接收之外，還需要系統層級設定的通訊端層級設定。</span><span class="sxs-lookup"><span data-stu-id="e9b04-139">In addition to socket-level configuration using the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket option to enable timestamp reception for a socket, system-level configuration is also needed.</span></span>

## <a name="estimating-latency-of-socket-send-path"></a><span data-ttu-id="e9b04-140">估計通訊端傳送路徑的延遲</span><span class="sxs-lookup"><span data-stu-id="e9b04-140">Estimating latency of socket send path</span></span>

<span data-ttu-id="e9b04-141">在本節中，我們將使用傳輸時間戳記來估計通訊端傳送路徑的延遲。</span><span class="sxs-lookup"><span data-stu-id="e9b04-141">In this section, we'll use transmit timestamps to estimate the latency of the socket send path.</span></span> <span data-ttu-id="e9b04-142">如果您的現有應用程式會使用應用層級 IO 時間戳記 &mdash; ，其中的時間戳記必須盡可能接近實際的傳輸點， &mdash; 則此範例會提供量化的描述，以瞭解 Winsock 時間戳記 api 可改善應用程式精確度的程度。</span><span class="sxs-lookup"><span data-stu-id="e9b04-142">If you have an existing application that consumes application-level IO timestamps&mdash;where the timestamp needs to be as close as possible to the actual point of transmission&mdash;then this sample provides a quantitative description as to how much the Winsock timestamping APIs can improve the accuracy of your application.</span></span>

<span data-ttu-id="e9b04-143">此範例假設系統中只有一張網路介面卡 (NIC) ，而且 *interfaceLuid* 是該介面卡的 LUID。</span><span class="sxs-lookup"><span data-stu-id="e9b04-143">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

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

## <a name="estimating-latency-of-socket-receive-path"></a><span data-ttu-id="e9b04-144">估計通訊端接收路徑的延遲</span><span class="sxs-lookup"><span data-stu-id="e9b04-144">Estimating latency of socket receive path</span></span>

<span data-ttu-id="e9b04-145">以下是接收路徑的類似範例。</span><span class="sxs-lookup"><span data-stu-id="e9b04-145">Here's a similar sample for the receive path.</span></span> <span data-ttu-id="e9b04-146">此範例假設系統中只有一張網路介面卡 (NIC) ，而且 *interfaceLuid* 是該介面卡的 LUID。</span><span class="sxs-lookup"><span data-stu-id="e9b04-146">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

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

## <a name="a-limitation"></a><span data-ttu-id="e9b04-147">限制</span><span class="sxs-lookup"><span data-stu-id="e9b04-147">A limitation</span></span>

<span data-ttu-id="e9b04-148">Winsock 時間戳記 Api 有一項限制，就是呼叫 [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) 一律是非封鎖的作業。</span><span class="sxs-lookup"><span data-stu-id="e9b04-148">One limitation of the Winsock timestamping APIs is that calling [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) is always a non-blocking operation.</span></span> <span data-ttu-id="e9b04-149">即使目前沒有可用的傳輸時間戳記，以重迭的方式呼叫 IOCTL 也會導致立即傳回 **WSAEWOULDBLOCK** 。</span><span class="sxs-lookup"><span data-stu-id="e9b04-149">Even calling the IOCTL in an OVERLAPPED fashion results in an immediate return of **WSAEWOULDBLOCK** if there are currently no available transmit timestamps.</span></span> <span data-ttu-id="e9b04-150">因為 [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) 傳回之後，傳輸時間戳記可能無法立即使用，所以您的應用程式必須輪詢 IOCTL，直到有可用的時間戳記為止。</span><span class="sxs-lookup"><span data-stu-id="e9b04-150">Since transmit timestamps might not be immediately available after [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) returns, your application must poll the IOCTL until the timestamp is available.</span></span> <span data-ttu-id="e9b04-151">如果傳送時間戳記緩衝區未滿，就保證在成功 **WSASendMsg** 呼叫之後可以使用傳輸時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e9b04-151">A transmit timestamp is guaranteed to be available after a successful **WSASendMsg** call given that the transmit timestamp buffer is not full.</span></span>

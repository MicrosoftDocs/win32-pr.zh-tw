---
title: 'Winsock 明確擁塞通知 (ECN) '
description: 某些以使用者資料包協定為基礎的應用程式和/或通訊協定 (UDP)  (例如，QUIC) 試圖利用明確的擁塞通知 (ECN) 字碼指標，以改善擁塞網路中的延遲和抖動。
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 090ac9b0575cb491aa6d726e7507223156460ace
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559944"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a>Winsock 明確擁塞通知 (ECN) 

## <a name="introduction"></a>簡介

某些以使用者資料包協定為基礎的應用程式和/或通訊協定 (UDP)  (例如，QUIC) 試圖利用明確的擁塞通知 (ECN) 字碼指標，以改善擁塞網路中的延遲和抖動。

Winsock ECN api 擴充了 **getsockopt** / **setsockopt** 介面，以及 &mdash; [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)控制訊息介面， &mdash; 支援在 IP 標頭中修改和接收 ECN 字碼指標。 提供的功能可讓您根據每個封包來取得和設定 ECN 字碼指標。

如需有關 ECN 的詳細資訊，請參閱 [新增明確的擁塞通知 (ECN) 至 IP](https://tools.ietf.org/html/rfc3168)。

傳送資料包時，不允許您的應用程式指定 (CE) 程式碼點遇到的擁塞。 傳送將會傳回錯誤 **WSAEINVAL**。

## <a name="query-ecn-with-wsagetrecvipecn"></a>使用 WSAGetRecvIPEcn 查詢 ECN

[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) 是中定義的內嵌函數 `ws2tcpip.h` 。

呼叫 **WSAGetRecvIPEcn** 來查詢接收 **IP_ECN** 的目前啟用 (或透過 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) **IPV6_ECN**) 控制訊息。

另請參閱 [**WSAMSG**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) 結構。

- **通訊協定**： IPv4
- **Cmsg_level**： IPPROTO_IP
- **Cmsg_type**： IP_ECN (50 十進位) 
- **描述**：指定/接收服務類型 (TOS) IPv4 標頭欄位中的 ECN 點。

- **通訊協定**： IPv6
- **Cmsg_level**： IPPROTO_IPV6
- **Cmsg_type**： IPV6_ECN (50 十進位) 
- **描述**：指定/接收流量類別 IPv6 標頭欄位中的 ECN 點。

## <a name="specify-ecn-with-wsasetrecvipecn"></a>使用 WSASetRecvIPEcn 指定 ECN

[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) 是中定義的內嵌函數 `ws2tcpip.h` 。

呼叫 **WSASetRecvIPEcn** 來指定 IP 堆疊是否應該在已接收資料包的訊息中，使用包含服務 IPv4 標頭欄位類型之 ECN 點的訊息來擴展控制項緩衝區 (或流量類別 IPv6 標頭欄位) 。 當設定為時 `TRUE` ， [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式會傳回選擇性的控制項資料，其中包含所接收資料包的 ECN 點。 傳回的控制訊息類型會 **IP_ECN** (或 **IPV6_ECN**) 層級 **IPPROTO_IP** (或 **IPPROTO_IPV6**) 。 控制訊息資料會以 **INT** 傳回。 此選項只適用于資料包通訊端， (通訊端類型必須 **SOCK_DGRAM**) 。

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a>程式碼範例 1 &mdash; 應用程式廣告 ECN 支援

```cpp
#define ECN_ECT_0 2

void sendEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSASENDMSG sendmsg, PCHAR data, INT datalen)
{
    DWORD numBytes;
    INT error;

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(INT));
    cmsg->cmsg_level = (addr->ss_family == AF_INET) ? IPPROTO_IP : IPPROTO_IPV6;
    cmsg->cmsg_type = (addr->ss_family == AF_INET) ? IP_ECN : IPV6_ECN;
    *(PINT)WSA_CMSG_DATA(cmsg) = ECN_ECT_0;

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
    }
}
```

## <a name="code-example-2mdashapplication-detecting-congestion"></a>程式碼範例 2 &mdash; 應用程式偵測擁塞

```cpp
#define ECN_ECT_CE 3

int recvEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg, PCHAR data, INT datalen, PBOOLEAN congestionEncountered)
{
    DWORD numBytes;
    INT error;
    INT ecnVal;
    SOCKADDR_STORAGE remoteAddr = { 0 };

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)&remoteAddr;
    wsaMsg.namelen = sizeof(remoteAddr);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    *congestionEncountered = FALSE;

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return -1;
    }

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if ((cmsg->cmsg_level == IPPROTO_IP && cmsg->cmsg_type == IP_ECN) ||
            (cmsg->cmsg_level == IPPROTO_IPV6 && cmsg->cmsg_type == IPV6_ECN)) {
            ecnVal = *(PINT)WSA_CMSG_DATA(cmsg);
            if (ecnVal == ECN_ECT_CE) {
                *congestionEncountered = TRUE;
            }
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    return numBytes;
}

void receiver(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    DWORD enabled;
    CHAR data[512];
    BOOLEAN congestionEncountered;

    error = bind(sock, (PSOCKADDR)addr, sizeof(*addr));
    if (error == SOCKET_ERROR) {
        printf("bind failed %d\n", WSAGetLastError());
        return;
    }

    enabled = TRUE;
    error = WSASetRecvIPEcn(sock, enabled);
    if (error == SOCKET_ERROR) {
        printf(" WSASetRecvIPEcn failed %d\n", WSAGetLastError());
        return;
    }

    do {
        numBytes = recvEcn(sock, addr, recvmsg, data, sizeof(data), &congestionEncountered);
        if (congestionEncountered) {
            // Tell sender to slow down
        }
    } while (numBytes > 0);
}
```

## <a name="see-also"></a>另請參閱

* [WSAGetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)

---
description: 控制項程式碼會抓取已接受 TCP/IP 連接的重新導向記錄，以供 Windows 篩選平台重新導向服務使用。
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988722"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a>SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS 控制程式代碼

## <a name="description"></a>Description

**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** 控制程式代碼會抓取已接受 tcp/ip 連接的重新導向記錄，以供 Windows 篩選平台 (WFP) 重新導向服務使用。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>參數

### <a name="s"></a>s

識別通訊端的描述元。

### <a name="dwiocontrolcode"></a>dwIoControlCode

作業的控制項程式碼。
使用 **SIO \_ 查詢 \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 進行此作業。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數未用來進行這項操作。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。
此參數未用來進行這項操作。

### <a name="lpvoutbuffer"></a>lpvOutBuffer

輸出緩衝區的指標。
如果 *lpOverlapped* 和 *LpCompletionRoutine* 參數為 **Null**，則此參數應指向 **ULONG** 資料類型。

### <a name="cboutbuffer"></a>cbOutBuffer

輸出緩衝區的大小（以位元組為單位）。
此參數必須至少為 **ULONG** 資料類型的大小。

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。

如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。

如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。

如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。
傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。
當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。

### <a name="lpvoverlapped"></a>lpvOverlapped

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。

如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。

如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。
在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。

針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。
否則，在作業完成或發生錯誤之前，函數不會傳回。

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。

### <a name="lpthreadid"></a>lpThreadId

[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。
在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。

**注意**  這個參數只適用于 **WSPIoctl** 函數。

### <a name="lperrno"></a>lpErrno

錯誤碼的指標。

**注意**  這個參數只適用于 **WSPIoctl** 函數。

## <a name="return-value"></a>傳回值

如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。

如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。
若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。

| 錯誤碼 | 意義 |
|------------|---------|
| **\_緩衝區不足的錯誤 \_** | 傳遞給系統呼叫的資料區域太小。 如果 *lpvOutBuffer* 參數所指向的緩衝區的緩衝區大小超過 *cbOutBuffer* 參數，則會傳回此錯誤。 所需的緩衝區大小將會在 *lpcbBytesReturned* 參數中傳回。 |
| **WSA_IO_PENDING** | 已成功起始重迭的作業，並會在稍後指出完成的時間。 |
| **WSA_OPERATION_ABORTED** | 因為通訊端關閉或 **SIO_FLUSH** IOCTL 命令的執行，所以重迭的作業已取消。 |
| **WSAEFAULT** | *LpvOutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。 |
| **WSAEINPROGRESS** | 當回呼正在進行時，就會叫用此函數。 |
| **WSAEINTR** | 封鎖作業已中斷。 |
| **WSAEINVAL** | *DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。 如果 *cbOutBuffer* 參數小於 **ULONG** 資料類型的大小，就會傳回此錯誤。 |
| **WSAENETDOWN** | 網路子系統失敗。 |
| **WSAENOPROTOOPT** | 指定的通訊協定不支援通訊端選項。 |
| **WSAENOTCONN** | *通訊端未連線*。 |
| **WSAENOTSOCK** | *描述項不是* 通訊端。 |
| **WSAEOPNOTSUPP** | 不支援指定的 IOCTL 命令。 如果傳輸提供者不支援 **SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL，則會傳回此錯誤。 |

## <a name="remarks"></a>備註

Windows 8、Windows Server 2012 和更新版本的作業系統上都支援 **SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL。

WFP 允許存取 TCP/IP 封包處理路徑，也就是傳出和傳入的封包可以進行檢查或變更，然後再讓它們進一步處理。
藉由使用 TCP/IP 處理路徑，獨立軟體廠商 (Isv) 可以更輕鬆地建立防火牆、防毒軟體、診斷軟體及其他類型的應用程式和服務。
WFP 提供使用者模式和核心模式元件，讓協力廠商 Isv 可以參與在 TCP/IP 通訊協定堆疊和整個作業系統中的數個層級進行的篩選決策。
[WFP 連接重新導向] 功能可讓 WFP 標注核心驅動程式將連接重新導向至使用者模式進程、在使用者模式中執行內容檢查，以及使用不同的連線將已檢查的內容轉送到原始目的地。

**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 和數個其他相關 IOCTLS 是使用者模式元件，用來允許多個以 WFP 為基礎的連線 proxy 應用程式以合作方式檢查相同的流量流程。
每個檢查代理程式都可以安全地重新檢查已由另一個檢查代理程式檢查的網路流量。
由於有多個 proxy (由不同的 Isv 開發，例如) 某個 proxy 用來與最終目的地通訊的連線，可能會被第二個 proxy 重新導向，而且原始 proxy 可以再次重新導向新的連接。
如果沒有連線追蹤，原始連接可能永遠不會到達它的最終目的地，因為它卡在無限的 proxy 迴圈中。

**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 可用來在重新導向的通訊端連線上提供代理的連接追蹤。
這種 WFP 功能可從連接的初始重新導向到目的地的最終連接，來協助追蹤重新導向記錄。

**SIO \_ QUERY \_ wfp 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 是由 WFP 型重新導向服務用來從已接受的 tcp/ip 封包連線取得重新導向記錄， (tcp 通訊端或 UDP 通訊端的連線通訊端，例如) 由在核心模式驅動程式中 **ALE_CONNECT_REDIRECT** 層級註冊的隨附核心模式注標重新導向。
**SIO \_ QUERY wfp 連線重新 \_ \_ \_ 導向 \_ 內容** IOCTL 會由 WFP 型重新導向服務用來從已接受的 TCP/IP 封包連線中，取得 tcp 通訊端或 UDP 通訊端的連線通訊端之重新導向記錄的重新導向內容，例如，) 由在 ALE 連線重新 **\_ \_ 導向** 層級註冊的隨附注標重新導向至該 (連接。
重新導向內容是選擇性的驅動程式配置內容，如果連接目前的重新導向狀態是由呼叫重新導向服務重新導向連接，或先前被呼叫的重新導向服務重新導向，但稍後又由不同的重新導向服務重新導向，則會使用此介面。
若為 TCP proxy 連線，重新導向服務會將抓取的重新導向記錄傳輸至它用來 proxy 原始內容的 TCP 通訊端，並使用 **SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL。

當重新導向服務將非 TCP 通訊端重新導向 (UDP （例如) ）時， **SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 的重新導向記錄會使用與 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函數搭配使用的 [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)結構，向重新導向服務表示這一點。
[**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)結構的控制項成員會在 **WSACMSGHDR** 結構中設定為 **IP \_ 連接重新 \_ 導向 \_ 記錄** 的 cmsg_type。
在接受非 TCP 重新導向時，重新導向服務必須提供 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 參數。

針對非 TCP 流量，重新導向記錄會使用 [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) 結構與 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 函式進行轉送。

請注意，針對非 TCP 流量，只有流程建立封包會包含 **IP 連接重新 \_ \_ 導向 \_ 記錄**。
因此，只有第一個 proxy 封包需要使用 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式來包含此資訊。

因為 WFP 重新導向記錄是可變長度的資料 blob，所以呼叫端可以提供大型的輸出緩衝區 (*lpvOutBuffer* 參數所指向的1024位元組緩衝區，例如) 或可傳遞 *cbOutBuffer* 參數0的輸出緩衝區大小，以查詢保存所傳回之 blob 所需的緩衝區大小。
如果輸出緩衝區大小不足以保存資料，則 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會傳回 **錯誤的 \_ \_ 緩衝區** ，而且所需的緩衝區大小將會以 *lpcbBytesReturned* 參數所指向的值傳回。

呼叫 [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) 的應用程式不需要瞭解包含已抓取之重新導向內容的 blob。
這是不透明的資料 blob，應用程式需要將其取出並傳回至新的通訊端。

## <a name="see-also"></a>另請參閱

[**IPPROTO_IP 通訊端選項**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

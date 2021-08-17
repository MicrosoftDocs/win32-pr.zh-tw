---
description: 控制項程式碼會在回送介面上設定 TCP 通訊端，以提供較低的延遲和更快速的作業。
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8650cd267d321569aca584e7195fb1bdb79c83a33d931e59e8db37521b8933a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740407"
---
# <a name="sio_loopback_fast_path-control-code"></a>SIO_LOOPBACK_FAST_PATH 控制程式代碼

## <a name="description"></a>描述

**SIO \_ 回送 \_ FAST \_ 路徑** 控制程式代碼會設定 TCP 通訊端，以在回送介面上進行較低的延遲和更快速的作業。

**重要** **SIO \_ 回送 \_ FAST \_ 路徑** 已被取代，不建議在您的程式碼中使用。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>參數

### <a name="s"></a>s

識別通訊端的描述元。

### <a name="dwiocontrolcode"></a>dwIoControlCode

作業的控制項程式碼。
使用 **SIO \_ 回送 \_ FAST \_ 路徑** 進行此作業。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數包含布林值的指標，指出是否應針對快速回送作業設定通訊端。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。

### <a name="lpvoutbuffer"></a>lpvOutBuffer

輸出緩衝區的指標。
此參數未用來進行這項操作。

### <a name="cboutbuffer"></a>cbOutBuffer

輸出緩衝區的大小（以位元組為單位）。
此參數必須設定為零。

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
|**WSA \_ IO \_ 暫止** | 重迭的 i/o 作業正在進行中。 如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。 |
| **已 \_ 中止 WSA 作業 \_** | I/o 作業因為執行緒結束或應用程式要求而中止。 如果因為通訊端關閉或 **SIO \_ FLUSH IOCTL** 命令的執行而取消重迭的作業，就會傳回此錯誤。 |
| **WSAEACCES** | 嘗試以存取權限禁止的方式存取通訊端。 持續性埠保留的幾個條件下會傳回此錯誤，包括下列各項：使用者在本機電腦上缺少必要的系統管理許可權，或應用程式未在增強型 shell 中執行，因為內建的系統管理員 (`RunAs administrator`) 。 |
| **WSAEFAULT** | 系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。 *LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。 |
| **WSAEINPROGRESS** | 正在執行封鎖作業。 如果回呼正在進行中，就會傳回此錯誤。 |
| **WSAEINTR** | 呼叫 [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)時，封鎖作業中斷。 當封鎖作業中斷時，就會傳回此錯誤。 |
| **WSAEINVAL** | 提供的引數無效。 如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。 |
| **WSAENETDOWN** | 通訊端作業遇到停止的網路。 如果網路子系統失敗，就會傳回此錯誤。 |
| **WSAENOTSOCK** | 嘗試對不是通訊端的某個作業進行作業。 如果 *描述項不是套* 接字，就會傳回此錯誤。 |
| **WSAEOPNOTSUPP** | 所參考的物件類型不支援所嘗試的操作。 如果不支援指定的 IOCTL 命令，則會傳回此錯誤。 如果傳輸提供者不支援 **SIO \_ 回送 \_ FAST \_ 路徑** IOCTL，也會傳回此錯誤。 |

## <a name="remarks"></a>備註

應用程式可以使用 **SIO \_ 回送 \_ FAST \_ 路徑** IOCTL 來降低延遲，並改善 TCP 通訊端上的回送作業效能。
此 IOCTL 要求 TCP/IP 堆疊針對此通訊端上的回送作業使用特殊的快速路徑。
**SIO \_ 回送 \_ FAST \_ 路徑** IOCTL 只能用於 TCP 通訊端。
這個 IOCTL 必須用於回送會話的兩端。
您可以使用 IPv4 或 IPv6 回送介面，來支援 TCP 回送快速路徑。

計畫起始連接要求的通訊端必須先套用此 IOCTL，然後再進行連線要求。
因此 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)、 [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex)、 [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect)、 [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)或 [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) 函式用來起始連接的通訊端必須套用此 IOCTL，才能使用回送作業的快速路徑。

接聽連接要求的通訊端必須在接受連接之前套用此 IOCTL。
因此，接聽函式所使用的通訊端必須套用此 IOCTL，因此任何接受的通訊端都將使用快速路徑進行回送。
接聽函式所傳回並傳遞至 [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) 函式的任何通訊端，都會標示為針對回送作業使用特殊的快速路徑。

當應用程式使用快速路徑在回送介面上建立連接時，連接存留期的所有封包都必須使用快速路徑。

將 **SIO \_ 回送 \_ FAST \_ 路徑** 套用至將連接至非回送路徑的通訊端，將不會有任何作用。

此 TCP 回送優化會導致封包流經傳輸層 (TL) ，而不是透過網路層進行傳統的回送。
此優化可改善回送封包的延遲。
一旦應用程式將連接層級設定為使用回送快速路徑之後，所有封包都會遵循回送路徑。
針對回送通訊，不需要擁塞和封包捨棄。
TCP 中的擁塞控制和可靠傳遞的概念不是必要的。
但是，流程式控制制的情況並不成立。
如果沒有流量控制，傳送者可能會造成接收緩衝區負荷，並導致錯誤的 TCP 回送行為。
TCP 優化回送路徑中的流程式控制制是藉由在佇列中放置傳送要求來維護的。
當接收緩衝區已滿時，TCP/IP 堆疊保證傳送將不會完成，直到佇列維修維護流量控制為止。

連接資料的 Windows 篩選平台 (WFP) 注標中的 TCP 快速路徑回送連線，必須採用非優化的緩慢路徑進行回送。
因此，WFP 篩選器會防止使用這個新的回送快速路徑。
啟用 WFP 篩選器時，系統會使用慢速路徑，即使已設定 **SIO \_ 回送 \_ FAST \_ 路徑** IOCTL 也一樣。
這可確保使用者模式應用程式具有完整的 WFP 安全性功能。

預設會停用 **SIO \_ 回送 \_ FAST \_ 路徑**。

當使用 **SIO \_ 回送 \_ FAST \_ 路徑** IOCTL 來啟用通訊端上的回送快速路徑時，僅支援 tcp/ip 通訊端選項的子集。
支援的選項清單包括下列各項：

* **IP \_ TTL**
* **IP \_ 單播（ \_ 如果**
* **IPV6 \_ 單播 \_ 躍點**
* **IPV6 \_ 單播 \_ IF**
* **IPV6 \_ V6ONLY**
* **因此 \_ 條件 \_ 接受**
* **\_EXCLUSIVEADDRUSE**
* **因此， \_ 埠擴充 \_ 性**
* **\_RCVBUF**
* **\_REUSEADDR**
* **TCP \_ BSDURGENT**

## <a name="see-also"></a>另請參閱

[**IPPROTO_IP 通訊端選項**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**IPPROTO_IPV6 通訊端選項**](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[**IPPROTO_TCP 通訊端選項**](/windows/desktop/winsock/ipproto-tcp-socket-options)

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOL_SOCKET 通訊端選項**](/windows/desktop/winsock/sol-socket-socket-options)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

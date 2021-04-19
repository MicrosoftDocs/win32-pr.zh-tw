---
description: 控制項程式碼會將重新導向記錄設定為用於連接重新導向服務的新 TCP 通訊端。
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS 控制碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981018"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a>SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS 控制碼

## <a name="description"></a>Description

**SIO \_ SET WFP 連線重新 \_ \_ \_ 導向 \_ 記錄** 控制程式代碼會將重新導向記錄設定為用於連接到最終目的地的新 TCP 通訊端，以供 Windows 篩選平台 (WFP) 重新導向服務使用。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a>參數

### <a name="s"></a>s

識別通訊端的描述元。

### <a name="dwiocontrolcode"></a>dwIoControlCode

作業的控制項程式碼。
使用 **SIO 設定此作業的 \_ \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數包含與通訊端相關聯的 WFP 重新導向記錄指標。

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
| **WSA \_ IO \_ 暫止** | 重迭的 i/o 作業正在進行中。 如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。 |
| **已 \_ 中止 WSA 作業 \_** | I/o 作業因為執行緒結束或應用程式要求而中止。 如果因為通訊端關閉或 **SIO_FLUSH** IOCTL 命令的執行而取消重迭的作業，就會傳回此錯誤。 |
| **WSAEACCES** | 嘗試以存取權限禁止的方式存取通訊端。 這項錯誤會在包含下列各項的條件下傳回：使用者缺少本機電腦上所需的系統管理許可權，或應用程式未在增強型 shell 中執行，因為內建的系統管理員 (`RunAs administrator`) 。 |
| **WSAEFAULT** | 系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。 *LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。 |
| **WSAEINPROGRESS** | 正在執行封鎖作業。 如果回呼正在進行中，就會傳回此錯誤。 |
| **WSAEINTR** | 呼叫 **WSACancelBlockingCall** 時，封鎖作業中斷。 當封鎖作業中斷時，就會傳回此錯誤。 |
| **WSAEINVAL** | 提供的引數無效。 如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。 |
| **WSAENETDOWN** | 通訊端作業遇到停止的網路。 如果網路子系統失敗，就會傳回此錯誤。 |
| **WSAENOTSOCK** | 嘗試對不是通訊端的某個作業進行作業。 如果 *描述項不是套* 接字，就會傳回此錯誤。 |
| **WSAEOPNOTSUPP** | 所參考的物件類型不支援所嘗試的操作。 如果不支援指定的 IOCTL 命令，則會傳回此錯誤。 如果傳輸提供者不支援 **SIO \_ SET \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL，也會傳回此錯誤。 |

## <a name="remarks"></a>備註

Windows 8、Windows Server 2012 和更新版本的作業系統都支援 **SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL。

WFP 允許存取 TCP/IP 封包處理路徑，也就是傳出和傳入的封包可以進行檢查或變更，然後再讓它們進一步處理。
藉由使用 TCP/IP 處理路徑，獨立軟體廠商 (Isv) 可以更輕鬆地建立防火牆、防毒軟體、診斷軟體及其他類型的應用程式和服務。
WFP 提供使用者模式和核心模式元件，讓協力廠商 Isv 可以參與在 TCP/IP 通訊協定堆疊和整個作業系統中的數個層級進行的篩選決策。
[WFP 連接重新導向] 功能可讓 WFP 標注核心驅動程式將連接重新導向至使用者模式進程、在使用者模式中執行內容檢查，以及使用不同的連線將已檢查的內容轉送到原始目的地。

**SIO \_ SET \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 和數個其他相關 IOCTLS 是使用者模式元件，可用來允許多個以 WFP 為基礎的連線 proxy 應用程式以合作方式檢查相同的流量流程。
每個檢查代理程式都可以安全地重新檢查已由另一個檢查代理程式檢查的網路流量。
由於有多個 proxy (由不同的 Isv 開發，例如) 某個 proxy 用來與最終目的地通訊的連線，可能會被第二個 proxy 重新導向，而且原始 proxy 可以再次重新導向新的連接。
如果沒有連線追蹤，原始連接可能永遠不會到達它的最終目的地，因為它卡在無限的 proxy 迴圈中。

**SIO \_ SET \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 可用來在重新導向的通訊端連線上提供代理的連接追蹤。
這種 WFP 功能可從連接的初始重新導向到目的地的最終連接，來協助追蹤重新導向記錄。

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)的 IOCTL 會由 WFP 型重新導向服務用來從已接受的 tcp/ip 封包連線取得重新導向記錄， (tcp 通訊端或 UDP 通訊端的已連接通訊端，例如，) 透過在核心模式驅動程式中的 **ALE \_ 連接重新 \_ 導向** 層所註冊的隨附核心模式注標重新導向至該連接。
[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)的 IOCTL 會取得重新導向記錄的重新導向內容，這是使用的。
重新導向內容是選擇性的，如果連接目前的重新導向狀態是由呼叫重新導向服務重新導向連接，或先前被呼叫重新導向服務重新導向，但稍後又由不同的重新導向服務重新導向，則會使用。重新導向服務會使用 **SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL，將抓取的重新導向記錄傳輸至它用來 proxy 原始內容的 TCP 通訊端。

呼叫 **SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 的應用程式不需要瞭解包含要設定之重新導向記錄的 blob。
這是不透明的資料 blob，應用程式必須將其傳回至新的通訊端。

## <a name="see-also"></a>另請參閱

[**IPPROTO_IP 通訊端選項**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

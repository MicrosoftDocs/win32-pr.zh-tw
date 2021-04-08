---
description: 當連接的理想傳送待處理專案值變更時，控制項程式碼會通知應用程式。
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: SIO_IDEAL_SEND_BACKLOG_CHANGE 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692212"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a>SIO_IDEAL_SEND_BACKLOG_CHANGE 控制程式代碼

## <a name="description"></a>Description

**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更控制程式碼會在理想的傳送待處理專案 (ISB) 值變更時通知應用程式。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
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
針對此作業，請使用 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數未用來進行這項操作。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。此參數未用來進行這項操作。

### <a name="lpvoutbuffer"></a>lpvOutBuffer

輸出緩衝區的指標。
此參數未用來進行這項操作。

### <a name="cboutbuffer"></a>cbOutBuffer

輸出緩衝區的大小（以位元組為單位）。
此參數必須設定為零。

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。
這項作業的傳回參數指向 **DWORD** 值零，因為沒有任何輸出。

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

[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。
在 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。

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
| **WSA \_ IO \_ 暫止** | 已成功起始重迭的作業，並會在稍後指出完成的時間。 |
| **已 \_ 中止 WSA 作業 \_** | 因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行，重迭的作業已取消。 |
| **WSAEFAULT** | *LpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。 |
| **WSAEINPROGRESS** | 當回呼正在進行時，就會叫用此函數。 |
| **WSAEINTR** | 封鎖作業已中斷。 |
| **WSAEINVAL** | *DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。 如果 *cbOutBuffer* 參數不是零，就會傳回此錯誤。 |
| **WSAENETDOWN** | 網路子系統失敗。 |
| **WSAENOPROTOOPT** | 指定的通訊協定不支援通訊端選項。 |
| **WSAENOTCONN** | *通訊端未連線*。 |
| **WSAENOTSOCK** | *描述項不是* 通訊端。 |
| **WSAEOPNOTSUPP** | 不支援指定的 IOCTL 命令。 如果傳輸提供者不支援 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL，則會傳回此錯誤。 當嘗試在資料包通訊端上進行使用 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 時，也會傳回此錯誤。 |

## <a name="remarks"></a>備註

Windows Server 2008、Windows Vista Service Pack 1 (SP1) 和更新版本的作業系統都支援 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL。

使用 Windows sockets 透過 TCP 連線傳送資料時，請務必保留足夠的資料量， (傳送但尚未認可到 TCP 中的) ，以達到最高的輸送量。
若要達到 TCP 連接的最佳輸送量，最理想的資料量值就稱為「理想的傳送待處理專案」 (ISB) 大小。
ISB 值是 TCP 連線之頻寬延遲乘積的函式，而接收者的通告接收視窗 (以及網路) 中的擁塞量部分。

您可以從 Windows Server 2008、Windows Vista SP1 和更新版本的作業系統中的 TCP 通訊協定，取得每個連接的 ISB 值。
**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 可供應用程式使用，以在 ISB 值針對連接動態變更時取得通知。

在 Windows Server 2008、Windows Vista （含 SP1）及更新版本的作業系統上， **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案（backlog）變更和 [**SIO \_ 理想的 \_ 傳送 \_ 待 \_**](sio-ideal-send-backlog-query.md) 處理專案（backlog）查詢 IOCTLs 可在已線上狀態的資料流程導向通訊端上受到支援。

TCP 連接的 ISB 值範圍理論上可能會因0到 16 mb 而異。

請參閱 [**SIO \_ 理想的 \_ 傳送 \_ 待 \_**](sio-ideal-send-backlog-query.md) 處理專案查詢 IOCTL 參考頁面，以取得 ISB 機制的一般使用方式，以透過高頻寬延遲的產品連線達到更佳的輸送量。

只有在已線上狀態的資料流程通訊端上，才允許 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL。
否則， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式將會失敗，並出現 **WSAENOTCONN**。

**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 在基礎連接上發生 ISB 變更之前，不會使用輸入或輸出緩衝區和 pends 或區塊。
當這個 IOCTL 完成時，Winsock 應用程式可以使用 [**SIO 理想的傳送待處理專案（ \_ \_ \_ BACKLOG） \_ 查詢**](sio-ideal-send-backlog-query.md) IOCTL 來取得連接上的新 ISB 值。

**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 不支援非封鎖模式。
允許應用程式在非封鎖通訊端上發出這個 IOCTL，但在 ISB 值變更之前，只會封鎖或暫止 IOCTL。

如果 *lpOverlapped* 和 *lpCompletionRoutine* 參數都是 Null，則會將此函式中的通訊端視為非重迭的通訊端。
若為非重迭的通訊端，則會忽略 *lpOverlapped* 和 *lpCompletionRoutine* 參數，不同之處在于如果通訊端 *s* 處於封鎖模式，函數可以封鎖。
如果通訊端 *s* 處於非封鎖模式中，此函式仍會封鎖，因為這個特定的 IOCTL 不支援非封鎖模式。

針對重迭的通訊端，將會起始無法立即完成的作業，並會在稍後指出完成的時間。

任何 IOCTL 可能會無限期地封鎖，視服務提供者的執行而定。
如果應用程式無法容忍 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式呼叫中的封鎖，則會建議對可能封鎖的 IOCTLs 進行重迭的 i/o。

**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 會提供通知，在 ISB 值變更之前，預期會封鎖或暫止。
因此，通常會以非同步方式呼叫 *lpOverlapped* 參數，並將其設定為有效的 WSAOVERLAPPED 結構。

**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 可能會失敗，並在下列情況下 **\_ \_ 中止** **WSAEINTR** 或 WSA 作業：

* TCP 連接會正常地在傳送方向中斷連線。 這可能是因為呼叫 shutdown 函式，並將參數設定為 **SD \_ SEND**、呼叫 **DisconnectEx** 函式，或是呼叫 **TransmitFile** 或 **TransmitPackets** 函式（ *dwFlags* 參數設定為 **tf \_ DISCONNECT** 或 **tf \_ 重複使用**）的結果。
* TCP 連接已重設或中止。
* 當已經有暫止的通知要求時，應用程式會發出 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL。 一次只允許 1 1 暫止的 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更要求。
* I/o 管理員會取消要求。
* 通訊端已關閉。

這些 IOCTLs 的兩個內嵌包裝函式是在 *Ws2tcpip .h* 標頭檔中定義。
建議使用這些內嵌函式，而不是使用 **SIO 理想的 \_ \_ 傳送 \_ 待 \_** 處理專案變更和 [**SIO 理想的傳送待處理專案 \_ \_ \_ （backlog） \_ 查詢**](sio-ideal-send-backlog-query.md) IOCTLs。

**SIO \_ 理想 \_ 傳送 \_ 待辦專案 \_ 變更** IOCTL 的內嵌包裝函式是 **idealsendbacklognotify** 函數。

[**SIO \_ 理想 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢**](sio-ideal-send-backlog-query.md)IOCTL 的內嵌包裝函式是 **idealsendbacklogquery** 函數。

## <a name="see-also"></a>另請參閱

[**SIO_IDEAL_SEND_BACKLOG_QUERY**](sio-ideal-send-backlog-query.md)

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

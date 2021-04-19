---
description: 控制項程式碼會抓取基礎連接的理想傳送待辦專案值。
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: SIO_IDEAL_SEND_BACKLOG_QUERY 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971516"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a>SIO_IDEAL_SEND_BACKLOG_QUERY 控制程式代碼

## <a name="description"></a>Description

**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案查詢控制項程式碼會針對基礎連接，取得理想的傳送待處理專案 (ISB) 值。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
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
使用 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案查詢進行此作業。

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
| **WSAEFAULT** | *LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。 |
| **WSAEINPROGRESS** | 當回呼正在進行時，就會叫用此函數。 |
| **WSAEINTR** | 封鎖作業已中斷。 |
| **WSAEINVAL** | *DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。 如果 *cbOutBuffer* 參數小於 **ULONG** 資料類型的大小，就會傳回此錯誤。
| **WSAENETDOWN** | 網路子系統失敗。 |
| **WSAENOPROTOOPT** | 指定的通訊協定不支援通訊端選項。 |
| **WSAENOTCONN** | 通訊端未連線。 |
| **WSAENOTSOCK** | *描述項不是* 通訊端。 |
| **WSAEOPNOTSUPP** | 不支援指定的 IOCTL 命令。 如果傳輸提供者不支援 **SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL，則會傳回此錯誤。 嘗試使用 **SIO \_ 理想的傳送待處理專案 \_ \_ （BACKLOG） \_ 查詢** IOCTL 是在資料包通訊端上進行時，也會傳回此錯誤。 |

## <a name="remarks"></a>備註

Windows Server 2008、Windows Vista Service Pack 1 (SP1) 和更新版本的作業系統都支援 **SIO \_ 理想的傳送待處理專案 \_ \_ （BACKLOG） \_ 查詢** IOCTL。

使用 Windows sockets 透過 TCP 連線傳送資料時，請務必保留足夠的資料量， (傳送但尚未認可到 TCP 中的) ，以達到最高的輸送量。
若要達到 TCP 連接的最佳輸送量，最理想的資料量值就稱為「理想的傳送待處理專案」 (ISB) 大小。
ISB 值是 TCP 連線之頻寬延遲乘積的函式，而接收者的通告接收視窗 (以及網路) 中的擁塞量部分。

您可以從 Windows Server 2008、Windows Vista SP1 和更新版本的作業系統中的 TCP 通訊協定，取得每個連接的 ISB 值。
**SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 可供應用程式用來在 ISB 值針對連接動態變更時取得通知。

在 Windows Server 2008、Windows Vista （含 SP1）及更新版本的作業系統上， [**SIO \_ 理想的 \_ 傳送 \_ 待 \_**](sio-ideal-send-backlog-change.md) 處理專案（backlog）變更和 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案（backlog）查詢 IOCTLs 可在已線上狀態的資料流程導向通訊端上受到支援。

TCP 連接的 ISB 值範圍理論上可能會因0到 16 mb 而異。

[**SIO 理想的傳送待處理 \_ 專案 \_ \_ \_ 變更**](sio-ideal-send-backlog-change.md)和 **SIO 理想的 \_ 傳送待處理專案 \_ \_ （backlog） \_ 查詢** IOCTLs 是根據應用程式所使用的傳送方法。
討論兩個常見的案例。

一次執行一個封鎖或非封鎖傳送要求的應用程式，通常會依賴 Winsock 的內部傳送緩衝處理，以達到較佳的輸送量。
給定連接的傳送緩衝區限制是由 **SO \_ SNDBUF** 通訊端選項控制。
對於封鎖和非封鎖傳送方法，傳送緩衝區限制會決定 TCP 中保留的資料量。
如果連接的 ISB 值大於傳送緩衝區限制，則在連接上達成的輸送量將不會是最佳的。
為了達到較佳的輸送量，應用程式可以根據 ISB 查詢的結果設定傳送緩衝區限制，因為連接上發生 ISB 變更通知。

針對使用重迭傳送方法的應用程式，如果有多個未處理的傳送要求，TCP 中未完成的資料量會由 Winsock 中的傳送緩衝區限制和未處理的重迭傳送要求中包含的總數據量來決定。
在此情況下，應用程式應該使用 ISB 值來判斷它們應該保留多少未處理的傳送要求，以及每個傳送要求的資料大小。
在理想的情況下，應用程式應該嘗試保持下列方程式的滿意：

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

請注意，以上述方式使用 ISB IOCTLs over TCP 通訊端可能會導致 exchange 中的記憶體使用量增加，以增加頻寬延遲最高的連接輸送量。
Windows 中的 TCP 執行會根據整體系統記憶體使用量，視需要節流 ISB 值。

**SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 只允許在處於已連接狀態的資料流程通訊端上。
否則， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式將會失敗，並出現 **WSAENOTCONN**。

任何 IOCTL 可能會無限期地封鎖，視服務提供者的執行而定。
如果應用程式無法容忍 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式呼叫中的封鎖，則會建議對可能封鎖的 IOCTLs 進行重迭的 i/o。

**SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 不太可能會封鎖，因此通常會在 *lpOverlapped* 和 *lpCompletionRoutine* 參數設定為 **Null** 的情況下同步呼叫。

**SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 可能會失敗，並在下列情況下 **\_ \_ 中止** **WSAEINTR** 或 WSA 作業：

TCP 連接會正常地在傳送方向中斷連線。
這可能是因為呼叫 shutdown 函式，並將參數設定為 **SD \_ SEND**、呼叫 **DisconnectEx** 函式，或是呼叫 **TransmitFile** 或 **TransmitPackets** 函式（ *dwFlags* 參數設定為 **tf \_ DISCONNECT** 或 **tf \_ 重複使用**）的結果。
TCP 連接已重設或中止。
I/o 管理員會取消要求。

這些 IOCTLs 的兩個內嵌包裝函式是在 *Ws2tcpip .h* 標頭檔中定義。
建議使用這些內嵌函式，而不是使用 [**SIO 理想的 \_ \_ 傳送 \_ 待 \_**](sio-ideal-send-backlog-change.md) 處理專案變更和 **SIO 理想的傳送待處理專案 \_ \_ \_ （backlog） \_ 查詢** IOCTLs。

[**SIO \_ 理想 \_ 傳送 \_ 待辦專案 \_ 變更**](sio-ideal-send-backlog-change.md)IOCTL 的內嵌包裝函式是 **idealsendbacklognotify** 函數。

**SIO \_ 理想 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 的內嵌包裝函式是 **idealsendbacklogquery** 函數。

在 Windows 7 和 Windows Server 2008 R2 上新增了 TCP 的動態傳送緩衝。
除非應用程式在資料流程通訊端上設定 **\_ SNDBUF** 通訊端選項，否則預設會啟用 TCP 的動態傳送緩衝。

使用 netsh 是查詢或設定 TCP 動態傳送緩衝的建議方法。

您可以使用下列命令來抓取 TCP 動態傳送緩衝的目前值：

`netsh winsock show autotuning`

您可以使用下列命令來停用 TCP 的動態傳送緩衝：

`netsh winsock set autotuning off`

您可以使用下列命令來啟用 TCP 的動態傳送緩衝：

`netsh winsock set autotuning on`

雖然不建議這麼做，您可以藉由將下列登錄值設定為零，從應用程式停用動態傳送緩衝：

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

使用 NetSh.exe 變更動態傳送緩衝的值或變更登錄值時，必須重新開機電腦，變更才會生效。

在 Windows 7 和 Windows Server 2008 R2 上使用動態傳送緩衝處理， [**SIO 理想的 \_ 傳送 \_ \_ 待 \_**](sio-ideal-send-backlog-change.md) 處理專案變更和 **SIO 理想的傳送待處理專案（ \_ \_ \_ backlog） \_ 查詢** IOCTLs 只有在特殊情況下才需要使用。

## <a name="see-also"></a>另請參閱

[**SIO_IDEAL_SEND_BACKLOG_CHANGE**](sio-ideal-send-backlog-change.md)

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

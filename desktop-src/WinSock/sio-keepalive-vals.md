---
description: 控制項程式碼會啟用或停用 TCP keep-alive 選項的每一連接設定，以指定 TCP keep-alive timeout 和 interval。
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: SIO_KEEPALIVE_VALS 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114904"
---
# <a name="sio_keepalive_vals-control-code"></a>SIO_KEEPALIVE_VALS 控制程式代碼

## <a name="description"></a>Description

**SIO \_ KEEPALIVE \_ VALS** control 程式碼會啟用或停用 tcp keep-alive 選項的每一連接設定，以指定 tcp 保持連線的超時和間隔。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
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
使用 **SIO \_ KEEPALIVE \_ VALS** 進行此作業。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數應指向 **tcp \_ keepalive** 結構。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。
此參數應等於或大於 *lpvInBuffer* 參數所指向之 **tcp \_ keepalive** 結構的大小。

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
|**WSA \_ IO \_ 暫止** | 已成功起始重迭的作業，並會在稍後指出完成的時間。 |
| **已 \_ 中止 WSA 作業 \_** | 因為通訊端關閉或 **SIO_FLUSH IOCTL** 命令的執行，所以重迭的作業已取消。 |
| **WSAEFAULT** | *LpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。 |
| **WSAEINPROGRESS** | 當回呼正在進行時，就會叫用此函數。 |
| **WSAEINTR** | 封鎖作業已中斷。 |
| **WSAEINVAL** | *DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。 |
| **WSAENETDOWN** | 網路子系統失敗。 |
| **WSAENOPROTOOPT** | 指定的通訊協定不支援通訊端選項。 資料包通訊端會傳回這個錯誤。 |
| **WSAENOTSOCK** | 描述項不是通訊端。 |
| **WSAEOPNOTSUPP** | 不支援指定的 IOCTL 命令。 如果傳輸提供者不支援 **SIO \_ KEEPALIVE \_ VALS** IOCTL，則會傳回此錯誤。 |

## <a name="remarks"></a>備註

在 Windows 2000 和更新版本的作業系統上，支援 **SIO \_ KEEPALIVE \_ VALS** IOCTL。

**SIO \_ KEEPALIVE \_ VALS** control 程式碼會啟用或停用 tcp keep-alive 選項的每個連線設定，以指定 tcp keep-alive 封包所使用的 tcp keep-alive timeout 和間隔。
如需保持連線選項的詳細資訊，請參閱4.2.3.6 中的「網際網路主機需求」一節：在 [IETF 網站](https://www.ietf.org/rfc/rfc1122.txt)提供的 RFC 1122 中所指定的通訊層。
 (此資源可能僅提供英文版。 ) 

*LpvInBuffer* 參數應指向 *Mstcpip .h* 標頭檔中定義的 **tcp \_ keepalive** 結構。
此結構的定義如下：

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

**Onoff** 成員中指定的值會決定是否啟用或停用 TCP 保持連線。
如果 **onoff** 成員設定為非零值，則會啟用 TCP 保持運作，並使用結構中的其他成員。
**Keepalivetime** 成員會指定在第一個 keep-alive 封包傳送之前沒有任何活動的超時時間（以毫秒為單位）。
**Keepaliveinterval** 成員會指定在未收到任何通知時，連續的 keep-alive 封包傳送的間隔（以毫秒為單位）。

[**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)選項（這是其中一個 [**SOL_SOCKET 通訊端選項**](/windows/desktop/winsock/sol-socket-socket-options)）也可用來啟用或停用連接上的 TCP keep-alive，以及查詢此選項的目前狀態。
若要查詢通訊端上是否啟用 TCP keep-alive，可以使用 [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) 選項來呼叫 getsockopt 函數。
若要啟用或停用 TCP keep-alive，可以使用 [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)選項來呼叫 **setsockopt** 函數。
如果已啟用 [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)的 tcp keep-alive，則預設 TCP 設定會用於 keep-alive timeout 和 interval，除非使用 **SIO \_ KEEPALIVE \_ VALS** 變更這些值。

Keep-alive timeout 的預設全系統值可透過 [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) 登錄設定來控制，此設定會採用以毫秒為單位的值。 如果未設定索引鍵，則預設的 keep-alive timeout 為2小時。
Keep-alive 間隔的預設全系統值可透過 [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) 登錄設定來控制，此設定會採用以毫秒為單位的值。 如果未設定索引鍵，則預設的 keep-alive 間隔為1秒。

在 Windows Vista 和更新版本上， (資料重新傳輸) 的 keep-alive 探查數目設定為10，而且無法變更。

在 Windows Server 2003、Windows XP 及 Windows 2000 上，保持運作探查數目的預設設定為5。
Keep-alive 探查的數目可透過 **TcpMaxDataRetransmissions** 和 [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) 登錄設定來控制。
Keep-alive 探查的數目會設定為兩個登錄機碼值的較大值。
如果這個數位為0，則不會傳送 keep-alive 探查。
如果此數位大於255，則會調整為255。

## <a name="see-also"></a>另請參閱

[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))

[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))

[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))

[插座](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

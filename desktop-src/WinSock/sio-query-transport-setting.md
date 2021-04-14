---
description: 控制項程式碼會查詢通訊端上的傳輸設定。
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: SIO_QUERY_TRANSPORT_SETTING 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848634"
---
# <a name="sio_query_transport_setting-control-code"></a>SIO_QUERY_TRANSPORT_SETTING 控制程式代碼

## <a name="description"></a>Description

**SIO \_ QUERY \_ 傳輸 \_ 設定** 控制程式代碼會查詢通訊端上的傳輸設定。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
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
使用 **SIO \_ 查詢 \_ 傳輸 \_ 設定** 進行此作業。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數包含結構的指標，其中結構的第一個成員是 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) 結構，可判斷正在查詢的傳輸設定。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。
此參數取決於正在查詢的傳輸設定。

### <a name="lpvoutbuffer"></a>lpvOutBuffer

輸出緩衝區的指標。
如果 *lpOverlapped* 和 *LpCompletionRoutine* 參數為 **Null**，則此參數取決於正在查詢的傳輸設定。

### <a name="cboutbuffer"></a>cbOutBuffer

輸出緩衝區的大小（以位元組為單位）。

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
| **WSA \_ IO \_ 暫止** | 已成功起始重迭的作業，並會在稍後指出完成的時間。 |
| **已 \_ 中止 WSA 作業 \_** | 因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行，重迭的作業已取消。 |
| **WSAEFAULT** | *LpvOutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。 |
| **WSAEINPROGRESS** | 當回呼正在進行時，就會叫用此函數。 |
| **WSAEINTR** | 封鎖作業已中斷。 |
| **WSAEINVAL** | *DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。 |
| **WSAENETDOWN** | 網路子系統失敗。 |
| **WSAENOPROTOOPT** | 指定的通訊協定不支援通訊端選項。 |
| **WSAENOTCONN** | 通訊端未連線。 |
| **WSAENOTSOCK** | 描述項不是通訊端。 |
| **WSAEOPNOTSUPP** | 不支援指定的 IOCTL 命令。 如果傳輸提供者不支援 **SIO \_ 查詢 \_ 傳輸 \_ 設定** IOCTL，則會傳回此錯誤。 |

## <a name="remarks"></a>備註

Windows 8、Windows Server 2012 和更新版本的作業系統都支援 **SIO \_ 查詢 \_ 傳輸 \_ 設定** 的 IOCTL。

**SIO \_ 查詢 \_ 傳輸 \_ 設定** IOCTL 是一般的 ioctl，用來查詢通訊端上的傳輸設定。
正在查詢的傳輸設定是以 *lpvInBuffer* 參數中傳遞的 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)為基礎。

目前唯一定義的傳輸設定是用於 TCP 通訊端上的 **即時 \_ \_ 通知 \_ 功能** 功能。

如果傳入 *lpvInBuffer* 參數的 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)將 Guid 成員設為 **即時 \_ \_ 通知 \_ 功能**，則這是要求查詢與 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)搭配使用的 TCP 通訊端即時通知設定，以在 Windows Store 應用程式中接收背景網路通知。
*LpvInBuffer* 參數應指向 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)結構。
*LpvOutBuffer* 參數應指向 **即時 \_ \_ 通知 \_ 設定 \_ 輸出** 結構。
此傳輸設定只適用于 TCP 通訊端。
此傳輸設定提供一種方式，讓 WinInet 或類似的網路服務查詢指定的 TCP 通訊端，以判斷 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) 狀態。
Windows Store 應用程式不會直接呼叫這個 IOCTL。
如果 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 呼叫成功，這個 IOCTL 會以目前的狀態傳回 **即時 \_ \_ 通知 \_ 設定 \_ 輸出** 結構。

**SIO \_ QUERY \_ 傳輸 \_ 設定** IOCTL 提供一種方式，可讓 WinInet 或類似的網路服務查詢指定 TCP 通訊端的傳輸設定狀態，以判斷是否已在通訊端上啟用 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) 。
Windows Store 應用程式不會直接呼叫這個 IOCTL。

這個 IOCTL 只適用于 TCP 通訊端。

## <a name="see-also"></a>另請參閱

[**CONTROL_CHANNEL_TRIGGER_STATUS**](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[**SIO_APPLY_TRANSPORT_SETTING**](sio-apply-transport-setting.md)

[插座](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

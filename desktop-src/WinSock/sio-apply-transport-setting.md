---
description: 控制項程式碼會將一或多個傳輸設定套用至通訊端。
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: SIO_APPLY_TRANSPORT_SETTING 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977830"
---
# <a name="sio_apply_transport_setting-control-code"></a>SIO_APPLY_TRANSPORT_SETTING 控制程式代碼

## <a name="description"></a>Description

**SIO 套用 \_ \_ 傳輸 \_ 設定** 控制程式代碼會將一或多個傳輸設定套用至通訊端。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
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
使用 **SIO \_ 適用于此作業的 \_ 傳輸 \_ 設定** 。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數包含結構的指標，其中結構的第一個成員是 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) 結構，可判斷要套用的傳輸設定。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。
此參數取決於所套用的傳輸設定。

### <a name="lpvoutbuffer"></a>lpvOutBuffer

輸出緩衝區的指標。
此參數取決於所套用的傳輸設定。

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
|**WSA \_ IO \_ 暫止** | 重迭的 i/o 作業正在進行中。 如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。 |
| **已 \_ 中止 WSA 作業 \_** | I/o 作業因為執行緒結束或應用程式要求而中止。 如果因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行而取消重迭的作業，就會傳回此錯誤。 |
| **WSAEFAULT** | 系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。 *LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。 |
| **WSAEINPROGRESS** | 正在執行封鎖作業。 如果回呼正在進行中，就會傳回此錯誤。 |
| **WSAEINTR** | 呼叫 [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)時，封鎖作業中斷。 當封鎖作業中斷時，就會傳回此錯誤。 |
| **WSAEINVAL** | 提供的引數無效。 如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。 |
| **WSAENETDOWN** | 通訊端作業遇到停止的網路。 如果網路子系統失敗，就會傳回此錯誤。 |
| **WSAENOTSOCK** | 嘗試對不是通訊端的某個作業進行作業。 如果 *描述項不是套* 接字，就會傳回此錯誤。 |
| **WSAEOPNOTSUPP** | 所參考的物件類型不支援所嘗試的操作。 如果不支援指定的 IOCTL 命令，則會傳回此錯誤。 如果傳輸提供者不支援 **SIO \_ APPLY \_ 傳輸 \_ 設定** IOCTL，也會傳回此錯誤。 當嘗試在 UDP 或 TCP 以外的通訊端上進行使用 **SIO 套用 \_ \_ 傳輸 \_ 設定** 時，也會傳回此錯誤。 |

## <a name="remarks"></a>備註

Windows 8、Windows Server 2012 和更新版本的作業系統都支援 **SIO 套用 \_ \_ 傳輸 \_ 設定** 的 IOCTL。

**SIO 套用 \_ \_ 傳輸 \_ 設定** IOCTL 是用來將傳輸設定套用至通訊端的一般 IOCTL。
所要套用的傳輸設定是以 *lpvInBuffer* 參數中傳遞的 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)為基礎。

從 Windows 8 和 Windows Server 2012 開始，系統會定義 TCP 通訊端上的 **REAL_TIME_NOTIFICATION_CAPABILITY** 功能。
從 Windows 10 和 Windows Server 2016 開始，也會定義 **\_ NAMERES \_ 內容的關聯** 。
如需詳細資訊，請參閱 [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) 和 [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input)。

如果在 lpvInBuffer 參數中傳遞的 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) 將 Guid 成員設為 **即時 \_ \_ 通知 \_ 功能**，則這是要求套用適用于 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) 的 TCP 通訊端的即時通知設定，以在 Windows Store 應用程式中接收背景網路通知。
*LpvInBuffer* 參數應指向 **REAL_TIME_NOTIFICATION_SETTING_INPUT** 結構。
此作業未使用 *lpvOutBuffer* 參數。
此傳輸設定只適用于 TCP 通訊端。
此傳輸設定提供一種方式，讓 WinInet 或類似的網路服務將指定的 TCP 通訊端標示為已啟用 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) 。
當呼叫這個選項時，Windows 會標示對應的 TCP 通訊端，並設定適當的硬體和軟體設定。
Windows Store 應用程式不會直接呼叫這個 IOCTL。

## <a name="see-also"></a>另請參閱

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[插座](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SIO_QUERY_TRANSPORT_SETTING**](sio-query-transport-setting.md)

[**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

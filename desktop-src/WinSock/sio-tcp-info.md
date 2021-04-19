---
description: 控制項程式碼會抓取傳輸控制通訊協定， (指定之通訊端的 TCP) 統計資料。
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: SIO_TCP_INFO 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: cea9a2d31654d1263f285ee9967b24700fe25138
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106992246"
---
# <a name="sio_tcp_info-control-code"></a>SIO_TCP_INFO 控制程式代碼

## <a name="description"></a>Description

**SIO \_ tcp \_ 資訊** 控制程式代碼會抓取傳輸控制通訊協定， (指定之通訊端的 TCP) 統計資料。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
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
使用 **SIO \_ TCP \_ 資訊** 進行這種操作。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數包含 **DWORD** 的指標，可指定您所使用的 **SIO \_ TCP \_ 資訊** 控制程式代碼版本。 指定0會使用 [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0)。 指定1可使用 [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1)，povides 更多欄位。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。
此參數應為 **DWORD** 資料類型的大小。

### <a name="lpvoutbuffer"></a>lpvOutBuffer

輸出緩衝區的指標。
成功輸出時，此參數會包含 [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) 結構的指標，其中包含指定之通訊端的 TCP 統計資料。

### <a name="cboutbuffer"></a>cbOutBuffer

輸出緩衝區的大小（以位元組為單位）。
此參數必須至少為 [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) 結構的大小。

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
| **WSAEMSGSIZE** | 輸入緩衝區的指標為 **Null**，或輸入緩衝區的指定大小不正確。 |
| **WSAEINVAL** | 提供的引數無效。 如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。 |

## <a name="remarks"></a>備註

與使用 [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) 函式來抓取 tcp 統計資料不同的是，使用這個控制項程式碼來抓取 tcp 統計資料並不需要使用者程式碼來載入、儲存和篩選 tcp 連接資料表，也不需要使用較高的許可權。

## <a name="see-also"></a>另請參閱

[插座](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

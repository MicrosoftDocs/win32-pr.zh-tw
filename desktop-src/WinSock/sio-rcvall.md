---
description: 控制項程式碼可讓通訊端接收透過網路介面傳遞的所有 IPv4 或 IPv6 封包。
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: SIO_RCVALL 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973638"
---
# <a name="sio_rcvall-control-code"></a>SIO_RCVALL 控制程式代碼

## <a name="description"></a>Description
**SIO \_ RCVALL** control 程式碼可讓通訊端接收透過網路介面傳遞的所有 IPv4 或 IPv6 封包。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>參數

### <a name="s"></a>s

識別通訊端的描述元。

### <a name="dwiocontrolcode"></a>dwIoControlCode

作業的控制項程式碼。
使用 **SIO \_ RCVALL** 進行此作業。

### <a name="lpvinbuffer"></a>lpvInBuffer

應包含選項值之輸入緩衝區的指標。
**SIO \_ RCVALL** IOCTL 選項的可能值是在 *Mstcpip .h* 標頭檔中定義的 **RCVALL_VALUE** 列舉中指定。

**SIO \_ RCVALL** 的可能值如下：

| 值 | 意義 |
|-------|---------|
| **RCVALL \_ 關閉** | 停用此選項，讓通訊端不會收到透過網路介面傳遞的所有 IPv4 或 IPv6 封包。 |
| **RCVALL \_ 于** | 啟用此選項，讓通訊端接收透過網路介面傳遞的所有 IPv4 或 IPv6 封包。 如果 NIC 支援混合模式，此選項會在網路介面卡上啟用混合模式 (NIC) 。 在網路中樞的 LAN 區段上，支援混合模式的 NIC 會在 LAN 上捕捉所有 IPv4 或 IPv6 流量，包括相同 LAN 區段上其他電腦之間的流量。 所有 (IPv4 或 IPv6 的已捕捉封包，視通訊端) 將會傳遞至原始通訊端而定。 此選項不會將其他封包捕獲 (ARP、IPX 和 NetBEUI 封包，例如介面上的) 。 Netmon 針對網路介面使用相同的模式，但不會使用此選項來捕捉流量。 |
| **RCVALL \_ SOCKETLEVELONLY** | 這項功能目前未執行，因此設定此選項不會有任何影響。 |
| **RCVALL \_ IPLEVEL** | 啟用此選項，讓 IPv4 或 IPv6 通訊端接收通過網路介面之 IP 層級的所有封包。 此選項不會在網路介面卡上啟用混合模式。 此選項只會影響在 IP 層級的封包處理。 NIC 仍只接收導向至其設定之單播和多播位址的封包。 不過，啟用此選項的通訊端不只會接收導向至特定 IP 位址的封包，而是會接收 NIC 接收的所有 IPv4 或 IPv6 封包。 此選項不會將其他封包捕捉 (ARP、IPX 和 NetBEUI 封包，例如在介面上收到) 。 |

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。
此參數應等於或大於 *lpvInBuffer* 參數所指向的 **RCVALL_VALUE** 列舉值的大小。

### <a name="lpvoutbuffer"></a>lpvOutBuffer

輸出緩衝區的指標。
此參數未用來進行這項操作。

### <a name="cboutbuffer"></a>cbOutBuffer

輸出緩衝區的大小（以位元組為單位）。
此參數未用來進行這項操作。

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。
此參數未用來進行這項操作。

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
| **WSA \_ IO \_ 暫止** | 已成功起始重迭的作業，並會在稍後指出完成的時間。 |
| **已 \_ 中止 WSA 作業 \_** | 因為通訊端關閉或 **SIO_FLUSH** IOCTL 命令的執行，所以重迭的作業已取消。 |
| **WSAEFAULT** | *LpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。 |
| **WSAEINPROGRESS** | 當回呼正在進行時，就會叫用此函數。 |
| **WSAEINTR** | 封鎖作業已中斷。 |
| **WSAEINVAL** | *DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。 如果 *cbInBuffer* 參數小於， `sizeof(UCHAR)` 或 *lpvInBuffer* 參數指向不是 **RCVALL_VALUE** 列舉值的值，也會傳回此錯誤。 如果找不到與通訊端關聯的網路介面，也可能會傳回此錯誤。 如果與通訊端相關聯的網路介面已刪除或移除 (移除 PCMCIA 或 USB 網路裝置，例如) ，就可能發生這種情況。 |
| **WSAENETDOWN** | 網路子系統失敗。 |
| **WSAENOBUFS** | 沒有可用的緩衝區空間。 |
| **WSAENOPROTOOPT** | 指定的通訊協定不支援通訊端選項。 |
| **WSAENOTSOCK** | *描述項不是* 通訊端。 |
| **WSAEOPNOTSUPP** | 不支援指定的 IOCTL 命令。 如果傳輸提供者不支援 **SIO \_ RCVALL** IOCTL，則會傳回此錯誤。 |

## <a name="remarks"></a>備註

在 Windows 2000 和更新版本的作業系統上，支援 **SIO \_ RCVALL** 的 IOCTL。

**SIO \_ RCVALL** IOCTL 可讓通訊端接收網路介面上的所有 IPv4 或 IPv6 封包。
傳遞給 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數的通訊端控制碼必須是下列其中一項：

* 以位址系列設定為 AF_INET、通訊端類型設定為 SOCK_RAW，以及將通訊協定設定為 [IPPROTO_IP] 建立的 IPv4 通訊端。
* 以位址系列設定為 AF_INET6、通訊端類型設定為 [SOCK_RAW，並將通訊協定設定為 [IPPROTO_IPV6] 建立的 IPv6 通訊端。

如需有關原始通訊端的詳細資訊，請參閱 [**Tcp/ip 原始通訊端**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)。

通訊端也必須系結至明確的本機 IPv4 或 IPv6 介面，這表示您無法系結至 **INADDR \_ any** 或 **in6addr \_ any**。

當通訊端系結且 IOCTL 順利完成之後，對 [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) 或 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 函式的呼叫會傳回通過指定 IPv4 介面傳遞的 ipv4 資料包，或傳回通過指定 ipv6 介面的 ipv6 資料包。
請注意，您必須提供夠大的緩衝區。
設定這個 IOCTL 只會在指定的介面上捕獲 IPv4 或 IPv6 封包。
這個 IOCTL 不會將其他封包捕捉 (ARP、IPX 和 NetBEUI 封包，例如介面上的) 。

使用 **SIO \_ RCVALL** IOCTL 系結至特定本機介面的通訊端，只會接收通過該介面的封包。
它不會接收在另一個介面上收到的封包，並在與 **SIO \_ RCVALL** IOCTL 系結之通訊端不同的其他介面上轉寄。

在 Windows Server 2008 及更早版本中， **SIO \_ RCVALL** IOCTL 設定不會捕捉從網路介面送出的本機封包。
這包含在另一個介面上收到的封包，並將針對 **SIO \_ RCVALL** IOCTL 指定的網路介面轉送出去。

在 Windows 7 和 Windows Server 2008 R2 上，這項變更已變更，因此也會捕捉從網路介面送出的本機封包。
這包括在另一個介面上收到的封包，然後使用 **SIO \_ RCVALL** IOCTL 轉送系結至通訊端的網路介面。

設定這個 IOCTL 需要本機電腦的系統管理員許可權。

這項功能有時稱為混合模式。
在某個介面上套用此選項，然後再到另一個使用此 IOCTL 的單一呼叫的介面，則不支援任何直接變更。
應用程式必須先使用這個 IOCTL 來關閉第一個介面上的行為，然後使用這個 IOCTL 來啟用新介面的行為。

## <a name="see-also"></a>另請參閱

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**TCP/IP 原始通訊端**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

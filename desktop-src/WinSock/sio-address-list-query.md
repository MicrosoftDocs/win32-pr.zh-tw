---
description: 控制項程式碼會取得應用程式可系結之通訊端通訊協定系列的本機傳輸地址清單。
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57d529ed4ea525b01e294efcacc1aa8dd2b118106177bd46cb64ffdf42a31a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097528"
---
# <a name="sio_address_list_query-control-code"></a>SIO_ADDRESS_LIST_QUERY 控制程式代碼

## <a name="description"></a>描述

**SIO \_ ADDRESS \_ LIST \_ QUERY** control code 會取得應用程式可系結之通訊端通訊協定系列的本機傳輸地址清單。
地址清單會根據地址系列而有所不同，而某些位址會從清單中排除。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
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
使用 **SIO \_ 位址 \_ 清單 \_ 查詢** 進行此作業。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數未用來進行這項操作。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。
此參數未用來進行這項操作。

### <a name="lpvoutbuffer"></a>lpvOutBuffer

輸出緩衝區的指標。

### <a name="cboutbuffer"></a>cbOutBuffer

輸出緩衝區的大小（以位元組為單位）。

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。

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
| **WSAEINVAL** | *DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。 如果 *cbInBuffer* 參數未設定為 **Null**，就會傳回此錯誤。 |
| **WSAENETDOWN** | 網路子系統失敗。 |
| **WSAENOBUFS** | 沒有可用的緩衝區空間。 |
| **WSAENOPROTOOPT** | 指定的通訊協定不支援通訊端選項。 |
| **WSAENOTSOCK** | *描述項不是* 通訊端。 |
| **WSAEOPNOTSUPP** | 不支援指定的 IOCTL 命令。 如果傳輸提供者不支援 **SIO \_ 位址 \_ 清單 \_ 查詢** IOCTL，則會傳回此錯誤。 |

## <a name="remarks"></a>備註

Windows 2000 和更新版本的作業系統都支援 **SIO \_ 位址 \_ 清單 \_ 查詢** IOCTL。

**SIO \_ ADDRESS \_ LIST \_ QUERY** control code 會取得應用程式可系結之通訊端通訊協定系列的本機傳輸地址清單。
地址清單會根據地址系列而有所不同。

若為 AF \_ INET6 位址系列，則會傳回除了下列以外的所有位址：

* 未 IpDadStatePreferred 重複位址偵測 (DAD) 狀態的任何 IP 位址。
* 在介面類別型為的介面上，任何範圍層級低於 ScopeLevelSubnet 的 IP 位址會 **是 \_ 類型 \_ 軟體 \_ 回送**。
這表示 **如果排除 \_ 型別 \_ 軟體 \_ 回送** 類型，則在介面上的 (fe80： * ) 和回送 (：： 1) 位址，但如果這些位址位於不同類型的介面上，則不是。

若為 **AF \_ INET** 位址系列，則會傳回除了下列以外的所有位址：

* 未 IpDadStatePreferred 重複位址偵測 (DAD) 狀態的任何 IP 位址。
* 介面類別型為的介面上的任何 IP 位址， **如果 \_ 類型 \_ 軟體 \_ 回送** 和連結是本機的，則為。
這表示連結-本機 (169.254。*) 和回送 (127。***如果排除 \_ 型別 \_ 軟體 \_ 回送** 類型，則在介面上) 位址，但如果這些位址位於不同類型的介面上，則不是。

如需有關 DAD 狀態的詳細資訊，請參閱有關 [**MIB \_ UNICASTIPADDRESS 資料 \_ 列**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)結構上 ip [**\_ DAD \_ 狀態**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)列舉和 [**IP \_ 配接器 \_ 單播 \_ 位址**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)結構和 mib 檔的 ip 協助程式檔。
如需介面類別型的詳細資訊，請參閱 ip [**\_ 配接器 \_ 位址**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) 結構上的 ip 協助程式檔和 [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) 函式，以及有關 [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) 結構的 MIB 檔。
如需範圍層級的詳細資訊，請參閱 [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) 結構和 [**範圍 \_ 層級**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) 列舉的 IP 協助程式檔。

*LpvOutBuffer* 參數所指向之輸出緩衝區中傳回的清單是 [**通訊端 \_ 位址 \_ 清單**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)結構的形式。

如果 *lpvOutBuffer* 參數中指定的輸出緩衝區不夠大，無法包含地址清單，則會傳回 **通訊端 \_ 錯誤** ，因為這個 IOCTL 的結果和 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEFAULT](windows-sockets-error-codes-2.md)。
在此情況下，輸出緩衝區所需的大小（以位元組為單位）會在 *lpcbBytesReturned* 參數中傳回。
請注意，如果 *lpvInBuffer*、 *lpvOutBuffer* 或 *lpcbBytesReturned* 參數未完全包含在使用者位址空間的有效部分中，也會傳回 [WSAEFAULT](windows-sockets-error-codes-2.md)錯誤碼。

**SIO \_ 位址 \_ 清單 \_ 查詢** IOCTL 通常會以同步方式呼叫，並將 *lpvOverlapped* 參數設定為 **Null**，因為會立即傳回地址清單。

**注意** 在 Windows 隨插即用環境中，可以動態新增和移除位址。
因此，應用程式無法依賴 **SIO \_ 位址 \_ 清單 \_ 查詢** 所傳回的資訊來持續存在。
應用程式可以透過 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL 來登入位址變更通知，以透過重迭的 I/o 或 **FD \_ 通訊 \_ 清單 \_ 變更** 事件提供通知。
下列動作順序可以用來保證應用程式一律具有目前的通訊清單資訊：

* 發出 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL
* 發出 **SIO \_ 位址 \_ 清單 \_ 查詢** IOCTL
* 只要 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL 呼叫，就會通知應用程式地址清單變更 (透過重迭的 I/o 或) 的 **FD \_ 通訊 \_ 清單 \_ 變更** 事件，就應該重複執行一系列的動作。

在 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 發行時，標頭檔的組織已變更，且 **SIO \_ ADDRESS \_ LIST \_ 查詢** 控制項程式碼定義于 *Ws2def .h* 標頭檔中。
請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。

## <a name="see-also"></a>另請參閱

[**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

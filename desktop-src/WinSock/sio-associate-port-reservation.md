---
description: 控制項程式碼會將一個通訊端與在埠保留權杖所識別之 TCP 或 UDP 區塊的持續或執行時間保留產生關聯。
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: SIO_ASSOCIATE_PORT_RESER加值稅ION 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194031"
---
# <a name="sio_associate_port_reservation-control-code"></a>SIO_ASSOCIATE_PORT_RESER加值稅ION 控制程式代碼

## <a name="description"></a>Description

**SIO 會 \_ 將通訊 \_ 埠 \_ 保留** 控制項程式碼與埠保留權杖所識別之 TCP 或 UDP 區塊的持續或執行時間保留產生關聯。
這個 IOCTL 必須在系結器之前發出。
當通訊端系結時，會從指定權杖所識別的埠保留中選取指派給它的通訊埠。
如果指定的保留中沒有任何可用的埠，系 [**結函數呼叫**](/windows/desktop/api/winsock/nf-winsock-bind) 將會失敗。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
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
使用 **SIO \_ 將 \_ 埠 \_ 保留關聯** 于此作業。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數包含 [**INET_PORT_RESER加值稅ION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) 結構的指標，其中包含要與通訊端產生關聯之 TCP 或 UDP 埠保留的權杖。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。
此參數必須至少為 [**INET_PORT_RESER加值稅ION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) 結構的大小。

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
| **WSAEOPNOTSUPP** | 所參考的物件類型不支援所嘗試的操作。 如果不支援指定的 IOCTL 命令，則會傳回此錯誤。 如果傳輸提供者不支援 **SIO \_ 相關聯的 \_ 埠 \_ 保留** 專案 IOCTL，也會傳回此錯誤。 當嘗試使用 SIO 在 UDP 或 TCP 以外的通訊端上建立 **\_ \_ 埠 \_ 保留** IOCTL 時，也會傳回此錯誤。 |

## <a name="remarks"></a>備註

在 Windows Vista 和更新版本的作業系統上，支援 **SIO \_ 關聯 \_ 埠 \_ 保留** 的 IOCTL。

需要保留埠的應用程式和服務可以分為兩個類別。
第一個類別包含元件，而這些元件需要特定的埠做為其作業的一部分。
這類元件通常會偏好在安裝期間指定其必要的埠 (在應用程式資訊清單中，例如) 。
第二個類別包含在執行時間需要任何可用埠或埠區塊的元件。
這兩個類別對應于特定和萬用字元埠保留要求。
特定的保留要求可能是持續性或執行時間，而萬用字元埠保留要求只在執行時間支援。

**SIO 會 \_ 建立 \_ 埠 \_ 保留** 專案 IOCTL 的關聯，以將 TCP 或 UDP 埠保留與持續或執行時間保留建立關聯。

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)或 [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)函數可讓應用程式或服務保留 TCP 或 UDP 埠的持續性區塊。
持續性埠保留會記錄在 Windows 中 TCP 或 UDP 模組的持續性存放區中。
請注意，每次重新開機系統時，指定的持續埠保留的權杖可能會變更。

一旦取得持續性 TCP 或 UDP 埠保留，應用程式就可以藉由開啟 TCP 或 UDP 通訊端，然後呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 函式來指定 **SIO \_ 建立 \_ 埠 \_ 保留** 型 [**IOCTL 的**](/windows/desktop/api/winsock/nf-winsock-bind) 關聯並傳遞保留權杖，然後再發出對通訊端之系結函式的呼叫，藉此從埠保留要求埠指派。

[**SIO_ACQUIRE_PORT_RESER加值稅ION**](sio-acquire-port-reservation.md)的 IOCTL 可以用來要求 TCP 或 UDP 埠區塊的執行時間保留。
針對執行時間埠保留，埠集區會要求從其通訊端已授與保留的進程取用保留。
執行時間埠保留最後只會在呼叫 [**SIO_ACQUIRE_PORT_RESER加值稅ION**](sio-acquire-port-reservation.md) IOCTL 的通訊端存留期內。
相反地，使用 [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) 或 [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) 函式所建立的持續性埠保留，可供任何程式使用，以取得持續保留。

一旦取得執行時間 TCP 或 UDP 埠保留之後，應用程式就可以開啟 TCP 或 UDP 通訊端，然後呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 函式來指定 **SIO \_ 建立 \_ 埠 \_ 保留** 專案 IOCTL 的關聯，並在發出對套 [**接字的系**](/windows/desktop/api/winsock/nf-winsock-bind) 結函式的呼叫之前傳遞保留權杖，藉此要求埠保留中的埠指派。

如果 *lpOverlapped* 和 *lpCompletionRoutine* 參數都是 Null，則會將此函式中的通訊端視為非重迭的通訊端。
若為非重迭的通訊端，則會忽略 *lpOverlapped* 和 *lpCompletionRoutine* 參數，不同之處在于如果通訊端 *s* 處於封鎖模式，函數可以封鎖。
如果通訊端 *s* 處於非封鎖模式中，此函式仍會封鎖，因為這個特定的 IOCTL 不支援非封鎖模式。

針對重迭的通訊端，將會起始無法立即完成的作業，並會在稍後指出完成的時間。

任何 IOCTL 可能會無限期地封鎖，視服務提供者的執行而定。
如果應用程式無法容忍 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式呼叫中的封鎖，則會建議對可能封鎖的 IOCTLs 進行重迭的 i/o。

SIO 會在下列情況下， **\_ 將 \_ 埠 \_ 保留** 的 IOCTL 關聯于 **WSAEINTR** 或 **WSA_OPERATION_ABORTED** ：

* I/o 管理員會取消要求。
* 通訊端已關閉。

SIO 會將傳遞給 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)或 **WSPIoctl** 函式的 **\_ \_ 埠 \_ 保留** 專案 IOCTL 關聯到持續性埠保留，只可在使用者以系統管理員群組成員的身分登入時，于應用程式中使用。
如果當使用者不是系統管理員群組的成員時，在應用程式中使用 **SIO \_ 關聯 \_ 埠 \_ 保留** 的 IOCTL，函式呼叫將會失敗，並傳回 **WSAEACCES** 。
使用 **SIO \_ 關聯 \_ 埠 \_ 保留** 的 IOCTL 也可能會因為使用者帳戶控制 (Windows Vista 和更新版本上的 UAC) 而失敗。
如果使用此 IOCTL 搭配持續性埠保留的應用程式是以內建系統管理員以外的 Administrators 群組成員身分登入，則此呼叫會失敗，除非應用程式已標示為 **並無 requestedexecutionlevel** 設定為 *requireAdministrator* 的資訊清單檔。
如果應用程式缺少此資訊清單檔，以內建系統管理員以外的 Administrators 群組成員身分登入的使用者，就必須在增強型 shell 中執行該應用程式，因為內建的系統管理員 (`RunAs administrator`) 讓此功能成功。

## <a name="see-also"></a>另請參閱

[**綁定**](/windows/desktop/api/winsock/nf-winsock-bind)

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESER加值稅ION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESER加值稅ION**](sio-acquire-port-reservation.md)

[**SIO_RELEASE_PORT_RESER加值稅ION**](sio-release-port-reservation.md)

[插座](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

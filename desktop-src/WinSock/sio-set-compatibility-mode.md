---
description: 要求網路堆疊應該如何處理特定行為，而這種行為的預設處理方式可能會在 Windows 版本之間不同。
ms.assetid: 9574e21f-5ac4-4210-8031-2f3b07416813
title: SIO_SET_COMPATIBILITY_MODE 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 58972595adb71a30728cb4817a80814cd987a6de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977017"
---
# <a name="sio_set_compatibility_mode-control-code"></a>SIO_SET_COMPATIBILITY_MODE 控制程式代碼

## <a name="description"></a>Description

**SIO \_ SET \_ 相容性 \_ 模式** 控制程式代碼會要求網路堆疊應該如何處理在不同 Windows 版本之間，其行為的預設處理方式可能不同的特定行為。

若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
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
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
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
使用 **SIO 設定此作業的 \_ \_ 相容性 \_ 模式** 。

### <a name="lpvinbuffer"></a>lpvInBuffer

輸入緩衝區的指標。
此參數應指向 **WSA \_ 相容性 \_ 模式** 結構。

### <a name="cbinbuffer"></a>cbInBuffer

輸入緩衝區的大小（以位元組為單位）。
此參數應等於或大於 *lpvInBuffer* 參數所指向的 **WSA \_ 相容性 \_ 模式** 結構的大小。

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
| **WSAEINVAL** | *DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。 如果 *cbInBuffer* 參數小於 **WSA \_ 相容性 \_ 模式** 結構的 sizeof，則會傳回此錯誤。
| **WSAENETDOWN** | 網路子系統失敗。 |
| **WSAENOPROTOOPT** | 指定的通訊協定不支援通訊端選項。 |
| **WSAENOTCONN** | 通訊端未連線。 |
| **WSAENOTSOCK** | *描述項不是* 通訊端。 |
| **WSAEOPNOTSUPP** | 不支援指定的 IOCTL 命令。 如果傳輸提供者不支援 **SIO \_ SET \_ 相容性 \_ 模式** IOCTL，則會傳回此錯誤。 當嘗試在資料包通訊端上進行使用 **SIO \_ SET \_ 相容性 \_ 模式** IOCTL 時，也會傳回此錯誤。 |

## <a name="remarks"></a>備註

**SIO \_ 設定的 \_ 相容性 \_ 模式** IOCTL 會要求網路堆疊應該如何處理在不同 Windows 版本之間，其行為的預設處理方式可能不同的特定行為。
**SIO \_ 集 \_ 相容性 \_ 模式** 的輸入引數結構是在 *Mswsockdef .H* 標頭檔中定義的 **WSA \_ 相容性 \_ 模式** 結構中指定。
在 *cbInBuffer* 參數中傳遞 **WSA \_ 相容性 \_ 模式** 結構的指標。
此結構的定義如下：

```cpp
// Need to #include <mswsock.h>

/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

**BehaviorId** 成員中指定的值會指出所要求的行為。
**TargetOsVersion** 成員中指定的值會指出所要求的行為的 Windows 版本。

**BehaviorId** 成員可以是 *Mswsockdef .h* 標頭檔中所定義之 **WSA \_ 相容性 \_ 行為 \_ 識別碼** 列舉類型的其中一個值。
**BehaviorId** 成員的可能值如下：

| 詞彙 | 描述 |
|------|-------------|
| WsaBehaviorAll | 這相當於要求針對 **WSA \_ 相容性 \_ 行為 \_ 識別碼** 定義的所有可能相容行為。 |
| WsaBehaviorReceiveBuffering | 當 **TargetOsVersion** 成員設定為 Windows Vista 或更新版本的值時，即使在建立 tcp 連線之後，也允許使用 **SO \_ RCVBUF** 通訊端選項減少此通訊端上的 TCP 接收緩衝區大小。 當 **TargetOsVersion** 成員設定為早于 Windows Vista 的值時，在連線建立之後，就不允許使用 **\_ RCVBUF** 通訊端選項來降低此通訊端上的 TCP 接收緩衝區大小。 |
| WsaBehaviorAutoTuning | 當 **TargetOsVersion** 成員設定為 Windows Vista 或更新版本的值時，會啟用 [接收視窗自動調整]，並將 [TCP 視窗縮放比例] 從預設值8縮減為2。 當 **TargetOsVersion** 設定為 Windows Vista 之前的值時，會停用 [接收視窗自動調整]。 [TCP 視窗調整] 選項也會停用，而 [最大值] 接收視窗大小則限制為65535個位元組。 即使在此通訊端上呼叫 **\_ RCVBUF** 通訊端選項，在建立連接之前指定大於65535個位元組的值，也無法在連接上協商 TCP 視窗調整選項。 |

**TargetOsVersion** 成員可以是 *sdkddkver.h .h* 標頭檔中定義的其中一個 NTDDI 版本常數。
**TargetOsVersion** 成員的一些可能值如下：

| 詞彙 | 描述 |
|------|-------------|
| NTDDI \_ LONGHORN | 目標行為是 Windows Vista 的預設行為。 |
| NTDDI \_ WS03 | 目標行為是 Windows Server 2003 的預設行為。 |
| NTDDI \_ >TEST-WINXP | 目標行為是 Windows XP 的預設行為。 |
| NTDDI \_ WIN2K | 目標行為是 Windows 2000 的預設行為。 |

**TargetOsVersion** 成員的主要影響是此成員是否設定為等於或大於 **NTDDI \_ LONGHORN** 的值。

TCP 效能不僅取決於傳輸速率本身，而是取決於傳輸速率和來回延遲時間的乘積。
這個頻寬延遲乘積會測量「填滿管道」的資料量。
此頻寬延遲產品是傳送者和接收者所需的緩衝區空間，可在路徑上取得 TCP 連接的最大輸送量。
此緩衝區空間代表 TCP 必須處理才能讓管線保持完整的未認可資料量。
當頻寬延遲乘積很大時，就會發生 TCP 效能問題。
在這些情況下運作的網路路徑通常稱為「長的 fat 管道」。
範例包括高容量封包附屬連結、高速無線連結，以及遠距離的地面光纖連結。

TCP 標頭會使用16位資料欄位 (TCP 封包標頭中的 [視窗] 欄位) 將接收視窗大小報告給傳送者。
因此，可以使用的最大視窗為65535個位元組。
為了規避這項限制，已為高效能 TCP 新增 tcp 延伸模組選項，以允許超過65535個位元組的 windows。
「TCP 視窗調整」選項 (WSopt) 是在 [IETF 網站](https://www.ietf.org/rfc/rfc1122.txt)提供的 RFC 1323 中定義。
WSopt 擴充功能會使用單一位元組的對數縮放比例，將 TCP 視窗的定義擴充至32位，以擴充 TCP 標頭中的16位視窗欄位。
WSopt 延伸模組會定義隱含的縮放比例 (2 到某些電源) ，用來將 TCP 標頭中找到的視窗大小值乘以以取得真正的視窗大小。
因此，視窗比例因數8會導致真正的視窗大小等於 TCP 標頭中的 [視窗] 欄位值乘以 2 ^ 8 或256。
因此，如果 TCP 標頭中的視窗欄位設定為65535個位元組的最大值，且 WSopt 縮放比例已協商為8的值，則真正的視窗大小會是16776960個位元組。

真正的接收視窗大小，因此，縮放比例取決於接收緩衝區的最大空間。
此最大緩衝區空間是 TCP 寄件者在等待通知之前，允許 TCP 寄件者傳送的資料量。
建立連線之後，會在每個 TCP 區段中通告接收視窗大小， (TCP 標頭中的視窗欄位) 。
通告傳送者可以傳送的最大資料量是接收端流程式控制制機制，可防止寄件者傳送接收者無法儲存的資料。
傳送主機只能在等待通知和接收視窗大小更新之前，傳送接收端所通告的資料量上限。

在 Windows Server 2003 和 Windows XP 上，根據傳送介面的連結速度，最大的接收緩衝區空間（代表 TCP/IP 堆疊的接收視窗大小）有預設值。
實際的值會自動調整為偶數的區段大小上限， (MSS) 在 TCP 連線建立期間協商。
因此，若是 10 Mbit/sec 的連結，預設的接收視窗大小通常會設定為16K 位元組，而在 100 MBit/sec 連結上，預設的接收視窗大小會設為65535個位元組。

在 Windows Server 2003 和 Windows XP 上，您可以使用特定介面或整個系統上的下列登錄值，手動設定 TCP/IP 堆疊的真正最大接收視窗大小：

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\TCPWindowSize`

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Interface\TCPWindowSize`

當 (使用 WSopt 擴充功能時， **TCPWindowSize** 的登錄值最多可設為65535個1073741823位元組（最大值為），) 支援最大的縮放因數4。
如果沒有視窗調整，應用程式只能達到大約每秒 5 mb 的輸送量 (Mbps) 在具有100毫秒的往返時間 (RTT) ，不論路徑頻寬為何。
此輸送量可以調整為超過每秒 gigabit (Gbps) 搭配視窗調整，這可讓 TCP 在建立連線時，協調視窗大小的縮放係數。

在 Windows Server 2003 和 Windows XP 上，您可以藉由設定下列登錄值來啟用 WSopt 擴充功能。

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Tcp1323Opts`

**Tcp1323Opts** 登錄值是 **DWORD** 編碼的，因此當設定位0時，會啟用 TCP WSopt 延伸。
當設定位1時，會啟用在 RFC 1323 中定義 (TSopt) 的 TCP 時間戳記選項。
因此，1或3的值會啟用 WSopt 延伸模組。

在 Windows Server 2003 和 Windows XP 上，預設為不會建立 TCPWindowSize 和 Tcp1323Opts 登錄值。
因此，預設值是停用 WSopt 延伸模組，而且 TCP 接收視窗大小是由系統設定為最大值，最大值為65535個位元組（以連結速度為基礎）。
藉由設定 Tcp1323Opts 登錄值，在 Windows Server 2003 和 Windows XP 上啟用視窗調整功能時，仍然只會在傳送者和接收者將 [同步處理 (SYN) 區段中包含 [TCP 視窗調整] 選項，以協調視窗縮放比例時使用 TCP 連接。
在連接上使用視窗調整時，TCP 標頭中的 [視窗] 欄位會設為65535個位元組，而 [視窗縮放比例] 則是用來在建立連接時，以協調的視窗縮放因數來調整真正的接收視窗大小。

應用程式可以使用 **\_ RCVBUF** 通訊端選項來指定連接的 TCP 接收視窗大小。
您可以使用 **\_ RCVBUF**，隨時增加通訊端的 TCP 接收視窗大小，但只能在建立連線之前降低。
若要使用視窗調整，應用程式必須在建立連線之前，使用 **\_ RCVBUF** 通訊端選項來指定大於65535位元組的視窗大小。

TCP 接收視窗大小的理想值通常很難判斷。
為了填滿傳送者與接收者之間的網路容量，接收視窗大小應設定為連線的頻寬延遲產品，也就是頻寬乘以來回時間。
即使應用程式可以正確地判斷頻寬延遲的產品，仍不知道接收應用程式從傳入資料緩衝區取出資料的速度， (應用程式取得速率) 。
雖然支援 TCP 視窗調整，但 Windows Server 2003 和 Windows XP 中的接收視窗大小上限仍然會限制輸送量，因為它是所有 TCP 連線的固定大小上限 (除非使用 **\_ RCVBUF**) 為每個應用程式指定，這樣可以增強某些連線的輸送量，並降低其他連線的輸送量。
此外，TCP 連線的固定接收視窗大小上限，不會隨著網路狀況的變更而改變。

為了解決根據網路目前狀況正確判斷 TCP 連接之接收視窗大小上限值的問題，Windows Vista 中的 TCP/IP 堆疊支援「接收視窗自動微調」功能。
啟用這項功能時，「接收視窗自動微調」會藉由測量頻寬延遲產品和應用程式取出率，持續判斷最佳的真正接收視窗大小，並根據變更的網路狀況調整真正的最大接收視窗大小。
依預設，[接收視窗自動調整] 會啟用 TCP WSopt 延伸模組，為真正的視窗大小允許最多16776960個位元組。
當資料在連線上流動時，TCP/IP 堆疊會監視連線、測量連接目前的頻寬延遲產品和應用程式接收率，以及調整實際的接收視窗大小以優化輸送量。
TCP/IP 堆疊會根據網路條件變更 TCP 標頭中的 [視窗] 欄位的值，因為 WSopt 縮放比例是在第一次建立連接時固定的。

Windows Vista 中的 TCP/IP 堆疊不再使用 **TCPWindowSize** 登錄值。
TCP 對等互連之間有更高的輸送量，則會在資料傳輸期間增加網路頻寬的使用率。
如果所有應用程式都經過優化以接收 TCP 資料，則網路的整體使用率可能會大幅增加，而使用服務品質 (QoS) 更重要的是在運作或接近容量的網路上。

當您未使用 **WsaBehaviorReceiveBuffering** 指定 **SIO \_ SET \_ 相容性 \_ 模式** 時，Windows Vista 上的 [接收緩衝處理] 的預設行為是，在建立連線之後，不允許使用 [允許 **\_ RCVBUF** 通訊端] 選項來降低接收視窗大小。

當您未使用 **WsaBehaviorAutoTuning** 指定 **SIO \_ SET \_ 相容性 \_ 模式** 時，Windows Vista 上的預設行為會自動調整，因為堆疊將會使用視窗比例因數8來自動調整視窗。
請注意，如果應用程式使用 **\_ RCVBUF** 通訊端選項設定有效的接收視窗大小，堆疊將會使用指定的大小，且將停用 [視窗接收自動調整]。
您也可以使用下列命令，完全停用 Windows 自動優化功能， `netsh interface tcp set global autotuninglevel=disabled` 在這種情況下，指定 **WsaBehaviorAutoTuning** 不會有任何影響。
您也可以根據 Windows Server 2008 上設定的群組原則來停用視窗接收自動優化。

某些網際網路閘道裝置和防火牆無法正確支援使用 WSopt 擴充功能和 Windows 縮放比例之 TCP 連線的資料流程時，Windows Vista 上需要 **WsaBehaviorAutoTuning** 選項。
在 Windows Vista 上，接收器預設會將視窗縮放比例（最大值為16776960個位元組的視窗大小）協調為8。
當資料開始在快速連結上流動時，Windows 一開始會先將 TCP 標頭的視窗欄位設定為256，並在 TCP 選項中將視窗比例因數設定為8，以在 [TCP 選項 (256 * 2 ^ 8 = 64KB) 的情況下，以 64 Kb 的真正視窗大小開始。
某些網際網路閘道裝置和防火牆會忽略視窗調整比例，並只查看指定為256的 TCP 標頭中的 [通告的視窗] 欄位，然後針對包含超過256個位元組之 TCP 資料的連接卸載連入封包。
若要支援 TCP 接收視窗調整，閘道裝置或防火牆必須監視 TCP 交握，並在 TCP 連線資料中追蹤已協商的視窗調整係數。
此外，其他平臺上的某些應用程式和 TCP 堆疊會忽略 TCP WSopt 延伸模組和視窗調整係數。
因此傳送資料的遠端主機可能會以 TCP 標頭的 [時間範圍] 欄位中通告的速率傳送資料 (256 個位元組) 。
這可能會導致接收端的資料接收速度非常緩慢。

將 **BehaviorId** 成員設定為 **WsaBehaviorAutoTuning** ，並將 **TargetOsVersion** 到 Windows Vista，將視窗縮放比例縮減為2，因此 TCP 標頭中的 [視窗] 欄位一開始會設定為16384個位元組，而 [視窗縮放比例] 會設定為 [2]，表示初始真正的視窗接收大小為64k 個位元組。
然後，視窗自動調整功能可將 TCP 標頭中的視窗欄位設定為65535個位元組，以增加最多262140個位元組的真正視窗接收大小。
一旦建立通訊端之後，應用程式應該立即設定 **SIO \_ set \_ 相容性 \_ 模式** 的 IOCTL，因為在傳送 SYN 之後，這個選項並不合理或不適用。
設定此選項的影響與下列命令相同： `netsh interface tcp set global autotuninglevel=highlyrestricted`

請注意， *Mswsockdef .h* 標頭檔會自動包含在 *Mswsock .h* 或 *Netiodef* 中，而且不能直接使用。

## <a name="see-also"></a>另請參閱

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

---
description: Windows 通訊端 (Winsock) 通訊端 IOCTLs 的流覽主題。
ms.assetid: 6a63c2c9-4e09-4a62-b39f-3ccb26287da8
title: Winsock IOCTLs (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7094f802b815bfbd7511bd67eb4e6b1767cb94
ms.sourcegitcommit: 392c0a56f99f4d19686e734291abcac887fc5ba2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/22/2021
ms.locfileid: "107000502"
---
# <a name="winsock-ioctls"></a>Winsock IOCTLs

本節描述 Winsock 通訊端輸入/輸出控制項 (IOCTLs) 適用于各種不同版本的 Windows 作業系統。 使用 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 或 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) 函數來發出 Winsock IOCTL，以控制通訊端、傳輸通訊協定或通訊子系統的模式。

有些 Winsock IOCTLs 需要比此資料表可以傳達的更多說明;這類選項包含其他主題的連結。

您可以採用編碼配置來保留目前定義的 [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) 操作碼，同時提供便利的方式來分割 opcode 識別碼空間，因為 *dwIoControlCode* 參數現在是32位實體。 *DwIoControlCode* 參數的建立目的，是要在加入新的控制程式代碼時，允許通訊協定和廠商獨立性，同時保留與 Windows 通訊端1.1 和 Unix 控制程式代碼的回溯相容性。 *DwIoControlCode* 參數的格式如下。

| I  | O  | V  | T  | 廠商/位址系列 | 程式碼                   |
|-|-|-|-|-|-|
| 3  | 3  | 2  | 2 2 | 2 2 2 2 2 2 2 1 1 1 1 | 1 1 1 1 1 1              |
| 1  | 0  | 9  | 8 7 | 6 5 4 3 2 1 0 9 8 7 6 | 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 |

> [!Note] 
> 在資料表中顯示的 *dwIoControlCode* 參數中的位，必須從上到下依資料行以垂直方式讀取。 因此最左邊的位是 bit 31，下個位是 bit 30，最右邊位則是 bit 0。

如果輸入緩衝區對程式碼而言是有效的，則會設定 I，如同 **IOC_IN** 一樣。

如果輸出緩衝區對程式碼而言是有效的，則會設定 O，如同 **IOC_OUT** 一樣。 使用輸入和輸出緩衝區的控制代碼都設定了 I 和 O。

如果程式碼沒有參數，則設定 V，如同 **IOC_VOID** 一樣。

T 是定義 IOCTL 類型的2位數量。 系統會定義下列值：

0： IOCTL 是標準的 Unix IOCTL 程式碼，如同 **FIONREAD** 和 **FIONBIO**。

1： IOCTL 是一般的 Windows 通訊端 2 IOCTL 程式碼。 針對 Windows 通訊端2定義的新 IOCTL 程式碼將會有 T = = 1。

2： IOCTL 只適用于特定的位址系列。

3： IOCTL 只適用于特定廠商的提供者，如同 **IOC_VENDOR** 一樣。 此類型可讓公司將出現在 **廠商/位址系列** 參數中的廠商編號指派給公司。 然後，廠商可以定義該廠商專屬的新 IOCTLs，而不需要向 clearinghouse 註冊 IOCTL，進而提供廠商的彈性和隱私權。

**廠商/位址系列** 11位的數量，定義擁有程式碼的廠商 (如果 T = = 3) 或包含程式碼套用的位址系列 (if T = = 2) 。 如果這是 Unix IOCTL 程式碼 (T = = 0) 則此參數的值與 Unix 上的程式碼相同。 如果這是泛型 Windows 通訊端 2 IOCTL (T = = 1) 則此參數可以用來做為程式碼參數的副檔名，以提供額外的程式碼值。

程式 **代碼** 16位的數量，其中包含作業的特定 IOCTL 程式碼。

## <a name="unix-ioctl-codes"></a>Unix IOCTL 代碼

支援) 的下列 Unix IOCTL 代碼 (命令。

### <a name="fionbio"></a>FIONBIO

啟用或停用通訊端 *s* 上的非封鎖模式。 *LpvInBuffer* 參數指向不 **帶正負** 號的 long (QoS) ，如果要啟用非封鎖模式則為非零，如果要停用，則為零。 建立通訊端時，它會在封鎖模式下運作 (也就是) 停用非封鎖模式。 這與 BSD 通訊端一致。

[**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)或 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)常式會自動將通訊端設定為非封鎖模式。 如果已在通訊端上發出 **WSAAsyncSelect** 或 **WSAEventSelect** ，則嘗試使用 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 將通訊端設定回封鎖模式將會失敗，並出現 WSAEINVAL。 若要將通訊端設定回封鎖模式，應用程式必須先使用等於零的 *lEvent* 參數呼叫 **WSAAsyncSelect** 來停用 **WSAAsyncSelect** ，或呼叫 **WSAEventSelect** ，並將 *lNetworkEvents* 參數等於零，以停用 **WSAEventSelect** 。

### <a name="fionread"></a>FIONREAD

判斷可 *從通訊端* 以不可部分完成的方式讀取的資料量。 *LpvOutBuffer* 參數指向 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)儲存結果的不 **帶正負** 號的 long。

如果傳入 *s* 參數的通訊端是資料流程導向 (例如，輸入 SOCK \_ Stream) ， **FIONREAD** 會傳回可在單一接收作業中讀取的資料總量; 這通常與套 (接字上佇列的資料總量相同，因為資料流程是位元組導向的，這並不保證) 。

如果傳入 *s* 參數的通訊端是訊息導向 (例如，輸入 SOCK \_ DGRAM) ， **FIONREAD** 會傳回可讀取的位元組總數，而不是第一個資料包 (訊息) 在通訊端上排入佇列的大小。

### <a name="siocatmark"></a>SIOCATMARK

判斷是否已讀取所有 OOB 資料。 這僅適用于資料流程樣式 (的通訊端，例如，輸入 SOCK \_ stream) ，其已設定為以內嵌方式接收任何 OOB 資料 (因此 \_ OOBINLINE) 。 如果沒有任何 OOB 資料正在等候讀取，則作業會傳回 TRUE。 否則，它會傳回 **FALSE**，而且在通訊端上執行的下一個接收作業會取出標記前面的部分或全部資料;應用程式應該使用 **SIOCATMARK** 作業來判斷是否有任何保留。 如果緊急 (的頻外) 資料中有任何一般資料，則會依序接收。  (請注意，在相同的呼叫中，[**接收**](/windows/desktop/api/winsock/nf-winsock-recv)作業永遠不會混用 OOB 和一般資料。在 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)儲存結果的布林值上，) *lpvOutBuffer* 點。

## <a name="windows-sockets-2-commands"></a>Windows 通訊端2命令

支援下列 Windows 通訊端2命令。

### <a name="sio_acquire_port_reservation-opcode-setting-i-t3"></a>SIO_ACQUIRE_PORT_RESER加值稅ION (opcode 設定： I，T = = 3) 

要求 TCP 或 UDP 埠區塊的執行時間保留。 針對執行時間埠保留，埠集區會要求從其通訊端已授與保留的進程取用保留。 執行時間埠保留最後只會在呼叫 [**SIO \_ 取得 \_ 埠 \_ 保留**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) IOCTL 的通訊端存留期內。 相反地，使用 [**CreatePersistentTcpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) 或 [**CreatePersistentUdpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) 函式所建立的持續性埠保留，可供任何程式使用，以取得持續保留。

如需詳細資訊，請參閱 [**SIO \_ 取得 \_ 埠 \_ 保留**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) 參考。

[**SIO \_Windows \_ \_**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) Vista 和更新版本的作業系統支援取得埠保留。

### <a name="sio_address_list_change-opcode-setting-v-t1"></a>SIO \_ 位址 \_ 清單 \_ 變更 (操作碼設定： V，T = = 1) 

接收應用程式可以系結之通訊端通訊協定系列的本機傳輸地址清單中的變更通知。 這項 IOCTL 完成時，將不會提供任何輸出資訊;完成隻會指出可用的本機地址清單已變更，且應該透過 **SIO \_ 位址 \_ 清單 \_ 查詢** 重新查詢。

雖然並非) 必要，但應用程式會使用重迭的 i/o 來 **SIO \_ 位址 \_ 清單 \_ 變更** 要求，以通知變更，但這是假設的 (。 或者，如果 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL 是在非封鎖通訊端上發出的，且沒有重迭的參數 (*lpOverlapped* /  *lpCompletionRoutine* 會設定為 **Null**) ，它會立即完成，並出現錯誤 [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md)。 然後，應用程式可以透過呼叫 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 或 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) ，以在 \_ \_ \_ 網路事件位元遮罩中設定的 FD 地址清單變更位來等候地址清單變更事件。

### <a name="sio_address_list_query-opcode-setting-o-t1"></a>SIO \_ 位址 \_ 清單 \_ 查詢 (操作碼設定： O，T = = 1) 

取得應用程式可系結之通訊端通訊協定系列的本機傳輸地址清單。 地址清單會根據地址系列而有所不同，而某些位址會從清單中排除。

> [!Note] 
> 在 Windows 隨插即用環境中，可以動態新增和移除位址。 因此，應用程式無法依賴 **SIO \_ 位址 \_ 清單 \_ 查詢** 所傳回的資訊來持續存在。 應用程式可以透過 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL 來登入位址變更通知，以透過重迭的 I/o 或 FD \_ 通訊 \_ 清單 \_ 變更事件提供通知。 下列動作順序可以用來保證應用程式一律具有目前的通訊清單資訊：

-  問題 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL
-  問題 **SIO \_ 位址 \_ 清單 \_ 查詢** IOCTL
-  每當 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL 通知應用程式地址清單變更時 (透過重迭的 I/o 或) 的 FD \_ 通訊 \_ 清單 \_ 變更事件，就應該重複執行整個動作順序。

如需詳細資訊，請參閱 [**SIO \_ 位址 \_ 清單 \_ 查詢**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) 參考。 **SIO \_Windows 2000 和更新版本支援位址 \_ 清單 \_ 查詢** 。

### <a name="sio_apply_transport_setting-opcode-setting-i-t3"></a>SIO \_ 套用 \_ 傳輸 \_ 設定 (操作碼設定： I，T = = 3) 

將傳輸設定套用至通訊端。 正在套用的傳輸設定是以 *lpvInBuffer* 參數中傳遞的 [**傳輸 \_ 設定 \_ 識別碼**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id)為基礎。

目前唯一定義的傳輸設定是用於 TCP 通訊端上的 **即時 \_ \_ 通知 \_ 功能** 功能。

如果傳遞的 [**傳輸 \_ 設定 \_ 識別碼**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id)具有設定為 **即時 \_ \_ 通知 \_ 功能** 的 **Guid** 成員，則這項要求會要求套用與 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)搭配使用的 TCP 通訊端的即時通知設定，以在 Windows 市集中應用程式接收背景網路通知。

如需詳細資訊，請參閱 [**SIO \_ 套用 \_ 傳輸 \_ 設定**](/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)) 參考。 **SIO \_Windows 8 \_ \_** 、Windows Server 2012 及更新版本都支援 [套用傳輸] 設定。

### <a name="sio_associate_handle-opcode-setting-i-t1"></a>SIO \_ 建立 \_ 控制碼 (opcode 設定的關聯： I，T = = 1) 

使這個通訊端與隨附介面的指定控制碼產生關聯。 輸入緩衝區包含對應至隨附介面之資訊清單常數的整數值 (例如，第 \_ NETDEV 和第 \_ 一個 TAPI。 ) ，後面接著一個值，也就是指定之附屬介面的控制碼，以及任何其他必要的資訊。 請參閱 [Winsock 附件](winsock-annexes.md) 中的適當區段，以取得特定隨附介面特定的詳細資料。 總大小會反映在輸入緩衝區長度中。 不需要輸出緩衝區。 針對不支援這個 IOCTL 的服務提供者，會指出 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) 錯誤碼。 您可以使用 **SIO \_ 轉譯 \_ 控制碼** 來抓取這個 IOCTL 相關聯的控制碼。

您可以使用隨附的介面，例如，如果特定提供者提供 (1) 通訊端行為的大量額外控制項，以及 (2) 控制項是提供者特定的，足以讓它們不會對應至現有的 Windows 通訊端函式，或未來可能會定義的控制項。 建議您) 使用元件物件模型 (COM，而不使用這個 IOCTL 來探索和追蹤通訊端可能支援的其他介面。 這個 IOCTL 存在於與 COM 無法使用或無法用於其他原因的系統 (反向) 相容性。

### <a name="sio_associate_port_reservation-opcode-setting-i-t3"></a>SIO \_ 將 \_ 埠 \_ 保留關聯 (操作碼設定： I，T = = 3) 

針對埠保留權杖所識別的 TCP 或 UDP 埠區塊，將通訊端與持續或執行時間保留建立關聯。 SIO 在系結器之前，必須先發出 [**\_ \_ 埠 \_ 保留**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) 的 IOCTL。 當通訊端系結時，會從指定權杖所識別的埠保留中選取指派給它的通訊埠。 如果指定的保留中沒有任何可用的埠，系 [**結函數呼叫**](/windows/desktop/api/winsock/nf-winsock-bind) 將會失敗。

如需詳細資訊，請參閱 [**SIO \_ 關聯 \_ 埠 \_ 保留**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) 參考。

[**SIO \_Windows \_ \_**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) Vista 和更新版本的作業系統支援埠保留的關聯。

### <a name="sio_base_handle-opcode-setting-o-t1"></a>SIO \_ 基底 \_ 控制碼 (操作碼設定： O，T = = 1) 

抓取給定通訊端的基底服務提供者控制碼。 傳回的值是 **通訊端**。

多層式服務提供者永遠不會攔截這個 IOCTL，因為傳回值必須是基底服務提供者的通訊端控制碼。

如果輸出緩衝區不夠大，以致于通訊端控制碼 (*cbOutBuffer* 小於 **通訊端** 的大小) 或 *lpvOutBuffer* 參數為 **Null** 指標，則會傳回 **通訊端 \_ 錯誤** ，因為這個 IOCTL 的結果和 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEFAULT](windows-sockets-error-codes-2.md)。

**SIO \_基底 \_ 控制碼** 定義于 *Mswsock .h* 標頭檔中，並在 Windows Vista 和更新版本上支援。

### <a name="sio_bsp_handle-opcode-setting-o-t1"></a>SIO \_ BSP \_ 控制碼 (opcode 設定： O，T = = 1) 

抓取 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 函式所使用之通訊端的基底服務提供者控制碼。 傳回的值是 **通訊端**。

這個 Ioctl 是由多層式服務提供者所使用，以確保提供者攔截 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 函數。

如果輸出緩衝區不夠大，以致于通訊端控制碼 (*cbOutBuffer* 小於 **通訊端** 的大小) 或 *lpvOutBuffer* 參數為 **Null** 指標，則會傳回 **通訊端 \_ 錯誤** ，因為這個 IOCTL 的結果和 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEFAULT](windows-sockets-error-codes-2.md)。

**SIO \_BSP \_ 控制碼** 定義于 *Mswsock .h* 標頭檔中，並在 Windows Vista 和更新版本上支援。

### <a name="sio_bsp_handle_select-opcode-setting-o-t1"></a>SIO \_ BSP \_ 控制碼 \_ SELECT (Opcode 設定： O，T = = 1) 

抓取 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 函數所用之通訊端的基底服務提供者控制碼。 傳回的值是 **通訊端**。

多層式服務提供者會使用這個 Ioctl，以確保提供者攔截 [**選取**](/windows/desktop/api/Winsock2/nf-winsock2-select) 的函式。

如果輸出緩衝區不夠大，以致于通訊端控制碼 (*cbOutBuffer* 小於 **通訊端** 的大小) 或 *lpvOutBuffer* 參數為 **Null** 指標，則會傳回 **通訊端 \_ 錯誤** ，因為這個 IOCTL 的結果和 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEFAULT](windows-sockets-error-codes-2.md)。

**SIO \_BSP \_ 控制碼 \_ SELECT** 是定義于 *Mswsock .h* 標頭檔中，並在 Windows Vista 和更新版本上支援。

### <a name="sio_bsp_handle_poll-opcode-setting-o-t1"></a>SIO \_ BSP \_ 控制碼 \_ 輪詢 (操作碼設定： O，T = = 1) 

抓取 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函式所使用之通訊端的基底服務提供者控制碼。 *LpOverlapped* 參數必須是 **Null** 指標。 傳回的值是 **通訊端**。

這個 Ioctl 是由多層式服務提供者所使用，以確保提供者攔截 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函數。

如果輸出緩衝區不夠大，以致于通訊端控制碼 (*cbOutBuffer* 小於 **通訊端**) 的大小，則 *lpvOutBuffer* 參數為 **null** 指標，或 *lpOverlapped* 參數不是 **null** 指標，則會傳回此 IOCTL 的結果 **， \_ 而** [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEFAULT](windows-sockets-error-codes-2.md)。

**SIO \_BSP \_ 控制碼 \_ 輪詢** 是定義于 *Mswsock .h* 標頭檔中，並在 Windows Vista 和更新版本上支援。

### <a name="sio_chk_qos-opcode-setting-i-o-t3"></a>SIO \_ .Chk \_ QOS (opcode 設定： I、O、T = = 3) 

捕獲 QoS 流量特性的相關資訊。 在 flow 設定和收到 RESV 訊息之間傳送系統的過渡階段期間 (查看「 [Rsvp 服務」如何](/previous-versions/windows/desktop/qos/how-the-rsvp-service-invokes-tc) 叫用 TC，以取得過渡階段) 的詳細資訊。與「回復」流程相關聯的流量會根據「服務類型」（ ([最大努力](/previous-versions/windows/desktop/qos/best-effort)、 [受控制的負載](/previous-versions/windows/desktop/qos/controlled-load)或 [保證](/previous-versions/windows/desktop/qos/guaranteed)) ）成形。 如需詳細資訊，請參閱 Platform SDK 的「[服務品質](/previous-versions/windows/desktop/qos/qos-start-page)」一節中的「[使用 SIO \_ .chk \_ QOS](/previous-versions/windows/desktop/qos/using-sio-chk-qos) 」。

### <a name="sio_cpu_affinity-opcode-setting-i-t3"></a>SIO_CPU_AFFINITY (opcode 設定： I，T = = 3) 

啟用埠共用和接收指示平行處理。 當您的應用程式使用此通訊端選項來建立通訊端與不同處理器之間的關聯，然後將通訊端系結至相同的位址時，將會根據接收端調整 (RSS) 雜湊，將接收指示分散到通訊端。 RSS 設定不會變更，因此任何指定的流程 (本機端點、遠端端點配對) 一律會在相同的處理器上指出。 如此一來，所有屬於指定流程的封包都會顯示在相同的通訊端中。 這個 IOCTL 必須在系結之前呼叫，否則將會傳回 WSAEINVAL。 輸入緩衝區是以 USHORT 類型 (0 為基礎) 的處理器索引。 IOCTL 與 SO_REUSEADDR 和 SO_REUSE_MULTICASTPORT 不相容。 僅支援 UDP 通訊端。

> [!NOTE]
> 如果您將目標設為版本 10.0.19041.0 (Windows 10，版本 2004) Windows SDK，請使用此值， `0x98000015` 而不是名稱 **SIO_CPU_AFFINITY**。

### <a name="sio_enable_circular_queueing-opcode-setting-v-t1"></a>SIO \_ 啟用 \_ 迴圈 \_ 佇列 (Opcode 設定： V，T = = 1) 

向基礎訊息導向服務提供者指出，新抵達的訊息絕對不應該卸載，因為緩衝區佇列溢位。 相反地，應該消除佇列中最舊的訊息，以便容納新抵達的訊息。 不需要輸入和輸出緩衝區。 請注意，這個 IOCTL 只適用于與不可靠的訊息導向通訊協定相關聯的通訊端。 針對不支援這個 IOCTL 的服務提供者，會指出 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) 錯誤碼。

### <a name="sio_find_route-opcode-setting-o-t1"></a>SIO \_ FIND \_ ROUTE (opcode 設定： O，T = = 1) 

發出時，此 IOCTL 會要求探索在輸入緩衝區中指定為 [**sockaddr**](sockaddr-2.md) 之遠端位址的路由。 如果位址已存在於本機快取中，則其專案會失效。 在 Novell 的 IPX 案例中，此呼叫會起始 IPX GetLocalTarget (GLT) ，以查詢網路中的指定遠端位址。

### <a name="sio_flush-opcode-setting-v-t1"></a>SIO \_ FLUSH (opcode 設定： V，T = = 1) 

捨棄與此通訊端關聯之傳送佇列的目前內容。 不需要輸入和輸出緩衝區。 針對不支援這個 IOCTL 的服務提供者，會指出 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) 錯誤碼。

### <a name="sio_get_broadcast_address-opcode-setting-o-t1"></a>SIO \_ 取得 \_ 廣播 \_ 位址 (Opcode 設定： O，T = = 1) 

這個 IOCTL 會使用 [sockaddr](sockaddr-2.md)結構來填滿輸出緩衝區，其中包含適用于 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)WSASendTo 的適當廣播位址 /  [****](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto)。 IPv6 通訊端不支援這個 IOCTL，並傳回 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) 錯誤碼。

### <a name="sio_get_extension_function_pointer-opcode-setting-o-i-t1"></a>SIO \_ 取得延伸模組函式 \_ \_ \_ 指標 (操作碼設定： O，I，T = = 1) 

取得相關聯服務提供者所支援之指定擴充功能的指標。 輸入緩衝區包含 (**GUID**) 的全域唯一識別碼，其值可識別有問題的擴充功能。 要在輸出緩衝區中傳回所需函式的指標。 延伸模組函式識別碼是由服務提供者廠商所建立，而且應該包含在描述擴充功能功能和語義的廠商檔中。

Windows TCP/IP 服務提供者所支援的擴充功能 GUID 值是定義在 *Mswsock .h* 標頭檔中。 這些 Guid 可能的值如下所示：

| 詞彙                                                                                                                | 描述                                                                               |
|-|-|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>WSAID \_ ACCEPTEX<br/>                                     | [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)擴充功能。<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>WSAID \_ CONNECTEX<br/>                                  | [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)擴充功能。 <br/>                      |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>WSAID \_ DISCONNECTEX<br/>                         | [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85))擴充功能。 <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>WSAID \_ GETACCEPTEXSOCKADDRS<br/> | [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs)擴充功能。<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>WSAID \_ TRANSMITFILE<br/>                         | [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)擴充功能。<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>WSAID \_ TRANSMITPACKETS<br/>                | [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets)擴充功能。 <br/>          |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>WSAID \_ WSARECVMSG<br/>                               | [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)擴充功能。<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>WSAID \_ WSASENDMSG<br/>                               | [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)擴充功能。 <br/>                      |

### <a name="sio_get_group_qos-opcode-setting-o-i-t1"></a>SIO \_ 取得 \_ 群組 \_ QOS (操作碼設定： O，I，T = = 1) 

保留供未來使用通訊端使用。

取得與此通訊端所屬之通訊端群組相關聯的 [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) 結構。 輸入緩衝區是選擇性的。 某些通訊協定 (例如，「RSVP) 允許輸入緩衝區用來限定服務要求的品質。 **QOS** 結構將會複製到輸出緩衝區。 如果這個通訊端不屬於適當的通訊端群組，則傳回的 **QOS** 結構的 **SendingFlowspec** 和 **ReceivingFlowspec** 成員會設定為 **Null**。 針對不支援服務品質的服務提供者，會指出 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) 錯誤碼。

### <a name="sio_get_interface_list-opcode-setting-o-t0"></a>SIO \_ GET \_ INTERFACE \_ LIST (Opcode 設定： O，T = = 0) 

傳回已設定的 IP 介面及其參數的清單，做為 [**介面 \_ 資訊**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) 結構的陣列。

> [!Note]  
> 對 Windows 通訊端2相容的 TCP/IP 服務提供者，此命令的支援是必要的。

*LpvOutBuffer* 參數會指向緩衝區，以將介面的相關資訊儲存為介面上單播 IP 位址的 [**介面 \_ 資訊**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info)結構陣列。 *CbOutBuffer* 參數會指定輸出緩衝區的長度。 在 *lpvOutBuffer* 參數所指向的緩衝區中傳回的結構數目 (傳回的介面數目) 可以根據 *lpcbBytesReturned* 參數中所傳回之輸出緩衝區的實際長度來決定。

如果使用 **SIO \_ GET \_ INTERFACE \_ LIST** 呼叫 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)函式，而通訊端 *s* 參數的層級成員未定義為 **IPPROTO \_ IP**，則會傳回 **WSAEINVAL** 。 如果指定輸出緩衝區長度的 *cbOutBuffer* 參數太小，則呼叫 **WSAIoctl** 函式的 **SIO \_ GET \_ INTERFACE \_ list** 會傳回 **WSAEFAULT** ，以取得已設定的介面清單。

**SIO \_GET \_ INTERFACE \_ LIST** 在 Windows Me/98 和 Windows NT 4.0 加裝 SP4 和更新版本支援。

### <a name="sio_get_interface_list_ex-opcode-setting-o-t0"></a>SIO \_ 取得 \_ 介面 \_ 清單， \_ 例如 (操作碼設定： O、T = = 0) 

保留供未來使用通訊端使用。

傳回已設定的 IP 介面及其參數的清單，做為 [**介面 \_ 資訊 \_ EX**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) 結構的陣列。

*LpvOutBuffer* 參數會指向緩衝區，以將介面的相關資訊儲存為介面上單播 IP 位址 [**的 \_ 介面 \_ 資訊**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex)的陣列。 *CbOutBuffer* 參數會指定輸出緩衝區的長度。 傳回的介面數目 (在 *lpvOutBuffer* 中傳回的結構數目) 可根據 *lpcbBytesReturned* 參數中所傳回之輸出緩衝區的實際長度來決定。

**SIO \_Windows 上目前不支援取得 \_ 介面 \_ 清單 \_ EX** 。

### <a name="sio_get_qos-opcode-setting-o-t1"></a>SIO \_ 取得 \_ QOS (操作碼設定： O，T = = 1) 

保留供未來使用通訊端使用。 取出與通訊端相關聯的 [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) 結構。 輸入緩衝區是選擇性的。 某些通訊協定 (例如，「RSVP) 允許輸入緩衝區用來限定服務要求的品質。 **QOS** 結構將會複製到輸出緩衝區。 輸出緩衝區的大小必須夠大，才能包含完整的 **QOS** 結構。 針對不支援服務品質的服務提供者，會指出 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) 錯誤碼。

傳送者可能不會呼叫 **SIO \_ 取得 \_ QOS** ，直到通訊端連線為止。

接收者可能會在系結時呼叫 **SIO \_ 取得 \_ QOS** 。

### <a name="sio_ideal_send_backlog_change-opcode-setting-v-t0"></a>SIO \_ 理想的 \_ 傳送待處理專案 \_ \_ 變更 (操作碼設定： V，T = = 0) 

當理想的傳送待處理專案 (ISB) 值變更基礎連接時通知應用程式。

使用 Windows sockets 透過 TCP 連線傳送資料時，請務必保留足夠的資料量， (傳送但尚未認可到 TCP 中的) ，以達到最高的輸送量。 若要達到 TCP 連接的最佳輸送量，最理想的資料量值就稱為「理想的傳送待處理專案」 (ISB) 大小。 ISB 值是 TCP 連線之頻寬延遲乘積的函式，而接收者的通告接收視窗 (以及網路) 中的擁塞量部分。

您可以從 Windows Server 2008、Windows Vista SP1 和更新版本的作業系統中的 TCP 通訊協定，取得每個連接的 ISB 值。 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 可供應用程式使用，以在 ISB 值針對連接動態變更時取得通知。

如需詳細資訊，請參閱 [**SIO \_ 理想的 \_ 傳送 \_ 待 \_**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) 處理專案變更參考。

[**SIO \_Windows \_ Server \_ \_**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) 2008、windows Vista SP1 和更新版本的作業系統都支援理想的傳送待處理專案變更。

### <a name="sio_ideal_send_backlog_query-opcode-setting-o-t0"></a>SIO \_ 理想 \_ 的傳送待處理專案 \_ （BACKLOG） \_ 查詢 (操作碼設定： O，T = = 0) 

抓取基礎連接 (ISB) 值的理想傳送待辦專案。

使用 Windows sockets 透過 TCP 連線傳送資料時，請務必保留足夠的資料量， (傳送但尚未認可到 TCP 中的) ，以達到最高的輸送量。 若要達到 TCP 連接的最佳輸送量，最理想的資料量值就稱為「理想的傳送待處理專案」 (ISB) 大小。 ISB 值是 TCP 連線之頻寬延遲乘積的函式，而接收者的通告接收視窗 (以及網路) 中的擁塞量部分。

您可以從 Windows Server 2008 和更新版本中的 TCP 通訊協定，取得每個連接的 ISB 值。 **SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 可以由應用程式用來查詢連接的 ISB 值。

如需詳細資訊，請參閱 [**SIO \_ 理想的 \_ 傳送 \_ 待 \_**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) 處理專案查詢參考。

[**SIO \_Windows \_ Server \_ \_**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) 2008、windows Vista SP1 和更新版本的作業系統都支援理想的傳送待處理專案查詢。

### <a name="sio_keepalive_vals-opcode-setting-i-t3"></a>SIO \_ KEEPALIVE \_ VALS (opcode 設定： I，T = = 3) 

啟用或停用 TCP **keep-alive** 選項的每一連接設定，以指定 tcp keep-alive timeout 和 interval。 如需保持連線選項的詳細資訊，請參閱4.2.3.6 中的「 *網際網路主機需求* 」一節：在 [IETF 網站](https://www.ietf.org/rfc/rfc1122.txt)提供的 RFC 1122 中所指定的通訊層。  (此資源可能僅提供英文版。 ) 

**SIO \_KEEPALIVE \_ VALS** 可用來啟用或停用 keep-alive 探查，並設定 keep-alive timeout 和 interval。 Keep-alive timeout 會以毫秒為單位來指定在第一個 keep-alive 封包傳送之前沒有任何活動的超時時間。 Keep-alive 間隔會指定如果沒有收到任何通知，在連續的 keep-alive 封包傳送時的間隔（以毫秒為單位）。

「 [**使用 \_ 中存留」選項（**](so-keepalive.md) 也就是其中一個「 [SOL \_ 通訊端通訊端」選項](sol-socket-socket-options.md)）也可用來啟用或停用連線上的 TCP keep-alive，以及查詢此選項的目前狀態。 若要查詢是否在通訊端上啟用 TCP keep-alive，可以使用「使用 **\_ KEEPALIVE** 」選項來呼叫 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函數。 若要啟用或停用 TCP 保持連線，您可以使用 [使用 [**\_ KEEPALIVE**](so-keepalive.md) ] 選項來呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函數。 如果啟用 TCP keep-alive，則會將預設 TCP 設定用於保持連線的超時時間和 **間隔，除非 \_** 使用 **SIO \_ KEEPALIVE \_ VALS** 變更這些值。

如需詳細資訊，請參閱 [**SIO \_ KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) 參考。 **SIO \_Windows \_** 2000 和更新版本支援 KEEPALIVE VALS。

### <a name="sio_loopback_fast_path-opcode-setting-i-t3"></a>SIO \_ 回送 \_ 快速 \_ 路徑 (操作碼設定： I，T = = 3) 

在回送介面上設定 TCP 通訊端，以降低延遲和加快作業的速度。 此 IOCTL 要求 TCP/IP 堆疊針對此通訊端上的回送作業使用特殊的快速路徑。 [**SIO \_ 回送 \_ 快速 \_ 路徑**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85))IOCTL 只能用於 TCP 通訊端。 這個 IOCTL 必須用於回送會話的兩端。 您可以使用 IPv4 或 IPv6 回送介面，來支援 TCP 回送快速路徑。 預設會停用 **SIO \_ 回送 \_ 快速 \_ 路徑** 。

如需詳細資訊，請參閱 [**SIO \_ 回送 \_ 快速 \_ 路徑**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) 參考。 **SIO \_Windows 8 \_ \_** 、Windows Server 2012 及更新版本都支援回送快速路徑。

### <a name="sio_multipoint_loopback-opcode-setting-v-t1"></a>SIO \_ MULTIPOINT \_ 回送 (操作碼設定： V，T = = 1) 

控制應用程式在本機電腦上傳送的資料 (不一定是在多播會話中的相同通訊端) ，將會由聯結至回送介面上多播目的地群組的通訊端接收。 **TRUE** 值會導致本機電腦上的應用程式傳送的多播資料，傳遞給回送介面上的接聽通訊端。 值為 **FALSE** 可防止本機電腦上的應用程式傳送的多播資料，將其傳遞至回送介面上的接聽通訊端。 預設會啟用 **SIO \_ MULTIPOINT \_ 回送** 。

### <a name="sio_multicast_scope-opcode-setting-i-t1"></a>SIO \_ 多播 \_ 範圍 (操作碼設定： I，T = = 1) 

指定將進行多播傳輸的範圍。 範圍定義為要涵蓋的路由網路區段數目。 範圍為零會指出多播傳輸不會放置在網路上，但是可以跨本機主機內的通訊端簡易性。 一個範圍值 (預設) 表示傳輸將放置在網路上，但不會跨越任何路由器。 較高範圍的值會決定可跨越的路由器數目。 請注意，這會對應至 IP 多播中的存留時間 (TTL) 參數。 範圍預設為1。

### <a name="sio_query_rss_processor_info-opcode-setting-o-t1"></a>SIO \_ 查詢 \_ RSS \_ 處理器 \_ 資訊 (操作碼設定： O，T = = 1) 

查詢通訊端與 RSS 處理器核心和 NUMA 節點之間的關聯。

[**SIO \_ 查詢 \_ RSS \_ 處理器 \_ 資訊**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85))IOCTL 會傳回 [**通訊端 \_ 處理器 \_ 親和性**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)結構，其中包含 [**處理器 \_ 編號**](/windows/win32/api/winnt/ns-winnt-processor_number)和 NUMA 節點識別碼。 傳回的 **處理器 \_ 編號** 結構包含群組中的群組編號和相對處理器號碼。

如需詳細資訊，請參閱 [**SIO \_ 查詢 \_ RSS \_ 處理器 \_ 資訊**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) 參考。 **SIO \_Windows 8、Windows Server 2012 及更新版本都支援查詢 \_ RSS \_ 處理器 \_ 資訊** 。

### <a name="sio_query_rss_scalability_info-opcode-setting-o-t3"></a>SIO \_ 查詢 \_ RSS 擴充 \_ 性 \_ 資訊 (操作碼設定： O，T = = 3) 

查詢會卸載用於接收端調整 (RSS) 功能的介面。 針對 **SIO \_ 查詢 \_ RSS 擴充 \_ 性 \_ 資訊** 所傳回的引數結構，是在 *Mstcpip .h* 標頭檔中定義的 **RSS 擴充 \_ 性 \_ 資訊** 結構中指定。 此結構的定義如下：

```cpp
// Scalability info for the transport
typedef struct _RSS_SCALABILITY_INFO {
   BOOLEAN RssEnabled;
} RSS_SCALABILITY_INFO, *PRSS_SCALABILITY_INFO;
```

在 **RssEnabled** 成員中傳回的值會指出是否已在至少一個介面上啟用 RSS。

如果輸出緩衝區不夠大，無法滿足 Rss 的 **擴充 \_ 性 \_ 資訊** 結構 (*cbOutBuffer* 小於 **rss 擴充 \_ 性 \_ 資訊** 的大小) 或 *lpvOutBuffer* 參數為 **Null** 指標，則會傳回 **通訊端 \_ 錯誤** ，因為這個 IOCTL 的結果和 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEINVAL](windows-sockets-error-codes-2.md)。

在多個 Cpu 位於單一系統內的高速網路中，會禁止網路通訊協定堆疊在多 CPU 系統上適當調整的能力，因為 NDIS 5.1 和較早版本的架構會限制只接收單一 CPU 的通訊協定處理。 接收端調整 (RSS) 可讓網路介面卡的網路負載跨多個 Cpu 進行平衡，藉此解決此問題。

**SIO \_Windows Vista 和更新版本支援查詢 \_ RSS 擴充 \_ 性 \_ 資訊** 。

### <a name="sio_query_transport_setting-opcode-setting-i-t3"></a>SIO \_ 查詢 \_ 傳輸 \_ 設定 (操作碼設定： I，T = = 3) 

查詢通訊端上的傳輸設定。 正在查詢的傳輸設定是以 *lpvInBuffer* 參數中傳遞的 [**傳輸 \_ 設定 \_ 識別碼**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id)為基礎。

目前唯一定義的傳輸設定是用於 TCP 通訊端上的 **即時 \_ \_ 通知 \_ 功能** 功能。

如果 [**傳輸 \_ 設定 \_ 識別碼**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) 的 **Guid** 成員設為 **即時 \_ \_ 通知 \_ 功能**，則需要查詢與 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) 搭配使用之 TCP 通訊端的即時通知設定，以在 Windows Store 應用程式中接收背景網路通知。 如果 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 或 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) 呼叫成功，這個 IOCTL 會以目前的狀態傳回 [**即時 \_ \_ 通知 \_ 設定 \_ 輸出**](/windows/desktop/api/Mstcpip/ns-mstcpip-real_time_notification_setting_input) 結構。

如需詳細資訊，請參閱 [**SIO \_ 查詢 \_ 傳輸 \_ 設定**](/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)) 參考。 **SIO \_Windows 8 \_ \_** 、Windows Server 2012 及更新版本都支援查詢傳輸設定。

### <a name="sio_query_wfp_ale_endpoint_handle-opcode-setting-o-t3"></a>SIO \_ QUERY \_ WFP \_ ALE \_ 端點 \_ 控制碼 (操作碼設定： O，T = = 3) 

查詢應用層強制 (ALE) 端點控制碼。

 (WFP 的 Windows 篩選平台) 支援網路流量檢查和修改。 在 Windows Vista 上，WFP 著重于主機電腦是通訊端點的案例。 不過，在 Windows Server 2008 上，有邊緣防火牆的執行，想要利用 WFP 平臺來檢查和 proxy 傳遞流量。 Internet Security and 加速 (ISA) server 是這類邊緣裝置的範例。

有些防火牆案例可能需要能夠將輸入封包插入與現有端點相關聯的傳送路徑。 需要有一種機制來探索與目的地端點相關聯的傳輸層端點控制碼。 建立端點的應用程式擁有這些傳輸層端點。 這個 IOCTL 可用來提供通訊端控制碼給傳輸層端點控制碼對應。

如果輸出緩衝區不夠大，以致于端點控制碼 (*cbOutBuffer* 小於 **UINT64**) 的大小，或 *lpvOutBuffer* 參數為 **Null** 指標，則會傳回 **通訊端 \_ 錯誤** ，因為這個 IOCTL 的結果和 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEINVAL](windows-sockets-error-codes-2.md)。

**SIO \_Windows Vista 和更新版本支援查詢 \_ WFP \_ ALE \_ 端點 \_ 控制碼** 。

### <a name="sio_query_wfp_connection_redirect_context-opcode-setting-i-t3"></a>SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 內容 (操作碼設定： I，T = = 3) 

查詢重新導向內容，以取得 Windows 篩選平台 (WFP) 重新導向服務所使用的重新導向記錄。

[**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 內容**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85))IOCTL 可用來在重新導向的通訊端連線上提供代理的連接追蹤。 這種 WFP 功能可從連接的初始重新導向到目的地的最終連接，來協助追蹤重新導向記錄。

如需詳細資訊，請參閱 [**SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 內容**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) 參考。 **SIO \_Windows 8、Windows Server 2012 及更新版本都支援查詢 \_ WFP \_ 連接重新 \_ 導向 \_ 內容** 。

### <a name="sio_query_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ 查詢 \_ WFP \_ 連接重新 \_ 導向 \_ 記錄 (操作碼設定： I，T = = 3) 

查詢已接受 TCP/IP 連接的重新導向記錄，以供 Windows 篩選平台 (WFP) 重新導向服務使用。

[**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 記錄**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85))IOCTL 可用來在重新導向的通訊端連線上提供代理的連接追蹤。 這種 WFP 功能可從連接的初始重新導向到目的地的最終連接，來協助追蹤重新導向記錄。

如需詳細資訊，請參閱 [**SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 記錄**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) 參考。 **SIO \_Windows 8、Windows Server 2012 及更新版本都支援查詢 \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 。

### <a name="sio_rcvall-opcode-setting-i-t3"></a>SIO \_ RCVALL (opcode 設定： I，T = = 3) 

可讓通訊端接收傳遞 throuigh 網路介面的所有 IPv4 或 IPv6 封包。 傳遞至 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式的通訊端控制碼必須是下列其中一項：

-   以位址系列設定為 AF \_ INET、通訊端類型設定為 SOCK \_ RAW，以及將通訊協定設定為 IPPROTO IP 所建立的 IPv4 通訊端 \_ 。
-   以位址系列設定為 AF \_ INET6、通訊端類型設定為 SOCK \_ RAW，以及將通訊協定設定為 IPPROTO IPv6 所建立的 IPv6 通訊端 \_ 。

通訊端也必須系結至明確的本機 IPv4 或 IPv6 介面，這表示您無法系結至 **INADDR \_ any** 或 **in6addr \_ any**。

在 Windows Server 2008 及更早版本中， [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) IOCTL 設定不會捕捉從網路介面送出的本機封包。 這包含在另一個介面上收到的封包，並將針對 **SIO \_ RCVALL** IOCTL 指定的網路介面轉送出去。

在 Windows 7 和 Windows Server 2008 R2 上，這項變更已變更，因此也會捕捉從網路介面送出的本機封包。 這包括在另一個介面上收到的封包，然後使用 [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) IOCTL 轉送系結至通訊端的網路介面。

設定這個 IOCTL 需要本機電腦的系統管理員許可權。

這項功能有時稱為混合模式。

**SIO \_ RCVALL** IOCTL 選項的可能值是在 *Mstcpip. .h* 標頭檔中定義的 **RCVALL \_ 值** 列舉中指定。 SIO RCVALL 的可能值如下 \_ ：

| 詞彙                                                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-|-|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>RCVALL \_ 關閉<br/>                                     | 停用此選項，讓通訊端不會接收網路上的所有 IPv4 或 IPv6 封包。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>RCVALL \_ 于<br/>                                        | 啟用此選項，讓通訊端接收網路上的所有 IPv4 或 IPv6 封包。 如果 NIC 支援混合模式，此選項會在網路介面卡上啟用混合模式 (NIC) 。 在網路中樞的 LAN 區段上，支援混合模式的 NIC 會在 LAN 上捕捉所有 IPv4 或 IPv6 流量，包括相同 LAN 區段上其他電腦之間的流量。 所有 (IPv4 或 IPv6 的已捕捉封包，視通訊端) 將會傳遞至原始通訊端而定。 <br/> 此選項不會將其他封包捕獲 (ARP、IPX 和 NetBEUI 封包，例如介面上的) 。<br/> Netmon 針對網路介面使用相同的模式，但不會使用此選項來捕捉流量。<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>RCVALL \_ SOCKETLEVELONLY<br/> | 這項功能目前未執行，因此設定此選項不會有任何影響。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>RCVALL \_ IPLEVEL<br/>                         | 啟用此選項，讓 IPv4 或 IPv6 通訊端接收網路上 IP 層級的所有封包。 此選項不會在網路介面卡上啟用混合模式。 此選項只會影響在 IP 層級的封包處理。 NIC 仍只接收導向至其設定之單播和多播位址的封包。 不過，啟用此選項的通訊端不只會接收導向至特定 IP 位址的封包，而是會接收 NIC 接收的所有 IPv4 或 IPv6 封包。<br/> 此選項不會將其他封包捕捉 (ARP、IPX 和 NetBEUI 封包，例如在介面上收到) 。<br/>                                                                                             |



 

如需詳細資訊，請參閱 [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) 參考。

**SIO \_** Windows 2000 和更新版本支援 RCVALL。

### <a name="sio_rcvall_igmpmcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ IGMPMCAST (opcode 設定： I，T = = 3) 

可讓通訊端接收網路上的所有 IGMP 多播 IP 流量，而不會接收其他多播 IP 流量。 傳遞至 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式的通訊端控制碼必須為 AF \_ INET 位址系列、SOCK \_ 原始通訊端類型和 IPPROTO \_ IGMP 通訊協定。 通訊端也必須系結至明確的本機介面，這表示您無法系結至 INADDR \_ ANY。

系結通訊端並設定 IOCTL 之後，對 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) 或 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 函式的呼叫會傳回透過指定介面傳遞的多播 IP 資料包。 請注意，您必須提供夠大的緩衝區。 設定這個 IOCTL 需要本機電腦的系統管理員許可權。

**SIO \_Windows \_** 2000 和更新版本支援 RCVALL IGMPMCAST。

### <a name="sio_rcvall_mcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ MCAST (opcode 設定： I，T = = 3) 

可讓通訊端接收網路上的所有多播 IP 流量 (也就是說，以224.0.0.0 到239.255.255.255 為範圍的 IP 位址為目標的所有 IP 封包) 。 傳遞至 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式的通訊端控制碼必須為 AF \_ INET 位址系列、SOCK \_ 原始通訊端類型和 IPPROTO \_ UDP 通訊協定。 通訊端也必須系結至明確的本機介面，這表示您無法系結至 INADDR \_ ANY。 通訊端應系結至埠零。

系結通訊端並設定 IOCTL 之後，對 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) 或 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 函式的呼叫會傳回透過指定介面傳遞的多播 IP 資料包。 請注意，您必須提供夠大的緩衝區。 設定這個 IOCTL 需要本機電腦的系統管理員許可權。

**SIO \_Windows \_** 2000 和更新版本支援 RCVALL MCAST。

### <a name="sio_release_port_reservation-opcode-setting-i-t3"></a>SIO \_ 版本 \_ 埠 \_ 保留 (操作碼設定： I，T = = 3) 

針對 TCP 或 UDP 埠的區塊釋放執行時間保留。 您必須使用 [**SIO \_ 取得 \_ 埠 \_ 保留**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) IOCTL，從發行程式取得要發行的執行時間保留。

如需詳細資訊，請參閱 [**SIO \_ 版本 \_ 埠 \_ 保留**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) 參考。

[**SIO \_Windows \_ \_**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) Vista 和更新版本的作業系統支援發行埠保留。

### <a name="sio_routing_interface_change-opcode-setting-i-t1"></a>SIO \_ 路由 \_ 介面 \_ 變更 (操作碼設定： I，T = = 1) 

若要接收路由介面變更的通知，而這些變更應該用來到達輸入緩衝區中的遠端位址 (指定為 [**sockaddr**](sockaddr-2.md) 結構) 。 這項 IOCTL 完成時，將不會提供新路由介面上的輸出資訊;完成隻會指出給定目的地的路由介面已經變更，應該使用 **SIO \_ 路由 \_ 介面 \_ 查詢** IOCTL 來查詢。

雖然並非必要，但應用程式會使用重迭的 i/o 來通知路由介面變更，以及完成 **SIO \_ 路由 \_ 介面 \_ 變更** 要求。 或者，如果 **SIO \_ 路由 \_ 介面 \_ 變更** IOCTL 是在 *LpOverlapped* 和 *lpCompletionRoutine* 參數設定為 **Null**) 的非封鎖通訊端上發出的，則它會立即完成傳回並 [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md) 為錯誤，然後應用程式可以透過呼叫 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 或 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) ，以在 \_ \_ \_ 網路事件位元遮罩中設定的 FD 路由介面變更位來等候路由變更事件。

在大部分的情況下，這是因為路由資訊會保持穩定，因此需要應用程式保留多個未處理的 IOCTLs 來取得有關它感興趣的所有目的地的通知，以及讓服務提供者追蹤這些通知要求，將會使用大量系統資源。 您可以藉由擴充輸入參數的意義，並放寬服務提供者需求，來避免這種情況，如下所示：

-   當要求系結至任何可用的位址) 以要求任何路由變更的通知時，應用程式可以指定通訊協定系列特定的萬用字元位址 (與系 [**結呼叫中所使用的相同**](/windows/desktop/api/winsock/nf-winsock-bind) 。 如此一來，應用程式就只會針對它所擁有的所有通訊端和目的地，保留一個未完成的 **SIO \_ 路由 \_ 介面 \_ 變更** ，然後使用 **SIO \_ 路由 \_ 介面 \_ 查詢** 來取得實際的路由資訊。
-   服務提供者可以選擇忽略 **SIO \_ 路由 \_ 介面 \_ 變更** 之輸入緩衝區中的應用程式所指定的資訊 (就像應用程式指定了萬用字元位址) ，並在發生任何路由資訊變更時完成 **SIO \_ 路由 \_ 介面 \_** 變更 IOCTL 或信號 FD \_ 路由 \_ 介面 \_ 變更事件， (不只是輸入緩衝區) 中指定之目的地的路由。

### <a name="sio_routing_interface_query-opcode-setting-i-o-t1"></a>SIO \_ 路由 \_ 介面 \_ 查詢 (操作碼設定： I、O、T = = 1) 

若要取得本機介面的位址 (以 [**sockaddr**](sockaddr-2.md) 結構表示，) 應該用來傳送至輸入緩衝區中指定的遠端位址， (為 **sockaddr**) 。 您可以在輸入緩衝區中提交遠端多播位址，以取得適用于多播傳輸的慣用介面位址。 在任何情況下，應用程式可能會在後續 bind () 要求中使用傳回的介面位址。

請注意，路由可能會變更。 因此，應用程式無法依賴 **SIO \_ 路由 \_ 介面 \_ 查詢** 所傳回的資訊持續存在。 應用程式可以透過 **SIO \_ 路由 \_ 介面 \_ 變更** IOCTL 來註冊路由變更通知，以透過重迭的 I/o 或 FD \_ 路由 \_ 介面變更事件提供通知 \_ 。 下列一系列的動作可以用來保證應用程式一律具有指定目的地的目前路由介面資訊：

-   發出 **SIO \_ 路由 \_ 介面 \_ 變更** IOCTL 的問題
-   發出 **SIO \_ 路由 \_ 介面 \_ 查詢** IOCTL 的問題
-   每當 **SIO \_ 路由 \_ 介面 \_ 變更** IOCTL 通知應用程式傳送變更時 (透過重迭的 i/o，或藉由發出 \_) 的 FD 路由 \_ 介面 \_ 變更事件，就應該重複執行整個動作順序。

如果輸出緩衝區不夠大，無法包含介面位址， \_ 則會傳回通訊端錯誤，因為這個 IOCTL 的結果和 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEFAULT](windows-sockets-error-codes-2.md)。 在此情況下， *lpcbBytesReturned* 會傳回所需的輸出緩衝區大小。 請注意，如果 *lpvInBuffer*、 *lpvOutBuffer* 或 *lpcbBytesReturned* 參數未完全包含在使用者位址空間的有效部分中，也會傳回 WSAEFAULT 錯誤碼。

如果無法透過任何可用的介面到達輸入緩衝區中指定的目的地位址， \_ 則會傳回通訊端錯誤，因為這個 IOCTL 的結果和 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會在所有網路連線都遺失時傳回 [WSAENETUNREACH](windows-sockets-error-codes-2.md) ，甚至是 [WSAENETDOWN](windows-sockets-error-codes-2.md) 。

### <a name="sio_set_compatibility_mode-opcode-setting-i-t3"></a>SIO \_ 設定 \_ 相容性 \_ 模式 (操作碼設定： I，T = = 3) 

要求網路堆疊應該如何處理特定行為，而這種行為的預設處理方式可能會在 Windows 版本之間不同。 **SIO \_ 集 \_ 相容性 \_ 模式** 的引數結構是在 *Mswsockdef .H* 標頭檔中定義的 **WSA \_ 相容性 \_ 模式** 結構中指定。 此結構的定義如下：

```cpp
/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

**BehaviorId** 成員中指定的值會指出所要求的行為。 **TargetOsVersion** 成員中指定的值會指出所要求的行為的 Windows 版本。

**BehaviorId** 成員可以是 *Mswsockdef .h* 標頭檔中所定義之 **WSA \_ 相容性 \_ 行為 \_ 識別碼** 列舉類型的其中一個值。 **BehaviorId** 成員的可能值如下所示。

| 詞彙                                                                                                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-|-|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>WsaBehaviorAll<br/>                                                     | 這相當於要求針對 **WSA \_ 相容性 \_ 行為 \_ 識別碼** 定義的所有可能相容行為。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>WsaBehaviorReceiveBuffering<br/> | 當 **TargetOsVersion** 成員設定為 Windows Vista 或更新版本的值時，即使在建立 tcp 連線之後，也允許使用 **SO \_ RCVBUF** 通訊端選項減少此通訊端上的 TCP 接收緩衝區大小。 <br/> 當 **TargetOsVersion** 成員設定為早于 Windows Vista 的值時，在連線建立之後，就不允許使用 **\_ RCVBUF** 通訊端選項來降低此通訊端上的 TCP 接收緩衝區大小。 <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>WsaBehaviorAutoTuning<br/>                         | 當 **TargetOsVersion** 成員設定為 Windows Vista 或更新版本的值時，會啟用 [接收視窗自動調整]，並將 [TCP 視窗縮放比例] 從預設值8縮減為2。<br/> 當 **TargetOsVersion** 設定為 Windows Vista 之前的值時，會停用 [接收視窗自動調整]。 [TCP 視窗調整] 選項也會停用，而 [最大值] 接收視窗大小則限制為65535個位元組。 即使在此通訊端上呼叫 **\_ RCVBUF** 通訊端選項，在建立連接之前指定大於65535個位元組的值，也無法在連接上協商 TCP 視窗調整選項。<br/> |



 

如需詳細資訊，請參閱 [**SIO \_ SET \_ 相容性 \_ 模式**](/previous-versions/windows/desktop/legacy/cc136103(v=vs.85)) 參考。

**SIO \_Windows Vista 和更新版本支援設定 \_ 相容性 \_ 模式** 。

### <a name="sio_set_group_qos-opcode-setting-i-t1"></a>SIO \_ 設定 \_ 群組 \_ QOS (操作碼設定： I，T = = 1) 

保留的。

### <a name="sio_set_priority_hint-opcode-setting-i-t3"></a>SIO_SET_PRIORITY_HINT (opcode 設定： I，T = = 3) 

提供提示給基礎傳輸通訊協定，以將此通訊端上的流量視為特定優先權。 *LpvInBuffer* 必須指向類型 **PRIORITY_HINT** 的變數，並將 *cbInBuffer* 設定為 sizeof (PRIORITY_HINT) 。 *LpvOutBuffer* 和 *cbOutBuffer* 參數必須分別為 **Null** 和0。 Microsoft Windows TCP 執行支援此 IOCTL，從 Windows 10 版本 1809 (10.0;組建 17763) 和更新版本，如下所示：當要求的優先權值設定為 **IoPriorityHintVeryLow** 時，TCP 會使用 LEDBAT 演算法的修改版本， (在 RFC 6817) 中定義，以控制通訊端上的輸出流量速率。 輸入流量不會受到這個 IOCTL 的影響。 LEDBAT 是一種清除程式演算法，其目標是要讓延遲降至最低，並防止對一般優先順序流量造成任何不利的影響，方法是在有正常優先順序的流量時，繼續進行。

另請參閱 [RFC 6817](https://tools.ietf.org/html/rfc6817)。

**SIO_SET_PRIORITY_HINT** 支援 Windows 10 版本 1809 (10.0;組建 17763) 和更新版本。

### <a name="sio_set_qos-opcode-setting-i-t1"></a>SIO \_ 將 \_ QOS (opcode 設定： I，T = = 1) 

將指定的 [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) 結構與通訊端建立關聯。 不需要輸出緩衝區，系統會從輸入緩衝區取得 **QOS** 結構。 針對不支援服務品質的服務提供者，會指出 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) 錯誤碼。

### <a name="sio_tcp_initial_rto-opcode-setting-i-t3"></a>SIO_TCP_INITIAL_RTO (opcode 設定： I，T = = 3) 

藉由設定初始重新傳輸超時 (RTO) 參數，來控制 TCP 通訊端的初始 (SYN/SYN + ACK) 重新傳輸特性。 設定參數是在 [**TCP \_ 初始 \_ RTO \_ 參數**](/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers) 結構中指定的。

如需詳細資訊，請參閱 [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) 參考。 Windows 8、Windows Server 2012 及更新版本都支援 [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) 。

### <a name="sio_translate_handle-opcode-setting-i-o-t1"></a>SIO \_ 轉譯 \_ 控制碼 (opcode 設定： I、O、T = = 1) 

若要取得通訊端 *s* 的對應控制碼，該控制碼在隨附介面的內容中有效 (例如，第 \_ NETDEV 和第一次 \_ TAPI) 。 在輸入緩衝區中指定了識別隨附介面的資訊清單常數，以及任何其他需要的參數。 當此函式完成時，將會在輸出緩衝區中提供對應的控制碼。 請參閱 [Winsock 附件](winsock-annexes.md) 中的適當區段，以取得特定隨附介面特定的詳細資料。 針對指定的隨附介面不支援這個 IOCTL 的服務提供者，會指出 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) 錯誤碼。 這個 IOCTL 會使用 **SIO \_ 轉譯 \_ 控制碼** 來抓取相關聯的控制碼。

建議您) 使用元件物件模型 (COM，而不使用這個 IOCTL 來探索和追蹤通訊端可能支援的其他介面。 這個 IOCTL 存在的目的是為了讓 COM 無法使用或無法用於其他原因的系統回溯相容性。

### <a name="sio_udp_connreset-opcode-setting-i-t3"></a>SIO \_ UDP \_ CONNRESET (opcode 設定： I，T = = 3) 

**WINDOWS XP：** 控制是否報告 UDP 埠 \_ 無法連線的訊息。 設定為 **TRUE** 以啟用報告功能。 設定為 **FALSE** 會停用報告。

### <a name="sio_set_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ 設定 \_ WFP \_ 連接重新 \_ 導向 \_ 記錄 (操作碼設定： I，T = = 3) 

將重新導向記錄設定為新的 TCP 通訊端，用來連接到最終目的地，以供 Windows 篩選平台 (WFP) 重新導向服務使用。

在重新導向的通訊端連線上，會使用 [**SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) IOCTL 作為 proxy 連接追蹤的一部分。 這種 WFP 功能可從連接的初始重新導向到目的地的最終連接，來協助追蹤重新導向記錄。

如需詳細資訊，請參閱 [**SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) 參考。 **SIO \_Windows 8、Windows Server 2012 及更新版本都支援設定 \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 。

### <a name="sio_tcp_info-opcode-setting-i-o-t3"></a>SIO \_ TCP \_ 資訊 (操作碼設定： I、O、T = = 3) 

抓取通訊端的 TCP 統計資料。 Tcp [**\_ 資訊 \_ v0**](/windows/desktop/api/Mstcpip/ns-mstcpip-tcp_info_v0) 結構中會提供 tcp 統計資料。

與使用 [**GetPerTcpConnectionEStats**](/windows/win32/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) 函式來抓取 tcp 統計資料不同的是，使用這個控制項程式碼來抓取 tcp 統計資料並不需要使用者程式碼來載入、儲存和篩選 tcp 連接資料表，也不需要使用較高的許可權。

如需詳細資訊，請參閱 [**SIO \_ TCP \_ 資訊**](/previous-versions/windows/desktop/legacy/mt823415(v=vs.85))。 **SIO \_Windows 10 \_** 、1703版、Windows Server 2016 和更新版本都支援 TCP 資訊。

## <a name="remarks"></a>備註

Winsock Ioctls 是以許多不同的標頭檔定義。 這些包括 *Winsock2. .h*、 *Mswsock .h* 和 *Mstcpip .h* 標頭檔。

在 Windows Vista （含）以後版本的 Microsoft Windows 軟體開發套件 (SDK) 上，標頭檔的組織已變更，而且 *Ws2def .h*、 *Ws2ipdef .h* 和 *Mswsockdef .h* 標頭檔中也會定義一些 Winsock Ioctls。 *Ws2def. h* 標頭檔會自動包含在 *Winsock2* 標頭檔中。 *Ws2ipdef .h* 標頭檔會自動包含在 *Ws2tcpip .h* 標頭檔中。 *Mswsockdef .h* 標頭檔會自動包含在 *Mswsockdef .h* 標頭檔中。

## <a name="requirements"></a>規格需求

|||
|-|-|
| 標頭<br/> | <dl> <dt>Winsock2. h;</dt><dt>Mstcpip .h;</dt><dt>Mswsock .h;</dt><dt>Windows Vista、Windows Server 2008 和 windows 7 (的 Mswsockdef，包括 Mswsock) ;</dt><dt>Windows Vista、Windows Server 2008 和 windows 7 (的 Ws2def，包括 Winsock2) ;</dt><dt>Windows Vista、Windows Server 2008 和 windows 7 (的 Ws2ipdef，包括 Ws2tcpip) </dt> </dl> |

---
description: 的設計目的是允許應用程式啟用通訊端連線的 keep-alive 封包。
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: 'SO_KEEPALIVE 通訊端選項 (Ws2def) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980577"
---
# <a name="so_keepalive-socket-option"></a>所以 \_ KEEPALIVE 通訊端選項

此「持續連線 **」通訊端 \_ 選項的設計** 目的是允許應用程式啟用通訊端連線的 keep-alive 封包。

若要查詢此通訊端選項的狀態，請呼叫 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函數。 若要設定此選項，請使用下列參數呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數。

## <a name="socket-option-value"></a>通訊端選項值

表示這個通訊端選項的常數是0x0008。

## <a name="syntax"></a>語法


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的 s\]
</dt> <dd>

識別通訊端的描述元。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

定義選項的層級。 使用 **SOL \_ 通訊端** 進行這種操作。

</dd> <dt>

*optname* \[在\]
</dt> <dd>

要設定其值的通訊端選項。 請使用此操作的 **\_ KEEPALIVE** 。

</dd> <dt>

*optval* \[擴展\]
</dt> <dd>

緩衝區的指標，其中包含要設定之選項的值。 此參數應指向等於或大於 **DWORD** 值大小的緩衝區。

此值會被視為布林值，0用來指出 **FALSE** (停用的) ，而非零值 **則表示 (啟用**) 。

</dd> <dt>

*optlen* \[in、out\]
</dt> <dd>

*Optval* 緩衝區大小的指標，以位元組為單位。 此大小必須等於或大於 **DWORD** 值的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 會傳回零。

如果作業失敗， \_ 則會傳回 SOCKET 錯誤的值，並藉由呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)來取出特定的錯誤碼。



| 錯誤碼                                                                                                                                              | 意義                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | 在使用此函式之前，必須先進行成功的 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 呼叫。<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | 網路子系統失敗。<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | 其中一個 *optval* 或 *optlen* 參數指向不在使用者位址空間有效部分的記憶體。 如果 *optlen* 參數所指向的值小於 **DWORD** 值的大小，也會傳回此錯誤。<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | 封鎖的 Windows 通訊端1.1 呼叫正在進行中，或服務提供者仍在處理回呼函數。<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | *層級* 參數未知或無效。 在 Windows Vista 和更新版本上，如果通訊端處於過渡狀態，也會傳回此錯誤。<br/>                                                                                                 |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | 指定的通訊協定系列未知或不支援此選項。 如果為資料包通訊端傳入 *s* 參數的通訊端描述元，則會傳回此錯誤。<br/>                                                                   |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | 描述項不是通訊端。<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>備註

使用「使用 **\_ KEEPALIVE** 通訊端」選項呼叫的 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函式可讓應用程式取出 KEEPALIVE 選項的目前狀態，不過這是通常不使用的功能。 如果應用程式需要在通訊端上啟用 keepalive 封包，它 justs 會呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式來啟用此選項。

以 with **\_ KEEPALIVE** 通訊端選項呼叫的 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式，可讓應用程式啟用通訊端連線的 keep-alive 封包。 預設會停用通訊端的 [ **SO \_ KEEPALIVE** ] 選項 (設定為 [ **FALSE** ]) 。

當這個通訊端選項啟用時，TCP 堆疊會在間隔內未收到連接的資料或通知封包時，傳送 keep-alive 封包。 如需保持連線選項的詳細資訊，請參閱4.2.3.6 中的「 *網際網路主機需求* 」一節：在 [IETF 網站](https://www.ietf.org/rfc/rfc1122.txt)提供的 RFC 1122 中所指定的通訊層。  (此資源可能僅提供英文版。 ) 

此 **「 \_** 持續連線」通訊端選項僅適用于支援保持運作 (連接導向的通訊協定) 概念的通訊協定。 若為 TCP，預設的 keep-alive timeout 為2小時，而 keep-alive 間隔為1秒。 預設的 keep-alive 探查數目會根據 Windows 版本而有所不同。

您可以使用 [**SIO \_ KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) control 程式碼來啟用或停用持續運作，以及調整單一連接的超時和間隔。 如果啟用 keep-alive，則 **會使用預設 \_** 的 TCP 設定來進行保持連線的超時時間和間隔，除非這些值已使用 **SIO \_ KEEPALIVE \_ VALS** 變更。

Keep-alive timeout 的預設全系統值可透過 [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) 登錄設定來控制，此設定會採用以毫秒為單位的值。 Keep-alive 間隔的預設全系統值可透過 [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) 登錄設定來控制，此設定會採用以毫秒為單位的值。

在 Windows Vista 和更新版本上， (資料重新傳輸) 的 keep-alive 探查數目設定為10，而且無法變更。

在 Windows Server 2003、Windows XP 及 Windows 2000 上，保持運作探查數目的預設設定為5。 Keep-alive 探查的數目可透過 [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) 和 [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) 登錄設定來控制。 Keep-alive 探查的數目會設定為兩個登錄機碼值的較大值。 如果這個數位為0，則不會傳送 keep-alive 探查。 如果此數位大於255，則會調整為255。

在 Windows Vista 和更新版本上，只有當通訊端處於已知狀態，而不是過渡狀態時，才能使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式來設定此「持續連線 **」通訊端 \_** 選項。 若為 TCP，則應該在 connect 函式 ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)、 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)、 [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)、 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)或 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) 呼叫之前，或在連接要求實際完成之後，設定 [ **SO \_ KEEPALIVE** 通訊端] 選項。 如果以非同步方式呼叫 connect 函式，則需要先等待連接完成，然後再嘗試設定「 **讓 \_ KEEPALIVE** 通訊端」選項。 如果應用程式在連線要求仍在處理時嘗試設定 [使用 **\_ KEEPALIVE** 通訊端] 選項， **setsockopt** 函式將會失敗，並傳回 [WSAEINVAL](windows-sockets-error-codes-2.md)。

在 Windows Server 2003、Windows XP 及 Windows 2000 上，如果通訊端是過渡狀態 (連接要求仍在進行中，則可以使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式來設定 [ **SO \_ KEEPALIVE** 通訊端] 選項，) 和已知狀態。

請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Ws2def (包含 Winsock2) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))
</dt> <dt>

[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))
</dt> <dt>

[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))
</dt> <dt>

[**插座**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**SIO \_ KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))
</dt> <dt>

[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 

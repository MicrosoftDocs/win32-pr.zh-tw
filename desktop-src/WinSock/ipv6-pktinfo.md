---
description: 允許應用程式啟用或停用 IPv6 通訊端上 WSARecvMsg 函式的封包資訊傳回。
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: 'IPV6_PKTINFO 通訊端選項 (Ws2ipdef) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd5b19cbaba7f6a66f5ba6fbd85d74eb2f2e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970807"
---
# <a name="ipv6_pktinfo-socket-option"></a>IPV6 \_ PKTINFO 通訊端選項

IPV6 \_ PKTINFO 通訊端選項可讓應用程式啟用或停用 ipv6 通訊端上的 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式的封包資訊。

若要查詢此通訊端選項的狀態，請呼叫 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函數。 若要設定此選項，請使用下列參數呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數。

## <a name="socket-option-value"></a>通訊端選項值

表示這個通訊端選項的常數是19。

## <a name="syntax"></a>語法


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
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

定義選項的層級。 使用 **IPPROTO \_ IPV6** 進行這種操作。

</dd> <dt>

*optname* \[在\]
</dt> <dd>

要取得或設定其值的通訊端選項。 使用 IPV6 \_ PKTINFO 進行這種操作。

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

如果作業順利完成， [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 或 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數會傳回零。

如果作業失敗， \_ 則會傳回 SOCKET 錯誤的值，並藉由呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)來取出特定的錯誤碼。



| 錯誤碼                                                                                                                                              | 意義                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | 在使用此函式之前，必須先進行成功的 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 呼叫。<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | 網路子系統失敗。<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | 其中一個 *optval* 或 *optlen* 參數指向不在使用者位址空間有效部分的記憶體。 如果 *optlen* 參數所指向的值小於 **DWORD** 值的大小，也會傳回此錯誤。<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | 封鎖的 Windows 通訊端1.1 呼叫正在進行中，或服務提供者仍在處理回呼函數。<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | 提供的引數無效。 如果 *層級* 參數未知或無效，就會傳回此錯誤。 在 Windows Vista 和更新版本上，如果通訊端處於過渡狀態，也會傳回此錯誤。<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | 指定的通訊協定系列未知或不支援此選項。 如果傳入 *s* 參數的通訊端描述項的 *類型* 參數不是 **SOCK \_ DGRAM** 或 **SOCK \_ RAW**，則會傳回此錯誤。 <br/>                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | 描述項不是通訊端。<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>備註

使用 [](/windows/desktop/api/winsock/nf-winsock-getsockopt) ipv6 \_ PKTINFO 通訊端選項呼叫的 getsockopt 函式，可讓應用程式判斷 IPV6 通訊端的 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函式是否會傳回封包資訊。

使用 [](/windows/desktop/api/winsock/nf-winsock-setsockopt) IPV6 \_ PKTINFO 通訊端選項呼叫的 setsockopt 函式可讓應用程式啟用或停用 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函式的封包資訊傳回。 \_預設會停用通訊端的 IPV6 PKTINFO 選項 (設定為 **FALSE**) 。

在 **SOCK \_ DGRAM** 或 **SOCK \_ RAW** 類型的 IPv6 通訊端上啟用這個通訊端選項時， [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函式會傳回 *WSAMSG* 參數所指向之 [**lpMsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)結構中的封包資訊。 所傳回 **WSAMSG** 結構中的其中一個控制資料物件將包含用來儲存所接收封包位址資訊的 [**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) 結構。

針對 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函式透過 IPv6 接收的資料包，所接收之 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)結構的 **控制項** 成員將包含包含 **WSACMSGHDR** 結構的 [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf)結構。 此 **WSACMSGHDR** 結構的 **cmsg \_ 層級** 成員會包含 **IPPROTO \_ ipv6**，此結構的 **cmsg \_ 類型** 成員會包含 **IPV6 \_ PKTINFO**，而 **cmsg \_ 資料** 成員會包含用來儲存所接收之 IPV6 封包位址資訊的 [**in6 \_ PKTINFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)結構。 **In6 \_ pktinfo** 結構中的 ipv6 位址是接收封包的 ipv6 位址。

對於雙重堆疊資料包通訊端，如果應用程式需要 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式以針對透過 IPv4 接收的資料包來傳回 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) 結構中的封包資訊，則必須在通訊端上將 [IP \_ PKTINFO](ip-pktinfo.md) 通訊端選項設定為 true。 如果 \_ 通訊端上的 ipv6 PKTINFO 選項設定為 true，封包資訊將會提供給透過 IPV6 接收的資料包，但可能不會提供給透過 IPv4 接收的資料包。

請注意， *Ws2ipdef .h* 標頭檔會自動包含在 *Ws2tcpip* 中，而且永遠不會直接使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Ws2ipdef (包含 Ws2tcpip) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[雙重堆疊通訊端](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[IP \_ PKTINFO](ip-pktinfo.md)
</dt> <dt>

[**IPPROTO \_ IPV6 通訊端選項**](ipproto-ipv6-socket-options.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**插座**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 

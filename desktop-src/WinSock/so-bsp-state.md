---
description: 傳回通訊端使用的本機位址、本機埠、遠端位址、遠端埠、通訊端類型和通訊協定。
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: 'SO_BSP_STATE 通訊端選項 (Ws2def) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692207"
---
# <a name="so_bsp_state-socket-option"></a>所以 \_ BSP \_ 狀態通訊端選項

**所謂的 \_ BSP \_ 狀態** 通訊端選項會傳回本機位址、本機埠、遠端位址、遠端埠、通訊端類型，以及通訊端使用的通訊協定。

若要執行這項作業，請使用下列參數呼叫 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函數。

## <a name="socket-option-value"></a>通訊端選項值

表示這個通訊端選項的常數是0x1009。

## <a name="syntax"></a>語法


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
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

要抓取值的通訊端選項。 請使用此作業的 **\_ BSP \_ 狀態** 。

</dd> <dt>

*optval* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會傳回所要求選項的值。 此參數應指向等於或大於 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構大小的緩衝區。

</dd> <dt>

*optlen* \[in、out\]
</dt> <dd>

*Optval* 緩衝區大小的指標，以位元組為單位。 此大小必須等於或大於 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 會傳回零。

如果作業失敗， \_ 則會傳回 SOCKET 錯誤的值，並藉由呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)來取出特定的錯誤碼。



| 錯誤碼                                                                                                                                              | 意義                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | 在使用此函式之前，必須先進行成功的 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 呼叫。<br/>                                                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | 網路子系統失敗。<br/>                                                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | 其中一個 *optval* 或 *optlen* 參數指向不在使用者位址空間有效部分的記憶體。 如果 *optlen* 參數所指向的值小於 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構的大小，也會傳回此錯誤。<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | 封鎖的 Windows 通訊端1.1 呼叫正在進行中，或服務提供者仍在處理回呼函數。<br/>                                                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | *層級* 參數未知或無效。<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | 指定的通訊協定系列未知或不支援此選項。<br/>                                                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | 描述項不是通訊端。<br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>備註

使用 @ **\_ BSP \_ 狀態** 通訊端選項呼叫的 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函式會抓取通訊端使用的本機位址、本機埠、遠端位址、遠端埠、通訊端類型和通訊協定。 **這樣的 \_ BSP \_ 狀態** 通訊端選項適用于 IPv6 或 IPv4 通訊端， (**af \_ INET6** 和 **af \_ INET** 位址系列) 。

如果 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函式成功，則會以 *optval* 參數所指向之緩衝區中的 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構傳回信息。 *Optlen* 所指向的整數最初應該包含這個緩衝區的大小;傳回時，它會設定為 *optval* 參數中所傳回值的長度（以位元組為單位）。

傳回之 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構中的 **iSocketType** 和 **iProtocol** 成員會填入 *s* 參數中的通訊端描述項。

如果通訊端處於連接或系結狀態，則傳回之 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構的 **LocalAddr** 成員將會設定為代表本機位址和埠的 [SOCKADDR](sockaddr-2.md)結構。 如果通訊端處於連接狀態，則傳回之 **CSADDR \_ 資訊** 結構的 **RemoteAddr** 成員將會設定為代表遠端位址和埠的 SOCKADDR 結構。

如果通訊端不是處於連接或系結狀態，則會傳回傳回之 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構的 **LocalAddr** 成員，並在 **lpSockaddr** 成員中傳回 **Null** 指標，並將 **iSockaddrLength** 成員設為零。 如果通訊端不是處於系結狀態，則傳回之 **CSADDR \_ 資訊** 結構的 **RemoteAddr** 成員會以 **lpSockaddr** 成員中的 **Null** 指標和 **iSockaddrLength** 成員設定為零的方式傳回。

如果 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函式失敗， *optval* 和 *optlen* 參數會保持不變，而且 *Optval* 參數不會指向傳回的 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構。

請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Ws2def (包含 Winsock2) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[SOCKADDR](sockaddr-2.md)
</dt> </dl>

 

 

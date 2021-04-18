---
description: 的設計目的是讓應用程式決定是否要接受接聽通訊端上的連入連線。
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: 'SO_CONDITIONAL_ACCEPT 通訊端選項 (Ws2def) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978071"
---
# <a name="so_conditional_accept-socket-option"></a>\_條件式 \_ 接受通訊端選項

「 **\_ 條件式 \_ 接受** 」通訊端選項的設計目的，是要讓應用程式決定是否要接受接聽通訊端上的連入連線。

## <a name="socket-option-value"></a>通訊端選項值

表示這個通訊端選項的常數是0x3002。

## <a name="syntax"></a>語法


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
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

要設定其值的通訊端選項。 針對此作業，請使用 **\_ 條件式 \_ 接受** 。

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
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | *層級* 參數未知或無效。 如果通訊端已處於接聽狀態，也會傳回此錯誤。<br/>                                                                                                                        |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | 指定的通訊協定系列未知或不支援此選項。<br/>                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | 描述項不是通訊端。<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>備註

以 with **\_ 條件式 \_ 接受** 通訊端選項呼叫的 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式，可讓應用程式決定是否要接受接聽通訊端上的連入連線。 預設會停用通訊端的條件式接受選項 (設定為 **FALSE**) 。

啟用此通訊端選項時，TCP 堆疊不會自動接受連接。 它會等待應用程式指出它會透過以 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函式註冊的條件式接受回呼接受連接。 一旦收到連接要求，Winsock 會叫用應用程式所註冊的條件式接受回呼。 只有當條件式接受回呼傳回 **CF \_ accept** 時，Winsock 才會通知傳輸，以完全接受連接。

當 [ **\_ 條件式 \_ 接受** 通訊端] 選項設為 [已啟用] 時 (設定為 [ **TRUE** ]) 時，會對通訊端產生數個副作用：

-   這會停用 TCP 堆疊的內建 SYN 攻擊保護防禦措施，因為應用程式現在會取得接受連線的擁有權。
-   這會有效地停用接聽待處理專案，因為不會代表接聽通訊端接受連接。 除非應用程式完全接受使用 **CF \_ 接受** 機制，否則永遠無法完全接受連接。
-   這也表示應用程式必須一律處於狀態，才能立即處理接受回呼以接受連接。 如果應用程式正在進行其他處理，用戶端可能會在應用程式實際接受連接之前停止運作。 這會導致用戶端體驗不佳。

一般而言，應用程式使用條件式接受的主要原因是檢查連線用戶端所使用的來源 IP 位址或埠，然後決定要接受或拒絕連接。 但是，如果 \_ 未啟用「條件式接受」選項， \_ 且應用程式允許 TCP 堆疊和「接聽」待處理專案如預期般運作，則應用程式可能會執行得更好。 然後，當應用程式處理已接受的連線時，如果它來自不正確的 IP 來源位址或埠，則應用程式可以直接關閉通訊端。 此行為的安全性缺點是現在用戶端已確認應用程式正在接聽 IP 位址和埠，因為它已強制關閉先前接受的連線。 不過，啟用 **\_ 條件式 \_ 接受** 的缺點通常超過這項限制。

使用「 **\_ 條件式 \_ 接受** 通訊端」選項呼叫的 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函式，可讓應用程式抓取「條件式接受」選項的目前狀態，不過這是通常不使用的功能。 如果應用程式需要在通訊端上啟用條件式接受，則 justs 會呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式來啟用此選項。

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

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 





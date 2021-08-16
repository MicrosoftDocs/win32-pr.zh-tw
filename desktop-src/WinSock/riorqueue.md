---
description: 指定傳送和接收要求與 Winsock 註冊的 i/o 擴充功能所使用的通訊端描述項。
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: 'RIO_RQ (Mswsockdef) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162b87d1ae320bfa0e74f08e5a0ef7493c053f39573249246e8b2884e74f599c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993578"
---
# <a name="rio_rq"></a>RIO \_ RQ

**RIO \_ RQ** typedef 會指定傳送和接收要求所使用的通訊端描述項，以及 Winsock 註冊的 i/o 延伸模組。


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

**RIO \_ RQ**
</dt> <dd>

一種資料類型，可指定傳送和接收要求所使用的通訊端描述項。

</dd> </dl>

## <a name="remarks"></a>備註

Winsock 註冊的 i/o 擴充功能主要是在 **RIO \_ RQ** 物件上運作，而不是通訊端。 應用程式會使用 [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)函數取得現有通訊端的 **RIO \_ RQ** 。 您必須使用 *dwFlags* 參數中所設定的 **WSA \_ 旗標 \_ RIO** 旗標來呼叫 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)函式，以建立輸入通訊端。

取得 **RIO \_ RQ** 物件之後，基礎通訊端描述項會保持有效。 應用程式可能會繼續使用基礎通訊端來設定和查詢通訊端選項、發出 IOCTLs，最後關閉通訊端。

> [!Note]  
> 基於效率的目的， ([**RIO \_ CQ**](riocqueue.md) 結構) 和要求佇列 (**RIO \_ RQ** 結構) 不會受到同步處理原始物件的保護，因此可存取完成佇列。 如果您需要從多個執行緒存取完成或要求佇列，存取應由重要區段、精簡型讀取器寫入鎖定或類似的機制進行協調。 單一線程不需要此鎖定即可進行存取。 不同的執行緒可以存取個別的要求/完成佇列，而不需要鎖定。 只有當多個執行緒嘗試存取相同的佇列時，才會發生同步處理的需求。 如果多個執行緒發出相同通訊端上的傳送和接收，則也需要同步處理，因為傳送和接收作業會使用通訊端的要求佇列。

 

[**RIO \_ RQ**](riocqueue.md) typedef 會定義在 *Mswsockdef .h* 標頭檔中，該檔案會自動包含在 *Mswsock. .h* 標頭檔中。 不應直接使用 *Mswsockdef* 標頭檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Mswsockdef (包含 Mswsock) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> <dt>

[**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 

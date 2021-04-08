---
description: 指定搭配 Winsock 註冊的 i/o 擴充功能使用的已註冊緩衝區描述元。
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: 'RIO_BUFFERID (Mswsockdef) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026499"
---
# <a name="rio_bufferid"></a>RIO \_ BUFFERID

**RIO \_ BUFFERID** typedef 會指定搭配 Winsock 註冊之 i/o 延伸模組使用的已註冊緩衝區描述元。


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**RIO \_ BUFFERID**
</dt> <dd>

資料類型，指定與傳送和接收要求搭配使用的已註冊緩衝區描述元。

</dd> </dl>

## <a name="remarks"></a>備註

Winsock 註冊的 i/o 擴充功能主要是在使用 **RIO \_ BUFFERID** 物件的已註冊緩衝區上運作。 應用程式會使用 [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))函數取得現有緩衝區的 **RIO \_ BUFFERID** 。 應用程式可以使用 [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) 函式釋放註冊。

使用 [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))函式將現有的緩衝區註冊為 **RIO \_ BUFFERID** 物件時，會從實體記憶體配置特定的內部資源，而現有的應用程式緩衝區將會鎖定到實體記憶體中。 [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)函式會被呼叫以取消註冊緩衝區、釋放這些內部資源，並允許將緩衝區解除鎖定並從實體記憶體釋放。

使用 Winsock 註冊的 i/o 擴充功能，重複註冊和解除登錄應用程式緩衝區可能會造成顯著的效能降低。 使用 Winsock 註冊的 i/o 擴充功能來設計應用程式時，應考慮下列緩衝區管理方法，以將應用程式緩衝區的重複註冊和解除登錄降至最低：

-   •最大化重複使用緩衝區。
-   •維護受限的未使用已註冊緩衝區集區，以供應用程式使用。
-   •維護受限的已註冊緩衝區集區，並在這些已註冊的緩衝區和其他未註冊的緩衝區之間執行緩衝區複製。

**RIO \_ BUFFERID** typedef 會定義在 *Mswsockdef .h* 標頭檔中，該檔案會自動包含在 *Mswsock. .h* 標頭檔中。 不應直接使用 *Mswsockdef* 標頭檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Mswsockdef (包含 Mswsock) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RIO \_ BUF**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> </dl>

 

 

---
description: 適用于通訊端關閉操作的 Winsock 網路追蹤事件。
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9068809c052638e33d45a5affadc23a289fa65ae04e6b1a71af1e40e4b508b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993748"
---
# <a name="afd_event_close-event"></a>AFD \_ 事件 \_ 關閉事件

**AFD \_ 事件 \_ CLOSE** 事件是通訊端關閉作業的 Winsock 網路追蹤事件。


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a>參數

<dl> <dt>

*EnterExit* 
</dt> <dd>

此事件的資訊。

下表列出 *EnterExit* 參數的可能值：



| 值                                                                        | 意義                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Winsock 要求的開始。<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Winsock 要求已完成。<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Winsock AFD 驅動程式採取內部動作 (中止連線，例如) 。<br/>      |
| <dl> <dt>3</dt> </dl> | TCP/IP 驅動程式導致此事件發生。 這通常表示資料通知。<br/> |
| <dl> <dt>4</dt> </dl> | Winsock AFD 驅動程式會導致此事件發生 (設定 socket 選項，例如) 。<br/> |



 

</dd> <dt>

*位置* 
</dt> <dd>

內部使用的私用欄位。

</dd> <dt>

*處理* 
</dt> <dd>

擁有相關通訊端之進程的 [EPROCESS](/windows-hardware/drivers/kernel/eprocess) 位址。 這是一個不透明的結構，可作為進程的處理常式物件。 如需詳細資訊，請參閱[EPROCESS](/windows-hardware/drivers/kernel/eprocess)結構的 Windows 驅動程式套件檔。

</dd> <dt>

*端點* 
</dt> <dd>

\_通訊端的 AFD 端點位址。

</dd> <dt>

*狀態* 
</dt> <dd>

運算的 NTSTATUS 程式碼。

</dd> </dl>

## <a name="remarks"></a>備註

**AFD \_ 事件 \_ 關閉** 事件是針對 Winsock 網路作業追蹤，以關閉通訊端。 此事件的通道是 Winsock-AFD。 此事件的層級為資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Winsock 追蹤的控制權](control-of-winsock-tracing.md)
</dt> <dt>

[**事件 \_ 描述項**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Winsock 追蹤](winsock-tracing.md)
</dt> <dt>

[Winsock 追蹤層級](winsock-tracing-levels.md)
</dt> <dt>

[Winsock 目錄變更追蹤詳細資料](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 


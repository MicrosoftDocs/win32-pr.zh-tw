---
description: 當它無法接受來自上游解碼器的動態格式變更要求時，由 VMR-7 和 VMR-9 傳送。
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: 'EC_VMR_RECONNECTION_FAILED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4dae6b2735d1ae21576591055aff9dc007f447660f5c96cf13239e5f420f81f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819958"
---
# <a name="ec_vmr_reconnection_failed"></a>EC \_ VMR 重新 \_ 連接 \_ 失敗

當它無法接受來自上游解碼器的動態格式變更要求時，由 VMR-7 和 VMR-9 傳送。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**HRESULT**) 從 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 傳回的狀態碼，而該 VMR 的輸入 pin 失敗了重新連接。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

未使用。

</dd> </dl>

## <a name="remarks"></a>備註

此事件會轉送至應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 





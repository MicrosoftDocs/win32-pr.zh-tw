---
title: 'DRV_FREE 訊息 (Mmsystem .h) '
description: 通知驅動程式正在將它從記憶體中移除。 驅動程式應該釋放任何已配置的記憶體和其他系統資源。
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a558dc7a2c3ece040790b2351ff39dc3054d660eb9368567ed7ce79d40c8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526208"
---
# <a name="drv_free-message"></a>WINSPOOL.DRV \_ 可用訊息

通知驅動程式正在將它從記憶體中移除。 驅動程式應該釋放任何已配置的記憶體和其他系統資源。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

可安裝的驅動程式實例的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

不會使用 *dwDriverId*、 *lParam1* 和 *lParam2* 參數。

**Winspool.drv \_ FREE** 訊息一律是設備磁碟機收到的最後一則訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[可安裝的驅動程式](installable-drivers.md)
</dt> <dt>

[可安裝的驅動程式訊息](installable-driver-messages.md)
</dt> </dl>

 

 






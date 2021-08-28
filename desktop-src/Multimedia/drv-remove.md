---
title: 'DRV_REMOVE 訊息 (Mmsystem .h) '
description: 通知驅動程式即將從系統中移除。 當驅動程式收到此訊息時，應移除它在登錄中建立的任何區段。
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- DRV_REMOVE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c08302d69e934ec77908b247f3c8f6368de8de4eab36809b6102b74858adde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496418"
---
# <a name="drv_remove-message"></a>WINSPOOL.DRV \_ 移除訊息

通知驅動程式即將從系統中移除。 當驅動程式收到此訊息時，應移除它在登錄中建立的任何區段。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

可安裝驅動程式的識別碼。 這與先前 [**Winspool.drv \_ 開啟**](drv-open.md) 訊息中的驅動程式所傳回的值相同。

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

可安裝的驅動程式實例的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

不會使用 *lParam1* 和 *lParam2* 參數。

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

 

 






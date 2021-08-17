---
title: 'DRV_DISABLE 訊息 (Mmsystem .h) '
description: 停用驅動程式。 驅動程式應該將對應的裝置（如果有的話）置於非使用中狀態，並終止任何回呼函式或執行緒。
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d9c5a99414f0b755efbae005365d89665a2b2bc5a4673436101066ec740564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144411"
---
# <a name="drv_disable-message"></a>WINSPOOL.DRV \_ 停用訊息

停用驅動程式。 驅動程式應該將對應的裝置（如果有的話）置於非使用中狀態，並終止任何回呼函式或執行緒。

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

停用驅動程式之後，系統通常會在從記憶體移除驅動程式之前，先傳送 [**winspool.drv 的 \_ 可用**](drv-free.md) 訊息給驅動程式。

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

 

 






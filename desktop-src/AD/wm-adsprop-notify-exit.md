---
title: 'WM_ADSPROP_NOTIFY_EXIT 訊息 (Adsprop .h) '
description: 當不再需要通知物件時，Active Directory 的屬性工作表延伸會將 WM \_ ADSPROP \_ 通知結束訊息傳送 \_ 給通知物件。
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_EXIT 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934920"
---
# <a name="wm_adsprop_notify_exit-message"></a>WM \_ ADSPROP \_ 通知結束 \_ 訊息

當不再需要通知物件時，Active Directory 的屬性工作表延伸會將 **WM \_ ADSPROP \_ 通知 \_** 結束訊息傳送給通知物件。


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

通知物件的控制碼。 若要取得此控制碼，請呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)。

</dd> <dt>

*wParam* 
</dt> <dd>

未使用。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

通知物件將會自行刪除以回應此訊息。 傳送此訊息時，應該將通知物件控制碼視為無效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Adsprop。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Active Directory Domain Services 中的訊息](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 






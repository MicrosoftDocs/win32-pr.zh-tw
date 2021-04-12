---
title: 'WM_ADSPROP_NOTIFY_PAGEHWND 訊息 (Adsprop .h) '
description: Active Directory Directory 服務屬性工作表延伸模組會呼叫 ADsPropSetHwnd，以通知屬性頁面視窗控制碼的通知物件。
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEHWND 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105617"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>WM \_ ADSPROP \_ 通知 \_ PAGEHWND 訊息

Active Directory Directory 服務屬性工作表延伸模組會呼叫 [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) ，以通知屬性頁面視窗控制碼的通知物件。 **ADsPropSetHwnd** 函式會將 **WM \_ ADSPROP \_ 通知 \_ PAGEHWND** 訊息傳送至通知物件，此物件會通知屬性頁面視窗控制碼的通知物件。


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a>參數

<dl> <dt>

*hNotifyObj* 
</dt> <dd>

通知物件的控制碼。 若要取得此控制碼，請呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)。

</dd> <dt>

*hPage* 
</dt> <dd>

屬性頁的視窗控制碼。

</dd> <dt>

*ptzTitle* 
</dt> <dd>

以 Null 終止的 **WCHAR** 緩衝區指標，其中包含屬性頁的標題。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

Active Directory 的屬性工作表延伸模組通常會在處理 [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)訊息時呼叫 [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Adsprop。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Active Directory Domain Services 中的訊息](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 


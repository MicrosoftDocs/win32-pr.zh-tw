---
title: 'WM_ADSPROP_NOTIFY_APPLY 訊息 (Adsprop .h) '
description: '\_ \_ \_ 如果屬性頁 PSN 套用 \_ 處理常式成功，則 Active Directory Directory 服務屬性工作表延伸會將 WM ADSPROP 通知套用訊息傳送至通知物件。'
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_APPLY 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967560"
---
# <a name="wm_adsprop_notify_apply-message"></a>WM \_ ADSPROP \_ 通知套用 \_ 訊息

如果屬性頁 PSN 套用處理程式成功，則 Active Directory Directory 服務屬性工作表延伸會將 **WM \_ ADSPROP \_ 通知 \_** 套用訊息傳送至通知物件 \_ 。


```C++
WM_ADSPROP_NOTIFY_APPLY

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

將頁面新增至 Active Directory Manager MMC 嵌入式管理單元時，Active Directory MMC 屬性工作表會透過呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) 函式來建立通知物件，然後將通知物件控制碼傳遞至每個屬性頁。

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

 

 






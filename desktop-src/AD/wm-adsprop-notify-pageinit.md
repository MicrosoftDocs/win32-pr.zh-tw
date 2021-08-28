---
title: 'WM_ADSPROP_NOTIFY_PAGEINIT 訊息 (Adsprop .h) '
description: Active Directory 屬性工作表延伸模組會呼叫 ADsPropGetInitInfo，以取得有關屬性工作表延伸適用之目錄物件的相關資料。
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEINIT 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcad6ed359edf195b2355920b08d6010597f33dbc0f4e3b1e4c2438c3841ca47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024206"
---
# <a name="wm_adsprop_notify_pageinit-message"></a>WM \_ ADSPROP \_ 通知 \_ PAGEINIT 訊息

Active Directory 屬性工作表延伸模組會呼叫 [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) ，以取得有關屬性工作表延伸適用之目錄物件的相關資料。 **ADsPropGetInitInfo** 函式會將 **WM \_ ADSPROP \_ 通知 \_ PAGEINIT** 訊息傳送至通知物件，以達成此結果。


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

通知物件的控制碼。 這是呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)所取得的 *hNotifyObject* 參數。

</dd> <dt>

*wParam* 
</dt> <dd>

未使用。

</dd> <dt>

*pADsPropInitParams* 
</dt> <dd>

接收目錄物件資訊之 [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) 結構的指標。 這是傳遞至 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)的 *pInitParams* 參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

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

[**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 






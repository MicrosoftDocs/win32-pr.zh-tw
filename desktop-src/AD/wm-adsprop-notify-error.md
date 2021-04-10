---
title: 'WM_ADSPROP_NOTIFY_ERROR 訊息 (Adsprop .h) '
description: WM \_ ADSPROP \_ 通知 \_ 錯誤訊息會將錯誤訊息加入至透過呼叫 ADsPropShowErrorDialog 函式所顯示的錯誤訊息清單。
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_ERROR 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103793"
---
# <a name="wm_adsprop_notify_error-message"></a>WM \_ ADSPROP \_ 通知 \_ 錯誤訊息

**WM \_ ADSPROP \_ 通知 \_ 錯誤** 訊息會將錯誤訊息加入至透過呼叫 [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)函式所顯示的錯誤訊息清單。


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

通知物件的控制碼。 這是 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)所取得的 *hNotifyObject* 參數。

</dd> <dt>

*wParam* 
</dt> <dd>

未使用。

</dd> <dt>

*lParam* 
</dt> <dd>

[**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)結構的指標，其中包含錯誤訊息資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

[**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)函數是傳送此訊息的慣用方法。

在呼叫 [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)之前，會累積由 **WM \_ ADSPROP \_ 通知 \_ 錯誤** 訊息所新增的錯誤訊息。 **ADsPropShowErrorDialog** 會結合並顯示累積的錯誤訊息。 當錯誤對話方塊關閉時，會刪除累積的錯誤訊息。

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

[**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 






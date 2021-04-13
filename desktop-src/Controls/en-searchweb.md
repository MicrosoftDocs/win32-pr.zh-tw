---
title: 'EN_SEARCHWEB (CommCtrl 的通知碼) '
description: 當編輯控制項失去鍵盤焦點時傳送。 編輯控制項的父視窗會透過 WM 通知訊息接收此通知碼 \_ 。
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464421"
---
# <a name="en_searchweb-notification-code"></a>EN \_ SEARCHWEB 通知碼

當 [搜尋 web] 功能啟用時，在編輯控制項執行 web 搜尋之後傳送，請參閱 [EM_ENABLESEARCHWEB](em-enablesearchweb.md)。 編輯控制項的父視窗會透過 [**WM \_ 通知**](wm-notify.md) 訊息接收此通知碼。


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

編輯控制項的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb)結構的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限 1809 desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2019 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ 通知**](wm-notify.md)
</dt> </dl>

 

 






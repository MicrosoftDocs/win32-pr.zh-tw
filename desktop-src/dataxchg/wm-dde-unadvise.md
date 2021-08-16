---
title: 'WM_DDE_UNADVISE 訊息 (的) '
description: 動態資料交換 (dde) 用戶端應用程式張貼一個 WM \_ dde \_ UNADVISE 訊息，通知 DDE 伺服器應用程式，該專案的指定專案或特定剪貼簿格式不應再更新。
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE 訊息資料 Exchange
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bbd0ac8e056cc43be764e745f824b50fc90b3cb2f0c50c9061d111fb3bc178d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915102"
---
# <a name="wm_dde_unadvise-message"></a>WM \_ DDE \_ UNADVISE 訊息

動態資料交換 (dde) 用戶端應用程式張貼一個 **WM \_ dde \_ UNADVISE** 訊息，通知 DDE 伺服器應用程式，該專案的指定專案或特定剪貼簿格式不應再更新。 這會終止指定專案的暖或經常性存取資料連結。

若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

傳送訊息之用戶端視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字組指定要撤銷更新要求之專案的剪貼簿格式。 如果這是 **Null**，就會終止專案的所有作用中 [**WM \_ DDE \_ 通知**](wm-dde-advise.md) 交談。

高序位單字包含全域 atom，可識別正在撤銷更新要求的專案。 如果這是 **Null**，就會終止與交談相關聯的所有作用中 [**WM \_ DDE \_ 通知**](wm-dde-advise.md) 連結。

</dd> </dl>

## <a name="remarks"></a>備註

用戶端應用程式會呼叫 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)函式，以配置 *lParam* 的高序位字組。

伺服器應用程式會張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。 張貼 **WM \_ DDE DDE \_ ACK** 時，伺服器可以重複使用 atom，也可以刪除 atom 並建立新的 atom。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>Dde. h (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**WM \_ DDE \_ 建議**](wm-dde-advise.md)
</dt> <dt>

**概念**
</dt> <dt>

[關於動態資料交換](about-dynamic-data-exchange.md)
</dt> </dl>

 


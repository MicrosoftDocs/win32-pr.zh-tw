---
title: 'MCIWNDM_SETINACTIVETIMER 訊息 (Vfw .h) '
description: MCIWNDM \_ SETINACTIVETIMER 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新在視窗標題列中顯示的位置資訊，以及在 MCIWnd 視窗處於非使用中狀態時將通知訊息傳送至父視窗的更新期間。 您可以使用 MCIWndSetInactiveTimer 宏明確地傳送此訊息。
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508891"
---
# <a name="mciwndm_setinactivetimer-message"></a>MCIWNDM \_ SETINACTIVETIMER 訊息

**MCIWNDM \_ SETINACTIVETIMER** 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新在視窗標題列中顯示的位置資訊，以及在 MCIWnd 視窗處於非使用中狀態時將通知訊息傳送至父視窗的更新期間。 您可以使用 [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) 宏明確地傳送此訊息。


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*無效*
</dt> <dd>

更新期間（以毫秒為單位）。 預設值為2000毫秒。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 






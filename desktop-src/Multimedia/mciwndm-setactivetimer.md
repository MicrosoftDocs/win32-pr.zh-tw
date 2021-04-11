---
title: 'MCIWNDM_SETACTIVETIMER 訊息 (Vfw .h) '
description: MCIWNDM \_ SETACTIVETIMER 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新在視窗標題列中顯示的位置資訊，以及在 MCIWnd 視窗為使用中時將通知訊息傳送至父視窗的更新期間。 您可以使用 MCIWndSetActiveTimer 宏明確地傳送此訊息。
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- MCIWNDM_SETACTIVETIMER message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104712"
---
# <a name="mciwndm_setactivetimer-message"></a>MCIWNDM \_ SETACTIVETIMER 訊息

**MCIWNDM \_ SETACTIVETIMER** 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新在視窗標題列中顯示的位置資訊，以及在 MCIWnd 視窗為使用中時將通知訊息傳送至父視窗的更新期間。 您可以使用 [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) 宏明確地傳送此訊息。


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*積極*
</dt> <dd>

更新期間（以毫秒為單位）。 預設值為500毫秒。

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

[**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 






---
title: 'MCIWNDM_SETTIMERS 訊息 (Vfw .h) '
description: MCIWNDM \_ SETTIMERS 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新顯示在視窗標題列中的位置資訊，以及將通知訊息傳送至父視窗的更新期間。
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9c17a131827459555ae51adc5d5bd48d98fabb88fc4c1f0dbbcd1eb3673466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807551"
---
# <a name="mciwndm_settimers-message"></a>MCIWNDM \_ SETTIMERS 訊息

**MCIWNDM \_ SETTIMERS** 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新顯示在視窗標題列中的位置資訊，以及將通知訊息傳送至父視窗的更新期間。 您可以使用 [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) 宏明確地傳送此訊息。


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*積極*
</dt> <dd>

當 MCIWnd 為使用中視窗時，所使用的更新期間。 預設值為500毫秒。 此值的儲存體限制為16位。

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*無效*
</dt> <dd>

MCIWnd 在非作用中視窗時所使用的更新期間。 預設值為2000毫秒。 此值的儲存體限制為16位。

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

[**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 






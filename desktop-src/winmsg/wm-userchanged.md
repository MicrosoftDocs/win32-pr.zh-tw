---
description: 在使用者登入或登出之後傳送到所有視窗。 當使用者登入時，系統會更新使用者特定的設定。 系統會在更新設定之後立即傳送此訊息。
title: 'WM_USERCHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bb466e80070fe1be5cd7af7889fc5727c81f8caad89ad60c48c7a105b688fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705698"
---
# <a name="wm_userchanged-message"></a>WM \_ USERCHANGED 訊息

在使用者登入或登出之後傳送到所有視窗。 當使用者登入時，系統會更新使用者特定的設定。 系統會在更新設定之後立即傳送此訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

> [!Note]  
> Windows Vista 不支援此訊息。

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows概述](windows.md)
</dt> </dl>

 

 

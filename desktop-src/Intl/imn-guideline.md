---
description: 當 IME 即將顯示錯誤訊息或其他資訊時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: 'IMN_GUIDELINE 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8bbcce8c1e7a04f4474d09f221ff2e2644e84b49d98edf09c1137604b71b226
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107098"
---
# <a name="imn_guideline-notification-code"></a>IMN \_ 指導方針碼

當 IME 即將顯示錯誤訊息或其他資訊時，通知應用程式。 應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMN \_ 指導方針。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此命令沒有傳回值。

## <a name="remarks"></a>備註

應用程式會藉由呼叫 [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) 函式來取得錯誤訊息或 IME 中的資訊來處理此命令。

IME 視窗會在資訊視窗中顯示錯誤訊息或資訊字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>Imm (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員命令](input-method-manager-commands.md)
</dt> <dt>

[**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[**WM \_ 輸入法 \_ 通知**](wm-ime-notify.md)
</dt> </dl>

 

 





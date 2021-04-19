---
description: 當選取的輸入法需要組合字元串中字元座標的相關資訊時，就會通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 要求訊息接收此命令， \_ 如下所示。
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: 'IMR_QUERYCHARPOSITION 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988780"
---
# <a name="imr_querycharposition-notification-code"></a>IMR \_ QUERYCHARPOSITION 通知碼

當選取的輸入法需要組合字元串中字元座標的相關資訊時，就會通知應用程式。 應用程式會透過包含參數設定的 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，如下所示。


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMR \_ QUERYCHARPOSITION。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition)結構的指標，其中包含字元在組合視窗中的位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式填滿 [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) 結構，則傳回非零值。 否則，此命令會傳回0。

## <a name="remarks"></a>備註

繪製組合字元串本身的應用程式（而不是依賴 IME）必須負責填入 [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) 結構的所有成員。 否則，應用程式應該將命令傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 或 [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) （如果它有自己的輸入法使用者介面視窗）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>Imm (包括 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員命令](input-method-manager-commands.md)
</dt> <dt>

[**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[**WM \_ IME \_ 要求**](wm-ime-request.md)
</dt> </dl>

 

 

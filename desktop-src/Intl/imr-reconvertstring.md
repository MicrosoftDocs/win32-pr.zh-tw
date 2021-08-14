---
description: 當選取的輸入法需要字串進行漢字重漢字時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 要求訊息接收此命令， \_ 如下所示。
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: 'IMR_RECONVERTSTRING 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dfc2b188a2873af3ec7004ffaac65a3cce0b4257c1428dfe4abfcba9d2b2aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948755"
---
# <a name="imr_reconvertstring-notification-code"></a>IMR \_ RECONVERTSTRING 通知碼

當選取的輸入法需要字串進行漢字重漢字時，通知應用程式。 應用程式會透過包含參數設定的 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，如下所示。


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMR \_ RECONVERTSTRING。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

包含 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構和字串的緩衝區指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回目前的漢字重組字串結構。 如果 *lParam* 設定為 **Null**，則應用程式會傳回保存結構所需的緩衝區大小。 如果不成功，此命令會傳回0。

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

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**WM \_ IME \_ 要求**](wm-ime-request.md)
</dt> </dl>

 

 





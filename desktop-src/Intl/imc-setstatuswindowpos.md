---
description: 指示 IME 視窗設定狀態視窗的位置。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配參數設定，如下所示。
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: 'IMC_SETSTATUSWINDOWPOS 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026293"
---
# <a name="imc_setstatuswindowpos-command"></a>IMC \_ SETSTATUSWINDOWPOS 命令

指示 IME 視窗設定狀態視窗的位置。 若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配參數設定，如下所示。


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMC \_ SETSTATUSWINDOWPOS。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**點**](/previous-versions//dd162808(v=vs.85))結構的指標，其中包含狀態視窗位置的 x 座標和 y 座標。 座標是在螢幕座標中，相對於顯示的左上角。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回0，否則傳回非零值。

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

[**WM \_ IME \_ 控制項**](wm-ime-control.md)
</dt> </dl>

 

 

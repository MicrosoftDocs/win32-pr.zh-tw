---
description: 指示 IME 視窗顯示狀態視窗。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: 'IMC_OPENSTATUSWINDOW 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd0b5e19ef6a026459eedb050e9ac9587b5ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848194"
---
# <a name="imc_openstatuswindow-command"></a>IMC \_ OPENSTATUSWINDOW 命令

指示 IME 視窗顯示狀態視窗。 若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMC \_ OPENSTATUSWINDOW。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回0，否則傳回非零值。

## <a name="remarks"></a>備註

如果作業系統不是顯示輸入法狀態模式，則會忽略這個命令。 使用者可以從工作列設定或清除 [顯示輸入法狀態模式]。

如果已顯示 [狀態] 視窗，此命令不會執行任何動作。 雖然應用程式可以將此命令傳送至 IME 視窗，但應用程式不會收到對應的 [**IMN \_ OPENSTATUSWINDOW**](imn-openstatuswindow.md) 命令。

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

 

 





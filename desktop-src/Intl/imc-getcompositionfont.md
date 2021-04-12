---
description: 指示 IME 視窗取出用來在組合視窗中顯示中繼字元的邏輯字型。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: 'IMC_GETCOMPOSITIONFONT 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191506"
---
# <a name="imc_getcompositionfont-command"></a>IMC \_ GETCOMPOSITIONFONT 命令

指示 IME 視窗取出用來在組合視窗中顯示中繼字元的邏輯字型。 若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMC \_ GETCOMPOSITIONFONT。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標，此結構會接收邏輯字型的相關資訊。

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
</dt> </dl>

 

 

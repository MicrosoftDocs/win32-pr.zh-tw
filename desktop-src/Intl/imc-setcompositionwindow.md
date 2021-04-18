---
description: 指示 IME 視窗設定組合視窗的樣式。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: 'IMC_SETCOMPOSITIONWINDOW 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971254"
---
# <a name="imc_setcompositionwindow-command"></a>IMC \_ SETCOMPOSITIONWINDOW 命令

指示 IME 視窗設定組合視窗的樣式。 若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMC \_ SETCOMPOSITIONWINDOW。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)結構的指標，其中包含樣式資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回0，否則傳回非零值。

## <a name="remarks"></a>備註

此命令會在目前的輸入內容中設定樣式，並接著將樣式套用到每個接收該輸入內容的輸入法視窗。

根據預設，IME 視窗具有 CFS \_ 點樣式。 使用此樣式時，IME 視窗會在開啟任何撰寫視窗時使用目前的插入號位置和視窗工作區。

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

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**WM \_ IME \_ 控制項**](wm-ime-control.md)
</dt> </dl>

 

 





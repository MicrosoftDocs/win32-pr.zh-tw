---
description: 指示 IME 視窗設定候選視窗的位置。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: 'IMC_SETCANDIDATEPOS 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690851"
---
# <a name="imc_setcandidatepos-command"></a>IMC \_ SETCANDIDATEPOS 命令

指示 IME 視窗設定候選視窗的位置。 若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMC \_ SETCANDIDATEPOS。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)結構的指標，其中包含候選視窗的 x 座標和 y 座標。 應用程式應該設定此結構的 **dwIndex** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回0，否則傳回非零值。

## <a name="remarks"></a>備註

此命令適用于單獨顯示撰寫字元的應用程式，但使用 IME 視窗顯示候選項目。

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

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**WM \_ IME \_ 控制項**](wm-ime-control.md)
</dt> </dl>

 

 





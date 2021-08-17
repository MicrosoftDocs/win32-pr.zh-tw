---
description: 當 IME 需要變更 RECONVERTSTRING 結構時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 要求訊息接收此命令， \_ 如下所示。
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: 'IMR_CONFIRMRECONVERTSTRING 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a0fd1c38c7552d09489c51b9acc897f679aa3a218e86bbba222225fcff57e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948795"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>IMR \_ CONFIRMRECONVERTSTRING 通知碼

當 IME 需要變更 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構時，通知應用程式。 應用程式會透過包含參數設定的 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，如下所示。


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMR \_ CONFIRMRECONVERTSTRING。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

輸入法中 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構的指標。 如需詳細資訊，請參閱＜備註＞一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式接受已變更的 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構，則傳回非零值。 否則，此命令會傳回0，且 IME 會使用原始的 **RECONVERTSTRING** 結構。

## <a name="remarks"></a>備註

應用程式會在收到 [IMR \_ RECONVERTSTRING](imr-reconvertstring.md)命令時填入 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)結構。

在應用程式處理 [IMR \_ RECONVERTSTRING](imr-reconvertstring.md)之後，IME 可能會或可能不會調整 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構。 IME 傳送 WM \_ ime \_ 要求與 **IMR \_ CONFIRMRECONVERTSTRING** ，以確認 **RECONVERTSTRING** 結構的變更。 如果應用程式針對 **IMR \_ CONFIRMRECONVERTSTRING** 傳回 **TRUE** ，則 IME 會根據 **IMR \_ CONFIRMRECONVERTSTRING** 命令的 **RECONVERTSTRING** 結構來產生新的組合字元串。 如果應用程式針對 **IMR \_ CONFIRMRECONVERTSTRING** 傳回 **FALSE** ，則 IME 會根據 IMR RECONVERTSTRING 命令中的應用程式所指定的原始 **RECONVERTSTRING** 結構，產生新的組合字元串 \_ 。

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

[IMR \_ RECONVERTSTRING](imr-reconvertstring.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**WM \_ IME \_ 要求**](wm-ime-request.md)
</dt> </dl>

 

 





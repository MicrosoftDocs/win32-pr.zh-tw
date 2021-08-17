---
description: 當 IME 即將開啟候選視窗時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: 'IMN_OPENCANDIDATE 事件 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf6db7415a62b6d77925a4fb7106b70f0b42d77f922e0c1b6df76e71d10c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147631"
---
# <a name="imn_opencandidate-event"></a>IMN \_ OPENCANDIDATE 事件

當 IME 即將開啟候選視窗時，通知應用程式。 應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMN \_ OPENCANDIDATE。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

候選清單旗標。 每個位都對應至候選清單： bit 0 到第一個清單，第1個到第二個，依此類推。 如果指定的位為1，則會開啟對應的候選視窗。

</dd> </dl>

## <a name="return-value"></a>傳回值

此命令沒有傳回值。

## <a name="remarks"></a>備註

如果應用程式顯示候選項本身，就應該處理這個命令。 應用程式可以使用 [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) 函式來取得要顯示的候選清單。

根據預設，IME 視窗在處理此命令時，會建立候選視窗。

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

[**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**WM \_ 輸入法 \_ 通知**](wm-ime-notify.md)
</dt> </dl>

 

 





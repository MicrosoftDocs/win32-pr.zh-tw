---
description: 當輸入內容的開啟狀態更新時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: 'IMN_SETOPENSTATUS 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57797210f9c0595a952315ca75858890b1998fe16e49049b3a22fb8ed72a5aea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107038"
---
# <a name="imn_setopenstatus-notification-code"></a>IMN \_ SETOPENSTATUS 通知碼

當輸入內容的開啟狀態更新時，通知應用程式。 應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMN \_ SETOPENSTATUS。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此命令沒有傳回值。

## <a name="remarks"></a>備註

應用程式可以使用 [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) 函數來取得開啟狀態的相關資訊。

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

[**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[**WM \_ 輸入法 \_ 通知**](wm-ime-notify.md)
</dt> </dl>

 

 





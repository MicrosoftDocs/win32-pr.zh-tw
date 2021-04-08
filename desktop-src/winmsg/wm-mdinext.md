---
description: 應用程式會將 WM \_ MDINEXT 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以啟動下一個或上一個子視窗。
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: 'WM_MDINEXT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690280"
---
# <a name="wm_mdinext-message"></a>WM \_ MDINEXT 訊息

應用程式會將 **WM \_ MDINEXT** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以啟動下一個或上一個子視窗。


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

MDI 子視窗的控制碼。 系統會根據 *lParam* 參數的值，啟動緊接在指定子視窗之前或之後的子視窗。 如果 *wParam* 參數為 **Null**，系統會啟動緊接在目前作用中子視窗之前或之後的子視窗。

</dd> <dt>

*lParam* 
</dt> <dd>

如果此參數為零，則系統會啟用下一個 MDI 子視窗，並將 *wParam* 參數所識別的子視窗放在所有其他子視窗後方。 如果此參數為非零值，則系統會啟動先前的子視窗，並將它放在 *wParam* 所識別的子視窗前方。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **零**

傳回值永遠是零。

## <a name="remarks"></a>備註

如果 MDI 用戶端視窗在使用中的 MDI 子視窗最大化時，收到變更其子視窗啟動的任何訊息，系統就會還原使用中的子視窗，並將新啟動的子視窗最大化。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ MDIACTI加值稅E**](wm-mdiactivate.md)
</dt> <dt>

[**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 





---
description: 應用程式會將 WM \_ MDICREATE 訊息傳送至多重文件介面， (mdi) 用戶端視窗來建立 mdi 子視窗。
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: 'WM_MDICREATE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c69a894ebd2e55bb74486e26cd118366b1e533a490cc50feb5f77aad64c6be3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056008"
---
# <a name="wm_mdicreate-message"></a>WM \_ MDICREATE 訊息

應用程式會將 **WM \_ MDICREATE** 訊息傳送至多重文件介面， (mdi) 用戶端視窗來建立 mdi 子視窗。


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)結構的指標，其中包含系統用來建立 MDI 子視窗的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HWND**

如果訊息成功，傳回值就是新子視窗的控制碼。

如果訊息失敗，則傳回值為 **Null**。

## <a name="remarks"></a>備註

MDI 子視窗會以 [**視窗樣式**](window-styles.md) 的 **ws \_ child**、 **ws \_ CLIPSIBLINGS**、 **ws \_ CLIPCHILDREN**、 **Ws \_ SYSMENU**、 **ws \_ CAPTION**、 **ws \_ THICKFRAME**、 **ws \_ MINIMIZEBOX** 和 **ws \_ MAXIMIZEBOX** 來建立，再加上 [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) 結構中指定的其他樣式位。 系統會將新子視窗的標題新增至框架視窗的 [視窗] 功能表。 應用程式應該使用此訊息來建立用戶端視窗的所有子視窗。

如果 MDI 用戶端視窗收到任何訊息，而該訊息會在作用中的子視窗最大化時變更其子視窗的啟用，系統會還原使用中的子視窗，並將新啟用的子視窗最大化。

建立 MDI 子視窗時，系統會將 [**WM \_ 建立**](wm-create.md) 訊息傳送至視窗。 **WM \_ 建立** 訊息的 *lParam* 參數包含 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構的指標。 此結構的 *lpCreateParams* 成員包含 [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) 結構的指標，該結構會與建立 MDI 子視窗的 **WM \_ MDICREATE** 訊息一起傳遞。

當您仍在處理 **wm \_ MDICREATE** 訊息時，應用程式不應該傳送第二個 **wm \_ MDICREATE** 訊息。 例如，在 MDI 子視窗處理其 **wm \_ MDICREATE** 訊息時，它不應該傳送 **wm \_ MDICREATE** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[**WM \_ 建立**](wm-create.md)
</dt> <dt>

[**WM \_ MDIDESTROY**](wm-mdidestroy.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 

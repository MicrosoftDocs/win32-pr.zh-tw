---
title: 'WM_CHOOSEFONT_SETFLAGS 訊息 (Commdlg .h) '
description: 應用程式會將 WM \_ CHOOSEFONT \_ SETFLAGS 訊息傳送至 [字型] 對話方塊，以設定對話方塊的顯示選項。
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- WM_CHOOSEFONT_SETFLAGS 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d77290dfb3668e24d3586cf6d742b524e05fb07979de7c8d45f39998aca9708
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726078"
---
# <a name="wm_choosefont_setflags-message"></a>WM \_ CHOOSEFONT \_ SETFLAGS 訊息

應用程式會將 **WM \_ CHOOSEFONT \_ SETFLAGS** 訊息傳送至 [ **字型** ] 對話方塊，以設定對話方塊的顯示選項。


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的指標，其中包含 **旗標** 成員中的新設定。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式會建立 [**字型**] 對話方塊，並使用 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構來指定 **旗標** 成員的初始值。 使用 **WM \_ CHOOSEFONT \_ SETFLAGS** 訊息，在 [**字型**] 對話方塊開啟時，為 **旗標** 成員指定不同的值。

一般來說，您應該從 [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)攔截程式傳送 **WM \_ CHOOSEFONT \_ SETFLAGS** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

 


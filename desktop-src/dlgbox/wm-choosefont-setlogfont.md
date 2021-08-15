---
title: 'WM_CHOOSEFONT_SETLOGFONT 訊息 (Commdlg .h) '
description: 應用程式會將 WM \_ CHOOSEFONT \_ SETLOGFONT 訊息傳送至 [字型] 對話方塊，以設定目前的邏輯字型資訊。
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- WM_CHOOSEFONT_SETLOGFONT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d35c6f54679389b411417e5539382fd322c0873e6dba87fc90efb93b8be7ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503421"
---
# <a name="wm_choosefont_setlogfont-message"></a>WM \_ CHOOSEFONT \_ SETLOGFONT 訊息

應用程式會將 **WM \_ CHOOSEFONT \_ SETLOGFONT** 訊息傳送至 [ **字型** ] 對話方塊，以設定目前的邏輯字型資訊。


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標，其中包含目前邏輯字型的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

當您呼叫 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式來建立 [**字型**] 對話方塊時，可以使用 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **lpLogFont** 成員來指定包含對話方塊初始值的 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構。 在 [**字型**] 對話方塊開啟時，使用 **WM \_ CHOOSEFONT \_ SETLOGFONT** 訊息來指定具有不同值的 **LOGFONT** 結構。

一般來說，您會從 [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)攔截程式傳送 **WM \_ CHOOSEFONT \_ SETLOGFONT** 訊息。 攔截程式也可以傳送 [**wm \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) 和 [**wm \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) 訊息。

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

[**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 


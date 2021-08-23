---
title: 'SETRGBSTRING message (Commdlg) '
description: '[色彩] 對話方塊（CCHookProc）的 [攔截程式] 可以將已註冊的 SETRGBSTRING 訊息傳送至對話方塊，以設定目前的色彩選取範圍。'
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- SETRGBSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8322bb07300ce188684f5097232563e80721fadf0f614c24ac5f7b2d034c1fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985308"
---
# <a name="setrgbstring-message"></a>SETRGBSTRING 訊息

[ **色彩** ] 對話方塊（ [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)）的 [攔截程式] 可以將已註冊的 **SETRGBSTRING** 訊息傳送至對話方塊，以設定目前的色彩選取範圍。


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

要在 [ **色彩** ] 對話方塊中選取之色彩的 RGB 值。 您可以使用 [**rgb**](/windows/desktop/api/wingdi/nf-wingdi-rgb) 宏來指定 rgb 色彩值的紅色、綠色和藍色濃度。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

如果 *lParam* 符合其中一個基本色彩或16個自訂色彩之一，則對話方塊程式會選取該色彩。 對話方塊程式也會更新 [ **色彩** ] 對話方塊之 [自訂色彩] 延伸中的所有控制項（如果已開啟）。

如果 *lParam* 不符合基本或自訂色彩，則對話方塊程式不會變更目前的色彩選取範圍，但會更新自訂色彩控制項（如果看得到的話）。

## <a name="examples"></a>範例

下列範例程式碼會取得 **SETRGBSTRING** 訊息識別碼，然後將色彩選取範圍設定為藍色。


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **SETRGBSTRINGW** (Unicode) 和 **SETRGBSTRINGA** (ANSI) <br/>                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

 


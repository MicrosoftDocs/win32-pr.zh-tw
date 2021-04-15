---
title: 'WM_GETTITLEBARINFOEX 訊息 (Winuser .h) '
description: 傳送至要求延伸的標題列資訊。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384138"
---
# <a name="wm_gettitlebarinfoex-message"></a>WM \_ GETTITLEBARINFOEX 訊息

傳送至要求延伸的標題列資訊。 視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為0。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex)結構的指標。 訊息寄件者負責為此結構配置記憶體。 將此結構的 **cbSize** 成員設定為， `sizeof(TITLEBARINFOEX)` 然後才傳遞此結構與訊息。

</dd> </dl>

## <a name="remarks"></a>備註

下列範例會顯示訊息接收者如何轉換 **LPARAM** 值，以抓取 [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) 結構。

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[功能表總覽](menus.md)
</dt> </dl>

 

